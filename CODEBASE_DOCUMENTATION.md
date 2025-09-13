# 🍴 BistroDelight - Codebase Documentation

## 📋 Project Overview

**BistroDelight** is a professional restaurant website built with modern web technologies, featuring responsive design, accessibility compliance, and cross-browser compatibility. This documentation provides a comprehensive guide to the codebase structure and implementation details.

---

## 🏗️ Architecture Overview

### **Technology Stack**
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Custom CSS with CSS Grid & Flexbox
- **Icons**: Font Awesome 6.4.0
- **Fonts**: Playfair Display (headings), Inter (body text)
- **Performance**: Lazy loading, hardware acceleration, PWA features

### **Browser Support**
- Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- Mobile browsers: iOS Safari 14+, Chrome Mobile 90+
- Cross-browser compatibility layer for Firefox-Chrome consistency

---

## 📁 File Structure

```
bistrodelight/
├── 📄 index.html              # Homepage with hero carousel
├── 📄 about.html              # About page with restaurant story
├── 📄 menu.html               # Interactive menu with filtering
├── 📄 gallery.html            # Image gallery with lightbox
├── 📄 contact.html            # Contact form and information
├── 📄 reservations.html       # Advanced reservation system
├── 📄 README.md               # Project documentation
├── 📄 CODEBASE_DOCUMENTATION.md # This file
├── 📁 css/
│   ├── 🎨 style.css           # Main stylesheet (3,400+ lines)
│   └── 📱 responsive.css      # Mobile-first responsive design
├── 📁 js/
│   └── ⚡ main.js             # Core JavaScript functionality (980+ lines)
├── 📁 images/
│   ├── 🖼️ hero/              # Hero section images
│   ├── 🍽️ menu/              # Food photography
│   └── 🏛️ gallery/           # Restaurant interior/exterior
└── 📁 docs/                   # Technical documentation
```

---

## 🎨 CSS Architecture

### **Main Stylesheet (css/style.css)**

**Structure:**
1. **Global Variables** - CSS custom properties for colors, fonts, spacing
2. **Base Styles** - Typography, layout foundations
3. **Component Styles** - Buttons, cards, forms
4. **Section Styles** - Hero, about, menu, gallery, contact
5. **Utility Classes** - Animations, accessibility helpers
6. **Browser Compatibility** - Firefox-Chrome consistency layer

