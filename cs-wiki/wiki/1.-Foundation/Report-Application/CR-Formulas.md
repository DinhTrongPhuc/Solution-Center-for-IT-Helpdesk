# CR Formulas (Conversion Rate)

CR (Conversion Rate) = tỷ lệ chuyển đổi trạng thái KH. Đo lường hiệu quả trong hành trình khách hàng.

> Bước chuyển đổi được tính từ trạng thái thấp nhất đến trạng thái cuối cùng trong thời gian filter.

## Các loại CR

| CR | Ý nghĩa |
|----|---------|
| **CR12** | Tỷ lệ chuyển đổi từ **KH mới** → **KH quan tâm sản phẩm** |
| **CR23** | Tỷ lệ chuyển đổi từ **KH quan tâm** → **KH đồng ý trải nghiệm** |
| **CR34** | Tỷ lệ chuyển đổi từ **KH hứa trải nghiệm** → **KH thực sự trải nghiệm** |
| **CR45** | Tỷ lệ chuyển đổi từ **KH hứa trải nghiệm** → **KH đồng ý trả tiền** |
| **CRX5** | Tỷ lệ chuyển đổi từ **KH tương tác** → **KH đồng ý trả tiền** |

## Công thức chi tiết

### CR12 (Quan tâm / Mới)

**CR12 = C12 / C1**

- **C12**: tổng số lead chuyển từ **L1 → L2, L3, L4, L5, L6**
- **C1**: tổng số lead L1 trong thời gian filter (bao gồm L1 renew)

### CR23 (Đồng ý trải nghiệm / Quan tâm)

**CR23 = C23 / C2**

- **C23**: tổng số lead chuyển từ **(L1 → L3,L4,L5,L6) + (L2 → L3,L4,L5,L6)**
- **C2**: tổng số lead chuyển từ **(L1 → L2,L3,L4,L5,L6) + (L2 → L3,L4,L5,L6)**

### CR34 (Thực trải nghiệm / Đồng ý)

**CR34 = C34 / C3**

- **C34**: tổng số lead chuyển từ **(L1 → L4,L5,L6) + (L2 → L4,L5,L6) + (L3 → L4,L5,L6)**
- **C3**: tổng số lead chuyển từ **(L1 → L3,L4,L5,L6) + (L2 → L3,L4,L5,L6) + (L3 → L4,L5,L6)**

### CR45 (Đóng tiền / Thực trải nghiệm)

**CR45 = C5 / C4**

- **C5**: tổng số lead chuyển từ **(L1 → L5,L6) + (L2 → L5,L6) + (L3 → L5,L6) + (L4 → L5,L6)**
- **C4**: tổng số lead chuyển từ **(L1 → L4,L5,L6) + (L2 → L4,L5,L6) + (L3 → L4,L5,L6) + (L4 → L5,L6)**

### CRX5

**CRX5 = C5 / (N1 + C5')**

- **C5**: tổng số lead chuyển từ **(L1 → L5,L6) + (L2 → L5,L6) + (L3 → L5,L6) + (L4 → L5,L6)**
- **N1**: Tổng số lead L1 mới trong thời gian filter (bao gồm L1 renew)
- **C5'**: số lead L1, L2, L3, L4 phát sinh trước thời gian filter nhưng chuyển lên L5, L6 trong thời gian filter

## Tra cứu trên Q&A Report

| Câu lệnh | Kết quả |
|----------|---------|
| `show me cr16 by month` | CR L1→L6 theo tháng |
| `show me cr45` | CR L4→L5 |

> **Lưu ý:** KH tương tác (CRX5) bao gồm KH mới sinh ra trong thời gian filter VÀ KH có chuyển đổi trong thời gian filter.

## Liên quan
- [Q&A Report](Q&A-Report)
- [Measures & Definitions](Measures-&-Definitions)
