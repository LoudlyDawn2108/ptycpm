# Renumbering Reference Map

> This file is the single source of truth for all ID changes during the master document merge.
> All agents MUST apply these mappings when they encounter old IDs.

## 1. FEAT Renumbering

### Rationale
- STRQ 14 → FEAT 1.5 and STRQ 15 → FEAT 3.1 broke the STRQ.X = FEAT prefix convention
- This created a gap: FEATs went 1.x–13.x then jumped to 16.x (no 14.x or 15.x)
- Fix: move FEAT 1.5 → 14.1, FEAT 3.1 → 15.1, and shift FEAT 3.2–3.6 down to 3.1–3.5

### FEAT Mapping (Old → New)

| Old FEAT | New FEAT | Description | Owner |
|----------|----------|-------------|-------|
| FEAT 1.1 | FEAT 1.1 | (unchanged) Đăng nhập | Phúc |
| FEAT 1.2 | FEAT 1.2 | (unchanged) Đăng xuất | Phúc |
| FEAT 1.3 | FEAT 1.3 | (unchanged) Tự động đăng xuất | Phúc |
| FEAT 1.4 | FEAT 1.4 | (unchanged) Đổi mật khẩu | Phúc |
| **FEAT 1.5** | **FEAT 14.1** | Ứng dụng web SPA + RESTful API | Phúc |
| FEAT 2.1 | FEAT 2.1 | (unchanged) Tìm kiếm tài khoản | Phúc |
| FEAT 2.2 | FEAT 2.2 | (unchanged) Thêm tài khoản | Phúc |
| FEAT 2.3 | FEAT 2.3 | (unchanged) Sửa tài khoản | Phúc |
| FEAT 2.4 | FEAT 2.4 | (unchanged) Phân quyền | Phúc |
| FEAT 2.5 | FEAT 2.5 | (unchanged) Thay đổi trạng thái | Phúc |
| FEAT 2.6 | FEAT 2.6 | (unchanged) Tự động khóa TK thôi việc | Phúc |
| **FEAT 3.1** | **FEAT 15.1** | Cơ cấu tổ chức phân cấp cha-con | Phúc |
| **FEAT 3.2** | **FEAT 3.1** | Thêm mới đơn vị | Phúc |
| **FEAT 3.3** | **FEAT 3.2** | Sửa thông tin đơn vị | Phúc |
| **FEAT 3.4** | **FEAT 3.3** | Giải thể đơn vị (+ cascading) | Phúc |
| **FEAT 3.5** | **FEAT 3.4** | Xem chi tiết đơn vị | Phúc |
| **FEAT 3.6** | **FEAT 3.5** | Sáp nhập đơn vị (+ cascading) | Phúc |
| FEAT 4.1 | FEAT 4.1 | (unchanged) | Ninh |
| FEAT 4.2 | FEAT 4.2 | (unchanged) | Ninh |
| FEAT 4.3 | FEAT 4.3 | (unchanged) | Ninh |
| FEAT 4.4 | FEAT 4.4 | (unchanged) | Ninh |
| FEAT 4.5 | FEAT 4.5 | (unchanged) | Ninh |
| FEAT 5.1 | FEAT 5.1 | (unchanged) | Ninh |
| FEAT 5.2 | FEAT 5.2 | (unchanged) | Ninh |
| FEAT 5.3 | FEAT 5.3 | (unchanged) | Ninh |
| FEAT 5.4 | FEAT 5.4 | (unchanged) | Ninh |
| FEAT 6.1 | FEAT 6.1 | (unchanged) | Ninh |
| FEAT 6.2 | FEAT 6.2 | (unchanged) | Ninh |
| FEAT 7.1 | FEAT 7.1 | (unchanged) | Tùng |
| FEAT 7.2 | FEAT 7.2 | (unchanged) | Tùng |
| FEAT 7.3 | FEAT 7.3 | (unchanged) | Tùng |
| FEAT 7.4 | FEAT 7.4 | (unchanged) | Tùng |
| FEAT 8.1 | FEAT 8.1 | (unchanged) | Tùng |
| FEAT 8.2 | FEAT 8.2 | (unchanged) | Tùng |
| FEAT 8.3 | FEAT 8.3 | (unchanged) | Tùng |
| FEAT 8.4 | FEAT 8.4 | (unchanged) | Tùng |
| FEAT 8.5 | FEAT 8.5 | (unchanged) | Tùng |
| FEAT 8.6 | FEAT 8.6 | (unchanged) | Tùng |
| FEAT 8.7 | FEAT 8.7 | (unchanged) | Tùng |
| FEAT 8.8 | FEAT 8.8 | (unchanged) | Tùng |
| FEAT 8.9 | FEAT 8.9 | (unchanged) | Tùng |
| FEAT 9.1 | FEAT 9.1 | (unchanged) | Khánh |
| FEAT 9.2 | FEAT 9.2 | (unchanged) | Khánh |
| FEAT 9.3 | FEAT 9.3 | (unchanged) | Khánh |
| FEAT 10.1 | FEAT 10.1 | (unchanged) | Khánh |
| FEAT 10.2 | FEAT 10.2 | (unchanged) | Khánh |
| FEAT 10.3 | FEAT 10.3 | (unchanged) | Khánh |
| FEAT 11.1 | FEAT 11.1 | (unchanged) | Khánh |
| FEAT 11.2 | FEAT 11.2 | (unchanged) | Khánh |
| FEAT 11.3 | FEAT 11.3 | (unchanged) | Khánh |
| FEAT 11.4 | FEAT 11.4 | (unchanged) | Khánh |
| FEAT 12.1 | FEAT 12.1 | (unchanged) | Khánh |
| FEAT 12.2 | FEAT 12.2 | (unchanged) | Khánh |
| FEAT 12.3 | FEAT 12.3 | (unchanged) | Khánh |
| FEAT 12.4 | FEAT 12.4 | (unchanged) | Khánh |
| FEAT 13.1 | FEAT 13.1 | (unchanged) | Phúc |
| FEAT 13.2 | FEAT 13.2 | (unchanged) | Phúc |
| **FEAT 14.1** | **FEAT 14.1** | NEW slot (was FEAT 1.5) | Phúc |
| **FEAT 15.1** | **FEAT 15.1** | NEW slot (was FEAT 3.1) | Phúc |
| FEAT 16.1 | FEAT 16.1 | (unchanged) | Phúc |

