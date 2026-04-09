# Storage Conventions

Use local files as the primary source of truth. Prefer minimal metadata plus natural-language narrative.

Recommended runtime layout:

```text
data/
  profile/
    personal-profile.md
    startup-config.md
  memory/
    long-term-memory.md
    weekly/
      YYYY-Www.md
    daily/
      YYYY-MM-DD.md
  logs/
    interaction-log.md
    startup-log.md
  notion/
    notion-config.md
    sync-status.md
```

Storage rules:
- Profile and config files define stable setup
- Long-term, weekly, and daily memory files are separate layers
- Logs store summaries, not raw transcript dumps
- Notion config and sync state are tracked locally
- Keep records readable as diary-like notes
