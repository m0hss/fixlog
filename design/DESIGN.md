---
name: Dev Terminal Notebook
colors:
  surface: '#111317'
  surface-dim: '#111317'
  surface-bright: '#37393d'
  surface-container-lowest: '#0c0e11'
  surface-container-low: '#1a1c1f'
  surface-container: '#1e2023'
  surface-container-high: '#282a2d'
  surface-container-highest: '#333538'
  on-surface: '#e2e2e6'
  on-surface-variant: '#c3c9ae'
  inverse-surface: '#e2e2e6'
  inverse-on-surface: '#2f3034'
  outline: '#8d937b'
  outline-variant: '#434934'
  surface-tint: '#a2d801'
  primary: '#ffffff'
  on-primary: '#263500'
  primary-container: '#bdf532'
  on-primary-container: '#516e00'
  inverse-primary: '#4c6700'
  secondary: '#c7bfff'
  on-secondary: '#2a039d'
  secondary-container: '#422db2'
  on-secondary-container: '#b4abff'
  tertiary: '#ffffff'
  on-tertiary: '#68000f'
  tertiary-container: '#ffdad8'
  on-tertiary-container: '#b6353a'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#bdf532'
  primary-fixed-dim: '#a2d801'
  on-primary-fixed: '#141f00'
  on-primary-fixed-variant: '#384e00'
  secondary-fixed: '#e4dfff'
  secondary-fixed-dim: '#c7bfff'
  on-secondary-fixed: '#170065'
  on-secondary-fixed-variant: '#422db2'
  tertiary-fixed: '#ffdad8'
  tertiary-fixed-dim: '#ffb3b0'
  on-tertiary-fixed: '#410006'
  on-tertiary-fixed-variant: '#8c1520'
  background: '#111317'
  on-background: '#e2e2e6'
  surface-variant: '#333538'
typography:
  headline-xl:
    fontFamily: Space Grotesk
    fontSize: 3rem
    fontWeight: '700'
    lineHeight: 3.5rem
    letterSpacing: -0.03em
  headline-xl-mobile:
    fontFamily: Space Grotesk
    fontSize: 2rem
    fontWeight: '700'
    lineHeight: 2.5rem
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Space Grotesk
    fontSize: 2.25rem
    fontWeight: '600'
    lineHeight: 2.75rem
    letterSpacing: -0.025em
  headline-lg-mobile:
    fontFamily: Space Grotesk
    fontSize: 1.625rem
    fontWeight: '600'
    lineHeight: 2.125rem
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Space Grotesk
    fontSize: 1.5rem
    fontWeight: '600'
    lineHeight: 2rem
    letterSpacing: -0.02em
  headline-sm:
    fontFamily: Space Grotesk
    fontSize: 1.25rem
    fontWeight: '500'
    lineHeight: 1.75rem
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 1.125rem
    fontWeight: '400'
    lineHeight: 1.85rem
  body-md:
    fontFamily: Inter
    fontSize: 1rem
    fontWeight: '400'
    lineHeight: 1.65rem
  body-sm:
    fontFamily: Inter
    fontSize: 0.875rem
    fontWeight: '400'
    lineHeight: 1.45rem
  code-inline:
    fontFamily: JetBrains Mono
    fontSize: 0.875em
    fontWeight: '400'
    lineHeight: '1.2'
  code-block:
    fontFamily: JetBrains Mono
    fontSize: 0.875rem
    fontWeight: '400'
    lineHeight: 1.6rem
  label-md:
    fontFamily: JetBrains Mono
    fontSize: 0.8125rem
    fontWeight: '500'
    lineHeight: 1.25rem
    letterSpacing: 0.04em
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 0.6875rem
    fontWeight: '500'
    lineHeight: 1rem
    letterSpacing: 0.06em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1.5rem
  gutter-mobile: 1rem
  margin: 2rem
  margin-mobile: 1rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2.5rem
---

## Brand & Style

