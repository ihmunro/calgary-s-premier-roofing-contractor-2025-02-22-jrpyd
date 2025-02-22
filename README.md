# Premier Roofing Landing Page - Maintenance Guide

This guide will help you maintain and customize the Premier Roofing landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

1. Change company name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">
    Premier Roofing  <!-- Replace this text -->
</a>
```

2. Modify navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be modified here -->
    <a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
</div>
```

### Hero Section
The main banner section includes your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Calgary's Premier Roofing Contractor  <!-- Update headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Our goal is to continually provide...  <!-- Update subheading here -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`, etc.
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive prefixes: `md:` (medium screens), `lg:` (large screens)

Example of modifying button styles:
```html
<!-- Original button -->
<a href="#" class="px-6 py-3 bg-blue-600 text-white rounded-full">

<!-- To make button larger with different color -->
<a href="#" class="px-8 py-4 bg-red-600 text-white rounded-full">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

2. Call-to-Action Links:
```html
<!-- Update this URL to your actual website -->
<a href="https://calgaryspremierroofer.com" class="inline-block px-8 py-4">
```

3. Contact Link:
```html
<!-- Update with your actual email -->
<a href="mailto:iainhmunro@gmail.com">
```

### How to Update Links
1. For internal section links (starting with #):
   - Ensure the href matches the id of the target section
   - Example: `href="#features"` should match `id="features"`

2. For external links:
   - Replace placeholder URLs with actual websites
   - Always include `https://` or `http://`
   - Example: `href="https://yourcalgaryroofer.com"`

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
1. Locate the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

2. Create matching HTML files:
   - Create `privacy.html` in the same folder as `index.html`
   - Create `terms.html` in the same folder as `index.html`
   - Use the same styling classes for consistency

## Troubleshooting

Common Issues:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive: `#FAQ` is different from `#faq`

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - Don't remove these as they control mobile/desktop appearance

3. **Style Changes Not Working**
   - Verify Tailwind CSS is properly loaded in the head section
   - Check for typos in class names
   - Classes must be exact: `bg-blue-600` not `background-blue-600`

4. **Email Links Not Working**
   - Ensure mailto: links are formatted correctly:
   ```html
   <a href="mailto:your.email@domain.com">
   ```

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your web developer.