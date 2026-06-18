# Product

## Dashboard sản phẩm **[v1]**

Chỉ Admin/Sale Manager mới có quyền quản lý sản phẩm.

| Cột | Ý nghĩa |
|-----|---------|
| Product Code | Mã SP, tìm kiếm nhanh |
| Product Name | Tên đầy đủ |
| Price | Giá niêm yết |
| Product Type | Loại SP (cấu hình khóa học khác nhau) |
| Limit Courses | Số khóa học giới hạn |
| Limit Duration | Thời gian hoạt động |
| Product Category | Độ tuổi (18+, Kids, Teen) hoặc chuyên ngành |
| Product Line | Nhánh nhỏ hơn |
| Status | Active / Deactive |
| Created At | Thời điểm tạo |

### Tạo sản phẩm mới **[v1]**

1. Menu **Sản phẩm** → **+ Add Product**
2. Điền: Product Code, Product Name, Price (≥ 1.000 VND), Product Type, Limit Courses, Limit Duration, Product Category, Product Line, Status
3. > Nếu Product Type = FlexCombo: cần chọn thêm Course Line (Criteria).
4. Nhấn **Create**

> Trường đỏ = bắt buộc. Lỗi → hệ thống báo trường cần sửa.

### Chỉnh sửa sản phẩm **[v1]**

1. Tìm SP → icon bút xanh (Actions)
2. Sửa thông tin (các trường tương tự tạo mới)
3. Nhấn **Save**

> Chỉ người có quyền mới sửa được.

## Tạo mới sản phẩm **[v2]**

Tạo SP trên v2 → tự động đồng bộ về v1.

### Bước 1: Truy cập Products
CRM v2 → màn hình Product

### Bước 2: Create
Click **"+ Create"** (góc trên phải).

### Bước 3: Nhập thông tin

| Trường | Mô tả |
|--------|-------|
| Product Code | Mã sản phẩm |
| Product Name | Tên sản phẩm |
| Price | Giá niêm yết (≥ 1.000 VND) |
| Product Type | Loại sản phẩm |
| Limit Courses | Số khóa học giới hạn |
| Limit Duration | Thời gian hoạt động |
| Product Category | Độ tuổi (18+, Kids, Teen) hoặc chuyên ngành |
| Product Line | Nhánh nhỏ hơn |
| Status | Active / Deactive |
| Created At | Thời điểm tạo |

> Nếu Product Type = FlexCombo: cần chọn thêm Course Line.

#### Legal (Hợp đồng)
Khi tạo/sửa sản phẩm, mục **Legal** cho phép chọn:
- **Contract template** — mẫu hợp đồng đã tạo trước
- **Representative** — người đại diện

### Bước 4: Hoàn thành
- Nhấn **Save**
- Lỗi → hệ thống báo trường cần bổ sung
- Trường màu đỏ = bắt buộc

## Liên quan
- [Order & Payment](Order-&-Payment)
- [Sale Process](Sale-Process)
