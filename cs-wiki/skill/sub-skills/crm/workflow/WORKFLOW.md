# Workflow — CRM (only)

## 0. Version Detection
Before answering, determine if user is using v1 or v2:
- Check URL patterns, feature names, or known errors (see `protocol/PROTOCOL.md`)
- If ambiguous → ask the user
- If answered previously → use the same version

## 1. Classify Intent
Determine whether the user is asking a **how-to** question or reporting a **bug/issue**:

| Type | Signal | Route |
|------|--------|-------|
| **How-to** | "Cách...", "Làm sao...", "Hướng dẫn...", "Tạo...", "Sửa...", "Xóa..." | → Step 1a |
| **Bug/Issue** | "Lỗi...", "Bị...", "Không... được", "Báo...", error message, behavior bất thường | → Step 1b |

> ⚠ Nếu user hỏi về LMS (class, attendance, điểm danh, khóa học trên LMS) → redirect: "Vấn đề này thuộc LMS. Dùng skill LMS để tra cứu."

### 1a. How-to Flow — CRM features only
**Parse feature** from the question:
| Câu hỏi | File | Ghi chú |
|---------|------|---------|
| Lead management (stage/status/assign) | `Lead-Management` | |
| Order/Payment | `Order-&-Payment` | |
| Enrollment — **Send Enroll (gửi yêu cầu từ CRM sang LMS)** | `Sale-Process` | Khác LMS enroll (duyệt yêu cầu) |
| Transfer/Upsale/Downsale | `Sale-Process` | |
| Econtract (hợp đồng điện tử) | `Econtract` | Chỉ v1 |
| Contract (thông tin hợp đồng) | `Contract` | v2 |
| Product | `Product` | |
| Receipt / Phiếu thu | `Receipt` | |
| Settings (hide phone, SMS, channel) | `Settings` | |
| Report/KPI | `Report-KPI` | |
| Customer management | `Customer-Management` | |

→ Continue to **Step 2a**

### 1b. Bug/Issue Flow — CRM only
1. **Confirm version** — v1 or v2 (ask if unclear)
2. **Identify affected feature** — enrollment? payment? lead? contract? product?
3. **Identify error context** — exact error message, behavior, what the user was doing
4. **Search Known Bugs** — look in `7.-Known-Issues-&-Edge-Cases/7.1-Known-Bugs-&-Workarounds.md` for matching Issue + Environment
5. **If match found** — report workaround + note status (Active/Resolved)
6. **If no match** → search broader wiki and GitBook for the feature + error
7. **If still nothing** → guide escalation: "Bug chưa được ghi nhận trong wiki. Hãy báo dev team với steps reproduce + ảnh chụp + timestamp."

→ Continue to **Step 2b**

## 2. Search
### 2a. Search Wiki (How-to)
Dùng **Grep** tool để search:
- **AND search**: `grep pattern:"keyword1 keyword2" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"`
- **Exact phrase**: `grep pattern:"exact phrase" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"`
- **OR search** (bug): `grep pattern:"keyword1|keyword2" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/CRM"`

### 2b. Search Known Bugs (Bug/Issue)
```bash
grep pattern:"error keyword1|error keyword2" include:"*.md" path:"cs-wiki/wiki/7.-Known-Issues-&-Edge-Cases"
```
Use OR mode (regex `|`) to catch partial matches in `7.1-Known-Bugs-&-Workarounds.md`.

## 3. Read Results
- Từ kết quả Grep, xác định file + line number
- Dùng **Read** tool để đọc section đầy đủ
- Ghi chú version tag `[v1]` / `[v2]` / `[v1+v2]`

## 4. Not Found → Check GitBook
If wiki yields no results:
1. Use GitBook MCP tools to search original docs
2. **v1**: `gitbook-crm_getPage(url: "https://mindxtech.gitbook.io/usage-crm-xschool/<path>")`
3. **v2**: `gitbook-crm-v2_getPage(url: "https://mindxtech.gitbook.io/usage-crm-v2-xschool/<path>")`
4. If content found → **update the wiki file first**
5. Then answer from wiki

## 5. Answer
### 5a. How-to Answer
- Cite file + section + version tag
- Keep answers concise
- If not found in wiki or GitBook: "Not yet documented in wiki"

### 5b. Bug/Issue Answer
- State: version + affected feature + error
- If workaround found: cite `7.1-Known-Bugs-&-Workarounds` + describe workaround + note status
- If no workaround: "Bug chưa được ghi nhận trong wiki. Steps để escalate: [steps reproduce → ảnh chụp → timestamp → báo dev team]"

## 6. Stop
No follow-up unless the user asks.
