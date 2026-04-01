# I. BẢN KẾ HOẠCH QUẢN LÝ YÊU CẦU

## 1.1. Giới thiệu

### 1.1.1. Mục đích

Tài liệu Kế hoạch Quản lý Yêu cầu (Requirements Management Plan – RMP) này được xây dựng nhằm xác định các phương pháp, quy trình và công cụ được sử dụng để quản lý các yêu cầu của Hệ thống Quản lý Nhân sự (Human Resource Management System – HRMS) phục vụ Trường Đại học Thủy Lợi.

Tài liệu đóng vai trò là cơ sở để:

* Định hướng hoạt động thu thập, phân tích, đặc tả và quản lý yêu cầu hệ thống;
* Đảm bảo các yêu cầu được xác định rõ ràng, nhất quán và có khả năng truy xuất nguồn gốc;
* Hỗ trợ kiểm soát và quản lý các thay đổi yêu cầu trong suốt vòng đời phát triển hệ thống;
* Làm tài liệu tham chiếu cho các giai đoạn thiết kế, phát triển, kiểm thử và nghiệm thu hệ thống.

### 1.1.2. Phạm vi áp dụng

Bản RMP này áp dụng cho toàn bộ các yêu cầu của hệ thống HRMS được phát triển nhằm phục vụ công tác quản lý nhân sự tại Trường Đại học Thủy Lợi, bao gồm các đơn vị đào tạo, đơn vị nghiên cứu khoa học, các phòng ban chức năng và các cơ sở trực thuộc nhà trường.

## 1.2. Các kiểu yêu cầu và tài liệu

### 1.2.1. Các kiểu yêu cầu cho dự án

| Loại yêu cầu | Viết tắt | Loại tài liệu | Mô tả |
| --- | --- | --- | --- |
| Yêu cầu của các bên liên quan | STRQ | Yêu cầu của các bên liên quan (STR) | Mô tả các nhu cầu, mong đợi và mục tiêu chính của người dùng và các bên liên quan đối với hệ thống. Thuộc miền vấn đề (problem domain). |
| Yêu cầu tính năng | FEAT | Tài liệu tầm nhìn (VIS) | Mô tả các điều kiện, khả năng và các tính năng tổng quát mà hệ thống cần cung cấp. Thuộc miền giải pháp (solution domain). |
| Ca sử dụng | UC | Đặc tả ca sử dụng (UCS) | Mô tả chi tiết các ca sử dụng dưới dạng tương tác giữa tác nhân và hệ thống, phản ánh các yêu cầu chức năng. Mỗi UC có một tài liệu đặc tả riêng. |
| Kịch bản | SCEN | Đặc tả ca sử dụng (UCS) | Mô tả các đường đi hợp lệ qua một ca sử dụng (luồng cơ bản và luồng thay thế), hỗ trợ triển khai lặp theo từng kịch bản. |
| Yêu cầu bổ sung | SUPL | Đặc tả bổ sung (SS) | Mô tả các yêu cầu phi chức năng và các ràng buộc của hệ thống không được thể hiện trong mô hình ca sử dụng. |
| Thuật ngữ | TERM | Bảng thuật ngữ (GLS) | Định nghĩa các thuật ngữ chuyên ngành và từ vựng chung được sử dụng trong dự án nhằm đảm bảo sự thống nhất trong giao tiếp. |

### 1.2.2. Loại tài liệu yêu cầu cho dự án

| Loại tài liệu | Viết tắt | Mô tả | Loại yêu cầu mặc định |
| --- | --- | --- | --- |
| Kế hoạch quản lý yêu cầu | RMP | Tài liệu mô tả phương pháp, quy trình và công cụ quản lý yêu cầu của dự án. | Không áp dụng |
| Yêu cầu của các bên liên quan | STR | Tập hợp các yêu cầu nghiệp vụ và mong đợi chính từ các bên liên quan. | Yêu cầu bên liên quan (STRQ) |
| Tài liệu tầm nhìn | VIS | Mô tả tổng quan hệ thống, phạm vi và các mục tiêu chính của dự án. | Yêu cầu tính năng (FEAT) |
| Đặc tả ca sử dụng | UCS | Mô tả chi tiết các ca sử dụng và cách người dùng tương tác với hệ thống. Mỗi UC có một tài liệu UCS riêng. | Ca sử dụng (UC) và Kịch bản (SCEN) |
| Đặc tả bổ sung | SS | Mô tả các yêu cầu phi chức năng và các ràng buộc của hệ thống. | Yêu cầu bổ sung (SUPL) |
| Bảng thuật ngữ | GLS | Định nghĩa từ vựng chung và thuật ngữ chuyên ngành nhân sự (hệ số lương, phụ cấp, bổ nhiệm, điều chuyển, v.v.) nhằm đảm bảo sự thống nhất trong trao đổi giữa các bên. | Thuật ngữ (TERM) |

## 1.3. Bảng liên lạc với các nhân tố chính (Stakeholder)

### 1.3.1. Các nhân tố chính

| STT | Nhân tố chính | Vai trò trong dự án | Đơn vị | Trách nhiệm chính | Hình thức liên lạc |
| --- | --- | --- | --- | --- | --- |
| 1 | Ban Giám hiệu | Nhà tài trợ / Phê duyệt | Ban Giám hiệu | Phê duyệt yêu cầu, xem xét báo cáo tổng hợp | Họp định kỳ, báo cáo |
| 2 | Phòng Tổ chức – Cán bộ | Khách hàng nghiệp vụ | Phòng TCCB | Cung cấp yêu cầu quản lý hồ sơ nhân sự | Họp, email |
| 3 | Phòng Tài chính – Kế toán | Khách hàng nghiệp vụ | Phòng TCKT | Cung cấp yêu cầu về lương, phụ cấp | Họp, trao đổi trực tiếp |
| 4 | Phòng CNTT | Đơn vị kỹ thuật | Phòng CNTT | Tư vấn kỹ thuật, hạ tầng, bảo mật | Họp kỹ thuật |
| 5 | Trưởng khoa / phòng | Người sử dụng chính | Các khoa / phòng | Góp ý, xác nhận yêu cầu quản lý nhân sự đơn vị | Họp, khảo sát |
| 6 | Nhóm phát triển | Thực hiện dự án | Nhóm dự án | Phân tích, thiết kế và triển khai hệ thống | Họp nhóm, công cụ trực tuyến |

### 1.3.2. Các bên liên quan khác

| STT | Bên liên quan | Vai trò / Mối liên hệ |
| --- | --- | --- |
| 1 | Bộ Nông nghiệp và Phát triển Nông thôn | Cơ quan quản lý nhà nước, ban hành quy định nhân sự, chế độ |
| 2 | Bộ Giáo dục và Đào tạo | Cơ quan quản lý chuyên ngành, quy định tiêu chuẩn cán bộ |
| 3 | Cơ quan Bảo hiểm xã hội | Đơn vị phối hợp quản lý bảo hiểm, chế độ người lao động |
| 4 | Cơ quan Thuế | Đơn vị phối hợp quản lý nghĩa vụ thuế thu nhập cá nhân |

## 1.4. Cấu trúc truy vết yêu cầu

### 1.4.1. Sơ đồ truy vết

Cấu trúc truy vết giữa các kiểu yêu cầu trong dự án được định nghĩa như sau:

```
STRQ ──→ FEAT ──→ UC ──→ SCEN
  │         │
  │         └──→ SUPL
  └──→ SUPL
```

Trong đó:
- **STRQ → FEAT**: Yêu cầu bên liên quan được chuyển đổi thành các tính năng hệ thống.
- **STRQ → SUPL**: Yêu cầu bên liên quan có thể truy vết trực tiếp tới yêu cầu bổ sung (phi chức năng).
- **FEAT → UC**: Tính năng được hiện thực hóa thông qua các ca sử dụng.
- **FEAT → SUPL**: Tính năng được hỗ trợ bởi các yêu cầu bổ sung.
- **UC → SCEN**: Ca sử dụng được phân tách thành các kịch bản (luồng cơ bản và luồng thay thế).

### 1.4.2. Chi tiết các đường truy vết

| Từ | Đến | Quan hệ | Ràng buộc bắt buộc |
| --- | --- | --- | --- |
| STRQ | FEAT | Nhiều-nhiều (thông thường 1 STRQ → nhiều FEAT) | Mỗi STRQ ở trạng thái **Approved** phải truy vết tới ít nhất một FEAT hoặc SUPL. |
| STRQ | SUPL | Nhiều-nhiều | (Nằm trong ràng buộc bao phủ STRQ ở trên) |
| FEAT | UC | Nhiều-nhiều | Mỗi FEAT ở trạng thái **Approved** phải truy vết tới ít nhất một UC hoặc SUPL. |
| FEAT | SUPL | Nhiều-nhiều | (Nằm trong ràng buộc bao phủ FEAT ở trên) |
| UC | FEAT | Truy vết ngược | UC truy vết ngược về FEAT mà nó hiện thực hóa. |
| SUPL | FEAT | Truy vết ngược | SUPL truy vết ngược về FEAT mà nó hỗ trợ. |
| UC | SCEN | Một-nhiều | Mỗi UC có ít nhất một SCEN (luồng cơ bản). |

## 1.5. Thuộc tính yêu cầu

Phần này định nghĩa các thuộc tính cho từng kiểu yêu cầu, bao gồm tập giá trị cho phép và ý nghĩa cụ thể trong ngữ cảnh dự án HRMS.

### 1.5.1. Thuộc tính cho FEAT (Yêu cầu tính năng)

#### Trạng thái (Status)

Theo dõi vòng đời của yêu cầu tính năng:

| Giá trị | Mô tả |
| --- | --- |
| **Proposed** (Đề xuất) | Tính năng đang được thảo luận, chưa được nhóm dự án xem xét và chấp nhận. |
| **Approved** (Đã phê duyệt) | Tính năng đã được xem xét và phê duyệt để tiến hành thiết kế và triển khai. |
| **Realized** (Đã hiện thực hóa trong thiết kế) | Tính năng đã được tích hợp vào thiết kế. Các sản phẩm thiết kế (sơ đồ, mô hình) phản ánh tính năng này. |
| **Incorporated** (Đã tích hợp vào sản phẩm) | Tính năng đã được triển khai trong mã nguồn. |
| **Validated** (Đã kiểm thử xác nhận) | Tính năng đã được kiểm thử và xác minh hoạt động đúng. |

#### Độ ưu tiên (Priority)

Xác định mức độ ưu tiên phân bổ nguồn lực phát triển:

| Giá trị | Mô tả |
| --- | --- |
| **High** (Cao) | Phải được triển khai không muộn hơn iteration đầu tiên của giai đoạn Xây dựng (Construction). |
| **Medium** (Trung bình) | Phải được triển khai không muộn hơn khi kết thúc giai đoạn Xây dựng (Construction). |
| **Low** (Thấp) | Có thể triển khai nếu còn thời gian. Ít quan trọng hơn và có thể được lùi sang các iteration hoặc phiên bản tiếp theo. |

#### Lợi ích (Benefit)

Mức độ quan trọng của tính năng đối với người dùng cuối và khách hàng:

| Giá trị | Mô tả |
| --- | --- |
| **Critical** (Thiết yếu) | Tính năng thiết yếu. Nếu không triển khai, hệ thống sẽ không đáp ứng nhu cầu khách hàng. Tất cả tính năng Critical phải có trong bản phát hành, nếu không lịch trình sẽ bị trễ. |
| **Important** (Quan trọng) | Tính năng quan trọng cho tính hiệu quả của hệ thống trong hầu hết các trường hợp sử dụng. Không thể dễ dàng cung cấp bằng cách khác. |
| **Useful** (Hữu ích) | Tính năng sẽ được sử dụng ít thường xuyên hơn, hoặc có thể có giải pháp thay thế hợp lý. Không ảnh hưởng đáng kể nếu không có trong bản phát hành. |

#### Công sức (Effort)

Ước lượng khối lượng công việc tính theo **ngày-người (person-days)**. Giá trị được xác định bởi đội phát triển (Team 3) phối hợp với Team SA/Design (Team 2).

#### Rủi ro (Risk)

Xác suất kết hợp với mức độ tác động của các sự kiện bất lợi khi triển khai:

| Giá trị | Mô tả |
| --- | --- |
| **High** (Cao) | Tác động của rủi ro kết hợp với xác suất xảy ra là cao. Ví dụ: sử dụng công nghệ mới mà nhóm chưa có kinh nghiệm, hoặc tính năng phụ thuộc hệ thống bên ngoài chưa ổn định. |
| **Medium** (Trung bình) | Tác động của rủi ro ít nghiêm trọng hơn và xác suất xảy ra nhỏ hơn. |
| **Low** (Thấp) | Tác động rủi ro tối thiểu và xác suất xảy ra thấp. |

#### Độ khó (Difficulty)

Ước lượng độ khó phân tích/thiết kế/triển khai của FEAT, được dùng để hỗ trợ lập kế hoạch iteration và đánh giá độ phức tạp kỹ thuật:

| Giá trị | Mô tả |
| --- | --- |
| **High** (Cao) | Tính năng có độ phức tạp cao, có nhiều ràng buộc nghiệp vụ hoặc kỹ thuật, hoặc phụ thuộc tích hợp/chuyển trạng thái phức tạp. |
| **Medium** (Trung bình) | Tính năng có độ phức tạp trung bình, phạm vi đủ rõ nhưng vẫn cần phân tích/thiết kế chi tiết trước khi triển khai. |
| **Low** (Thấp) | Tính năng đơn giản, ít rủi ro kỹ thuật, có thể triển khai theo mẫu quen thuộc của hệ thống. |

#### Độ ổn định (Stability)

Xác suất yêu cầu sẽ thay đổi hoặc hiểu biết của nhóm về yêu cầu sẽ thay đổi:

| Giá trị | Mô tả |
| --- | --- |
| **High** (Cao — ổn định) | Xác suất thay đổi thấp. Yêu cầu đã được hiểu rõ và thống nhất. |
| **Medium** (Trung bình) | Xác suất thay đổi vừa phải. |
| **Low** (Thấp — dễ biến động) | Xác suất thay đổi cao. Yêu cầu cần được thu thập thêm thông tin (elicitation bổ sung). Các mục có Stability = Low nên được ưu tiên làm rõ sớm. |

#### Bản phát hành mục tiêu (Target Release)

Tên hoặc số hiệu của iteration mà tính năng dự kiến được tích hợp vào sản phẩm. Kiểu dữ liệu: **Văn bản** (ví dụ: "Iteration 1", "Construction-2").

#### Người phụ trách (Assigned To)

Người chịu trách nhiệm thu thập thêm thông tin, viết đặc tả yêu cầu phần mềm và theo dõi triển khai. Kiểu dữ liệu: **Văn bản** (tên người).

#### Lý do (Reason)

Giải thích nguồn gốc hoặc lý do của yêu cầu tính năng — tham chiếu tới STRQ hoặc giải thích cụ thể. Kiểu dữ liệu: **Văn bản tự do**.

#### Kỹ thuật biến đổi (Transformation)

Ghi nhận kỹ thuật được sử dụng để chuyển đổi STRQ thành FEAT. Thuộc tính này hỗ trợ truy nguyên lý do hình thành FEAT và giải thích vì sao FEAT được tách/gộp/làm rõ theo cách hiện tại.

