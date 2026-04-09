# Personal Secretary Skill

A warm, general-purpose personal secretary skill for Claude.

This skill is designed to be configured in Claude Desktop, triggered proactively through Claude Cowork Dispatch, and used day to day through Claude conversations, including on mobile.

## What It Does

- Runs a full startup flow on first use
- Builds a reusable personal profile
- Sets greeting, reminder, and review rhythms
- Uses local memory files as the primary continuity layer
- Mirrors daily, weekly, and long-term memory to Notion for user viewing
- Supports startup revision later without rebuilding everything

## Default Domain Framework

By default, the secretary organizes commitments into four domains:

- Life
- Leisure
- Work
- Personal

These are only defaults. During startup, the user can keep them or define a different domain framework.

## Platform Model

- Setup and configuration happen in Claude Desktop
- Proactive outreach happens through Claude Cowork Dispatch
- Day-to-day interaction often happens through Claude conversations, including on mobile

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

This repository intentionally does not include runtime data, logs, local memory files, or private Notion configuration.

## Runtime Behavior

On first use, the skill should create local runtime files such as:

- `data/profile/personal-profile.md`
- `data/profile/startup-config.md`
- `data/memory/long-term-memory.md`
- `data/memory/weekly/YYYY-Www.md`
- `data/memory/daily/YYYY-MM-DD.md`
- `data/logs/interaction-log.md`
- `data/logs/startup-log.md`
- `data/notion/notion-config.md`
- `data/notion/sync-status.md`

These are runtime artifacts and should not be committed to a public repository.

## License

This release uses the MIT License.
