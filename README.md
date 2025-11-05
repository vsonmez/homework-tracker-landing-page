# ÖdevCim Landing Page

**Multi-page** landing website for ÖdevCim - a gamified homework tracking Progressive Web App for children and parents.

---

## 🎯 Project Overview

ÖdevCim is an educational application that transforms homework tracking into an engaging, gamified experience. This repository contains the marketing website with multiple pages showcasing features, how it works, privacy policy, and more.

**Live Site**: [TBD - Production URL]
**Staging**: [TBD - Staging URL]

---

## 🚀 Quick Start

### Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools required (static HTML/CSS/JS)

### Local Development

```bash
# Clone the repository
git clone https://github.com/[username]/odevcim-landing.git

# Navigate to project directory
cd odevcim-landing

# Open in browser
# Option 1: Double-click index.html
# Option 2: Use a local server (recommended)
python -m http.server 8000
# or
npx serve
```

Visit `http://localhost:8000` in your browser.

---

## 📁 Project Structure

```
odevcim-landing/
├── index.html              # Home page
├── ozellikler.html         # Features page
├── nasil-calisir.html      # How it works
├── hakkimizda.html         # About us
├── gizlilik.html           # Privacy policy
├── kullanim-sartlari.html  # Terms of service
├── iletisim.html           # Contact form
├── sss.html                # FAQ
├── css/
│   ├── styles.css          # Global styles
│   └── pages/              # Page-specific styles
├── js/
│   ├── main.js             # Global JS
│   ├── navigation.js       # Header/nav logic
│   └── contact-form.js     # Form validation
├── images/                 # All images
├── docs/                   # Project documentation
├── sitemap.xml             # SEO sitemap
└── robots.txt              # SEO robots file
```

See `docs/FILE_STRUCTURE_MULTIPAGE.md` for detailed structure.

---

## 🛠 Tech Stack

- **HTML5**: Semantic markup, accessibility-first
- **CSS3**: Custom properties (CSS variables), Flexbox, Grid
- **TailwindCSS**: Utility-first CSS framework (v3.4+ via CDN)
- **Vanilla JavaScript**: Minimal, progressive enhancement
- **Google Fonts**: Inter font family

**No frameworks, no build process, no dependencies.**

---

## 📚 Documentation

All project documentation is in the `/docs` folder:

| File                             | Purpose                                     |
| -------------------------------- | ------------------------------------------- |
| **FILE_STRUCTURE_MULTIPAGE.md**  | ✅ Active: Multi-page structure             |
| **PROJECT_CONTEXT.md**           | Project overview, context, goals            |
| **LANDING_PAGE_REQUIREMENTS.md** | Detailed page requirements                  |
| **CONTENT_COPY.md**              | All text content, SEO metadata              |
| **DESIGN_SYSTEM.md**             | Design tokens, color palette, typography    |
| **IMPLEMENTATION_CHECKLIST.md**  | Step-by-step implementation guide           |
| **SEO_REQUIREMENTS.md**          | SEO strategy, meta tags, structured data    |
| FILE_STRUCTURE.md                | Deprecated: Single-page version (reference) |

---

## 🎨 Design System

**Color Palette:**

- Primary: `#3B82F6` (Blue 500)
- Secondary: `#F59E0B` (Amber 500)
- Success: `#10B981` (Green 500)
- Background: `#F9FAFB` (Gray 50)

**Typography:**

- Font: Inter (Google Fonts)
- Base size: 16px
- Scale: 1.125 ratio

**Spacing:**

- Base unit: 4px
- Scale: 4, 8, 12, 16, 24, 32, 48, 64, 80px

See `docs/DESIGN_SYSTEM.md` for complete design tokens.

---

## 🌐 Pages

### index.html - Home Page

**Purpose**: First impression, value proposition, primary CTA

**Sections**:

- Hero (compressed)
- Problem Statement (3 cards)
- Solution Overview (4 features)
- Final CTA

---

### ozellikler.html - Features Page

