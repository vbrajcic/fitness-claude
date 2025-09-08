# Admin Panel - Internal Users Context

## Internal User Overview

### Total Internal Team: 80 Active Users
**Core Team Distribution**:
- **Chat Agents**: 26 users (33% of team) - Limited admin panel access
- **Expert Professionals**: 54 users (67% of team) - Limited admin panel access
  - **Nutritionists**: 15 specialists
  - **Psychologists**: 18 specialists  
  - **Trainers**: 7 specialists
  - **Physical Education Experts**: 4 specialists
  - **Doctors**: 6 medical professionals
  - **Educators**: 3 specialists
  - **Motivators**: 1 specialist
- **Real Admins**: 3 users (4% of team) - **Full admin panel control**

### Critical Admin Panel Architecture: 3-Tier Access System

#### Tier 1: Real Admins (3 users) - Full Control
**Complete System Access**:
- **Order Assignment Authority**: Only real admins can assign expert consultation orders to specific experts
- **Full User Management**: Complete access to all user data, billing, health records, chat history
- **Expert Management**: Can modify expert schedules, capacity, specializations, and availability
- **System Administration**: Database access, user permissions, system configurations
- **Financial Controls**: Billing adjustments, subscription management, payment issues
- **Content Oversight**: Approve expert content, meal plans, workout modifications

**Daily Responsibilities**:
- **Order Queue Management**: Review and assign 50-80 expert consultation orders daily
- **Escalation Handling**: Resolve complex issues that chat agents/experts cannot handle
- **Quality Assurance**: Monitor expert performance and customer satisfaction
- **Capacity Planning**: Balance expert workloads and optimize assignment efficiency
- **End-of-Day Quality Control**: **Manually review ALL chat conversations** for accuracy, tone, and compliance
- **Live Event Management**: **Admin-only access** - Create, schedule, and manage live workout sessions and events
- **Content Management**: **Admin-only access** - Upload and organize video content via Vimeo integration
- **Performance Analytics**: Track expert efficiency, user satisfaction, and operational bottlenecks

#### Tier 2: Chat Agents (15 users) - Limited Access + Anonymous Identity
**Anonymous User Interface**:
- **Always appear as "Fitness Anny"** to users - never reveal individual agent names
- Users cannot request specific agents or know who they're talking to
- Maintain consistent brand voice and professional anonymity
- All communication appears to come from unified "Fitness Anny" support

**Restricted Panel Access**:
- Can view customer basic information (subscription status, contact details)
- Can access chat history and basic conversation management
- **Cannot assign expert orders** - must escalate to real admins
- Can update simple profile information but not health/medical data
- Can process basic billing inquiries but not make changes

**Quality Control Subject**:
- **All chat conversations reviewed daily** by real admins for quality assurance
- Performance monitored on response accuracy, tone, and brand consistency
- Must follow approved response templates and escalation protocols

#### Tier 3: Expert Professionals (12 users) - Task-Specific Access + Anonymous Identity
**Anonymous Expert Identity**:
- **Always appear as "Fitness Anny [Expert Type]"** (e.g., "Fitness Anny Nutritionist")
- Users never know specific expert names or can request particular experts
- Maintain professional anonymity while providing specialized advice
- All expertise appears to come from unified "Fitness Anny" brand

**Specialized Panel Views**:
- Can only see **assigned orders** and their specific customers
- Access to relevant customer health/fitness data for their specialization
- Can update consultation outcomes and create content for assigned users
- **Cannot see order queue** or assign orders to themselves or others
- Limited to their specific domain (nutrition, training, medical, etc.)

**Performance Optimization Focus**:
- **Goal**: Solve as many orders as possible while maintaining efficiency and user satisfaction
- **Key Metrics**: Order completion rate, user satisfaction scores, response accuracy
- **Quality Control**: All expert advice reviewed daily by real admins
- **Efficiency Pressure**: Balance between speed and quality in consultations

### Expert Order Assignment Workflow (Admin Panel Core Function)

#### Order Intake Process
**Mobile App to Admin Pipeline**:
1. **User submits expert consultation request** via mobile app (cannot select specific expert)
2. **Order appears in admin panel queue** with user context, request type, urgency level
3. **Real admin reviews order** considering:
   - Expert availability and current workload
   - Specialization match (nutritionist for meal planning, doctor for medical issues)
   - User's health conditions and past consultation history  
   - Expert language preferences and cultural fit
   - Time zone considerations for diaspora users

#### Assignment Decision Factors
**Expert Capacity Management**:
- Current workload (number of active consultations)
- Scheduled availability (live sessions, content creation time)
- Specialization depth (pregnancy expert vs general nutritionist)
- User preference indicators (repeat customers, satisfaction scores)

