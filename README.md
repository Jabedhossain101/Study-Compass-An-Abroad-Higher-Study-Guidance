# Study Compass — Website Design (HTML/CSS)

A fully responsive, static HTML/CSS prototype of the Study Compass platform,
covering 6 screens in one file (switch between them with the dark bar at the top):

1. Landing page
2. Student dashboard
3. University search
4. Application tracker
5. Community forum
6. Admin dashboard

## Structure
```
study-compass/
├── index.html      → all 6 screens (markup)
└── css/
    └── style.css    → design tokens + all styling + responsive rules
```

## Opening it
Just open `index.html` in a browser, or use the VS Code "Live Server" extension
for auto-reload while editing.

## Editing tips
- All colors, fonts, and spacing are defined as CSS variables at the top of
  `style.css` inside `:root { ... }` — change a value there to restyle the
  whole site at once (e.g. `--primary`, `--gold`, `--radius-m`).
- Fonts (Fraunces for headings, Public Sans for body/UI) are loaded from
  Google Fonts via the `<link>` tags in `index.html`'s `<head>`.
- Each screen is a `<section class="screen" id="...">` in `index.html`.
  The prototype nav bar at the top toggles which one is visible — remove
  `.proto-bar` and the `showScreen()` script at the bottom if you want to
  ship these as separate real pages instead of one switchable file.
- Responsive breakpoints: 980px (tablet), 720px (mobile — app screens switch
  to a horizontal top nav), and 480px (small phones). They're grouped at the
  bottom of `style.css`.


