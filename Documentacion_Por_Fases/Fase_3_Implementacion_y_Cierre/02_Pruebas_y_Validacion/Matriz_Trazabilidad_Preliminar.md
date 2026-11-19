# Matriz de trazabilidad preliminar — Fase 3

**Proyecto:** OMM Hotel El Almendro — equipo BPB  
**Estado:** borrador basado en inventario técnico y matriz histórica; requiere contrastar IDs con `Documentos_Fase_2/Documentacion/06_Matriz_Requerimientos_V2.pdf` y Jira.  
**Regla:** no asignar una historia de Jira ni declarar cumplimiento sin evidencia verificable.

| Área | Requisito / ID de la matriz | Componente técnico identificado por Codex | Prueba disponible | Evidencia y estado |
|---|---|---|---|---|
| Dashboard | RF-DASH-01 (panel principal) | `js/views/dashboard.js` | `tests/harness_dashboard.js` | 54/54 históricos; ejecución vigente pendiente |
| Mantenciones | RF-MANT-01 (ficha de mantención) | `js/views/mantenciones.js`, servicio de mantenciones | Harness Baños y pruebas de mantenciones parciales | Cobertura parcial; validación de ficha pendiente |
| Áreas | RF-AREA-01 (tarjetas de área) | `js/views/areas.js` | `tests/harness_areas.js` | Harness con fallos históricos de fixture; pendiente |
| Activos fijos | RF-ACT-01 (ficha de activo fijo) | `js/views/activos.js` | Sin prueba funcional acreditada | Pendiente/no implementado operativamente |
| Solicitudes | Pendiente de confirmar ID exacto | `js/views/solicitudes.js`, `js/services/solicitudes.service.js` | `tests/harness_solicitudes_consulta.js` y harness Reactiva | Cobertura simulada/histórica; falta caso end-to-end |
| Gestión de tareas | Pendiente de confirmar ID exacto | `js/views/gestionTareas.js`, `js/services/gestionTareas.service.js` | `tests/gestion_tareas.test.mjs` | 25/25 por árbol reportados al 17-11-2026 |
| Inventario | Pendiente de confirmar ID exacto | `js/views/inventario.js`, servicio de inventario | `tests/harness_inv4.js` | Harness históricos con fixtures fallidos |
| Acceso y usuarios | Pendiente de confirmar ID exacto | `js/controlSesion.js`, `js/views/admin.js` | Harness Auth y usuarios | Resultados históricos, no autorización RLS certificada |

**Precisión:** los IDs RF-DASH-01, RF-MANT-01, RF-AREA-01 y RF-ACT-01 provienen de la matriz aportada; para el resto se deja el ID pendiente en lugar de inventarlo.

## Campos faltantes para convertirla en matriz final

- ID exacto de la historia de usuario y épica Jira
- Criterio de aceptación y prioridad vigentes
- Commit/versión del componente evaluado
- Caso de prueba e informe de ejecución correspondiente
- Captura o log verificable, con fecha y responsable
- Estado validado por el equipo/stakeholder

No confundir la existencia del código con aceptación o aprobación académica.
