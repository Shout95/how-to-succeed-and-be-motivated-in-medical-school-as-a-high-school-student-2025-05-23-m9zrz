# MedSchool Academy Landing Page Maintenance Guide

This guide will help you maintain and customize the MedSchool Academy landing page. Whether you're new to web development or just getting started, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site name and navigation menu. To update:

1. **Site Name**:
```html
<!-- Find this line in the header -->
<a href="#" class="text-xl font-bold text-white hover:text-blue-400 transition duration-300">MedSchool Academy</a>
```
Simply replace "MedSchool Academy" with your desired name.

2. **Navigation Menu Items**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <!-- More menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page with the main heading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">
    How To Succeed and be Motivated in Medical School
</h1>
```

To modify:
- Change the heading text between the `<h1>` tags
- Adjust text size by modifying `text-4xl`, `text-5xl`, and `text-6xl`
- Change gradient colors by updating `from-blue-400` and `to-cyan-400`

### Tailwind CSS Class Guide
Common classes used in this template:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-300`, `bg-blue-600`, `from-blue-400`
- Spacing: `px-4`, `py-2`, `mb-6`, `mt-8`
- Flex layout: `flex`, `items-center`, `justify-between`

Example of changing button color:
```html
<!-- Original -->
<a href="#" class="bg-blue-600 hover:bg-blue-700">

<!-- Modified (to green) -->
<a href="#" class="bg-green-600 hover:bg-green-700">
```

## Managing Links

### Current Link Structure
The page contains several types of links:

1. **Navigation Menu Links**:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
These are internal links (marked with #) that scroll to page sections.

2. **Call-to-Action Links**:
```html
<a href="https://sites.google.com/view/medicalsubjectsacademy/home" class="inline-block px-8 py-4 bg-blue-600">
```

To update links:

1. Internal links:
   - Keep the `#` prefix
   - Ensure the ID matches your section: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace the full URL in `href=""`
   - Always include `https://` or `http://`

Example:
```html
<!-- Original -->
<a href="https://sites.google.com/view/medicalsubjectsacademy/home">

<!-- Updated -->
<a href="https://yournewsite.com">
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Links Not Working**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure section IDs match their corresponding links

2. **Styles Not Applying**
   - Confirm Tailwind CSS is properly loaded
   - Check for typos in class names
   - Verify class order (Tailwind uses a specificity system)

3. **Responsive Design Issues**
   - Test at different screen sizes
   - Check responsive classes (e.g., `md:`, `lg:` prefixes)
   - Use browser developer tools to inspect elements

For additional help:
- Contact: premedpoland@gmail.com
- Refer to [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements

Remember to always test changes in multiple browsers and screen sizes before publishing updates.