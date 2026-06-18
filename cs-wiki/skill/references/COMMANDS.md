# Wiki Skill — Command Reference

All searches use agent tools (not Python CLI).

## Search CRM wiki
```bash
grep pattern:"<query>" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"
```
Dùng **Grep** tool. Multiple keywords = AND match (cùng dòng).

## Search full wiki
```bash
grep pattern:"<query>" include:"*.md" path:"cs-wiki/wiki/1.-Foundation"
```
Search tất cả thư mục con trong `1.-Foundation`.

## List CRM sections
Dùng **Read** tool để xem nội dung file. Các file CRM nằm tại `cs-wiki/wiki/1.-Foundation/CRM/`.

## Add/Edit FAQ
Dùng **Read** + **Edit** tool trực tiếp trên file:
1. Đọc file để tìm section
2. Thêm nội dung vào dưới `## <section-title>` với format:
   ```
   ### <Question>
   
   <Answer>
   ```

## Common patterns

| Intent | Cách làm |
|--------|---------|
| Tra cứu CRM | `grep pattern:"payment xanh" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"` |
| Tra cứu toàn bộ | `grep pattern:"enrollment" include:"*.md" path:"cs-wiki/wiki/1.-Foundation"` |
| Tìm file | `glob pattern:"**/*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"` |
