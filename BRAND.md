# Restore Land Brand Rules & Guidelines

This document serves as the technical implementation guide for maintaining brand consistency in the Restore Land codebase and all digital communications.

## Quick Reference

### Colors (CSS Variables)
```css
:root {
  --restore-green: #16a34a;    /* Primary brand color */
  --growth-green: #10b981;     /* Interactive elements */
  --deep-forest: #065f46;      /* Dark text, emphasis */
  --light-growth: #34d399;     /* Backgrounds, accents */
  --vibrant-earth: #059669;    /* Supporting elements */
  --fresh-mint: #6ee7b7;       /* Light accents */
  --rich-black: #1a1a1a;       /* Primary text */
  --warm-gray: #4b5563;        /* Secondary text */
  --clean-white: #fafafa;      /* Background */
}
```

### Typography
```css
/* Headlines */
font-family: 'Playfair Display', serif;
font-weight: 700-900;
letter-spacing: -1px to -3px (for large sizes);

/* Body Text */
font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
font-weight: 400-700;
line-height: 1.5-1.7;
```

### Logo Implementation
```html
<!-- Primary Logo -->
<svg><!-- Use restore-land-primary.svg --></svg>

<!-- Text-based Logo (when SVG not available) -->
<h1 style="font-family: 'Playfair Display', serif; font-weight: 900; color: #16a34a; letter-spacing: -1px;">
  RESTORE LAND
</h1>
```

## Brand Implementation Rules

### 1. Color Usage
- **Primary Green (#16a34a)**: Logo, main headings, primary buttons, key CTAs
- **Growth Green (#10b981)**: Hover states, interactive elements, secondary buttons
- **Deep Forest (#065f46)**: Important text, dark backgrounds, emphasis
- **Never** use colors outside the approved palette
- **Always** ensure sufficient contrast (4.5:1 minimum for text)

### 2. Typography Hierarchy
```css
/* H1 - Hero Headlines */
font-size: clamp(3.5rem, 10vw, 8rem);
font-family: 'Playfair Display', serif;
font-weight: 900;

/* H2 - Section Headlines */
font-size: clamp(2.5rem, 6vw, 4rem);
font-family: 'Playfair Display', serif;
font-weight: 700;

/* H3 - Subsection Headlines */
font-size: clamp(1.5rem, 4vw, 2rem);
font-family: 'Playfair Display', serif;
font-weight: 700;

/* Body Text */
font-size: 1rem;
font-family: 'Inter', sans-serif;
font-weight: 400;
line-height: 1.6;

/* Large Text */
font-size: 1.3rem;
font-weight: 400-600;
```

### 3. Interactive Elements
```css
/* Primary Button */
.cta-button {
  background: linear-gradient(135deg, #10b981, #059669);
  color: white;
  padding: 20px 45px;
  border-radius: 60px;
  font-weight: 700;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.cta-button:hover {
  transform: translateY(-4px) scale(1.05);
  box-shadow: 0 20px 50px rgba(16, 185, 129, 0.5);
}
```

### 4. Spacing System
```css
/* Use consistent spacing multipliers */
--spacing-xs: 8px;
--spacing-sm: 16px;
--spacing-md: 24px;
--spacing-lg: 32px;
--spacing-xl: 48px;
--spacing-2xl: 64px;
--spacing-3xl: 96px;
```

## Content Guidelines

### Language Standards
- **British English**: All content must use British English spelling and terminology
- **Consistency**: Maintain consistent language standards across all platforms and materials
- **Examples**: Use "colour" not "color", "centre" not "center", "organisation" not "organization", "optimise" not "optimize", "behaviour" not "behavior"

### Voice & Tone
- **Direct**: "This isn't about the environment. It's about prosperity."
- **Urgent**: "Simple. Clear. Urgent."
- **Practical**: "This isn't utopian dreaming - it's practical patriotism."
- **Confident**: "Britain will build the world's first..."

### Key Messaging
1. **Core Promise**: "Restore Land" - the two-word revolution
2. **Value Proposition**: Focus on prosperity, not just environment
3. **Evidence**: Use specific, measurable outcomes
4. **Call to Action**: Clear next steps for different audiences

### Content Hierarchy
1. **Headline**: Clear benefit or transformation
2. **Subheadline**: Supporting detail or urgency
3. **Body**: Specific evidence and practical steps
4. **CTA**: Direct action with clear value

## File Organisation

### Brand Assets Structure
```
brand-assets/
├── logos/                  # All logo variants
├── colours/                # Colour swatches and CSS
├── fonts/                  # Typography assets
├── templates/              # Social media and presentation templates
├── icons/                  # Favicons and app icons
└── README.md              # Asset usage guidelines
```

### Naming Conventions
- Logo files: `restore-land-[variant].[format]`
- Colour files: `restore-land-colours.[format]`
- Templates: `[platform]-template.[format]`

## Implementation Checklist

### New Page/Component Checklist
- [ ] Uses approved colour palette
- [ ] Implements correct typography hierarchy
- [ ] Includes proper meta tags for social sharing
- [ ] Maintains consistent spacing system
- [ ] Follows voice and tone guidelines
- [ ] Includes appropriate CTAs with brand styling

### Social Media Checklist
- [ ] Uses 1200x630px dimensions for sharing
- [ ] Includes Restore Land branding
- [ ] Maintains readable text contrast
- [ ] Uses approved colour scheme
- [ ] Includes appropriate CTAs

### Brand Compliance Review
Before publishing any content:
1. **Visual**: Does it use our colours and fonts correctly?
2. **Content**: Does it sound like Restore Land (direct, urgent, practical)?
3. **Technical**: Are meta tags and structured data correct?
4. **Accessibility**: Is contrast sufficient and text readable?

## Contact for Brand Questions
- Technical implementation: Review this document and brand-guidelines.html
- New asset requests: hello@restoreland.uk
- Brand compliance questions: Reference this document first

## Last Updated
2025-01-01 - Initial brand system implementation