# Programi Landing Page - Jira Tickets

**Design Reference**: `.claude/platforms/web/design/Programi.jpg`  
**Platform**: Web  
**Epic**: Program Landing Page Implementation  
**Created**: 2025-09-16

## TICKET 1: Hero Section Implementation

**Title**: Implement Hero Section with Navigation and Program Introduction

### Design Reference
**Design File**: `.claude/platforms/web/design/Programi.jpg`  
**Design Section**: Top hero section with navigation and "PROGRAM MRŠANJA" heading  
**Component Type**: Page header with navigation integration  
**Breakpoints**: Desktop (1200px+), Tablet (768-1199px), Mobile (<768px)

### Visual Specifications
**Layout**:
- Full-width hero section with background image/gradient
- Sticky navigation bar with logo and menu items
- Centered content with program title and description
- Right-aligned promotional badge/CTA element

**Typography**:
- Main heading: Bold, large display font (48px desktop, 32px mobile)
- Subheading: Medium weight, readable size (18px desktop, 16px mobile)
- Navigation: Clean, medium weight (16px)
- CTA text: Bold, contrasting (14px uppercase)

**Colors**:
- Background: Dark gradient or image overlay
- Text: White/light text for contrast
- CTA elements: Brand accent colors (yellow/orange)
- Navigation: Semi-transparent background with hover effects

### Content Management Requirements

#### Static Content
- [x] **Navigation Menu**: 
  - Logo/brand mark
  - Menu items: Programs, About, Contact, Login
  - Language selector (if multi-language support)
  - Mobile hamburger menu

- [x] **Hero Content**:
  - Main headline: "PROGRAM MRŠANJA" (Weight Loss Program)
  - Supporting description text
  - Key benefit points or USPs
  - Primary CTA button

#### Dynamic Content
- [x] **User State**: Show different navigation for logged-in users
- [x] **Promotional Elements**: Configurable promotional badges or announcements
- [x] **A/B Testing**: Support for headline/CTA variations

### Responsive Design Requirements
- [x] **Mobile Navigation**: Collapsible hamburger menu with smooth animations
- [x] **Hero Scaling**: Proportional scaling of hero content across breakpoints
- [x] **Touch Optimization**: Minimum 44px touch targets for all interactive elements
- [x] **Performance**: Optimized images with WebP support and lazy loading

### Technical Implementation
**Framework**: Responsive HTML/CSS with JavaScript for navigation interactions  
**Images**: Optimized hero images with fallbacks and responsive sizing  
**Navigation**: Semantic menu structure with ARIA labels for accessibility  
**Performance**: Critical CSS inlining and progressive image loading

### Acceptance Criteria
- [x] **Navigation Functionality**: All menu items navigate correctly with active states
- [x] **Responsive Behavior**: Hero section scales properly across all device sizes
- [x] **Performance**: Page loads within 3 seconds on 3G connection
- [x] **Accessibility**: WCAG 2.1 AA compliance with proper headings and navigation
- [x] **Cross-browser**: Works consistently across Chrome, Firefox, Safari, Edge

---

## TICKET 2: Three-Tier Pricing Cards Implementation

**Title**: Create Program Pricing Cards with Feature Comparison (60KM/80KM/100KM)

### Design Reference
**Design File**: `.claude/platforms/web/design/Programi.jpg`  
**Design Section**: Three pricing tier cards section  
**Component Type**: Pricing comparison cards with feature lists  
**Breakpoints**: Desktop 3-column, Tablet 2-column, Mobile stacked

### Visual Specifications
**Layout**:
- Three distinct cards with visual hierarchy (basic, popular, premium)
- Card elevation/shadows to create depth
- Featured/recommended card with distinct highlighting
- Consistent spacing and alignment across all cards

**Typography**:
- Pricing: Large, bold numerals (36px) with currency
- Plan names: Medium weight headings (24px)
- Feature lists: Regular weight, readable (14px)
- CTA buttons: Bold, action-oriented (16px)

**Colors**:
- Card backgrounds: White/light with subtle shadows
- Popular card: Accent color border or background
- Pricing text: High contrast for readability
- CTA buttons: Brand colors with hover states

### Content Management Requirements

#### Static Content Structure
- [x] **60KM Plan (Basic)**:
  - Price display and billing period
  - Core feature list (8-10 key features)
  - CTA button: "POGLEDAJ" or "ODABERI PLAN"
  - "Najosnovniji" or similar descriptor

