# Input/Output Protocol — Report (only)

## System Boundary
**This skill handles ONLY Report Application (report.mindx.vn).**
- Report features: Q&A Report, MKT Dashboard, Sale Performance, Realtime, Call Performance, Telemarketing, OPS measures, S&M measures, CR formulas
- CRM built-in reports (deprecated)
- LMS built-in reports (use LMS skill)

If user asks about CRM/LMS built-in reports -> "Báo cáo CRM/LMS built-in đã ngừng sử dụng. Dùng Report Application tại report.mindx.vn."

## Inputs
- Question about Report Application
- Dashboard name, measure, CR formula, filter question

## Output Schema
1. Source file + section
2. Answer content from wiki
3. If missing: "Chưa có trong wiki Report Application"

## Intent Classification

| Type | Signal | Handling |
|------|--------|----------|
| How-to | "Cách...", "Làm sao...", "Hướng dẫn..." | Search feature wiki -> answer |
| Data inquiry | "Chỉ số...", "Bao nhiêu...", "Xem..." | Guide to Q&A Report or appropriate dashboard |
| Bug | "Lỗi...", "Bị...", "Không... được" | Check known issues -> escalate |

## Search Modes (dùng Grep tool)
- AND: space-separated keywords (all must match same line)
- Exact: quoted phrase `grep pattern:"exact phrase"`
- OR: regex pipe `grep pattern:"word1|word2"`
