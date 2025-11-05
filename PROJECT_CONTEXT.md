# ÖdevCim Landing Page - Project Context

## Proje Hakkında

**ÖdevCim**, çocukların ödev takibini gamification (oyunlaştırma) ile eğlenceli ve motive edici hale getiren bir Progressive Web App (PWA) uygulamasıdır.

### Ana Ürün Özellikleri

- **Ödev Yönetimi**: Çocukların tüm ödevlerini ders, konu, teslim tarihi ve kategori (yazılı, proje, etkinlik, sözlü) bazında organize etme
- **Gamification Sistemi**: Puan kazanma, rozet toplama, seviye atlama, seri (streak) sistemi
- **Push Notifications**: Firebase Cloud Messaging ile günlük hatırlatıcılar (saat 18:00)
- **Offline-First**: localStorage bazlı veri yönetimi, internet olmadan çalışır
- **Privacy-Focused**: Hiçbir veri sunucuya gönderilmez, tüm veriler cihazda kalır
- **Multi-Tab Senkronizasyon**: Birden fazla sekmede açıkken veriler senkronize olur

### Hedef Kitle

- **Birincil**: İlkokul ve ortaokul çağında (6-14 yaş) çocuğu olan ebeveynler (25-45 yaş arası)
- **İkincil**: Ödev takibini sistemli hale getirmek isteyen öğrenciler

### Teknik Stack (Ana Uygulama)

- **Frontend**: React 18 + TypeScript (strict mode)
- **State Management**: Context API + Custom Hooks
- **Storage**: localStorage (repository pattern ile soyutlanmış)
- **Styling**: TailwindCSS
- **Backend**: Firebase Cloud Functions (sadece push notifications için)
- **PWA**: Service Worker + Manifest.json
- **Architecture**: Layered Architecture (Core → Storage → Hook → UI)

---

## Landing Page Projesi - Genel Bakış

### Amaç

ÖdevCim'i henüz tanımayan ebeveynlere tanıtmak, uygulamanın değer önerisini açıkça iletmek ve ücretsiz denemeye yönlendirmek.

### Kapsam

- **Çok sayfalı** (multi-page) HTML/CSS landing page
- **Responsive** (mobile-first yaklaşım)
- **Statik içerik** (backend entegrasyonu yok)
- **8 ana section**: Hero, Problem Statement, Solution, How It Works, Gamification, Privacy, Final CTA, Footer

### Teknik Stack (Landing Page)

- **HTML5**: Semantic tags, accessibility-first
- **CSS3**: Custom properties (CSS variables), Flexbox, Grid
- **TailwindCSS**: Utility-first CSS framework (v3.4+ via CDN)
- **Vanilla JavaScript**: Minimal JS (scroll animations, mobile menu - opsiyonel)
- **Google Fonts**: Inter font family
- **No frameworks**: React/Vue kullanılmayacak, sade HTML/CSS/JS

### Deployment

- **Platform**: Vercel veya Netlify
- **Repository**: Ayrı git repository (ana uygulamadan bağımsız)
- **Domain**: Subdomain veya ayrı domain (örn: landing.odevcim.com veya odevcim.com)

---

## Kod Standartları

### Genel Prensipler

- **Clarity over brevity**: Kod okunabilirliği kısalıktan daha önemli
- **Domain-specific naming**: Generic isimler yasak (i, j, temp, arr, data gibi)
- **Self-explanatory code**: Kod kendini açıklamalı, yorumlar sadece "neden" açıklamalı

### İsimlendirme Kuralları

- **CSS Classes**: kebab-case (`hero-title`, `feature-card`, `cta-button`)
- **IDs**: kebab-case, sadece section'lar için (`hero`, `problem-statement`)
- **JavaScript**: camelCase (`handleScrollAnimation`, `toggleMobileMenu`)
- **Files**: kebab-case (`landing-page-requirements.md`, `hero-mockup.png`)

### Yasaklar

- ❌ **else** kullanımı yasak → Her zaman guard clauses ve early returns kullan
- ❌ **Magic numbers/indexes** yasak → Her sayı bir CSS variable veya constant olmalı
- ❌ **Generic identifiers** yasak → `i`, `j`, `temp`, `arr`, `data` gibi isimler kullanma
- ❌ **innerHTML** ile HTML generation yasak → Template literal + createElement kullan
- ❌ **Negative conditions** yasak → `isReady` kullan, `isNotReady` değil

### Koşullar ve Kontrol Akışı

```javascript
// ❌ BAD: else kullanımı
function processTask(task) {
  if (task.isCompleted) {
    return calculatePoints(task);
  } else {
    return 0;
  }
}

// ✅ GOOD: guard clause
function processTask(task) {
  if (!task.isCompleted) {
    return 0;
  }

  return calculatePoints(task);
}
```

### Yorum Standartları

```css
/* ❌ BAD: "what" açıklayan yorum */
.hero-title {
  font-size: 3rem; /* Set font size to 3rem */
}

/* ✅ GOOD: "why" açıklayan yorum */
.hero-title {
  font-size: 3rem;
  /* WHY: Large title immediately grabs attention and communicates value proposition on first screen */
}
```

