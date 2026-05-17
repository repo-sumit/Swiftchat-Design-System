# Dark Portal Blog Design System

## Overview

A retro-futuristic editorial UI system inspired by The Nifty Portal, redesigned into a dark-theme blog experience with stronger spacing tokens, clearer layout rhythm, and more production-ready CSS variables.

Core identity:

- Retro portal interface
- Editorial grid system
- Technical UI styling
- Pixel-inspired decorative patterns
- Monospace typography
- Bold outlined panels
- Futuristic but minimal
- Dark operating-system surface language

---

# 1. Design Philosophy

## Experience Goals

The interface should feel like:

```text
A futuristic editorial operating system running in dark mode.
```

Not a typical SaaS blog.

The UI should communicate:

- structure
- signal
- transmission
- system states
- editorial curation
- digital archive aesthetics
- terminal-grade clarity
- high-contrast modularity

---

# 2. Brand Keywords

```text
retro-futuristic
technical
editorial
pixel-grid
mono-ui
interface-first
portal-system
mechanical
structured
minimal
dark-console
signal-led
archive-terminal
```

---

# 3. Visual Language

## Key Characteristics

### Borders Everywhere

Use strong outlined structures. In dark mode, borders should feel luminous but not neon by default.

```css
border: 2px solid var(--border-main);
```

### Rounded Technical Panels

```css
border-radius: var(--radius-panel);
```

### Grid-Based Layout

Every section should feel modular and intentionally aligned.

### Monospace Labels

Use uppercase UI metadata:

```text
SYSTEM ONLINE
PORTAL ACTIVE
001 // FEATURED
BOOT SEQUENCE INITIATED
DARK SIGNAL LOCKED
```

### Japanese Micro Text

Use small accents:

```text
ポータル
記事
システム
通信
```

### Decorative Technical Shapes

Use:

- checkerboards
- wireframe triangles
- concentric circles
- pixel hearts
- dotted lines
- ASCII arrows
- terminal scanlines
- low-opacity grid overlays

---

# 4. Design Tokens

## 4.1 Color Tokens

```css
:root {
  /* Surfaces */
  --bg-main: #08090d;
  --bg-page: #0b0d12;
  --bg-panel: #11141b;
  --bg-panel-raised: #171b24;
  --bg-panel-soft: #0f1218;
  --bg-inverse: #f4f0df;

  /* Text */
  --text-main: #f5f1e8;
  --text-muted: #a8a294;
  --text-soft: #6f6a5f;
  --text-inverse: #111111;

  /* Borders */
  --border-main: #f5f1e8;
  --border-muted: #373c49;
  --border-soft: #252a35;
  --border-glow: rgba(245, 241, 232, 0.28);

  /* Accents */
  --accent-orange: #ff5a1f;
  --accent-blue: #4f8cff;
  --accent-green: #35d07f;
  --accent-yellow: #ffd166;
  --accent-red: #ff4d5e;

  /* Pixel + Pattern */
  --pixel-dark: #08090d;
  --pixel-light: #f5f1e8;
  --grid-line: rgba(245, 241, 232, 0.08);
  --noise-opacity: 0.055;

  /* Shadows */
  --shadow-soft: 0 18px 50px rgba(0, 0, 0, 0.42);
  --shadow-panel: 0 12px 32px rgba(0, 0, 0, 0.32);
  --shadow-glow: 0 0 0 1px rgba(245, 241, 232, 0.08),
                 0 18px 60px rgba(79, 140, 255, 0.12);
}
```

## 4.2 Spacing Tokens

Use an 8px-based spacing scale with larger editorial steps for sections.

```css
:root {
  --space-0: 0;
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-7: 28px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-14: 56px;
  --space-16: 64px;
  --space-20: 80px;
  --space-24: 96px;
  --space-28: 112px;
  --space-32: 128px;
}
```

## 4.3 Layout Tokens

