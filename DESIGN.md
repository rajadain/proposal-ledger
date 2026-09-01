---
name: Proposal Ledger
description: A proposal-hours outliner in the Flexoki palette, where serif structure meets a monospace ledger column.
colors:
  accent-blue: "#205EA6"
  ink: "#100F0F"
  total-ink: "#100F0F"
  muted: "#6F6E69"
  surface-canvas: "#F2F0E5"
  surface-panel: "#FFFCF0"
  surface-leaf: "#E6E4D9"
  accent-soft: "#E1ECEB"
  line: "#DAD8CE"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif"
    fontSize: "20px"
    fontWeight: 650
    lineHeight: 1.4
    letterSpacing: "-0.01em"
  section:
    fontFamily: "ui-serif, 'New York', Georgia, Cambria, 'Times New Roman', Times, serif"
    fontSize: "22px"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: "-0.02em"
  subsection:
    fontFamily: "ui-serif, 'New York', Georgia, Cambria, 'Times New Roman', Times, serif"
    fontSize: "18.5px"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: "-0.015em"
  body:
    fontFamily: "ui-serif, 'New York', Georgia, Cambria, 'Times New Roman', Times, serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.35
    letterSpacing: "normal"
  data:
    fontFamily: "ui-monospace, 'SF Mono', SFMono-Regular, Menlo, Consolas, 'Liberation Mono', monospace"
    fontSize: "15px"
    fontWeight: 700
    lineHeight: 1.35
    letterSpacing: "normal"
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif"
    fontSize: "13.5px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "normal"
rounded:
  sm: "6px"
  md: "7px"
  lg: "9px"
  xl: "12px"
spacing:
  s1: "4px"
  s2: "8px"
  s3: "12px"
  s4: "16px"
  s5: "24px"
  s6: "32px"
components:
  button-default:
    backgroundColor: "{colors.surface-panel}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.lg}"
    padding: "7px 12px"
  button-primary:
    backgroundColor: "{colors.accent-blue}"
    textColor: "#FFFCF0"
    typography: "{typography.label}"
    rounded: "{rounded.lg}"
    padding: "7px 12px"
  button-primary-hover:
    backgroundColor: "#1A4F8C"
    textColor: "#FFFCF0"
    rounded: "{rounded.lg}"
    padding: "7px 12px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.lg}"
    padding: "7px 12px"
  hours-input:
    backgroundColor: "{colors.surface-leaf}"
    textColor: "{colors.total-ink}"
    typography: "{typography.data}"
    rounded: "{rounded.md}"
    padding: "4px 6px"
    width: "52px"
  sheet-card:
    backgroundColor: "{colors.surface-panel}"
    rounded: "{rounded.xl}"
    padding: "8px 0"
  toggle:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    rounded: "{rounded.md}"
    size: "24px"
  toggle-hover:
    backgroundColor: "{colors.accent-soft}"
    textColor: "{colors.accent-blue}"
    rounded: "{rounded.md}"
    size: "24px"
---

# Design System: Proposal Ledger

## Overview

**Creative North Star: "The Proposal Ledger"**