The design system embodies the tension between a high-utility UNIX terminal and an intimate, unpolished research lab notebook. Built for engineers, tinkerers, and builders who appreciate raw technical depth wrapped in calculated aesthetic restraint, it trades sterile corporate polish for playful candor and field-tested reality.

Visually, the style merges dark-mode minimalism with tactile hacker artifacts: faint dot-grid patterns reminiscent of gridded engineering pads, hairline borders mimicking CRT phosphor framing, and sharp neon data points punctuating deep space. The emotional experience balances the thrill of a breakthrough with the messy humor of debugging at 3:00 AM—unfiltered, technical, and deliberate.

## Colors

The palette operates on an ultra-dark field inspired by low-reflection terminal emulators, punctuated by high-potency status accents:

- **Canvas & Surface**: Pure near-black canvas (`#0B0D10`) with stepped elevation via hairline dividers (`#1F242C`) and subtle surface fills (`#13171D`, `#191F27`).
- **Typography & Neutrals**: Primary readability is driven by soft off-white (`#E6EDF3`), preventing the harsh optical fatigue of pure `#FFFFFF`. Secondary metadata uses muted slate (`#8A95A5`), while inactive structures rest in steel (`#485263`).
- **Accent & Functional Outcomes**:
  - `Worked`: Acid Lime (`#C6FF3D`) serves as the primary visual hook and confirmation signal.
  - `Still Poking`: Electric Violet (`#8B7CFF`) acts as secondary accent for exploratory states, deep dives, and system notes.
  - `Didn't Work`: Vibrant Coral (`#FF6B6B`) provides high-contrast failure telemetry without feeling punitive.
  - `In Progress`: Warm Amber (`#FFB84D`) flags active diagnostics and ongoing experiments.
- **Accents & Effects**: Acid Lime and Violet are leveraged in ultra-subtle, high-blur ambient glows (`box-shadow: 0 0 24px -6px rgba(198, 255, 61, 0.18)`), reserved strictly for interactive focus, active tabs, and outcome hero badges.

## Typography

Typography establishes an intentional tri-font hierarchy that directly maps function to typographic voice:

1. **Space Grotesk** handles editorial display and structural headings. Its geometric rhythm and idiosyncratic letterforms provide an inventive, experimental tone.
2. **Inter** provides high legibility for long-form narrative text, post breakdowns, and analysis notes. It recedes into the background to allow rapid absorption.
3. **JetBrains Mono** anchors the developer identity. It is applied strictly to data metadata, timestamps, outcome tags, inline code snippets, terminal traces, and prompt lines (`$`).

## Layout & Spacing

The layout philosophy uses a centered, disciplined column grid layered over an ambient 24px dot-grid background (`radial-gradient(#1F242C 1px, transparent 1px)`).

- **Desktop (>= 1024px)**: Max reading container width of 768px for single-column entries to preserve optimal 65–75 character line lengths. Main portal/index views expand to a 12-column grid constrained to 1120px with 24px gutters and 32px canvas margins.
- **Tablet (768px - 1023px)**: 8-column layout with 24px margins and gutters. Side-by-side metadata collapses to contextual inline banners.
- **Mobile (< 768px)**: Single column with 16px lateral padding. Horizontal scroll rails are utilized for dense tabular data and code snippets with gradient edge fades.

## Elevation & Depth

Depth is defined through layered dark surfaces and hairline boundaries rather than dramatic physical drop shadows.

- **Base Layer (Level 0)**: `#0B0D10` base canvas with 1px dot-grid pattern (`rgba(31, 36, 44, 0.6)` at 20px intervals).
- **Surface Layer (Level 1)**: `#13171D` container fills with a crisp `1px solid #1F242C` outline. No shadow.
- **Hover & Overlay Layer (Level 2)**: `#191F27` container fill with a slightly highlighted border (`#2F3744`). Interactive cards gain an ambient diffuse bloom: `0 4px 20px -2px rgba(0, 0, 0, 0.5), 0 0 16px -4px rgba(198, 255, 61, 0.12)`.
- **Floating Modals & Command Palette (Level 3)**: `#11141A` with `backdrop-filter: blur(16px)` and a dual border structure (`1px solid #2F3744` with a subtle inner rim `inset 0 1px 0 0 rgba(255, 255, 255, 0.05)`).

