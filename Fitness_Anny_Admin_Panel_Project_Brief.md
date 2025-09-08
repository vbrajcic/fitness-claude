# Fitness Anny Admin Panel - Project Brief

**Document Purpose**: Comprehensive overview for new project manager  
**Date**: 2025-09-08  
**Company**: Fitness Anny - Croatian Women's Fitness Platform  
**Current Scale**: ~15,000 monthly subscribers, targeting 25,000+

---

## Executive Summary

Fitness Anny operates a **complex order assignment and quality management system** powered by an admin panel that manages **80 team members** across multiple specializations. The current system has **critical bottlenecks** that limit scalability and operational efficiency.

**Key Challenge**: **3 real admins** manually manage order assignments, quality control, and system administration for **80 team members** serving 15,000+ users daily.

**Project Goal**: Optimize admin panel to support growth to 25,000+ subscribers without proportional team expansion.

---

## Business Context & Strategic Priority

### Company Mission
Empowering Balkan women 35+ to achieve fitness goals through personalized human support and convenient home-based solutions.

### Competitive Advantage
- **24/7 Croatian-speaking human experts** (doctors, nutritionists, trainers)
- **Deep understanding of Balkan culture** and lifestyle
- **Women 35+ specific approach** vs general audience
- **Integrated medical/wellness support** beyond fitness

### Strategic Priorities (Next 6 Months)
1. **Scale to 25,000+ subscribers** through improved user acquisition and retention
2. **Improve operational efficiency** to handle growth without proportional cost increase
3. **Reduce technical debt** to accelerate feature development velocity
4. **Strengthen competitive moat** through enhanced human support experience

---

## Current Team Structure & Scale

### Total Team: 80 Active Users
**Critical Understanding**: This is a **much larger operation** than typical SaaS admin panels.

#### Team Distribution:
- **Chat Agents**: 26 users (33% of team) - Limited admin panel access
- **Expert Professionals**: 54 users (67% of team) - Specialized access
  - **Nutritionists**: 15 specialists (largest group)
  - **Psychologists**: 18 specialists (largest group)
  - **Trainers**: 7 specialists
  - **Physical Education Experts**: 4 specialists
  - **Doctors**: 6 medical professionals
  - **Educators**: 3 specialists
  - **Motivators**: 1 specialist
- **Real Admins**: 3 users (4% of team) - **Full control over everything**

#### Access Hierarchy (Critical Architecture):
1. **Tier 1 - Real Admins (3 people)**: Complete system control, order assignment authority, quality oversight
2. **Tier 2 - Chat Agents (26 people)**: Limited access, cannot assign expert orders
3. **Tier 3 - Experts (54 people)**: Only see assigned orders, no queue visibility

---

## Core System: Expert Consultation Order Management

### How It Works (Critical Business Process)
This is **NOT a typical support chat system** - it's an **order assignment and fulfillment system**.

#### User Experience Flow:
1. **Order Creation**: User selects expert type but **cannot choose specific expert by name**
2. **Order Submission**: Request becomes an "order" in admin panel queue
3. **Manual Assignment**: **3 real admins review and assign** orders to available experts
4. **Expert Fulfillment**: Assigned expert provides consultation
5. **Quality Control**: **All conversations reviewed daily** by real admins

#### Available Expert Types (7 Categories):
- **Nutritionists** (15): Meal planning, dietary advice, cultural food integration
- **Psychologists** (18): Mental health support, stress management, body image
- **Trainers** (7): Workout modifications, form checks, exercise progressions
- **Doctors** (6): Medical consultations, health condition management
- **Physical Education Experts** (4): Movement therapy, exercise science
- **Educators** (3): Health information, lifestyle guidance
- **Motivators** (1): Emotional support, goal setting, accountability

### Anonymity System (Brand Protection)
- **All team members appear as "Fitness Anny"** to users
- Users **never see individual names** or request specific people
- Maintains unified brand identity and professional standards

---

## Critical Operational Bottlenecks

### 1. Manual Order Assignment Crisis
**Current Process**: 3 real admins manually assign 50-80 expert orders daily

**Bottleneck Impact**:
- Peak hour delays (7-10pm) create user frustration
- Admin cognitive overload during high-volume periods
- Inconsistent assignment criteria
- No automated load balancing across 54 experts
- Complex specialization matching decisions

**Scale Problem**: **3 people managing order distribution for 54 experts**

### 2. Unsustainable Quality Control Review
**Current Process**: Real admins manually review **ALL daily chat conversations**

**Scale Problem**:
- **80 team members** producing hundreds of conversations daily
- 3 admins reviewing work of 80 people = **massive bottleneck**
- Time-intensive manual process
- Inconsistent quality standards
- Delayed feedback to team members

### 3. Team Efficiency Management
**Current Challenge**: Maximize productivity across 80 people while maintaining user satisfaction

**Complexity Factors**:
- 26 agents with varied experience levels
- 54 experts across 7 different specializations
- Uneven workload distribution (Nutritionists and Psychologists handle majority)
- Performance tracking and training coordination

---

## Additional Admin Panel Features

### Content Management (Admin-Only Access)
#### Live Event Scheduling & Management
- **Event Creation**: Schedule live workout sessions, webinars, Q&A sessions
- **Trainer Assignment**: Assign trainers to lead events (users still see "Fitness Anny")
- **Capacity Management**: Set limits and manage registrations
- **Real-time Monitoring**: Track attendance and engagement

