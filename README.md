# Claude Productivity Skills for Notion

A complete productivity system integrating Claude Skills with Notion databases for seamless thought capture, task management, and goal tracking.

## 🎯 What This Is

Five interconnected Claude Skills that create a complete productivity workflow:

1. **brain-dump-capture** - Frictionless thought capture
2. **task-creator** - Convert thoughts into actionable tasks  
3. **area-tracker** - Organize knowledge by theme
4. **okr-manager** - Quarterly goal setting and tracking
5. **weekly-processing** - Systematic review workflow

## 🔄 How They Work Together

```
Thought → Brain Dump → Weekly Processing → Task/Area → Link to OKR
```

**Example workflow:**
- Coffee chat generates 3 ideas → Brain dump captures them
- Weekly review: 1 becomes a task, 1 links to an area, 1 gets discarded
- Task automatically links to your Q1 Key Result
- Progress tracked toward quarterly goals

## ⚡ Features

- **Automatic linking** between brain dumps, tasks, areas, and OKRs
- **Smart defaults** for tags, priority, and status
- **Natural language triggers** - no need to memorize exact commands
- **Two-way relationships** - connected data across all systems
- **Progress tracking** - see how daily work connects to quarterly goals

## 📋 Prerequisites

1. **Claude.ai account** with Skills feature enabled
2. **Notion workspace** with the following databases:
   - Brain Dump
   - Tasks
   - Areas of Interest
   - Objectives (OKRs)
   - Key Results
   - Progress Log

## 🛠️ Setup Instructions

### Step 1: Create Notion Databases

Create these databases in your Notion workspace. Required fields for each:

**Brain Dump Database:**
- Note (title)
- Status (status: Unprocessed, Processing, Processed, Archived)
- Source (select: Brain Dump, Meeting Notes, etc.)
- Priority (select: High, Medium, Low)
- Tags (multi-select)
- Action Taken (select)
- Processing Notes (text)
- Related Tasks (relation to Tasks)
- Related Area of Interest (relation to Areas)

**Tasks Database:**
- Task Name (title)
- Status (status: To Do, In Progress, Done, etc.)
- Priority (select: High, Medium, Low)
- Created Date (date)
- Tags (multi-select)
- Description (text)
- Related Brain Dump (relation to Brain Dump)
- Related Key Results (relation to Key Results)
- Related Area of Interest (relation to Areas)

**Areas of Interest Database:**
- Interest (title)
- Status (status: Idea Stage, Active Exploration, Learning, Integrated, Archived)
- Category (multi-select)
- Date Added (date)
- Notes & Insights (text)
- Related Brain Dump (relation to Brain Dump)
- Related Tasks (relation to Tasks)

**Objectives Database:**
- Objective (title)
- Intent (text)
- Quarter (select: Q1, Q2, Q3, Q4)
- Status (status: Planning, Active, Completed, Paused, Abandoned)
- Related Key Results (relation to Key Results)

**Key Results Database:**
- Key Result (title)
- Target (text)
- Unit (select: posts, clients, revenue, etc.)
- Current Progress (number)
- Status (status: Not Started, On Track, At Risk, Behind, Completed)
- Related Objective (relation to Objectives)
- Related Tasks (relation to Tasks)

**Progress Log Database:**
- Current Progress (title)
- Month (select: January-December)
- Year (select: 2025, 2026, etc.)
- Progress Notes (text)
- Related Key Result (relation to Key Results)

### Step 2: Get Your Database URLs

1. Open each database in Notion
2. Click "..." → "Copy link"
3. Extract the ID from the URL (the long string of letters/numbers)

Example URL: `https://www.notion.so/2ec845ad210e807fb357e485e597ed62`  
Database ID: `2ec845ad210e807fb357e485e597ed62`

You'll also need the data source collection IDs (found in the database URL when viewing a specific view).

### Step 3: Update SKILL.md Files

For each skill, replace the placeholder database URLs with your own:

**In brain-dump-capture/SKILL.md:**
```markdown
- Database URL: `https://www.notion.so/YOUR-DATABASE-ID`
- Data Source: `collection://YOUR-COLLECTION-ID`
```

**Repeat for all 5 skills**, replacing:
- Brain Dump database URLs
- Tasks database URLs  
- Areas database URLs
- Objectives database URLs
- Key Results database URLs
- Progress Log database URLs

### Step 4: Install Skills in Claude.ai

1. Go to Claude.ai → Settings → Skills
2. Click "+ Add Skill"
3. Upload each `.zip` file (or paste SKILL.md content)
4. Repeat for all 5 skills

### Step 5: Test the System

In a new Claude conversation:

```
You: Brain dump: Test the new productivity system

Claude: Captured.

You: Process my brain dumps

Claude: You have 1 unprocessed brain dump...
```

If you see this, you're all set!

## 🎓 Usage Guide

### Brain Dump Capture

**Trigger phrases:**
- "Brain dump: [thought]"
- "Capture this: [idea]"
- "Remember: [note]"

**What it does:** Immediately saves to Notion with smart tags and priority

### Task Creator

**Trigger phrases:**
- "Create task: [action]"
- "Make this a task"
- "Turn my brain dump about X into a task"

**What it does:** Creates actionable tasks with dates, links to brain dumps/OKRs

### Weekly Processing

**Trigger phrase:** "Process my brain dumps"

**What it does:** Guides you through each unprocessed item with options:
- Create Task
- Add to Area
- Keep as Reference
- Discard

### Area Tracker

**Trigger phrases:**
- "Create area: [topic]"
- "Show me my active areas"
- "What topics am I thinking about most?"

**What it does:** Organizes your knowledge development by theme

### OKR Manager

**Trigger phrases:**
- "Create Q1 OKR: [objective]"
- "Update [key result] to [number]"
- "How's Q1 looking?"

**What it does:** Connects daily tasks to quarterly goals

## 💡 Best Practices

1. **Capture everything** - Process later, capture now
2. **Weekly processing** - Set recurring time (Friday afternoons)
3. **Link to OKRs** - Connect tasks to strategic goals
4. **Review monthly** - Update key result progress
5. **Archive regularly** - Keep areas and brain dumps current

## 🔧 Customization

Feel free to modify the skills:
- Add/remove tags
- Change status options
- Adjust priority levels
- Modify trigger phrases
- Add new fields

Edit skills in Claude.ai → Settings → Skills

## 🤝 Contributing

This system is open for others to use and improve. If you make enhancements:
- Fork this repo
- Make your changes
- Submit a pull request

## 📄 License

MIT License - Use freely, modify as needed

## 🙏 Credits

Built with Claude Skills and Notion API integration.

## ⚠️ Privacy Note

These skills contain database structure but no personal data. When you fork this repo:
- Replace all database URLs with your own
- Don't commit files with your actual database IDs to public repos
- Keep your Notion workspace private

## 📞 Support

Questions? Open an issue or reach out!

---

**Start capturing thoughts, building systems, and achieving goals.** 🚀
