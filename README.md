# iser.io

Personal blog and project hub for Kevin Lee (Iser) — Developer Relations Engineer @ Google Chrome.

A blog-forward site for writing about AI, vibe coding, ad tech, the web, and Chrome, with a projects page linking to separately deployed apps.

**Stack:** Next.js 16 App Router, Tailwind CSS v4, shadcn/ui, MDX, Vercel

## Local Setup

### Prerequisites

- Node.js 20+
- npm 10+
- Git

### Getting Started

```bash
# Clone the repo
git clone https://github.com/nicholasgasior/iser.io.git
cd iser.io

# Install dependencies
npm install

# Start the dev server (uses Turbopack)
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the site.

### Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start dev server with Turbopack |
| `npm run build` | Production build (static export) |
| `npm run start` | Serve the production build locally |
| `npm run lint` | Run ESLint |

## Project Structure

```
iser.io/
├── app/                    # Next.js App Router pages
│   ├── layout.tsx          # Root layout (nav, footer, theme provider)
│   ├── page.tsx            # Homepage — hero + post card grid
│   ├── blog/               # Blog listing and individual posts
│   ├── projects/           # Project showcase
│   ├── about/              # About page
│   ├── rss.xml/route.ts    # RSS feed
│   └── api/subscribe/      # Newsletter signup endpoint
├── content/posts/          # MDX blog posts with frontmatter
├── components/             # React components
│   ├── ui/                 # shadcn/ui components
│   └── mdx/                # Custom MDX components
├── lib/                    # Utilities (MDX parsing, search index)
├── public/                 # Static assets
└── docs/                   # Design specs and implementation plans
```

## Writing Blog Posts

Create a new `.mdx` file in `content/posts/`:

```mdx
---
title: "My Post Title"
date: "2026-04-02"
tags: ["ai", "web"]
summary: "A short description for cards and SEO."
---

Post content here with full MDX support.
```

## Deployment

The site is deployed to [Vercel](https://vercel.com) on push to `main`. Preview deployments are created for pull requests.

## License

MIT
