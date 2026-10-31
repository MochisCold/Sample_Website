# Led Zeppelin — Team Portfolio

A single-page, fully static portfolio site built around a classic rock aesthetic: dark
zinc surfaces, amber accents, and a "tracklist" framing for project work.

No build step, no dependencies, no CDN. Open `index.html` and it works.

## Structure

```
.
├── index.html    # All markup: hero, tracklist, lineup, contact, footer
├── styles.css    # Hand-written utility stylesheet (Tailwind-compatible class names)
├── .gitignore
└── README.md
```

## Sections

| Section   | Anchor      | Content                                          |
| --------- | ----------- | ------------------------------------------------ |
| Hero      | —           | Headline, tagline, CTAs                          |
| Tracklist | `#projects` | Featured projects presented as tracks (Side A/B) |
| Lineup    | `#team`     | The four team members (Page, Plant, Jones, Bonham) |
| Contact   | `#contact`  | "Backstage Pass" enquiry form                    |

## Running locally

Just open the file:

```powershell
start index.html
```

Or serve it over HTTP if you prefer:

```powershell
python -m http.server 8000
# then visit http://localhost:8000
```

## Notes on the styling

`styles.css` is a hand-rolled subset of Tailwind utility classes rather than the
compiled framework output, so the page stays readable and offline-safe. A handful of
classes use CSS custom properties for gradient stops:

```css
.bg-gradient-to-r { background-image: linear-gradient(to right, var(--from), var(--via), var(--to)); }
.from-amber-400   { --from: #fbbf24; }
.via-amber-600    { --via: #d97706; }
.to-red-500       { --to: #ef4444; }
```

If you later switch to real Tailwind, the class names in `index.html` already match
Tailwind's vocabulary and will mostly carry over as-is.

## Deploying

The site is static, so GitHub Pages works with no configuration changes:

Settings → Pages → Source: **Deploy from a branch** → `main` / `/ (root)`.
