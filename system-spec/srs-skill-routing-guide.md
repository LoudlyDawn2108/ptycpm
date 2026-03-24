# Hướng dẫn chọn skill để viết tài liệu SRS

Tài liệu này hướng dẫn **AI** chọn đúng skill trong thư mục `.agents/skills` khi viết nội dung cho **Tài liệu Đặc tả Yêu cầu Phần mềm (SRS)** của hệ thống phần mềm mà nhóm đang phân tích yêu cầu.

Mục tiêu của tài liệu này là:
- chọn **đúng skill chính** cho từng phần của SRS;
- biết khi nào cần dùng **skill hỗ trợ**;
- tránh dùng sai skill cho sai loại nội dung;
- bảo đảm nội dung SRS có thể **truy vết**, **nhất quán**, **đúng loại yêu cầu** và **đủ chất lượng**.

---

## 1. Danh sách skill hiện có và vai trò chính

| Skill | Vai trò chính | Nên dùng khi nào |
|---|---|---|
| `stakeholder-requests` | Thu thập và cấu trúc nhu cầu thô từ stakeholder | Khi làm việc với phỏng vấn, nhu cầu người dùng, bối cảnh nghiệp vụ, môi trường sử dụng |
| `vision-document` | Chuyển nhu cầu stakeholder thành phạm vi sản phẩm và các feature (FEAT) | Khi viết phạm vi, mô tả sản phẩm, các chức năng chính, ranh giới hệ thống |
| `use-case-specification` | Đặc tả yêu cầu chức năng dưới dạng tương tác actor–system | Khi viết use case, actor, basic flow, alternative flow, pre/postconditions |
| `supplementary-specification` | Viết và đánh giá yêu cầu bổ sung / phi chức năng / ràng buộc | Khi viết NFR, quality attributes, constraints, interface requirements, legal/privacy |
| `requirement-evaluation` | Đánh giá chất lượng requirement | Khi kiểm tra requirement có rõ, đo được, atomic, không mơ hồ, không trùng lặp hay không |
| `requirements-management-plan` | Tổ chức loại yêu cầu, thuộc tính, truy vết, cấu trúc tài liệu | Khi cần xác định loại requirement, mapping tài liệu, traceability, attribute rules |
| `oo-design-from-use-cases` | Dẫn xuất class/sequence diagram từ use case | **Không dùng để viết SRS gốc**; chỉ dùng sau khi use case đã ổn định |
| `test-case-tables` | Dẫn xuất test case từ use case và supplementary requirements | **Không dùng để viết SRS gốc**; chỉ dùng sau khi SRS/UCS/SUPL đã ổn định |

---

## 2. Nguyên tắc chọn skill cho SRS

### 2.1. Nguyên tắc chung

1. **Bắt đầu từ stakeholder/problem domain** → dùng `stakeholder-requests`.
2. **Chuyển nhu cầu thành phạm vi sản phẩm và feature** → dùng `vision-document`.
3. **Mô tả yêu cầu chức năng chi tiết** → dùng `use-case-specification`.
4. **Mô tả yêu cầu phi chức năng / ràng buộc / yêu cầu cắt ngang** → dùng `supplementary-specification`.
5. **Tổ chức loại yêu cầu, traceability, thuộc tính yêu cầu** → dùng `requirements-management-plan`.
6. **Rà chất lượng requirement trước khi chốt** → dùng `requirement-evaluation`.

### 2.2. Nguyên tắc quan trọng

- Nếu nội dung là **nhu cầu người dùng thô** → không nhảy ngay sang `use-case-specification`.
- Nếu nội dung là **feature/phạm vi sản phẩm** → ưu tiên `vision-document`, không ưu tiên `supplementary-specification`.
- Nếu nội dung là **tương tác actor–system theo luồng** → ưu tiên `use-case-specification`.
- Nếu nội dung là **cross-cutting / system-wide / NFR / constraint** → ưu tiên `supplementary-specification`.
- Nếu nhiệm vụ là **chấm / sửa chất lượng câu requirement** → bắt buộc dùng `requirement-evaluation`.

---

## 3. Mapping skill theo cấu trúc SRS

## 3.1. Phần 1 — Giới thiệu

### 1.1. Phạm vi (sản phẩm và lĩnh vực)

- **Skill chính:** `vision-document`
- **Skill hỗ trợ:** `stakeholder-requests`, `requirements-management-plan`

**Dùng khi:**
- xác định hệ thống phục vụ lĩnh vực nào;
- xác định phạm vi nghiệp vụ, phạm vi sản phẩm, ranh giới hệ thống;
- phân biệt cái gì thuộc hệ thống, cái gì nằm ngoài hệ thống.

