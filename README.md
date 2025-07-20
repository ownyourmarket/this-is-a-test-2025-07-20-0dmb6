# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**: Locate this code in the header:
```html
<div class="text-xl font-bold text-white">
    <span class="text-blue-500">Test</span>Pro
</div>
```
- Change "Test" and "Pro" to your brand name
- The blue portion uses `text-blue-500` class

2. **Navigation Menu Items**: Find these lines:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```
- Update text between `<a>` tags
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-r from-blue-400 to-blue-600">
    This is a Test
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    You have passed the test
</p>
```
- Replace "This is a Test" with your headline
- Update the paragraph text
- The gradient effect is created by `bg-gradient-to-r from-blue-400 to-blue-600`

### Understanding Tailwind Classes
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `bg-[color]-[shade]`: Background colors (e.g., `bg-gray-900`)
- `px-[size]` and `py-[size]`: Padding (x=horizontal, y=vertical)
- `mb-[size]`: Margin bottom
- `md:`: Applies styles at medium screen sizes and up

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates section IDs on the same page
2. Ensure section IDs match these links (e.g., `id="features"`)
3. For external links, replace with full URL:
```html
<a href="https://yoursite.com/page">Page Name</a>
```

### Call-to-Action Buttons
Current form link:
```html
<a href="https://form.typeform.com/to/Y937ravs">
```
To update:
1. Replace the Typeform URL with your form link
2. Update this link in all CTA buttons:
   - "Get Started" in header
   - "Start Now" in hero section
   - "Start Your Journey" in contact section

## Adding Privacy and Terms Pages

### Footer Links
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <div class="space-y-2">
        <a href="#" class="block text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="#" class="block text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

To add links:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<a href="privacy.html" class="block text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="block text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match navigation links exactly
   - IDs are case-sensitive
   - Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These ensure proper display on different screen sizes
   - Test your page at various browser widths

3. **Styling Problems**
   - Keep the `class` attributes intact when updating text
   - Maintain spacing between class names
   - Don't remove transition classes (they control hover effects)

4. **Contact Information**
   - Update email address in both contact section and footer:
   ```html
   <p class="text-gray-400">myusalocal+tes@gmail.com</p>
   ```

Remember to:
- Always make backups before editing
- Test all links after making changes
- View your page on different devices
- Keep the original class structure to maintain design consistency

Need help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).