```css
:root {
  --container-sm: 760px;
  --container-md: 960px;
  --container-lg: 1180px;
  --container-xl: 1360px;

  --shell-padding-desktop: var(--space-8);
  --shell-padding-tablet: var(--space-6);
  --shell-padding-mobile: var(--space-4);

  --section-gap-desktop: var(--space-24);
  --section-gap-tablet: var(--space-16);
  --section-gap-mobile: var(--space-12);

  --grid-gap-sm: var(--space-4);
  --grid-gap-md: var(--space-6);
  --grid-gap-lg: var(--space-8);
}
```

## 4.4 Radius Tokens

```css
:root {
  --radius-xs: 8px;
  --radius-sm: 12px;
  --radius-md: 16px;
  --radius-lg: 20px;
  --radius-panel: 24px;
  --radius-xl: 32px;
  --radius-pill: 999px;
}
```

## 4.5 Typography Tokens

```css
:root {
  --font-ui: "Space Mono", monospace;
  --font-hero: "Orbitron", sans-serif;

  --tracking-tight: -0.06em;
  --tracking-label: 0.18em;
  --tracking-wide: 0.12em;

  --leading-hero: 0.85;
  --leading-title: 0.95;
  --leading-body: 1.65;
}
```

---

# 5. Color Usage Rules

## Backgrounds

- Use near-black surfaces instead of pure black.
- Layer panels with subtle surface elevation.
- Avoid flat black-on-white inversion.
- Use grid and noise overlays to avoid empty dark surfaces.

## Borders

- Primary structural element.
- Use warm off-white for important borders.
- Use muted gray-blue borders for internal dividers.

## Accent Colors

Use sparingly:

- orange for active states
- blue for links/system actions
- green for online/success states
- yellow for warning/attention states
- red only for destructive/error states

---

# 6. Typography System

## Primary Fonts

### UI Font

```css
font-family: var(--font-ui);
```

### Hero Font

```css
font-family: var(--font-hero);
```

## Typography Scale

### Hero Title

```css
font-size: clamp(56px, 13vw, 176px);
line-height: var(--leading-hero);
letter-spacing: var(--tracking-tight);
font-weight: 800;
```

### Section Titles

```css
font-size: clamp(28px, 5vw, 64px);
line-height: var(--leading-title);
```

### Technical Labels

```css
font-size: 11px;
text-transform: uppercase;
letter-spacing: var(--tracking-label);
```

### Metadata

```css
font-size: 12px;
font-family: var(--font-ui);
color: var(--text-muted);
```

### Body Copy

```css
font-size: 15px;
line-height: var(--leading-body);
color: var(--text-muted);
```

---

# 7. Layout System

## Main Container

```css
.portal-shell {
  max-width: var(--container-lg);
  margin: 0 auto;
  padding: var(--shell-padding-desktop);
}

@media (max-width: 900px) {
  .portal-shell {
    padding: var(--shell-padding-tablet);
  }
}

@media (max-width: 560px) {
  .portal-shell {
    padding: var(--shell-padding-mobile);
  }
}
```

## Section Rhythm

```css
.portal-section {
  margin-block: var(--section-gap-desktop);
}

@media (max-width: 900px) {
  .portal-section {
    margin-block: var(--section-gap-tablet);
  }
}

@media (max-width: 560px) {
  .portal-section {
    margin-block: var(--section-gap-mobile);
  }
}
```

## Grid System

```css
.portal-grid {
  display: grid;
  gap: var(--grid-gap-md);
}

.portal-grid--articles {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

@media (max-width: 900px) {
  .portal-grid--articles {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 640px) {
  .portal-grid--articles {
    grid-template-columns: 1fr;
  }
}
```

## Panel Style

```css
.portal-panel {
  background: var(--bg-panel);
  border: 2px solid var(--border-main);
  border-radius: var(--radius-panel);
  box-shadow: var(--shadow-panel);
  overflow: hidden;
}
```

