# GDR Concrete Construction LLC — Homepage

A premium, redesigned homepage for **GDR Concrete Construction LLC**, a concrete repair and
construction contractor in Capitol Heights, MD serving the surrounding DMV. Rebuilt from the
existing site at [concretecontractor-md.com](https://concretecontractor-md.com/), using the
company's **real logo, brand color, and service imagery**.

Built as a fast, dependency-free static site with a full-bleed **background video hero**.

**Live site:** _(GitHub Pages — see repo Settings → Pages)_

---

## Business details
- **Company:** GDR Concrete Construction LLC
- **Phone:** (240) 359-1422
- **Based in:** Capitol Heights, MD 20743
- **Service area:** ~20-mile radius across Prince George's County & the DMV (Hyattsville, New Carrollton, Mount Rainier, Landover, Greenbelt, Laurel, Beltsville, Bladensburg, Camp Springs, Kettering, and more)
- **Tagline:** "The right concrete contractor for your project."
- **Hours:** Mon–Sat 7 AM – 5 PM · Sun closed
- **Offers:** Free estimates; discounts for seniors, military & new customers

## Services
Driveway repair & construction · Sidewalk/walkway repair & construction · Foundation repair ·
Foundation construction · Retaining-wall repair & construction · Concrete flatwork ·
Concrete repair · CMU block services · Bathroom/kitchen remodeling & painting.

## Tech
- Static **HTML + CSS + vanilla JS** — no build step, no framework, no dependencies.
- Google Fonts (Archivo + Inter). Everything else is local.
- Accessible: semantic landmarks, single `<h1>`, keyboard nav, visible focus,
  `prefers-reduced-motion`, descriptive alt text.
- SEO: descriptive title/meta, Open Graph, and `GeneralContractor` JSON-LD with service
  areas, opening hours, and a free-estimate offer.

## Structure
```
index.html            # full homepage
css/styles.css        # design system + all sections + responsive
js/main.js            # fixed/transparent header, mobile menu, scroll reveals, form shell
assets/img/           # real logo + service photos + favicon
assets/video/         # hero background video + poster
```

## Design
**Sky-blue on charcoal** palette drawn from the company's own site accent (`#2EA3F2`). Dark,
transparent header (goes solid on scroll); the company's white wordmark logo (keyed to a
transparent PNG) reads cleanly over the video and the dark nav. Archivo + Inter typography.

## Hero video
Full-bleed, muted, looping background video (`assets/video/hero-720.mp4`, ~0.8 MB, 720p) from
Pexels (free license), with `hero-poster.jpg` as the poster/fallback; reduced-motion users
get the still frame. Plays on mobile and desktop; the transparent nav overlays it.

---

## Notes for the client
- **Logo** — GDR has no real logo, so one was built **as type**: a two-line wordmark
  ("GDR **Concrete** / CONSTRUCTION LLC") in the brand font with a sky-blue accent bar. It's
  pure HTML/CSS, so it stays crisp at any size and is trivial to edit. Swap in a real logo
  image later if one is designed.
- **Photos** — the gallery uses the higher-resolution project photos pulled from the site's
  service pages (real crews finishing driveways, foundation footings, walkways, retaining
  walls). Drop more GDR project photos into `assets/img/` to expand the gallery.
- **Testimonial** — the single review shown is the real one from the source site (Mitchell
  McCarthy). Add more as they come in.
- **Estimate form** — front-end only; wire it to email or a CRM (Formspree, Netlify Forms,
  GHL, etc.) to capture leads.
- Only substantiated facts are used (phone, service area, hours, free estimates, discounts) —
  no invented license numbers, founding year, or review counts.

## Deploy (GitHub Pages)
Settings → Pages → Source: `main` / root. The site publishes at the Pages URL.
Local preview: open `index.html`, or run `python3 -m http.server` in the repo root.
