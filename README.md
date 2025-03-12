# Willaby Landing Page Maintenance Guide

This guide will help you maintain and customize the Willaby Solutions landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Hero Section
The main headline is located in the first `<section>` tag. To update:

```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    End Customer Service Nightmares in 60 Seconds
</h1>

<!-- Example modification -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Your New Headline Here
</h1>
```

Understanding the classes:
- `text-4xl`: Base font size
- `md:text-5xl`: Font size on medium screens
- `lg:text-6xl`: Font size on large screens
- `bg-gradient-to-r`: Creates right-flowing gradient
- `from-purple-400 to-pink-400`: Gradient colors

### Feature Cards
Located in the `features` section, each card follows this structure:

```html
<div class="bg-gray-800 rounded-2xl p-8 hover:shadow-xl hover:shadow-purple-500/10 transition-all duration-300 transform hover:scale-105">
    <div class="w-12 h-12 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg mb-6 flex items-center justify-center">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description text</p>
</div>
```

To add a new feature card:
1. Copy the entire card `<div>` structure
2. Paste it within the `grid grid-cols-1 md:grid-cols-3 gap-8` container
3. Update the title and description text
4. Replace the SVG icon if desired

## Managing Links

### Navigation Menu Links
Located in the header section:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text between the tags

### Call-to-Action Buttons
Currently pointing to "https://willabysolutions.com". To update:

```html
<!-- Original -->
<a href="https://willabysolutions.com" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-full">
    Get Started
</a>

<!-- Update to your new URL -->
<a href="https://your-new-url.com" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-full">
    Get Started
</a>
```

## Adding Privacy and Terms Pages

### Footer Legal Links
Located in the footer section:

```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the href attributes:

```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check that all Tailwind CSS classes are spelled correctly
   - Verify the Tailwind CSS CDN link is working
   - Ensure closing tags match opening tags

2. **Links Not Working**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure internal links match section IDs

3. **Gradient Text Not Showing**
   - Confirm all gradient classes are present:
     - `bg-gradient-to-r`
     - `from-[color]`
     - `to-[color]`
     - `bg-clip-text`
     - `text-transparent`

### Need Help?
- Double-check the Tailwind CSS documentation
- Validate your HTML using W3C Validator
- Test responsiveness using browser dev tools
- Ensure Alpine.js is properly loaded for FAQ section functionality

Remember to always test your changes across different devices and browsers before deploying to production.