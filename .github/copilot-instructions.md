# Portfolio Website - AI Agent Instructions

## Project Overview
This is a single-page portfolio website for a software development agency. The site is a **vanilla HTML/CSS static website** with no build process, JavaScript framework, or backend dependencies.

## Architecture
- **Tech Stack**: Pure HTML5, CSS3, no JavaScript
- **Structure**: Single `index.html` with inline sections, single `style.css` for all styles
- **Assets**: `/images/` contains `.webp` optimized images (adrian.webp, hamburger.webp)
- **Deployment**: Static files - can be deployed to any web server or CDN

## Design System

### Color Palette
- Primary Dark: `#19231a` (navbar, hero background, footer)
- Primary Accent: `#7c220a` (buttons, highlights, brand elements)
- Secondary Accent: `#f54c1e` (text highlights)
- Light Background: `#f9f9f9` / `#efefef` (alternate sections)
- Text: `#eeeeee` (on dark), `#434343` (on light)

### Typography
- **Headings/Buttons**: `Roboto` (900 weight), uppercase for nav/buttons
- **Body**: `Poppins` (400, 600 weights)
- Fonts loaded via Google Fonts with preconnect optimization

### Responsive Breakpoints
Uses mobile-first with these specific breakpoints:
- Default: < 800px (mobile)
- `@media (min-width: 800px)`: Tablet - switches hero to row-reverse layout
- `@media (min-width: 992px)`: Desktop
- `@media (min-width: 1440px)`: Large desktop - hero image scales to 400px

## Layout Patterns

### Section Structure
All main sections use `.default-section` class with this pattern:
```html
<section class="default-section [modifier-class]">
  <h3>Section Title</h3>
  <div class="default-list">
    <!-- Grid items here -->
  </div>
</section>
```

- `.default-list`: Flexbox container with `flex-wrap`, 20px gap, centers items
- Alternating backgrounds: white → `#f9f9f9` → white pattern
- Specific modifiers: `.features-section`, `.pricing-section`, `.contact-section`, `.about-section`

### Hero Section
- Full viewport height (`100vh`)
- Flex layout that switches between column (mobile) and row-reverse (desktop)
- Circular profile image with fixed sizes per breakpoint
- `.hero-align` constrains content width (max 350-600px depending on screen)

### Numbered Features Pattern
`.feature` items use absolute positioning for numbered badges:
- Circle badge with `#7c220a` background positioned outside top-left
- Content uses `padding-left: 30px` to accommodate badge
- Badge sized relative to `1rem + 20px` base unit

## Component Conventions

### Cards
- All cards (`.benefit`, `.plan`, `.feature`) use consistent box-shadow:
  ```css
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px,
              rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
  ```

### Buttons
- Always full-width on mobile (`width: 100%`)
- Use `.button` class or inline button styles
- Standard: `#7c220a` background, white text, uppercase, 5px border-radius

### Lists (Pricing Plans)
- `.included` items: checkmark (✓ `\2713`) prefix, standard color
- `.non-included` items: X mark (× `\00D7`) prefix, line-through, muted color

### SVG Icons
- Inline SVG for icons and decorative elements
- Fill color matches context: `#7c220a` on light backgrounds, `#f9f9f9` on dark

## Editing Guidelines

1. **Responsive changes**: Always update ALL breakpoints when modifying hero section sizing
2. **New sections**: Follow `.default-section` + `.default-list` pattern for consistency
3. **Text content**: Main content in `index.html` lines 48-370 (hero through contact form)
4. **Color changes**: Update color palette constants across entire stylesheet - no CSS variables used
5. **Forms**: Contact form uses standard inputs with 1px gray border, 5px border-radius
6. **Images**: Use `.webp` format for optimization, include explicit width/height attributes

## Known Issues/TODOs
- Hamburger menu button in navbar is non-functional (no JavaScript)
- Contact form has no submission handler
- Commented out old media query block around line 24 of `style.css`
- Social links point to real profiles (Twitter: @adrianbatdev, YouTube: @adrianbatdev)

## Development Workflow
No build process required:
1. Edit HTML/CSS directly
2. Open `index.html` in browser to preview
3. Test across different viewport sizes
4. Deploy by copying files to web server
