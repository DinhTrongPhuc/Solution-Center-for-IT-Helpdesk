# MKT Reports

Báo cáo hiệu quả Marketing. Truy cập: [report.mindx.vn](https://report.mindx.vn) → MKT Dashboard.

## MKT Dashboard

Đánh giá hiệu quả các kênh Marketing, tối ưu chi phí MKT.

### Mục đích
- **Business:** Tối ưu kênh/campaign → tối ưu chi phí MKT; tăng bảo mật qua phân quyền
- **MKT team:** Giảm thời gian làm report, giảm file ngoài, tập trung report MKT

### Các chiều xem
- **Thời gian:** Month (theo tháng) / Day (theo ngày)
- **Lead:** New leads (lead sinh ra trong time filter) / All leads (lead chuyển đổi trong time filter)
- **Business rule:** Nếu lead lên stage cao hơn thì cũng tính cho stage thấp hơn. VD: Lead L5 → L1, L2, L3, L4, L5 đều tính 1

### Filter
- BU, K12/18+ BU, Learning method
- Product Group (trong Order), Interested Product Group
- Bộ UTM: Channel, Source, Campaign, Medium, Content

### Measures
| Measure | Description |
|---------|-------------|
| Revenue | Số tiền thực tế công ty nhận được |
| ME | Chi phí Marketing |
| ANSV | Revenue / Student seat |
| CAC | ME / Paying customer |
| ANSV / CAC | Tỷ lệ doanh thu và chi phí để có 1 KH đăng ký |
| CPL1 | ME / L1 — chi phí có 1 lead mới |
| CPL2 | ME / L2 — chi phí có 1 qualified lead |
| NL1–NL6 | Số lead mới tạo trong time filter chuyển lên các stage |
| L1–L6 | Số lead chuyển stage trong time filter |

### Biểu đồ ME, CPL1, CPL3
- Trục tung 2 chiều để biểu diễn số liệu không bị quá bé (do CPL vs ME chênh lớn)
- Có thanh kéo để so sánh dễ hơn

### Khác biệt so với version cũ
- Công thức mới nhất (VD: L4 tính cả chuyển về L4B → L2F)
- Thêm chỉ số: ME/RE, L4B MKT / InterestPG, so sánh tháng trước & năm trước
- Thời gian load ưu tiên hơn (bộ dữ liệu riêng)
- DIM: BU theo lead thay vì BU theo salesman
- Giao diện: chọn BU kèm BA, hiển thị K12 vs 18+, search + select all/bỏ all

## Phân biệt New Lead vs All Lead

Dựa trên 2 yếu tố:
1. **Created at**: Ngày tạo lead
2. **Conversion day**: Ngày chuyển đổi lead

### New Lead
Số lead có **Created at** và **Conversion day** đều trong khoảng thời gian filter.

### All Lead
Số lead có **Conversion day** trong khoảng thời gian filter (không quan tâm Created at).

> Cả New Lead và All Lead đều tính lũy kế. VD: Nếu lead chuyển thành L2 → được tính 1 L1 trong cùng time filter.

### Câu hỏi thường gặp
- **NL1 và L1 khác nhau không?** Có. Nếu lead được chuyển về L1 do Admin nhưng không tạo trong time filter → tính L1 nhưng không tính NL1.
- **L1A → L1B có tính L1 và NL1 không?** Không. Chuyển đổi status trong cùng stage không tính.

## Marketing Performance Dashboard

Phục vụ tối ưu chi phí Marketing theo BA, BU, Project.

### Chiều xem
- **Thời gian:** Last / This / Next + Day / Week / Month / Year + số nguyên > 0
- **BR, BA, BU:** Theo đơn vị kinh doanh
- **Project:** Art / Robotic / Coding (Marketing project gắn cho mỗi lead)

### Chỉ số
- Tiến độ doanh thu, chi phí marketing
- Tỷ lệ chuyển đổi Lead
- Hiệu quả theo BA, BU, và Project

## DIM Channel (Q&A Report)

Tra cứu chi tiết kênh MKT:
- Campaign, Channel Group Id, Medium, Source, Status
- Is Active, Is Default, Start/End Effective Date
- Tenant

**Tra cứu theo:** Channel name / Channel code

**VD:**
- `Show me list of channel and campaign, medium, source and channel group`
- `Show me count of campaign by channel and source as table`
- `Top 5 list of channel and campaign, medium, source and channel group`

## Liên quan
- [Q&A Report](Q&A-Report)
- [Measures & Definitions](Measures-&-Definitions)
- [CR Formulas](CR-Formulas)
