# AWD Website Build Specification
## For Cursor AI Development

---

## PROJECT OVERVIEW

**Company:** Affordable Web Designer (AWD)  
**Purpose:** Marketing website showcasing AWD's value proposition - delivering high-profile business solutions at a fraction of traditional development costs.

**Core Message:** Where traditional development required entire IT teams (business analysts, database designers, programmers) costing tens of thousands of dollars, AWD leverages modern technology to streamline development to just a few resources with quick time-to-market.

---

## TECH STACK

- **Framework:** Astro
- **Styling:** Tailwind CSS
- **Deployment:** Netlify/Vercel (static)
- **Icons/Emoji:** Native emoji + Lucide icons (optional)

---

## DESIGN SYSTEM

### Color Palette

```css
/* Dark Blue Gradient Hues - Primary */
--blue-900: #1a365d;
--blue-800: #1e4175;
--blue-700: #2c5282;
--blue-600: #2b6cb0;
--blue-500: #3182ce;

/* Gold Accents */
--gold-600: #d69e2e;
--gold-500: #ecc94b;
--gold-400: #f6e05e;

/* Neutrals */
--white: #ffffff;
--gray-100: #f7fafc;
--gray-200: #edf2f7;
--gray-800: #1a202c;
--gray-900: #171923;
```

### Tailwind Config Additions
```javascript
// tailwind.config.mjs
colors: {
  primary: {
    900: '#1a365d',
    800: '#1e4175',
    700: '#2c5282',
    600: '#2b6cb0',
    500: '#3182ce',
  },
  gold: {
    600: '#d69e2e',
    500: '#ecc94b',
    400: '#f6e05e',
  }
}
```

### Typography
- **Headings:** Inter or Poppins (sans-serif), bold weights
- **Body:** Inter or Poppins, regular weight
- **Font import:** Google Fonts

