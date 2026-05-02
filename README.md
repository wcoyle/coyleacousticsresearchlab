# CARL Website — Coyle Acoustics Research Lab

Built with [Astro](https://astro.build) · Deployed on [Netlify](https://netlify.com)

## Project structure

```
carl-website/
├── public/
│   └── favicon.svg          ← Swap with your real logo
├── src/
│   ├── layouts/
│   │   └── Layout.astro     ← Nav + footer (edit links/contact here)
│   ├── pages/
│   │   ├── index.astro      ← Homepage
│   │   ├── research.astro   ← Research projects
│   │   ├── team.astro       ← Team + alumni
│   │   ├── news.astro       ← News & updates
│   │   ├── publications.astro ← Publications list
│   │   └── join.astro       ← Open positions + contact
│   └── styles/
│       └── global.css       ← Design system (colors, buttons, utilities)
├── astro.config.mjs
└── package.json
```

## Getting started

### 1. Install dependencies
```bash
npm install
```

### 2. Run locally
```bash
npm run dev
```
Visit `http://localhost:4321` in your browser.

### 3. Build for production
```bash
npm run build
```

## Deploying to Netlify

1. Push this folder to a GitHub repository
2. Go to [netlify.com](https://netlify.com) → "Add new site" → "Import from Git"
3. Connect your GitHub repo
4. Set build command: `npm run build`
5. Set publish directory: `dist`
6. Click Deploy — done!

Every time you push to GitHub, Netlify auto-deploys.

## Customizing content

### Colors
All colors are in `src/styles/global.css` under `:root`. The main ones are:
- `--navy`  → `#1B2D6B`
- `--gold`  → `#EAA020`

### Adding a team member
Open `src/pages/team.astro` and add an entry to the `members` array:
```js
{ initials: 'XY', name: 'Your Name', role: 'PhD Student, yr 1', area: 'Your research area' }
```

### Adding a news post
Open `src/pages/news.astro` and add to the `posts` array at the top.

### Adding a publication
Open `src/pages/publications.astro` and add to the `pubs` array.

### Custom domain
In Netlify: Site settings → Domain management → Add custom domain.
Your university IT can point `carllab.rollins.edu` (or similar) at Netlify.

## Adding your logo image

Replace `public/favicon.svg` with your actual logo file.
To add the logo to the nav, edit `src/layouts/Layout.astro` and add an `<img>` tag.
