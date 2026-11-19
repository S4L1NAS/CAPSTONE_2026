# Informe preliminar de auditoría y pruebas — Fase 3

**Proyecto:** Sistema de Obras, Mantención y Mejoras (OMM), Hotel & Centro de Eventos El Almendro  
**Equipo:** BPB  
**Fecha de corte de la auditoría:** 17-11-2026  
**Origen de evidencia:** informe de auditoría de solo lectura realizado por Codex, entregado por el equipo; no constituye una ejecución nueva de pruebas al publicarse este documento.  
**Estado:** preliminar, pendiente de revisión y aprobación del equipo.

## 1. Alcance

El sistema inspeccionado comprende acceso y sesiones, administración, solicitudes, mantenciones, inventario, tareas, trabajadores, documentación y módulos complementarios de obras y planificación. No hay evidencia en esta auditoría para describirlo como sistema de reservas hoteleras, huéspedes o facturación.

Este informe registra **resultados reportados por la auditoría**, no resultados ejecutados por este repositorio académico.

## 2. Verificaciones ejecutadas por Codex durante la auditoría

| ID | Verificación | Resultado informado | Alcance / limitación |
|---|---|---|---|
| AUD-01 | Correspondencia código local vs. GitHub | 200/200 archivos idénticos | Coincidencia de archivos; no demuestra comportamiento |
| AUD-02 | Frontend público vs. raíz local | 55/55 archivos idénticos | HTTP/archivos estáticos; no comprueba sesiones ni backend |
| AUD-03 | Sintaxis JS/MJS/CJS | 159/159 correctos | Análisis sintáctico, no prueba funcional |
| AUD-04 | Referencias HTML locales | Sin referencias faltantes en ocho HTML | Solo enlaces locales |
| AUD-05 | Gestión de tareas | 25/25 en raíz y 25/25 en espejo | Simulaciones y mocks, no operaciones reales |
| AUD-06 | Trabajadores, selección focalizada | 5/5 por árbol | Tests focalizados con dobles |
| AUD-07 | Reautenticación servidor | 6/6 | Dependencias simuladas; no Auth real |

El informe de Codex suma 66 ejecuciones de casos considerando las repeticiones de raíz/espejo. **No son 66 requisitos distintos**.

## 3. Evidencias históricas, no repetidas en esa auditoría

- Auth: 211/211 y gestión de usuarios: 45/45 por árbol, según registro histórico GIT-02.
- Dashboard: 54/54 históricos.
- Baños: 35/35; Bodegas: 31/31 históricos.
- HTTP Deno: 14/14 históricos.
- Verificaciones visuales y documentales de etapas anteriores: existen registros **informados por el usuario**, no una certificación actual del sistema.

Estas cifras deben citarse como históricas hasta disponer de salidas de pruebas, fecha, versión y entorno reproducibles.

## 4. Limitaciones y pendientes importantes

- No se certificaron las políticas RLS/Storage/JWT y MFA efectivamente instaladas en producción.
- Algunos harness antiguos tienen fallos de fixtures; otros están bloqueados por falta de Playwright. No presentar esos fallos de infraestructura como defectos funcionales demostrados.
- Raíz y `publicacion/` tienen nueve archivos distintos. No asumir que son copias idénticas.
- Se identificó posible XSS por interpolación de valores sin escape en Remodelaciones. **Hallazgo pendiente de confirmar en entorno aislado**, no explotación acreditada.
- No ejecutar operaciones destructivas sobre Supabase ni utilizar datos personales reales para obtener capturas.
- La instalación completa del backend no es reproducible solo a partir de los SQL de referencia disponibles.

## 5. Casos funcionales a documentar formalmente

| ID propuesto | Recorrido | Rol orientativo | Estado |
|---|---|---|---|
| CP-01 | Inicio/cierre de sesión y rechazo de acceso sin perfil autorizado | Usuarios habilitados | Pendiente de evidencia manual actual |
| CP-02 | Registrar y consultar solicitud | Recepción (según permisos vigentes) | Pendiente de evidencia manual actual |
| CP-03 | Decidir solicitud y comprobar trazabilidad | Administrador autorizado | Pendiente de evidencia manual actual |
| CP-04 | Crear, asignar y consultar tarea | Administrador autorizado | Pruebas simuladas existentes; evidencia manual pendiente |
| CP-05 | Consultar inventario sin privilegios de edición | Técnico | Pendiente de evidencia manual actual |
| CP-06 | Consultar historial de mantenciones | Rol operativo habilitado | Pendiente de evidencia manual actual |
| CP-07 | Verificar restricciones de roles | AP / AT / Técnico / Recepción | Pendiente de evidencias servidor y manual |
| CP-08 | Consultar documento con acceso autorizado y denegado | Roles según contrato | Pendiente de evidencia manual actual |

Los IDs CP son **numeración documental propuesta**, no códigos originales de Jira ni evidencia de ejecución.

## 6. Formato para completar cada caso

- ID y requisito/historia de Jira:
- Versión, commit y entorno:
- Fecha y responsable:
- Rol, datos sintéticos y precondición:
- Procedimiento:
- Resultado esperado:
- Resultado observado:
- Evidencia (captura, log saneado o archivo):
- Veredicto: Aprobado / Fallido / Bloqueado / No ejecutado
- Incidencia vinculada:

## 7. Fuente de verdad y aprobación

Repositorio técnico: https://github.com/Pablok00/pruebaelalmendro  
Auditoría: reporte de Codex entregado al equipo con corte 17-11-2026.  
**Pendiente:** que el equipo contraste las observaciones con el estado de producción y firme una versión final antes de la entrega.
