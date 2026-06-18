# Order & Payment

## 1. Order Flow **[v1+v2]**

Khi KH chốt mua sản phẩm → tạo Order/Phiếu mua hàng để theo dõi thanh toán và chăm sóc KH.

### Tạo Order

1. Mở lead → tab **Order** → **Tạo Order**
2. Chọn **Candidates** (người sử dụng khóa học)
3. Chọn đúng **sản phẩm**
4. Điền **ngày tạo order**
5. Áp **Direct Discount** (nếu có)
6. **OK** → hệ thống tự gửi SMS thông báo tới KH

> **Lưu ý:** Gia đình có 2 con mua 2 sản phẩm → cần chọn đúng tên **Candidates** theo nhu cầu thực tế.

### Apply Coupon
1. Tạo Order xong → nhấn **Áp mã coupon**
2. Nhập mã → coupon áp dụng trên **Price after discount**
3. Coupon chia đều cho từng order item

> Chỉ thêm được coupon khi Lead ở trạng thái **L5A**.

### Fix Price **[v1]**

**Nguyên nhân cần fix giá:**
- Giá product chưa đúng
- Cách tính coupon của Sale khác hệ thống
- Chuyển đổi khóa học
- Chuyển nhượng
- Đổi từ học online sang offline

**Cách sửa:** Mở Order → icon **bút chì** → edit Price/Discount → Save

**Bo tròn giá:** Admin tạo **coupon Fix giá** khi Tổng sau giảm giá cần trừ số tiền lẻ.
VD: Tổng 9.504.000 → tạo coupon 4.000 → giá mới 9.500.000

> Coupon chỉ thêm được khi Lead ở **L5A**. Coupon chia đều cho từng order item.

### Order Status
- **Pending**: Chờ xử lý
- **Signed/Unsigned**: Trạng thái hợp đồng

## 2. Payment / Thu học phí **[v1]**

### Điều kiện trước
- Phải **upload hợp đồng đã ký** lên Order trước (PDF/JPEG)
- Mở Order → icon **+** trước đơn hàng → upload file

### Tạo Payment
1. Tab Order → nhấn **Add Payment** → chọn phương thức
2. Điền: **Amount** (học phí), **Payday** (ngày đóng), **Note** (thông tin chuyển khoản nếu có)
3. **Save**

### Payment Status
- **Unconfirmed** (đỏ): chưa được Kế toán xác nhận
- **Confirmed** (xanh): Kế toán xác nhận tiền đã về

### Lịch sử
Payment tạo xong lưu ở **Payment History** (phía dưới Order). Kế toán kiểm tra và cập nhật trạng thái.

## 3. Payment Methods **[v1+v2]**

| Method | Auto-reconciliation |
|--------|-------------------|
| Bank transfer | Tự động |
| POS (Quẹt thẻ) | Tự động — Provider BIDV/Payoo |
| Cash (Tiền mặt) | Tự động — Salesman chuyển vào QR cá nhân |
| QR Center | Thủ công |
| QR Order | Bán tự động |
| Payment Gateway | Tự động — Onepay/Payoo |
| Third-party installment | Thủ công |
| Customer debit conversion | Tự động |

### Payment Creation Steps
1. Upload hợp đồng đã ký vào Order
2. Nhấn **Add Payment** → chọn phương thức
3. Nhập **Amount**, **Payday**, **Note**
4. Nhấn **Save**

### Payment Status
- **Confirmed**: Tự động xác nhận khi tiền về
- **Unconfirmed**: Chưa xác nhận — đối soát trong 48h

### Cash Payment
1. Nhận tiền mặt từ KH
2. Salesman chuyển khoản vào **QR code cá nhân**
3. Tạo payment chọn **Tiền mặt** → chọn giao dịch
4. Tự động confirmed

### POS Payment
Add Payment → POS → chọn Provider (BIDV/Payoo) → nhập Reference code → Amount → OK.
Tự động đối soát 48h.

### Payment Gateway
Add Payment → Payment gateway → chọn Provider (Onepay/Payoo) → nhập Reference code → OK.

### QR Code Payments **[v1+v2]**

#### QR tại trung tâm **[v2]**
Roles được tạo: Salesman, ASM, DSL, GM. Mỗi center + ngân hàng = 1 QR duy nhất.

**Tạo thanh toán QR trung tâm** **[v1]**:
Lead → Add Payment → QR center → nhập Center, Beneficiary bank, Account holder, Transfer bank, Transaction ID, Pay day, Note, Attachment. Payment ở trạng thái Unconfirmed.

**Xác nhận thanh toán** **[v2]**:
Transaction list → Center QR payment → chọn payment → Reconcile → Confirm.

