# Claude Productivity Skills - Template Collection

A complete productivity system built on Claude Skills and Notion. These templates provide a proven workflow for capture, process, and structure.

## What's Included

This collection contains 5 interconnected Claude skills that work together:

### 1. Action Keeper
Intelligent task and reminder capture using natural language
- Routes automatically to Reminders (simple) or Tasks (complex)
- Semantic project matching
- Natural date/time parsing

### 2. Brain Dump
Zero-friction thought capture without structure
- Capture verbatim, process later
- Optional context tagging
- Minimal confirmation

### 3. Note Processor
Weekly review and processing of brain dumps
- Query unprocessed notes
- Convert to tasks, projects, or save elsewhere
- Track completion automatically

### 4. Problem Externalizer
Structured thinking for overwhelming situations
- 5-phase interview process
- Separates you from the problem
- Creates actionable clarity

### 5. Work Structurer
Organize everything into Notion hierarchy
- Areas → Projects → Tasks
- Discovery Mode for unclear goals
- Full hierarchy creation

## The Complete Workflow

```
CAPTURE                  PROCESS                    STRUCTURE
─────────────────────────────────────────────────────────────
Brain Dump          →   Note Processor        →   Work Structurer
Action Keeper                                  ↓
                                              Projects & Tasks
                        Problem Externalizer  →
```

## Installation

### Prerequisites

- Claude.ai account (with Skills enabled)
- Notion workspace
- Basic understanding of Notion databases

### Setup Process

**For each skill:**

1. **Create Required Notion Databases**
   - Follow database setup instructions in each skill's SKILL.md
   - Note the collection IDs for each database

2. **Customize the Skill File**
   - Open SKILL.md
   - Replace placeholder database IDs with your own
   - Update examples to match your workflow
   - Add your project names and contexts

3. **Package the Skill** (if you have packaging tools)
   - Or use the .skill file directly if provided

4. **Upload to Claude.ai**
   - Go to Settings → Skills
   - Click "Upload Skill"
   - Upload the .skill file or SKILL.md
   - Enable the skill

5. **Test It**
   - Try the example commands from the skill documentation
   - Verify it creates entries in your Notion databases

## Recommended Setup Order

1. **Brain Dump** (simplest, one database)
2. **Action Keeper** (core capture mechanism)
3. **Problem Externalizer** (no Notion databases needed)
4. **Work Structurer** (requires Areas + Projects setup)
5. **Note Processor** (ties everything together)

## Required Notion Databases

### Minimal Setup (Action Keeper + Brain Dump)
- Reminders
- Tasks
- Projects (with "General" project)
- Brain Dump

### Full Setup (All Skills)
- Reminders
- Tasks
- Projects (with "General" project)
- Areas of Interest
- Brain Dump

## Customization Guide

### Database IDs

Find your collection IDs:
1. Open database in Notion
2. Copy URL from browser
3. Extract ID between last `/` and `?v=`
4. Format as `collection://[ID-with-hyphens-at-8-12-16-20]`

Example:
- URL: `https://www.notion.so/2eb845ad210e80baabe2d51903515188`
- ID: `2eb845ad210e80baabe2d51903515188`
- Formatted: `collection://2eb845ad-210e-80ba-abe2-d51903515188`

### Personal Contexts

Update these lists in each skill:
- **Brain Dump**: Related-To contexts (5-10 categories)
- **Action Keeper**: Active project names
- **Work Structurer**: Areas of Interest, Active projects

### Examples

Replace generic examples with ones relevant to your:
- Work domain
- Project types
- Common tasks
- Life contexts

## Integration Patterns

**After Problem Externalization:**
→ Work Structurer creates project structure
→ Action Keeper creates first tasks

**During Weekly Review:**
→ Note Processor queries brain dumps
→ Converts to tasks (Action Keeper) or projects (Work Structurer)

**Daily Capture:**
→ Brain Dump for random thoughts
→ Action Keeper for concrete actions

## Best Practices

### Capture
- Use Brain Dump liberally - capture everything
- Use Action Keeper for anything with timing or project context
- Don't worry about organization during capture

### Process
- Schedule weekly review sessions
- Process brain dumps using Note Processor
- Use Problem Externalizer when feeling stuck

### Structure
- Define clear project goals (use Discovery Mode)
- Keep Areas broad, Projects specific
- Don't create tasks until needed

## Troubleshooting

**Skill not triggering:**
- Check trigger phrases in skill description
- Try exact phrases from examples
- Verify skill is enabled in Claude.ai

**Wrong database:**
- Double-check collection IDs
- Verify database has required properties
- Check for typos in collection:// format

**Integration not working:**
- Ensure all referenced skills are installed
- Verify database relations are set up correctly
- Check that "General" project exists

## Philosophy

This system follows these principles:

**Capture now, organize later**
- Zero friction during capture
- Structure during dedicated review time

**Separate person from problem**
- Problems are external challenges
- You are not your problems

**Intentional outcomes**
- Every project has a goal
- Goals can evolve
- "Designed on purpose" not by accident

**Trust the process**
- The system handles organization
- You focus on thinking and doing

## Credits

These skills are based on patterns developed through extensive trial and refinement. They represent proven workflows for productivity with ADHD-friendly design principles.

## License

These templates are provided as-is for personal use. Customize freely for your own workflow.

## Support

For questions about:
- **Claude Skills**: See Anthropic's documentation
- **Notion Setup**: See Notion's help center
- **These Templates**: Create an issue in this repository

## Version

Template Collection v1.0 - January 2026
