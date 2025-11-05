# ÖdevCim Landing Page - Project Specification

## Project Overview

A multi-page landing website for ÖdevCim, a gamified homework tracking application for parents and children. The site must be built with vanilla HTML and CSS (no frameworks), optimized for performance, and fully responsive.

## Target Audience

**Primary:** Parents (25-45 years old) with children in elementary/middle school

**Pain Points:**

- Difficulty tracking children's homework
- Children procrastinating until the last minute
- Lack of awareness about upcoming deadlines
- Difficulty motivating children to complete homework

**Concerns:**

- "Is it too complex to learn?"
- "Will it take up phone storage?"
- "Is my data safe?"
- "Can my child use it?"

## Technical Requirements

### Technology Stack

- Pure HTML5 (semantic markup)
- Pure CSS3 (no preprocessors, use CSS custom properties)
- Vanilla JavaScript (minimal, for interactions only)
- No frameworks, no build tools
- Multi-page application (separate HTML files)

### Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)

### Performance Requirements

- Lighthouse score: 90+ (all categories)
- First Contentful Paint: < 1.5s
- Time to Interactive: < 3s
- Image optimization: WebP format with fallbacks
- Lazy loading for images below the fold

### Accessibility Requirements

- WCAG 2.1 AA compliance
- Semantic HTML structure
- Proper heading hierarchy (h1 → h2 → h3)
- Alt text for all images
- Keyboard navigation support
- Sufficient color contrast (4.5:1 minimum)
- Skip to main content link

### SEO Requirements

- Proper meta tags (title, description, OG tags)
- Structured data (JSON-LD)
- Sitemap.xml
- Robots.txt
- Canonical URLs

## Site Structure

### Pages

1. **index.html** - Homepage/Landing Page
2. **features.html** - Detailed Features Page
3. **how-it-works.html** - Step-by-step Guide
4. **privacy.html** - Privacy Policy
5. **terms.html** - Terms of Service
6. **contact.html** - Contact Form

### Navigation Structure

```
Header (all pages):
├── Logo (links to index.html)
├── Features (links to features.html)
├── How It Works (links to how-it-works.html)
├── Privacy (links to privacy.html)
└── CTA Button: "Ücretsiz Dene" (links to app URL)

Footer (all pages):
├── Quick Links
│   ├── Features
│   ├── How It Works
│   ├── Privacy Policy
│   └── Terms of Service
├── Contact
│   └── Contact Form Link
└── Social Media (placeholder icons)
```

## Page Specifications

### 1. Homepage (index.html)

#### Section A: Hero Section

**Purpose:** Grab attention immediately, communicate core value proposition

**Content:**

- H1: "Çocuğunuzun Ödevlerini Oyuna Çevirin"
- Subheading: "ÖdevCim ile çocuğunuz ödevlerini zamanında tamamlıyor, puan kazanıyor ve eğlenerek öğreniyor. Ücretsiz, reklamsız, tamamen sizin kontrolünüzde."
- Primary CTA: "Ücretsiz Dene" (large button, prominent)
- Secondary CTA: "Nasıl Çalışır?" (text link or smaller button)
- Hero Image: Mockup of app interface showing task list + badges + points

**Layout:**

- Desktop: 50/50 split (text left, image right)
- Mobile: Stacked (text top, image bottom)

**Why This Headline:**

- "Turn homework into a game" highlights gamification
- "Complete on time" addresses main pain point
- "Free, no ads" builds trust and transparency

---

#### Section B: Problem Statement

**Purpose:** Create empathy, establish "this is for me" feeling

**Heading:** "Bu Sorunlar Size Tanıdık Geliyor mu?"

**3 Problem Cards:**

1. **📚 "Hangi ödevler vardı?"**

   - Description: Çocuk defterini kontrol etmiyorsunuz, son gün panik oluyor

2. **⏰ "Son gün ödev stresine son"**

   - Description: Teslim tarihleri unutuluyor, geciken ödevler not düşüyor

