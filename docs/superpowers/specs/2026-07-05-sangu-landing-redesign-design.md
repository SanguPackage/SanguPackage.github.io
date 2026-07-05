# sangu.be landing redesign — Blood & Pirate Warband

## Goal
Turn the current four-clashing-styles landing page into one coherent, characterful
one-pager. Same content, same scope (single static `index.html` + one CSS file on
GitHub Pages), but it reads as a pirate crew's flag instead of four half-finished
experiments.

## Identity
- **Voice:** weathered pirate warband. Blood (Sangu/Exsanguination), rum, sea-chart.
- **Palette:** dark parchment / sea-chart background, blood-red `#8b0000` + tarnished
  gold accents, bone/off-white text.
- **Ties into:** PirateFlix "Dark Sea-Chart" theme + Sanguine Spirits dark red, so the
  whole project family feels connected.

## Page structure (top → bottom)

### 1. Masthead
- Wordmark: **SANGU** with tagline **Exsanguination**.
- Manifesto line, worn as a badge of honour: `free · open-source (MIT) · ad-free`.

### 2. ⚓ Still Sailing (active crew)
Full-colour, alive (subtle hover life). Four cards:

| Project              | Blurb (draft — refine)                                                             | Link                          |
|----------------------|------------------------------------------------------------------------------------|-------------------------------|
| **PirateFlix**       | A one-step Home Theater PC. Docker hoists the sails; you just watch.                | `https://sangu.be/htpc`       |
| **Sanguine Spirits** | Dark, elegant cocktail recipes. Warriors have taste buds too — pure indulgence.     | `https://sangu.be/Sanguine-Spirits` |
| **Scout**            | Send a scout past the horizon. Open an issue — it sails back with cited, charted findings. | `https://laoujin.github.io/Scout/` |
| **Meridian**         | A logbook of your voyages. Drop in photos and your travels chart themselves across the map. | `https://laoujin.github.io/Meridian/` |

Scout & Meridian use Midjourney gilded-relief crests (`assets/scout.webp`,
`assets/meridian.webp`), matching the PirateFlix emblem style.

### 3. ☠ Run Aground (retired)
Visually weathered / dimmed so "retired" reads instantly — affectionate, not hidden.
Each owns *why* it's retired. Two cards:

| Project        | Blurb (draft — refine)                                                                       | Link                       |
|----------------|----------------------------------------------------------------------------------------------|----------------------------|
| **TribalWars** | Sangu was a TribalWars clan. The tools still work and see use, but the clan has sailed on.    | `https://tribalwars.sangu.be` |
| **Fall Guys**  | Covid-era crown guides. Still pretty accurate — just no longer updated.                        | `https://sangu.be/fallguys` |

### 4. Footer
`Exsanguination · 2015–2026` (kept).

## Tech / constraints
- Static: one `index.html`, one `assets/index.css`. **No build step, no framework.**
- Rework the markup so all four cards share one card component/class (currently each
  card is bespoke). Retire the per-project bespoke styles (TribalWars gold-border
  chrome, Fall Guys cartoon card, inline photo backgrounds).
- Responsive: cards reflow to one column on mobile.
- Keep existing GA snippet and OG/meta tags.
- Hover life on active cards only, and only if it's cheap (CSS-only) and mobile-safe.

## Out of scope
- No changes to the linked sub-sites (PirateFlix, cocktails, tribalwars, fallguys).
- No JS framework, no asset pipeline, no new dependencies.

## Verification
This is a presentational page with no logic, so "tests" = visual verification:
- Render locally and screenshot desktop + mobile widths.
- Confirm all four links resolve to the correct URLs.
- Confirm active vs retired grouping is visually obvious at a glance.

## Open questions
1. Card blurbs above are drafts — approve or tweak wording.
2. Keep the existing `background.jpg`, or want a new sea-chart/parchment background?
   (If new, that's an asset to source/generate separately.)
