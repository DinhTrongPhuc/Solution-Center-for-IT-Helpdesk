# Workflow — Shared (all sub-skills)

## 0. Xác định hệ thống
Trước khi trả lời, xác định user đang hỏi về hệ thống nào:

| Hệ thống | Signal | Route |
|----------|--------|-------|
| **CRM v1** | crm.mindx.edu.vn, CRM cũ, giao diện xanh/trắng | → `sub-skills/crm/` + detect v1 |
| **CRM v2** | crm-v2.mindx.edu.vn, CRM mới, giao diện tím/trắng | → `sub-skills/crm/` + detect v2 |
| **LMS** | lms.mindx.vn, lớp học, điểm danh, học viên, khóa học | → `sub-skills/lms/` |
| **Web khác** | (future) | → sub-skill tương ứng |

> Nếu không rõ → hỏi user.

## 1. Classify Intent
Determine how-to vs bug/issue (see sub-skill workflow for domain-specific details).

## 2. Search
Dùng **Grep** tool với keywords để search wiki files:
- Search trong `cs-wiki/wiki/1.-Foundation/`
- VD: `grep pattern:"<query>" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/<system>"`
- Nếu không rõ `<system>` → dùng Glob tìm file `.md` trong `1.-Foundation/`

## 3. Read Results
Từ kết quả Grep, dùng **Read** tool đọc section match.

## 4. Not Found → Check GitBook
Use GitBook MCP tools for the relevant system:
- CRM v1: `gitbook-crm_searchDocumentation`
- CRM v2: `gitbook-crm-v2_searchDocumentation` 
- LMS: use webfetch to query `usage-lms-xschool`

If content found → update wiki → answer from wiki.

## 5. Answer
- Cite file + section + version tag (if CRM)
- If not found: "Chưa có trong wiki"
- Keep concise

## 6. Stop
No follow-up unless the user asks.
