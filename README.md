# Budget Challenge Landing Page - Maintenance Guide

This guide will help you maintain and customize the Budget Challenge landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<div class="text-xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Budget Challenge <!-- Change this text to update the logo -->
</div>
```

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Voordelen</a> <!-- Update text here -->
    <a href="#faq">FAQ</a>           <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
The main banner section at the top:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Budget Challenge Kaarten <!-- Update main heading -->
</h1>
<p class="text-xl md:text-2xl mb-12 text-gray-300 max-w-3xl mx-auto">
    Koop Budget Challenge Kaarten Met Korting <!-- Update subheading -->
</p>
```

### Styling Tips
- The page uses Tailwind CSS classes for styling
- Common class patterns:
  - Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
  - Colors: `text-gray-100`, `bg-gray-900`, etc.
  - Spacing: `p-4` (padding), `m-4` (margin), `mb-8` (margin-bottom)
  - Responsive design: `md:text-xl` (applies at medium screens and up)

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Locate the section you want to link to
2. Note its `id` attribute
3. Use that id in the href with a # prefix
4. Example: `<section id="new-section">` → `<a href="#new-section">`

### Call-to-Action Buttons
The page has two main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://amzn.to/3YN9hQa" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500 px-8 py-4 rounded-full">
    Bekijk Speciale Aanbieding
</a>

<!-- Bottom CTA button -->
<a href="https://amzn.to/3YN9hQa" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500 px-8 py-4 rounded-full">
    Bestel Nu Met Korting
</a>
```

To update:
1. Replace `https://amzn.to/3YN9hQa` with your new URL
2. Update button text between `<a>` tags
3. Maintain the existing classes for consistent styling

## Adding Policy Pages

### Footer Links Section
Locate the footer links section:
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create your policy pages (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Classes starting with `md:` only apply on medium screens and larger
   - Check mobile view using browser dev tools
   - Common responsive classes used:
     - `md:text-xl`
     - `md:grid-cols-2`
     - `lg:grid-cols-3`

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

4. **Navigation Menu Not Working**
   - Verify Alpine.js is loading (check browser console)
   - Ensure `x-data` attribute is present on header
   - Check that button click handler `@click` is properly set

### Need More Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test all links after making changes
- Always backup your files before making major changes

Remember to test your changes across different devices and browsers to ensure consistency in appearance and functionality.