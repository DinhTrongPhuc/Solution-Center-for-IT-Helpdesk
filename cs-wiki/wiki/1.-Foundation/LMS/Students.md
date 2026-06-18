# Học sinh (Students)

## Trạng thái học sinh

Theo dõi tại tab Student trong LMS. Click chi tiết HS → trạng thái hiển thị bên cạnh tên.

| Trạng thái | Ý nghĩa |
|------------|---------|
| **Waitlisted (waiting up level)** | (i) Ko trong lớp nào (do withdraw) + còn slot enrollment trống. (ii) Đang ở lớp Pre-open/Pending/Suspended/Abandoned/Finished |
| **Waitlisted (waiting new class)** | (i) Học viên chưa có khóa học trước đây trên hệ thống. (ii) Học viên đã được thêm đơn hàng (add order) từ CRM |
| **Active** | Đang ở lớp Running |
| **Onhold** | Đang bảo lưu hoặc quá hạn bảo lưu |
| **Dropout** | Đã có thông tin nghỉ ngang |
| **Completed** | (i) Đã nhập hết slot enrollment. (ii) Tất cả lớp đều Finished |

> Có thể filter theo từng trạng thái trong danh sách HS.

### Bảng migrate trạng thái

| Trạng thái cũ | Trạng thái mới | Định nghĩa |
|---------------|----------------|------------|
| Active | **Active** | HS đang ở trong lớp Running |
| Inactive | **Waitlisted (waiting up level)** | HS ở lớp Finished/Preparing/Pre-open/Pending/Suspended/Abandoned + còn slot trống; hoặc ko trong lớp nào (do withdraw) + còn slot trống |
| Inactive | **Completed** | Đã nhập hết slot enrollment; tất cả lớp đều Finished |
| On hold | **On hold** | Đang có yêu cầu bảo lưu |
| Onhold expired | **On hold** | Đang có yêu cầu bảo lưu |
| Dropout | **Dropout** | Đã có thông tin nghỉ ngang |
| N/A | **Waitlisted (waiting new class)** | Chưa có khóa học trước đó; đã được add order từ CRM |

## Enrollment

Student → chi tiết → Enrollments
- Từ 12/2024: bắt buộc chọn **Class session**
- **Scope**: Default (buổi đầu) / Specified (chọn session cụ thể)
- Khi duyệt yêu cầu từ CRM: chọn **Learning medium** + Scope + Class session
- **Học phí**: chia đều số slot. Slot 1: enroll dù chưa đóng. Slot 2+: đóng >= TB. Special: ko ràng buộc.
- **Nhiều product có Special**: chia đều các slot trừ slot Special. Enroll 1st slot gói nào → 1st slot gói kia nhảy theo logic.
- **Phân quyền**: View / Enroll / Withdraw

## Withdraw

Student → Enrollments → Withdraw
- Bắt buộc: scope + class session + lý do → Submit
- Yêu cầu sale Withdraw trên CRM → CXO duyệt LMS
- Sau withdraw: CRM trả Not Enrolled; LMS đổi Deactive

## Chuyển lớp

Từ lớp → Student → Transfer
- Auto fill: tên + email HS
- Transfer from: class hiện tại + lý do
- Transfer to: center, package, course line, course, class, learning method
- Ko đổi Course line: hệ thống gợi ý lớp có tiến độ không lệch quá 02 buổi so với lớp hiện tại
- Đổi Course line: hệ thống gợi ý lớp chưa học buổi đầu so với lớp hiện tại
- Transfer reason đồng bộ uncompleted reason

**Xem chuyển lớp:** Students → chi tiết HS → Classes → trạng thái **Transfered**. Click để xem chi tiết thông tin chuyển lớp.

## Onhold Request

Bảo lưu là trạng thái HS tạm thời nghỉ học, sẽ quay lại sau. Thời gian bảo lưu theo quy định OM. (Cập nhật 05/2024)

> CXO tạo yêu cầu khi HS đang **Active** (đang học trong lớp Running). Hệ thống yêu cầu HS phải ở trạng thái **INACTIVE** (ko trong lớp nào) để request được ghi nhận — CXO cần rút HS khỏi lớp trước hoặc trong quá trình tạo.

### Các trạng thái

