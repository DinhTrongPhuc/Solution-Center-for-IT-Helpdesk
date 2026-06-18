# Input/Output Protocol — LMS (only)

## System Boundary
**This skill handles ONLY LMS Xschool (lms.mindx.vn).**
- ✅ LMS features: class, attendance, course, student, teacher, office hours, reports, calling, settings
- ❌ CRM features: payment, order, lead management, sale process, econtract, receipt, upsale/downsale

If user asks about CRM → "Vấn đề này thuộc CRM. Dùng skill CRM để tra cứu."

## Inputs
- Question about LMS Xschool
- Error message, screenshots, behavior description

## Output Schema
1. Source file + section
2. Answer content from wiki
3. If missing: "Chưa có trong wiki LMS"

## Intent Classification

| Type | Signal | Handling |
|------|--------|----------|
| How-to | "Cách...", "Làm sao...", "Hướng dẫn..." | Search feature wiki → answer |
| Bug | "Lỗi...", "Bị...", "Không... được" | Search Known Bugs + feature wiki |

## Search Modes
- AND (default): All words required
- Exact (`-e`): Exact phrase match
- OR (`-o`): Any word matches