3. **🎮 "Motivasyon sorunu"**
   - Description: Çocuk ödevi sıkıcı buluyor, yapmak için sürekli ikna gerekiyor

**Layout:**

- Desktop: 3 columns (cards side by side)
- Mobile: Stacked vertically

**Visual Style:**

- Each card has icon, heading, description
- Light background color per card
- Consistent padding and spacing

**Why This Section:**

- Don't sell solution before defining problem
- Creates emotional connection with target audience

---

#### Section C: Solution Overview

**Purpose:** Present core features as direct solutions to problems

**Heading:** "ÖdevCim ile Ödev Takibi Artık Eğlenceli"

**4 Feature Cards:**

1. **✅ Tüm Ödevler Tek Yerde**

   - Çocuğunuzun tüm ödevlerini ekleyin, derse ve konuya göre organize edin
   - Teslim tarihlerini girin, hangi ödevler yaklaşıyor hemen görün

2. **🔔 Akıllı Hatırlatıcılar**

   - Her gün saat 18:00'de push notification ile hatırlatma
   - "Yarın 2 ödevin teslim tarihi!" gibi bildirimler

3. **🎯 Oyunlaştırma Sistemi**

   - Her ödev tamamlandığında puan kazanın
   - Rozetler, seviyeler ve seri sistemleri ile çocuğunuzu motive edin
   - Proje, yazılı, etkinlik gibi kategorilerde özel rozetler

4. **📱 Offline Çalışır, Veri Güvenli**
   - İnternet olmadan çalışır, veriler cihazınızda kalır
   - Hiçbir bilginiz sunucularımıza gönderilmez
   - PWA teknolojisi: uygulama gibi kullanın, indirme gerektirmez

**Layout:**

- Desktop: 2x2 grid
- Mobile: Stacked vertically

**Why These Features:**

- Each feature directly addresses a problem from Section B
- Focus on benefits, not technical details
- Addresses privacy and security concerns upfront

---

#### Section D: How It Works

**Purpose:** Remove friction, show how easy it is to get started

**Heading:** "3 Adımda Başlayın"

**3 Step Cards:**

**1️⃣ Çocuğunuzu Ekleyin**

- İsim ve sınıf bilgisini girin (5 saniye)

**2️⃣ Ödevleri Ekleyin**

- Ders, konu, teslim tarihi ve ödev türünü belirtin
- Örnek: "Matematik - Çarpma İşlemleri - Yazılı - 10 Kasım"

**3️⃣ Çocuğunuz Tamamlasın, Rozetleri Kazansın**

- Her ödev tamamlandıkça puan ve rozet kazanın
- İlerlemeyi birlikte takip edin

**Layout:**

- Desktop: 3 columns with step numbers
- Mobile: Stacked with connecting lines between steps
- Optional: Small mockup screenshot for each step

**Why This Section:**

- "3 steps" feels achievable
- "5 seconds" removes barrier to entry
- Concrete example reduces ambiguity

---

#### Section E: Privacy & Security

**Purpose:** Address biggest parent concern: data safety

**Heading:** "Verileriniz Tamamen Güvende"

**3 Security Promises:**

1. **🔒 Hiçbir Veri Sunucuya Gitmiyor**

   - Tüm veriler cihazınızda localStorage'da tutuluyor
   - Hiçbir kişisel bilgi paylaşılmıyor

2. **📱 Offline Çalışır**

   - İnternet olmadan tüm özellikler kullanılabilir
   - Sadece push notification için bağlantı gerekir

3. **🚫 Reklamsız, Tamamen Ücretsiz**
   - Hiçbir reklam gösterilmez
   - Gizli ücret yok, tüm özellikler ücretsiz

**Layout:**

- Desktop: 3 columns
- Mobile: Stacked
- Each card with icon, heading, description

**Why This Section:**

- Privacy is #1 parent concern
- "Local storage" = trust builder
- "No ads" = premium feel, professionalism

---

#### Section F: Final CTA

**Purpose:** Convert visitors, remove last objections

