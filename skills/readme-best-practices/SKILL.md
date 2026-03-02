---
name: readme-best-practices
description: Write READMEs that make people install. Use when creating, rewriting, or auditing a README for any open source project.
---

# README Best Practices

A README is a landing page. You have 5 seconds before someone closes the tab. Every line competes for attention. Write like you're selling, not documenting.

## Before Writing

1. **Understand the project** - read the source, understand what it does, who it's for
2. **Find the angle** - what problem does this solve? What's the current alternative? Why is the current alternative bad?
3. **Check for assets** - look for demo GIFs, screenshots, logos in `assets/`. Only reference files that exist on disk
4. **Study the repo** - look at existing READMEs in the workspace for established patterns and conventions

## Structure

### 1. Header Block (centered)

```markdown
<h1 align="center">project-name</h1>

<p align="center">
  <strong>Bold punchline. One sentence. The value prop.</strong>
</p>

<p align="center">
  Context that makes the punchline land.<br>
  Two or three lines max.
</p>

<p align="center">
  <em>A line that makes the reader curious enough to scroll.</em>
</p>
```

**BLUF - Bottom Line Up Front.** Lead with the punchline, not the setup. Bold it. The reader decides in 3 seconds whether to keep reading.

Good: "Multiple developers. One AI agent. Same conversation."
Good: "Your AI agent writes your code. The least you can do is give it an office."
Bad: "In today's collaborative development world, teams need better tools for..."

### 2. Navigation Buttons

```markdown
<p align="center">
  <a href="#quick-start"><img src="https://img.shields.io/badge/Quick_Start-grey?style=for-the-badge" alt="Quick Start" /></a>
  &nbsp;
  <a href="#features"><img src="https://img.shields.io/badge/Features-grey?style=for-the-badge" alt="Features" /></a>
  &nbsp;
  <a href="#contributing"><img src="https://img.shields.io/badge/Contributing-grey?style=for-the-badge" alt="Contributing" /></a>
</p>
```

3-4 buttons max. Grey `for-the-badge` style. Link to anchors. Use a colored button only for external links (live demo, hosted version).

### 3. Status Badges

```markdown
<p align="center">
  <a href="https://github.com/USER/REPO/actions/workflows/ci.yml"><img src="https://github.com/USER/REPO/actions/workflows/ci.yml/badge.svg" alt="CI" /></a>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT" /></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-strict-blue" alt="TypeScript" /></a>
</p>
```

Only badges that are true. No npm badge if not published. No Docker badge without a Dockerfile.

Badge URL reference:
- CI: `https://github.com/USER/REPO/actions/workflows/ci.yml/badge.svg`
- npm version: `https://img.shields.io/npm/v/PACKAGE.svg`
- npm downloads: `https://img.shields.io/npm/dm/PACKAGE.svg`
- License MIT: `https://img.shields.io/badge/License-MIT-yellow.svg`
- TypeScript: `https://img.shields.io/badge/TypeScript-strict-blue`
- Bundle size: `https://img.shields.io/badge/Bundle-SIZE-brightgreen.svg`

### 4. Horizontal Rule + Demo

```markdown
---

![Demo](assets/demo.gif)
```

If no demo GIF exists, skip entirely. Never reference missing assets.

### 5. The Story

This is the most important section. NOT called "The Problem" or "Introduction" or "Overview" or "About." Give it a name with personality.

Good: "Your Agent Works in a Void", "AI Spend Is a Blind Spot", "Two Developers, One Agent"
Bad: "The Problem", "Introduction", "Overview", "Motivation"

Content:
- Start with the reader's current situation. Make them feel it
- List the bad alternatives they use now (2-3 max)
- What this project does differently, in 1-2 paragraphs
- End with a crisp summary line

Never start with "In today's..." or "Have you ever..." or generic scene-setting. Start concrete.

### 6. Quick Start

Copy-paste ready. 3-5 bash lines. The reader goes from zero to running in 30 seconds.

```markdown
## Quick Start

\```bash
git clone https://github.com/user/repo.git
cd repo
npm install
npm run dev
\```

Open `http://localhost:3000`. Done.
```

### 7. Features

Use tables for features. Tables are scannable. Bold-label bullet lists are the most AI-detectable README pattern.

```markdown
| | |
|---|---|
| **Live streaming** | Responses stream to all participants simultaneously |
| **Message queue** | Messages get queued when the agent is busy, never lost |
| **Git awareness** | Sees branch, status, and diffs in real time |
```

Group features into 2-3 sections with short headers. Never dump 15 features in one table.

### 8. Architecture / Tech Stack

Brief component table, then a one-line stack summary:

```markdown
**Stack:** Next.js 16 · Socket.io · Claude Agent SDK · TypeScript (strict)
```

Use middle dots (`·`) for stack lists, not commas or bullets.

### 9. Author

Use a visual author card to make the author section stand out. [GitShow](https://gitshow.dev) renders a live card image from any GitHub username:

```markdown
## Author

[![Made by USERNAME](https://gitshow.dev/api/card/USERNAME)](https://gitshow.dev/USERNAME)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/USERNAME)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/USERNAME)
```

The GitShow card goes above the social badges. It renders as a 460x56 PNG with the author's avatar, name, and GitHub stats. Much better than a plain text "Made by" line.

### 10. License

```markdown
## License

[MIT](LICENSE) &copy; [Author Name](https://github.com/USERNAME)
```

## Anti-Patterns (Never Do These)

| Pattern | Why it's bad |
|---|---|
| Section called "The Problem" | Boring, reads like a homework assignment |
| `**Feature:** description` bullets | The #1 AI-detectable README pattern |
| All paragraphs same length | Vary them. Some one line, some a paragraph |
| References to missing assets | Broken images kill credibility instantly |
| "seamless", "robust", "comprehensive" | Marketing words that mean nothing |
| Opening with what the tool is | "A real-time collaborative..." is boring. Open with WHY |
| "Other projects by @user" footer | Looks self-promotional |
| "Happy coding!" at the end | Filler. Cut it |
| Em dashes everywhere | AI writing tell. Use hyphens with spaces or periods |
| `$` prefix in bash commands | Breaks copy-paste |

## Formatting Rules

- `align="center"` for the header block only. Body content is left-aligned
- Horizontal rules (`---`) between major sections, not between every section
- Tables over bullet lists for features
- Code blocks must be copy-paste ready
- Libraries: under 300 lines. Applications: under 400 lines
- Vary sentence length and paragraph structure

## Checklist

Before finishing any README, verify:
- [ ] Opening hook captures value in under 5 seconds
- [ ] No section called "The Problem", "Introduction", or "Overview"
- [ ] Quick Start is copy-paste ready, under 5 commands
- [ ] No references to files that don't exist
- [ ] All badges are truthful
- [ ] Feature tables, not bold-label bullet lists
- [ ] No AI vocabulary (seamless, robust, comprehensive, cutting-edge)
- [ ] No em dashes
- [ ] Under 400 lines total
- [ ] Author section has a visual card (GitShow or similar)
- [ ] No "Other projects" or cross-promotion footers