**Purpose**: Detailed feature showcase

**Sections**:

- Gamification system (points, badges, streaks)
- Smart reminders
- Offline capability
- Privacy-focused architecture

---

### nasil-calisir.html - How It Works

**Purpose**: Step-by-step onboarding guide

**Sections**:

- 3-step process
- Screenshots/demos
- Common questions

---

### hakkimizda.html - About Us

**Purpose**: Brand story, mission, values

**Content**:

- Mission statement
- Team (future)
- Values & principles

---

### gizlilik.html - Privacy Policy

**Purpose**: Legal requirement, GDPR compliance

**Content**:

- Data collection
- Data usage
- User rights
- localStorage explanation

---

### kullanim-sartlari.html - Terms of Service

**Purpose**: Legal protection

**Content**:

- Service scope
- User responsibilities
- Liability disclaimer

---

### iletisim.html - Contact

**Purpose**: User inquiries, support

**Content**:

- Contact form (name, email, subject, message)
- Email: iletisim@odevcim.com

---

### sss.html - FAQ

**Purpose**: Common questions, reduce support load

**Content**:

- General questions
- Technical questions
- Privacy & security
- Pricing

---

## 🔍 SEO Strategy

### Target Keywords

- ödev takibi
- çocuk ödevi
- ödev hatırlatıcı
- oyunlaştırma eğitim
- ücretsiz ödev uygulaması

### Meta Tags

All pages include:

- Title tag (60-70 chars)
- Meta description (150-160 chars)
- Open Graph tags (Facebook, LinkedIn)
- Twitter Card tags
- Canonical URL

### Structured Data

- Organization schema
- WebSite schema
- SoftwareApplication schema
- Breadcrumb schema (on sub-pages)

See `docs/SEO_REQUIREMENTS.md` for complete SEO strategy.

---

## 📱 Responsive Design

**Breakpoints:**

- Mobile: `< 640px` (base styles)
- Tablet: `640px - 1024px`
- Desktop: `> 1024px`

**Approach**: Mobile-first, progressive enhancement

---

## ♿ Accessibility

**Standards**: WCAG 2.1 AA compliance

**Features:**

- Semantic HTML5 tags
- ARIA labels on sections
- Alt text on all images
- Keyboard navigation support
- Color contrast ratio > 4.5:1
- Focus states visible
- Skip to main content link

**Testing**: VoiceOver (Mac), NVDA (Windows), Lighthouse

---

## 🚀 Deployment

### Vercel (Recommended)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Production deployment
vercel --prod
```

**Configuration**: `vercel.json` included in root

---

### Netlify (Alternative)

```bash
# Install Netlify CLI
npm i -g netlify-cli

# Deploy
netlify deploy

# Production deployment
netlify deploy --prod
```

**Configuration**: `netlify.toml` included in root

---

### Manual Deployment

1. Upload all files to web server
2. Ensure `.html` extension removal works (or configure redirects)
3. Verify HTTPS is enabled
4. Test all pages load correctly

---

## 🧪 Testing

### Pre-Launch Checklist

**Functionality:**

- [ ] All pages load without errors
- [ ] Navigation works (header links)
- [ ] CTA buttons have correct hrefs
- [ ] Forms validate properly (contact form)
- [ ] Mobile menu toggles correctly

**Performance:**

- [ ] Lighthouse score > 90 (all metrics)
- [ ] Images compressed (< 200KB each)
- [ ] CSS/JS minified (production)
- [ ] Page load < 3 seconds

**SEO:**

- [ ] All meta tags present
- [ ] Sitemap.xml accessible
- [ ] Robots.txt configured
- [ ] Structured data validated (Google Rich Results Test)

**Accessibility:**

- [ ] Keyboard navigation works
- [ ] Screen reader compatible
- [ ] Color contrast sufficient
- [ ] Alt texts descriptive

**Cross-Browser:**

- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)

**Responsive:**

- [ ] Mobile (375px width)
- [ ] Tablet (768px width)
- [ ] Desktop (1440px width)

---

## 📊 Analytics

### Google Analytics 4 (GA4)

**Setup:**

1. Create GA4 property
2. Add tracking code to all pages
3. Configure events:
   - CTA button clicks
   - Form submissions
   - Scroll depth
   - Outbound links

**Tracking ID**: `G-XXXXXXXXXX` (add to all pages)

---

### Google Search Console

**Setup:**

1. Add property: `https://odevcim.com`
2. Verify ownership (HTML file or meta tag)
3. Submit sitemap: `https://odevcim.com/sitemap.xml`
4. Monitor performance

