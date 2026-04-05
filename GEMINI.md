# iser.io

## Project Overview

This project is the personal blog and project hub for Kevin Lee (Iser). 

**Current State:** The site is currently a single-page static HTML site containing a portfolio of projects with a highly styled, dark-themed UI. 

*Note: The `README.md` and `CLAUDE.md` files describe a target architecture (Next.js 16, Tailwind CSS v4, MDX) that is currently in the planning phase. The actual codebase at this moment consists only of the static HTML file.*

## Tech Stack (Current)

- **HTML5:** Semantic markup.
- **Vanilla CSS:** Embedded directly in the `<head>` of `index.html`. Uses CSS variables, advanced gradients, animations, and responsive media queries. No external preprocessors or frameworks are used.
- **Typography:** Google Fonts (`DM Sans`, `JetBrains Mono`).

## Key Files & Structure

- `index.html`: The entire current website. It contains all the HTML structure, inline CSS styling, SVG icons, and content (links to projects like Chromascope, Contexta Bot, etc.).
- `CNAME`: Configuration for the custom domain `iser.io`.
- `docs/superpowers/`: Contains the specification (`specs/`) and implementation plans (`plans/`) for the upcoming migration to a full Next.js application.
- `README.md` / `CLAUDE.md`: Aspirations/documentation for the *future* state of the project.

## Building and Running

Because this is currently a pure static HTML project without a build step, there are no dependencies to install.

To view the site locally, you can use any simple HTTP server. For example:

```bash
# Using Python
python -m http.server 3000

# Using Node.js (npx)
npx serve .
```

Then, open `http://localhost:3000/index.html` in your browser.

## Development Conventions

- **Current Static Editing:** Any changes to the site's content, links, or styles must be made directly within `index.html`.
- **Future Migration:** Work is planned to migrate this static file into a Next.js App Router application. Before writing Next.js code, consult the plans in `docs/superpowers/plans/2026-04-02-personal-blog.md`.
