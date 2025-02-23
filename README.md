# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text (TWD)**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your desired logo text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
The main banner section contains your primary heading and call-to-action:

```html
<h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-700 mb-8">Best Websites In Texas</p>
```
- Update headings between the `<h1>` tags
- Modify subtext between the `<p>` tags
- `md:text-6xl` means text size changes on medium screens
- `mb-6` controls bottom margin (options: mb-2, mb-4, mb-8, etc.)

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Enjoy premium hosting services...</p>
</div>
```
To modify:
1. Change icon by updating `fa-server` to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading text between `<h3>` tags
3. Modify description between `<p>` tags
4. Adjust padding using `p-8` (options: p-4, p-6, p-12, etc.)

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page sections):
   - Keep the `#` prefix
   - Ensure the ID matches your section: `href="#sectionid"`
2. External links:
   - Replace `#sectionid` with full URL: `href="https://example.com"`
3. Test all links after updating

### Call-to-Action Button
Update the main CTA button:
```html
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>
```
- Replace `https://twd.com` with your desired URL
- Modify button text between the tags
- Adjust colors using `bg-blue-600` and `text-white`

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert these links in the footer's Quick Links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure section IDs exist for internal links

2. **Styling Problems**
   - Confirm Tailwind CDN is loading
   - Check class names for typos
   - Use browser inspector to verify classes are applied

3. **Responsive Issues**
   - Test on multiple screen sizes
   - Verify `md:` prefixed classes are working
   - Check mobile menu functionality

### Getting Help
- Review [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Inspect similar elements for correct class usage
- Keep original code backed up before making changes

Remember to test all changes thoroughly before publishing to your live site. When in doubt, make one change at a time and verify it works before proceeding.