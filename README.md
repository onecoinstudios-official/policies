# One Coin Studios policies

Public privacy policies served with GitHub Pages, styled with the
One Coin Studios brand.

| Page | URL |
| --- | --- |
| Index | `https://onecoinstudios-official.github.io/policies/` |
| Bento Rush privacy policy | `https://onecoinstudios-official.github.io/policies/bento-rush.html` |

## Layout

| Path | Purpose |
| --- | --- |
| `index.html` | Policy index, links to each game's policy |
| `bento-rush.html` | Bento Rush privacy policy (the URL Play Console uses) |
| `assets/` | Generated brand images served by the site |
| `.nojekyll` | Stops GitHub Pages from running Jekyll over the files |

## Brand assets

`assets/` is generated from `/Users/oscar/Desktop/One-Coin-Studios/studio_branding`
(`one-coin-logo.png`, `one-coin-banner.png`). Nothing is drawn by hand, so
keep the source art as the single source of truth and regenerate if it
changes.

| File | Size | Used for |
| --- | --- | --- |
| `one-coin-logo.png` | 512×512 | Header mark on both pages |
| `favicon.png` | 64×64 | Browser tab icon (`rel="icon"`) |
| `apple-touch-icon.png` | 180×180 | iOS home-screen icon |
| `one-coin-banner.png` | 1400×560 | Footer banner, PNG fallback |
| `one-coin-banner.webp` | 1400×560 | Footer banner, served first via `<picture>` |
| `og-image.png` | 1200×630 | Open Graph / Twitter social card |

The logo asset is cropped to the roundel and padded to a square on the
brand cream (`#FBF6EB`) so it sits cleanly in a rounded-corner header badge.

### Palette

Taken from the studio art and used as CSS custom properties:

| Token | Light | Dark |
| --- | --- | --- |
| Paper | `#FBF6EB` | `#1B1216` |
| Ink | `#271B21` | `#FDFCF6` |
| Accent | `#713129` | `#9EDDFF` |
| Gold | `#FCBD39` | `#FCBD39` |
| Sky | `#77D6FD` | `#77D6FD` |

Both pages are single-file HTML with inline CSS and no external fonts,
scripts, or trackers. They honour `prefers-color-scheme` and include
print styles that strip the banner and chrome.

## Publishing

1. Push to `main`.
2. In the repository: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main**, folder: **/ (root)**
3. Wait for the Pages deployment, then open
   `https://onecoinstudios-official.github.io/policies/bento-rush.html`.
4. Paste that URL into Play Console → **App content → Privacy policy**.

If the repository ever moves to a different account or organisation, the
URL prefix changes to `https://<account>.github.io/policies/`. Update
`README.md`, the `rel="canonical"` and `og:url` tags in both HTML pages,
and the game repo's policy references to match.

HTTPS is enforced once GitHub has provisioned the certificate for the
custom Pages domain; the site already serves over HTTPS either way.

## Editing the policy

Edit `bento-rush.html` **and** the source of truth at
`../games/bento_rush/store/privacy_policy.md`, then update the
"Last updated" date in both places and the date shown on `index.html`.
