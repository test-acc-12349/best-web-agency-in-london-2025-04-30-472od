# Landing Page Maintenance Guide

This guide will help you maintain and customize your WebAgency landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu:
```html
<div class="text-2xl font-bold text-gray-800">WebAgency</div>
```
To change the company name:
1. Locate this div in the header section
2. Replace "WebAgency" with your company name
3. Adjust text size if needed by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
The main headline and subtitle are in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Best Web Agency In London
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Grow your business with clicks
</p>
```
To update:
1. Replace the h1 text with your main headline
2. Update the paragraph text with your new subtitle
3. The classes `md:text-5xl` and `lg:text-6xl` control text size on different screen sizes

### Features and Benefits Cards
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-mouse-pointer text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">
        Intuitive interface and user-friendly design...
    </p>
</div>
```
To modify:
1. Change the icon by replacing the `fa-mouse-pointer` class with another FontAwesome icon
2. Update the h3 heading with your feature title
3. Modify the paragraph text with your feature description
4. Keep the existing Tailwind classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Internal links (starting with #) connect to sections on the same page
2. Ensure section IDs match exactly (case-sensitive)
3. For external links, replace "#" with the full URL: `href="https://example.com"`

### Call-to-Action Buttons
Current CTA buttons point to "fixrr.online":
```html
<a href="https://fixrr.online" class="inline-block bg-blue-600...">
```
To update:
1. Replace "https://fixrr.online" with your desired URL
2. Test the link after updating
3. Maintain the existing classes for styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```
To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match navigation links exactly
   - Example: `href="#Features"` won't work if section ID is `id="features"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `md:text-5xl` makes text larger on medium screens

3. **Icon Problems**
   - Ensure FontAwesome is properly loaded in the head section
   - Verify icon class names match FontAwesome 6.0 naming
   - Example: `fa-mouse-pointer` should include `fas` prefix

### Tips
- Always test changes in multiple browsers
- View the page at different screen sizes
- Keep a backup copy of the original HTML
- Use browser developer tools (F12) to inspect elements
- Maintain consistent spacing and indentation in the code

Remember to test all changes thoroughly before publishing to ensure everything works as expected.