**Key Features:**
- **Color Palette**: Champagne gold (#C9A961), burgundy (#722F37), cream (#FAF7F2)
- **Typography Scale**: Responsive font sizing with clamp()
- **Animation System**: Hardware-accelerated transforms
- **Accessibility**: WCAG 2.1 AA compliance with focus indicators

### **Responsive Design (css/responsive.css)**

**Breakpoints:**
- Small Mobile: 320px - 479px
- Mobile: 480px - 767px
- Tablet: 768px - 1023px
- Desktop: 1024px - 1199px
- Large Desktop: 1200px+

**Mobile Optimizations:**
- Touch-friendly interface elements (44px minimum touch targets)
- Optimized hamburger menu with scroll lock
- Reduced animations for better performance
- Flexible grid systems

---

## ⚡ JavaScript Architecture

### **Core Functionality (js/main.js)**

**Module Structure:**
1. **Accessibility Utils** - Screen reader support, focus management
2. **Performance Utils** - Lazy loading, resource preloading
3. **Browser Compatibility** - Firefox-Chrome rendering consistency
4. **Mobile Optimizations** - Touch events, performance tuning
5. **Interactive Components** - Carousel, navigation, forms
6. **Animation System** - Intersection Observer, scroll effects

**Key Components:**

#### **Hero Carousel**
```javascript
const carousel = {
    slides: document.querySelectorAll('.carousel-slide'),
    currentSlide: 0,
    autoPlayInterval: null,
    // Methods: init, goToSlide, nextSlide, prevSlide, startAutoPlay
};
```

#### **Mobile Navigation**
```javascript
// Enhanced hamburger menu with:
// - Debounced click handling
// - Scroll lock when open
// - Keyboard navigation (Escape key)
// - Auto-close on window resize
```

#### **Menu Filtering**
```javascript
// Dynamic category filtering with:
// - Smooth animations
// - Active state management
// - Responsive grid updates
```

---

## 🎯 Key Features Implementation

### **1. Cross-Browser Compatibility**
- **Firefox-Chrome Rendering**: Detects Chrome and applies Firefox-style CSS properties
- **Color Profile Consistency**: Ensures identical background colors across browsers
- **Font Rendering**: Applies consistent antialiasing and text rendering

### **2. Performance Optimizations**
- **Lazy Loading**: Images load only when entering viewport
- **Hardware Acceleration**: Uses `transform3d()` for smooth animations
- **Passive Event Listeners**: Improves scroll performance
- **Resource Preloading**: Critical images preloaded for faster initial render

### **3. Accessibility Features**
- **Screen Reader Support**: ARIA labels, live regions, semantic HTML
- **Keyboard Navigation**: Full keyboard accessibility for all interactive elements
- **Focus Management**: Visible focus indicators, focus trapping in modals
- **Skip Links**: "Skip to main content" for screen reader users

### **4. Mobile Experience**
- **Touch Gestures**: Swipe support for carousel navigation
- **Responsive Images**: Optimized images for different screen densities
- **Touch Targets**: Minimum 44px touch targets for better usability
- **Scroll Lock**: Prevents background scrolling when mobile menu is open

---

## 🔧 Development Guidelines

### **CSS Best Practices**
- Use CSS custom properties for maintainable theming
- Follow BEM methodology for class naming
- Implement mobile-first responsive design
- Use `clamp()` for responsive typography
- Optimize for performance with `will-change` property

### **JavaScript Best Practices**
- Use modern ES6+ features with fallbacks
- Implement debouncing for performance-critical events
- Use Intersection Observer for scroll-based animations
- Handle errors gracefully with try-catch blocks
- Follow accessibility guidelines for interactive elements

### **Performance Guidelines**
- Optimize images (WebP format, appropriate sizing)
- Minimize DOM manipulation
- Use CSS transforms instead of changing layout properties
- Implement lazy loading for non-critical resources
- Use passive event listeners where appropriate

---

## 🚀 Deployment Information

### **🌐 Live Production Website**
**URL**: [https://plp-webtechnologies-classroom-july2-three.vercel.app/](https://plp-webtechnologies-classroom-july2-three.vercel.app/)

**Platform**: Vercel
**Status**: ✅ Live and Fully Functional
**Performance**: Global CDN with edge optimization
**Security**: HTTPS with SSL certificate
**Deployment**: Automatic from GitHub main branch

### **Production Optimizations**
- ✅ **Vercel Edge Network** - Global CDN for fast loading
- ✅ **Automatic HTTPS** - SSL certificate included
- ✅ **Image Optimization** - WebP format with compression
- ✅ **Gzip Compression** - Enabled by default on Vercel
- ✅ **Caching Headers** - Optimized for performance
- ✅ **Mobile Performance** - Lighthouse score optimized

### **SEO Implementation**
- Structured data (JSON-LD) for restaurant information
- Open Graph and Twitter Card meta tags
- Semantic HTML structure
- Optimized meta descriptions and titles
- XML sitemap generation

---

## 📱 Progressive Web App Features

### **PWA Capabilities**
- Service Worker for offline functionality
- Web App Manifest for installability
- Responsive design for all devices
- Fast loading with resource optimization
- Reliable performance across network conditions

---

## 🔍 Testing & Quality Assurance

### **Browser Testing**
- Cross-browser compatibility testing
- Mobile device testing (iOS, Android)
- Accessibility testing with screen readers
- Performance testing with Lighthouse
- Visual regression testing

### **Code Quality**
- Professional commenting throughout codebase
- Consistent code formatting and style
- Error handling and graceful degradation
- Performance monitoring and optimization
- Security best practices implementation

---

## 📞 Support & Maintenance

For technical support or questions about this codebase:
- Review this documentation first
- Check browser console for error messages
- Validate HTML/CSS with W3C validators
- Test accessibility with WAVE or axe tools
- Monitor performance with Chrome DevTools

---

**Last Updated**: January 13, 2025  
**Version**: 2.0.0  
**Maintained by**: BistroDelight Development Team
