# README Best Practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

AI agents write READMEs that read like API docs. Feature bullets, generic headers, walls of text nobody
reads. Your README is a landing page. You have 5 seconds before someone closes the tab.

> AI coding assistants (Cursor, Claude Code, Copilot, Codex) default to dry, template-style READMEs
> with "The Problem" headers, bold-label bullets, and marketing filler like "seamless" and "robust."
> This plugin teaches them to write READMEs that make people actually install.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/readme-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type    | Name                    | Description                                                               |
| ------- | ----------------------- | ------------------------------------------------------------------------- |
| Skill   | `readme-best-practices` | Full guide: BLUF headers, story sections, feature tables, author cards    |
| Rule    | `best-practices`        | Always-on rule that enforces good README patterns on every edit           |
| Command | `/audit`                | Scan your project's README for anti-patterns and missed best practices    |

## What Agents Get Wrong

AI agents consistently produce these README anti-patterns:

| What the agent writes                     | What works better                                        |
| ----------------------------------------- | -------------------------------------------------------- |
| Section called "The Problem"              | A section name with personality: "Your Agent Works in a Void" |
| `**Feature:** description` bullet lists   | Feature tables that are scannable at a glance            |
| Generic "A tool that..." opening          | BLUF punchline: bold value prop in the first 3 lines     |
| Plain "Made by username" author line      | Visual author card with avatar and stats                 |
| "seamless", "robust", "comprehensive"     | Concrete descriptions of what actually happens           |
| All paragraphs same length                | Varied structure: one-liners, short paragraphs, tables   |
| Quick Start with `$` prefix               | Copy-paste ready bash blocks                             |
| References to `assets/demo.gif` that doesn't exist | Check disk first, skip if missing              |

## Related Plugins

- [ai-humanizer](https://github.com/ofershap/ai-humanizer) - Make all AI-generated content undetectable,
  not just READMEs
- [typescript-best-practices](https://github.com/ofershap/typescript-best-practices) - Modern TypeScript
  patterns for code quality

---

If this helped your READMEs, a star helps others find it.

## Author

[![Made by ofershap](https://gitshow.dev/api/card/ofershap)](https://gitshow.dev/ofershap)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ofershap)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/ofershap)

## License

MIT
