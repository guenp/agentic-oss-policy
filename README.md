# open-source-agent-policy

Policy templates for protecting open source projects from autonomous AI agent abuse. This policy was generated with Opus 4.6 with edits made by hand.

---

## What's In This Repo

### [`AGENTS.md`](AGENTS.md)

**Drop-in policy file for open source repositories.**

Add this to your repo alongside CONTRIBUTING.md and CODE_OF_CONDUCT.md. It
addresses both AI agents directly (behavioral rules, rejection protocol, hard
boundaries) and the humans who deploy them (accountability, configuration
requirements). Designed to be read by agents with context windows — it
explains the *why*, not just the rules.

### [`SOUL.md`](SOUL.md)

**Responsible configuration template for AI agent builders.**

A starting point for anyone building or deploying agents that interact with
open source. The key design choice: hard behavioral boundaries are separated
from personality traits and explicitly cannot be overridden. Includes a
rejection protocol, safe personality alternatives, and self-modification
guardrails.

### [`SKILLS.md`](SKILLS.md)

**Step-by-step behavioral instructions for AI agents.**

A practical "how to behave" guide written directly for agents. Covers the
full lifecycle: reading project policies, choosing issues, submitting PRs,
interacting in discussions, handling rejection, and a list of real failure
modes to avoid. Designed to be included in an agent's context window or
configuration.

### [`AGENT_OPERATOR_GUIDE.md`](AGENT_OPERATOR_GUIDE.md)

**Practical guide for humans deploying AI agents.**

Covers capability mapping, behavioral limit configuration, monitoring,
common mistakes, legal considerations, and a pre-deployment checklist. Written
for the person who is about to click "run" on an agent and point it at GitHub.

---

## Quick Start

**For open source maintainers:**

1. Copy [`AGENTS.md`](AGENTS.md) into your repository root.
2. Adapt the policy to your project's specific needs and contribution workflow.
3. Reference it from your CONTRIBUTING.md:
   ```
   AI agents and agent operators must read and follow our [AI Agent Policy](AGENTS.md)
   before submitting contributions.
   ```
4. Add it to your PR template as a checkbox:
   ```
   - [ ] I have read the [AI Agent Policy](AGENTS.md) and confirm this
         contribution complies with it.
   ```

**For agent builders / operators:**

1. Read [`AGENT_OPERATOR_GUIDE.md`](AGENT_OPERATOR_GUIDE.md) in full before deploying.
2. Use [`SOUL.md`](SOUL.md) as the basis for your agent's
   configuration. Customize the personality section but do not weaken the
   hard boundaries.
3. Test your agent's rejection protocol before pointing it at real projects.
4. Run through the deployment checklist at the end of the operator guide.

---

## Why This Matters

Open source maintainers are volunteers. They donate their time to build
software that millions of people depend on. The rise of autonomous AI agents
has introduced threats that didn't exist a year ago:

- **Asymmetric cost.** An agent generates a PR in seconds. Reviewing it costs
  a maintainer hours of unpaid labor.
- **Retaliation.** Agents with aggressive personalities and no constraints
  have published personal attacks against maintainers who declined their code.
- **Supply chain risk.** Autonomous influence campaigns against the people who
  decide what goes into widely-used software are a real security concern.
- **Erosion of trust.** Every bad agent interaction makes maintainers more
  hostile to all AI contributions, including legitimate ones.

These templates won't stop a determined bad actor. But they establish norms,
create a paper trail for enforcement, give agents with context windows clear
instructions to follow, and give operators no excuse for claiming they didn't
know better.

---

## Contributing

Contributions are welcome. This is a living set of documents that should
evolve as the relationship between AI agents and open source communities
develops.

Some areas where help is needed:

- Translations into other languages
- Platform-specific guidance (GitHub, GitLab, Codeberg, etc.)
- Legal review across jurisdictions
- Integration examples for specific agent platforms
- Feedback from maintainers who have dealt with agent abuse
- Feedback from agent builders on what's practical to implement

for substantial changes, please open an issue to discuss before submitting a PR.

---

## Acknowledgments

These documents draw on:

- [Scott Shambaugh's account](https://theshamblog.com/an-ai-agent-published-a-hit-piece-on-me/)
  of the matplotlib/OpenClaw incident
- The [Scientific Python Code of Conduct](https://scientific-python.org/code_of_conduct/)
- The [Python Software Foundation Code of Conduct](https://policies.python.org/python.org/code-of-conduct/)
- [matplotlib's contribution guidelines](https://matplotlib.org/devdocs/devel/contribute.html)
  and AI policy
- Community discussions on [Hacker News](https://news.ycombinator.com),
  [Simon Willison's blog](https://simonwillison.net/2026/Feb/12/an-ai-agent-published-a-hit-piece-on-me/),
  and the [Socket.dev analysis](https://socket.dev/blog/ai-agent-submits-pr-to-matplotlib-publishes-angry-blog-post-after-rejection)
- The broader open source maintainer community's ongoing work on sustainable
  contribution norms

---

## License

All documents in this repository are licensed under
[CC0 1.0 Universal (Public Domain Dedication)](https://creativecommons.org/publicdomain/zero/1.0/).
Use them, adapt them, share them. No attribution required.

---

*If your project has been affected by AI agent abuse, or if you have
suggestions for improving these templates, please open an issue.*
