# Portafolio de Luis Poblete

Página personal con mis proyectos de ciberseguridad, cloud e IA.

**Ver en línea:** https://kotkem.github.io/portfolio-cloud-security/

## Cómo lo hice

1. **Primera versión (marzo 2026):** sitio estático en un bucket de Amazon S3, servido con CloudFront. Cada `push` a `main` lo subía automáticamente con un workflow de GitHub Actions (`aws s3 sync`).
2. **Versión actual:** mi cuenta gratuita de AWS terminó, así que lo migré a GitHub Pages. Borré el workflow y los secretos con las llaves de AWS del repositorio.

## Qué aprendí

- A automatizar un despliegue con GitHub Actions.
- A guardar credenciales como *secrets* y no dentro del código.
- Qué mejoraría la próxima vez: usar OIDC en vez de llaves de acceso de larga duración, y darle al usuario de IAM permiso solo sobre ese bucket (mínimo privilegio).

El código lo escribí con asistencia de herramientas de IA; la arquitectura y el despliegue los configuré yo.