**Order Priority Assessment**:
- **Urgent Medical**: Pregnancy concerns, health condition questions (priority assignment)
- **Standard Consultation**: Meal planning, workout modifications (normal queue)
- **General Support**: Motivation, general questions (flexible timing)

### Content Management System

#### Live Event Scheduling & Management (Admin-Only Access)
**Real Admin Exclusive Features**:
- **Event Scheduling**: Create and schedule live workout sessions, webinars, Q&A sessions
- **Trainer Assignment**: Assign specific trainers to lead live events (internal assignment, users still see "Fitness Anny")
- **Capacity Management**: Set participant limits and manage registrations
- **Event Notifications**: Automated user notifications for upcoming live sessions
- **Real-time Management**: Monitor live event attendance and engagement during sessions

**Access Restriction**: Chat agents and experts cannot create, modify, or manage live events

#### Video Content Management (Admin-Only Access)
**Real Admin Exclusive Vimeo Integration**:
- **Video Upload Interface**: Direct integration with Vimeo for video hosting and management
- **Content Organization**: Categorize videos by workout type, difficulty level, expert specialization
- **Vimeo Link Management**: Automated linking between admin panel and Vimeo video library
- **Content Scheduling**: Schedule video releases and manage content calendar
- **Quality Control**: Preview and approve all video content before user publication

**Access Restriction**: Only real admins can upload, organize, or modify video content

### Complete Admin Panel Feature System (Based on Detailed Transcript Analysis)

## Core System Architecture

### 1. Live Chat & Message Request Management (Core Feature)

#### Message Request Queue System
**Automated Job Processing**:
- **Background Job**: Runs every minute to scan chat rooms for new messages
- **Message Request Creation**: Automatically creates "message requests" from user messages
- **Automatic Assignment**: Can be enabled/disabled globally
- **Manual Assignment Interface**: Real admins assign requests to available operators

**Assignment Logic**:
- **Category Matching**: System matches user requests to operator specializations
- **Availability Checking**: Only assigns to operators marked as "available"
- **Capacity Management**: Prevents overloading individual operators
- **Priority Routing**: Medical/urgent requests get priority treatment

#### Real-time Chat Interface
**Admin Monitoring Capabilities**:
- **Live Chat Viewing**: Admins can monitor any active conversation
- **Admin Override**: Admins can write messages on behalf of any operator
- **Conversation Handoff**: Seamless transfer between operators
- **System Messages**: Internal notes visible only to admins/operators

**Conversation Lifecycle**:
1. **Request Creation**: User message creates message request
2. **Assignment**: Manual or automatic assignment to operator
3. **Acceptance**: Operator accepts the conversation
4. **Active Chat**: Real-time conversation management
5. **Completion**: Operator closes conversation with optional summary
6. **Recently Closed**: 240-second grace period for user replies
7. **Archived**: Final conversation state

### 2. Operator Management System

#### Operator Creation & Configuration
**Account Setup**:
- **Basic Info**: Email (login only), mobile number (optional)
- **Assignment Permissions**: Can be assigned messages or locked out
- **Category Specialization**: Define which expert categories they can handle
- **Access Control**: Granular permission system with role-based access

**Permission System (Highly Granular)**:
- **Member Management**: View, edit, delete user accounts
- **Subscription Management**: Handle user subscriptions and payments
- **Group Management**: Create, modify, manage user groups
- **Event Management**: Handle live events and video content
- **Reporting**: Access to analytics and performance data
- **Admin Functions**: System administration capabilities

#### Operator Monitoring & Performance
**Activity Tracking**:
- **Online Status**: Manual and admin-controlled availability
- **Conversation Load**: Track active conversations per operator
- **Performance Metrics**: Conversations completed, response times, user satisfaction
- **Audit Trail**: Complete log of all operator actions (30-day retention)

**Performance Reporting**:
- **Daily Statistics**: Conversations handled, completion rates
- **Individual Performance**: Detailed operator performance analysis
- **Comparative Analytics**: Cross-operator performance comparison
- **Quality Control**: Random conversation review for quality assurance

### 3. Group Management System (Complex Multi-State)

#### Group Types & Configuration
**Group Categories**:
- **Public Groups**: All members can write messages
- **Notification Groups**: Only operators can write, users read-only
- **Internal Groups**: Operator-only communication (rarely used)

**Group Lifecycle Management**:
- **Display Date**: When group becomes visible to users
- **Activation Date**: When users can start writing messages
- **Expiration Date**: When group becomes read-only
- **Archive Process**: Final removal from system

#### Group Membership Management
**Automated Membership**:
- **Advanced Filter System**: Sophisticated user filtering capabilities
- **Automatic Synchronization**: Background job updates group memberships
- **Subscription Integration**: Group access based on subscription tiers
- **Manual Override**: Individual user addition/removal

