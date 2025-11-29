# 💼 Portfolio Website - Adrian Batista

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

> A modern, responsive single-page portfolio website showcasing web development services. Built with pure HTML5 and CSS3 - no frameworks, no build process, just clean and efficient code.

## 🌟 Features

- **100% Vanilla** - Pure HTML5 and CSS3, zero JavaScript dependencies
- **Fully Responsive** - Mobile-first design with breakpoints for tablet (800px), desktop (992px), and large screens (1440px)
- **SEO Optimized** - Complete meta tags, Open Graph, Twitter Cards, and structured data
- **Performance First** - WebP images, preconnect optimization, minimal CSS
- **Modern Design** - Clean UI with smooth shadows, consistent spacing, and professional typography
- **Accessible** - Semantic HTML and proper ARIA attributes

## 🎨 Design System

### Color Palette
```css
Primary Dark:     #19231a  /* Navbar, hero, footer */
Primary Accent:   #7c220a  /* Buttons, highlights */
Secondary Accent: #f54c1e  /* Text highlights */
Light Background: #f9f9f9  /* Alternate sections */
Text Dark:        #434343  /* Body text on light */
Text Light:       #eeeeee  /* Text on dark backgrounds */
```

### Typography
- **Headings/Buttons**: Roboto (900 weight)
- **Body Text**: Poppins (400, 600 weights)
- Loaded via Google Fonts with preconnect optimization

### Responsive Breakpoints
- **Mobile**: < 800px (default)
- **Tablet**: 800px - 991px
- **Desktop**: 992px - 1439px
- **Large Desktop**: ≥ 1440px

## 📁 Project Structure

```
portifolio-new/
├── index.html          # Main HTML file
├── style.css           # All styles in one file
├── robots.txt          # Search engine crawling rules
├── sitemap.xml         # XML sitemap for SEO
├── SEO-REPORT.md       # SEO analysis and recommendations
├── README.md           # This file
└── images/
    ├── adrian.webp     # Profile image (optimized)
    └── hamburger.webp  # Menu icon
```

## 🚀 Quick Start

### Option 1: Direct Browser Opening
Simply open `index.html` in any modern web browser:
```bash
# Windows
start index.html

# Mac
open index.html

# Linux
xdg-open index.html
```

### Option 2: Local Development Server

**Using Python:**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

**Using Node.js (http-server):**
```bash
npx http-server -p 8000
```

**Using PHP:**
```bash
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## 📦 Deployment

This is a static website that can be deployed to any web server or CDN:

### GitHub Pages
1. Push code to GitHub repository
2. Go to Settings → Pages
3. Select branch (usually `main`) and root directory
4. Your site will be live at `https://yourusername.github.io/repository-name`

### Netlify
1. Drag and drop the project folder to [Netlify Drop](https://app.netlify.com/drop)
2. Or connect your GitHub repository for continuous deployment

### Vercel
```bash
npm i -g vercel
vercel
```

### Traditional Hosting
Upload all files via FTP/SFTP to your web server's public directory (often `public_html`, `www`, or `htdocs`).

## 🛠️ Customization Guide

### Changing Colors
All colors are defined directly in `style.css`. Search and replace:
- `#19231a` - Primary dark color
- `#7c220a` - Primary accent color
- `#f54c1e` - Secondary accent color

### Updating Content
All content is in `index.html` between lines 48-370:
- **Hero Section**: Lines 48-81
- **Features**: Lines 83-163
- **Pricing Plans**: Lines 165-248
- **About Section**: Lines 250-297
- **Contact Form**: Lines 299-370

### Adding New Sections
Follow this pattern for consistency:
```html
<section class="default-section">
  <h3>Your Section Title</h3>
  <div class="default-list">
    <!-- Your content here -->
  </div>
</section>
```

### Images
- Use `.webp` format for best performance
- Place in `/images/` directory
- Include explicit `width` and `height` attributes
- Optimize with tools like [Squoosh](https://squoosh.app/)

## 📊 Performance

- **No Build Process**: Zero compilation time
- **Minimal CSS**: Single stylesheet, no frameworks
- **Optimized Images**: WebP format with compression
- **Fast Load**: Preconnect to Google Fonts, preload critical resources
- **Mobile First**: Optimized for mobile performance

## 🔧 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Opera (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📝 Key Components

### Hero Section
Full-height viewport section with circular profile image and call-to-action button.

### Feature Cards
Numbered features with absolute-positioned badges and consistent card styling.

### Pricing Plans
Three-tier pricing with checkmarks (✓) for included features and X marks (×) for non-included items.

### Contact Form
Standard HTML5 form with validation (note: no backend handler included).

## 🐛 Known Limitations

- **Hamburger Menu**: Navigation button is visible but non-functional (no JavaScript)
- **Contact Form**: No submission handler - integrate with backend or form service like Formspree
- **No JavaScript**: Some interactive features would require JS implementation

## 📧 Contact & Social

- **Twitter**: [@adrianbatdev](https://twitter.com/adrianbatdev)
- **YouTube**: [@adrianbatdev](https://www.youtube.com/@adrianbatdev)
- **Website**: [adrianbatista.com](https://adrianbatista.com)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Built with ❤️ using pure HTML & CSS**

*No frameworks were harmed in the making of this portfolio.*