**Lý do:**
- `vision-document` mạnh nhất ở phần **scope**, **problem**, **product boundary**, **summary of capabilities**.
- `stakeholder-requests` hỗ trợ khi phạm vi còn đang nằm trong lời nói/nhu cầu thô của stakeholder.
- `requirements-management-plan` hỗ trợ khi cần nhất quán với kiểu requirement và tài liệu của dự án.

**Không nên dùng skill chính:**
- `use-case-specification` vì phần này chưa phải luồng tương tác chi tiết.
- `supplementary-specification` vì đây chưa phải phần NFR.

---

### 1.2. Tổng quan về tài liệu

- **Skill chính:** `requirements-management-plan`
- **Skill hỗ trợ:** `vision-document`

**Dùng khi:**
- mô tả tài liệu SRS gồm những phần nào;
- giải thích quan hệ giữa SRS với STR, VIS, UCS, SS;
- giải thích logic tổ chức requirement trong dự án.

**Lý do:**
- `requirements-management-plan` mạnh nhất ở phần **document organization**, **requirement types**, **document-to-requirement mapping**, **traceability structure**.

---

## 3.2. Phần 2 — Mô tả chung

### 2.1. Mô tả chung về giao diện

- **Skill chính:** `vision-document`
- **Skill hỗ trợ:** `stakeholder-requests`, `supplementary-specification`

**Dùng khi:**
- mô tả môi trường sử dụng, nhóm người dùng, thiết bị, kênh truy cập, kỳ vọng giao diện ở mức tổng quan;
- mô tả giao diện ở mức **overview**, chưa đi vào requirement chi tiết từng màn hình.

**Lý do:**
- `vision-document` phù hợp hơn với phần **mô tả chung** trong một tài liệu SRS vì skill này bao phủ **product overview**, **product perspective**, **user environment ở mức tổng quan** và **ranh giới sản phẩm**.
- `stakeholder-requests` chỉ nên dùng như nguồn đầu vào hỗ trợ khi phần mô tả giao diện tổng quan còn đang nằm trong ghi chép phỏng vấn, nhu cầu thô hoặc mô tả môi trường sử dụng của stakeholder.
- `supplementary-specification` chỉ hỗ trợ nếu cần nhắc đến yêu cầu giao diện mang tính cross-cutting như accessibility, compatibility, consistency.

**Lưu ý:**
- Nếu là **mô tả giao diện tổng quan**, không viết như danh sách UI requirement chi tiết.
- Nếu đã là **“hệ thống shall…”** về UI, hãy chuyển sang mục 3.1 hoặc dùng `supplementary-specification`.

---

### 2.2. Các chức năng chính

- **Skill chính:** `vision-document`
- **Skill hỗ trợ:** `stakeholder-requests`, `use-case-specification`

**Dùng khi:**
- liệt kê các chức năng/capability chính của hệ thống ở mức feature;
- chưa đi vào basic flow / alternative flow chi tiết.

**Lý do:**
- `vision-document` là skill phù hợp nhất để chuyển **STRQ → FEAT**.
- `stakeholder-requests` giúp bảo đảm các chức năng chính bám nhu cầu thật của stakeholder.
- `use-case-specification` chỉ hỗ trợ khi cần đối chiếu feature nào sẽ được hiện thực hóa bằng use case nào.

---

## 3.3. Phần 3 — Các yêu cầu cụ thể

### 3.1. Các yêu cầu về giao diện

- **Skill chính:** `supplementary-specification`
- **Skill hỗ trợ:** `use-case-specification`, `stakeholder-requests`, `requirement-evaluation`

**Dùng khi:**
- viết các yêu cầu UI có thể kiểm thử: consistency, accessibility, responsive behavior, keyboard navigation, browser compatibility, error message behavior, interface constraints;
- viết các interface requirement mang tính toàn hệ thống hoặc nhiều use case.

**Lý do:**
- `supplementary-specification` bao phủ đúng **Interface Requirements**, **Usability**, **Compatibility**, **cross-cutting UI requirements**.
- `use-case-specification` chỉ dùng bổ trợ nếu giao diện gắn chặt với một use case cụ thể.
- `requirement-evaluation` dùng để soát các câu requirement UI sau khi viết xong.

**Quy tắc phân ranh:**
- UI tổng quan → 2.1
- UI requirement cụ thể, đo được → 3.1
- UI chỉ gắn với đúng một use case → có thể đưa vào UCS Special Requirements thay vì SS

---

### 3.2. Các yêu cầu chức năng

- **Skill chính:** `use-case-specification`
- **Skill hỗ trợ:** `vision-document`, `requirement-evaluation`, `requirements-management-plan`

