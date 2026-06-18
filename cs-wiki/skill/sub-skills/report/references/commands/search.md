# Search Wiki (dùng agent tools)

Dùng **Grep** tool thay vì CLI command:

### AND search
```bash
grep pattern:"CR formula" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/Report-Application"
grep pattern:"MKT dashboard" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/Report-Application"
```

### Exact phrase
```bash
grep pattern:"call performance realtime" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/Report-Application"
```

### OR (bug search)
```bash
grep pattern:"lỗi realtime không load" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/Report-Application"
```
