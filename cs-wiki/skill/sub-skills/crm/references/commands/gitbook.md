# GitBook Fetch

Use when wiki search returns no results.

## v1 GitBook
```bash
gitbook-crm_getPage(url: "https://mindxtech.gitbook.io/usage-crm-xschool/<path>")
```

## v2 GitBook
```bash
gitbook-crm-v2_getPage(url: "https://mindxtech.gitbook.io/usage-crm-v2-xschool/<path>")
```

## Protocol
1. Try common URL patterns first (`/contract`, `/product`, `/lead`, etc.)
2. If page not found → try search via MCP
3. If content found → **update wiki file first** → then answer from wiki
4. If not found → "Not yet documented in wiki"
