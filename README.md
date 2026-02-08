# Luxury Interior Design Website

A clean, professional, multi-page website for an interior design and home improvement business.

## Pages Included

1. **Home (index.html)** - Hero section, about preview, services overview, featured projects
2. **Portfolio (portfolio.html)** - Filterable project gallery with detailed case studies
3. **Services (services.html)** - Comprehensive service offerings and process
4. **About (about.html)** - Company story, values, team
5. **Contact (contact.html)** - Contact form and business information

## Features

- **Responsive Design** - Works perfectly on mobile, tablet, and desktop
- **Modern Aesthetic** - Luxury design with clean typography and elegant colors
- **Portfolio Filtering** - Interactive filtering system for project categories
- **Contact Form** - Ready-to-integrate contact form
- **Mobile Menu** - Hamburger menu for mobile devices
- **Smooth Animations** - Subtle fade-in effects and hover states

## Customization Guide

### 1. Update Business Information

**Contact Details** (Update in all HTML files in footer):
```html
<p>Email: info@yourdesign.com</p>
<p>Phone: +966 XX XXX XXXX</p>
```

**Business Name** (Update nav-brand in all files):
```html
<div class="nav-brand">YOUR BUSINESS NAME</div>
```

### 2. Replace Placeholder Images

All placeholder images are marked with the class `.placeholder-image`. To replace:

1. Add your images to the `/images` folder
2. Replace the placeholder divs with `<img>` tags:

```html
<!-- Before -->
<div class="placeholder-image">
    <span>Project 1</span>
</div>

<!-- After -->
<img src="images/project-1.jpg" alt="Project description">
```

### 3. Customize Colors

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #2c3e50;     /* Main dark color */
    --secondary-color: #c8a97e;   /* Gold/accent color */
    --accent-color: #8b7355;      /* Secondary accent */
    --text-dark: #2c3e50;         /* Body text */
    --text-light: #6c757d;        /* Secondary text */
}
```

### 4. Update Content

- **Portfolio Projects**: Edit `portfolio.html` to add/remove projects
- **Services**: Modify `services.html` to reflect your actual services
- **Team Members**: Update `about.html` with your team information
- **Hero Text**: Change the main headline in `index.html`

### 5. Integrate Contact Form

The contact form currently shows a success message. To connect to a backend:

**Option A: PHP Backend**
```php
// contact.php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = $_POST['name'];
    $email = $_POST['email'];
    $message = $_POST['message'];
    
    // Send email or save to database
    mail("your@email.com", "New Contact Form", $message);
    
    echo json_encode(['success' => true]);
}
?>
```

**Option B: Third-Party Service**
- Use Formspree: https://formspree.io
- Use Netlify Forms: https://www.netlify.com/products/forms
- Use EmailJS: https://www.emailjs.com

Update the form action in `script.js` to point to your endpoint.

### 6. Add Google Maps

Replace the map placeholder in `contact.html`:

```html
<iframe 
    src="https://www.google.com/maps/embed?pb=YOUR_EMBED_URL" 
    width="100%" 
    height="450" 
    style="border:0;" 
    allowfullscreen="" 
    loading="lazy">
</iframe>
```

Get your embed URL from Google Maps → Share → Embed a map

## Deployment Options

### Option 1: Traditional Web Hosting
Upload all files via FTP to your web hosting provider (GoDaddy, Bluehost, HostGator, etc.)

### Option 2: Netlify (Free, Recommended)
1. Create account at netlify.com
2. Drag and drop your folder
3. Get instant HTTPS domain

### Option 3: GitHub Pages (Free)
1. Create GitHub repository
2. Upload files
3. Enable GitHub Pages in repository settings

### Option 4: Vercel (Free)
1. Create account at vercel.com
2. Connect repository or upload folder
3. Automatic deployment

## File Structure

```
interior-design-site/
│
├── index.html          # Homepage
├── portfolio.html      # Portfolio page
├── services.html       # Services page
├── about.html          # About page
├── contact.html        # Contact page
├── styles.css          # All styling
├── script.js           # Interactivity
├── README.md           # This file
│
└── images/             # Your images folder (create this)
    ├── project-1.jpg
    ├── project-2.jpg
    └── ...
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Tips

1. **Optimize Images**: Use tools like TinyPNG or ImageOptim to compress images
2. **Use WebP Format**: Convert images to WebP for better performance
3. **Lazy Loading**: Add `loading="lazy"` to images below the fold
4. **Minify CSS/JS**: Use online tools to minify for production

## Need Help?

For questions or issues:
- Check browser console for JavaScript errors
- Validate HTML at validator.w3.org
- Test responsiveness with browser dev tools

## License

This is a custom-built website for your business. You own all rights to modify and use as needed.
