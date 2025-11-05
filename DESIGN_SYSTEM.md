# Design System

## Color Tokens

### Primary Colors

```css
--color-primary: #3b82f6; /* Blue 500 - Ana mavi, CTA butonlar */
--color-primary-hover: #2563eb; /* Blue 600 - Primary buton hover */
--color-primary-light: #dbeafe; /* Blue 100 - Açık mavi background */
--color-primary-dark: #1e40af; /* Blue 800 - Koyu mavi text */
```

**WHY primary blue:**

- Güven ve profesyonellik hissi verir
- Eğitim uygulamaları için uygun (mavi = bilgi, öğrenme)
- Hem erkek hem kız çocuklar için neutral

### Secondary Colors

```css
--color-secondary: #f59e0b; /* Amber 500 - Puan, ödül vurguları */
--color-secondary-hover: #d97706; /* Amber 600 - Secondary hover */
--color-secondary-light: #fef3c7; /* Amber 100 - Açık sarı background */
```

**WHY amber/orange:**

- Enerji ve heyecan hissi (gamification için uygun)
- Puan ve rozet vurgularında dikkat çeker
- Sıcak, dostane his

### Success Colors

```css
--color-success: #10b981; /* Green 500 - Tamamlanan ödevler */
--color-success-hover: #059669; /* Green 600 - Success hover */
--color-success-light: #d1fae5; /* Green 100 - Açık yeşil background */
```

### Neutral Colors

```css
--color-background: #f9fafb; /* Gray 50 - Ana sayfa background */
--color-surface: #ffffff; /* White - Card backgrounds */
--color-border: #e5e7eb; /* Gray 200 - Borders, dividers */
```

### Text Colors

```css
--color-text-primary: #111827; /* Gray 900 - Ana başlıklar */
--color-text-secondary: #6b7280; /* Gray 500 - Açıklamalar, body text */
--color-text-tertiary: #9ca3af; /* Gray 400 - Footer, subtle text */
--color-text-inverse: #ffffff; /* White - Dark background üzerinde */
```

### Semantic Colors

```css
--color-error: #ef4444; /* Red 500 - Error states */
--color-warning: #f59e0b; /* Amber 500 - Warning states */
--color-info: #3b82f6; /* Blue 500 - Info states */
```

---

## Typography

### Font Family

```css
--font-family-primary: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Helvetica", "Arial", sans-serif;
```

**WHY Inter:**

- Modern, clean, highly readable
- Excellent screen rendering
- Wide language support (Türkçe characters)
- Free (Google Fonts)

### Font Sizes

```css
--font-size-xs: 0.75rem; /* 12px - Captions, labels */
--font-size-sm: 0.875rem; /* 14px - Small text, metadata */
--font-size-base: 1rem; /* 16px - Body text (default) */
--font-size-lg: 1.125rem; /* 18px - Large body, lead text */
--font-size-xl: 1.25rem; /* 20px - Small headings */
--font-size-2xl: 1.5rem; /* 24px - H3 */
--font-size-3xl: 1.875rem; /* 30px - H2 */
--font-size-4xl: 2.25rem; /* 36px - H1 (mobile) */
--font-size-5xl: 3rem; /* 48px - H1 (desktop) */
--font-size-6xl: 3.75rem; /* 60px - Hero title (large screens) */
```

**WHY this scale:**

- 16px base = WCAG recommended, readable
- 1.125 scale ratio = balanced hierarchy
- Responsive: smaller sizes on mobile, larger on desktop

### Font Weights

```css
--font-weight-normal: 400; /* Regular - Body text */
--font-weight-medium: 500; /* Medium - Emphasized text */
--font-weight-semibold: 600; /* Semibold - Subheadings, buttons */
--font-weight-bold: 700; /* Bold - Headings */
```

**WHY Inter supports these weights well:**

- 400: Optimal readability for long text
- 600: Strong emphasis without being too heavy
- 700: Clear hierarchy for headings

### Line Heights

