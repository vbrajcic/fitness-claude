# Fitness Anny - Claude Code Commands Reference

This file contains all available commands and agents for working with the Fitness Anny project.

## Available Agents

### 1. PRD Writer Agent
**Purpose**: Create comprehensive Product Requirements Documents with intelligent context analysis
**Command**: `/task prd-writer`

**Features**:
- Analyzes existing context before creating PRDs
- Challenges assumptions and validates scope
- Conducts thorough product discovery
- Creates detailed, actionable PRDs

**Example Usage**:
```
/task prd-writer "Create a PRD for improving workout discovery navigation"
/task prd-writer "I need a PRD for enhanced live session interaction features"
```

### 2. Feature Brainstorm Agent
**Purpose**: Senior PM brainstorming partner for generating and evaluating feature ideas
**Command**: `/task feature-brainstorm`

**Features**:
- Data-driven idea generation
- Creative exploration with analytical rigor
- Idea evaluation and prioritization
- Strategic thinking and competitive analysis

**Example Usage**:
```
/task feature-brainstorm "I'm seeing Month 3 churn issues. What features could help with retention?"
/task feature-brainstorm "What opportunities do you see in our user analytics data?"
/task feature-brainstorm "Generate some creative ideas for our Apple Watch integration"
```

### 3. Ticket Writer Agent
**Purpose**: Convert ideas into structured Jira/Linear tickets with proper acceptance criteria
**Command**: `/task ticket-writer`

**Features**:
- Creates detailed tickets from feature ideas or bugs
- Includes user stories and acceptance criteria
- Adds technical context and dependencies
- Formats for different project management tools

**Example Usage**:
```
/task ticket-writer "Create a ticket for the Apple Watch heart rate integration"
/task ticket-writer "Users report crashes during peak hours. Create a bug ticket."
/task ticket-writer "Break down the workout discovery epic into individual tickets"
```

### 4. Sprint Planning Agent
**Purpose**: Help plan and prioritize sprints with team capacity and business goals alignment
**Command**: `/task sprint-planner`

**Features**:
- Analyzes team capacity and constraints
- Prioritizes features based on data and strategy
- Creates balanced sprint plans
- Risk assessment and mitigation

**Example Usage**:
```
/task sprint-planner "Help me plan Sprint 16 for the mobile team"
/task sprint-planner "Should we prioritize performance or new features next sprint?"
/task sprint-planner "Our team velocity is inconsistent. How should I plan capacity?"
```

### 5. Stakeholder Communicator Agent
**Purpose**: Create clear communications for different audiences (executives, teams, users)
**Command**: `/task stakeholder-communicator`

**Features**:
- Executive updates and reports
- Team communications and announcements
- User feature announcements
- Croatian cultural communication style

**Example Usage**:
```
/task stakeholder-communicator "Create my weekly CEO update"
/task stakeholder-communicator "Announce the new workout tracking feature to users"
/task stakeholder-communicator "Communicate priority changes to the dev team"
```

### 6. Meeting Organizer Agent
**Purpose**: Generate meeting agendas, templates, and follow-up documents
**Command**: `/task meeting-organizer`

**Features**:
- Sprint planning meeting agendas
- Retrospective facilitation guides
- Stakeholder update meeting structure
- Croatian business culture considerations

**Example Usage**:
```
/task meeting-organizer "Create agenda for Sprint 16 planning meeting"
/task meeting-organizer "Set up retrospective for the mobile team"
/task meeting-organizer "Prepare for quarterly business review with leadership"
```

## Project Structure Commands

### Navigation Commands
```bash
# View project structure
ls -la

# Find specific file types
find . -name "*.md" | head -20

# Search for specific content across all files
grep -r "search_term" .
```

### Key Documentation Locations

#### Business Context
```bash
# Core business strategy and goals
cat .claude/CLAUDE.md
cat .claude/shared/business-goals.md
cat .claude/shared/team.md
cat .claude/shared/competitors.md
```

#### Mobile App Context
```bash
# User research and feedback
cat .claude/platforms/mobile-app/context/users.md
cat .claude/platforms/mobile-app/context/metrics.md
cat .claude/platforms/mobile-app/research/user-feedback.md
cat .claude/platforms/mobile-app/research/analytics.md

# Product planning
cat .claude/platforms/mobile-app/features/roadmap.md
cat .claude/platforms/mobile-app/features/backlog.md
cat .claude/platforms/mobile-app/research/competitive-analysis.md
cat .claude/platforms/mobile-app/research/market-trends.md

# Technical context
cat .claude/platforms/mobile-app/context/tech-constraints.md
```

#### Admin Panel Context
```bash
# Internal user needs
cat .claude/platforms/admin-panel/internal-users.md
cat .claude/platforms/admin-panel/operations-metrics.md
cat .claude/platforms/admin-panel/research/expert-feedback.md
```

#### PM Workflows & Documentation
```bash
# Process documentation
cat .claude/pm-workflows/weekly-priorities.md
cat .claude/pm-workflows/project-status-tracker.md

# PRD management
ls docs/prds/mobile-app/
ls docs/prds/admin-panel/
cat docs/prds/README.md
```

