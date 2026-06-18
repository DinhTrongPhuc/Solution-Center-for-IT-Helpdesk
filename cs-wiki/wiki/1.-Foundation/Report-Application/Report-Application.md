# Report Application

## Tổng quan

Hiện tại hệ thống có nhiều Dashboard riêng lẻ (CRM Report, LMS Report, Q&A Report...), mỗi loại cần truy cập hệ thống khác nhau → mất thời gian, ảnh hưởng hiệu suất.

Report Application gộp tất cả Dashboard vào **1 hệ thống duy nhất** → người dùng chỉ cần truy cập 1 nơi để xem tất cả.

**Truy cập:** [report.mindx.vn](https://report.mindx.vn) → đăng nhập tài khoản hệ thống → chọn Dashboard cần xem

## Phân quyền

### A. Quyền xem Dashboard
- Cấp theo phòng ban (VD: Sale xem Doanh thu, KPI; ko xem Vận hành)
- Ko có quyền → hiện thông báo ko có quyền

### B. Quyền xem dữ liệu
- Chỉ xem được dữ liệu cơ sở mình quản lý/làm việc (BU)

### C. Admin set quyền

**Quyền truy cập:**
1. [base-beta.mindx.edu.vn](https://base-beta.mindx.edu.vn) → **Roles** → Role Detail
2. Chọn **Report** → tích quyền tương ứng

**Quyền xem Dashboard:**
1. Report → **Setting → Dashboard Management**
2. Chọn Role có quyền xem Dashboard tương ứng

## Các Dashboard chính

| Dashboard | Mô tả | Link |
|---|---|---|
| **Q&A Report** | Tra cứu dữ liệu bằng câu lệnh tiếng Anh | [Chi tiết](Q&A-Report) |
| **MKT Dashboard** | Hiệu quả Marketing, CAC, CPL, Channel | [Chi tiết](MKT-Reports) |
| **Marketing Performance Dashboard** | Tối ưu chi phí MKT theo BA, BU, Project | [Chi tiết](MKT-Reports) |
| **Sale Performance — Dashboard** | Doanh thu, CR, Call Performance | [Chi tiết](Sale-Reports) |
| **Realtime Performance** | Dữ liệu real-time (cập nhật 5 phút) | [Chi tiết](Sale-Reports) |
| **Call Performance — Realtime** | Hiệu suất & hiệu quả cuộc gọi realtime | [Chi tiết](Sale-Reports) |
| **Telemarketing Report** | Hiệu suất nhân sự Telemarketing | [Chi tiết](Sale-Reports) |
| **OPS Report** | Chỉ số vận hành | [Chi tiết](Measures-&-Definitions) |

## Tần suất cập nhật dữ liệu

| Report Type | Frequency |
|---|---|---|
| Q&A, MKT, Econtract, Financial, Kế toán | 4-5 giờ/lần |
| Realtime, Sale Performance | < 1 giờ/lần (cập nhật 5 phút) |
| Payment trong Realtime, Telemarketing | 3 phút/lần |
| Add payment → nhảy Report | 5-10 phút |

## Refresh data
Admin: search report → **View lineage** → tìm report → **Refresh**

## Liên quan
- [Q&A Report](Q&A-Report)
- [Measures & Definitions](Measures-&-Definitions)
- [CR Formulas](CR-Formulas)
- [Sale Reports](Sale-Reports)
- [MKT Reports](MKT-Reports)
