# Implementation Checklist

## Overview

Bu checklist, Claude Code'un landing page'i adım adım implement etmesi için hazırlanmıştır. Her adım tamamlandıkça işaretlenmelidir.

**Toplam Süre Tahmini**: 4-6 saat (tek kişi, dikkatli çalışma)

---

## Phase 1: Project Setup (15 dakika)

### 1.1 Repository Initialization

- [ ] Git repository oluştur
- [ ] `.gitignore` dosyası ekle
- [ ] `README.md` dosyası oluştur (temel bilgiler)
- [ ] Initial commit yap: `git commit -m "chore: initial project setup"`

**WHY bu sırayla:**

- Git tracking hemen başlamalı (değişiklikleri takip et)
- `.gitignore` önce ekle (gereksiz dosyaları commit etme)

---

### 1.2 Directory Structure

- [ ] `/css` klasörü oluştur
- [ ] `/js` klasörü oluştur
- [ ] `/images` klasörü oluştur
- [ ] `/docs` klasörü oluştur
- [ ] Tüm `.md` dosyalarını `/docs` içine yerleştir

**Verify**: Dizin yapısı `FILE_STRUCTURE.md`'deki gibi mi?

---

### 1.3 Documentation Files

- [ ] `PROJECT_CONTEXT.md` → `/docs` içine kopyala
- [ ] `LANDING_PAGE_REQUIREMENTS.md` → `/docs` içine kopyala
- [ ] `CONTENT_COPY.md` → `/docs` içine kopyala
- [ ] `DESIGN_SYSTEM.md` → `/docs` içine kopyala
- [ ] `FILE_STRUCTURE.md` → `/docs` içine kopyala
- [ ] `IMPLEMENTATION_CHECKLIST.md` → `/docs` içine kopyala

**Commit**: `git commit -m "docs: add project documentation"`

---

## Phase 2: HTML Structure (45 dakika)

### 2.1 Create index.html

- [ ] `index.html` dosyası oluştur
- [ ] DOCTYPE ve HTML lang="tr" ekle
- [ ] `<head>` section oluştur
- [ ] `<body>` section oluştur

**WHY bu adımlar:**

- HTML5 semantic yapı (SEO ve accessibility)
- Türkçe dil desteği (lang="tr")

---

### 2.2 Head Section - Meta Tags