| Trạng thái | Diễn giải |
|------------|-----------|
| **Pending** | Vừa tạo, chờ duyệt |
| **Approved** | Đã duyệt. Student status = Onhold |
| **Reject** | Bị từ chối duyệt (cần nhập lý do) |
| **Cancelled** | Bị xóa bởi người tạo, trước khi duyệt |
| **Abandon** | Hủy bởi người duyệt, trước ngày bắt đầu |
| **Suspended** | Đã diễn ra và dừng lại trước ngày kết thúc |
| **Returned** | Tự động: hết hạn + HS enrolled lớp Running |
| **Expired** | Quá ngày kết thúc, HS chưa đi học lại |
| **Extra** | Đã được thêm ngày kết thúc (đang chờ duyệt) |

### Giới hạn

- **Standard**: theo chính sách OM từng thời điểm, tính theo **gói khóa học** HS đang theo học
- **Exception**: 1 lần toàn hệ thống, tối đa 365 ngày

### Quy trình

**Flow chính:** Tạo yêu cầu bảo lưu → Sửa yêu cầu bảo lưu → Duyệt yêu cầu bảo lưu

1. **Tạo yêu cầu bảo lưu** (CXO thực hiện): Students → Details → Onhold request → **+**
   - Chọn **Recent product** (gói HS đang dùng) → giới hạn tính theo gói này
   - Nhập số ngày, chọn ngày bắt đầu → End date tự động nhảy
   - Lý do: chọn từ danh sách có sẵn (thêm tại Settings → Reason for absence)
   - Nếu thiếu lý do, CXO liên hệ OM để bổ sung
2. **Sửa yêu cầu bảo lưu** (nếu cần):
   - CXO sửa request do mình tạo
   - CXL/OM sửa tất cả
   - **Huỷ (Cancelled):** chỉ người tạo hoặc OD/OM thao tác được, trước khi duyệt
3. **Duyệt yêu cầu bảo lưu** (OM thực hiện): Students → tab **Onhold request**
   - **Approved** — chấp nhận. Request chuyển Pending → Approved, Student status = Onhold
   - **Rejected** — từ chối. Cần nhập lý do từ chối
   - Filter hỗ trợ xử lý nhanh: Search (tên/SĐT), Onhold request status, Center, Start date, End date
   - Sau duyệt: chỉ **OM** sửa được, có thể thêm ngày nhưng **không sửa được Start date**

### Xóa yêu cầu bảo lưu đã được duyệt (Abandon)

Khi request đã duyệt nhưng chưa tới ngày bảo lưu, HS **ko thể vào lớp nào**. Abandon giúp hủy request này → HS về **Inactive**, có thể đưa vào lớp bình thường.

**VD:** HS A có request duyệt 24/12, bắt đầu 15/1. Từ 24/12→15/1, A ko học được lớp nào. Nếu A ko muốn bảo lưu nữa → dùng Abandon.

**Thao tác:** Danh sách request → mở request → nút **Abandon**

- **Cần quyền** mới thấy nút Abandon
- Nếu đã **qua ngày bắt đầu** → ko Abandon được, hệ thống báo lỗi

### Tạm dừng bảo lưu (Suspend)

HS đang bảo lưu muốn quay lại học sớm hơn → nhấn **Suspend**, request dừng lại ngay lập tức, HS có thể vào lớp bình thường.

**Điều kiện:**
- Request (chính hoặc Extra) **chưa đến ngày kết thúc**
- Người dùng **được cấp quyền**

> Số ngày và lượt bảo lưu đã qua được tính vào tổng thời gian/lượt bảo lưu của HS.

### Bảo lưu bổ sung (Extra)

Dùng khi HS đã hết hạn bảo lưu nhưng muốn gia hạn tiếp, hoặc CS ko liên hệ được để đưa HS đi học lại.

- Giới hạn: **1 lần/package**, tối đa **60 ngày**
- Chỉ dùng khi đã hết số lượt/thời gian bảo lưu theo quy định
- Chọn ngày extra + thêm lý do extra (vào description)
- **Cần duyệt** — tương tự request chính

### Returned

Tự động khi hết hạn + HS enrolled lớp Running.

### Tạo nhiều request

- **Tạo request mới** chỉ được khi request cũ: Cancelled / Rejected / Expired / Suspended
- Có thể tạo **nhiều request liên tiếp** khi request cũ **Expired** (để dùng hết số lượt theo chính sách)

### Lý do bảo lưu

Người dùng có quyền tự thêm/sửa, **ko cần Tech team**.

Settings → **Reason for absence**

**Tạo mới:**
- Click icon **+** (góc trên bên phải) → điền tên → **Save**
- Hệ thống popup "Data saved"
- **Lưu ý:** Active → hiển thị khi tạo request; Inactive → ko hiển thị

**Sửa:**
- Di chuột vào tên lý do → click icon sửa
- Sửa được: **tên** (lưu ý giới hạn ký tự) hoặc **trạng thái** Active/Inactive
- Click **Save** → popup "Data saved"

