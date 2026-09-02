# Sunday Swagger — Design System v1.0

**Purpose:** one source of truth for emails, website edits, and ads.
**Built from:** the 8-page Brand Guidelines PDF + style evidence measured from
production Sunday Swagger page markup in this repo.

## Confidence key

Every rule in this document carries one of these tags. Read them — they tell you
what is brand law and what is a designed default you're free to overrule.

| Tag | Meaning |
|---|---|
| `[BRAND]` | Stated in the Brand Guidelines. Do not change without brand approval. |
| `[SITE]` | Measured from production Sunday Swagger page markup. |
| `[SYSTEM]` | Designed here because the guidelines are silent. Overrule freely, then update this doc. |

> **Known gap:** `sundayswagger.com` is blocked by this environment's network
> egress policy, so the live storefront could not be crawled directly. Buttons,
> shadows, radii, spacing and card layout are therefore `[SYSTEM]` — designed to
> match the brand's stated aesthetic, not transcribed from the site. See
> §10 for the two-minute way to close that gap.

---

## 1. Brand foundation `[BRAND]`

**Mission —** Empowering the individual to own it.
**Vision —** We are committed to high-quality products that redefine the new classic.
**Positioning —** Own your swagger.

**Personality:** Daring · Innovative · Inclusive · Confident · Stylish

**The aesthetic rule that governs everything below:**
> "The goal is to keep a clean, modern, and sleek look, while allowing our loud
> designs to speak for themselves."

That is the whole system in one sentence. The product prints are the loud part.
The frame around them — layout, buttons, type, chrome — stays black, white, and
quiet. When in doubt, take color *out*.

**Voice:** confident, warm, funny, never smug. Golf-adjacent but never
gatekeeping ("including you non-golfers out there"). Second person. Short
sentences. Uppercase for the shout, sentence case for the talk.

---

## 2. Color

### 2.1 Primary `[BRAND]`

| Token | Hex | CMYK | Role |
|---|---|---|---|
| `--ss-black` | `#000000` | 0 / 0 / 0 / 100 | The brand. Type, buttons, backgrounds, logo. |
| `--ss-white` | `#FFFFFF` | 0 / 0 / 0 / 0 | The brand. Type, backgrounds, logo. |

> The guidelines print these as `#00000` and `#FFFFF` (five digits). That's a
> typo in the source document; the CMYK and RGB values on the same page confirm
> `#000000` and `#FFFFFF`.

### 2.2 Secondary `[BRAND]`

| Token | Hex | CMYK | Role |
|---|---|---|---|
| `--ss-grey` | `#ECECEC` | 6 / 4 / 4 / 0 | Backgrounds and section separation **only**. Never type. |

### 2.3 Tertiary accents `[BRAND]`

| Token | Hex | CMYK | Contrast vs white | Contrast vs black |
|---|---|---|---|---|
| `--ss-blue`  | `#00B3D8` | 77 / 4 / 11 / 0 | 2.49:1 ❌ | 8.44:1 ✅ AAA |
| `--ss-green` | `#C2FC08` | 29 / 0 / 100 / 0 | 1.22:1 ❌ | 17.22:1 ✅ AAA |
| `--ss-pink`  | `#EE4492` | 0 / 88 / 4 / 0 | 3.57:1 ⚠️ large only | 5.88:1 ✅ AA |

Guidelines usage: *"to be used sparingly and as an accent"* — specifically for
**lines, accents on design elements, or single words in copy**, on black, white,
or grey backgrounds.

### 2.4 The accessibility rules that fall out of those numbers `[SYSTEM]`

These are not style preferences. They're arithmetic, and they matter most in
email and ads where you can't A/B your way out of unreadable type.

1. **Never put white text on blue, green, or pink.** Blue fails at 2.49:1 and
   green at 1.22:1 — green-on-white is effectively invisible.
2. **Accent-filled buttons take black labels.** Black on blue = 8.44:1, on green
   = 17.22:1, on pink = 5.88:1. All pass.
3. **Blue and green as *text* only work on black.** On white they're decoration:
   underlines, rules, dots, fills behind black type.
4. **Pink is the only accent that reads as text on white**, and only at 18px bold
   or 24px regular and up. Below that, use black.
5. **Grey `#ECECEC` is never a text color.** 1.18:1 on white. Background only.
   For muted text use `--ss-text-muted` (`#6B6D70`, 5.9:1).

### 2.5 Print vs digital swatches `[BRAND, reconciliation]`

The color chips printed in the guidelines don't match the spec'd hex on the same
page — they're the CMYK builds converted back to RGB:

| Color | Spec'd hex (use this digitally) | Printed swatch renders as |
|---|---|---|
| Blue | `#00B3D8` | `#1CBFD5` |
| Green | `#C2FC08` | `#B0D235` |
| Pink | `#EE4492` | `#EC048C` |

**Use the spec'd hex for anything on a screen.** Hand the CMYK values to print
vendors. The green is the widest gap — the CMYK build (29/0/100/0) is a much
duller olive-lime than the electric `#C2FC08`; if the electric green matters on a
printed piece, ask the vendor for a spot or extended-gamut match.