---

# 8. Signature Components

# A. Portal Ticker

Inspired by a scrolling header bar.

## Structure

```text
PORTAL 1 OF ?
BOOT SEQUENCE INITIATED
THE BLOG PORTAL
システム ONLINE
DARK SIGNAL ACTIVE
```

## CSS

```css
.portal-ticker {
  border: 2px solid var(--border-main);
  border-radius: var(--radius-pill);
  padding: var(--space-3) var(--space-5);
  white-space: nowrap;
  overflow: hidden;
  font-family: var(--font-ui);
  text-transform: uppercase;
  background: var(--bg-panel-soft);
  color: var(--text-main);
}
```

---

# B. Hero Section

## Structure

```text
------------------------------------------------
| PORTAL 1 OF ?                                |
------------------------------------------------
|                                               |
| THE BLOG                                     |
| PORTAL                                       |
|                                               |
| [ENTER BLOG] [LATEST ARTICLE]                |
|                                               |
------------------------------------------------
```

## Content Style

### Headline

```text
THE BLOG PORTAL
```

### Subheadline

```text
Ideas, stories, and signals from culture,
design, technology, and modern creativity.
```

### CTA Labels

```text
ENTER BLOG
READ SIGNAL
OPEN ARTICLE
```

## CSS

```css
.hero-panel {
  padding: clamp(var(--space-8), 7vw, var(--space-20));
  background:
    linear-gradient(var(--grid-line) 1px, transparent 1px),
    linear-gradient(90deg, var(--grid-line) 1px, transparent 1px),
    var(--bg-panel);
  background-size: 32px 32px;
}

.hero-title {
  margin: var(--space-10) 0 var(--space-6);
  font-family: var(--font-hero);
  font-size: clamp(56px, 13vw, 176px);
  line-height: var(--leading-hero);
  letter-spacing: var(--tracking-tight);
  color: var(--text-main);
}

.hero-copy {
  max-width: 680px;
  color: var(--text-muted);
  font-size: clamp(15px, 2vw, 20px);
  line-height: 1.6;
}
```

---

# C. Category Strip

## Categories

```text
CULTURE
DESIGN
PRODUCT
TECH
STARTUPS
IDEAS
```

Each category should contain:

- icon
- title
- subtitle
- outlined block
- active signal indicator

## CSS

```css
.category-card {
  padding: var(--space-5);
  background: var(--bg-panel-soft);
  border: 2px solid var(--border-muted);
  border-radius: var(--radius-lg);
}

.category-card:hover {
  border-color: var(--border-main);
  box-shadow: var(--shadow-glow);
}
```

---

# D. Article Cards

## Structure

```text
--------------------------------
| abstract image/pattern        |
--------------------------------
| 001 // DESIGN                 |
| Building Better Interfaces    |
| Short excerpt text...         |
| AUTHOR · DATE · 6 MIN READ    |
--------------------------------
```

## CSS

```css
.article-card {
  background: var(--bg-panel-raised);
  border: 2px solid var(--border-muted);
  border-radius: var(--radius-lg);
  overflow: hidden;
  transition:
    transform 0.2s ease,
    border-color 0.2s ease,
    box-shadow 0.2s ease;
}

.article-card:hover {
  transform: translateY(-6px);
  border-color: var(--border-main);
  box-shadow: var(--shadow-glow);
}

.article-card__media {
  min-height: 220px;
  background:
    radial-gradient(circle at 20% 20%, rgba(255, 90, 31, 0.22), transparent 28%),
    radial-gradient(circle at 80% 30%, rgba(79, 140, 255, 0.18), transparent 32%),
    var(--bg-panel-soft);
  border-bottom: 2px solid var(--border-muted);
}

.article-card__body {
  padding: var(--space-6);
}

.article-card__meta {
  margin-bottom: var(--space-3);
  font-family: var(--font-ui);
  font-size: 12px;
  letter-spacing: var(--tracking-wide);
  color: var(--accent-orange);
  text-transform: uppercase;
}
```

