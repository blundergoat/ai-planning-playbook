# Generate Code Map Prompt

> **When to use:** When setting up context files for a new or existing project. Creates a scannable reference for AI agents and developers to quickly understand the repo layout.
>
> **Output:** `docs/code-map.md` — reference this from your [hot-path context file](08-claude-md-hot-path-prompt.md).
>
> **Next step:** Generate [system architecture diagrams](06-system-architecture-prompt.md) to map how your system is wired.

```
Create docs/code-map.md: a quick-reference tree map of the repository layout.
Use this format:

project-name/
├── file.yaml        = brief description
├── dir/
│   ├── subdir/      = brief description
│   └── file.go      = brief description
└── other/           = brief description

Rules:
- Explore the full directory structure before writing
- One-line "= description" for every entry
- Call out generated/never-edit files explicitly
- Group related items but don't go deeper than 3-4 levels (summarize beyond that)
- Include key files by name when they're important (e.g. router.go, api.ts)
- Note ports, stack choices, and tools inline where relevant
- Keep it scannable: someone should understand the project layout in 30 seconds
```

---

*Source: [BlunderGoat](https://www.blundergoat.com) · [AI Planning Playbook](https://www.blundergoat.com/articles/planning-first-playbook-ai-development)*
