---
name: astro-blog-architecture
description: Use when creating or refactoring Astro blog pages, layouts, content collections, tags, archive pages, or post detail pages.
---

# Astro Blog Architecture

When working on this Astro blog:

1. Keep the site static unless explicitly asked otherwise.
2. Prefer Content Collections over ad-hoc content loading.
3. Keep routes under `src/pages`.
4. Reuse layouts/components before creating duplicate page structures.
5. For blog changes, check:
   - `src/content/config.ts`
   - `src/content/blog/`
   - `src/pages/blog/`
   - `src/layouts/`
   - `src/components/`

## Expected outputs
- Minimal file changes
- Clear route structure
- No unnecessary client-side JavaScript
- Good academic readability

## Do not
- Add React islands unless needed
- Add a CMS
- Add server-only features to a static blog