| Giá trị cho phép | Mô tả |
| --- | --- |
| **Phân tách** | Tách một STRQ thành nhiều FEAT nhỏ hơn, dễ quản lý và truy vết hơn. |
| **Làm cho đầy đủ** | Bổ sung phần còn thiếu để FEAT đủ điều kiện đặc tả/triển khai. |
| **Làm rõ** | Làm rõ ý nghĩa mơ hồ, giới hạn phạm vi hoặc điều kiện áp dụng của STRQ. |
| **Thêm chi tiết** | Bổ sung chi tiết nghiệp vụ hoặc chi tiết giải pháp để FEAT khả thi hơn. |
| **Tổng quát hóa** | Trừu tượng hóa yêu cầu để áp dụng cho nhiều trường hợp thay vì một tình huống đơn lẻ. |
| **Kết hợp / Hợp nhất** | Gộp nhiều ý nhỏ hoặc nhiều nguồn yêu cầu thành một FEAT thống nhất. |
| **Hủy bỏ / Sửa lỗi** | Loại bỏ hoặc sửa lại nội dung FEAT/STRQ khi phát hiện mâu thuẫn hoặc sai sót. |

Thuộc tính này cho phép gán **một hoặc nhiều giá trị** cho cùng một FEAT. Nếu sử dụng kỹ thuật biến đổi ngoài danh sách trên, nhóm BA/PM phải ghi chú giải thích rõ trong trường Reason hoặc phần chú thích ma trận FEAT.

---

### 1.5.2. Thuộc tính cho STRQ (Yêu cầu của các bên liên quan)

Tương tự FEAT, **ngoại trừ** không có thuộc tính **Bản phát hành mục tiêu (Target Release)** và **Người phụ trách (Assigned To)** — vì STRQ thuộc miền vấn đề và không được lên lịch trực tiếp vào iteration:

| Thuộc tính | Kiểu dữ liệu | Giá trị cho phép |
| --- | --- | --- |
| Trạng thái (Status) | Liệt kê | Proposed / Approved / Realized / Incorporated / Validated |
| Độ ưu tiên (Priority) | Liệt kê | High / Medium / Low |
| Lợi ích (Benefit) | Liệt kê | Critical / Important / Useful |
| Công sức (Effort) | Số | Ngày-người (person-days) |
| Rủi ro (Risk) | Liệt kê | High / Medium / Low |
| Độ ổn định (Stability) | Liệt kê | High / Medium / Low |
| Lý do (Reason) | Văn bản | Tự do — ghi nhận nguồn gốc nhu cầu (ví dụ: "Phòng TCCB yêu cầu trong buổi phỏng vấn ngày 10/01") |

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.5.1.

---

### 1.5.3. Thuộc tính cho UC (Ca sử dụng)

Tương tự FEAT, **bổ sung thêm** thuộc tính **Tác nhân (Actor)**:

| Thuộc tính | Kiểu dữ liệu | Giá trị cho phép |
| --- | --- | --- |
| Trạng thái (Status) | Liệt kê | Proposed / Approved / Realized / Incorporated / Validated |
| Độ ưu tiên (Priority) | Liệt kê | High / Medium / Low |
| Lợi ích (Benefit) | Liệt kê | Critical / Important / Useful |
| Công sức (Effort) | Số | Ngày-người (person-days) |
| Rủi ro (Risk) | Liệt kê | High / Medium / Low |
| Độ ổn định (Stability) | Liệt kê | High / Medium / Low |
| Bản phát hành mục tiêu (Target Release) | Văn bản | Tên/số iteration |
| Lý do (Reason) | Văn bản | Tự do — tham chiếu tới FEAT nguồn |
| **Tác nhân (Actor)** | Văn bản | Tên tác nhân khởi tạo UC (ví dụ: "Quản trị viên", "Phòng TCCB", "Người dùng", "Hệ thống") |

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.5.1.

---

### 1.5.4. Thuộc tính cho SUPL (Yêu cầu bổ sung)

Tương tự FEAT (không có Assigned To trong tập chuẩn):

| Thuộc tính | Kiểu dữ liệu | Giá trị cho phép |
| --- | --- | --- |
| Trạng thái (Status) | Liệt kê | Proposed / Approved / Realized / Incorporated / Validated |
| Độ ưu tiên (Priority) | Liệt kê | High / Medium / Low |
| Lợi ích (Benefit) | Liệt kê | Critical / Important / Useful |
| Công sức (Effort) | Số | Ngày-người (person-days) |
| Rủi ro (Risk) | Liệt kê | High / Medium / Low |
| Độ ổn định (Stability) | Liệt kê | High / Medium / Low |
| Bản phát hành mục tiêu (Target Release) | Văn bản | Tên/số iteration |
| Lý do (Reason) | Văn bản | Tự do — tham chiếu tới FEAT hoặc STRQ nguồn |

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.5.1.

---

### 1.5.5. Bảng tổng hợp thuộc tính theo kiểu yêu cầu

| Thuộc tính | STRQ | FEAT | UC | SUPL |
| --- | :---: | :---: | :---: | :---: |
| Trạng thái (Status) | ✔ | ✔ | ✔ | ✔ |
| Độ ưu tiên (Priority) | ✔ | ✔ | ✔ | ✔ |
| Lợi ích (Benefit) | ✔ | ✔ | ✔ | ✔ |
| Công sức (Effort) | ✔ | ✔ | ✔ | ✔ |
| Rủi ro (Risk) | ✔ | ✔ | ✔ | ✔ |
| Độ ổn định (Stability) | ✔ | ✔ | ✔ | ✔ |
| Độ khó (Difficulty) | — | ✔ | — | — |
| Bản phát hành mục tiêu (Target Release) | — | ✔ | ✔ | ✔ |
| Người phụ trách (Assigned To) | — | ✔ | — | — |
| Lý do (Reason) | ✔ | ✔ | ✔ | ✔ |
| Kỹ thuật biến đổi (Transformation) | — | ✔ | — | — |
| Tác nhân (Actor) | — | — | ✔ | — |

## 1.6. Báo cáo và chế độ xem

Phần này xác định các báo cáo sẽ được tạo ra để giám sát độ bao phủ và trạng thái của yêu cầu trong suốt vòng đời dự án.

### 1.6.1. Ma trận thuộc tính (Attribute Matrices)

Mỗi kiểu yêu cầu có một ma trận thuộc tính liệt kê toàn bộ yêu cầu thuộc kiểu đó kèm giá trị các thuộc tính:

| Ma trận | Nội dung |
| --- | --- |
| Ma trận thuộc tính STRQ | Tất cả STRQ kèm Status, Priority, Benefit, Effort, Risk, Stability, Reason |
| Ma trận thuộc tính FEAT | Tất cả FEAT kèm Status, Priority, Benefit, Risk, Stability, Difficulty, Effort, Target Release, Assigned To, Reason, Transformation |
| Ma trận thuộc tính UC | Tất cả UC kèm Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason, Actor |
| Ma trận thuộc tính SUPL | Tất cả SUPL kèm Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason |

### 1.6.2. Ma trận truy vết (Traceability Matrices)

Thể hiện ánh xạ giữa các yêu cầu thuộc các kiểu khác nhau:

| Ma trận | Nội dung |
| --- | --- |
| Ma trận STRQ → FEAT | Mỗi STRQ ánh xạ tới (các) FEAT mà nó dẫn xuất |
| Ma trận STRQ → SUPL | Mỗi STRQ ánh xạ tới (các) SUPL phi chức năng/ràng buộc mà nó dẫn xuất trực tiếp |
| Ma trận FEAT → UC | Mỗi FEAT ánh xạ tới (các) UC hiện thực hóa tính năng đó |
| Ma trận FEAT → SUPL | Mỗi FEAT ánh xạ tới (các) SUPL hỗ trợ tính năng đó |
| Ma trận UC → Design | Mỗi UC ánh xạ tới (các) artefact thiết kế tương ứng; trong baseline hiện tại neo chính là `class-diagram.md` |



# II. PHỎNG VẤN BÊN LIÊN QUAN

## 2.1. Bảng phân công thành viên

| Thành viên | STRQs | FEATs |
|---|---|---|
| Nguyễn Hồng Phúc | 1–3 | 1.1–3.5 (15) |
| Nguyễn Hải Ninh | 4–6 | 4.1–6.2 (11) |
| Ngô Quang Tùng | 7–8 | 7.1–8.9 (13) |
| Ngô Đức Nam Khánh | 9–12 | 9.1–12.4 (14) |

## 2.2. Nội dung tổng hợp STRQ và FEAT theo thành viên

### 2.2.1. Phần đóng góp của Nguyễn Hồng Phúc (STRQ 1–3)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | * Phân tách * Làm cho đầy đủ * Tổng quát hóa * Thêm chi tiết | * **FEAT 1.1:** Hệ thống cho phép người dùng đăng nhập bằng tài khoản. * **FEAT 1.2:** Hệ thống cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng. * **FEAT 1.3:** Hệ thống tự động đăng xuất khỏi phiên làm việc nếu người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web trong 30 phút. * **FEAT 1.4:** Hệ thống cho phép người dùng đổi mật khẩu tài khoản đang sử dụng; mọi mật khẩu được thiết lập mới phải được lưu trữ dưới dạng không thể khôi phục nguyên văn và không được lưu ở dạng văn bản thuần. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 2.1:** Hệ thống cho phép quản trị viên tìm kiếm tài khoản người dùng. * **FEAT 2.2:** Hệ thống cho phép quản trị viên thêm mới tài khoản người dùng. * **FEAT 2.3:** Hệ thống cho phép quản trị viên sửa tài khoản người dùng. * **FEAT 2.4:** Hệ thống cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống theo các vai trò chức năng được định nghĩa sẵn: Quản trị viên, Phòng TCCB, Phòng TCKT, Người dùng (Cán bộ/Giảng viên/Nhân viên). * **FEAT 2.5:** Hệ thống cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Khóa/Mở khóa). * **FEAT 2.6:** Hệ thống tự động khóa tài khoản của nhân sự đã được đánh dấu thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 3.1:** Hệ thống cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi. * **FEAT 3.2:** Hệ thống cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự. * **FEAT 3.3:** Hệ thống cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự. * **FEAT 3.4:** Hệ thống cho phép quản trị viên và phòng TCCB thay đổi trạng thái của đơn vị tổ chức nhân sự (Trạng thái: Giải thể/Sáp nhập). * **FEAT 3.5:** Hệ thống cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. |

> **Ghi chú thiết kế – FEAT 2.4:** "Nhóm nghiệp vụ" trong FEAT 2.4 chỉ các vai trò chức năng được hệ thống định nghĩa sẵn, tương ứng với phân nhóm tác nhân: Quản trị viên, Phòng TCCB, Phòng TCKT, Người dùng (Cán bộ/Giảng viên/Nhân viên). Mỗi nhóm nghiệp vụ quy định tập quyền truy cập các chức năng hệ thống khác nhau.

> **Ghi chú thiết kế – FEAT 1.5:** FEAT 1.5 là feature mức giải pháp mô tả hình thức cung cấp hệ thống dưới dạng ứng dụng web nhiều người dùng. FEAT này được hiện thực hóa bởi SUPL-DC01 nên không tách thành UC riêng.

### 2.2.2. Phần đóng góp của Nguyễn Hải Ninh (STRQ 4–6)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 4:** Phòng TCCB có thể cấu hình lương, loại phụ cấp, loại hợp đồng. | * Phân tách * Làm cho đầy đủ | * **FEAT 4.1:** Hệ thống cho phép phòng TCCB thêm mới hệ số lương (Hệ số lương được thêm sẽ được dùng làm thông tin cho hồ sơ). * **FEAT 4.2:** Hệ thống cho phép phòng TCCB sửa thông tin đối với hệ số lương chưa được hồ sơ nào sử dụng, phục vụ sửa chữa nhập liệu lỗi. * **FEAT 4.3:** Hệ thống cho phép phòng TCCB xóa hệ số lương khi không được hồ sơ nào sử dụng, hoặc thay đổi trạng thái (đưa vào trạng thái ngừng sử dụng hoặc kích hoạt lại) nếu đã được sử dụng. * **FEAT 4.4:** Hệ thống cho phép phòng TCCB thêm mới, sửa và thay đổi trạng thái danh mục loại phụ cấp theo bộ danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt; các mục đã được tham chiếu trong dữ liệu nghiệp vụ không được xóa mà chỉ được chuyển giữa trạng thái "Đang sử dụng" và "Ngừng sử dụng". * **FEAT 4.5:** Hệ thống cho phép phòng TCCB thêm mới, sửa và thay đổi trạng thái danh mục loại hợp đồng theo bộ danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt; các mục đã được tham chiếu trong dữ liệu nghiệp vụ không được xóa mà chỉ được chuyển giữa trạng thái "Đang sử dụng" và "Ngừng sử dụng". |

> **Ghi chú thiết kế – FEAT 4.4/4.5:** Đối với danh mục loại phụ cấp và loại hợp đồng, hệ thống cho phép thêm mới, sửa và thay đổi trạng thái theo bộ danh mục nhân sự được phê duyệt. Các mục đã từng được tham chiếu trong dữ liệu nghiệp vụ không được xóa mà chỉ được chuyển giữa "Đang sử dụng" và "Ngừng sử dụng" để bảo toàn dữ liệu lịch sử và phục vụ kiểm toán.

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 5:** Phòng TCKT và TCCB muốn thống kê chi tiết về nhân sự. | * Phân tách * Thêm chi tiết | * **FEAT 5.1:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê tổng quan nhân sự và biến động nhân sự. * **FEAT 5.2:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh. * **FEAT 5.3:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê hợp đồng, tình trạng làm việc, đánh giá cán bộ. * **FEAT 5.4:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê đào tạo, phát triển, bổ nhiệm nhân sự. |
| **STRQ 6:** Hệ thống yêu cầu tự động log dấu vết hoạt động người dùng (System Logging). | * Phân tách * Thêm chi tiết | * **FEAT 6.1:** Hệ thống tự động ghi vết tất cả các tác vụ truy cập tài khoản, thay đổi/cập nhật hệ thống hoặc dữ liệu. * **FEAT 6.2:** Hệ thống cho phép quản trị viên truy xuất xem và xuất Audit log (Nhật ký hệ thống) nhằm truy vết hoạt động. |

