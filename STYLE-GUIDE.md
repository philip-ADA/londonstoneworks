# London Stoneworks Style Guide

## Color Palette

### Primary Colors
| Name | Variable | Hex | Usage |
|------|----------|-----|-------|
| Navy | `--navy` | `#001640` | Primary brand color, headings, buttons |
| Navy Dark | `--navy-dark` | `#141d32` | Footer background |
| Navy Light | `--navy-light` | `#243454` | Button hover states |
| Burgundy/Red | `--red-hover` | `#b72b35` | Accent color, CTA buttons, stars |
| Burgundy Alt | - | `#9b2c3d` | Section tags, star ratings |
| Gold | `--gold` | `#c9a962` | Accent highlights, form focus |

### Neutral Colors
| Name | Variable | Hex | Usage |
|------|----------|-----|-------|
| White | `--white` | `#ffffff` | Backgrounds, text on dark |
| Gray 50 | `--gray-50` | `#f9fafb` | Card backgrounds, FAQ items |
| Gray 100 | `--gray-100` | `#f3f4f6` | Section tag backgrounds |
| Gray 200 | `--gray-200` | `#e5e7eb` | Borders, dividers |
| Gray 300 | `--gray-300` | `#d1d5db` | Secondary text on dark, borders |
| Gray 400 | `--gray-400` | `#9ca3af` | Icons, muted text |
| Gray 500 | `--gray-500` | `#6b7280` | Placeholder text |
| Gray 600 | `--gray-600` | `#4b5563` | Body text, descriptions |
| Gray 700 | `--gray-700` | `#374151` | Primary body text |

### Background Colors
| Section | Color |
|---------|-------|
| Default | `#ffffff` |
| Alternate | `#FAFAFA` |
| About Card | `#dfe3e8` |
| Hero/Contact | `#001640` (Navy) |
| Footer | `#141d32` (Navy Dark) |

---

## Typography

### Font Families
```css
--font-heading: 'League Spartan', sans-serif;
--font-serif: Georgia, 'Playfair Display', serif;
--font-sans: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
```

### Font Stack
| Element | Font Family | Size | Weight | Line Height |
|---------|-------------|------|--------|-------------|
| Body | `--font-serif` | 16px | 400 | 1.6 |
| H1 | `--font-heading` | 51px (clamp: 2rem-3rem) | 500 | 1.1-1.2 |
| H2 | `--font-heading` | clamp(1.75rem, 3vw, 2.5rem) | 500 | 1.2 |
| H3 | `--font-heading` | 1.25rem (20px) | 500 | 1.2 |
| Section Tag | `--font-heading` | 22px | 500 | - |
| Navigation | `--font-serif` | 14px | 400 | - |
| Button | `--font-serif` | 15-17px | 400 | - |
| Body Text | `--font-serif` | 16-18px | 400 | 1.6-1.8 |
| Small Text | `--font-serif` | 14-15px | 400 | 1.7 |