#### Video Content Management (Vimeo Integration)
- **Upload Interface**: Direct Vimeo integration for video hosting
- **Content Organization**: Categorize by workout type, difficulty, specialization
- **Content Scheduling**: Manage release calendar
- **Quality Control**: Preview and approve before publication

### User Management & Payment Administration

#### User Management Tab
**Comprehensive Database Interface**:
- Complete user profiles and subscription status
- Payment method tracking (app vs web purchases)
- Progress photo management
- Health information and consultation history
- Usage analytics and engagement tracking

#### Payments Tab (Separated for Troubleshooting)
**Dedicated Payment Resolution**:
- Complete transaction history per user
- Duplicate payment detection and resolution
- Access issue troubleshooting ("paid but no access" scenarios)
- Platform payment conflict resolution (app store vs web)

**Common Admin Scenarios**:
- "I paid but don't have access" → Cross-reference payment with account status
- "Payment went through twice" → Identify duplicates and process refunds
- Subscription troubleshooting and billing dispute management

---

## Technical Architecture Context

### Current System Limitations
- **Legacy admin panel** not built for current 80-person scale
- **Separate systems** for chat, billing, user data, content management
- **Manual processes** that don't scale with team growth
- **Peak hour performance issues** during 7-10pm user demand

### External Dependencies
- **ejabberd** (chat system) - separate login and interface
- **Vimeo** integration for video hosting
- **Multiple payment systems** (app store vs web) creating complexity

---

## Key Performance Metrics & Targets

### Current Performance Benchmarks
**Response Times**:
- Chat agents average: 3.2 minutes (target: <2 minutes)
- Peak hour average: 5.8 minutes (major issue)
- Expert consultation assignment: 2.3 minutes to find available expert

**Productivity Metrics**:
- Conversations per agent per hour: 8 average (target: 12)
- Expert utilization: 72% (target: 80%)
- Order assignment efficiency: Manual bottleneck

### Business Impact Metrics
- **Customer satisfaction**: 4.6/5 (target: 4.7/5)
- **First-contact resolution**: 85% (target: 90%)
- **Expert escalation rate**: 18% (target: 15%)

---

## Automation Opportunities & Project Scope

### High-Impact Automation Targets

#### 1. Smart Order Assignment System
**Current**: 3 admins manually assign orders  
**Opportunity**: Automated routing based on:
- Expert availability and current workload
- Specialization matching
- User history and preferences
- Performance optimization algorithms

#### 2. AI-Powered Quality Control
**Current**: Manual review of all conversations  
**Opportunity**: 
- Automated conversation analysis for tone and accuracy
- Flagging system for conversations requiring human review
- Real-time quality scoring and feedback
- Template compliance checking

#### 3. Performance Analytics Dashboard
**Current**: Manual tracking and reporting  
**Opportunity**:
- Real-time productivity dashboards
- Automated performance coaching
- Workload balancing insights
- Predictive capacity planning

### Expected Business Impact
- **20% improvement in expert assignment speed**
- **30% reduction in admin manual work**
- **15% increase in agent productivity**
- **Support for 25,000+ users without proportional team growth**

---

## Project Considerations & Challenges

### Technical Complexity
- **Integration complexity** with existing chat, billing, and user systems
- **Scale requirements** for 80 concurrent users and 15,000+ customers
- **Real-time performance** needs during peak hours
- **Data consistency** across multiple integrated systems

### Operational Continuity
- **Zero downtime requirement** - system operates 14 hours daily, 6 days/week
- **Training coordination** for 80 team members on new systems
- **Quality maintenance** during transition period
- **Performance metrics continuity** throughout implementation

### Stakeholder Management
- **3 real admins** are primary system power users
- **26 chat agents** need efficient workflow tools
- **54 experts** require specialized interfaces
- **15,000+ users** expect consistent service quality

---

## Success Criteria & Expected Outcomes

### Operational Efficiency Goals
- **Reduce manual order assignment time** by 50%
- **Automate 70% of quality control reviews**
- **Increase team productivity** by 15% overall
- **Support 25,000 users** with minimal team expansion

### Technical Performance Targets
- **Sub-2-minute average response times** across all peak hours
- **Real-time order assignment** with automated expert matching
- **Unified dashboard experience** for all admin panel users
- **95% system uptime** during operational hours

### Business Impact Measures
- **Customer satisfaction improvement** to 4.7+/5
- **Expert utilization optimization** to 80%+
- **Scalable operations** supporting business growth targets
- **Competitive advantage preservation** through operational excellence

---

## Next Steps & Recommendations

### Immediate Project Priorities
1. **Deep-dive technical assessment** of current admin panel architecture
2. **Detailed workflow mapping** with the 3 real admins
3. **Integration requirements analysis** for chat, billing, and user systems
4. **Performance bottleneck identification** during peak operational hours

### Stakeholder Engagement Strategy
1. **Real Admins Workshop**: Map current workflows and pain points
2. **Agent/Expert Interviews**: Understand daily operational challenges
3. **Technical Architecture Review**: Assess integration complexity
4. **Phased Implementation Planning**: Minimize operational disruption

### Project Timeline Considerations
- **Current system must remain operational** throughout implementation
- **Peak hour performance** cannot be compromised during development
- **Training and adoption** coordination across 80 team members
- **Quality standards maintenance** during system transition

---

**Document Owner**: Product Manager  
**Technical Lead**: [To be assigned]  
**Stakeholder Review**: Real Admins + Operations Team  
**Next Update**: Weekly during active development

---

*This document provides foundational understanding for project planning. Additional technical specifications and detailed requirements gathering will be conducted during project kickoff phase.*