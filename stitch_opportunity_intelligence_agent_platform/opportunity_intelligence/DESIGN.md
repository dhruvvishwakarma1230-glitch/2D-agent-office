---
name: Opportunity Intelligence
colors:
  surface: '#f8f9ff'
  surface-dim: '#cbdbf5'
  surface-bright: '#f8f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eff4ff'
  surface-container: '#e5eeff'
  surface-container-high: '#dce9ff'
  surface-container-highest: '#d3e4fe'
  on-surface: '#0b1c30'
  on-surface-variant: '#444653'
  inverse-surface: '#213145'
  inverse-on-surface: '#eaf1ff'
  outline: '#757684'
  outline-variant: '#c4c5d5'
  surface-tint: '#3755c3'
  primary: '#00288e'
  on-primary: '#ffffff'
  primary-container: '#1e40af'
  on-primary-container: '#a8b8ff'
  inverse-primary: '#b8c4ff'
  secondary: '#565e74'
  on-secondary: '#ffffff'
  secondary-container: '#dae2fd'
  on-secondary-container: '#5c647a'
  tertiary: '#002e81'
  on-tertiary: '#ffffff'
  tertiary-container: '#0042b2'
  on-tertiary-container: '#a4b9ff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dde1ff'
  primary-fixed-dim: '#b8c4ff'
  on-primary-fixed: '#001453'
  on-primary-fixed-variant: '#173bab'
  secondary-fixed: '#dae2fd'
  secondary-fixed-dim: '#bec6e0'
  on-secondary-fixed: '#131b2e'
  on-secondary-fixed-variant: '#3f465c'
  tertiary-fixed: '#dbe1ff'
  tertiary-fixed-dim: '#b4c5ff'
  on-tertiary-fixed: '#00174b'
  on-tertiary-fixed-variant: '#003ea8'
  background: '#f8f9ff'
  on-background: '#0b1c30'
  surface-variant: '#d3e4fe'
typography:
  headline-xl:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
    letterSpacing: -0.015em
  headline-lg:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.015em
  headline-lg-mobile:
    fontFamily: Inter
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 26px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Inter
    fontSize: 15px
    fontWeight: '600'
    lineHeight: 22px
  body-lg:
    fontFamily: Inter
    fontSize: 15px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 18px
  label-md:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: '500'
    lineHeight: 14px
    letterSpacing: 0.04em
  label-xs:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '600'
    lineHeight: 12px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-sm: 0.75rem
  gutter-lg: 1.5rem
  margin: 1.5rem
  margin-sm: 1rem
  margin-lg: 2.5rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 0.75rem
  space-lg: 1.25rem
  space-xl: 2rem
---

## Brand & Style

This design system serves an enterprise-grade opportunity intelligence platform engineered for high-density analysis, discovery, and automated agent workflows. It sits squarely between the structured legibility of Notion and the focused networking utility of LinkedIn, pairing rigorous data clarity with rapid scannability.

The emotional signature is poised, authoritative, and analytical. Users should experience zero visual friction, feeling immediate confidence in signal validity, data provenance, and automated intelligence. 

The aesthetic is Modern Corporate with a deliberate dual-mode personality:
1. **Intelligence Engine (Default)**: Crisp, high-utility operational environment featuring low-contrast outlines, high-density structured tables, pill badges, and restrained structural typography.
2. **Agent Office (Tactile Sub-environment)**: A warm, isometric/pixel-inspired spatial view where background automation and multi-agent coordination are rendered visually accessible. It employs warm cream flooring, honey-amber woodwork, and structured foliage tones to evoke an organized mid-century operational command post without breaking structural token parity.

## Colors

The core color strategy emphasizes clarity and scannability, utilizing deep slate blues for structural anchor points and reserving vibrant tones exclusively for actionable state changes and verification signals.

### Surface & Neutral Architecture
- **Base Canvas**: `#F8FAFC` provides an eye-resting foundation with reduced glare during extended analytical sessions.
- **Surface Elevation**: `#FFFFFF` cards and inspect panels project clean structural planes against the canvas.
- **Subtle Surface & Inset Wells**: `#F1F5F9` is applied to table headers, code blocks, empty states, and inactive filters.
- **Structural Borders**: `#E2E8F0` defines ghost borders and structural cell separators at strict 1px widths.
- **Body & Headline Text**: Deep slate `#0F172A` provides optimal typographic contrast, stepped down to `#475569` for secondary copy and `#64748B` for metadata timestamps and label prefixes.

