# Bento — Developer Portfolio

A stunning bento grid developer portfolio built with **Astro 6** and **Tailwind CSS v4**. Dark mode by default, zero JavaScript frameworks, and a beautiful CSS Grid layout that makes your work stand out.

[![Built with Astro](https://astro.badg.es/v2/built-with-astro/small.svg)](https://astro.build)

> **[Live Demo](https://grid-sigma-ruby.vercel.app)**

## Features

- **Bento Grid Homepage** - A CSS Grid layout with cards of varying sizes, not another boring hero section
- **Dark Mode Default** - Developers prefer dark. Light mode available via toggle with localStorage persistence
- **Zero JS Frameworks** - Pure Astro components + vanilla JS. Ships almost no JavaScript to the client
- **Animated Counters** - Stats animate on scroll using IntersectionObserver
- **Gradient Hover Effects** - Cards glow with a violet-to-blue gradient border on hover
- **6 Blog Posts Included** - MDX-powered blog with reading time, tags, and related posts
- **Fully Responsive** - Looks great at every breakpoint from 320px to 1440px+
- **SEO Ready** - Meta tags, Open Graph, Twitter cards, JSON-LD Person schema, auto-generated sitemap
- **Self-Hosted Font** - Inter Variable loaded locally with no external CDN calls
- **Performance First** - Sub-second loads, 90+ Lighthouse across all categories
- **Single Config File** - Customize every piece of content from `src/data/site-config.json`
- **Glassmorphism Header** - Backdrop-blur effect appears on scroll
- **Staggered Animations** - Cards fade in with staggered delays on page load

## Pages

| Page | Description |
|------|-------------|
| `/` | Bento grid homepage with hero, stats, projects, skills, social, blog, testimonial, and "currently" cards |
| `/projects` | Filterable project grid with category tabs (All, Web, Mobile, Open Source, SaaS) |
| `/blog` | Blog listing with date, reading time, tags, and excerpts |
| `/blog/[slug]` | Full blog post with prose styling, tags, and related posts |
| `/about` | Extended bio, career timeline, categorized skills, education, and testimonials |
| `/404` | "Lost in the Grid" - themed 404 page with navigation links |

## Quick Start

```bash
# Clone the repo
git clone https://github.com/meggnotec/bento.git
cd bento

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

Open [http://localhost:4321](http://localhost:4321) to see the site.

## Customization

### Content

All content lives in a single config file. Open `src/data/site-config.json` and update:

- **Personal info** - name, title, bio, location, email
- **Social links** - GitHub, Twitter/X, LinkedIn
- **Projects** - title, description, tech stack, links (6 included)
- **Stats** - numbers that matter (projects, experience, commits, users)
- **Skills** - your tech stack with categories (8 included)
- **Testimonials** - quotes from colleagues or clients (3 included)
- **Timeline** - your career history with dates and descriptions
- **Currently** - what you are working on, reading, listening to

### Blog Posts

Add new blog posts as `.mdx` files in `src/content/blog/`:

```yaml
---
title: "Your Post Title"
description: "A brief description for SEO and cards."
date: "2025-04-01"
tags: ["Tag1", "Tag2"]
---

Your content here. Full MDX support with code blocks, images, and more.
```

### Colors

Edit the CSS custom properties in `src/styles/global.css`:

```css
@theme {
  --color-accent-violet: #8B5CF6;
  --color-accent-blue: #3B82F6;
  --color-dark-bg: #09090B;
  --color-dark-card: #18181B;
}
```

## Project Structure

```
bento/
├── public/
│   ├── fonts/              # Self-hosted Inter Variable font
│   ├── favicon.svg         # Bento-themed SVG favicon
│   └── robots.txt
├── src/
│   ├── components/
│   │   ├── bento/          # 10 bento grid card components
│   │   ├── BentoCard.astro # Base card with hover effects
│   │   ├── Header.astro    # Glassmorphism nav with mobile menu
│   │   ├── Footer.astro
│   │   ├── Icons.astro     # All SVG icons (inline, no dependencies)
│   │   ├── SEOHead.astro   # Meta, OG, Twitter, JSON-LD
│   │   └── ThemeToggle.astro
│   ├── content/
│   │   └── blog/           # 6 MDX blog posts
│   ├── data/
│   │   └── site-config.json
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro     # Bento grid homepage
│   │   ├── projects.astro  # Filterable project grid
│   │   ├── about.astro     # Bio, timeline, skills
│   │   ├── 404.astro
│   │   └── blog/
│   └── styles/
│       └── global.css      # Tailwind v4, animations, prose
├── astro.config.mjs
├── package.json
├── theme.json
└── LICENSE (MIT)
```

## Tech Stack

- [Astro 6](https://astro.build) - Static site generator with island architecture
- [Tailwind CSS v4](https://tailwindcss.com) - Utility-first CSS via `@tailwindcss/vite`
- [MDX](https://mdxjs.com) - Markdown with JSX for rich blog posts
- [Inter Variable](https://rsms.me/inter/) - Self-hosted variable font

No React. No Vue. No Svelte. Just Astro.

## Premium Themes

Like Bento? Check out our premium theme collection at **[meggnotec.com](https://meggnotec.com)** - professionally built themes for Astro, Next.js, SvelteKit, Nuxt, and more. Portfolio, ecommerce, blog, SaaS, and documentation themes.

## Contributing

Contributions are welcome. Please open an issue first to discuss what you would like to change.

## License

[MIT](LICENSE) - Use it for personal or commercial projects. Attribution appreciated but not required.

---

If this theme helped you, please consider giving it a star. It helps others discover it and motivates continued development.
