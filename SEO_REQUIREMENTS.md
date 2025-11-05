# SEO Requirements

## Overview

Bu doküman, ÖdevCim landing page'inin arama motorlarında (Google, Bing, Yandex) iyi sıralanması için gerekli SEO gereksinimlerini içerir.

**Hedef Keywords:**

- ödev takibi
- çocuk ödevi
- ödev hatırlatıcı
- oyunlaştırma eğitim
- ücretsiz ödev uygulaması

**Target Audience Location:** Türkiye (Türkçe content)

---

## Meta Tags

### Basic Meta Tags

#### Page Title

```html
<title>ÖdevCim - Çocuğunuzun Ödevlerini Oyuna Çevirin | Ücretsiz Ödev Takip Uygulaması</title>
```

**Specs:**

- Karakter sayısı: 60-70 karakter (Google'da tam görünür)
- Primary keyword başta: "ÖdevCim"
- Secondary keyword: "Ödev Takip Uygulaması"
- Brand + value proposition birlikte

**WHY bu title:**

- "ÖdevCim" = Brand recognition
- "Ödevlerini Oyuna Çevirin" = Unique value proposition
- "Ücretsiz" = Önemli diferansiyatör
- Pipe (|) = Görsel ayırıcı, okunabilir

---

#### Meta Description

```html
<meta
  name="description"
  content="ÖdevCim ile çocuğunuzun ödevlerini eğlenceli hale getirin. Oyunlaştırma, rozetler ve hatırlatıcılarla ödev takibi artık kolay. Ücretsiz, reklamsız, güvenli."
/>
```

**Specs:**

- Karakter sayısı: 150-160 karakter (Google snippet'te tam görünür)
- Primary keywords: "ödev takibi", "oyunlaştırma", "hatırlatıcı"
- Call-to-action implicit: "eğlenceli hale getirin"
- USPs: "Ücretsiz, reklamsız, güvenli"

**WHY bu description:**

- Action-oriented (hale getirin = imperative)
- Benefit-focused (eğlenceli, kolay)
- Trust signals (güvenli, ücretsiz)

---

#### Meta Keywords (Optional, eski ama bazı arama motorları kullanıyor)

```html
<meta
  name="keywords"
  content="ödev takibi, çocuk ödevi, oyunlaştırma, eğitim uygulaması, ödev hatırlatıcı, ücretsiz ödev uygulaması, rozet sistemi, puan kazanma, ebeveyn için ödev takibi, ödev yönetimi"
/>
```

**WHY bu keywords:**

- Long-tail keywords dahil ("ebeveyn için ödev takibi")
- User intent kelimeler ("yönetimi", "hatırlatıcı")
- Feature keywords ("rozet sistemi", "puan kazanma")

---

#### Meta Robots

```html
<meta name="robots" content="index, follow" />
```

**WHY:**

- "index" = Bu sayfayı index'le
- "follow" = Bu sayfadaki linkleri takip et
- Default behavior ama explicit tanımlamak best practice

---

#### Canonical URL

```html
<link rel="canonical" href="https://odevcim.com" />
```

**WHY:**

- Duplicate content sorununu önler
- Preferred URL'i belirtir
- Production URL'i buraya eklenecek

---

### Open Graph Tags (Social Media SEO)

#### OG Basic Tags

```html
<meta property="og:type" content="website" />
<meta property="og:url" content="https://odevcim.com" />
<meta property="og:site_name" content="ÖdevCim" />
<meta property="og:locale" content="tr_TR" />
```

**WHY locale:**

- tr_TR = Türkçe içerik, Türkiye lokasyonu
- Facebook/LinkedIn bu bilgiyi kullanır

---

#### OG Title

```html
<meta property="og:title" content="ÖdevCim - Çocuğunuzun Ödevlerini Oyuna Çevirin" />
```

**Specs:**

- Karakter sayısı: 60-90 karakter
- Page title'dan biraz farklı olabilir (daha kısa)

---

#### OG Description

```html
<meta
  property="og:description"
  content="Ücretsiz, reklamsız ödev takip uygulaması. Rozetler, puanlar ve hatırlatıcılarla çocuğunuzu motive edin. Veriler güvende, offline çalışır."
/>
```

**Specs:**

- Karakter sayısı: 200 karakter max
- Meta description'dan farklı olabilir (social media için optimize)

---

#### OG Image

```html
<meta property="og:image" content="https://odevcim.com/images/og-image.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:image:alt" content="ÖdevCim - Ödev takip uygulaması ekran görüntüsü" />
```

**Image Specs:**

- Dimensions: 1200x630px (Facebook recommended)
- Format: PNG or JPG
- File size: < 300KB
- Content: Logo + tagline + mockup preview

**WHY 1200x630:**

- Facebook optimal size
- Twitter large card compatible
- LinkedIn compatible

---

### Twitter Card Tags

#### Twitter Card Type

```html
<meta name="twitter:card" content="summary_large_image" />
```

**WHY summary_large_image:**

- Büyük görsel = Daha çok dikkat çeker
- Summary = Başlık + açıklama + görsel

---

#### Twitter Title & Description

```html
<meta name="twitter:title" content="ÖdevCim - Ödev Takibini Eğlenceli Hale Getirin" />
<meta name="twitter:description" content="Çocuklar için gamification ile ödev takibi. Rozetler, puanlar, hatırlatıcılar. Tamamen ücretsiz." />
```

**Specs:**

- Title: 70 karakter max
- Description: 200 karakter max

---

#### Twitter Image

```html
<meta name="twitter:image" content="https://odevcim.com/images/og-image.png" />
<meta name="twitter:image:alt" content="ÖdevCim ödev takip uygulaması" />
```

**WHY same image as OG:**

- Consistency across platforms
- 1200x630 works for Twitter too

---

#### Twitter Site & Creator (Optional)

```html
<meta name="twitter:site" content="@odevcim" /> <meta name="twitter:creator" content="@odevcim" />
```

**Note:** Twitter handle yoksa şimdilik ekleme, gelecekte eklenebilir

---

## Structured Data (JSON-LD)

### Organization Schema

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "ÖdevCim",
    "url": "https://odevcim.com",
    "logo": "https://odevcim.com/images/logo.svg",
    "description": "Çocukların ödev takibini eğlenceli hale getiren ücretsiz uygulama",
    "address": {
      "@type": "PostalAddress",
      "addressCountry": "TR",
      "addressLocality": "Ankara"
    },
    "contactPoint": {
      "@type": "ContactPoint",
      "contactType": "Customer Support",
      "email": "iletisim@odevcim.com"
    }
  }
</script>
```

**WHY Organization Schema:**

- Google Knowledge Panel için
- Brand recognition artırır
- Contact bilgilerini structure'lar

---

### WebSite Schema

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "WebSite",
    "name": "ÖdevCim",
    "url": "https://odevcim.com",
    "potentialAction": {
      "@type": "SearchAction",
      "target": "https://odevcim.com/?s={search_term_string}",
      "query-input": "required name=search_term_string"
    }
  }
</script>
```

**WHY WebSite Schema:**

- Google sitelink search box için
- Gelecekte search feature eklenirse hazır

---

### SoftwareApplication Schema

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "ÖdevCim",
    "applicationCategory": "EducationalApplication",
    "operatingSystem": "Web Browser, iOS, Android",
    "offers": {
      "@type": "Offer",
      "price": "0",
      "priceCurrency": "TRY"
    },
    "aggregateRating": {
      "@type": "AggregateRating",
      "ratingValue": "4.8",
      "ratingCount": "150"
    }
  }
