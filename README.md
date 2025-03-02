# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
Located near the top of the page, find the following section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8 leading-tight tracking-tight">
    Lorem ipsum dolor
</h1>
```
To update:
1. Replace "Lorem ipsum dolor" with your desired heading
2. Maintain the existing HTML tags (`<h1>`)
3. Keep all class attributes unchanged to preserve styling

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Feature 1</h3>
    <p class="text-gray-600">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
</div>
```
To update:
1. Replace "Feature 1" with your feature name
2. Update the description text while keeping the `<p>` tags intact

### Tailwind CSS Classes Explained

#### Responsive Design Classes
The landing page uses these breakpoint prefixes:
- `md:` - Applied at medium screens (768px and up)
- `lg:` - Applied at large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile (default): text-4xl (2.25rem)
- Medium screens: text-5xl (3rem)
- Large screens: text-6xl (4rem)

#### Common Class Patterns
- Background gradients: `bg-gradient-to-r from-purple-600 to-pink-600`
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom)
- Flex layouts: `flex items-center justify-between`

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute in each `<a>` tag
2. For internal page sections, use `#section-id`
3. For external links, use the full URL: `https://example.com`

### Footer Links
Current footer link structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">About</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Careers</a></li>
</ul>
```

To update:
1. Replace `#` with your actual URL
2. Maintain the class attributes for consistent styling
3. Test all links after updating

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Add these links to the footer section:

```html
<div>
    <h3 class="text-lg font-semibold text-gray-900 mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Place this code:
1. Inside the footer's grid container
2. Alongside other footer columns
3. Before the copyright notice

### Styling Consistency
- Use the same classes as existing footer links
- Maintain the `space-y-2` spacing between items
- Keep the same hover effects and transitions

## Troubleshooting

Common issues and solutions:

### Broken Layouts
If the layout appears broken:
1. Check for missing closing tags
2. Verify all Tailwind CSS classes are spelled correctly
3. Ensure the Tailwind CSS CDN link is working

### Missing Styles
If styles aren't applying:
1. Confirm the Tailwind CSS link in the header is accessible
2. Check for typos in class names
3. Verify you're using supported Tailwind CSS classes

### Links Not Working
If links aren't functioning:
1. Verify the `href` attributes are correctly formatted
2. Check that referenced section IDs exist in the document
3. Ensure external URLs include the proper protocol (https://)

Need additional help? Contact your development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).