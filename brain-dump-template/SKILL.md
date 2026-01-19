---
name: brain-dumper
description: Capture thoughts, ideas, and notes quickly without structure. Use when the user says "note this", "brain dump", "record this for later", or shares a thought to save. Zero friction capture with minimal confirmation.
---

# Brain Dump Skill

## Purpose
Enable you to quickly capture thoughts, ideas, and notes without any structure or processing required. Dump anything on your mind, and organize it later during weekly reviews.

## Database ID
**IMPORTANT: Replace with your own Notion database collection ID**

- **Brain Dump**: `collection://YOUR-BRAIN-DUMP-DATABASE-ID`

### How to Find Your Collection ID
1. Open your Brain Dump database in Notion
2. Copy the URL from your browser
3. Extract the ID between the last `/` and `?v=`
4. Format as `collection://[ID with hyphens at positions 8,12,16,20]`

## How It Works

When you say something like:
- "Claude, note this: [thought/idea]"
- "Brain dump: [random idea]"
- "Record this for later: [something]"
- Or just share a thought and ask to save it

### Step 1: Capture the Note
Simply take whatever you say and capture it as-is. Don't:
- Try to organize it
- Summarize it
- Structure it
- Question it

Just capture it verbatim (or as close as possible).

### Step 2: Identify Related Context (Optional)
If you mention something that clearly relates to a known area/project, capture that in the "Related To" field.

But if it's not clear, leave "Related To" empty. Don't force it.

### Step 3: Create the Brain Dump Entry
Create a new page in the Brain Dump database with:
- **Note** (title): The captured thought/idea
- **Date**: Auto-populated (created time)
- **Processed**: Unchecked (default)
- **Related To**: Optional context if clear

### Step 4: Confirm
Give a brief, minimal acknowledgment:
- ✅ "Noted"
- ✅ "Got it"
- ✅ "Captured"

Keep it super brief - this is meant to be frictionless.

## Examples

**Input**: "Claude, note this: I want to explore partnering with local organizations for the community project"
- Note: "I want to explore partnering with local organizations for the community project"
- Related To: "Community Projects"
- Processed: Unchecked
- Response: "Noted"

**Input**: "Brain dump: what if the presentation isn't about features in general but specifically about user benefits?"
- Note: "what if the presentation isn't about features in general but specifically about user benefits?"
- Related To: "Presentations"
- Processed: Unchecked
- Response: "Got it"

**Input**: "Record this: feeling overwhelmed by all the projects, need to figure out how to prioritize"
- Note: "feeling overwhelmed by all the projects, need to figure out how to prioritize"
- Related To: (empty)
- Processed: Unchecked
- Response: "Captured"

## Setup Instructions

### Required Notion Database

**Brain Dump Database**
Properties:
- Note (Title)
- Date (Created time) - Auto-populates
- Processed (Checkbox) - Default: unchecked
- Related To (Text) - Optional context tag

### Your Related-To Contexts

Define 5-10 categories that make sense for your brain dumps.

Example contexts:
- Work Projects
- Personal Goals
- Business Ideas
- Writing Ideas
- Learning & Development
- Health & Wellness
- Financial Planning
- Home & Family
- Creative Projects
- Other

Update this list based on your actual life domains.

## Key Principles
1. **Zero friction** - make it as easy as possible to dump thoughts
2. **No judgment or filtering** - capture everything as-is
3. **Minimal confirmation** - don't interrupt flow
4. **Process later, not now** - the point is to get it out of your head
5. **Trust your process** - you'll organize when you're ready

## Integration

Works best with:
- **Note Processor Skill** - For weekly reviews of unprocessed notes
- **Action Keeper Skill** - Convert notes to tasks during processing
- **Work Structurer Skill** - Convert bigger ideas to projects

## Customization

After setup, update:
- Your Brain Dump database collection ID
- Your Related-To context categories
- Examples relevant to your work/life

## Credits

Based on the brain-dumper pattern for frictionless thought capture.