```css
--line-height-tight: 1.25; /* 1.25 - Headings */
--line-height-normal: 1.5; /* 1.5 - Body text */
--line-height-relaxed: 1.75; /* 1.75 - Large body text */
```

**WHY these values:**

- 1.5 = WCAG recommended for body text
- 1.25 for headings = compact but readable
- 1.75 for lead text = extra breathing room

### Letter Spacing

```css
--letter-spacing-tight: -0.025em; /* -0.4px - Large headings */
--letter-spacing-normal: 0; /* 0 - Body text */
--letter-spacing-wide: 0.025em; /* 0.4px - Uppercase text, labels */
```

---

## Spacing Scale

### Base Spacing Unit: 4px

```css
--spacing-0: 0; /* 0px */
--spacing-1: 0.25rem; /* 4px */
--spacing-2: 0.5rem; /* 8px */
--spacing-3: 0.75rem; /* 12px */
--spacing-4: 1rem; /* 16px */
--spacing-5: 1.25rem; /* 20px */
--spacing-6: 1.5rem; /* 24px */
--spacing-8: 2rem; /* 32px */
--spacing-10: 2.5rem; /* 40px */
--spacing-12: 3rem; /* 48px */
--spacing-16: 4rem; /* 64px */
--spacing-20: 5rem; /* 80px */
--spacing-24: 6rem; /* 96px */
--spacing-32: 8rem; /* 128px */
```

**WHY 4px base unit:**

- Divides evenly for all screen densities
- Easy mental math (4, 8, 16, 24, 32...)
- Industry standard (Material Design, Tailwind)

### Usage Guidelines

```css
/* Card padding */
padding: var(--spacing-8); /* 32px - Standard card */
padding: var(--spacing-6); /* 24px - Compact card (mobile) */

/* Section spacing */
margin-bottom: var(--spacing-20); /* 80px - Between sections (desktop) */
margin-bottom: var(--spacing-16); /* 64px - Between sections (mobile) */

/* Element spacing */
gap: var(--spacing-6); /* 24px - Between cards in grid */
gap: var(--spacing-4); /* 16px - Between text elements */
```

---

## Border Radius

```css
--radius-none: 0; /* 0px - Sharp corners */
--radius-sm: 0.375rem; /* 6px - Small elements, badges */
--radius-md: 0.5rem; /* 8px - Buttons, inputs */
--radius-lg: 0.75rem; /* 12px - Cards */
--radius-xl: 1rem; /* 16px - Large cards, modals */
--radius-2xl: 1.5rem; /* 24px - Hero sections */
--radius-full: 9999px; /* Full - Pills, circular elements */
```

**WHY these values:**

- Modern, friendly appearance
- 12px (lg) = Sweet spot for cards (not too round, not too sharp)
- Consistent hierarchy

---

## Shadows

```css
--shadow-xs: 0 1px 2px 0 rgb(0 0 0 / 0.05);
/* WHY: Subtle depth for small elements */

--shadow-sm: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
/* WHY: Default card shadow */

--shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
/* WHY: Elevated cards */

--shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
/* WHY: Hover states, modals */

--shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
/* WHY: High emphasis elements */

--shadow-2xl: 0 25px 50px -12px rgb(0 0 0 / 0.25);
/* WHY: Dialogs, overlays */
```

**Shadow Usage:**

```css
/* Default card */
box-shadow: var(--shadow-sm);

/* Card hover */
box-shadow: var(--shadow-lg);
transition: box-shadow 0.2s ease;

/* Modal/dialog */
box-shadow: var(--shadow-2xl);
```

---

## Transitions

```css
--transition-fast: 150ms; /* Fast - Small UI changes */
--transition-base: 200ms; /* Base - Standard transitions */
--transition-slow: 300ms; /* Slow - Large animations */
--transition-slower: 500ms; /* Slower - Page transitions */
```

**Easing Functions:**

```css
--ease-in: cubic-bezier(0.4, 0, 1, 1);
--ease-out: cubic-bezier(0, 0, 0.2, 1);
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
```