### Text Colors
| Context | Color |
|---------|-------|
| Headings (light bg) | `--navy` (#001640) |
| Headings (dark bg) | `--white` (#ffffff) |
| Body text | `--gray-600` or `--gray-700` |
| Body text (dark bg) | `--gray-300` |
| Links hover | `--red-hover` (#b72b35) |

---

## Spacing

### Section Padding
```css
padding: 6rem 0;  /* Standard sections */
padding: 5rem 0;  /* Features section */
```

### Container
```css
max-width: 1200px;
padding: 0 20px;
margin: 0 auto;
```

### Common Gaps
| Size | Value | Usage |
|------|-------|-------|
| XS | 0.75rem | FAQ items, small gaps |
| SM | 1rem | Grid gaps, card padding |
| MD | 1.5rem | Portfolio grid, testimonials |
| LG | 2rem | Feature grid, section margins |
| XL | 3rem | About card gap, section headers |
| XXL | 4rem | Two-column layouts |

---

## Components

### Section Tag (Pill)
```css
.section-tag {
    display: inline-block;
    font-size: 22px;
    font-family: var(--font-heading);
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--navy);
    background: var(--gray-100);
    padding: 0.5rem 1.25rem;
    border-radius: 50px;
    margin-bottom: 1rem;
}

/* Variant: Services (burgundy) */
.services .section-tag {
    background: #9b2c3d;
    color: var(--white);
}

/* Variant: Dark background */
.contact .section-tag {
    background: rgba(255, 255, 255, 0.1);
    color: var(--white);
}
```

### Buttons

#### Primary Button
```css
.btn-primary {
    display: inline-block;
    padding: 0.875rem 1.75rem;
    font-size: 0.9375rem;
    font-family: var(--font-serif);
    font-weight: 400;
    border-radius: 6px;
    background-color: var(--navy);
    color: var(--white);
    border: 2px solid var(--navy);
    cursor: pointer;
    transition: all 0.3s ease;
}

.btn-primary:hover {
    background-color: var(--navy-light);
    border-color: var(--navy-light);
}
```

#### Hero CTA Button (Pill with Arrow)
```css
.btn-hero {
    display: inline-flex;
    align-items: center;
    gap: 12px;
    background-color: rgba(255, 255, 255, 0.4);
    color: var(--white);
    font-size: 17px;
    font-family: var(--font-serif);
    padding: 9px 12px 11px 26px;
    border-radius: 50px;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.btn-hero:hover {
    background-color: var(--red-hover);
}

.btn-hero .arrow-circle {
    width: 32px;
    height: 32px;
    background-color: #b72b35;
    border-radius: 50%;
}
```

#### FAQ Button (Outline with Arrow)
```css
.btn-faq {
    display: inline-flex;
    align-items: center;
    gap: 12px;
    background-color: transparent;
    color: var(--navy);
    font-size: 16px;
    font-family: var(--font-serif);
    padding: 10px 12px 10px 20px;
    border-radius: 50px;
    border: 1px solid var(--gray-300);
    transition: all 0.3s ease;
}

.btn-faq:hover {
    background-color: var(--navy);
    color: var(--white);
    border-color: var(--navy);
}
```

### Cards

#### Testimonial Card
```css
.testimonial-card {
    background: var(--white);
    padding: 1.5rem;
    border-radius: 12px;
    border: 1px solid var(--gray-200);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
    width: 320px;
}
```

#### About Card
```css
.about-card {
    display: grid;
    grid-template-columns: 350px 1fr;
    gap: 3rem;
    align-items: center;
    background-color: #dfe3e8;
    border-radius: 12px;
    padding: 2.5rem;
}
```

#### Portfolio Card
```css
.portfolio-item {
    position: relative;
    border-radius: 12px;
    overflow: hidden;
    aspect-ratio: 4/3;
}

.portfolio-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 1.5rem;
    background: linear-gradient(transparent, rgba(0, 0, 0, 0.7));
    color: var(--white);
}
```

### Accordion

#### Services Accordion
```css
.accordion-item {
    border-bottom: 1px solid var(--gray-200);
}

.accordion-header {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.25rem 0;
    background: none;
    border: none;
    cursor: pointer;
}

.accordion-icon {
    position: relative;
    width: 20px;
    height: 20px;
}

/* Plus icon using pseudo-elements */
.accordion-icon::before,
.accordion-icon::after {
    content: '';
    position: absolute;
    background-color: var(--gray-400);
    transition: transform 0.3s ease;
}

.accordion-icon::before {
    width: 100%;
    height: 2px;
    top: 50%;
    transform: translateY(-50%);
}

.accordion-icon::after {
    width: 2px;
    height: 100%;
    left: 50%;
    transform: translateX(-50%);
}

.accordion-item.active .accordion-icon::after {
    transform: translateX(-50%) rotate(90deg);
}
```

#### FAQ Accordion (Card Style)
```css
.faq-item {
    background: var(--gray-50);
    border-radius: 8px;
    overflow: hidden;
}

.faq-question {
    padding: 1.25rem 1.5rem;
    font-family: var(--font-serif);
    color: var(--navy);
}
```

### Author Avatar
```css
.author-avatar {
    width: 36px;
    height: 36px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--white);
    font-size: 0.75rem;
    font-family: var(--font-heading);
    font-weight: 500;
    background-color: #1a3a5c; /* or custom color */
}
```

### Star Rating
```css
.stars {
    color: #9b2c3d;
    font-size: 1rem;
    margin-bottom: 1rem;
    letter-spacing: 2px;
}
```

### Form Elements
```css
.form-group input,
.form-group textarea {
    padding: 0.875rem 1rem;
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 6px;
    background: rgba(255, 255, 255, 0.05);
    color: var(--white);
    font-size: 1rem;
    font-family: var(--font-serif);
    transition: border-color 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: var(--gold);
}
```

### Social Links
```css
.social-links a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border: 1px solid rgba(255, 255, 255, 0.3);
    border-radius: 50%;
    color: var(--white);
    transition: all 0.3s ease;
}

.social-links a:hover {
    background: var(--white);
    color: var(--navy);
}
```

---

## Layout Patterns

### Two-Column Split (Hero)
```css
.hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 100vh;
}
```

### Two-Column Content (Services, FAQ)
```css
.services-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
}

.faq-content {
    display: grid;
    grid-template-columns: 300px 1fr;
    gap: 4rem;
    align-items: start;
}
```

### Four-Column Grid (Features)
```css
.features-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 2rem;
}
```

### Two-Column Grid (Portfolio)
```css
.portfolio-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
}
```

---

## Animations

### Marquee (Horizontal Scroll)
```css
/* Left to right */
@keyframes marquee {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
}

/* Right to left */
@keyframes testimonials-scroll-right {
    0% { transform: translateX(-50%); }
    100% { transform: translateX(0); }
}

/* Usage */
.badges-track {
    animation: marquee 20s linear infinite;
}

.about-gallery-track {
    animation: gallery-scroll 30s linear infinite;
}

.testimonials-track-top {
    animation: testimonials-scroll-left 40s linear infinite;
}
```

### Hover Transitions
```css
/* Standard transition */
transition: all 0.3s ease;

/* Image zoom on hover */
.portfolio-item img {
    transition: transform 0.5s ease;
}
.portfolio-item:hover img {
    transform: scale(1.05);
}

/* Arrow rotation */
.btn-hero .arrow-circle svg {
    transform: rotate(-45deg);
    transition: transform 0.3s ease;
}
.btn-hero:hover .arrow-circle svg {
    transform: rotate(0deg);
}
```

### Accordion Animation
```css
.accordion-content {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease, padding 0.3s ease;
}

.accordion-item.active .accordion-content {
    max-height: 200px;
    padding-bottom: 1.25rem;
}
```

---

## Responsive Breakpoints

| Breakpoint | Target |
|------------|--------|
| 1024px | Tablet landscape |
| 768px | Tablet portrait |
| 480px | Mobile |

### Key Responsive Changes

#### 1024px
- Hero: Single column
- Features: 2 columns
- Contact: Single column

#### 768px
- Navigation: Mobile menu
- Portfolio: Single column
- Features: Single column
- About card: Single column, centered
- Services: Single column
- FAQ: Single column
- Forms: Single column

#### 480px
- Hero buttons: Full width, stacked
- Gallery items: Smaller (200x230px)

---

## Border Radius Scale

| Size | Value | Usage |
|------|-------|-------|
| Small | 4px | Nav highlight |
| Medium | 6px | Buttons, inputs |
| Large | 8px | FAQ items, about image |
| XL | 12px | Cards, about card |
| Pill | 50px | Section tags, CTA buttons |
| Circle | 50% | Avatars, social links |

---

## Box Shadows

```css
/* Header */
box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);

/* Cards */
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);

/* Mobile menu */
box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
```

---

## Z-Index Scale

| Element | Z-Index |
|---------|---------|
| Header | 1000 |

---

## Icon Sizes

| Context | Size |
|---------|------|
| Feature icons | 24x34px |
| Service accordion icons | 32x32px |
| Arrow in buttons | 14x14px |
| Social icons | 24x24px |
| Accordion +/- | 20x20px |
