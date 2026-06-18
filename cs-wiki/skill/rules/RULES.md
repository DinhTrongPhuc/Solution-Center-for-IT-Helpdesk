# Rules — Shared (all sub-skills)

1. **Never guess** — only use content from wiki files. Do not invent workflows or features.
2. **Source from wiki only** — do not cite GitBook directly. If content comes from GitBook, update wiki first, then cite wiki.
3. **Search before answering** — always search wiki with **Grep** tool first.
4. **Always cite sources** — include file, section, and version tag (if CRM). Example: `CRM/Lead-Management > Lead Filters [v1]` or `LMS/Classes > Điểm danh`.
5. **Distinguish intent** — classify user message as "how-to" or "bug/issue" before processing. Do not treat a bug report as a how-to question.
6. **Not found → check GitBook** — if wiki search returns nothing, check GitBook via MCP tools. Update wiki file → answer from wiki.
7. **Not found anywhere** → "Not yet documented in wiki" (or "Chưa có trong wiki").
8. **Do not modify files** without user instruction — read-only by default.
9. **Report source always** — include the file path and section in every answer.
10. **System boundary** — if question is about CRM → delegate to `sub-skills/crm/`. If LMS → delegate to `sub-skills/lms/`. If other → delegate to appropriate sub-skill.
11. **Skill to skill** — sub-skills inherit these rules. Each sub-skill adds its own domain-specific rules.
