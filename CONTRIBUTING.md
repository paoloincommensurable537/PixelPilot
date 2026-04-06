# Contributing to PixelPilot

Thank you for your interest in contributing! This guide explains how to add new rules, fix issues, and maintain consistency across all editor configurations.

---

## Table of Contents

- [Before You Start](#before-you-start)
- [Repository Structure](#repository-structure)
- [Adding a New Rule](#adding-a-new-rule)
- [Updating Existing Rules](#updating-existing-rules)
- [Editor-Specific Guidelines](#editor-specific-guidelines)
- [Testing Your Changes](#testing-your-changes)
- [Submitting a Pull Request](#submitting-a-pull-request)

---

## Before You Start

1. **Read existing rules** - Start with `uiux-tokens.md` and `uiux-components.md`
2. **Check for duplicates** - Your idea might already be covered
3. **Open an issue first** - Discuss major additions before implementing
4. **Understand the structure** - See Repository Structure below

---

## Repository Structure

```
pixelpilot/
├── README.md                    # Main documentation
├── CHANGELOG.md                 # Version history
├── CONTRIBUTING.md              # This file
├── LICENSE                      # MIT License
│
├── cursor/                      # Cursor AI
│   ├── .cursorrules             # Main config (copy to project root)
│   └── .cursor/
│       └── rules/               # 91 rule files
│           ├── uiux-tokens.md
│           ├── uiux-components.md
│           └── ...
│
├── vscode/                      # VS Code / GitHub Copilot
│   └── .github/
│       ├── copilot-instructions.md    # Main config
│       └── instructions/              # 91 instruction files
│           ├── uiux-tokens.instructions.md
│           └── ...
│
├── windsurf/                    # Windsurf / Codeium
│   └── .windsurf/
│       └── rules/               # 91+ rule files with frontmatter
│           ├── uiux-main.md     # Always-on main rules
│           └── ...
│
├── opencode/                    # OpenCode
│   ├── AGENTS.md                # Main config (copy to project root)
│   └── .opencode/
│       └── rules/               # 91 rule files
│
└── zed/                         # Zed Editor
    └── .rules                   # Combined single file
```

---

## Adding a New Rule

### Step 1: Choose the Right Name

```
uiux-{category}.md
```

**Examples:**
- `uiux-charts.md` - Data visualization
- `uiux-drag-drop.md` - Drag and drop patterns
- `uiux-notifications.md` - Notification system

**Non-UI files (exceptions):**
- `reasoning.md` - Workflow skills
- `threat-modeling.md` - Security patterns
- `ai-*.md` - AI-specific skills

### Step 2: Use the Standard Template

```markdown
---
description: One-line description for AI to understand when to load this file.
---

# Title

Brief intro (2-3 sentences max).

---

## Section 1

Content with code examples...

---

## Section 2

More content...

---

## Checklist

- [ ] Requirement 1
- [ ] Requirement 2
```

### Step 3: Follow These Requirements

| Requirement | Required | Notes |
|-------------|----------|-------|
| YAML frontmatter | Yes | Must have `description` field |
| Design tokens | Yes | Never hardcode colors/spacing |
| Reduced motion | Yes | For any animation |
| Code examples | Yes | At least one per section |
| Accessibility | Yes | ARIA, keyboard, screen reader |
| Checklist | Recommended | Helps AI verify implementation |

### Step 4: Use Design Tokens

```css
/* BAD - hardcoded values */
.button {
  padding: 12px 24px;
  background: #3b82f6;
  border-radius: 8px;
}

/* GOOD - design tokens */
.button {
  padding: var(--space-12) var(--space-24);
  background: var(--color-primary);
  border-radius: var(--radius-md);
}
```

### Step 5: Respect Motion Preferences

```css
.animated-element {
  transition: transform 0.3s var(--ease-out);
}

@media (prefers-reduced-motion: reduce) {
  .animated-element {
    transition: none;
  }
}
```

### Step 6: Add to ALL Editors

When adding a new rule, you must add it to **every** editor folder:

| Editor | Location | Format |
|--------|----------|--------|
| Cursor | `cursor/.cursor/rules/` | `uiux-yourfile.md` |
| VS Code | `vscode/.github/instructions/` | `uiux-yourfile.instructions.md` |
| Windsurf | `windsurf/.windsurf/rules/` | `uiux-yourfile.md` (with frontmatter) |
| OpenCode | `opencode/.opencode/rules/` | `uiux-yourfile.md` |
| Zed | `zed/.rules` | Append to combined file |

---

## Updating Existing Rules

### What to Fix

- Typos and grammar
- Outdated code examples
- Missing accessibility attributes
- Broken links
- Missing edge cases

### What NOT to Change

- Design token names (breaking change)
- Law numbers in main configs
- Fundamental principles
- Required sections

---

## Editor-Specific Guidelines

### Cursor

- Main config: `.cursorrules`
- Rules folder: `.cursor/rules/`
- No special formatting required

### VS Code (GitHub Copilot)

- Main config: `.github/copilot-instructions.md`
- Rules folder: `.github/instructions/`
- Files must end with `.instructions.md`

### Windsurf

- Rules folder: `.windsurf/rules/`
- Requires YAML frontmatter with trigger:

```yaml
---
trigger: always_on
---
```

Trigger options:
- `always_on` - Always loaded
- `glob: "*.tsx"` - Loaded for matching files
- `model_decision` - AI decides when to load
- `manual` - User must explicitly request

### OpenCode

- Main config: `AGENTS.md` at project root
- Rules folder: `.opencode/rules/`
- No special formatting required

### Zed

- Single file: `.rules`
- All rules combined into one file
- Supports Markdown format

---

## Testing Your Changes

### Manual Testing

1. Copy your changes to a test project
2. Configure for your preferred editor
3. Ask the AI to implement something that triggers your rule
4. Verify the AI follows your guidelines

### Pre-Submit Checklist

- [ ] File has YAML frontmatter with `description`
- [ ] All values use design tokens
- [ ] All animations respect `prefers-reduced-motion`
- [ ] All interactive elements are accessible
- [ ] Code examples are complete and runnable
- [ ] No native browser UI (custom components only)
- [ ] Added to ALL editor folders
- [ ] Updated CHANGELOG.md

---

## Submitting a Pull Request

### Commit Message Format

```
type(scope): description

- Detail 1
- Detail 2
```

**Types:**
- `feat` - New rule file
- `fix` - Bug fix in existing rule
- `docs` - Documentation only
- `refactor` - Restructuring without behavior change

**Example:**
```
feat(rules): add uiux-charts.md for data visualization

- Bar, line, pie chart patterns
- Recharts integration with dark mode
- Accessible data tables fallback
```

### Pull Request Process

1. **Fork** the repository
2. **Create a branch:** `feat/uiux-charts`
3. **Make changes** following guidelines above
4. **Test** in a real project
5. **Submit PR** with description

### PR Template

```markdown
## What

Brief description of the change.

## Why

Why is this needed? Link to issue if applicable.

## Changes

- Added `uiux-yourfile.md` to all editor folders
- Updated CHANGELOG.md

## Checklist

- [ ] Follows naming convention
- [ ] Uses design tokens
- [ ] Includes accessibility
- [ ] Added to ALL editor folders
- [ ] Updated CHANGELOG.md
```

---

## Questions?

- **Open an issue** for questions or suggestions
- **Check existing issues** before asking
- **Tag maintainers** for design system questions

---

## Code of Conduct

Be respectful, constructive, and helpful. We're all here to make better UIs.

---

Thank you for contributing to PixelPilot!
