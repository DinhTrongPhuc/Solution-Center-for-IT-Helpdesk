# Gọi điện trên LMS

Gọi điện trực tiếp từ LMS, ghi nhận lịch sử & ghi âm.

## Thực hiện cuộc gọi

- **Students** → tìm tên theo số điện thoại → **View detail** → click icon gọi
- Brand hiển thị: **Call customer [số điện thoại]**. Branding trên máy khách: *Trường học công nghệ MindX*.
- Mặc định: **Customer's phone**. Nếu có 2 SĐT khác nhau → click chọn số để đổi.
- Trạng thái: **Calling...** (đang đổ chuông) → **đồng hồ** (đã kết nối).

**Trạng thái cuộc gọi:**

| Trạng thái | Định nghĩa |
|------------|-----------|
| **Answered** | Kết nối thành công, hai bên trao đổi |
| **No Answer** | Máy khách rung chuông nhưng không trả lời, tự ngắt |
| **Rejected** | Máy khách rung chuông, từ chối nhận cuộc gọi |
| **Cancel** | Máy khách rung chuông, CS tắt máy |
| **Failed** | Chưa kết nối tới khách, máy chưa rung chuông nhưng tự ngắt |

## Kịch bản CSKH

**Tạo mới:** Settings → **Customer care script** → **+** → điền Name, Description, Customer care type, Status = **Active**.
Question: Title, Feedback options (select), Handler input (cho nhập tay).

> Hiện nay **chưa ràng buộc** hiển thị kịch bản theo Customer care type.

**Sử dụng:** Students → chọn học viên → **Customer care record** → chọn script → trả lời → Confirm → Save.

**Lưu ý — phải theo đúng thứ tự:**
1. **Select Customer care script** — chọn kịch bản phù hợp
2. **Check results** — ghi nhận câu trả lời PHHS theo kịch bản
3. **Confirm** — xác nhận câu trả lời
4. **Save Customer care record** — lưu nội dung CSKH

> Câu trả lời kịch bản tự lưu vào phần ghi chú CSKH. Vẫn cần điền đầy đủ các trường bắt buộc trước khi Save.

## Lịch sử cuộc gọi

**2 nơi xem:** Call history (menu) — tất cả cuộc gọi; Tab Call history trong student — riêng học viên đó.

| Cột | Ý nghĩa |
|-----|---------|
| Caller | Người gọi |
| Role | Vai trò |
| App | CRM / LMS |
| From | Đầu số hiển thị |
| To | SĐT nhận + thông tin người nhận |
| Status | Trạng thái |
| Start time | Thời gian gọi |
| Time duration | Thời lượng |
| Full call | Nghe/tua/download ghi âm |

> Ko bắt máy → **00:00**, không nghe được.

## Hẹn lịch gọi lại

**Tạo sau khi gọi:** Ko liên lạc được → auto hiện form → nhập ngày/giờ/ghi chú → **Lưu**.

**Tạo từ Call history:** Chọn cuộc gọi ko thành công → icon tạo lịch → điền → **Lưu**.

> Chỉ tạo được với cuộc gọi **không thành công**.

**Nhắc nhở:** Email tự động **8-9h sáng** ngày hẹn. Ko gửi nếu gọi lại **cùng ngày**.

**Màn Lịch gọi lại:**

*Filter:*

| Filter | Ý nghĩa |
|--------|---------|
| Thanh tìm kiếm | SĐT khách hàng hoặc Student ID |
| Tạo bởi | Người tạo lịch |
| Cơ sở | Cơ sở người tạo |
| Ngày gọi lại | Ngày dự kiến |
| Trạng thái | Pending / Done |

*Cột hiển thị:* Remind Date, Called by, Status, Call date, Customer phone, Student Name/ID, Class Name, Centre.

- Chuyển Pending → **Done** ở cột Status.
- Phân quyền: xem tất cả / chỉ lịch cá nhân.

## Liên hệ bổ sung

Dùng khi SĐT CRM ko liên lạc được, cần SĐT thay thế.

**Thêm SĐT:** Student → tìm HS (SĐT CRM hoặc ID) → **SDT bổ sung** → nhập SĐT mới → **Lưu**.

**Gọi:** Chọn **SĐT bổ sung** → Calling → kết nối.
