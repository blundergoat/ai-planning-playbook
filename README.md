# AI Planning Playbook

Vibe-coding is fast until it isn't. Plan sharply and ship reliably with AI.

Read the full article: [The Planning-First Playbook for AI-Assisted Development](https://www.blundergoat.com/articles/planning-first-playbook-ai-development)

A collection of templates, prompts, and workflows for planning software projects before handing them to AI coding agents. Born from the ashes of [BlunderLab](https://github.com/blundergoat) - 882 commits, ~21,500 lines of Python, 70 releases, and nothing worked. The engineering standards were there but the planning wasn't.

This playbook is the answer to: *"How would I approach this project with a real tech team?"* Plan before coding, sharpen that plan together, then build.

## What's Inside

| File | Description |
|---|---|
| [`01-feature-brief-template.md`](01-feature-brief-template.md) | Feature brief template (Problem, Users, Scope, Risks, Success Criteria) |
| [`02-mob-elaboration-prompt.md`](02-mob-elaboration-prompt.md) | Mob Elaboration - AI generates targeted questions to lock in requirements |
| [`03-sbao-ranking-prompt.md`](03-sbao-ranking-prompt.md) | Signal-Based Adaptive Orchestration - multi-agent plan ranking |
| [`04-milestone-planning-prompt.md`](04-milestone-planning-prompt.md) | Milestone planning: prototype, internal testers, production-ready, future improvements |
| [`05-code-map-prompt.md`](05-code-map-prompt.md) | Generate a quick-reference tree map of your repository layout |
| [`06-system-architecture-prompt.md`](06-system-architecture-prompt.md) | Generate Mermaid diagrams showing how your system works |
| [`07-domain-instruction-files-prompt.md`](07-domain-instruction-files-prompt.md) | Create cold-path domain instruction files per area of the codebase |
| [`08-claude-md-hot-path-prompt.md`](08-claude-md-hot-path-prompt.md) | Create a lean hot-path CLAUDE.md / AGENTS.md / GEMINI.md router |
| [`09-footguns-prompt.md`](09-footguns-prompt.md) | Seed and maintain a `docs/footguns.md` for preventive debugging |

## Quick Start

```bash
git clone https://github.com/blundergoat/ai-planning-playbook.git
```

**Existing codebase with no context files?** Go straight to [`05-code-map-prompt.md`](05-code-map-prompt.md) through [`09-footguns-prompt.md`](09-footguns-prompt.md). Copy the prompts into your coding agent and ask it to build a hot/cold file strategy for your project.

**New feature or project?** Start with the [feature brief](01-feature-brief-template.md). Create a `requirements-<feature-name>.md`, run it through the [Mob Elaboration prompt](02-mob-elaboration-prompt.md), then use [SBAO](03-sbao-ranking-prompt.md) to pressure-test the plan with multiple agents before anyone writes code.

**Ready to break work into tasks?** Use the [milestone planning prompt](04-milestone-planning-prompt.md) to structure objectives, exit criteria, and gotchas before handing off to a developer or agent.

## Core Ideas

### Plan Before You Code
AI coding agents don't attend your meetings. They don't know what's most important until you tell them. Start with a [feature brief](01-feature-brief-template.md), a brain dump is fine, but make sure you understand *why* the feature was requested and how it benefits users.

### Multi-Agent Plan Refinement (SBAO)
Don't treat AI output as a single source of truth. Have multiple agents produce competing plans, rank them, and look for consensus signals. If three agents flag the same dependency as a blocker, that's a high-strength signal. [Details &rarr;](03-sbao-ranking-prompt.md)

### The AI Trap: Fast BDUF
AI makes Big Design Up Front dangerously easy. You can generate a fully future-proofed architecture in seconds, but the deeper you get, the more the context rots and the harder it is to change. Milestones force an evolutionary approach: prototype first, then iterate toward something shippable. [Details &rarr;](04-milestone-planning-prompt.md)

### Context Files Beat Good Prompts
Good context engineering means finding the smallest possible set of high-signal tokens that maximise the desired outcome. Separate your **hot path** (lean router, loaded every session) from your **cold path** (deep domain knowledge, loaded on demand). [Details &rarr;](08-claude-md-hot-path-prompt.md)

## Contributing

Clone the repo, adapt the templates to your project, and open a PR if you improve them. The prompts are designed to be flexible and adaptable to different types of projects and teams.

## License

Open source. If this playbook saves you from your own BlunderLab moment, star the repo and let me know what you built.