**Heading:** "Çocuğunuzun Ödev Başarısını Şimdi Artırın"

**Subheading:** "Kurulum 5 saniye, ilk ödev ekleme 30 saniye. Hemen deneyin, kredi kartı gerekmez."

**CTA Buttons:**

- Primary: "Ücretsiz Başla" (large, prominent)
- Secondary: "Özellikleri Keşfet" (link to features.html)

**Why:**

- Emphasizes ease ("5 seconds")
- "No credit card" removes friction
- Clear, simple CTA

---

### 2. Features Page (features.html)

**Purpose:** Deep dive into features for users who want more detail

**Hero Section:**

- H1: "Ödev Takibini Kolaylaştıran Güçlü Özellikler"
- Brief intro paragraph

**Feature Sections (6 detailed sections):**

1. **Task Management**

   - Heading: Organize ve Takip Et
   - Details: Subject categorization, due dates, task types, completion tracking
   - Mockup: Task list interface

2. **Gamification System**

   - Heading: Oyunlaştırma ile Motivasyon
   - Details: Points system, badges, streaks, levels, category-based rewards
   - Mockup: Rewards page with badges and progress bars

3. **Smart Notifications**

   - Heading: Akıllı Hatırlatıcılar
   - Details: Daily reminders, deadline alerts, customizable timing
   - Mockup: Notification examples

4. **Multi-Child Support**

   - Heading: Birden Fazla Çocuk Desteği
   - Details: Separate profiles, individual tracking, easy switching
   - Mockup: Child selector interface

5. **Progress Analytics**

   - Heading: İlerleme Takibi
   - Details: Category statistics, completion rates, streak tracking
   - Mockup: Statistics dashboard

6. **PWA Technology**
   - Heading: Uygulama Gibi Kullanın
   - Details: Install to home screen, offline access, no app store needed
   - Mockup: Install prompt

**Layout Pattern:**

- Alternating left/right image placement (zigzag pattern)
- Each section: heading, paragraph, bullet points, mockup
- Generous white space between sections

---

### 3. How It Works Page (how-it-works.html)

**Purpose:** Step-by-step guide for first-time users

**Hero Section:**

- H1: "ÖdevCim'i Kullanmaya Başlayın"
- Subheading: "Adım adım rehber ile 2 dakikada hazır olun"

**Detailed Step Sections:**

**Step 1: İlk Kurulum**

- Open app
- Grant notification permissions (optional)
- Add first child (name + grade)
- Screenshot mockups for each sub-step

**Step 2: Ödev Ekleme**

- Click "Ödev Ekle" button
- Select child
- Choose subject
- Select task category (yazılı, proje, etkinlik, etc.)
- Set due date
- Add description
- Screenshot mockups

**Step 3: Ödev Tamamlama**

- Check off completed tasks
- View earned points
- See unlocked badges
- Track streak progress
- Screenshot mockups

**Step 4: Hatırlatıcılar Kurma**

- Access settings
- Enable/disable notifications
- Choose reminder time
- Screenshot mockups

**FAQ Section (at bottom):**

- "Birden fazla çocuk ekleyebilir miyim?"
- "Verilerim kaybolur mu?"
- "İnternet olmadan çalışır mı?"
- "Hangi cihazlarda kullanabilirim?"

---

### 4. Privacy Policy Page (privacy.html)

**Purpose:** Legal compliance and transparency

**Required Sections:**

1. Introduction
2. Data Collection (what data is collected)
3. Data Storage (localStorage, no server storage)
4. Data Usage (how data is used)
5. Third-Party Services (Firebase for notifications only)
6. User Rights
7. Children's Privacy
8. Changes to Policy
9. Contact Information

**Tone:** Legal but readable, parent-friendly language

**Why This Matters:**

- Legal requirement
- Builds trust
- Demonstrates transparency

---

### 5. Terms of Service Page (terms.html)

**Purpose:** Legal protection and usage guidelines

**Required Sections:**

