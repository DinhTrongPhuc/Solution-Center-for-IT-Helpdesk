# Lớp học (Classes)

## Kế hoạch mở lớp (Class Opening Plan)

**Classes -> Opening plan.**

**Filter:** Search, Center, Course, Operation method, Class type (New/Uplevel), Approval status (Pending/Approved/Rejected), Start date.

**Tạo:** Centre, Course, Operation method, Class type, Start date, Start time, End time -> **Create**.

**Sửa:**

| Status | Không được sửa | Được sửa |
| ------ | -------------- | -------- |
| Pending / Rejected | Center, Course, Operation method | Class type, Start date/time, End time |
| Approved | Tất cả | — |

## Tạo lớp mới

**Tên:** `CƠ SỞ - MÃ KHÓA - MÔN.TT - MÔ HÌNH` (VD: `NCT - C4K - SB01 ONL`)

**Steps:** Chọn center + course → gen tên → tổng buổi → schedule → thêm GV.

**Mô hình:** ONL / OFF / ... (theo cấu hình khóa học).

**Vai trò GV:**

| Role | Ý nghĩa |
| ---- | ------- |
| LEC | Giảng viên chính |
| MT | Trợ giảng |
| Judge | Giám khảo |

## Class Site

Chia lớp thành nhóm nhỏ (hybrid/đông). Mỗi lớp có 1 nhóm **Default**. GV chỉ thấy/thao tác được class site được gán. Lịch sử điểm danh giữ nguyên khi chuyển site.

**Tạo nhóm:** Tab **Class Sites** → Name, Center, Teachers, Students, Operation executive.

**Thêm GV vào class site:**
- C1: Tab Class sites → chọn GV → Tab Teacher → cài vai trò + lịch dạy.
- C2: Tab Teacher → chọn class site → thêm GV + vai trò + lịch.

1 GV không thể ở nhiều class site cùng lúc.

**Phân quyền class site:**
| Role | Quyền |
|------|-------|
| Teacher 18 | Điểm danh buổi của nhóm mình |
| CXO Leader | Điểm danh tất cả slots/nhóm |
| CXO | Điểm danh nhóm được thêm vào |

## Yêu cầu nhập học/rút (Enrollment Requests)

**Classes -> Enrollment Request.**

| Type | Ý nghĩa | Icon |
| ---- | ------- | ---- |
| Enroll | Đăng ký vào lớp | Mũi tên xanh |
| Withdraw | Rút khỏi lớp | Mũi tên đỏ |

| Status | Ý nghĩa | Icon |
| ------ | ------- | ---- |
| Approved | Đã duyệt | V xanh |
| Rejected | Từ chối | X đỏ |
| Waiting | Chờ xử lý | Đồng hồ cam |

**Filter:** Search, Course, Class, Type, Scope, Status.

**Duyệt Enroll:** Waiting → Approve → Learning medium, Scope (Default/Specified), Session → Submit.

**Duyệt Withdraw:** Approve → Session + lý do → Submit (lập tức rút). Từ 12/2024 bắt buộc chọn session.

**Từ chối:** Reject.

## Xem tài khoản Denise

**Students trong Class** → nút xem. Chỉ học sinh **ACTIVE**.

**Info:** Name, Email, Default password, Link. Copy từng HS hoặc all.

## Điểm danh

| Trạng thái | Ý nghĩa |
| ---------- | ------- |
| Unchecked | Chưa điểm danh |
| Attended | Đi học đúng giờ |
| Late arrived | Đi muộn |
| Absent with notice | Vắng có phép |
| Absent | Vắng không phép |

**Quy tắc:**
- GV điểm danh trong 15p đầu → đúng giờ; sau 15p → đi muộn.
- LEC/MT điểm danh cho nhau được. Role Operator: không giới hạn tgian.
- GV không tự điểm danh cho mình.
- Sau 15p chưa điểm danh → LMS tự động báo động.
- ≤ 17 HS: điểm danh toàn phần. > 17 HS: điểm danh từng phần.

## Completed status

Tích **V** (hoàn thành) / **X** (không hoàn thành) + lý do.

**ĐK:** điểm danh ≥ 1 buổi + lớp đã tới buổi cuối.

**Uncompleted:** Reason + Description.

## Retention confirmation

Ghi nhận ngày HS dự định học tiếp. Nhập tay hoặc chọn lịch.

Lớp **Running** hoặc **Finish** (trong 30 ngày). Admin/OM sửa bất cứ lúc nào.

## Student comment

Nhận xét sau buổi học (Summary + Homework + Details). Thiếu 1/3 → LMS báo quá hạn.

**Upload sản phẩm:**

| Trường | Bắt buộc | Giới hạn |
| ------ | -------- | -------- |
| Tiêu đề | Có | — |
| Link Youtube | Không | ≤ 5 |
| Thumbnail | Có | 16:9 |
| Hình ảnh | Không | ≤ 10 |
| File | Không | ≤ 10 |
| Đường dẫn | Không | ≤ 5 |
| Bình luận GV | Có | — |

Hiển thị trên Compass.

## Student performance

Kết quả học tập. Filter: Type (checkpoint/homework/demo), Session, Class site.

**Danh sách:** Name, Class site, Confirm status, Process, Average score.

BT về nhà: **In progress** / **Submitted** / **Marked** (đồng bộ từ Denise).
- **Confirm status:** trạng thái phê duyệt hiển thị điểm lên Compass
- **Approve:** hiển thị lên Compass. **Reject:** không hiển thị.

## Record checkpoint evaluation

Buổi CP = buổi kiểm tra đánh giá năng lực HS. Tiêu chí khác với buổi học thông thường. Mỗi khóa có 02 buổi CP: CP1 (buổi 4/5), CP2 (buổi 8/9).

**Flow ghi nhận:**
1. Chọn buổi học để nhận xét
2. Điền nhận xét (dạng comment)
3. Điền **điểm thực hành** (dạng thập phân, VD: 0-10)
4. Chấm **điểm trắc nghiệm** (tích các câu trả lời đúng → tự tổng điểm)
5. **Lưu** lại thông tin nhận xét

> GV được nhận xét + chấm điểm cho HS **kể cả khi HS vắng mặt** (ko cần điểm danh).

**Cấu hình tiêu chí CP:** Setting → Student comment areas → Type of Comment = **Checkpoint**:
- Cấu hình **thang điểm thực hành** (VD: 0-10)
- Cấu hình **câu hỏi trắc nghiệm + đáp án đúng + điểm tương ứng**

**Always active:** Buổi CP tự động hiển thị "Always active" — comment luôn hiện kể cả khi HS vắng. Bỏ tick nếu muốn ẩn khi vắng.

## Tạm dừng/Hủy lớp

| Hành động | Mô tả |
| --------- | ----- |
| **Suspend** | CXO tự chuyển. Nếu sau khi dừng 1-2 tuần: xóa buổi ko học trước. Kích hoạt lại: email CXO HO. |
| **Abandon** | CXO thực hiện. Lớp vẫn hiển thị, có thể kích hoạt lại — ko mất thông tin. |