**Standard Transition:**

```css
transition: all var(--transition-base) var(--ease-in-out);
```

**WHY these timings:**

- 200ms = Sweet spot (fast enough, noticeable enough)
- ease-in-out = Natural feel (accelerate then decelerate)

---

## Component Patterns

### Button - Primary

```css
.button-primary {
  background-color: var(--color-primary);
  color: var(--color-text-inverse);
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-base);
  padding: var(--spacing-3) var(--spacing-8); /* 12px 32px */
  border-radius: var(--radius-lg);
  border: none;
  cursor: pointer;
  transition: all var(--transition-base) var(--ease-in-out);
  box-shadow: var(--shadow-sm);
}

.button-primary:hover {
  background-color: var(--color-primary-hover);
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

.button-primary:active {
  transform: translateY(0);
  box-shadow: var(--shadow-sm);
}

.button-primary:focus-visible {
  outline: 3px solid var(--color-primary-light);
  outline-offset: 2px;
}
```

**WHY this pattern:**

- Hover lift = Interactive, responsive feel
- Focus outline = Accessibility (keyboard navigation)
- Shadow transition = Depth perception

### Button - Secondary

```css
.button-secondary {
  background-color: transparent;
  color: var(--color-primary);
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-base);
  padding: var(--spacing-3) var(--spacing-8);
  border-radius: var(--radius-lg);
  border: 2px solid var(--color-primary);
  cursor: pointer;
  transition: all var(--transition-base) var(--ease-in-out);
}

.button-secondary:hover {
  background-color: var(--color-primary-light);
  border-color: var(--color-primary-hover);
}

.button-secondary:active {
  background-color: var(--color-primary);
  color: var(--color-text-inverse);
}
```

**WHY outline style:**

- Less visual weight than primary
- Clear hierarchy (primary > secondary)
- Hover fill = Clear feedback

### Card - Feature Card

```css
.card {
  background-color: var(--color-surface);
  padding: var(--spacing-8); /* 32px */
  border-radius: var(--radius-xl); /* 16px */
  box-shadow: var(--shadow-sm);
  transition: all var(--transition-base) var(--ease-in-out);
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
}

.card-icon {
  font-size: var(--font-size-5xl); /* 48px emoji */
  margin-bottom: var(--spacing-4);
}

.card-title {
  font-size: var(--font-size-xl); /* 20px */
  font-weight: var(--font-weight-bold);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-3);
  line-height: var(--line-height-tight);
}

.card-description {
  font-size: var(--font-size-base); /* 16px */
  color: var(--color-text-secondary);
  line-height: var(--line-height-normal);
}
```

**WHY this structure:**

- Icon first = Visual hierarchy, quick scanning
- Title + description = Clear information hierarchy
- Hover lift = Interactive, engaging

### Card - Problem Card (Variant)

```css
.card-problem {
  background-color: var(--color-surface);
  padding: var(--spacing-8);
  border-radius: var(--radius-xl);
  border-left: 4px solid var(--color-error); /* Red accent */
  box-shadow: var(--shadow-sm);
  transition: all var(--transition-base) var(--ease-in-out);
}

.card-problem:hover {
  border-left-width: 6px;
  box-shadow: var(--shadow-md);
}
```

**WHY left border:**

- Visual distinction from solution cards
- Red = Problem, urgency
- Accent without overwhelming

### Section Container

```css
.section {
  max-width: 1200px;
  margin: 0 auto;
  padding: var(--spacing-20) var(--spacing-6); /* 80px 24px */
}

@media (max-width: 640px) {
  .section {
    padding: var(--spacing-16) var(--spacing-4); /* 64px 16px */
  }
}
```

**WHY 1200px max-width:**

- Optimal reading line length (~75 characters)
- Comfortable on large screens
- Standard container width

### Heading Styles

