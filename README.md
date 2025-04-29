# Sugga Mamaz Sweetz Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Sugga Mamaz Sweetz landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold">Sugga Mamaz</a>
```
- Replace "Sugga Mamaz" with your desired text
- The `text-2xl` class controls size (options: text-sm, text-lg, text-3xl)

2. **Navigation Menu Items:**
```html
<a href="#menu" class="hover:text-gray-600 transition-colors duration-300">Menu</a>
```
- Update text between `<a>` tags
- Keep the `hover:text-gray-600` class for hover effects

### Hero Section
Located at the top of the page with the main image:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Fresh, Good Food Is a Big Deal – Because Every Bite Deserves Gourmet Love.
</h1>
```
- Update text between the `<h1>` tags
- `md:text-6xl` makes text larger on medium screens
- `mb-6` adds bottom margin (spacing)

2. **Hero Image:**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
     alt="Luxury Catering" class="w-full h-full object-cover">
```
- Replace the `src` URL with your image
- Update the `alt` text for accessibility
- Keep `object-cover` for proper image scaling

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <div class="w-16 h-16 bg-black text-white rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-star text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Exclusive</h3>
    <p class="text-gray-600">Curated experiences for discerning tastes</p>
</div>
```
- Change icon by updating `fa-star` to any [Font Awesome icon](https://fontawesome.com/icons)
- Update heading text in `<h3>` tags
- Modify description in `<p>` tags

## Managing Links

### Navigation Menu Links
Current placeholder links that need updating:
```html
<a href="#menu">Menu</a>
<a href="#services">Services</a>
<a href="#contact">Contact</a>
<a href="https://stripe.com/suggarmamazsweetz">Order Now</a>
```

To update:
1. Replace `#menu` with actual page URL (e.g., `/menu.html`)
2. For external links, use complete URLs (e.g., `https://example.com`)
3. Test all links after updating

### Footer Links
Current footer links requiring updates:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About Us</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Services</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Menu</a></li>
</ul>
```

To update:
1. Replace `#` with actual page URLs
2. Maintain the `hover:text-white` class for consistent styling
3. Add new links by copying the `<li>` structure

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy header and footer from `index.html` for consistent styling
3. Add content between header and footer

Example structure for privacy.html:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-4 py-12">
        <h1 class="text-3xl font-bold mb-6">Privacy Policy</h1>
        <!-- Add your privacy policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Images**
   - Verify image URLs are correct and accessible
   - Check file paths for local images
   - Ensure images are in the correct directory

2. **Responsive Design Issues**
   - Keep `md:` prefixed classes for medium screen styles
   - Maintain `container` class on main sections
   - Test on multiple screen sizes

3. **Font Awesome Icons Not Showing**
   - Verify the Font Awesome CDN link in the head section
   - Check icon class names against Font Awesome documentation
   - Ensure proper class prefix (`fas`, `fab`, etc.)

Need additional help? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).