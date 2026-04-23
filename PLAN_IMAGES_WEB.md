# Plan de Integración de Imágenes para la Web

## 1. Dirección adoptada

La línea correcta para este proyecto es:

- priorizar ilustraciones sobre fotografía,
- preferir imágenes generadas,
- mantener texto primero en móvil,
- usar las imágenes como apoyo editorial y no como elemento dominante,
- evitar cualquier dramatización explícita de la violencia.

Esta decisión encaja con el tono jurídico-académico del sitio y con su función de orientación pública.

## 2. Qué se necesita para llevar a cabo el plan

Con la información actual del proyecto, ya es posible avanzar hasta la etapa de prompts y definición visual.

### Mínimo indispensable

1. Mantener una sola línea visual para todas las imágenes.
2. Confirmar que las imágenes serán ilustraciones generadas, no fotografías.
3. Mantener la prioridad del texto en móvil.
4. Generar imágenes sin texto incrustado dentro de la ilustración.
5. Definir solo 3 puntos iniciales de uso:
   - inicio,
   - problemática,
   - solución.

### Información opcional que ayudaría

No es obligatoria para empezar, pero sí puede mejorar el resultado final:

1. Confirmar si quieres una referencia visual sutil a Nicaragua.
2. Confirmar si prefieres figuras humanas abstractas o composición más simbólica.
3. Decidir si también quieres un set pequeño de micro-ilustraciones o íconos para reforzar secciones.
4. Confirmar si alguna imagen debe tener fondo transparente o si todas vivirán dentro de paneles con fondo claro.

## 3. Mejor opción general

La mejor estrategia no es llenar el sitio de imágenes, sino usar una combinación controlada de:

1. Ilustraciones editoriales sobrias.
   Uso recomendado: hero, introducciones y bloques clave.
2. Diagramas o infografías simples.
   Uso recomendado: rutas de apoyo, barreras de denuncia, pasos de actuación.
3. Micro-ilustraciones discretas.
   Uso recomendado: cards, acentos visuales y refuerzo de categorías.

## 4. Por qué esta es la mejor opción

- Se adapta al tono serio y profesional del sitio.
- Evita el problema ético y visual de representar la violencia de forma explícita.
- Mantiene coherencia entre desktop, tablet y móvil.
- Funciona bien con la estructura actual, que es tipográfica, clara y editorial.
- Permite construir una identidad visual propia sin depender de imágenes de stock genéricas.

## 5. Qué evitar

- fotografías dramáticas o sensacionalistas,
- golpes, llanto o escenas explícitas de agresión,
- estética policial o punitiva exagerada,
- mazos, esposas o balanzas usadas de forma cliché y dominante,
- composiciones muy oscuras o demasiado corporativas,
- texto incrustado dentro de la imagen,
- overlays de texto sobre la ilustración en móvil.

## 6. Dónde conviene poner imágenes

### Inicio

- Sí conviene una ilustración principal.
- Debe apoyar el mensaje del hero, no competir con él.
- En móvil debe quedar debajo de:
  - título,
  - subtítulo,
  - CTA principal,
  - highlights.

### Problemática

- Muy recomendable una pieza visual.
- La mejor opción es una ilustración analítica o una infografía sin texto incrustado sobre:
  - barreras sociales,
  - desinformación jurídica,
  - estigma,
  - acceso a la justicia.

### Solución

- Es la mejor página para recursos visuales.
- Aquí convienen:
  - diagramas,
  - flujos,
  - rutas de orientación,
  - apoyo institucional,
  - pasos de actuación.

### Proyecto

- Solo conviene una imagen si agrega contexto real.
- Si no aporta valor claro, mejor no usarla.

### Referencias

- No se recomienda una imagen protagonista.
- A lo sumo, acentos visuales discretos o micro-ilustraciones normativas.

## 7. Reglas responsive y UI/UX

### Mobile

Orden recomendado:

1. título,
2. subtítulo,
3. CTA,
4. highlights,
5. imagen.

Reglas:

- La imagen nunca debe desplazar el mensaje principal.
- Ratio recomendado: `4:3` o `16:10`.
- Altura visual: moderada, nunca tipo banner alto.
- No usar texto incrustado dentro de la imagen.

### Tablet

