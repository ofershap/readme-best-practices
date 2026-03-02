---
name: audit
description: Audit the current project's README for anti-patterns and missed best practices
---

Scan this project's README.md for anti-patterns and best practice violations.

Check for:
1. **Missing hook** - Does the first visible text sell the project in under 5 seconds?
2. **Generic section names** - "The Problem", "Introduction", "Overview", "About"
3. **Bold-label bullets** - `**Feature:** description` pattern instead of tables
4. **Broken asset references** - Images, GIFs, logos that don't exist on disk
5. **Non-copy-paste Quick Start** - `$` prefix, missing commands, fake output
6. **Missing author card** - Plain text author line instead of a visual card
7. **AI vocabulary** - "seamless", "robust", "comprehensive", "cutting-edge"
8. **Em dashes** - `—` characters anywhere in the file
9. **Fake badges** - npm badge but no npm package, CI badge but no workflow
10. **Cross-promotion** - "Other projects by" or "Check out my other repos" footers
11. **Excessive length** - Libraries over 300 lines, applications over 400 lines

For each issue found:
1. Show the line number and content
2. Explain what's wrong
3. Show the correct pattern
4. Rate severity: critical / warning / info

Use the readme-best-practices skill for reference on correct patterns.