**Dùng khi:**
- viết yêu cầu chức năng chi tiết dưới dạng actor, trigger, basic flow, alternative flow, preconditions, postconditions;
- tổ chức requirement theo các UC.

**Lý do:**
- `use-case-specification` là skill đúng nhất cho **functional requirements** thể hiện dưới dạng tương tác actor–system.
- `vision-document` giúp bảo đảm mỗi UC truy vết về đúng FEAT.
- `requirement-evaluation` dùng để rà câu requirement chức năng nếu được viết ngoài bảng UC.
- `requirements-management-plan` giúp giữ đúng ID, loại requirement và truy vết.

**Không nên dùng skill chính:**
- `supplementary-specification` cho phần hành vi chi tiết theo luồng.

---

### 3.3. Các yêu cầu bổ sung

> Bao gồm: các yêu cầu thực thi, các yêu cầu về ràng buộc thiết kế, các đặc tính của phần mềm.

- **Skill chính:** `supplementary-specification`
- **Skill hỗ trợ:** `requirements-management-plan`, `requirement-evaluation`, `vision-document`

**Dùng khi:**
- viết các yêu cầu phi chức năng (performance, reliability, security, usability, supportability);
- viết design constraints, implementation constraints, interface constraints, legal/privacy constraints;
- viết các yêu cầu cross-cutting nhiều use case;
- phân loại requirement theo FURPS+.

**Lý do:**
- đây chính là phạm vi mạnh nhất của `supplementary-specification`.
- `requirements-management-plan` hỗ trợ về **thuộc tính requirement**, **traceability**, **document placement**.
- `requirement-evaluation` dùng để sửa các câu SUPL cho đủ atomic, measurable, unambiguous, testable.
- `vision-document` hỗ trợ khi cần truy ngược SUPL về FEAT nguồn.

**Quy tắc phân ranh bắt buộc:**
- nếu yêu cầu chỉ áp dụng cho **một use case / một bước của flow** → cân nhắc đặt ở UCS Special Requirements;
- nếu yêu cầu là **system-wide hoặc cross-use-case** → đặt ở mục 3.3 và dùng `supplementary-specification`.

---

### 3.4. Các yêu cầu khác

- **Skill chính:** `requirements-management-plan`
- **Skill hỗ trợ:** `supplementary-specification`, `stakeholder-requests`, `requirement-evaluation`

**Dùng khi:**
- phần “yêu cầu khác” chứa các mục như: traceability note, quy ước đặt ID, requirement attributes, assumptions/dependencies, document constraints, reporting views, glossary linkage, hoặc các yêu cầu còn lại không khớp gọn với 3.1–3.3;
- cần quyết định requirement này nên nằm ở đâu trong hệ tài liệu.

**Lý do:**
- `requirements-management-plan` mạnh nhất ở **phân loại requirement**, **mapping requirement ↔ document**, **traceability**, **attribute policy**.
- nếu “yêu cầu khác” thực chất là NFR/constraint → dùng `supplementary-specification` làm skill phụ hoặc skill chính tùy nội dung cụ thể.
- nếu “yêu cầu khác” đến từ stakeholder/context → dùng `stakeholder-requests` để bóc nguồn gốc.

---

## 4. Mapping nhanh dạng bảng

| Phần SRS | Skill chính | Skill hỗ trợ | Ghi chú |
|---|---|---|---|
| 1.1 Phạm vi | `vision-document` | `stakeholder-requests`, `requirements-management-plan` | Dùng để xác định scope, boundary, product/lĩnh vực |
| 1.2 Tổng quan tài liệu | `requirements-management-plan` | `vision-document` | Dùng để tổ chức tài liệu và quan hệ giữa các loại requirement |
| 2.1 Mô tả chung về giao diện | `vision-document` | `stakeholder-requests`, `supplementary-specification` | Chỉ cho overview, chưa đi vào UI requirement chi tiết |
| 2.2 Các chức năng chính | `vision-document` | `stakeholder-requests`, `use-case-specification` | Mức feature/capability |
| 3.1 Các yêu cầu về giao diện | `supplementary-specification` | `use-case-specification`, `stakeholder-requests`, `requirement-evaluation` | UI requirements đo được, cross-cutting |
| 3.2 Các yêu cầu chức năng | `use-case-specification` | `vision-document`, `requirements-management-plan`, `requirement-evaluation` | Functional behavior, actor-system flows |
| 3.3 Các yêu cầu bổ sung | `supplementary-specification` | `requirements-management-plan`, `requirement-evaluation`, `vision-document` | NFR, constraints, quality attributes |
| 3.4 Các yêu cầu khác | `requirements-management-plan` | `supplementary-specification`, `stakeholder-requests`, `requirement-evaluation` | Dùng cho traceability, attributes, placement rules, residual requirements |

