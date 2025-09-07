# Product Requirements Documents (PRDs)

Organized PRDs by platform and feature type for Fitness Anny.

## Directory Structure

```
docs/prds/
├── mobile-app/           # Mobile app features and improvements
├── admin-panel/          # Internal tools and agent workflows  
├── web/                  # Website features and optimizations
├── cross-platform/       # Features affecting multiple platforms
└── archived/             # Completed or deprecated PRDs
```

## Current PRDs

### Mobile App
- `workout-tracking-prd.md` - Workout history and progress tracking feature

### Admin Panel
- *No PRDs yet*

### Web Platform  
- *No PRDs yet*

### Cross-Platform
- *No PRDs yet*

## PRD Naming Convention

Use descriptive, consistent naming:
- **Feature PRDs**: `feature-name-prd.md` (e.g., `apple-watch-integration-prd.md`)
- **Improvement PRDs**: `improvement-area-prd.md` (e.g., `performance-optimization-prd.md`)
- **Epic PRDs**: `epic-name-prd.md` (e.g., `family-features-epic-prd.md`)

## Creating New PRDs

### Using the PRD Writer Agent
```bash
# The agent will ask where to save the PRD
/task prd-writer "Create PRD for [feature description]"

# When prompted for location, specify:
# - docs/prds/mobile-app/ for mobile features
# - docs/prds/admin-panel/ for internal tools
# - docs/prds/cross-platform/ for multi-platform features
```

### Manual PRD Creation
```bash
# Use existing PRD as template
cp docs/prds/mobile-app/workout-tracking-prd.md docs/prds/mobile-app/new-feature-prd.md
```

## PRD Status Tracking

Mark PRD status in the document title:
- `[DRAFT]` - In development, not final
- `[APPROVED]` - Ready for development  
- `[IN PROGRESS]` - Currently being implemented
- `[COMPLETED]` - Feature shipped and validated
- `[ARCHIVED]` - No longer relevant or superseded

### Example:
```markdown
# [APPROVED] PRD: Apple Watch Integration
# [IN PROGRESS] PRD: Live Session Discovery Improvements  
# [COMPLETED] PRD: Workout History & Progress Tracking
```

## PRD Review Process

1. **Draft**: Created by PM using prd-writer agent
2. **Technical Review**: Development team reviews feasibility
3. **Stakeholder Review**: Leadership approves business case
4. **Final Approval**: PM incorporates feedback and marks [APPROVED]
5. **Implementation**: Development team works from PRD
6. **Completion**: Feature shipped, PRD marked [COMPLETED]

## Integration with Project Management

### Link PRDs to Other Documents
- Reference PRDs in sprint planning (`.claude/pm-workflows/`)
- Include PRD status in project tracker updates
- Link tickets back to relevant PRDs

### PRD to Ticket Flow
```bash
# 1. Create PRD
/task prd-writer "Create PRD for feature X"

# 2. Break into tickets
/task ticket-writer "Break down [PRD name] into development tickets"

# 3. Plan implementation  
/task sprint-planner "Plan sprints for [PRD name] implementation"
```

---

*PRD Organization Owner*: Product Manager  
*Review Process*: Each PRD includes review checklist  
*Location Updates*: Update this README when adding new PRDs*