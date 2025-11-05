# ÖdevCim Landing Page - Style Guide

## Visual Design System

This document defines the complete visual design system for the ÖdevCim landing page. All design decisions should reference this guide to maintain consistency.

---

## Color System

### Primary Palette

**Primary Brand Color (Indigo)**

```css
--color-primary-50: #eef2ff;
--color-primary-100: #e0e7ff;
--color-primary-200: #c7d2fe;
--color-primary-300: #a5b4fc;
--color-primary-400: #818cf8;
--color-primary-500: #6366f1; /* Main brand color */
--color-primary-600: #4f46e5; /* Primary buttons, links */
--color-primary-700: #4338ca; /* Hover states */
--color-primary-800: #3730a3;
--color-primary-900: #312e81;
```

**WHY Indigo:**

- Conveys trust and professionalism
- Modern, tech-forward appearance
- High contrast with white backgrounds
- Not overused (differentiates from competitors)

---

**Secondary Accent Color (Amber)**

```css
--color-secondary-50: #fffbeb;
--color-secondary-100: #fef3c7;
--color-secondary-200: #fde68a;
--color-secondary-300: #fcd34d;
--color-secondary-400: #fbbf24;
--color-secondary-500: #f59e0b; /* Badges, rewards */
--color-secondary-600: #d97706; /* Hover states */
--color-secondary-700: #b45309;
--color-secondary-800: #92400e;
--color-secondary-900: #78350f;
```

**WHY Amber:**

- Represents achievement and rewards
- Creates warmth and energy
- High visibility for gamification elements
- Complements indigo without clashing

---

**Success Color (Emerald)**

```css
--color-success-50: #ecfdf5;
--color-success-100: #d1fae5;
--color-success-200: #a7f3d0;
--color-success-300: #6ee7b7;
--color-success-400: #34d399;
--color-success-500: #10b981; /* Completed tasks */
--color-success-600: #059669; /* Hover states */
--color-success-700: #047857;
--color-success-800: #065f46;
--color-success-900: #064e3b;
```

**Usage:**

- Completed task checkboxes
- Success messages
- Positive metrics and progress

---

### Neutral Palette

**Grays**

```css
--color-gray-50: #f9fafb; /* Alternate section backgrounds */
--color-gray-100: #f3f4f6; /* Card backgrounds (hover) */
--color-gray-200: #e5e7eb; /* Borders, dividers */
--color-gray-300: #d1d5db; /* Disabled states */
--color-gray-400: #9ca3af; /* Placeholder text */
--color-gray-500: #6b7280; /* Secondary text */
--color-gray-600: #4b5563; /* Body text (light backgrounds) */
--color-gray-700: #374151;
--color-gray-800: #1f2937;
--color-gray-900: #111827; /* Headings, primary text */
```

**WHY This Gray Scale:**

- Sufficient variety for all UI needs
- Maintains readability at all contrast levels
- Neutral enough to not compete with brand colors

---

### Semantic Colors

**Error/Warning/Info**

```css
--color-error: #ef4444; /* Red 500 - form errors */
--color-warning: #f59e0b; /* Amber 500 - warnings */
--color-info: #3b82f6; /* Blue 500 - informational messages */
```

**Background Colors**

```css
--color-background-primary: #ffffff; /* Main backgrounds */
--color-background-secondary: #f9fafb; /* Alternate sections */
--color-background-tertiary: #f3f4f6; /* Cards on gray backgrounds */
```

**Text Colors**

```css
--color-text-primary: #111827; /* Headings, body text */
--color-text-secondary: #6b7280; /* Captions, labels */
--color-text-tertiary: #9ca3af; /* Placeholders, disabled */
--color-text-inverse: #ffffff; /* Text on dark backgrounds */
```

**Border Colors**

```css
--color-border-primary: #e5e7eb; /* Default borders */
--color-border-secondary: #d1d5db; /* Emphasized borders */
--color-border-focus: #4f46e5; /* Focus rings on inputs */
```

---

### Color Usage Rules

**DO:**

- Use primary color for CTAs, links, and interactive elements
- Use secondary color sparingly for emphasis (badges, icons)
- Use success color only for positive feedback
- Maintain sufficient contrast (4.5:1 minimum for text)

**DON'T:**

