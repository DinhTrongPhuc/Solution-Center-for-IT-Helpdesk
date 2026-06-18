# Sale Process — Enrollment, Transfer, Upsale, Downsale

## 1. Enrollment **[v1+v2]**

Đưa học viên vào lớp (từ CRM sang LMS):
1. Lead → tab **Enrollments**
2. Chọn **Course/Class** tương ứng
3. Nhấn **Send Enroll** → gửi yêu cầu sang LMS
4. LMS staff xử lý: chấp nhận hoặc từ chối

> Điều kiện: Lớp phải tạo thành công trên LMS; course đã cấu hình mặc định.
> Slot đầu tiên: không cần đóng tiền. Slot thứ 2+: phải đóng đủ học phí.

## 2. Transfer (Chuyển nhượng) **[v1+v2]**

### Điều kiện
Sản phẩm đã phân bổ thanh toán **hoặc** đã học nhưng còn học phí chưa dùng.

### Flow
1. Lead → Order → chọn sản phẩm → **Transfer**
2. Chọn hình thức phí chuyển nhượng (mặc định 10%):
   - **Thanh toán phí CN** (KH chuyển nhượng trả)
   - **Trừ vào học phí chưa dùng**
   - **Không tính phí**
3. Chọn KH thụ hưởng (có sẵn hoặc tạo mới)
4. Hệ thống gửi yêu cầu đến Customer CRM v2 + email Sale

### Thông tin Transfer request
| Trường | Mô tả |
|--------|-------|
| Create date | Ngày tạo yêu cầu |
| Customer | KH chuyển nhượng |
| Salesman | Sale chăm sóc KH chuyển nhượng |
| Debit amount | Số tiền chuyển nhượng |
| Status | Pending / Confirmed / Denied |

### Duyệt Transfer
Customer CRM v2 → **Transfer request** → Accept/Deny.

### Thanh toán phí chuyển nhượng
Lead KH chuyển nhượng → Add Payment → nhập số tiền → phân bổ vào ô **phí chuyển nhượng**.

### Hoàn tác Transfer
Hoàn tác nếu chưa chuyển debit sang thanh toán SP khác. Nếu đã thanh toán phí CN → không hoàn tác.

### Customer Debit
Sau transfer, tiền vào **Debit** của Customer (CRM v2).
Chuyển debit thành thanh toán: Lead → Add Payment → **Customer debit conversion**.

## 3. Upsale **[v1+v2]**

### Điều kiện
Sản phẩm đã **enroll ít nhất 1 slot** trong khóa học.

### Flow
1. Lead → Order → sản phẩm → **Upsale**
2. Chọn sản phẩm mới (cùng product group)
3. Nhập mã coupon (nếu có) — coupon dành riêng cho upsale
4. Hệ thống cập nhật: giá mới, hợp đồng mới (phụ lục), activity log

### Create at khi Upsale
Create at (ngày tạo SP trong order) phải ≤ payday, nếu không payment không được tính.

### Hoàn tác Upsale
Chỉ hoàn tác được **lần upsale gần nhất**. Upsale có **áp dụng mã coupon** → không hoàn tác.

## 4. Downsale **[v1+v2]**

### Điều kiện
Sản phẩm đã **enroll ít nhất 1 slot**.

### Flow
1. Lead → Order → sản phẩm → **Downsale**
2. Chọn sản phẩm mới
3. Hệ thống cập nhật: giá mới, hợp đồng mới, activity log

### Hoàn tác Downsale
Chỉ hoàn tác được **lần downsale gần nhất** (nếu chưa phân bổ thanh toán).

### Customer Debit từ Downsale
Nếu tiền chưa dùng > giá sp downsale → tiền dư vào **Customer debit**.
- Chuyển thành thanh toán: Add Payment → **Customer debit conversion**
- Chuyển thành hoàn tiền: CRM v2 → Customer → Debits → Chuyển đổi thành hoàn tiền

## 5. Filter Sale Process **[v1+v2]**
Tab Sale process filter trên lead dashboard → lọc lead đã upsale/downsale/transfer/change product.

## 6. Related
- [Lead Management](Lead-Management)
- [Order & Payment](Order-&-Payment)
