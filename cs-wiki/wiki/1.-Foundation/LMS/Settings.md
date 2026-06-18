# Thiết lập (Settings)

## Đổi mật khẩu
Profile → Change password → mật khẩu mới + xác nhận → Save.

## Các thiết lập khác
- **Class Roles** — vai trò trong lớp
- **Email Templates** — mẫu email
- **SMS Templates** — mẫu SMS
- **Hour Preset** — cài đặt giờ mặc định

## Student comment areas (Tiêu chí nhận xét HS)
Setting → Student comment areas. Các trường:
- **Name** — tên tiêu chí
- **Sort order** — thứ tự hiển thị
- **Is active** — trạng thái
- **Type of comment**: Rating (thang điểm), Content (văn bản tự do), Checkpoint (Practice point + Multiple choice), Demo (Title + Max grade)
- **Slot** — buổi học áp dụng (ko bắt buộc)
- **Public** — chia sẻ cho tất cả HS (ko bắt buộc)

## Course process (Bộ tiêu chí nhận xét)
Setting → Course process. Xem [Courses.md](./Courses.md).

## Learning medium (Phương thức học tập)
Phương thức học chính của HS trong 1 lớp. Setting → Learning medium.

| Trường | Mô tả |
|---|---|
| Name | Tên đầy đủ |
| Short name | Tên viết tắt |
| Description | Định nghĩa cụ thể |
| Status | Active/Inactive. Chỉ chọn được Active |

> Có thể thay đổi phương thức học của HS trong quá trình vận hành lớp.

## Operation method (Mô hình vận hành)
Cách thức vận hành thực tế của lớp. Setting → Operation method.

| Trường | Mô tả |
|---|---|
| Method name | Tên đầy đủ |
| Method code | Mã (hiển thị trong tên lớp, VD: ONL, OFF) |
| Learning medium | Phương thức học liên kết |
| Description | Định nghĩa chi tiết |

Tab **History**: xem lịch sử tạo/cập nhật.

> Có thể thay đổi mô hình vận hành trong quá trình vận hành lớp.

### Cấu hình theo Course lines

**Mối quan hệ cấu hình:**

```
Learning medium → Operation methods → Course line
```

- **Learning medium** → người dùng chỉ chọn được phương thức học đã cấu hình theo **Operation methods**
- **Operation methods** → người dùng chỉ chọn được mô hình đã cấu hình theo **Course line**

**Truy cập:** [base.mindx.edu.vn/admin/course-lines](https://base.mindx.edu.vn/admin/course-lines) (chỉ Manager/Admin)

- Chọn operation method cho từng course line
- Khi tạo lớp thuộc course line → chỉ chọn được method đã cấu hình
- Khi cấu hình cho course line → **tất cả khóa học** thuộc course line đều hiển thị method đã chọn

## Reason for absence (Lý do bảo lưu)
Setting → Reason for absence. Quản lý lý do bảo lưu (Active/Inactive). Active → hiển thị khi tạo Onhold request.

## Tài khoản & phân quyền
Quản lý người dùng và vai trò trên LMS.
