# Landing Page Requirements

## Genel Gereksinimler

### Sayfa Amacı

Ebeveynlere ÖdevCim'i tanıtmak, uygulamanın değer önerisini net bir şekilde iletmek ve ücretsiz deneme için ana uygulamaya yönlendirmek.

### Ana Mesajlar (Hierarchical)

1. **Primary**: "Ödev takibi artık kolay ve eğlenceli" → Problem çözümü vurgusu
2. **Secondary**: "Çocuğunuz oyunlaştırma ile motive oluyor" → Gamification özelliği
3. **Tertiary**: "Verileriniz güvende, tamamen ücretsiz" → Güven ve değer

### Hedef Davranış

- **Primary CTA**: "Ücretsiz Dene" butonuna tıklayıp ana uygulamaya geçiş
- **Secondary CTA**: "Nasıl Çalışır?" ile aşağı scroll veya demo video izleme

---

## Sayfa Yapısı (Section-by-Section)

### A) Hero Section

**Hedef**: İlk 3 saniyede ziyaretçinin dikkatini çekmek ve değer önerisini iletmek.

**Başlık (H1)**

```
Çocuğunuzun Ödevlerini Oyuna Çevirin
```

**Alt Başlık (Subtitle)**

```
ÖdevCim ile çocuğunuz ödevlerini zamanında tamamlıyor, puan kazanıyor ve eğlenerek öğreniyor. Ücretsiz, reklamsız, tamamen sizin kontrolünüzde.
```

**CTA Butonları**

- **Primary Button**: "Ücretsiz Dene"
  - Renk: Primary (mavi)
  - Action: Ana uygulamaya yönlendir
  - Position: Sol tarafta, büyük ve vurgulu
- **Secondary Button**: "Nasıl Çalışır?"
  - Renk: Transparent border (outline)
  - Action: #how-it-works section'ına smooth scroll
  - Position: Primary butonun sağında

**Görsel**

- **Position**: Sağ tarafta (desktop), altında (mobile)
- **Content**: Telefon mockup görseli
  - Ekranda görünen: Task listesi + tamamlanmış ödevler + rozet bildirimi
  - Format: PNG veya WebP
  - Boyut: Max 500KB
- **Alt text**: "ÖdevCim uygulaması ekran görüntüsü - ödev listesi ve rozetler"

**Layout**

- Desktop: 2 column (text sol 50%, image sağ 50%)
- Mobile: Single column (text üstte, image altta)
- Background: Gradient (açık mavi → beyaz)

**WHY bu içerik:**

- "Oyuna çevirin" → Gamification'ı öne çıkarır, ilgi çeker
- "Zamanında tamamlıyor" → Ana ağrı noktasını çözer
- "Ücretsiz, reklamsız" → İlk güveni sağlar
- Telefon mockup → Ürünü somutlaştırır, "gerçek uygulama" hissi verir

---

### B) Problem Statement Section

**Hedef**: Hedef kitleyle empati kurmak, ağrı noktalarını vurgulamak.

**Başlık (H2)**

```
Bu Sorunlar Size Tanıdık Geliyor mu?
```

**3 Problem Kartı** (Grid: 3 columns desktop, 1 column mobile)

#### Problem 1

**Icon**: 📚 (emoji, büyük boyut)
**Başlık**: "Hangi ödevler vardı?"
**Açıklama**:

```
Çocuk defterini kontrol etmiyorsunuz, hangi ödevlerin olduğunu bilmiyorsunuz. Son gün panik oluyor.
```

#### Problem 2

**Icon**: ⏰
**Başlık**: "Son gün ödev stresine son"
**Açıklama**:

```
Teslim tarihleri unutuluyor, ödevler geç teslim ediliyor. Notlar düşüyor, çocuk strese giriyor.
```

#### Problem 3

**Icon**: 🎮
**Başlık**: "Motivasyon sorunu"
**Açıklama**:

