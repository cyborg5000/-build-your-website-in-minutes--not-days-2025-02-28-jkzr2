# Landing Page Maintenance Guide

This guide will help you maintain and customize the Innodium landing page. Whether you're new to web development or just getting started, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. Change the brand name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-indigo-600">Innodium</a>
```
Simply replace "Innodium" with your brand name.

### Hero Section
The main banner section contains your primary message:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-8 leading-tight">Build Your Website in Minutes, Not Days</h1>
<p class="text-xl md:text-2xl mb-12 max-w-3xl mx-auto">Best AI Website Builder, No Code Required</p>
```
- Replace the text between the `<h1>` tags for the main heading
- Update the text between the `<p>` tags for the subheading
- The `md:text-6xl` means the text will be larger on desktop screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-indigo-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-cloud text-2xl text-indigo-600"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Launch your website instantly...</p>
</div>
```
To modify:
1. Change the icon by updating the `fa-cloud` class to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the heading text between `<h3>` tags
3. Modify the description between `<p>` tags

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600 transition-colors">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-indigo-600 transition-colors">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-indigo-600 transition-colors">FAQ</a>
</div>
```
To update:
1. The `href="#features"` links to sections within the page
2. Ensure section IDs match these links (e.g., `id="features"`)
3. To link to external pages, replace with full URLs: `href="https://example.com"`

### Call-to-Action Buttons
There are several CTA buttons throughout the page:
```html
<a href="https://innodium.com" class="inline-block px-8 py-4 bg-indigo-600 text-white rounded-full">
```
Replace `https://innodium.com` with your desired destination URL.

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the footer section with legal links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:

1. Create new HTML files:
   - Create `privacy.html` in your root directory
   - Create `terms.html` in your root directory

2. Update the links in the footer:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Section IDs should not contain spaces
   - Example: `href="#features"` links to `id="features"`

2. **Responsive Design Issues**
   - Don't remove `md:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `text-4xl md:text-6xl` means normal size on mobile, larger on desktop

3. **Icon Not Showing**
   - Verify Font Awesome is properly loaded in the head section
   - Check that icon class names are correct
   - Example: `fas fa-cloud` should match exactly

### Style Guide
- Keep the indigo/purple color scheme using these classes:
  - Primary buttons: `bg-indigo-600`
  - Hover states: `hover:bg-indigo-700`
  - Text accents: `text-indigo-600`
- Maintain consistent spacing using:
  - Vertical spacing: `py-24` for sections
  - Horizontal spacing: `px-6` for containers

Remember to test all changes on both desktop and mobile devices before publishing updates.