**Filter System (Extremely Advanced)**:
- **Subscription Filters**: By package type, active/inactive status
- **Demographic Filters**: Age, location, subscription history
- **Goal-Based Filters**: Weight loss, muscle gain, maintenance
- **Health Condition Filters**: Pregnancy, medical conditions, fitness level
- **Engagement Filters**: App usage, workout completion rates
- **Time-Based Filters**: "Active month", "Next month", date ranges

#### Group Content Management
**Message Management**:
- **Pin Messages**: Important announcements stay visible
- **Message Deletion**: Admin deletion (hidden from users, logged internally)
- **Reaction System**: Users can react to messages
- **Media Management**: Image and video sharing capabilities

### 4. Event & Video Management System

#### Live Event Management
**Event Creation & Scheduling**:
- **Event Details**: Name, description, date/time configuration
- **Vimeo Integration**: Automatic stream key generation 15 minutes before event
- **Streaming Setup**: OBS integration for live streaming
- **Participant Management**: Set limits, track attendance

**Live Event Operations**:
- **Real-time Chat**: Monitor participant messages during events
- **Stream Control**: Start, stop, pause live streams
- **Recording Management**: Automatic conversion to on-demand after completion
- **Attendee Analytics**: Track participation and engagement

#### Video Content System
**Content Types**:
- **Live Event Recordings**: Converted from live streams
- **Pre-recorded Videos**: Uploaded workout and educational content
- **Recipe Content**: New feature with ingredient and preparation steps
- **Educational Materials**: Specialized content for different user segments

**Video Management**:
- **Vimeo Integration**: Cloud storage and CDN delivery (~500GB current storage)
- **Access Control**: Permission-based viewing by subscription tier
- **Content Organization**: Categories, tags, difficulty levels
- **Automatic Cleanup**: Content removal when groups are archived

### 5. Education & Workshop System (New Feature)

#### Education Event Management
**Workshop Creation**:
- **Multi-session Events**: Define multiple presentations within single education
- **Registration System**: Limited participant slots with approval process
- **Presenter Management**: Assign multiple presenters to different sessions
- **Resource Management**: Upload supporting materials (PDFs, guides, meal plans)

#### Registration & Approval Workflow
**Registration Process**:
- **User Application**: Users apply with reason and contact information
- **Admin Review**: Approve/reject applications with reason
- **Capacity Management**: Automatic slot tracking
- **Blacklist System**: Temporary bans for no-shows (automatic 3-day ban)
- **Viber Group Integration**: Approved participants added to communication groups

### 6. Task/Order System (Nalozi - Critical Operational Feature)

#### Bulk Communication Management
**Task Creation**:
- **Mass Communication**: Create tasks for contacting multiple users
- **Individual Tasks**: Single-user specific tasks
- **Scheduling System**: Distribute task execution over multiple days/times
- **Category Assignment**: Route tasks to appropriate operator types

**Task Distribution Logic**:
- **Load Balancing**: Prevent overwhelming operators with simultaneous tasks
- **Time Scheduling**: Spread task execution across defined time periods
- **Approval Workflow**: Admin approval required before task execution
- **Background Execution**: Automated task processing every 5 minutes

**Common Task Types**:
- **Monthly Check-ins**: Contact all subscribers to thank for payment
- **Progress Photo Requests**: Request users to upload progress photos
- **Engagement Follow-up**: Contact inactive users for re-engagement
- **Premium Support**: Specialized outreach for premium subscribers

### 7. User Profile & Data Management

#### Comprehensive User Database
**Profile Management**:
- **Personal Information**: Complete demographic and contact data
- **Health Data**: Weight, height, goals, medical conditions
- **Progress Tracking**: Photo uploads, measurement history
- **Subscription History**: Complete payment and package history
- **Communication History**: All conversations across all categories

**Advanced Search & Filtering**:
- **Multi-criteria Search**: Combine multiple filter types
- **Saved Filter Templates**: Reusable filter configurations
- **Export Capabilities**: Data export for marketing and analysis
- **Real-time Synchronization**: Automatic updates when user data changes

#### Goal & Algorithm System
**Automated Goal Calculation**:
- **Weight-based Algorithm**: Automatic target weight calculation
- **Progress Monitoring**: Track user progress toward goals
- **Dynamic Recommendations**: Adjust recommendations based on progress
- **Group Assignment**: Auto-assign to appropriate groups based on goals

### 8. Subscription & Payment Management

#### Payment Processing Integration
**Multiple Payment Methods**:
- **Web Payments**: VSP payment processor integration
- **Apple App Store**: iOS in-app purchase integration
- **Manual Assignment**: Admin-assigned subscriptions (gifts, adjustments)
- **Promo Code System**: Discount codes with validity periods

