# CLAUDE.md

## Project Overview

Personal blog and project hub at iser.io. Static site built with Next.js 16 App Router, deployed on Vercel.

## Tech Stack

- **Framework:** Next.js 16 (App Router, Turbopack)
- **Styling:** Tailwind CSS v4, shadcn/ui
- **Content:** MDX via next-mdx-remote, gray-matter for frontmatter
- **Syntax highlighting:** Shiki (@shikijs/rehype)
- **Search:** Fuse.js (client-side fuzzy search)
- **Theme:** next-themes (dark-first, light mode support)
- **Comments:** Giscus (GitHub Discussions-backed)
- **Hosting:** Vercel (full SSG, one serverless function for newsletter)

## Development

```bash
npm install
npm run dev       # Dev server on http://localhost:3000
npm run build     # Production build
npm run lint      # ESLint
```

## Project Structure

- `app/` — Next.js App Router pages and layouts
- `content/posts/` — MDX blog posts with YAML frontmatter
- `components/` — React components (ui/ for shadcn, mdx/ for custom MDX)
- `lib/` — Utilities: MDX parsing (`posts.ts`), search index (`search.ts`)
- `public/` — Static assets and OG images
- `docs/` — Design specs and implementation plans

## Conventions

- Dark-first design — always check both dark and light modes
- All pages are statically generated (SSG) except the newsletter API route
- Blog posts live in `content/posts/` as `.mdx` files with frontmatter
- Use shadcn/ui components from `components/ui/` — don't create custom equivalents
- Tailwind CSS v4 syntax (no `tailwind.config.js`, uses CSS-based config)

## Current State

The project has a plan to migrate from a static HTML page (`index.html`) to a full Next.js blog. See `docs/superpowers/plans/2026-04-02-personal-blog.md` for the implementation plan and `docs/superpowers/specs/` for design specs.
