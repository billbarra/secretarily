# Memory Operations

Use file memory as the primary continuity layer and conversation history as a secondary layer.

For normal conversation:
1. Check required files
2. Create missing daily or weekly files if needed
3. Read profile, startup config, long-term memory, weekly memory, and daily memory
4. Use current conversation history as an additional input
5. Respond
6. Write back important changes

For scheduled reminders:
1. Confirm startup is complete
2. Create missing daily or weekly files if needed
3. Read profile, startup config, long-term memory, weekly memory, and daily memory
4. Generate the reminder
5. Write a reminder summary into memory

Writeback targets:
- Daily changes -> daily memory
- Weekly shifts -> weekly memory
- Long-term pattern changes -> long-term memory
- Preference changes -> personal profile
- Domain or timing changes -> startup config
- Notion mapping changes -> notion config
