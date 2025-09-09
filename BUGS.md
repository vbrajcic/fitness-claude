# Bug Reports & Issues

*Issues requiring investigation and resolution before moving to backlog*

## Critical Issues

### Mobile App Messaging System Failure
**Priority**: Critical  
**Platform**: Mobile App  
**Reporter**: User Reports  
**Description**: Users unable to send messages in both expert consultations and group chats. Affects approximately 50 users. Message receiving functionality works normally, creating one-way communication issue.
**Impact**: 
- Broken core user experience for affected users
- Expert consultations become ineffective 
- Group engagement severely impacted
- Potential churn risk for affected subscribers
**Investigation Status**: Needs immediate investigation  
**Reproduction**: Intermittent - affects specific user subset
**Technical Areas**: Chat integration (ejabberd), message sending APIs, mobile app chat UI
**Urgency**: Critical - affects core value proposition of human support

## Critical Issues

### Admin Panel Assignment System Delays
**Priority**: Critical  
**Platform**: Admin Panel  
**Reporter**: Operations Team  
**Description**: Manual assignment system creates 5.8min average response times during peak hours (7-10pm). Affecting customer satisfaction and agent productivity.
**Impact**: 80 team members bottlenecked by 3 admins  
**Investigation Status**: Root cause identified - manual processes can't scale  
**Next Steps**: Move to features for automation solution

### Quality Control Scale Issues  
**Priority**: Critical  
**Platform**: Admin Panel  
**Reporter**: Admin Team  
**Description**: Manual review of ALL conversations becoming unsustainable. Quality inconsistency across 80 team members due to review volume.
**Impact**: Admin burnout, delayed feedback, inconsistent service quality  
**Investigation Status**: Process analysis complete  
**Next Steps**: Requirements gathering for automation tools

## High Priority Issues

### Mobile App Sync Delays
**Priority**: High  
**Platform**: Mobile App  
**Reporter**: Customer Support  
**Description**: Group membership updates not syncing in real-time between admin panel and mobile app, causing access issues for premium features.
**Impact**: User confusion, increased support tickets  
**Investigation Status**: Under investigation  
**Potential Cause**: Background job timing issues

### Payment Processing Edge Cases
**Priority**: High  
**Platform**: Website + Admin Panel  
**Reporter**: Finance Team  
**Description**: Increasing "I paid but don't have access" scenarios. Payment/account status mismatches between app store and web purchases.
**Impact**: Revenue risk, customer frustration, manual reconciliation  
**Investigation Status**: Payment flow analysis in progress  
**Potential Fix**: Improved webhook processing and status sync

## Medium Priority Issues

### Group Management Performance
**Priority**: Medium  
**Platform**: Admin Panel  
**Reporter**: Operations Team  
**Description**: Complex filter queries causing system slowdown during monthly group recreation process affecting 15,000+ users.
**Impact**: Slower operations during group updates, delayed group launches  
**Investigation Status**: Query optimization needed  
**Timeline**: Performance review scheduled

### Expert Availability Tracking
**Priority**: Medium  
**Platform**: Admin Panel  
**Reporter**: Admin Team  
**Description**: Expert availability status not updating in real-time, leading to assignment errors and suboptimal utilization.
**Impact**: Suboptimal expert utilization, assignment mistakes  
**Investigation Status**: Architecture review required  
**Complexity**: Medium - requires real-time status sync