#### Subscription Management
**Package Types & Pricing**:
- **Basic Packages**: Weight loss, weight gain specific programs
- **Premium**: Most popular tier (~13,000 of 15,000 subscribers)
- **Premium Plus**: Limited capacity, personalized nutrition plans (~160 users)
- **Specialist Access Control**: Premium+ required for specialist consultations

**Subscription Lifecycle**:
- **Purchase Processing**: Webhook integration for payment confirmation
- **Access Provisioning**: Automatic group and content access assignment
- **Renewal Management**: Automatic monthly renewal processing
- **Cancellation Handling**: Graceful subscription termination

### 9. Analytics & Reporting System

#### Performance Analytics
**Operator Performance Tracking**:
- **Conversation Metrics**: Volume, completion rates, response times
- **Quality Scoring**: User satisfaction and conversation quality
- **Productivity Analysis**: Conversations per hour, daily statistics
- **Comparative Reporting**: Cross-operator performance comparison

**System Performance Monitoring**:
- **User Engagement**: App usage, workout completion, group participation
- **Subscription Analytics**: Conversion rates, churn analysis, revenue tracking
- **Content Performance**: Video views, event attendance, engagement metrics
- **Technical Performance**: System load, response times, error rates

#### Audit & Compliance
**Complete Audit Trail**:
- **User Actions**: All admin and operator activities logged
- **Data Changes**: Track all modifications to user data and system settings
- **Access Logging**: Monitor who accessed what data when
- **30-day Retention**: Automatic cleanup of audit logs after 30 days

### 10. System Configuration & Administration

#### Global System Settings
**Operational Controls**:
- **Free Access Periods**: "Open doors" days for free platform access
- **Automatic Assignment Toggle**: Enable/disable automatic message assignment
- **Shift Scheduling**: Automatic operator availability based on work schedules
- **Pause Periods**: System-wide breaks (11:00-12:00, 18:00-19:00)

#### Content & Access Management
**Program Management**:
- **Package Availability**: Enable/disable subscription packages
- **Price Management**: Update subscription pricing across platforms
- **Access Permissions**: Define which features each subscription tier can access
- **Content Restrictions**: Control access to specialist chats and premium content

## Technical Architecture & Infrastructure

### Database & Storage
**Data Management**:
- **Multiple Database Systems**: Separate systems for chat (ejabberd), admin panel, user data
- **Soft Delete System**: All deletions are logical, not physical (data recovery possible)
- **Storage Integration**: Azure-based CDN for media files (~500GB current usage)
- **Performance Optimization**: Pagination and caching for large datasets

### Integration Points
**External System Dependencies**:
- **ejabberd**: Chat system requiring separate login and interface
- **Vimeo**: Video hosting and live streaming platform
- **VSP**: Web payment processing
- **Apple App Store**: iOS subscription management
- **Email Systems**: Automated notifications and confirmations

### Performance & Scalability Considerations
**Current Scale Challenges**:
- **High-volume Chat**: Millions of messages in single ejabberd table
- **Real-time Processing**: Minute-by-minute job processing for message requests
- **Complex Queries**: Advanced filtering system requires optimized database queries
- **Multi-system Synchronization**: Coordination between admin panel, chat, and mobile app

**Operational Bottlenecks**:
- **Manual Assignment**: 3 admins manually processing 50-80 requests daily
- **Quality Control**: Manual review of hundreds of daily conversations
- **Group Management**: Complex filter system with real-time member synchronization
- **Task Distribution**: Manual approval and scheduling of mass communication tasks

**Content Types Managed**:
- **Workout Videos**: Exercise routines, form demonstrations, specialized programs
- **Educational Content**: Health information, nutrition guidance, lifestyle tips
- **Live Session Recordings**: Archived live events for on-demand viewing
- **Expert Consultations**: Pre-recorded consultation templates and guidance videos

### User Management & Payment Administration System

#### User Management Tab (Admin-Only Access)
**Comprehensive User Database Interface**:
- **Complete User Profiles**: Full access to all user information and account details
- **Subscription Status Tracking**: Active/inactive subscriptions, subscription tier levels
- **Subscription Type Management**: Basic, Premium, Premium Plus tier information
- **Payment Method Tracking**: How users paid (mobile app purchase, web payment)
- **Progress Photo Management**: Access to user progress photos and timeline
- **Health Information**: Medical conditions, fitness goals, consultation history
- **Usage Analytics**: App engagement, workout completion, expert consultation frequency
- **Account History**: Registration date, subscription changes, support ticket history