### 2.2.3. Phần đóng góp của Ngô Quang Tùng (STRQ 7–8)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 7:** Phòng TCCB có thể tạo hợp đồng lao động của nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 7.1:** Hệ thống cho phép phòng TCCB tạo hợp đồng cho nhân sự không có hợp đồng hoặc cần gia hạn hợp đồng. * **FEAT 7.2:** Hệ thống cho phép phòng TCCB xem danh sách và chi tiết hợp đồng lao động của nhân sự. * **FEAT 7.3:** Hệ thống cho phép phòng TCCB chỉnh sửa hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực. * **FEAT 7.4:** Hệ thống cho phép phòng TCCB chấm dứt hợp đồng lao động trước hạn của nhân sự. |
| **STRQ 8:** Phòng TCCB muốn quản lý hồ sơ nhân sự như thêm, sửa hồ sơ và cho phép đánh dấu thôi việc nếu nhân sự không còn làm việc, có thêm phương pháp tìm kiếm và lọc để tiện quản lý. | * Phân tách * Làm rõ * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 8.1:** Hệ thống cho phép phòng TCCB và phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa. * **FEAT 8.2:** Hệ thống cho phép phòng TCCB và phòng TCKT lọc đa tiêu chí hồ sơ nhân sự. * **FEAT 8.3:** Hệ thống cho phép phòng TCCB thêm mới hồ sơ nhân sự (gồm nhập tay hoặc upload từ Excel) và tự động cấp mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng tại thời điểm tạo hồ sơ. * **FEAT 8.4:** Hệ thống cho phép phòng TCCB chỉnh sửa hồ sơ nhân sự (thông tin cá nhân, trình độ học vấn, khen thưởng/kỷ luật, quá trình công tác, thông tin hợp đồng). * **FEAT 8.5:** Hệ thống cho phép phòng TCCB đánh dấu thôi việc nhân sự. * **FEAT 8.6:** Hệ thống tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. * **FEAT 8.7:** Hệ thống cho phép phòng TCCB và phòng TCKT xem chi tiết hồ sơ nhân sự theo từng chế độ xem. * **FEAT 8.8:** Hệ thống cho phép phòng TCCB và phòng TCKT in hoặc xuất Excel hồ sơ nhân sự. * **FEAT 8.9:** Hệ thống cho phép phòng TCCB cấu hình ẩn/hiện các mục khen thưởng, kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc phòng TCCB. |

### 2.2.4. Phần đóng góp của Ngô Đức Nam Khánh (STRQ 9–12)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 9:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 9.1:** Hệ thống cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự. * **FEAT 9.2:** Hệ thống cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác. * **FEAT 9.3:** Hệ thống cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 10:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 10.1:** Hệ thống cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật). * **FEAT 10.2:** Hệ thống cho phép phòng TCCB xem lịch sử đánh giá khen thưởng và kỷ luật của nhân sự. * **FEAT 10.3:** Hệ thống cho phép phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo nhân sự, loại đánh giá, hoặc khoảng thời gian. |
| **STRQ 11:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 11.1:** Hệ thống cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ. * **FEAT 11.2:** Hệ thống cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành); khi khóa đào tạo được chuyển sang trạng thái "Đang đào tạo", hệ thống phải tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang "Đang học". * **FEAT 11.3:** Hệ thống cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký. * **FEAT 11.4:** Hệ thống cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
| **STRQ 12:** Người dùng phần mềm có thể xem hồ sơ cá nhân, xem thông tin đơn vị đang công tác và thực hiện các luồng tác vụ cá nhân. | * Phân tách * Làm rõ * Thêm chi tiết | * **FEAT 12.1:** Hệ thống cho phép người dùng xem thông tin cá nhân của bản thân. * **FEAT 12.2:** Hệ thống cho phép người dùng xem thông tin đơn vị mình đang công tác và cơ cấu các thành phần đơn vị trực thuộc. * **FEAT 12.3:** Hệ thống cho phép người dùng đăng ký hoặc hủy đăng ký tham gia khóa học/đào tạo được nhà trường phê duyệt mở. * **FEAT 12.4:** Hệ thống cho phép người dùng xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. |

> **Ghi chú thiết kế – FEAT 12.3/12.4:** "Luồng tác vụ cá nhân" trong STRQ 12 được giới hạn phạm vi ở đăng ký đào tạo trong phiên bản hiện tại. Các tác vụ cá nhân khác (ví dụ: yêu cầu cập nhật thông tin, đề xuất nghỉ phép) có thể được bổ sung trong các phiên bản sau nếu có yêu cầu từ stakeholder.

# III. MÔ HÌNH HOÁ YÊU CẦU

## 3.1. Xác định các Tác nhân (Actors)

Dựa vào các yêu cầu thu thập (STRQ và FEAT), phân tích xác định được các tác nhân (Actors) tham gia vào hệ thống như sau:

1. **Người dùng (Cán bộ / Giảng viên / Nhân viên)**: Là tác nhân sử dụng các chức năng tự phục vụ trong hệ thống như đăng ký học, đổi mật khẩu, xem hồ sơ, xem thông tin đơn vị.
2. **Quản trị viên (Admin)**: Là tác nhân đảm nhiệm quản trị kỹ thuật của hệ thống, thực hiện quản lý tài khoản người dùng, phân quyền truy cập, thiết lập cơ cấu đơn vị tổ chức nhà trường và xem giám sát nhật ký (Audit Log).
3. **Phòng Tổ chức - Cán bộ (TCCB)**: Là tác nhân thực hiện các nghiệp vụ quản lý lõi của hệ thống bao gồm quản lý hồ sơ nhân sự, hợp đồng lao động, bổ nhiệm/điều chuyển, đánh giá khen thưởng/kỷ luật, thiết lập và đánh giá đào tạo, kết hợp việc thiết lập các cấu hình tham chiếu (lương, phụ cấp, hợp đồng).
4. **Phòng Tài chính - Kế toán (TCKT)**: Là tác nhân có nhu cầu tra cứu thông tin nhân sự và xuất các báo cáo, thống kê liên quan đến cơ cấu và biến động nhân sự, hợp đồng, đào tạo.
5. **Hệ thống (System Timer / Auto-Job)**: Tác nhân hệ thống tự động chạy ngầm thực hiện các quy trình động như tự động đăng xuất, tạo mã, khóa tài khoản tự động, đánh dấu hết hiệu lực.

## 3.2. Xác định các Use Case (UCs)

Từ các FEAT đã được phân tách và xác định, chi tiết thành các Use Case (UC) chính cho hệ thống:

> **Ghi chú:** Tổng cộng hệ thống bao gồm **50 Use Case** (UC 4.1 – UC 4.50), được phân nhóm theo chức năng như sau:

**► Nhóm UC Hệ thống & Tài khoản:**

* UC Đăng nhập
* UC Đăng xuất
* UC Đổi mật khẩu
* UC Quản lý tài khoản (Tìm kiếm, Thêm, Sửa, Đổi trạng thái khóa/mở)
* UC Phân quyền tài khoản
* UC Xem nhật ký hệ thống (Audit Log)

**► Nhóm UC Quản lý Cơ cấu tổ chức:**

* UC Quản lý đơn vị tổ chức (Thêm mới đơn vị, Sửa thông tin, Cập nhật trạng thái giải thể/sáp nhập, Xem chi tiết đơn vị)
* UC Điều chuyển nhân sự (Bổ nhiệm nhân sự vào đơn vị, Điều chuyển nhân sự sang đơn vị khác, Bãi nhiệm nhân sự khỏi đơn vị)

**► Nhóm UC Danh mục Cấu hình:**

* UC Quản lý danh mục Hệ số lương (Thêm mới, Sửa, Xóa, Thay đổi trạng thái)
* UC Quản lý danh mục Loại phụ cấp (Thêm mới, Sửa, Thay đổi trạng thái)
* UC Quản lý danh mục Loại hợp đồng (Thêm mới, Sửa, Thay đổi trạng thái)

**► Nhóm UC Quản lý Hồ sơ & Nhân sự:**

* UC Tìm kiếm hồ sơ nhân sự
* UC Lọc danh sách hồ sơ nhân sự
* UC Thêm mới Hồ sơ nhân sự
* UC Chỉnh sửa trong chi tiết hồ sơ nhân sự
* UC Xem Chi tiết thông tin hồ sơ nhân sự
* UC In và xuất Excel hồ sơ nhân sự
* UC Đánh dấu thôi việc nhân sự
* UC Thôi việc nhân sự tự động
* UC Thêm mới Hợp đồng lao động
* UC Ghi nhận đánh giá khen thưởng/kỷ luật nhân sự
* UC Xem danh sách và chi tiết hợp đồng lao động
* UC Chỉnh sửa hợp đồng lao động chưa có hiệu lực
* UC Chấm dứt hợp đồng lao động trước hạn
* UC Xem lịch sử đánh giá khen thưởng/kỷ luật
* UC Tìm kiếm và lọc danh sách đánh giá
* UC Cấu hình ẩn/hiện mục khen thưởng/kỷ luật

**► Nhóm UC Quản lý Đào tạo:**

* UC Mở khóa đào tạo cho cán bộ giảng viên
* UC Sửa thông tin khóa đào tạo đã mở
* UC Xem chi tiết thông tin khóa đào tạo đã mở
* UC Ghi nhận kết quả đào tạo cho cán bộ giảng viên

**► Nhóm UC Cá nhân (Self-service):**

* UC Xem thông tin trong hồ sơ cá nhân
* UC Xem thông tin chi tiết đơn vị đang công tác
* UC Thay đổi trạng thái đăng ký khóa đào tạo
* UC Xem danh sách các khóa đào tạo đã đăng ký

**► Nhóm UC Báo cáo & Thống kê:**

* UC Xem chi tiết các thống kê nhân sự và báo cáo

## 3.3. Vẽ biểu đồ UCs (UC tổng quát, UC phân rã theo các tác nhân)

### 3.3.1. Biểu đồ Use Case tổng quát (Nguyễn Hồng Phúc)

> **Ghi chú quan hệ giữa các UC:** UC 4.5 (Thêm tài khoản) và UC 4.6 (Sửa tài khoản) **<<include>>** UC 4.7 (Phân quyền) để thực hiện phân quyền vai trò cho tài khoản trong cùng luồng tạo/sửa.

### 3.3.2. Biểu đồ Use Case phân rã theo tác nhân

**a. Phân rã cho Quản trị viên (Admin)**

* **Tác nhân**: Quản trị viên
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Quản lý tài khoản người dùng
  + Phân quyền tài khoản
  + Thay đổi trạng thái tài khoản
  + Nhóm UC Quản lý Đơn vị tổ chức
  + Xem nhật ký hệ thống (Audit Log)
  + Nhóm UC Cá nhân (Self-service): Xem hồ sơ cá nhân, Xem đơn vị công tác, Thay đổi trạng thái đăng ký đào tạo, Xem khóa đào tạo đã đăng ký *(kế thừa quyền Người dùng)*

**b. Phân rã cho Phòng Tổ chức - Cán bộ**

* **Tác nhân**: Phòng Tổ chức - Cán bộ
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Nhóm UC Quản lý hồ sơ nhân sự (Thêm/Sửa/Đánh dấu thôi việc/Lọc tìm)
  + Nhóm UC Quản lý hợp đồng (Thêm/Xem/Sửa/Chấm dứt)
  + Điều chuyển nhân sự (Bổ nhiệm/Điều chuyển/Bãi nhiệm)
  + Nhóm UC Đánh giá (Ghi nhận/Xem lịch sử/Tìm kiếm lọc)
  + Cấu hình ẩn/hiện khen thưởng/kỷ luật trong hồ sơ
  + Nhóm UC Quản lý khóa đào tạo & kết quả
  + Nhóm UC Cấu hình danh mục (lương, phụ cấp, HD)
  + Nhóm UC Quản lý Đơn vị tổ chức (Thêm mới, Sửa thông tin, Thay đổi trạng thái, Xem chi tiết)
  + Xem báo cáo thống kê
  + Nhóm UC Cá nhân (Self-service): Xem hồ sơ cá nhân, Xem đơn vị công tác, Thay đổi trạng thái đăng ký đào tạo, Xem khóa đào tạo đã đăng ký *(kế thừa quyền Người dùng)*

**c. Phân rã cho Phòng Tài chính - Kế toán**

* **Tác nhân**: Phòng Tài chính - Kế toán
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Chế độ xem: Tìm kiếm, Xem và Lọc chi tiết hồ sơ nhân sự
  + Xem chi tiết các thống kê
  + Nhóm UC Cá nhân (Self-service): Xem hồ sơ cá nhân, Xem đơn vị công tác, Thay đổi trạng thái đăng ký đào tạo, Xem khóa đào tạo đã đăng ký *(kế thừa quyền Người dùng)*

**d. Phân rã cho Người dùng (Cán bộ/Giảng viên/Nhân viên)**

* **Tác nhân**: Người dùng
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Xem hồ sơ cá nhân
  + Xem thông tin chi tiết đơn vị công tác
  + Thay đổi trạng thái đăng ký đào tạo
  + Xem danh sách các khóa đào tạo đã đăng ký

### 3.3.3. Bảng phân công thành viên cho Use Case

| Thành viên | UCs |
|---|---|
| Nguyễn Hồng Phúc | 4.1–4.12 (12) |
| Nguyễn Hải Ninh | 4.13–4.24 (12) |
| Ngô Quang Tùng | 4.25–4.37 (13) |
| Ngô Đức Nam Khánh | 4.38–4.50 (13) |

### 3.3.4. Danh mục Use Case đã đánh số lại

- UC 4.1: Đăng nhập
- UC 4.2: Đăng xuất
- UC 4.3: Đổi mật khẩu
- UC 4.4: Tìm kiếm tài khoản người dùng
- UC 4.5: Thêm mới tài khoản người dùng
- UC 4.6: Sửa thông tin tài khoản người dùng
- UC 4.7: Phân quyền tài khoản người dùng
- UC 4.8: Thay đổi trạng thái cho tài khoản người dùng
- UC 4.9: Tạo mới đơn vị tổ chức nhân sự
- UC 4.10: Sửa thông tin đơn vị tổ chức nhân sự
- UC 4.11: Cập nhật trạng thái cho đơn vị tổ chức nhân sự
- UC 4.12: Xem chi tiết thông tin đơn vị tổ chức nhân sự
- UC 4.13: Thêm mới danh mục hệ số lương
- UC 4.14: Sửa danh mục hệ số lương
- UC 4.15: Xóa danh mục hệ số lương
- UC 4.16: Thay đổi trạng thái danh mục hệ số lương
- UC 4.17: Thêm mới danh mục loại phụ cấp
- UC 4.18: Sửa danh mục loại phụ cấp
- UC 4.19: Thay đổi trạng thái danh mục loại phụ cấp
- UC 4.20: Thêm mới danh mục loại hợp đồng
- UC 4.21: Sửa danh mục loại hợp đồng
- UC 4.22: Thay đổi trạng thái danh mục loại hợp đồng
- UC 4.23: Xem chi tiết các thống kê
- UC 4.24: Xem nhật ký hệ thống (Audit Log)
- UC 4.25: Thêm mới Hợp đồng lao động
- UC 4.26: Xem danh sách và chi tiết hợp đồng lao động
- UC 4.27: Chỉnh sửa hợp đồng lao động chưa có hiệu lực
- UC 4.28: Chấm dứt hợp đồng lao động trước hạn
- UC 4.29: Tìm kiếm hồ sơ nhân sự
- UC 4.30: Lọc danh sách hồ sơ nhân sự
- UC 4.31: Thêm mới Hồ sơ nhân sự
- UC 4.32: Chỉnh sửa trong chi tiết hồ sơ nhân sự
- UC 4.33: Đánh dấu thôi việc nhân sự
- UC 4.34: Thôi việc nhân sự tự động
- UC 4.35: Xem Chi tiết thông tin hồ sơ nhân sự
- UC 4.36: In và xuất Excel hồ sơ nhân sự
- UC 4.37: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật
- UC 4.38: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự
- UC 4.39: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự
- UC 4.40: Ghi nhận đánh giá cho nhân sự
- UC 4.41: Xem lịch sử đánh giá khen thưởng/kỷ luật
- UC 4.42: Tìm kiếm và lọc danh sách đánh giá
- UC 4.43: Mở khóa đào tạo cho cán bộ giảng viên
- UC 4.44: Sửa thông tin khóa đào tạo đã mở
- UC 4.45: Xem chi tiết thông tin khóa đào tạo đã mở
- UC 4.46: Ghi nhận kết quả đào tạo của cán bộ giảng viên
- UC 4.47: Xem các thông tin trong hồ sơ cá nhân của nhân sự
- UC 4.48: Xem thông tin chi tiết đơn vị đang công tác
- UC 4.49: Thay đổi trạng thái đăng ký khóa đào tạo
- UC 4.50: Xem danh sách các khóa đào tạo đã đăng ký

