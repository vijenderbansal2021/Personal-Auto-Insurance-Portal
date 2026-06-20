# AutoQuote FL — Personal Auto Insurance PWA

A complete Progressive Web App for personal auto insurance quoting in Florida ZIP 33545 (Wesley Chapel, Pasco County). Targets drivers aged 16–30 with full telematics-integrated actuarial pricing.

## Features

- **8-step guided quote wizard** with full form validation
- **Live actuarial rating engine** — exact PRD v2.1 factors applied in-browser
- **Telematics Risk Score (TRS)** calculator with real-time 0–100 scoring
- **Auto-underwriting decision engine** — Accept / Refer / Decline logic
- **Full coverage selection** — BI, PD, PIP, UM, COMP, COLL with FL-compliant defaults
- **Offline capable** via Service Worker caching
- **Installable PWA** — works on iOS, Android, and desktop

## Deploy to GitHub Pages (Free)

### Option 1: GitHub Pages (static hosting)

```bash
# 1. Create a new repository on github.com
# 2. Clone it locally
git clone https://github.com/YOUR_USERNAME/auto-quote-portal.git
cd auto-quote-portal

# 3. Copy files into repo
cp index.html sw.js manifest.json .nojekyll README.md ./

# 4. Create icons directory and add icons (or use placeholder)
mkdir icons
# Add icon-192.png and icon-512.png to the icons/ folder

# 5. Push to GitHub
git add .
git commit -m "Initial deploy: AutoQuote FL PWA"
git push origin main

# 6. Enable GitHub Pages
# Go to: Settings → Pages → Source: Deploy from branch → Branch: main → / (root)
# Your site will be live at: https://YOUR_USERNAME.github.io/auto-quote-portal
```

### Option 2: Vercel (recommended for custom domain)

```bash
npm install -g vercel
vercel --prod
# Follow prompts — deploys in under 60 seconds
```

### Option 3: Netlify drag-and-drop

1. Go to https://app.netlify.com
2. Drag the entire folder onto the deploy area
3. Done — live URL provided instantly

## Required Files

```
auto-quote-portal/
├── index.html          ← Main PWA (entire app in one file)
├── sw.js               ← Service Worker for offline support
├── manifest.json       ← PWA manifest
├── .nojekyll           ← Prevents Jekyll processing on GitHub Pages
├── icons/
│   ├── icon-192.png    ← App icon (192×192px)
│   └── icon-512.png    ← App icon (512×512px)
└── README.md           ← This file
```

## Icons

Create icons using any image editor (Canva, Figma, etc.) or use a generator:
- https://realfavicongenerator.net
- Use the shield logo from the app header as your base

## Actuarial Reference

Rates are based on PRD_Auto_Underwriting_33545.docx v2.1:
- Base territory: ZIP 33545, Pasco County, FL (LCM: 1.12)
- Target segment: ages 16–30
- PIP territory: Zone 6 (LCM: 1.18)
- Expense LCM: 1.439 (telematics enrolled) / 1.471 (traditional)
- All age, telematics, credit, mileage, and history factors from PRD

## License

For educational and demonstration purposes. Not a licensed insurance product.
Contact an authorized Florida insurance agent to purchase coverage.
