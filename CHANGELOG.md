# CHANGELOG - Registro de Actividades y Asistencia de IA (Órbita 2)

## Proyecto: Sistema Visual MyGaraje (Órbita 2)

### 2026-11-08 · Sesión de Diseño de Sistema Visual y Mockups
- **Qué se le pidió a la IA**: 
  - Asistencia para calcular contrastes WCAG de la paleta Orange/Gray.
  - Estructuración de la escala de tokens semánticos (Light/Dark) y nomenclatura CSS.
  - Tabla de correspondencia entre los 8 niveles tipográficos de Roboto y etiquetas semánticas de HTML.
  - Revisión estricta de jerarquía visual y accesibilidad en las 6 pantallas del Happy Path.
- **Qué devolvió la IA**:
  - Lista de tokens primitivos y semánticos con sintaxis `var(--color-...)`.
  - Mediciones de contraste Stark para la Guía de estilo.
  - Justificaciones técnicas basadas en leyes de Gestalt (proximidad), Ley de Fitts y criterios WCAG 2.5.5.
- **Qué se conservó**:
  - Los nombres y sintaxis de variables semánticas.
  - Las tablas de contraste y correspondencia HTML para la página `🎨 Guía de estilo`.
  - La estructura de variantes de estado en componentes maestros (`Default`, `Hover`, `Pressed`, `Disabled`, `Focus`, `Error`).
- **Qué se cambió**:
  - Ajuste visual manual de componentes en Figma para adaptarse a la estética de taller/dashboard motero.
  - Creación y afinado de Auto Layout en tarjetas, inputs y botones.
  - Implementación práctica de modos claro y oscuro en Figma mediante el selector de colecciones.