1. Acceptance of Terms
2. Description of Service
3. User Responsibilities
4. Prohibited Uses
5. Intellectual Property
6. Disclaimers
7. Limitation of Liability
8. Termination
9. Governing Law
10. Contact Information

**Tone:** Legal but clear, avoid excessive jargon

---

### 6. Contact Page (contact.html)

**Purpose:** Support channel for users

**Hero Section:**

- H1: "Bizimle İletişime Geçin"
- Subheading: "Sorularınız mı var? Size yardımcı olmaktan mutluluk duyarız."

**Contact Form:**

- Name (required)
- Email (required)
- Subject (dropdown: Genel Soru, Teknik Destek, Öneri, Diğer)
- Message (textarea, required)
- Submit button

**Alternative Contact Methods:**

- Email: destek@odevcim.com (placeholder)
- Response time: 24-48 hours

**FAQ Link:** "Sıkça sorulan sorular için How It Works sayfasını ziyaret edin"

**Why This Page:**

- Builds trust (real support exists)
- Captures user feedback
- Reduces friction for questions

---

## Design Specifications

### Color Palette

```css
:root {
  /* Primary Colors */
  --color-primary: #4f46e5; /* Indigo 600 - main CTA, links */
  --color-primary-dark: #4338ca; /* Indigo 700 - hover states */
  --color-primary-light: #818cf8; /* Indigo 400 - accents */

  /* Secondary Colors */
  --color-secondary: #f59e0b; /* Amber 500 - badges, points */
  --color-secondary-dark: #d97706; /* Amber 600 */

  /* Success/Positive */
  --color-success: #10b981; /* Emerald 500 - completed tasks */

  /* Neutral Colors */
  --color-background: #ffffff;
  --color-background-alt: #f9fafb; /* Gray 50 - section backgrounds */
  --color-text: #111827; /* Gray 900 - primary text */
  --color-text-muted: #6b7280; /* Gray 500 - secondary text */

  /* Borders */
  --color-border: #e5e7eb; /* Gray 200 */
}
```

**Why These Colors:**

- Indigo: Modern, trustworthy, professional
- Amber: Energetic, gamification feel
- Emerald: Positive reinforcement
- High contrast ensures readability

---

### Typography

```css
:root {
  /* Font Families */
  --font-primary: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;

  /* Font Sizes */
  --font-size-xs: 0.75rem; /* 12px */
  --font-size-sm: 0.875rem; /* 14px */
  --font-size-base: 1rem; /* 16px */
  --font-size-lg: 1.125rem; /* 18px */
  --font-size-xl: 1.25rem; /* 20px */
  --font-size-2xl: 1.5rem; /* 24px */
  --font-size-3xl: 1.875rem; /* 30px */
  --font-size-4xl: 2.25rem; /* 36px */
  --font-size-5xl: 3rem; /* 48px */

  /* Font Weights */
  --font-weight-normal: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;
  --font-weight-bold: 700;

  /* Line Heights */
  --line-height-tight: 1.25;
  --line-height-normal: 1.5;
  --line-height-relaxed: 1.75;
}
```

**Typography Rules:**

- H1: 48px (desktop), 36px (mobile), bold, tight line-height
- H2: 36px (desktop), 30px (mobile), semibold
- H3: 24px, semibold
- Body: 16px (mobile), 18px (desktop), normal line-height
- Small text: 14px, muted color

**Why Inter Font:**

- Excellent readability at all sizes
- Professional, modern appearance
- System font fallbacks for fast loading

---

### Spacing System

```css
:root {
  --spacing-xs: 0.25rem; /* 4px */
  --spacing-sm: 0.5rem; /* 8px */
  --spacing-md: 1rem; /* 16px */
  --spacing-lg: 1.5rem; /* 24px */
  --spacing-xl: 2rem; /* 32px */
  --spacing-2xl: 3rem; /* 48px */
  --spacing-3xl: 4rem; /* 64px */
  --spacing-4xl: 6rem; /* 96px */
}
```

**Spacing Rules:**

