# Rose Toy Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Rose Toy landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original -->
<div class="text-2xl font-bold text-pink-600">RoseToy</div>

<!-- How to modify -->
<div class="text-2xl font-bold text-pink-600">Your Brand Name</div>
```

#### Hero Section
The hero section contains three main text elements:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">Rose Toy Vibrator</h1>
<p class="text-xl md:text-2xl mb-8">Discover Personal Pleasure & Intimacy</p>
```
To update, simply replace the text between the tags while maintaining the HTML structure.

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing Classes:
  - `px-4`: Horizontal padding
  - `py-2`: Vertical padding
  - `mb-6`: Margin bottom
  - `space-x-6`: Horizontal spacing between elements

- Responsive Classes:
  - `md:text-6xl`: Applies on medium screens and larger
  - `md:grid-cols-2`: Two columns on medium screens

- Colors:
  - `bg-pink-600`: Background color
  - `text-white`: Text color
  - `hover:bg-pink-700`: Background color on hover

#### Example Modification
```html
<!-- Original button -->
<button class="bg-pink-600 text-white px-6 py-2 rounded-full">

<!-- Modified button (different color and size) -->
<button class="bg-blue-600 text-white px-8 py-3 rounded-full">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-6">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

To update internal links:
1. Locate the section ID you want to link to
2. Add a `#` followed by the section ID
3. Example: `<a href="#features">Features</a>`

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-pink-400"><i class="fab fa-instagram"></i></a>
    <a href="#" class="hover:text-pink-400"><i class="fab fa-twitter"></i></a>
    <a href="#" class="hover:text-pink-400"><i class="fab fa-facebook"></i></a>
</div>
```

To update:
1. Replace `#` with your social media URL
2. Example: `<a href="https://instagram.com/youraccount">`

## Linking Privacy and Terms Pages

### Footer Policy Links
Current structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-pink-400">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-pink-400">Terms of Service</a></li>
    <li><a href="#" class="hover:text-pink-400">Returns</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-pink-400">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-pink-400">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating new policy pages:
1. Copy the header and footer from index.html
2. Use the same Tailwind CSS CDN link
3. Maintain consistent styling classes:
```html
<main class="container mx-auto px-4 py-16">
    <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
    <div class="prose max-w-none">
        <!-- Your policy content here -->
    </div>
</main>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout on Mobile**
   - Check for proper responsive classes (md:, lg:)
   - Ensure container class is present
   - Verify viewport meta tag exists

2. **Missing Icons**
   - Confirm Font Awesome CDN is loaded
   - Check icon class names against Font Awesome documentation
   - Example: `<i class="fas fa-check-circle"></i>`

3. **Links Not Working**
   - Verify href attributes are correct
   - Check for typos in section IDs
   - Ensure file paths are relative to index.html

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all CDN links are accessible
3. Test responsiveness using browser dev tools
4. Ensure all files are in the correct directory

Remember to always test changes across different devices and browsers before deploying to production.