### Summary of FEAT changes (only items that change):
- FEAT 1.5 → FEAT 14.1
- FEAT 3.1 → FEAT 15.1
- FEAT 3.2 → FEAT 3.1
- FEAT 3.3 → FEAT 3.2
- FEAT 3.4 → FEAT 3.3
- FEAT 3.5 → FEAT 3.4
- FEAT 3.6 → FEAT 3.5

### Cascading FEAT changes on traceability:
- FEAT 14.1 (was 1.5) → SUPL-DC01 (no UC)
- FEAT 15.1 (was 3.1) → SUPL-DC02 (no UC)
- FEAT 3.1 (was 3.2) → UC 4.8
- FEAT 3.2 (was 3.3) → UC 4.9
- FEAT 3.3 (was 3.4) → UC 4.10
- FEAT 3.4 (was 3.5) → UC 4.11
- FEAT 3.5 (was 3.6) → UC 4.12

## 2. STRQ changes

STRQs 1–16 remain consecutive. No renumbering needed.

### STRQ → FEAT row updates:
- STRQ 14 row: FEAT column changes from "FEAT 1.5" to "FEAT 14.1"
- STRQ 15 row: FEAT column changes from "FEAT 3.1" to "FEAT 15.1"
- STRQ 3 row: FEAT 3.2–3.6 become FEAT 3.1–3.5

## 3. UC Renumbering

UCs 4.1–4.50 remain as-is. No renumbering needed. All consecutive with no gaps.

### UC ownership:
- Phúc: UC 4.1–4.12 (12 UCs)
- Ninh: UC 4.13–4.24 (12 UCs)
- Tùng: UC 4.25–4.37 (13 UCs)
- Khánh: UC 4.38–4.50 (13 UCs)

## 4. SUPL Renumbering

### 4.1 Functionality (F series) — Owner: Phúc
No renumbering needed. SUPL-F01 through SUPL-F09 already consecutive.

### 4.2 Design Constraints (DC series) — Owner: Phúc
No renumbering needed. SUPL-DC01 through SUPL-DC03 already consecutive.
Note: DC01 is missing from current master — must be added during merge.

### 4.3 Legal/Regulatory (LR series) — Owner: Phúc
No renumbering needed. SUPL-LR01 through SUPL-LR07 already consecutive.
Note: LR04–LR07 are missing from current master — must be added during merge.