- Si hay espacio, imagen al lado del texto.
- Si no, imagen debajo del texto.
- No dejar media columna vacía ni imagen dominante.
- El bloque visual debe sentirse como apoyo editorial, no como segunda portada.

### Desktop

- La imagen puede convivir al lado del texto.
- Debe ocupar aproximadamente `35% a 45%` del bloque, no más.
- El texto sigue siendo el actor principal.

## 8. Buenas prácticas técnicas

Cuando se implementen imágenes reales, la mejor forma es:

1. Guardarlas en `src/assets/images/`.
2. Usar `astro:assets` con `Image`.
3. Preferir:
   - `SVG` para ilustración lineal e íconos,
   - `WebP` o `AVIF` para ilustraciones raster.
4. Definir siempre:
   - `width`,
   - `height`,
   - `alt`,
   - `sizes`.
5. Usar `loading="eager"` solo para la imagen principal del hero si está realmente above the fold.
6. El resto debe cargarse de forma diferida.

## 9. Componentes recomendados

Si luego se implementa la capa visual, los patrones mínimos correctos serían:

1. `HeroIllustration`
   Para la imagen principal o imagen editorial de portada.
2. `FigureBlock`
   Para imágenes o diagramas dentro del contenido.

No recomendaría más componentes al inicio.

## 10. Dirección visual recomendada

La línea más fuerte para este proyecto es:

- ilustración editorial sobria,
- tonos navy, marfil, gris carbón y dorado sutil,
- trazos finos o formas geométricas suaves,
- composición serena, institucional y contemporánea,
- figuras humanas abstractas o semisimbólicas,
- sin dramatización visual,
- sin recursos visuales que parezcan policiales o propagandísticos.

## 11. Plan de implementación

1. Definir mini guía visual:
   - estilo,
   - paleta,
   - composición,
   - nivel de abstracción.
2. Seleccionar los primeros 3 puntos de uso:
   - inicio,
   - problemática,
   - solución.
3. Generar 1 ilustración principal y 2 recursos secundarios.
4. Integrarlos primero en desktop.
5. Ajustar comportamiento tablet y móvil.
6. Revisar peso visual, legibilidad y prioridad del texto.

## 12. Recomendación final

La mejor estrategia inicial es:

- 1 ilustración principal en inicio,
- 1 ilustración analítica en problemática,
- 1 diagrama o ilustración de ruta en solución,
- sin imagen grande en referencias.

Eso da impacto visual sin romper la seriedad ni la claridad del sitio.

## 13. Prompts para generar imágenes con ChatGPT

Todos los prompts están pensados para:

- mantener el tono jurídico-académico,
- evitar violencia explícita,
- priorizar claridad visual,
- permitir integración responsive,
- convivir bien con texto web real encima o al lado.

### Prompt 1: Ilustración principal para Inicio

**Uso**

- Hero principal del sitio.
- Debe apoyar el mensaje de orientación inicial.

**Ratio recomendado**

- `4:3` o `16:10`

**Prompt**

```text
Ilustración editorial sobria y contemporánea para un sitio web jurídico-académico sobre violencia intrafamiliar contra hombres en Nicaragua. La escena debe comunicar orientación legal inicial, acceso a la justicia, información clara y apoyo institucional sin mostrar violencia explícita. Composición con una figura masculina adulta representada de forma respetuosa y no estereotipada, documentos legales, expediente, ruta visual sutil, símbolos discretos de protección y acompañamiento, ambiente sereno y confiable. Estilo editorial limpio, líneas finas, formas suaves, detalle medio, fondo claro marfil, paleta navy, gris carbón y dorado sutil, iluminación suave, sin dramatismo, sin estética policial, sin mazos ni esposas dominantes, sin texto incrustado, sin logotipos, sin marcas de agua. Imagen horizontal pensada para convivir con interfaz web y texto informativo.
```

**Negative prompt sugerido**

```text
violencia explícita, sangre, golpes, llanto dramático, escena de crimen, armas, esposas, mazo de juez gigante, estética stock, fotografía realista dura, neón, fondo oscuro, texto incrustado, logotipos, marcas de agua
```

### Prompt 2: Ilustración analítica para Problemática

**Uso**

- Página de problemática.
- Debe visualizar barreras y contexto sin dramatizar.

**Ratio recomendado**

- `4:3`

**Prompt**

