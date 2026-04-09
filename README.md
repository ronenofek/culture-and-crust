# Culture & Crust

An editorial website exploring the intersection of ancestral craft and modern culinary science — sourdough baking, lacto-fermentation, kitchen technique, and the philosophy behind slow food.

Live site: **[ronenofek.github.io/culture-and-crust](https://ronenofek.github.io/culture-and-crust)**

---

## Pages

| File | Section | Description |
|---|---|---|
| `index.html` | Home | Landing page with hero, Four Pillars navigation tiles |
| `bakery.html` | The Bakery | 75% hydration sourdough batard — full recipe with phases |
| `ferments.html` | The Ferments | Lacto-fermented red plums — methodology and brine mechanics |
| `kitchen.html` | The Kitchen | Plum-brine glazed cod — links back to ferments |
| `essence.html` | The Essence | Editorial essay on salt, time, and fermentation philosophy |
| `equipment.html` | Equipment | Curated tool guide with Amazon affiliate links |
| `style.css` | Global | Shared design tokens, nav, footer, tech-hud, pillar colors |

---

## Running Locally

No build step or install needed. All dependencies load from CDN.

**Quickest option — just open the file:**
```
Double-click index.html
```

**If browser blocks local navigation between pages, use Python's built-in server:**
```bash
cd path/to/Website-fermentation
python -m http.server 8000
```
Then visit `http://localhost:8000`

**Or use VS Code Live Server:**
Right-click `index.html` → *Open with Live Server*

---

## Tech Stack

- **HTML** — static, no framework
- **Tailwind CSS** — loaded via CDN with inline config
- **Google Fonts** — Noto Serif, Work Sans, Space Grotesk
- **Material Symbols** — icon set via Google CDN
- **style.css** — global system layer on top of Tailwind

---

## Design System

### Pillar Colors
| Pillar | Color | Hex |
|---|---|---|
| The Bakery | Golden Crust | `#F39C12` |
| The Ferments | Vibrant Beet | `#C70039` |
| The Kitchen | Deep Umber | `#5D4037` |
| The Essence | Fresh Sage | `#27AE60` |

### Key CSS Classes (style.css)
- `.glass-nav` — frosted glass navigation bar
- `.tech-hud` / `.tech-hud__label` / `.tech-hud__value` — monospace data display cards
- `.path-link` — cross-page CTA arrows (e.g. ferments → kitchen)
- `.page-bakery` / `.page-ferments` / etc. — body class sets `--pillar-accent` variable
- `.scroll-target` — anchor offset for fixed nav

### Cross-Page Loop
`ferments.html` → `kitchen.html#recipe-glazed-cod` (the plum brine becomes the glaze)
`kitchen.html` → `ferments.html#ferment-recipe` (View Ferment Guide)

---

## Deploying Updates

```bash
cd path/to/Website-fermentation
git add .
git commit -m "describe your change"
git push
```

GitHub Pages auto-deploys from the `main` branch within ~60 seconds.

---

## To Do

- [ ] Add newsletter / Journal signup backend
- [ ] Mobile hamburger menu
- [ ] Search functionality
- [ ] More recipes and ferment entries
- [ ] Dark mode toggle