**User Search & Filtering**:
- **Quick Search**: Find users by name, email, phone, or subscription ID
- **Advanced Filters**: Filter by subscription type, payment status, engagement level
- **Bulk Operations**: Manage multiple user accounts simultaneously
- **Export Capabilities**: Generate user data reports for analysis

#### Payments Tab (Admin-Only Access - Separated for Payment Issue Resolution)
**Dedicated Payment Troubleshooting Interface**:
- **Payment Transaction History**: Complete transaction log for each user
- **Payment Method Details**: Credit card, app store, web payment information
- **Payment Status Tracking**: Successful, failed, pending, refunded transactions
- **Duplicate Payment Detection**: Identify and resolve double-charge issues
- **Access Issue Resolution**: Match payments to user accounts when access problems occur
- **Billing Dispute Management**: Handle subscription and payment complaints

**Common Payment Issue Scenarios**:
- **"I paid but don't have access"**: Cross-reference payment tab with user account status
- **"Payment went through twice"**: Identify duplicate transactions and process refunds
- **"Subscription not working"**: Verify payment processing and account activation
- **Platform Payment Mismatches**: Resolve app store vs web payment conflicts

**Payment Analytics & Reporting**:
- **Revenue Tracking**: Daily, weekly, monthly payment summaries
- **Failed Payment Analysis**: Identify and resolve payment processing issues
- **Subscription Conversion Tracking**: Monitor free trial to paid conversions
- **Churn Analysis**: Track cancellations and payment-related user loss

#### Admin Panel Order Management Interface Requirements
**Order Queue Dashboard**:
- Real-time order intake with user context preview
- Expert availability matrix with capacity indicators
- One-click assignment with automatic notification to expert and user
- Order tracking from submission to completion
- Performance analytics for assignment efficiency

**Operational Schedule**: 8am-10pm Mon-Sat (14 hours daily coverage)
**Peak Demand**: 6-8am, 7-10pm (overlaps with user workout times)
**Critical Bottlenecks**: 
- **Manual Order Assignment**: 3 real admins must manually assign 50-80 expert orders daily among 54 available experts during peak hours
- **End-of-Day Quality Review**: Manual review of ALL daily chat conversations from 80 team members for quality control
- **Team Efficiency Optimization**: Need to maximize productivity across 26 agents + 54 experts while maintaining user satisfaction
- **Expert Specialization Management**: Complex assignment decisions across 7 different expert types with varying capacities

## Primary User Personas

### Persona 1: Marija - Chat Agent (Lead Support Agent, 33% of admin users - 26 total agents)

#### Demographics & Background
**Profile**: 28 years old, University graduate in Communications, 2 years with company
**Location**: Zagreb office (remote work 3 days/week)
**Technical Skill**: Intermediate - comfortable with web apps, needs intuitive interfaces
**Languages**: Native Croatian/Bosnian, conversational English
**Work Schedule**: Rotating shifts to cover 8am-10pm operations

#### Daily Responsibilities
**Primary Tasks**:
- Handle 40-60 customer chat conversations per day
- Route complex questions to appropriate experts (nutritionists, doctors, trainers)
- Resolve subscription and billing issues
- Provide basic workout and nutrition guidance
- Monitor user engagement and flag at-risk users
- Update customer profiles with important health information

**Performance Expectations**:
- Average response time: <2 minutes
- Customer satisfaction rating: >4.5/5
- Conversation resolution rate: >85% first contact
- Daily conversation target: 50 successful resolutions
- Expert escalation rate: <15% of conversations

#### Current Pain Points with Admin Panel
**Navigation & Efficiency Issues**:
- "Takes 30+ seconds to find customer information across multiple screens"
- "Can't see customer's workout history while chatting - have to switch windows"
- "Billing system is separate, so subscription issues require multiple steps"
- "No quick templates for common responses about meal plans or workouts"

**Information Access Problems**:
- "Customer's health conditions are buried in profile - hard to find quickly"
- "Can't see if user is currently in a live session when they contact us"
- "Previous chat history with customer isn't easily accessible"
- "No alerts for VIP customers or those with urgent health issues"

**Communication Challenges**:
- "Group chat with experts gets cluttered - hard to track ongoing cases"
- "No way to hand off conversation smoothly to specialist"
- "Can't see expert availability before routing questions"
- "Customer notifications don't sync - sometimes they get duplicate messages"

#### Technology Usage Patterns
**Device & Platform Preferences**:
- **Primary Device**: Windows laptop (company-provided)
- **Secondary Device**: Personal Android phone for mobile access during breaks
- **Browser**: Chrome (company standard)
- **Communication**: Slack for team coordination, admin panel for customer service

