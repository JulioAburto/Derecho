# Imágenes del sitio

Coloca aquí las ilustraciones editoriales y recursos visuales del proyecto.

## Estructura recomendada

- `inicio/`
  Ilustración principal del hero de portada.
- `problematica/`
  Ilustraciones analíticas o visuales sobre barreras, estigma y acceso a la justicia.
- `solucion/`
  Diagramas, rutas de actuación o ilustraciones de orientación jurídica.
- `shared/`
  Recursos reutilizables, micro-ilustraciones o imágenes comunes a varias páginas.

## Convenciones sugeridas

- Usar nombres cortos y claros, por ejemplo:
  - `inicio/hero-orientacion-legal.webp`
  - `problematica/barreras-acceso-justicia.webp`
  - `solucion/ruta-orientacion-denuncia.webp`
- Preferir `webp`, `avif` o `svg` según el tipo de ilustración.
- Evitar espacios en blanco y caracteres especiales en los nombres de archivo.

## Integración esperada

Cuando se usen en Astro, lo ideal es importarlas desde `src/assets/images/...` y renderizarlas con `astro:assets`.
