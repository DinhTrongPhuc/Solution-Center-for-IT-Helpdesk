# Workflow — Report (only)

## 0. Classify Intent
Determine how-to vs data inquiry vs bug:

| Type | Signal | Route |
|------|--------|-------|
| How-to | "Cách...", "Làm sao...", "Hướng dẫn..." | -> Step 1a |
| Data inquiry | "Chỉ số...", "Bao nhiêu...", "Xem...", "CR..." | -> Step 1a (guide to dashboard/Q&A) |
| Bug/Issue | "Lỗi...", "Bị...", "Không... được" | -> Step 1b |

## 1a. How-to / Data Inquiry — Parse Feature (Report only)

**Report features** (wiki: `1.-Foundation/Report-Application/`):
| Câu hỏi | File | Ghi chú |
|---------|------|---------|
| Tổng quan, truy cập, phân quyền | `Report-Application` | |
| Q&A Report (tra cứu câu lệnh) | `Q&A-Report` | Nhắc user dùng tiếng Anh |
| CR Formula (CR12/23/34/45/CRX5) | `CR-Formulas` | |
| Measures S&M / OPS | `Measures-&-Definitions` | |
| MKT Dashboard / Marketing Performance | `MKT-Reports` | |
| Sale Performance / Realtime / Call / Telemarketing | `Sale-Reports` | |

## 1b. Bug/Issue — Parse Error (Report only)
1. Identify affected dashboard
2. Search wiki for known issues
3. If not found -> escalate: "Bug chưa được ghi nhận trong wiki Report Application. Hãy báo BI team với screenshot + timestamp."

## 2. Search (Report wiki)
Dùng **Grep** tool để search:
```bash
grep pattern:"<query>" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/Report-Application"
```

## 3. Not Found -> Check GitBook
Use MCP tools to check `xschool-ad-hoc-report`. Update wiki -> answer.

## 4. Answer
- Cite file + section
- If data inquiry: guide user to use Q&A Report or appropriate dashboard
- If not found: "Chưa có trong wiki Report Application"
- If question is about CRM/LMS built-in reports -> redirect: "Đã chuyển sang Report Application. Dùng skill Report để tra cứu."