- Mix too many colors in one section (max 2-3)
- Use color as the only indicator (accessibility)
- Use secondary color for large areas (overwhelming)
- Use pure black (#000000) for text

---

## Typography System

### Font Families

**Primary Font: Inter**

```css
--font-primary: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Helvetica Neue", Arial, sans-serif;
```

**WHY Inter:**

- Designed for screens (high legibility)
- Open source and free
- Excellent at all sizes
- Professional, modern aesthetic
- Wide character set (includes Turkish characters)

**Font Loading Strategy:**

- Use Google Fonts with `font-display: swap`
- Fallback to system fonts immediately
- Subset to Latin + Latin Extended (includes Turkish)

**Font Declaration:**

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
```

---

### Font Sizes

**Scale (using major third ratio: 1.250)**

```css
--font-size-xs: 0.75rem; /* 12px - small labels, captions */
--font-size-sm: 0.875rem; /* 14px - secondary text */
--font-size-base: 1rem; /* 16px - body text baseline */
--font-size-lg: 1.125rem; /* 18px - large body text */
--font-size-xl: 1.25rem; /* 20px - subheadings */
--font-size-2xl: 1.5rem; /* 24px - H3 */
--font-size-3xl: 1.875rem; /* 30px - H2 (mobile) */
--font-size-4xl: 2.25rem; /* 36px - H1 (mobile), H2 (desktop) */
--font-size-5xl: 3rem; /* 48px - H1 (desktop) */
--font-size-6xl: 3.75rem; /* 60px - Hero text (desktop only) */
```

**WHY This Scale:**

- Major third ratio creates harmonious sizing
- Large enough for mobile (16px base)
- Sufficient variety for hierarchy
- Easy to remember and apply

---

### Font Weights

```css
--font-weight-normal: 400; /* Body text */
--font-weight-medium: 500; /* Emphasis in body */
--font-weight-semibold: 600; /* Subheadings, buttons */
--font-weight-bold: 700; /* Headings */
```

**Usage:**

- 400: All body copy, captions
- 500: Emphasized text within paragraphs
- 600: Buttons, labels, H3, H4
- 700: H1, H2, strong emphasis

**DON'T:**

- Use 300 (too light, poor readability)
- Use 800-900 (too heavy, overwhelming)

---

### Line Heights

```css
--line-height-tight: 1.25; /* Headings */
--line-height-normal: 1.5; /* Body text */
--line-height-relaxed: 1.75; /* Long-form content */
```

**Usage:**

- Tight: All headings (H1-H6)
- Normal: Short paragraphs, UI text
- Relaxed: Long paragraphs (privacy policy, terms)

**WHY These Values:**

- Tight line-height for headings improves visual impact
- Normal (1.5) is WCAG recommended for body text
- Relaxed improves readability for long content

---

### Letter Spacing

```css
--letter-spacing-tight: -0.025em; /* Large headings */
--letter-spacing-normal: 0; /* Body text */
--letter-spacing-wide: 0.025em; /* Uppercase text, small text */
```

**Usage:**

- Tight: H1, H2 (improves visual balance at large sizes)
- Normal: H3-H6, body text
- Wide: Uppercase labels, small captions

---

### Text Styles (Presets)

**Heading Styles:**

```css
/* H1 - Hero Headline */
.heading-1 {
  font-size: var(--font-size-5xl); /* 48px */
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  letter-spacing: var(--letter-spacing-tight);
  color: var(--color-text-primary);
}

@media (max-width: 768px) {
  .heading-1 {
    font-size: var(--font-size-4xl); /* 36px on mobile */
  }
}

/* H2 - Section Headings */
.heading-2 {
  font-size: var(--font-size-4xl); /* 36px */
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  color: var(--color-text-primary);
}

@media (max-width: 768px) {
  .heading-2 {
    font-size: var(--font-size-3xl); /* 30px on mobile */
  }
}

/* H3 - Subsection Headings */
.heading-3 {
  font-size: var(--font-size-2xl); /* 24px */
  font-weight: var(--font-weight-semibold);
  line-height: var(--line-height-tight);
  color: var(--color-text-primary);
}

/* H4 - Card Titles */
.heading-4 {
  font-size: var(--font-size-xl); /* 20px */
  font-weight: var(--font-weight-semibold);
  line-height: var(--line-height-normal);
  color: var(--color-text-primary);
}
```

**Body Styles:**

```css
/* Body - Default */
.body-default {
  font-size: var(--font-size-base); /* 16px */
  font-weight: var(--font-weight-normal);
  line-height: var(--line-height-normal);
  color: var(--color-text-primary);
}

/* Body - Large (introductory paragraphs) */
.body-large {
  font-size: var(--font-size-lg); /* 18px */
  font-weight: var(--font-weight-normal);
  line-height: var(--line-height-normal);
  color: var(--color-text-secondary);
}

/* Body - Small (captions, disclaimers) */
.body-small {
  font-size: var(--font-size-sm); /* 14px */
  font-weight: var(--font-weight-normal);
  line-height: var(--line-height-normal);
  color: var(--color-text-secondary);
}

/* Label (form labels, uppercase labels) */
.label {
  font-size: var(--font-size-sm); /* 14px */
  font-weight: var(--font-weight-medium);
  line-height: var(--line-height-normal);
  color: var(--color-text-primary);
}
```

---

## Spacing System

### Scale (using 4px base unit)

```css
--spacing-0: 0;
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

**WHY 4px Base:**

- Divides evenly by 2 (easy to halve)
- Common standard in design systems
- Creates visual rhythm
- Easy to remember and calculate

---

### Spacing Usage Guidelines

**Component Padding:**

- Button: `--spacing-4 --spacing-8` (16px vertical, 32px horizontal)
- Card: `--spacing-8` (32px all sides) on desktop, `--spacing-6` (24px) on mobile
- Input: `--spacing-3 --spacing-4` (12px vertical, 16px horizontal)

**Layout Spacing:**

- Section vertical: `--spacing-20` (80px) on desktop, `--spacing-16` (64px) on mobile
- Between cards: `--spacing-8` (32px)
- Between paragraphs: `--spacing-6` (24px)
- Between heading and text: `--spacing-4` (16px)

**Container Padding:**

- Desktop: `--spacing-6` (24px)
- Mobile: `--spacing-4` (16px)

---

## Border Radius

```css
--radius-none: 0;
--radius-sm: 0.25rem; /* 4px - small elements */
--radius-base: 0.5rem; /* 8px - default (buttons, inputs) */
--radius-md: 0.75rem; /* 12px - cards */
--radius-lg: 1rem; /* 16px - large cards, modals */
--radius-xl: 1.5rem; /* 24px - feature cards */
--radius-full: 9999px; /* Fully rounded (badges, pills) */
```

**Usage:**

- sm: Small buttons, tags
- base: Standard buttons, inputs, dropdowns
- md: Small cards, thumbnails
- lg: Cards, modals
- xl: Hero cards, feature showcases
- full: Avatar placeholders, badge icons

**WHY These Values:**

- Rounded corners feel modern and friendly
- Consistent rounding creates visual harmony
- Full rounding for circular elements

---

## Shadows

### Shadow Scale

```css
--shadow-xs: 0 1px 2px rgba(0, 0, 0, 0.05);
--shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.1), 0 1px 2px rgba(0, 0, 0, 0.06);
--shadow-base: 0 4px 6px rgba(0, 0, 0, 0.07), 0 2px 4px rgba(0, 0, 0, 0.06);
--shadow-md: 0 10px 15px rgba(0, 0, 0, 0.1), 0 4px 6px rgba(0, 0, 0, 0.05);
--shadow-lg: 0 20px 25px rgba(0, 0, 0, 0.1), 0 10px 10px rgba(0, 0, 0, 0.04);
--shadow-xl: 0 25px 50px rgba(0, 0, 0, 0.25);
```

**Usage:**

- xs: Subtle borders replacement
- sm: Cards (default state)
- base: Cards (hover state), dropdowns
- md: Modals, floating elements
- lg: Hero cards, prominent features
- xl: Large modals, overlays

**WHY Layered Shadows:**

- Multiple shadows create depth and realism
- Soft shadows feel modern and friendly
- Consistent elevation hierarchy

---

## Transitions

```css
--transition-fast: 150ms ease-in-out; /* Hover effects, checkboxes */
--transition-base: 200ms ease-in-out; /* Default interactions */
--transition-slow: 300ms ease-in-out; /* Modals, larger animations */
```

**Usage:**

- Fast: Small UI elements (buttons, links)
- Base: Most interactions (forms, cards)
- Slow: Page transitions, large modals

**Properties to Animate:**

- `background-color`
- `color`
- `transform` (scale, translate)
- `opacity`
- `box-shadow`

**DON'T Animate:**

- `height` / `width` (causes reflow, use transform scale instead)
- `margin` / `padding` (causes reflow, use transform translate instead)

---

## Component Specifications

### Buttons

#### Primary Button

**Visual Specs:**

```css
.button-primary {
  /* Layout */
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--spacing-2);
  padding: var(--spacing-4) var(--spacing-8);

  /* Typography */
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-semibold);
  line-height: 1;

  /* Colors */
  background-color: var(--color-primary-600);
  color: var(--color-text-inverse);

  /* Visual */
  border: none;
  border-radius: var(--radius-base);
  box-shadow: var(--shadow-sm);

  /* Interaction */
  cursor: pointer;
  transition: all var(--transition-base);
}

.button-primary:hover {
  background-color: var(--color-primary-700);
  box-shadow: var(--shadow-base);
  transform: translateY(-1px);
}

.button-primary:active {
  transform: translateY(0);
  box-shadow: var(--shadow-xs);
}

.button-primary:focus-visible {
  outline: 2px solid var(--color-primary-600);
  outline-offset: 2px;
}
```

**Usage:** Primary CTAs, form submissions

---

#### Secondary Button

**Visual Specs:**

```css
.button-secondary {
  /* Layout */
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--spacing-2);
  padding: calc(var(--spacing-4) - 2px) calc(var(--spacing-8) - 2px);

  /* Typography */
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-semibold);
  line-height: 1;

  /* Colors */
  background-color: transparent;
  color: var(--color-primary-600);

  /* Visual */
  border: 2px solid var(--color-primary-600);
  border-radius: var(--radius-base);

  /* Interaction */
  cursor: pointer;
  transition: all var(--transition-base);
}

.button-secondary:hover {
  background-color: var(--color-primary-600);
  color: var(--color-text-inverse);
  transform: translateY(-1px);
}
```

**Usage:** Secondary actions, "Learn More" links

---

#### Text Button

**Visual Specs:**

```css
.button-text {
  /* Layout */
  display: inline-flex;
  align-items: center;
  gap: var(--spacing-2);
  padding: var(--spacing-2) 0;

  /* Typography */
  font-size: var(--font-size-base);
  font-weight: var(--font-weight-medium);
  line-height: 1;

  /* Colors */
  background-color: transparent;
  color: var(--color-primary-600);

  /* Visual */
  border: none;
  border-bottom: 1px solid transparent;

  /* Interaction */
  cursor: pointer;
  transition: all var(--transition-fast);
}

.button-text:hover {
  border-bottom-color: var(--color-primary-600);
}
```

**Usage:** Inline links, "Learn More" within text

---

### Cards

#### Standard Card

**Visual Specs:**

```css
.card {
  /* Layout */
  padding: var(--spacing-8);

  /* Colors */
  background-color: var(--color-background-primary);

  /* Visual */
  border: 1px solid var(--color-border-primary);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-sm);

  /* Interaction */
  transition: all var(--transition-base);
}

.card:hover {
  box-shadow: var(--shadow-base);
  transform: translateY(-2px);
}

/* Mobile adjustments */
@media (max-width: 768px) {
  .card {
    padding: var(--spacing-6);
  }
}
```

**Structure:**

```html
<div class="card">
  <div class="card__icon">[Icon]</div>
  <h3 class="card__title">[Title]</h3>
  <p class="card__description">[Description]</p>
</div>
```

---

#### Feature Card (Large)

**Visual Specs:**

```css
.card-feature {
  /* Layout */
  padding: var(--spacing-12);
  text-align: center;

  /* Colors */
  background-color: var(--color-background-primary);

  /* Visual */
  border: 1px solid var(--color-border-primary);
  border-radius: var(--radius-xl);
  box-shadow: var(--shadow-base);

  /* Interaction */
  transition: all var(--transition-base);
}

.card-feature:hover {
  box-shadow: var(--shadow-md);
  transform: translateY(-4px);
}
```

**Usage:** Main feature showcases on homepage

---

### Form Elements

#### Input Field

**Visual Specs:**

```css
.input {
  /* Layout */
  width: 100%;
  padding: var(--spacing-3) var(--spacing-4);

  /* Typography */
  font-size: var(--font-size-base);
  font-family: var(--font-primary);
  line-height: var(--line-height-normal);

  /* Colors */
  background-color: var(--color-background-primary);
  color: var(--color-text-primary);

  /* Visual */
  border: 1px solid var(--color-border-primary);
  border-radius: var(--radius-base);

  /* Interaction */
  transition: all var(--transition-base);
}

.input:hover {
  border-color: var(--color-border-secondary);
}

.input:focus {
  outline: none;
  border-color: var(--color-border-focus);
  box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.1);
}

.input::placeholder {
  color: var(--color-text-tertiary);
}

/* Error state */
.input--error {
  border-color: var(--color-error);
}

.input--error:focus {
  box-shadow: 0 0 0 3px rgba(239, 68, 68, 0.1);
}
```

---

#### Textarea

**Same styling as input, with additions:**

```css
.textarea {
  /* Inherits all .input styles */
  min-height: 150px;
  resize: vertical;
}
```

---

#### Select Dropdown

**Visual Specs:**

```css
.select {
  /* Inherits all .input styles */

  /* Custom arrow */
  appearance: none;
  background-image: url("data:image/svg+xml,..."); /* Chevron down SVG */
  background-repeat: no-repeat;
  background-position: right var(--spacing-4) center;
  background-size: 16px;
  padding-right: calc(var(--spacing-4) * 2 + 16px);
}
```

---

### Navigation

#### Header

**Visual Specs:**

```css
.header {
  /* Layout */
  padding: var(--spacing-4) 0;

  /* Colors */
  background-color: var(--color-background-primary);
  border-bottom: 1px solid var(--color-border-primary);

  /* Position */
  position: sticky;
  top: 0;
  z-index: 100;

  /* Visual */
  box-shadow: var(--shadow-xs);
}
```

**Logo Size:**

- Desktop: 40px height
- Mobile: 32px height

**Navigation Links:**

```css
.nav-link {
  /* Typography */
  font-size: var(--font-size-base);
  font-weight: var(--font-weight-medium);

  /* Colors */
  color: var(--color-text-primary);
  text-decoration: none;

  /* Interaction */
  transition: color var(--transition-fast);
}

.nav-link:hover {
  color: var(--color-primary-600);
}

.nav-link--active {
  color: var(--color-primary-600);
}
```

---

#### Mobile Menu

**Visual Specs:**

```css
.mobile-menu {
  /* Position */
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  width: 280px;

  /* Colors */
  background-color: var(--color-background-primary);

  /* Visual */
  box-shadow: var(--shadow-xl);

  /* Animation */
  transform: translateX(100%);
  transition: transform var(--transition-slow);
}

.mobile-menu--open {
  transform: translateX(0);
}
```

---

### Icons

**Size Standards:**

```css
--icon-xs: 16px; /* Inline with text */
--icon-sm: 20px; /* Small UI elements */
--icon-base: 24px; /* Default icon size */
--icon-md: 32px; /* Card icons */
--icon-lg: 48px; /* Feature card icons */
--icon-xl: 64px; /* Hero section icons */
```

**Stroke Width:**

- Default: 2px
- Thin: 1.5px (large icons)
- Thick: 2.5px (emphasis)

**Color Usage:**

- Primary actions: `var(--color-primary-600)`
- Decorative: `var(--color-gray-400)`
- Success: `var(--color-success-500)`
- Warning: `var(--color-warning-500)`

---

## Layout Patterns

### Container

**Max Width:**

```css
.container {
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  padding-left: var(--spacing-6);
  padding-right: var(--spacing-6);
}

@media (max-width: 768px) {
  .container {
    padding-left: var(--spacing-4);
    padding-right: var(--spacing-4);
  }
}
```

**WHY 1200px:**

- Comfortable reading width
- Works well on 1366px and 1920px screens
- Leaves breathing room on larger displays

---

### Grid System

**Two Column:**

```css
.grid-2 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--spacing-8);
}

@media (max-width: 768px) {
  .grid-2 {
    grid-template-columns: 1fr;
    gap: var(--spacing-6);
  }
}
```

**Three Column:**

```css
.grid-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--spacing-8);
}

@media (max-width: 1024px) {
  .grid-3 {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .grid-3 {
    grid-template-columns: 1fr;
    gap: var(--spacing-6);
  }
}
```

---

### Section Spacing

```css
.section {
  padding-top: var(--spacing-20); /* 80px */
  padding-bottom: var(--spacing-20);
}

@media (max-width: 768px) {
  .section {
    padding-top: var(--spacing-16); /* 64px */
    padding-bottom: var(--spacing-16);
  }
}

/* Alternate background sections */
.section--alt {
  background-color: var(--color-background-secondary);
}
```

---

## Animation Guidelines

### Hover Effects

**Standard Hover Pattern:**

```css
element {
  transition: all var(--transition-base);
}

element:hover {
  transform: translateY(-2px);
  box-shadow: [elevated shadow];
}
```

**WHY This Pattern:**

- Subtle upward movement suggests "lift"
- Increased shadow reinforces depth
- Smooth transition feels polished

---

### Focus States

**All Interactive Elements:**

```css
element:focus-visible {
  outline: 2px solid var(--color-primary-600);
  outline-offset: 2px;
}
```

**WHY This Pattern:**

- Clear visibility for keyboard navigation
- 2px offset prevents overlap with element
- Uses brand color for consistency

---

### Loading States

**Skeleton Loader:**

```css
.skeleton {
  background: linear-gradient(90deg, var(--color-gray-200) 25%, var(--color-gray-100) 50%, var(--color-gray-200) 75%);
  background-size: 200% 100%;
  animation: loading 1.5s ease-in-out infinite;
}

@keyframes loading {
  0% {
    background-position: 200% 0;
  }
  100% {
    background-position: -200% 0;
  }
}
```

---

## Responsive Breakpoints

```css
/* Mobile: 0-767px (default) */

/* Tablet: 768px-1023px */
@media (min-width: 768px) {
}

/* Desktop: 1024px-1279px */
@media (min-width: 1024px) {
}

/* Large Desktop: 1280px+ */
@media (min-width: 1280px) {
}
```

**WHY These Breakpoints:**

- 768px: Standard tablet landscape width
- 1024px: Standard desktop/laptop width
- 1280px: Large desktops (for max-width containers)

---

## Accessibility

### Color Contrast Requirements

**Text Contrast:**

- Normal text (< 18px): 4.5:1 minimum
- Large text (≥ 18px): 3:1 minimum
- UI components: 3:1 minimum

**Verified Combinations:**

- `--color-primary-600` on white: 4.5:1 ✓
- `--color-text-primary` on white: 16.5:1 ✓
- `--color-text-secondary` on white: 4.6:1 ✓

---

### Focus Indicators

**All interactive elements must have visible focus:**

- Keyboard users rely on focus indicators
- Never remove outline without replacement
- Focus state should be as visible as hover state

---

### Motion Preferences

**Respect prefers-reduced-motion:**

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## Print Styles

```css
@media print {
  /* Hide navigation, footers */
  .header,
  .footer,
  .cta-section {
    display: none;
  }

  /* Optimize typography for print */
  body {
    font-size: 12pt;
    line-height: 1.5;
    color: black;
  }

  /* Remove shadows and backgrounds */
  * {
    box-shadow: none !important;
    background: transparent !important;
  }

  /* Page breaks */
  h1,
  h2,
  h3 {
    page-break-after: avoid;
  }
}
```

---

## Dark Mode (Future Consideration)

**Not implemented in v1, but prepared:**

```css
@media (prefers-color-scheme: dark) {
  :root {
    --color-background-primary: #111827;
    --color-background-secondary: #1f2937;
    --color-text-primary: #f9fafb;
    --color-text-secondary: #d1d5db;
    /* ... adjust all colors */
  }
}
```

**WHY Not Now:**

- Focus on single implementation first
- Dark mode requires thorough testing
- Can be added in v2 with user toggle

---

## Usage Examples

### Example: Hero Section Styling

```html
<section class="section hero">
  <div class="container">
    <div class="hero__content">
      <h1 class="heading-1">Çocuğunuzun Ödevlerini Oyuna Çevirin</h1>
      <p class="body-large">ÖdevCim ile çocuğunuz ödevlerini zamanında tamamlıyor...</p>
      <div class="hero__cta">
        <button class="button-primary">Ücretsiz Dene</button>
        <button class="button-text">Nasıl Çalışır?</button>
      </div>
    </div>
    <div class="hero__image">
      <img src="..." alt="..." />
    </div>
  </div>
</section>
```

---

### Example: Feature Card

```html
<div class="card card-feature">
  <div class="card__icon">
    <svg width="48" height="48">...</svg>
  </div>
  <h3 class="heading-3 card__title">Tüm Ödevler Tek Yerde</h3>
  <p class="body-default card__description">Çocuğunuzun tüm ödevlerini ekleyin...</p>
</div>
```

---

## Design Checklist

Before considering a component "complete," verify:

- [ ] Follows color palette (no arbitrary colors)
- [ ] Uses spacing system (no random px values)
- [ ] Includes hover state
- [ ] Includes focus state (keyboard accessibility)
- [ ] Works on mobile (responsive)
- [ ] Maintains contrast ratios (accessibility)
- [ ] Uses consistent border-radius
- [ ] Follows typography hierarchy
- [ ] Includes transition/animation where appropriate
- [ ] Tested with long content (text overflow)

---

**This style guide should be the single source of truth for all design decisions. Any deviation should be documented and justified.**