### Filter

**Bộ lọc:** Search (tên/SĐT), Onhold request status, Center, Start date, End date.

**Due soon** — lọc nhanh HS sắp hết hạn bảo lưu:
1. Vào **Students** → tab **Onhold request**
2. **Onhold request status** → chọn **Approved**
3. Bấm **Due Soon** hoặc chọn khoảng **End date**
4. Kiểm tra cột **End date** trong bảng kết quả

## Dropout Request

**Dropout** = HS rời MindX trước khi hoàn thành chương trình học. Cần tạo request + được phê duyệt để chuyển HS sang trạng thái Dropout. (Cập nhật 04/2024)

> Chỉ tạo được khi HS ở trạng thái **INACTIVE / ONHOLD / ONHOLD EXPIRE / UNKNOWN**. Cần quyền để tạo/sửa/duyệt.

### Các trạng thái

| Trạng thái | Diễn giải |
|------------|-----------|
| **Pending** | Vừa tạo, chờ phê duyệt |
| **Approved** | Đã duyệt. Student status = Dropout |
| **Rejected** | Bị từ chối (cần nhập lý do). HS giữ nguyên trạng thái cũ |
| **Expired** | Quá **60 ngày** kể từ dropout date. Từ đây, muốn nhập học lại cần xét duyệt |
| **Returned** | HS quay lại học sau dropout. Nếu có nhiều request, request gần nhất chuyển sang Returned khi HS enrolled lớp mới |

### Tạo yêu cầu nghỉ ngang

Students → Details → **Dropout information** → điền thông tin → **Save**

**Thông tin cần nhập:**
- **Registered products** / **Last class**: tự động cập nhật
- **Dropout date** (bắt buộc): ngày nhận thông tin hoặc ngày HS thông báo nghỉ ngang
- **Type** (bắt buộc): phân loại lý do
- **Description** (bắt buộc): mô tả chi tiết
- **Proof photo** (bắt buộc): hình ảnh minh chứng

Sau khi Save → trạng thái **Pending**. Hệ thống lưu lịch sử: ngày/giờ thao tác, tài khoản, nội dung chi tiết.

### Phê duyệt yêu cầu nghỉ ngang

Students → tab **Dropout request** → Approve / Reject (cần nhập lý do nếu Reject).

Có phân quyền trên hệ thống cho thao tác phê duyệt.

### HS nghỉ ngang quay lại nhập học

- **Trong 60 ngày** kể từ dropout date → nhập học lại bình thường, ko ràng buộc
- **Từ ngày thứ 61** → cần **phê duyệt** mới được vào lớp

## Student Makeup

**Định nghĩa:** Học bù là buổi dạy lại kiến thức ở buổi học mà HS vắng mặt, trước buổi học chính thức kế tiếp của lớp.

> Cần quyền mới tạo được lịch học bù.

### Tạo lịch học bù

Lớp → Attendance → chọn buổi + HS → icon Make up session

**Thông tin cần điền:**

- **Reason**: Absent (vắng ko phép) / Absent with notice (vắng có phép) / Use makeup time (dùng giờ học bù)
- **Type**:

| Type | Ý nghĩa |
|------|---------|
| **Send attachment** | Gửi video/tài liệu để HS tự học |
| **Make up class** | Ghép vào lớp khác học bù |
| **Office hour** | GV dạy bù (lịch OH) |
| **Student reject makeup** | HS từ chối học bù |

> 1 buổi chỉ tạo **1 lịch học bù / 1 HS**.

### Theo dõi kết quả học bù

Students → Details → **Make up record** — xem lịch sử các buổi học bù của HS, bao gồm thông tin lịch đã tạo và kết quả thực hiện.

## Customer Care

Thực hiện CSKH từ **Students** (chọn HS → Customer care) hoặc **Students in Class**.
- **Bắt buộc**: Channel. Có thể thêm: Class, Session, Call record, Nội dung, Upload file
- Sửa trong **30p** sau lưu (chỉ người tạo). Sau 30p chỉ có thể **xóa**.
- Tính năng **Kết quả cuộc gọi + Kết quả chăm sóc** chỉ áp dụng khi Channel = **Call (Gọi điện)**

