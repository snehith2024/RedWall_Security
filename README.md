# RedWall Security — Website

A production-grade cybersecurity startup website built with pure HTML, CSS, and JavaScript.
No build tools required. Deploy in seconds.

---

## 🗂 Project Structure

```
redwall-security/
└── index.html          # Complete single-file website (all pages, styles, logic)
```

All CSS, JavaScript, and HTML live in one optimized file — zero dependencies,
zero build step, instant load.

---

## 🚀 Run Locally

**Option A — Direct open**
```bash
open index.html
# or double-click the file in your file manager
```

**Option B — Local dev server (recommended)**
```bash
# Python 3
python3 -m http.server 8080
# visit http://localhost:8080

# Node.js (npx)
npx serve .
# visit http://localhost:3000
```

---

## ☁️ Deploy to Vercel

```bash
npm i -g vercel
cd redwall-security
vercel
```
Follow the prompts. Your site will be live at `https://redwall-security.vercel.app`
(or a custom domain you configure).

---

## 🌐 Deploy to Netlify

**Drag & Drop (fastest):**
1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag the `redwall-security/` folder onto the page
3. Done — live URL generated instantly

**CLI:**
```bash
npm i -g netlify-cli
netlify deploy --prod --dir .
```

---

## 🖥 Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/redwall-security.git
git push -u origin main
```
Then in GitHub → Settings → Pages → Source: `main` branch → `/root`.

---

## ✨ Pages & Features

| Feature | Details |
|---|---|
| **Home** | Hero with animated terminal, stats, CTA |
| **Services** | 6-card grid with hover effects, process strip |
| **About** | Mission, values, team cards |
| **Contact** | Validated form, live threat feed ticker |
| **Navigation** | Fixed navbar, smooth page transitions |
| **Responsive** | Full mobile layout with hamburger menu |
| **Custom Cursor** | Red dot + ring, follows mouse |
| **Animations** | Fade-slide-up on , card glow on hover |
| **Scanlines** | Subtle CRT overlay for atmosphere |

---

## 🎨 Customization

All design tokens are CSS variables at the top of `<style>`:

```css
:root {
  --red:     #e5000f;   /* Primary accent */
  --black:   #060608;   /* Page background */
  --surface: #0d0d10;   /* Card backgrounds */
  /* ... */
}
```

### To add real form submission:
Replace the `setTimeout` in the form handler with a `fetch()` call to your
backend endpoint, Formspree, or Netlify Forms:

```js
// Netlify Forms: add  data-netlify="true"  to the <form> tag

// Formspree:
const res = await fetch('https://formspree.io/f/YOUR_ID', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ name, email, company, service, message })
});
```

---

## 📦 Upgrade to React / Next.js

When ready to scale, migrate to:
```
next-app/
├── app/
│   ├── page.jsx          # Home
│   ├── services/page.jsx
│   ├── about/page.jsx
│   └── contact/page.jsx
├── components/
│   ├── Navbar.jsx
│   ├── Footer.jsx
│   └── ServiceCard.jsx
└── tailwind.config.js
```
The design system (colors, fonts, spacing) maps directly to Tailwind config.

---

**© 2025 RedWall Security LLC**