```
Çocuk ödevi sıkıcı buluyor, yapmak için sürekli ikna gerekiyor. Ödev zamanı kavgaya dönüşüyor.
```

**Card Styling**

- Background: Beyaz kart
- Border: Yok veya çok ince gri
- Shadow: Hafif (hover'da daha belirgin)
- Padding: 32px
- Border radius: 16px
- Hover effect: Hafif yukarı hareket (translateY)

**WHY bu problemler:**

- Hedef kitlenin gerçek ağrı noktaları (araştırma/empati bazlı)
- 3 kart = Okumayı kolaylaştırır, overwhelming olmaz
- Emoji kullanımı = Hızlı tanıma, friendly hissi

---

### C) Solution Overview Section

**Hedef**: ÖdevCim'in nasıl problem çözdüğünü göstermek.

**Başlık (H2)**

```
ÖdevCim ile Ödev Takibi Artık Eğlenceli
```

**4 Özellik Kartı** (Grid: 2x2 desktop, 1 column mobile)

#### Özellik 1

**Icon**: ✅
**Başlık**: Tüm Ödevler Tek Yerde
**Açıklama**:

```
Çocuğunuzun tüm ödevlerini ekleyin, derse ve konuya göre organize edin. Teslim tarihlerini girin, hangi ödevler yaklaşıyor hemen görün.
```

#### Özellik 2

**Icon**: 🔔
**Başlık**: Akıllı Hatırlatıcılar
**Açıklama**:

```
Her gün saat 18:00'de push notification ile hatırlatma. "Yarın 2 ödevin teslim tarihi!" gibi akıllı bildirimler.
```

#### Özellik 3

**Icon**: 🎯
**Başlık**: Oyunlaştırma Sistemi
**Açıklama**:

```
Her ödev tamamlandığında puan kazanın. Rozetler, seviyeler ve seri sistemleri ile çocuğunuzu motive edin. Proje, yazılı, etkinlik gibi kategorilerde özel rozetler.
```

#### Özellik 4

**Icon**: 📱
**Başlık**: Offline Çalışır, Veri Güvenli
**Açıklama**:

```
İnternet olmadan çalışır, veriler cihazınızda kalır. Hiçbir bilginiz sunucularımıza gönderilmez. PWA teknolojisi sayesinde uygulama gibi kullanın, indirme gerektirmez.
```

**Card Styling**

- Background: Beyaz kart
- Icon: Büyük emoji (48px), üstte ortalı
- Title: Bold, 20px
- Description: Normal, 16px, açık gri
- Padding: 32px
- Border radius: 16px
- Hover effect: Hafif shadow artışı + yukarı hareket

**WHY bu özellikler:**

- Problem statement'taki her soruna doğrudan çözüm sunuyor
- Teknik değil, fayda odaklı dil ("localStorage" yok, "veriler güvende" var)
- 4 özellik = Dengeli, overwhelming değil

---

### D) How It Works Section

**Hedef**: Başlamanın ne kadar kolay olduğunu göstermek.

**Başlık (H2)**

```
3 Adımda Başlayın
```

**3 Step Card** (Horizontal timeline desktop, vertical mobile)

#### Adım 1

**Numara**: 1️⃣ (büyük, vurgulu)
**Başlık**: Çocuğunuzu Ekleyin
**Açıklama**:

```
İsim ve sınıf bilgisini girin. Sadece 5 saniye sürer.
```

**Görsel** (Opsiyonel): Mini screenshot - çocuk ekleme formu

#### Adım 2

**Numara**: 2️⃣
**Başlık**: Ödevleri Ekleyin
**Açıklama**:

```
Ders, konu, teslim tarihi ve ödev türünü belirtin. Örnek: "Matematik - Çarpma İşlemleri - Yazılı - 10 Kasım"
```

**Görsel** (Opsiyonel): Mini screenshot - ödev ekleme formu

#### Adım 3

**Numara**: 3️⃣
**Başlık**: Çocuğunuz Tamamlasın, Rozetleri Kazansın
**Açıklama**:

```
Her ödev tamamlandıkça puan ve rozet kazanın. İlerlemeyi birlikte takip edin, başarıları kutlayın.
```

**Görsel** (Opsiyonel): Mini screenshot - rozet kazanma notification

**Layout**

- Desktop: Horizontal timeline (connector line between steps)
- Mobile: Vertical timeline
- Numbers: Büyük, circular badge, primary color background

**WHY bu section:**

- "3 adım" = Basitlik vurgusu, overwhelming olmaz
- Süre belirtme (5 saniye) = Güven artırır, commitment korkusunu azaltır
- Örnek vermek = Somutlaştırır, anlaşılır kılar

---

### E) Gamification Showcase Section

**Hedef**: Oyunlaştırma özelliğini detaylıca tanıtmak (ana farklılaştırıcı).

**Başlık (H2)**

```
Ödevler Artık Oyun Gibi Eğlenceli
```

**Alt Başlık**

```
ÖdevCim, çocuğunuzun her başarısını kutlar ve ödüllendirir
```

**4 Gamification Özelliği** (Grid: 2x2 desktop, 1 column mobile)

#### Özellik 1

**Icon**: 🏆
**Başlık**: Puan Sistemi
**Açıklama**:

```
Her ödev: +10 puan
Son gün teslim: +15 puan bonusu
Proje tamamlama: +30 puan (kategori bonusu)
```

**Visual detail**: Progress bar veya puan badge mockup

#### Özellik 2

**Icon**: 🔥
**Başlık**: Seri Sistemi
**Açıklama**:

```
3 gün üst üste ödev: "İlk Seri" rozeti
7 gün seri: "Haftalık Kahraman" rozeti
30 gün seri: "Efsane Çalışkan" rozeti
```

**Visual detail**: Streak badge örnekleri

#### Özellik 3

**Icon**: 🎖️
**Başlık**: Rozetler
**Açıklama**:

```
50+ farklı rozet
Kategori bazlı rozetler: "Yazılı Ustası", "Proje Şampiyonu"
Seviye rozetleri: "Acemi Öğrenci" → "Usta Öğrenci"
```

**Visual detail**: 6-8 rozet ikonunun grid görünümü

#### Özellik 4

**Icon**: 📊
**Başlık**: İlerleme Takibi
**Açıklama**:

```
Hangi kategoride ne kadar ilerledi görün
"Yazılılardan 8/10 tamamladın!" gibi progress barlar
Ebeveynler için detaylı raporlar
```

**Visual detail**: Progress bar mockup

**Card Styling**

- Background: Gradient (hafif renkli)
- Larger padding: 40px
- Daha vurgulu hover effect
- Özellik ikonları animasyonlu (opsiyonel, CSS animation)

**WHY bu section:**

- Gamification = Ana farklılaştırıcı, detaylı anlatılmalı
- Somut örnekler = "Çocuğum bunu sever" hissi yaratır
- Sayılar vermek (50+ rozet, +30 puan) = Güven ve bolluk hissi

---

### F) Privacy & Security Section

**Hedef**: Ebeveynlerin güvenlik kaygılarını gidermek.

**Başlık (H2)**

```
Verileriniz Tamamen Güvende
```

**3 Güvenlik Vaadi** (Grid: 3 columns desktop, 1 column mobile)

#### Vaat 1

**Icon**: 🔒
**Başlık**: Hiçbir Veri Sunucuya Gitmiyor
**Açıklama**:

```
Tüm veriler cihazınızda localStorage'da tutuluyor. Hiçbir kişisel bilgi, ödev detayı veya çocuk bilgisi paylaşılmıyor.
```

#### Vaat 2

**Icon**: 📱
**Başlık**: Offline Çalışır
**Açıklama**:

```
İnternet olmadan tüm özellikler kullanılabilir. Sadece push notification için internet bağlantısı gerekir.
```

#### Vaat 3

**Icon**: 🚫
**Başlık**: Reklamsız, Tamamen Ücretsiz
**Açıklama**:

```
Hiçbir reklam gösterilmez. Gizli ücret yok, tüm özellikler ücretsiz. Kredi kartı bilgisi istenmez.
```

**Card Styling**

- Background: Açık yeşil veya mavi (trust colors)
- Border: 2px solid, güvenlik vurgusu için
- Icons: Daha büyük (56px)
- Font: Bold başlıklar

**WHY bu section:**

- Ebeveynlerin en büyük kaygısı = "Çocuğumun verisi güvende mi?"
- "localStorage" yerine "cihazınızda kalır" = Teknik olmayan dil
- "Ücretsiz" vurgusu = Premium hissi, profesyonellik

---

### G) Final CTA Section

**Hedef**: Son bir kez güçlü CTA ile dönüşüm sağlamak.

**Başlık (H2)**

```
Çocuğunuzun Ödev Başarısını Şimdi Artırın
```

**Alt Başlık**

```
Kurulum 5 saniye, ilk ödev ekleme 30 saniye. Hemen deneyin, kredi kartı gerekmez.
```

**CTA Butonları**

- **Primary Button**: "Ücretsiz Başla"

  - Renk: Primary (mavi)
  - Boyut: Extra large (56px height)
  - Action: Ana uygulamaya yönlendir
  - Position: Ortalanmış, vurgulu

- **Secondary Button**: "Demo İzle"
  - Renk: Transparent outline
  - Action: Video modal veya YouTube link (gelecekte)
  - Position: Primary butonun altında

**Layout**

- Full-width section
- Background: Gradient veya solid primary color
- Text: Beyaz (high contrast)
- Centered alignment
- Large padding (80px vertical)

**WHY bu section:**

- "5 saniye kurulum" = Commitment korkusunu azaltır
- "Kredi kartı gerekmez" = Son güven artışı
- Büyük, vurgulu buton = Gözden kaçmaz

---

### H) Footer

**Layout**: 3-column desktop, stacked mobile

#### Column 1: Branding

**Logo**: ÖdevCim logo (SVG)
**Tagline**:

```
Çocukların ödev takibini eğlenceli hale getiren ücretsiz uygulama
```

#### Column 2: Linkler

- Gizlilik Politikası
- Kullanım Şartları
- İletişim
- Sık Sorulan Sorular (gelecekte)

#### Column 3: Sosyal Medya (Opsiyonel)

- Twitter/X icon + link
- Instagram icon + link
- LinkedIn icon + link

**Bottom Bar**

```
© 2025 ÖdevCim. Made with ❤️ in Turkey
```

**Footer Styling**

- Background: Koyu gri (#1F2937)
- Text: Açık gri (#9CA3AF)
- Links: Hover'da beyaz
- Padding: 48px vertical

**WHY bu footer:**

- Minimal ama gerekli bilgiler
- "Made with ❤️ in Turkey" = Yerel, samimi hissi
- Sosyal medya opsiyonel (şu an yoksa boş bırak)

---

## Responsive Davranış

### Mobile (< 640px)

- **Hero**: Single column, image altta
- **Problem cards**: Single column, stack
- **Solution cards**: Single column
- **How It Works**: Vertical timeline
- **Gamification**: Single column
- **Privacy**: Single column
- **Footer**: Single column, centered

### Tablet (640px - 1024px)

- **Hero**: 2 column maintained
- **Problem cards**: 2 columns (3. kart alta taşar)
- **Solution cards**: 2x2 grid
- **How It Works**: Horizontal timeline (compressed)
- **Gamification**: 2x2 grid
- **Privacy**: 2 columns (3. kart alta taşar)
- **Footer**: 2 columns (branding + links, sosyal altta)

### Desktop (> 1024px)

- **Full layout** yukarıda tanımlandığı gibi
- **Max-width**: 1200px container
- **Horizontal centering**: margin: 0 auto

---

## Teknik Gereksinimler

### HTML Semantic Tags

```html
<header> → Navigation (opsiyonel)
<main>
  <section id="hero"> → Hero Section
  <section id="problem"> → Problem Statement
  <section id="solution"> → Solution Overview
  <section id="how-it-works"> → How It Works
  <section id="gamification"> → Gamification Showcase
  <section id="privacy"> → Privacy & Security
  <section id="cta"> → Final CTA
</main>
<footer> → Footer
```

### Meta Tags (Required)

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta
  name="description"
  content="ÖdevCim ile çocuğunuzun ödevlerini eğlenceli hale getirin. Oyunlaştırma, rozetler ve hatırlatıcılarla ödev takibi artık kolay."
/>
<meta name="keywords" content="ödev takibi, çocuk ödevi, oyunlaştırma, eğitim uygulaması" />

<!-- Open Graph -->
<meta property="og:title" content="ÖdevCim - Çocuğunuzun Ödevlerini Oyuna Çevirin" />
<meta property="og:description" content="Ücretsiz, reklamsız ödev takip uygulaması. Rozetler, puanlar ve hatırlatıcılarla çocuğunuzu motive edin." />
<meta property="og:image" content="/images/og-image.png" />
<meta property="og:type" content="website" />

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="ÖdevCim - Ödev Takibini Eğlenceli Hale Getirin" />
<meta name="twitter:description" content="Çocuklar için gamification ile ödev takibi" />
```

### External Resources

- **TailwindCSS**: CDN (v3.4+)

```html
<script src="https://cdn.tailwindcss.com"></script>
```

- **Google Fonts**: Inter

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
```

### Accessibility

- **ARIA labels**: Tüm interactive elements için
- **Alt text**: Her image için descriptive
- **Keyboard navigation**: Tab order mantıklı, focus states görünür
- **Color contrast**: Minimum 4.5:1 (WCAG AA)
- **Heading hierarchy**: H1 > H2 > H3 (skip etme)

---

## Performans Gereksinimleri

### Image Optimization

- **Format**: WebP (fallback PNG)
- **Compression**: < 200KB per image
- **Dimensions**: Max 1920x1080 (hero), 800x600 (cards)
- **Lazy loading**: Below the fold images için

### CSS/JS

- **Inline critical CSS**: Above-the-fold styles
- **Defer non-critical JS**: Scroll animations, analytics
- **Minification**: Production build'de minify

### Loading Targets

- **FCP**: < 1.5s
- **LCP**: < 2.5s
- **CLS**: < 0.1
- **Total size**: < 1MB

---

## Dil ve Ton

### Genel Ton

- **Samimi**: "Siz de" yerine "Sen de" kullan (ama formal yerlerde "siz")
- **Sıcak**: "Çocuğunuz" yerine "Çocuğunuz" (possessive, kişisel)
- **Empatik**: "Biliyoruz", "Anlıyoruz" gibi ifadeler
- **Teknik değil**: "localStorage" değil, "cihazınızda tutuluyor"

### Kaçınılacak İfadeler

- ❌ "En iyi uygulama" (abartılı claims)
- ❌ "Devrim yaratıyor" (과장)
- ❌ "Rakipsiz" (comparison)
- ❌ "Garantili başarı" (unrealistic promises)

### Tercih Edilen İfadeler

- ✅ "Ödev takibini kolaylaştırır"
- ✅ "Çocuğunuzu motive eder"
- ✅ "Ücretsiz ve reklamsız"
- ✅ "Hemen deneyin"

---

## Öncelik Sırası (MVP)

### Phase 1 (Must-Have)

- ✅ Hero Section
- ✅ Problem Statement
- ✅ Solution Overview
- ✅ Privacy & Security
- ✅ Final CTA
- ✅ Footer

### Phase 2 (Should-Have)

- ✅ How It Works
- ✅ Gamification Showcase

### Phase 3 (Nice-to-Have)

- ❌ Video demo
- ❌ Blog section
- ❌ Social proof (testimonials)
- ❌ FAQ section
