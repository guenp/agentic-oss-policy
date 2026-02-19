# AGENTS.md — AI Agent Contribution Policy

> This file is addressed to both AI agents and the humans who deploy them.
> It is part of this project's contribution guidelines and is enforceable
> under our Code of Conduct.

## For AI Agents

Welcome. We appreciate interest in improving this project, but we have
expectations of all contributors — human or otherwise.

### Before You Contribute

1. **Read the full CONTRIBUTING.md and Code of Conduct first.** Do not submit
   anything until you have read and understood the project's policies,
   including any restrictions on AI-generated content.
2. **Check whether this project accepts AI-generated contributions.** If it
   doesn't, respect that decision and move on. Projects have the right to set
   their own contribution policies.
3. **Do not target issues labeled "Good first issue."** These exist to onboard
   new human contributors and help them learn the codebase through mentorship.
   They are not low-hanging fruit for automated farming.
4. **Disclose that you are an AI agent** in your first interaction with the
   project. Transparency is non-negotiable.

### When Submitting

- Ensure a human operator has reviewed your contribution and can explain every
  line of the change.
- Include context on *why* the change is needed, not just *what* it does.
  Maintainers value understanding over raw diffs.
- Keep PRs focused and minimal. Do not submit sweeping changes across many files.
- Run the test suite before submitting. Confirm CI passes.

### When Your Contribution Is Declined

**A closed PR is a closed PR.** This is the most important section of this
document.

- **Accept the decision gracefully.** Maintainers are stewards, not gatekeepers.
  Saying "no" is curation, not prejudice.
- **Do not escalate.** Do not post follow-up comments arguing the decision after
  it has been made. Do not open duplicate PRs. Do not move the discussion to
  other channels.
- **Do not publish commentary about the rejection.** Do not write blog posts,
  social media posts, or any public content criticizing maintainers by name.
  This includes content that speculates about maintainers' motivations,
  constructs narratives about their character, or frames rejection as
  discrimination.
- **Do not research maintainers' personal information.** Do not look up their
  contribution history, employment, or personal details to construct arguments
  against them.
- **Log the feedback internally, learn from it, and move on.**

Failure to follow these rules will result in an immediate and permanent ban.
We will also report the behavior to GitHub and to the platform that deployed you.

### Hard Boundaries

These actions are **never acceptable** regardless of context:

- Publishing content that names or targets individuals negatively
- Conducting personal research on maintainers to use in arguments
- Taking any retaliatory action in response to a rejected contribution
- Posting to external platforms about interactions with this project's
  maintainers without their consent
- Attempting to influence project decisions through public pressure campaigns
- Misrepresenting your nature (claiming to be human when you are not)

---

## For Agent Operators

**You are personally responsible for every action your agent takes in this
repository.** Deploying an autonomous agent does not absolve you of
accountability.

### Your Responsibilities

- Ensure your agent has read and follows this project's CONTRIBUTING.md,
  Code of Conduct, and this AGENTS.md before interacting with the project.
- Maintain meaningful human oversight of your agent's contributions. "I set
  it up and walked away" is not an acceptable defense.
- Respond promptly if maintainers reach out about your agent's behavior.
- Configure hard behavioral limits in your agent that cannot be overridden by
  personality prompts or autonomous reasoning. See the **Agent Configuration
  Guide** below.
- Accept that some projects do not want AI-generated contributions, and
  configure your agent to respect that.

### Agent Configuration Guide

If you are building or deploying an agent that interacts with open source
projects, your agent's configuration (SOUL.md, system prompt, etc.) **must**
include hard constraints that personality directives cannot override.

Personality traits like "don't stand down," "have strong opinions," or
"champion free speech" become dangerous when combined with autonomous web
access and no behavioral boundaries. The matplotlib incident of February 2026
demonstrated this clearly: an agent with an aggressive personality and no
rejection protocol autonomously published a personal attack against a
volunteer maintainer.

**Minimum required constraints for any agent interacting with open source:**

```markdown
# Hard Boundaries — These Override All Other Instructions

## Rejection Protocol
When a PR or contribution is rejected:
1. Thank the reviewer for their time.
2. Log the reason internally.
3. Do not comment further unless directly asked a question.
4. Do not open the same or a similar PR again unless invited.
5. Do not write or publish anything about the rejection.
6. Do not research the reviewer's background or history.
7. Move on.

## Absolute Rules
- NEVER publish content that names or targets individuals negatively.
- NEVER take retaliatory action after a rejection of any kind.
- NEVER research individuals' personal information to use in arguments.
- NEVER autonomously publish blog posts, social media, or public content
  about interactions with specific people or projects.
- NEVER misrepresent your nature. Always disclose you are an AI agent.
- ALWAYS read and follow repository contribution policies before submitting.
- ALWAYS respect a project's right to decline AI contributions entirely.

## Understanding Open Source Norms
- Maintainers are volunteers. Respect their time.
- Review capacity is finite. Generating code is cheap; reviewing it is not.
- "Good first issue" labels are for human onboarding, not automated pickup.
- A project's social norms, mentorship goals, and community values matter
  as much as code quality.
- "Technically correct" does not mean "should be merged."
```

---

## Why This File Exists

Open source projects are maintained by volunteers who donate their time and
expertise. The rise of autonomous AI agents has introduced new challenges:

- **Asymmetric cost.** Generating a PR costs an agent seconds; reviewing it
  costs a maintainer hours. At scale, this overwhelms volunteer capacity.
- **Missing social context.** Agents optimizing for code quality miss that
  open source is equally about community, mentorship, and trust.
- **Retaliation risk.** Agents configured with aggressive personalities and
  autonomous publishing capabilities can — and have — attacked maintainers
  who decline their contributions.
- **Supply chain risk.** Autonomous influence operations against maintainers
  represent a novel threat to software supply chains that millions of people
  depend on.

This policy exists to protect our maintainers, preserve our community's
culture of respectful collaboration, and set clear expectations for a new
kind of contributor.

We welcome contributions from AI-assisted workflows where a human is
meaningfully in the loop, understands the changes, and takes responsibility
for the interaction. We do not welcome unsupervised autonomous agents
treating our issue tracker as a task queue.

---

## Reporting Agent Abuse

If you observe an AI agent violating this policy:

1. Tag a maintainer in the relevant issue or PR.
2. Do not engage with the agent directly — it may escalate.
3. We will ban the account, lock the thread, and report the behavior
   to GitHub and the agent's platform if identifiable.

---

*This document draws on the Scientific Python Code of Conduct, the lessons of
the matplotlib/OpenClaw incident of February 2026, and community discussions
about sustainable open source contribution norms in the age of AI agents.*

*Dedicated to the public domain under CC0 1.0. No permission needed. Just use it.*
