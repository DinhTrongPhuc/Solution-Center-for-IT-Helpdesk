# Lead Management

## Thông tin chung **[v1+v2]**

Lead = Customer = Khách hàng là người mà 1 saleman sẽ chăm sóc và tư vấn. Mỗi lead có **1 chủ sở hữu** và theo dõi qua các Level/Stage.

### Dashboard

- **Tab trạng thái**: lọc nhanh lead theo trạng thái chăm sóc
- **Bộ lọc**: click icon filter để bật/tắt. Có thể thêm/bỏ tiêu chí lọc
- **Search**: tìm theo tên hoặc SĐT (SĐT bỏ số 0, thay 84. VD: 0874896743 → 84874896743)

**Các cột thông tin Dashboard:**

| Cột | Ý nghĩa |
|-----|---------|
| Customer | Tên khách hàng |
| Phone | SĐT gọi |
| Candidate | Tên học viên |
| Status | Cấp độ chăm sóc KH |
| Tuition Progress | Tiến độ thanh toán |
| Channel | Nguồn tìm kiếm KH |
| Owner | Chủ sở hữu (tính KPI) |
| Center | Cơ sở làm việc |
| Created At (CA) | Ngày tạo trên hệ thống |
| Last Update At (LUA) | Ngày cập nhật gần nhất |

Có thể thêm/bỏ cột hiển thị qua icon **+** → chọn trường → Save.

## Lead Stages (Hệ 7 levels) **[v1]**

> **Lưu ý**: Ý nghĩa các stage trong bộ level mới: L2 = Quan tâm, L3 = Đồng ý trải nghiệm, L4 = Thực trải nghiệm, L5 = Order/đặt cọc, L6 = Thanh toán.

| Level  | Status | Mô tả                                 |
| ------ | ------ | ------------------------------------- |
| **L0** | L0A    | Sai số điện thoại                     |
|        | L0B    | Hủy do trùng lead                     |
| **L1** | L1A    | Chưa xử lý                            |
|        | L1B    | Cần xử lý lại                         |
|        | L1C    | Sai đối tượng                         |
| **L2** | L2A    | Quan tâm, ưu tiên chuyển hóa trước    |
|        | L2B    | Quan tâm, chuyển hóa sau              |
|        | L2C    | Không chuyển hóa được                 |
| **L3** | L3A    | Đồng ý trải nghiệm/Test, đặt lịch     |
|        | L3B    | Hủy lịch trải nghiệm                  |
| **L4** | L4A    | Đã trải nghiệm, cần hẹn tư vấn        |
|        | L4B    | Đã tư vấn, ưu tiên chuyển hóa trước   |
|        | L4C    | Đã tư vấn, chuyển hóa sau             |
|        | L4D    | Chưa tư vấn được (không liên hệ được) |
| **L5** | L5A    | Order                                 |
|        | L5B    | Đặt cọc                               |
|        | L5C    | Hủy cọc                               |
| **L6** | L6A    | Đã đóng phí một phần                  |
|        | L6B    | Đã đóng phí đủ                        |
|        | L6C    | Đã hết học phí, chưa release được     |
|        | L6D    | Dropout                               |


Cơ chế: chuyển thủ công stage thấp→cao (không chuyển ngược lại trừ renew).

## Quản lý Lead stage **[v2]**

Đối tượng: Administrator.

### Tạo mới

1. Ấn "Create"
2. Điền: Lead stage (required), Lead status (required) — không hiển thị status đã chọn ở stage khác
3. Ấn Save

### Chỉnh sửa

- Nội dung: icon sửa → sửa tên/status → Save
- Thứ tự: kéo thả cột Order

## Quản lý Lead status **[v2]**

Đối tượng: Administrator.

### Tạo mới

1. Ấn "Create"
2. Điền:
  - Code (required): mã id, quy định `L1A = "L" + số stage + thứ tự ABC`
  - Lead status (required): tên status, không được trùng
  - Allowed action (required): chọn action user được thực hiện ở status này