- Section padding: 4rem (desktop), 3rem (mobile)
- Card padding: 2rem (desktop), 1.5rem (mobile)
- Element margins: Use consistent spacing scale
- Grid gaps: 2rem (desktop), 1.5rem (mobile)

**Why Consistent Spacing:**

- Creates visual rhythm
- Improves readability
- Makes layout predictable

---

### Component Specifications

#### Buttons

**Primary Button:**

```css
.button-primary {
  background: var(--color-primary);
  color: white;
  padding: 1rem 2rem;
  border-radius: 0.5rem;
  font-weight: 600;
  font-size: 1.125rem;
  transition: background 0.2s ease;
}

.button-primary:hover {
  background: var(--color-primary-dark);
}
```

**Secondary Button:**

```css
.button-secondary {
  background: transparent;
  color: var(--color-primary);
  border: 2px solid var(--color-primary);
  padding: 0.875rem 1.75rem;
  border-radius: 0.5rem;
  font-weight: 600;
  transition: all 0.2s ease;
}

.button-secondary:hover {
  background: var(--color-primary);
  color: white;
}
```

**Button States:**

- Default: As specified above
- Hover: Background darkens, scale: 1.02
- Focus: Outline ring (accessibility)
- Active: Scale: 0.98
- Disabled: Opacity: 0.5, cursor: not-allowed

---

#### Cards

**Standard Card:**

```css
.card {
  background: white;
  border: 1px solid var(--color-border);
  border-radius: 1rem;
  padding: 2rem;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  transition: box-shadow 0.2s ease;
}

.card:hover {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

**Card Structure:**

- Icon (top)
- Heading (H3)
- Description (paragraph)
- Optional: CTA link or button

---

#### Form Elements

**Input Fields:**

```css
.input {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 1px solid var(--color-border);
  border-radius: 0.5rem;
  font-size: 1rem;
  transition: border-color 0.2s ease;
}

.input:focus {
  outline: none;
  border-color: var(--color-primary);
  box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.1);
}
```

**Textarea:**

- Same styling as input
- Min-height: 150px
- Resize: vertical only

**Select Dropdown:**

- Same styling as input
- Custom arrow icon (SVG)

---

### Layout System

**Container:**

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1.5rem;
}
```

**Grid System:**

```css
.grid {
  display: grid;
  gap: 2rem;
}

.grid-cols-2 {
  grid-template-columns: repeat(2, 1fr);
}

.grid-cols-3 {
  grid-template-columns: repeat(3, 1fr);
}

/* Mobile: all grids collapse to 1 column */
@media (max-width: 768px) {
  .grid-cols-2,
  .grid-cols-3 {
    grid-template-columns: 1fr;
  }
}
```

**Section Layout:**

```css
.section {
  padding: 4rem 0;
}

.section-alt {
  background: var(--color-background-alt);
}
```

---

### Responsive Breakpoints

```css
/* Mobile: 0-767px (default styles) */

/* Tablet: 768px-1023px */
@media (min-width: 768px) {
  /* Adjust typography, increase spacing */
}

/* Desktop: 1024px+ */
@media (min-width: 1024px) {
  /* Multi-column layouts, larger typography */
}
```

**Mobile-First Approach:**

- Write styles for mobile first
- Use min-width media queries to add complexity
- Test on actual devices, not just browser resize

---

## Asset Requirements

### Images

**Mockups/Screenshots:**

- Task list view (showing multiple tasks with categories)
- Badge/rewards page (showing earned badges and progress)
- Notification example (push notification mockup)
- Add task form (modal view)
- Child selector (multi-child interface)
- Install prompt (PWA installation)

**Format:**

- WebP with PNG fallback
- Optimize for web (max 200KB per image)
- 2x resolution for retina displays

**Alt Text Required:**

- Descriptive, functional alt text for all images
- Example: "ÖdevCim uygulama ekranı gösterimi - ödev listesi ve puan sistemi"

---

### Icons

**Icon System:**

