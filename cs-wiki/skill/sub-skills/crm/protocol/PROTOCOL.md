# Input/Output Contract

## Inputs
- **Required:** question about CRM (v1 or v2)
- **Optional:** version hint (URL, feature name, error message)

## Intent Classification
Before processing, classify the user's message:

| Type | Signal | Handling |
|------|--------|----------|
| **How-to** | "Cách...", "Làm sao...", "Hướng dẫn...", "Tạo...", "Sửa..." | Search feature wiki → answer |
| **Bug/Issue** | "Lỗi...", "Bị...", "Không... được", "Báo...", error message cụ thể | See WORKFLOW.md Step 1b — Bug Handling |

## Version Detection

### Signals → v1
- URL: `crm.mindx.edu.vn`, "usage-crm-xschool"
- Lead stages L0–L6 (7 levels), upsale/downsale/transfer, enrollment → LMS
- econtract, phiên ký, KPI/Daily/CR Report, QR payment
- Known errors: "upsale xám" (not enrolled), "payment unconfirm" (48h reconciliation), "SĐT tồn tại", "phiên ký hết hạn"

### Signals → v2
- URL: `crm-v2.mindx.edu.vn`, "usage-crm-v2-xschool"
- Lead stage/status (admin), automate transition, renewal threshold
- Customer payment request (import excel), phiếu thu/receipt (export/approve)
- Call management (đầu số branding/normal), hide phone (showable/no showable)
- SMS policy (by Sales Target Rank), transaction reminder
- Customer upload (.xlsx file), product type FlexCombo

### Ambiguous
- If no clear signal → ask user: "Bạn dùng CRM v1 (crm.mindx.edu.vn) hay v2 (crm-v2.mindx.edu.vn)?"
- If user mentioned both → treat as v1+v2 cross-reference
- If answered previously → reuse same version

## Output Schema
1. Source file + section + version tag
2. Answer content from wiki
3. If missing: "Not yet documented in wiki"

## Search Modes

| Mode | Flag | Behavior |
|------|------|----------|
| AND (default) | (none) | All words required → fallback IDF-weighted OR |
| Exact | `-e` | Exact phrase match, auto-strips version tags |
| OR | `-o` | Any word matches, ranked by match count |