</script>
```

**Note:** Rating values placeholder, gerçek değerler eklenecek

**WHY SoftwareApplication Schema:**

- Google Search'te app card görünür
- "Ücretsiz" vurgusu yapılır
- Rating gösterilir (güven artırır)

---

### BreadcrumbList Schema (Future, multi-page olursa)

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "BreadcrumbList",
    "itemListElement": [
      {
        "@type": "ListItem",
        "position": 1,
        "name": "Ana Sayfa",
        "item": "https://odevcim.com"
      }
    ]
  }
</script>
```

**WHY:** Landing page tek sayfa olduğu için şimdilik gerek yok, blog eklenirse kullanılır

---

## HTML Semantic Structure

### Heading Hierarchy

**Critical Rule:** Sadece 1 H1, mantıksal sıra (H1 → H2 → H3, skip yok)

```html
<h1>Çocuğunuzun Ödevlerini Oyuna Çevirin</h1>
<!-- Hero -->

<h2>Bu Sorunlar Size Tanıdık Geliyor mu?</h2>
<!-- Problem -->
<h3>"Hangi ödevler vardı?"</h3>
<h3>"Son gün ödev stresine son"</h3>
<h3>"Motivasyon sorunu"</h3>

<h2>ÖdevCim ile Ödev Takibi Artık Eğlenceli</h2>
<!-- Solution -->
<h3>Tüm Ödevler Tek Yerde</h3>
<h3>Akıllı Hatırlatıcılar</h3>
<h3>Oyunlaştırma Sistemi</h3>
<h3>Offline Çalışır, Veri Güvenli</h3>

<h2>3 Adımda Başlayın</h2>
<!-- How It Works -->
<h3>Çocuğunuzu Ekleyin</h3>
<h3>Ödevleri Ekleyin</h3>
<h3>Rozetleri Kazansın</h3>

<h2>Ödevler Artık Oyun Gibi Eğlenceli</h2>
<!-- Gamification -->
<h3>Puan Sistemi</h3>
<h3>Seri Sistemi</h3>
<h3>Rozetler</h3>
<h3>İlerleme Takibi</h3>

<h2>Verileriniz Tamamen Güvende</h2>
<!-- Privacy -->
<h3>Hiçbir Veri Sunucuya Gitmiyor</h3>
<h3>Offline Çalışır</h3>
<h3>Reklamsız, Tamamen Ücretsiz</h3>

<h2>Çocuğunuzun Ödev Başarısını Şimdi Artırın</h2>
<!-- CTA -->
```