### 2.6 Neutral ramp `[SITE + SYSTEM]`

`#F2F2F2`, `#E5E5E5`, `#E0E0E0`, `#D9D9D9` are measured from live storefront
markup (table fills, dividers, borders, hairlines). The rest of the ramp is
designed to fill it out. See `tokens.css`.

---

## 3. Typography

### 3.1 The four typefaces `[BRAND]`

| Role | Typeface | Where to get it | Notes |
|---|---|---|---|
| **Primary / display** | Futura PT Condensed, Extra Bold | Adobe Fonts (Typekit) | Needs a licensed Adobe Fonts web project for the site. |
| **Web alternate display** | Tilt Warp | Google Fonts (free) | Named in the guidelines as the web backup for Futura. |
| **Secondary / script** | Starlit Drive | Commercial license | The logo font. Accent only — see 3.3. |
| **Tertiary / body** | Lato | Google Fonts (free) | Lato Medium for body, Lato Black for subheads. |

### 3.2 Print specimen the scale is derived from `[BRAND]`

| Element | Face | Case | Size | Tracking | Leading |
|---|---|---|---|---|---|
| Headline | Futura PT Cond. Extra Bold | UPPERCASE | 62pt | 10 | — |
| Subtitle | Lato Black | UPPERCASE | 30pt | 0 | — |
| Accent | Starlit | lowercase | 68pt | 0 | — |
| Body | Lato Medium | Sentence case | 10pt | 20 | 16pt |

Tracking is InDesign units: divide by 1000 for em. Tracking 10 = `0.01em`,
tracking 20 = `0.02em`. Body leading 16pt on 10pt type = `line-height: 1.6`.

### 3.3 Usage rules

- **Display is always uppercase.** Futura PT Cond Extra Bold, `0.01em` tracking,
  `0.92` line height so caps stack tight. One display headline per screen, per
  email, per ad. Two competing display lines kills the effect. `[BRAND + SYSTEM]`
- **Subheads are Lato Black uppercase at zero tracking.** They pair *under* or
  *over* the display line, never beside it. `[BRAND]`
- **Body is Lato Medium, sentence case, 1.6 leading, `0.02em`.** Cap the measure
  at ~680px. `[BRAND]`
- **Starlit is for one or two lowercase words.** It's the logo font — every extra
  use dilutes the logo. Never body copy, never a full sentence, never below ~28px.
  **Prefer setting it as artwork (SVG/PNG) rather than live web text**, since it
  isn't a webfont you can rely on. `[BRAND + SYSTEM]`
- **Tilt Warp substitutes for Futura on web only** when the Adobe Fonts project
  isn't available. It is a chunkier, rounder face — it will not metric-match
  Futura, so re-check line breaks after swapping. `[BRAND + SYSTEM]`

### 3.4 Live-site reality vs the guidelines — a decision you need to make `[SITE]`

Production Sunday Swagger page markup renders body copy in **Work Sans**, not
Lato. Section headings there are Lato 900, uppercase, 20px, `line-height: 1.3`.

So the storefront is currently running a Work Sans body / Lato Black heading
combination while the guidelines specify Lato throughout.

**Recommendation:** treat Lato as canonical and migrate the theme, because
Work Sans has no standing in the brand book and every off-book font is one more
thing to keep in sync across email, ads, and web. Until that migration happens,
**use `--ss-font-body-site` (Work Sans first) when editing existing pages** so
new blocks don't visibly differ from the ones beside them, and
`--ss-font-body` (Lato first) for everything new — email, ads, rebuilt pages.

Both stacks are in `tokens.css`. If you'd rather adopt Work Sans as the official
body face, say so and this document gets updated — the point is that one of the
two wins, not that both keep running.

### 3.5 Web type scale `[SYSTEM]`

`11 · 12 · 14 · 16 · 18 · 20 · 24 · 32 · 40 · 56 · 72 · 96` px.
18px and 20px are pinned to measured live-site values. See `--ss-text-*`.

---

## 4. Logo `[BRAND]`

**Primary:** the "Sunday Swagger" script wordmark with the underscore-arrow.
**Secondary:** the shaka hand in a golf glove.

Rules from the guidelines:
- Reproduce in **black or white only**, on a branded color background.
- **Clear space = the height of the logo (`x`) on all sides.** Nothing enters it.
- Never crop it, recolor it, or add elements to it without pre-approval.
- Alongside partner logos (e.g. the PGA lockup), all logos sit at approximately
  equal visual size.

Extracted assets in `assets/`, transparent PNG at 300dpi:

| File | Use |
|---|---|
| `ss-wordmark-black.png` | Primary mark on white/grey/accent backgrounds |
| `ss-wordmark-white.png` | Primary mark on black or photography |
| `ss-glove-black.png` | Secondary mark on light backgrounds |
| `ss-glove-white.png` | Secondary mark on dark backgrounds |

> These are raster traces pulled from the guidelines PDF — good for email and web
> at display sizes. **For print and large-format ads, use the original vector
> logo files** from the brand folder, not these.

---

## 5. Shape, space, elevation `[SYSTEM]`

The guidelines say nothing about any of this. These defaults are designed to
serve "clean, modern, sleek."