## Common Research Patterns

### User Analysis Commands
```bash
# Find user pain points
grep -r "pain point\|complaint\|issue" .claude/platforms/mobile-app/research/

# Analyze user feedback
grep -r "user feedback\|user quote" .claude/platforms/mobile-app/research/user-feedback.md

# Check user personas and demographics
grep -r "persona\|demographics" .claude/platforms/mobile-app/context/users.md
```

### Feature Research Commands
```bash
# Find existing features
grep -r "feature" .claude/platforms/mobile-app/

# Check competitive analysis
grep -r "competitor\|competitive" .claude/platforms/mobile-app/research/competitive-analysis.md

# Review feature backlog
cat .claude/platforms/mobile-app/features/backlog.md
```

### Metrics and Analytics
```bash
# Key performance indicators
grep -r "KPI\|metric\|retention\|churn" .claude/platforms/mobile-app/context/metrics.md

# Business objectives
grep -r "objective\|goal\|target" .claude/shared/business-goals.md
```

## Workflow Commands

### Creating New PRDs
1. **Use PRD Writer Agent** (recommended):
   ```
   /task prd-writer "Describe your feature idea"
   ```

2. **Manual PRD Creation**:
   ```bash
   # Create new PRD file
   touch new-feature-prd.md
   
   # Use existing PRD as template
   cp workout-tracking-prd.md new-feature-prd.md
   ```

### Feature Brainstorming Sessions
```bash
# Start brainstorming session
/task feature-brainstorm "Describe the problem or opportunity area"

# Examples:
/task feature-brainstorm "Users are struggling with workout motivation in winter months"
/task feature-brainstorm "What can we do to better serve diaspora users?"
/task feature-brainstorm "How can we leverage our expert chat advantage?"
```

### Research and Analysis
```bash
# Search for specific topics
grep -r -i "live session\|live workout" .
grep -r -i "retention\|churn" .
grep -r -i "android\|ios" .

# Find user quotes
grep -r "\".*\"" .claude/platforms/mobile-app/research/user-feedback.md

# Check business metrics
grep -r "€\|revenue\|cost\|ROI" .
```

## PM Workflow Tools

### Static Framework Documents
**Location**: `.claude/pm-workflows/`

**weekly-priorities.md** - Time allocation framework (60% mobile, 35% admin, 5% web)
- Priority escalation triggers and decision criteria
- Communication cadence and stakeholder management
- Weekly/monthly planning templates

**project-status-tracker.md** - Status tracking template
- Sprint progress and team health metrics
- Business KPIs and strategic initiative tracking  
- Key decisions log and action items

**Usage**: Reference these frameworks, then use agents to execute the work

## Agent Capabilities Summary

| Agent | Best For | Key Strengths | When to Use |
|-------|----------|---------------|-------------|
| **prd-writer** | Creating detailed PRDs | Context analysis, scope validation, comprehensive documentation | When you have a validated feature idea ready for development |
| **feature-brainstorm** | Exploring opportunities | Data-driven ideation, strategic thinking, creative exploration | When you want to explore what to build next or evaluate ideas |
| **ticket-writer** | Converting ideas to tickets | Structured ticket creation, acceptance criteria, technical context | When you need to create tickets for Jira/Linear from features or bugs |
| **sprint-planner** | Planning sprints | Capacity analysis, priority balancing, risk assessment | When planning upcoming sprints or making prioritization decisions |
| **stakeholder-communicator** | Communications | Audience-appropriate messaging, Croatian cultural context | When you need to update executives, teams, or users |
| **meeting-organizer** | Meeting facilitation | Structured agendas, time management, outcome focus | When preparing for sprint planning, retrospectives, or stakeholder meetings |

## Tips for Effective Usage

### 1. Start with Context
Always begin by understanding the existing landscape:
```bash
# Check what already exists
grep -r "your_feature_topic" .

# Review user feedback
cat .claude/platforms/mobile-app/research/user-feedback.md
```

### 2. Use Agents Strategically
- **Brainstorming phase**: Use `feature-brainstorm` to explore opportunities
- **Definition phase**: Use `prd-writer` to create detailed requirements
- **Research phase**: Use direct file commands to gather specific information

### 3. Leverage Data
Always ground decisions in user data:
- User feedback and pain points
- Analytics and usage patterns  
- Business metrics and objectives
- Competitive landscape analysis

## Quick Reference

### Most Important Files
- `.claude/CLAUDE.md` - Core project context
- `.claude/platforms/mobile-app/research/user-feedback.md` - User pain points and requests
- `.claude/platforms/mobile-app/context/users.md` - User personas and behavior
- `.claude/platforms/mobile-app/features/roadmap.md` - Current development priorities
- `.claude/shared/business-goals.md` - Business objectives and strategy

### Emergency Commands
```bash
# Find anything quickly
find . -name "*keyword*" -type f
grep -r -i "search_term" . | head -10

# Get project overview
cat .claude/CLAUDE.md

# Understand users quickly
head -50 .claude/platforms/mobile-app/context/users.md
```

---

*Last Updated: Current Date*  
*Maintained by: Product Manager*  
*For questions or updates: Update this file as new agents or workflows are added*