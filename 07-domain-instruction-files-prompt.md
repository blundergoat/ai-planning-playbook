# Domain Instruction Files Prompt (Cold Path)

> **When to use:** When setting up the cold-path context layer for your project. Creates self-contained instruction files so the AI loads deep domain knowledge only when working in that area.
>
> **Note:** The `.github/instructions/` path follows GitHub Copilot conventions. For other tools, adapt the location (e.g., `docs/instructions/`, `.cursor/rules/`).
>
> **Output:** One `{domain}.instructions.md` file per area of the codebase — reference these from your [hot-path context file](08-claude-md-hot-path-prompt.md).
>
> **Next step:** Create the [hot-path context file](08-claude-md-hot-path-prompt.md) that ties all cold-path files together.

```
Create domain-specific instruction files in .github/instructions/ for each major area of this codebase. Each file should:
- Start with a YAML frontmatter containing `applyTo` glob pattern matching
the files it covers (e.g., applyTo: "apps/api/**/*.go")
- Cover: project structure for that domain, conventions, patterns to follow,
common gotchas, "never do this" warnings, and a complete code example
- Be self-contained: an AI agent reading only this file should be able to
work correctly in that area of the codebase
- Include a "See Also" line pointing back to CLAUDE.md / AGENTS.md / GEMINI.md
- Target 200-400 lines per file

Create one file per distinct domain (e.g., backend language, frontend framework, database/SQL, tests, infrastructure/DevOps, HTTP handlers if they have unique patterns). Name them: {domain}.instructions.md

Explore the codebase first to discover the actual conventions and patterns in use: don't invent new ones. Extract rules from what the code already does.
```

---

*Source: [BlunderGoat](https://www.blundergoat.com) · [AI Planning Playbook](https://www.blundergoat.com/articles/planning-first-playbook-ai-development)*