### Brand & Interactive Tones
- **Primary Interactive (Action)**: `#2563EB` handles primary callouts, button actions, and focus rings.
- **Deep Navy (Brand & Structure)**: `#1E40AF` serves as the anchor for persistent side-navigation states, key badge containers, and intelligence indicators.

### Semantic Status Tokens
- **Verified / High Signal**: `#059669` (surface fill: `#ECFDF5`, border: `#A7F3D0`).
- **Uncertainty / Pending Review**: `#D97706` (surface fill: `#FFFBEB`, border: `#FDE68A`).
- **Alert / At-Risk / Expired**: `#DC2626` (surface fill: `#FEF2F2`, border: `#FECACA`).

### Agent Office Thematic Extension (Scoped Tokens)
- **Flooring Canvas**: Primary `#FDFBF7`, alternate parquetry `#F5EFEB`.
- **Architectural Wood & Desks**: Deep walnut `#854D0E`, warm teak `#B45309`, light beech `#D97706`.
- **Office Infrastructure**: Task chairs `#2563EB`, botanical accents `#15803D` (leaf highlight `#22C55E`).

## Typography

Typography prioritizes rapid document scanning and tabular layout stability. 

- **Primary Interface Font (Inter)**: Handles all structural layout titles, entity names, descriptions, and user inputs. Its tall x-height and neutral geometry ensure legible rendering at dense sizes (12px–14px).
- **Metadata & Telemetry Font (JetBrains Mono)**: Applied systematically to signal confidence metrics, dates, match scores, verified source links, and ticker tags. Monospaced rendering ensures numerical figures remain aligned across stacked comparison rows.

Use negative tracking exclusively on headlines sized 18px and above to produce a tight, editorial presence. Ensure all uppercase tags set in `JetBrains Mono` maintain expanded tracking (`+0.04em` to `+0.05em`) to preserve legibility across low-contrast badges.

## Layout & Spacing

The layout model utilizes a hybrid system: a persistent 240px collapsable left navigation rail paired with a 12-column responsive fluid grid across the primary workspace.

### Form Factor Behavior
- **Desktop (> 1280px)**: 12-column grid with `1.5rem` gutters and `2.5rem` outer margins. Supports side-by-side analytical split screens (e.g., list feed left at 5 columns, detail inspector right at 7 columns).
- **Tablet (768px – 1279px)**: 8-column grid with `1rem` gutters and `1.5rem` outer canvas padding. Sidebar collapses into an icon dock (64px width). Detail panels convert to sliding overlays.
- **Mobile (< 768px)**: 4-column fluid layout with `0.75rem` gutters and `1rem` edge margins. Primary view converts to single-stack feed cards; full-screen modal overlays handle opportunity inspection and evidence trails.

The rhythmic scale relies strictly on 4px and 8px multipliers. Dense components (tables, badges, action toolbars) utilize `space-xs` (4px) and `space-sm` (8px), while layout containers adhere to `space-md` (12px), `space-lg` (20px), and `space-xl` (32px).

## Elevation & Depth

This system avoids heavy drop shadows, relying on low-contrast outlines and subtle tonal layering to construct visual hierarchy.

- **Level 0 (Canvas Base)**: `#F8FAFC`. Completely flat; structural ground plane.
- **Level 1 (Card & Content Blocks)**: `#FFFFFF` filled surface with a continuous `1px solid #E2E8F0` border. No drop shadow. Hover state triggers a border color transition to `#CBD5E1` and a hyper-subtle ambient lift (`0 1px 3px rgba(15, 23, 42, 0.04)`).
- **Level 2 (Floating Popovers, Dropdowns, Flyouts)**: `#FFFFFF` surface, `1px solid #E2E8F0` border, paired with an ambient shadow: `0 4px 16px -2px rgba(15, 23, 42, 0.08), 0 2px 4px -1px rgba(15, 23, 42, 0.04)`.
- **Level 3 (Modal Dialogs & Command Bar)**: Centered structural overlay backed by an ultra-subtle tinted scrim (`rgba(15, 23, 42, 0.4)` with `backdrop-filter: blur(2px)`). Shadow: `0 12px 32px -4px rgba(15, 23, 42, 0.12)`.
- **Agent Office Sub-Viewport**: Uses a distinct crisp pixel border aesthetic: sharp 1px structural inset lines (`#E2D9C8`) over warm `#FDFBF7` canvas, intentionally bypassing soft blurs in favor of architectural precision.

