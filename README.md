# Lazar Milicevic - Portfolio

Professional portfolio website for Customer Success & Technical Support Engineer positions.

## Quick Start

### Local Development

Simply open `index.html` in your browser - no build process required.

```bash
# Or use a simple server
npx serve .
# or
python -m http.server 8000
```

## Deployment

### GitHub Pages

1. Create a new repository on GitHub

```bash
git init
git add .
git commit -m "Initial portfolio commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/portfolio.git
git push -u origin main
```

2. Go to repository Settings > Pages
3. Select "main" branch as source
4. Your site will be live at `https://YOUR-USERNAME.github.io/portfolio`

### Vercel Deployment

**Option 1: CLI**

```bash
npm i -g vercel
vercel login
vercel              # Preview deployment
vercel --prod       # Production deployment
```

**Option 2: GitHub Integration**

1. Go to [vercel.com](https://vercel.com)
2. Import your GitHub repository
3. Vercel will auto-detect settings
4. Click Deploy

Your site will be available at `https://your-project.vercel.app`

### Custom Domain (Vercel)

1. Go to Project Settings > Domains
2. Add your domain (e.g., `lazarmilicevic.com`)
3. Update DNS records as instructed:
   - A Record: `76.76.19.19`
   - CNAME: `cname.vercel-dns.com`

## File Structure

```
/
├── index.html          # Main portfolio (single file)
├── README.md           # This file
├── vercel.json         # Vercel configuration
├── .gitignore          # Git ignore rules
├── CUSTOMIZATION.md    # Customization guide
└── cv.pdf              # Your CV (add this)
```

## Features

- Single HTML file with inline CSS/JS
- Dark mode (default) with light mode toggle
- Responsive design (mobile-first)
- Animated skill bars and counters
- Smooth scroll navigation
- Expandable case studies
- SEO optimized
- Print-friendly styles
- Accessibility features (ARIA, keyboard nav)

## Customization

See [CUSTOMIZATION.md](CUSTOMIZATION.md) for detailed instructions on how to update content, colors, and add your personal information.

## Performance

- Total size: ~50KB (uncompressed)
- No external dependencies (except Google Fonts)
- Single HTTP request for main content
- Lazy-loaded animations

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

Personal use - All rights reserved.

---

Built for Customer Success & Technical Support positions at Automattic, Support Adventure, and aThemes.
