# Fitness Anny PM Toolkit - Usage Examples

Real-world examples showing how to use your agents, frameworks, and templates together for effective project management.

## 📅 Scenario 1: Weekly Planning & Execution

### Monday Morning - Priority Setting
**Use:** `weekly-priorities.md` framework + your user research data

1. **Check the framework allocation:**
   - 60% mobile app focus (24 hours)
   - 35% admin panel focus (14 hours)  
   - 5% website maintenance (2 hours)

2. **Review current metrics** from `project-status-tracker.md`:
   ```
   Monthly Active Subscribers: 16,200 / 25,000 target
   Android crash rate: 3.5% (above 2% target) ← PRIORITY
   Live session discovery complaints: 38% of feedback ← PRIORITY
   ```

3. **Apply escalation triggers** from weekly-priorities framework:
   - Crash rate >5% → Would be immediate focus shift
   - Current 3.5% → High priority but not emergency

### Tuesday - Sprint Planning
**Use:** `/task sprint-planner` agent

**Command:**
```
/task sprint-planner "Plan Sprint 16 for mobile team. We have 5 developers for 2 weeks. Priority issues: Android crash rate at 3.5% and live session discovery problems (38% of user complaints). Also continuing Apple Watch integration."
```

**Expected Agent Response:**
- Analyzes your user feedback showing discovery pain points
- Reviews team capacity and Apple Watch roadmap progress
- Suggests balanced sprint with 65% stability work, 35% feature work
- Recommends specific story point allocation and risk mitigation

### Wednesday - Create Tickets
**Use:** `/task ticket-writer` agent

**Commands:**
```
# High priority bug
/task ticket-writer "Android app crashes during peak hours (7-9pm). Affects 3.5% of users. Create a P1 bug ticket."

# Feature improvement  
/task ticket-writer "Users can't find live sessions easily - 38% of complaints. Create epic for live session discovery improvements."

# Technical task
/task ticket-writer "Apple Watch heart rate integration - continuing from Sprint 15. Create ticket for HealthKit data sync."
```

### Thursday - Prepare Sprint Planning Meeting
**Use:** `/task meeting-organizer` agent

**Command:**
```
/task meeting-organizer "Create agenda for Sprint 16 planning meeting with mobile team. Focus on crash fixes, live session discovery, and Apple Watch progress."
```

**Expected Output:**
- 2-hour structured agenda with time allocations
- Pre-meeting prep tasks for team
- Decision points and success criteria

### Friday - CEO Update
**Use:** `/task stakeholder-communicator` agent

**Command:**
```
/task stakeholder-communicator "Create weekly CEO update. Sprint 15 completed, Sprint 16 planning done. Focus: crash rate reduction efforts, discovery improvements planned, Apple Watch 75% complete."
```

---

## 🔥 Scenario 2: Crisis Management

### Situation: App Store Rating Drops to 3.8 ⭐
**Current Status:** Users complaining about app freezing during live sessions

### Immediate Response (First Hour)

1. **Update project status tracker:**
   ```markdown
   ## Crisis Status - [Date]
   **Issue**: App Store rating dropped to 3.8 (from 4.5)
   **Root Cause**: Live session freezing on Android devices
   **User Impact**: 65% of user base (Android users)
   **Business Impact**: Threatens 25k subscriber target
   ```

2. **Create crisis communication:**
   ```
   /task stakeholder-communicator "App Store rating dropped to 3.8 due to Android live session freezing. Need immediate crisis communication for CEO and team."
   ```

3. **Emergency ticket creation:**
   ```
   /task ticket-writer "CRITICAL: Android app freezing during live sessions. Multiple app store reviews. Create P0 ticket with immediate action plan."
   ```

### Day 1-3: Sprint Adjustment

4. **Replan current sprint:**
   ```
   /task sprint-planner "Emergency replanning. Android live session freezing is P0. Current Sprint 16 has Apple Watch work and discovery improvements. How do we adjust for crisis response?"
   ```

5. **Team communication:**
   ```
   /task stakeholder-communicator "Communicate sprint priority change to development team. Pausing Apple Watch work to focus on Android stability crisis."
   ```

6. **Stakeholder meeting:**
   ```
   /task meeting-organizer "Emergency stakeholder meeting. Topics: crisis response plan, resource reallocation, timeline impacts, user communication strategy."
   ```

---

## 🚀 Scenario 3: New Feature Development

### Situation: CEO Wants Family Workout Features
**Context:** Competitive pressure from family-focused fitness apps

### Week 1: Discovery & Validation

1. **Brainstorm opportunities:**
   ```
   /task feature-brainstorm "CEO wants family workout features to compete with family-focused apps. What opportunities do we have based on our Croatian family-focused user base?"
   ```

2. **Validate with existing research:**
   - Check `.claude/platforms/mobile-app/research/user-feedback.md`
   - Look for family-related requests: "My daughter joins me for stretching"
   - Review `.claude/platforms/mobile-app/features/backlog.md` for existing family ideas

3. **Evaluate strategic fit:**
   ```
   /task feature-brainstorm "Evaluate family workout features against our business goals: 25k subscribers, Croatian market focus, working mothers. Is this worth pursuing vs Apple Watch completion?"
   ```

### Week 2: Requirements & Planning

4. **Create comprehensive PRD:**
   ```
   /task prd-writer "Create PRD for family workout features. Target Croatian working mothers who want to include kids in fitness routines. Based on user feedback about family integration."
   ```

