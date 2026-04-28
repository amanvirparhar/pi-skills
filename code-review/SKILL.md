---
name: code-review
description: Review diff on the current branch against remote master. Use when the user asks for any type of code review.
---

Run `git diff origin/master...HEAD` to get the full diff (unstaged, staged, and committed changes on this branch).

Review every change for correctness, readability, performance, maintainability, and security.

For each issue, provide:
- File and line range
- Severity: minor / major / critical
- Concise explanation
- Concrete fix/resolution
