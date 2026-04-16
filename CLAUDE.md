# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal portfolio website for Saad — a bachelor's student specializing in n8n workflow automation and Python. The site targets technical recruiters and hiring managers at German startups and SMEs looking for Werkstudent automation talent.

Planned stack: **Astro** (framework) + **Tailwind CSS** (styling) + **Vercel** (hosting) + **Formspree** (contact form).

## Development Commands

Once the Astro project is scaffolded, these will be the standard commands:

```bash
npm run dev        # Start local dev server (localhost:4321)
npm run build      # Production build to ./dist
npm run preview    # Preview the production build locally
npm run astro      # Run Astro CLI commands
```

## Architecture

The site is a static Astro project — no backend, no CMS. Key design decisions:

- **Zero runtime JS by default**: Astro ships zero JS unless a component explicitly uses a client directive (`client:load`, `client:visible`, etc.)
- **Contact form**: Handled by Formspree (external service) — no backend required
- **Deployment**: CI/CD via Vercel's GitHub integration; every push to `main` deploys automatically
- **Content**: Project case studies are authored as Astro component data or markdown files — no CMS

### Planned Sections

1. **Hero** — who Saad is, what he does, what he's looking for
2. **Projects** — 2–3 case studies (customer support automation, RAG pipeline, AI chatbot), each with problem statement, how it works, business impact, links to GitHub/demo/n8n JSON
3. **About** — skills (n8n, Python), languages (German B1, English), personal narrative
4. **CV** — downloadable PDF + inline skills summary
5. **Contact** — Formspree email form, LinkedIn, GitHub

## BMAD Workflow

This project uses the BMAD planning framework. Planning artifacts live in `_bmad-output/`:

- `planning-artifacts/` — product brief, PRD, epics, stories
- `implementation-artifacts/` — architecture decisions, implementation plans
- `test-artifacts/` — test plans

The product brief is at `_bmad-output/planning-artifacts/product-brief-portfolio.md` and is the authoritative source for scope, success criteria, and what's intentionally out of V1 scope.

### V1 Out-of-Scope (do not implement)
- Blog/articles section
- German/English language toggle
- CMS or admin interface
- Analytics dashboard
- Paid backend infrastructure
