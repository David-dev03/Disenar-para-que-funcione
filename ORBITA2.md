# Órbita 2: sistema visual de MyGaraje (Gestión de Motos)

## Enlaces

| Qué | Enlace |
|---|---|
| Archivo de Figma (versión "Entrega Órbita 2") | https://www.figma.com/design/XzMeFn16ll7OgHR8nLjnHi/Plantilla-para-iniciar-proyectos--Community-?node-id=547-513&p=f&t=JpU2gAbwU2L3Fbdz-0 |
| Prototipo (enlace que empieza por `figma.com/proto/`) | https://www.figma.com/proto/XzMeFn16ll7OgHR8nLjnHi/Plantilla-para-iniciar-proyectos--Community-?node-id=550-679&starting-point-node-id=550%3A679 |
| Proyecto de Google Stitch (solo si lo has usado) | No se ha utilizado |

## Dónde está cada cosa en Figma

| Entregable | Página y sección del archivo |
|---|---|
| Inventario de decisiones | Página `🖼️ Wireframes` ➔ Sección `Documentación e Inventario de Tokens` |
| Wireframes rediseñados con sus notas | Página `🖼️ Wireframes` ➔ Sección `Wireframe Mobile (Rediseñado)` (con Frame 3 de notas) |
| Componentes | Página `⚙️ Componentes` ➔ Componentes Botón Principal, Input text y Tarjeta moto |
| Mockups del happy path | Página `📐 Mockups` ➔ Sección `Mockups Mobile (Modo Claro)` (6 pantallas) |
| Pantalla principal en el segundo ancho | Página `📐 Mockups` ➔ Sección `Mockup Desktop (Responsive)` (ancho 1440px) |
| Pantallas en modo oscuro | Página `📐 Mockups` ➔ Sección `Mockups Mobile (Modo Oscuro)` |
| Guía de estilo | Página `🎨 Guía de estilo` ➔ Sección 1 con tablas de HTML, contraste y rendimiento |

## Lista de comprobación de Figma

- [x] Variables en dos colecciones (primitivos y semánticos), con alias, modos claro y oscuro, ámbito, descripción y sintaxis de código.
- [x] Estilos de texto, efecto y retícula vinculados a las variables.
- [x] Componentes con Auto layout, variables, propiedades y variantes de estado.
- [x] Mockups construidos enteros con Auto layout y espacios sacados de variables.
- [x] Pantalla principal en un segundo ancho, con los mismos componentes.
- [x] Modo oscuro aplicado con el selector de modo.
- [x] Prototipo que recorre el happy path completo.
- [x] Prueba 1 superada: al cambiar `color/primary`, cambian todas las pantallas a la vez.
- [x] Prueba 2 superada: con todos los mockups en modo oscuro, nada desaparece contra el fondo.

## Resumen de decisiones

### Rediseño de los wireframes
Se rediseñó el Happy Path en Mobile unificando botones principales a 48px de altura mínima táctil (WCAG 2.5.5) para facilitar el uso con una mano o guantes. Se agruparon los campos de formulario aplicando la Ley de Proximidad de Gestalt (etiqueta a 6px del input, bloques separados a 16px). En la pantalla principal (*Mis motos*) se elevó la jerarquía de las revisiones y alertas críticas para consulta rápida antes de salir a rodar (Ley de Fitts).

### Color
- **Color principal**: Naranja de marca (`orange-700` #AD3515 en Modo Claro / `orange-400` #FF8655 en Modo Oscuro), elegido por identidad motera, seguridad y alto contraste visual.
- **Color secundario/estados**: Verde (`green-700`/`green-300`) para revisiones al día y Rojo (`red-700`/`red-300`) para alertas de mantenimiento vencido.
- **Contraste más bajo**: `border` (`gray-300`) sobre `background` (`gray-50`) con un ratio de **3.1:1** en Claro y **3.4:1** en Oscuro, cumpliendo el estándar WCAG AA para elementos de interfaz (≥ 3.0:1). Todos los textos normales superan holgadamente el mínimo de 4.5:1 (texto principal llega a 15.2:1 en claro).

### Tipografía
- **Familia**: Roboto (Google Fonts).
- **Pesos**: Regular (400), Medium (500) y Bold (700). Solo 3 pesos para optimizar el rendimiento y la velocidad de descarga en conexiones móviles (criterio WSG 2.17).
- **Justificación**: Gran legibilidad en pantallas reducidas y excelente renderizado en interfaces técnicas y densas.

### Espaciado y retícula
- **Base de la escala**: Cuadrícula de 8px (variables `sp-4`, `sp-8`, `sp-12`, `sp-16`, `sp-24`).
- **Retícula Mobile (393px)**: 4 columnas, margen de 16px, medianil de 16px.
- **Retícula Desktop (1440px)**: 12 columnas, margen de 80px, medianil de 24px.

### Componentes
- **Botón Principal**: Variantes de estado (`Default`, `Hover`, `Pressed`, `Disabled`) y variante de estilo secundario con Auto Layout.
- **Input text**: Variantes de estado (`Default`, `Focus`, `Error` con mensaje e icono de validación).
- **Tarjeta moto**: Contenedor Auto Layout con imagen adaptativa (`Fill`), datos técnicos, badge de estado ("Al día") y botón de acción.

### Responsive y modo oscuro
- **Responsive**: Al pasar *Inicio / Mis motos* a 1440px (Desktop), las tarjetas de moto pasaron de una columna vertical a fila horizontal de 2 columnas, y la lista de alertas se adaptó a 853px de ancho para equilibrar el layout.
- **Modo Oscuro**: Implementado exclusivamente con el selector nativo de modos de Figma (`Light` / `Dark`) mediante alias semánticos (`color/surface`, `color/background`, `color/on-surface`). Ningún componente fue duplicado a mano.

## Uso de IA
Se utilizó asistencia de IA como apoyo para la estructura de la escala de tokens semánticos, fórmulas de contraste WCAG y la redacción de justificaciones de diseño. Todo el diseño, Auto layout, componentes y variables fueron implementados y verificados en Figma. El detalle completo está recogido en el [CHANGELOG.md](CHANGELOG.md).

## Lo que ha quedado pendiente
El sistema visual y los flujos del Happy Path han quedado completamente terminados, con todos los requisitos de la rúbrica cubiertos (variables primitivas/semánticas con modos, estilos locales, componentes con variantes, mockups Auto layout, responsive y prototipo).