- [x] **80KM Plan (Popular)**:
  - Highlighted as "PREPORUČENO" or "NAJPOPULARNIJI"
  - Enhanced feature list with additional benefits
  - Prominent CTA styling
  - Value proposition emphasis

- [x] **100KM Plan (Premium)**:
  - Full feature access indicator
  - Premium support mentions
  - All-inclusive messaging
  - Premium CTA styling

#### Dynamic Content Features
- [x] **Pricing Updates**: Backend-controlled pricing for easy A/B testing
- [x] **Feature Toggles**: Show/hide features based on business needs
- [x] **Promotional Pricing**: Support for discount displays and limited-time offers
- [x] **User Personalization**: Highlight recommended plans based on user profile

### Interactive Elements
- [x] **Card Hover Effects**: Subtle elevation changes on hover
- [x] **Feature Tooltips**: Expandable explanations for complex features
- [x] **Comparison Highlights**: Visual emphasis when comparing features
- [x] **CTA Tracking**: Click tracking for conversion analytics

### Technical Implementation
**Framework**: CSS Grid/Flexbox for responsive card layout  
**Interactions**: JavaScript for hover effects and feature comparisons  
**Data Structure**: JSON-based pricing configuration for easy updates  
**Analytics**: Event tracking for card interactions and CTA clicks

### Acceptance Criteria
- [x] **Responsive Layout**: Cards stack properly on mobile, maintain alignment on desktop
- [x] **Feature Parity**: All advertised features accurately reflect actual program offerings
- [x] **CTA Functionality**: All buttons lead to correct signup/checkout flows
- [x] **Visual Hierarchy**: Popular plan clearly stands out without overwhelming other options
- [x] **Loading Performance**: Cards render quickly with smooth animations

---

## TICKET 3: Video Testimonial Section Implementation

**Title**: Implement Video Player Section with Testimonial Integration

### Design Reference
**Design File**: `.claude/platforms/web/design/Programi.jpg`  
**Design Section**: Video testimonial section with custom player  
**Component Type**: Embedded video player with overlay controls  
**Integration**: Vimeo player integration (existing platform dependency)

### Visual Specifications
**Layout**:
- Full-width video container with 16:9 aspect ratio
- Custom play button overlay with brand styling
- Optional testimonial text overlay or adjacent content
- Responsive scaling maintaining aspect ratio

**Player Styling**:
- Custom play button with brand colors
- Minimal control bar with brand accent colors
- Loading states with brand-consistent spinners
- Error states with helpful messaging

**Typography** (for any text overlays):
- Testimonial quotes: Italic, medium size (18px)
- Attribution: Regular weight, smaller (14px)
- Call-to-action text: Bold, contrasting

### Content Management Requirements

#### Video Content
- [x] **Primary Video**: Success story or program demonstration
- [x] **Fallback Options**: Multiple video qualities for different connection speeds
- [x] **Thumbnail Image**: High-quality poster frame for initial load
- [x] **Captions/Subtitles**: Croatian captions for accessibility

#### Dynamic Elements
- [x] **Video Rotation**: Support for multiple testimonial videos
- [x] **Personalized Content**: Different videos based on user segment
- [x] **A/B Testing**: Test different video content for conversion optimization
- [x] **Analytics Integration**: Track video engagement metrics

### Technical Requirements
**Video Platform**: Vimeo integration (matching existing platform usage)  
**Player Customization**: Branded player controls and styling  
**Performance**: Progressive loading and adaptive bitrate streaming  
**Analytics**: Video completion rates and engagement tracking

### Vimeo Integration Specifics
- [x] **API Integration**: Use Vimeo Player API for custom controls
- [x] **Privacy Settings**: Ensure videos are properly configured for public viewing
- [x] **Brand Compliance**: Remove Vimeo branding where possible
- [x] **Mobile Optimization**: Touch-friendly controls for mobile devices

### Acceptance Criteria
- [x] **Video Playback**: Smooth playback across all devices and browsers
- [x] **Custom Styling**: Player matches Fitness Anny brand guidelines
- [x] **Loading Performance**: Video loads quickly with appropriate fallbacks
- [x] **Accessibility**: Keyboard navigation and screen reader compatibility
- [x] **Analytics**: Comprehensive tracking of video engagement metrics

---

## TICKET 4: Detailed Program Comparison Table

**Title**: Build "Usporedi programe" Feature Comparison Matrix

