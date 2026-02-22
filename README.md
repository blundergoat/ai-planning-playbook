# AI Planning Playbook

Vibe-coding is fast until it isn't. Plan sharply and ship reliably with AI.

Read the full article: [The Planning-First Playbook for AI-Assisted Development](https://www.blundergoat.com/articles/planning-first-playbook-ai-development)

Born from the ashes of [BlunderLab](https://github.com/blundergoat) — 882 commits, ~21,500 lines of Python, 70 releases, and nothing worked. The engineering standards were there. The planning wasn't.

## What's Inside

| File | Description |
|---|---|
| [`01-feature-brief-template.md`](01-feature-brief-template.md) | Feature brief template (Problem, Users, Scope, Risks, Success Criteria) |
| [`02-mob-elaboration-prompt.md`](02-mob-elaboration-prompt.md) | Mob Elaboration — AI generates targeted questions to lock in requirements |
| [`03-sbao-ranking-prompt.md`](03-sbao-ranking-prompt.md) | Signal-Based Adaptive Orchestration — multi-agent plan ranking |
| [`04-milestone-planning-prompt.md`](04-milestone-planning-prompt.md) | Milestone planning: prototype, internal testers, production-ready, future improvements |
| [`05-code-map-prompt.md`](05-code-map-prompt.md) | Quick-reference tree map of your repository layout |
| [`06-system-architecture-prompt.md`](06-system-architecture-prompt.md) | Mermaid diagrams showing how your system works |
| [`07-domain-instruction-files-prompt.md`](07-domain-instruction-files-prompt.md) | Cold-path domain instruction files per area of the codebase |
| [`08-claude-md-hot-path-prompt.md`](08-claude-md-hot-path-prompt.md) | Lean hot-path CLAUDE.md / AGENTS.md / GEMINI.md router |
| [`09-footguns-prompt.md`](09-footguns-prompt.md) | Seed and maintain a `docs/footguns.md` for preventive debugging |

## Quick Start

```bash
git clone https://github.com/blundergoat/ai-planning-playbook.git
```

**Existing codebase with no context files?** Go straight to files 05–09. Copy the prompts into your coding agent and ask it to build a hot/cold file strategy for your project.

**New feature or project?** Start with the [feature brief](01-feature-brief-template.md). Run it through [Mob Elaboration](02-mob-elaboration-prompt.md), then use [SBAO](03-sbao-ranking-prompt.md) to pressure-test the plan with multiple agents before anyone writes code.

**Ready to break work into tasks?** Use the [milestone planning prompt](04-milestone-planning-prompt.md) to structure objectives, exit criteria, and gotchas before handing off.

## License

Open source. If this saves you from your own BlunderLab moment, star the repo and let me know what you built.
