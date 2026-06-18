# Settings

## Hide phone number setting **[v2]**

Đối tượng: Admin.

**Policy (từ SOD):**
- L1: Ẩn hoàn toàn
- Stage khác: Ẩn nhưng xem được khi ấn vào

### Cài đặt
Chọn stage → 2 loại:
- Showable: ấn xem được số
- No Showable: ấn cũng không xem được

Quyền xem No showable: cấu hình tại CRM v1 cho Admin.

## Cấu hình Chính sách cho Saleman **[v2]**

Thiết lập rules kiểm soát tài nguyên (VD: hạn mức SMS/tháng) theo Sales Target Rank của từng BU.

**Policy:**
- Không tạo/cập nhật chính sách cùng điều kiện lọc
- Chỉ người có quyền mới thao tác

### Danh sách chính sách
- Tên: click để xem/sửa
- Trạng thái: Hoạt động (xanh)
- Điều kiện áp dụng: VD "Cấp bậc: Bằng B"
- Ngưỡng hạn chế: VD "1000 SMS/tháng"

### Tạo mới
1. Cài đặt → Cài đặt về Sales & Marketing → Quy tắc
2. Nhấn "+ Tạo mới"
3. Nhập Tên, Trạng thái, Điều kiện áp dụng, Ngưỡng hạn chế
4. Nhấn Lưu

## Channel Group setting **[v2]**

Đối tượng: Marketing Manager, Sale Manager.

### Tạo Channel Group
1. Ấn "Create"
2. Channel Group Name (required) + Description
3. Ấn Save

### Sửa / Xóa
Sửa tên, mô tả, Active/Inactive → Save. Xóa qua icon sửa → nút Xóa.

## Marketing content **[v2]**

Đối tượng: Marketer.

### Các cột
- Title: tên content
- Type: loại content
- Status: Active/Inactive

### Tạo content mới
1. Ấn "Create"
2. Nhập Title, Category (K12/18), Type (Facebook ads/Normal), Product Group
3. Ấn Save

## Cài đặt nhắc nhở giao dịch **[v2]**

Kế toán cấu hình để các bên (Salesman, BU Leader, BA Leader) nhận thông báo về giao dịch chưa được thêm sau X ngày.

CRM v2 → mục Thanh toán → Cài đặt nhắc nhở transaction.

### Tạo mới
1. Chọn "Tạo mới"
2. Điền: Vai trò, Tên thông báo, Tần suất, Trạng thái, Điều kiện thông báo
3. Nhấn Gửi

## Payment Method Management **[v2]**

CRM v2 → **Payment method management** (sidemenu).

### Danh sách phương thức

| Cột | Ý nghĩa |
|-----|---------|
| Payment method | Phương thức thanh toán |
| Confirm type | Hình thức xác nhận: **Manual** (thủ công) / **Automated** (tự động) |
| Usage status | Trạng thái sử dụng (bật/tắt) |

**Bật/tắt:** Click **switch button** ở cột Usage status. Khi tắt → hệ thống hiện cửa sổ xác nhận (tránh tắt nhầm ảnh hưởng Add payment).

### Phân quyền

Admin → Roles → chọn role → Edit → **Config system** → tích quyền:
- **View payment method usage**: xem danh sách phương thức
- **Edit payment method usage**: chỉnh sửa trạng thái sử dụng

## Backup Bank Management (for QR Salesman) **[v2]**

CRM v2 → **Backup bank management** (sidemenu). Dành cho Admin. Quản lý ngân hàng backup để tạo QR salesman.

### Danh sách

| Cột | Ý nghĩa |
|-----|---------|
| Bank name | Tên ngân hàng |
| Bank account | Tên tài khoản |
| Status | Trạng thái sử dụng |

**Bật/tắt:** Click **switch button** ở cột Status. Sau khi bật → Salesman thấy thêm ngân hàng khi tạo QR cá nhân.

> **Vietinbank** là ngân hàng mặc định chính — không nằm trong danh sách backup này.

### Phân quyền

Admin → Roles → chọn role → Edit → **Bank provider** → tích:
- **View**: xem danh sách ngân hàng backup
- **Edit**: chỉnh sửa trạng thái sử dụng

## Auto Assign từ Digital **[v1]**
Cấu hình landing page + UTM → tự động assign lead về BU. (Chi tiết: [Lead Management > Assign](Lead-Management))

## Account / Tài khoản **[v1]**

Danh sách toàn bộ tài khoản trên CRM + kích hoạt tài khoản.

> Chỉ áp dụng cho tài khoản có quyền **Admin/Manager**. Tài khoản phải đã đăng ký trên base.mindx.edu.vn. Sau khi tạo thành công → CRM hiện hộp thoại **"Update user success"** ở góc dưới bên phải màn hình.

### User Profile / Đổi thông tin cá nhân **[v1]**

Tại User Profile, người dùng có thể **đổi tên** và **đổi mật khẩu** tài khoản.

Nhập thông tin cần thay đổi → **Save** → CRM hiện hộp thoại cập nhật thành công.

## Roles / Vai trò **[v1]**

### Dashboard Roles

