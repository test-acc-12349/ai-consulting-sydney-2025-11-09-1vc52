# AI Consulting Sydney Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the AI Consulting Sydney landing page for developers of all experience levels.

---

## Table of Contents

1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Color Scheme Customization](#color-scheme-customization)
8. [Responsive Design Best Practices](#responsive-design-best-practices)
9. [Troubleshooting Common Issues](#troubleshooting-common-issues)
10. [Performance Optimization](#performance-optimization)

---

## Overview

The AI Consulting Sydney landing page is a modern, responsive website built with:

- **HTML5** for semantic structure
- **Tailwind CSS** for utility-first styling
- **Lucide Icons** for scalable SVG icons
- **Font Awesome** for additional icons
- **Vanilla JavaScript** for interactivity

### Key Features
- Mobile-responsive design
- Sticky navigation header
- Multiple content sections (Hero, Features, Benefits, Testimonials, About)
- Interactive mobile menu
- Smooth scrolling navigation
- Optimized for SEO

---

## Project Structure

### File Organization

```
project-folder/
├── index.html              (Main landing page)
├── privacy.html            (Privacy policy - to be created)
├── terms.html              (Terms of service - to be created)
├── blog.html               (Blog page - referenced in footer)
└── assets/                 (Optional: for images and custom CSS)
    ├── images/
    └── css/
```

### Current File Size & Load Time
- **index.html**: Single-file design (~15KB)
- **Load Time**: Optimized for fast rendering with CDN-hosted libraries

---

## Updating Text Content

### Understanding Text Sections

The landing page contains six main content sections. Here's how to update each one:

### 1. Header & Navigation

**Location**: Lines 58-95 in the HTML

```html
<!-- CURRENT CODE -->
<div class="text-2xl font-bold primary-color">
    <i data-lucide="zap" class="inline-block mr-2"></i>AI Consulting
</div>
```

**How to Update**:
- Change `"AI Consulting"` to your company name
- The icon (`<i data-lucide="zap"`) can be changed to any [Lucide icon](https://lucide.dev/)
- Example: Change `zap` to `brain`, `cpu`, `rocket`, etc.

```html
<!-- UPDATED EXAMPLE -->
<div class="text-2xl font-bold primary-color">
    <i data-lucide="brain" class="inline-block mr-2"></i>Tech Solutions
</div>
```

### 2. Hero Section (Main Headline & Subtitle)

**Location**: Lines 113-147

**Headline Update**:
```html
<!-- CURRENT CODE -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 leading-tight mb-6">
    We automate your <span class="primary-color">business</span>
</h1>
```

**How to Update**:
- Replace the entire text while keeping the `<span class="primary-color">` tags around words you want to highlight in red
- Keep the class names (`text-5xl`, `md:text-6xl`, etc.) to maintain responsive sizing
- The responsive classes mean: 5xl on mobile, 6xl on tablets (md:), 7xl on desktop (lg:)

```html
<!-- UPDATED EXAMPLE -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 leading-tight mb-6">
    Transform your <span class="primary-color">operations</span> today
</h1>
```

**Subtitle Update**:
```html
<!-- CURRENT CODE -->
<p class="text-xl md:text-2xl text-gray-600 font-medium mb-8 leading-relaxed">
    Transform your operations with intelligent AI solutions that streamline processes, 
    reduce costs, and accelerate growth. Our expert consulting team delivers measurable results.
</p>
```

**How to Update**:
- Simply replace the text between `<p>` and `</p>`
- Keep all the class names intact
- These classes control: font size (`text-xl`, `md:text-2xl`), color (`text-gray-600`), weight (`font-medium`)

### 3. Features Section

**Location**: Lines 159-260

Each feature card contains three parts:

**Feature Title**:
```html
<!-- CURRENT CODE - Feature 1 -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Smart Process Automation</h3>
```

**How to Update**:
- Replace `"Smart Process Automation"` with your feature name
- Keep the class names for consistent styling

**Feature Description**:
```html
<!-- CURRENT CODE -->
<p class="text-gray-600 font-medium leading-relaxed mb-4">
    Eliminate manual workflows and repetitive tasks with our intelligent automation solutions...
</p>
```

**How to Update**:
- Replace the description text
- Keep all class names
- You can make this text longer or shorter as needed

**Feature Bullet Points**:
```html
<!-- CURRENT CODE -->
<li class="flex items-start gap-3">
    <i data-lucide="check" class="w-5 h-5 text-[#FF5A5F] flex-shrink-0 mt-0.5"></i>
    <span class="text-gray-700 font-medium">Workflow optimization</span>
</li>
```

**How to Update**:
- Replace `"Workflow optimization"` with your bullet point text
- Keep the icon and styling classes intact
- To add more bullet points, copy the entire `<li>` element and paste it below

**Complete Example - Updating One Feature**:

```html
<!-- BEFORE -->
<div class="card-base">
    <div class="feature-icon mb-6">
        <i data-lucide="workflow" class="w-6 h-6"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Smart Process Automation</h3>
    <p class="text-gray-600 font-medium leading-relaxed mb-4">
        Eliminate manual workflows...
    </p>
    <ul class="space-y-3">
        <li class="flex items-start gap-3">
            <i data-lucide="check" class="w-5 h-5 text-[#FF5A5F] flex-shrink-0 mt-0.5"></i>
            <span class="text-gray-700 font-medium">Workflow optimization</span>
        </li>
    </ul>
</div>

<!-- AFTER -->
<div class="card-base">
    <div class="feature-icon mb-6">
        <i data-lucide="zap" class="w-6 h-6"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Lightning-Fast Deployment</h3>
    <p class="text-gray-600 font-medium leading-relaxed mb-4">
        Get your AI solutions up and running in days, not months. Our rapid deployment 
        methodology ensures minimal disruption to your business operations.
    </p>
    <ul class="space-y-3">
        <li class="flex items-start gap-3">
            <i data-lucide="check" class="w-5 h-5 text-[#FF5A5F] flex-shrink-0 mt-0.5"></i>
            <span class="text-gray-700 font-medium">Quick implementation</span>
        </li>
        <li class="flex items-start gap-3">
            <i data-lucide="check" class="w-5 h-5 text-[#FF5A5F] flex-shrink-0 mt-0.5"></i>
            <span class="text-gray-700 font-medium">Minimal downtime</span>
        </li>
    </ul>
</div>
```

### 4. Benefits Section

**Location**: Lines 262-357

Similar structure to Features section:

```html
<!-- CURRENT CODE -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Streamline Operations</h3>
<p class="text-gray-600 font-medium leading-relaxed mb-6">
    Optimize every aspect of your business operations...
</p>
```

**How to Update**:
- Replace the title and description text
- Keep all class names
- The benefit cards use bullet points with colored dots instead of checkmarks

### 5. Testimonials Section

**Location**: Lines 444-527

Each testimonial has four parts to update:

**Star Rating** (usually keep at 5 stars):
```html
<!-- CURRENT CODE -->
<div class="flex items-center gap-1 mb-4">
    <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
    <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
    <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
    <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
    <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
</div>
```

**Testimonial Quote**:
```html
<!-- CURRENT CODE -->
<p class="text-gray-700 font-medium leading-relaxed mb-6">
    "AI Consulting Sydney completely transformed our operations..."
</p>
```

**How to Update**:
- Replace the text between the quotation marks
- Keep the opening and closing quotation marks
- Keep all class names

**Client Name**:
```html
<!-- CURRENT CODE -->
<p class="font-bold text-gray-900">Sarah Mitchell</p>
```

**Client Title/Company**:
```html
<!-- CURRENT CODE -->
<p class="text-gray-600 font-medium">Operations Director, TechCore Industries</p>
```

**Complete Testimonial Update Example**:

```html
<!-- BEFORE -->
<div class="card-base">
    <div class="flex items-center gap-1 mb-4">
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
    </div>
    <p class="text-gray-700 font-medium leading-relaxed mb-6">
        "AI Consulting Sydney completely transformed our operations..."
    </p>
    <div>
        <p class="font-bold text-gray-900">Sarah Mitchell</p>
        <p class="text-gray-600 font-medium">Operations Director, TechCore Industries</p>
    </div>
</div>

<!-- AFTER -->
<div class="card-base">
    <div class="flex items-center gap-1 mb-4">
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
        <i data-lucide="star" class="w-5 h-5 fill-[#FFD166] text-[#FFD166]"></i>
    </div>
    <p class="text-gray-700 font-medium leading-relaxed mb-6">
        "The implementation was seamless and the results exceeded our expectations. 
        Our productivity increased by 50% within the first month."
    </p>
    <div>
        <p class="font-bold text-gray-900">David Johnson</p>
        <p class="text-gray-600 font-medium">CTO, Innovation Labs</p>
    </div>
</div>
```

### 6. About Us Section

**Location**: Lines 529-591

```html
<!-- CURRENT CODE -->
<h2 class="section-heading mb-8">About AI Consulting Sydney</h2>

<p class="text-lg text-gray-700 font-medium leading-relaxed mb-6">
    Founded in 2018, AI Consulting Sydney emerged from a vision...
</p>
```

**How to Update**:
- Replace the heading with your company name
- Replace the paragraphs with your company story
- Keep the class names for consistent styling

**Statistics Box**:
```html
<!-- CURRENT CODE -->
<div class="text-center">
    <p class="text-5xl font-bold primary-color mb-2">500+</p>
    <p class="text-gray-600 font-medium">Projects Completed</p>
</div>
```

**How to Update**:
- Replace `"500+"` with your statistic
- Replace `"Projects Completed"` with your label
- Keep the class names intact

### 7. Footer Section

**Location**: Lines 593-680

**Company Description**:
```html
<!-- CURRENT CODE -->
<p class="text-gray-400 font-medium mb-6">
    Transforming businesses through intelligent automation and AI-driven solutions.
</p>
```

**Footer Links** (updated in the "Fixing and Managing Links" section below):
```html
<!-- CURRENT CODE -->
<li><a href="#features" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Process Automation</a></li>
```

**Copyright Year**:
```html
<!-- CURRENT CODE -->
&copy; 2025 AI Consulting Sydney. All rights reserved.
```

**How to Update**:
- Change `2025` to the current year
- Change `"AI Consulting Sydney"` to your company name

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS uses utility classes to style elements. Instead of writing custom CSS, you combine predefined classes directly in your HTML.

### Common Tailwind Classes Used in This Project

#### Text Sizing
- `text-sm` = Small text (14px)
- `text-base` = Normal text (16px)
- `text-lg` = Large text (18px)
- `text-xl` = Extra large (20px)
- `text-2xl` = 2x large (24px)
- `text-5xl` = 5x large (48px)

#### Responsive Prefixes
- `sm:` = Apply on small screens (640px+)
- `md:` = Apply on medium screens (768px+)
- `lg:` = Apply on large screens (1024px+)

**Example - Making Text Larger on Mobile**:
```html
<!-- CURRENT CODE -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold">
    We automate your business
</h1>

<!-- EXPLANATION -->
<!-- Mobile: text-5xl (48px) -->
<!-- Tablet (768px+): md:text-6xl (60px) -->
<!-- Desktop (1024px+): lg:text-7xl (72px) -->

<!-- TO MAKE EVEN LARGER -->
<h1 class="text-6xl md:text-7xl lg:text-8xl font-bold">
    We automate your business
</h1>
```

#### Font Weight
- `font-light` = Thin (300)
- `font-normal` = Regular (400)
- `font-medium` = Medium (500)
- `font-bold` = Bold (700)

#### Colors

The page uses custom color variables defined in the `<style>` section:

```css
.primary-color {
    color: #FF5A5F;        /* Red - used for headings and accents */
}

.primary-bg {
    background-color: #FF5A5F;
}

.secondary-bg {
    background-color: #1A1A1A;  /* Dark gray/black */
}

.accent-color {
    color: #FFD166;        /* Yellow/gold */
}

.accent-bg {
    background-color: #FFD166;
}
```

**How to Change Colors**:

1. Find the color definitions in the `<style>` section (Lines 25-50)
2. Replace the hex color codes

```css
/* BEFORE */
.primary-color {
    color: #FF5A5F;  /* Red */
}

/* AFTER - Change to blue */
.primary-color {
    color: #0066FF;  /* Blue */
}
```

**Color Reference**:
- Red: `#FF5A5F`
- Yellow/Gold: `#FFD166`
- Dark Gray: `#1A1A1A`
- Light Gray: `#F9F9F9`
- White: `#FFFFFF`
- Gray text: `#666666` or `#999999`

#### Spacing

Tailwind uses a spacing scale (in multiples of 4px):
- `p-4` = Padding 16px
- `p-8` = Padding 32px
- `mb-4` = Margin bottom 16px
- `gap-4` = Gap between items 16px

```html
<!-- CURRENT CODE - Large padding -->
<div class="card-base">  <!-- Has p-8 (32px padding) -->
    Content
</div>

<!-- TO INCREASE PADDING -->
<div class="card-base p-12">  <!-- 48px padding instead of 32px -->
    Content
</div>
```

#### Border Radius (Rounded Corners)

- `rounded-lg` = 8px corners
- `rounded-xl` = 12px corners
- `rounded-2xl` = 16px corners
- `rounded-full` = Fully rounded (pill-shaped)

```html
<!-- CURRENT CODE -->
<div class="rounded-2xl">  <!-- 16px rounded corners -->
    Content
</div>

<!-- TO MAKE MORE ROUNDED -->
<div class="rounded-3xl">  <!-- 24px rounded corners -->
    Content
</div>
```

#### Shadow Effects

- `shadow-md` = Medium shadow
- `shadow-lg` = Large shadow
- `shadow-xl` = Extra large shadow

```html
<!-- CURRENT CODE -->
<div class="card-base">  <!-- Has shadow-md (10px 40px shadow) -->
    Content
</div>

<!-- TO ADD STRONGER SHADOW -->
<div class="card-base shadow-2xl">  <!-- Stronger shadow -->
    Content
</div>
```

### Practical Examples: Making Common Changes

#### Example 1: Make Section Headings Smaller

```html
<!-- CURRENT CODE -->
<h2 class="section-heading mb-4">Powerful Features Built for Your Success</h2>

<!-- WHAT IT LOOKS LIKE NOW -->
<!-- Desktop: 56px (2.25rem) -->
<!-- Mobile: 48px (1.875rem) -->

<!-- TO MAKE SMALLER -->
<h2 class="text-4xl md:text-5xl font-bold mb-4">Powerful Features Built for Your Success</h2>

<!-- NEW SIZES -->
<!-- Desktop: 36px (text-4xl) -->
<!-- Tablet: 48px (md:text-5xl) -->
```

#### Example 2: Add More Space Between Cards

```html
<!-- CURRENT CODE -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- gap-8 = 32px space between cards -->
</div>

<!-- TO INCREASE SPACE -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
    <!-- gap-12 = 48px space between cards -->
</div>
```

#### Example 3: Change Button Size

```html
<!-- CURRENT CODE -->
.btn-primary {
    padding: 12px 32px;
    font-weight: 600;
}

<!-- TO MAKE LARGER -->
.btn-primary {
    padding: 16px 48px;  /* More vertical and horizontal padding */
    font-weight: 600;
}
```

#### Example 4: Change Card Padding

```html
<!-- CURRENT CODE -->
.card-base {
    padding: 32px;  /* 32px on all sides */
}

<!-- TO MAKE TIGHTER -->
.card-base {
    padding: 24px;  /* 24px on all sides */
}

<!-- TO MAKE LOOSER -->
.card-base {
    padding: 48px;  /* 48px on all sides */
}
```

### Mobile-First Design Tips

The page uses mobile-first responsive design:

```html
<!-- STRUCTURE -->
<div class="text-2xl md:text-3xl lg:text-4xl">
    <!-- Mobile (default): text-2xl (24px) -->
    <!-- Tablet 768px+: md:text-3xl (30px) -->
    <!-- Desktop 1024px+: lg:text-4xl (36px) -->
</div>
```

**Best Practices**:
1. Start with mobile classes (no prefix)
2. Add `md:` classes for tablets
3. Add `lg:` classes for desktops
4. Test on actual devices to verify

---

## Fixing and Managing Links

### Understanding Link Types

The landing page uses three types of links:

1. **Internal Links** (anchor links within the page)
2. **External Links** (to external websites)
3. **Email Links** (mailto: links)

### Current Links Overview

#### Navigation Links (Header)

**Location**: Lines 67-76 (Desktop) and Lines 81-88 (Mobile)

```html
<!-- DESKTOP MENU -->
<a href="#features" class="font-medium text-gray-700 hover:primary-color transition-colors duration-300">Features</a>
<a href="#benefits" class="font-medium text-gray-700 hover:primary-color transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="font-medium text-gray-700 hover:primary-color transition-colors duration-300">Testimonials</a>
<a href="#about" class="font-medium text-gray-700 hover:primary-color transition-colors duration-300">About</a>
<a href="mailto:admin@admin.com" class="btn-primary">Contact Us</a>
```

**How These Work**:
- `#features` = Links to the section with `id="features"`
- `#benefits` = Links to the section with `id="benefits"`
- `#testimonials` = Links to the section with `id="testimonials"`
- `#about` = Links to the section with `id="about"`
- `mailto:admin@admin.com` = Opens email client with this address

#### Hero Section CTA Buttons

**Location**: Lines 140-147

```html
<a href="https://test.com" class="btn-primary text-center">
    Get Started Today
</a>
<a href="mailto:admin@admin.com" class="btn-secondary text-center">
    Schedule Consultation
</a>
```

**Issues to Fix**:
- `https://test.com` is a placeholder - should be replaced with your actual URL
- Email link should be your real email address

#### CTA Section Buttons

**Location**: Lines 391-399

```html
<a href="https://test.com" class="btn-primary text-center">
    Start Your Transformation
</a>
<a href="mailto:admin@admin.com" class="btn-secondary text-center">
    Contact Our Team
</a>
```

**Issues to Fix**:
- Same placeholder URL needs to be replaced
- Email should be your real address

#### Footer Links

**Location**: Lines 603-680

**Footer Navigation Links**:
```html
<!-- Services Links -->
<li><a href="#features" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Process Automation</a></li>
<li><a href="#features" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">AI Integration</a></li>
<li><a href="#benefits" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Cost Optimization</a></li>
<li><a href="#" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Consulting</a></li>

<!-- Company Links -->
<li><a href="#about" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">About Us</a></li>
<li><a href="#testimonials" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Testimonials</a></li>
<li><a href="blog.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Blog</a></li>
<li><a href="mailto:admin@admin.com" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Contact</a></li>

<!-- Legal Links -->
<li><a href="privacy.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Terms of Service</a></li>
<li><a href="#" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Cookie Policy</a></li>
<li><a href="#" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Disclaimer</a></li>
```

**Issues to Fix**:
- `privacy.html` and `terms.html` need to be created
- `blog.html` needs to be created or linked elsewhere
- `mailto:admin@admin.com` should be your real email
- Several links point to `#` (placeholder) - these need proper URLs

#### Bottom Footer Links

**Location**: Lines 673-680

```html
<div class="flex gap-6">
    <a href="privacy.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Privacy</a>
    <a href="terms.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Terms</a>
    <a href="blog.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Blog</a>
</div>
```

### Step-by-Step: Fixing Links

#### Step 1: Replace Placeholder URLs

Find all instances of `https://test.com` and replace with your real URL:

**Search for**: `https://test.com`

**Replace with**: Your actual website (e.g., `https://www.yourconsultingsite.com`)

**Locations**:
1. Line 140: Hero section "Get Started Today" button
2. Line 390: CTA section "Start Your Transformation" button

```html
<!-- BEFORE -->
<a href="https://test.com" class="btn-primary text-center">
    Get Started Today
</a>

<!-- AFTER -->
<a href="https://www.aiconsultingsydney.com/get-started" class="btn-primary text-center">
    Get Started Today
</a>
```

#### Step 2: Replace Email Addresses

Find all instances of `mailto:admin@admin.com` and replace with your email:

**Search for**: `mailto:admin@admin.com`

**Replace with**: Your email address (e.g., `mailto:info@yourcompany.com`)

**Locations**:
1. Line 74: Header "Contact Us" button
2. Line 87: Mobile menu "Contact Us" button
3. Line 145: Hero section "Schedule Consultation" button
4. Line 397: CTA section "Contact Our Team" button
5. Line 640: Footer "Contact" link
6. Line 658: Footer contact email link

```html
<!-- BEFORE -->
<a href="mailto:admin@admin.com" class="btn-primary">Contact Us</a>

<!-- AFTER -->
<a href="mailto:info@aiconsultingsydney.com.au" class="btn-primary">Contact Us</a>
```

#### Step 3: Update Placeholder Links

Links pointing to `#` need to be updated:

**Location**: Lines 652, 662, 666

```html
<!-- BEFORE -->
<li><a href="#" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Consulting</a></li>

<!-- AFTER - Option 1: Link to external page -->
<li><a href="https://www.yoursite.com/services/consulting" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Consulting</a></li>

<!-- AFTER - Option 2: Link to section on this page -->
<li><a href="#features" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Consulting</a></li>

<!-- AFTER - Option 3: Add class to disable link temporarily -->
<li><a href="#" onclick="return false;" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300 cursor-not-allowed">Consulting</a></li>
```

#### Step 4: Update Social Media Links

**Location**: Lines 620-632

```html
<!-- CURRENT CODE -->
<a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-[#FF5A5F] transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f text-gray-300"></i>
</a>
```

**How to Update**:

```html
<!-- BEFORE -->
<a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-[#FF5A5F] transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f text-gray-300"></i>
</a>

<!-- AFTER -->
<a href="https://www.facebook.com/yourpage" target="_blank" rel="noopener noreferrer" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-[#FF5A5F] transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f text-gray-300"></i>
</a>
```

**Important Attributes**:
- `target="_blank"` = Opens link in new tab
- `rel="noopener noreferrer"` = Security best practice for external links

**Update All Social Links**:

```html
<!-- FACEBOOK -->
<a href="https://www.facebook.com/yourpage" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- TWITTER -->
<a href="https://www.twitter.com/yourhandle" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-twitter"></i>
</a>

<!-- LINKEDIN -->
<a href="https://www.linkedin.com/company/yourcompany" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-linkedin-in"></i>
</a>

<!-- INSTAGRAM -->
<a href="https://www.instagram.com/yourprofile" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-instagram"></i>
</a>
```

### Complete Link Replacement Checklist

Use this checklist to ensure all links are updated:

- [ ] Replace all `https://test.com` with your actual website
- [ ] Replace all `mailto:admin@admin.com` with your email
- [ ] Update all `#` placeholder links
- [ ] Add social media links (Facebook, Twitter, LinkedIn, Instagram)
- [ ] Verify `privacy.html` link (to be created)
- [ ] Verify `terms.html` link (to be created)
- [ ] Verify `blog.html` link or remove if not available
- [ ] Test all links by clicking them
- [ ] Ensure external links open in new tabs (`target="_blank"`)

---

## Adding Privacy and Terms Pages

### Understanding Why These Pages Are Important

- **Privacy Policy**: Explains how you collect and use user data (required by law in most countries)
- **Terms of Service**: Outlines the rules for using your website and services
- **GDPR/Legal Compliance**: Many jurisdictions require these pages

### Creating the Privacy Policy Page

#### Step 1: Create the File

Create a new file named `privacy.html` in the same folder as `index.html`:

```
project-folder/
├── index.html
├── privacy.html        ← Create this file
└── terms.html          ← Create this file
```

#### Step 2: Add Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - AI Consulting Sydney">
    <meta name="title" content="Privacy Policy - AI Consulting Sydney">
    <title>Privacy Policy - AI Consulting Sydney</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        body {
            background-color: #FFFFFF;
            color: #1A1A1A;
        }
        
        .primary-color {
            color: #FF5A5F;
        }
        
        .primary-bg {
            background-color: #FF5A5F;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center">
                <a href="index.html" class="text-2xl font-bold primary-color">
                    <i data-lucide="zap" class="inline-block mr-2"></i>AI Consulting
                </a>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html#features" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">Features</a>
                <a href="index.html#benefits" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">Testimonials</a>
                <a href="index.html#about" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">About</a>
                <a href="mailto:info@aiconsultingsydney.com.au" class="btn-primary" style="background-color: #FF5A5F; color: white; border-radius: 9999px; padding: 12px 32px; font-weight: 600;">Contact Us</a>
            </div>
            
            <button class="md:hidden mobile-menu-button focus:outline-none p-2" aria-label="Toggle mobile menu">
                <i class="fas fa-bars text-2xl primary-color"></i>
            </button>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <p class="text-gray-600 font-medium mb-8">
            Last updated: <span id="last-updated"></span>
        </p>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
            <p class="text-gray-700 leading-relaxed mb-4">
                AI Consulting Sydney ("we," "us," "our," or "Company") is committed to protecting your privacy. 
                This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you 
                visit our website, including any other media form, media channel, mobile website, or mobile application 
                related or connected thereto (collectively, the "Site").
            </p>
            <p class="text-gray-700 leading-relaxed">
                Please read this privacy policy carefully. If you do not agree with our policies and practices, 
                please do not use our Site.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
            <p class="text-gray-700 leading-relaxed mb-4">
                We may collect information about you in a variety of ways. The information we may collect on the Site includes:
            </p>
            <ul class="list-disc list-inside space-y-2 text-gray-700 mb-4">
                <li><strong>Personal Data:</strong> Name, email address, phone number, company name, and other contact information you voluntarily provide.</li>
                <li><strong>Usage Data:</strong> Information about how you interact with our Site, including pages visited, time spent, and links clicked.</li>
                <li><strong>Device Information:</strong> Browser type, operating system, IP address, and device type.</li>
                <li><strong>Cookies:</strong> We use cookies to enhance your experience on our Site.</li>
            </ul>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">3. How We Use Your Information</h2>
            <p class="text-gray-700 leading-relaxed mb-4">
                Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. 
                Specifically, we may use information collected about you via the Site to:
            </p>
            <ul class="list-disc list-inside space-y-2 text-gray-700">
                <li>Process your transactions and send related information</li>
                <li>Email regarding your account or order</li>
                <li>Fulfill and manage purchases, orders, payments, and other transactions related to the Site</li>
                <li>Generate a personal profile about you to make future visits to the Site easier</li>
                <li>Increase the efficiency and operation of the Site</li>
                <li>Monitor and analyze usage and trends to improve your experience with the Site</li>
                <li>Notify you of updates to the Site</li>
                <li>Offer new products, services, and/or recommendations to you</li>
            </ul>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Disclosure of Your Information</h2>
            <p class="text-gray-700 leading-relaxed mb-4">
                We may share information we have collected about you in certain situations:
            </p>
            <ul class="list-disc list-inside space-y-2 text-gray-700">
                <li><strong>By Law or to Protect Rights:</strong> If required by law or if we believe in good faith that disclosure is necessary to protect your rights, our rights, or the rights of others.</li>
                <li><strong>Third-Party Service Providers:</strong> We may share your information with third parties that perform services for us, including payment processing, data analysis, email delivery, and customer service.</li>
                <li><strong>Business Transfers:</strong> Your information may be transferred as part of a merger, acquisition, or sale of assets.</li>
            </ul>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Security of Your Information</h2>
            <p class="text-gray-700 leading-relaxed">
                We use administrative, technical, and physical security measures to protect your personal information. 
                However, no method of transmission over the Internet or method of electronic storage is 100% secure. 
                While we strive to use commercially acceptable means to protect your personal information, we cannot guarantee 
                its absolute security.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Contact Us</h2>
            <p class="text-gray-700 leading-relaxed">
                If you have questions or comments about this Privacy Policy, please contact us at:
            </p>
            <p class="text-gray-700 leading-relaxed mt-4">
                <strong>Email:</strong> <a href="mailto:info@aiconsultingsydney.com.au" class="text-[#FF5A5F] hover:underline">info@aiconsultingsydney.com.au</a><br>
                <strong>Address:</strong> Sydney, NSW, Australia
            </p>
        </section>
    </main>

    <!-- Footer (same as index.html, shortened for example) -->
    <footer class="bg-gray-900 text-gray-300 py-16 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 font-medium">
                    &copy; 2025 AI Consulting Sydney. All rights reserved.
                </p>
                <div class="flex justify-center gap-6 mt-4">
                    <a href="privacy.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Terms</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        lucide.createIcons();
        // Set last updated date
        document.getElementById('last-updated').textContent = new Date().toLocaleDateString('en-US', { 
            year: 'numeric', 
            month: 'long', 
            day: 'numeric' 
        });
    </script>
</body>
</html>
```

### Creating the Terms of Service Page

#### Step 1: Create the File

Create a new file named `terms.html` in the same folder as `index.html`

#### Step 2: Add Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - AI Consulting Sydney">
    <meta name="title" content="Terms of Service - AI Consulting Sydney">
    <title>Terms of Service - AI Consulting Sydney</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        body {
            background-color: #FFFFFF;
            color: #1A1A1A;
        }
        
        .primary-color {
            color: #FF5A5F;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center">
                <a href="index.html" class="text-2xl font-bold primary-color">
                    <i data-lucide="zap" class="inline-block mr-2"></i>AI Consulting
                </a>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html#features" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">Features</a>
                <a href="index.html#benefits" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">Testimonials</a>
                <a href="index.html#about" class="font-medium text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300">About</a>
                <a href="mailto:info@aiconsultingsydney.com.au" style="background-color: #FF5A5F; color: white; border-radius: 9999px; padding: 12px 32px; font-weight: 600; display: inline-block;">Contact Us</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <p class="text-gray-600 font-medium mb-8">
            Last updated: <span id="last-updated"></span>
        </p>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
            <p class="text-gray-700 leading-relaxed">
                By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. 
                If you do not agree to abide by the above, please do not use this service.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
            <p class="text-gray-700 leading-relaxed mb-4">
                Permission is granted to temporarily download one copy of the materials (information or software) on 
                AI Consulting Sydney's website for personal, non-commercial transitory viewing only. This is the grant of a license, 
                not a transfer of title, and under this license you may not:
            </p>
            <ul class="list-disc list-inside space-y-2 text-gray-700">
                <li>Modifying or copying the materials</li>
                <li>Using the materials for any commercial purpose or for any public display</li>
                <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                <li>Removing any copyright or other proprietary notations from the materials</li>
                <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
            </ul>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
            <p class="text-gray-700 leading-relaxed">
                The materials on AI Consulting Sydney's website are provided on an 'as is' basis. AI Consulting Sydney makes no warranties, 
                expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties 
                or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
            <p class="text-gray-700 leading-relaxed">
                In no event shall AI Consulting Sydney or its suppliers be liable for any damages (including, without limitation, damages for loss of data 
                or profit, or due to business interruption) arising out of the use or inability to use the materials on the website, even if AI Consulting Sydney 
                or an authorized representative has been notified orally or in writing of the possibility of such damage.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
            <p class="text-gray-700 leading-relaxed">
                The materials appearing on AI Consulting Sydney's website could include technical, typographical, or photographic errors. 
                AI Consulting Sydney does not warrant that any of the materials on its website are accurate, complete, or current. 
                AI Consulting Sydney may make changes to the materials contained on its website at any time without notice.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
            <p class="text-gray-700 leading-relaxed">
                AI Consulting Sydney has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. 
                The inclusion of any link does not imply endorsement by AI Consulting Sydney of the site. Use of any such linked website is at the user's own risk.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
            <p class="text-gray-700 leading-relaxed">
                AI Consulting Sydney may revise these terms of service for its website at any time without notice. 
                By using this website, you are agreeing to be bound by the then current version of these terms of service.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
            <p class="text-gray-700 leading-relaxed">
                These terms and conditions are governed by and construed in accordance with the laws of New South Wales, Australia, 
                and you irrevocably submit to the exclusive jurisdiction of the courts located in Sydney, NSW.
            </p>
        </section>

        <section class="mb-12">
            <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Contact Information</h2>
            <p class="text-gray-700 leading-relaxed">
                If you have any questions about these Terms of Service, please contact us at:
            </p>
            <p class="text-gray-700 leading-relaxed mt-4">
                <strong>Email:</strong> <a href="mailto:info@aiconsultingsydney.com.au" class="text-[#FF5A5F] hover:underline">info@aiconsultingsydney.com.au</a><br>
                <strong>Address:</strong> Sydney, NSW, Australia
            </p>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 font-medium">
                    &copy; 2025 AI Consulting Sydney. All rights reserved.
                </p>
                <div class="flex justify-center gap-6 mt-4">
                    <a href="privacy.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 font-medium hover:text-[#FF5A5F] transition-colors duration-300">Terms</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        lucide.createIcons();
        // Set last updated date
        document.getElementById('last-updated').textContent = new Date().toLocaleDateString('en-US', { 
            year: 'numeric', 
            month: 'long', 
            day: 'numeric' 
        });
    </script>
</body>
</html>
```

### Verifying Links Work Correctly

After creating the privacy and terms pages, verify that all links work:

#### In index.html - Check These Links:

1. **Footer Legal Section** (Line 662-663):
```html
<li><a href="privacy.html">Privacy Policy</a></li>
<li><a href="terms.html">Terms of Service</a></li>
```

2. **Bottom Footer** (Line 676-677):
```html
<a href="privacy.html">Privacy</a>
<a href="terms.html">Terms</a>
```

#### Test Procedure:

1. Save all three files (`index.html`, `privacy.html`, `terms.html`) in the same folder
2. Open `index.html` in your browser
3. Scroll to the footer
4. Click on "Privacy Policy" - should navigate to `privacy.html`
5. Click on "Terms of Service" - should navigate to `terms.html`
6. On the privacy/terms pages, click the logo to return to `index.html`

#### Troubleshooting:

**Problem**: Links don't work
- **Solution**: Ensure all three files are in the same folder
- **Solution**: Check file names match exactly (case-sensitive on some servers)
- **Solution**: Use browser developer tools (F12) to check for error messages

**Problem**: Links work locally but not on server
- **Solution**: Upload all three files to your server
- **Solution**: Check file permissions on server
- **Solution**: Verify folder structure matches local setup

---

## Color Scheme Customization

### Current Color Scheme

The landing page uses a specific color palette defined in the `<style>` section:

```css
.primary-color {
    color: #FF5A5F;        /* Red */
}

.primary-bg {
    background-color: #FF5A5F;
}

.secondary-bg {
    background-color: #1A1A1A;  /* Dark Gray/Black */
}

.accent-color {
    color: #FFD166;        /* Yellow/Gold */
}

.accent-bg {
    background-color: #FFD166;
}
```

### Color Usage Map

| Element | Color | Hex Code |
|---------|-------|----------|
| Primary Buttons | Red | #FF5A5F |
| Primary Text | Red | #FF5A5F |
| Accents (Stars, Highlights) | Yellow/Gold | #FFD166 |
| Secondary Buttons | Yellow/Gold | #FFD166 |
| Footer Background | Dark Gray | #1A1A1A |
| Body Background | White | #FFFFFF |
| Text Color | Dark Gray | #1A1A1A |
| Secondary Text | Gray | #666666 |

### How to Change the Color Scheme

#### Example 1: Change Primary Color from Red to Blue

**Step 1**: Find the color definitions in `<style>` section (Lines 25-50)

**Step 2**: Replace the hex codes

```css
/* BEFORE - Red */
.primary-color {
    color: #FF5A5F;
}

.primary-bg {
    background-color: #FF5A5F;
}

/* AFTER - Blue */
.primary-color {
    color: #0066FF;  /* Blue */
}

.primary-bg {
    background-color: #0066FF;
}
```

**Step 3**: Update button colors

```css
/* BEFORE */
.btn-primary {
    background-color: #FF5A5F;
}

.btn-primary:hover {
    background-color: #E54A4F;
}

/* AFTER */
.btn-primary {
    background-color: #0066FF;  /* Blue */
}

.btn-primary:hover {
    background-color: #0052CC;  /* Darker Blue */
}
```

**Step 4**: Update shadow colors in CSS

```css
/* BEFORE */
.btn-primary:hover {
    box-shadow: 0 10px 40px rgba(255, 90, 95, 0.3);  /* Red shadow */
}

/* AFTER */
.btn-primary:hover {
    box-shadow: 0 10px 40px rgba(0, 102, 255, 0.3);  /* Blue shadow */
}
```

#### Example 2: Change Accent Color from Yellow to Purple

```css
/* BEFORE - Yellow */
.accent-color {
    color: #FFD166;
}

.accent-bg {
    background-color: #FFD166;
}

/* AFTER - Purple */
.accent-color {
    color: #9C27B0;  /* Purple */
}

.accent-bg {
    background-color: #9C27B0;
}
```

**Also update**:
```css
/* BEFORE */
.btn-secondary {
    background-color: #FFD166;
    color: #1A1A1A;
}

.btn-secondary:hover {
    background-color: #FFC847;
    box-shadow: 0 10px 40px rgba(255, 209, 102, 0.3);
}

/* AFTER */
.btn-secondary {
    background-color: #9C27B0;
    color: #FFFFFF;  /* White text for dark background */
}

.btn-secondary:hover {
    background-color: #7B1FA2;  /* Darker purple */
    box-shadow: 0 10px 40px rgba(156, 39, 176, 0.3);
}
```

### Color Picker Tools

Use these free online tools to find hex codes for colors:

1. **Google Color Picker**: Search "color picker" in Google
2. **Coolors.co**: Generate color palettes
3. **Color-hex.com**: Find color variations
4. **Paletton.com**: Create complementary color schemes

### Professional Color Schemes

Here are some pre-made color schemes you can use:

#### Modern Blue Scheme
- Primary: `#0066FF` (Blue)
- Secondary: `#00D4FF` (Cyan)
- Accent: `#FFB300` (Orange)

#### Corporate Green Scheme
- Primary: `#00A651` (Green)
- Secondary: `#003D2D` (Dark Green)
- Accent: `#FFD700` (Gold)

#### Tech Purple Scheme
- Primary: `#7C3AED` (Purple)
- Secondary: `#EC4899` (Pink)
- Accent: `#06B6D4` (Cyan)

#### Minimal Dark Scheme
- Primary: `#1F2937` (Dark Gray)
- Secondary: `#374151` (Medium Gray)
- Accent: `#EF4444` (Red)

### Updating Inline Color References

Some colors are also specified inline in the HTML. Search for these and update them:

**Search for**:
- `#FF5A5F` (Primary Red)
- `#FFD166` (Accent Yellow)
- `#1A1A1A` (Secondary Dark)

**Replace with your new colors**

Example inline color in HTML:
```html
<!-- BEFORE -->
<div style="background-color: #FF5A5F;">
    Content
</div>

<!-- AFTER -->
<div style="background-color: #0066FF;">
    Content
</div>
```

### Testing Your Color Changes

1. Save your changes
2. Refresh the browser (Ctrl+R or Cmd+R)
3. Check all sections:
   - Navigation buttons
   - Hero section
   - Feature cards
   - Testimonial stars
   - Footer
4. Verify contrast is readable (dark text on light backgrounds)
5. Test on mobile and desktop

---

## Responsive Design Best Practices

### Understanding Responsive Design

Responsive design means the website looks good and functions properly on all devices:
- Mobile phones (320px - 480px)
- Tablets (481px - 768px)
- Desktops (769px+)

### Tailwind CSS Breakpoints

The landing page uses these breakpoints:

| Prefix | Screen Size | Common Devices |
|--------|------------|-----------------|
| (none) | 0px+ | Mobile-first default |
| `sm:` | 640px+ | Large phones |
| `md:` | 768px+ | Tablets |
| `lg:` | 1024px+ | Desktops |
| `xl:` | 1280px+ | Large desktops |
| `2xl:` | 1536px+ | Extra large screens |

### Current Responsive Elements

#### 1. Navigation Menu

```html
<!-- Desktop Menu (hidden on mobile) -->
<div class="hidden md:flex items-center gap-8">
    <!-- Shows only on md (768px+) screens -->
</div>

<!-- Mobile Menu Button (hidden on desktop) -->
<button class="md:hidden mobile-menu-button">
    <!-- Shows only on screens smaller than md (768px) -->
</button>
```

**How It Works**:
- On mobile: Only hamburger menu button shows
- On tablet/desktop: Full navigation menu shows

#### 2. Hero Section Grid

```html
<!-- CURRENT CODE -->
<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
    <!-- Mobile: 1 column (stacked) -->
    <!-- Desktop (1024px+): 2 columns (side by side) -->
</div>
```

#### 3. Feature Cards

```html
<!-- CURRENT CODE -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- Mobile: 1 column -->
    <!-- Tablet (768px+): 3 columns -->
</div>
```

#### 4. Text Sizes

```html
<!-- CURRENT CODE -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold">
    We automate your business
</h1>

<!-- Sizes by screen: -->
<!-- Mobile: text-5xl (48px) -->
<!-- Tablet: md:text-6xl (60px) -->
<!-- Desktop: lg:text-7xl (72px) -->
```

### Testing Responsive Design

#### Using Browser Developer Tools

1. **Open Developer Tools**: Press F12 or Ctrl+Shift+I
2. **Toggle Device Toolbar**: Click the device icon (top left of DevTools)
3. **Test Different Sizes**:
   - iPhone 12: 390px × 844px
   - iPad: 768px × 1024px
   - Desktop: 1920px × 1080px

#### Checklist for Testing

- [ ] Mobile (320px): All text readable, buttons tappable
- [ ] Mobile (480px): Images not cut off, spacing good
- [ ] Tablet (768px): Navigation works, cards stack properly
- [ ] Desktop (1024px): Layout looks balanced
- [ ] Desktop (1920px): Content doesn't stretch too wide
- [ ] All links clickable on mobile
- [ ] Forms easy to use on mobile
- [ ] Images scale properly

### Common Responsive Issues & Fixes

#### Issue 1: Text Too Small on Mobile

```html
<!-- BEFORE - Only one size -->
<h2 class="text-4xl font-bold">Features</h2>

<!-- AFTER - Responsive sizes -->
<h2 class="text-2xl md:text-3xl lg:text-4xl font-bold">Features</h2>
```

#### Issue 2: Images Overflow on Mobile

```html
<!-- BEFORE - Fixed width -->
<img src="image.jpg" style="width: 500px;">

<!-- AFTER - Responsive width -->
<img src="image.jpg" class="w-full max-w-2xl">
```

#### Issue 3: Too Much Padding on Mobile

```css
/* BEFORE - Same padding everywhere */
.card-base {
    padding: 32px;
}

/* AFTER - Less padding on mobile */
.card-base {
    padding: 16px;  /* Mobile: 16px */
}

@media (min-width: 768px) {
    .card-base {
        padding: 32px;  /* Tablet+: 32px */
    }
}
```

#### Issue 4: Hamburger Menu Not Working

**Check**:
1. Mobile menu button JavaScript is running
2. Mobile menu has correct ID/class
3. Click handler is properly attached

```javascript
// In script section (around line 686)
const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
const mobileMenu = document.querySelector('header nav .mobile-menu');

if (mobileMenuButton && mobileMenu) {
    mobileMenuButton.addEventListener('click', () => {
        mobileMenu.classList.toggle('hidden');
    });
}
```

### Making Custom Responsive Changes

#### Example: Change Feature Cards Layout

```html
<!-- CURRENT - 3 columns on tablet -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">

<!-- CHANGE TO - 2 columns on tablet, 3 on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

#### Example: Adjust Spacing on Mobile

```html
<!-- CURRENT - Same gap everywhere -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">

<!-- CHANGE TO - Smaller gap on mobile -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:gap-8">
```

---

## Troubleshooting Common Issues

### Issue 1: Icons Not Showing

**Symptoms**: Empty spaces where icons should be

**Causes**:
- Lucide library not loaded
- Icon name spelled wrong
- Font Awesome not loaded

**Solutions**:

```html
<!-- CHECK 1: Lucide library loaded -->
<script src="https://unpkg.com/lucide@latest"></script>

<!-- CHECK 2: Icons initialized -->
<script>
    lucide.createIcons();  // Must be called after page loads
</script>

<!-- CHECK 3: Icon name correct -->
<!-- WRONG -->
<i data-lucide="zappp"></i>  <!-- Typo -->

<!-- RIGHT -->
<i data-lucide="zap"></i>  <!-- Correct name -->

<!-- CHECK 4: Font Awesome loaded for social icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```

### Issue 2: Buttons Not Styled Correctly

**Symptoms**: Buttons look plain or different colors

**Causes**:
- CSS classes missing
- Tailwind CSS not loaded
- Conflicting styles

**Solutions**:

```html
<!-- CHECK 1: Tailwind CSS loaded -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- CHECK 2: Button has correct classes -->
<!-- WRONG -->
<a href="#" class="btn">Click Me</a>

<!-- RIGHT -->
<a href="#" class="btn-primary">Click Me</a>

<!-- CHECK 3: Inline styles override CSS -->
<!-- WRONG - Inline style overrides CSS -->
<a href="#" class="btn-primary" style="background-color: blue;">Click Me</a>

<!-- RIGHT -->
<a href="#" class="btn-primary">Click Me</a>
```

### Issue 3: Mobile Menu Not Opening

**Symptoms**: Hamburger menu doesn't respond to clicks

**Causes**:
- JavaScript error
- Wrong selectors
- Event listener not attached

**Solutions**:

```javascript
// CHECK 1: Verify selectors match HTML
const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
const mobileMenu = document.querySelector('header nav .mobile-menu');

// If these return null, the selectors are wrong
console.log(mobileMenuButton);  // Should not be null
console.log(mobileMenu);         // Should not be null

// CHECK 2: Verify JavaScript runs after page loads
document.addEventListener('DOMContentLoaded', function() {
    // All code should be inside this
    const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
    // ...
});

// CHECK 3: Check browser console for errors
// Press F12 > Console tab > Look for red errors
```

### Issue 4: Links Not Working

**Symptoms**: Clicking links does nothing

**Causes**:
- Wrong href attribute
- File not in same folder
- Typo in link

**Solutions**:

```html
<!-- CHECK 1: Internal link format -->
<!-- WRONG -->
<a href="features">Features</a>  <!-- Missing # -->

<!-- RIGHT -->
<a href="#features">Features</a>

<!-- CHECK 2: External link format -->
<!-- WRONG -->
<a href="www.example.com">Link</a>  <!-- Missing https:// -->

<!-- RIGHT -->
<a href="https://www.example.com">Link</a>

<!-- CHECK 3: File exists -->
<!-- WRONG - File doesn't exist -->
<a href="blog.html">Blog</a>

<!-- RIGHT - File exists in same folder -->
<a href="index.html">Home</a>

<!-- CHECK 4: Email link format -->
<!-- WRONG -->
<a href="email@example.com">Email</a>

<!-- RIGHT -->
<a href="mailto:email@example.com">Email</a>
```

### Issue 5: Page Not Styled (Looks Plain)

**Symptoms**: No colors, no formatting, just plain text

**Causes**:
- CSS not loaded
- Font not loaded
- Browser cache issue

**Solutions**:

```html
<!-- CHECK 1: Tailwind CSS loaded -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- CHECK 2: Fonts loaded -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<!-- CHECK 3: Custom styles loaded -->
<style>
    /* All custom CSS should be here */
</style>

<!-- CHECK 4: Clear browser cache -->
<!-- Method 1: Hard refresh -->
<!-- Windows: Ctrl+Shift+R -->
<!-- Mac: Cmd+Shift+R -->

<!-- Method 2: Open in private/incognito window -->
```

### Issue 6: Responsive Design Not Working

**Symptoms**: Website doesn't change layout on mobile

**Causes**:
- Viewport meta tag missing
- Tailwind CSS not processing
- Wrong breakpoint used

**Solutions**:

```html
<!-- CHECK 1: Viewport meta tag present -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- CHECK 2: Using correct breakpoints -->
<!-- WRONG -->
<div class="md-flex">  <!-- Typo: md- instead of md: -->

<!-- RIGHT -->
<div class="md:flex">

<!-- CHECK 3: Test in browser DevTools -->
<!-- Press F12 > Toggle Device Toolbar > Test different sizes -->
```

### Issue 7: Smooth Scrolling Not Working

**Symptoms**: Page jumps instead of smoothly scrolling to sections

**Causes**:
- JavaScript not running
- CSS not applied
- Section IDs don't match links

**Solutions**:

```html
<!-- CHECK 1: Section has correct ID -->
<!-- WRONG -->
<section name="features">

<!-- RIGHT -->
<section id="features">

<!-- CHECK 2: Link points to correct ID -->
<!-- WRONG -->
<a href="#feature">Features</a>  <!-- Typo -->

<!-- RIGHT -->
<a href="#features">Features</a>

<!-- CHECK 3: JavaScript is running -->
<!-- In console (F12 > Console tab), type: -->
<!-- document.querySelector('#features') -->
<!-- Should return the section element, not null -->
```

### Debugging Steps

When something doesn't work:

1. **Open Browser Console** (F12 key)
2. **Look for Red Errors** - These tell you what's wrong
3. **Check the Elements Tab** - Right-click > Inspect to see HTML
4. **Use Console Commands**:
   ```javascript
   // Check if element exists
   document.querySelector('#features')
   
   // Check if CSS loaded
   document.styleSheets
   
   // Check JavaScript errors
   // Look in console tab
   ```
5. **Test in Different Browser** - Chrome, Firefox, Safari
6. **Clear Cache** - Ctrl+Shift+R
7. **Check File Paths** - Make sure files are in correct folders

---

## Performance Optimization

### Current Performance

The landing page is already optimized with:
- CDN-hosted libraries (faster loading)
- Minimal custom CSS
- Optimized images
- Single-page design (no page loads)

### Basic Performance Tips

#### 1. Optimize Images

```html
<!-- BEFORE - Large, unoptimized image -->
<img src="large-image.jpg" width="1920" height="1080">

<!-- AFTER - Optimized image with responsive sizes -->
<img src="image-optimized.jpg" 
     srcset="image-small.jpg 480w, image-medium.jpg 768w, image-large.jpg 1920w"
     sizes="(max-width: 640px) 100vw, (max-width: 1024px) 50vw, 100vw"
     alt="Descriptive text"
     class="w-full h-auto">
```

#### 2. Lazy Load Images

```html
<!-- Add loading="lazy" to images below the fold -->
<img src="image.jpg" loading="lazy" alt="Description">
```

#### 3. Minimize CSS

The page uses Tailwind CSS via CDN, which is already optimized. If hosting locally:

```html
<!-- Remove unused CSS by building with Tailwind CLI -->
<!-- This removes any unused Tailwind classes -->
```

#### 4. Minimize JavaScript

Current JavaScript is minimal and necessary. To further optimize:

```javascript
// Only load what's needed
document.addEventListener('DOMContentLoaded', function() {
    // Only initialize necessary features
    initMobileMenu();
    lucide.createIcons();
});
```

#### 5. Enable Gzip Compression

Ask your hosting provider to enable Gzip compression. This reduces file sizes by 70%.

### Monitoring Performance

Use these free tools:

1. **Google PageSpeed Insights** (pagespeed.web.dev)
   - Enter your website URL
   - Get performance score and recommendations

2. **GTmetrix** (gtmetrix.com)
   - Detailed performance report
   - Waterfall chart showing load times

3. **WebPageTest** (webpagetest.org)
   - Test from different locations
   - Detailed metrics

### Performance Checklist

- [ ] Images optimized (< 200KB each)
- [ ] CSS minified
- [ ] JavaScript minified
- [ ] Gzip compression enabled
- [ ] Browser caching enabled
- [ ] CDN used for static files
- [ ] Lazy loading implemented for images
- [ ] Page Speed Insights score > 90

---

## Summary & Quick Reference

### Quick Edit Checklist

Before launching, make sure to update:

**Essential**:
- [ ] Company name (Header, Footer)
- [ ] Email address (All contact links)
- [ ] External website URL (CTA buttons)
- [ ] Privacy Policy page created
- [ ] Terms of Service page created
- [ ] Social media links added

**Recommended**:
- [ ] Company description (Hero, About sections)
- [ ] Feature descriptions
- [ ] Testimonials
- [ ] Statistics (About section)
- [ ] Color scheme customized
- [ ] Logo/icon updated

**Optional**:
- [ ] Blog page created
- [ ] Additional pages created
- [ ] Images optimized
- [ ] Analytics added

### File Structure for Deployment

```
public_html/
├── index.html          (Main landing page)
├── privacy.html        (Privacy policy)
├── terms.html          (Terms of service)
├── blog.html           (Blog page - optional)
└── assets/             (Optional folder)
    ├── images/
    │   └── hero-image.jpg
    └── css/
        └── custom.css
```

### Common Commands

**Find and Replace** (in code editor):
- `Ctrl+H` (Windows) or `Cmd+H` (Mac)
- Find: `admin@admin.com`
- Replace: `your-email@company.com`

**Check for Broken Links**:
- Use browser DevTools (F12)
- Check Console tab for errors
- Click each link to verify

**Test Responsive Design**:
- Press F12 in browser
- Click device icon
- Test on multiple sizes

### Resources

- **Tailwind CSS Documentation**: tailwindcss.com/docs
- **Lucide Icons**: lucide.dev
- **Font Awesome Icons**: fontawesome.com
- **HTML Reference**: mdn.org/docs/Web/HTML
- **CSS Reference**: mdn.org/docs/Web/CSS

### Getting Help

**If something breaks**:
1. Check browser console (F12) for errors
2. Verify all files are in same folder
3. Clear browser cache (Ctrl+Shift+R)
4. Compare with original HTML
5. Search error message online

---

## Conclusion

This landing page is designed to be easily maintainable and customizable. By following this guide, you should be able to:

✅ Update all text content  
✅ Modify colors and styling  
✅ Fix and manage links  
✅ Add privacy and terms pages  
✅ Ensure responsive design  
✅ Troubleshoot common issues  

**Start with the essential updates**, then gradually customize the design to match your brand. Test thoroughly on mobile and desktop before launching.

Good luck with your AI Consulting Sydney landing page! 🚀