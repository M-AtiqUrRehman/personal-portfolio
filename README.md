# Atiq ur Rehman — Frontend Developer Portfolio

A premium, fully responsive personal portfolio built with **plain HTML5, CSS3, and vanilla JavaScript (ES6+)** — no frameworks, no build step. Designed around a "developer's terminal" visual identity: a dark editor-inspired palette, monospace structural accents, and a hero terminal card as the page's signature element.

🔗 **Live demo:** _add your deployed URL here once published_

---

## ✨ Features

- Dark, glassmorphism-accented theme with a blue/violet gradient accent
- Sticky navbar with active-section highlighting (via `IntersectionObserver`)
- Boot-sequence loading animation
- Scroll-reveal animations on every section
- Animated skill bars and animated statistic counters
- Responsive project grid with hover/focus reveal overlays
- Client-side validated contact form (no backend wired up — see below)
- Scroll-to-top button, custom scrollbar, smooth scrolling
- Mobile-first responsive layout — no horizontal scroll at any breakpoint
- Respects `prefers-reduced-motion`
- Semantic HTML, visible focus states, and `aria-live` form feedback for accessibility

---

## 📁 Project Structure

```
portfolio/
├── index.html
├── css/
│   ├── variables.css      # design tokens: color, type, spacing, shadows
│   ├── base.css            # reset + global typography + scrollbar
│   ├── layout.css          # navbar, hero, section scaffolding, grids
│   ├── components.css      # buttons, cards, terminal card, forms
│   ├── animations.css      # keyframes + scroll-reveal classes
│   └── responsive.css      # breakpoints (1100 / 880 / 600 / 380px)
├── js/
│   ├── loader.js           # boot-sequence loading animation
│   ├── navigation.js       # sticky navbar, mobile menu, active link
│   ├── animations.js       # scroll reveal, scroll-to-top, ripple, counters
│   ├── skills.js           # animated skill bar fills
│   ├── projects.js         # reserved for future dynamic project loading
│   ├── contact-form.js     # validation + simulated submit
│   └── main.js             # footer year, reduced-motion sync
├── assets/
│   ├── images/             # SVG project thumbnails (placeholders)
│   └── icons/               # favicon
├── resume/
│   └── Atiq_ur_Rehman_Resume.pdf   # placeholder résumé — replace with your own
└── README.md
```

---

## 🚀 Getting Started Locally

No build tools or package manager required.

```bash
# Option 1: just open it
open index.html          # macOS
start index.html         # Windows

# Option 2: serve it (recommended, avoids any file:// quirks)
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## 🛠 Customizing

| What | Where |
|---|---|
| Name, role, bio, links | `index.html` — Hero, About, Contact sections |
| Colors / fonts / spacing | `css/variables.css` |
| Skills & percentages | `index.html` — Skills section (`data-level` attribute on `.skill-bar__fill`) |
| Projects | `index.html` — Projects section, plus matching SVGs in `assets/images/` |
| GitHub stats | `index.html` — GitHub Statistics section (`data-count` attributes). Currently static placeholders — wire up the [GitHub REST API](https://docs.github.com/en/rest) or [github-readme-stats](https://github.com/anuraghazra/github-readme-stats) for live data |
| Résumé file | Replace `resume/Atiq_ur_Rehman_Resume.pdf` with your real résumé, same filename (or update the `href` in `index.html`) |
| Contact form backend | `js/contact-form.js` — the `simulateSubmit()` function is a placeholder. Swap in a real `fetch()` call to your API, or a form service like [Formspree](https://formspree.io) or [Netlify Forms](https://docs.netlify.com/forms/setup/) |

---

## 🌐 Deployment

### GitHub Pages
1. Push this folder to a GitHub repository.
2. In the repo: **Settings → Pages → Source** → select your branch (e.g. `main`) and root folder.
3. Save. Your site will be live at `https://<username>.github.io/<repo-name>/` within a minute or two.

### Netlify
1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Deploy manually**.
2. Drag and drop the `portfolio` folder (or connect your GitHub repo for continuous deployment).
3. Netlify auto-detects this as a static site — no build command needed. Leave **Build command** blank and **Publish directory** as the repo root (or `portfolio` if nested).

### Vercel
1. Go to [vercel.com/new](https://vercel.com/new) and import your GitHub repository.
2. Framework Preset: choose **Other** (static site).
3. Leave Build Command and Output Directory blank/default — Vercel will serve `index.html` directly.
4. Deploy.

---

## ♿ Accessibility & Performance Notes

- All interactive elements are keyboard reachable; focus states are visible (`:focus-visible`).
- The contact form announces errors via `role="alert"` and submission status via `aria-live="polite"`.
- A skip link lets keyboard users jump straight to main content.
- Animations are disabled when the OS-level `prefers-reduced-motion` setting is on.
- Images use `loading="lazy"` and explicit `width`/`height` to avoid layout shift.
- Project thumbnails are inline SVG — zero network requests, crisp at any resolution.

---

## 📄 License

Free to use and adapt for your own portfolio.
