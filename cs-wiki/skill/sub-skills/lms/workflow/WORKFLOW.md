# Workflow

## 0. Classify Intent
Determine how-to vs bug/issue:

| Type | Signal | Route |
|------|--------|-------|
| How-to | "Cách...", "Làm sao...", "Hướng dẫn..." | → Step 1a |
| Bug/Issue | "Lỗi...", "Bị...", "Không... được", error | → Step 1b |

## 1a. How-to — Parse Feature (LMS only)
**LMS features** (wiki: `1.-Foundation/LMS/`):
| Câu hỏi | File | Ghi chú |
|---------|------|---------|
| Tổng quan, dashboard, roles | `Overview` | |
| Khóa học (course line/topic/course) | `Courses` | |
| Học sinh — trạng thái, profile | `Students` | |
| Enrollment — **duyệt yêu cầu từ CRM** | `Students` | Khác với CRM Enrollment (gửi yêu cầu) |
| Withdraw — rút khỏi lớp | `Students` | |
| Onhold/Dropout request | `Students` | |
| Học bù (Makeup) | `Students` | |
| Customer care / gọi điện | `Calling`, `Students` | |
| Giáo viên — tạo tk, schedule, bảng công | `Teachers` | |
| Lớp học — tạo lớp, schedule, class site | `Classes` | |
| Điểm danh (attendance) | `Classes` | |
| Nhận xét, performance, checkpoint | `Classes` | |
| Office Hours (trial/fixed/event/makeup) | `Office-Hours` | |
| Báo cáo, bảng chấm công | `Reports` | |
| Khiếu nại công | `Reports` | |
| Thiết lập, đổi mật khẩu | `Settings` | |

> ⚠ **Enrollment**: Nếu user hỏi "không enroll được" → hỏi rõ "bạn enroll từ CRM (Send Enroll) hay duyệt trên LMS?" CRM enroll ≠ LMS enroll.

## 1b. Bug/Issue — Parse Error (LMS only)
1. Identify affected feature
2. Search Known Bugs at `cs-wiki/wiki/7.-Known-Issues-&-Edge-Cases/7.1-Known-Bugs-&-Workarounds`
3. If match → report workaround
4. If not → escalate

## 2. Search (LMS wiki)
Dùng **Grep** tool để search:
```bash
grep pattern:"<query>" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/LMS"
```

## 3. Not Found → Check GitBook
Use LMS MCP tools to check `usage-lms-xschool`. Update wiki → answer.

## 4. Answer
- Cite file + section
- If not found: "Chưa có trong wiki LMS"
- If question is about CRM → redirect: "Đây là CRM, dùng skill CRM để tra cứu."
