# IncludEdU — includedu.org

The official website for [IncludEdU](https://includedu.org), a 501(c)(3) student-led nonprofit empowering all youth in inclusive education.

## Stack

Static HTML/CSS/JS — deployed on [Vercel](https://vercel.com) with automatic deploys from this repo.

## Files

| File | What it is |
|---|---|
| `index.html` | Main single-page site |
| `hackathon.html` | IncludAI: The Neurodiversity Hackathon page |
| `styles.css` | Design system — colors, fonts, layout, animations |
| `script.js` | Mobile menu, scroll-reveal, footer year |
| `vercel.json` | Deployment config (caching, security headers) |
| `assets/images/` | All site images and team photos |

## Local preview

```powershell
python -m http.server 8000
# then open http://localhost:8000
```

## Deploying

Every push to `master` auto-deploys to [includedu.org](https://includedu.org) via Vercel.
