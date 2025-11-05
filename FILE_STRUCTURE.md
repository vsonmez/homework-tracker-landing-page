> ⚠️ **DEPRECATED**: Bu single-page versiyonu içindir.
> **Aktif dokümantasyon**: FILE_STRUCTURE_MULTIPAGE.md

# File Structure

## Directory Layout

```
odevcim-landing/
/
├── index.html           (Ana landing page)
├── ozellikler.html      (Features detay sayfası)
├── nasil-calisir.html   (How it works detay)
├── hakkimizda.html      (About us)
├── gizlilik.html        (Privacy policy)
├── iletisim.html        (Contact)
└── sss.html            (FAQ)
├── css/
│   └── styles.css
├── js/
│   └── main.js
├── images/
│   ├── hero-mockup.png
│   ├── logo.svg
│   ├── favicon.ico
│   └── og-image.png
├── docs/
│   ├── PROJECT_CONTEXT.md
│   ├── LANDING_PAGE_REQUIREMENTS.md
│   ├── CONTENT_COPY.md
│   ├── DESIGN_SYSTEM.md
│   ├── FILE_STRUCTURE.md
│   └── IMPLEMENTATION_CHECKLIST.md
├── README.md
├── .gitignore
└── vercel.json (or netlify.toml)
```

**WHY this structure:**

- Flat, simple hierarchy (no deep nesting)
- Clear separation of concerns (HTML, CSS, JS, images, docs)
- Easy to navigate for future maintainers
- Standard web project structure

---

## Root Level Files

### index.html

**Purpose**: Main HTML file, entry point for landing page

**Content Structure**:

```html
<!DOCTYPE html>
<html lang="tr">
  <head>
    <!-- Meta tags -->
    <!-- External resources (TailwindCSS, Google Fonts) -->
    <!-- Custom CSS -->
  </head>
  <body>
    <main>
      <section id="hero">...</section>
      <section id="problem">...</section>
      <section id="solution">...</section>
      <section id="how-it-works">...</section>
      <section id="gamification">...</section>
      <section id="privacy">...</section>
      <section id="cta">...</section>
    </main>

    <footer>...</footer>

    <!-- Optional JS -->
    <script src="js/main.js"></script>
  </body>
</html>
```

**WHY single HTML file:**

- Landing page = Single page application
- No routing needed
- Easier to maintain
- Better SEO (all content in one file)

---

### README.md

**Purpose**: Project documentation, setup instructions

**Content**:

```markdown
# ÖdevCim Landing Page

Landing page for ÖdevCim - a gamified homework tracking app for children.

## Quick Start

1. Clone the repository
2. Open `index.html` in a browser
3. No build process required

## Tech Stack

- HTML5 (semantic markup)
- CSS3 (custom properties, Grid, Flexbox)
- TailwindCSS (via CDN)
- Vanilla JavaScript (minimal, for animations)

## Project Structure

See `docs/FILE_STRUCTURE.md` for detailed structure

## Development

- All content: `docs/CONTENT_COPY.md`
- Design tokens: `docs/DESIGN_SYSTEM.md`
- Requirements: `docs/LANDING_PAGE_REQUIREMENTS.md`

## Deployment

Hosted on Vercel/Netlify

- Production URL: [TBD]
- Staging URL: [TBD]

## Contact

Questions? Contact: [email]
```

**WHY README at root:**

- First file developers see
- Quick orientation
- Standard practice

---

### .gitignore

**Purpose**: Exclude unnecessary files from version control

**Content**:

```
# OS files
.DS_Store
Thumbs.db

# Editor files
.vscode/
.idea/
*.swp
*.swo
*~

# Logs
*.log
npm-debug.log*

# Dependencies (if npm is added later)
node_modules/

# Build output (if build process added later)
dist/
build/

# Environment variables (if added)
.env
.env.local

# Temporary files
tmp/
temp/
```

**WHY these exclusions:**

- OS files clutter repository
- Editor configs are personal
- Logs not needed in version control

---

### vercel.json

**Purpose**: Vercel deployment configuration

**Content**:

