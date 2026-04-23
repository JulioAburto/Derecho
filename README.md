# Derecho INOP

Sitio web estático en Astro orientado a informar sobre la violencia intrafamiliar contra hombres en Nicaragua, con un enfoque jurídico, académico y accesible para público general, estudiantes y personas que buscan una orientación inicial.

## Propósito

El proyecto no debe comportarse como una transcripción del entregable académico en formato `.doc`.

La web está pensada como una página informativa abierta que:

- explica la problemática y sus barreras sociales e institucionales,
- presenta una lectura jurídica clara y comprensible,
- orienta sobre rutas iniciales de apoyo y denuncia,
- reúne el marco normativo e institucional citado en el proyecto.

## Enfoque editorial

- Tono formal, claro y académico.
- Lenguaje accesible para personas no especialistas.
- Sin invención de hechos, normas, instituciones o datos no presentes en las fuentes del proyecto.
- Prioridad a la utilidad pública del sitio por encima del formato del entregable universitario.

## Estado actual del sitio

La experiencia está organizada como sitio informativo real, no como ficha de presentación del documento académico.

Rutas principales:

- `/` Inicio y panorama general del sitio
- `/proyecto` Proyecto e identificación
- `/problematica` Contexto, planteamiento y análisis
- `/solucion` Solución, orientación y rutas de actuación
- `/referencias` Marco normativo e institucional

## Estructura del proyecto

```text
/
├── docs/
├── public/
├── src/
│   ├── components/
│   │   ├── ContentCard.astro
│   │   ├── PageHero.astro
│   │   ├── SiteFooter.astro
│   │   └── SiteHeader.astro
│   ├── layouts/
│   │   └── BaseLayout.astro
│   └── pages/
│       ├── index.astro
│       ├── proyecto.astro
│       ├── problematica.astro
│       ├── solucion.astro
│       └── referencias.astro
├── package.json
└── README.md
```

## Fuentes del proyecto

Documentos principales en `docs/`:

- `TRABAJO INOP.doc`
- `Desafío INOP.docx`
- `Creatividad y la innovacion .doc`
- `MENSAJESPROFE.MD`

La orientación del profesor confirma que la materialización correcta del proyecto es una página web informativa abierta para la población nicaragüense.

## Sistema visual

La UI utiliza actualmente 2 familias tipográficas de referencia:

- `--font-body`: Inter y fallback sans-serif para lectura general
- `--font-display`: Iowan Old Style y fallback serif para títulos

Esta cantidad es adecuada para el proyecto.

Usar 2 familias es la decisión correcta aquí porque:

- mantiene identidad visual sobria,
- evita ruido tipográfico,
- conserva jerarquía clara entre títulos y cuerpo,
- mejora consistencia en un sitio jurídico-académico.

## Comandos

Todos los comandos se ejecutan desde la raíz del proyecto.

| Comando | Acción |
| :-- | :-- |
| `npm install` | Instala dependencias |
| `npm run dev` | Inicia el servidor local |
| `npm run build` | Genera la versión estática en `dist/` |
| `npm run preview` | Previsualiza la build local |

## Criterios de trabajo

- Mantener Astro y la arquitectura simple del proyecto.
- Evitar convertir la web en una copia literal del esquema de entrega universitaria.
- No agregar funciones tipo CMS, autenticación o chatbot salvo solicitud explícita.
- Preservar la utilidad pública, la legibilidad y la claridad jurídica del contenido.