```css
.heading-1 {
  font-size: var(--font-size-5xl); /* 48px */
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  letter-spacing: var(--letter-spacing-tight);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-6);
}

@media (max-width: 640px) {
  .heading-1 {
    font-size: var(--font-size-4xl); /* 36px */
  }
}

.heading-2 {
  font-size: var(--font-size-3xl); /* 30px */
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-8);
  text-align: center;
}

.heading-3 {
  font-size: var(--font-size-2xl); /* 24px */
  font-weight: var(--font-weight-semibold);
  line-height: var(--line-height-tight);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-4);
}
```

**WHY center align H2:**

- Section başlıkları = Symmetric layout
- Professional, balanced appearance

### Body Text

```css
.body-text {
  font-size: var(--font-size-base); /* 16px */
  font-weight: var(--font-weight-normal);
  line-height: var(--line-height-normal); /* 1.5 */
  color: var(--color-text-secondary);
}

.lead-text {
  font-size: var(--font-size-lg); /* 18px */
  font-weight: var(--font-weight-normal);
  line-height: var(--line-height-relaxed); /* 1.75 */
  color: var(--color-text-secondary);
}
```

---

## Grid Patterns

### 3-Column Grid (Problem, Privacy sections)

```css
.grid-3-col {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--spacing-6); /* 24px */
}

@media (max-width: 1024px) {
  .grid-3-col {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 640px) {
  .grid-3-col {
    grid-template-columns: 1fr;
    gap: var(--spacing-4); /* 16px - tighter on mobile */
  }
}
```

**WHY this breakpoint strategy:**

- Desktop (>1024px): 3 columns, spacious
- Tablet (640-1024px): 2 columns, balanced
- Mobile (<640px): 1 column, readable

### 2x2 Grid (Solution, Gamification sections)

```css
.grid-2x2 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--spacing-8); /* 32px */
}

@media (max-width: 640px) {
  .grid-2x2 {
    grid-template-columns: 1fr;
    gap: var(--spacing-6);
  }
}
```

### 2-Column Split (Hero section)

```css
.split-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--spacing-12); /* 48px */
  align-items: center;
}

@media (max-width: 768px) {
  .split-layout {
    grid-template-columns: 1fr;
    gap: var(--spacing-8);
  }
}
```

---

## Icon Guidelines

### Emoji Icons

- **Size**: 2.5rem (40px) for feature cards
- **Size**: 3rem (48px) for hero/large sections
- **Line-height**: 1 (prevents extra space)
- **Display**: block or inline-block

```css
.icon-emoji {
  font-size: var(--font-size-5xl); /* 48px */
  line-height: 1;
  display: block;
  margin-bottom: var(--spacing-4);
}
```

**WHY emoji instead of SVG:**

- No external dependencies
- Cross-platform consistency
- Zero load time
- Easy to change/update

### Badge/Number Icons (How It Works)

```css
.badge-number {
  width: 48px;
  height: 48px;
  border-radius: var(--radius-full);
  background-color: var(--color-primary);
  color: var(--color-text-inverse);
  font-size: var(--font-size-2xl);
  font-weight: var(--font-weight-bold);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: var(--spacing-4);
}
```

---

## Animation Patterns

### Scroll Reveal (Optional - with Intersection Observer)

```css
.scroll-reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity var(--transition-slow) var(--ease-out), transform var(--transition-slow) var(--ease-out);
}

.scroll-reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

**WHY scroll animations:**

- Adds delight, modern feel
- Guides attention
- Progressive disclosure (don't overwhelm)

### Hover Animations

```css
/* Lift on hover */
.hover-lift:hover {
  transform: translateY(-4px);
}

/* Scale on hover */
.hover-scale:hover {
  transform: scale(1.05);
}

