# Design System: personal_portfolio

Character: warm print-shop editorial — a paper résumé that happens to be interactive. Confident type, one green, technical mono details.

## Character block (visual-character axes)
- **Type:** high contrast. Archivo 800 display (hero clamps 44–80px, −0.035em) against Space Grotesk 16px body — ratio well past 2.5×. JetBrains Mono carries all labels/metadata in 10–11px uppercase. Three families, each with one job.
- **Color:** signature green `#2f6a43`, reserved for the primary action, active states, and key accents. Warm paper neutrals (`#f7f5ef` bg, `#15140f` ink) — deliberately not framework gray; the page reads as printed stock.
- **Space:** airy editorial with compression inside groups (4–10px) and release between sections (60–96px bands). Base grid 4px going forward; legacy off-grid paddings are tolerated but new values must snap.
- **Finish:** 1px borders are the separation language. The single deep shadow (`--shadow`) is *focal elevation only*: the detail pane and the portrait. Nothing else casts a shadow.

## Color
- `--paper #f7f5ef` / `--paper2 #efece3` / `--card #fffefb`: warm off-whites; the page should feel like paper stock, not a screen
- `--ink #15140f` / `--ink2 #33302a` / `--muted #615b51` / `--dim #938c7f`: warm text ramp, four steps of receding emphasis
- `--line #e2ddd1` / `--line2 #d2ccbd`: warm hairlines; `--line2` where the edge must be firmer (interactive borders)
- `--green #2f6a43` (hover `--green2 #265636`, wash `--green-soft` / `--green-tint`): the one signature. Primary action + the single thing that must be found. Strip it and the page still works in neutrals.
- `#e0a92e` (star): the only non-green accent, meaning "featured" and nothing else

## Typography
- `--arch` Archivo 700–900: display and headings; contrast lives in weight + size
- `--sans` Space Grotesk 400–600: body, 16px/1.6
- `--mono` JetBrains Mono 400–500: labels, kickers, metadata, buttons — always uppercase + letterspaced
- Scale — mono micro: **10 / 11** (+ 12 for inline `code` only); body: **13 / 14 / 15 / 16 / 17 / 20**; display: **16 / 18 / 20 / 24 / 32** + hero/contact clamps. No in-between sizes; a new size is an extension, propose it here first.

## Spacing
- Base 4px; scale 4 / 8 / 12 / 16 / 20 / 24 / 32 / 40 / 64+ for section bands
- Rhythm: tight within a group (gap 4–12), generous between groups (24–40), grand between bands (84–96)

## Shape & elevation
- Radii tokens: `--r-s 8px` (buttons, inputs, chips, thumbs) · `--r-m 12px` (cards, rail items, browser frames) · `--r-l 16px` (detail pane, portrait) · `--r-pill 999px` (status pills, tags, badges) · 50% for dots
- Separation: **borders**, 1px `--line`/`--line2`. `--shadow` appears on exactly two surfaces: `.detail` and `.photo` (plus the lightbox overlay image). Shadows anywhere else are off-system.

## Motion
- 150ms micro (hovers, caption swaps) / 200ms small transforms / 350ms pane swap / 600ms reveal; ease and cubic-bezier(.2,.7,.3,1) for the pane
- `prefers-reduced-motion` disables the brand-mark animation; keep honoring it for any new animation

## Components
- Button: primary = green fill, white mono text; ghost = 1px `--line2` border, green on hover. Both `--r-s`, mono 11px uppercase
- Status pill: `--r-pill`, mono 10px uppercase; filled green = venture, soft green = live/professional, paper = in-progress
- Card / rail item: `--card` bg, 1px `--line`, `--r-m`; active = green border + 4px green left bar (no shadow)
- Browser frame: `--r-m`, `--paper2` bar, three `--line2` dots

## Voice
- Kickers and metadata in mono uppercase; headings are short declaratives with a period ("Browse the projects."). Buttons are verbs with a trailing →.