- **Radius:** near-square. `4px` default on buttons, inputs, cards. `2px` for
  sticker-style promo. `8px` for media tiles and modals. Pills (`999px`) are
  reserved for badges and filter chips. Nothing else gets a pill.
- **Spacing:** 4px base — `4 · 8 · 12 · 16 · 24 · 32 · 40 · 56 · 72 · 96 · 128`.
  Section padding is `96px` desktop, `56px` for tight sections.
- **Borders:** `1px` hairline, `2px` for buttons and emphasis, `3px` focus rings.
- **Shadows:** two families, deliberately.
  - *Soft* (`sm`/`md`/`lg`) — the restrained default. Barely-there elevation for
    dropdowns, modals, sticky bars.
  - *Hard offset* (`4px 4px 0 #000`, no blur) — the brand-expressive one. Reads
    as print/sticker/screen-print, which is exactly what the product is. Use it
    on promo buttons, drop banners, and ad CTAs. **Never mix the two families in
    one composition.**

---

## 6. Components

Full CSS in `components.css`. The rules that matter:

**Buttons.** Uppercase, Lato Black (900), `0.06em` tracking, `48px` min height,
`4px` radius, `2px` border. Primary is black fill / white text — this is the
default CTA everywhere. Secondary is an outline that inverts on hover. Accent
fills (blue/green/pink) are for the single loudest action on a page and **always
carry black label text** (§2.4). The `--sticker` modifier adds the hard offset
shadow and presses into it on click; save it for promo.

**Badges.** Pill, 11px, Lato Black, `0.06em` tracking. This is the best home for
accent color — small, high-frequency, black type on a bright chip. `NEW DROP`,
`LAST CHANCE`, `BEST SELLER`.

**Product cards.** 4:5 media, grey placeholder, `4px` radius, subtle 1.03 zoom on
hover. Title in Lato Black uppercase 14px. Chrome stays minimal — the print on
the polo is the content.

**Announcement bar.** The one place accent color runs full-bleed. Black by
default; blue/green/pink with black text for a drop or a sale.

**Tables.** Match the live size guides: `#F2F2F2` header, `#E0E0E0` border,
`#E5E5E5` row divider, 16px/12px padding, centered.

---

## 7. Composition patterns `[SYSTEM]`

Three layouts cover most of what you'll build:

1. **Black slab.** Black background, white display headline, one accent word or
   underline, white outline CTA. The default hero. Highest brand recognition.
2. **Product-forward.** White or `#ECECEC` background, big product photo, black
   display headline, black CTA. The default for collection and PDP sections.
3. **Sticker promo.** Accent-color field, black display type, black-labeled
   button with a hard offset shadow. Sale and drop only — it's the loudest thing
   in the system, so it stops working if it's always on.

**Accent budget:** one accent color per composition. Not two, not a gradient
between them. The palette has three accents so different drops can feel
different, not so one email can use all of them.

---

## 8. Email `[SYSTEM]`

Full spec and a ready template in `email/`. Headlines:

- Gmail strips webfonts. **Futura PT Condensed and Tilt Warp will not render for
  most of your list.** For a hero display headline, either export it as an image
  (with real `alt` text) or accept the fallback — `Arial Narrow` / `Arial Black`.
- Body: `Lato, 'Helvetica Neue', Helvetica, Arial, sans-serif` — Lato loads in
  Apple Mail and iOS, everyone else gets Helvetica/Arial and it still looks right.
- 600px body width, inline styles, table layout, bulletproof VML buttons.
- Accent-filled CTA buttons still take black text.

## 9. Ads `[SYSTEM]`

Full spec in `ads/AD-SPEC.md`. The short version:

- One display headline, ≤6 words, uppercase.
- One accent color, one CTA.
- Logo in a corner with full `x` clear space, in black or white only.
- Meta/Instagram: keep type out of the outer 14% on 9:16 for Stories/Reels safe
  areas; 1:1 and 4:5 for feed.
- Never put small type over a busy product print — that's what the black slab
  pattern is for.

---

## 10. Closing the live-site gap

Two of the three uses you named — website edits and ads that match the site —
depend on matching the storefront exactly, and this environment can't reach it.
Any of these fixes it, fastest first:

1. **Paste the theme CSS.** In the Shopify admin: Online Store → Themes → Edit
   code → `assets/*.css` (or `base.css` / `theme.css`). Even just the `:root`
   block and the `.button` rules is enough.
2. **View-source a product page** and paste the `<head>` — that gives the font
   loads and CSS variables.
3. **Ask your admin to allow `sundayswagger.com`** for this session's egress
   policy, and I'll crawl it directly.
4. **Screenshots** of the homepage, a PDP, and the cart drawer — enough to
   confirm radius, shadow, and button treatment by eye.

With any one of those, every `[SYSTEM]` tag in §5 and §6 becomes `[SITE]`, and
this system stops being a well-reasoned proposal and starts being a mirror of
what's actually shipping.

---

## 11. Using this in Claude Design

Paste the block in `README.md` §"Prompt block" at the top of any Claude Design
request. It's a compressed version of this document written for a prompt window.
