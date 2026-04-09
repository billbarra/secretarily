# Secretarily

Secretarily is a Claude skill for scheduling, reflective reviews, and emotional support. It is designed to feel like a warm personal secretary rather than a cold task tracker: helping users remember what matters, receive timely prompts, reflect on their state, and adjust plans without losing context.

## What It Helps With

- Daily scheduling and reminders
- Weekly planning and review
- Emotional check-ins before or after important tasks
- Startup onboarding for new users
- Ongoing secretary-style support that can be revised over time

## Why It Is Different

Most calendar or todo systems track events. Secretarily is designed to carry context.

It does that by combining:

- scheduling support
- reflective review
- emotional support
- local memory files for continuity
- Notion mirroring for user-facing browsing

The goal is not just to remind someone about tasks, but to help them maintain a rhythm, understand overload, and make future plans feel more realistic and humane.

## Quick Start

If Cowork cannot access GitHub directly, use a packaged copy of this repository instead of pulling from GitHub inside Cowork.

1. Download a release zip of this project from a non-GitHub file host.
2. Extract the archive locally.
3. Copy `skills/personal-secretary/` into your Claude skills directory.
4. Open Claude Desktop and invoke `$personal-secretary`.
5. Let the startup flow build a profile, confirm domains, and set reminder and review rhythms.
6. Connect Notion if you want daily, weekly, and long-term memory views.
7. Use Cowork Dispatch for proactive reminders and reviews.

### Manual Install

The only folder you need at runtime is:

```text
skills/
  personal-secretary/
```

If you are distributing this skill to a Cowork environment with restricted GitHub access, ship that folder inside a zip file from an accessible host.

## Product Model

Secretarily is built around a three-part usage model:

1. Claude Desktop is the setup and control center
2. Claude Cowork Dispatch is the proactive reminder channel
3. Claude conversations, often on mobile, are the day-to-day interaction surface

In practice, that means the user can configure the secretary on desktop, receive proactive outreach through Dispatch, and continue short everyday interactions wherever they are.

## Core Workflow

On first use, the skill runs a startup flow that:

1. creates a personal profile
2. defines or confirms the user's main life domains
3. sets greeting, reminder, and review rhythms
4. initializes local memory
5. connects Notion databases for daily, weekly, and long-term memory views

After startup, the secretary works in four main modes:

- Reminder
- Organizing
- Companion
- Review

## Technical Approach

The skill uses a local-first memory architecture.

- Local files are the primary continuity layer
- Conversation history is a secondary layer
- Scheduled reminders must read memory files before producing output
- Important interactions write back into the appropriate memory layer
- Notion acts as a mirror for user-facing browsing rather than the primary brain

The memory model is layered:

- personal profile
- long-term memory
- weekly memory
- daily memory

This makes the skill more resilient in workflows where proactive reminders may run in separate Claude conversations.

## Default Domain Framework

By default, the secretary organizes commitments into four domains:

- Life
- Leisure
- Work
- Personal

These are only defaults. During startup, the user can keep them or define a different domain framework.

## Repository Layout

```text
skills/
  personal-secretary/
    SKILL.md
    agents/
      openai.yaml
    references/
    assets/
      templates/
```

## License

MIT