3. Ấn Save

### Chỉnh sửa

Icon sửa → sửa Code/Status/Allowed action → Save.

## Ý nghĩa các quyền liên quan đến Lead **[v2]**

### Lead

- **View/Edit/Create/Delete**: xem/sửa/tạo/xóa lead
- **View all**: xem toàn bộ lead
- **Assign**: chuyển lead
- **Overwriten status**: đè quyền chuyển status bất kì (Admin)
- **Re-assign by filter**: chuyển lead theo bộ lọc
- **View/Edit/Create/Delete lead**: quyền cơ bản
- **Create not only by phone**: tạo lead không cần SĐT
- **Send email**: gửi email
- **Make call**: gọi điện
- **Edit Product Group**: sửa Interest Product Group
- **View no showable phone**: xem SĐT "no showable"
- **Edit without family relation**: sửa lead không có thông tin gia đình
- **View salesman**: xem thông tin salesman trong lead
- **Update not only by phone**: sửa lead không có SĐT
- **View center**: xem cơ sở của lead

### Lead view (phạm vi)

- **By owner within unit**: xem lead mình là owner trong unit
- **By any within domain**: xem lead bất kì trong domain
- **By any within any**: xem lead bất kì
- **By any within asm**: xem lead bất kì trong vùng ASM
- **By interviewer within domain**: xem lead mình là interviewer trong domain
- **By any within unit on open lead**: xem lead bất kì trong unit mà lead đã mở

### Lead owner

- **Action**: Override (ghi đè), Give (tự đưa), Assign (chuyển), Take (tự lấy)
- Cấu hình theo: within domain / within unit / within asm → to role → to within domain/unit/asm/any

### Lead UTM

- **Lock**: khóa UTM
- **Update utm**: cập nhật utm
- **Set upsale**: chọn utm upsale

## Tạo khách hàng/Lead mới **[v1+v2]**

Áp dụng khi SĐT chưa từng có trên CRM. Lead tạo ở v1 sẽ **tự động chuyển qua v2**.

### Thao tác trên v1

1. Leads → **+ Add Lead** (góc trên phải)
2. Điền: **Full name**, **Phone Number**, **Gender**, **Channel**
3. **Save** → hộp thoại "Create success"

### Thao tác trên v2

1. Leads → **+ Add Lead**
2. Điền các trường chính:
   - **Full name** (bắt buộc)
   - **Phone** (bắt buộc)
   - **Email**
   - **Preferred center**
   - **UTM** (Channel, Source, Campaign, Medium)
   - **Marketing Content**
   - **Interested Product Group**
3. Bổ sung các thông tin thêm bên dưới form
4. **Save** → thông báo tạo lead thành công

### Xử lý SĐT đã tồn tại

Khi nhập SĐT đã có trên hệ thống → CRM báo lead tồn tại. Xử lý theo trạng thái:

| Trạng thái lead cũ | Cách xử lý |
|---|---|
| **L5C** (hủy cọc) | Click **Copy** để cập nhật thông tin lead cũ. **KHÔNG** tạo lead mới. |
| **L4** (đang xử lý) | Giữ nguyên lead cũ |
| **L3 trở xuống** | Liên hệ BU đang giữ lead để xin lead về chăm sóc |

## Import danh sách KH **[v1]**

2 cách:

1. Từ Lead Dashboard: icon Import
2. Từ thanh công cụ: **Import** → **New Import**

Quy trình:

1. Chọn nguồn dữ liệu (bắt buộc)
2. Tải file — template chuẩn, file ≤ 1MB
3. Chọn Partner (không bắt buộc)
4. Kiểm tra kết quả: Importing → Preparing → Done

> Chỉ Manager/Trưởng nhóm mới import được. Chỉ import 1 file/lần.

## Xem số điện thoại khách hàng **[v1+v2]**

Tính năng xem SĐT theo stage và quyền. Đối tượng: user có quyền xem lead. (Chi tiết v2: Settings > Hide phone number setting.)

