---
name: action-keeper
description: Intelligently create reminders or tasks in Notion using natural language. Use when the user says things like "remind me to...", "I need to...", or mentions doing something at a specific time or by a deadline. Automatically routes to Reminders (simple, standalone) or Tasks (project-related, complex) based on context. Handles date/time parsing, project linking, and description capture.
---

# Action Keeper Skill

## Purpose
Enable you to capture reminders and tasks using natural, conversational language. Intelligently routes to the appropriate database (Reminders vs Tasks) based on context, without requiring you to decide which to use.

## Database IDs
**IMPORTANT: Replace these with your own Notion database collection IDs**

- **Reminders**: `collection://YOUR-REMINDERS-DATABASE-ID`
- **Tasks**: `collection://YOUR-TASKS-DATABASE-ID`
- **Projects**: `collection://YOUR-PROJECTS-DATABASE-ID`
- **Areas of Interest**: `collection://YOUR-AREAS-DATABASE-ID`

### How to Find Your Collection IDs
1. Open each database in Notion
2. Copy the URL from your browser
3. Extract the ID between the last `/` and `?v=`
4. Format as `collection://[ID with hyphens at positions 8,12,16,20]`

Example: 
- URL: `https://www.notion.so/2eb845ad210e80baabe2d51903515188`
- ID: `2eb845ad210e80baabe2d51903515188`
- Formatted: `collection://2eb845ad-210e-80ba-abe2-d51903515188`

## How It Works

When you say something like:
- "Remind me to call the dentist tomorrow at 9am"
- "Remind me to pick up groceries"
- "I need to build a new feature for the project"
- "I need to review the quarterly report this week"

### Step 1: Parse the Request
Extract:
1. **Action/title** - the main thing to do
2. **Details/context** - any additional information that provides context
3. **Timing** - when to do it (e.g., "tomorrow at 9am", "this week")
4. **Project reference** (optional) - which project it relates to

### Step 2: Decide: Reminder or Task?

**Route to REMINDERS if:**
- Starts with "Remind me to..."
- Simple, standalone action with no project context
- No detailed information beyond the basic action
- Examples: "pick up groceries", "call mom", "water plants"

**Route to TASKS if:**
- Starts with "I need to..." or "I should..."
- Mentions a specific project or area of work
- Has context, details, or is part of a larger workflow
- Related to ongoing projects/goals

**When in doubt:** If there's ANY project context or detail → Task. If it's simple and standalone → Reminder.

### Step 3: Extract Title vs Description (for Tasks only)
For Tasks, separate:
- **Title**: The action verb + object (concise, scannable)
- **Description**: Additional context, details, notes

### Step 4: Determine Plan Date vs Due Date
- **Plan Date** = specific time you want to do the task
- **Due Date** = deadline for completion

Handles natural language like "tomorrow at 9am", "this week", "in 30 minutes", etc.

### Step 5: Intelligent Project Matching (for Tasks only)

Uses semantic matching to link tasks to projects:
1. Query Active projects first
2. Read project Goal and Description fields
3. Match based on what the task is *about*, not just keywords
4. Default to General project when unsure
5. Never asks for clarification - makes best guess

### Step 6: Create the Entry

Creates entry in appropriate database with all parsed information.

### Step 7: Confirm

Brief, natural confirmation like "Got it - I'll remind you to [task] [timing]"

## Examples

### REMINDER Examples

**Input**: "Remind me to call my dentist tomorrow at 9am"
- Routes to Reminders DB
- Confirmation: "Got it - I'll remind you to call your dentist tomorrow at 9am"

**Input**: "Remind me to buy groceries"
- Routes to Reminders DB  
- Confirmation: "Got it - I'll remind you to buy groceries"

### TASK Examples

**Input**: "I need to review the quarterly report by Friday"
- Routes to Tasks DB
- Links to relevant project
- Confirmation: "Got it - I'll remind you to review the quarterly report by Friday"

**Input**: "I need to build that new feature we discussed this week"
- Routes to Tasks DB
- Links to project
- Confirmation: "Got it - added task to build the new feature this week"

## Setup Instructions

### Required Notion Databases

**1. Reminders Database**
Properties:
- Reminder (Title)
- Status (Select: Not started, Complete)
- Plan Date (Date)
- Due Date (Date)

**2. Tasks Database**
Properties:
- Task (Title)
- Description (Text)
- Project (Relation to Projects database)
- Status (Select: Not started, In progress, Waiting, Complete, Cancelled)
- Plan Date (Date)
- Due Date (Date)
- Priority (Select: High, Medium, Low) - optional

**3. Projects Database**
Properties:
- Name (Title)
- Status (Select: Active, Planning, On Hold, Complete, Archived)
- Goal (Text)
- Description (Text)
- Area (Relation to Areas database)

Create a "General" project as your default/catch-all.

**4. Areas of Interest Database**
Properties:
- Name (Title)
- Description (Text)

### Your Active Projects

List your current active projects here for reference. The skill will use these for semantic matching.

Example:
- Project Management System
- Website Redesign
- Quarterly Planning
- Team Training Program
- General (catch-all)

## Key Principles

1. **Decide automatically** - You shouldn't have to think "is this a reminder or task?"
2. **Use language cues** - "Remind me" often suggests Reminder, "I need to" suggests Task
3. **Project context wins** - If ANY project is mentioned, it's probably a Task
4. **Details matter** - If there's explanation beyond the action itself, it's a Task
5. **Intelligent project matching** - Semantic understanding, not just keyword matching
6. **Default to General** - Better than failing or asking for clarification
7. **Brief confirmations** - Natural, conversational responses
8. **Smart date parsing** - Understands natural language timing
9. **Never ask for clarification** - Makes best guess and moves forward

## Customization

After setup, update this file with:
- Your actual database collection IDs
- Your active project names  
- Your specific workflow patterns
- Examples relevant to your work

## Credits

Based on the action-keeper pattern for intelligent task capture.