---

## 5. Skill dùng để kiểm tra chéo sau khi viết xong

### 5.1. Kiểm tra chất lượng requirement

- **Skill bắt buộc dùng để review:** `requirement-evaluation`

**Dùng sau khi đã viết xong bất kỳ phần nào của SRS** để kiểm tra:
- requirement có rõ không;
- có đo được không;
- có atomic không;
- có implementation-free không;
- có bị trùng/mâu thuẫn/thiếu điều kiện không.

---

### 5.2. Kiểm tra cấu trúc quản lý yêu cầu và truy vết

- **Skill bắt buộc dùng khi rà toàn bộ bộ tài liệu:** `requirements-management-plan`

**Dùng để kiểm tra:**
- loại requirement đã đặt đúng chỗ chưa;
- FEAT, UC, SUPL có trace đúng chưa;
- attribute policy có nhất quán chưa;
- mapping SRS ↔ UCS ↔ SS có rõ chưa.

---

## 6. Những skill không phải để viết SRS gốc

### `oo-design-from-use-cases`

Không dùng như skill chính để soạn nội dung SRS. Chỉ dùng **sau khi** phần yêu cầu chức năng / use case đã ổn định, để:
- chuyển use case thành class diagram;
- sinh sequence diagram;
- kiểm tra BCE-based design.

### `test-case-tables`

Không dùng như skill chính để soạn nội dung SRS. Chỉ dùng **sau khi** requirement đã ổn định, để:
- sinh test case từ UC và SUPL;
- lập test matrix;
- kiểm tra coverage, boundary, negative cases.

---

## 7. Quy trình AI nên làm khi viết SRS cho nhóm

### Bước 1 — Thu thập và chuẩn hóa đầu vào
- Dùng `stakeholder-requests` nếu đầu vào còn là ghi chép phỏng vấn, nhu cầu người dùng, bối cảnh thô.

### Bước 2 — Xác định phạm vi và các chức năng chính
- Dùng `vision-document` để viết phần 1.1, 2.2 và dựng khung feature của hệ thống.

### Bước 3 — Tổ chức kiểu requirement và truy vết
- Dùng `requirements-management-plan` để xác định phần nào là FEAT, UC, SUPL; phần nào nằm ở SRS, UCS, SS.

### Bước 4 — Viết yêu cầu chức năng chi tiết
- Dùng `use-case-specification` cho mục 3.2.

### Bước 5 — Viết yêu cầu giao diện và yêu cầu bổ sung
- Dùng `supplementary-specification` cho mục 3.1, 3.3 và phần constraint trong 3.4 nếu phù hợp.

### Bước 6 — Kiểm tra chất lượng toàn bộ requirement
- Dùng `requirement-evaluation` để rà chất lượng từng mục và toàn bộ SRS.

### Bước 7 — Chỉ sau khi SRS ổn định mới làm bước sau
- Dùng `oo-design-from-use-cases` để đi sang thiết kế.
- Dùng `test-case-tables` để đi sang kiểm thử.

---

## 8. Chỉ dẫn ngắn cho AI

Nếu AI được giao viết SRS theo cấu trúc này, hãy áp dụng routing rule sau:

1. **Scope / overview / main functions** → `vision-document`
2. **Stakeholder context / user environment / raw needs** → `stakeholder-requests`
3. **Functional requirements / use cases** → `use-case-specification`
4. **UI requirements / NFR / constraints / supplementary requirements** → `supplementary-specification`
5. **Traceability / requirement types / document organization** → `requirements-management-plan`
6. **Quality review of written requirements** → `requirement-evaluation`
7. **Design from stable use cases** → `oo-design-from-use-cases`
8. **Test derivation from stable requirements** → `test-case-tables`

---

## 9. Kết luận

Khi viết SRS cho hệ thống phần mềm mà nhóm đang phân tích yêu cầu, AI **không nên dùng một skill duy nhất cho toàn bộ tài liệu**. Cách đúng là:

- dùng `vision-document` cho phần **scope và feature**;
- dùng `use-case-specification` cho phần **functional requirements**;
- dùng `supplementary-specification` cho phần **supplementary requirements / NFR / constraints**;
- dùng `requirements-management-plan` để giữ **đúng cấu trúc và truy vết**;
- dùng `requirement-evaluation` để **soát chất lượng cuối**.

Đây là cách phân chia phù hợp nhất với hệ skill hiện có trong dự án.
