# website

Bonzai marketing / landing website.

A single-file, dependency-free static landing page (`index.html`) for Bonzai —
financial control for businesses and households: one Root account with total
control over every card it issues. Imported from the Claude Design project
"Bonzai" (`Bonzai Site.dc.html`, Editorial hero variant) and converted to a
standalone site: the design-canvas template directives (`sc-if` / `sc-for` /
`{{ }}` bindings) were resolved into real HTML, and the motion, counters,
balance-line chart, and FAQ accordion were reimplemented in vanilla JS
(with `prefers-reduced-motion` support and a mobile hamburger nav).

Sections: hero, stat band, how it works (4 steps), AI insights (animated
balance-line chart), features, security, **About Us / founding team**, waitlist
(email CTA), FAQ, footer.

## Pages / routes

Clean URLs are served as directories (`<route>/index.html`), so they work under
the custom domain at the site root. Sub-pages reference assets with root-absolute
`/uploads/...` paths and link "Back to site" to `/`.

- `/` — landing page (`index.html`)
- `/cvs` — founding team with CV (PDF) + LinkedIn links
- `/product-demo` — Product Demo video (YouTube embed)
- `/pitch-video` — Pitch Video (YouTube embed)
- `/pitch-slides` — Pitch Deck (embedded PDF; falls back to "coming soon" if the PDF is absent)

## Assets

`uploads/` is organized into brand marks (root), founder photos, CVs, and
business documents:

```
uploads/
  logo_color.png, logo_dark.png, logo_green.png   # brand marks + favicon
  pictures/  taha.jpg, tajwaar.jpg, farhan.jpg     # founder photos
  cvs/       Syed-Taha-Ali-CV.pdf, Tajwaar-Shafiq-CV.pdf, Mohamed-Farhan-Feroz-CV.pdf
  docs/      Bonzai-Pitch-Deck.pdf                 # business documents
```

Each founder `<img>` falls back to a styled initials avatar via `onerror`, so a
missing photo degrades gracefully rather than showing a broken image. Video
embeds: Product Demo `youtu.be/9AXX1CwQks0`, Pitch Video `youtu.be/aHXKYE0wVFo`.

## View locally

It's a static file — just open it:

```bash
open index.html
# or serve it
python3 -m http.server 8080   # then visit http://localhost:8080
```

No build step or dependencies. Fonts load from Google Fonts at runtime.