**WHY bu hierarchy:**

- SEO: Google heading hierarchy'i okur
- Accessibility: Screen readers heading'lerle navigate eder
- UX: Görsel hiyerarşi net

---

### Semantic HTML Tags

```html
<main id="main">
  <!-- Main content landmark -->
  <section id="hero">
    <!-- Thematic grouping -->
    <div class="container">
      <!-- Layout wrapper -->
      <article>
        <!-- Independent content -->
        <h1>...</h1>
        <p>...</p>
      </article>
    </div>
  </section>

  <section id="problem">
    <article>
      <!-- Each problem card is independent -->
      <h3>...</h3>
      <p>...</p>
    </article>
  </section>
</main>

<footer role="contentinfo">
  <!-- Footer landmark -->
  <nav>
    <!-- Navigation links -->
    <a href="...">Gizlilik Politikası</a>
  </nav>
</footer>
```

**WHY semantic tags:**

- SEO: Google content structure'ı anlar
- Accessibility: ARIA landmarks (main, footer)
- Future-proof: HTML5 standard

---

## Image Optimization for SEO

### Alt Text Guidelines

**Rule:** Her image mutlaka alt text olmalı, descriptive olmalı

```html
<!-- ❌ BAD -->
<img src="hero-mockup.png" alt="mockup" />
<img src="logo.png" alt="" />

<!-- ✅ GOOD -->
<img src="hero-mockup.png" alt="ÖdevCim uygulaması ekran görüntüsü - ödev listesi, tamamlanan görevler ve kazanılan rozetler görünüyor" />
<img src="logo.svg" alt="ÖdevCim logosu" />
```

**Alt Text Formula:**

```
[What it is] - [What's shown] - [Context]
```

**WHY detailed alt text:**

- SEO: Google Images indexing
- Accessibility: Screen readers için
- Image fail olursa meaningful text görünür

---

### Image File Naming

**Rule:** Descriptive, lowercase, hyphenated

```
❌ BAD: img1.png, Image_Final.png, DSC0012.jpg
✅ GOOD: hero-phone-mockup.png, odevcim-logo.svg, task-list-screenshot.png
```

**WHY:**

- SEO: Filename Google'da index'lenir
- Maintainability: Dosya ne olduğu belli

---

### Image Lazy Loading

```html
<img src="hero-mockup.png" alt="..." loading="lazy" />
```

**WHY:**

- Performance: Page load speed artırır
- SEO: Google Core Web Vitals (LCP) için önemli
- Below-the-fold images için kullan

---

## Internal Linking Strategy

### Anchor Text Best Practices

```html
<!-- ❌ BAD: Generic anchor text -->
<a href="#how-it-works">Tıklayın</a>
<a href="#gamification">Buraya</a>

<!-- ✅ GOOD: Descriptive anchor text -->
<a href="#how-it-works">Nasıl Çalışır?</a>
<a href="#gamification">Oyunlaştırma Özellikleri</a>
```

**WHY:**

- SEO: Anchor text Google'a context verir
- Accessibility: Screen reader kullanıcıları link purpose'u anlar
- UX: Kullanıcı nereye gideceğini bilir

---

### Smooth Scroll Links

```html
<a href="#how-it-works" aria-label="Nasıl çalıştığını öğrenmek için aşağı kaydır"> Nasıl Çalışır? </a>
```

**WHY aria-label:**

- Accessibility: Ekstra context (screen readers)
- Link purpose net

---

## URL Structure (Future, multi-page olursa)

### URL Best Practices

```
❌ BAD:
/page?id=123
/p/12345
/index.php?page=about

✅ GOOD:
/ozellikler
/hakkimizda
/gizlilik-politikasi
/blog/odev-takibi-ipuclari
```