5. **Break down into tickets:**
   ```
   /task ticket-writer "Break down family workout features epic into individual tickets. Include kid-friendly content, family challenges, and safety considerations."
   ```

6. **Plan integration into roadmap:**
   ```
   /task sprint-planner "How do we integrate family workout features into our roadmap? Current priorities: performance, Apple Watch, discovery improvements. What's the capacity impact?"
   ```

---

## 📊 Scenario 4: Monthly Business Review

### Situation: Preparing for Board Meeting
**Context:** Q1 performance review, need to show progress toward 25k subscriber goal

### Data Preparation

1. **Update project status tracker** with comprehensive metrics:
   ```markdown
   ## Q1 2025 Performance Review
   
   ### North Star Metrics
   - Monthly Active Subscribers: 18,500 / 25,000 (74% of target)
   - Monthly Growth Rate: 12% (Target: 15%)
   - Churn Rate: 13% (Target: <12%) ✅
   
   ### Strategic Initiative Progress
   - Apple Watch Integration: 85% complete
   - Performance Optimization: 60% complete (crash rate: 2.1%)
   - Live Session Discovery: 30% complete (user complaints down 15%)
   ```

2. **Create board presentation:**
   ```
   /task stakeholder-communicator "Create quarterly board update. Q1 results: 18.5k subscribers (74% of target), Apple Watch nearly complete, performance improvements showing results. Need to address growth rate gap."
   ```

3. **Prepare for tough questions:**
   ```
   /task meeting-organizer "Prepare for Q1 board review meeting. Likely questions: why growth rate below target, resource allocation decisions, Q2 plan to reach 25k subscribers."
   ```

### Strategic Planning Session

4. **Analyze performance gaps:**
   ```
   /task feature-brainstorm "Growth rate is 12% vs 15% target. What opportunities can accelerate user acquisition and retention based on our data?"
   ```

5. **Plan Q2 roadmap adjustments:**
   ```
   /task sprint-planner "Based on Q1 performance, how should we adjust Q2 priorities? Apple Watch completing, but need growth acceleration ideas."
   ```

---

## 🔄 Scenario 5: Continuous Improvement Workflow

### Weekly Routine (Every Friday Afternoon)

1. **Review and update project status:**
   - Edit `.claude/pm-workflows/project-status-tracker.md`
   - Update sprint progress, metrics, and key decisions
   - Note any new user feedback themes or competitive intelligence

2. **Prepare next week using framework:**
   ```
   Check weekly-priorities.md for:
   - Time allocation reminders (60/35/5 split)
   - Escalation triggers (crash rate, response time, growth rate)
   - Communication cadence requirements
   ```

3. **Generate stakeholder communications:**
   ```
   /task stakeholder-communicator "Weekly CEO update with sprint progress, user metrics, and next week priorities"
   ```

4. **Team retrospective planning:**
   ```
   /task meeting-organizer "Sprint retrospective for mobile team. Recent focus on performance optimization and Apple Watch integration."
   ```

### Monthly Deep Dive (First Monday of Month)

1. **Strategic brainstorming:**
   ```
   /task feature-brainstorm "Monthly opportunity analysis. Review user feedback trends, competitive moves, and business metrics. What should we explore for next quarter?"
   ```

2. **Resource allocation review:**
   ```
   /task sprint-planner "Monthly capacity planning. Team performance review, upcoming holidays, skill development needs."
   ```

3. **Documentation updates:**
   - Update user personas in `.claude/platforms/mobile-app/context/users.md` with new insights
   - Revise roadmap in `.claude/platforms/mobile-app/features/roadmap.md`
   - Update competitive analysis with new market intelligence

---

## 💡 Pro Tips for Maximum Effectiveness

### 1. **Start with Context, Always**
Before using any agent, quickly check:
- Current metrics in project-status-tracker.md
- User feedback themes in research files  
- Strategic priorities in business-goals.md

### 2. **Combine Agents for Complex Tasks**
Example workflow for new feature:
```
feature-brainstorm → prd-writer → ticket-writer → sprint-planner → stakeholder-communicator
```

### 3. **Use Frameworks to Guide Agent Usage**
- Weekly-priorities.md tells you WHAT to focus on
- Agents help you execute HOW to do the work
- Project tracker captures WHAT was accomplished

### 4. **Iterate Based on Outcomes**
- If agent suggestions don't fit your context, give more specific prompts
- Update your documentation with new learnings
- Adjust frameworks based on what works in practice

### 5. **Croatian Context Matters**
Always mention relevant context in agent prompts:
- "Croatian working mothers" vs just "users"
- "65% Android user base" vs generic mobile users
- "Family-focused culture" vs individual fitness focus

---

## 🎯 Quick Reference Commands

```bash
# Weekly planning
/task sprint-planner "Plan next sprint with [context]"

# Turn ideas into tickets  
/task ticket-writer "Create ticket for [feature/bug description]"

# Explore opportunities
/task feature-brainstorm "What opportunities do you see in [problem area]?"

# Create requirements
/task prd-writer "Create PRD for [validated feature idea]"

# Prepare communications
/task stakeholder-communicator "Create [type] update for [audience]"

# Organize meetings
/task meeting-organizer "Create agenda for [meeting type] about [topics]"
```

Remember: These tools work best when used together as a complete workflow, not as isolated commands!

---

*Last Updated*: [Current Date]  
*Usage Tip*: Bookmark this file and refer back to these patterns as you develop your own PM rhythms*