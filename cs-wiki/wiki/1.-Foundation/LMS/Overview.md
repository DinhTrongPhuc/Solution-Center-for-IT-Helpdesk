# Tổng quan về LMS

> LMS (Learning Management System) — hệ thống quản lý học tập được xây dựng bởi MindX.

## Vai trò trên LMS

| Role | Định nghĩa | Nhìn thấy | Thao tác |
|------|-----------|-----------|----------|
| **CXO HO** | Vận hành - Điều phối khối HO | Tất cả lớp + báo cáo toàn hệ thống | Kích hoạt khóa học/tài khoản; mọi thao tác CXO (trừ tạo lớp mới, xóa buổi đã điểm danh, đổi trạng thái lớp); xuất báo cáo |
| **CXO Leader** | Quản lý nhóm CXO theo khu vực/khối | Tất cả lớp + báo cáo toàn hệ thống | Mọi thao tác như CXO; xem báo cáo toàn hệ thống |
| **CXO** | Quản lý lớp tại 1 cơ sở/khối | Lớp tại cơ sở mình | Mọi quyền chỉnh sửa lớp mình tạo; xuất bảng chấm công cơ sở mình |
| **BTL** | Quản lý Vận hành - Kinh doanh tại cơ sở | Lớp tại cơ sở mình | Chỉ xem lớp; tạo/chỉnh sửa trạng thái Office Hours |
| **Salesman** | Kinh doanh tại cơ sở | Lớp tại cơ sở mình | Chỉ xem lớp; tạo Office Hours |
| **TE** | Điều phối giảng viên tại cơ sở | Lớp tại cơ sở mình | Điểm danh lớp mình phụ trách; điều phối GV/đổi trạng thái OH cơ sở mình |
| **LEC/MT/Judge** | LEC: GV chính. MT: Trợ giảng. Judge: Chấm demo | Lớp tại cơ sở mình | Điểm danh lớp mình phụ trách; cập nhật kết quả OH |

## Dashboard

Dashboard hiển thị:
- Thống kê lớp đang hoạt động theo cơ sở
- Tình trạng điểm danh theo lớp (HV + GV) — hôm qua, tuần hiện tại, tháng
- Đề xuất nhập học từ CRM
- Lịch lớp theo tuần/tháng

### Ý nghĩa màu sắc Attendance

| Màu | Ý nghĩa |
|-----|---------|
| Xanh | Điểm danh/HV tham gia từ khá đầy đủ đến đầy đủ |
| Cam | Cần chú ý |
| Đỏ | Báo động |

## Trạng thái lớp học

| Trạng thái | Diễn giải |
|------------|-----------|
| **New** | Lớp mới tạo, chỉ có tên lớp |
| **Preparing** | Đã có tên lớp, lịch học, giảng viên |
| **Pre-open** | Đã có thêm thông tin học viên |
| **Pending** | Đầy đủ thông tin, gửi yêu cầu để HO mở lớp |
| **Rejected** | HO từ chối mở lớp (không đạt tiêu chí) |
| **Open** | HO đã duyệt, chưa đến ngày khai giảng. Qua 12h đêm cùng ngày → Running |
| **Running** | Đã duyệt, có lịch khai giảng trong ngày |
| **Finished** | Hoàn thành thời gian học (hiển thị sau 24h ngày học cuối) |
| **Suspended** | Đang chạy nhưng tạm dừng. CXO cần xóa các buổi sau để k điểm danh |
| **Abandoned** | Lớp có thông tin bị sai, CXO bỏ hoàn toàn |

## Thanh công cụ

1. Cơ sở (Centres)
2. Khóa học (Course)
3. Học viên (Students)
4. Lớp học (Classes) — Lớp học + Yêu cầu nhập học
5. Office Hours — Trial, Fixed, Event, Makeup
6. Giảng viên (Teachers)
7. Tin nhắn (Messenger) — SMS + Email tự động
8. Báo cáo (Report)
9. Thiết lập (Settings) — Class Roles, Email/SMS Templates, Hour Preset
10. Xác thực (Auth)
