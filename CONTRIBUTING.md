# Contributing to Claude Productivity Skills

Thanks for your interest in contributing! This project helps people build productivity systems using Claude Skills and Notion.

## 🎯 Ways to Contribute

### 1. Share Your Enhancements
- Modified trigger phrases that work better
- Additional field mappings
- New workflow patterns
- Integration with other tools

### 2. Improve Documentation
- Clearer setup instructions
- More usage examples
- Troubleshooting tips
- Video tutorials

### 3. Report Issues
- Bugs in skill logic
- Unclear documentation
- Missing features
- Compatibility problems

### 4. Create Templates
- New skill combinations
- Alternative database structures
- Industry-specific adaptations
- Workflow variations

## 🛠️ Development Guidelines

### Before Submitting Changes

1. **Test thoroughly** - Verify skills work with Notion databases
2. **Update documentation** - Explain what changed and why
3. **Keep it generic** - Don't include your personal database URLs
4. **Follow naming conventions** - Lowercase with hyphens

### Skill File Structure

```yaml
---
name: skill-name-lowercase-hyphens
description: Brief description of what the skill does
---

# Skill Name

## When to Use This Skill
[Trigger phrases and use cases]

## Technical Implementation
[Database URLs, field mappings, etc.]

## Interaction Patterns
[Examples of how the skill works]

## Response Style
[How Claude should respond]
```

### Commit Message Format

```
type: Brief description

Detailed explanation of changes:
- What changed
- Why it changed
- Impact on users
```

Types: `feat`, `fix`, `docs`, `refactor`, `test`

## 🔒 Privacy & Security

**Never commit:**
- Personal database URLs (use placeholders)
- API keys or credentials
- Private workspace data
- Personal task/note content

**Always:**
- Use `.env.example` for configuration templates
- Document what needs to be customized
- Keep examples generic

## 📝 Pull Request Process

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-enhancement`)
3. **Make your changes**
4. **Test with your own Notion setup**
5. **Update documentation** (README, SKILL.md files, etc.)
6. **Commit your changes** (`git commit -m 'feat: add amazing enhancement'`)
7. **Push to your fork** (`git push origin feature/amazing-enhancement`)
8. **Open a Pull Request**

### PR Checklist

- [ ] Skill names use lowercase and hyphens
- [ ] No personal database URLs committed
- [ ] Documentation updated
- [ ] Examples provided
- [ ] Tested with actual Notion databases
- [ ] Clear description of changes

## 🤔 Questions?

Open an issue with the `question` label and we'll help!

## 📜 Code of Conduct

- Be respectful and constructive
- Help others learn and improve
- Share knowledge generously
- Credit others' contributions

## 🎉 Recognition

Contributors will be recognized in the README and release notes!

---

**Thank you for helping make productivity systems more accessible!** 🚀
