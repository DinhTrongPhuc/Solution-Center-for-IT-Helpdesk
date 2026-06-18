# Office Hours (OH)

Các sự kiện có chấm công GV nhưng **không** thuộc lớp học.

| Type | Mô tả |
|------|-------|
| Trial | Trải nghiệm (offline/online/tại nhà) |
| Fixed | Trực trải nghiệm offline cố định (~3h/ca) |
| Event | Sự kiện khai trương, liên kết |
| Makeup | Dạy bù cho HS nghỉ/không theo kịp |

## Roles
- **Salesman**: tạo/sửa Fixed, Trial, Event
- **BTL**: xác nhận công Fixed, Trial, Event thực tế
- **CXO**: tạo/sửa/xác nhận Makeup
- **TE**: nhận lịch, phân công GV
- **GV**: điền kết quả OH sau buổi dạy

## Trạng thái lịch OH

| Trạng thái | Diễn giải |
|------------|-----------|
| **Pending** | Yêu cầu đã được tạo thành công |
| **Abandoned** | Yêu cầu đã được xóa, không được ghi nhận trên hệ thống |
| **Approved** | TE đã thêm giảng viên. Yêu cầu đã được xử lý |
| **Confirmed** | Lịch OH đã diễn ra. GV đã được ghi nhận công |
| **Denied** | Lịch OH đã bị hủy |
| **Rejected** | Lịch OH bị TE từ chối xử lý |

## Quy trình xử lý OH

1. **Bước 1:** BTL/Sale/CXO tạo yêu cầu trên OH → LMS gửi email thông báo cho TE
2. **Bước 2 (TE xác nhận & bố trí GV):**
   - TE nhận thông tin → điều phối GV (nếu chi nhánh chưa đăng ký hoặc đăng ký chưa phù hợp)
   - Điền thông tin GV vào mục **Teacher** → Ấn **Approve**
   - GV có account được set-up cho lớp này sẽ nhận **email + SMS** báo lịch dạy OH
3. **Bước 3:** GV tham gia giảng dạy theo thông tin trên OH
4. **Bước 4 (Ghi nhận công GV — BTL/ASM/STL):**
   - Chọn **Confirm** với ca đã diễn ra thực tế
   - Chọn **Deny** với ca bị hủy
   - ASM/STL kiểm tra lại hàng loạt công OH cần xác nhận:
     - Thời gian thực tế khác → thay đổi thông tin
     - Format Note GV chưa chuẩn → fix lại
     - Trial/Makeup: lượng HV thực tế khác → thêm/bớt

> OH sửa được trước **Confirm/Deny**. Có thể thêm HS vào lịch đã tạo để tối ưu chi phí.

**Lưu ý:**
- Đăng ký muộn được nhưng khuyến khích **trong ngày**, ko đăng ký công tháng trước
- Chú ý ngày cuối tháng, qua tháng ko back về chỉnh nữa
- Tạo sai → chọn **Abandon** để hủy

## Quỹ giờ (Budget)
Office hours → Budget. Quản lý quỹ giờ học bù hàng tháng. Chỉ OM/OD tạo/cập nhật.

**Tạo**: Center, Applied month, Type=Make up, Budget (hours). 1 center/tháng. Ko giảm dưới mức đã dùng.

## Appointment
Kết hợp CRM + LMS theo dõi hành trình sau trải nghiệm.

1. **Salesman tạo OH** trên LMS (loại "Trực trải nghiệm") → TE xếp GV + Approve
2. **Tạo Appointment trên CRM**: lead CRM → tab Appointment → Thêm. Tên, HS, Cơ sở, Khóa học, OH, Due at (auto), Người phỏng vấn (auto), Status=Waiting
3. **Cập nhật**: CRM → Canceled. LMS (GV) → Fail/Passed + Note. Passed → Trailed → Has order → Has payment.

## Tạo giờ học bù
OH type **Makeup**:
1. Office hours → Tạo mới → Type=Makeup
2. **Class** (Running), **Session** (buổi cần bù), **Students** (chọn từ lớp), Hour, Date, Note
3. TE xác nhận + Approve → GV nhận thông báo
4. Nếu quỹ giờ hết 100% → hệ thống cảnh báo nhưng vẫn cho tạo
