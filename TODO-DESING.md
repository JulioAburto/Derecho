Mapa Actual

- src/pages/ tiene 5 rutas claras y alineadas con el entregable: index, proyecto, problematica, solucion, referencias.
- src/layouts/BaseLayout.astro concentra el shell global, tokens visuales y casi todo el CSS compartido.
- src/components/ tiene 4 piezas reutilizables: SiteHeader, PageHero, ContentCard, SiteFooter.
- El stack es mínimo y correcto para el alcance actual: Astro puro, sin librería UI (package.json:14-16).
- La estructura compila bien: npm run build pasó sin errores.
  Diagnóstico Rápido
- Funciona bien la arquitectura de información: la navegación y la división por páginas traducen bien la estructura académica.
- Funciona también la consistencia base: PageHero y ContentCard dan una forma uniforme a casi todo el sitio.
- Lo más débil no es la organización, sino el lenguaje visual: hoy se siente más “landing page moderna” que “sitio informativo jurídico/académico” (src/layouts/BaseLayout.astro:95-152).
- El mayor riesgo de mantenimiento es que el “sistema de diseño” está demasiado concentrado en un solo archivo global (src/layouts/BaseLayout.astro:44-471).
  Problemas UI/UX
- El hero tiene demasiado peso en todas las páginas. En PageHero.astro:25-53 funciona bien para portada, pero repetido en todas las secciones retrasa la entrada al contenido real.
- Hay demasiada navegación compitiendo a la vez: header, botones primario/secundario y quick-nav dentro del hero. Para un sitio informativo esto puede sentirse redundante.
- Todas las superficies hacen hover aunque no sean clicables (src/layouts/BaseLayout.astro:254-258). Eso sugiere interactividad donde no siempre existe.
- El tono de algunos textos reduce confianza institucional porque insiste en “esqueleto”, “maqueta” y placeholders (src/components/SiteHeader.astro:23, src/components/SiteFooter.astro:5-13, src/pages/index.astro:15).
- La jerarquía interna es consistente, pero algo plana: muchas tarjetas comparten el mismo peso visual, incluso cuando unas son centrales y otras solo de apoyo.
  Observaciones De Sistema De Diseño
- La base está bien encaminada: hay tokens de color, radios y contenedor en :root (src/layouts/BaseLayout.astro:45-62).
- El problema es el acoplamiento: PageHero depende de estilos definidos fuera del componente (src/components/PageHero.astro:25-53 vs src/layouts/BaseLayout.astro:260-287,430-433).
- BaseLayout mezcla demasiadas responsabilidades: shell, utilidades, patrones de cards, tablas, listas y estados interactivos.
- Hay una primera señal de deriva del sistema con un estilo inline en src/pages/index.astro:23.
- No veo necesidad de meter una librería UI ahora; el sistema custom actual es suficiente si se ordena mejor.
  Accesibilidad Y Responsive
- No hay estados claros de :focus-visible para enlaces y botones. Encontré hover, pero no foco de teclado (src/components/SiteHeader.astro:103-108, src/layouts/BaseLayout.astro:254-258).
- No se usa aria-current en la navegación activa (src/components/SiteHeader.astro:27-33).
- La tabla de presupuesto no tiene estrategia responsive; en móvil puede desbordarse (src/pages/solucion.astro:114-149, src/layouts/BaseLayout.astro:374-399).
- En móvil el header pasa a columna pero sigue siendo sticky (src/components/SiteHeader.astro:110-119), así que puede ocupar demasiado alto visible.
- Punto positivo: la estructura de headings es limpia; PageHero centraliza un único h1 por página (src/components/PageHero.astro:29).
  Mejoras Recomendadas

1. Mantener la arquitectura actual, pero bajar la intensidad visual del shell global.
2. Reservar el hero dividido grande para inicio y usar encabezados más compactos en páginas internas.
3. Quitar el hover global sobre .surface y dejar feedback solo en elementos realmente interactivos.
4. Añadir :focus-visible y aria-current antes de seguir refinando estética.
5. Envolver la tabla en un contenedor con overflow-x: auto.
6. Separar estilos por componente y dejar en BaseLayout solo tokens, shell y utilidades realmente globales.
7. Sustituir cuanto antes el copy meta de “maqueta/esqueleto” en zonas visibles.
   Guía De Implementación

- BaseLayout debería conservar :root, body, .container, .surface y quizá .stack-\*.
- SiteHeader debería contener sus propios estados de nav, activo y foco.
- PageHero debería mover sus estilos de layout al propio componente.
- ContentCard ya va mejor encaminado; ahí sí tiene sentido mantener variantes como accent y span.
- Si el contenido crece, el siguiente componente reusable lógico sería un SectionIntro, no una librería completa.
  Alternativas Y Trade-offs

1. Reajuste mínimo: mantener todo y solo corregir accesibilidad, hover y sobriedad visual. Es la mejor opción ahora.
2. Refactor medio: repartir CSS por componente y formalizar tokens de spacing/tipografía. Mejor para crecer sin dolor.
3. Rediseño completo o librería UI: no lo recomiendo todavía; el problema actual no es falta de componentes, sino exceso de peso visual y acoplamiento del CSS.
   Conclusión: la estructura actual es buena a nivel de información y suficiente para seguir construyendo. No la rehacería. Haría una refactorización pequeña para volverla más sobria, más accesible y más mantenible antes de cargar el contenido real.
