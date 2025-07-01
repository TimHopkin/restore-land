# Enhanced Hero Image System - Restore Land

## Overview
The hero section has been upgraded with a dynamic background system that showcases the vision of Restore Land - balancing future technology with natural beauty in British landscapes. The system creates a more inspiring, engaging hero experience while maintaining the sophisticated design and brand consistency.

## Features Implemented

### 🎨 **Dynamic Background System**
- **4 Unique Hero Themes**: Each embodying the "future meets nature" philosophy
- **Automatic Rotation**: Images rotate every 15-25 seconds (device-optimized timing)
- **Smooth Transitions**: CSS-powered fade transitions between backgrounds
- **Ken Burns Effect**: Subtle zoom and movement for visual interest

### 🚀 **Performance Optimizations**
- **Mobile-First**: Reduced animations and optimized timing for mobile devices
- **Reduced Motion Support**: Respects user accessibility preferences
- **Visibility API**: Pauses animations when page is hidden
- **Hardware Detection**: Adjusts performance based on device capabilities

### 📱 **Responsive Design**
- **Mobile Optimizations**: Simplified animations and optimized text sizing
- **Tablet Support**: Medium-device specific optimizations
- **High DPI Support**: Enhanced rendering for retina displays
- **Accessibility**: Proper ARIA labels and contrast ratios

### ✨ **Enhanced Visual Effects**
- **Improved Overlays**: Brand-colored gradient overlays for better text readability
- **Enhanced Particles**: More sophisticated floating particle animations
- **Text Glow Effects**: Subtle glow effects on hero text for better impact
- **Brand Integration**: All effects use the official Restore Land color palette

## Hero Image Themes

### 1. **Regenerative Farm** (hero-bg-1)
- **Theme**: Modern farming with integrated technology
- **Elements**: Solar panels, wind turbine, modern farming equipment
- **Mood**: Prosperous, technological, natural
- **Use Case**: Default/primary hero, appeals to farmers and landowners

### 2. **Energy Landscape** (hero-bg-2)
- **Theme**: Clean energy in British countryside
- **Elements**: Wind turbines at sunrise, wildflower meadows, sun
- **Mood**: Forward-thinking, hopeful, pristine
- **Use Case**: Sustainability-focused campaigns, appeals to climate advocates

### 3. **Community Farming** (hero-bg-3)
- **Theme**: Community-led land restoration
- **Elements**: People working together, market gardens, village background
- **Mood**: Collaborative, productive, beautiful
- **Use Case**: Community events, local engagement campaigns

### 4. **Soil Restoration** (hero-bg-4)
- **Theme**: Soil health and regeneration
- **Elements**: Rich soil cross-section, root systems, mycorrhizal networks
- **Mood**: Scientific, natural, abundant
- **Use Case**: Technical content, appeals to researchers and soil health advocates

## Technical Implementation

### CSS Structure
```css
.hero {
    /* Dynamic background container */
}

.hero-background {
    /* Background image layer with transitions */
    transition: opacity 1.5s ease-in-out;
    transform: scale(1.05); /* Ken Burns base */
}

.hero-background.hero-bg-1 { /* Regenerative farm */ }
.hero-background.hero-bg-2 { /* Energy landscape */ }
.hero-background.hero-bg-3 { /* Community farming */ }
.hero-background.hero-bg-4 { /* Soil restoration */ }

.hero::before {
    /* Enhanced overlay system */
    background: brand-colored gradients + dark overlay;
}

.hero::after {
    /* Floating particles animation */
    animation: floatingParticles 25s linear infinite;
}
```

### JavaScript API
```javascript
// Change hero background programmatically
changeHeroBackground(index, animate = true);

// Hero image data
const heroImages = [
    { class: 'hero-bg-1', name: 'Regenerative Farm', description: '...' },
    // ... other themes
];

// Automatic initialization
initializeHeroSystem();
```

## Usage Guidelines

### When to Use Different Hero Images

1. **General/Homepage**: Use rotation or Regenerative Farm (hero-bg-1)
2. **Energy/Climate Content**: Energy Landscape (hero-bg-2)
3. **Community Events**: Community Farming (hero-bg-3)
4. **Technical/Scientific**: Soil Restoration (hero-bg-4)

### Performance Considerations

- **Mobile**: Automatic performance optimizations applied
- **Low-End Devices**: Reduced animation frequency and complexity
- **Accessibility**: Respects `prefers-reduced-motion` setting
- **Visibility**: Pauses when page is hidden to save resources

### Development/Testing

Add `#hero-controls` to URL to show hero selection buttons:
```
https://restoreland.uk/#hero-controls
```

### Customization Options

1. **Rotation Timing**: Modify `rotationInterval` in JavaScript
2. **Transition Speed**: Adjust CSS `transition` duration
3. **Ken Burns**: Enable/disable via `.ken-burns` class
4. **Particle Effects**: Modify `.hero::after` animation

## Future Enhancements

### Phase 2: Production Images
Replace SVG placeholders with high-quality photography:
- Commission professional landscape photography
- Implement WebP format with JPEG fallbacks
- Add 2x resolution versions for retina displays
- Implement proper image preloading

### Phase 3: Advanced Features
- **Video Backgrounds**: Option for hero video backgrounds
- **Seasonal Variations**: Automatic seasonal hero image selection
- **User Preferences**: Remember user's preferred hero theme
- **Campaign Integration**: Dynamic hero based on active campaigns

### Phase 4: Performance Optimization
- **Intersection Observer**: Only animate when hero is visible
- **Service Worker**: Cache hero images for offline experience
- **WebP Support**: Automatic format selection based on browser support
- **CDN Integration**: Serve images from optimized CDN

## Brand Compliance

All hero images and effects strictly follow Restore Land brand guidelines:
- **Color Palette**: Only approved brand colors used in overlays and effects
- **Typography**: Maintains existing font hierarchy and styling
- **Voice**: Images support the "practical patriotism" messaging
- **Accessibility**: Proper contrast ratios and motion preferences respected

## Browser Support

- **Modern Browsers**: Full feature support (Chrome 60+, Firefox 60+, Safari 12+)
- **Legacy Browsers**: Graceful degradation to static background
- **Mobile Browsers**: Optimized experience with reduced animations
- **Accessibility**: Screen reader support with proper ARIA labels

## File Structure

```
/
├── initial.html                 # Main implementation
├── brand-assets/
│   ├── hero-images/
│   │   ├── README.md           # Hero image guidelines
│   │   └── (future image files)
└── HERO_SYSTEM.md              # This documentation
```

## Contact & Support

- **Technical Questions**: Reference this documentation and code comments
- **New Hero Images**: Email hello@restoreland.uk with requirements
- **Brand Compliance**: Ensure all new images follow brand guidelines
- **Performance Issues**: Check browser DevTools and reduce motion if needed

---

*Last updated: January 2025*
*System version: 1.0.0*