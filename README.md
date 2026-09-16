# My Portfolio

A personal portfolio site built with Next.js and Tailwind CSS.

[![CI](https://github.com/Menzi-Thami/My-Portfolio/actions/workflows/ci.yml/badge.svg)](https://github.com/Menzi-Thami/My-Portfolio/actions/workflows/ci.yml)

**Live:** https://my-portfolio-five-lyart-52.vercel.app/

## Stack

- **Next.js 15** (Pages Router) with **React 19**
- **Tailwind CSS 3** for styling
- **Headless UI 2** and **react-icons 5** for components and iconography
- Deployed on **Vercel**; also builds to static output for GitHub Pages

Pages: home, services, work, clients, contact.

## Running locally

Node 22 is required — it is pinned in `engines` and `.nvmrc` because Vercel's default
runtime once diverged from the local one and broke the production build while local builds
stayed green.

```bash
npm install
npm run dev     # http://localhost:3000
```

```bash
npm run build   # production build
npm start       # serve the production build
```

## Notes

Tailwind is deliberately held at v3. Version 4's `@import "tailwindcss"` entry point fails
under Next 15's webpack CSS pipeline, and v4 also changes default border, ring and shadow
rendering — a visual migration rather than a drop-in upgrade.

`package.json` has a `lint` script but ESLint is not a dependency, so CI does not run it.

## Licence

[MIT](LICENSE).
