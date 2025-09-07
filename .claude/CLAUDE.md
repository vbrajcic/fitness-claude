# Fitness Anny - Project Context for Claude

## Business Overview
**Mission**: Empowering Balkan women 35+ to achieve fitness goals through personalized human support and convenient home-based solutions.

**Current Scale**: ~15,000 monthly subscribers  
**Target Market**: Women (80%) + Balkan diaspora (20%)  
**Revenue Model**: Monthly subscriptions (Basic, Premium, Premium Plus)  

## Strategic Priorities (Next 6 Months)
1. **Scale to 25,000+ subscribers** through improved user acquisition and retention
2. **Improve operational efficiency** to handle growth without proportional cost increase
3. **Reduce technical debt** to accelerate feature development velocity
4. **Strengthen competitive moat** through enhanced human support experience

## Platform Architecture & Focus
```
Mobile App (60% PM focus) → Daily user engagement, retention driver
Admin Panel (35% PM focus) → Operational backbone, 30 agents, efficiency critical  
Website (5% PM focus) → Acquisition funnel, minimal maintenance mode
```

## Key Business Challenges
- **Scaling Bottlenecks**: Chat agent efficiency limiting growth capacity
- **User Acquisition**: Need sustainable channels beyond word-of-mouth
- **Technical Debt**: Legacy admin panel constraining operational improvements
- **Development Capacity**: 5-person team stretched across 3 platforms

## Success Metrics Framework
**North Star**: Monthly Active Subscribers (Target: 25k by Q2)

**Primary KPIs**:
- Monthly Subscriber Growth Rate (Target: 15% monthly)
- Chat Response Time (Target: <2 min average)
- Monthly Churn Rate (Target: <15%)

**Secondary KPIs**:
- Daily Active Users / Subscriber Ratio (Target: >60%)
- Agent Productivity (Conversations/hour) (Target: 12/hour)
- Subscription Conversion Rate (Target: >3%)

**Operational Metrics**:
- App Performance (Target: <3s load time)
- System Uptime (Target: >99.5%)
- Feature Development Velocity (Target: 8 features/quarter)

## Competitive Landscape
**Direct Competitors**:
- Sweat (Kayla Itsines) - Global scale, no Croatian focus
- Freeletics - German-based, male-focused
- Nike Training Club - Free but no personal support

**Competitive Advantages**:
- 24/7 Croatian-speaking human experts (doctors, nutritionists, trainers)
- Deep understanding of Balkan culture and lifestyle
- Women 35+ specific approach (vs general audience)
- Integrated medical/wellness support beyond fitness

**Market Threats**:
- Global players entering Croatian market with localization
- AI-powered fitness apps reducing need for human support
- Economic downturn affecting discretionary spending

## Team Structure & Constraints
**Development Team**: 5 people (2 backend, 2 mobile, 1 designer)  
**Chat Team**: 30 agents/experts (8am-10pm Mon-Sat)  
**Leadership**: CEO (final product decisions), PM (day-to-day prioritization)

**Resource Constraints**:
- Development capacity is primary bottleneck
- No budget for additional hires in near term
- Designer shared across all platforms and marketing needs

## Technical Architecture
**Shared Backend**: Single system serving all platforms  
**External Dependencies**: Vimeo (video), ejabberd (chat)  
**Main Technical Debt**: Legacy admin panel not built for current scale  
**Performance Concerns**: Peak hour load during morning/evening workouts

## Decision Framework
**Priority Matrix**:
1. High Impact + Low Effort → Immediate development
2. High Impact + High Effort → Roadmap planning
3. Low Impact + Low Effort → Maintenance cycles
4. Low Impact + High Effort → Backlog/decline

**Platform Prioritization**:
- Mobile: User-facing improvements for retention/engagement
- Admin: Efficiency gains that enable scaling without hiring
- Website: Only critical conversion blockers

## Communication & Stakeholder Management
**Weekly CEO Updates**: Simple progress lists, focus on subscriber metrics  
**Development Team**: Bi-weekly releases, implementing formal sprints  
**Chat Team**: Monthly feedback collection for admin improvements

---

*Last Updated: [Current Date]*  
*Next Strategic Review: Quarterly*