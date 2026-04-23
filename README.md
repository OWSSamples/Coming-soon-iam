<div align="center">

# Opendex — Coming Soon

**High-performance "coming soon" landing page for [opendex.dev](https://opendex.dev)**

![Next.js](https://img.shields.io/badge/Next.js-14-black?logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?logo=tailwindcss&logoColor=white)
![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-deployed-F38020?logo=cloudflare&logoColor=white)
![License](https://img.shields.io/badge/license-private-red)

</div>

---

## Overview

Minimal, animated landing page built to hold the domain while the full Opendex platform is under development. It features a fluid animated background, GSAP-powered entrance animations, automatic dark/light theming, and a production-ready SEO setup — all shipped as a static export to Cloudflare Pages.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | [Next.js 14](https://nextjs.org/) (App Router, static export) |
| Language | TypeScript 5 |
| Styling | Tailwind CSS 3 + CSS keyframe animations |
| Animations | [GSAP 3](https://gsap.com/) + SplitType |
| 3D / WebGL | Three.js · @react-three/fiber · @react-three/drei |
| UI Primitives | Radix UI · shadcn/ui |
| Package Manager | [Bun](https://bun.sh/) |
| Deployment | [Cloudflare Pages](https://pages.cloudflare.com/) via Wrangler |

---

## Features

- **Animated background** — CSS keyframe blobs/particles with subtle looping motion
- **GSAP animations** — Smooth entrance animations that respect `prefers-reduced-motion`
- **Auto dark / light theme** — Driven by the user's system preference (`prefers-color-scheme`)
- **Fully responsive** — Fluid layout across all screen sizes
- **Production SEO** — Open Graph, Twitter Card, structured metadata, `robots.txt`, `manifest.json`
- **Facebook domain verification** — Meta tag included for `opendex.dev`
- **Perfect Lighthouse score target** — Static export with no server-side overhead

---

## Getting Started

### Prerequisites

- [Bun](https://bun.sh/) `>= 1.3.8`
- Node.js `>= 20`

### Install dependencies

```bash
bun install
```

### Run development server

```bash
bun dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Type-check

```bash
bun typecheck
```

### Build for production

```bash
bun build
```

The output is a fully static site exported to the `out/` directory.

---

## Deployment

The project deploys to **Cloudflare Pages** using Wrangler.

### Preview deployment

```bash
bun deploy
```

### Production deployment (`main` branch)

```bash
bun deploy:prod
```

> Requires a Cloudflare account and `wrangler` authenticated via `wrangler login`.

---

## Project Structure

```
src/
├── app/
│   ├── globals.css       # Global styles & CSS custom properties
│   ├── layout.tsx        # Root layout — metadata, viewport, fonts
│   └── page.tsx          # Landing page entry point
├── components/
│   ├── Beams.jsx         # Animated beam background component
│   └── ui/               # shadcn/ui primitives (Button, Card, Badge, Input)
└── lib/
    └── utils.ts          # Shared utility helpers (cn, etc.)
docs/
└── blueprint.md          # Design brief & style guidelines
public/
├── manifest.json         # Web app manifest
├── robots.txt
├── _headers              # Cloudflare Pages custom headers
└── _redirects            # Cloudflare Pages redirect rules
```

---

## Design Tokens

| Token | Value | Usage |
|---|---|---|
| Primary | `#006AFF` (Zodiac Blue) | CTAs, accents |
| Background (light) | `#E5F0FF` | Page background |
| Background (dark) | `#111728` | Dark mode background |
| Accent | `#00ADA0` (Atoll) | Highlights, hover states |
| Font | `Inter` (Google Fonts) | All text |

---

## License

Private — © 2026 [Opendex Web Services](https://opendex.dev). All rights reserved.