## Shapes

The design system employs a disciplined, soft corner vocabulary (`roundedness: 1`). Radii are kept small to reinforce an efficient, enterprise data-tool aesthetic:

- **Inputs, Buttons, and Select Menus**: `4px` (`rounded-sm` / `0.25rem`).
- **Cards, Table Shells, and Modules**: `8px` (`rounded-lg` / `0.5rem`).
- **Dialogs and Inspector Panels**: `12px` (`rounded-xl` / `0.75rem`).
- **Pills, Status Badges, and Verification Tags**: `9999px` (Full pill shape). Badges use circular geometry to contrast against the rectangular grid structure of cards and tables.

## Components

### Buttons
- **Primary**: Solid `#2563EB` background, white text, 4px radius. Height 36px (compact: 30px). Hover: `#1E40AF`. Active: `#1D4ED8`. Focus: 2px offset ring in `#2563EB`.
- **Secondary**: `#FFFFFF` background with `1px solid #E2E8F0` border, text `#0F172A`. Hover: background `#F8FAFC` and border `#CBD5E1`.
- **Ghost/Tertiary**: Transparent surface, text `#475569`. Hover: `#F1F5F9`, text `#0F172A`.

### Verification Badges & Status Chips
- Height is fixed at 22px with full pill rounding (`rounded-full`).
- Typography is strictly `label-xs` set in `JetBrains Mono`.
- **Verified**: Background `#ECFDF5`, text `#059669`, border `1px solid #A7F3D0`, prepended with a 6px solid green dot or micro-check icon.
- **Uncertainty**: Background `#FFFBEB`, text `#D97706`, border `1px solid #FDE68A`.
- **Alert / Urgent**: Background `#FEF2F2`, text `#DC2626`, border `1px solid #FECACA`.
- **Confidence Score Pill**: Background `#F1F5F9`, text `#334155`, border `1px solid #E2E8F0`, presenting numerical percentages (`94.2% MATCH`).

### Opportunity Detail Cards
- Structured compound card containing three tiers:
  1. **Header Row**: Left-aligned entity title (`headline-sm`), right-aligned confidence score pill, and timestamp (`label-sm`).
  2. **Metadata Matrix**: 2- or 3-column micro-grid showing deal size, velocity, and territory in `body-sm` muted text.
  3. **Evidence Footer**: Separated by a `1px solid #F1F5F9` divider, detailing source citations (e.g., "SEC Filings", "Team Expansion") with quick-link triggers.

### Input Fields & Search Bars
- Standard height 36px, `4px` radius, `#FFFFFF` background, border `1px solid #CBD5E1`.
- Typographic style: `body-md` (`#0F172A`), placeholder `#94A3B8`.
- Focus state: Border transitions to `#2563EB` with an ambient glow (`box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.15)`).
- Search inputs include a leading 14px monochrome lens icon and a trailing keyboard shortcut tag (`⌘K`) in `label-xs` using `#F1F5F9` background and `#64748B` text.

### Checkboxes & Radio Controls
- Dimensions: 16px × 16px.
- Checkbox has a `3px` corner radius; radio is fully circular.
- Unchecked: `1px solid #CBD5E1` on `#FFFFFF`. Checked: solid `#2563EB` fill with crisp white check/dot icon.

### Agent Office Interface Modules
- Specialized retro-warm cards for live agent orchestration. 
- Border: `1px solid #E5DECF`. Background: `#FDFBF7`. 
- Status indicator: Monospaced running status line (`JetBrains Mono`, 11px) with pulsating green terminal dot (`#15803D`) signaling active model scraping or processing.