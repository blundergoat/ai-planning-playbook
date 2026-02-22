# Footguns Prompt

> **When to use:** After setting up your [hot-path context file](08-claude-md-hot-path-prompt.md). Creates a living document of cross-cutting issues that prevent bugs before they happen.
>
> **Output:** `docs/footguns.md` + a new hard rule in your context file.

```
Read docs/footguns.md. If it doesn't exist, create it. Seed it with 2-3 footguns from this codebase — real cross-cutting issues you can find evidence of in the code, comments, or docs (not invented ones). Use this format per entry:

## Footgun: [short name]
**Symptoms:** What the developer or AI sees when this bites
**Why it happens:** Root cause spanning multiple domains
**Prevention:** Concrete steps to avoid it

Then add this line to the Hard Rules section of CLAUDE.md / AGENTS.md / GEMINI.md:
- **Log footguns.** When you cause a bug that spans multiple domains (e.g., API + frontend, infra + auth), append it to `docs/footguns.md` using the existing format before closing the task.
```
