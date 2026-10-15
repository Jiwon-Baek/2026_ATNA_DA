# Confident Design System — PPT & UI Design Prompt

## Overview

This design system governs all presentations (PowerPoint), HTML web applications, and GUI executables produced under the Confident brand. The aesthetic is warm, approachable, and encouraging — designed for lectures and communications directed at students and parents. The palette draws from strawberry-milk tones: soft pink canvas accents, a vibrant rose-magenta as the key brand color, and deep wine-rose for dramatic moments. Every surface defaults to white canvas; Confident Rose appears scarcely and purposefully. Rounded geometry is the only geometry: rounded rectangles everywhere, pill shapes for any single-line text element.

**Key Characteristics:**
- Single brand color: `{colors.primary}` (#E63E81 Confident Rose). Every CTA, key accent, and title uses it.
- Calm, friendly typographic weight via **Freesentation** family. No other typeface used.
- Rounded rectangles everywhere. Single-line standalone textboxes always use pill radius (50% of height).
- All slides are 16:9. All GUI applications default to 16:9 as well.
- Every slide carries four fixed structural zones: Chapter Title / Slide Title / Small Header Message / Main Article Placeholder — always at the same measured positions.
- Bottom of each slide is never left empty; gradient and geometric artwork fills the lower decorative zone.
- No logo used anywhere.
- All standalone text elements: vertical alignment = middle, horizontal alignment = center.

---

## Colors

### Brand & Accent

- **Confident Rose** (`{colors.primary}` — #E63E81): The sole brand color. Vivid rose-magenta with warmth and energy. Used for slide titles, primary CTA pills, key shape fills, and border accents.
- **Confident Rose Active** (`{colors.primary-active}` — #C4326E): Press/hover deepening of the primary.
- **Confident Rose Disabled** (`{colors.primary-disabled}` — #F0A0C0): Faded primary tint for disabled states.
- **Confident Rose Accent** (`{colors.primary-accent}` — #FF4A5C): Warmer coral-red variant for inline emphasis links and callout highlights. Use sparingly — one or two moments per slide.
- **Confident Rose Pale** (`{colors.primary-pale}` — #FFD9E8): Very light primary tint for surface fills, alternating band backgrounds, table header rows.

### Surface

- **Canvas** (`{colors.canvas}` — #FFFFFF): Default slide and page floor.
- **Surface Soft** (`{colors.surface-soft}` — #FFF5F8): Subtle alternating band; barely perceptible.
- **Surface Strong** (`{colors.surface-strong}` — #FFE0EC): Behind small labels, secondary buttons, chapter header pills.
- **Surface Dark** (`{colors.surface-dark}` — #3D0A20): Deep wine-rose for cover slides, dark section breaks, and decorative bottom artwork.
- **Surface Dark Elevated** (`{colors.surface-dark-elevated}` — #5C1435): One step lighter dark, used for elevated cards on dark backgrounds.

### Hairlines

- **Hairline** (`{colors.hairline}` — #F7BDD0): Default 1px divider on light surfaces, figure placeholder borders.
- **Hairline Soft** (`{colors.hairline-soft}` — #FFE0EC): Lighter divider, same as `{colors.surface-strong}`.

### Text

- **Ink** (`{colors.ink}` — #1A0810): All headings, primary labels. Near-black with a warm rose undertone.
- **Body** (`{colors.body}` — #4A2535): Default body and running text; warm dark rose-brown.
- **Muted** (`{colors.muted}` — #7A4858): Sub-labels, captions, footnotes.
- **Muted Soft** (`{colors.muted-soft}` — #B08898): Disabled text.
- **On Primary** (`{colors.on-primary}` — #FFFFFF): Text on Confident Rose fills.
- **On Dark** (`{colors.on-dark}` — #FFFFFF): Text on dark surfaces.
- **On Dark Soft** (`{colors.on-dark-soft}` — #FFB8CC): Secondary text on dark surfaces.

### Semantic (text-color use only — never as background fill)

- **Semantic Up** (`{colors.semantic-up}` — #1A7A50): Positive / success indicator.
- **Semantic Down** (`{colors.semantic-down}` — #C01A3A): Negative / error indicator.

---

## Typography

### Font Family

**Freesentation** is the only permitted typeface. It comes in nine weights (1 Thin through 9 Black). The three working weights are:

| Role | Font File | CSS weight |
|---|---|---|
| Light (small text) | Freesentation-3Light.ttf | 300 |
| Medium (default) | Freesentation-5Medium.ttf | 500 |
| Bold (emphasis) | Freesentation-7Bold.ttf | 700 |

Local font path: `C:\Baekjiwon\Documents\글꼴 모음\Freesentation-*.ttf`

In CSS: `font-family: 'Freesentation', 'Freesentation 5 Medium', sans-serif;`

### Hierarchy (PPT point sizes / Web pixel equivalents)

| Token | PPT | Web | Weight | Use |
|---|---|---|---|---|
| `{type.chapter-label}` | 14pt | 18px | Medium (500) | Chapter title strip at slide top |
| `{type.slide-title}` | 36pt | 48px | Bold (700) | Main slide title |
| `{type.sub-header}` | 16pt | 21px | Medium (500) | Small header message bar |
| `{type.body-lg}` | 18pt | 24px | Medium (500) | Lead / prominent body text |
| `{type.body}` | 15pt | 20px | Medium (500) | Default body text |
| `{type.body-sm}` | 13pt | 17px | Light (300) | Secondary body text |
| `{type.caption}` | 11pt | 14px | Light (300) | Captions, footnotes, small labels |
| `{type.emphasis}` | (context) | (context) | Bold (700) | Inline emphasis; size follows context |
| `{type.table-header}` | 14pt | 18px | Bold (700) | Table header row |
| `{type.table-body}` | 13pt | 17px | Light (300) | Table body cells |
| `{type.figure-header}` | 14pt | 18px | Medium (500) | Figure label / header pill |

### Principles

- **Medium is the neutral weight.** Default to Freesentation 5 Medium for all body, labels, and sub-headers.
- **Bold only for titles and headers.** Freesentation 7 Bold for slide titles, chapter labels (when emphasized), table headers, and any text requiring strong hierarchy.
- **Light for density.** Use Freesentation 3 Light in table body, captions, footnotes, and small descriptive text where visual weight reduction prevents crowding.

---

## Layout

### Canvas

**All work is exclusively 16:9.** Reference resolutions:

| Context | Width | Height | Notes |
|---|---|---|---|
| PowerPoint (screen) | 1280 px | 720 px | 13.33 × 7.50 in / 33.87 × 19.05 cm |
| HTML / Web | 1920 px | 1080 px | Default viewport; content max-width follows |
| Executable GUI | 1280 px | 720 px | Window default; scale to screen |

In PowerPoint, set slide size to **Widescreen (13.33 × 7.5 in)** or equivalently 33.87 × 19.05 cm.  
In EMU: **12,192,000 × 6,858,000**.

### Slide Structure — Four Fixed Zones

Every slide (except full-bleed cover slides) contains these four elements at consistent positions.

#### Measured Positions (from reference deck)

| Element | Left | Top | Width | Height |
|---|---|---|---|---|
| **Chapter Title** | 2.7% | 0.0% | 68.7% | 5.7% |
| **Slide Title** | 2.7% | 5.7% | 68.7% | 8.5% |
| **Small Header Message** | 2.6% | 14.7% | 94.9% | 4.5% |
| **Main Article Placeholder** | 2.7% | 16.9% | 94.5% | 77.7% |

#### In pixels (at 1280 × 720 reference)

| Element | Left | Top | Width | Height |
|---|---|---|---|---|
| Chapter Title | 35 px | 0 px | 880 px | 41 px |
| Slide Title | 35 px | 41 px | 880 px | 61 px |
| Small Header Message | 33 px | 106 px | 1215 px | 32 px |
| Main Article Placeholder | 35 px | 122 px | 1210 px | 560 px |

#### In EMU (for PowerPoint at 12,192,000 × 6,858,000)

| Element | Left | Top | Width | Height |
|---|---|---|---|---|
| Chapter Title | 329,184 | 0 | 8,375,904 | 390,906 |
| Slide Title | 329,184 | 390,906 | 8,375,904 | 582,930 |
| Small Header Message | 316,992 | 1,008,126 | 11,574,048 | 308,610 |
| Main Article Placeholder | 329,184 | 1,158,942 | 11,521,440 | 5,328,666 |

#### In centimeters (for PowerPoint metric input)

| Element | Left | Top | Width | Height |
|---|---|---|---|---|
| Chapter Title | 0.91 cm | 0 cm | 23.27 cm | 1.09 cm |
| Slide Title | 0.91 cm | 1.09 cm | 23.27 cm | 1.62 cm |
| Small Header Message | 0.88 cm | 2.80 cm | 32.15 cm | 0.86 cm |
| Main Article Placeholder | 0.91 cm | 3.22 cm | 32.00 cm | 14.80 cm |

#### Layout notes

- **Chapter Title** and **Slide Title** boxes share the same left edge and width. They visually layer without conflict because Chapter Title text is small (`{type.chapter-label}`) aligned to the top of its box, while Slide Title text is large (`{type.slide-title}`) aligned to the middle.
- The right 28.6% of the slide (from 71.4% to 100%) is the **top-right decorative zone** — reserved for subtle gradient artwork, a chapter/page indicator, or supplementary decorative shapes. Never place primary text content here.
- The bottom 5% of the slide below the Main Article Placeholder (94.8%–100%) is the **bottom trim zone** — used exclusively for gradient/decorative fills.

### Decorative Zones

**Top-right zone** (right of chapter/slide title, top ~14% of slide):
- May contain: abstract geometric shapes in `{colors.primary-pale}` (#FFD9E8) or `{colors.surface-strong}` (#FFE0EC), a thin vertical separator line at 71.4%, or a chapter/page indicator pill.

**Bottom decorative zone** (lower 15–25% of main article + bottom trim):
- Every slide must have artwork here. Use: gradient rectangles blending from `{colors.primary}` (#E63E81) or `{colors.surface-dark}` (#3D0A20) to transparent, overlapping semi-transparent rounded rectangles in primary tints, or abstract layered shapes.
- Must not overlap or obscure body text.
- Opacity of decorative shapes: 10–35%. Do not use high-opacity fills that compete with content.

---

## Geometry & Shapes

### Border Radius Scale

| Token | Value | Use |
|---|---|---|
| `{rounded.none}` | 0 px | Reserved; avoid entirely |
| `{rounded.sm}` | 4 px | Inline micro-tags only |
| `{rounded.md}` | 8 px | Form inputs, compact chips |
| `{rounded.lg}` | 12 px | Mid-size cards |
| `{rounded.xl}` | 16 px | Main article placeholder, figure placeholders |
| `{rounded.xxl}` | 24 px | Large feature / section cards |
| `{rounded.pill}` | 50% of the shorter dimension | ALL single-line standalone textboxes, CTA buttons, small header message bar, figure headers |
| `{rounded.full}` | 9999 px | Circle icon plates, avatar elements |

**The pill rule is absolute:** Any text element that appears alone (not within a larger box) and spans a single line must use `{rounded.pill}` — the shorter dimension (height for landscape boxes) times 50%.

### Shadow

Single shadow tier only:

| Level | CSS / Treatment | Use |
|---|---|---|
| Flat | No shadow | 80% of surfaces |
| Soft drop | `0 4px 16px rgba(230,62,129,0.10)` | Figure placeholders, elevated cards |
| Dark card drop | `0 6px 24px rgba(61,10,32,0.18)` | Cards on dark backgrounds |

---

## Components

### 1. Chapter Title

The topmost text element on every slide. A thin label identifying the current chapter or section (e.g., "I. Introduction", "III. Methodology").

- **Shape**: No background fill; transparent. No border.
- **Position**: `{layout.chapter-title}` (left=0.91 cm, top=0 cm, width=23.27 cm, height=1.09 cm)
- **Font**: `{type.chapter-label}` — Freesentation 5 Medium, 14pt
- **Color**: `{colors.primary}` (#E63E81)
- **Alignment**: Vertical = Top; Horizontal = Left
- **Text format**: Roman numeral + period + space + section name (e.g., "II. Problem Definition")

---

### 2. Slide Title

The primary heading for the slide.

- **Shape**: No background fill; transparent. No border.
- **Position**: `{layout.slide-title}` (left=0.91 cm, top=1.09 cm, width=23.27 cm, height=1.62 cm)
- **Font**: `{type.slide-title}` — Freesentation 7 Bold, 36pt
- **Color**: `{colors.ink}` (#1A0810)
- **Alignment**: Vertical = Middle; Horizontal = Left
- **Note**: Title boxes layer with the Chapter Title box (they share the left zone). Text size difference creates visual separation without physical separation.

---

### 3. Small Header Message (Slide Sub-Header)

A thin full-width rounded-pill bar immediately below the header zone. Acts as a sub-topic label or section descriptor for the slide's main content.

- **Shape**: Rounded rectangle, `{rounded.pill}` radius (50% of 32 px height ≈ 16 px radius)
- **Fill**: `{colors.primary}` (#E63E81) at 100% — solid Confident Rose bar
- **No border, no shadow**
- **Position**: `{layout.small-header}` (left=0.88 cm, top=2.80 cm, width=32.15 cm, height=0.86 cm)
- **Font**: `{type.sub-header}` — Freesentation 5 Medium, 16pt
- **Text color**: `{colors.on-primary}` (#FFFFFF)
- **Alignment**: Vertical = Middle; Horizontal = Center
- **Variant — Partial-width**: When used as a content sub-label inside the main area (e.g., "Tip", "Point"), use the same pill style at roughly 20–35% width, centered or left-offset within the section. Fill may use `{colors.surface-strong}` (#FFE0EC) with `{colors.ink}` text for lower-emphasis labels.

---

### 4. Main Article Placeholder

The primary content container for each slide.

- **Shape**: Rounded rectangle, `{rounded.xl}` (16 px)
- **Fill**: `{colors.canvas}` (#FFFFFF) — white
- **Border**: 1 px solid `{colors.hairline}` (#F7BDD0)
- **Shadow**: `{shadow.soft-drop}` (`0 4px 16px rgba(230,62,129,0.10)`)
- **Position**: `{layout.main-article}` (left=0.91 cm, top=3.22 cm, width=32.00 cm, height=14.80 cm)
- **Internal padding**: 0.5 cm / 20px on all sides
- **Note**: The lower 20–30% of this rectangle is the decorative artwork zone. Place gradient/geometric fills there, keeping the upper content area clean.

---

### 5. Figure Placeholder

A card-style container for images, charts, diagrams, or illustrations.

- **Shape**: Rounded rectangle, `{rounded.xl}` (16 px)
- **Fill**: `{colors.canvas}` (#FFFFFF) — white
- **Border**: 1 px solid `{colors.hairline}` (#F7BDD0)
- **Shadow**: `{shadow.soft-drop}` (`0 4px 16px rgba(230,62,129,0.10)`)
- **Size**: Variable; determined by content. Maintain 16:9 or other intentional aspect ratio.
- **Internal padding**: 0.3 cm / 12px

---

### 6. Figure Header

An optional pill label attached to or overlapping the top edge of a Figure Placeholder, giving the figure a short title or identifier.

- **Shape**: Rounded rectangle, `{rounded.pill}` (50% of height)
- **Fill**: `{colors.primary}` (#E63E81)
- **No border, no shadow**
- **Height**: ~0.7 cm / 28 px (PPT) — keeps the pill compact
- **Width**: Auto-sized to text with ~16 px horizontal padding
- **Font**: `{type.figure-header}` — Freesentation 5 Medium, 14pt
- **Text color**: `{colors.on-primary}` (#FFFFFF)
- **Alignment**: Vertical = Middle; Horizontal = Center
- **Placement**: Positioned atop the Figure Placeholder, left-aligned or centered.

---

### 7. Table

Tables follow a borderless-column style with horizontal lines only where structurally necessary.

**Cell padding**: Narrow (PPT: 0.05 cm top/bottom, 0.10 cm left/right).  
**Alignment**: Horizontal = Center; Vertical = Middle for all cells.

**Borders**:
- No vertical borders anywhere.
- Horizontal borders:
  - Above the header row: 1.5 pt solid `{colors.ink}` (#1A0810)
  - Below the header row: 1.5 pt solid `{colors.ink}` (#1A0810)
  - Below the last body row: 1 pt solid `{colors.hairline}` (#F7BDD0)
  - No borders between body rows.

**Header row**:
- Fill: `{colors.primary-pale}` (#FFD9E8) — very light Confident Rose tint
- Font: `{type.table-header}` — Freesentation 7 Bold, 14pt
- Text color: `{colors.ink}` (#1A0810)

**Body rows**:
- Fill: None (transparent)
- Font: `{type.table-body}` — Freesentation 3 Light, 13pt
- Text color: `{colors.body}` (#4A2535)
- Alternating row shading (optional, subtle): `{colors.surface-soft}` (#FFF5F8) at 60% opacity for even rows.

---

### 8. Standalone Single-Line Text Box

Any text element that stands alone (not nested in a larger shape) and spans a single line.

- **Shape**: Rounded rectangle, `{rounded.pill}` (radius = 50% of box height)
- **Fill**: Context-dependent:
  - Primary label: `{colors.primary}` (#E63E81)
  - Secondary label: `{colors.surface-strong}` (#FFE0EC)
  - Transparent / no fill: when used as a title overlay
- **Alignment**: Vertical = Middle; Horizontal = Center
- **Font**: `{type.body}` — Freesentation 5 Medium, 15pt (adjust size to context)
- **Text color**: `{colors.on-primary}` for filled; `{colors.ink}` for surface-filled.

---

### 9. CTA / Button Pill

Interactive call-to-action elements in HTML and GUI applications.

- **Shape**: Fully pill-shaped, `{rounded.pill}`
- **Height**: 44 px (standard) / 56 px (hero/prominent CTA)
- **Padding**: 12 px vertical, 24 px horizontal

**`button-primary`**: Background `{colors.primary}` (#E63E81), text `{colors.on-primary}`, font `{type.body}` 500, height 44 px.  
**`button-primary-active`**: Background `{colors.primary-active}` (#C4326E).  
**`button-primary-disabled`**: Background `{colors.primary-disabled}` (#F0A0C0), cursor not-allowed.  
**`button-secondary`**: Background `{colors.surface-strong}` (#FFE0EC), text `{colors.ink}`.  
**`button-outline`**: Border 1.5 px `{colors.primary}` (#E63E81), transparent background, text `{colors.primary}`.  
**`button-hero`**: Background `{colors.primary}` (#E63E81), height 56 px, padding 16 px × 32 px.

---

### 10. Bottom Decorative Artwork

Every slide and page must have non-empty decorative content in the lower 15–25% of the main content area and the bottom trim zone.

**Approach**: Layer 2–4 semi-transparent geometric shapes:
1. A gradient rectangle spanning the full slide width, fading from `{colors.surface-dark}` (#3D0A20) (opacity 15–25%) at the very bottom edge to transparent.
2. 1–2 rounded rectangles (`{rounded.xxl}`) in `{colors.primary}` (#E63E81) at 8–15% opacity, offset to the right or left bottom corner.
3. Optionally: a thin diagonal or horizontal bar shape in `{colors.primary-pale}` (#FFD9E8) at 40–60% opacity.

**Constraints**:
- All decorative shapes: opacity ≤ 35%.
- Decorative shapes must not intrude above the lower 25% boundary of the Main Article Placeholder.
- Never use text or images as decorative bottom fill.

---

## Do's and Don'ts

### Do

- Use `{colors.primary}` (#E63E81) exclusively for: Chapter Title text, Small Header Message fill, primary CTA buttons, Figure Headers, and key shape accents.
- Apply `{rounded.pill}` to every standalone single-line textbox without exception.
- Keep all four structural zones (Chapter Title / Slide Title / Small Header / Main Article) at the exact measured positions on every slide.
- Set all standalone text boxes to vertical = middle, horizontal = center alignment.
- Fill the lower 15–25% of each slide with gradient/geometric artwork at low opacity.
- Use Freesentation 3 Light for table body, captions, and dense small text to maintain visual lightness.
- Use Freesentation 7 Bold only for Slide Title, table headers, and emphasis highlights.
- Use `{rounded.xl}` (16px) for the Main Article Placeholder and Figure Placeholders.
- Keep soft pink tones (#FFD9E8, #FFE0EC, #FFF5F8) on large background areas and reserve the vivid rose (#E63E81) for small, intentional accent moments.

### Don't

- Don't introduce any font other than Freesentation.
- Don't use `{colors.primary-accent}` (#FF4A5C) as a background fill — accent tint only (inline text emphasis, small callout tags).
- Don't use `{colors.semantic-up}` or `{colors.semantic-down}` as background fills.
- Don't leave the bottom of a slide visually empty.
- Don't use sharp corners (`{rounded.none}`) on any element — rounded geometry is mandatory.
- Don't include a logo on any slide.
- Don't create slides in any ratio other than 16:9.
- Don't position the four structural elements at inconsistent coordinates across slides — pixel-perfect consistency is required.
- Don't exceed two shadow tiers; no additional drop-shadow levels beyond the two defined.
- Don't use vertical borders in tables.
- Don't bold any body text using CSS/PPT bold unless using Freesentation 7 Bold explicitly — avoid `font-weight: bold` with wrong font weight mapping.
- Don't use both `{colors.primary}` (#E63E81) and `{colors.primary-accent}` (#FF4A5C) in the same accent role on the same slide — pick one per context to avoid color noise.

---

## Platform Notes

### PowerPoint

- Slide size: Widescreen (13.33 × 7.5 in) — do not change to custom; this maps to exactly 12,192,000 × 6,858,000 EMU.
- Use the EMU values in the Layout section when placing shapes via VBA or python-pptx.
- Font embedding: Embed Freesentation fonts in the file (File → Options → Save → Embed fonts).
- Corner radius in PPT: for `{rounded.pill}` on a rectangle, set `Adjust corner radius` to 50% of the shorter dimension. PPT stores this as a fraction (0–0.5 of shorter side).
- Table cell margins: set to "Narrow" in the Table Tools Layout tab.

### HTML / Web

```css
@font-face {
  font-family: 'Freesentation';
  src: url('Freesentation-3Light.ttf') format('truetype');
  font-weight: 300;
}
@font-face {
  font-family: 'Freesentation';
  src: url('Freesentation-5Medium.ttf') format('truetype');
  font-weight: 500;
}
@font-face {
  font-family: 'Freesentation';
  src: url('Freesentation-7Bold.ttf') format('truetype');
  font-weight: 700;
}

:root {
  --color-primary:          #E63E81;
  --color-primary-active:   #C4326E;
  --color-primary-disabled: #F0A0C0;
  --color-primary-accent:   #FF4A5C;
  --color-primary-pale:     #FFD9E8;

  --color-canvas:              #FFFFFF;
  --color-surface-soft:        #FFF5F8;
  --color-surface-strong:      #FFE0EC;
  --color-surface-dark:        #3D0A20;
  --color-surface-dark-elev:   #5C1435;

  --color-ink:          #1A0810;
  --color-body:         #4A2535;
  --color-muted:        #7A4858;
  --color-muted-soft:   #B08898;
  --color-on-primary:   #FFFFFF;
  --color-on-dark:      #FFFFFF;
  --color-on-dark-soft: #FFB8CC;

  --color-hairline:      #F7BDD0;
  --color-hairline-soft: #FFE0EC;

  --rounded-sm:   4px;
  --rounded-md:   8px;
  --rounded-lg:   12px;
  --rounded-xl:   16px;
  --rounded-xxl:  24px;
  --rounded-pill: 9999px;
  --rounded-full: 9999px;
}

/* 16:9 slide canvas for web */
.slide-canvas {
  width: 1920px;
  height: 1080px;
  aspect-ratio: 16 / 9;
  overflow: hidden;
  position: relative;
  background: var(--color-canvas);
  font-family: 'Freesentation', sans-serif;
  font-weight: 500;
}
```

- Default viewport: 1920 × 1080 px. Scale the `.slide-canvas` with CSS transforms for responsive displays.
- All text sizes: use the web pixel values from the Typography table, with `px` units.

### Executable GUI

- Default window size: 1280 × 720 px (fixed; no resizing unless explicitly required).
- Apply all color tokens and font weights from this system.
- Button components: follow `button-primary` / `button-secondary` specs.
- Use platform-native rounded-rect APIs with the pixel radii from the Geometry section.