**Rules:**

- Lowercase
- Hyphenated (not underscore)
- Descriptive
- Short (3-5 kelime max)
- Keywords include et

---

## Mobile SEO

### Viewport Meta Tag

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

**WHY:**

- Google mobile-first indexing kullanıyor
- Responsive design için kritik

---

### Mobile-Friendly Test

**Checklist:**

- [ ] Text 16px+ (readable without zoom)
- [ ] Tap targets 44x44px minimum
- [ ] No horizontal scroll
- [ ] Fast loading (< 3 seconds)
- [ ] No intrusive interstitials (pop-ups)

**Test Tool:** Google Mobile-Friendly Test
https://search.google.com/test/mobile-friendly

---

## Page Speed Optimization (SEO Impact)

### Core Web Vitals Targets

**Largest Contentful Paint (LCP):** < 2.5s

- Hero section hızlı yüklenmeli
- Above-the-fold images optimize et

**First Input Delay (FID):** < 100ms

- JavaScript minimal olmalı
- Defer non-critical scripts

**Cumulative Layout Shift (CLS):** < 0.1

- Image dimensions belirt (width, height)
- Font loading strategy (font-display: swap)

**WHY Core Web Vitals:**

- Google ranking factor (2021'den beri)
- User experience direkt etkiliyor

---

### Performance Checklist

- [ ] Images compressed (< 200KB each)
- [ ] WebP format kullan (PNG fallback)
- [ ] Lazy load below-the-fold images
- [ ] Minify CSS/JS (production)
- [ ] Use CDN for external resources
- [ ] Enable GZIP compression (server-side)
- [ ] Browser caching headers (server-side)

---

## Sitemap.xml (Future)

### Basic Sitemap Structure

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://odevcim.com/</loc>
    <lastmod>2025-11-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

**WHY sitemap:**

- Google'a URL'leri bildirmek için
- Crawl efficiency artırır
- Landing page tek sayfa olduğu için şimdilik gerek yok

**Future:** Blog eklendiğinde sitemap oluştur

---

## Robots.txt (Future)

### Basic Robots.txt

```
User-agent: *
Allow: /

Sitemap: https://odevcim.com/sitemap.xml
```

**WHY:**

- Crawl budget yönetimi
- Disallow specific paths (admin, private)

**Landing page için:** Şimdilik gerek yok, tüm sayfa public

---

## Analytics & Search Console Setup

### Google Analytics 4 (GA4)

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag() {
    dataLayer.push(arguments);
  }
  gtag("js", new Date());
  gtag("config", "G-XXXXXXXXXX");
</script>
```

**Track Events:**

- CTA button clicks
- Scroll depth
- Time on page

---

### Google Search Console

**Setup Steps:**

1. Add property (https://odevcim.com)
2. Verify ownership (HTML file veya meta tag)
3. Submit sitemap (gelecekte)
4. Monitor performance:
   - Impressions
   - Clicks
   - Average position
   - CTR (Click-through rate)

**Verification Meta Tag:**

```html
<meta name="google-site-verification" content="your-verification-code" />
```

---

## Local SEO (İleride Türkiye'de lokalize ederken)

### Google My Business (Optional)

Eğer fiziksel ofis varsa:

- Google My Business profile oluştur
- NAP (Name, Address, Phone) consistent olsun
- Reviews topla

**WHY:**

- Local search'te görünürlük
- Trust signal

---

## Content SEO Best Practices

### Keyword Density

**Target:** 1-2% keyword density (natural, not stuffed)

**Primary keyword ("ödev takibi") kullanımı:**

- Title: ✅
- H1: ✅
- Meta description: ✅
- Body text: 3-5 kez natural şekilde
- Alt text: 1-2 kez

**WHY low density:**

- Keyword stuffing penalty
- Readability > SEO tricks

---

### Content Length

**Minimum:** 300-500 kelime (landing page için yeterli)
**Optimal:** 1000+ kelime (blog posts için)

**Current landing page:** ~800 kelime (all sections combined)

**WHY:**

- Google long-form content'i tercih ediyor
- More content = More keyword opportunities
- Better user experience (detailed info)

---

### Content Freshness

**Update Frequency:** Landing page için 3-6 ayda bir

**Update Triggers:**

- Yeni özellik eklendiğinde
- User feedback'e göre content değişikliği
- Seasonal updates (ör: "2025 için en iyi ödev uygulaması")

**WHY:**

- Google fresh content'i tercih ediyor
- Evergreen content > Dated content

---

## Competitor Analysis

### Target Competitors

1. Ödev takip uygulamaları (Türkiye)
2. Eğitim teknolojileri (EdTech)
3. Parenting tools

**Analyze:**

- Hangi keywords'leri hedefliyorlar?
- Meta descriptions nasıl?
- Content structure nasıl?
- Backlink profili nasıl?

**Tools:**

- Ahrefs (keyword research)
- SEMrush (competitor analysis)
- Google Search Console (performance tracking)

---

## Backlink Strategy (Future)

### Quality Backlinks

**Target Sites:**

- Eğitim blogları
- Parenting websites
- Teknoloji haberleri
- Öğretmen forumları

**Tactics:**

- Guest posting
- Product reviews
- Resource page links
- Social media shares

**WHY backlinks:**

- Google ranking factor #1
- Trust signal
- Referral traffic

---

## Social Media Integration (Indirect SEO)

### Social Signals

**Platforms:**

- Twitter/X (tech-savvy parents)
- Instagram (visual content)
- LinkedIn (professional parents, educators)
- Facebook (parent groups)

**Share Buttons:** Landing page'de ekle (footer'da)

**WHY:**

- Social shares = indirect SEO benefit
- Brand awareness
- Referral traffic

---

## Monitoring & Reporting

### Weekly Checks

- [ ] Google Search Console (clicks, impressions)
- [ ] Google Analytics (traffic, bounce rate)
- [ ] Page speed (PageSpeed Insights)

### Monthly Checks

- [ ] Keyword rankings (Ahrefs, SEMrush)
- [ ] Backlink profile
- [ ] Competitor analysis

### Quarterly Checks

- [ ] Content update needed?
- [ ] New features to add?
- [ ] SEO strategy adjustment?

---

## SEO Checklist (Pre-Launch)

### On-Page SEO

- [ ] Title tag optimized (60-70 chars)
- [ ] Meta description optimized (150-160 chars)
- [ ] H1 sadece bir tane, keyword içeriyor
- [ ] Heading hierarchy doğru (H1 → H2 → H3)
- [ ] Alt texts tüm imagelerde
- [ ] Internal links descriptive anchor text ile
- [ ] URL structure clean (lowercase, hyphenated)
- [ ] Canonical tag var
- [ ] Robots meta tag var

### Technical SEO

- [ ] Mobile-friendly (responsive design)
- [ ] Page speed < 3 seconds
- [ ] HTTPS enabled (SSL certificate)
- [ ] Structured data (JSON-LD) ekli
- [ ] XML sitemap (gelecekte)
- [ ] Robots.txt (gelecekte)
- [ ] 404 page (gelecekte)

### Off-Page SEO (Post-Launch)

- [ ] Google Search Console setup
- [ ] Google Analytics setup
- [ ] Social media profiles oluştur
- [ ] Backlink strategy başlat

---

## Expected Results Timeline

### Month 1-3 (Initial Indexing)

- Google index'e girme
- Branded searches görünme ("ÖdevCim")
- ~100-500 organic visitors/month

### Month 4-6 (Ranking Growth)

- Long-tail keywords için ilk sayfa
- ~500-1000 organic visitors/month
- Domain authority artışı (backlinks ile)

### Month 7-12 (Established Presence)

- Primary keywords için top 10
- ~1000-5000 organic visitors/month
- Featured snippets (potential)

**WHY realistic timeline:**

- SEO takes time (6-12 months typical)
- Competition level dependent
- Content quality + backlinks = success

---

## Tools & Resources

### Free Tools

- **Google Search Console** - Performance tracking
- **Google Analytics 4** - Traffic analysis
- **Google PageSpeed Insights** - Speed testing
- **Mobile-Friendly Test** - Mobile optimization
- **Rich Results Test** - Structured data validation

### Paid Tools (Optional)

- **Ahrefs** ($99/month) - Keyword research, backlinks
- **SEMrush** ($119/month) - Competitor analysis
- **Screaming Frog** (Free up to 500 URLs) - Technical SEO audit

---

## Common SEO Mistakes to Avoid

### ❌ Don't Do

- Keyword stuffing (unnatural keyword usage)
- Hidden text (white text on white background)
- Duplicate content (copy-paste from other sites)
- Paid backlinks (Google penalty)
- Slow page load (> 5 seconds)
- Mobile-unfriendly design
- Broken links (404 errors)
- Missing alt texts
- Generic meta descriptions ("Welcome to our site")

### ✅ Do

- Natural keyword usage (readability first)
- Original, valuable content
- Quality backlinks (editorial, earned)
- Fast page load (< 3 seconds)
- Responsive design
- Fix broken links immediately
- Descriptive alt texts
- Unique, compelling meta descriptions