### Design Reference
**Design File**: `.claude/platforms/web/design/Programi.jpg`  
**Design Section**: "Usporedi programe" comparison table section  
**Component Type**: Detailed feature matrix with checkmarks and highlights  
**Functionality**: Interactive comparison table with filtering/sorting capabilities

### Visual Specifications
**Layout**:
- Three-column comparison (60KM, 80KM, 100KM programs)
- Feature categories with visual grouping
- Clear checkmark/cross indicators for feature availability
- Responsive table that works on mobile devices

**Typography**:
- Section heading: Bold, large (32px desktop, 24px mobile)
- Feature categories: Medium weight subheadings (18px)
- Feature items: Regular weight, readable (14px)
- Program headers: Bold, prominent (20px)

**Interactive Elements**:
- Checkmarks: Green checkmarks for included features
- Missing features: Gray crosses or empty indicators
- Hover states: Highlight rows on hover for better readability
- Mobile accordion: Collapsible sections for mobile viewing

### Content Management Requirements

#### Feature Categories Structure
- [x] **Program Overview**:
  - Duration (weeks)
  - Workout frequency
  - Difficulty level
  - Equipment needed

- [x] **Support Features**:
  - Personal trainer access
  - Nutritionist consultation
  - 24/7 chat support
  - Group community access

- [x] **Content Access**:
  - Workout video library
  - Meal planning guides
  - Recipe collections
  - Progress tracking tools

- [x] **Additional Benefits**:
  - Mobile app access
  - Offline content download
  - Expert webinars
  - Personalized meal plans

#### Dynamic Content Management
- [x] **Feature Toggle System**: Easy enable/disable of features per program
- [x] **Content Updates**: Backend management of feature descriptions
- [x] **Seasonal Promotions**: Highlight special features during promotions
- [x] **User Customization**: Show relevant features based on user preferences

### Technical Implementation
**Responsive Design**: CSS Grid for desktop, accordion pattern for mobile  
**Data Management**: JSON-based feature matrix for easy updates  
**Interactions**: JavaScript for smooth hover effects and mobile accordion  
**Accessibility**: Proper table semantics with ARIA labels

### Mobile Experience
- [x] **Accordion Design**: Tap to expand each program's features
- [x] **Swipe Navigation**: Horizontal swipe between program columns
- [x] **Sticky Headers**: Program names stay visible while scrolling
- [x] **Touch Optimization**: Large touch targets for mobile interaction

### Acceptance Criteria
- [x] **Data Accuracy**: All features accurately reflect actual program offerings
- [x] **Responsive Function**: Table works seamlessly across all device sizes
- [x] **Performance**: Fast loading with smooth animations
- [x] **Accessibility**: Screen reader compatible with proper table structure
- [x] **Maintenance**: Easy content updates through backend interface

---

## TICKET 5: FAQ Section Implementation

**Title**: Create "Česta pitanja" Accordion FAQ Section

### Design Reference
**Design File**: `.claude/platforms/web/design/Programi.jpg`  
**Design Section**: Yellow "Česta pitanja" FAQ section  
**Component Type**: Expandable accordion with Croatian content  
**Styling**: Brand yellow background with accessible contrast

### Visual Specifications
**Layout**:
- Full-width section with brand yellow background
- Accordion-style expandable questions
- Clean typography hierarchy for questions and answers
- Proper spacing for readability and touch interaction

**Typography**:
- Section heading: Bold, large (32px desktop, 24px mobile)
- Questions: Medium weight (18px) with expand/collapse indicators
- Answers: Regular weight, readable (16px) with proper line spacing
- Expand icons: Clear visual indicators (+/- or arrows)