- Use SVG icons inline (for best performance)
- Icon library suggestion: Heroicons or Lucide icons
- Consistent size: 24px standard, 48px for feature cards
- Stroke width: 2px

**Required Icons:**

- Checkmark (completed tasks)
- Calendar (due dates)
- Trophy (badges/rewards)
- Bell (notifications)
- Lock (privacy/security)
- Phone (mobile device)
- Star (gamification)
- Chart (progress tracking)
- Users (multi-child)
- Menu (mobile navigation)

---

### Logo

**Requirements:**

- SVG format (scalable, small file size)
- Two versions: full logo (with text) and icon-only
- Color: Primary brand color
- White version for dark backgrounds

**Usage:**

- Header: Full logo on desktop, icon-only on mobile
- Footer: Full logo
- Favicon: Icon-only, multiple sizes

---

## Content Guidelines

### Voice & Tone

**Voice Characteristics:**

- Warm and friendly (not corporate)
- Parent-to-parent communication
- Empathetic to daily struggles
- Encouraging without being preachy

**Tone Guidelines:**

- Use "you" and "your child" (direct address)
- Avoid technical jargon
- Focus on benefits, not features
- Be specific with examples
- Keep sentences short and clear

**Examples:**

- Good: "Çocuğunuz her ödev tamamladığında puan kazanır"
- Bad: "Uygulama gamification mekanizması ile engagement artırır"

---

### Writing Style

**Headlines:**

- Clear, benefit-driven
- Action-oriented verbs
- Max 10 words
- No punctuation at end

**Body Copy:**

- Short paragraphs (2-3 sentences)
- Bullet points for lists
- One idea per paragraph
- Active voice

**CTAs:**

- Action verbs ("Başla", "Keşfet", "Dene")
- Create urgency without being pushy
- Specific, not generic
- Examples: "Ücretsiz Dene" > "Tıklayın"

---

### Legal Content

**Privacy Policy:**

- Plain language (avoid legalese when possible)
- Explain technical terms
- Short paragraphs
- Table of contents for easy navigation

**Terms of Service:**

- Clear expectations for users
- Define what is/isn't allowed
- Explain consequences
- Contact information for questions

---

## Implementation Guidelines

### File Structure

```
/
├── index.html
├── features.html
├── how-it-works.html
├── privacy.html
├── terms.html
├── contact.html
├── css/
│   ├── reset.css         (CSS reset/normalize)
│   ├── variables.css     (CSS custom properties)
│   ├── base.css          (base styles, typography)
│   ├── components.css    (buttons, cards, forms)
│   ├── layout.css        (grid, container, sections)
│   └── pages/
│       ├── home.css
│       ├── features.css
│       ├── how-it-works.css
│       └── contact.css
├── js/
│   ├── main.js          (shared functionality)
│   └── contact-form.js  (form validation/submission)
├── images/
│   ├── hero/
│   ├── mockups/
│   ├── icons/
│   └── logo/
├── favicon.ico
├── sitemap.xml
└── robots.txt
```

**Why This Structure:**

- Separation of concerns (CSS, JS, images)
- Modular CSS (easier to maintain)
- Page-specific styles in separate files
- Clear naming conventions

---

### HTML Standards

**Required Meta Tags (all pages):**

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta name="description" content="[Page-specific description]" />
<meta name="keywords" content="ödev takibi, çocuk eğitimi, gamification" />

<!-- Open Graph (social sharing) -->
<meta property="og:title" content="[Page title]" />
<meta property="og:description" content="[Page description]" />
<meta property="og:image" content="[Share image URL]" />
<meta property="og:url" content="[Page URL]" />

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="[Page title]" />
<meta name="twitter:description" content="[Page description]" />
<meta name="twitter:image" content="[Share image URL]" />
```

**Semantic HTML Requirements:**

- Use `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- Proper heading hierarchy (only one h1 per page)
- Use `<figure>` and `<figcaption>` for images
- Use `<button>` for actions, `<a>` for navigation
- Form fields must have `<label>` elements