## 3.4. Ma trận truy vết yêu cầu (Traceability Matrix)

| FEAT | UC tương ứng |
|------|-------------|
| FEAT 1.1 | UC 4.1 (Đăng nhập) |
| FEAT 1.2 | UC 4.2 (Đăng xuất) |
| FEAT 1.3 | UC 4.2 A1 (Đăng xuất tự động) |
| FEAT 1.4 | UC 4.3 (Đổi mật khẩu) |
| FEAT 2.1 | UC 4.4 (Tìm kiếm tài khoản người dùng) |
| FEAT 2.2 | UC 4.5 (Thêm mới tài khoản người dùng) |
| FEAT 2.3 | UC 4.6 (Sửa thông tin tài khoản người dùng) |
| FEAT 2.4 | UC 4.7 (Phân quyền tài khoản người dùng) |
| FEAT 2.5 | UC 4.8 (Thay đổi trạng thái cho tài khoản người dùng) |
| FEAT 2.6 | UC 4.8 A2 (Tự động khóa tài khoản) |
| FEAT 3.1 | UC 4.9 (Tạo mới đơn vị tổ chức nhân sự) — cấu trúc cây |
| FEAT 3.2 | UC 4.9 (Tạo mới đơn vị tổ chức nhân sự) |
| FEAT 3.3 | UC 4.10 (Sửa thông tin đơn vị tổ chức nhân sự) |
| FEAT 3.4 | UC 4.11 (Cập nhật trạng thái cho đơn vị tổ chức nhân sự) |
| FEAT 3.5 | UC 4.12 (Xem chi tiết thông tin đơn vị tổ chức nhân sự) |
| FEAT 4.1 | UC 4.13 (Thêm mới danh mục hệ số lương) |
| FEAT 4.2 | UC 4.14 (Sửa danh mục hệ số lương) |
| FEAT 4.3 | UC 4.15 (Xóa danh mục hệ số lương), UC 4.16 (Thay đổi trạng thái danh mục hệ số lương) |
| FEAT 4.4 | UC 4.17 (Thêm mới danh mục loại phụ cấp), UC 4.18 (Sửa danh mục loại phụ cấp), UC 4.19 (Thay đổi trạng thái danh mục loại phụ cấp) |
| FEAT 4.5 | UC 4.20 (Thêm mới danh mục loại hợp đồng), UC 4.21 (Sửa danh mục loại hợp đồng), UC 4.22 (Thay đổi trạng thái danh mục loại hợp đồng) |
| FEAT 5.1 | UC 4.23 (Thống kê tổng quan nhân sự và biến động nhân sự) |
| FEAT 5.2 | UC 4.23 (Cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh) |
| FEAT 5.3 | UC 4.23 (Hợp đồng, tình trạng làm việc, đánh giá cán bộ) |
| FEAT 5.4 | UC 4.23 (Đào tạo, phát triển, bổ nhiệm nhân sự) |
| FEAT 6.1 | SUPL Ghi nhật ký (auto logging) |
| FEAT 6.2 | UC 4.24 (Xem nhật ký hệ thống — Audit Log) — truy xuất |
| FEAT 7.1 | UC 4.25 (Thêm mới Hợp đồng lao động) |
| FEAT 7.2 | UC 4.26 (Xem danh sách và chi tiết hợp đồng lao động) |
| FEAT 7.3 | UC 4.27 (Chỉnh sửa hợp đồng lao động chưa có hiệu lực) |
| FEAT 7.4 | UC 4.28 (Chấm dứt hợp đồng lao động trước hạn) |
| FEAT 8.1 | UC 4.29 (Tìm kiếm hồ sơ nhân sự) |
| FEAT 8.2 | UC 4.30 (Lọc danh sách hồ sơ nhân sự) |
| FEAT 8.3 | UC 4.31 (Thêm mới Hồ sơ nhân sự) |
| FEAT 8.4 | UC 4.32 (Chỉnh sửa trong chi tiết hồ sơ nhân sự) |
| FEAT 8.5 | UC 4.33 (Đánh dấu thôi việc nhân sự) |
| FEAT 8.6 | UC 4.34 (Thôi việc nhân sự tự động) |
| FEAT 8.7 | UC 4.35 (Xem Chi tiết thông tin hồ sơ nhân sự) |
| FEAT 8.8 | UC 4.36 (In và xuất Excel hồ sơ nhân sự) |
| FEAT 8.9 | UC 4.37 (Cấu hình ẩn/hiện mục khen thưởng/kỷ luật) |
| FEAT 9.1 | UC 4.38 (Bổ nhiệm nhân sự vào đơn vị tổ chức nhân sự) |
| FEAT 9.2 | UC 4.38 (Điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác) |
| FEAT 9.3 | UC 4.39 (Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự) |
| FEAT 10.1 | UC 4.40 (Ghi nhận đánh giá cho nhân sự) |
| FEAT 10.2 | UC 4.41 (Xem lịch sử đánh giá khen thưởng/kỷ luật) |
| FEAT 10.3 | UC 4.42 (Tìm kiếm và lọc danh sách đánh giá) |
| FEAT 11.1 | UC 4.43 (Mở khóa đào tạo cho cán bộ giảng viên) |
| FEAT 11.2 | UC 4.44 (Sửa thông tin khóa đào tạo đã mở) |
| FEAT 11.3 | UC 4.45 (Xem chi tiết thông tin khóa đào tạo đã mở) |
| FEAT 11.4 | UC 4.46 (Ghi nhận kết quả đào tạo của cán bộ giảng viên) |
| FEAT 12.1 | UC 4.47 (Xem các thông tin trong hồ sơ cá nhân của nhân sự) |
| FEAT 12.2 | UC 4.48 (Xem thông tin chi tiết đơn vị đang công tác) |
| FEAT 12.3 | UC 4.49 (Thay đổi trạng thái đăng ký khóa đào tạo) |
| FEAT 12.4 | UC 4.50 (Xem danh sách các khóa đào tạo đã đăng ký) |

# IV. ĐẶC TẢ CA SỬ DỤNG

## 4.1 Phần đóng góp của Nguyễn Hồng Phúc (UC 4.1–4.12)

### 4.1. Use Case: Đăng nhập (Nguyễn Hồng Phúc)

|  |  |
| --- | --- |
| **Tên use case** | **Đăng nhập** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng xác thực và truy cập vào hệ thống dựa trên thông tin tài khoản được cấp. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Ấn “Đăng nhập” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã được cấp tài khoản.  Hệ thống đang hoạt động bình thường. |
| Điều kiện thành công  (Post-condition) | Người dùng được chuyển đến trang chủ (Dashboard) tương ứng với vai trò của mình. |
| Điều kiện thất bại | Tác nhân đăng nhập vào tài khoản thất bại |
| Luồng sự kiện chính  (Basic Flow) | 1.  Người dùng truy cập vào địa chỉ web của hệ thống.  2.  Hệ thống hiển thị màn hình Đăng nhập.  3.  Người dùng nhập `Tên đăng nhập` (Mã nhân viên) và `Mật khẩu`.  4.  Người dùng nhấn nút "Đăng nhập".  5.  Hệ thống kiểm tra tính hợp lệ của dữ liệu nhập (không được để trống).  6.  Hệ thống xác thực thông tin tài khoản với cơ sở dữ liệu.  7.  Hệ thống kiểm tra trạng thái tài khoản (Active/ Lock).  8.  Hệ thống xác định vai trò của người dùng.  9.  Hệ thống chuyển hướng người dùng đến Dashboard tương ứng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Đăng nhập khi đã có session**   1. Tại bước 1, Người dùng truy cập trang đăng nhập khi đã có session hợp lệ, 2. Hệ thống tự động chuyển hướng vào Dashboard. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Sai Tên đăng nhập hoặc Mật khẩu**   1. Tại bước 6, hệ thống kiểm tra thông tin không khớp. 2. Hệ thống hiển thị thông báo "Tên đăng nhập hoặc mật khẩu không đúng". 3. Quay về bước 3   **E2: Tài khoản bị khóa**   1. Tại bước 7, nếu tài khoản bị khóa, 2. Hệ thống hiển thị thông báo "Tài khoản của bạn đã bị khóa. Vui lòng liên hệ Quản trị viên".   **E3: Không hợp lệ Tên đăng nhập hoặc Mật khẩu**   1. Tại bước 5, hệ thống kiểm tra không hợp lệ 2. Hệ thống hiển thị thông báo “Vui lòng nhập tên đăng nhập và mật khẩu hợp lệ” 3. Quay lại bước 3 |

### 4.2. Use Case: Đăng xuất

|  |  |
| --- | --- |
| **Tên use case** | **Đăng xuất** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự, Hệ thống |
| Mục đích (mô tả) | Cho phép người dùng thoát khỏi phiên làm việc hiện tại một cách an toàn. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Ấn “Đăng xuất” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đang trong phiên đăng nhập hợp lệ. |
| Điều kiện thành công  (Post-condition) | Phiên làm việc bị hủy bỏ.  Người dùng được chuyển về màn hình Đăng nhập. |
| Điều kiện thất bại | Không có |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng chọn "Đăng xuất".  2. Hệ thống yêu cầu xác nhận đăng xuất  3. Người dùng xác nhận đăng xuất.  4. Hệ thống hủy session hiện tại.  5. Hệ thống chuyển hướng về trang Đăng nhập. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Đăng xuất tự động**  1.  Hệ thống giám sát việc người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web.  2.  Nếu người dùng không có tương tác giao diện với trang web trong **30 phút**  3.  Hệ thống tự động hủy session.  4.  Hệ thống hiển thị thông báo "Phiên làm việc đã hết hạn" và chuyển về trang Đăng nhập. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.3. Use Case: Đổi mật khẩu

|  |  |
| --- | --- |
| **Tên use case** | **Đổi mật khẩu** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng đã đăng nhập thay đổi mật khẩu hiện tại sang một mật khẩu mới để tăng cường bảo mật. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Ấn “Đổi mật khẩu” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đang đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Mật khẩu được đổi thành công |
| Điều kiện thất bại | Đổi mật khẩu thất bại |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng chọn "Đổi mật khẩu".  2. Hệ thống hiển thị các trường thông tin: Mật khẩu cũ, mật khẩu mới, xác nhận mật khẩu mới  3. Người dùng nhập dữ liệu.  4. Hệ thống yêu cầu xác nhận.  5. Người dùng xác nhận đổi mật khẩu.  6. Hệ thống kiểm tra dữ liệu  -  Kiểm tra "Mật khẩu hiện tại" có khớp với mật khẩu trong CSDL không.  -  Kiểm tra "Mật khẩu mới" có đúng quy tắc bảo mật (Độ dài, ký tự đặc biệt) không.  -   Kiểm tra "Mật khẩu mới" và "Xác nhận mật khẩu" có khớp nhau không.  -   Kiểm tra "Mật khẩu mới" có khác "Mật khẩu hiện tại" không.  7. Hệ thống cập nhật mật khẩu, lưu lịch sử thay đổi và thông báo đổi mật khẩu thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Sai thông tin trường dữ liệu**  1.  Tại bước 6, hệ thống phát hiện các lỗi tại các trường thông tin  2.  Hệ thống thông báo lỗi  3. Hệ thống từ chối lưu dữ liệu.  **E2: Hủy thao tác**   1. Tại bước 2, người dùng nhấn “Hủy” 2. Hệ thống quay lại màn hình chính. |

### 4.4. Use Case: Tìm kiếm tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên tìm kiếm tài khoản người dùng |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên nhập từ khóa tìm kiếm và thực hiện tìm kiếm trong menu “Quản lý tài khoản người dùng” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách tài khoản người dùng thỏa điều kiện tìm kiếm được hiển thị. |
| Điều kiện thất bại | Hệ thống không xử lý được yêu cầu tìm kiếm |
| Luồng sự kiện chính  (Basic Flow) | 1.  Quản trị viên chọn menu "Quản lý tài khoản người dùng".  2.  Hệ thống hiển thị danh sách người dùng (phân trang).  3.  Quản trị viên nhập từ khóa vào ô tìm kiếm (Mã nhân sự, Họ tên, Email).  4. Quản trị viên chọn lọc các thông tin theo dropdown:  - **Vai trò**: Tất cả (Mặc định), Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự  - **Trạng thái**: Tất cả, Hoạt động (Mặc định), Không hoạt động  5.  Quản trị viên nhấn nút tìm kiếm.  6.  Hệ thống lọc và hiển thị danh sách kết quả tương ứng bao gồm các cột:  - STT  - Mã nhân sự  - Họ tên  - Email  - Vai trò  - Trạng thái |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không nhập từ khóa**   1. Tại bước 3, Quản trị viên không nhập từ khóa 2. Hệ thống hiển thị toàn bộ danh sách người dùng |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không tìm thấy kết quả**   1. Tại bước 6, Hệ thống không tìm thấy người dùng phù hợp 2. Hệ thống hiển thị thông báo “Không có người dùng” |

### 4.5. Use Case: Thêm mới tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên thêm mới tài khoản người dùng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên nhấn nút “Thêm mới người dùng”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Tài khoản người dùng mới được tạo và lưu trong cơ sở dữ liệu. |
| Điều kiện thất bại | Tài khoản người dùng không được tạo do dữ liệu không hợp lệ hoặc trùng lặp |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Quản trị viên nhấn nút "Thêm mới".  2.  Hệ thống hiển thị form thêm người dùng.  3.  Quản trị viên nhập thông tin: Email, Nhân sự, Vai trò (UC 4.7).  4.  Quản trị viên nhấn "Lưu".  5.  Hệ thống validate dữ liệu (Đầy đủ các trường thông tin, Email đúng định dạng và duy nhất, Nhân sự tồn tại và chưa có tài khoản liên kết, Vai trò tồn tại)  6. Hệ thống tự động tạo mật khẩu ngẫu nhiên và gửi mật khẩu đã tạo cho email tương ứng.  7.  Hệ thống lưu thông tin.  8.  Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện các trường thông tin không hợp lệ. 2. Hệ thống thông báo lỗi tương ứng 3. Dữ liệu không được lưu   **E2: Quản trị viên hủy thao tác**   1. Tại bước 2, Quản trị viên nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách người dùng |

### 4.6. Use Case: Sửa thông tin tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên cập nhật thông tin tài khoản người dùng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên chọn một tài khoản và nhấn nút “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống.  Tài khoản cần chỉnh sửa đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin tài khoản người dùng được cập nhật trong cơ sở dữ liệu. |
| Điều kiện thất bại | Không có thay đổi nào được lưu vào hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại danh sách, Quản trị viên nhấn "Sửa" trên một dòng user.  2.  Hệ thống hiển thị form cập nhật.  3.  Quản trị viên thay đổi Email, Vai trò (UC 4.7).  4.  Quản trị viên nhấn "Lưu".  5.  Hệ thống validate dữ liệu (Đầy đủ các trường thông tin, Email đúng định dạng và duy nhất, Vai trò tồn tại).  6.  Hệ thống lưu thay đổi.  7.  Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện trường dữ liệu không hợp lệ. 2. Hệ thống thông báo lỗi 3. Dữ liệu không được lưu   **E2: Quản trị viên** **hủy thao tác**   1. Tại bước 2, Quản trị viên nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách người dùng |

