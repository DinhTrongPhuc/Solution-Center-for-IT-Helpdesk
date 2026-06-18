# Giáo viên (Teachers)

## Tạo tài khoản GV
LMS → Teachers → Create (Admin/Teaching Admin only)

- **Full name**: nhập → auto username `ten-hodem` (ko dấu). Trùng → hậu tố số 2 chữ số.
- **Personal email**: nhận thông tin tài khoản + work email
- **Password**: auto random (dùng chung LMS + Work email)

**Work email**: https://mail.bizflycloud.vn → đổi pass sau lần đầu.

## Teacher Schedule
### Xem lịch
Gồm: Class (lịch dạy lớp chính), Office hours (dạy ngoài lớp), Available time (lịch nhận lớp). Phân biệt = màu sắc.

- GV: chỉ xem lịch của mình
- Quản lý (leader+): xem lịch GV được quyền quản lý

### Tạo lịch nhận lớp
Profile → Schedule → **Add**: Date, Start time, End time, Repeat, Repeat time → Save.

GV chỉ được xếp vào buổi dạy trùng lịch nhận lớp.

**Sửa**: chuột vào lịch → Edit (This schedule / This and following).
**Xóa**: icon thùng rác (cần quyền). Tùy chọn tương tự.

## Timesheet (Bảng công) **[v1]**

### Đăng nhập & xuất file

1. Đăng nhập [lms.mindx.vn](https://lms.mindx.vn) bằng account đã đăng ký
2. **Class** → **Attendance** → chọn **Center** (cơ sở) + **Date** (thời gian)
3. Click **Export** → popup xác nhận nhận file qua email → **OK**
4. Hệ thống xử lý → gửi link download về **email** (email đăng ký LMS)

> Mỗi link download có thời hạn **2 giờ**. Hết hạn → link báo "đã hết hạn".

### Download file từ email

- Email tiêu đề: **"[MindX] Dữ liệu điểm danh [dd/mm/yyyy]"**
- Nội dung: link tải + thời gian hết hạn
- Định dạng: file Excel

### Các cột trong file bảng công

| Cột | Ý nghĩa |
|-----|---------|
| Center shortname | Tên cơ sở |
| Type | Loại công: **Class** (lớp chính) / **Office Hours** (dạy bù, trải nghiệm, sự kiện) |
| Class name | Tên đầy đủ lớp |
| Teacher name | Tên đầy đủ GV |
| Teacher email | Email cá nhân GV (phân biệt trùng tên) |
| Username | Tên hiển thị trên hệ thống |
| Class role/Office Hours | Vai trò GV trong lớp |
| Request by | Người tạo lịch OH |

### Vai trò GV trong lớp

| Role | Định nghĩa |
|------|-----------|
| **LEC** | Giảng viên chính |
| **MT** | Trợ giảng |
| **Judge** | Giám khảo ngoài (chấm điểm/nhận xét buổi 14, ko giảng dạy) |

> GV có công Office Hours đều mặc định role **LEC**.

## Attendance Request (Khiếu nại công)
Gửi khiếu nại công cho Class và Office hours.
