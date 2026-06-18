# Quick Answers

## Sale Process [v1+v2]

### Enrollment
Lead → tab Enrollments → chọn Course/Class → Send Enroll.
Điều kiện: lớp phải có trên LMS. Slot 1: không cần đóng tiền. Slot 2+: đóng đủ học phí.

### Upsale
Lead → Order → sản phẩm → Upsale → chọn sp mới (cùng product group).
Điều kiện: đã enroll ≥1 slot. Hoàn tác: chỉ lần gần nhất. Coupon upsale → không hoàn tác.

### Downsale
Lead → Order → sản phẩm → Downsale → chọn sp mới.
Hoàn tác: chỉ lần gần nhất (nếu chưa phân bổ). Tiền dư → Customer debit.

### Transfer
Lead → Order → chọn sp → Transfer → chọn phí CN (10%) → chọn KH thụ hưởng.
Hoàn tác: nếu chưa chuyển debit.

## Payment [v1+v2]

### Add Payment
Order → Add Payment → nhập Amount, method, date → upload attachment → Save.

### Payment Methods
Bank transfer (tự động), POS/BIDV-Payoo (48h), Cash (QR cá nhân), QR Center (thủ công), QR Order (bán tự động), Payment Gateway (Onepay/Payoo), Third-party installment (thủ công).

## Lead [v2]

### Stage
Setting → Lead stage → Create → name + select statuses.

### Automate Transition
Event + Condition → Target lead status.
Actions: Add appointment, UTM update, Create order, Add payment, Add refund, v.v.

### Renewal
Threshold = days from last call/status/note.
Renew = update utm + change to L1A + update created at.
L1A: auto renew sau 2 ngày không thay đổi. L5B, L6A, L6B: không renew.

## Receipt / Phiếu thu [v2]

### Export
`crm-v2.mindx.edu.vn/receipt/export-receipt` → select sale, method, cost type → enter info → save draft → print → sign → upload → set "Đã xuất".

### Approve
`crm-v2.mindx.edu.vn/receipt/confirm-receipt` → accounting → Approve/Reject.

## Settings [v2]

### Hide phone
Stage L1: ẩn hoàn toàn. Stage khác: ẩn nhưng xem được khi click.
Setting → chọn stage → Showable / No Showable.

### SMS policy
Settings → Sales & Marketing → Rules → tạo policy theo Sales Target Rank.

### Channel Group
Tạo channel groups (MKT/Sale/B2B...).
