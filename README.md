# Bento Grid Portfolio

A stunning bento grid developer portfolio built with Astro 6 and Tailwind CSS v4. Dark-first design with violet-blue gradient accents, perfect for developers and designers who want a modern, eye-catching portfolio.

![Preview](/.qc-screenshots/home-dark.png)

## Features

- **Bento Grid Layout** — CSS Grid with responsive breakpoints (1→2→4 columns)
- **Dark Mode Default** — Beautiful dark theme with light mode toggle
- **Fully Responsive** — Tested at 320px, 768px, 1024px, and 1440px
- **Blog** — Markdown-powered blog with Content Collections
- **SEO Ready** — Meta tags, Open Graph, sitemap, robots.txt
- **Zero Dependencies** — No icon fonts, no external CDN calls
- **Performance** — Static output, optimized builds

## Pages

- Home (bento grid)
- Projects
- Blog (listing + individual posts)
- About
- Contact
- 404

## Quick Start

```bash
npm install
npm run dev
```

Open [http://localhost:4321](http://localhost:4321) to view the site.

## Build

```bash
npm run build
npm run preview
```

## Customization

Edit `src/data/site-config.json` to change:
- Name, title, bio
- Social links
- Navigation items
- Stats

Edit `src/data/projects.json` to update the project showcase.

Add blog posts as Markdown files in `src/content/blog/`.

### Colors

All colors are CSS custom properties defined in `src/styles/global.css`:

```css
:root {
  --bg: #09090B;
  --card: #18181B;
  --border: #27272A;
  --text: #FAFAFA;
  --muted: #A1A1AA;
  --accent-violet: #8B5CF6;
  --accent-blue: #3B82F6;
}
```

## Folder Structure

```
src/
├── components/     # Header, Footer, ThemeToggle, SkillIcon, ProjectCard
├── content/        # Blog posts (Markdown)
├── data/           # site-config.json, projects.json
├── layouts/        # BaseLayout
├── pages/          # All routes
└── styles/         # global.css (Tailwind + CSS variables)
```

## Tech Stack

- [Astro](https://astro.build) 6.x
- [Tailwind CSS](https://tailwindcss.com) 4.x
- [MDX](https://mdxjs.com) support
- Self-hosted Inter variable font

## License

MIT
