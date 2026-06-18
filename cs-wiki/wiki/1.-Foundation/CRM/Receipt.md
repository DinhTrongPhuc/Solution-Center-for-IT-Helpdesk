# Receipt

## Phiếu thu **[v2]**

Phiếu thu không còn in và phát tới cơ sở. Admin space/lễ tân dùng CRM-v2 để nhập thông tin và in phiếu thu trực tiếp cho khách hàng.

### Xuất phiếu thu

Đối tượng sử dụng: Admin space, Lễ tân, CSL, Sale.

URL: `https://crm-v2.mindx.edu.vn/receipt/export-receipt` (XSchool) / `https://crm-v2.mindxspace.com` (XSpace)

#### 1. Thông tin chỉ định sale
- Business Unit: lọc sale theo BU
- Center: lọc sale theo cơ sở
- Sale được chỉ định: chọn sale chăm sóc KH

#### 2. Thông tin chung
- Xuất tại (cơ sở)
- Phương thức thanh toán: tiền mặt, quẹt thẻ POS, chuyển khoản
- Loại chi phí:
  - Vận hành cơ sở: phí chuyển phát nhanh
  - Doanh thu: tiền khóa học/dịch vụ

#### 3. Thông tin trên phiếu thu
- Nhập thông tin bắt buộc → lưu nháp (Draft)
- In và xuất phiếu cho KH ký

**Yêu cầu in ấn:**
- In **3 liên**: 1 KH ký nhận, 1 lưu CS, 1 gửi kế toán
- Đóng dấu "Đã thu tiền" + dấu mộc công ty (nếu KH yêu cầu)
- Chấp nhận in đen trắng từ máy in CS
- In trên giấy A4

**Sau khi in:**
- KH ký → chụp/scan phiếu đã ký + hóa đơn/chứng từ
- Tải lên hệ thống → phiếu chuyển "Đã xuất" (Exported)
- Chuyển kế toán duyệt

#### Chỉnh sửa phiếu thu
Phiếu "đã xuất": **chỉ sửa** sale chỉ định và thông tin chung — **không sửa** nội dung phiếu.

#### Phân quyền
Base beta → Role → CRM-v2 → Receipt management:
- **View**: xem danh sách/duyệt phiếu thu
- **Create**: tạo phiếu thu
- **Edit**: chỉnh sửa phiếu thu sau khi xuất

> **Lưu ý**: XSchool vs XSpace là 2 hệ thống riêng. Xác định đúng mảng KH trước khi tạo phiếu.

### Duyệt phiếu thu

Đối tượng: Kế toán.

URL: `https://crm-v2.mindx.edu.vn/receipt/confirm-receipt`

- Hiển thị danh sách phiếu thu đã xuất từ các cơ sở
- Chọn xem chi tiết → đối chiếu sổ quỹ → Duyệt hoặc Từ chối
- Phiếu thu tiền mặt: khi duyệt sẽ tự động confirm payment cho thanh toán của sale
