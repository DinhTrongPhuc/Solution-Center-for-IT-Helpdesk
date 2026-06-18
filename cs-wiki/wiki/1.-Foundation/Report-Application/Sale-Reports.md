# Sale Reports

Báo cáo hiệu suất kinh doanh. Truy cập: [report.mindx.vn](https://report.mindx.vn) → Sale Dashboard.

## Realtime Performance

**Truy cập:** [report.mindx.vn/real-time/call-metrics](https://report.mindx.vn/real-time/call-metrics)

> Dữ liệu cập nhật **mỗi 5 phút**.

### Chuyển đổi thời gian
Xem theo: **Hôm nay** / **Tuần này** / **Tháng này**

### Chỉ số cuộc gọi

| Chỉ số | Mô tả |
|--------|-------|
| Tổng cuộc gọi | Tổng số cuộc gọi trên toàn hệ thống |
| Tổng cuộc gọi nhấc máy | Tổng cuộc gọi salesman nhấc máy |
| Tổng thời gian gọi | Tổng thời gian gọi |
| Số cuộc gọi / salesman | Tổng cuộc gọi / Tổng salesman active |
| Số cuộc gọi nhấc máy / salesman | Tương tự, chỉ tính nhấc máy |
| Thời lượng gọi / salesman | Thời gian gọi TB mỗi salesman |

### Chỉ số doanh thu

| Chỉ số | Mô tả |
|--------|-------|
| Doanh thu tổng | Payment + Refund |
| Doanh thu KPI | (Payment + Refund) / Tổng KPI |
| CR45 | Tổng lead L5 / Tổng lead L4 |
| Doanh thu / Salesman | Tổng doanh thu / Tổng salesman active |

> **Payment** tính theo pay date salesman nhập. **Refund** tính theo refund date.

### Biểu đồ

**Cuộc gọi nhấc máy:**
- Top 5 đầu (đỏ) / Top 5 cuối (đen) **BA** theo số cuộc gọi nhấc máy
- Top 5 đầu (đỏ) / Top 5 cuối (đen) **BU** theo số cuộc gọi nhấc máy
- Top 10 **Salesman** theo số cuộc gọi nhấc máy

**Doanh thu:**
- Top 3 **BA** theo Doanh thu / KPI Doanh thu / CR45
- Top 5 **BU** theo Doanh thu / KPI Doanh thu / CR45
- Top 10 **Salesman** theo Doanh thu / KPI Doanh thu

## Sale Performance — Dashboard

Cung cấp chỉ số Doanh thu, CR, Call Performance theo khoảng thời gian.

### Doanh thu
- **Tổng doanh thu** = Tổng (payment + refund) trong thời gian chọn
- Doanh thu theo BR / BA / BU / Salesman: Tổng (payment + refund) filter theo đơn vị

### Tỉ lệ chuyển đổi
- **CR16:** CR L1→L6 của tổ chức
- **CR funnel:** Đếm lead chuyển đến mỗi stage trong thời gian chọn:
  - L1: lead có phát sinh chuyển đổi trạng thái
  - L2: lead ≥ L2
  - L3: lead ≥ L3
  - L4: lead ≥ L4
  - L5: lead ≥ L5
  - L6: lead = L6
- **CR theo BA / BU / Salesman:** CR12, CR23, CR34, CR45

### Call Performance
| Chỉ số | Mô tả |
|--------|-------|
| Total | Tổng cuộc gọi |
| Pickup | Tổng cuộc gọi nhấc máy |
| Avg Duration | Thời lượng gọi TB |

- Call performance theo BA / BU / Salesman

### Filter
- Thời gian: Năm + Tháng
- BA: BR → BA → BU → Salesman
- Product: Product Group → Product
- Channel Group: Channel Group → Channel → Source

### Biểu đồ
- **Revenue:** Total + By BR, xếp hạng top 5 BA / top 8 BU / top 14 Salesman có doanh thu thấp nhất (kèm Revenue Target, %KPI)
- **CR:** CR16 + CR funnel; CR by BA/BU/Salesman (xếp hạng top 6 BA / top 10 BU / top 10 salesman thấp nhất)
- **Call Performance:** Total, Pickup, Total Duration, Avg Duration; Call by BA/BU/Salesman (top 5 BA / top 10 BU / top 10 salesman thấp nhất)
- **Thao tác chart:** Copy ảnh, filter, focus, zoom, xem thêm tùy chọn

## Call Performance — Realtime

Phân tích hiệu suất và hiệu quả cuộc gọi realtime.

> **Hiệu suất:** số lượng công việc (cuộc gọi, thời gian). **Hiệu quả:** kết quả (lead chuyển đổi, CR).

### Filter
- Thời gian: Start date → End date
- BA: BA → BU → Salesman
- Channel Group: Channel Group → Channel → Source

> Channel directsales, Direct Sale, Direct Sales, direct → gộp thành Channel directsales.

### Tính chất dữ liệu (IMPORTANT)
- **Chỉ số hiệu suất:** Dữ liệu realtime (lịch sử gọi điện)
- **Chỉ số hiệu quả:** Dữ liệu delay 4-6 tiếng (lead convert), với điều kiện:
  - Ghi nhận tất cả cuộc gọi trong **15 ngày trước** thời điểm chuyển trạng thái lead
  - Nếu lead chuyển trạng thái nhưng không có cuộc gọi nào → không tính (chỉ cần có lịch sử call, bắt máy hay không vẫn tính)
  - Call và Lead Convert phải cùng User, trên cùng Lead

### Measures

**Hiệu suất:**
| Chỉ số | Mô tả |
|--------|-------|
| Total call | Tổng cuộc gọi (bất kể trạng thái) |
| Pick-up call | Tổng cuộc gọi bắt máy |
| Pick-up Percentage | Pick-up / Total call |
| Total Call Time | Tổng thời gian gọi |
| AVG Call Time | Thời gian gọi TB |

**Hiệu quả:**
| Chỉ số | Mô tả |
|--------|-------|
| Lead Stage Count | Đếm lead User chuyển đến mỗi Stage (L1, L2, L3, L3_C, L4, L4_C, L5, L6) |
| Conversion Rate (CR) | CR12, CR23, CR34, CR45, CRX5 |
| Churn Reason | L1, L2 Churn by Churn reason |

### Biểu đồ
- **Overview:** Pick-up Call vs Call Amount, Total Call Duration / AVG Pick-up Duration, Lead stage (L3, L3_C, L4, L4_C), Call Amount by Status & Time, No. Lead by Stage + Call Perform + AVG Call Time
- **Hiệu suất:** Pick-up Call by Channel Group/Channel, Pick-up Call by BA/BU/Salesman (switch: Total/Pickup%/Total time/AVG time)
- **Hiệu quả:** No. Lead by Stage + BA or Channel (switch Channel Group/BA), CR by Channel Group/Channel/Source, CR by BA/BU/Salesman (switch CR nhóm: Channel Quality - CR12, Telesales Quality - CR23/CR34, Seal The Deal - CR45/CRX5)
- **Churn Reason:** L1, L2 Churn by Churn reason (switch L1/L2)

### Khác biệt so với version cũ
- Bổ sung DIM Channel
- Thêm chỉ số đo hiệu quả (L3, L4)
- Thêm Churn Reason
- Visual: Table → Chart
- Bổ sung Channel Group config

## Telemarketing Report

Hiệu suất nhân sự Telemarketing.

### Flow làm việc
1. TMK gọi → lead lên **L3A**
2. Chuyển lead qua các BU → salesman BU tiếp tục chuyển hóa

### Cách tính
| Stage | Điều kiện |
|-------|-----------|
| **L3A** | TMKer đưa lead từ L1, L2 lên L3A |
| **L4A** | Lead TMKer chuyển lên L3A → salesman BU tiếp tục chuyển đổi. Ghi nhận L4A sau **30 ngày** kể từ ngày salesman chuyển lead lên L3A |
| **L6A / L6B** | Ghi nhận theo ngày first payment kể từ ngày chuyển lên L3A. Nguồn MKT: sau **90 ngày (3T)**. Nguồn khác: sau **180 ngày (6T)** |

### Filter
- Thời gian, Status (L3A, L4A, L6A, L6B), BU, Salesman (TMKer)

### Bảng hiển thị
- **Call by Salesman:** Số lead tính cho TMKer
- **Call by Business unit:** Số lead TMKer chuyển hóa chuyển về các BU

## L1 Target & L6 Target
Tra cứu mục tiêu theo BU, BA, Marketing Project:

- `total l1 target by BU name`
- `l1 target and l6 target by bu ba and project name as table`

## Revenue
Tra cứu theo Channel, Channel Group, Salesman:

- `revenue by channel and channel group and salesman in December 2024`
- `revenue by channel and channel group and salesman admin`

## Liên quan
- [Q&A Report](Q&A-Report)
- [Measures & Definitions](Measures-&-Definitions)
- [CR Formulas](CR-Formulas)
