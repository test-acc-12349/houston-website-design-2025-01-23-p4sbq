# Houston Website Design - Landing Page Maintenance Guide

This guide will help you maintain and customize the Houston Website Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To modify:

1. **Logo Text**: Find this line and replace "HWD" with your text:
```html
<a href="#" class="text-2xl font-bold text-gray-800 dark:text-white">HWD</a>
```

2. **Navigation Items**: Located in the header's `<div class="hidden md:flex space-x-8">`. Each link follows this pattern:
```html
<a href="#section-name" class="text-gray-600 hover:text-gray-900 dark:text-gray-300 dark:hover:text-white transition duration-300">Menu Item</a>
```

### Hero Section
The main banner section contains:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 dark:text-white mb-6 leading-tight">Houston Website Design</h1>
<p class="text-xl md:text-2xl text-gray-600 dark:text-gray-300 mb-8">Best Websites In Houston</p>
```

To modify:
1. Change the text between the `<h1>` tags for the main heading
2. Update the subheading text between the `<p>` tags
3. The button text can be changed in: `<a href="https://hwd.com" class="inline-block...">Get Started Today</a>`

### Understanding Tailwind Classes
Common classes used throughout:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `text-{color}-{shade}`: Sets text color (gray-600, blue-600, etc.)
- `bg-{color}-{shade}`: Sets background color
- `dark:`: Prefix for dark mode styles
- `hover:`: Prefix for hover state styles
- `md:`: Prefix for medium screen sizes and up

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. The `#` symbol indicates an internal link to a section ID
2. Match the `href` value to the `id` of the target section
3. For external links, use the full URL: `href="https://example.com"`

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-twitter"></i></a>
    <a href="#" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-facebook"></i></a>
    <a href="#" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-linkedin"></i></a>
</div>
```

To update:
1. Replace the `#` with your social media profile URLs
2. Ensure all links include `https://` or `http://`

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the Quick Links section in the footer:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

Example privacy page structure:
```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="bg-white dark:bg-gray-900">
    <!-- Copy header section -->
    
    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your privacy policy content here -->
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Styling Issues**
   - Check for typos in Tailwind class names
   - Maintain the responsive prefixes (md:, lg:)
   - Keep the dark mode classes (dark:) when modifying styles

3. **Layout Problems**
   - Preserve the container classes: `container mx-auto px-4 sm:px-6 lg:px-8`
   - Maintain the grid structure in features and benefits sections
   - Keep the responsive classes for proper mobile display

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).