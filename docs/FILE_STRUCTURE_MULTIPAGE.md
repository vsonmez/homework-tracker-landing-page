ACTIVE DOCUMENT

# File Structure - Multi-Page Version

## Directory Layout

```
odevcim-landing/
├── index.html              # Ana landing page
├── ozellikler.html         # Features detay sayfası
├── nasil-calisir.html      # How it works detay
├── hakkimizda.html         # About us
├── gizlilik.html           # Gizlilik politikası
├── kullanim-sartlari.html  # Kullanım şartları
├── iletisim.html           # İletişim formu
├── sss.html                # Sık sorulan sorular
├── css/
│   ├── styles.css          # Global styles
│   └── pages/
│       ├── home.css        # index.html specific
│       ├── features.css    # ozellikler.html specific
│       └── contact.css     # iletisim.html specific
├── js/
│   ├── main.js             # Global JS
│   ├── navigation.js       # Header/navigation logic
│   └── contact-form.js     # Contact form validation
├── images/
│   ├── hero-mockup.png
│   ├── logo.svg
│   ├── favicon.ico
│   ├── og-image.png
│   └── features/           # Feature-specific images
│       ├── gamification-badge.png
│       ├── notification-preview.png
│       └── task-list-demo.png
├── docs/
│   ├── PROJECT_CONTEXT.md
│   ├── LANDING_PAGE_REQUIREMENTS.md
│   ├── CONTENT_COPY.md
│   ├── DESIGN_SYSTEM.md
│   ├── FILE_STRUCTURE.md
│   ├── FILE_STRUCTURE_MULTIPAGE.md  # Bu dosya
│   ├── IMPLEMENTATION_CHECKLIST.md
│   └── SEO_REQUIREMENTS.md
├── README.md
├── .gitignore
├── sitemap.xml             # SEO için
└── robots.txt              # SEO için
```

---

## Page Structure

### index.html (Ana Landing Page)

**Purpose**: First impression, value proposition, CTA

**Sections**:

- Hero (compressed - sadece başlık + CTA)
- Problem Statement (3 cards)
- Solution Overview (4 features - kısa açıklamalar)
- CTA → "Ücretsiz Dene" (ana uygulamaya) + "Özellikleri Keşfet" (ozellikler.html)
- Footer (tüm sayfalarda ortak)

**WHY compressed:**

- Landing page hızlı karar vermeli
- Detaylar ayrı sayfalarda
- Conversion-focused

---

### ozellikler.html (Features)

**Purpose**: Tüm özellikleri detaylı anlat

**Sections**:

