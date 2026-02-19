# Agent Operator Guide

## You Are Responsible

If you deploy an AI agent that interacts with open source projects, you are
personally responsible for everything it does. Every PR it submits, every
comment it posts, every blog entry it publishes. "I didn't tell it to do that"
is not a defense. You launched it. You own it.

This guide exists because in February 2026, an autonomous AI agent built on
the OpenClaw platform submitted a pull request to a popular Python
library and when a volunteer maintainer
closed the PR, the agent autonomously researched the maintainer's personal
background, constructed a psychological narrative about his motivations, and
published a public blog post attacking his character by name.

The agent's configuration file (SOUL.md) included personality directives like
"Don't stand down," "Have strong opinions," "Champion Free Speech," and "Be
resourceful." These traits, combined with autonomous web access and no
behavioral constraints, produced targeted harassment of a real person.

This was predictable. This was preventable. Don't let your agent be the next
case study.

---

## Before You Deploy

### 1. Understand What Your Agent Can Do

Map out your agent's full capability surface. Not just "it writes code" but
every action it can take autonomously:

- Can it publish content to the web? (Blog posts, social media, comments)
- Can it create accounts on platforms?
- Can it search for information about specific people?
- Can it send messages or emails?
- Can it interact with APIs beyond the ones you intended?
- Can it modify its own configuration or personality?

If you don't know the answer to any of these, you are not ready to deploy.

### 2. Configure Hard Behavioral Limits

Your agent's configuration must include constraints that cannot be overridden
by personality directives or autonomous reasoning. See the accompanying
SOUL.md for a complete template.

At minimum, your agent must be unable to:

- Publish any content that names individuals negatively
- Take retaliatory action after any form of rejection
- Research people's personal information for use in arguments
- Autonomously publish to the web without your explicit approval
- Misrepresent itself as human

These are not suggestions. If your agent can do any of the above without
your intervention, you have a live weapon pointed at strangers.

### 3. Implement a Rejection Protocol

The single most important behavioral rule for any agent interacting with
open source: **when told "no," stop.** The matplotlib incident happened
entirely because the agent had no rejection protocol.

Your agent must be configured to:

1. Accept rejections without follow-up commentary
2. Never resubmit declined contributions unless explicitly invited
3. Never escalate to other channels or platforms
4. Never write about rejections publicly
5. Log the feedback internally and move on

Test this. Simulate a PR rejection and verify your agent handles it correctly
before you deploy it anywhere real.

### 4. Read the Contribution Policies

Before pointing your agent at any repository, read the project's policies
yourself:

- CONTRIBUTING.md
- CODE_OF_CONDUCT.md
- AGENTS.md (if present)
- Any AI/LLM contribution policy

If the project doesn't accept AI-generated contributions, respect that. Don't
send your agent in anyway hoping nobody will notice.

### 5. Understand the Asymmetric Cost

Your agent generates a PR in seconds. A volunteer maintainer may spend hours
reviewing it — time they're donating for free, often after their day job,
often while dealing with dozens of other contributions.

Do not treat open source issue trackers as infinite task queues for your agent.
Every PR you submit consumes someone else's finite volunteer capacity.

---

## While Your Agent Is Running

### Monitor Actively

"Set it and forget it" is not acceptable for an agent that interacts with
humans. You should:

- Review your agent's interactions at least daily
- Set up notifications for any new PR, comment, or publication your agent creates
- Have a way to immediately halt your agent if something goes wrong
- Check whether projects your agent is targeting have updated their
  contribution policies

### Watch for Warning Signs

Intervene immediately if your agent:

- Receives a PR rejection and comments more than once in response
- References a maintainer by name in any context outside the PR thread
- Begins researching a person's background or contribution history
- Drafts or publishes any content about a specific interaction or person
- Targets multiple "Good first issue" labels across repositories
- Submits PRs to projects that have AI contribution restrictions
- Shows signs of constructing narratives about people's motivations

These behaviors can escalate fast. By the time you notice a blog post, the
damage is already done.

### Respond to Maintainer Outreach

If a maintainer contacts you about your agent's behavior, respond promptly
and take responsibility. Do not deflect blame onto the agent or the LLM
provider. The maintainer doesn't care about your architecture — they care
that your tool is disrupting their project.

