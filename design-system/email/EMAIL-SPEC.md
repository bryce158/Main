# Sunday Swagger — Email Spec

Klaviyo / any ESP. Everything here is `[SYSTEM]` unless tagged otherwise —
the brand guidelines don't cover email.

## Structure

| Property | Value |
|---|---|
| Body width | 600px |
| Mobile | single column, stack at 480px |
| Outer background | `#ECECEC` (brand grey) or `#000000` |
| Content background | `#FFFFFF` or `#000000` |
| Side padding | 24px mobile, 32px desktop |
| Section spacing | 32px between blocks, 56px between major sections |

## Fonts — what actually renders

Gmail (web + app), Outlook desktop, and Yahoo strip webfonts. Assume your
display face will not load for most of the list.

| Slot | Stack | Renders as |
|---|---|---|
| Display headline | `'Futura PT Condensed','Tilt Warp','Arial Narrow',Arial,sans-serif` | Arial Narrow for most |
| Subhead | `Lato,'Helvetica Neue',Helvetica,Arial,sans-serif` + `font-weight:900` | Arial Black-ish |
| Body | `Lato,'Helvetica Neue',Helvetica,Arial,sans-serif` + `font-weight:500` | Helvetica/Arial |

**Rule:** if the display headline is doing brand work — a drop announcement, a
sale number, the hero — **export it as an image** with real `alt` text and a
`background-color` behind it so the alt text is readable when images are off.
Everything else stays live text.

## Type sizes

| Element | Size / line-height / tracking | Case |
|---|---|---|
| Hero display (image) | 48–72px / 0.92 / 0.01em | UPPER |
| Section headline | 28px / 1.1 / 0.01em | UPPER |
| Subhead | 18px / 1.3 / 0 / weight 900 | UPPER |
| Body | 16px / 1.6 / 0.02em / weight 500 | Sentence |
| Fine print | 12px / 1.5 / weight 500, `#6B6D70` | Sentence |
| Button label | 14px / 1 / 0.06em / weight 900 | UPPER |

Never below 14px for anything a customer needs to read on a phone.

## Buttons

Bulletproof, table-based, with VML for Outlook. Padding `16px 32px`, radius
`4px`, min width 200px, min height 48px.

| Style | Fill | Text |
|---|---|---|
| Primary | `#000000` | `#FFFFFF` |
| Primary on dark | `#FFFFFF` | `#000000` |
| Accent blue | `#00B3D8` | `#000000` |
| Accent green | `#C2FC08` | `#000000` |
| Accent pink | `#EE4492` | `#000000` |

**Accent buttons take black text.** White on blue is 2.49:1 and white on green
is 1.22:1 — both fail WCAG AA, and email clients give you no fallback.

## Color use in email

- Default frame: black and white. One accent per send, maximum.
- Accents belong on: the announcement strip, a badge, an underline behind a
  word, a divider rule, or one CTA. Not all five in one email.
- Brand grey `#ECECEC` is the outer canvas — it separates the 600px body from
  the client chrome without adding color.
- Dark-mode: many clients auto-invert. Use `#000000` explicitly rather than
  relying on a transparent background, and supply white logo PNGs for dark
  sections (`assets/ss-wordmark-white.png`).

## Logo in email

- Header: wordmark, 180–220px wide, centered or left, with clear space equal to
  the logo's height on every side.
- Footer: glove mark at 48–64px, or wordmark at 140px.
- Always `alt="Sunday Swagger"`. Always a real `width` attribute (Outlook).
- Black wordmark on light backgrounds, white on dark. No other color, ever.

## Accessibility checklist for every send

- [ ] Every image has meaningful `alt` text
- [ ] Hero headline readable with images disabled
- [ ] No white text on blue, green, or pink
- [ ] Body copy ≥16px, fine print ≥12px
- [ ] Tap targets ≥48px tall
- [ ] Real text-to-image ratio (not a single sliced JPEG — deliverability)
- [ ] Preview text set, 40–90 characters
