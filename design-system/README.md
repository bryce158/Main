# Sunday Swagger Design System

One source of truth for **emails, website edits, and ads**.

```
design-system/
├── DESIGN-SYSTEM.md      ← read this first. The full spec, with confidence tags.
├── tokens.css            ← CSS custom properties. Import into any web work.
├── tokens.json           ← same tokens as data (Figma plugins, scripts, tooling).
├── components.css        ← buttons, badges, cards, tables, sections.
├── email/
│   ├── EMAIL-SPEC.md     ← what renders in Gmail, what doesn't, and sizes.
│   └── template.html     ← 600px Klaviyo-ready table template.
├── ads/
│   └── AD-SPEC.md        ← three ad templates, canvas sizes, safe areas.
└── assets/               ← transparent-PNG logo marks, 300dpi.
```

## Two things to know before you use it

**1. Read the confidence tags.** `[BRAND]` is brand law from the guidelines.
`[SITE]` is measured from live storefront markup. `[SYSTEM]` is designed here
because the guidelines cover only color, type, and logo — they say nothing about
buttons, shadows, radii, spacing, or layout. Overrule any `[SYSTEM]` decision you
disagree with, then update the doc so the next person inherits your call.

**2. The live site was not crawled.** `sundayswagger.com` is blocked by this
environment's network egress policy. Component styling is designed from the
brand's stated aesthetic, not transcribed from production.
`DESIGN-SYSTEM.md` §10 lists four ways to close that gap in about two minutes.

## The one rule everything else serves

> "Keep a clean, modern, and sleek look, while allowing our loud designs to
> speak for themselves." — Brand Guidelines, p.1

The prints on the product are the loud part. The frame around them stays black
and white. When a layout feels off, the fix is almost always to take color out.

---

## Prompt block — paste this into Claude Design

Copy everything between the lines into the top of any Claude Design request.

---

```
BRAND: Sunday Swagger — golf apparel with loud, in-house prints.
Mission: empowering the individual to own it. Positioning: own your swagger.
Personality: daring, innovative, inclusive, confident, stylish.
Governing rule: clean, modern, sleek frame — the product prints are the loud
part. When in doubt, take color out.

COLOR
  Primary   black #000000 · white #FFFFFF   (the brand is black and white)
  Secondary grey  #ECECEC                   (backgrounds only, never type)
  Accents   blue  #00B3D8 · green #C2FC08 · pink #EE4492
            Used SPARINGLY — lines, underlines, badges, one CTA, single words.
            ONE accent per composition. Never two, never a gradient.
  HARD RULE: accent fills always take BLACK text.
            White-on-blue is 2.49:1 and white-on-green is 1.22:1 — both fail AA.
            Blue and green work as TEXT only on black. Pink on white is 18px+ bold only.
  Neutrals  #F2F2F2 #E5E5E5 #E0E0E0 #D9D9D9 (borders/dividers) · #6B6D70 (muted text)

TYPE
  Display : Futura PT Condensed Extra Bold — ALWAYS UPPERCASE,
            letter-spacing 0.01em, line-height 0.92. Web fallback: Tilt Warp.
            ONE display headline per screen / email / ad.
  Subhead : Lato Black (900), UPPERCASE, letter-spacing 0.
  Body    : Lato Medium (500), sentence case, line-height 1.6,
            letter-spacing 0.02em, max measure 680px.
  Script  : Starlit Drive — the LOGO font. One or two lowercase words max,
            never body copy, never under 28px, prefer artwork over live text.
  Scale   : 11 12 14 16 18 20 24 32 40 56 72 96 px

SHAPE / SPACE / DEPTH
  Radius  : 4px default (buttons, inputs, cards) · 2px sticker · 8px media ·
            999px badges and chips only.
  Spacing : 4px base — 4 8 12 16 24 32 40 56 72 96 128. Sections 96px desktop.
  Borders : 1px hairline · 2px buttons and emphasis · 3px focus rings.
  Shadow  : soft (0 4px 12px rgba(0,0,0,.10)) is the restrained default;
            HARD offset (4px 4px 0 #000, no blur) is the brand-expressive option
            for promo. Never mix the two families in one composition.

BUTTONS
  Uppercase, Lato Black 900, 14px, letter-spacing 0.06em,
  padding 16px 32px, min-height 48px, radius 4px, 2px border.
  Primary          black fill  / white text        ← default CTA everywhere
  Primary invert   white fill  / black text        ← on dark
  Secondary        transparent / black text / 2px black border, inverts on hover
  Accent           blue|green|pink fill / BLACK text ← one per page, loudest action
  Sticker modifier adds 4px 4px 0 #000 and presses into it on click (promo only)

LOGO
  Primary: "Sunday Swagger" script wordmark. Secondary: shaka hand in a golf glove.
  BLACK OR WHITE ONLY. Clear space on all sides = the logo's own height.
  Never crop, recolor, or add elements.

LAYOUT PATTERNS
  1. Black slab      — black bg, white display headline, one accent word,
                       white outline CTA. Default hero, highest recognition.
  2. Product-forward — white or #ECECEC bg, big product photo, black headline,
                       black CTA. Default for collection and PDP sections.
  3. Sticker promo   — accent field, black display type, black CTA with hard
                       offset shadow. Sale and drops ONLY.

VOICE
  Confident, warm, funny, never smug. Golf-adjacent, never gatekeeping.
  Second person. Short sentences. UPPERCASE for the shout, sentence case for the talk.
  Ad and email headlines: 6 words maximum.
```

---

## Provenance

- **Brand Guidelines** (8pp PDF): color palette with CMYK/RGB builds, four
  typefaces with print specimen specs, logo options and exclusion zone, mission,
  vision, positioning, and the five personality traits.
- **Live-site evidence**: production Sunday Swagger page markup in `../pages/`
  — Work Sans body, Lato 900 uppercase headings at 20px/1.3, and the
  `#F2F2F2` / `#E5E5E5` / `#E0E0E0` / `#D9D9D9` neutral set.
- **Contrast ratios**: computed from the WCAG 2.x relative-luminance formula
  against the spec'd hex values.
- **Logo assets**: vector artwork traced out of the guidelines PDF at 300dpi and
  alpha-keyed. Good for web and email; **use the original vector files for print
  and large-format.**
