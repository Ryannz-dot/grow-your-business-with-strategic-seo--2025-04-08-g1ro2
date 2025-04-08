# SEO Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To modify:

1. **Brand Name**: Locate this line and change "SEOGrow":
```html
<a href="/" class="text-2xl font-bold text-blue-600">SEOGrow</a>
```

2. **Navigation Items**: Find the `<div class="hidden md:flex space-x-8">` section to update menu items:
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
```

### Hero Section
Located right after the header, customize your main message:

1. **Main Heading**: Find and modify:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Grow Your Business with Strategic SEO
</h1>
```

2. **Subheading**: Update this line:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Boosting visibility and traffic for sustainable results
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-blue-600`, `bg-white`
- Spacing: `px-4`, `py-2`, `mb-6`
- Responsive prefixes: `md:`, `lg:`

To modify styling, adjust these classes. For example:
```html
<!-- Original -->
<div class="text-xl text-blue-600">

<!-- Make text larger and change color -->
<div class="text-2xl text-green-600">
```

## Managing Links

### Navigation Links
1. Internal links use hashtags (#) for page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. External links (currently pointing to rehannawaz.info) should be updated:
```html
<!-- Find and replace all instances of -->
<a href="https://www.rehannawaz.info">
<!-- With your actual URL -->
<a href="https://www.your-domain.com">
```

### Social Media Links
Located in the footer, update these placeholder links:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Replace # with your social media URLs -->
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the Quick Links section in the footer:
```html
<ul class="space-y-4">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues

1. **Broken Layout**
- Check for missing closing tags
- Verify Tailwind classes are spelled correctly
- Ensure responsive classes (md:, lg:) are properly set

2. **Missing Icons**
If Font Awesome icons don't appear:
```html
<!-- Verify this line is present in <head> -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```

3. **Navigation Links Not Working**
- Ensure section IDs match href attributes
- Check for extra spaces in IDs
- Verify sections exist in the document

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Use browser developer tools (F12) to inspect elements

Remember to:
- Test all changes across different screen sizes
- Keep backup copies before making major changes
- Validate links after updating
- Maintain consistent styling throughout the page