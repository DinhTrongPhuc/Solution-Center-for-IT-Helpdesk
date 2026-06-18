# Báo cáo

## Bảng chấm công GV
Class → Attendance → Center + Date → Export (Excel). File gửi email (link 2h).

**Info**: Center shortname, Type (Class/OH), Class name, Teacher name, Teacher email, Username, Role (LEC/MT/Judge), Request by.

## Phê duyệt khiếu nại công
LMS → Attendance request → Class / Office hour.

**Class**: danh sách yêu cầu + thống kê (pending/approved/rejected). Email khi GV gửi.
**OH**: tương tự.

## Report LMS
Mỗi báo cáo gồm 3 phần: **Bộ lọc** (thời gian, center, course) + **Biểu đồ** + **Data chi tiết** (tên lớp, sĩ số, center, trạng thái, link LMS).

### Summary
- **Lọc**: thời gian, center (Ctrl+chọn), course lines (Ctrl+chọn).
- **Active Students**: tổng / theo center / theo course / theo tháng.
- **Số lớp**: tổng / theo center / theo course / theo tháng / theo trạng thái.
- **Yêu cầu nhập/rút cần xử lý**: xem chi tiết ở Enrollments.
- **Top 5 khóa học mở nhiều lớp nhất**.
- **Top 10 CXO mở nhiều lớp nhất**.

### Attendance & Schedule
- **Lọc**: thời gian, center (Ctrl), course lines (Ctrl), **Consecutive days** (nghỉ x buổi liên tiếp).
- **ATTENDANCE CHECKS**: tỷ lệ hoàn thành điểm danh (cần / đã điểm danh / quá hạn).
- **ATTENDANCE CHECKS BY CENTER**: tỷ lệ theo cơ sở (thấp → cao).
- **DS HS nghỉ x buổi**: Center, Class, Course, Start date, Student, No. absent, Absent dates, Link.

### Student detail
Báo cáo tình trạng hết khóa của học viên.

## Cấu hình
- **Learning medium**: Phương thức học chính của HS trong lớp. Setting → Learning medium (Name, Short name, Description, Status).
- **Operation method**: Cách thức vận hành thực tế của lớp. Setting → Operation method (Method name, Method code, Learning medium, Description). Tab History: lịch sử tạo/cập nhật.
- **Cấu hình theo Course lines**: [base.mindx.edu.vn/admin/course-lines](https://base.mindx.edu.vn/admin/course-lines) (chỉ Manager/Admin). Khi cấu hình → tất cả khóa thuộc course line hiển thị method đã chọn. Khi tạo lớp chỉ chọn được method đã cấu hình.
- Có thể thay đổi operation method + learning medium trong quá trình vận hành lớp.

## Thay đổi Enroll/Withdraw
Enrollments → tab **Enrollment operation**.

**Lọc**: Course, Class, Student, Type (Enroll/Withdraw), Scope (All/Default/Specified).

**Chọn HS:**
- Mũi tên **xanh (→)**: Enroll
- Mũi tên **đỏ (←)**: Withdraw
- Nhấn **Edit** để mở cửa sổ chỉnh sửa

**Sửa:**
- **Enroll**: Default (buổi đầu) / Specified session (chọn buổi cụ thể)
- **Withdraw**: Default (buổi cuối) / Specified session (VD buổi 09 → HS học hết buổi 08)
- **Submit** để lưu

> Kiểm tra kỹ trước khi Submit. Thay đổi cập nhật **ngay lập tức**.
