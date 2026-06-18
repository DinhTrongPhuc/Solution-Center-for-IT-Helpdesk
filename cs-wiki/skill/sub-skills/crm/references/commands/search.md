# Search Wiki

## Cách search (dùng agent tools)

Dùng **Grep** tool thay vì CLI command:

### AND search
```bash
grep pattern:"upsale xám" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"
grep pattern:"hide phone" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"
```
Tất cả keywords phải match (cùng dòng).

### Exact phrase
```bash
grep pattern:"xem số điện thoại khách hàng" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"
grep pattern:"quản lý lead status" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"
```
Dùng quotes cho exact phrase.

### OR (bug search)
```bash
grep pattern:"upsale|phiếu thu|lead" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"
```
Dùng regex `|` để match bất kỳ keyword nào.

## Reading Results
- Kết quả Grep trả về: `file-path:line-number: matching line`
- Dùng **Read** tool để đọc section đầy đủ từ file
- Ghi chú version tag `[v1]` / `[v2]` / `[v1+v2]`
