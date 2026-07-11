# Design

## Theme

Dark-primary premium consulting brand. Deep, authoritative base with luxurious gold accents. The scene: a dimly-lit executive boardroom, polished surfaces reflecting strategic insight. Not a bright startup hub — a room where decisions are made.

## Color Palette

### Primary Roles

| Role | OKLCH | Usage |
|------|-------|-------|
| `--ink` | `oklch(0.13 0.02 260)` | Primary text, headings, deep backgrounds |
| `--surface` | `oklch(0.98 0.005 260)` | Page background, light sections |
| `--surface-alt` | `oklch(0.95 0.01 260)` | Alternate section backgrounds |
| `--accent` | `oklch(0.75 0.15 85)` | Gold accents, CTAs, highlights |
| `--accent-hover` | `oklch(0.68 0.18 85)` | Gold accent hover state |
| `--muted` | `oklch(0.55 0.02 260)` | Secondary text, captions |
| `--deep` | `oklch(0.15 0.04 260)` | Hero backgrounds, dark sections |
| `--deep-surface` | `oklch(0.20 0.03 260)` | Cards on dark backgrounds |
| `--border` | `oklch(0.90 0.01 260)` | Subtle borders, dividers |
| `--success` | `oklch(0.65 0.15 155)` | Positive indicators |
| `--error` | `oklch(0.60 0.20 25)` | Error states |

### Color Strategy

**Committed**: Deep navy/near-black dominates the hero and key sections (40-50% of surface). Clean off-white provides breathing room. Gold is used sparingly (≤5%) for maximum impact — button hovers, accent lines, icon highlights, small decorative elements.

## Typography

### Font Stack

- **Headings**: `'Inter', 'system-ui', sans-serif` — Weight 700-800
- **Body**: `'Inter', 'system-ui', sans-serif` — Weight 400-500
- **Accent/Numbers**: `'Inter', 'system-ui', sans-serif` — Weight 600-700

### Scale

| Token | Size | Line Height | Usage |
|-------|------|-------------|-------|
| `--text-hero` | `clamp(2.5rem, 5vw, 4.5rem)` | 1.1 | Hero headline |
| `--text-display` | `clamp(2rem, 4vw, 3.5rem)` | 1.15 | Section headlines |
| `--text-heading` | `clamp(1.5rem, 3vw, 2rem)` | 1.2 | Sub-headings |
| `--text-body` | `clamp(1rem, 1.2vw, 1.125rem)` | 1.6 | Body text |
| `--text-small` | `0.875rem` | 1.5 | Captions, labels |
| `--text-micro` | `0.75rem` | 1.4 | Badges, tags |

### Type Treatment

- `text-wrap: balance` on all headlines
- `text-wrap: pretty` on body paragraphs
- Letter-spacing: -0.02em on display text, normal on body
- Max line length: 65ch for body text

## Spacing

| Token | Value | Usage |
|-------|-------|-------|
| `--space-xs` | `0.5rem` | Tight gaps |
| `--space-sm` | `1rem` | Component internal |
| `--space-md` | `1.5rem` | Card padding |
| `--space-lg` | `2.5rem` | Section gaps |
| `--space-xl` | `4rem` | Major sections |
| `--space-2xl` | `6rem` | Hero/padding |

## Layout

- Max content width: `1200px`
- Grid: `repeat(auto-fit, minmax(300px, 1fr))` for card grids
- Flexbox for 1D layouts
- Responsive breakpoints: 480px, 768px, 1024px, 1280px

## Components

### Buttons

- **Primary**: `--deep` background, `--surface` text, gold border accent on hover
- **Secondary**: Transparent with gold border, gold text
- **Size**: Generous padding (1rem 2rem), rounded corners (8px)
- **Hover**: Smooth transition 300ms ease-out, subtle scale(1.02)

### Cards

- Minimal border (1px `--border`)
- Subtle shadow on hover: `0 4px 24px oklch(0.13 0.02 260 / 0.08)`
- No nested cards
- Transition: transform 300ms, shadow 300ms

### Navigation

- Fixed top, backdrop-blur on scroll
- Logo left, nav links center, CTA right
- Transparent on hero, solid on scroll

## Motion

### Timing

- Default: `300ms ease-out`
- Entrance: `600ms cubic-bezier(0.16, 1, 0.3, 1)`
- Stagger: `100ms` between sibling elements

### Animations

- Scroll-triggered fade-up for sections (opacity + translateY 20px)
- Counter animation for metrics
- Smooth scroll for anchor links
- Parallax on select background elements (subtle, ≤10% movement)

### Reduced Motion

All animations respect `prefers-reduced-motion: reduce` — instant transitions, no transforms.

## Icons

- Style: Outline/stroke, 1.5px stroke weight
- Size: 24px default, 32px for feature icons
- Color: inherit from text, gold for highlights
- Source: Lucide Icons (SVG)

## Z-Index Scale

| Level | Value | Usage |
|-------|-------|-------|
| Base | 0 | Default |
| Dropdown | 100 | Menus, tooltips |
| Sticky | 200 | Fixed nav |
| Modal-backdrop | 300 | Overlay |
| Modal | 400 | Dialogs |
| Toast | 500 | Notifications |
| Floating | 600 | WhatsApp button, back-to-top |
