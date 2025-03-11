# PetCare Landing Page - Maintenance Guide

This guide will help you maintain and customize the PetCare landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu:

```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
        <div class="flex items-center space-x-10">
            <a href="#" class="text-2xl font-bold">PetCare</a> <!-- Brand name here -->
```

To modify:
1. Change brand name: Replace "PetCare" with your desired name
2. Adjust font size: Modify `text-2xl` to `text-3xl` for larger text or `text-xl` for smaller
3. Change spacing: Adjust `space-x-10` to increase/decrease menu item spacing

### Hero Section
The main banner section includes:

```html
<div class="max-w-4xl">
    <h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight">
        Extraordinary care for extraordinary companions.
    </h1>
    <p class="text-xl md:text-2xl text-white/90 mb-8">
        Essentials that honor the joy your pet brings daily.
    </p>
```

To customize:
1. Update headline: Replace text within `<h1>` tags
2. Modify subheading: Change text within `<p>` tags
3. Adjust responsive sizing:
   - `text-4xl` controls mobile size
   - `md:text-6xl` controls desktop size

### Tailwind CSS Class Guide
Common classes used throughout:
- `container mx-auto`: Centers content with automatic margins
- `px-4`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `space-x-4`: Creates horizontal spacing between elements
- `rounded-xl`: Applies rounded corners
- `shadow-md`: Adds medium shadow effect

## Managing Links

### Navigation Menu Links
Current navigation structure:

```html
<div class="hidden md:flex space-x-6">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors">Shop</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors">About</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors">Contact</a>
</div>
```

To update links:
1. Locate the `href="#"` attributes
2. Replace with proper URLs:
   ```html
   <a href="/shop.html" class="text-gray-600 hover:text-gray-900 transition-colors">Shop</a>
   <a href="/about.html" class="text-gray-600 hover:text-gray-900 transition-colors">About</a>
   <a href="/contact.html" class="text-gray-600 hover:text-gray-900 transition-colors">Contact</a>
   ```

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors">
        <i class="fab fa-facebook-f"></i>
    </a>
```

To update:
1. Replace `href="#"` with your social media URLs
2. Example:
   ```html
   <a href="https://facebook.com/yourpage" class="text-gray-400 hover:text-white transition-colors">
   ```

## Adding Privacy and Terms Pages

### Footer Integration
Add privacy and terms links to the footer:

1. Locate the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
```

2. Add new links:
```html
<ul class="space-y-2">
    <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
    <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
</ul>
```

### Styling Consistency
Maintain consistent styling by:
1. Using `text-gray-400` for normal state
2. Including `hover:text-white` for hover effect
3. Adding `transition-colors` for smooth color changes

## Troubleshooting

### Common Issues

1. **Broken Images**
   - Verify image paths in `src` attributes
   - Ensure images exist in referenced locations
   - Check image URL accessibility

2. **Responsive Issues**
   - Check mobile classes (before `md:` prefix)
   - Verify desktop classes (after `md:` prefix)
   - Test different screen sizes using browser dev tools

3. **Link Problems**
   - Confirm file paths are correct
   - Use relative paths for internal links
   - Use complete URLs for external links

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify HTML syntax using W3C Validator
- Test all links before deploying changes

Remember to always backup your files before making significant changes, and test your updates across different browsers and devices.