**Colors**:
- Background: Brand yellow (#FFD700 or similar)
- Text: Dark text for contrast and readability
- Hover states: Subtle darkening or highlighting
- Active states: Clear indication of expanded items

### Content Management Requirements

#### Core FAQ Content (Croatian)
- [x] **Program Questions**:
  - "Kako pristupam treningu?" (How do I access training?)
  - "Koliko traje program?" (How long is the program?)
  - "Kakva je komunikacija sa stručnjacima?" (What communication with experts?)
  - "Mogu li da prekinem predjo početak?" (Can I pause before starting?)

- [x] **Support Questions**:
  - "Šta ako nemam vremena za sve treninge?" (What if I don't have time for all workouts?)
  - "Da li mogu da kombinujem programe?" (Can I combine programs?)
  - "Kakva je podrška tokom programa?" (What support during the program?)

- [x] **Technical Questions**:
  - "Koje aplikacije koristim?" (Which apps do I use?)
  - "Da li mogu da skinem sadržaj?" (Can I download content?)
  - "Šta ako imam tehničkih problema?" (What about technical issues?)

#### Dynamic Content Features
- [x] **Content Updates**: Easy backend editing of FAQ content
- [x] **Usage Analytics**: Track which questions are most frequently expanded
- [x] **Search Function**: Allow users to search within FAQ content
- [x] **Related Questions**: Suggest related FAQs based on user behavior

### Interactive Functionality
**Accordion Behavior**: Smooth expand/collapse animations  
**Multiple Expand**: Allow multiple questions open simultaneously  
**Deep Linking**: URL anchors to specific FAQ items  
**Search Integration**: Filter FAQ items based on search terms

### Technical Implementation
**Accessibility**: Proper ARIA attributes for screen readers  
**Performance**: Smooth animations without blocking UI  
**SEO**: Structured data markup for FAQ schema  
**Analytics**: Track FAQ interaction patterns for content optimization

### Acceptance Criteria
- [x] **Content Accuracy**: All FAQs reflect current program policies and procedures
- [x] **Smooth Animation**: Accordion opens/closes without visual glitches
- [x] **Mobile Optimization**: Touch-friendly interaction on all devices
- [x] **Accessibility**: Keyboard navigation and screen reader compatibility
- [x] **Performance**: Fast loading and responsive interactions

---

## TICKET 6: Responsive Design System Implementation

**Title**: Implement Mobile-First Responsive Design Across All Sections

### Design Reference
**Design File**: `.claude/platforms/web/design/Programi.jpg`  
**Scope**: Complete responsive implementation for all page sections  
**Approach**: Mobile-first design with progressive enhancement  
**Breakpoints**: Mobile (<768px), Tablet (768-1199px), Desktop (1200px+)

### Responsive Strategy
**Mobile-First Approach**:
- Base styles optimized for mobile devices
- Progressive enhancement for larger screens
- Touch-first interaction patterns
- Optimized content hierarchy for small screens

**Performance Priorities**:
- Critical CSS for above-the-fold content
- Lazy loading for images and non-critical elements
- Optimized font loading and rendering
- Minimal JavaScript for core functionality

### Breakpoint Implementation

#### Mobile (<768px)
- [x] **Navigation**: Hamburger menu with slide-out drawer
- [x] **Hero Section**: Stacked content with large touch targets
- [x] **Pricing Cards**: Single column, card stacking
- [x] **Video Player**: Full-width with touch-optimized controls
- [x] **Comparison Table**: Accordion-style with swipe navigation
- [x] **FAQ Section**: Optimized accordion with larger touch areas

#### Tablet (768-1199px)
- [x] **Navigation**: Condensed horizontal menu
- [x] **Hero Section**: Balanced two-column layout
- [x] **Pricing Cards**: Two-column grid with featured card prominence
- [x] **Video Player**: Maintained aspect ratio with sidebar content
- [x] **Comparison Table**: Simplified table with horizontal scroll
- [x] **FAQ Section**: Two-column accordion layout

#### Desktop (1200px+)
- [x] **Navigation**: Full horizontal menu with dropdowns
- [x] **Hero Section**: Full layout with sidebar elements
- [x] **Pricing Cards**: Three-column grid with hover effects
- [x] **Video Player**: Integrated layout with surrounding content
- [x] **Comparison Table**: Full table display with hover states
- [x] **FAQ Section**: Multi-column layout with expanded content

### Performance Optimization
**Image Optimization**:
- WebP format with fallbacks
- Responsive image sizes for different breakpoints
- Lazy loading implementation
- Progressive JPEG for hero images

**CSS Optimization**:
- Critical CSS inlining
- Non-critical CSS lazy loading
- CSS Grid and Flexbox for layout
- Minimal custom properties usage

**JavaScript Optimization**:
- Minimal vanilla JavaScript for interactions
- Progressive enhancement approach
- Async loading for non-critical features
- Service worker for offline functionality

### Accessibility Compliance
- [x] **WCAG 2.1 AA Standards**: Full compliance across all breakpoints
- [x] **Keyboard Navigation**: Complete keyboard accessibility
- [x] **Screen Reader Support**: Proper semantic markup and ARIA labels
- [x] **Color Contrast**: Minimum 4.5:1 contrast ratio for all text
- [x] **Focus Management**: Clear focus indicators and logical tab order

### Technical Implementation
**CSS Framework**: Custom responsive system with CSS Grid and Flexbox  
**JavaScript**: Vanilla JavaScript for interactions, no heavy frameworks  
**Testing**: Cross-browser testing across all major browsers and devices  
**Performance**: Target <3 second load time on 3G connection

### Acceptance Criteria
- [x] **Performance**: Page Speed Insights score >90 on mobile and desktop
- [x] **Responsiveness**: Perfect display across all target breakpoints
- [x] **Accessibility**: WCAG 2.1 AA compliance verified with testing tools
- [x] **Cross-browser**: Consistent experience across Chrome, Firefox, Safari, Edge
- [x] **Touch Optimization**: All interactive elements meet 44px minimum touch target

---

## TICKET 7: Footer and Social Integration

**Title**: Implement Footer Section with Social Links and Brand Information

### Design Reference
**Design File**: `.claude/platforms/web/design/Programi.jpg`  
**Design Section**: Footer section with social media links and contact information  
**Component Type**: Site-wide footer with social integration  
**Breakpoints**: Responsive footer layout across all devices

### Visual Specifications
**Layout**:
- Multi-column footer with organized information sections
- Social media icons with brand-consistent styling
- Copyright and legal information
- Contact information and quick links

**Typography**:
- Footer headings: Medium weight (16px)
- Link text: Regular weight (14px) 
- Copyright text: Smaller, subdued (12px)
- Social icons: Consistent sizing (24px or larger for touch)

**Colors**:
- Background: Dark footer background (#1a1a1a or similar)
- Text: Light text for contrast (#ffffff, #cccccc)
- Social icons: Brand colors or white with hover effects
- Links: Hover states with brand accent colors

### Content Management Requirements

#### Static Content
- [x] **Company Information**: 
  - "Fitness Anny" brand name
  - Tagline or mission statement
  - Contact information (email, phone)
  - Physical address if applicable

- [x] **Social Media Links**:
  - Facebook: "@FitnessAnny"
  - Instagram: "@fitnessannyofficial" 
  - YouTube: Fitness Anny channel
  - TikTok: @fitnessanny (if applicable)

- [x] **Quick Links**:
  - Programs
  - About Us (O nama)
  - Contact (Kontakt)  
  - FAQ
  - Privacy Policy (Pravila privatnosti)
  - Terms of Service (Uvjeti korištenja)

#### Dynamic Content
- [x] **Social Feed Integration**: Latest posts from social media accounts
- [x] **Newsletter Signup**: Email subscription with backend integration
- [x] **Contact Form**: Quick contact form integration
- [x] **App Download Links**: Dynamic links to iOS/Android apps

### Social Media Integration
- [x] **Open Graph Tags**: Proper meta tags for social sharing
- [x] **Analytics Tracking**: Track social link clicks for engagement metrics
- [x] **Share Buttons**: Allow users to share programs page on social media
- [x] **Social Proof**: Follower counts or social testimonials

### Technical Implementation
**Framework**: Semantic HTML with CSS for responsive footer grid  
**Social Icons**: SVG icons for crisp display at all sizes  
**Performance**: Optimized loading with minimal external dependencies  
**Analytics**: Track footer engagement and social media clicks

### Acceptance Criteria
- [x] **Social Integration**: All social media links functional and tracking clicks
- [x] **Responsive Layout**: Footer adapts properly across all breakpoints  
- [x] **Brand Consistency**: Footer styling matches overall site design
- [x] **Legal Compliance**: Required legal links and information included
- [x] **Performance**: Footer loads without impacting page speed

---

## Implementation Notes

### Development Priority
1. **Hero Section + Navigation** (Foundation)
2. **Pricing Cards** (Core conversion element)
3. **Responsive Framework** (Essential for mobile users)
4. **Comparison Table** (Decision support)
5. **Video Section** (Social proof)
6. **FAQ Section** (Objection handling)
7. **Footer** (Brand completion)

### Technical Dependencies
- **Vimeo Integration**: Existing platform dependency for video content
- **Backend API**: Pricing and feature data management
- **Analytics**: Conversion tracking and user behavior analysis
- **CMS**: Content management for Croatian localization

### Success Metrics
- **Page Load Speed**: <3 seconds on 3G
- **Mobile Usability**: 95%+ mobile-friendly score
- **Conversion Rate**: Track pricing card clicks and signups
- **User Engagement**: FAQ expansion rates and video completion
- **Accessibility**: WCAG 2.1 AA compliance verification