---

# E. Newsletter Section

## Headline

```text
RECEIVE THE NEXT SIGNAL
```

## Supporting Copy

```text
No spam. Only useful dispatches.
```

## Style

- centered card
- bordered input
- mono labels
- subtle technical graphics
- strong dark panel contrast

## CSS

```css
.newsletter-panel {
  padding: clamp(var(--space-8), 6vw, var(--space-16));
  text-align: center;
  background:
    radial-gradient(circle at 50% 0%, rgba(79, 140, 255, 0.16), transparent 42%),
    var(--bg-panel);
}

.newsletter-form {
  display: flex;
  gap: var(--space-3);
  max-width: 560px;
  margin: var(--space-8) auto 0;
}

.newsletter-input {
  flex: 1;
  min-height: 52px;
  padding: 0 var(--space-4);
  background: var(--bg-main);
  border: 2px solid var(--border-muted);
  border-radius: var(--radius-pill);
  color: var(--text-main);
  font-family: var(--font-ui);
}

.newsletter-input:focus {
  outline: none;
  border-color: var(--accent-blue);
  box-shadow: 0 0 0 4px rgba(79, 140, 255, 0.18);
}
```

---

# F. Footer

## Include

- brand
- navigation
- social links
- copyright
- system labels

Example:

```text
SYSTEM STATUS: ONLINE
PORTAL VERSION 1.0
DARK MODE ACTIVE
```

## CSS

```css
.portal-footer {
  padding-block: var(--space-12);
  color: var(--text-muted);
  border-top: 2px solid var(--border-muted);
}
```

---

# 9. Pattern Library

## Checkerboard Pattern

```css
.checker {
  background-image:
    linear-gradient(45deg, var(--pixel-light) 25%, transparent 25%),
    linear-gradient(-45deg, var(--pixel-light) 25%, transparent 25%),
    linear-gradient(45deg, transparent 75%, var(--pixel-light) 75%),
    linear-gradient(-45deg, transparent 75%, var(--pixel-light) 75%);
  background-position:
    0 0,
    0 6px,
    6px -6px,
    -6px 0;
  background-size: 12px 12px;
  opacity: 0.12;
}
```

## Grid Overlay

```css
.grid-overlay {
  background-image:
    linear-gradient(var(--grid-line) 1px, transparent 1px),
    linear-gradient(90deg, var(--grid-line) 1px, transparent 1px);
  background-size: 32px 32px;
}
```

## Concentric Circle Pattern

Use SVG or CSS radial gradients.

```css
.concentric {
  background:
    repeating-radial-gradient(
      circle,
      rgba(245, 241, 232, 0.16) 0 1px,
      transparent 1px 18px
    );
}
```

## Wireframe Triangle

Use thin outlined SVG triangles with `stroke: var(--border-main)` and opacity between `0.16` and `0.32`.

## Noise Texture

Apply subtle grain overlay.

```css
.noise {
  mix-blend-mode: screen;
  opacity: var(--noise-opacity);
  pointer-events: none;
}
```

---

# 10. Motion System

## Motion Philosophy

Animations should feel:

- technical
- mechanical
- interface-driven
- lightweight
- precise

Avoid luxury-style animations.

## Allowed Animations

### Hover Lift

```css
transform: translateY(-4px);
```

### Ticker Scroll

Horizontal continuous movement.

### Fade-Up

Used for section reveals.

### Cursor Blink

Tiny blinking UI cursor.

### SVG Rotation

Slow rotating wireframe elements.

### Signal Pulse

Use only for online indicators.

```css
.signal-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--accent-green);
  box-shadow: 0 0 16px rgba(53, 208, 127, 0.55);
  animation: signalPulse 1.6s ease-in-out infinite;
}

@keyframes signalPulse {
  0%, 100% {
    opacity: 0.65;
    transform: scale(1);
  }
  50% {
    opacity: 1;
    transform: scale(1.28);
  }
}
```