```text
Ilustración editorial analítica para explicar barreras de acceso a la justicia en casos de violencia intrafamiliar contra hombres en Nicaragua. La imagen debe representar de forma conceptual y respetuosa tres dimensiones: desinformación jurídica, estigma social y barreras institucionales. Usar símbolos como documentos no leídos, ruta interrumpida, puerta institucional semiabierta, figura masculina en silencio, burbujas de juicio social abstractas y elementos de orientación legal. Estilo limpio, serio, académico, contemporáneo, sin violencia explícita, sin escenas de agresión, sin dramatismo. Paleta marfil, navy, gris carbón y dorado sutil. Composición clara, legible y estructurada, apta para sitio web informativo. Sin texto dentro de la imagen, sin logotipos, sin marcas de agua.
```

**Negative prompt sugerido**

```text
golpes, sangre, escenas familiares violentas, rostros llorando en primer plano, propaganda, estética policial, fotomontaje, colores saturados, neón, texto incrustado, logos
```

### Prompt 3: Ilustración o diagrama para Solución

**Uso**

- Página de solución.
- Debe mostrar orientación, apoyo y ruta de actuación.

**Ratio recomendado**

- `4:3`

**Prompt**

```text
Ilustración editorial tipo diagrama para un sitio web jurídico sobre orientación y apoyo en casos de violencia intrafamiliar contra hombres en Nicaragua. La imagen debe mostrar de forma clara una ruta de actuación no textual: recopilación de evidencia, orientación legal inicial, acompañamiento institucional y solicitud de protección. Incluir símbolos discretos como documentos, mensajes, carpeta legal, mesa de orientación, escudo de protección y ruta conectada entre etapas. Estilo editorial sobrio, contemporáneo, limpio, institucional, con composición modular y ordenada. Paleta marfil, navy, gris carbón y dorado sutil. Sin violencia explícita, sin escenas dramáticas, sin texto incrustado, sin logotipos, sin marcas de agua.
```

**Negative prompt sugerido**

```text
tabla de datos literal, interfaz de app cargada, mazos o esposas dominantes, escena judicial teatral, agresión explícita, colores chillones, texto incrustado, marcas de agua
```

### Prompt 4: Ilustración secundaria sobre apoyo institucional

**Uso**

- Apoyo visual para bloques sobre Defensoría Pública, Ministerio Público o bufetes populares universitarios.

**Ratio recomendado**

- `1:1` o `4:3`

**Prompt**

```text
Ilustración editorial sobria sobre acompañamiento institucional y orientación jurídica inicial. Composición con escritorio de atención, documentos, carpeta legal, señal de dirección, figuras humanas abstractas en interacción respetuosa y ambiente institucional claro. Debe transmitir ayuda, escucha, orden y acceso a información jurídica, no burocracia fría. Estilo limpio, académico, contemporáneo, con líneas finas y formas suaves. Paleta marfil, navy, gris carbón y dorado sutil. Sin texto incrustado, sin logotipos, sin marcas de agua.
```

### Prompt 5: Set de micro-ilustraciones o íconos editoriales

**Uso**

- Reforzar secciones, cards o highlights.

**Formato recomendado**

- SVG o fondo transparente

**Prompt**

```text
Set de micro-ilustraciones editoriales sobrias para un sitio jurídico-académico. Crear íconos o mini ilustraciones coherentes entre sí para: marco jurídico, orientación accesible, análisis del problema, ruta de denuncia, apoyo institucional y protección de derechos. Estilo lineal fino con rellenos mínimos, elegante, contemporáneo, serio, sin caricatura, sin exceso de detalle. Paleta limitada en navy, gris carbón y dorado sutil, fondo transparente o fondo muy claro, sin texto incrustado, sin logotipos, sin marcas de agua.
```

## 14. Notas finales para generar bien las imágenes

- Pedir siempre versiones sin texto incrustado.
- Si ChatGPT genera demasiada dramatización, reforzar: `editorial, calmado, institucional, sin violencia explícita`.
- Si la imagen sale demasiado genérica, reforzar: `sitio jurídico-académico, acceso a la justicia, orientación inicial, composición clara para web`.
- Si la imagen sale demasiado corporativa, reforzar: `editorial, humana, accesible, contemporánea, no empresarial`.
- Si quieres variantes por sección, la mejor práctica es generar 3 opciones por prompt y luego elegir una sola línea visual coherente.