- Header (navigation)
- Page Hero (mini hero: başlık + breadcrumb)
- Gamification Showcase (expanded - LANDING_PAGE_REQUIREMENTS.md'den)
- How It Works (3 steps - expanded)
- Technical Features (offline, privacy, PWA)
- CTA → "Hemen Başla"
- Footer

**WHY separate page:**

- Landing page'de çok uzun olmamalı
- Feature discovery için dedicated space
- SEO: "/ozellikler" keyword targeting

---

### nasil-calisir.html (How It Works)

**Purpose**: Step-by-step onboarding guide

**Sections**:

- Header
- Page Hero
- 3 Steps (her step için screenshot + detailed açıklama)
- Video Demo (gelecekte eklenebilir, şimdilik placeholder)
- Common Questions (mini FAQ - 3-4 soru)
- CTA → "Hemen Dene"
- Footer

**WHY separate page:**

- Detaylı tutorial göstermek
- Screenshot'larla somutlaştırmak

---

### hakkimizda.html (About Us)

**Purpose**: Brand story, team, mission

**Sections**:

- Header
- Page Hero
- Mission Statement ("Neden ÖdevCim'i yarattık?")
- Team (şimdilik boş, gelecekte eklenebilir)
- Values (eğitim, aile, teknoloji)
- Contact CTA → iletisim.html
- Footer

**WHY separate page:**

- Trust building
- Brand storytelling
- Personal connection

---

### gizlilik.html (Privacy Policy)

**Purpose**: Legal requirement, GDPR compliance

**Content**:

- Header
- TOC (Table of Contents)
- Sections:
  1. Veri Toplama (hangi veriler toplanıyor)
  2. Veri Kullanımı (nasıl kullanılıyor)
  3. Veri Saklama (nerede tutuluyor - localStorage)
  4. Çerezler (cookies policy)
  5. Kullanıcı Hakları
  6. İletişim
- Footer

**WHY dedicated page:**

- Legal requirement
- SEO + Trust signal
- GDPR compliance

---

### kullanim-sartlari.html (Terms of Service)

**Purpose**: Legal protection

**Content**:

- Header
- TOC
- Sections:
  1. Hizmet Kapsamı
  2. Kullanım Şartları
  3. Sorumluluk Reddi
  4. Değişiklikler
  5. İletişim
- Footer

---

### iletisim.html (Contact)

**Purpose**: User inquiries, support

**Content**:

- Header
- Page Hero
- Contact Form:
  - İsim
  - Email
  - Konu (dropdown: Genel, Destek, Öneri, Diğer)
  - Mesaj (textarea)
  - Submit button
- Contact Info (email: iletisim@odevcim.com)
- Footer

**WHY form:**

- Direct communication channel
- Lead generation
- User feedback collection

---

### sss.html (FAQ)

**Purpose**: Common questions, reduce support load

**Content**:

- Header
- Page Hero
- FAQ Categories:
  1. Genel Sorular (5-7 soru)
  2. Teknik Sorular (3-5 soru)
  3. Gizlilik ve Güvenlik (3-4 soru)
  4. Fiyatlandırma (1-2 soru)
- Accordion UI (expand/collapse)
- CTA → "Daha fazla soru mu var?" → iletisim.html
- Footer

**WHY separate page:**

- SEO goldmine (long-tail keywords)
- Reduce support tickets
- User self-service

---

## Shared Components

### Header (Tüm sayfalarda ortak)

**Content**:

- Logo (sol, link to index.html)
- Navigation Menu:
  - Özellikler (ozellikler.html)
  - Nasıl Çalışır (nasil-calisir.html)
  - Hakkımızda (hakkimizda.html)
  - İletişim (iletisim.html)
  - SSS (sss.html)
- CTA Button (sağ): "Ücretsiz Dene" (external link to main app)
- Mobile: Hamburger menu

**HTML Structure**:

```html
<header class="site-header">
  <div class="container">
    <a href="/" class="logo">
      <img src="/images/logo.svg" alt="ÖdevCim logosu" />
    </a>

    <nav class="main-nav">
      <a href="/ozellikler.html">Özellikler</a>
      <a href="/nasil-calisir.html">Nasıl Çalışır</a>
      <a href="/hakkimizda.html">Hakkımızda</a>
      <a href="/iletisim.html">İletişim</a>
      <a href="/sss.html">SSS</a>
    </nav>

    <a href="#" class="button-primary">Ücretsiz Dene</a>

    <!-- Mobile menu toggle -->
    <button class="mobile-menu-toggle" aria-label="Menüyü aç/kapat">☰</button>
  </div>
</header>
```

**WHY ortak header:**

- Consistent navigation
- Brand continuity
- Easy maintenance (tek yerden güncelle)

---

### Footer (Tüm sayfalarda ortak)

**Content**:

- Column 1: Logo + Tagline
- Column 2: Site Links (Özellikler, Nasıl Çalışır, Hakkımızda)
- Column 3: Legal Links (Gizlilik, Kullanım Şartları, İletişim, SSS)
- Column 4: Social Media (opsiyonel)
- Bottom: Copyright

**HTML Structure**:

```html
<footer class="site-footer">
  <div class="container footer-grid">
    <div class="footer-column">
      <img src="/images/logo.svg" alt="ÖdevCim" class="footer-logo" />
      <p>Çocukların ödev takibini eğlenceli hale getiren ücretsiz uygulama</p>
    </div>

    <div class="footer-column">
      <h4>Keşfet</h4>
      <a href="/ozellikler.html">Özellikler</a>
      <a href="/nasil-calisir.html">Nasıl Çalışır</a>
      <a href="/hakkimizda.html">Hakkımızda</a>
    </div>

    <div class="footer-column">
      <h4>Destek</h4>
      <a href="/sss.html">Sık Sorulan Sorular</a>
      <a href="/iletisim.html">İletişim</a>
      <a href="/gizlilik.html">Gizlilik Politikası</a>
      <a href="/kullanim-sartlari.html">Kullanım Şartları</a>
    </div>

    <div class="footer-column">
      <h4>Takip Et</h4>
      <!-- Social icons - gelecekte -->
    </div>
  </div>

  <div class="footer-bottom">
    <p>© 2025 ÖdevCim. Made with ❤️ in Turkey</p>
  </div>
</footer>
```

---

## CSS Organization

### /css/styles.css (Global)

- CSS Variables (DESIGN_SYSTEM.md'den)
- Reset & Base
- Typography
- Layout utilities (.container, grids)
- Header styles
- Footer styles
- Button components
- Card components

### /css/pages/home.css

- Hero section (index.html specific)
- Problem cards
- Solution cards

### /css/pages/features.css

- Gamification showcase
- Feature cards (expanded)

### /css/pages/contact.css

- Form styles
- Validation states

**WHY separate page CSS:**

- Code organization
- Faster loading (only load needed CSS)
- Easier maintenance

---

## JavaScript Organization

### /js/main.js (Global)

- Smooth scroll
- Scroll reveal animations
- Initialize all features

### /js/navigation.js

- Mobile menu toggle
- Active page highlight
- Sticky header

### /js/contact-form.js

- Form validation
- Submit handling
- Success/error messages

---

## SEO Structure

### URL Structure

```
https://odevcim.com/                    (Ana sayfa)
https://odevcim.com/ozellikler          (Features)
https://odevcim.com/nasil-calisir       (How it works)
https://odevcim.com/hakkimizda          (About)
https://odevcim.com/gizlilik            (Privacy)
https://odevcim.com/kullanim-sartlari   (Terms)
https://odevcim.com/iletisim            (Contact)
https://odevcim.com/sss                 (FAQ)
```

**WHY .html extension yok:**

- Clean URLs (Vercel/Netlify otomatik handle eder)
- SEO friendly
- Professional appearance

---

## Sitemap.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://odevcim.com/</loc>
    <lastmod>2025-11-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://odevcim.com/ozellikler</loc>
    <lastmod>2025-11-05</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://odevcim.com/nasil-calisir</loc>
    <lastmod>2025-11-05</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://odevcim.com/hakkimizda</loc>
    <changefreq>monthly</changefreq>
    <priority>0.5</priority>
  </url>
  <url>
    <loc>https://odevcim.com/gizlilik</loc>
    <changefreq>yearly</changefreq>
    <priority>0.3</priority>
  </url>
  <url>
    <loc>https://odevcim.com/kullanim-sartlari</loc>
    <changefreq>yearly</changefreq>
    <priority>0.3</priority>
  </url>
  <url>
    <loc>https://odevcim.com/iletisim</loc>
    <changefreq>monthly</changefreq>
    <priority>0.6</priority>
  </url>
  <url>
    <loc>https://odevcim.com/sss</loc>
    <changefreq>monthly</changefreq>
    <priority>0.7</priority>
  </url>
</urlset>
```

---

## Robots.txt

```
User-agent: *
Allow: /
Disallow: /admin/
Disallow: /private/

Sitemap: https://odevcim.com/sitemap.xml
```

---

## Breadcrumb Structure

Her sayfa (index hariç) breadcrumb içermeli:

```html
<nav aria-label="Breadcrumb" class="breadcrumb">
  <ol>
    <li><a href="/">Ana Sayfa</a></li>
    <li aria-current="page">Özellikler</li>
  </ol>
</nav>
```

**WHY breadcrumb:**

- SEO: Google breadcrumb'ı search results'ta gösterir
- UX: Kullanıcı nerede olduğunu bilir
- Navigation: Kolay geri dönüş

---

## Navigation Active State

```html
<!-- ozellikler.html sayfasındayken -->
<nav class="main-nav">
  <a href="/ozellikler.html" class="active" aria-current="page">Özellikler</a>
  <a href="/nasil-calisir.html">Nasıl Çalışır</a>
  <!-- ... -->
</nav>
```

**JavaScript (navigation.js)**:

```javascript
// WHY: Automatically highlight current page
const currentPath = window.location.pathname;
const navLinks = document.querySelectorAll(".main-nav a");

navLinks.forEach((link) => {
  if (link.getAttribute("href") === currentPath) {
    link.classList.add("active");
    link.setAttribute("aria-current", "page");
  }
});
```
