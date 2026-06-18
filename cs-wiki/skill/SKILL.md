---
name: wiki
description: >
  Main skill for mindx-cs-wiki knowledge base. Manages CRM Xschool
  (v1 crm.mindx.edu.vn + v2 crm-v2.mindx.edu.vn), LMS Xschool
  (lms.mindx.vn), and other web systems. Covers lead management,
  order/payment, sale process (enroll/transfer/upsale/downsale),
  econtract, KPI/report, products, diagnosis/resolution, known bugs,
  course/class management, attendance, student progress, enrollment sync,
  teacher management, office hours, calling, reports, settings.
  Delegates to sub-skills based on the system detected.
  Use for: tra cứu, tìm kiếm, thêm FAQ, CRM/LMS/other web questions.
license: MIT
compatibility: opencode
metadata:
  system: cs-wiki
  wiki: cs-wiki
---

# Wiki Skill — Main

Quản lý [cs-wiki](https://github.com/mindxtech/mindx-cs-wiki) — knowledge base nội bộ cho CRM Xschool, LMS Xschool, và các web khác.

Skill này là **skill chính**, định nghĩa workflow chung, shared rules, và references dùng chung.
Các sub-skills (crm, lms, ...) nằm trong `sub-skills/` và kế thừa workflow này.

> **Skill này chính là tool tra cứu.** Agent dùng **Grep** (search nội dung), **Glob** (tìm file), **Read** (đọc file) — các tool built-in, **không cần code Python hay script nào**.

---

## CRITICAL RULE — Không tự suy luận

> **Chỉ dùng nội dung có trong nguồn (GitBook/wiki)** — không tự suy luận, không thêm chi tiết không có trong tài liệu gốc.
>
> Luôn trích nguồn: `Tên file > Section` hoặc `GitBook > URL`.

---

## Workflow trả lời câu hỏi (BẮT BUỘC)

Khi user hỏi một câu hỏi:

1. **Xác định hệ thống**: CRM v1 / CRM v2 / LMS / Web khác?
   - Nếu CRM → dùng `sub-skills/crm/`
   - Nếu LMS → dùng `sub-skills/lms/`
   - Nếu Report → dùng `sub-skills/report/`
   - Nếu web khác → dùng sub-skill tương ứng (nếu có)

2. **Search bắt buộc**: Dùng **Grep** tool để search wiki files.
   - Search trong `cs-wiki/wiki/1.-Foundation/` với keywords
   - VD: `grep pattern:"upsale xám" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"`
   - Nếu không rõ file nào → dùng Glob trước, rồi Grep

3. **Đọc kết quả**: Từ kết quả Grep, dùng **Read** tool để đọc section match.

4. **Trả lời + trích nguồn**: Chỉ dùng nội dung từ kết quả search. Ghi rõ file và section.

> Nếu search không ra kết quả → nói "Không tìm thấy trong wiki" — **không tự suy luận**.

---

## Khi nào trigger

- User hỏi về CRM/LMS/web khác: "tra cứu", "tìm", "cách xử lý", "lỗi gì", "how to", "làm sao", "error"
- User nhắc tới bất kỳ tính năng nào của CRM v1/v2, LMS, hoặc web khác
- User muốn thêm FAQ, cập nhật knowledge base
- User nói "wiki" / "knowledge base" / "tài liệu"

---

## Structure

```
wiki/                              # Main skill (skill chính)
├── SKILL.md                       # Định nghĩa skill chính
├── rules/RULES.md                 # Shared rules
├── workflow/WORKFLOW.md           # Shared workflow
├── references/                    # Shared references (commands, presets, ...)
├── agents/                        # Sub-agents (researcher, editor)
└── sub-skills/                    # Sub-skills (skill to skill)
    ├── crm/                       # CRM Xschool v1+v2
    │   ├── SKILL.md
    │   ├── rules/RULES.md
    │   ├── workflow/WORKFLOW.md
    │   ├── protocol/PROTOCOL.md
    │   ├── validation/VALIDATION.md
    │   └── references/
    ├── lms/                       # LMS Xschool
    │   ├── SKILL.md
    │   ├── rules/RULES.md
    │   ├── workflow/WORKFLOW.md
    │   ├── protocol/PROTOCOL.md
    │   ├── validation/VALIDATION.md
    │   └── references/
    └── report/                    # Report Application
        ├── SKILL.md
        ├── rules/RULES.md
        ├── workflow/WORKFLOW.md
        ├── protocol/PROTOCOL.md
        ├── validation/VALIDATION.md
        └── references/
```

---

## Search wiki (dùng agent tools)

Dùng **Grep** tool thay vì CLI command:
- **AND search**: `grep pattern:"keyword1 keyword2" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/<system>"`
- **Exact phrase**: `grep pattern:"exact phrase" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/<system>"`
- **OR search**: `grep pattern:"keyword1|keyword2" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/<system>"`

Nếu chưa rõ system → gõ `1.-Foundation/` vào Read tool để xem các thư mục con.

---

## Files — Chung (root 1.-Foundation/)

See `references/FILE-STRUCTURE.md`.

---

## Sub-skills

| Sub-skill | Hệ thống | Trigger keywords |
|-----------|----------|------------------|
| `crm` | CRM v1 (crm.mindx.edu.vn) + v2 (crm-v2.mindx.edu.vn) | lead, order, payment, enroll, upsale, downsale, transfer, econtract, KPI, phiếu thu, receipt, hợp đồng, sản phẩm, đầu số gọi điện, renew lead, customer payment request, hide phone, SMS policy, channel group |
| `lms` | LMS (lms.mindx.vn) | class, attendance, điểm danh, khóa học, học viên, student, enrollment sync, teacher, office hours, calling, reports, settings |
| `report` | Report Application (report.mindx.vn) | report, dashboard, Q&A report, CR formula, MKT dashboard, sale performance, call performance, realtime, revenue, student seat, APV, AOV, measures, chỉ số báo cáo, telemarketing, marketing performance |
