# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<a href="#" class="text-2xl font-['Playfair_Display'] font-bold text-gray-800">Logo</a>
```
- Replace "Logo" with your company name
- Maintain the Playfair Display font for consistent branding

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
- Update text between `<a>` tags
- Keep the `href` attributes matching your section IDs
- Maintain the spacing class `space-x-8` for consistent layout

### Hero Section
```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Lorem ipsum dolor
</h1>
```
- Replace "Lorem ipsum dolor" with your headline
- Keep responsive text sizes (`text-4xl md:text-5xl lg:text-6xl`)
- Maintain the Playfair Display font

### Tailwind CSS Class Guide
Common classes explained:
- `text-gray-600`: Text color
- `hover:text-gray-900`: Color on hover
- `md:text-5xl`: Responsive text size for medium screens
- `mb-8`: Margin bottom spacing
- `py-24`: Vertical padding
- `container mx-auto`: Centers content with auto margins

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```
To update:
1. Identify the section ID you want to link to
2. Add a matching ID to that section: `<section id="your-section-name">`
3. Update the href with a hashtag: `<a href="#your-section-name">`

### Call-to-Action Buttons
```html
<a href="#" class="inline-block bg-gradient-to-r from-purple-600 to-indigo-600">
    Get Started Now
</a>
```
To update:
1. Replace `#` with your target URL
2. Example: `<a href="https://example.com/signup">`

### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition duration-300">About</a></li>
    <li><a href="#" class="hover:text-white transition duration-300">Careers</a></li>
    <li><a href="#" class="hover:text-white transition duration-300">Contact</a></li>
</ul>
```
To update:
1. Replace `#` with your page URLs
2. Example: `<a href="/about.html">`
3. Keep the hover classes for consistent styling

## Adding Privacy and Terms Pages

### Step 1: Create New Footer Column
Add this code to the footer grid:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create Required Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Add your policy content between them

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header
   - Test on different screen sizes

3. **Font Problems**
   - Verify the Google Fonts link is in the `<head>`
   - Keep both 'Playfair Display' and 'Inter' font families
   - Check font-family classes are properly quoted

Need help? Contact our support team or refer to the Tailwind CSS documentation for detailed class references.