**Thông tin đã lưu:** hiển thị số thứ tự (#1, #2...) + ngày giờ. **Gần nhất lên đầu**.

**Customer care dashboard:** Student → Customer care (cần quyền). Thống kê toàn hệ thống.

**Phân quyền:** OPS roles (OM/CXO Leader/CXO/TEGL/TE): Create, View any, Update any, Delete any.

## Student Class Progress

Student → Profile → Class progress
- **General information**: thông tin đồng bộ từ CRM (học viên, phụ huynh, tiến trình học tập)
- **Tổng quan**: Total enrollment slots / classes enrolled / classes running
- **Chi tiết từng lớp**: Tên, trạng thái, chuyên ngành, center, ngày khai giảng, ngày kết khóa, CXO, completed status, retention, ds nghỉ (đỏ 2 buổi liên tiếp)
- **Lớp Running** luôn ở đầu

> Tất cả tài khoản đều xem được Class progress của HS mình quản lý.

## Student Package Progress

Student → Profile → Package progress
- Package trên LMS = Order item trên CRM. Hiển thị từ khi CRM tạo order.

**2 phần chính:**
1. **Package summary** — thông tin tổng quan tất cả gói sản phẩm HS đã mua
2. **One package** — danh sách chi tiết từng gói (click icon mở rộng)

| Trường | Mô tả |
|--------|-------|
| **Name** | Tên gói sản phẩm hiển thị trên CRM |
| **Summary progress** | Tiến độ. Chỉ nhảy số khi lớp về trạng thái **Finished** |
| **Category** | **Single/Flexcombo/Combo** (giới hạn số lượng lớp); **Special** (ko giới hạn số lượng lớp); **Service** (phí chuyển nhượng/các chi phí khác, ko tính học phí) |
| **Package price** | Giá sau discount (Price after discount trên CRM) |
| **Total enrollment slots** | Tổng số lớp HS có thể được đưa vào học |
| **No. of enrolled slots** | Số lớp HS đã được đưa vào học |
| **No. of unenrolled slots** | Số lớp HS chưa được đưa vào học |
| **Finished enrolled slots** | Số lớp HS đã học xong |

- **Service**: ko được tính vào tổng tất cả gói sản phẩm (Package summary)
- **Special**: ko có trạng thái Finished. Ko giới hạn thời gian/số lượng lớp. Chỉ số chung chỉ có **No. of enrolled slots**, các chỉ số khác hiển thị **N/A**

## Share Profile

Chia sẻ học bạ trực tuyến (Compass). **Điều kiện:** No. of enrolled slots > 0.

**Bước 1:** Students → tìm kiếm học viên → nút **Share Profile** → copy link + password.
**Bước 2:** Gửi cho PHHS. Học bạ hiển thị: thông tin cá nhân, lịch học, KQHT từng buổi (nhận xét GV + bài tập).

## Student Cares

Classes → Student cares (cần quyền).

**2 nội dung chính:**

**1. Student status** — tổng hợp số lượng HS CS phụ trách:
- **Student active**: HS đang học lớp Running do CS là operator
- **Student onhold**: HS bảo lưu, lớp gần nhất do CS là operator
- **Status in class**: Uncompleted (đánh dấu ko hoàn thành) / Transfer class (chuyển lớp) / Transfer course line (chuyển khối)

**2. Bảng danh sách HS chi tiết:**
- **Filter**: tên/SĐT, center, student status, courses, status in class, completed status, slots, have slot in (khoảng thời gian lớp có buổi học)
- Click tên HS → **chăm sóc khách hàng ngay lập tức**

## Onhold / Dropout Candidate

Hệ thống hiển thị **cảnh báo** trên dashboard để nhận biết HS có khả năng bảo lưu hoặc nghỉ ngang.

**Nguyên tắc để hiển thị cảnh báo:**

- **Onhold candidate**: HS nghỉ liên tiếp **2 buổi** (ko phân biệt nghỉ có phép hay không phép) trong 1 lớp **Running**. Nếu sau 2 buổi vắng, HS đi học trở lại và **được điểm danh** → cảnh báo **tự tắt**.
- **Dropout candidate**: HS ở trạng thái **Onhold expired** và thời gian quá hạn bảo lưu **> 30 ngày** kể từ ngày hết hạn bảo lưu.

## Quick Filters

| Filter | Mô tả |
|--------|-------|
| Due Soon | Onhold Approved, hết hạn trong 7 ngày (đỏ) |
| New student | Chưa có enrollment, chờ lớp mới |
| Uplevel student | Đã có enrollment, chờ lên lớp |
| Attendance miss | Last month / This month (Class sessions) |
| Comments due | Today / This month (Class sessions) |
| Export | Cần quyền |

## Phân quyền

| Role | Quyền |
|------|-------|
| OM / CXO Leader / CXO / TEGL / TE | View any, export |
