# Search Scoring Algorithm

Công thức tính score cho mỗi section:

```
score = density × 200 + ratio × 200 + title_boost + CRM_PRIORITY
```

## Components

### 1. Token Density (×200)
```
density = Σ(count(t) × idf(t) × weight(t)) / len(section_tokens)
```
- `count(t)`: số lần token xuất hiện trong section (title + 2000 ký tự đầu body)
- `idf(t)`: inverse document frequency (BM25-style)
- `weight(t)`: 1.0 cho original query tokens, 0.25 cho compound split tokens

### 2. Token Ratio (×200)
```
ratio = số token match / tổng số token trong query (có weight)
```

### 3. Title Boost (×50 × idf)
- Chỉ áp dụng cho **original query tokens** (không áp dụng cho split tokens)
- `title_boost = Σ(50 × idf(t))` for original query tokens `t` xuất hiện trong title

### 4. CRM Priority
| File | Priority |
|------|----------|
| 2.3-Diagnosis | 500 |
| 2.4-Resolution | 500 |
| 1.1-Products-&-Services | 300 |
| 1.6-Econtract | 300 |
| 1.7-Lead-Management | 300 |
| 1.8-Order-&-Payment | 300 |
| 1.9-Sale-Process | 300 |
| 6.1-Account-Management | 200 |
| 1.4-Tools-&-Access | 100 |
| 7.1-Known-Bugs-&-Workarounds | 50 |
| 8.1-Past-Resolutions-Log | 50 |

## Compound Word Splitting
Nếu token không tồn tại trong `all_tokens`:
- Thử split tại mọi vị trí `i` (1..len-1)
- Nếu cả `token[:i]` và `token[i:]` đều có trong `all_tokens` → thêm cả 2 với weight 0.25
- Ví dụ: `addpayment` → `add` + `payment` (mỗi từ 0.25)

## Result Grouping
- Kết quả gom nhóm theo `display` path.
- Sort groups by max score trong group.
- Trong mỗi group, sort by score descending.
