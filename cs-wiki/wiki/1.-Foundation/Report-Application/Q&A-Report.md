# Q&A Report

Tra cứu dữ liệu nhanh bằng câu lệnh tự nhiên (tiếng Anh). Truy cập: [report.mindx.vn](https://report.mindx.vn) → Q&A Report.

## Mục tiêu
- Bảo mật: chỉ email được cấu hình mới xem được
- Chi tiết hơn: chỉ số chuyên sâu qua kết nối nhiều nguồn dữ liệu
- Chủ động: tự lấy dữ liệu, ko cần chờ đợi

## Giao diện
- **Màu đỏ**: ô gõ câu lệnh tìm kiếm
- **Màu xanh dương**: câu hỏi gợi ý từ team BI (click → trả kết quả)
- **Màu xanh lá**: log out

## Công thức tra cứu

```
[Measure] by [Filter] [Time range] as [Visual Type]
```

- **Measure** = phạm vi dữ liệu muốn tra cứu
- **Filter** = đơn vị (BU, BA, Salesman, Channel...)
- **Time range** = khoảng thời gian
- **Visual Type** = hình ảnh dữ liệu

> **BẮT BUOC dùng tiếng Anh.** Chỉ dùng keywords, không dùng câu hỏi.

### Tra cứu giá trị Measure/Filter
- [Bảng tra cứu Sale & Marketing](https://docs.google.com/spreadsheets/d/1LE8_MnWRL7B0Sda495mY8zFI69Gm-EF2LFdZdbUB1Ng/edit#gid=0)
- [Bảng tra cứu Operations](https://docs.google.com/spreadsheets/d/1LE8_MnWRL7B0Sda495mY8zFI69Gm-EF2LFdZdbUB1Ng/edit#gid=1050562801)

## Kiểu biểu đồ
- **Table**: xem số liệu
- **Pie chart**: xem tỷ lệ %
- **Bar chart**: xem tương quan
- **Scatter chart**: tìm sự khác biệt

## Tips
- Dùng **'and'** để gộp: tối đa 2-3 measure/filter cùng lúc
- Câu lệnh càng dài → càng chậm → có thể lỗi
- Ko dùng câu hỏi, dùng keywords

### Keywords hữu ích

| Loại | Keywords |
|------|----------|
| Aggregates | total, sum, largest, smallest, max, highest... |
| Time | today, last __, this __, N days from now... |
| Range | equal to, >, =, <, between, more than, less than... |
| Order/ranking | top N, bottom N... |
| Name | starting with "...", contain "..." |

- Dùng phím **Space** để loading lại dữ liệu

## Các Dimension tra cứu

### DIM Teacher (Giáo viên)
Tính theo sự hiện diện (đã điểm danh) của GV trong lớp.

**Chỉ số:**
- Completion rate: tỷ lệ HS hoàn thành khóa
- Retention confirmed student: số HS xác nhận quay lại
- Retention rate: tỷ lệ HS xác nhận quay lại
- Attended student: số HS đi học (có điểm danh)

**Tra cứu theo:** Teacher name / Teacher code

> Top N: thêm "top 5/10" trước chỉ số. VD: `attended student with teacher by top 10 teacher code as table`

### DIM Channel (Kênh MKT)
Đánh giá hiệu quả các kênh truyền thông.

**Chỉ số:** Campaign, Channel Group Id, Medium, Source, Status, Is Active, Is Default...

**Tra cứu theo:** Channel name / Channel code

### DIM Product (Sản phẩm)
Thông tin sản phẩm trong hệ thống.

**Chỉ số:** ID, Product Line ID, Product Category ID, Product Topic ID, Name, Is Active, Code, Type, Price, Contract Required, Limited Internship, Combo Max Courses, Flex Combo Max Courses, Special Max Duration, Special Max No Courses Per Year, Is Vip, Planning, Product Group, Unit Quota, Skipped In KPI, Start/End Effective Date

**VD:**
- `Show me list of product and product line, type, price, isActive as table`
- `Show me list of product where isActive is true and contractRequired is true as table`

### Org Dimension (Phân cấp)
**BR** (Vùng) → **BA** (Khu vực) → **BU** (Đơn vị) → **SM** (Salesman)

- BU status: Active / Inactive

**VD:**
- `show me the list of salesman, bu, ba, br and bu status where bu <> BLANK`
- `show me the list of salesman with bu NPS`

### Call (Cuộc gọi)
- Call duration, Pickup call theo BU, BA, Salesman, Channel, Source, Channel Group, Marketing Project
- VD: `call duration by BU name`

### L1 target & L6 target
- Tra cứu theo BU, BA, Marketing Project (Project name)

### Revenue
- Tra cứu theo Channel, Channel Group, Salesman
- VD: `revenue by channel and channel group and salesman in December 2024`

### CR (Conversion Rate)
- CR12, CR16, CR23, CR34, CR45, CR56
- VD: `show me cr16 by month`, `show me cr45`
