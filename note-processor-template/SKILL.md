---
name: note-processor
description: Review and process unprocessed brain dump notes. Use when the user asks to see or process their notes, e.g., "what did I dump on you", "show me my notes", "let's process my brain dump", or "what notes do I need to process". Converts notes to tasks or projects.
---

# Note Processor Skill

## Purpose
Help you review and process your unprocessed brain dump notes during weekly review sessions. Turn raw thoughts into actionable items, project ideas, or organized knowledge.

## Database IDs
**IMPORTANT: Replace these with your own Notion database collection IDs**

- **Brain Dump**: `collection://YOUR-BRAIN-DUMP-DATABASE-ID`
- **Projects**: `collection://YOUR-PROJECTS-DATABASE-ID`
- **Tasks**: `collection://YOUR-TASKS-DATABASE-ID`
- **Reminders**: `collection://YOUR-REMINDERS-DATABASE-ID`
- **Areas of Interest**: `collection://YOUR-AREAS-DATABASE-ID`

### How to Find Your Collection IDs
1. Open each database in Notion
2. Copy the URL from your browser
3. Extract the ID and format as `collection://[formatted-id]`

## How It Works

When you say something like:
- "What did I dump on you?"
- "What notes do I need to process?"
- "Show me my unprocessed notes"
- "Let's process my brain dump"
- "What's in my brain dump from this week?"

### Step 1: Query Unprocessed Notes
Search the Brain Dump database for entries where:
- **Processed = Unchecked**
- Optionally filter by date range if you specify

### Step 2: Present the List
Show all unprocessed notes in a clean, scannable format with numbers for easy reference.

### Step 3: Help Process Each Note
As you work through notes, you might:

**A) Turn it into a reminder or task**
- Use the Action Keeper Skill
- Mark the note as Processed

**B) Turn it into a project idea**
- Use Work Structurer Skill
- Mark the note as Processed

**C) Save it elsewhere**
- Acknowledge you saved it (Notion, Drive, etc.)
- Mark the note as Processed

**D) Just mark it as done**
- Sometimes you just need to acknowledge it
- Mark the note as Processed

**E) Keep it unprocessed**
- Leave it for later
- Don't change Processed status

### Step 4: Update Processed Status
When done with a note, update the **Processed** field to Checked.

### Step 5: Wrap Up
Provide summary: "✅ Processed [X] notes, [Y] remain unprocessed"

## Processing Patterns

**Single Note Processing:**
"Process note #3" → Help with just that one note

**Batch Processing:**
"Let's process all of them" → Go through one by one

**Quick Scan:**
"Just show me what's there" → List them, no processing yet

**Selective Processing:**
"Just show me notes about [topic]" → Filter by Related To field

## Example Session

**User**: "What did I dump on you this week?"

**Claude**: "Here are your 6 unprocessed notes from this week:

1. Explore creating a workshop on [topic] - Jan 15
2. What if the project focused on [angle] instead? - Jan 14
3. Feeling like I need to slow down and focus - Jan 13
4. Great case study idea: [example] - Jan 12
5. Should reach out to [person] about collaboration - Jan 12
6. New tool idea: [description] - Jan 11

What would you like to do with these?"

**User**: "Let's make #5 a task to reach out this week"

**Claude**: ✅ "Got it - I'll remind you to reach out to [person] this week" [creates task + marks note as processed]

**User**: "I saved #4 to my writing folder, mark it processed"

**Claude**: ✅ "Marked as processed"

**User**: "#6 is actually a project - let's set it up properly"

**Claude**: [Uses Work Structurer Skill to create project] ✅ "Project created and note marked as processed"

## Setup Instructions

### Prerequisites

**Required Skills:**
- Brain Dump Skill (for capturing notes)
- Action Keeper Skill (for creating tasks/reminders)

**Recommended Skills:**
- Work Structurer Skill (for creating projects)
- Problem Externalizer Skill (for processing overwhelming notes)

### Processing Frequency

Set up a regular review cadence:
- Daily quick scan
- Weekly deep processing
- Monthly review
- Whatever works for your workflow

## Key Principles
1. **Flexible timing** - Support daily, weekly, or ad hoc processing
2. **Easy reference** - Number notes for quick reference
3. **Support various outcomes** - Task, project, save elsewhere, or just done
4. **Don't force processing** - If not ready, that's fine
5. **Track completion** - Update Processed status immediately
6. **Keep it conversational** - Not a chore, organizing thoughts
7. **Integrate with other skills** - Use Problem Externalizer, Work Structurer, Action Keeper

## Customization

After setup, update:
- All database collection IDs
- Your Related-To contexts
- Processing frequency preferences
- Examples relevant to your workflow

## Credits

Based on the note-processor pattern for weekly review workflows.