### 4.4 Usability (U series) — Owner: Ninh
Source of truth: section-vi-ninh.md (more granular than master's U01–U07).
Replace master's consolidated U01–U07 with contribution's granular version.

| Old SUPL | New SUPL |
|----------|----------|
| SUPL-U01 | SUPL-U01 |
| SUPL-U02a | SUPL-U02 |
| SUPL-U02b | SUPL-U03 |
| SUPL-U02c | SUPL-U04 |
| SUPL-U03 | SUPL-U05 |
| SUPL-U04 | SUPL-U06 |
| SUPL-U05 | SUPL-U07 |
| SUPL-U06 | SUPL-U08 |
| SUPL-U07 | SUPL-U09 |
| SUPL-U08 | SUPL-U10 |
| SUPL-U09 | SUPL-U11 |
| SUPL-U10 | SUPL-U12 |
| SUPL-U11 | SUPL-U13 |
| SUPL-U12 | SUPL-U14 |
| SUPL-U13 | SUPL-U15 |
| SUPL-U14 | SUPL-U16 |

### 4.5 Supportability (S series) — Owner: Ninh
Source of truth: section-vi-ninh.md (more granular than master's S01–S05).
Replace master's consolidated S01–S05 with contribution's granular version.

| Old SUPL | New SUPL |
|----------|----------|
| SUPL-S01 | SUPL-S01 |
| SUPL-S02 | SUPL-S02 |
| SUPL-S03 | SUPL-S03 |
| SUPL-S04 | SUPL-S04 |
| SUPL-S05 | SUPL-S05 |
| SUPL-S06 | SUPL-S06 |
| SUPL-S07 | SUPL-S07 |
| SUPL-S08 | SUPL-S08 |
| SUPL-S09a | SUPL-S09 |
| SUPL-S09b | SUPL-S10 |
| SUPL-S09c | SUPL-S11 |
| SUPL-S09d | SUPL-S12 |
| SUPL-S09e | SUPL-S13 |
| SUPL-S09f | SUPL-S14 |
| SUPL-S10 | SUPL-S15 |

### 4.6 Performance (P series) — Owner: Tùng
Source of truth: section-vi-tung.md.

| Old SUPL | New SUPL |
|----------|----------|
| SUPL-P01 | SUPL-P01 |
| SUPL-P01b | SUPL-P02 |
| SUPL-P02 | SUPL-P03 |
| SUPL-P04 | SUPL-P04 |
| SUPL-P05 | SUPL-P05 |
| SUPL-P07a | SUPL-P06 |
| SUPL-P07b | SUPL-P07 |

### 4.7 Reliability (R series) — Owner: Tùng
Source of truth: section-vi-tung.md.

| Old SUPL | New SUPL |
|----------|----------|
| SUPL-R01 | SUPL-R01 |
| SUPL-R03a | SUPL-R02 |
| SUPL-R03b | SUPL-R03 |
| SUPL-R03c | SUPL-R04 |
| SUPL-R03d | SUPL-R05 |
| SUPL-R04 | SUPL-R06 |
| SUPL-R05a | SUPL-R07 |
| SUPL-R05b | SUPL-R08 |

### 4.8 Security (SE series) — Owner: Khánh
No renumbering needed. SUPL-SE01 through SUPL-SE09 already consecutive.

### 4.9 Implementation Constraints (IC series) — Owner: Khánh
No renumbering needed. SUPL-IC01 through SUPL-IC04 already consecutive.

## 5. Source Files → Master Document Mapping

| Master Document | Source Content |
|-----------------|---------------|
| stakeholder-interviews.md | Part A from: phuc-contribution.md, ninh-contribution.md, tung-contribution.md (in Tung/), khanh-contribution.md |
| requirement-modeling.md | Part B + C from: phuc-contribution.md, ninh-contribution.md, tung-contribution.md (in Tung/), khanh-contribution.md |
| use-case-document.md | Part D from: phuc-contribution.md, Tung/uc-tung.md; Ninh + Khánh UC specs already in current master |
| suplementary-requirement.md | Part E from: phuc-contribution.md; section-vi-ninh.md; Tung/section-vi-tung.md; section-vi-khanh.md |
| srs.md | Update all FEAT/SUPL references to match new numbering |

## 6. Cross-reference dependencies to watch

- Ninh's section-vi-ninh.md references old FEAT 3.4 → must become FEAT 3.3
- Khánh's section-vi-khanh.md references FEAT 7.4 and 8.9 → unchanged
- Tùng's uc-tung.md references UC 4.40–4.42 and UC 4.47 (Khánh's range) → unchanged
- Phúc's SUPL-DC01 traces to old FEAT 1.5 → must become FEAT 14.1
- Phúc's SUPL-DC02 traces to old FEAT 3.1 → must become FEAT 15.1
- All section-vi files reference FEATs from multiple owners — check ALL FEAT refs against mapping
