# 📁 Workspace của Ngô Quang Tùng

> File này liệt kê các phần Tùng phụ trách và skill AI cần dùng khi sửa từng file.

---

## 📋 Tổng quan phân công

| Phần | Nội dung | File | Skill AI |
|------|----------|------|----------|
| II | STRQ 7, 8 → FEAT 7.x, 8.x | `tung-contribution.md` | `vision-document` |
| III | UC 4.25–4.35, FEAT→UC mapping | `tung-contribution.md` | `use-case-specification` |
| IV | Đặc tả UC 4.25–4.35 (11 UC) | `uc-tung.md` | `use-case-specification` |
| VI | Performance (6.6) + Reliability (6.7) | `section-vi-tung.md` | `supplementary-specification` |
| VII | Section 7.3.3 (NFR trong SRS) | `srs.md` | `requirement-evaluation` |

---

## 📂 Danh sách file theo thứ tự I → VII

### ❌ Phần I: RMP — Không có

---

### ✅ Phần II: Phỏng vấn bên liên quan (STRQ → FEAT)

| File | Nội dung |
|------|----------|
| `tung-contribution.md` | Part A: STRQ 7, 8 → FEAT 7.1–7.4, 8.1–8.9 |

**Skill:** `vision-document`

```
skill(name="vision-document")
```

**Trigger keywords:** STRQ, FEAT, product features, derive features, transformation rules

---

### ✅ Phần III: Mô hình hóa yêu cầu (UC Model)

| File | Nội dung |
|------|----------|
| `tung-contribution.md` | Part B: UC 4.25–4.35 list |
| `tung-contribution.md` | Part C: FEAT→UC traceability |

**Skill:** `use-case-specification`

```
skill(name="use-case-specification")
```

**Trigger keywords:** use case model, actor, FEAT→UC mapping

---

### ✅ Phần IV: Đặc tả ca sử dụng (Use Case Specification)

| File | Nội dung |
|------|----------|
| `uc-tung.md` | UC 4.25–4.35 (11 UC đầy đủ) |

**Skill:** `use-case-specification`

```
skill(name="use-case-specification")
```

**Trigger keywords:** basic flow, alternative flow, precondition, postcondition, scenario

**Danh sách UC:**
| UC | Tên |
|----|-----|
| UC 4.25 | Thêm mới Hợp đồng lao động |
| UC 4.26 | Xem danh sách và chi tiết hợp đồng lao động |
| UC 4.27 | Chỉnh sửa hợp đồng lao động chưa có hiệu lực |
| UC 4.28 | Chấm dứt hợp đồng lao động trước hạn |
| UC 4.29 | Tìm kiếm hồ sơ nhân sự |
| UC 4.30 | Lọc danh sách hồ sơ nhân sự |
| UC 4.31 | Thêm mới Hồ sơ nhân sự |
| UC 4.32 | Chỉnh sửa trong chi tiết hồ sơ nhân sự |
| UC 4.33 | Đánh dấu thôi việc nhân sự |
| UC 4.34 | Xem Chi tiết thông tin hồ sơ nhân sự |
| UC 4.35 | Cấu hình ẩn/hiện mục khen thưởng/kỷ luật |

---

### ❌ Phần V: Biểu đồ lớp — Không có

---

### ✅ Phần VI: Yêu cầu bổ sung (Supplementary Specification)

| File | Nội dung |
|------|----------|
| `section-vi-tung.md` | Section 6.6: Performance (SUPL-P01–P07) |
| `section-vi-tung.md` | Section 6.7: Reliability (SUPL-R01–R05) |

**Skill:** `supplementary-specification`

```
skill(name="supplementary-specification")
```

**Trigger keywords:** NFR, non-functional, FURPS+, performance, reliability, quality attributes

**Danh sách SUPL:**
| Nhóm | SUPL IDs |
|------|----------|
| Performance | SUPL-P01, P01b, P02, P03a, P03b, P04, P05, P06, P07a, P07b |
| Reliability | SUPL-R01, R03a, R03b, R03c, R03d, R04, R05a, R05b |

---

### ✅ Phần VII: SRS (Software Requirements Specification)

| File | Nội dung |
|------|----------|
| `srs.md` | Section 7.3.3: Các yêu cầu bổ sung (dòng 226+) |

**Skill:** `requirement-evaluation`

```
skill(name="requirement-evaluation")
```

**Trigger keywords:** SRS, requirements quality, NFR summary

---

## 🔧 Hướng dẫn sử dụng

### Khi cần sửa file, nói với AI:

| Cần làm | Lệnh |
|---------|------|
| Sửa STRQ/FEAT | `Load skill vision-document, sửa STRQ 7 trong tung-contribution.md` |
| Sửa UC Spec | `Load skill use-case-specification, review UC 4.25 trong uc-tung.md` |
| Sửa NFR/SUPL | `Load skill supplementary-specification, sửa SUPL-P01 trong section-vi-tung.md` |
| Sửa SRS | `Load skill requirement-evaluation, review section 7.3.3 trong srs.md` |

---

## 📍 Quick Reference

| Cần làm gì | File | Skill |
|------------|------|-------|
| Sửa STRQ 7, 8 | `tung-contribution.md` | `vision-document` |
| Sửa FEAT 7.x, 8.x | `tung-contribution.md` | `vision-document` |
| Sửa UC list/mapping | `tung-contribution.md` | `use-case-specification` |
| Sửa UC 4.25–4.35 | `uc-tung.md` | `use-case-specification` |
| Sửa SUPL Performance | `section-vi-tung.md` (6.6) | `supplementary-specification` |
| Sửa SUPL Reliability | `section-vi-tung.md` (6.7) | `supplementary-specification` |
| Sửa SRS NFR section | `srs.md` (7.3.3) | `requirement-evaluation` |
