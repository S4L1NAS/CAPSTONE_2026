# Alcance y limitaciones del sistema — Fase 3

**Proyecto:** Sistema web de Obras, Mantención y Mejoras (OMM), Hotel & Centro de Eventos El Almendro  
**Equipo:** BPB  
**Documento preliminar de cierre (18-11-2026).**

## Propósito

Centralizar información y operaciones del hotel que antes se gestionaban en archivos Excel y registros dispersos, facilitando la consulta, seguimiento y trazabilidad de trabajos y solicitudes.

## Alcance funcional identificado en la auditoría

- Acceso y autenticación, administración de usuarios y permisos diferenciados.
- Dashboard y vistas de áreas/instalaciones.
- Mantención general y reactiva, con historiales.
- Solicitudes, inventario y bodegas.
- Gestión de tareas, responsables, avances y visualización temporal.
- Trabajadores y gestión documental con restricciones de acceso.
- Obras, mejoras, remodelaciones, prevención de riesgos y Gantt, con niveles distintos de madurez.

**Aclaración:** la existencia de una pantalla o handler no equivale a prueba integral de funcionamiento. Algunas operaciones administrativas dependen de contratos remotos no auditados.

## Fuera del alcance acreditado

Reservas hoteleras, gestión de huéspedes, facturación y venta de eventos no quedaron acreditadas en la revisión de código.

## Limitaciones registradas

1. Los contratos completos instalados de Supabase y respaldos de base de datos/Storage no están íntegramente versionados en el repositorio.
2. Existe evidencia de pruebas automatizadas con mocks y resultados históricos, pero falta una certificación global actual por requisito y rol.
3. Algunas pantallas están pendientes o son informativas, como Activos Fijos e Importación desde la interfaz.
4. Hay una posible exposición XSS pendiente de validación segura en Remodelaciones.
5. Existen diferencias deliberadas/no reconciliadas entre la raíz operativa y `publicacion/`.
6. La plataforma usa Supabase como fuente de verdad; no asumir que el frontend por sí solo garantiza las autorizaciones.

## Próximos pasos propuestos

Completar casos de prueba con evidencias saneadas, verificar autorizaciones efectivas, cerrar hallazgos de seguridad y mejorar reproducibilidad técnica. Priorizar la validación del producto existente sobre nuevas funcionalidades antes del cierre académico.

**Fuente:** auditoría Codex de solo lectura con corte 17-11-2026, proporcionada por el equipo. Estado sujeto a confirmación final.