| Khái niệm | Định nghĩa |
|-----------|-----------|
| Name | Tên hiển thị của người dùng trên CRM |
| Description | Mô tả vai trò (dành cho ai? quyền hạn gì?) |
| Permissions | Số lượng quyền hạn được cấp cho vai trò đó |
| Status | Trạng thái hoạt động của tài khoản trên CRM |
| Business domain required | Khối kinh doanh nhân sự làm việc |
| Business unit required | Đơn vị kinh doanh nhân sự làm việc |
| Centre required | Địa điểm nhân sự làm việc |
| Created At | Thời gian khởi tạo tài khoản trên CRM |
| Action | Thao tác chỉnh sửa tài khoản trên CRM |

> **Business domain required, Business unit required, Centre required** được bật xanh nghĩa là **BẮT BUỘC** phải điền các thông tin trên khi kích hoạt tài khoản CRM cho nhân sự thuộc roles/vai trò đó.

### Tạo Roles mới

> Chỉ **Admin/Manager**.

**Lưu ý:**
- Kiểm tra mục đích, tránh trùng lặp roles hiện có
- Bật tính năng **BẮT BUỘC** để giới hạn quyền hạn
- Tích xanh vào quyền muốn cấp → tính năng ko được cấp sẽ **ko hiển thị** trên CRM của roles đó

### Ý nghĩa các quyền trên hệ thống

**Thuật ngữ:** unit = đơn vị KD, area = vùng KD, domain = miền KD

**1. Lead view** (quyền xem lead):
- By any within domain/any/asm/unit: xem tất cả lead trong domain/toàn hệ/area/unit
- By any within unit on open lead: xem lead mở trong unit
- By owner within unit: xem lead mình sở hữu trong unit
- By interviewer within domain: xem lead mình interview trong domain

**2. Lead owner** (4 hành động):
- **Override**: chuyển owner từ người khác sang người thứ 3
- **Assign**: chuyển từ no owner sang người khác
- **Give**: đưa owner của mình sang người khác
- **Take**: lấy owner của người khác về mình

Cách đọc: `[Hành động] trong [Địa bàn người chuyển] tới [Vai trò người nhận] trong [Địa bàn người nhận]`

VD: Override within domain to any role to within domain = chuyển owner từ người cùng domain sang bất kỳ vai trò trong domain.

### ASM (Area Sale Manager) **[v1]**

ASM là nhân sự quản lý kinh doanh tại một khu vực địa lý. Một khu vực có thể có nhiều BU.

**Thuật ngữ:**
- **Business Unit (BU)**: đơn vị kinh doanh
- **Child Business Unit**: BU nằm trong khu vực ASM quản lý. 1 Child BU chỉ thuộc 1 BU lớn.

**3 quyền cơ bản của ASM:**

1. **View** — nhìn thấy **tất cả lead** thuộc các BU mình quản lý. Có thể lọc theo BU cụ thể. BU không thuộc khu vực → CRM ko hiển thị.
2. **Edit** — **toàn quyền chỉnh sửa** lead thuộc BU mình quản lý: Note, Customer/Family, Add Payment, Add Order, Enrollment...
3. **Assign** — bàn giao lead cho:
   - ASM và STL trong cùng hệ thống
   - Saleman thuộc BU mình quản lý
   - VD: ASM 1 chỉ bàn giao cho saleman x, y, z của BU mình; ASM 2 chỉ bàn giao cho saleman o, p, t, m của BU mình.

### Phân quyền vai trò trên CRM **[v1]**

| Bộ phận | Vị trí | Vai trò CRM | Quyền View | Quyền Edit |
|---------|--------|-------------|-----------|-----------|
| **Sale** | NV kinh doanh/NV tư vấn | Salesman | Toàn bộ KH họ sở hữu | Nhập thông tin, gọi điện, tạo order |
| | | SaleHO | | |
| | GĐ kinh doanh/TP kinh doanh/TN kinh doanh | GM | | |
| **CXO** | Quản lý vận hành cấp Hội sở | CXO HO | Toàn bộ KH trên hệ thống | - |
| | Trưởng nhóm vận hành | CXO Leader | Toàn bộ KH trên hệ thống | |
| | NV quản lý vận hành cấp cơ sở | CXO | Toàn bộ KH trên hệ thống | |
| **Marketing** | | CMO | | |
| | | Digital mkt leader | | |
| | | Branding manager | | |
| | | Chief Marketing Officer | | |
| **RnD** | | Research and Development member | | |
| **BD** | Quản lý BD | BDM | | |
| | Nhân sự BD | BL | | |
| **Other** | | Administrator | | |
| | Nhà đầu tư MindX | Investor | Toàn bộ KH trên toàn hệ thống | Gọi điện, ghi chú lead |

### Dashboard tài khoản

**Tìm kiếm:** gõ tên / email / SĐT → Enter

**Bộ lọc:**
- **Roles**: lọc theo vai trò (VD: salesman)
- **Status**: Active (hoạt động) / Deactive (ko hoạt động)

**Nội dung chi tiết dashboard:**

| Khái niệm | Định nghĩa |
|-----------|-----------|
| Name | Tên hiển thị trên CRM |
| Email | Email đăng ký CRM |
| Roles | Vai trò trên CRM |
| Status | Active / Deactive |
| Center | Địa điểm làm việc |
| Business unit | Đơn vị kinh doanh |
| Business domain | Khối kinh doanh |
| Created At | Thời gian tạo tài khoản |
| Action | Chỉnh sửa thông tin tài khoản |