---

# 11. Responsive System

## Desktop

- large portal hero
- multi-column layout
- ticker fully visible
- 3-column article grid
- generous section rhythm
- visible technical decorations

## Tablet

- simplified hero
- 2-column article grid
- reduced spacing
- fewer decorative elements

## Mobile

- single-column stack
- horizontal ticker scroll
- hamburger menu
- oversized wrapped hero title
- touch-friendly buttons
- minimum 44px interactive targets

## Responsive Spacing Rules

```css
@media (max-width: 900px) {
  :root {
    --section-gap-desktop: var(--section-gap-tablet);
  }
}

@media (max-width: 560px) {
  :root {
    --section-gap-desktop: var(--section-gap-mobile);
  }

  .newsletter-form {
    flex-direction: column;
  }
}
```

---

# 12. UI Labels Library

## System Labels

```text
SYSTEM ONLINE
PORTAL ACTIVE
SIGNAL RECEIVED
BOOT SEQUENCE INITIATED
ARCHIVE OPEN
TRANSMISSION ACTIVE
DARK SIGNAL ACTIVE
NIGHT INDEX ONLINE
```

## Section Labels

```text
001 // FEATURED
002 // ARTICLES
003 // TRANSMISSION
004 // ARCHIVE
005 // SIGNAL FEED
```

## Japanese Labels

```text
ポータル
記事
システム
通信
暗号
信号
```

---

# 13. Suggested Page Structure

```text
1. Portal Ticker
2. Hero Section
3. Category Strip
4. Featured Article
5. Latest Articles Grid
6. Newsletter Block
7. Footer
```

---

# 14. Button System

## Primary Button

```css
.btn-primary {
  min-height: 48px;
  padding: 0 var(--space-5);
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);
  background: var(--text-main);
  color: var(--text-inverse);
  border: 2px solid var(--border-main);
  border-radius: var(--radius-pill);
  font-family: var(--font-ui);
  font-size: 12px;
  letter-spacing: var(--tracking-label);
  text-transform: uppercase;
}
```

## Secondary Button

```css
.btn-secondary {
  min-height: 48px;
  padding: 0 var(--space-5);
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);
  background: transparent;
  color: var(--text-main);
  border: 2px solid var(--border-muted);
  border-radius: var(--radius-pill);
  font-family: var(--font-ui);
  font-size: 12px;
  letter-spacing: var(--tracking-label);
  text-transform: uppercase;
}
```

## Button Hover

```css
.btn-primary:hover,
.btn-secondary:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-glow);
}
```

---

# 15. Accessibility Rules

- Maintain strong contrast between text and background.
- Do not rely on accent color alone for state.
- Use visible focus rings.
- Respect reduced-motion settings.

```css
:focus-visible {
  outline: 2px solid var(--accent-blue);
  outline-offset: 4px;
}

@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

# 16. Claude Prompt

```text
Create a complete responsive frontend and design system inspired by The Nifty Portal screenshots.

Translate the same visual language into a dark-theme editorial blog portal.

Use:
- retro portal UI
- thick outlined panels
- dark technical surfaces
- luminous but restrained borders
- pixel patterns
- Japanese micro text
- monospace typography
- large futuristic headings
- grid-based editorial layout
- ticker bars
- system labels
- spacing tokens based on an 8px scale
- responsive modular sections

Do not copy NFT content or branding.

Build:
1. Hero section
2. Portal ticker
3. Category strip
4. Featured article section
5. Blog article grid
6. Newsletter section
7. Footer
8. Full responsive system
9. Buttons and cards
10. Technical decorative graphics

Use near-black backgrounds, warm off-white text, layered dark panels, strong outlines, subtle grid/noise textures, and restrained orange/blue/green accents.

Output a complete single-file HTML page with embedded CSS and JavaScript.
```
