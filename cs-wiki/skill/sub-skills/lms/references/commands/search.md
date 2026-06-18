# Search Wiki (dùng agent tools)

Dùng **Grep** tool thay vì CLI command:

### AND search
```bash
grep pattern:"tạo lớp mới" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/LMS"
grep pattern:"điểm danh học viên" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/LMS"
```

### Exact phrase
```bash
grep pattern:"trạng thái học sinh" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/LMS"
```

### OR (bug search)
```bash
grep pattern:"lỗi enroll không vào lớp" include:"*.md" path:"cs-wiki/wiki/1.-Foundation/LMS"
```