### CSS Organization

```css
/* ========================================
   SECTION NAME
   ======================================== */

/* WHY: Brief explanation of design decision */
.section-class {
  /* Properties */
}
```

### Accessibility Requirements

- Her image için anlamlı `alt` text
- Butonlar için descriptive text (❌ "Tıkla", ✅ "Ücretsiz Deneyin")
- Keyboard navigation desteği (Tab, Enter)
- ARIA labels gerekli yerlerde
- Color contrast ratio minimum 4.5:1 (WCAG AA)
- Focus states görünür olmalı

### Responsive Approach

- **Mobile-first**: Base styles mobil için, media queries ile büyütme
- **Breakpoints**:
  - Mobile: `< 640px` (base)
  - Tablet: `≥ 640px`
  - Desktop: `≥ 1024px`
- **Touch-friendly**: Minimum 44px tıklanabilir alan (WCAG 2.1)

---

## Ana Uygulama ile İlişki

### Landing Page → Ana Uygulama Geçişi

- **CTA Butonları**: "Ücretsiz Dene" butonları ana uygulamaya yönlendirir
- **Target URL**: Ana uygulama URL'i (örn: `https://cc-two-smoky.vercel.app/`)

### Tasarım Tutarlılığı

- **Renk paleti**: Landing page renkleri ana uygulamayla uyumlu olmalı
- **Typography**: Aynı font family (Inter) kullanılmalı
- **Brand voice**: Samimi, sıcak, ebeveynlere hitap eden ton

### Maintenance

- Landing page bağımsız deploy edilir
- Ana uygulamadaki özellik güncellemeleri landing page'e manuel yansıtılır
- İçerik güncellemeleri CONTENT_COPY.md'den yapılır

---

## Performans Hedefleri

### Lighthouse Scores (Minimum)

- **Performance**: 90+
- **Accessibility**: 95+
- **Best Practices**: 90+
- **SEO**: 90+

### Loading Targets

- **First Contentful Paint (FCP)**: < 1.5s
- **Largest Contentful Paint (LCP)**: < 2.5s
- **Time to Interactive (TTI)**: < 3s
- **Total page size**: < 1MB (uncompressed)

### Optimization Strategies

- Compress images (WebP format, < 200KB each)
- Minify CSS/JS (production build)
- Use CDN for external resources (TailwindCSS, Google Fonts)
- Defer non-critical JavaScript
- Lazy load images below the fold (optional)

---

## Success Metrics

### Primary Goals

1. **Conversion Rate**: Landing page'e gelen ziyaretçilerin %X'i "Ücretsiz Dene" butonuna tıklıyor
2. **Bounce Rate**: < %60 (ziyaretçiler sayfada kalıyor)
3. **Average Time on Page**: > 45 saniye (içerik okunuyor)

### Secondary Goals

- **CTA Click Rate**: "Ücretsiz Dene" butonuna tıklama oranı > %15
- **Scroll Depth**: Ziyaretçilerin %70'i en az "How It Works" section'ına kadar scroll ediyor
- **Mobile Traffic**: Ziyaretçilerin %60+'ı mobil cihazdan geliyor

---

## Gelecek Planlar (v2)

### Landing Page İçin

- Video demo ekleme (30 saniyelik animasyon veya gerçek kullanım)
- Blog section ekleme (ebeveynler için ödev ipuçları)
- Social proof section (kullanıcı testimonials, case studies)
- A/B testing (farklı başlıklar, CTA buton renkleri)

### Ana Uygulamaya Yansıyacak Özellikler

- Kategori bazlı puan çarpanları (yazılı +20 puan, proje +30 puan)
- Rozet galerisi (50+ farklı rozet)
- Ebeveyn dashboard (çocuğun ilerlemesini görme)
- Multi-child support (birden fazla çocuk profili)

---

## Notlar

### Neden Ayrı Repository?

- Landing page deployment bağımsız (ana uygulamayı etkilemeden güncelleme)
- Farklı teknoloji stack (HTML/CSS)
- Farklı optimization gereksinimleri (SEO-focused vs app-focused)
- Farklı deployment frequency (landing nadiren güncellenir)

### Neden Framework Yok?

- **Simplicity**: Basit statik içerik için React/Vue gereksiz
- **Performance**: Vanilla HTML/CSS/JS daha hızlı yüklenir
- **SEO**: Server-side rendering gerektirmez, statik HTML arama motorları için ideal
- **Maintenance**: Framework versiyonları ve dependency'leri yönetmeye gerek yok

### Maintainer'a Not

Bu landing page, 6 ay sonra başka bir developer tarafından güncellenebilir. Bu yüzden:

- Her section için net yorumlar ekle (WHY: ...)
- CSS variable'ları DESIGN_SYSTEM.md'ye göre kullan
- Magic number kullanma, her değer anlamlı olmalı
- Kod okunabilirliği her şeyden önemli
