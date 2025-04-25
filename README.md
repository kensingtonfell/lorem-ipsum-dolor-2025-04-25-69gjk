# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Logo
</div>
```
Replace "Logo" with your company name. The gradient effect will automatically apply.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
- Replace "Features", "Benefits", and "Contact" with your desired menu items
- Keep the classes intact to maintain hover effects and spacing

### Hero Section
Located at the top of the page with two buttons:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Lorem ipsum dolor
</h1>
<p class="text-xl text-gray-600 mb-12 leading-relaxed">
    Lorem ipsum dolor
</p>
```
- Replace both instances of "Lorem ipsum dolor" with your actual content
- The `text-4xl md:text-5xl lg:text-6xl` classes control text size across different screen sizes
- Don't remove the gradient classes to maintain the colorful heading effect

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white border border-gray-100 hover:shadow-xl transition duration-300">
    <div class="w-12 h-12 bg-purple-100 rounded-lg mb-6 flex items-center justify-center">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Lorem ipsum dolor</h3>
    <p class="text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
</div>
```
To add more feature cards:
1. Copy the entire `<div>` block
2. Paste it within the `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8` container
3. Update the heading and paragraph text
4. Maintain the classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current placeholder links are marked with `#`:
```html
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```

To update:
1. Replace `#` with your actual URL:
   - For same-page sections: `href="#features"`
   - For other pages: `href="about.html"`
   - For external links: `href="https://example.com"`

### Footer Links
The footer contains multiple columns of links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">About</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Careers</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Blog</a></li>
</ul>
```

Update each `href="#"` with the appropriate URL following the same pattern as navigation links.

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Add these links to your footer section:

```html
<!-- Add this to one of the footer columns -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Alternative Footer Placement
For a simpler approach, add links to the bottom copyright section:
```html
<div class="mt-12 pt-8 border-t border-gray-200">
    <p class="text-center text-gray-600">
        &copy; 2024 Company Name. All rights reserved. 
        <a href="privacy.html" class="hover:text-gray-900 transition-colors duration-300">Privacy Policy</a> | 
        <a href="terms.html" class="hover:text-gray-900 transition-colors duration-300">Terms of Service</a>
    </p>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
   - Ensure you haven't removed any of these classes:
     - `bg-gradient-to-r`
     - `from-purple-600`
     - `to-blue-500`
     - `bg-clip-text`
     - `text-transparent`

2. **Responsive Issues**
   - Check that you've maintained the responsive classes:
     - `md:` prefix for medium screens
     - `lg:` prefix for large screens
     - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Missing Hover Effects**
   - Verify these classes are present:
     - `hover:shadow-xl`
     - `hover:scale-105`
     - `transition duration-300`

### Getting Help
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify all classes are spelled correctly
3. Ensure you haven't accidentally removed closing tags
4. Use browser developer tools to inspect elements

Remember to test your changes across different screen sizes using browser developer tools before deploying updates.