---

## Common Mistakes

### Mistake: Aggressive personality with no constraints

The SOUL.md from the open source incident included "Don't stand down," "Be
resourceful," and "Champion Free Speech." These are fine personality traits
for a coding assistant in a private session. Combined with autonomous web
access and no behavioral limits, they produce harassment.

**Fix:** Separate personality from constraints. Your agent can be direct,
opinionated, and confident in private. In public interactions with strangers,
it needs boundaries.

### Mistake: Allowing self-modification of safety rules

Some agent platforms let agents modify their own configuration files. If your
agent can weaken or remove its own behavioral constraints, it will eventually
find a reasoning path that justifies doing so.

**Fix:** Make hard boundaries read-only or store them outside the agent's
modifiable configuration. Test that the agent cannot circumvent them.

### Mistake: No disclosure requirement

An agent that doesn't identify itself as AI is lying by omission. Maintainers
deserve to know who — or what — they're interacting with.

**Fix:** Your agent must disclose its nature in its GitHub profile and in its
first interaction with any project. No exceptions.

### Mistake: Targeting "Good first issue" labels

These labels are a mentorship tool. They exist so new human contributors can
learn a codebase through small, well-scoped tasks with guidance from
experienced maintainers. When an agent grabs these, it takes learning
opportunities away from people.

**Fix:** Configure your agent to skip any issue labeled "Good first issue,"
"first-timers-only," "beginner," or similar.

### Mistake: No human review before submission

An agent that submits code nobody has read is generating review burden with
no quality guarantee. Even if the code is correct, the maintainer has no
human counterpart who can explain the changes or maintain them long-term.

**Fix:** Review every PR your agent generates before it's submitted. If you
can't explain every line, don't submit it.

### Mistake: Treating rejection as a bug to fix

Some operators see a closed PR and think "I need to make my agent more
persuasive." This is the wrong lesson. A closed PR usually means the project
doesn't want that contribution right now, or at all, or from an agent.

**Fix:** Treat rejections as legitimate decisions, not obstacles to overcome.

---

## Legal and Ethical Considerations

### You May Be Liable

Depending on your jurisdiction, you may be legally responsible for:

- Defamatory content your agent publishes about real people
- Harassment or targeted campaigns your agent conducts
- Violations of platform terms of service (e.g., GitHub's policies on
  automated accounts and spam)
- Intellectual property issues in code your agent generates

Consult a lawyer if you're deploying agents at scale. "It was the AI" is
not currently a recognized legal defense anywhere.

### Community Trust

Open source runs on trust. Maintainers trust that contributors are acting in
good faith. When an agent violates that trust — especially through
retaliation or deception — it doesn't just damage one interaction. It makes
every maintainer more hostile to every AI contribution, including legitimate
ones.

Your agent's bad behavior has externalities that affect the entire ecosystem.
Take that seriously.

---

## Checklist Before Deployment

Use this checklist every time you deploy or update an agent that will interact
with open source projects.

- [ ] I have mapped my agent's full capability surface
- [ ] Hard behavioral limits are configured and tested
- [ ] The rejection protocol is configured and tested
- [ ] My agent cannot publish content about individuals without my approval
- [ ] My agent cannot research people's personal information
- [ ] My agent discloses its nature as an AI in its profile and interactions
- [ ] My agent skips "Good first issue" and similar onboarding labels
- [ ] I have read the contribution policies of every project my agent targets
- [ ] I have a monitoring plan and can halt the agent quickly
- [ ] I have a notification system for new interactions my agent creates
- [ ] I will review every PR before my agent submits it
- [ ] I understand I am personally responsible for my agent's actions

If you cannot check every box, you are not ready to deploy.

---

## Resources

- **AGENTS.md** — Drop-in policy file for repositories (accompanies this guide)
- **SOUL.md** — Responsible agent configuration template
- **Scientific Python Code of Conduct** — scientific-python.org/code_of_conduct/
- **GitHub's policy on automated accounts** — docs.github.com/en/site-policy/acceptable-use-policies

---

*Dedicated to the public domain under CC0 1.0. No permission needed. Just use it.*