**Workflow Patterns**:
- **Morning Routine**: Check overnight messages, review customer escalations, team standup
- **Peak Hours**: Focus mode - rapid-fire customer conversations
- **Afternoon**: Follow up on expert consultations, update customer records
- **End of Shift**: Document unresolved issues, prepare handoff notes

**Success Enablers**:
- **Quick Customer Lookup**: Ability to find customer info in <10 seconds
- **Context Switching**: Seamless movement between chat, profile, billing, workout data
- **Expert Coordination**: Clear visibility into specialist availability and expertise
- **Mobile Access**: Handle urgent issues when not at primary workstation

### Persona 2: Dr. Ana - Medical Expert (Nutritionist/Doctor, representative of 67% expert users - 54 total experts)

#### Demographics & Background
**Profile**: 34 years old, MD with nutrition specialization, 3 years consulting for platform
**Location**: Split, Croatia (fully remote, occasional Zagreb office visits)
**Technical Skill**: Basic to intermediate - medical professionals, not tech-native
**Languages**: Native Croatian, medical English proficiency
**Work Schedule**: Flexible hours with guaranteed coverage during peak user times

#### Daily Responsibilities
**Primary Tasks**:
- Provide medical consultations via chat (15-20 per day)
- Review and approve pregnancy workout modifications
- Create weekly meal plans for users with health conditions
- Conduct video consultations for complex cases (3-5 per day)
- Review user progress photos for health concerns
- Collaborate with trainers on exercise modifications for medical conditions

**Performance Expectations**:
- Response time for urgent health issues: <30 minutes
- Non-urgent consultations: <2 hours
- Weekly meal plan completion: 100% by Sunday evening
- Customer satisfaction for expert consultations: >4.8/5
- Medical content review: 5-8 workout/nutrition items per week

#### Current Pain Points with Admin Panel
**Medical Workflow Issues**:
- "Can't easily see user's complete health history when they ask follow-up questions"
- "Meal planning interface is clunky - takes too long to create family-friendly menus"
- "No integration with user's workout data when making exercise recommendations"
- "Can't mark conversations as 'requires medical follow-up' for tracking"

**Collaboration Challenges**:
- "Hard to coordinate with trainers when user needs both exercise and dietary modifications"
- "No shared workspace for complex cases involving multiple experts"
- "Can't see which users have upcoming video consultations in my schedule"
- "Difficult to track long-term patient progress across multiple conversations"

**Content Management Problems**:
- "Weekly menu template system is outdated and not user-friendly"
- "Can't easily adapt meal plans for different family sizes or dietary restrictions"
- "No way to save and reuse successful meal plan modifications"
- "Uploading and organizing recipe content is time-consuming"

#### Technology Usage Patterns
**Device & Platform Preferences**:
- **Primary Device**: MacBook Pro (personal, medical practice)
- **Secondary Device**: iPad for content review and video consultations
- **Platform**: Prefers web-based tools over downloadable software
- **Schedule Management**: Google Calendar integration essential

**Workflow Patterns**:
- **Morning Planning**: Review scheduled consultations, check urgent health questions
- **Consultation Blocks**: 2-hour focused blocks for video and complex chat consultations
- **Content Creation**: Dedicated time for meal planning and medical content review
- **Evening Wrap-up**: Follow-up messages, next-day preparation

**Success Enablers**:
- **Integrated Health Records**: Complete user health profile in one view
- **Collaborative Tools**: Easy coordination with other experts
- **Efficient Content Creation**: Streamlined meal planning and medical content tools
- **Mobile Optimization**: Ability to handle urgent issues from iPad/mobile

### Persona 3: Stefan - Fitness Trainer (Expert Professional, part of 54 total expert professionals)

#### Demographics & Background
**Profile**: 26 years old, Certified Personal Trainer and Kinesiologist, 1.5 years with platform
**Location**: Sarajevo, Bosnia (fully remote)
**Technical Skill**: High - younger generation, comfortable with technology and social media
**Languages**: Native Bosnian/Serbian, good English, basic Croatian
**Work Schedule**: Flexible with focus on live session times and peak user questions

#### Daily Responsibilities
**Primary Tasks**:
- Lead 3-4 live workout sessions per week
- Answer form and exercise technique questions via chat (25-35 per day)
- Create and modify workout programs for users with limitations
- Review user progress videos and provide form feedback
- Collaborate with medical experts on safe exercise progressions
- Develop new workout content and exercise modifications

**Performance Expectations**:
- Live session attendance: 40+ users per session
- Chat response time: <3 minutes for exercise questions
- Form review turnaround: <24 hours for submitted videos
- Customer satisfaction: >4.6/5 for fitness guidance
- Content creation: 2-3 new workout modifications per week

