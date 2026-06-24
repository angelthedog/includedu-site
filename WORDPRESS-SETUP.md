# IncludEdU → WordPress setup guide

This guide turns the prototype in this folder (`index.html`) into a live WordPress site on
**free nonprofit hosting**, keeping your domain `includedu.org`.

> The prototype is the **design spec**. You don't have to match it pixel-for-pixel — it shows
> the target look (colors, fonts, sections, the hackathon feature) so the WordPress build has a
> clear goal.

---

## 0. What you'll need (one-time)
- ✅ IncludEdU's **501(c)(3)** determination letter (you have this)
- ✅ Access to the **includedu.org domain** (wherever it's registered)
- A **TechSoup** account (free) — validates your nonprofit status: https://www.techsoup.org

---

## 1. Get free hosting (DreamHost for nonprofits)
DreamHost gives **free hosting for the lifetime of the account** to US 501(c)(3)s, with 1-click
WordPress, free SSL, and free migrations.

1. Go to DreamHost's nonprofit program and apply with your 501(c)(3) details.
2. Once approved, open the panel → **WordPress → Install WordPress** (1-click).
3. Point `includedu.org` to DreamHost (update nameservers at your registrar). DreamHost support
   will do this migration for you for free if you ask.

> Alternative (also free, no host needed): **Netlify** or **Cloudflare Pages** can host the
> prototype's HTML/CSS/JS *as-is* — drag the folder in and you're live in minutes. Choose this if
> you decide you don't need WordPress's editor. (You picked WordPress, so the steps below assume it.)

---

## 2. Pick the theme + builder
To reproduce the prototype's look fast, use a **block theme + Elementor** (free) or a flexible
starter theme:

- **Recommended:** Theme **"Astra"** (free) + **Elementor** (free) — closest to a drag-and-drop,
  Wix-like editing experience with full design control.
- **Lighter option:** the default block theme **"Twenty Twenty-Four"** + the built-in Site Editor.

Install: WP Admin → **Appearance → Themes → Add New** → search "Astra" → Activate.
Then **Plugins → Add New** → "Elementor" → Activate.

---

## 3. Match the design tokens
Set these in the theme's **Global Settings** (Elementor → Site Settings, or Astra → Customize) so
everything inherits the right look:

| Token | Value |
|---|---|
| Primary | `#4f46e5` (indigo) |
| Secondary | `#8b5cf6` (violet) |
| Accent | `#f59e0b` (amber) / `#ec4899` (pink) |
| Ink (text) | `#1a1730` |
| Tint (section bg) | `#f6f5ff` |
| Heading font | **Sora** (700/800) |
| Body font | **Inter** (400/500) |
| Button radius | fully rounded (999px / "pill") |
| Card radius | 18px, soft shadow |

Brand gradient (buttons, accents): `linear-gradient(135deg, #4f46e5, #8b5cf6 55%, #ec4899)`.
Neurodiversity rainbow accent (announcement tag, hackathon top border):
`linear-gradient(90deg,#ef4444,#f59e0b,#eab308,#22c55e,#3b82f6,#8b5cf6)`.

---

## 4. Build the pages (content is ready below)
Recreate these sections as one long Home page (the prototype is a single-page scroller), with the
nav linking to anchors. Plugins to install:

- **Forms:** "WPForms Lite" or "Fluent Forms" (free) — for the contact/hackathon-register form.
- **Donations:** "GiveWP" (free) — connect Stripe/PayPal for tax-deductible donations.
- **SEO:** "Rank Math" or "Yoast" (free).

### Section-by-section content

**Announcement bar:** `IncludEdU × Stanford NNEA Neurodiversity Hackathon — Learn more & register →`

**Hero**
- Eyebrow: `501(c)(3) nonprofit · Student-led · Global`
- Headline: `Empowering All Youth in Education`
- Subtext: `We make learning inclusive for every young person — through community outreach, educational programs, and a worldwide network of volunteer-run chapters.`
- Buttons: `Donate Now` · `Explore Chapters`

**About**
> IncludEdU is a 501(c)(3) nonprofit that specializes in community outreach, educational programs,
> and volunteer coordination. We tailor our services to fit the unique needs of the communities we
> serve, helping them thrive and succeed. Around the world, our chapters unite to promote inclusive
> education for all youth — including neurodivergent learners who deserve a strengths-based approach.

**What We Do** (3 cards): Community Outreach · Educational Programs · Volunteer Coordination
(copy in `index.html`).

**Hackathon (featured)** — dark gradient band with rainbow top border:
- Eyebrow: `Featured Event · In partnership with Stanford NNEA`
- Title: `The Neurodiversity Awareness Hackathon`
- Body: partnership with the **Stanford Network for K-12 Neurodiversity Education and Advocacy (NNEA)**.
- Meta: When `[Date]` · Where `[Location/Online]` · Who `Students & allies` · Cost `Free`
- Tracks: Accessibility tools · Awareness & storytelling · Inclusive EdTech · Design for all minds
- Buttons: `Register Interest` (→ form) · `About Stanford NNEA` (→ https://www.stanfordnnea.com/)
- ⚠️ **Fill in the bracketed `[Date]`, `[Location]`, and registration link before launch.**

**Chapters:** Join a chapter / Start a chapter (two panels).
**Materials:** Learning Guides · Educator Toolkits · Family Resources.
**Success Stories:** two testimonial quotes — *replace the `[Add real story]` placeholders with real ones.*
**Team:** Isabella Guan (Founder & President), Andrew Pan (VP Engineering), Penny Liang (VP Finance),
Wendy Liu (VP Operations), Larry Cui (VP). *Add real headshots when available.*
**FAQ:** four items (in `index.html`).
**Donate CTA + Contact:** email `contact@includedu.org`, phones `+1 (425) 312-3215` /
`+1 (954) 605-3871`, socials Instagram / LinkedIn / Twitter.

---

## 5. Before you launch — checklist
- [ ] Replace all `[bracketed]` placeholders (hackathon date/venue/registration, real stories, social URLs)
- [ ] Connect the form (WPForms) and donations (GiveWP → Stripe/PayPal)
- [ ] Add real photos (team headshots, event/community photos) — biggest single "fancy" upgrade
- [ ] Set up `includedu.org` SSL (free, automatic on DreamHost)
- [ ] Run an accessibility pass (contrast, alt text, keyboard nav) — fitting for a neurodiversity org
- [ ] Add Google Analytics / install Rank Math for SEO

---

## TL;DR
1. Free hosting → **DreamHost nonprofit** (or host the prototype as-is on **Netlify** free).
2. **Astra + Elementor**, apply the color/font tokens above.
3. Rebuild the Home page section-by-section using the ready content here + in `index.html`.
4. Add **WPForms** (forms) + **GiveWP** (donations).
5. Fill placeholders, add real photos, launch on `includedu.org`.
