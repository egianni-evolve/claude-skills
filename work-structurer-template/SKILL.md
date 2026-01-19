---
name: work-structurer
description: Structure work into proper Notion hierarchy (Areas → Projects → Tasks). Use when the user says "let's set up my projects", "help me structure this work", "break this project down", or after problem externalization when ready to organize. Creates full hierarchy with goals and helps discover project outcomes through guided questions.
---

# Work Structurer Skill

## Purpose
Help you translate ideas, goals, and work into the proper Notion structure (Areas → Projects → Tasks) without having to explain the system every time.

## Database IDs
**IMPORTANT: Replace these with your own Notion database collection IDs**

- **Areas of Interest**: `collection://YOUR-AREAS-DATABASE-ID`
- **Projects**: `collection://YOUR-PROJECTS-DATABASE-ID`
- **Tasks**: `collection://YOUR-TASKS-DATABASE-ID`

### How to Find Your Collection IDs
1. Open each database in Notion
2. Copy the URL from your browser
3. Extract the ID and format as `collection://[formatted-id]`

## The Structure Hierarchy

```
AREA OF INTEREST
├─ Description (what this area encompasses)
└─ PROJECTS
    ├─ Goal (what success looks like)
    ├─ Status (Active, Planning, On Hold, Complete, Archived)
    └─ TASKS
        ├─ Plan Date (when to do it)
        ├─ Due Date (deadline)
        └─ Status (Not started, In progress, Waiting, Complete, Cancelled)
```

## When to Use This Skill
When you say things like:
- "Let's set up my projects in Notion"
- "Help me structure this work"
- "I need to add this to my project system"
- "Let's break this project down into tasks"
- Or after Problem Externalizer when ready to organize

## How It Works

### Step 1: Understand the Scope
Ask clarifying questions:
- Is this a new Area of Interest?
- Is this a Project within an existing Area?
- Is this breaking down an existing Project into Tasks?
- Is this all of the above?

### Step 2: Start with Areas (if needed)
If creating or updating Areas:
- **Name**: Clear, concise label
- **Description**: What this area encompasses, why it matters

Examples:
- "Professional Development: Building expertise and thought leadership"
- "Business Operations: Core consulting and service delivery"
- "Personal Life: Health, relationships, and personal growth"

### Step 3: Create Projects
For each project:
- **Name**: Specific, outcome-focused
- **Goal**: What success looks like (use Discovery Mode if unclear)
- **Area**: Link to the appropriate Area of Interest
- **Status**: Active, Planning, On Hold, Complete, or Archived

### Discovery Mode: When the Goal Isn't Clear

If you don't know what success looks like yet, the skill helps discover it through questions:

**Discovery Questions:**
1. "What would make this feel successful to you?"
2. "What changes if this works?"
3. "Who benefits from this project?"
4. "If you completed this perfectly, what would be different?"
5. "What would disappointing look like? (so we can flip it)"

**When Goal is Still Fuzzy:**
That's okay! Write something like:
- "Explore and establish foundation in X space"
- "Build capability for future clarity"
- "Learn what's possible with Y"

Goals can evolve - they're not locked in forever.

### Step 4: Break Down into Tasks (Optional)
If you want to break a project into tasks:
- Keep task **titles** actionable and specific (verb + object)
- Use **Description** field for context, details, or notes
- Use Plan Date for "when I'll do this"
- Use Due Date for "when it must be done by"
- Link all tasks to the Project
- Default Status: "Not started"

### Step 5: Present the Structure
Shows clear visual hierarchy of what was created.

## Setup Instructions

### Required Notion Databases

**1. Areas of Interest Database**
Properties:
- Name (Title)
- Description (Text)

**2. Projects Database**
Properties:
- Name (Title)
- Status (Select: Active, Planning, On Hold, Complete, Archived)
- Goal (Text) - What success looks like
- Description (Text) - Additional context
- Area (Relation to Areas database)
- Start Date (Date) - Optional
- Target End (Date) - Optional

Create a "General" project as your default/catch-all.

**3. Tasks Database**
Properties:
- Task (Title)
- Description (Text)
- Project (Relation to Projects database)
- Status (Select: Not started, In progress, Waiting, Complete, Cancelled)
- Plan Date (Date)
- Due Date (Date)
- Priority (Select: High, Medium, Low) - Optional

### Your Areas of Interest

Define 5-10 broad life/work domains.

Example areas:
- Professional Development
- Business Operations
- Creative Projects
- Health & Wellness
- Financial Planning
- Personal Life
- Home & Family
- Learning & Growth

Update based on your actual domains.

### Your Active Projects

List your current active projects for reference.

Example projects:
- Website Redesign (Professional Development)
- Q1 Planning (Business Operations)
- Home Office Setup (Home & Family)
- Spanish Learning (Learning & Growth)
- General (catch-all)

## Key Principles

### 1. Don't Over-Task
Not every project needs tasks immediately. Sometimes just having the project defined is enough.

### 2. Think in Outcomes
Projects should be outcome-focused:
- ✅ "Launch New Service Offering"
- ✅ "Complete Website Redesign"
- ❌ "Work on website stuff"
- ❌ "Business things"

### 3. Areas are Broad, Projects are Specific
- **Area**: Business Operations (ongoing, no end date)
- **Project**: Launch New Service Offering (specific, has an outcome)

### 4. Status Reflects Reality
- "On Hold" is not failure - it's strategic pausing
- "Planning" means defined but not started
- Be honest about what's actually "Active"

### 5. Goals Create Clarity
Every project should have a Goal, even if it's fuzzy at first:
- Ask discovery questions when outcome isn't clear
- It's okay to start with "Explore X" or "Build foundation for Y"
- Goals can evolve - they're not permanent

### 6. Integrate with Other Skills
After structuring:
- Offer to create reminders for urgent tasks (Action Keeper Skill)
- Save additional thoughts to Brain Dump
- Use Problem Externalizer if feeling overwhelmed by scope

## Common Scenarios

**Scenario 1: Brand New Area + Projects**
Creates full area with description, multiple linked projects

**Scenario 2: Add Project to Existing Area**
Adds single project, links to area, sets status

**Scenario 3: Break Down Existing Project**
Fetches project, creates linked tasks with dates

**Scenario 4: Full Setup from Scratch**
Creates all areas, all projects, links everything, presents map

## Example Output

```
✅ Here's your complete structure in Notion:

💼 **Professional Development**
Building expertise and thought leadership

Projects:
   📋 Advanced Certification (Active)
      Goal: Complete certification and implement learnings
   📋 Portfolio Website (Active)
      Goal: Launch professional website with case studies

🎯 **Business Operations**
Core consulting and service delivery

Projects:
   📋 New Service Launch (Active)
      Goal: Launch with defined offering and first 3 clients
   📋 Client Onboarding System (Planning)
      Goal: Streamlined onboarding process

Want to break down any projects into tasks?
```

## Integration Points

**With Problem Externalizer:**
After externalizing a problem, offer: "Want me to set this up as a project in Notion?"

**With Action Keeper Skill:**
When creating tasks during setup, Action Keeper automatically handles:
- Routing to Tasks DB
- Date/time parsing
- Title vs description extraction
- Project linking

**With Brain Dump:**
If you mention additional ideas while structuring: "Want me to capture that in Brain Dump for later?"

## Customization

After setup, update:
- All database collection IDs
- Your Areas of Interest list
- Your active projects list
- Examples relevant to your workflow
- Status options if different

## Credits

Based on the work-structurer pattern for hierarchical project management.