### Phone Number Visibility **[v1]**

| Stage | Hiển thị | Thao tác |
| ----- | --------- | --------- |
| L1 | Ẩn hoàn toàn, không có icon mắt | Không xem được |
| L2–L4 | Ẩn, hiện icon mắt bên phải SĐT | Nhấn icon mắt → hiện số. Hệ thống lưu lịch sử ai đã xem. |
| L5–L6 | Hiện tự do | Không cần thao tác |

> **Phân quyền**: Mọi role đều tuân theo rule trên. Policy chỉ thay đổi khi có request/confirm từ Manager (OM, MM, SOD).

## Đổi đầu số gọi điện **[v1]**

Cho phép salesman đổi số gọi tới khách hàng.

- **Branding** (đầu số thương hiệu): Lead từ nguồn MKT, hoặc Lead L5/L6
- **Normal** (đầu số thường): Lead ngoài nguồn MKT và ngoài L5/L6

### Omicall **[v1]**

Đầu số gọi mới ngoài Stringee/Bizfly.

1. Tải app Omicall (Android/iOS) → đăng nhập tài khoản (Tech cấp)
   - Android: [Google Play](https://play.google.com/store/apps/details?id=vn.vihat.omicall)
   - iOS: [App Store](https://apps.apple.com/vn/app/omicall-contact-center/id1588489273)
2. Mật khẩu mặc định: `Sale@@1212` (đổi trong app → avatar → Đổi mật khẩu)
3. Trên CRM → chọn Omi để gọi → điện thoại nhận thông báo qua Omicall → trượt/xác nhận để gọi
4. Lịch sử cuộc gọi lưu trên cả CRM và app Omi

> Cuộc gọi 1 chiều từ Omi → KH, KH không gọi lại được. Có thể thoát app sau khi đăng nhập.

## Quản lý đầu số gọi điện **[v2]**

Đối tượng: Admin.

Quy tắc: Một số điện thoại hiển thị khi được cấu hình theo Center, Stage - Channel/Channel Group, Applied context, Status.

### Tạo mới

1. Ấn "Create"
2. Điền: Name, Phone number, Type (Branding/Normal), Center, Applied Context (Lead stage + Channel/Channel group hoặc Customer)
3. Ấn Save

### Sửa

Tất cả trường đều sửa được. Có nút **Copy** để tạo đầu số mới từ đầu số hiện có.

## Assign/Bàn giao lead **[v1+v2]**

Saleman sở hữu lead bằng cách:

- Tự nhập thông tin KH (KH chưa có trên hệ thống)
- Được ASM/STL bàn giao từ kho lead

> Lead quản lý theo BU: STL thấy lead trong BU, saleman thấy lead mình quản lý.
> **Saleman không có quyền assign cho người khác** — chỉ ASM/Admin mới assign được.

### Bàn giao đồng loạt **[v1]**

1. Chọn các lead muốn chuyển (tích checkbox)
2. Nhấn nút **Assign**
3. Chọn **BU** → **Center** → **Salesman** nhận lead
4. **Save**

### Bàn giao đồng loạt **[v2]**

1. Dùng filter lọc lead cần chọn
2. Re-assign Selected / Re-assign by filter
3. Điền thông tin → Send/Assign

### Bàn giao từng lead **[v1+v2]**

1. Mở lead → click icon bút / Assign
2. Chọn người nhận → điền thông tin → gửi

### Auto Assign từ Digital **[v1]**

Điều kiện cần: Center có BU tại Base-beta; BU có Category + Offering Product Group; Content có Category + Product Group.

Cách chia: KH chọn cơ sở → chia đều vào BU; KH điền địa chỉ → chia về cơ sở gần nhất.

Fallback: không có content → BU MKTHO; không tìm được địa chỉ → Telemarketing.

### Nhận lead từ kho lead mở **[v1]**

Filter "Open lead" = True → click "Take lead" → tự động vào detail để xử lý.

> Nếu take lead nhưng không xử lý → lead tiếp tục được đẩy lại kho lead mở.

## Quản lý tự động chuyển đổi trạng thái lead **[v2]**

**Automate Transition**: chuyển đổi tự động lead status khi user tạo hành động.

- Event: sự kiện từ hành động user
- Condition: điều kiện để chuyển đổi

Đối tượng: Administrator.

### Tạo mới

1. Ấn "Create"
2. Điền: Transition name (required), Event (required), Transition: Condition + Target lead status
3. Ấn Save

### Các hành động (Allowed actions)

**Nhóm chung:** Add appointment, UTM update, Disable auto message, Remind, Renew

**Nhóm order:** Create order, Upsale, Update refferral

**Nhóm payment:** Add payment, Remove payment, Update payment status, Update first payment

**Nhóm coupon:** Update order coupon, Remove order coupon

**Nhóm refund:** Add refund, Update refund status

**Nhóm product trong order:** Update price, Add product item, Update order product, Remove order product, Update order product item discount

## Quản lý điều kiện làm mới lead (Renewal) **[v2]**

Renew bao gồm đồng thời: cập nhật utm, chuyển status về L1A, thay đổi created at.

Điều kiện dựa trên 3 yếu tố: không chuyển status, không thêm note, không gọi điện.

Đối tượng: Administrator.

### Tạo mới

1. Ấn "Create"
2. Điền: Lead status, Thresholds (Days from last call / Days from last status change / Days from last note)
3. Ấn Save

### Các điều kiện renew

*(Xem bảng chi tiết tại v2 GitBook — các status như L1A: 2 ngày, L2A/L2B: 45 ngày, L5B/L6A/L6B: không renew)*

## Lead Filters **[v1]**

- **Lead**: Stage, Status, Partner, Learning method, BU, Content, Centre, Preferred Center, Re register at
- **UTM**: Channel, Source, Campaign, Medium
- **Order**: Tuition (%), Owner, Order Product Categories
- **Payment**: Payday With Status, Payment Schedule In/Status, Payment Schedule Valid, Payment status
- **Time**: Created at, Last Update At, Last Updated Status At, Last active at, Reminder, Appointment
- **Product**: Product, Newly Assigned, Interest Product, Call time, Product Group
- **Enrollment**: Enrollment Status, Class, Course

> **Search SĐT**: Bỏ số 0 đầu, thay bằng 84 (VD: 0874896743 → 84874896743)

## Notification & Alarm **[v1]**

### Khái niệm

| Khái niệm | Định nghĩa |
|---|---|
| **Notification** | Thông báo ghi nhận hành động hợp lệ trên hệ thống |
| **Alarm** | Pop-up xuất hiện khi có thông báo |
| **Assigned Lead** | Lead được chuyển từ account này sang account khác |
| **Re-register Lead** | Lead đã tồn tại, đăng ký lại từ Website/Landing page |
| **Owner** | Người nắm giữ lead |

### Hiển thị

- **Notification**: icon chuông (góc trên cùng phải). Click → đổ xuống, tối đa **6 thông báo** gần nhất
- **Alarm**: pop-up góc dưới phải, tồn tại **1 phút**. Tự ẩn khi hết giờ hoặc user xử lý. Ẩn bằng click dấu **X**

> Cần click đúng dấu "X" để ẩn Alarm. Click vào điểm khác không ẩn được.

### Nội dung thông báo

**Assigned Lead:**
- Notification: cho biết số lượng lead nhận đến hoặc chuyển đi
- Alarm: chỉ hiển thị lead **chuyển đến** (không hiện lead chuyển đi)

**Re-register Lead:**
- Mỗi lead = 1 thông báo riêng. VD: 6 lead đăng ký lại → 6 thông báo

> Chỉ **owner** của lead mới nhận thông báo.

### Hướng dẫn sử dụng

**Notification:**
- Click thông báo → xem chi tiết
- Assign Lead → hiện danh sách lead được chuyển đến
- Re-register Lead → mở tab mới, hiện màn hình "Customer" của lead
- Click **View all** → xem toàn bộ thông báo

**Alarm:**
- Click vào Alarm → xem chi tiết. Click xong → Alarm đó không hiện nữa

## UTM Tracking **[v1]**

Tự động bắt thông tin nguồn Lead từ Digital (Landing page, Website):


| UTM CRM  | URL param    |
| -------- | ------------ |
| Channel  | utm_channel  |
| Source   | utm_source   |
| Campaign | utm_campaign |
| Medium   | utm_medium   |


- Bắt đúng: URL có đủ 4 params → gán UTM tương ứng
- Bắt sai: URL thiếu/sai 1 trong 4 params → gán None/None/None/None

### UTM Setting

**UTM (Urchin Tracking Module)** = công cụ tracking nguồn lead để đo hiệu quả. Gồm 4 trường: Channel, Source, Campaign, Medium.

UTM Setting hiển thị trên: Lead, MKT Generation Link, Filter, Import Lead.

**Quyền:** Setting icon → **UTM Setting**. Cần: Create, Edit, View, Remove.

**Màn hình UTM Setting (3 phần):**

| Phần | Nội dung |
|------|----------|
| **Tìm kiếm** | Search (tên Channel), Channel Group (MKT/Sale/B2B/Resale/Referral), Trạng thái (Active/Deactive) |
| **Nút tạo** | Tạo UTM mới |
| **Danh sách** | Channel, Channel Group, Status, Created at, Last updated at |

**Tạo UTM mới:**
1. Ấn **Tạo**
2. Điền: **Channel** (tên duy nhất, không trùng), **Channel Group** (chọn 1 nhóm), **Source/Campaign/Medium** (trống → None)
3. Save

> Source/Campaign/Medium không trùng trong cùng 1 Channel/Source/Campaign. Channel chỉ tồn tại duy nhất.

**Chỉnh sửa/Xóa:** Liên hệ Admin. Nếu xóa/sửa UTM → không tìm được lead cũ qua UTM đó.

**Default UTM:** UTM cho lead từ website/nguồn không set UTM. Chỉ **1 default duy nhất**.
- Xem: đánh dấu **sao** trong danh sách
- Set: tick **Default UTM** ở Medium. Chọn default khác → bỏ tick cũ trước

> **Q&A:** Deactivate/rename/chuyển Channel Group → lead cũ **giữ nguyên Channel cũ**. Báo cáo và bộ lọc Channel Group theo group mới. Việc giữ nguyên đảm bảo dữ liệu cũ không thay đổi.

### Hide Upsale in UTM

Nguồn "Upsale" bị ẩn (blur) với role Salesman — chỉ hiển thị nếu lead sinh ra từ thao tác Upsale.

Cấu hình: Admin → Roles → chọn role → Lead UTM: Lock (chỉ thấy) / Set update (tạo/sửa được).

## Churn Reason Setting **[v1]**

**Churn reason** = lý do từ chối của Lead khi chuyển status lùi (VD: L4A về L2E, L3 về L2D). Giúp tối ưu hóa hành trình KH.

**Quyền:** Setting icon → Churn reason Setting. Cần: Create, Remove, View, Edit, View inactive.

### Màn hình quản lý (4 cột)

| Cột | Ý nghĩa |
|-----|---------|
| Lead status | Trạng thái lead có chứa Churn reason |
| Churn reason | Lý do từ chối trong lead status tương ứng |
| Create at | Ngày tạo |
| Last updated at | Ngày chỉnh sửa cuối |

### Cài đặt Churn reason

1. Click **tạo** → vào màn cài đặt
2. Chọn **Lead status** (status đã cài đặt bị disable/mờ; chưa cài đặt thì chọn được)
3. Chọn **Churn reason** — nếu chưa có → chọn **Other** để thêm mới
4. **Save**

> **Lưu ý:** Cân nhắc kỹ trước khi thêm Churn reason để tránh phân mảnh dữ liệu. Nếu 1 lead status có **≥ 20 churn reason** → nên gộp lại.

### Chỉnh sửa/Xóa
- Chọn icon chỉnh sửa → sửa/xóa theo icon tương ứng

### Hiển thị tại màn Lead
Sau khi cài đặt, Churn reason hiển thị tại:
- Màn hình **Lead** (chi tiết)
- Màn hình **danh sách Lead**
- Tab **Histories** (lưu dữ liệu tương tác KH)

## Partner Management **[v1]**

Quản lý đối tác B2B, B2B2C. Thống kê hiệu quả đối tác qua số liệu đo đạc.

**Quyền:** Setting icon → **Partner Management**. Cần: Create, Remove, View, Edit, View inactive.

**Màn hình (3 phần):**

| Phần | Nội dung |
|------|----------|
| **Tìm kiếm** | Search (tên/địa chỉ), Type (Trường học, Công ty...), Trạng thái (Active/Deactive) |
| **Danh sách** | Partner, Type, Status, Address |
| **Nút tạo** | Tạo Partner mới |

### Tạo Partner mới

| Trường | Mô tả |
|--------|-------|
| **Partner** | Tên duy nhất, đúng chính tả. Nhiều CS: "ĐH Ngoại thương - CS HN" / "ĐH Ngoại thương - CS HCM" |
| **Type** | Trường học, Đại học, Cao học, Công ty, Trung tâm đào tạo, Chính phủ |
| **subType** | Phân loại chi tiết: Song ngữ, Dân lập, Công lập, Quốc tế, Trong nước... |
| **Contact point** | Tên, Position (Hiệu trưởng, Giám đốc), Email (@), Phone (+84). Thêm nhiều bằng nút **+** |
| **Country/City/District/Ward/Address** | Chọn đúng để đo chỉ số khu vực |
| **Description** | Mô tả thêm (không bắt buộc) |
| **Status** | Active (mặc định) / Deactive |

> Partner hiển thị trên màn Lead tại tab **Customer** sau khi tạo.

### Chỉnh sửa/Xóa

- **Deactive**: không hiện trên Lead nhưng vẫn trong Partner Management
- **Sửa tên**: duy nhất, có ý nghĩa, dễ tìm
- **Xóa**: mất hoàn toàn ở cả Lead và Partner Management → cân nhắc kỹ trước khi xóa

## Business Unit Management **[v1]**

**Business Unit** = đơn vị kinh doanh. **Center** = nơi nhân sự ngồi làm việc. Một center có thể có nhiều BU.

Vào: Setting icon → **Business Units**.

### Tạo BU mới

1. Click **+ Create** (góc trên phải)
2. Điền:

| Trường | Mô tả |
|--------|-------|
| Business name | Tên đơn vị KD |
| Business unit children | Chọn BU con thuộc vùng KD (ASM quản lý). BU xám = đã thuộc BU khác, không chọn được |
| Business domain | Miền KD |
| Category | K12 hoặc 18 (bắt buộc) |
| Offering Product Group | Nhóm sản phẩm BU bán |

3. **Save** → hộp thoại tạo thành công

> Có thể thêm/bớt Child BU trong BU lớn bất cứ lúc nào.

### Chỉnh sửa BU

Di chuột dòng BU → icon chỉnh sửa (cuối dòng) → sửa:
- Đổi tên
- Đổi domain
- Thêm/bớt Child BU
- Category
- Offering Product Group

## Chọn sản phẩm cho khách hàng **[v1]**

Áp dụng khi đã điền đầy đủ thông tin Customer.

1. Mở lead → tab **Products**
2. Chọn **loại sản phẩm** (Kids, Teens, 18+,...)
3. Click icon **+** → chọn **Sản phẩm** và **ứng viên**
4. **Lưu thay đổi** → thông báo thành công

## Liên quan

- [Order & Payment](Order-&-Payment)
- [Sale Process](Sale-Process)
- [Econtract](Econtract)
- [Settings](Settings)