### 4.7. Use Case: Phân quyền tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Phân quyền tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên phân quyền tài khoản người dùng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên nhấn “Phân quyền người dùng”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Tài khoản người dùng được đổi quyền thành công. |
| Điều kiện thất bại | Tài khoản người dùng được đổi quyền thất bại. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Quản trị viên bấm dropdown chọn vai trò.  2. Hệ thống hiển thị các Vai trò cho người dùng kèm các chi tiết quyền hạn cho vai trò được chọn.  **Quản trị viên** (Quản trị viên)   * Quản lý đơn vị nhân sự. * Quản lý tài khoản người dùng.   **Nhân sự phòng Tổ chức Cán bộ** (TCCB)   * Cấu hình một số danh mục: hệ số lương, loại phụ cấp và một số danh mục có thể được cấu hình trong tương lai. * Quản lý lưu trữ hợp đồng lao động của nhân sự * Quản lý hồ sơ nhân sự (thông tin cơ bản nhân sự, thông tin lương, thông tin khen thưởng/kỷ luật, thông tin, hợp đồng) * Quản lý các thông tin về đơn vị nhân sự * Quản lý các khóa đào tạo.   **Nhân sự phòng Tài chính kế toán**(TCKT)   * Xem hồ sơ nhân sự (thông tin nhân sự - thông tin hồ sơ, hợp đồng, đánh giá, lương & phụ cấp)   **Cán bộ** (Employee)   * Xem thông tin hồ sơ * Xem thông tin đơn vị đang công tác * Đăng ký các khóa đào tạo và xem thông tin khóa đào tạo đã đăng ký.   3. Quản trị viên chọn vai trò.  4. Quản trị viên nhấn **"Lưu"**.  5. Hệ thống kiểm tra tính hợp lệ của thay đổi vai trò.  6. Hệ thống lưu thay đổi vai trò, ghi lịch sử thay đổi và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Phân quyền khi được gọi từ UC 4.5 (Thêm tài khoản) hoặc UC 4.6 (Sửa tài khoản)**   1. UC 4.5 hoặc UC 4.6 gọi UC 4.7 thông qua quan hệ <<include>>. 2. Hệ thống hiển thị phần chọn vai trò (dropdown) được nhúng trực tiếp trong form thêm/sửa tài khoản. 3. Người dùng chọn vai trò cho tài khoản. 4. Hệ thống ghi nhận vai trò đã chọn như một phần của luồng thêm/sửa tài khoản. 5. Kết quả phân quyền được lưu cùng với thao tác lưu tài khoản tại UC gọi. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Quản trị viên nhấn "Hủy". 2. Hệ thống quay lại màn hình trước đó mà không lưu thay đổi. |

### 4.8. Use Case: Thay đổi trạng thái cho tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái cho tài khoản người dùng** |
| Tác nhân chính | Quản trị viên, Hệ thống |
| Mục đích (mô tả) | Cho phép Quản trị viên thay đổi trạng thái tài khoản người dùng (Khóa/Mở khóa) |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên chọn chức năng thay đổi trạng thái khóa tài khoản người dùng. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Trạng thái tài khoản người dùng được cập nhật thành Hoạt động hoặc Bị khóa |
| Điều kiện thất bại | Trạng thái tài khoản người dùng không thay đổi. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại danh sách, Quản trị viên nhấn icon "Khóa" trên dòng user có trạng thái ‘Đang hoạt động’(mặc định) .  2.  Hệ thống hiển thị xác nhận.  3.  Quản trị viên xác nhận.  4.  Hệ thống cập nhật trạng thái ‘Bị khóa’ cho tài khoản.  5.  Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Mở khóa tài khoản**   1. Tại bước 1, Quản trị viên nhấn icon "Mở khóa" trên dòng user tại danh sách. 2. Hệ thống hiển thị xác nhận. 3. Quản trị viên xác nhận 4. Hệ thống cập nhật trạng thái ‘Đang hoạt động’ cho tài khoản.   **A2: Tự động khóa tài khoản**   1. Hệ thống phát hiện nhân sự liên kết với tài khoản đã được đánh dấu thôi việc. 2. Hệ thống cập nhật trạng thái ‘Bị khóa’ cho tài khoản. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không thể khóa tài khoản đang đăng nhập**   1. Tại bước 1, Quản trị viên chọn khóa tài khoản đang sử dụng 2. Hệ thống từ chối thao tác 3. Hiển thị thông báo “Không thể khóa tài khoản đang sử dụng” |

### 4.9. Use Case: Tạo mới đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Tạo mới đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép Người dùng tạo mới một đơn vị tổ chức trong hệ thống, xác định mối quan hệ đơn vị cha – đơn vị con, phục vụ việc xây dựng và quản lý cơ cấu tổ chức nhân sự và nhập liệu thông tin đơn vị đang công tác cho nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng “Thêm mới đơn vị” trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Cán bộ TCCB.  Hệ thống đã tồn tại đơn vị gốc “Trường đại học Thủy lợi”. |
| Điều kiện thành công  (Post-condition) | Đơn vị tổ chức mới được tạo và lưu thành công trong hệ thống.  Đơn vị mới được gắn đúng vào cây cơ cấu tổ chức theo quan hệ cha – con.  Sơ đồ cơ cấu tổ chức được cập nhật và hiển thị ngay sau khi tạo.  Đơn vị mới có thể được sử dụng để gán thông tin đơn vị công tác cho hồ sơ nhân sự. |
| Điều kiện thất bại | Đơn vị không được tạo do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại.  2. Người dùng chọn một đơn vị làm đơn vị cha (hoặc chọn “đơn vị gốc”).  3. Người dùng nhấn chức năng “Thêm mới đơn vị” dưới cấp của đơn vị đã chọn.  4. Hệ thống hiển thị màn hình nhập thông tin đơn vị mới.  5. Người dùng nhập các thông tin:   * Tên đơn vị * Mã đơn vị * Loại đơn vị (Hội đồng, Ban, Khoa, Phòng, Bộ môn, Phòng thí nghiệm, Trung tâm) * Đơn vị cha (mặc định là đơn vị đã chọn ở bước 3) * Thông tin liên hệ (Ngày thành lập, Địa chỉ, Địa chỉ văn phòng,  Email, Số điện thoại, link website(tùy chọn)) * Xác nhận đơn vị nút (Nếu xác nhận thì ta sẽ không thể thêm mới đơn vị con dưới đơn vị này)   6. Người dùng nhấn “Lưu”.  7. Hệ thống kiểm tra dữ liệu hợp lệ (Dữ liệu cần đầy đủ các trường bắt buộc).  8. Hệ thống xác nhận lưu  9. Người dùng xác nhận  10. Hệ thống lưu đơn vị mới vào cơ sở dữ liệu và trạng thái của đơn vị mặc định là “Đang hoạt động”.  11. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Trùng mã đơn vị**   1. Tại bước 7, hệ thống phát hiện mã đơn vị đã tồn tại. 2. Hệ thống hiển thị thông báo: “Mã đơn vị đã tồn tại. Vui lòng nhập mã khác.”   **E2: Thiếu thông tin bắt buộc**   1. Tại bước 7, hệ thống phát hiện thiếu các trường bắt buộc (Tên đơn vị, Mã đơn vị, Loại đơn vị). 2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. 3. Quay lại bước 6.   **E3: Đơn vị cha không hợp lệ**   1. Tại bước 3, hệ thống phát hiện người dùng muốn thêm mới tại đơn vị cha đang ở trạng thái Giải thể/Bị sáp nhập. 2. Hệ thống hiển thị thông báo: “Không thể tạo đơn vị trực thuộc đơn vị đã giải thể/ bị sáp nhập”   **E4: Hủy thao tác**   1. Tại bước 5, Người dùng chọn “Hủy”. 2. Quay lại sơ đồ cơ cấu tổ chức. **E5: Đơn vị cha là đơn vị nút** 1. Tại bước 3, hệ thống phát hiện đơn vị cha đã được xác nhận là đơn vị nút. 2. Hệ thống ẩn/vô hiệu hóa chức năng "Thêm mới đơn vị" dưới cấp đơn vị này và hiển thị thông báo nếu người dùng cố truy cập. |

### 4.10. Use Case: Sửa thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép Người dùng chỉnh sửa thông tin của đơn vị trong cơ cấu tổ chức nhằm đảm bảo dữ liệu luôn chính xác và cập nhật theo thực tế. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng “Sửa thông tin đơn vị” tại màn hình chi tiết đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Cán bộ TCCB.  Đơn vị tổ chức cần chỉnh sửa đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin đơn vị được cập nhật thành công.  Sơ đồ cơ cấu tổ chức phản ánh dữ liệu mới. |
| Điều kiện thất bại | Thông tin đơn vị không được cập nhật do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ đơn vị hiện tại  2. Người dùng chọn chức năng “Sửa thông tin đơn vị”của một đơn vị.  3. Hệ thống hiển thị form chỉnh sửa với các thông tin hiện tại của đơn vị, bao gồm:  **- Thông tin cơ bản:** Tên đơn vị, Mã đơn vị (Không được sửa), Loại đơn vị;  **- Thông tin liên hệ:** Địa chỉ, Địa chỉ văn phòng, Email, Số điện thoại, Website.  4. Người dùng chỉnh sửa các thông tin cần thiết.  5. Người dùng nhấn **“Lưu”**. 6. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  7. Hệ thống xác nhận lưu  8. Người dùng xác nhận.  9. Hệ thống cập nhật thông tin đơn vị.  10. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ**   1. Tại bước 6, hệ thống phát hiện thiếu dữ liệu bắt buộc hoặc định dạng không hợp lệ. 2. Hệ thống hiển thị cảnh báo và không cho phép lưu.   **E2: Không được phép chỉnh sửa**   1. Tại bước 2, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép chỉnh sửa.   **E3: Hủy thao tác**   1. Tại bước 5, Người dùng chọn “Hủy”. 2. Quay lại sơ đồ cơ cấu tổ chức. |

### 4.11. Use Case: Cập nhật trạng thái cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Cập nhật trạng thái cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép người dùng cập nhật trạng thái hoạt động của đơn vị tổ chức (Giải thể hoặc Sáp nhập), đồng thời xử lý các đơn vị con trực thuộc và tự động cập nhật dữ liệu nhân sự, hợp đồng lao động nhằm đảm bảo tính nhất quán của hệ thống. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng “Cập nhật trạng thái” đối với một đơn vị cụ thể tại menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống với quyền Quản trị viên hoặc Phòng TCCB.  Đơn vị tổ chức cần cập nhật đã tồn tại và đang ở trạng thái “Đang hoạt động”. |
| Điều kiện thành công  (Post-condition) | Trạng thái đơn vị được cập nhật thành “Giải thể” hoặc “Sáp nhập”.  Lịch sử thay đổi trạng thái đơn vị được ghi nhận đầy đủ.  Dữ liệu nhân sự, hợp đồng lao động và trạng thái làm việc của nhân sự được cập nhật tự động theo quy định nghiệp vụ. |
| Điều kiện thất bại | Việc cập nhật trạng thái đơn vị không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại. 2. Người dùng chọn một đơn vị đang ở trạng thái "Đang hoạt động". 3. Người dùng chọn chức năng "Cập nhật trạng thái đơn vị". 4. Hệ thống hiển thị form cập nhật, đồng thời **hiển thị cảnh báo danh sách các đơn vị con trực thuộc** (nếu có). 5. Người dùng chọn loại sự kiện: **Giải thể**. 6. Người dùng nhập các thông tin bắt buộc: 6.1. Ngày hiệu lực (ngày giải thể). 6.2. Quyết định (Số quyết định, Ngày quyết định, File đính kèm). 6.3. Lý do (Giải thể / Tái cơ cấu / Khác). 7. **Xử lý đơn vị con (Nếu có):** Người dùng chọn phương án xử lý cho các đơn vị trực thuộc: 7.1. *Tùy chọn A:* Giải thể toàn bộ đơn vị con. 7.2. *Tùy chọn B:* Điều chuyển đơn vị con sang trực thuộc một đơn vị cha khác (yêu cầu chọn đơn vị cha mới từ danh sách). 8. Người dùng nhấn nút **"Lưu xác nhận"**. 9. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào. 10. Hệ thống thực hiện cập nhật đồng loạt: 10.1. Cập nhật trạng thái đơn vị đang thao tác từ “Đang hoạt động” → **“Giải thể”**. 10.2. **Đối với đơn vị con:** Thực hiện Giải thể hoặc Cập nhật đơn vị quản lý cấp trên mới tùy theo lựa chọn tại Bước 7. 10.3. **Đối với nhân sự:**     1. Tất cả hợp đồng đang hiệu lực → "Hết hiệu lực".     2. Trạng thái hợp đồng của nhân sự → "Chưa hợp đồng".     3. Trạng thái làm việc của nhân sự → "Đang chờ xét".     4. Xóa thông tin đơn vị công tác hiện tại của các nhân sự thuộc đơn vị bị giải thể. 11. Hệ thống lưu lịch sử thay đổi và hiển thị thông báo "Cập nhật thành công". |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1.5:** Người dùng chọn loại sự kiện: **Sáp nhập** thay vì Giải thể.  **A1.6:** Người dùng nhập thông tin bắt buộc: Ngày hiệu lực, Quyết định, Lý do và **chọn Đơn vị nhận sáp nhập** từ danh sách đơn vị đang hoạt động.  **A1.7:** **Xử lý đơn vị con:** Hệ thống tự động thiết lập chuyển toàn bộ các đơn vị con trực thuộc sang làm đơn vị con của Đơn vị nhận sáp nhập.  **A1.8:** Người dùng nhấn nút **"Lưu xác nhận"**.  **A1.9:** Hệ thống kiểm tra tính hợp lệ của dữ liệu.  **A1.10:** Hệ thống thực hiện cập nhật đồng loạt:  Cập nhật trạng thái đơn vị đang thao tác từ “Đang hoạt động” → **“Sáp nhập”**.  **Đối với đơn vị con:** Cập nhật "Đơn vị quản lý cấp trên" sang Đơn vị nhận sáp nhập.  **Đối với nhân sự:** Tự động chuyển toàn bộ nhân sự sang Đơn vị nhận sáp nhập (Trạng thái hợp đồng giữ nguyên; Trạng thái làm việc giữ nguyên "Đang công tác"; Thông tin đơn vị mới được cập nhật).  **A1.11:** Hệ thống lưu lịch sử thay đổi và hiển thị thông báo "Cập nhật thành công". |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Đơn vị không hợp lệ để cập nhật trạng thái**   * Tại bước 2, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. * Hệ thống vô hiệu hóa nút chức năng và hiển thị thông báo "Đơn vị này không còn hoạt động".   **E2: Dữ liệu không hợp lệ**   * Tại bước 9 hoặc A1.9, nếu thiếu thông tin bắt buộc, ngày hiệu lực sai định dạng hoặc chưa đính kèm file Quyết định. * Hệ thống chặn thao tác lưu, bôi đỏ các trường bị lỗi và yêu cầu nhập lại.   **E3: Chưa xử lý đơn vị con khi Giải thể**   * Tại bước 7, nếu đơn vị có đơn vị con nhưng người dùng chọn Tùy chọn B (Điều chuyển) mà không chọn Đơn vị cha mới. * Hệ thống cảnh báo: *"Vui lòng chọn đơn vị quản lý mới cho các đơn vị trực thuộc trước khi giải thể."*   **E4: Ràng buộc chức vụ quản lý**   * Tại bước 7, nếu đơn vị bị giải thể đang có nhân sự giữ chức vụ quản lý (Trưởng phòng, Trưởng khoa...). * Hệ thống chặn thao tác và thông báo: *"Vui lòng thực hiện bãi nhiệm chức vụ quản lý của đơn vị trước khi thực hiện giải thể."* |

