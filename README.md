# website

Bonzai marketing / landing website.

A single-file, dependency-free static landing page (`index.html`) for Bonzai — private
family banking that grows branch by branch. Imported from the Claude Design project
"Bonzai" (`Bonzai Site.dc.html`, Editorial hero variant) and converted to a standalone
site: the design-canvas template directives (`sc-if` / `sc-for` / `{{ }}` bindings) were
resolved into real HTML, and the motion, counters, balance-line chart, FAQ accordion, and
waitlist form were reimplemented in vanilla JS.

## View locally

It's a static file — just open it:

```bash
open index.html
# or serve it
python3 -m http.server 8080   # then visit http://localhost:8080
```

No build step or dependencies. Fonts load from Google Fonts at runtime.