```json
{
  "version": 2,
  "builds": [
    {
      "src": "index.html",
      "use": "@vercel/static"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "/index.html"
    }
  ],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "X-Frame-Options",
          "value": "DENY"
        },
        {
          "key": "X-XSS-Protection",
          "value": "1; mode=block"
        }
      ]
    },
    {
      "source": "/images/(.*)",
      "headers": [
        {
          "key": "Cache-Control",
          "value": "public, max-age=31536000, immutable"
        }
      ]
    }
  ]
}
```

**WHY these configurations:**

- Security headers protect against common attacks
- Cache headers optimize image loading
- SPA routing fallback to index.html

---

### netlify.toml (Alternative)

**Purpose**: Netlify deployment configuration

**Content**:

```toml
[build]
  publish = "."
  command = "echo 'No build required'"

[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-XSS-Protection = "1; mode=block"
    X-Content-Type-Options = "nosniff"

[[headers]]
  for = "/images/*"
  [headers.values]
    Cache-Control = "public, max-age=31536000, immutable"
```

---

## /css Directory

### styles.css

**Purpose**: Custom CSS styles (extends TailwindCSS)

**File Organization**:

```css
/* ==========================================
   CSS VARIABLES
   WHY: Centralized design tokens, easy to update
   ========================================== */
:root {
  /* Color tokens */
  --color-primary: #3b82f6;
  /* ... all tokens from DESIGN_SYSTEM.md */
}

/* ==========================================
   RESET & BASE STYLES
   WHY: Consistent baseline across browsers
   ========================================== */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: var(--font-family-primary);
  font-size: var(--font-size-base);
  line-height: var(--line-height-normal);
  color: var(--color-text-primary);
  background-color: var(--color-background);
}

/* ==========================================
   UTILITY CLASSES
   WHY: Reusable patterns, DRY principle
   ========================================== */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: var(--spacing-6);
}

/* ==========================================
   COMPONENT STYLES
   WHY: Modular, reusable components
   ========================================== */
.button-primary {
  /* ... */
}
.card {
  /* ... */
}

/* ==========================================
   SECTION STYLES
   WHY: Specific styling per section
   ========================================== */
#hero {
  /* ... */
}
#problem {
  /* ... */
}

/* ==========================================
   RESPONSIVE OVERRIDES
   WHY: Mobile-first approach, progressive enhancement
   ========================================== */
@media (max-width: 640px) {
  /* ... */
}
@media (min-width: 1024px) {
  /* ... */
}

/* ==========================================
   ANIMATIONS
   WHY: Delight, modern feel (optional)
   ========================================== */
@keyframes fadeIn {
  /* ... */
}
```

**WHY single CSS file:**

- Landing page = limited scope, no need to split
- Easier to maintain (all styles in one place)
- No additional HTTP requests
- Can be minified to single file for production

---

## /js Directory

### main.js

**Purpose**: Minimal JavaScript for interactivity

**Content Structure**:

```javascript
/**
 * ÖdevCim Landing Page - Main JavaScript
 * WHY: Minimal JS, progressive enhancement, works without JS
 */

// ==========================================
// SMOOTH SCROLL TO SECTIONS
// WHY: Better UX for "Nasıl Çalışır?" button
// ==========================================
function initSmoothScroll() {
  const smoothScrollLinks = document.querySelectorAll('a[href^="#"]');

  smoothScrollLinks.forEach((link) => {
    link.addEventListener("click", (event) => {
      const targetId = link.getAttribute("href");

      // WHY: Skip if href is just "#"
      if (targetId === "#") {
        return;
      }

      event.preventDefault();

      const targetSection = document.querySelector(targetId);

      // WHY: Guard clause, early return if target not found
      if (!targetSection) {
        return;
      }

      targetSection.scrollIntoView({
        behavior: "smooth",
        block: "start",
      });
    });
  });
}

// ==========================================
// SCROLL REVEAL ANIMATIONS (OPTIONAL)
// WHY: Adds delight, modern feel
// ==========================================
function initScrollReveal() {
  // WHY: Feature detection, graceful degradation
  if (!("IntersectionObserver" in window)) {
    return;
  }

  const revealElements = document.querySelectorAll(".scroll-reveal");

  const observerOptions = {
    threshold: 0.15,
    rootMargin: "0px 0px -50px 0px",
  };

  const revealObserver = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.add("visible");
        // WHY: Stop observing after reveal (performance)
        revealObserver.unobserve(entry.target);
      }
    });
  }, observerOptions);

  revealElements.forEach((element) => {
    revealObserver.observe(element);
  });
}

// ==========================================
// MOBILE MENU TOGGLE (FUTURE)
// WHY: Prepared for navigation menu if added
// ==========================================
function initMobileMenu() {
  const menuToggle = document.querySelector("[data-mobile-menu-toggle]");
  const mobileMenu = document.querySelector("[data-mobile-menu]");

  // WHY: Guard clause, exit if elements don't exist
  if (!menuToggle || !mobileMenu) {
    return;
  }

  menuToggle.addEventListener("click", () => {
    const isExpanded = menuToggle.getAttribute("aria-expanded") === "true";

    menuToggle.setAttribute("aria-expanded", !isExpanded);
    mobileMenu.classList.toggle("hidden");
  });
}

// ==========================================
// INITIALIZE ALL FEATURES
// WHY: Run after DOM is loaded
// ==========================================
document.addEventListener("DOMContentLoaded", () => {
  initSmoothScroll();
  initScrollReveal();
  initMobileMenu();
});
```