### 4.12. Use Case: Xem chi tiết thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB, Quản trị viên |
| Mục đích (mô tả) | Cho phép Phòng TCCB hoặc Quản trị viên xem đầy đủ thông tin của một đơn vị tổ chức trong cơ cấu tổ chức, bao gồm:   * Thông tin cơ bản và trạng thái đơn vị * Danh sách nhân sự và chức vụ hiện tại * Lịch sử bổ nhiệm, miễn nhiệm chức vụ * Lịch sử thay đổi tổ chức (thành lập, sáp nhập, giải thể)   Nhằm phục vụ công tác theo dõi, quản lý và tra cứu dữ liệu tổ chức nhân sự theo thời gian |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB hoặc Quản trị viên chọn  chức năng xem chi tiết một đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB hoặc Quản trị viên đã đăng nhập hệ thống.  Đơn vị tổ chức đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Toàn bộ thông tin chi tiết của đơn vị được hiển thị chính xác. Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được dữ liệu do lỗi hệ thống hoặc không tồn tại đơn vị. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức.  2. Người dùng chọn một đơn vị trong cây.  3. Hệ thống hiển thị chi tiết thông tin các đơn vị, bao gồm:   * Tab **“Tổng quan”**, bao gồm: Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị (Đang hoạt động / Sáp nhập / Giải thể) * Tab **“Nhân sự”**: Hệ thống hiển thị danh sách các nhân sự, Tên chức vụ, hệ thống hiển thị: Họ tên nhân sự, Mã cán bộ, Ngày bắt đầu. Hệ thống hiển thị danh sách nhân sự thuộc đơn vị * Tab **“Đơn vị trực thuộc”**: Hệ thống hiển thị danh sách các đơn vị dưới cấp trực thuộc đơn vị đang xem. * Tab **“Lịch sử”**: Hệ thống hiển thị lịch sử bổ nhiệm, miễn nhiệm chức vụ và lịch sử thay đổi tổ chức (thành lập, sáp nhập, giải thể). |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

## 4.2 Phần đóng góp của Nguyễn Hải Ninh (UC 4.13–4.24)

### 4.13. Use Case: Thêm mới danh mục hệ số lương (Nguyễn Hải Ninh)

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB thiết lập hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công  (Post-condition) | Thiết lập hệ số lương theo ngạch/bậc thành công |
| Điều kiện thất bại | Hệ số lương không được cập nhật mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm hệ số lương.  2.  Hệ thống hiển thị màn hình nhập hệ số lương.  3.  Phòng TCCB nhập các các thông tin   * Ngạch viên chức * Bậc lương * Hệ số lương   4.  Phòng TCCB xác nhận lưu thông tin  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống thêm thông tin.  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Bậc lương trong cùng ngạch đã tồn tại * Hệ số lương phải là số thực, không được nhỏ hơn 0 * Bậc lương phải là số nguyên * Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi 3. Dữ liệu không được lưu   **E2: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách bậc lương. |

### 4.14. Use Case: Sửa danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu như nhập liệu sai sót. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục hệ số lương cần chỉnh sửa đã tồn tại trong hệ thống.  Danh mục hệ số lương đang ở trạng thái “Đang sử dụng”.  Hệ số lương chưa được hồ sơ nhân sự nào sử dụng. |
| Điều kiện thành công  (Post-condition) | Sửa hệ số lương theo ngạch/bậc thành công |
| Điều kiện thất bại | Hệ số lương không được cập nhật trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa hệ số lương của một bản ghi hệ số lương đã được cấu hình.  2.  Hệ thống hiển thị màn hình nhập hệ số lương.  3.  Phòng TCCB sửa các các thông tin   * Ngạch viên chức * Bậc lương * Hệ số lương mỗi bậc   4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống cập nhật thông tin.  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Bậc lương trong cùng ngạch đã tồn tại * Hệ số lương phải là số thực, không được nhỏ hơn 0 * Bậc lương phải là số nguyên * Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi 3. Dữ liệu không được lưu   **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, hệ thống phát hiện danh mục hệ số lương đang ở trạng thái “Ngừng sử dụng”. 2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”   **E3: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách bậc lương   **E4: Hệ số lương đã được hồ sơ nhân sự sử dụng**   1. Tại bước 1, hệ thống phát hiện hệ số lương đã được ít nhất một hồ sơ nhân sự sử dụng. 2. Hệ thống hiển thị thông báo: “Không thể chỉnh sửa hệ số lương đã được sử dụng trong hồ sơ nhân sự.” 3. Hệ thống vô hiệu hóa nút “Sửa”. |

### 4.16. Use Case: Thay đổi trạng thái danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục hệ số lương giữa "Đang sử dụng" và "Ngừng sử dụng", nhằm kiểm soát việc áp dụng hệ số lương cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục hệ số lương cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh mục hệ số lương được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”).  Nếu chuyển sang “Ngừng sử dụng”: hệ số lương không còn được chọn khi tạo hoặc chỉnh sửa hồ sơ nhân sự mới; các hồ sơ nhân sự đã sử dụng hệ số lương này không bị ảnh hưởng.  Nếu chuyển sang “Đang sử dụng”: hệ số lương được phép chọn lại khi tạo hoặc chỉnh sửa hồ sơ nhân sự. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục hệ số lương đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục hệ số lương thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, Phòng TCCB chọn một danh mục hệ số lương đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục hệ số lương thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.17. Use Case: Thêm mới danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB thêm mới loại phụ cấp phục vụ cho việc quản lý và nhập liệu thông tin nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công  (Post-condition) | Danh mục loại phụ cấp được thêm thành công |
| Điều kiện thất bại | Loại phụ cấp  không được cập nhật mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm mới danh mục loại phụ cấp.  2.  Hệ thống hiển thị màn hình nhập danh mục loại phụ cấp.  3.  Phòng TCCB thêm các các thông tin   * Tên loại phụ cấp * Mô tả * Cách tính   4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **Không có** |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Tên loại phụ cấp dài quá 200 từ, có ký tự đặc biệt không hợp lệ. * Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi 3. Dữ liệu không được lưu   **E2: Hủy thao tác**   1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách. |

### 4.18. Use Case: Sửa danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa loại phụ cấp phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu có nhập liệu danh mục sai sót |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục loại phụ cấp cần chỉnh sửa đã tồn tại trong hệ thống.  Danh mục loại phụ cấp đang ở trạng thái “Đang sử dụng”. |
| Điều kiện thành công  (Post-condition) | Danh mục loại phụ cấp được sửa thành công |
| Điều kiện thất bại | Loại phụ cấp không được cập nhật trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa loại phụ cấp đã tồn tại.  2.  Hệ thống hiển thị màn hình sửa danh mục loại phụ cấp.  3.  Phòng TCCB sửa các các thông tin   * Tên loại phụ cấp * Mô tả * Cách tính   4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi: 2. Tên loại phụ cấp dài quá 200 từ, có ký tự đặc biệt không hợp lệ. 3. Thông tin bắt buộc đầy đủ  4. Hệ thống báo lỗi 5. Dữ liệu không được lưu   **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, hệ thống phát hiện danh mục loại phụ cấp đang ở trạng thái “Ngừng sử dụng”. 2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”   **E3: Hủy thao tác**   1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách. |

### 4.19. Use Case: Thay đổi trạng thái danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục loại phụ cấp giữa “Đang sử dụng” và “Ngừng sử dụng”, nhằm kiểm soát việc áp dụng loại phụ cấp cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại phụ cấp cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh mục loại phụ cấp được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”).  Nếu chuyển sang “Ngừng sử dụng”: loại phụ cấp không còn được chọn khi tạo hoặc chỉnh sửa hồ sơ nhân sự mới; các loại phụ cấp được hồ sơ nhân sự đã sử dụng sẽ được hiển thị khác với các loại phụ cấp ở trạng thái “Đang sử dụng”.  Nếu chuyển sang “Đang sử dụng”: loại phụ cấp được phép chọn lại khi tạo hoặc chỉnh sửa hồ sơ nhân sự. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục loại phụ cấp đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại phụ cấp thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, Phòng TCCB chọn một danh mục loại phụ cấp đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại phụ cấp thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.20. Use Case: Thêm mới danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB cấu hình loại hợp đồng theo quy định nhà nước phục vụ cho việc quản lý và nhập liệu hợp đồng nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công  (Post-condition) | Thiết lập loại hợp đồng thành công |
| Điều kiện thất bại | Loại hợp đồng không được cập nhật mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm loại hợp đồng.  2.  Hệ thống hiển thị các trường thông tin (Tên loại hợp đồng, Số tháng tối thiểu, Số tháng tối đa, Số lần gia hạn tối đa, thời gian theo ngày chờ gia hạn).  3. Phòng TCCB nhập đầy đủ thông tin  4.  Phòng TCCB xác nhận lưu thông tin  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Số tháng, số lần gia hạn, thời gian chờ gia hạn phải là số nguyên * Thông tin bắt buộc đầy đủ * Hệ thống báo lỗi * Dữ liệu không được lưu   **E2: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách loại hợp đồng |

### 4.21. Use Case: Sửa danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa cấu hình loại hợp đồng theo quy định nhà nước phục vụ cho việc quản lý và nhập liệu hợp đồng nhân sự nếu như nhập liệu sai sót. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục loại hợp đồng cần chỉnh sửa đã tồn tại trong hệ thống.  Danh mục loại hợp đồng đang ở trạng thái “Đang sử dụng”. |
| Điều kiện thành công  (Post-condition) | Sửa loại hợp đồng  thành công |
| Điều kiện thất bại | Loại hợp đồng  không được cập nhật trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa loại hợp đồng của một loại hợp đồng đã được cấu hình.  2.  Hệ thống hiển thị màn hình sửa loại hợp đồng và các trường thông tin  (Tên loại hợp đồng, Số tháng tối thiểu, Số tháng tối đa, Số lần gia hạn tối đa, thời gian theo ngày chờ gia hạn).  3.  Phòng TCCB sửa các các thông tin  4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Số tháng, số lần gia hạn, thời gian chờ gia hạn phải là số nguyên * Thông tin bắt buộc đầy đủ   + Hệ thống báo lỗi   + Dữ liệu không được lưu   **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, hệ thống phát hiện danh mục loại hợp đồng đang ở trạng thái “Ngừng sử dụng”. 2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”   **E3: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách loại hợp đồng |

### 4.22. Use Case: Thay đổi trạng thái danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục loại hợp đồng giữa “Đang sử dụng” và “Ngừng sử dụng”, nhằm kiểm soát việc áp dụng loại hợp đồng cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại hợp đồng cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh mục loại hợp đồng được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”).  Nếu chuyển sang “Ngừng sử dụng”: loại hợp đồng không còn được chọn khi tạo hoặc chỉnh sửa hợp đồng lao động mới; các loại hợp đồng đã được sử dụng trong hợp đồng lao động sẽ được hiển thị khác với các loại hợp đồng ở trạng thái “Đang sử dụng”.  Nếu chuyển sang “Đang sử dụng”: loại hợp đồng được phép chọn lại khi tạo hoặc chỉnh sửa hợp đồng lao động. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục loại hợp đồng đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại hợp đồng thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, Phòng TCCB chọn một danh mục loại hợp đồng đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại hợp đồng thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.23. Use Case: Xem chi tiết các thống kê

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết các thống kê** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cung cấp cho Phòng TCCB, Phòng TCKT có các báo cáo tổng hợp, thống kê trực quan về tình hình nhân sự, cơ cấu tổ chức, đào tạo và biến động nhân sự theo thời gian; hỗ trợ theo dõi, phân tích và ra quyết định quản lý. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn menu “Báo cáo và Thống kê” trên hệ thống. |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB hoặc Phòng TCKT đã đăng nhập hệ thống.  Dữ liệu nhân sự, đơn vị, đào tạo đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Các báo cáo thống kê được hiển thị đầy đủ, chính xác. Người dùng có thể xem chi tiết, lọc dữ liệu và xuất báo cáo theo nhu cầu. |
| Điều kiện thất bại | Không hiển thị được báo cáo do lỗi dữ liệu hoặc hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng truy cập menu **“Báo cáo và Thống kê”**.  2. Hệ thống hiển thị **Danh sách nhóm báo cáo**.  3. Người dùng chọn từng nhóm báo cáo để xem chi tiết.   * Báo cáo tổng quan nhân sự * Báo cáo biến động nhân sự * Báo cáo cơ cấu nhân sự theo đơn vị * Báo cáo cơ cấu nhân sự theo trình độ, học hàm, chức danh * Báo cáo bổ nhiệm nhân sự * Báo cáo đào tạo và phát triển * Báo cáo hợp đồng và tình trạng làm việc * Báo cáo đánh giá của cán bộ với khóa đào tạo   4. Hệ thống hiển thị dữ liệu thống kê tương ứng dưới dạng biểu đồ và bảng đa dạng theo thời gian, đơn vị, loại nhân sự. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Xuất báo cáo**   1. Tại bước 4, Người dùng chọn chức năng “Xuất báo cáo” (Định dạng xuất: PDF / Excel, Phạm vi dữ liệu (theo bộ lọc hiện tại)) 2. Người dùng xác nhận xuất 3. Hệ thống tạo file báo cáo và cho phép tải về |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.24. Use Case: Xem nhật ký hệ thống (Audit Log)