**Accessibility Requirements:**

- All images must have alt text
- Forms must have labels
- Skip to main content link
- ARIA labels where semantic HTML isn't sufficient
- Focus styles visible for keyboard navigation

---

### CSS Standards

**Organization:**

1. CSS Reset/Normalize
2. CSS Custom Properties (variables)
3. Base styles (typography, defaults)
4. Layout styles (grid, container)
5. Component styles (buttons, cards)
6. Page-specific styles
7. Responsive overrides

**Naming Conventions:**

- Use BEM methodology (Block\_\_Element--Modifier)
- Example: `.card`, `.card__title`, `.card--featured`
- Descriptive class names (no abbreviations)
- Lowercase with hyphens

**CSS Best Practices:**

- Mobile-first (base styles for mobile, media queries for larger screens)
- Use CSS custom properties for theming
- Avoid !important
- Group related properties
- Comment complex selectors

---

### JavaScript Requirements

**JavaScript Usage:**

- Minimal JavaScript (progressive enhancement)
- No frameworks required
- ES6+ syntax (const/let, arrow functions, template literals)
- Event delegation for better performance

**Required Functionality:**

1. **Mobile Menu Toggle**

   - Hamburger menu on mobile
   - Smooth open/close animation
   - Close on outside click

2. **Contact Form Validation**

   - Client-side validation before submission
   - Display error messages
   - Prevent submission if invalid
   - Form submission handling (can be placeholder)

3. **Smooth Scroll**
   - Smooth scrolling for anchor links
   - Optional: scroll-triggered animations

**JavaScript Best Practices:**

- Strict mode (`'use strict';`)
- Avoid global variables
- Use event listeners, not inline handlers
- Graceful degradation (site works without JS)

---

### Performance Optimization

**Image Optimization:**

- Compress all images (TinyPNG or similar)
- Use WebP with PNG/JPG fallback
- Lazy load images below the fold
- Use `<picture>` element for responsive images
- Serve appropriate sizes for different viewports

**CSS Optimization:**

- Minimize CSS files
- Remove unused styles
- Inline critical CSS (above-the-fold styles)
- Defer non-critical CSS

**JavaScript Optimization:**

- Minimize JavaScript files
- Defer or async script loading
- Load scripts at end of body
- Code splitting if needed

**Loading Performance:**

- Minimize HTTP requests
- Use browser caching
- Compress assets (gzip/brotli)
- Optimize font loading (font-display: swap)

---

### Testing Requirements

**Browser Testing:**

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile Safari (iOS)
- Chrome Mobile (Android)

**Device Testing:**

- Desktop: 1920x1080, 1366x768
- Tablet: iPad (768x1024), iPad Pro
- Mobile: iPhone 12/13 (390x844), Android (360x640)

**Functionality Testing:**

- All links work correctly
- Forms validate and submit
- Navigation works on mobile
- Images load correctly
- Responsive layout works at all breakpoints

**Accessibility Testing:**

- Keyboard navigation works
- Screen reader compatible
- Color contrast sufficient
- Focus indicators visible
- Alt text present

**Performance Testing:**

- Lighthouse audit (score 90+ all categories)
- PageSpeed Insights
- WebPageTest
- Test on slow 3G connection

---

## Deployment

### Pre-Deployment Checklist

- [ ] All pages load without errors
- [ ] All links work (no 404s)
- [ ] Images optimized and loading
- [ ] Forms validate and submit
- [ ] Mobile responsive at all breakpoints
- [ ] Browser testing complete
- [ ] Accessibility audit passed
- [ ] Performance audit passed (Lighthouse 90+)
- [ ] Meta tags correct on all pages
- [ ] Sitemap.xml generated
- [ ] Robots.txt configured
- [ ] Favicon present and working
- [ ] Analytics code added (if applicable)

### Hosting Requirements

**Static Hosting Options:**

- Netlify (recommended)
- Vercel
- GitHub Pages
- Cloudflare Pages

