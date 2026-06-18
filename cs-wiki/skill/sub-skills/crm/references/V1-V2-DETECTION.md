# CRM v1 vs v2 — Detection Guide

> **Note:** Wiki đã merge v1+v2 thành 1 file/tính năng (thư mục `CRM/`), phân biệt bằng tag `[v1]` / `[v2]` / `[v1+v2]`. Dùng guide này để detect version trước khi search.

## Dấu hiệu → v1

**Tên / URL:**
- "crm v1", "crm.mindx", "usage-crm-xschool", "crm cũ"

**Lead:**
- L0–L6 (7 levels, 24 statuses)
- upsale / downsale / transfer / change product
- enrollment → LMS (Send Enroll)
- interest product, product group

**Tài chính:**
- add payment, attachment order items
- QR payment (order QR, user/center QR)
- customer debit conversion
- coupon upsale

**Hợp đồng:**
- econtract, phiên ký

**Báo cáo:**
- KPI, Daily Report, CR Report

**Lỗi đặc thù:**
- "upsale xám" → upsale không enabled do chưa enrolled
- "payment unconfirm" → POS chưa đối soát
- "không add được payment" → thiếu attachment
- "SĐT tồn tại" → lead đã có trên hệ thống
- "phiên ký hết hạn"
- "created at > payday" → payment không tính
- "slot đầu không cần đóng tiền" → enrollment

## Dấu hiệu → v2

**Tên / URL:**
- "crm v2", "crm-v2.mindx", "usage-crm-v2-xschool", "crm mới"

**Lead (Admin):**
- lead stage management (tạo stage, kéo thả order)
- lead status (code: L1A = L + stage + ABC)
- allowed actions (gán action cho từng status)
- automate transition (event + condition → target status)
- renewal threshold (days from last call/status/note)
- churn reason

**Payment:**
- customer payment request (import excel template)
- trạng thái: New → Sending → Sent → Paid / Payment expired
- reference code, bank account info

**Phiếu thu:**
- receipt, export receipt (xuất phiếu)
- confirm receipt (duyệt phiếu — kế toán)
- 3 liên: KH, cơ sở, kế toán
- sale chỉ định, phương thức thanh toán
- đối soát tự động với tiền mặt

**Call:**
- call management, đầu số gọi điện
- Branding (hiển thị tên CTY) vs Normal (hiển thị số)
- center, stage, channel group config

**Setting:**
- hide phone number (showable / no showable)
- SMS policy / SMS quota (theo Sales Target Rank)
- channel group setting (nhóm kênh)
- marketing content (Facebook ads, Normal)
- transaction reminder (kế toán config)

**Customer:**
- customer management (customers screen)
- customer upload (tải lên file .xlsx)
- general information, purchased product, transfer request, debits

**Product:**
- product code, product name, price
- product type (FlexCombo → Course Line)
- limit courses, limit duration
- product category (18+, Kids, Teen)
- product line

**Contract:**
- soạn thảo hợp đồng (3 tab: KH, người dùng, sản phẩm)
- tiền kiểm hệ thống (chờ xử lý / đạt / không đạt)
## Dấu hiệu chung (cần hỏi)

Các từ khóa dùng cho cả v1 và v2:
- lead, customer, order, payment, product
- sale, salesman, assign, BU, center
