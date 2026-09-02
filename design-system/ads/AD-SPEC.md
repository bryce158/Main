# Sunday Swagger — Ad Spec

All `[SYSTEM]` — the brand guidelines don't cover paid media. Built to hold the
brand's stated rule: clean, sleek frame; the product print is the loud part.

## The three ad templates

### 1. Black slab
Black field, white display headline, one accent word or underline, product cut
out or photographed on black, white outline CTA.
**Use for:** brand, new drop, top-of-funnel. Highest recognition, lowest noise.

### 2. Product-forward
White or `#ECECEC` field, full-bleed product photo, black display headline,
black solid CTA.
**Use for:** catalog, retargeting, best-sellers. Lets the print sell.

### 3. Sticker promo
Accent field (`#00B3D8` / `#C2FC08` / `#EE4492`), black display type, black CTA
with a `4px 4px 0 #000` hard offset shadow.
**Use for:** sale, last chance, code drops. It's the loudest asset in the system
— if it's always running it stops reading as urgent.

## Canvas sizes

| Placement | Ratio | Pixels |
|---|---|---|
| Meta / IG feed square | 1:1 | 1080 × 1080 |
| Meta / IG feed portrait | 4:5 | 1080 × 1350 |
| Stories / Reels / TikTok | 9:16 | 1080 × 1920 |
| Google Display leaderboard | — | 728 × 90 |
| Google Display MPU | — | 300 × 250 |
| Google Display half-page | — | 300 × 600 |
| Pinterest | 2:3 | 1000 × 1500 |
| Email hero | 2:1 | 1200 × 600 (renders at 600) |

## Safe areas

- **9:16 (Stories/Reels/TikTok):** keep all type and the logo out of the top 14%
  and bottom 20%. Platform UI covers both.
- **1:1 and 4:5:** 64px minimum margin on 1080px canvases.
- **Display banners:** 16px margin; on 728×90 use one line of type and the
  glove mark only — the wordmark is unreadable at that height.

## Type in ads

| Element | Face | Size on 1080px canvas |
|---|---|---|
| Display headline | Futura PT Cond Extra Bold, UPPER, `0.01em` | 96–160px |
| Subhead | Lato Black, UPPER | 40–56px |
| Body / offer detail | Lato Medium | 28–36px |
| Legal / disclaimer | Lato Medium, `#999B9E` | 20–24px |
| CTA label | Lato Black, UPPER, `0.06em` | 32–40px |

**Headline ceiling: 6 words.** If it needs more, it's a landing page, not an ad.

## Rules

1. **One display headline. One accent color. One CTA.** Every ad.
2. **Never small type over a busy product print.** If the copy has to sit on the
   garment, you want the black slab template instead.
3. **Accent-filled CTAs take black labels** — the contrast math in
   `DESIGN-SYSTEM.md` §2.4 applies to paid media too, and platforms compress
   aggressively.
4. **Logo in one corner**, black or white only, with clear space equal to its own
   height. Never over the product, never recolored.
5. **Starlit script:** one or two lowercase words maximum, as artwork. It's the
   logo font — every extra use costs the logo some of its distinctiveness.
6. **Meta text-density:** keep copy well under a third of the canvas. The 20%
   rule isn't hard-enforced any more but dense-text creative still gets throttled.

## Motion (video / Reels)

- Cuts, not fades. Brand personality is "daring" and "confident," not soft.
- Type in: 120–200ms, ease `cubic-bezier(.2,.7,.3,1)`, no bounce.
- Hold every headline ≥1.5s at Reels pace.
- Logo sting: last 0.8–1.2s, wordmark on black, silence or a hard stop.
- Caption everything — most of the feed is watched muted.
