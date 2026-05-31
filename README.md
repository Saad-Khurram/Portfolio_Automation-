# Saad Khurram — Portfolio Website

Personal portfolio site built to showcase automation and Python projects, targeting technical recruiters and hiring managers at German startups and SMEs.

## Stack

- **Framework**: Astro (static site, zero runtime JS by default)
- **Styling**: Tailwind CSS
- **Hosting**: Vercel (auto-deploys on push to `main`)
- **Contact form**: Formspree

## Sections

- **Hero** — introduction and what I am looking for
- **Projects** — case studies: customer support automation, RAG pipeline, AI chatbot
- **About** — skills, languages, background
- **CV** — downloadable PDF and inline skills summary
- **Contact** — email form, LinkedIn, GitHub

## Development

```bash
npm install       # Install dependencies
npm run dev       # Start local dev server at localhost:4321
npm run build     # Build for production
npm run preview   # Preview production build locally
```

## Project Structure

```
src/
  components/
    Hero.astro
    Projects.astro
    About.astro
    CV.astro
    Contact.astro
  layouts/
    Layout.astro
  pages/
    index.astro
  styles/
    global.css
public/
  hero-bg.mp4
  logo.svg
```

## Deployment

Connected to Vercel via GitHub integration. Every push to `main` triggers an automatic redeploy.
