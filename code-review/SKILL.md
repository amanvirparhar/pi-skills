---
name: code-review
description: Review diff on the current branch against the remote's default branch. Use when the user asks for any type of code review.
---

Get the full diff against the remote's default branch by running these commands, all in one go:

```sh
git fetch origin --quiet
git --no-pager diff --merge-base origin/HEAD
git ls-files --others --exclude-standard -z \
  | xargs -0 -I{} git --no-pager diff --no-index -- /dev/null {}
```

Review every change for correctness, readability, performance, maintainability, and security.

For each issue, provide:
- File and line range
- Severity: minor / major / critical
- Concise explanation
- Concrete fix/resolution
