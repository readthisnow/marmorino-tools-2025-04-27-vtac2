# Marmorino Tools Landing Page - Maintenance Guide

This guide will help you maintain and customize the Marmorino Tools landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo text. To update:

1. **Logo Text**: Find this line near the top:
```html
<a href="#" class="text-2xl font-bold text-gray-800">Marmorino Tools</a>
```
Simply replace "Marmorino Tools" with your desired text.

2. **Navigation Items**: Locate the navigation menu:
```html
<div class="hidden lg:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
Replace any menu text while keeping the href attributes matching their corresponding section IDs.

### Hero Section
The main banner section contains:

1. **Main Heading**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold">
    Koop Marmorino Tools Met Korting
</h1>
```
- `text-4xl`: Controls text size on mobile
- `md:text-5xl`: Medium screen size
- `lg:text-6xl`: Large screen size

2. **Subheading**:
```html
<p class="text-xl md:text-2xl text-gray-600">
    Ontdek onze premium collectie...
</p>
```

### Tailwind CSS Tips
- Font sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`, etc.
- Spacing: `p-4` (padding), `m-4` (margin), `space-x-8` (horizontal spacing)
- Responsive prefixes: `sm:`, `md:`, `lg:` for different screen sizes

## Managing Links

### Navigation Links
Current internal links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute
3. For internal sections, use `#section-id`
4. For external links, use full URLs

### Call-to-Action Buttons
There are two main CTA buttons:
```html
<!-- Hero section -->
<a href="https://amzn.to/3S7YmNe" class="inline-block bg-blue-600">
    Bekijk Aanbiedingen
</a>

<!-- Bottom CTA section -->
<a href="https://amzn.to/3S7YmNe" class="inline-block bg-white">
    Bekijk Aanbiedingen
</a>
```
Replace the Amazon affiliate links with your desired URLs.

## Adding Policy Pages

### Footer Links Section
Locate the footer links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-gray-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-gray-300">Terms of Service</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-gray-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-gray-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating policy pages:
1. Copy the header and footer from index.html
2. Use the same Tailwind CSS and Alpine.js imports
3. Maintain consistent text styling:
```html
<main class="container mx-auto px-4 py-24">
    <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
    <div class="prose max-w-none">
        <!-- Your policy content here -->
    </div>
</main>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check responsive prefixes (`sm:`, `md:`, `lg:`)
   - Test on different screen sizes
   - Verify mobile menu functionality

3. **Style Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing closing tags
   - Verify class names are correct

Need additional help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).