- [ ] Charset meta tag ekle: `<meta charset="UTF-8">`
- [ ] Viewport meta tag ekle: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- [ ] Description meta tag ekle (CONTENT_COPY.md'den al)
- [ ] Keywords meta tag ekle
- [ ] Title tag ekle: `<title>ÖdevCim - Çocuğunuzun Ödevlerini Oyuna Çevirin</title>`

**Verify**: Meta description 150-160 karakter arası mı?

---

### 2.3 Head Section - Open Graph Tags

- [ ] `og:title` ekle
- [ ] `og:description` ekle
- [ ] `og:image` ekle (og-image.png path)
- [ ] `og:type` ekle (website)
- [ ] `og:url` ekle (production URL, geçici olarak placeholder)

**WHY Open Graph:**

- Facebook/LinkedIn share'de güzel görünüm
- Profesyonel görünüm

---

### 2.4 Head Section - Twitter Card Tags

- [ ] `twitter:card` ekle (summary_large_image)
- [ ] `twitter:title` ekle
- [ ] `twitter:description` ekle
- [ ] `twitter:image` ekle

---

### 2.5 Head Section - Favicon Links

- [ ] `<link rel="icon" type="image/x-icon" href="/images/favicon.ico">`
- [ ] `<link rel="icon" type="image/png" sizes="32x32" href="/images/favicon-32x32.png">`
- [ ] `<link rel="icon" type="image/png" sizes="16x16" href="/images/favicon-16x16.png">`
- [ ] `<link rel="apple-touch-icon" sizes="180x180" href="/images/apple-touch-icon.png">`

**Note**: Placeholder paths şimdilik, gerçek dosyalar Phase 3'te eklenecek

---

### 2.6 Head Section - External Resources

- [ ] Google Fonts preconnect ekle:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" /> <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
```

- [ ] Inter font ekle:

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
```

- [ ] TailwindCSS CDN ekle:

```html
<script src="https://cdn.tailwindcss.com"></script>
```

- [ ] Custom CSS link ekle:

```html
<link rel="stylesheet" href="/css/styles.css" />
```

**WHY bu sırayla:**

- Preconnect = DNS lookup hızlandırır
- Fonts early = FOUT (Flash of Unstyled Text) önler
- Tailwind before custom CSS = Custom CSS overrides Tailwind

---

### 2.7 Body Section - Skip to Main Link

- [ ] Body başına "skip to main content" link ekle:

```html
<a href="#main" class="skip-to-main">Skip to main content</a>
```

**WHY:**

- Accessibility (keyboard navigation)
- Screen reader kullanıcıları için

---

### 2.8 Body Section - Main Structure

- [ ] `<main id="main">` elementi oluştur
- [ ] 7 section elementi oluştur (id'lerle):
  - [ ] `<section id="hero" aria-label="Hero section">`
  - [ ] `<section id="problem" aria-label="Problem statement">`
  - [ ] `<section id="solution" aria-label="Solution overview">`
  - [ ] `<section id="how-it-works" aria-label="How it works">`
  - [ ] `<section id="gamification" aria-label="Gamification features">`
  - [ ] `<section id="privacy" aria-label="Privacy and security">`
  - [ ] `<section id="cta" aria-label="Call to action">`

**Verify**: Her section'ın id ve aria-label'ı var mı?

---

### 2.9 Body Section - Footer

- [ ] `<footer role="contentinfo">` elementi oluştur
- [ ] Footer içi boş bırak (Phase 4'te doldurulacak)

---

### 2.10 Body Section - JavaScript

- [ ] Body sonuna JS link ekle:

```html
<script src="/js/main.js"></script>
```

**WHY en sonda:**

- Non-blocking (sayfa JS olmadan render olur)
- Progressive enhancement

---

### 2.11 HTML Validation

- [ ] W3C HTML Validator ile kontrol et: https://validator.w3.org/
- [ ] Hataları düzelt

**Commit**: `git commit -m "feat: add HTML structure with semantic tags"`

---

## Phase 3: Content Integration (1 saat)

### 3.1 Hero Section Content

- [ ] Hero section içine container div ekle: `<div class="container">`
- [ ] 2-column layout için wrapper div: `<div class="split-layout">`
- [ ] Sol kolon: Text content
  - [ ] H1 başlık ekle (CONTENT_COPY.md'den)
  - [ ] Alt başlık ekle (p tag)
  - [ ] CTA butonları ekle:
    - [ ] Primary button: "Ücretsiz Dene" (href="#" şimdilik)
    - [ ] Secondary button: "Nasıl Çalışır?" (href="#how-it-works")
- [ ] Sağ kolon: Image
  - [ ] `<img>` tag ekle
  - [ ] `src="/images/hero-mockup.png"` (placeholder şimdilik)
  - [ ] `alt` text ekle (CONTENT_COPY.md'den)

**Verify**: Tüm metinler CONTENT_COPY.md'den birebir kopyalandı mı?

---

### 3.2 Problem Section Content

- [ ] Container div ekle
- [ ] H2 başlık ekle: "Bu Sorunlar Size Tanıdık Geliyor mu?"
- [ ] 3-column grid div ekle: `<div class="grid-3-col">`
- [ ] Problem 1 kartı:
  - [ ] `<article>` tag (semantic)
  - [ ] Icon ekle: 📚 (emoji, `<div class="icon-emoji">`)
  - [ ] H3 başlık ekle
  - [ ] Açıklama paragrafı ekle
- [ ] Problem 2 kartı (aynı yapı)
  - [ ] Icon: ⏰
  - [ ] H3 + p
- [ ] Problem 3 kartı (aynı yapı)
  - [ ] Icon: 🎮
  - [ ] H3 + p

**WHY `<article>` tag:**

- Semantic HTML (her problem kartı bağımsız içerik)
- SEO ve accessibility

---

### 3.3 Solution Section Content

- [ ] Container div ekle
- [ ] H2 başlık ekle: "ÖdevCim ile Ödev Takibi Artık Eğlenceli"
- [ ] 2x2 grid div ekle: `<div class="grid-2x2">`
- [ ] 4 özellik kartı oluştur (her biri `<article>`):
  - [ ] Özellik 1: ✅ Tüm Ödevler Tek Yerde
  - [ ] Özellik 2: 🔔 Akıllı Hatırlatıcılar
  - [ ] Özellik 3: 🎯 Oyunlaştırma Sistemi
  - [ ] Özellik 4: 📱 Offline Çalışır

**Her kart yapısı**:

- Icon (emoji)
- H3 başlık
- p açıklama

---

### 3.4 How It Works Section Content

- [ ] Container div ekle
- [ ] H2 başlık ekle: "3 Adımda Başlayın"
- [ ] Steps container div ekle
- [ ] 3 step kartı oluştur:
  - [ ] Step 1: 1️⃣ Çocuğunuzu Ekleyin
  - [ ] Step 2: 2️⃣ Ödevleri Ekleyin
  - [ ] Step 3: 3️⃣ Rozetleri Kazansın

**Her step yapısı**:

- Number badge (emoji veya styled div)
- H3 başlık
- p açıklama

---

### 3.5 Gamification Section Content

- [ ] Container div ekle
- [ ] H2 başlık ekle: "Ödevler Artık Oyun Gibi Eğlenceli"
- [ ] Alt başlık ekle (p tag)
- [ ] 2x2 grid div ekle
- [ ] 4 gamification özelliği kartı oluştur:
  - [ ] 🏆 Puan Sistemi
  - [ ] 🔥 Seri Sistemi
  - [ ] 🎖️ Rozetler
  - [ ] 📊 İlerleme Takibi

**WHY alt başlık:**

- Ek açıklama, context sağlar
- Okuma akışını düzenler

---

### 3.6 Privacy Section Content

- [ ] Container div ekle
- [ ] H2 başlık ekle: "Verileriniz Tamamen Güvende"
- [ ] 3-column grid div ekle
- [ ] 3 güvenlik kartı oluştur:
  - [ ] 🔒 Hiçbir Veri Sunucuya Gitmiyor
  - [ ] 📱 Offline Çalışır
  - [ ] 🚫 Reklamsız, Tamamen Ücretsiz

---

### 3.7 Final CTA Section Content

- [ ] Container div ekle
- [ ] H2 başlık ekle: "Çocuğunuzun Ödev Başarısını Şimdi Artırın"
- [ ] Alt başlık ekle
- [ ] CTA buttons container ekle
- [ ] 2 buton ekle:
  - [ ] Primary: "Ücretsiz Başla"
  - [ ] Secondary: "Demo İzle"

**WHY 2 CTA:**

- Primary = Ana aksiyon
- Secondary = Daha az commitment (video izle)

---

### 3.8 Footer Content

- [ ] 3-column grid div ekle (desktop), stack (mobile)
- [ ] Column 1: Branding
  - [ ] Logo placeholder (img tag veya text)
  - [ ] Tagline paragrafı
- [ ] Column 2: Linkler
  - [ ] "Gizlilik Politikası" link (href="#" şimdilik)
  - [ ] "Kullanım Şartları" link
  - [ ] "İletişim" link
  - [ ] "Sık Sorulan Sorular" link
- [ ] Column 3: Sosyal Medya (opsiyonel, şimdilik boş bırak)
- [ ] Bottom bar: Copyright text
  - [ ] "© 2025 ÖdevCim. Made with ❤️ in Turkey"

---

### 3.9 Content Proofreading

- [ ] Tüm başlıkları kontrol et (typo var mı?)
- [ ] Tüm açıklamaları kontrol et
- [ ] CTA buton metinleri doğru mu?
- [ ] Emoji'ler doğru mu?

**Commit**: `git commit -m "feat: add all content from CONTENT_COPY.md"`

---

## Phase 4: CSS Styling (2 saat)

### 4.1 Create styles.css

- [ ] `/css/styles.css` dosyası oluştur
- [ ] Dosya başına comment ekle:

```css
/**
   * ÖdevCim Landing Page - Custom Styles
   * WHY: Extends TailwindCSS, implements design system tokens
   */
```

---

### 4.2 CSS Variables

- [ ] `:root` selector oluştur
- [ ] DESIGN_SYSTEM.md'den tüm color tokens ekle:

```css
--color-primary: #3b82f6;
--color-primary-hover: #2563eb;
/* ... tüm renkler */
```

- [ ] Typography tokens ekle:

```css
--font-family-primary: "Inter", sans-serif;
--font-size-base: 1rem;
/* ... tüm font sizes */
```

- [ ] Spacing tokens ekle:

```css
--spacing-4: 1rem;
--spacing-6: 1.5rem;
/* ... tüm spacing */
```

- [ ] Border radius tokens ekle
- [ ] Shadow tokens ekle
- [ ] Transition tokens ekle

**Verify**: Tüm tokens DESIGN_SYSTEM.md'den eksiksiz kopyalandı mı?

**WHY CSS variables:**

- Tek yerden değişiklik yapmak kolay
- Magic number kullanımını önler
- Maintainability artırır

---

### 4.3 Reset & Base Styles

- [ ] Universal box-sizing ekle:

```css
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

- [ ] Body base styles:

```css
body {
  font-family: var(--font-family-primary);
  font-size: var(--font-size-base);
  line-height: var(--line-height-normal);
  color: var(--color-text-primary);
  background-color: var(--color-background);
}
```

- [ ] Smooth scroll behavior:

```css
html {
  scroll-behavior: smooth;
}
```

**WHY reset:**

- Consistent baseline across browsers
- Removes default browser styles

---

### 4.4 Utility Classes

- [ ] `.container` class:

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: var(--spacing-6);
}
```

- [ ] `.grid-3-col` class (DESIGN_SYSTEM.md'den)
- [ ] `.grid-2x2` class
- [ ] `.split-layout` class (hero için)
- [ ] `.skip-to-main` class (accessibility, visually hidden)

**Verify**: Her utility class responsive mi?

---

### 4.5 Component Styles - Buttons

- [ ] `.button-primary` class oluştur (DESIGN_SYSTEM.md'den)
  - Base styles
  - Hover state
  - Active state
  - Focus-visible state
- [ ] `.button-secondary` class oluştur
  - Base styles
  - Hover state
  - Active state

**Verify**: Focus outline görünür mü? (Accessibility)

---

### 4.6 Component Styles - Cards

- [ ] `.card` class oluştur (feature cards için)
  - Base styles
  - Hover state (lift effect)
- [ ] `.card-icon` class (emoji icons için)
- [ ] `.card-title` class
- [ ] `.card-description` class

**WHY lift effect:**

- Interactivity hissi
- Modern, engaging UX

---

### 4.7 Section Styles - Hero

- [ ] `#hero` section styles:
  - Background gradient
  - Padding
- [ ] `.hero-title` class (H1)
- [ ] `.hero-subtitle` class
- [ ] `.hero-buttons` container
- [ ] `.hero-image` class

**Verify**: Mobile'da image alta taşıyor mu?

---

### 4.8 Section Styles - Problem

- [ ] `#problem` section styles
- [ ] `.problem-card` class (border-left accent)

**WHY border-left:**

- Visual distinction (problem vs solution)
- Red accent = urgency

---

### 4.9 Section Styles - Solution

- [ ] `#solution` section styles
- [ ] `.solution-card` class

---

### 4.10 Section Styles - How It Works

- [ ] `#how-it-works` section styles
- [ ] `.step-card` class
- [ ] `.step-number` class (badge style)

---

### 4.11 Section Styles - Gamification

- [ ] `#gamification` section styles
- [ ] `.gamification-card` class (gradient background)

**WHY gradient background:**

- Visual emphasis (ana özellik)
- Daha attractive

---

### 4.12 Section Styles - Privacy

- [ ] `#privacy` section styles
- [ ] `.privacy-card` class (trust colors, border)

---

### 4.13 Section Styles - Final CTA

- [ ] `#cta` section styles
  - Full-width
  - Background gradient (solid primary)
  - White text
- [ ] `.cta-title` class
- [ ] `.cta-subtitle` class

**WHY solid background:**

- High contrast (attention-grabbing)
- Clear separation from other sections

---

### 4.14 Footer Styles

- [ ] `footer` element styles
  - Dark background
  - Light text
- [ ] `.footer-column` class
- [ ] `.footer-link` class (hover state)
- [ ] `.footer-bottom` class (copyright)

---

### 4.15 Responsive Overrides - Mobile

- [ ] `@media (max-width: 640px)` media query ekle
- [ ] Container padding küçült (var(--spacing-4))
- [ ] Section padding küçült (var(--spacing-16))
- [ ] Grid 3-col → 1-col
- [ ] Grid 2x2 → 1-col
- [ ] Split-layout → 1-col
- [ ] Font sizes küçült (H1: 36px)

**Test**: Mobil cihazda test et (Chrome DevTools)

---

### 4.16 Responsive Overrides - Tablet

- [ ] `@media (min-width: 641px) and (max-width: 1024px)` ekle
- [ ] Grid 3-col → 2-col
- [ ] Font sizes orta boyut

---

### 4.17 CSS Validation

- [ ] W3C CSS Validator ile kontrol et: https://jigsaw.w3.org/css-validator/
- [ ] Hataları düzelt

**Commit**: `git commit -m "style: implement complete design system with responsive layout"`

---

## Phase 5: JavaScript (30 dakika)

### 5.1 Create main.js

- [ ] `/js/main.js` dosyası oluştur
- [ ] Dosya başına comment ekle

---

### 5.2 Smooth Scroll Function

- [ ] `initSmoothScroll()` function oluştur
- [ ] Tüm `a[href^="#"]` linklerini seç
- [ ] Her link için click event listener ekle
- [ ] Smooth scroll to target section

**WHY:**

- Better UX ("Nasıl Çalışır?" butonu için)
- Modern feel

---

### 5.3 Scroll Reveal Function (Opsiyonel)

- [ ] `initScrollReveal()` function oluştur
- [ ] IntersectionObserver feature detection
- [ ] `.scroll-reveal` elementleri seç
- [ ] Observer oluştur (threshold: 0.15)
- [ ] `.visible` class ekle (viewport'a girdiğinde)

**Test**: Scroll animasyonları çalışıyor mu?

---

### 5.4 Mobile Menu Function (Gelecek için hazırlık)

- [ ] `initMobileMenu()` function oluştur
- [ ] Guard clause ekle (elements yoksa return)
- [ ] Toggle functionality implement et

**Note**: Şu an menü yok, future-proof için hazır

---

### 5.5 Initialize Functions

- [ ] `DOMContentLoaded` event listener ekle
- [ ] Tüm init functions'ı çağır:

```javascript
document.addEventListener("DOMContentLoaded", () => {
  initSmoothScroll();
  initScrollReveal();
  initMobileMenu();
});
```

---

### 5.6 JavaScript Validation

- [ ] Console'da hata var mı kontrol et
- [ ] JS çalışmazsa sayfa çalışıyor mu? (progressive enhancement)

**Commit**: `git commit -m "feat: add smooth scroll and scroll reveal animations"`

---

## Phase 6: Images & Assets (30 dakika)

### 6.1 Create Placeholder Images

- [ ] `hero-mockup.png` placeholder oluştur veya bul
  - Dimensions: 800x1600px
  - Content: Phone mockup with task list mockup
- [ ] Logo oluştur veya placeholder ekle
- [ ] Favicon oluştur (16x16, 32x32, 48x48)
- [ ] OG image oluştur (1200x630px)

**Tools**:

- Figma (mockup design)
- Canva (quick graphics)
- Favicon.io (favicon generator)

---

### 6.2 Optimize Images

- [ ] TinyPNG veya Squoosh ile compress et
- [ ] WebP format'a çevir (PNG fallback tut)
- [ ] Dosya boyutlarını kontrol et (< 200KB)

---

### 6.3 Add Images to /images

- [ ] Tüm görselleri `/images` klasörüne ekle
- [ ] Dosya isimlerini kontrol et (kebab-case)

---

### 6.4 Update HTML Image Paths

- [ ] Hero mockup `src` güncelle
- [ ] Logo `src` güncelle
- [ ] Favicon paths güncelle
- [ ] OG image path güncelle

**Verify**: Tüm görseller yükleniyor mu?

**Commit**: `git commit -m "feat: add optimized images and update paths"`

---

## Phase 7: Accessibility & SEO (30 dakika)

### 7.1 Accessibility Audit

- [ ] Her image'in alt text'i var mı?
- [ ] Butonlar descriptive text içeriyor mu?
- [ ] ARIA labels var mı?
- [ ] Heading hierarchy doğru mu? (H1 → H2 → H3, skip yok)
- [ ] Color contrast > 4.5:1 mı? (WebAIM kontrol et)
- [ ] Focus states görünür mü?
- [ ] Keyboard navigation çalışıyor mu? (Tab testi)

**Tool**: Lighthouse Accessibility audit

---

### 7.2 SEO Audit

- [ ] Title tag 60 karakterden kısa mı?
- [ ] Meta description 150-160 karakter arası mı?
- [ ] H1 sadece bir tane mi?
- [ ] Image alt texts descriptive mi?
- [ ] Internal links var mı? (smooth scroll links)
- [ ] OG tags tamamlandı mı?

**Tool**: Lighthouse SEO audit

---

### 7.3 Screen Reader Test

- [ ] VoiceOver (Mac) veya NVDA (Windows) ile test et
- [ ] Section labels okunuyor mu?
- [ ] Button labels anlamlı mı?
- [ ] Skip to main content link çalışıyor mu?

---

### 7.4 Lighthouse Audit

- [ ] Chrome DevTools → Lighthouse → Run audit
- [ ] Performance score > 90
- [ ] Accessibility score > 95
- [ ] Best Practices score > 90
- [ ] SEO score > 90

**Fix issues**: Lighthouse'un önerdiği düzeltmeleri yap

**Commit**: `git commit -m "fix: improve accessibility and SEO scores"`

---

## Phase 8: Responsive Testing (30 dakika)

### 8.1 Mobile Testing (< 640px)

- [ ] iPhone SE (375x667) test et
- [ ] iPhone 12 Pro (390x844) test et
- [ ] Text okunuyor mu?
- [ ] Butonlar tıklanabilir mi? (min 44px)
- [ ] Images overflow yok mu?
- [ ] Horizontal scroll yok mu?

---

### 8.2 Tablet Testing (640-1024px)

- [ ] iPad (768x1024) test et
- [ ] iPad Pro (1024x1366) test et
- [ ] Grid layout doğru mu? (2-column)
- [ ] Spacing uygun mu?

---

### 8.3 Desktop Testing (> 1024px)

- [ ] 1440px width test et
- [ ] 1920px width test et
- [ ] Container max-width çalışıyor mu? (1200px)
- [ ] Grid layout doğru mu? (3-column)
- [ ] Whitespace uygun mu?

---

### 8.4 Cross-Browser Testing

- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)

**Note**: Can I Use (caniuse.com) ile CSS feature support kontrol et

**Commit**: `git commit -m "test: verify responsive layout across devices"`

---

## Phase 9: Performance Optimization (30 dakika)

### 9.1 Image Optimization

- [ ] Lazy loading ekle (below-the-fold images):

```html
<img src="..." loading="lazy" alt="..." />
```

- [ ] WebP format + PNG fallback:

```html
<picture>
  <source srcset="hero.webp" type="image/webp" />
  <img src="hero.png" alt="..." />
</picture>
```

---

### 9.2 CSS Optimization

- [ ] Critical CSS inline et (hero section styles)
- [ ] Non-critical CSS defer et (gelecekte)
- [ ] Minify CSS (production için):

```bash
  npx cssnano css/styles.css css/styles.min.css
```

---

### 9.3 JavaScript Optimization

- [ ] Defer non-essential scripts
- [ ] Minify JS (production için):

```bash
  npx terser js/main.js -o js/main.min.js
```

---

### 9.4 Font Optimization

- [ ] `font-display: swap` ekle (Google Fonts URL'ye `&display=swap`)
- [ ] Font preconnect var mı?

---

### 9.5 Lighthouse Performance Audit

- [ ] Performance score > 90
- [ ] First Contentful Paint < 1.5s
- [ ] Largest Contentful Paint < 2.5s
- [ ] Cumulative Layout Shift < 0.1

**Fix issues**: Lighthouse önerilerini uygula

**Commit**: `git commit -m "perf: optimize images, CSS, and fonts for faster loading"`

---

## Phase 10: Deployment (30 dakika)

### 10.1 Pre-Deployment Checklist

- [ ] Tüm console.log'lar kaldırıldı mı?
- [ ] Placeholder links güncellendi mi? (CTA butonları)
- [ ] OG image path absolute URL mi? (https://...)
- [ ] Tüm images yükleniyor mu?
- [ ] No broken links
- [ ] HTML/CSS/JS validated

---

### 10.2 Vercel Deployment

- [ ] Vercel hesabı oluştur (github ile login)
- [ ] "New Project" → GitHub repository seç
- [ ] Build settings:
  - Framework Preset: Other
  - Build Command: (boş bırak, static site)
  - Output Directory: (boş bırak, root)
- [ ] Deploy butonuna tık
- [ ] Deployment success mu kontrol et

---

### 10.3 Custom Domain (Opsiyonel)

- [ ] Domain satın al (Namecheap, GoDaddy, vb.)
- [ ] Vercel dashboard → Domain settings
- [ ] Domain ekle, DNS kayıtlarını güncelle
- [ ] SSL certificate provision (automatic)

---

### 10.4 Post-Deployment Testing

- [ ] Production URL'de tüm sections yükleniyor mu?
- [ ] Images görünüyor mu?
- [ ] CTA butonları çalışıyor mu?
- [ ] Mobile'da test et (gerçek cihaz)
- [ ] Lighthouse audit (production URL)

---

### 10.5 Analytics Setup (Opsiyonel)

- [ ] Google Analytics hesabı oluştur
- [ ] Tracking code ekle (head'e, defer ile)
- [ ] Verify tracking çalışıyor (Real-Time report)

**Commit**: `git commit -m "chore: configure deployment and analytics"`

---

## Phase 11: Final Review & Polish (30 dakika)

### 11.1 Content Proofreading

- [ ] Tüm metinleri tekrar oku (typo kontrolü)
- [ ] CTA metinleri net mi?
- [ ] Alt texts descriptive mi?

---

### 11.2 Visual Polish

- [ ] Spacing tutarlı mı? (section arası)
- [ ] Alignment doğru mu? (centered vs left)
- [ ] Colors consistent mi? (design system'e uygun)
- [ ] Hover effects çalışıyor mu?

---

### 11.3 User Flow Test

- [ ] Hero'dan CTA'ya kadar flow mantıklı mı?
- [ ] Smooth scroll çalışıyor mu?
- [ ] CTA butonları dikkat çekiyor mu?

---

### 11.4 Documentation Update

- [ ] README.md güncelle (production URL ekle)
- [ ] CHANGELOG.md oluştur (opsiyonel)
- [ ] Deployment notları ekle

---

### 11.5 Final Lighthouse Audit

- [ ] Performance > 90
- [ ] Accessibility > 95
- [ ] Best Practices > 90
- [ ] SEO > 90

**Screenshot**: Lighthouse scores'u kaydet

---

### 11.6 Launch Announcement

- [ ] Social media post hazırla (Twitter, LinkedIn)
- [ ] Email announcement hazırla (eğer liste varsa)
- [ ] Product Hunt submission düşün (gelecekte)

**Commit**: `git commit -m "chore: final polish and launch preparation"`

---

## Phase 12: Post-Launch Monitoring (Ongoing)

### 12.1 Analytics Monitoring

- [ ] İlk hafta günlük kontrol et:
  - Visitor count
  - Bounce rate
  - Average time on page
  - CTA click rate
- [ ] Ikinci hafta haftalık kontrol

---

### 12.2 User Feedback Collection

- [ ] Hotjar veya benzer tool ekle (heatmap, recordings)
- [ ] Feedback formu ekle (gelecekte)
- [ ] User comments topla

---

### 12.3 A/B Testing (Gelecekte)

- [ ] Hero başlık alternatifleri test et
- [ ] CTA buton renkleri test et
- [ ] CTA buton metinleri test et

---

### 12.4 Iteration Planning

- [ ] Analytics'ten insights çıkar
- [ ] High bounce rate sections belirle
- [ ] Improvement roadmap oluştur

---

## Success Criteria

Landing page başarılı sayılır eğer:

### Technical Metrics

- ✅ Lighthouse Performance > 90
- ✅ Lighthouse Accessibility > 95
- ✅ Lighthouse SEO > 90
- ✅ No critical errors (console, HTML validation)
- ✅ Mobile responsive (tüm cihazlarda çalışıyor)

### User Metrics (İlk 2 hafta)

- ✅ Bounce rate < 60%
- ✅ Average time on page > 45 saniye
- ✅ CTA click rate > 10% (ziyaretçilerin %10'u tıklıyor)
- ✅ Scroll depth > 70% (ziyaretçilerin %70'i "How It Works" section'ına kadar scroll ediyor)

---

## Troubleshooting

### Common Issues

**Issue**: Images yüklenmiyor
**Fix**:

- Path'leri kontrol et (absolute vs relative)
- Console'da 404 hataları var mı bak
- Image dosya isimleri doğru mu? (case-sensitive)

**Issue**: CSS styles uygulanmıyor
**Fix**:

- `<link>` tag doğru mu?
- CSS dosya path'i doğru mu?
- Browser cache'i temizle (Cmd+Shift+R)
- CSS selector specificity kontrolü

**Issue**: Smooth scroll çalışmıyor
**Fix**:

- JavaScript console hatası var mı?
- `href` doğru ID'yi işaret ediyor mu?
- `scroll-behavior: smooth` CSS'de var mı?

**Issue**: Mobile'da horizontal scroll var
**Fix**:

- `overflow-x: hidden` ekle (body'ye)
- Fixed width elements var mı kontrol et
- Viewport meta tag var mı?

**Issue**: Lighthouse score düşük
**Fix**:

- Performance: Images compress et, lazy loading ekle
- Accessibility: Alt texts, ARIA labels, color contrast
- SEO: Meta tags, heading hierarchy
- Best Practices: HTTPS, no console errors

---

## Notes for Future Maintainers

### Where to Find What

- **Content changes**: `docs/CONTENT_COPY.md` → Update here, then update HTML
- **Design changes**: `docs/DESIGN_SYSTEM.md` → Update tokens, then update CSS
- **New sections**: Follow pattern in `docs/LANDING_PAGE_REQUIREMENTS.md`
- **Responsive issues**: Check `docs/DESIGN_SYSTEM.md` → Responsive patterns

### Common Maintenance Tasks

**Update CTA button link**:

1. Find all `.button-primary` in HTML
2. Update `href` attribute
3. Test on staging before production

**Add new section**:

1. Add section to HTML (follow semantic structure)
2. Add content from CONTENT_COPY.md
3. Add styles in CSS (follow naming convention)
4. Update IMPLEMENTATION_CHECKLIST.md

**Update images**:

1. Replace file in `/images`
2. Keep same filename (no HTML changes needed)
3. Compress before commit
4. Test on all devices

---

## Estimated Timeline

| Phase                       | Duration | Cumulative |
| --------------------------- | -------- | ---------- |
| 1. Project Setup            | 15 min   | 15 min     |
| 2. HTML Structure           | 45 min   | 1 hour     |
| 3. Content Integration      | 1 hour   | 2 hours    |
| 4. CSS Styling              | 2 hours  | 4 hours    |
| 5. JavaScript               | 30 min   | 4.5 hours  |
| 6. Images & Assets          | 30 min   | 5 hours    |
| 7. Accessibility & SEO      | 30 min   | 5.5 hours  |
| 8. Responsive Testing       | 30 min   | 6 hours    |
| 9. Performance Optimization | 30 min   | 6.5 hours  |
| 10. Deployment              | 30 min   | 7 hours    |
| 11. Final Review            | 30 min   | 7.5 hours  |

**Total**: ~7.5 hours (single developer, focused work)

**WHY this is realistic:**

- Includes testing and iteration time
- Accounts for debugging
- Buffer for unexpected issues
