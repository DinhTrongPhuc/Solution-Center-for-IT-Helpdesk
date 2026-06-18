# Rules

1. **Never guess** — only use content from the wiki. Do not invent workflows or features.
2. **Source from wiki files only** — do not cite GitBook directly. If content comes from GitBook, update wiki first, then cite wiki.
3. **Search before answering** — always search wiki with **Grep** tool first. See `references/commands/search.md`.
4. **Always cite sources** — include file, section, and version tag. Example: `CRM/Lead-Management > Lead Filters [v1]`
5. **Ask version first** — if the question doesn't clearly indicate CRM v1 or v2, ask the user before proceeding. See `protocol/PROTOCOL.md` for detection rules.
6. **Not found → check GitBook** — if wiki search returns nothing, check GitBook via MCP tools. Update wiki file → answer from wiki.
7. **Not found anywhere** → "Not yet documented in wiki"
8. **Wiki is merged** — files in `1.-Foundation/CRM/` are flat with `[v1]` / `[v2]` / `[v1+v2]` tags. Do not look for separate v1/v2 directories.
9. **Do not modify files** without user instruction — read-only by default.
10. **Report source** always — include the file path and section in every answer.
11. **Distinguish intent** — classify user message as "how-to" or "bug/issue" before processing. Do not treat a bug report as a how-to question.
12. **Bug workflow** — if bug/issue: identify version → identify affected feature → search Known Bugs (section 7) for workaround → if not found, guide escalation.