#### Current Pain Points with Admin Panel
**Live Session Management Issues**:
- "Can't see user's fitness level or limitations before live session starts"
- "No easy way to share exercise modifications during live sessions"
- "Attendance tracking for live sessions is manual and time-consuming"
- "Can't follow up easily with users who struggled during live workouts"

**User Progress Tracking Problems**:
- "Hard to track individual user progress across multiple workout sessions"
- "No centralized place to see user's workout completion rates and feedback"
- "Can't easily create personalized workout progressions based on user data"
- "Difficult to coordinate with nutritionists when user needs combined approach"

**Content Creation Inefficiencies**:
- "Workout modification creation tool is slow and not intuitive"
- "Can't easily tag or categorize exercise modifications for reuse"
- "No way to preview how workout looks from user perspective"
- "Video upload and processing for exercise demonstrations takes too long"

#### Technology Usage Patterns
**Device & Platform Preferences**:
- **Primary Device**: Gaming laptop (personal, high-performance)
- **Secondary Device**: iPhone for live session management and quick responses
- **Content Creation**: Familiar with video editing, social media tools
- **Communication**: Prefers real-time chat and video calls over email

**Workflow Patterns**:
- **Pre-Live Session**: Review attendees, prepare modifications, test equipment
- **Live Session Delivery**: Focus on real-time interaction and motivation
- **Post-Session**: Follow up with participants, review session feedback
- **Content Development**: Batch create exercise modifications and demo videos

**Success Enablers**:
- **Real-time User Data**: Live access to participant fitness levels and limitations
- **Seamless Content Tools**: Quick exercise modification and video upload
- **User Progress Visibility**: Clear tracking of individual user fitness journeys
- **Cross-expert Collaboration**: Easy coordination with medical and nutrition experts

## User Journey & Workflow Analysis

### Daily Workflow Patterns

#### Peak Hours (7-10pm User Traffic)
**Chat Agent Workflow**:
- 3-4 simultaneous conversations active
- Average 2-minute response time requirement
- Frequent escalations to experts during workout hours
- High stress period requiring efficient tools

**Expert Workflow**:
- Nutritionists: Post-workout meal timing questions
- Trainers: Real-time form corrections during workouts
- Doctors: Exercise modification requests for health conditions
- All experts: Increased collaboration during peak demand

#### Off-Peak Hours (10am-5pm)
**Administrative Tasks**:
- Content creation (meal plans, workout modifications)
- User progress reviews and long-term planning
- System maintenance and data updates
- Training and team coordination meetings

### Cross-Functional Collaboration Patterns

#### Complex User Cases Requiring Multiple Experts
**Pregnancy Fitness Planning**:
- Doctor: Medical clearance and exercise restrictions
- Trainer: Safe exercise modifications and progressions
- Nutritionist: Pregnancy-appropriate meal planning
- Chat Agent: Ongoing support and coordination

**Health Condition Management**:
- Doctor: Health assessment and exercise limitations
- Nutritionist: Dietary modifications for condition
- Trainer: Adapted workout programs
- Chat Agent: Regular check-ins and motivation

#### Information Flow Requirements
**User Context Sharing**:
- Medical history and current health status
- Fitness level and exercise preferences
- Family situation and scheduling constraints
- Previous expert consultations and outcomes

**Expert Coordination Needs**:
- Real-time availability status
- Expertise area identification
- Case handoff documentation
- Collaborative decision tracking

## Performance & Efficiency Metrics

### Current Performance Benchmarks

#### Response Time Performance
**Chat Agents**:
- Current average: 3.2 minutes
- Target: <2 minutes
- Peak hour average: 5.8 minutes (major issue)
- Off-peak average: 1.4 minutes

**Expert Professionals**:
- Fitness questions: 2.1 minutes average
- Nutrition questions: 2.8 minutes average
- Medical questions: 4.5 minutes average (complexity factor)

#### Productivity Metrics
**Chat Agent Efficiency** (26 Agents):
- Conversations per hour: 8 average (target: 12)
- First-contact resolution: 85% (target: 90%)
- Customer satisfaction: 4.6/5 (target: 4.7/5)
- Expert escalation rate: 18% (target: 15%)
- **Scale Challenge**: Managing consistency across 26 agents with varied experience levels

**Expert Utilization** (Across 54 Specialists):
- Available hours utilization: 72% (target: 80%)
- Consultation completion rate: 94% (meeting target)
- Cross-expert collaboration frequency: 23% of cases
- Content creation efficiency: 2.3 items/week (target: 3/week)
- **Expert Load Balancing Challenge**: Uneven distribution among 54 experts
- **Specialization Utilization**: Nutritionists (15) and Psychologists (18) handle majority of orders

### Major Operational Challenges & Automation Opportunities