**Configuration:**

- Custom domain support
- SSL certificate (HTTPS)
- CDN for asset delivery
- Redirect rules (www to non-www)
- 404 page configuration

### Post-Deployment

**Monitoring:**

- Set up uptime monitoring
- Track page load performance
- Monitor error logs
- Set up analytics (Google Analytics or similar)

**SEO:**

- Submit sitemap to Google Search Console
- Submit to Bing Webmaster Tools
- Verify social sharing previews

---

## Content Placeholders

### App URLs (to be replaced)

Throughout the site, use placeholder URLs that will be replaced with actual app URLs:

- `https://app.odevcim.com` - Main app URL
- `mailto:destek@odevcim.com` - Support email
- Social media links (currently placeholders)

### Imagery

If actual app screenshots are not available:

- Use Figma mockups
- Use placeholder illustrations from unDraw or Humaaans
- Use icon-only representations for features

---

## Success Metrics

### Primary Goals

1. **Conversion Rate:** % of visitors who click "Ücretsiz Dene"
2. **Engagement:** Time on site, pages per session
3. **Bounce Rate:** < 50% on homepage

### Secondary Goals

1. Contact form submissions
2. Social shares
3. Return visitor rate

### Tracking Implementation

- Google Analytics 4 (or privacy-friendly alternative)
- Event tracking for CTA clicks
- Form submission tracking
- Scroll depth tracking

---

## Future Enhancements (v2)

**Not in MVP, consider for future:**

1. **Blog Section**

   - Parenting tips
   - Homework strategies
   - Product updates

2. **Video Demo**

   - Screen recording walkthrough
   - Embedded YouTube/Vimeo

3. **Social Proof**

   - User testimonials
   - Usage statistics
   - Success stories

4. **Localization**

   - English version
   - Language switcher

5. **Interactive Demo**

   - Try app without signing up
   - Sample data populated

6. **FAQ Page**

   - Dedicated FAQ section
   - Search functionality

7. **Animations**
   - Scroll-triggered animations
   - Micro-interactions
   - Lottie animations

**Why Not Now:**

- Focus on core messaging first
- Get user feedback before adding complexity
- Faster time to launch

---

## Project Timeline Estimate

**Assuming full-time work:**

- Day 1-2: HTML structure for all pages
- Day 3-4: CSS implementation (layout, components)
- Day 5: Responsive design and mobile optimization
- Day 6: JavaScript functionality
- Day 7: Content population and imagery
- Day 8: Testing and bug fixes
- Day 9: Performance optimization
- Day 10: Final review and deployment

**Total: ~2 weeks for complete site**

**MVP (homepage only): ~5 days**

---

## Questions for Stakeholder

Before implementation, confirm:

1. Is the app URL ready? (for CTA buttons)
2. Are actual app screenshots available?
3. Is there a logo/brand identity?
4. Who handles form submissions? (contact form)
5. What analytics tool should be used?
6. Is there a preferred hosting platform?
7. Any specific legal requirements? (KVKK compliance for Turkey)

---

## Notes for Claude Code

**Implementation Priority:**

1. Start with homepage (index.html) - this is highest priority
2. Build CSS system (variables, components) early
3. Create reusable header/footer as HTML partials (copy-paste to each page)
4. Test responsive layout continuously during build
5. Implement accessibility features from the start (don't retrofit)

**Code Quality Standards:**

- Follow the coding preferences specified in user preferences
- Explicit, self-documenting names (no abbreviations)
- Comments explain "why", not "what"
- Guard clauses, early returns (no else blocks)
- Separate structure and behavior

**Common Pitfalls to Avoid:**

- Don't use Lorem Ipsum (all content is specified above)
- Don't create overly complex layouts (keep it simple)
- Don't ignore mobile (mobile-first approach)
- Don't forget alt text on images
- Don't use external dependencies unless necessary

---

**This specification is comprehensive and should provide Claude Code with everything needed to build the landing site. If any section needs clarification or expansion, ask before beginning implementation.**