#### QR từ đơn hàng **[v1]**
Tích hợp Flex. Tạo order → hệ thống sinh QR → gửi KH → tự động Confirmed khi KH chuyển khoản.
> Khi KH thanh toán 100% → QR bị vô hiệu hóa.

#### QR từ tài khoản saleman **[v2]**
User Profile → Personal QR code. 3 nhà cung cấp: One Pay, Pay Os, Bank (MSB).
2 chế độ: Một lần (nhập số tiền) / Cố định (chọn bank).

**Tạo thanh toán** **[v1]**: Add Payment → Sử dụng đối soát tự động → chọn giao dịch → phân bổ → OK. Tự động Confirmed.

### Backup Bank Management **[v2]**
CRM v2 → **Backup bank management** (Admin). Vietinbank là ngân hàng mặc định chính. (Chi tiết: [Settings](Settings))

## 3. Payment Allocation **[v1+v2]**

Bắt buộc với mọi phương thức thanh toán:
1. Tạo payment → nhập số tiền
2. **Product payment allocation**: Phân bổ cho từng sản phẩm
3. **Unallocated amount** = tiền chưa phân bổ

### Allocation Status
- **Allocated**: User thêm payment → tự động allocated
- **Unallocated**: Payment từ QR Order → chưa phân bổ

### Điều chỉnh phân bổ
Salesman có thể sửa số tiền phân bổ sau khi tạo payment.

## 4. Role Permissions **[v1+v2]**
Các role được phép tạo payment allocation: Salesman, GM, ASM, SMA, SMKT.

## 5. Payment Method Management **[v2]**
CRM v2 → **Payment method management**. Bật/tắt phương thức bằng switch button.

## 6. Customer Payment Request (v2) **[v2]**

### View
CRM → menu Customer Payment Request. Lọc theo tên file, trạng thái.

| Cột | Ý nghĩa |
|-----|---------|
| Status | PREPARING / READY TO SEND / SENDING / SENT |
| Total / Success / Failed | Tổng / thành công / thất bại |

**Chi tiết Payment Request List:**
| Cột | Ý nghĩa |
|-----|---------|
| Status | New / Sending / Sending failed / Sent / Paid / Payment expired |
| Due Date | Thời hạn thanh toán |
| Bank Name / Account | Thông tin ngân hàng |
| Amount | Số tiền |

### Import
1. FAM → Customer Payment Request → "+ Create"
2. Upload file excel (template mẫu)
3. Template lưu ý: SĐT có 0 hoặc 84 đầu; Due date dd/mm/yy; Ghi chú cách nhau bằng `|`

## 7. Promotions / Ưu đãi **[v1]**

Hai loại ưu đãi: **Direct Discount** (giảm trực tiếp khi tạo order) và **Coupon** (giảm sau khi tạo order). Có thể áp dụng đồng thời.

### Các loại ưu đãi

| | Direct Discount | Coupon |
|---|---|---|
| Định nghĩa | Giảm trực tiếp vào giá SP khi tạo order | Giảm sau khi tạo order, áp dụng trên Price after discount |
| Cách dùng | Dùng khi đang tạo order | Áp mã sau khi tạo order xong |

### Dashboard

Bộ lọc: Promotions type, Status, Apply date.

| Cột | Ý nghĩa |
|-----|---------|
| Name | Tên chương trình ưu đãi |
| Code | Mã dùng khi tạo order |
| Type | Loại giảm giá |
| Discount value | Giá trị ưu đãi (VNĐ hoặc %) |
| Applied categories | Phạm vi SP được áp dụng |
| Start date / End date | Ngày hiệu lực (23:59p ngày kết thúc) |
| Status | Active / Deactive / Cancelled / Completed / Paused |

### Tạo mã ưu đãi mới

1. Promotions/Ưu đãi → **+** (góc trên phải)
2. Điền: Name, Discount value (VNĐ hoặc %), Start date, End date, Quantity (số lần sử dụng), Active quantity, Code, Applied categories/products, Status, Approval
3. Nhấn **Save**

> Mã tạo xong có Approval = Pending → cần được Admin/Finance phê duyệt mới dùng được.
> Điều kiện sử dụng: Status = Active **và** Approval = Approved.

### Phê duyệt mã ưu đãi (CRM v2)

Dành cho Admin/Finance.

1. CRM v2 → Promotions → chọn mã → icon Edit
2. Chọn **Approve** (chấp thuận) hoặc **Reject** (từ chối)
3. Reject → nhập lý do → mã không dùng được, chờ người tạo cập nhật gửi lại

## 8. Related
- [Lead Management](Lead-Management)
- [Sale Process](Sale-Process)
- [Receipt](Receipt)
