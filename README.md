# README Best Practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Your README is a landing page. You have 5 seconds before someone closes the tab. This plugin teaches
your AI agent to write READMEs that hook the reader and make them install.

> Every coding assistant defaults to dry, template-style documentation. This plugin changes that.
> Bold punchlines up front, scannable feature tables, copy-paste Quick Start blocks, visual author
> cards. The structure that top open source projects use, applied automatically.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/readme-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type    | Name                    | Description                                                                |
| ------- | ----------------------- | -------------------------------------------------------------------------- |
| Skill   | `readme-best-practices` | Full guide: BLUF headers, story sections, feature tables, author cards     |
| Rule    | `readme-best-practices` | Always-on rule that enforces great README patterns on every edit           |
| Command | `/create-readme`        | Create or rewrite the project README following the full best practices     |

## The Transformation

| Before                                 | After                                                     |
| -------------------------------------- | --------------------------------------------------------- |
| Generic "A tool that..." opening       | BLUF punchline: bold value prop in the first 3 lines      |
| Section called "The Problem"           | A name with personality: "Your Agent Works in a Void"     |
| `**Feature:** description` bullets     | Feature tables, scannable at a glance                     |
| Plain "Made by username"               | Visual author card with avatar and stats ([GitShow](https://gitshow.dev)) |
| Quick Start with `$` prefix            | Copy-paste ready bash blocks                              |
| All paragraphs the same length         | Varied structure: one-liners, short paragraphs, tables    |
| Missing demo GIF link                  | Assets verified on disk before referencing                |

## How It Works

The plugin embeds a complete README structure into your agent's behavior:

1. **BLUF header** - bold punchline first, context second. The reader decides in 3 seconds
2. **Navigation buttons** - for-the-badge style, linking to key sections
3. **Story section** - named with personality, not "Introduction" or "Overview"
4. **Feature tables** - scannable, two-column format instead of bullet lists
5. **Copy-paste Quick Start** - zero to running in under 30 seconds
6. **Author card** - [GitShow](https://gitshow.dev) renders a live card image from any GitHub username

The always-on rule enforces these patterns on every README edit, so nothing slips through.

## Related Plugins

- [ai-humanizer](https://github.com/ofershap/ai-humanizer) - Prevent AI-detectable patterns in all
  generated content, not just READMEs
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