**WHY minimal JavaScript:**

- Landing page should work without JS (progressive enhancement)
- SEO friendly (no client-side rendering)
- Fast load time
- Accessibility (JS failure doesn't break page)

---

## /images Directory

### Required Images

#### hero-mockup.png

**Purpose**: Phone mockup showing app interface
**Specs**:

- Format: PNG or WebP
- Dimensions: 800x1600px (phone aspect ratio)
- File size: < 200KB (compressed)
- Content: Task list + completed tasks + badge notification visible

**WHY these specs:**

- 800px width = Retina display ready (displays at 400px)
- WebP = Better compression than PNG
- < 200KB = Fast loading on mobile

---

#### logo.svg

**Purpose**: ÖdevCim logo for footer
**Specs**:

- Format: SVG (vector, scalable)
- Dimensions: 200x60px viewBox
- Colors: Use CSS variables for fill (color consistency)

**WHY SVG:**

- Scalable without quality loss
- Small file size
- Can be styled with CSS

---

#### favicon.ico

**Purpose**: Browser tab icon
**Specs**:

- Format: ICO (multi-resolution)
- Sizes: 16x16, 32x32, 48x48
- Simple, recognizable icon (e.g., checkmark or book)

**Additional favicon files** (modern browsers):

```
favicon-16x16.png
favicon-32x32.png
apple-touch-icon.png (180x180)
android-chrome-192x192.png
android-chrome-512x512.png
```

**WHY multiple sizes:**

- Different devices/contexts use different sizes
- Apple requires specific format for home screen
- Android uses specific sizes for PWA

---

#### og-image.png

**Purpose**: Open Graph image (social media sharing)
**Specs**:

- Format: PNG or JPG
- Dimensions: 1200x630px (Facebook/Twitter recommended)
- File size: < 300KB
- Content: Logo + tagline + visual (mockup preview)

**WHY 1200x630:**

- Facebook recommended size
- Twitter large card compatible
- LinkedIn compatible
- Displays well across platforms

---

### Image Naming Conventions

**DO:**

- ✅ `hero-mockup.png` (descriptive, lowercase, hyphenated)
- ✅ `feature-icon-gamification.svg`
- ✅ `screenshot-task-list.png`

**DON'T:**

- ❌ `img1.png` (not descriptive)
- ❌ `Hero_Mockup.png` (inconsistent casing)
- ❌ `heroMockup.png` (camelCase not standard for files)

**WHY hyphenated lowercase:**

- URL-safe (no spaces or special characters)
- Consistent with web standards
- Easy to type and remember

---

## /docs Directory

### Purpose

Contains all project documentation for Claude Code and future maintainers.

### Files

1. **PROJECT_CONTEXT.md** - High-level project overview
2. **LANDING_PAGE_REQUIREMENTS.md** - Detailed section requirements
3. **CONTENT_COPY.md** - All text content
4. **DESIGN_SYSTEM.md** - Design tokens and patterns
5. **FILE_STRUCTURE.md** - This file, explains file organization
6. **IMPLEMENTATION_CHECKLIST.md** - Step-by-step implementation guide

**WHY separate docs folder:**

- Keeps documentation organized
- Doesn't clutter root directory
- Easy to find for developers
- Can be excluded from production build

---

## HTML Structure (index.html)

### Document Head Structure

```html
<head>
  <!-- WHY: UTF-8 ensures Turkish characters display correctly -->
  <meta charset="UTF-8" />

  <!-- WHY: Responsive design, mobile-first -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- WHY: SEO, appears in search results -->
  <meta name="description" content="..." />
  <meta name="keywords" content="..." />

  <!-- WHY: Social media sharing (Facebook, LinkedIn) -->
  <meta property="og:title" content="..." />
  <meta property="og:description" content="..." />
  <meta property="og:image" content="/images/og-image.png" />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://odevcim.com" />

  <!-- WHY: Twitter card (better preview on Twitter) -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="..." />
  <meta name="twitter:description" content="..." />
  <meta name="twitter:image" content="/images/og-image.png" />

  <!-- WHY: Browser tab title, SEO -->
  <title>ÖdevCim - Çocuğunuzun Ödevlerini Oyuna Çevirin</title>

  <!-- WHY: Favicon, browser tab icon -->
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico" />
  <link rel="icon" type="image/png" sizes="32x32" href="/images/favicon-32x32.png" />
  <link rel="icon" type="image/png" sizes="16x16" href="/images/favicon-16x16.png" />
  <link rel="apple-touch-icon" sizes="180x180" href="/images/apple-touch-icon.png" />

  <!-- WHY: Font loading, faster than @import -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />

  <!-- WHY: TailwindCSS for rapid prototyping, utility classes -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- WHY: Custom styles, extends Tailwind, design system tokens -->
  <link rel="stylesheet" href="/css/styles.css" />
</head>
```

**WHY this order:**

1. Meta tags first (browser needs these immediately)
2. Title (appears in browser tab, SEO)
3. Favicons (browser tab icon)
4. Fonts (load early, prevent FOUT)
5. External CSS (Tailwind)
6. Custom CSS last (overrides Tailwind)

---

### Document Body Structure

```html
<body>
  <!-- WHY: Skip to main content (accessibility, keyboard navigation) -->
  <a href="#main" class="skip-to-main">Skip to main content</a>

  <!-- WHY: Optional navigation, can be added later -->
  <!-- <nav>...</nav> -->

  <!-- WHY: Main landmark, screen readers identify main content -->
  <main id="main">
    <!-- WHY: Each section has ID for smooth scroll navigation -->
    <section id="hero" aria-label="Hero section">...</section>
    <section id="problem" aria-label="Problem statement">...</section>
    <section id="solution" aria-label="Solution overview">...</section>
    <section id="how-it-works" aria-label="How it works">...</section>
    <section id="gamification" aria-label="Gamification features">...</section>
    <section id="privacy" aria-label="Privacy and security">...</section>
    <section id="cta" aria-label="Call to action">...</section>
  </main>

  <!-- WHY: Footer landmark, screen readers identify footer -->
  <footer role="contentinfo">...</footer>

  <!-- WHY: JS at bottom, non-blocking, progressive enhancement -->
  <script src="/js/main.js"></script>
</body>
```

**WHY this structure:**

- Semantic HTML5 tags (better SEO, accessibility)
- ARIA labels (screen reader support)
- IDs for smooth scroll navigation
- JavaScript at bottom (page renders before JS loads)

---

### Section ID Naming Convention

**Pattern**: `#section-name` (lowercase, hyphenated)

**Examples**:

- `#hero`
- `#problem`
- `#solution`
- `#how-it-works` (multi-word)
- `#gamification`
- `#privacy`
- `#cta`

**WHY this pattern:**

- Consistent with CSS class naming
- URL-safe (can be used in links: `page.html#hero`)
- Easy to type and remember

---

## Asset Optimization

### Image Optimization Checklist

**Before commit:**

- [ ] Compress images (TinyPNG, Squoosh, ImageOptim)
- [ ] Use WebP format (with PNG fallback)
- [ ] Ensure dimensions match usage (no oversized images)
- [ ] Add descriptive alt text
- [ ] Check file size (< 200KB per image)

**Tools**:

- **TinyPNG**: https://tinypng.com (online compression)
- **Squoosh**: https://squoosh.app (Google, advanced options)
- **ImageOptim**: https://imageoptim.com (Mac app)

---

### CSS Optimization (Production)

**Development**: Use unminified `styles.css` for readability

**Production**: Minify CSS

```bash
# Using cssnano or similar
npx cssnano styles.css styles.min.css
```

**WHY minification:**

- Removes whitespace, comments
- Reduces file size (faster load)
- Preserves functionality

---

### JavaScript Optimization (Production)

**Development**: Use unminified `main.js` with comments

**Production**: Minify JavaScript

```bash
# Using terser
npx terser main.js -o main.min.js -c -m
```

**WHY minification:**

- Removes comments, whitespace
- Shortens variable names (obfuscation)
- Smaller file size

---

## Version Control Best Practices

### Commit Message Convention

**Format**: `type: short description`

**Types**:

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code formatting (no logic change)
- `refactor:` Code restructuring (no behavior change)
- `perf:` Performance improvement
- `test:` Adding tests
- `chore:` Maintenance (dependencies, config)

**Examples**:

```
feat: add hero section with CTA buttons
fix: correct hero image alt text for accessibility
docs: update CONTENT_COPY.md with new tagline
style: format CSS with consistent spacing
refactor: extract button styles to component class
perf: compress hero-mockup.png from 500KB to 180KB
```

**WHY this convention:**

- Clear commit history
- Easy to generate changelog
- Standard practice (Conventional Commits)

---

### Branch Strategy (if using branches)

**Main branch**: `main` (production-ready code)
**Development branch**: `dev` (work-in-progress)
**Feature branches**: `feature/section-name`

**Example workflow**:

```bash
git checkout -b feature/hero-section
# Work on hero section
git commit -m "feat: add hero section structure"
git checkout dev
git merge feature/hero-section
```

**WHY branches:**

- Isolate work-in-progress from stable code
- Multiple developers can work simultaneously
- Easy to review changes (pull requests)

---

## Deployment Configuration

### Vercel Deployment

**Automatic deployment**:

1. Connect GitHub repository to Vercel
2. Push to `main` branch
3. Vercel automatically builds and deploys

**Custom domain**:

1. Add domain in Vercel dashboard
2. Update DNS records (provided by Vercel)
3. SSL certificate automatically provisioned

---

### Netlify Deployment

**Automatic deployment**:

1. Connect GitHub repository to Netlify
2. Configure build settings (use `netlify.toml`)
3. Push to `main` branch

**Custom domain**:

1. Add domain in Netlify dashboard
2. Update DNS records
3. Enable HTTPS (automatic Let's Encrypt)

---

## Environment-Specific Files

### Development vs Production

**Development**:

- Unminified CSS/JS
- Source maps enabled
- Verbose logging

**Production**:

- Minified CSS/JS
- No source maps
- Error tracking (Sentry, optional)

**Conditional loading** (future consideration):

```html
<!-- Development -->
<link rel="stylesheet" href="/css/styles.css" />

<!-- Production -->
<link rel="stylesheet" href="/css/styles.min.css" />
```

---

## File Checklist Before Launch

### Pre-launch Checklist

**HTML**:

- [ ] All meta tags present (description, OG, Twitter)
- [ ] Favicon links correct
- [ ] All images have alt text
- [ ] All links work (no broken hrefs)
- [ ] ARIA labels on sections
- [ ] Semantic HTML5 tags used

**CSS**:

- [ ] All design tokens from DESIGN_SYSTEM.md used
- [ ] No magic numbers (all values from variables)
- [ ] Responsive breakpoints tested
- [ ] Hover states defined
- [ ] Focus states visible

**JS**:

- [ ] Progressive enhancement (works without JS)
- [ ] No console.log statements
- [ ] Error handling present
- [ ] Comments explain "why", not "what"

**Images**:

- [ ] All images compressed (< 200KB)
- [ ] WebP format used (with fallback)
- [ ] Correct dimensions (not oversized)
- [ ] Alt text descriptive

**Performance**:

- [ ] Lighthouse score > 90
- [ ] Images lazy loaded (below fold)
- [ ] CSS/JS minified (production)
- [ ] External resources loaded via CDN

**Accessibility**:

- [ ] Color contrast > 4.5:1
- [ ] Keyboard navigation works
- [ ] Focus states visible
- [ ] Screen reader tested (VoiceOver/NVDA)
