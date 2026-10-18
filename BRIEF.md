# Brief del Proyecto — App de Mantenimiento de Motos 125cc (Órbita 1)

**Autor:** David  
**Módulo:** Diseño de Interfaces Web  

---

## 🔗 Enlaces a los Entregables
* **Tablero de Investigación, Personas, MVP, User Flow y Sitemap (FigJam):** [PEGAR_ENLACE_PÚBLICO_FIGJAM_AQUÍ]
* **Wireframes (Desktop & Mobile) y Prototipo Navegable (Figma):** [PEGAR_ENLACE_PÚBLICO_FIGMA_AQUÍ]
* **Prototipo Interactivo (Vista directa de reproducción):** [PEGAR_ENLACE_PLAY_PROTOTYPE_AQUÍ]

---

## 1. El Problema
Los propietarios de motocicletas de 125cc que reparan o mantienen su moto por su cuenta tienen dificultades para encontrar las referencias exactas de piezas por ficha técnica, carecen de algunas herramientas o no saben cómo montarlas paso a paso. Por otro lado, quienes prefieren delegar en un profesional suelen olvidar cuándo les toca revisión (fiándose solo de la pegatina del taller o llevándolo "a ojo") y temen que en los talleres les engañen con el precio o no trabajen bien.

**Respaldo con datos reales (Encuesta propia en Google Forms a 17 motoristas de 125cc):**
* **Perfiles identificados:** 
  * **Perfil "Manitas" (7 de 17 respuestas — 41,2%):** Afirman *"Me encanta meterle mano yo mismo"* y apuntan las revisiones en notas o en el calendario, pero chocan con no saber qué piezas exactas comprar, cómo montarlas o la falta de herramientas.
  * **Perfil "Práctico / Taller" (10 de 17 respuestas — 58,8%):** Se dividen entre *"Sé lo básico pero me da miedo liarla"* y *"No tengo ni idea, lo llevo al taller"*. Su freno principal es el miedo a romper algo, no saber si en el taller trabajan bien, que les timen con el precio o encontrar uno de confianza cerca.
* **Funciones más demandadas en la encuesta:** El **58,8% (10 de 17)** eligió *"Compra de piezas y tutoriales"* como función favorita, seguido de *"Recordatorios de mantenimiento"* (**35,3% — 6 de 17**) y *"Buscador de talleres recomendados"*.

---

## 2. Alcance (MVP)

### ✅ Lo que ENTRA en el MVP (4 semanas):
1. **Registro e Inicio de sesión:** Acceso rápido de usuario y creación de cuenta.
2. **Garaje virtual (`Inicio / Mis motos` y `Añadir moto`):** Registro de la moto (marca, modelo, año de fabricación, cilindrada y número de bastidor), elección del tipo de seguimiento y panel de alertas de mantenimiento (`Alerta 1, 2, 3`).
3. **Guías y Tareas (`Guía y tareas`):** Pantalla de tarea con vídeo explicativo, listado exacto de herramientas necesarias (ej. destornillador estrella, carraca 50mm, caballete) e instrucciones paso a paso (`1. Desmontar... 2. Cambiar... 3. Volver a montar...`).
4. **Buscador y Mapa de Talleres (`Mapa talleres`):** Mapa con buscador, filtros y listado de talleres cercanos recomendados indicando descripción, ubicación y cómo llegar.

### ❌ Lo que QUEDA FUERA del MVP (Descartado por viabilidad):
* **Conexión con hardware OBD2:** Descartado por ser demasiado complejo de implementar en un alcance de 4 semanas.
* **Tienda interna con pasarela de pago:** Gestionar cobros y venta directa de piezas dentro de la app es inviable ahora mismo; se suple indicando las herramientas necesarias y guías paso a paso.

---

## 3. Personas

### 👤 Persona Principal: El Motero "Manitas"
* **Frase representativa:** *"Me encanta meterle mano yo mismo a la moto, pero necesito la referencia exacta para no equivocarme al comprar."*
* **Contexto de uso:** Usa la app por la noche en el garaje. Dispositivo: **Teléfono móvil**. Conexión: **4G inestable y lenta** porque está bajo tierra.
* **Hábitos y Frustraciones (Pain Points):** Lleva más de 1 año con su 125cc y apunta las revisiones en notas o calendario. Sus mayores obstáculos son no saber qué piezas exactas comprar por ficha técnica o no saber cómo montarlas.
* **Qué exige de la App:** Vídeos y tutoriales claros, listado de herramientas necesarias para cada tarea y preguntas frecuentes por modelo.

### 👤 Persona Secundaria: El Motero Práctico
* **Frase representativa:** *"Sé lo básico pero me da miedo liarla. Quiero que la app me avise de todo y me diga a qué taller de confianza ir."*
* **Contexto de uso:** Usa la app entre semana por la tarde en su casa. Dispositivo: **Portátil o móvil**. Conexión: **Wi-Fi estable y rápida** de fibra óptica.
* **Hábitos y Frustraciones (Pain Points):** Se fía de la pegatina del taller o lo lleva cuando se acuerda. En casa le frena la falta de herramientas o el miedo a romper algo; al buscar mecánico, le aterra que le timen con el precio y le cuesta encontrar uno de confianza cerca.
* **Qué exige de la App:** Avisos de mantenimiento con antelación (ITV, seguro, revisiones) y un buscador de talleres honesto donde no aparezca primero simplemente el que más pague.

---

## 4. Criterios de Éxito
1. **Criterio para "El Motero Manitas":** Encuentra las herramientas necesarias y los pasos para realizar el mantenimiento (ej. cambiar el aceite) en **3 clics o menos** desde que inicia sesión.
2. **Criterio para "El Motero Práctico":** Registra su moto con su tipo de seguimiento o localiza un taller de confianza en el mapa en **menos de 1 minuto**.

---

## 5. Restricción Ambiental y Sostenibilidad Web
Dado que nuestra Persona Principal (*El Motero "Manitas"*) utiliza la aplicación desde un **garaje subterráneo con cobertura 4G inestable y lenta**, el diseño aplica medidas de sostenibilidad web y bajo consumo de datos:
* **Prioridad al texto ligero:** El listado de herramientas necesarias y las instrucciones numeradas paso a paso se muestran en texto plano de carga instantánea, sin obligar a descargar el vídeo explicativo si el usuario solo necesita consultar un paso o herramienta.
* **Carga bajo demanda (Lazy Loading):** El vídeo explicativo y los recursos del mapa solo se cargan cuando el usuario interactúa con ellos, reduciendo la transferencia de megabytes innecesarios y el consumo de batería del dispositivo móvil.
