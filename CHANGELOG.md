# CHANGELOG — Registro de Uso de Inteligencia Artificial

En cumplimiento con los criterios de evaluación y trazabilidad de la Órbita 1, se documenta a continuación el uso de herramientas de Inteligencia Artificial durante el proyecto, especificando qué se consultó y qué decisiones y modificaciones se tomaron manualmente.

---

## 1. Síntesis de resultados de la encuesta (Google Forms)
* **Herramienta utilizada:** Gemini (Google AI).
* **Qué se pidió (Prompt/Consulta):** Sintetizar y organizar los resultados exportados de mi encuesta de validación en Google Forms (`Validacion App Mantenimiento Moto 125cc`) para redactar el resumen de investigación y las fichas de *Personas* en FigJam.
* **Qué hice yo manualmente / Qué cambié:** 
  * Creé y difundí personalmente la encuesta de Google Forms, obteniendo **17 respuestas reales** de usuarios de motos de 125cc.
  * Verifiqué que los porcentajes (58,8% que prioriza piezas/tutoriales frente a recordatorios y talleres) y las citas textuales de los encuestados (*"Que sea gratis, fácil de usar y honesto a la hora de buscar taller"*, *"Tener la referencia exacta de las piezas por ficha técnica"*) correspondieran exactamente al PDF de respuestas reales, corrigiendo cualquier error de lectura automática.

## 2. Revisión de coherencia entre FigJam y Figma
* **Herramienta utilizada:** Gemini (Google AI).
* **Qué se pidió (Prompt/Consulta):** Comparar mi tablero de FigJam y mis wireframes de Figma con la rúbrica del enunciado para comprobar si faltaba algún requisito.
* **Qué hice yo manualmente / Qué cambié:**
  * Ajusté manualmente el `4. Sitemap` en FigJam para incluir el acceso (`Inicio sesión / Crear cuenta`) y la rama de `Añadir motos` de modo que coincidiera exactamente con las 6 pantallas diseñadas en Figma.
  * Creé manualmente los componentes en Figma (`Navbar desktop`, `Navbar mobile` y tarjetas repetidas) y conecté todas las interacciones del prototipo navegable en Desktop y Mobile.

## 3. Maquetación en Markdown del archivo `BRIEF.md`
* **Herramienta utilizada:** Gemini (Google AI).
* **Qué se pidió (Prompt/Consulta):** Estructurar el documento `BRIEF.md` en formato Markdown con los 5 apartados obligatorios del enunciado.
* **Qué hice yo manualmente / Qué cambié:** Revisé y corregí las cifras de participación (17 encuestados) y añadí los enlaces públicos a mis archivos de FigJam y Figma.
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
