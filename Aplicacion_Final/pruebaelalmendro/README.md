# Sistema web de Obras, Mantención y Mejoras — El Almendro

Aplicación web desarrollada con **HTML, CSS y JavaScript**, conectada a servicios de **Supabase y PostgreSQL**.

## Estructura principal

| Ruta | Función |
|---|---|
| `index.html` | Interfaz principal del sistema |
| `login.html` | Inicio de sesión |
| `registrar.html` | Registro de usuarios |
| `recuperar-password.html` | Recuperación de contraseña |
| `css/` | Estilos de la aplicación |
| `js/` | Vistas, servicios y lógica del cliente |
| `publicacion/` | Copia de archivos utilizada durante el desarrollo y revisiones |
| `docs/` | Documentación técnica y registros de evolución |

## Ejecución y despliegue

La interfaz puede servirse con un servidor HTTP local, por ejemplo Live Server. No se requiere instalar Next.js ni ejecutar una compilación de JavaScript para utilizar esta copia.

La configuración documentada de Vercel utiliza la raíz del proyecto. Antes de publicar, verificar la configuración real del despliegue y las diferencias que puedan existir entre raíz y `publicacion/`.

La conexión con Supabase puede utilizar servicios alojados aunque la interfaz se ejecute localmente. Emplear cuentas de prueba y autorización para operaciones que modifiquen información.

## Documentación técnica

- [Estado del proyecto](docs/ESTADO_PROYECTO.md)
- [Bitácora de cambios](docs/BITACORA_CAMBIOS.md)
- [Guía técnica de continuidad](docs/HANDOFF_TECNICO.md)

Este código es una copia académica del repositorio operativo [Pablok00/pruebaelalmendro](https://github.com/Pablok00/pruebaelalmendro). No presupone sincronización automática con él ni aceptación final de la plataforma.
