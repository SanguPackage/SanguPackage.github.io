# Midjourney prompts — sangu.be "Blood & Pirate Warband" redesign

Image assets for the landing redesign (see
`docs/superpowers/specs/2026-07-05-sangu-landing-redesign-design.md`).

Each fenced code block = one prompt. Feed this file to the `midjourney-submit` skill,
optionally filtered by a heading substring (e.g. `Background`, `Cards`, `Branding`).

## Consistency workflow
1. Generate **Background** first. Pick the winner, copy its job URL.
2. Append that URL as a style reference — `--sref <url>` — to every other prompt so the
   whole set shares one look. (Swap the `--sref` note in each block below.)
3. Shared palette baked into every prompt: blood-red `#8b0000`, tarnished antique gold,
   bone white, aged sepia parchment, deep charcoal.

## Post-processing notes
- **Background:** keep the center low-contrast — text sits on top. Darken further in an
  editor if needed. Export to `assets/background.jpg`.
- **Favicon:** upscale the 1:1 mark, export square PNG → `favicon.png` (multi-size ICO
  optional via the `create-ico` skill).
- **Cards:** crop to a consistent ratio; retired-project art is desaturated on purpose.
- **Divider/ornaments:** MJ has no true alpha — generate on flat black, key it out, or
  just skip and do dividers in CSS.
- **Fall Guys card** is described generically (no trademark art) — it's decorative only.

---

## Background

Primary full-page atmosphere.

```
A dark weathered pirate sea chart filling the whole frame, aged torn parchment stained with rum and salt, faint nautical map lines, rhumb lines and a corner compass rose, sea-monster marginalia, deep charcoal ground with blood-red ink annotations and tarnished antique-gold trim, deliberately low-contrast toward the center so overlaid text stays readable, moody candlelight, cinematic painterly texture, subtle vignette --ar 16:9 --v 7 --style raw
```

Darker alt.

```
Extreme close-up of ancient blood-stained nautical chart parchment, near-black charcoal tones, ghostly faded map contours and a single dim compass rose, cracked leather and scorched torn edges, faint tarnished-gold filigree in the corners, heavy central shadow for text legibility, ominous candlelit mood, high-detail painterly grain --ar 16:9 --v 7 --style raw
```

## Textures

Seamless parchment for weathered/retired card panels.

```
Seamless tileable aged parchment texture, weathered water-stained sepia vellum, faint coffee rings, subtle paper fibers, torn and scorched edges, muted desaturated tone, flat top-down scan --tile --ar 1:1 --v 7 --style raw
```

## Cards

Four project emblems, one consistent engraved-woodcut-meets-painterly-poster style.
Active projects are vivid; retired projects are faded and cobwebbed.

PirateFlix (active — HTPC).

```
Centered emblem for "PirateFlix", a pirate-themed home cinema: a skull and crossbones wearing 3D cinema glasses set over a ship's wheel, a glowing film-projector beam and film-reel waves behind it, deep charcoal background with blood-red and tarnished-gold accents, engraved woodcut meets painterly movie-poster art, bold iconic emblem composition --ar 3:2 --v 7 --style raw
```

Sanguine Spirits (active — cocktails).

```
Centered emblem for "Sanguine Spirits", a dark elegant pirate cocktail: a crystal coupe filled with deep blood-red drink, skewered cherry and flamed orange peel garnish, an old rum bottle and a dagger resting beside it, a single crimson drip, candlelit baroque still life, charcoal background with blood-red and antique-gold accents, moody painterly style --ar 3:2 --v 7 --style raw
```

TribalWars (retired — weathered).

```
Weathered emblem for a long-retired medieval warband: crossed battle axes over a cracked wooden clan shield bearing a faded blood-red sigil, moss and dust, cobwebs across the metal, muted desaturated sepia tones with dull tarnished gold, engraved woodcut poster style, abandoned-relic mood, dark charcoal background --ar 3:2 --v 7 --style raw
```

Fall Guys (retired — weathered, generic, no trademark art).

```
Weathered retired emblem: round wobbling jellybean contestants tumbling through a chaotic obstacle-course gauntlet, once-bright carnival colors faded to muted dusty sepia, a tarnished golden crown trophy draped in cobwebs, playful yet abandoned mood, dark charcoal background with dull gold accents, painterly poster style --ar 3:2 --v 7 --style raw
```

## Branding

OG / social-share banner (replaces the current `assets/logo.png` share image).

```
Social share banner for "SANGU — Exsanguination": a dark weathered pirate sea chart with a bold central skull-and-crossbones wax seal dripping blood-red, tarnished-gold filigree border, distressed bone-white lettering space in the composition, cinematic candlelit mood, painterly, wide banner layout --ar 40:21 --v 7 --style raw
```

Favicon / brand mark.

```
App icon: a single glossy blood-red droplet shaped like a skull, minimal centered emblem on deep charcoal, thin tarnished-gold rim, bold simple silhouette that stays readable at tiny size, clean vector-like rendering --ar 1:1 --v 7 --style raw
```

## Ornaments

Optional section divider (Still Sailing / Run Aground). Skip if doing dividers in CSS.

```
Horizontal decorative divider ornament: a taut nautical rope with a central anchor flanked by crossed cutlasses, tarnished antique gold on flat black, symmetrical engraved filigree, thin wide banner strip, clean woodcut line art --ar 8:1 --v 7 --style raw
```