|  |  |
| --- | --- |
| **Tên use case** | **Xem nhật ký hệ thống (Audit Log)** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên xem, tìm kiếm và lọc nhật ký ghi lại toàn bộ các thao tác quan trọng trên hệ thống (đăng nhập, thêm/sửa/xóa dữ liệu, phân quyền, thay đổi trạng thái…) nhằm phục vụ công tác giám sát, kiểm tra an ninh và truy vết sự cố. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên chọn menu "Nhật ký hệ thống" (Audit Log). |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. Hệ thống đã ghi nhận các bản ghi nhật ký từ hoạt động của người dùng. |
| Điều kiện thành công  (Post-condition) | Danh sách nhật ký hệ thống được hiển thị đầy đủ, chính xác theo tiêu chí lọc. Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được nhật ký do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Quản trị viên chọn menu "Nhật ký hệ thống".  2. Hệ thống hiển thị danh sách nhật ký (phân trang), mỗi bản ghi bao gồm:   * Thời gian thao tác, * Tài khoản thực hiện (Username), * Họ tên người thực hiện, * Vai trò, * Loại hành động (Đăng nhập / Đăng xuất / Thêm / Sửa / Xóa / Phân quyền / Thay đổi trạng thái), * Đối tượng bị tác động (Tên module, Mã đối tượng), * Mô tả chi tiết thay đổi, * Địa chỉ IP.   3. Quản trị viên có thể lọc nhật ký theo các tiêu chí:   * Khoảng thời gian: Từ ngày – Đến ngày * Tài khoản thực hiện: Nhập Username hoặc Họ tên * Loại hành động: Tất cả (Mặc định), Đăng nhập, Đăng xuất, Thêm, Sửa, Xóa, Phân quyền, Thay đổi trạng thái * Module: Tất cả (Mặc định), Quản lý tài khoản, Hồ sơ nhân sự, Cơ cấu tổ chức, Hợp đồng, Đào tạo, Danh mục cấu hình   4. Quản trị viên nhấn "Tìm kiếm" hoặc "Áp dụng bộ lọc".  5. Hệ thống hiển thị kết quả nhật ký phù hợp với tiêu chí đã chọn.  6. Quản trị viên có thể nhấn vào một bản ghi để xem chi tiết thay đổi (giá trị trước và sau khi thay đổi). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Xuất nhật ký**   1. Tại bước 5, Quản trị viên chọn chức năng "Xuất nhật ký". 2. Hệ thống cho phép xuất danh sách nhật ký theo bộ lọc hiện tại dưới định dạng Excel hoặc PDF. 3. Quản trị viên xác nhận xuất. 4. Hệ thống tạo file và cho phép tải về. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không tìm thấy kết quả**   1. Tại bước 5, nếu không có bản ghi nhật ký nào phù hợp với tiêu chí lọc, Hệ thống hiển thị thông báo: "Không tìm thấy nhật ký phù hợp với tiêu chí tìm kiếm." |

## 4.3 Phần đóng góp của Ngô Quang Tùng (UC 4.25–4.37)

> Nội dung UC chi tiết của phần Ngô Quang Tùng (UC 4.25–4.37) được tham chiếu tại file [`Tung/uc-tung.md`](./Tung/uc-tung.md).

## 4.4 Phần đóng góp của Ngô Đức Nam Khánh (UC 4.38–4.50)

### 4.38. Use Case: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB bổ nhiệm nhân sự vào đơn vị tổ chức hoặc điều chuyển nhân sự đang công tác sang đơn vị tổ chức khác. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng bổ nhiệm trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức.  Nhân sự phải có trạng thái hợp đồng 'Còn hiệu lực' hoặc 'Chờ gia hạn' và trạng thái làm việc 'Đang chờ xét' hoặc 'Đang công tác'. |
| Điều kiện thành công  (Post-condition) | Nhân sự được bổ nhiệm vào đơn vị mới hoặc được điều chuyển sang đơn vị khác thành công. Thông tin nhân sự của các đơn vị liên quan được cập nhật. |
| Điều kiện thất bại | Việc bổ nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Phòng TCCB chọn bổ nhiệm nhân sự chưa công tác.  3. Hệ thống hiển thị danh sách nhân sự ở trạng thái “Đang chờ xét” và trạng thái hợp đồng “Còn hiệu lực”.  4. Phòng TCCB chọn nhân sự và nhập thông tin như Chức vụ, Ngày bắt đầu.  5. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  6. Hệ thống cập nhật danh sách nhân sự của đơn vị, chuyển trạng thái công việc của nhân sự thành “Đang công tác” và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Điều chuyển nhân sự đang công tác ở đơn vị khác**  1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Phòng TCCB chọn điều chuyển nhân sự đang công tác tại đơn vị khác.  3. Hệ thống yêu cầu chọn đơn vị hiện tại và chọn nhân sự từ đơn vị được chọn.  4. Phòng TCCB chọn nhân sự và nhập thông tin như Chức vụ, Ngày bắt đầu.  5. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  6. Hệ thống gỡ nhân sự khỏi đơn vị cũ, thêm vào đơn vị mới, cập nhật danh sách nhân sự của cả hai đơn vị và thông báo thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ**   1. Tại bước 5, Hệ thống kiểm tra phát hiện:  * Ngày bắt đầu < ngày hiện tại  2. Hệ thống yêu cầu nhập lại và không lưu dữ liệu.   **E2: Không được phép tiếp tục**   1. Tại bước 1, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục cập nhật bổ nhiệm. |

### 4.39. Use Case: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thực hiện bãi nhiệm nhân sự trong đơn vị tổ chức, nhằm cập nhật chính xác tình trạng nhân sự và phục vụ công tác quản lý nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng bãi nhiệm nhân sự của đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức. |
| Điều kiện thành công  (Post-condition) | Nhân sự được miễn nhiệm khỏi chức vụ. Trạng thái công việc của nhân sự được cập nhật thành “Đang chờ xét”. Nhân sự được xóa khỏi danh sách của đơn vị tổ chức. |
| Điều kiện thất bại | Việc bãi nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Hệ thống hiển thị danh sách nhân sự của đơn vị.  3. Phòng TCCB chọn chức năng bãi nhiệm đối với một nhân sự trong danh sách.  4. Hệ thống yêu cầu xác nhận thao tác.  5. Phòng TCCB xác nhận thao tác bãi nhiệm.  6. Hệ thống cập nhật trạng thái công việc của nhân sự thành “Đang chờ xét” và xóa nhân sự khỏi danh sách của đơn vị tổ chức. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không được phép tiếp tục**   1. Tại bước 3, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục thực hiện bãi nhiệm. |

### 4.40. Use Case: Ghi nhận đánh giá cho nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận đánh giá cho nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Ghi nhận các quyết định đánh giá đối với nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Thêm đánh giá khen thưởng hoặc kỷ luật” |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã được tạo Nhân sự không ở trạng thái làm việc 'Đã thôi việc'. |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được cập nhật.  Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Dữ liệu đánh giá không được ghi nhận vào hệ thống do thiếu các trường thông tin bắt buộc, hoặc do lỗi kết nối cơ sở dữ liệu/phiên đăng nhập hết hạn |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn tab " Thêm đánh giá khen thưởng hoặc kỷ luật".  2. Hệ thống yêu cầu nhập mã nhân sự và chọn loại đánh giá  3. Phòng TCCB nhập mã nhân sự và chọn loại đánh giá (Khen thưởng/ Kỷ luật)  4.  Hệ thống hiển thị giao diện nhập liệu:   * Nếu chọn loại đánh giá là khen thưởng: `Loại khen thưởng`, ‘Tên khen thưởng’, `Ngày quyết định`, `Số quyết định`, `Nội dung`, `Số tiền thưởng` (nếu có). * Nếu chọn loại đánh giá là kỷ luật: `Loại kỷ luật`, ‘Tên kỷ luật’,  `Ngày quyết định`, `Lý do`, `Hình thức xử lý`.   5.  Nhấn "Lưu".  6. Hệ thống kiểm tra dữ liệu hợp lệ (Đầy đủ các trường thông tin)  7. Hệ thống lưu dữ liệu và đẩy vào hồ sơ cá nhân và thông báo thành công. *Lưu ý: Xem UC 4.41 (Xem lịch sử đánh giá khen thưởng/kỷ luật) và UC 4.42 (Tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật) cho các tác vụ tra cứu liên quan.* |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Mã nhân sự không hợp lệ**   1. Tại bước 3, Hệ thống phát hiện mã nhân sự không tồn tại. 2. Hệ thống từ chối tiếp tục tạo bản đánh giá.   **E2: Dữ liệu không hợp lệ**   1. Tại bước 6, Hệ thống phát hiện dữ liệu không đầy đủ các trường thông tin. 2. Hệ thống từ chối lưu thông tin và thông báo lỗi.   **E3: Hủy thao tác**  1. Tại bước 2, Phòng TCCB chọn “Hủy”.  2. Quay lại màn hình danh sách nhân sự. **E4: Nhân sự đã thôi việc**   1. Tại bước 3, hệ thống phát hiện nhân sự đang ở trạng thái làm việc “Đã thôi việc”. 2. Hệ thống từ chối ghi nhận đánh giá và hiển thị thông báo: “Không thể ghi nhận đánh giá cho nhân sự đã thôi việc.” |

### 4.41. Use Case: Xem lịch sử đánh giá khen thưởng/kỷ luật (FEAT 10.2)

|  |  |
| --- | --- |
| **Tên use case** | **Xem lịch sử đánh giá khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem lịch sử toàn bộ các bản ghi đánh giá khen thưởng và kỷ luật của một nhân sự theo trình tự thời gian, phục vụ tra cứu, đối chiếu và theo dõi hồ sơ đánh giá của nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn tab “Khen thưởng/Kỷ luật” trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Lịch sử đánh giá khen thưởng/kỷ luật của nhân sự được hiển thị đầy đủ, chính xác.  Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không thể hiển thị lịch sử đánh giá do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.35).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **“Khen thưởng/Kỷ luật”**.  4. Hệ thống hiển thị danh sách toàn bộ bản ghi đánh giá của nhân sự theo thứ tự thời gian, bao gồm các thông tin: Ngày quyết định, Loại đánh giá (Khen thưởng/Kỷ luật), Tên đánh giá, Số quyết định, Mô tả ngắn/Nội dung.  5. Phòng TCCB chọn một bản ghi đánh giá trong danh sách.  6. Hệ thống hiển thị chi tiết bản ghi đã chọn, bao gồm đầy đủ thông tin đã được ghi nhận từ UC 4.40. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Nhân sự chưa có lịch sử đánh giá**   1. Tại bước 3, nếu hồ sơ nhân sự chưa có bản ghi khen thưởng hoặc kỷ luật nào. 2. Hệ thống hiển thị tab **“Khen thưởng/Kỷ luật”** ở trạng thái trống và thông báo: *“Nhân sự chưa có lịch sử đánh giá khen thưởng/kỷ luật.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.42. Use Case: Tìm kiếm và lọc danh sách đánh giá (FEAT 10.3)

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm và lọc danh sách đánh giá** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tìm kiếm và lọc danh sách các bản ghi khen thưởng/kỷ luật theo nhân sự, loại đánh giá hoặc khoảng thời gian nhằm phục vụ công tác tra cứu, thống kê và đối chiếu dữ liệu đánh giá. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB truy cập chức năng quản lý đánh giá khen thưởng/kỷ luật. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách các bản ghi đánh giá phù hợp với điều kiện tìm kiếm/lọc được hiển thị đầy đủ, chính xác.  Phòng TCCB có thể tiếp tục xem chi tiết từng bản ghi. |
| Điều kiện thất bại | Hệ thống không thể xử lý yêu cầu tìm kiếm/lọc do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chức năng **quản lý đánh giá khen thưởng/kỷ luật**.  2. Hệ thống hiển thị danh sách các bản ghi đánh giá và vùng bộ lọc tìm kiếm.  3. Phòng TCCB nhập từ khóa tìm kiếm và/hoặc chọn các tiêu chí lọc, bao gồm: Nhân sự (Mã cán bộ/Họ tên), Loại đánh giá (Khen thưởng/Kỷ luật), Khoảng thời gian (Từ ngày – Đến ngày).  4. Phòng TCCB nhấn **“Tìm kiếm”** hoặc **“Áp dụng bộ lọc”**.  5. Hệ thống hiển thị danh sách kết quả phù hợp với tiêu chí đã chọn, bao gồm các thông tin: Mã cán bộ, Họ tên, Loại đánh giá, Tên đánh giá, Ngày quyết định, Số quyết định.  6. Phòng TCCB có thể chọn một bản ghi bất kỳ trong danh sách kết quả.  7. Hệ thống hiển thị chi tiết bản ghi đánh giá đã chọn (tham chiếu UC 4.41). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không có kết quả phù hợp**   1. Tại bước 5, nếu không có bản ghi nào phù hợp với tiêu chí tìm kiếm/lọc. 2. Hệ thống hiển thị thông báo: *“Không tìm thấy đánh giá phù hợp với tiêu chí tìm kiếm.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.43. Use Case: Mở khóa đào tạo cho cán bộ giảng viên (Ngô Đức Nam Khánh)