Proposal Ledger is where an editor's outline meets an accountant's column. The
work — the estimate itself — is set in a serif and reads top‑to‑bottom like a
proposal draft, while every hour is a monospace, tabular figure locked to a
single right‑hand gutter that totals into the header like the bottom line of a
ledger. The palette is [Flexoki](https://stephango.com/flexoki) — an inky scheme
modeled on analog printing inks and warm shades of paper — so the surface reads
as warm stock rather than clinical white, one quiet ink‑blue is the only accent,
and generous air between sections makes the structure legible before a single
number is read.

Nothing decorates. Surfaces are flat at rest; depth and color arrive only when
you act — a focus border, a floating action pill, a leaf dot. The one accent
blue is rationed hard so that when it appears it always means "this is live."
The result should feel like a well‑kept worksheet you trust: dense enough to
hold a real breakdown, quiet enough to think in.

This world rejects dashboard maximalism — no gradient fills, no glassmorphism,
no heavy drop shadows, no icon‑and‑stat cards. It also rejects the spreadsheet's
undifferentiated grid: hierarchy here comes from type size and whitespace, not
from boxing every row.

**Key Characteristics:**
- Serif outline, monospace numbers, sans chrome — three voices, three jobs.
- Font size encodes nesting depth; the deeper the bullet, the smaller (to a floor).
- One rationed ink‑blue accent; everything else is warm ink on paper.
- Flat by default; depth is a response to interaction, never decoration.
- A single anchored number column that lands in the grand total.

## Colors

The [Flexoki](https://stephango.com/flexoki) palette: a warm paper‑and‑ink
system carrying exactly one accent. Values below are the light‑theme (default)
source of truth; the dark theme redefines the same nine tokens (see the
Dual‑Theme Rule). Following Flexoki convention, light mode uses the 600‑weight
accents and dark mode uses the 400‑weight.

### Primary
- **Ledger Blue** (`#205EA6`, Flexoki blue‑600): The sole accent. Appears only on leaf bullet dots,
  input/toggle focus, and the single primary action (Copy Markdown). Never a
  fill behind text, never body color. Dark theme uses Flexoki blue‑400 (`#4385BE`).

### Neutral
- **Paper** (`#FFFCF0`, Flexoki paper): The estimate sheet — the primary reading surface.
- **Base Canvas** (`#F2F0E5`, Flexoki base‑50): The stock behind the sheet, and the resting row hover.
- **Leaf Field** (`#E6E4D9`, Flexoki base‑100): The subtle inset behind an editable hours input, marking it as the one typeable number.
- **Ink** (`#100F0F`, Flexoki black): Primary text, the app title, and the numbers.
- **Muted** (`#6F6E69`, Flexoki base‑600): Metadata, unit labels, parent chevrons, hint text.
- **Line** (`#DAD8CE`, Flexoki base‑150): Section dividers, card borders, indent guides.
- **Accent Soft** (`#E1ECEB`, Flexoki blue‑50): The wash behind a focused field or a hovered collapse toggle.

### Named Rules
**The One Blue Rule.** Ledger Blue covers a tiny fraction of any screen — dots,
focus, one button. Its rarity is what makes it read as "interactive." Never use
it as a surface fill or for prose.

**The Dual‑Theme Rule.** Color is addressed only through the nine semantic
tokens; both themes redefine the *same* tokens (dark, Flexoki: canvas `#100F0F`,
panel `#1C1B1A`, ink `#CECDC3`, muted `#878580`, line `#343331`, accent `#4385BE`,
accent‑soft `#101A24`, total `#E6E4D9`, leaf `#282726`). Never hard‑code a raw
color at a call site; on dark surfaces, muted text is tinted from the hue, never
flat gray.

## Typography

**Outline Font:** `ui-serif` (New York / Georgia fallback)
**Number Font:** `ui-monospace` (SF Mono / Menlo fallback)
**Chrome Font:** system sans (`-apple-system` stack)

**Character:** An editorial serif gives the estimate the voice of a written
proposal; a tabular monospace turns every hour into aligned data; a neutral sans
keeps the app's controls quiet and out of the way. The three never blur into one
another.

### Hierarchy
- **Display** (sans, 650, 20px, -0.01em): The app title "Proposal Ledger" only.
- **Section** (serif, 600, 22px, 1.35): Top‑level (level‑0) outline rows.
- **Subsection** (serif, 600, 18.5px): Level‑1 outline rows; level‑2 steps to 16.5px.
- **Body** (serif, 400, 15px, 1.35): Leaf rows and level‑3+ outline text; the size floor.
- **Data** (mono, 700, 15px, tabular): All hour figures; the header total renders at 22px.
- **Label** (sans, 400, 13.5px): Toolbar buttons; the keyboard hint runs at 12.5px with mono `kbd` chips.

### Named Rules
**The Three Voices Rule.** Serif is for the outline, monospace is for numbers,
sans is for chrome. A number is never serif; a control label is never a serif;
the outline is never sans.

**The Depth Ramp Rule.** Font size encodes nesting: 22 → 18.5 → 16.5 → 15px as
you descend. The ramp never drops below the 15px body floor, so a leaf is never
smaller than comfortable no matter how deep it sits.

## Layout

A single centered column (max‑width 920px) on paper, holding one bordered sheet.
Spacing follows a 4‑based scale (`4 / 8 / 12 / 16 / 24 / 32`); horizontal gutter
and the numeric column are fixed tokens (`--pad-x: 16px`, `--hours-col: 74px`,
`--indent-step: 22px`).

Rhythm is deliberate rather than uniform: generous air (24px) plus a full‑bleed
1px rule precedes every top‑level section, while child rows sit tight beneath at
a 36px min row height. Nesting is shown by stretched vertical indent guides, not
by boxing rows. The layout is intrinsically responsive — the toolbar wraps and
the column fluidly narrows — with no hard breakpoints; long labels wrap while the
number stays vertically centered.

### Named Rules
**The Anchored Column Rule.** Every hour right‑aligns to one gutter that lands
directly under the header grand total. Leaf rows carry an editable field; parent
rows show a computed, display‑only sum. Parents are never typed.

## Elevation & Depth

Flat by default. The system conveys structure through tonal surfaces (paper →
panel → leaf field) and hairline lines, not stacked shadows. Two soft ambient
shadows exist, and both are quiet: the resting sheet/button lift, and the
floating action pill that appears on row hover.

### Shadow Vocabulary
- **Resting lift** (`box-shadow: 0 1px 2px rgba(16,15,15,.05), 0 8px 24px rgba(16,15,15,.07)`): The sheet, buttons, and the action pill. In dark theme: `0 1px 2px rgba(0,0,0,.4), 0 10px 30px rgba(0,0,0,.5)`.

### Named Rules
**The Flat‑By‑Default Rule.** Surfaces are flat at rest. Depth and color are a
*response* to interaction — the hover action pill lifting in, a focus border, a
toggle's soft wash — never ambient ornament.

## Shapes

A soft, consistent radius family and hairline borders. Corners round on a
four‑step scale: 6px (focus targets, text field), 7px (hour inputs, collapse
toggles), 9px (buttons, the action pill), 12px (the sheet). Borders are always
1px in the Line token; there are no thick or colored side‑borders. Icons are
authored SVG on a 16px grid at a single 1.6px stroke with round caps/joins.

## Components

### Buttons
- **Shape:** 9px radius (`{rounded.lg}`), 1px Line border, resting lift shadow.
- **Default:** Paper background, Ink text, 13.5px sans, `7px 12px` padding. Hover lightens to Base Canvas (`#F2F0E5`) with a `#CECDC3` border.
- **Primary:** Ledger Blue fill, Paper text (the single Copy Markdown action). Hover deepens to blue‑700 (`#1A4F8C`); in dark mode it brightens to blue‑300 and carries Ink text for contrast.
- **Ghost:** Transparent, no shadow (Import, Load sample, theme, Clear all).

### Hours field (signature)
- **Leaf input:** Leaf Field background, Ink monospace, 7px radius, `4px 6px` padding, 52px wide, right‑aligned. Transparent border at rest → Line on hover → Ledger Blue on focus (background flips to Paper). Focusing a `0` clears it so typing replaces.
- **Parent total:** Same monospace/weight, no field background — display‑only, signalling it cannot be typed.

### Collapse toggle & bullets (signature)
- **Leaf:** a 2.6px‑radius filled Ledger‑Blue dot in a 24×24 target.
- **Parent:** a Muted chevron in a 24×24 button — right when collapsed, down when open — with `aria-expanded`. Hover fills Accent Soft and turns the chevron Ledger Blue.

### Row action pill
- A floating panel pill (9px radius, Line border, resting lift) anchored just left of the number gutter, holding five 26px SVG icon buttons (indent, outdent, move up/down, delete). Opacity 0 at rest; fades and slides in on row hover/focus, so numbers stay visible and the row stays quiet until touched. Delete tints red on hover.

### Outline row
- Flex row, 36px min height, centered. Stretched 1px indent guides at 0.55 opacity show nesting. Level‑0 rows are preceded by 24px air and a full‑bleed 1px rule.

## Do's and Don'ts

### Do:
- **Do** keep every number monospace and tabular, right‑anchored to the 74px hours gutter that lands under the grand total.
- **Do** size outline rows by depth (22 / 18.5 / 16.5 / 15px) and never below the 15px floor.
- **Do** draw icons as authored SVG at a 1.6px stroke; leaf = dot, parent = chevron.
- **Do** separate top‑level sections with 24px air and a full‑bleed 1px Line rule.
- **Do** address color only through the nine semantic tokens so both themes stay in sync; tint muted text from the hue on dark surfaces.

### Don't:
- **Don't** use Ledger Blue as a surface fill or for body text — keep it rationed to dots, focus, and the one primary action.
- **Don't** make parent rows editable; their numbers are computed roll‑ups.
- **Don't** reintroduce unicode glyphs or emoji as icons.
- **Don't** add gradients, glass/blur decoration, or hard offset shadows; the world is flat and quiet.
- **Don't** mix the three type voices — serif outline, monospace numbers, sans chrome stay in their lanes.
