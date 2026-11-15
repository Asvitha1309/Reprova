---
name: Reprova Precision Dark
colors:
  surface: '#0f131d'
  surface-dim: '#0f131d'
  surface-bright: '#353944'
  surface-container-lowest: '#0a0e18'
  surface-container-low: '#171b26'
  surface-container: '#1c1f2a'
  surface-container-high: '#262a35'
  surface-container-highest: '#313540'
  on-surface: '#dfe2f1'
  on-surface-variant: '#c7c4d7'
  inverse-surface: '#dfe2f1'
  inverse-on-surface: '#2c303b'
  outline: '#908fa0'
  outline-variant: '#464554'
  surface-tint: '#c0c1ff'
  primary: '#c0c1ff'
  on-primary: '#1000a9'
  primary-container: '#8083ff'
  on-primary-container: '#0d0096'
  inverse-primary: '#494bd6'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffb2b7'
  on-tertiary: '#67001b'
  tertiary-container: '#ff516a'
  on-tertiary-container: '#5b0017'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e1e0ff'
  primary-fixed-dim: '#c0c1ff'
  on-primary-fixed: '#07006c'
  on-primary-fixed-variant: '#2f2ebe'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffdadb'
  tertiary-fixed-dim: '#ffb2b7'
  on-tertiary-fixed: '#40000d'
  on-tertiary-fixed-variant: '#92002a'
  background: '#0f131d'
  on-background: '#dfe2f1'
  surface-variant: '#313540'
typography:
  headline-xl:
    fontFamily: Geist
    fontSize: 36px
    fontWeight: '600'
    lineHeight: 44px
    letterSpacing: -0.025em
  headline-xl-mobile:
    fontFamily: Geist
    fontSize: 28px
    fontWeight: '600'
    lineHeight: 36px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline-sm:
    fontFamily: Geist
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 26px
    letterSpacing: -0.015em
  body-lg:
    fontFamily: Geist
    fontSize: 15px
    fontWeight: '400'
    lineHeight: 22px
    letterSpacing: -0.01em
  body-md:
    fontFamily: Geist
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
    letterSpacing: -0.005em
  body-sm:
    fontFamily: Geist
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-code-md:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 18px
  label-code-sm:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '600'
    lineHeight: 14px
    letterSpacing: 0.06em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 0.75rem
  gutter-lg: 1.25rem
  margin: 1rem
  margin-lg: 1.5rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 0.75rem
  space-lg: 1rem
  space-xl: 1.5rem
---

## Brand & Style

This design system targets software engineers, QA leads, and devops teams seeking deterministic, automated browser bug isolation. The design ethos combines the hyper-focused efficiency of modern developer consoles (Linear, Raycast, Vercel) with deep observability ergonomics. 

The aesthetic is precision dark minimalist: high spatial density, pixel-crisp borders, neutral atmospheric background layering, and zero ornamental noise. Typography is dialed for scanability across complex stack traces, network payloads, and parallel browser execution matrixes. Visual accents are surgical and purpose-driven: rich purples anchor executive commands, while high-chroma semantic alerts immediately clarify state transitions without cognitive drag.

## Colors

The palette leverages an ink-like obsidian base with subtle slate steps, letting technical output remain primary.

- **Canvas & Layering**:
  - Base canvas: `#0B0F19` (midnight base).
  - Surface elevated panels & sidebars: `#151B2B`.
  - Nested inset wells (code/terminal logs, active run outputs): `#0D121F`.
  - Borders & Dividers: `#222B3E` for prominent framing; `rgba(255, 255, 255, 0.08)` for subtle internal card separators.

- **Interactive Primary**:
  - `#6366F1` (Indigo/Electric Violet) for core CTA surfaces, focused state indicators, and active workflow transitions. Hover: `#4F46E5`.

- **Semantic Signals**:
  - Success/Passed: `#10B981` (Emerald). Emitted on deterministic test passage and script validation.
  - Danger/Reproduced: `#F43F5E` (Crimson Rose). Marks bug confirmations, script timeouts, and fatal runtime exceptions.
  - Warning/Pending: `#F59E0B` (Amber). Used for flaky step flags and ongoing dynamic runs.
  - Neutral / Text: High-contrast primary `#F8FAFC`, muted secondary `#94A3B8`, and faint auxiliary `#64748B`.

## Typography

Geist powers structural labels and layout headings, delivering tight geometric tracking optimized for digital density. JetBrains Mono takes over for code payloads, runtime outputs, keybind tooltips, timestamps, HTTP status tokens, and git SHA hashes.

- **Scale Discipline**: Font sizes are intentionally constrained between 11px and 36px to support dense information environments.
- **Micro-labels**: Status headers and column categorizers use `label-caps` in uppercase styling with deliberate character spacing to maximize readability in narrow sidebars and data grids.

## Layout & Spacing

The layout philosophy follows a responsive, high-density workbench architecture:

