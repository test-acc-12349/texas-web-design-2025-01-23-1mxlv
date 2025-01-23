# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">Texas Web Design</a>
```
- Replace "Texas Web Design" with your company name
- Keep the classes unchanged to maintain the gradient effect

### Hero Section
The main banner section contains your primary headline:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">Best Texas Website Design</h1>
```
- Update the text between the `<h1>` tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
To modify feature cards:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-paint-brush text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Custom Design</h3>
    <p class="text-gray-600">Unique, tailored designs that perfectly reflect your brand identity</p>
</div>
```
- Update the icon by changing the `fa-paint-brush` class to any [Font Awesome](https://fontawesome.com/icons) icon
- Modify the heading and paragraph text as needed
- Keep the structural classes to maintain layout and hover effects

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. Change the `href` value to your desired destination
2. Update the link text between the `<a>` tags
3. Keep the classes for consistent styling

### Call-to-Action Links
Update the "Get Started" buttons:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white font-bold rounded-full hover:bg-blue-700 transform hover:scale-105 transition-all duration-300 shadow-lg">Start Your Project</a>
```
- Replace `https://twd.com` with your actual URL
- Modify button text as needed

### Email Links
Update email addresses:
```html
<a href="mailto:admin@twd.com" class="text-xl hover:underline">admin@twd.com</a>
```
- Change both the `href="mailto:..."` and the visible email address

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes start with either:
     - `#` for same-page links
     - `https://` for external links
     - `mailto:` for email links
     - Relative paths (`/`, `./`, or `../`) for local pages

2. **Styling Problems**
   - Don't remove `class` attributes
   - Keep the responsive classes (starting with `md:` or `lg:`)
   - Maintain the gradient classes for branded elements

3. **Icon Issues**
   - Ensure Font Awesome is properly loaded
   - Check that icon class names match exactly
   - Keep the `fas`, `fab`, or `far` prefix as needed

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Font Awesome icons at [fontawesome.com](https://fontawesome.com)
- Test all changes in multiple browsers
- Keep a backup of the original files before making changes

Remember to test all changes on multiple devices and screen sizes to ensure the responsive design remains intact.