# IncludEdU — website prototype

A modern, accessible redesign of [includedu.org](https://includedu.org), built from the current
site's content and featuring the **IncludEdU × Stanford NNEA Neurodiversity Awareness Hackathon**.

## Files
| File | What it is |
|---|---|
| `index.html` | The full site (single-page scroller) with all sections |
| `styles.css` | Design system — colors, fonts, layout, animations |
| `script.js` | Mobile menu, scroll-reveal, footer year |
| `WORDPRESS-SETUP.md` | Step-by-step: turn this into a live WordPress site on free hosting |

## Preview it (no install needed)
Just **double-click `index.html`** to open it in your browser. That's it.

Or, for the smoothest experience (live reload), run a tiny local server:
```powershell
# from this folder
python -m http.server 8000
# then open http://localhost:8000
```

## What's included
- Hero, About, What We Do, **Hackathon feature**, Chapters, Materials, Success Stories,
  Team, FAQ, Donate CTA, Contact + form, footer
- Neurodiversity-affirming design touches (rainbow infinity motif, strengths-based copy)
- Responsive (mobile menu) + accessibility (skip link, focus styles, reduced-motion support)

## ⚠️ Placeholders to fill before launch
Search the code for `[` to find them:
- Hackathon **date**, **location/online**, and **registration link**
- Real **success stories** (currently `[Add real story]`)
- **Social media URLs** (Instagram / LinkedIn / Twitter)
- The contact **form action** (`formspree.io/f/your-id` → your real endpoint)

## Next step
You chose the **WordPress** route — open `WORDPRESS-SETUP.md` for the full walkthrough
(free DreamHost nonprofit hosting + Astra/Elementor, with all content ready to paste).