- **Structure**: A fixed 240px utility sidebar, collapsible step-inspection panel, and a primary fluid canvas that houses execution timelines, live headless browser viewports, and console dumps.
- **Grids & Layout Rhythm**: Uses an 8-point base grid with 4-point micro-increments. Tight gutters (`0.75rem` / `12px`) guarantee maximum screen real estate on desktop monitors while avoiding visual clutter.
- **Density Control**: Elements prefer compact vertical heights (e.g., table rows capped at 32px or 36px, buttons at 32px).
- **Responsive Adaptations**:
  - **Desktop (>=1200px)**: 3-column split view (Spec Tree -> Execution Viewport -> Trace Log).
  - **Tablet (768px - 1199px)**: Sidebar shrinks to icon-rail mode; trace logs convert into a bottom sliding drawer.
  - **Mobile (<768px)**: Stacked single-column card layout with horizontal swipe tabs across execution steps, logs, and screenshots.

## Elevation & Depth

This design system rejects heavy blur dropshadows in favor of sharp, layered surfaces and hairline contrast edges:

- **Surface Tiers**:
  - `Level 0`: Canvas background (`#0B0F19`).
  - `Level 1`: Panels, sidebars, execution headers (`#151B2B`), delineated by a 1px solid border of `#222B3E`.
  - `Level 2`: Modals, drop-down menus, floating command palettes (`#1E2638`), highlighted with an inner border of `rgba(255, 255, 255, 0.08)`.
- **Shadow Signature**: When required for detached floating elements (e.g., Quick Command Palette `Cmd+K`), use an ultra-diffused shadow with a subtle dark ink tint: `0 16px 36px -8px rgba(0, 0, 0, 0.65), 0 0 0 1px rgba(255, 255, 255, 0.08)`.
- **Focus Rings**: Pure 2px offset-free outline using `#6366F1` with an inner 1px gap matching the container base color.

## Shapes

The design system maintains a modern, crisp edge definition. It leverages roundedness level `1` (Soft) across all elements:
- Base inputs, buttons, chips, and code inline blocks: `4px` (`0.25rem`).
- Cards, modal containers, and tab groups: `8px` (`0.5rem`).
- Outer viewport wrappers and frame canvases: `12px` (`0.75rem`).
- Pills and circles are reserved solely for status indicators and micro-badges to retain a disciplined, engineering-first aesthetic.

## Components

### Buttons
- **Primary**: Background `#6366F1`, text `#FFFFFF`, border `transparent`. Hover `#4F46E5`. Active transforms scale to `0.99`.
- **Secondary / Panel Action**: Background `#151B2B`, text `#F8FAFC`, 1px border `#222B3E`. Hover background `#1E2638`, border `rgba(255, 255, 255, 0.15)`.
- **Danger (Reproduce/Fail)**: Subtle tinted background `rgba(244, 63, 94, 0.12)`, text `#F43F5E`, border `1px solid rgba(244, 63, 94, 0.3)`. Hover background `rgba(244, 63, 94, 0.2)`.
- **Sizes**: Height 28px (compact) and 34px (standard). Typography uses Geist 13px weight 500.

### Input Fields & Terminal Search
- Background `#0D121F` inset with 1px border `#222B3E`.
- Text `#F8FAFC` with placeholder `#64748B`.
- Integrated shortcut token on the trailing edge (e.g., `⌘K`) styled with `JetBrains Mono` at 10px inside a `#151B2B` badge.

### Status Chips & Badges
- **Confirmed Bug / Reproduced**: Background `rgba(244, 63, 94, 0.15)`, text `#F43F5E`, border `1px solid rgba(244, 63, 94, 0.3)`. Accompanied by a pulsing 6px dot.
- **Run Passed**: Background `rgba(16, 185, 129, 0.15)`, text `#10B981`, border `1px solid rgba(16, 185, 129, 0.3)`.
- **Pending Analysis**: Background `rgba(245, 158, 11, 0.15)`, text `#F59E0B`, border `1px solid rgba(245, 158, 11, 0.3)`.

### Cards & Execution Steps
- Background `#151B2B`, radius 8px, border `1px solid #222B3E`.
- Card headers feature an integrated horizontal metadata bar separating trace duration, status chip, and browser engine tags (`Chromium 124`, `WebKit 17`).

### Data Tables & Trace Lists
- Alternating row fills are avoided. Selected rows receive a left 2px border accent in `#6366F1` and a background tint of `rgba(99, 102, 241, 0.08)`.
- Dividers between steps use 1px solid `rgba(255, 255, 255, 0.05)`.
- Numeric row steps, time deltas (+124ms), and network codes render strictly in `JetBrains Mono`.

### Specialized Tooling Components
- **Step Replay Scrubber**: A high-precision horizontal timeline with tick-marks for DOM mutations, console warnings, and screenshot captures.
- **Diff / Code Inspector**: Split view with `#0D121F` base, gutter lines in `#64748B`, added lines tinted `#10B981` (10% fill), and deleted/failed lines tinted `#F43F5E` (10% fill).