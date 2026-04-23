# Project: Static Astro Informational Site for Derecho INOP

## Goal
Build and maintain a static informational site in Astro for the Derecho INOP project, based on verified documentation in `/docs`.

## Scope
- The project is a public informational website, not a CMS, dashboard, or authenticated app.
- The site must remain static and simple unless the user explicitly requests a broader scope.
- Content should be educational, academic, and accessible to the general public.
- Do not present the site as personalized legal advice or as an official legal authority.

## Project direction
- The broad theme is access to justice in Nicaragua.
- Current project drafts focus especially on rights awareness, legal orientation, and barriers affecting men who may be victims of violence or family conflict.
- Keep the implementation aligned with the professor guidance: an open informational website is the default direction.
- A chatbot is only a future option if the user explicitly requests it.

## Source hierarchy

### Primary project sources
Use these as the main factual source of truth:
- `docs\Desafío INOP.docx`
- `docs\TRABAJO INOP.doc`
- `docs\Creatividad y la innovacion .doc`
- `docs\MENSAJESPROFE.MD`

### Structure and deliverable references
Use these to shape sections, ordering, and required deliverable parts, but not to invent project facts:
- `docs\ESTRUCTURA.MD`
- `docs\Estructura.docx`

### Reference examples only
These files are examples from other topics or careers and must not be treated as factual project content:
- `docs\Documento.pdf`
- `docs\EcoLYBorrador.docx`

If extracted text from legacy binary files such as `.doc` is incomplete, noisy, or conflicts with another source, report the ambiguity and ask before relying on it.

## Content rules
- Do not invent legal facts, institutions, procedures, dates, names, or references.
- Preserve academic tone and readable public-facing language.
- Follow the professor guidance to write content in a more developed and argumentative way, not as short isolated phrases.
- When docs conflict, prioritize verified project-specific guidance and explicitly report the conflict.
- If a statement cannot be confirmed from the primary sources, leave it out or ask the user.

## Required structure
When organizing pages or major sections, align with the official deliverable structure:
1. Nombre del proyecto
2. Categorias
3. Universidad
4. Nombre del equipo
5. Integrantes y telefonos
6. Nombre del mentor
7. Planteamiento del problema
8. Descripcion de la problematica segun el desafio
9. Descripcion de la solucion
10. Impacto
11. Innovacion
12. Presupuesto
13. Propuestas descartadas
14. Referencias

## Astro conventions
- Use `src/pages` for routes.
- Prefer `.astro` components unless interactivity is clearly necessary.
- Prefer reusable components over duplicated markup.
- Only introduce `src/content/*` and content collections if the site actually needs article-style content.
- Keep styling simple, readable, and appropriate for an academic presentation.

## Current repo state
- The repository currently starts from a minimal Astro scaffold.
- Do not assume an existing blog architecture, content collection setup, or completed site structure.
- Inspect current routes and files before making structural changes.

## Commands
- Install: `npm install`
- Dev: `npm run dev`
- Build: `npm run build`
- Preview: `npm run preview`

## Working rules for the agent
- Before changing content or structure, inspect the primary project docs and the current implementation.
- Prefer the smallest viable implementation that matches the verified documentation.
- Do not introduce CMS, database, authentication, or chatbot features unless explicitly requested.
- Keep public content informative, grounded in the docs, and suitable for a university deliverable.