## Shapes

The design system employs a structured 16px (`rounded-lg` at scale 2) container radius, balancing the sharp, utilitarian ethos of developer terminals with the friendlier, approachable feel of a personal creative notebook:

- **Cards & Modals**: 16px border-radius (`1rem`).
- **Interactive Controls (Inputs, Buttons)**: 8px border-radius (`0.5rem`).
- **Tags, Outcome Chips, Keycaps**: 4px to 6px border-radius (`0.25rem` to `0.375rem`) for compact precision.
- **Floating Status Beads**: 9999px (Pill/Circle) for active telemetry dots.

## Components

### 1. Cards (Log Entries & Field Notes)
- Background: `#13171D`, border: `1px solid #1F242C`, radius: `16px`.
- Padding: `1.5rem` (`space-lg`).
- Behavior: Hover lifts border color to `#2F3744` and injects a soft radial glow matching the card's specific outcome tag.
- Header contains an inline monospaced metadata row: `ENTRY #042 // [TIMESTAMP] // [OUTCOME-BADGE]`.

### 2. Status Outcome Badges
Compact pill markers with `label-sm` JetBrains Mono uppercase typography:
- **Worked**: Text `#C6FF3D`, background `rgba(198, 255, 61, 0.08)`, border `1px solid rgba(198, 255, 61, 0.25)`.
- **Didn't Work**: Text `#FF6B6B`, background `rgba(255, 107, 107, 0.08)`, border `1px solid rgba(255, 107, 107, 0.25)`.
- **In Progress**: Text `#FFB84D`, background `rgba(255, 184, 77, 0.08)`, border `1px solid rgba(255, 184, 77, 0.25)`.
- **Still Poking**: Text `#8B7CFF`, background `rgba(139, 124, 255, 0.08)`, border `1px solid rgba(139, 124, 255, 0.25)`.

### 3. Buttons
- **Primary**: Background `#C6FF3D`, text `#0B0D10`, font `Space Grotesk` (weight 600), radius `8px`. Hover: `filter: brightness(1.1); box-shadow: 0 0 16px rgba(198, 255, 61, 0.35)`.
- **Secondary / Ghost**: Background `transparent`, text `#E6EDF3`, border `1px solid #1F242C`. Hover: Background `#191F27`, border `#2F3744`.

### 4. Command Palette (⌘K) Indicator & Modal
- **Indicator**: Compact keycap badge in header. Background `#13171D`, border `1px solid #1F242C`, text `#8A95A5`, font `JetBrains Mono`. Includes physical key styling (`kbd` tag with slight lower shadow).
- **Modal**: Centered overlay with backdrop blur. Input field styled with green command prompt (`>_`) cursor prefix in `#C6FF3D`.

### 5. Code Blocks & Terminal Traces
- Background `#0D1014`, border `1px solid #1F242C`, radius `12px`.
- Header bar includes faux OS window dots (subdued slate, not rainbow) and an instant "COPY // RAW" toggle in `JetBrains Mono`.

### 6. Minimal RSS / Atom Feed Trigger
- Low-key utilitarian anchor rendered as `[RSS FEED // XML]` in `label-sm`.
- Accent color transition to `#8B7CFF` on hover with a micro terminal arrow indicator (`->`).

### 7. Form Controls (Input & Selection)
- **Inputs**: Dark field `#0E1116`, border `1px solid #1F242C`, text `#E6EDF3`. Focus: Border `#C6FF3D`, inner shadow zero, subtle outer ring `0 0 0 1px #C6FF3D`.
- **Checkboxes**: Custom square with `4px` radius, background `#13171D`, border `1px solid #1F242C`. Checked: Background `#C6FF3D`, checkmark `#0B0D10`.