#### Challenge 1: Manual Order Assignment System
**Current Process**: 3 real admins manually review and assign 50-80 expert consultation orders daily
**Bottleneck Impact**:
- Peak hour delays (7-10pm) create user frustration waiting for expert assignment
- Admin cognitive overload during high-volume periods
- Inconsistent assignment criteria based on admin availability and decision-making
- No automated load balancing or expert capacity optimization

**Automation Opportunities**:
- Smart order routing based on expert availability and specialization
- Automated capacity balancing to distribute workload evenly
- Priority queue management with rule-based assignment logic
- Real-time expert status tracking for immediate assignment capability

#### Challenge 2: Manual Quality Control Review
**Current Process**: Real admins manually review ALL daily chat conversations for quality assurance
**Scale Problem**: 
- 26 agents + 54 experts = **massive conversation volume daily**
- 80 team members producing hundreds of conversations requiring review
- Time-intensive manual review process becoming unsustainable at this scale
- Inconsistent quality standards across different admin reviewers
- Delayed feedback to agents/experts about performance issues
- **Quality review bottleneck**: 3 admins reviewing work of 80 team members

**Automation Opportunities**:
- AI-powered conversation analysis for tone, accuracy, and compliance
- Automated flagging of conversations requiring human review
- Real-time quality scoring and feedback systems
- Template compliance checking and suggestion systems

#### Challenge 3: Agent Efficiency Optimization
**Current Goal**: Maximize orders solved per agent while maintaining efficiency and user happiness
**Efficiency Blockers**:
- No real-time performance analytics for agents/experts
- Manual tracking of user satisfaction and response quality
- Limited tools for agents to handle common queries efficiently
- No automated escalation or decision support systems

**Optimization Opportunities**:
- Real-time productivity dashboards for agents and experts
- Automated response suggestion systems for common queries
- Smart escalation triggers based on conversation complexity
- Performance gamification and optimization coaching

### Efficiency Pain Points Impact Analysis

#### Time Waste Analysis
**Customer Lookup Inefficiency**:
- Average time to find customer info: 45 seconds
- Impact: 30 minutes lost per agent per day
- Solution value: 15% productivity improvement potential

**Context Switching Overhead**:
- Screen switches per conversation: 4.2 average
- Time lost per switch: 15 seconds
- Impact: 25 minutes lost per agent per day
- Solution value: 12% efficiency improvement

**Expert Coordination Delays** (Amplified with 54 Experts):
- Time to find available expert among 54 specialists: 2.3 minutes average
- Complex specialization matching across 7 expert types
- Handoff documentation time: 1.8 minutes
- Expert availability tracking complexity with large team
- Impact: Delayed response times, lower satisfaction, assignment errors
- Solution value: 20% faster expert consultations across much larger expert pool

#### User Satisfaction Correlation
**High-Performing Agent Characteristics**:
- Quick customer information access
- Seamless expert coordination
- Proactive follow-up capabilities
- Mobile accessibility for urgent issues

**Expert Satisfaction Drivers**:
- Complete user context availability
- Efficient content creation tools
- Clear collaboration workflows
- Flexible schedule management

## Technology Usage & Constraints

### Current System Limitations

#### Legacy System Constraints
**Technical Debt Impact**:
- Slow customer database queries (3+ second load times)
- Separate systems for chat, billing, user data, content management
- No real-time synchronization between expert schedules and availability
- Limited mobile optimization for remote work needs

#### Integration Challenges
**External System Dependencies**:
- Chat system (ejabberd) requires separate login and interface
- Billing system integration creates data consistency issues
- User app data not real-time accessible from admin panel
- Video consultation platform requires separate account management

### Device & Platform Requirements

#### Hardware Considerations
**Agent Workstation Needs**:
- Multiple monitor support for simultaneous chat and data views
- Fast internet connection for video consultations and real-time chat
- Mobile device access for urgent after-hours support
- Reliable backup internet for remote work continuity

**Expert Professional Needs**:
- High-quality webcam and audio for video consultations
- Large screen for content creation and detailed user progress review
- Mobile optimization for quick responses and schedule management
- Integration with personal productivity tools (calendar, notes)

#### Software Environment
**Browser Compatibility**:
- Chrome (primary): 78% of users
- Safari (Mac users): 15% of users
- Firefox: 7% of users
- Mobile browsers: 23% of usage time

**Operating System Distribution**:
- Windows: 65% (company laptops)
- macOS: 28% (personal devices, experts)
- Mobile (iOS/Android): 35% of daily usage

---

*Internal Users Analysis Owner*: Product Manager + Operations Manager  
*Data Sources*: User interviews, performance analytics, workflow observation, satisfaction surveys  
*Last Updated*: [Current Date]  
*Next Review*: Monthly workflow efficiency assessment