|  |  |
| --- | --- |
| **Tên use case** | **Mở khóa đào tạo cho cán bộ giảng viên** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Cán bộ TCCB tạo mới và thiết lập thông tin một khóa đào tạo dành cho cán bộ, giảng viên; cấu hình hình thức đào tạo, thời gian, kinh phí và điều kiện đăng ký, làm cơ sở cho việc đăng ký tham gia và quản lý đào tạo sau này. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng mở khóa học trong menu “Đào tạo & Phát triển” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Khóa đào tạo được tạo mới và lưu thành công.  Trạng thái khóa đào tạo được thiết lập theo cấu hình. |
| Điều kiện thất bại | Khóa đào tạo không được tạo do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB chọn menu "Đào tạo & Phát triển".  2.  Phòng TCCB nhấn "Tạo khóa đào tạo mới".  3. Hệ thống hiển thị thông tin nhập  4.  Phòng TCCB nhập thông tin: Tên khóa đào tạo, Loại khóa đào tạo (theo cấu hình), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo (Tên chứng chỉ, Loại chứng chỉ).  5.  Phòng TCCB thiết lập thời gian mở đăng ký từ ngày - đến ngày, Giới hạn số người tham gia.  6. Phòng TCCB nhấn “Lưu”.  7. Hệ thống kiểm tra dữ liệu hợp lệ.  8. Hệ thống yêu cầu xác nhận tạo khóa đào tạo.  9. Phòng TCCB xác nhận.  10. Hệ thống lưu khóa đào tạo và thiết lập trạng thái ban đầu là “Đang mở đăng ký" |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu các trường bắt buộc (Tên khóa, Loại khóa, Thời gian), thời gian mở đăng ký kết thúc sau ngày bắt đầu đào tạo. 2. Hệ thống hiển thị cảnh báo và yêu cầu chỉnh sửa.   **E2: Hủy thao tác**   1. Tại bước 4, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.44. Use Case: Sửa thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa các thông tin của khóa đào tạo đã được tạo nhằm cập nhật kế hoạch đào tạo phù hợp với thực tế, đồng thời đảm bảo không vi phạm các ràng buộc nghiệp vụ đối với khóa đào tạo đã mở đăng ký hoặc đã có người tham gia |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Sửa thông tin khóa đào tạo” tại một khóa đào tạo trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Khóa đào tạo đã tồn tại trong hệ thống.  Khóa đào tạo đang ở trạng thái "Đang mở đăng ký" hoặc "Đang đào tạo". |
| Điều kiện thành công  (Post-condition) | Thông tin khóa đào tạo được cập nhật thành công. Các thay đổi được ghi nhận và áp dụng ngay cho khóa đào tạo. |
| Điều kiện thất bại | Thông tin khóa đào tạo không được cập nhật do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo. 3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Sửa thông tin”**.  4. Hệ thống hiển thị màn hình chỉnh sửa thông tin khóa đào tạo.  5. Phòng TCCB chỉnh sửa các thông tin cho phép:   * Tên khóa đào tạo * Địa điểm * Kinh phí (nếu có) * Cam kết sau đào tạo (nếu có) * Thông tin chứng chỉ sau đào tạo * Trạng thái khóa đào tạo * Thời gian mở đăng ký và giới hạn số người tham gia (nếu được phép)   6. Phòng TCCB nhấn **“Lưu”**. 7. Hệ thống kiểm tra tính hợp lệ và ràng buộc nghiệp vụ (bao gồm kiểm tra chuyển trạng thái khóa đào tạo phải tuân theo thứ tự: Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước).  8. Hệ thống yêu cầu xác nhận cập nhật.  9. Phòng TCCB xác nhận.  10. Hệ thống cập nhật thông tin khóa đào tạo và thông báo thành công.  *Lưu ý: Khi trạng thái khóa đào tạo được chuyển sang "Đang đào tạo", hệ thống tự động cập nhật tất cả đăng ký tham gia có trạng thái "Đã đăng ký" sang "Đang học".* |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Chỉnh sửa khi khóa đào tạo đang diễn ra**   1. Tại bước 4, nếu khóa đào tạo ở trạng thái "Đang đào tạo", hệ thống chỉ cho phép chỉnh sửa: Địa điểm, Kinh phí, Cam kết sau đào tạo, Thông tin chứng chỉ sau đào tạo. 2. Hệ thống khóa không cho phép chỉnh sửa: Tên khóa đào tạo, Loại khóa đào tạo, Thời gian mở đăng ký, Giới hạn số người tham gia. 3. Tiếp tục từ bước 6. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Chuyển trạng thái không hợp lệ**   1. Tại bước 7, hệ thống phát hiện trạng thái mới được chọn vi phạm thứ tự chuyển đổi (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước). 2. Hệ thống hiển thị thông báo: *"Chuyển trạng thái không hợp lệ."* và yêu cầu chọn lại.   **E2: Vi phạm ràng buộc đăng ký**   1. Tại bước 7, hệ thống phát hiện nếu: Giảm giới hạn số người tham gia nhỏ hơn số lượng đã đăng ký. 2. Hệ thống hiển thị cảnh báo và không cho phép lưu.   **E3: Dữ liệu không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu trường bắt buộc hoặc thời gian không hợp lệ. 2. Hệ thống yêu cầu chỉnh sửa lại thông tin.   **E4: Hủy thao tác**   1. Tại bước 5, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.45. Use Case: Xem chi tiết thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem đầy đủ thông tin chi tiết của một khóa đào tạo đã được tạo, bao gồm trạng thái khóa học, thông tin tổ chức đào tạo, danh sách cán bộ – giảng viên đăng ký tham gia, và tình trạng tham gia của từng nhân sự, nhằm phục vụ công tác quản lý, theo dõi và ra quyết định điều chỉnh khóa đào tạo khi cần thiết. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn một khóa đào tạo và nhấn chức năng “Xem chi tiết” trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Khóa đào tạo đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết của khóa đào tạo được hiển thị đầy đủ và chính xác.  Phòng TCCB có thể theo dõi tình trạng khóa học và danh sách nhân sự tham gia. |
| Điều kiện thất bại | Không thể hiển thị thông tin khóa đào tạo do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo.  3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Xem chi tiết”**.  4. Hệ thống hiển thị màn hình chi tiết khóa đào tạo với đầy đủ các nhóm thông tin sau:   * **Thông tin chung khóa đào tạo**: Tên khóa đào tạo, Loại khóa đào tạo, Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo. * **Thông tin đăng ký**: Thời gian mở đăng ký, Giới hạn số lượng người tham gia, Số lượng đã đăng ký / số lượng tối đa. * **Danh sách tham gia**: Hệ thống hiển thị danh sách cán bộ, giảng viên đã đăng ký khóa đào tạo, bao gồm Họ và tên, Mã cán bộ, Đơn vị đang công tác, Thời điểm đăng ký và Trạng thái tham gia. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.46. Use Case: Ghi nhận kết quả đào tạo của cán bộ giảng viên

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận kết quả đào tạo của cán bộ giảng viên** |
| Tác nhân chính | Cán bộ TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB ghi nhận kết quả tham gia khóa đào tạo của cán bộ, giảng viên sau khi khóa học kết thúc; cập nhật trạng thái hoàn thành, không đạt và lưu trữ chứng chỉ đào tạo vào hồ sơ nhân sự nhằm phục vụ công tác quản lý và đánh giá năng lực. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Ghi nhận kết quả đào tạo” tại tab “Danh sách học viên” của một khóa đào tạo. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Khóa đào tạo đã tồn tại trong hệ thống.  Trạng thái khóa đào tạo là “Đã hoàn thành”.  Khóa đào tạo có danh sách học viên đã đăng ký. |
| Điều kiện thành công  (Post-condition) | Kết quả đào tạo của từng học viên được ghi nhận thành công.  Trạng thái tham gia của học viên được cập nhật (Hoàn thành / Không đạt).  Chứng chỉ đào tạo (nếu có) được lưu vào hồ sơ cá nhân của nhân sự.  Lịch sử đào tạo của nhân sự được cập nhật. |
| Điều kiện thất bại | Kết quả đào tạo không được ghi nhận do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2. Phòng TCCB chọn xem chi tiết tab **“Danh sách học viên”** của một khóa đào tạo có trạng thái **“Đã hoàn thành”**.  3. Hệ thống hiển thị danh sách học viên tham gia khóa đào tạo, bao gồm: Họ tên, Mã cán bộ, Đơn vị công tác, Trạng thái tham gia hiện tại (Đang học).  4. Phòng TCCB chọn một học viên và nhấn **“Ghi nhận kết quả”**.  5. Hệ thống hiển thị biểu mẫu ghi nhận kết quả, bao gồm: Trạng thái kết quả (Hoàn thành / Không đạt), Ngày hoàn thành (mặc định là ngày kết thúc khóa học), File chứng chỉ (PDF; tùy chọn nhưng bắt buộc nếu trạng thái là “Hoàn thành”).  6. Phòng TCCB nhập thông tin và nhấn **“Lưu”**.  7. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  8. Hệ thống cập nhật trạng thái học viên:   * Nếu **Hoàn thành**: ghi nhận kết quả đào tạo và lưu chứng chỉ vào hồ sơ nhân sự. * Nếu **Không đạt**: chỉ lưu trạng thái kết quả, không cập nhật chứng chỉ, đồng thời thông báo ghi nhận kết quả thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Ghi nhận kết quả cho nhiều học viên**   1. Tại bước 4, Phòng TCCB có thể chọn nhiều học viên. 2. Hệ thống cho phép ghi nhận kết quả hàng loạt với cùng trạng thái. 3. Tiếp tục bước 5 |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Khóa đào tạo chưa hoàn thành**   1. Tại bước 4, nếu trạng thái khóa đào tạo khác “Đã hoàn thành”. 2. Hệ thống hiển thị thông báo: *“Chỉ có thể ghi nhận kết quả khi khóa đào tạo đã hoàn thành.”*   **E2: Thiếu chứng chỉ khi hoàn thành, Dữ liệu không hợp lệ**   1. Tại bước 8, Hệ thống phát hiện thiếu thông tin bắt buộc hoặc file không đúng định dạng hoặc nếu học viên được đánh dấu “Hoàn thành” nhưng không upload file chứng chỉ (trong trường hợp bắt buộc). 2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. |

### 4.47. Use Case: Xem các thông tin trong hồ sơ cá nhân của nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem các thông tin trong hồ sơ cá nhân của nhân sự** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng xem toàn bộ thông tin hồ sơ cá nhân của mình đang được lưu trong hệ thống, tra cứu lịch sử hợp đồng, hệ số, bậc lương và các quyết định khen thưởng, kỷ luật của bản thân. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng “Hồ sơ cá nhân” trên giao diện hệ thống. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập. |
| Điều kiện thành công  (Post-condition) | Thông tin hồ sơ cá nhân được hiển thị đầy đủ cho người dùng. |
| Điều kiện thất bại | Không thể hiển thị thông tin hồ sơ cá nhân do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng chọn chức năng xem hồ sơ cá nhân.  2. Hệ thống hiển thị đầy đủ thông tin theo các tab:   * **Tab "Thông tin chung":** Mã cán bộ, lý lịch, liên hệ, gia đình, ảnh chân dung. * **Tab "Trình độ & Chức danh":** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác. * **Tab "Thông tin Đảng/Đoàn":** Thông tin Đảng/Đoàn đã được lưu. * **Tab "Lương & Phụ cấp":** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng. * **Tab "Hợp đồng":** Thông tin về các loại hợp đồng đã ký. * **Tab "Khen thưởng/Kỷ luật":** Mục khen thưởng/kỷ luật chỉ hiển thị nếu Phòng TCCB đã cấu hình cho phép (xem UC 4.37, FEAT 8.9). * **Tab "Công tác":** Quá trình công tác. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.48. Use Case: Xem thông tin chi tiết đơn vị đang công tác

|  |  |
| --- | --- |
| **Tên use case** | **Xem thông tin chi tiết đơn vị đang công tác** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng xem thông tin chi tiết về đơn vị tổ chức mà mình đang công tác trong cơ cấu tổ chức của đơn vị, bao gồm thông tin cơ bản của đơn vị, danh sách chức vụ và nhân sự hiện tại trong đơn vị. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng xem thông tin đơn vị công tác từ hồ sơ cá nhân hoặc menu liên quan. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống. Người dùng đã được gán đơn vị công tác trong hệ thống. Đơn vị tổ chức đang tồn tại trong cơ cấu tổ chức. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết của đơn vị công tác được hiển thị đầy đủ và chính xác.  Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin do lỗi hệ thống hoặc không xác định được đơn vị công tác của người dùng. |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng truy cập chức năng xem thông tin đơn vị công tác. 2. Hệ thống xác định đơn vị mà người dùng đang trực thuộc.  3. Hệ thống hiển thị thông tin chi tiết của đơn vị, bao gồm:   * Tab **“Tổng quan”**: Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị (Đang hoạt động / Sáp nhập / Giải thể). * Tab **“Nhân sự”**: Danh sách nhân sự thuộc đơn vị, bao gồm Họ tên nhân sự, Mã cán bộ, Tên chức vụ, Ngày bắt đầu. * Tab **“Đơn vị trực thuộc”**: Danh sách các đơn vị dưới cấp trực thuộc đơn vị đang xem. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.49. Use Case: Thay đổi trạng thái đăng ký khóa đào tạo

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái đăng ký khóa đào tạo** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng đăng ký hoặc hủy đăng ký tham gia các khóa đào tạo do nhà trường tổ chức đang trong thời gian mở đăng ký, làm cơ sở cho việc quản lý học viên, theo dõi quá trình và ghi nhận kết quả đào tạo. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn menu “Đào tạo”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống. Khóa đào tạo tồn tại và đang ở trạng thái **“Đang mở đăng ký”**. Thời điểm hiện tại nằm trong khoảng **Thời gian mở đăng ký**. |
| Điều kiện thành công  (Post-condition) | Đăng ký tham gia khóa đào tạo của người dùng được ghi nhận trong hệ thống (trường hợp đăng ký). Bản ghi đăng ký của người dùng được xóa khỏi hệ thống (trường hợp hủy đăng ký). |
| Điều kiện thất bại | Không thể thay đổi trạng thái đăng ký do khóa đào tạo không hợp lệ, hết hạn đăng ký hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng truy cập menu “Đào tạo”.  2. Hệ thống hiển thị danh sách các khóa đào tạo ở trạng thái Đang mở đăng ký.  3. Người dùng chọn một khóa đào tạo để xem chi tiết thông tin.  4. Hệ thống hiển thị thông tin chi tiết khóa đào tạo. Nếu người dùng chưa đăng ký, hiển thị nút “Đăng ký tham gia”. Nếu người dùng đã đăng ký (trạng thái tham gia là “Đã đăng ký”), hiển thị nút “Hủy đăng ký”.  5. Người dùng nhấn nút “Đăng ký tham gia”.  6. Hệ thống kiểm tra các điều kiện đăng ký (thời gian mở đăng ký, số lượng đăng ký chưa đạt giới hạn, trạng thái khóa đào tạo).  7. Hệ thống tạo bản ghi đăng ký đào tạo và thiết lập trạng thái tham gia là “Đã đăng ký”.  8. Hệ thống thông báo đăng ký thành công cho người dùng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hủy đăng ký khóa đào tạo**   1. Tại bước 4, người dùng đã đăng ký khóa đào tạo này với trạng thái tham gia “Đã đăng ký”. Hệ thống hiển thị nút “Hủy đăng ký”. 2. Người dùng nhấn nút “Hủy đăng ký”. 3. Hệ thống yêu cầu xác nhận hủy đăng ký. 4. Người dùng xác nhận. 5. Hệ thống kiểm tra trạng thái tham gia phải là “Đã đăng ký” và khóa đào tạo phải đang ở trạng thái “Đang mở đăng ký”. 6. Hệ thống xóa bản ghi đăng ký đào tạo của người dùng. 7. Hệ thống thông báo hủy đăng ký thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hết thời gian đăng ký**   1. Tại bước 4, nếu thời gian hiện tại nằm ngoài khoảng mở đăng ký. 2. Hệ thống ẩn nút “Đăng ký tham gia” và “Hủy đăng ký”, hiển thị thông báo: *“Khóa đào tạo đã hết thời gian đăng ký.”*   **E2: Đã đủ số lượng người tham gia**   1. Tại bước 6, nếu số lượng đăng ký đã đạt giới hạn. 2. Hệ thống hiển thị thông báo: *“Khóa đào tạo đã đủ số lượng đăng ký.”*   **E3: Không thể hủy đăng ký**   1. Tại bước A1.5, nếu trạng thái tham gia không phải “Đã đăng ký” (ví dụ: đã chuyển sang “Đang học” do khóa đào tạo đã bắt đầu) hoặc khóa đào tạo không còn ở trạng thái “Đang mở đăng ký”. 2. Hệ thống hiển thị thông báo: *“Không thể hủy đăng ký do khóa đào tạo đã chuyển sang giai đoạn tiếp theo.”* |

### 4.50. Use Case: Xem danh sách các khóa đào tạo đã đăng ký

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách các khóa đào tạo đã đăng ký** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng xem danh sách tất cả các khóa đào tạo mà mình đã đăng ký tham gia, theo dõi trạng thái tham gia và kết quả đào tạo của từng khóa (Đã đăng ký, Đang học, Hoàn thành, Không đạt), phục vụ việc tra cứu, theo dõi quá trình học tập và kết quả đào tạo cá nhân. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Chọn menu "Đào tạo" |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống. Người dùng đã từng đăng ký ít nhất một khóa đào tạo. |
| Điều kiện thành công  (Post-condition) | Danh sách các khóa đào tạo đã đăng ký của người dùng được hiển thị đầy đủ và chính xác. Trạng thái tham gia và kết quả đào tạo của từng khóa được hiển thị đúng theo dữ liệu do Phòng TCCB ghi nhận. |
| Điều kiện thất bại | Không hiển thị được danh sách do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng truy cập chức năng **“Khóa đào tạo đã đăng ký”**.  2. Hệ thống truy xuất danh sách các khóa đào tạo mà người dùng đã đăng ký.  3. Hệ thống hiển thị danh sách khóa đào tạo, bao gồm các thông tin:   * Tên khóa đào tạo * Loại khóa đào tạo * Thời gian đào tạo (từ ngày – đến ngày) * Đơn vị/địa điểm tổ chức * Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành) * Trạng thái tham gia của cá nhân (Đã đăng ký, Đang học, Hoàn thành, Không đạt). |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

