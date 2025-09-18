# Jelovnici Migration to Prehrana Tab — Feature Specification

## Background Context

**Current state:** Daily Jelovnici (menus) are published by operators in group chats as manually designed images. This creates chat clutter for users and requires significant manual design work for each menu publication.

**Problem:**
- Group chats become cluttered with daily menu posts, diluting their primary purpose of community interaction
- Operators spend excessive time manually designing menu graphics instead of focusing on content creation
- Users struggle to find specific menus in chat history
- No consistent branding or design standards across menu publications
- Operators cannot efficiently filter menus by user goals during creation

**Goal:** Migrate Jelovnici from group chats to the existing Prehrana tab, enabling standardized PDF generation, consistent branding, goal-based filtering, and improved operational efficiency.

## What We're Building

A comprehensive Jelovnici management system that moves daily menus out of group chats into the structured Prehrana tab environment, with automated PDF generation and goal-based user filtering.

**Current state:**
- Operators manually create menu graphics in image editing tools
- Menus published as images in group chats mixed with user conversations
- No systematic organization or filtering of menus by user goals
- Users must scroll through chat history to find specific menus

**What we want to add:**
- Admin panel form for Jelovnici creation with goal-based targeting
- Automatic branded PDF generation using standardized templates
- Integration with existing Prehrana tab to display Jelovnici alongside video recipes
- User filtering by their personal goals (weight loss/gain, pregnancy, etc.)
- Push/in-app notifications when new menus matching user's goals are published
- Last 30 days of published menus available for viewing and download

## Requirements

### App Requirements

**User Stories:**
- As a working mother (Marija persona), I want to quickly access daily menus that match my family's nutritional goals so that I can plan meals without scrolling through group chat history
- As a diaspora user (Ana persona), I want to download Jelovnici as PDFs for offline access so that I can reference them during grocery shopping regardless of connectivity
- As an operator, I want to create Jelovnici using a structured form and target them to specific user goals so that I can focus on content quality instead of manual design work
- As a user, I want to receive notifications when new menus matching my goals are published so that I stay informed about relevant nutrition content

**Core Functionality:**
- **Jelovnici Category in Prehrana Tab** - New section displaying daily menus alongside existing video recipes
- **Goal-based Filtering** - Users see only menus relevant to their personal goals (weight loss/gain, pregnancy, special diets, etc.)
- **PDF View and Download** - In-app PDF viewer with download capability for offline reference
- **30-day Archive** - Rolling archive of published menus from the last 30 days
- **Smart Notifications** - Push and in-app notifications for new menus matching user preferences

**Specific Requirements:**
- Prehrana tab adds "Jelovnici" category alongside existing "Video recepti" section
- Menu PDFs display with consistent Fitness Anny branding and Croatian cultural design elements
- Users can view PDFs in-app using native PDF viewer or download to device storage
- Goal filtering integrates with existing user profile goal settings (no new goal selection required)
- Notification settings allow users to enable/disable Jelovnici notifications separately
- Menus older than 30 days automatically archive but remain accessible through search
- PDF files optimized for mobile viewing with readable text size and clear layout
- Empty state messaging when no menus match user's goals with suggestion to broaden preferences

### Admin/Backend Requirements

**Admin Panel Features:**
- **Jelovnik Creation Form** - Structured form with fields for title, description, ingredients, preparation instructions, and nutritional highlights
- **Goal Targeting System** - Checkboxes to target specific user goals (weight loss, weight gain, pregnancy, diabetes, family meals, etc.)
- **Template Selection** - Multiple PDF template options maintaining brand consistency
- **Auto-PDF Generation** - Automated PDF creation upon form submission with proper Croatian typography and branding
- **Publication Controls** - Schedule publication date/time or publish immediately
- **Content Management** - Edit, unpublish, or archive existing Jelovnici with audit trail

**Backend API Requirements:**
- **Jelovnici Content API** - Endpoints for creating, retrieving, updating, and archiving menu content
- **Goal-based Filtering Logic** - Server-side filtering to return only menus matching user's profile goals
- **PDF Generation Service** - Automated PDF creation using predefined templates with Croatian language support
- **Notification System Integration** - Trigger push/in-app notifications when new menus are published
- **30-day Archive Management** - Automated archiving of menus older than 30 days with cleanup processes
- **Analytics Tracking** - Track menu views, downloads, and user engagement for optimization

## User Experience

**Key User Flows:**
1. **Menu Discovery Flow:**
   - User opens Prehrana tab → sees "Video recepti" and "Jelovnici" sections
   - Taps Jelovnici → sees list of menus filtered by their goals (e.g., "Family meals", "Weight loss")
   - Can scroll through last 30 days of relevant menus with clear publication dates

2. **Menu Consumption Flow:**
   - User taps on specific Jelovnik → opens PDF viewer showing branded menu layout
   - Can read nutritional information, ingredients, and preparation tips in Croatian
   - Can download PDF for offline reference or share with family members
   - Can return to menu list or navigate to other Prehrana content

3. **Notification Flow:**
   - New Jelovnik published matching user's goals → push notification sent
   - User taps notification → directly opens the new menu in PDF viewer
   - Can adjust notification preferences in app settings

**UI Components and States:**
- **Jelovnici Section Header** - Clear section title with count of available menus
- **Menu List Cards** - Title, publication date, brief description, goal tags
- **PDF Viewer Integration** - Native iOS/Android PDF viewer with download and share options
- **Filter Indicators** - Visual indication of active goal-based filtering
- **Loading States** - Skeleton screens while PDF content loads
- **Empty States** - Informative messaging when no menus match user's goals

