# WebLondon Landing Page - Maintenance Guide

This guide will help you maintain and customize the WebLondon landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line in the header:
```html
<a href="/" class="text-2xl font-bold text-gray-900">WebLondon</a>
```
Replace "WebLondon" with your company name.

2. **Navigation Links**: Located in:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <!-- More links -->
</div>
```
Modify the text between `<a>` tags to change menu items.

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Best Websites In London</h1>
<p class="text-xl md:text-2xl text-gray-600">Custom Websites For Your Business</p>
```
- Change text between the tags
- Keep the classes intact to maintain responsive design
- `md:` and `lg:` prefixes control appearance on different screen sizes

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Intuitive interface...</p>
</div>
```
To modify:
1. Change the heading text between `<h3>` tags
2. Update description text between `<p>` tags
3. Keep all classes to maintain styling

### Tailwind CSS Tips
- `text-{size}`: Controls font size (xl, 2xl, etc.)
- `font-{weight}`: Controls font boldness (semibold, bold)
- `mb-{number}`: Adds margin bottom (4 = 1rem)
- `p-{number}`: Adds padding all around
- `bg-{color}-{shade}`: Sets background color

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600">
```

### Updating Links
1. Internal Links (same page sections):
```html
<!-- Original -->
<a href="#features">Features</a>

<!-- Update to link to new section -->
<a href="#new-section">New Section</a>
```

2. External Links:
```html
<!-- Original -->
<a href="https://sigmaseo.io">

<!-- Update to your domain -->
<a href="https://yourwebsite.com">
```

### Footer Links
Located in:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Services Section -->
    <ul class="space-y-2">
        <li><a href="#">Web Design</a></li>
        <!-- More links -->
    </ul>
</div>
```
Replace `#` with actual URLs.

## Adding Privacy and Terms Pages

### Step 1: Locate Footer Links
Find this section:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Update Links
```html
<!-- Change from -->
<a href="#" class="hover:text-white">Privacy Policy</a>

<!-- To -->
<a href="privacy.html" class="hover:text-white">Privacy Policy</a>

<!-- And -->
<a href="terms.html" class="hover:text-white">Terms of Service</a>
```

### Step 3: Create Policy Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same styling classes for consistency
3. Example structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="font-['Inter'] antialiased">
    <!-- Copy header from index.html -->
    <main class="pt-32 container mx-auto px-6">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content -->
    </main>
    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues:
1. **Broken Links**: Ensure all `href` attributes start with:
   - `#` for same-page sections
   - `https://` for external links
   - Relative paths (`privacy.html`) for internal pages

2. **Styling Issues**: 
   - Don't remove `md:` or `lg:` prefixes
   - Keep all existing classes when updating text
   - Maintain the class order for consistent styling

3. **Layout Problems**:
   - Check that all opening tags have closing tags
   - Maintain the grid structure in sections
   - Keep the container classes (`container mx-auto px-6`)

Need more help? Refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)