---

## 🔧 Development Guidelines

### Code Standards

**Naming Conventions:**

- CSS classes: `kebab-case` (`.hero-title`)
- IDs: `kebab-case` (`#how-it-works`)
- JavaScript: `camelCase` (`handleClick`)
- Files: `kebab-case` (`nasil-calisir.html`)

**Forbidden:**

- ❌ `else` statements (use guard clauses)
- ❌ Magic numbers (use CSS variables)
- ❌ Generic identifiers (`i`, `temp`, `data`)
- ❌ `innerHTML` for HTML generation

**Required:**

- ✅ "WHY" comments (explain reasoning)
- ✅ Semantic HTML
- ✅ Descriptive names
- ✅ Positive conditionals (`isReady`, not `isNotReady`)

See `docs/PROJECT_CONTEXT.md` for complete coding standards.

---

### Commit Convention

**Format**: `type: short description`

**Types:**

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Code formatting
- `refactor:` Code restructuring
- `perf:` Performance improvement
- `chore:` Maintenance

**Examples:**

```
feat: add contact form validation
fix: correct footer link URLs
docs: update README with deployment steps
style: format CSS with consistent spacing
perf: compress hero image from 500KB to 180KB
```

---

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'feat: add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

**Before submitting PR:**

- [ ] Code follows style guide
- [ ] All pages tested locally
- [ ] No console errors
- [ ] Accessibility tested
- [ ] Documentation updated

---

## 📞 Contact

**Project Lead**: [Your Name]
**Email**: iletisim@odevcim.com
**Website**: https://odevcim.com

**Issues**: Please report bugs and feature requests via [GitHub Issues](https://github.com/[username]/odevcim-landing/issues)

---

## 📄 License

This project is proprietary and confidential.
© 2025 ÖdevCim. All rights reserved.

---

## 🗺 Roadmap

### Phase 1 (Current) - MVP Launch

- [x] Multi-page structure
- [x] Core pages (Home, Features, How It Works)
- [x] Contact form
- [x] Privacy policy & Terms
- [ ] FAQ page
- [ ] Production deployment

### Phase 2 - Enhancement

- [ ] Video demo (nasil-calisir.html)
- [ ] Blog section
- [ ] User testimonials
- [ ] A/B testing setup

### Phase 3 - Optimization

- [ ] Advanced analytics
- [ ] Conversion funnel optimization
- [ ] Multilingual support (English)
- [ ] Advanced SEO (backlink strategy)

---

## 🙏 Acknowledgments

- **Design inspiration**: Modern SaaS landing pages
- **Icons**: Emoji (built-in, no dependencies)
- **Fonts**: Google Fonts (Inter)
- **CSS Framework**: TailwindCSS (via CDN)

---

## 📝 Notes

### Why Multi-Page?

Previously single-page, switched to multi-page for:

1. **Better SEO**: Individual page optimization
2. **Easier navigation**: Dedicated pages for features
3. **Scalability**: Easy to add blog, testimonials
4. **Load performance**: Smaller initial payload
5. **User experience**: Clear information architecture

### Why No Build Process?

- **Simplicity**: Anyone can contribute
- **Fast deployment**: Push and deploy
- **No dependencies**: Works everywhere
- **Easy debugging**: View source shows actual code
- **Progressive enhancement**: Works without JS

---

**Built with ❤️ for Turkish families**
