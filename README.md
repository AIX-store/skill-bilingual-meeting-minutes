# Bilingual Meeting Minutes

An AI skill that turns a meeting transcript or rough notes into short, actionable minutes in English, Arabic or both. It pulls out decisions, action items with owners and due dates, open questions and a parking lot, and it handles meetings where people switch between Arabic and English. Nothing is invented: unclear owners and missing dates are flagged, not guessed.

## Install

Claude Code:

```
git clone https://github.com/AIX-store/skill-bilingual-meeting-minutes ~/.claude/skills/bilingual-meeting-minutes
```

Other agents (Codex, Cursor, Claude Desktop projects): copy the contents of `SKILL.md` into the agent's instructions or rules file.

## Example prompts

- "Here is the transcript from today's call. Give me minutes in Arabic and English."
- "Extract only the decisions and action items from these notes as a table."
- "Write a short recap email for the client based on this meeting."

## Licence

MIT, © 2026 CodeMeld LLC.

Listed on AiX: https://aixstore.ai/store
