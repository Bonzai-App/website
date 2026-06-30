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

## Assets

Brand and team images live in `uploads/` and are referenced relatively:

- `logo_dark.png`, `logo_green.png` — brand marks (nav, footer, waitlist, hero watermark)
- `Taha.jpg`, `Tajwaar Shafiq - Resized.jpg`, `Farhan Feroz - Resized.jpg` — founder photos

Each founder `<img>` falls back to a styled initials avatar via `onerror`, so a
missing photo degrades gracefully rather than showing a broken image.

## View locally

It's a static file — just open it:

```bash
open index.html
# or serve it
python3 -m http.server 8080   # then visit http://localhost:8080
```

No build step or dependencies. Fonts load from Google Fonts at runtime.
