# Wiki File Structure — mindx-cs-wiki

```
cs-wiki/wiki/
├── 1.-Foundation/
│   ├── 1.1-Products-&-Services.md       [Chung] products, services, promotions
│   ├── 1.2-Service-Tiers-&-SLAs.md      [Chung]
│   ├── 1.3-Glossary.md                  [Chung] CRM/LMS concepts + glossary
│   ├── 1.4-Tools-&-Access.md            [Chung] UI, Account, Roles, Permissions
│   ├── CRM/                             [CRM v1+v2 merged, flat]
│   │   ├── Lead-Management.md           Lead stages, status, assign, filters, UTM, phone
│   │   ├── Order-&-Payment.md           Order flow, payment, promotions, fix price
│   │   ├── Sale-Process.md              Enrollment, transfer, upsale, downsale
│   │   ├── Econtract.md                 Hợp đồng điện tử (v1)
│   │   ├── Contract.md                  Thông tin hợp đồng (v2)
│   │   ├── Receipt.md                   Phiếu thu (v2)
│   │   ├── Customer-Management.md       Quản lý khách hàng (v2)
│   │   ├── Product.md                   Tạo/sửa sản phẩm
│   │   ├── Settings.md                  Hide phone, SMS, channel, payment method, backup bank
│   │   └── Report-KPI.md                Report built-in (deprecated → Report Application)
│   ├── LMS/
│   │   ├── Overview.md                  Roles, dashboard, trạng thái lớp
│   │   ├── Courses.md                   Course line, topic, course
│   │   ├── Students.md                  Trạng thái HS, enrollment, withdraw, makeup
│   │   ├── Classes.md                   Tạo lớp, điểm danh, nhận xét, checkpoint
│   │   ├── Teachers.md                  Tài khoản GV, timesheet, attendance request
│   │   ├── Office-Hours.md              Trial/fixed/event/makeup OH
│   │   ├── Calling.md                   Gọi điện, CSKH script
│   │   ├── Reports.md                   Summary, attendance, student detail
│   │   ├── Centers.md                   Quản lý cơ sở
│   │   └── Settings.md                  Learning medium, operation method, course lines
│   └── Report-Application/
│       ├── Report-Application.md        Tổng quan, phân quyền, tần suất cập nhật
│       ├── Q&A-Report.md                Tra cứu câu lệnh, DIM, keywords
│       ├── Measures-&-Definitions.md    S&M measures, OPS measures, student status
│       ├── CR-Formulas.md               CR12/23/34/45/CRX5 + công thức chi tiết
│       ├── MKT-Reports.md               MKT Dashboard, Marketing Performance, DIM Channel
│       └── Sale-Reports.md              Realtime, Sale Performance, Call Performance, Telemarketing
├── 2.-Ticket-Lifecycle/
│   ├── 2.1-Reception-&-Triage.md
│   ├── 2.2-Initial-Response.md
│   ├── 2.3-Diagnosis.md
│   ├── 2.4-Resolution.md
│   ├── 2.5-Communication.md
│   ├── 2.6-Closure.md
│   └── 2.7-Trend-Analysis.md
├── 3.-Escalation/
│   ├── 3.1-When-to-Escalate.md
│   ├── 3.2-Tier-Definitions-&-Routing.md
│   └── 3.3-Emergency-Contacts.md
├── 4.-Communication-Playbook/
│   ├── 4.1-To-Customers.md
│   ├── 4.2-To-Dev-Team.md
│   └── 4.3-To-Management.md
├── 5.-Response-Templates/
│   ├── 5.1-Acknowledgment.md
│   ├── 5.2-Status-Updates.md
│   ├── 5.3-Resolution-Confirmed.md
│   ├── 5.4-Negative-Outcomes.md
│   └── 5.5-Template-Description.md
├── 6.-Policies/
│   ├── 6.1-Account-Management.md
│   └── 6.2-Privacy-&-Data-Handling.md
├── 7.-Known-Issues-&-Edge-Cases/
│   ├── 7.1-Known-Bugs-&-Workarounds.md
│   ├── 7.2-Edge-Cases.md
│   ├── 7.3-HTML-Templates-Archive.md
│   └── 7.3-HTML-Templates-Archive/      (template files .md)
└── 8.-Resolved-Tickets/
    └── 8.1-Past-Resolutions-Log.md
```

## Ghi chú cấu trúc

### CRM (merged v1+v2)
- Tất cả file CRM nằm tại `1.-Foundation/CRM/` (flat, không tách v1/v2)
- Mỗi section tagged `[v1]` / `[v2]` / `[v1+v2]`

### Skill
- Skill files tại `cs-wiki/skill/` (đồng bộ từ `.opencode/skills/wiki/`)
- Dùng **Grep/Glob/Read** tools để tra cứu — không dùng Python CLI