**Empty States and Error Handling:**
- No menus for user's goals: "Trenutno nema jelovnika za vaše ciljeve. Provjerite ponovo kasnije ili kontaktirajte nutricionist."
- PDF loading error: "Greška pri učitavanju jelovnika. Provjerite internetsku vezu."
- Offline mode: "Niste povezani na internet. Prikazujemo ranije preuzete jelovnike."

## Assumptions & Dependencies

**Technical Assumptions:**
- Existing Prehrana tab infrastructure can accommodate new Jelovnici section without performance degradation
- Mobile app PDF viewing capabilities are sufficient for menu display (iOS PDFKit, Android PdfRenderer)
- Current backend can handle increased API load from PDF generation and serving
- Push notification system can support goal-based targeting without major modifications

**Business Assumptions:**
- Users will prefer structured PDF menus over chat-based image sharing
- Operators will adapt to form-based menu creation instead of manual graphic design
- Goal-based filtering will improve user engagement with menu content
- Reduced group chat clutter will improve community interaction quality

**External Dependencies:**
- PDF generation library or service for automated template-based creation
- Croatian typography support for proper diacritic rendering in PDFs
- File storage system for PDF hosting and content delivery
- Integration with existing user goal/preference storage system

**Integration Requirements:**
- Seamless integration with existing Prehrana tab navigation and UI patterns
- Compatibility with current user authentication and goal preference systems
- Integration with push notification service for goal-based targeting
- Admin panel integration with existing operator authentication and permissions

## Risk Assessment

**Technical Risks:**
- **PDF Generation Performance**: Large PDF files may impact app performance on older Android devices | Implement progressive loading and file size optimization
- **Storage Impact**: 30-day menu archive may consume significant device storage | Set storage limits and implement automatic cleanup
- **Cross-platform PDF Rendering**: Inconsistent PDF display between iOS and Android | Standardize PDF format and test extensively across devices

**Business Risks:**
- **User Adoption**: Users may continue expecting menus in group chats | Gradual migration with education campaign and chat reminders
- **Operator Workflow Disruption**: Staff resistance to new form-based creation process | Comprehensive training and workflow optimization
- **Content Quality**: Automated PDF generation may reduce visual appeal vs manual design | Design high-quality templates and gather operator feedback

**User Experience Risks:**
- **Navigation Confusion**: Adding Jelovnici to Prehrana tab may overwhelm existing users | Clear section separation and user onboarding
- **Goal Filtering Accuracy**: Users may miss relevant menus due to overly restrictive filtering | Allow manual filter adjustment and provide "show all" option
- **Notification Fatigue**: Daily menu notifications may annoy users | Granular notification controls and smart frequency management

## Definition of Done (DoD)

### End-User Experience (iOS & Android)
- [ ] Users can access Jelovnici section within existing Prehrana tab with clear visual separation from video recipes
- [ ] Goal-based filtering shows only menus relevant to user's profile settings (weight loss, pregnancy, family meals, etc.)
- [ ] PDF viewer displays menus with proper Croatian text rendering and readable layout on mobile screens
- [ ] Download functionality allows users to save PDFs to device for offline access
- [ ] Push notifications are sent when new menus matching user goals are published
- [ ] 30-day rolling archive shows publication dates and allows access to recent menus
- [ ] Empty states display helpful messages when no menus match user's goals
- [ ] Share functionality enables users to send menus to family/friends via WhatsApp, email, etc.

### Admin/Backend
- [ ] Admin panel form allows operators to create Jelovnici with title, description, ingredients, instructions, and goal targeting
- [ ] Automated PDF generation creates branded menus using standardized templates
- [ ] Goal targeting system enables operators to select which user types should receive each menu
- [ ] Publication controls allow immediate publishing or scheduled release
- [ ] Content management interface supports editing, unpublishing, and archiving menus
- [ ] API endpoints serve goal-filtered menu lists and individual PDF content
- [ ] 30-day automatic archiving removes old content from active display
- [ ] Analytics tracking captures menu views, downloads, and user engagement metrics

### Quality & Performance
- [ ] PDF generation completes within 5 seconds of form submission
- [ ] Menu list loading time under 2 seconds on 3G connection
- [ ] PDF viewing performance acceptable on minimum supported Android devices (4GB RAM)
- [ ] Notification delivery within 1 minute of menu publication
- [ ] File size optimization keeps average PDF under 2MB for mobile data efficiency
- [ ] Croatian diacritic rendering displays correctly across all supported devices
- [ ] Offline PDF access works for previously downloaded menus without internet connection

### Security & Compliance
- [ ] PDF files are served with proper authentication and user access controls
- [ ] Goal-based filtering prevents users from accessing menus not intended for them
- [ ] Admin panel menu creation restricted to authorized operators with proper permissions
- [ ] User notification preferences are respected and can be easily modified
- [ ] GDPR compliance maintained for user goal data and content preference tracking

### Documentation & Rollout
- [ ] Operator training materials created for new menu creation workflow
- [ ] User help documentation explains how to find and use Jelovnici in Prehrana tab
- [ ] Migration communication plan notifies users about transition from group chat to app
- [ ] A/B testing framework ready to measure user adoption and engagement
- [ ] Rollback plan prepared in case of technical issues or user resistance
- [ ] Analytics dashboard configured to monitor feature adoption and operational efficiency gains
- [ ] Success metrics defined and baseline measurements established for post-launch evaluation