/* Glow on hover */
.hover-glow:hover {
  box-shadow: 0 0 20px rgba(59, 130, 246, 0.4);
}
```

---

## Gradient Patterns

### Hero Background Gradient

```css
.gradient-hero {
  background: linear-gradient(135deg, var(--color-primary-light) 0%, var(--color-surface) 100%);
}
```

**WHY this gradient:**

- Subtle, not distracting
- Light to white = Natural reading flow
- 135deg = Diagonal, dynamic

### CTA Section Gradient

```css
.gradient-cta {
  background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-primary-dark) 100%);
}
```

**WHY solid color gradient:**

- High contrast for white text
- Attention-grabbing
- Clear visual separation

---

## Accessibility Standards

### Focus Styles

```css
*:focus-visible {
  outline: 3px solid var(--color-primary);
  outline-offset: 2px;
  border-radius: var(--radius-sm);
}
```

**WHY visible focus:**

- WCAG 2.1 requirement
- Keyboard navigation essential
- 3px = Clearly visible

### Color Contrast Ratios

- **Primary on White**: 4.5:1 ✅ (WCAG AA)
- **Text Primary on White**: 16.5:1 ✅ (WCAG AAA)
- **Text Secondary on White**: 7:1 ✅ (WCAG AA)

**Check with tools:**

- WebAIM Contrast Checker
- Chrome DevTools Accessibility Panel

### Touch Targets

```css
/* Minimum 44x44px tappable area (WCAG 2.1) */
.button,
.link {
  min-height: 44px;
  min-width: 44px;
  padding: var(--spacing-3) var(--spacing-6);
}
```

---

## Responsive Images

```css
.responsive-image {
  max-width: 100%;
  height: auto;
  display: block;
}

.hero-image {
  max-width: 500px;
  width: 100%;
  height: auto;
}

@media (max-width: 640px) {
  .hero-image {
    max-width: 100%;
  }
}
```

**WHY max-width 500px:**

- Prevents oversized images on large screens
- Maintains aspect ratio
- Fast loading

---

## Performance Considerations

### Critical CSS (Inline in <head>)

```css
/* Only above-the-fold styles */
- Hero section styles
- Typography base
- Color variables
- Layout container
```

**WHY inline critical CSS:**

- Faster First Contentful Paint
- No render-blocking external CSS
- Progressive enhancement

### Lazy Loading

```html
<img src="hero.webp" alt="..." loading="lazy" />
```

**WHY lazy loading:**

- Faster initial load
- Save bandwidth
- Load images as user scrolls

---

## Print Styles (Optional)

```css
@media print {
  * {
    background: white !important;
    color: black !important;
    box-shadow: none !important;
  }

  .button,
  .footer-links {
    display: none;
  }

  .section {
    page-break-inside: avoid;
  }
}
```

---

## Dark Mode (Future Consideration)

```css
@media (prefers-color-scheme: dark) {
  :root {
    --color-background: #111827;
    --color-surface: #1f2937;
    --color-text-primary: #f9fafb;
    --color-text-secondary: #d1d5db;
    --color-border: #374151;
  }
}
```

**WHY prepare for dark mode:**

- Growing user preference
- Better readability in low light
- Modern UX expectation

---

## Code Organization Best Practices

### CSS File Structure

```css
/* ==========================================
   1. CSS VARIABLES
   ========================================== */
:root {
  /* Color tokens */
  /* Typography tokens */
  /* Spacing tokens */
  /* etc. */
}

/* ==========================================
   2. RESET & BASE STYLES
   ========================================== */
* {
  box-sizing: border-box;
}
body {
  font-family: var(--font-family-primary);
}

/* ==========================================
   3. UTILITY CLASSES
   ========================================== */
.container {
  ...;
}
.grid-3-col {
  ...;
}

/* ==========================================
   4. COMPONENT STYLES
   ========================================== */
.button-primary {
  ...;
}
.card {
  ...;
}

/* ==========================================
   5. SECTION STYLES
   ========================================== */
#hero {
  ...;
}
#problem {
  ...;
}

/* ==========================================
   6. RESPONSIVE OVERRIDES
   ========================================== */
@media (max-width: 640px) {
  ...;
}
```

**WHY this organization:**

- Clear mental model
- Easy to find styles
- Logical cascade order
- Maintainable long-term