### Theme Support
- Light mode: Light backgrounds, dark blue text, gold accents
- Dark mode: Dark blue backgrounds (#1a365d → #171923), white/light text, gold accents
- Toggle switch in header
- Respect system preference by default

### Visual Effects
- Gradient backgrounds (dark blue hues)
- Hover effects on buttons, cards, links
- Smooth transitions (300ms ease)
- Subtle animations on scroll (optional)
- Generous emoji use throughout 🚀💼✨💎🤝🔧📊

---

## SITE STRUCTURE

```
/
├── index.astro (Home)
├── services.astro
├── case-studies/
│   ├── index.astro (Case Studies listing)
│   ├── lake-country-fruit.astro
│   └── community-wellness.astro
├── about.astro
└── contact.astro
```

---

## COMPONENT REQUIREMENTS

### Layout Components

**Header (`components/Header.astro`)**
- AWD logo/text logo with tagline
- Navigation: Home | Services | Case Studies | About | Contact
- Dark/Light mode toggle (sun/moon icons)
- Mobile: Hamburger menu
- Sticky on scroll (optional)

**Footer (`components/Footer.astro`)**
- Navigation links (mirror main nav)
- Contact info
- Social media links (placeholder)
- "© 2025 Affordable Web Designers. All Rights Reserved."
- Privacy Policy | Terms of Service links (placeholder)

### Reusable Components

**Button (`components/Button.astro`)**
- Primary: Gold background, dark text
- Secondary: Transparent with gold border
- Hover: Scale slightly, brightness change

**Card (`components/Card.astro`)**
- For services, case studies
- Hover: Lift effect (shadow + translateY)
- Support for icon/emoji, title, description

**SectionHeading (`components/SectionHeading.astro`)**
- Consistent heading style with optional emoji
- Gradient underline accent

**TestimonialCard (`components/TestimonialCard.astro`)**
- Quote text
- Attribution
- Optional company/industry tag

**StatCard (`components/StatCard.astro`)**
- Large number/value
- Label
- Optional emoji

---

## PAGE SPECIFICATIONS

### Home Page (`index.astro`)

**Hero Section**
- Headline: "High-Profile Business Solutions at a Fraction of the Cost" (or similar)
- Subheadline: Brief value proposition about streamlined development
- CTA buttons: "View Our Work" | "Get a Free Quote"
- Background: Dark blue gradient
- Optional: Subtle animated shapes or particles

**Problem/Solution Section**
- Traditional vs AWD comparison
- Use stats/icons:
  - Traditional: 5-10+ team members, months of development, $50K-$200K+
  - AWD: 1-3 resources, weeks to launch, fraction of the cost

**Services Overview**
- Grid of service cards with emoji icons:
  - 🌐 Custom Web Applications
  - ⚙️ Business Process Automation
  - 🗄️ Data Management Systems
  - 📊 Reporting & Analytics
  - 🔗 Integration Services
- "Learn More" link to services page

**Featured Case Studies**
- 2 cards highlighting:
  - 🍎 Lake Country Fruit Storage
  - 🏥 Community Wellness Center
- Brief description + "Read Case Study" link

**Why Choose AWD**
- Feature highlights with emoji:
  - ✨ Cost Savings
  - 🚀 Speed to Market
  - 💎 Quality Solutions
  - 🤝 Personal Service
  - 🔧 Modern Technology
  - 📊 Data-Driven Results

**CTA Section**
- "Ready to Transform Your Business?"
- Contact button
- Gold accent background or gradient

---

### Services Page (`services.astro`)

**Hero**
- Title: "Our Services"
- Brief intro paragraph

**Service Sections** (alternating layout left/right)

1. **Custom Web Applications** 🌐
   - Full-stack responsive solutions
   - Modern frameworks (React, Blazor, .NET)
   - Mobile-first design

2. **Business Process Automation** ⚙️
   - Workflow optimization
   - Digital transformation
   - Reduce manual labor and errors

3. **Data Management Systems** 🗄️
   - Database design and architecture
   - Migration from legacy systems (Access → SQL Server)
   - Scalable solutions

4. **Reporting & Analytics** 📊
   - Transform raw data into insights
   - Natural language query interfaces
   - Custom dashboards and reports

5. **Integration Services** 🔗
   - Connect disparate systems
   - API development
   - Seamless data flow

**CTA Section**
- "Let's Discuss Your Project"

---

### Case Studies Index (`case-studies/index.astro`)

**Hero**
- Title: "Case Studies"
- Intro: "See how we've helped businesses transform their operations"

**Case Study Cards**
- Lake Country Fruit Storage
  - Industry: Agricultural Warehousing
  - Emoji: 🍎
  - Brief summary
  
- Community Wellness Center
  - Industry: Healthcare & Fitness
  - Emoji: 🏥
  - Brief summary

---

### Lake Country Fruit Storage (`case-studies/lake-country-fruit.astro`)

**Content:**
- **Industry:** Agricultural Warehousing & Distribution
- **Location:** Western New York Fruit Belt
- **Challenge:** Replace extensive MS Access database without business interruption

**Solution Highlights:**
- Microsoft .NET + SQL Server + Crystal Reports
- Receiving & inventory management with climate-controlled tracking
- Tagging and precise warehouse location assignment
- Advanced search for quick batch identification
- Complete sales workflow: Receipt → Bill of Lading → Picking → Bill of Sale
- Quality monitoring and testing features

**Results:**
- ✅ Seamless Access to SQL Server migration
- ✅ Zero business interruption
- ✅ Reduced manual labor and errors
- ✅ Enhanced customer satisfaction
- ✅ System remains critical to operations years later

**Quote:**
> "This application marks a significant advancement in the agricultural sector... demonstrating the impactful role that targeted software development can play in addressing industry-specific challenges."

---

### Community Wellness Center (`case-studies/community-wellness.astro`)

**Content:**
- **Industry:** Healthcare & Fitness Services
- **Challenge:** Transform simple attendance tracking into actionable business intelligence

**Original Scope:** Basic check-in/check-out tracking

**Solution Delivered:**
- Natural language query interface (ask questions in plain English)
- Automated schedule reporting and variance analysis
- Member engagement tracking and trends
- Program utilization analytics
- Staff scheduling optimization

**Information Goldmine Features:**
- 📈 Predictive Analytics - Identify at-risk members
- 🎯 Program Optimization - Data-driven insights
- 📅 Capacity Planning - Peak usage patterns
- 🗺️ Member Journey Mapping - Trial to long-term
- 💰 Revenue Attribution - Connect attendance to outcomes

**Results:**
- ✅ Turned raw data into strategic intelligence
- ✅ Enabled proactive member retention
- ✅ Instant answers to complex questions
- ✅ Reporting time reduced from hours to seconds

**Quote:**
> "We asked for attendance tracking. AWD delivered an information goldmine that transformed how we understand and serve our members."

---

### About Page (`about.astro`)

**Hero**
- Title: "About Affordable Web Designer"

**Our Story/Mission**
- Democratizing professional-grade business solutions
- Making enterprise-level technology accessible and affordable

**The AWD Difference**
- Traditional development comparison table
- AI-assisted development approach
- Direct communication, no bureaucracy
- Value-based pricing

**Technology Philosophy**
- Modern frameworks and tools
- Cloud-native architecture
- Focus on maintainability and scalability

---

### Contact Page (`contact.astro`)

**Hero**
- Title: "Let's Build Something Great"
- Subheadline: "Get a free consultation for your project"

**Contact Form**
- Name (required)
- Email (required)
- Company (optional)
- Project Type (dropdown):
  - Web Application
  - Business Automation
  - Data Management
  - Reporting & Analytics
  - Integration
  - Other
- Message (textarea, required)
- Submit button

**Direct Contact Info**
- Email: [placeholder]
- Phone: [placeholder]
- Response time: "We typically respond within 24 hours"

**FAQ Section (collapsible)**
- "How much does a project cost?"
- "How long does development take?"
- "What technologies do you use?"
- "Do you provide ongoing support?"

---

## RESPONSIVE BREAKPOINTS

```css
/* Mobile first */
sm: 640px
md: 768px
lg: 1024px
xl: 1280px
```

**Mobile (<768px):**
- Hamburger navigation
- Single column layouts
- Stacked cards
- Larger touch targets

**Tablet (768px - 1023px):**
- 2-column grids
- Condensed navigation

**Desktop (1024px+):**
- Full navigation
- Multi-column layouts
- Side-by-side content sections

---

## DARK/LIGHT MODE IMPLEMENTATION

```javascript
// Check system preference and localStorage
const theme = localStorage.getItem('theme') || 
  (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');

// Apply theme
document.documentElement.classList.toggle('dark', theme === 'dark');

// Toggle function
function toggleTheme() {
  const isDark = document.documentElement.classList.toggle('dark');
  localStorage.setItem('theme', isDark ? 'dark' : 'light');
}
```

---

## SEO REQUIREMENTS

Each page needs:
- Unique `<title>` tag
- Meta description
- Open Graph tags (og:title, og:description, og:image)
- Canonical URL
- Semantic HTML (header, main, footer, article, section)

---

## PERFORMANCE TARGETS

- Lighthouse Performance: 95+
- Lighthouse Accessibility: 95+
- Lighthouse SEO: 95+
- First Contentful Paint: < 1.5s
- Largest Contentful Paint: < 2.5s

---

## FILE NAMING CONVENTIONS

- Components: PascalCase (`Header.astro`, `Button.astro`)
- Pages: kebab-case (`case-studies.astro`, `lake-country-fruit.astro`)
- Styles: kebab-case (`global.css`)
- Assets: kebab-case (`hero-bg.jpg`)

---

## EMOJI REFERENCE

Use these consistently throughout:
- 🚀 Speed/Launch
- 💼 Business
- ✨ Quality/Premium
- 💎 Value
- 🤝 Partnership/Service
- 🔧 Technology/Tools
- 📊 Data/Analytics
- 🌐 Web
- ⚙️ Automation
- 🗄️ Database
- 🔗 Integration
- 🍎 Lake Country (fruit/agriculture)
- 🏥 Community Wellness (healthcare)
- ✅ Success/Checkmark
- 📈 Growth
- 🎯 Target/Goals
- 💰 Cost/Revenue

---

## NOTES FOR CURSOR AI

1. **Start with:** Layout components (Header, Footer), then base styles, then pages
2. **Tailwind:** Use `@apply` sparingly, prefer utility classes
3. **Dark mode:** Use Tailwind's `dark:` variant
4. **Gradients:** `bg-gradient-to-r from-primary-900 to-primary-700`
5. **Gold accents:** Use for CTAs, highlights, hover states
6. **Transitions:** `transition-all duration-300 ease-in-out`
7. **Hover effects:** `hover:scale-105 hover:shadow-lg`
8. **Test both themes** as you build each component

---

## QUICK START COMMANDS

```bash
# Create project
npm create astro@latest awd-website
cd awd-website

# Add Tailwind
npx astro add tailwind

# Install fonts (optional)
npm install @fontsource/inter @fontsource/poppins

# Run dev server
npm run dev
```

---

**End of Specification**
