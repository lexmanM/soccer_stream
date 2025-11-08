# GameOn Landing Page – Figma Handoff

This document mirrors the current HTML so you can rapidly rebuild the layout inside Figma. Follow the checklist below to recreate the design (or drop the values into your own template).

## 1. Frame & Grid
- Create a `1440 × 3900` desktop frame named **Landing Page**.
- Apply a 12-column layout, 72px margins, and 24px gutters.
- Set frame background to `#FDF6F6` to emulate the soft surface tone from the site.

## 2. Color Styles
Create shared color styles to keep the palette consistent:
| Style | Hex | Usage |
| --- | --- | --- |
| `Primary / Red` | `#C8102E` | Buttons, header background, accent text |
| `Primary / Red Soft` | `rgba(200,16,46,0.12)` | Shadows & borders |
| `Accent / Teal` | `#00B2A9` | Secondary CTAs, dividers |
| `Highlight / Yellow` | `#F6EB61` | Footer gradient accent |
| `Surface / Base` | `#FFFFFF` | Cards, header text |
| `Text / Strong` | `#C8102E` | Headings |
| `Text / Base` | `rgba(200,16,46,0.78)` | Body copy |
| `Text / Muted` | `rgba(200,16,46,0.62)` | Captions, meta labels |

## 3. Typography Styles
Font: **Space Grotesk** (Google Fonts).

| Style | Size / Weight | Line Height | Case |
| --- | --- | --- | --- |
| `Display / H1` | 56 / 700 | 120% | Sentence |
| `Heading / H2` | 28 / 700 | 120% | Sentence |
| `Heading / H3` | 20 / 600 | 130% | Sentence |
| `Body / Base` | 18 / 500 | 150% | Sentence |
| `Body / Small` | 15 / 500 | 150% | Sentence |
| `Label / Meta` | 12 / 600 | 140% | Uppercase |
| `UI / Button` | 16 / 600 | 130% | Uppercase |

## 4. Components to Build
1. **Wordmark Stack**
   - Vertical Auto Layout, spacing `8`.
   - Top line “GameOn” using `Heading / H2`, letter spacing `0.04em`, uppercase disabled.
   - Bottom line “Never miss a match” using `Label / Meta`, uppercase ON, tracking `80`.
   - Set both fills to `Surface / Base`.

2. **Pill Tag**
   - `Auto Layout` horizontal, padding `8×14`, corner radius `999`, fill `Surface / Base`, stroke `Primary / Red` 1px.

3. **Primary CTA Button**
   - `Auto Layout`, padding `16×32`, radius `999`, fill `#F6EB61`, drop shadow `0 16 32 rgba(246,235,97,0.35)`.

4. **Fixture Card**
   - Frame `min 300×320`, padding `28`, radius `22`, fill `Surface / Base`, stroke `Primary / Red Soft`, drop shadow `0 18 42 rgba(200,16,46,0.12)`.
   - Column Auto Layout: (a) competition label, (b) pill-style countdown, (c) two-line match title (“Liverpool vs” on line 1, opponent on line 2), (d) single date/time line, (e) pill CTA.
   - Keep everything left-aligned to maintain vertical rhythm. Button uses `Accent / Teal` fill.

5. **Feature Card**
   - Frame `min 220×220`, padding `24`, radius `18`, same border/shadow as fixture card but lighter drop shadow `0 14 34 rgba(200,16,46,0.12)`.

6. **Footer**
   - Frame with linear gradient fill: `linear(180°, #F6EB61 → rgba(255,255,255,0.92))`, 1px top stroke `Primary / Red Soft`.

## 5. Layout Sections
1. **Hero Header**
   - Header background color `Primary / Red`.
   - Place the wordmark stack above the hero copy (max width 560px). Include CTA row (button + caption) directly under the paragraph.

2. **Fixtures Section**
   - Title pill now reads “Next 3 fixtures”. Use a responsive grid that can show three cards per row on desktop.
   - Countdown badge uses `Label / Meta` style and solid `Primary / Red` fill; keep it directly beneath the competition label for alignment.

3. **Features Section**
   - Title pill reused.
   - Feature cards in responsive grid.

4. **Footer**
   - Centered text using `Body / Small` style.

## 6. Assets & Export Notes
- Reuse the same gradients/ shadows as in CSS for visual parity.
- Once built, publish the components so we can reference them in future iterations.
- If you prefer an automated import, load this markdown into the **"Builder.io → Figma"** or **"Scripter"** plugin to generate frames with the provided sizes/values.

## 7. Collaboration Plan
1. Recreate the frame using this spec and share the Figma link.
2. Tag me with the node IDs you care about (logo, fixture card, feature card) so I can update HTML/CSS in lockstep.
3. Future tweaks (color or spacing changes) can flow from Figma → code by mapping the shared tokens defined above.

Let me know once the file exists in your workspace and I’ll sync any subsequent code changes with that source of truth.
