# Pizza & Pasta Express Landing Page - Maintenance Guide

This guide will help you maintain and customize the Pizza & Pasta Express landing page. Whether you're new to HTML and CSS or just getting started, follow these instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update the logo text:

```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold tracking-tight text-gray-900">
    Pizza & Pasta Express  <!-- Change this text -->
</a>
```

### Hero Section
The main headline and subtitle are in the hero section:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Die einfach beste Pasta, basta!  <!-- Main headline -->
</h1>
<p class="text-xl text-gray-600 mb-12 leading-relaxed">
    Experience authentic Italian cuisine...  <!-- Subtitle -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color

Example of modifying a feature card:
```html
<!-- Original -->
<div class="group p-8 rounded-2xl bg-gray-50 hover:bg-white hover:shadow-xl transition-all duration-300">

<!-- To make it darker with more padding -->
<div class="group p-12 rounded-2xl bg-gray-100 hover:bg-white hover:shadow-xl transition-all duration-300">
```

## Managing Links

### Navigation Menu Links
The main navigation contains these links:
```html
<div class="hidden lg:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://www.pizzapastabasta.de">Order Now</a>
</div>
```

To update:
1. Find the `href` attribute
2. Replace with your new URL
3. For internal links, keep the `#` prefix (e.g., `#features`)
4. For external links, use complete URLs (e.g., `https://...`)

### Order Now Buttons
Multiple "Order Now" buttons exist throughout the page. Update all instances:
```html
<!-- Find all instances of -->
<a href="https://www.pizzapastabasta.de" class="inline-flex...">
    Order Now
</a>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Files
1. Create two new files in your website folder:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper links:
```html
<li><a href="privacy.html" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check that you haven't removed any essential Tailwind classes
   - Verify all `div` tags are properly closed
   - Maintain the responsive classes (e.g., `sm:`, `lg:` prefixes)

2. **Links Not Working**
   - Ensure file names match exactly (case-sensitive)
   - Check that files are in the correct folder
   - Verify URLs start with `http://` or `https://` for external links

3. **Styles Not Applying**
   - Confirm the Tailwind CSS link in the header is present:
   ```html
   <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
   ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Keep backups before making changes

Remember to test all changes on different devices and browsers to ensure everything works as expected.