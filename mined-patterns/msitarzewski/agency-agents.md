# agency-agents — selected role contracts

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

Specialist prompts can improve deliverables while an entire roster adds unnecessary context. [README.md](https://github.com/msitarzewski/agency-agents/blob/765dbfb652da5e23ab48e28ac14c37392c0b18f7/README.md) describes roles with defined responsibilities and outputs; the installer supports selecting individual agents or divisions.

## What to mine

Start with Codebase Onboarding Engineer, Software Architect, Code Reviewer, Minimal Change Engineer, Technical Writer, and Prompt Engineer. Consider Multi-Agent Systems Architect, Voice AI Integration Engineer, Desktop App Engineer, and Section 508 Accessibility Specialist for relevant tasks. Keep RAG and privacy roles for later.

Extract scope, required inputs, output contracts, verification expectations, and handoff boundaries. A role is useful reference material even when it is executed by one agent rather than a separate process.

## Exclusions and proposed adaptation

Do not install the full roster, import personalities wholesale, or let role prompts override project rules. Adapt small role contracts for the existing planner/scout/implementer workflow; retain architecture, ambiguous requirements, and final verification with the orchestrator.

## Source entry points

- [Software Architect](https://github.com/msitarzewski/agency-agents/blob/765dbfb652da5e23ab48e28ac14c37392c0b18f7/engineering/engineering-software-architect.md)
- [Code Reviewer](https://github.com/msitarzewski/agency-agents/blob/765dbfb652da5e23ab48e28ac14c37392c0b18f7/engineering/engineering-code-reviewer.md)
- [Minimal Change Engineer](https://github.com/msitarzewski/agency-agents/blob/765dbfb652da5e23ab48e28ac14c37392c0b18f7/engineering/engineering-minimal-change-engineer.md)
- [Technical Writer](https://github.com/msitarzewski/agency-agents/blob/765dbfb652da5e23ab48e28ac14c37392c0b18f7/engineering/engineering-technical-writer.md)
- [Prompt Engineer](https://github.com/msitarzewski/agency-agents/blob/765dbfb652da5e23ab48e28ac14c37392c0b18f7/engineering/engineering-prompt-engineer.md)

- [Codebase Onboarding Engineer](https://github.com/msitarzewski/agency-agents/blob/765dbfb652da5e23ab48e28ac14c37392c0b18f7/engineering/engineering-codebase-onboarding-engineer.md)

## Next analysis

Compare each shortlisted role against existing skills before creating duplicates. Test whether a role improves a representative task with less unnecessary context. Individual role content and permissions still need review before adoption.
