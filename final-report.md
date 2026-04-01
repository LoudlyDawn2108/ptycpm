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
| Yêu cầu của các bên liên quan | STRQ | Yêu cầu của các bên liên quan (STR) | Mô tả các nhu cầu, mong đợi và mục tiêu chính của người dùng và các bên liên quan đối với hệ thống. |
| Yêu cầu tính năng | FEAT | Tài liệu tầm nhìn (VIS) | Mô tả các điều kiện, khả năng và các tính năng tổng quát mà hệ thống cần cung cấp. |
| Ca sử dụng | UC | Đặc tả ca sử dụng (UCS) | Mô tả chi tiết các ca sử dụng dưới dạng tương tác giữa tác nhân và hệ thống, phản ánh các yêu cầu chức năng. Mỗi UC có một tài liệu đặc tả riêng. |
| Kịch bản | SCEN | Đặc tả ca sử dụng (UCS) | Mô tả các đường đi hợp lệ qua một ca sử dụng (luồng cơ bản và luồng thay thế). |
| Yêu cầu bổ sung | SUPL | Đặc tả bổ sung (SS) | Mô tả các yêu cầu phi chức năng và các ràng buộc của hệ thống không được thể hiện trong mô hình ca sử dụng. |

### 1.2.2. Loại tài liệu yêu cầu cho dự án

| Loại tài liệu | Viết tắt | Mô tả | Loại yêu cầu mặc định |
| --- | --- | --- | --- |
| Kế hoạch quản lý yêu cầu | RMP | Tài liệu mô tả phương pháp, quy trình và công cụ quản lý yêu cầu của dự án. | Không áp dụng |
| Yêu cầu của các bên liên quan | STRQ | Tập hợp các yêu cầu nghiệp vụ và mong đợi chính từ các bên liên quan. | Yêu cầu bên liên quan (STRQ) |
| Tài liệu tầm nhìn | VIS | Mô tả tổng quan hệ thống, phạm vi và các mục tiêu chính của dự án. | Yêu cầu tính năng (FEAT) |
| Đặc tả ca sử dụng | UCS | Mô tả chi tiết các ca sử dụng và cách người dùng tương tác với hệ thống. Mỗi UC có một tài liệu UCS riêng. | Ca sử dụng (UC) |
| Đặc tả bổ sung | SS | Mô tả các yêu cầu phi chức năng và các ràng buộc của hệ thống. | Yêu cầu bổ sung (SUPL) |

## 1.3. Bảng liên lạc với các nhân tố chính (Stakeholder)

### 1.3.1. Các nhân tố chính

| STT | Nhân tố chính | Vai trò trong dự án | Đơn vị | Trách nhiệm chính | Hình thức liên lạc |
| --- | --- | --- | --- | --- | --- |
| 1 | Ban Giám hiệu | Nhà tài trợ / Phê duyệt | Ban Giám hiệu | Phê duyệt yêu cầu, xem xét báo cáo tổng hợp | Họp định kỳ, báo cáo |
| 2 | Phòng Tổ chức – Cán bộ | Người sử dụng chính | Phòng TCCB | Cung cấp yêu cầu quản lý hồ sơ nhân sự | Họp, email |
| 3 | Phòng Tài chính – Kế toán | Người sử dụng chính | Phòng TCKT | Cung cấp yêu cầu về lương, phụ cấp | Họp, trao đổi trực tiếp |
| 4 | Phòng CNTT | Đơn vị kỹ thuật | Phòng CNTT | Tư vấn kỹ thuật, hạ tầng, bảo mật | Họp kỹ thuật |
| 5 | Cán bộ viên chức | Người sử dụng chính | Toàn bộ nhân sự trường Đại học Thủy Lợi | Góp ý, xác nhận yêu cầu quản lý hồ sơ cá nhân | Họp, khảo sát |
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

STRQ ──→ FEAT ──→ UC ──→ SCEN
 │ │
 │ └──→ SUPL
 └──→ SUPL

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

Tên hoặc số hiệu của iteration mà tính năng dự kiến được tích hợp vào sản phẩm. Kiểu dữ liệu: **Văn bản** (ví dụ: “Iteration 1”, “Construction-2”).

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
| Lý do (Reason) | Văn bản | Tự do — ghi nhận nguồn gốc nhu cầu (ví dụ: “Phòng TCCB yêu cầu trong buổi phỏng vấn ngày 10/01”) |

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.5.1.

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
| **Tác nhân (Actor)** | Văn bản | Tên tác nhân khởi tạo UC (ví dụ: “Quản trị viên”, “Phòng TCCB”, “Người dùng”, “Hệ thống”) |

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.5.1.

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

### 1.5.5. Bảng tổng hợp thuộc tính theo kiểu yêu cầu

| Thuộc tính | STRQ | FEAT | UC | SUPL |
| --- | --- | --- | --- | --- |
| Trạng thái (Status) | x | x | x | x |
| Độ ưu tiên (Priority) | x | x | x | x |
| Lợi ích (Benefit) | x | x | x | x |
| Công sức (Effort) | x | x | x | x |
| Rủi ro (Risk) | x | x | x | x |
| Độ ổn định (Stability) | x | x | x | x |
| Độ khó (Difficulty) | - | x | - | - |
| Bản phát hành mục tiêu (Target Release) | - | x | x | x |
| Người phụ trách (Assigned To) | - | x | - | - |
| Lý do (Reason) | x | x | x | x |
| Kỹ thuật biến đổi (Transformation) | - | x | - | - |
| Tác nhân (Actor) | - | - | x | —- |

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
| Ma trận UC → Design | Mỗi UC ánh xạ tới (các) artefact thiết kế tương ứng; trong baseline hiện tại neo chính là class-diagram.md |

# II. PHỎNG VẤN BÊN LIÊN QUAN

## 2.1. Bảng phân công thành viên

| Thành viên | STRQs | FEATs |
| --- | --- | --- |
| Nguyễn Hồng Phúc | 1–3 | 1.1–3.5 (15) |
| Nguyễn Hải Ninh | 4–6 | 4.1–6.2 (11) |
| Ngô Quang Tùng | 7–8 | 7.1–8.9 (13) |
| Ngô Đức Nam Khánh | 9–12 | 9.1–12.4 (14) |

## 2.2. Nội dung tổng hợp STRQ và FEAT theo thành viên

### 2.2.1. Phần đóng góp của Nguyễn Hồng Phúc (STRQ 1–3, 13–16)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 1.1:** Hệ thống cho phép người dùng đăng nhập bằng tài khoản. * **FEAT 1.2:** Hệ thống cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng. * **FEAT 1.3:** Hệ thống tự động đăng xuất khỏi phiên làm việc nếu người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web trong 30 phút. * **FEAT 1.4:** Hệ thống cho phép người dùng đổi mật khẩu tài khoản đang sử dụng. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 2.1:** Hệ thống cho phép quản trị viên tìm kiếm tài khoản người dùng. * **FEAT 2.2:** Hệ thống cho phép quản trị viên thêm mới tài khoản người dùng. * **FEAT 2.3:** Hệ thống cho phép quản trị viên sửa tài khoản người dùng. * **FEAT 2.4:** Hệ thống cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống theo các vai trò chức năng được định nghĩa sẵn: Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự (Cán bộ/Giảng viên/Nhân viên). * **FEAT 2.5:** Hệ thống cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Đang hoạt động/Bị khóa). * **FEAT 2.6:** Hệ thống tự động khóa tài khoản của nhân sự đã được đánh dấu thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | * Phân tách * Làm cho đầy đủ | * **FEAT 3.1:** Hệ thống cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự. * **FEAT 3.2:** Hệ thống cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự. * **FEAT 3.3:** Hệ thống cho phép quản trị viên và phòng TCCB giải thể đơn vị tổ chức nhân sự; khi giải thể, hệ thống chuyển hợp đồng đang hiệu lực sang trạng thái Hết hiệu lực, trạng thái hợp đồng nhân sự sang Chưa hợp đồng, trạng thái làm việc sang Đang chờ xét và xóa liên kết đơn vị công tác khỏi hồ sơ nhân sự. * **FEAT 3.4:** Hệ thống cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. * **FEAT 3.5:** Hệ thống cho phép quản trị viên và phòng TCCB sáp nhập đơn vị tổ chức nhân sự vào đơn vị nhận sáp nhập; hệ thống chuyển nhân sự và đơn vị con sang đơn vị nhận sáp nhập với trạng thái hợp đồng và trạng thái làm việc giữ nguyên. |
| **STRQ 13:** Hệ thống phải tuân thủ các quy định về bảo vệ dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP, bao gồm quản lý sự đồng ý thu thập dữ liệu và xử lý yêu cầu ẩn danh hóa dữ liệu khi có yêu cầu hợp lệ. | * Làm cho đầy đủ * Phân tách | * **FEAT 13.1:** Hệ thống cho phép ghi nhận, xem lịch sử và thu hồi sự đồng ý thu thập dữ liệu cá nhân cho từng cán bộ, theo Nghị định 13/2023/NĐ-CP. * **FEAT 13.2:** Hệ thống phải xử lý yêu cầu ẩn danh hóa dữ liệu cá nhân (thay thế thông tin định danh bằng dữ liệu ẩn danh) khi có yêu cầu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên, theo Nghị định 13/2023/NĐ-CP. |
| **STRQ 14:** Hệ thống cần được triển khai dưới dạng ứng dụng web để toàn bộ cán bộ, nhân viên có thể truy cập từ trình duyệt trên máy tính văn phòng mà không cần cài đặt phần mềm riêng. | * Thêm chi tiết | * **FEAT 14.1:** Hệ thống được cung cấp dưới dạng ứng dụng web nhiều người dùng; frontend dạng SPA giao tiếp với backend thông qua RESTful API của hệ thống. |
| **STRQ 15:** Cơ cấu tổ chức của trường cần được thể hiện theo cấu trúc phân cấp từ cấp trường xuống các đơn vị trực thuộc, phản ánh đúng mối quan hệ quản lý giữa các đơn vị. | * Thêm chi tiết | * **FEAT 15.1:** Hệ thống cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi. |
| **STRQ 16:** Mật khẩu người dùng phải được bảo vệ an toàn khi lưu trữ, không cho phép khôi phục nguyên văn nhằm ngăn ngừa rò rỉ dữ liệu xác thực khi cơ sở dữ liệu bị xâm nhập. | * Thêm chi tiết | * **FEAT 16.1:** Hệ thống phải lưu trữ mọi mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu ở dạng văn bản thuần. |

### 2.2.2. Phần đóng góp của Nguyễn Hải Ninh (STRQ 4–6)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 4:** Phòng TCCB có thể cấu hình lương, loại phụ cấp, loại hợp đồng. | * Phân tách * Làm cho đầy đủ | * **FEAT 4.1:** Hệ thống cho phép phòng TCCB thêm mới hệ số lương (Hệ số lương được thêm sẽ được dùng làm thông tin cho hồ sơ). * **FEAT 4.2:** Hệ thống cho phép phòng TCCB sửa thông tin đối với hệ số lương chưa được hồ sơ nào sử dụng, phục vụ sửa chữa nhập liệu lỗi. * **FEAT 4.3:** Hệ thống cho phép phòng TCCB xóa hệ số lương khi không được hồ sơ nào sử dụng, hoặc thay đổi trạng thái (đưa vào trạng thái ngừng sử dụng hoặc kích hoạt lại) nếu đã được sử dụng. * **FEAT 4.4:** Hệ thống cho phép phòng TCCB thêm mới, sửa và thay đổi trạng thái danh mục loại phụ cấp theo bộ danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt; các mục đã được tham chiếu trong dữ liệu nghiệp vụ không được xóa mà chỉ được chuyển giữa trạng thái "Đang sử dụng" và "Ngừng sử dụng". * **FEAT 4.5:** Hệ thống cho phép phòng TCCB thêm mới, sửa và thay đổi trạng thái danh mục loại hợp đồng theo bộ danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt; các mục đã được tham chiếu trong dữ liệu nghiệp vụ không được xóa mà chỉ được chuyển giữa trạng thái "Đang sử dụng" và "Ngừng sử dụng". |
| **STRQ 5:** Phòng TCKT và TCCB muốn thống kê chi tiết về nhân sự. | * Phân tách * Thêm chi tiết | * **FEAT 5.1:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê tổng quan nhân sự và biến động nhân sự. * **FEAT 5.2:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh. * **FEAT 5.3:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê hợp đồng, tình trạng làm việc, đánh giá cán bộ. * **FEAT 5.4:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê đào tạo, phát triển, bổ nhiệm nhân sự. |
| **STRQ 6:** Hệ thống yêu cầu tự động log dấu vết hoạt động người dùng (System Logging). | * Phân tách * Thêm chi tiết | * **FEAT 6.1:** Hệ thống tự động ghi vết tất cả các tác vụ truy cập tài khoản, thay đổi/cập nhật hệ thống hoặc dữ liệu. * **FEAT 6.2:** Hệ thống cho phép quản trị viên truy xuất xem và xuất Audit log (Nhật ký hệ thống) nhằm truy vết hoạt động. |

### 2.2.3. Phần đóng góp của Ngô Quang Tùng (STRQ 7–8)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 7:** Phòng TCCB có thể tạo hợp đồng lao động của nhân sự. | * Làm rõ * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 7.1:** Hệ thống cho phép phòng TCCB tạo hợp đồng cho nhân sự không có hợp đồng hoặc cần gia hạn hợp đồng. * **FEAT 7.2:** Hệ thống cho phép phòng TCCB xem danh sách và chi tiết hợp đồng lao động của nhân sự. * **FEAT 7.3:** Hệ thống cho phép phòng TCCB chỉnh sửa hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực. * **FEAT 7.4:** Hệ thống cho phép phòng TCCB chấm dứt hợp đồng lao động trước hạn của nhân sự. |
| **STRQ 8:** Phòng TCCB muốn quản lý hồ sơ nhân sự như thêm, sửa hồ sơ và cho phép đánh dấu thôi việc nếu nhân sự không còn làm việc, có thêm phương pháp tìm kiếm và lọc để tiện quản lý. | * Phân tách * Làm rõ * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 8.1:** Hệ thống cho phép phòng TCCB và phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa. * **FEAT 8.2:** Hệ thống cho phép phòng TCCB và phòng TCKT lọc đa tiêu chí hồ sơ nhân sự. * **FEAT 8.3:** Hệ thống cho phép phòng TCCB thêm mới hồ sơ nhân sự (gồm nhập tay hoặc upload từ Excel) và tự động cấp mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng tại thời điểm tạo hồ sơ. * **FEAT 8.4:** Hệ thống cho phép phòng TCCB chỉnh sửa hồ sơ nhân sự (thông tin cá nhân, trình độ học vấn, khen thưởng/kỷ luật, quá trình công tác, thông tin hợp đồng). * **FEAT 8.5:** Hệ thống cho phép phòng TCCB đánh dấu thôi việc nhân sự. * **FEAT 8.6:** Hệ thống tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. * **FEAT 8.7:** Hệ thống cho phép phòng TCCB và phòng TCKT xem chi tiết hồ sơ nhân sự theo từng chế độ xem. * **FEAT 8.8:** Hệ thống cho phép phòng TCCB và phòng TCKT in hoặc xuất Excel hồ sơ nhân sự. * **FEAT 8.9:** Hệ thống cho phép phòng TCCB cấu hình ẩn/hiện các mục khen thưởng, kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc phòng TCCB. |

### 2.2.4. Phần đóng góp của Ngô Đức Nam Khánh (STRQ 9–12)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 9:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 9.1:** Hệ thống cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự. * **FEAT 9.2:** Hệ thống cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác. * **FEAT 9.3:** Hệ thống cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 10:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 10.1:** Hệ thống cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật). * **FEAT 10.2:** Hệ thống cho phép phòng TCCB xem lịch sử đánh giá khen thưởng và kỷ luật của nhân sự. * **FEAT 10.3:** Hệ thống cho phép phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo nhân sự, loại đánh giá, hoặc khoảng thời gian. |
| **STRQ 11:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 11.1:** Hệ thống cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ. * **FEAT 11.2:** Hệ thống cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành); khi khóa đào tạo được chuyển sang trạng thái "Đang đào tạo", hệ thống phải tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang "Đang học". * **FEAT 11.3:** Hệ thống cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký. * **FEAT 11.4:** Hệ thống cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
| **STRQ 12:** Người dùng phần mềm có thể xem hồ sơ cá nhân, xem thông tin đơn vị đang công tác và thực hiện các luồng tác vụ cá nhân. | * Phân tách * Làm rõ * Thêm chi tiết | * **FEAT 12.1:** Hệ thống cho phép người dùng xem thông tin cá nhân của bản thân. * **FEAT 12.2:** Hệ thống cho phép người dùng xem thông tin đơn vị mình đang công tác và cơ cấu các thành phần đơn vị trực thuộc. * **FEAT 12.3:** Hệ thống cho phép người dùng đăng ký hoặc hủy đăng ký tham gia khóa học/đào tạo được nhà trường phê duyệt mở. * **FEAT 12.4:** Hệ thống cho phép người dùng xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. |

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

**Ghi chú:** Tổng cộng hệ thống bao gồm **49 Use Case** (UC 4.1 – UC 4.50, bỏ qua UC 4.15), được phân nhóm theo chức năng như sau:

**► Nhóm UC Hệ thống & Tài khoản:**

* UC Đăng nhập
* UC Đăng xuất
* UC Đổi mật khẩu
* UC Tìm kiếm tài khoản người dùng
* UC Thêm mới tài khoản người dùng
* UC Sửa thông tin tài khoản người dùng
* UC Thay đổi trạng thái cho tài khoản người dùng
* UC Xem nhật ký hệ thống (Audit Log)

**► Nhóm UC Quản lý Cơ cấu tổ chức:**

* UC Tạo mới đơn vị tổ chức nhân sự
* UC Sửa thông tin đơn vị tổ chức nhân sự
* UC Giải thể đơn vị tổ chức nhân sự
* UC Xem chi tiết thông tin đơn vị tổ chức nhân sự
* UC Sáp nhập đơn vị tổ chức nhân sự
* UC Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự
* UC Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự

**► Nhóm UC Danh mục Cấu hình:**

* UC Thêm mới danh mục hệ số lương
* UC Sửa danh mục hệ số lương
* UC Thay đổi trạng thái danh mục hệ số lương
* UC Thêm mới danh mục loại phụ cấp
* UC Sửa danh mục loại phụ cấp
* UC Thay đổi trạng thái danh mục loại phụ cấp
* UC Thêm mới danh mục loại hợp đồng
* UC Sửa danh mục loại hợp đồng
* UC Thay đổi trạng thái danh mục loại hợp đồng

**► Nhóm UC Báo cáo & Nhật ký hệ thống:**

* UC Xem chi tiết các thống kê
* UC Xem nhật ký hệ thống (Audit Log)

**► Nhóm UC Quản lý Hồ sơ nhân sự:**

* UC Thêm mới Hợp đồng lao động
* UC Xem danh sách và chi tiết hợp đồng lao động
* UC Chỉnh sửa hợp đồng lao động chưa có hiệu lực
* UC Chấm dứt hợp đồng lao động trước hạn
* UC Tìm kiếm hồ sơ nhân sự
* UC Lọc danh sách hồ sơ nhân sự
* UC Thêm mới Hồ sơ nhân sự
* UC Chỉnh sửa trong chi tiết hồ sơ nhân sự
* UC Đánh dấu thôi việc nhân sự
* UC Thôi việc nhân sự tự động
* UC Xem Chi tiết thông tin hồ sơ nhân sự
* UC In và xuất Excel hồ sơ nhân sự
* UC Cấu hình ẩn/hiện mục khen thưởng/kỷ luật
* UC Ghi nhận đánh giá cho nhân sự
* UC Xem lịch sử đánh giá khen thưởng/kỷ luật
* UC Tìm kiếm và lọc danh sách đánh giá

**► Nhóm UC Quản lý Đào tạo:**

* UC Mở khóa đào tạo cho cán bộ giảng viên
* UC Sửa thông tin khóa đào tạo đã mở
* UC Xem chi tiết thông tin khóa đào tạo đã mở
* UC Ghi nhận kết quả đào tạo của cán bộ giảng viên

**► Nhóm UC Cá nhân (Self-service):**

* UC Xem các thông tin trong hồ sơ cá nhân của nhân sự
* UC Xem thông tin chi tiết đơn vị đang công tác
* UC Thay đổi trạng thái đăng ký khóa đào tạo
* UC Xem danh sách các khóa đào tạo đã đăng ký

## 3.3. Vẽ biểu đồ UCs (UC tổng quát, UC phân rã theo các tác nhân)

### 3.3.1. Biểu đồ Use Case tổng quát (Nguyễn Hồng Phúc)

**Ghi chú quan hệ giữa các UC:** UC 4.5 (Thêm tài khoản) và UC 4.6 (Sửa tài khoản) **<>** UC 4.7 (Phân quyền) để thực hiện phân quyền vai trò cho tài khoản trong cùng luồng tạo/sửa.

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

![Image: image_002](./report_images/image_002.png)

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

=![Image: image_003](./report_images/image_003.png)

**c. Phân rã cho Phòng Tài chính - Kế toán**

* **Tác nhân**: Phòng Tài chính - Kế toán
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Chế độ xem: Tìm kiếm, Xem và Lọc chi tiết hồ sơ nhân sự
  + Xem chi tiết các thống kê
  + Nhóm UC Cá nhân (Self-service): Xem hồ sơ cá nhân, Xem đơn vị công tác, Thay đổi trạng thái đăng ký đào tạo, Xem khóa đào tạo đã đăng ký *(kế thừa quyền Người dùng)*

![Image: image_004](./report_images/image_004.png)

**d. Phân rã cho Người dùng (Cán bộ/Giảng viên/Nhân viên)**

* **Tác nhân**: Người dùng
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Xem hồ sơ cá nhân
  + Xem thông tin chi tiết đơn vị công tác
  + Thay đổi trạng thái đăng ký đào tạo
  + Xem danh sách các khóa đào tạo đã đăng ký

![Image: image_005](./report_images/image_005.png)

### 3.3.3. Bảng phân công thành viên cho Use Case

| Thành viên | UCs |
| --- | --- |
| Nguyễn Hồng Phúc | 4.1–4.12 (12) |
| Nguyễn Hải Ninh | 4.13–4.24 (12) |
| Ngô Quang Tùng | 4.25–4.37 (13) |
| Ngô Đức Nam Khánh | 4.38–4.50 (13) |

### 3.3.4. Danh mục Use Case đã đánh số lại

* UC 4.1: Đăng nhập
* UC 4.2: Đăng xuất
* UC 4.3: Đổi mật khẩu
* UC 4.4: Tìm kiếm tài khoản người dùng
* UC 4.5: Thêm mới tài khoản người dùng
* UC 4.6: Sửa thông tin tài khoản người dùng
* UC 4.7: Thay đổi trạng thái cho tài khoản người dùng
* UC 4.8: Tạo mới đơn vị tổ chức nhân sự
* UC 4.9: Sửa thông tin đơn vị tổ chức nhân sự
* UC 4.10: Giải thể đơn vị tổ chức nhân sự
* UC 4.11: Xem chi tiết thông tin đơn vị tổ chức nhân sự
* UC 4.12: Sáp nhập đơn vị tổ chức nhân sự
* UC 4.13: Thêm mới danh mục hệ số lương
* UC 4.14: Sửa danh mục hệ số lương
* UC 4.16: Thay đổi trạng thái danh mục hệ số lương
* UC 4.17: Thêm mới danh mục loại phụ cấp
* UC 4.18: Sửa danh mục loại phụ cấp
* UC 4.19: Thay đổi trạng thái danh mục loại phụ cấp
* UC 4.20: Thêm mới danh mục loại hợp đồng
* UC 4.21: Sửa danh mục loại hợp đồng
* UC 4.22: Thay đổi trạng thái danh mục loại hợp đồng
* UC 4.23: Xem chi tiết các thống kê
* UC 4.24: Xem nhật ký hệ thống (Audit Log)
* UC 4.25: Thêm mới Hợp đồng lao động
* UC 4.26: Xem danh sách và chi tiết hợp đồng lao động
* UC 4.27: Chỉnh sửa hợp đồng lao động chưa có hiệu lực
* UC 4.28: Chấm dứt hợp đồng lao động trước hạn
* UC 4.29: Tìm kiếm hồ sơ nhân sự
* UC 4.30: Lọc danh sách hồ sơ nhân sự
* UC 4.31: Thêm mới Hồ sơ nhân sự
* UC 4.32: Chỉnh sửa trong chi tiết hồ sơ nhân sự
* UC 4.33: Đánh dấu thôi việc nhân sự
* UC 4.34: Thôi việc nhân sự tự động
* UC 4.35: Xem Chi tiết thông tin hồ sơ nhân sự
* UC 4.36: In và xuất Excel hồ sơ nhân sự
* UC 4.37: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật
* UC 4.38: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự
* UC 4.39: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự
* UC 4.40: Ghi nhận đánh giá cho nhân sự
* UC 4.41: Xem lịch sử đánh giá khen thưởng/kỷ luật
* UC 4.42: Tìm kiếm và lọc danh sách đánh giá
* UC 4.43: Mở khóa đào tạo cho cán bộ giảng viên
* UC 4.44: Sửa thông tin khóa đào tạo đã mở
* UC 4.45: Xem chi tiết thông tin khóa đào tạo đã mở
* UC 4.46: Ghi nhận kết quả đào tạo của cán bộ giảng viên
* UC 4.47: Xem các thông tin trong hồ sơ cá nhân của nhân sự
* UC 4.48: Xem thông tin chi tiết đơn vị đang công tác
* UC 4.49: Thay đổi trạng thái đăng ký khóa đào tạo
* UC 4.50: Xem danh sách các khóa đào tạo đã đăng ký

## 3.4. Ma trận truy vết yêu cầu (Traceability Matrix)

| FEAT | UC tương ứng |
| --- | --- |
| FEAT 1.1 | UC 4.1 (Đăng nhập) |
| FEAT 1.2 | UC 4.2 (Đăng xuất) |
| FEAT 1.3 | Ràng buộc hệ thống — hiện thực hóa bởi SUPL-F03 (không tách UC riêng) |
| FEAT 1.4 | UC 4.3 (Đổi mật khẩu) |
| FEAT 2.1 | UC 4.4 (Tìm kiếm tài khoản người dùng) |
| FEAT 2.2 | UC 4.5 (Thêm mới tài khoản người dùng) |
| FEAT 2.3 | UC 4.6 (Sửa thông tin tài khoản người dùng) |
| FEAT 2.4 | Ràng buộc thiết kế — hiện thực hóa bởi SUPL-DC03 (không tách UC riêng); gán vai trò tích hợp trong UC 4.5 và UC 4.6 |
| FEAT 2.5 | UC 4.7 (Thay đổi trạng thái cho tài khoản người dùng) |
| FEAT 2.6 | Ràng buộc hệ thống — hiện thực hóa bởi SUPL-F04 (không tách UC riêng) |
| FEAT 3.1 | UC 4.8 (Tạo mới đơn vị tổ chức nhân sự) |
| FEAT 3.2 | UC 4.9 (Sửa thông tin đơn vị tổ chức nhân sự) |
| FEAT 3.3 | UC 4.10 (Giải thể đơn vị tổ chức nhân sự) |
| FEAT 3.4 | UC 4.11 (Xem chi tiết thông tin đơn vị tổ chức nhân sự) |
| FEAT 3.5 | UC 4.12 (Sáp nhập đơn vị tổ chức nhân sự) |
| FEAT 4.1 | UC 4.13 (Thêm mới danh mục hệ số lương) |
| FEAT 4.2 | UC 4.14 (Sửa danh mục hệ số lương) |
| FEAT 4.3 | UC 4.16 (Thay đổi trạng thái danh mục hệ số lương) |
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
| FEAT 13.1 | Ràng buộc pháp lý — được hiện thực hóa bởi SUPL-LR01 (không tách UC riêng) |
| FEAT 13.2 | Ràng buộc pháp lý — được hiện thực hóa bởi SUPL-LR04 (không tách UC riêng) |
| FEAT 14.1 | Ràng buộc thiết kế — hiện thực hóa bởi SUPL-DC01 (không tách UC riêng) |
| FEAT 15.1 | Ràng buộc thiết kế — hiện thực hóa bởi SUPL-DC02 (không tách UC riêng) |
| FEAT 16.1 | Ràng buộc bảo mật — hiện thực hóa bởi SUPL-F08 (không tách UC riêng); áp dụng tại UC 4.3 và UC 4.5 |

# VI. CÁC YÊU CẦU BỔ SUNG

## 6.1 Functionality — Phúc

### Danh sách yêu cầu

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
| --- | --- | --- | --- | --- |
| **SUPL-F01** | Ghi nhật ký kiểm toán tự động | Hệ thống phải tự động ghi nhật ký cho mọi thao tác truy cập tài khoản, thay đổi dữ liệu, thay đổi trạng thái và thay đổi cấu hình, kèm thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. | FEAT 12.1 | **M** |
| **SUPL-F02** | Tự động cấp mã cán bộ | Khi tạo mới hồ sơ nhân sự, hệ thống phải tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. | FEAT 7.3 | **M** |
| **SUPL-F03** | Tự động đăng xuất phiên không hoạt động | Hệ thống phải tự động đăng xuất phiên làm việc sau 30 phút không có tương tác của người dùng trên giao diện. | FEAT 1.3 | **M** |
| **SUPL-F04** | Tự động khóa tài khoản nhân sự thôi việc | Khi nhân sự được chuyển sang trạng thái thôi việc, hệ thống phải tự động khóa tài khoản liên kết của nhân sự đó. | FEAT 2.6 | **M** |
| **SUPL-F05** | Tự động chuyển trạng thái hợp đồng | Hệ thống phải tự động chuyển hợp đồng từ trạng thái "Còn hiệu lực" sang "Chờ gia hạn" khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. | FEAT 5.1 | **M** |
| **SUPL-F06** | Tự động cập nhật trạng thái đăng ký đào tạo | Khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang "Đang đào tạo", hệ thống phải tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang "Đang học". | FEAT 8.2 | **M** |
| **SUPL-F07** | Ngừng sử dụng / kích hoạt lại loại phụ cấp | Hệ thống phải cho phép chuyển loại phụ cấp đã được tham chiếu trong dữ liệu nghiệp vụ sang trạng thái ngừng sử dụng hoặc kích hoạt lại mà không làm mất liên kết dữ liệu lịch sử; loại phụ cấp đã được tham chiếu không được xóa. | FEAT 4.4 | **M** |
| **SUPL-F08** | Bảo vệ mật khẩu lưu trữ | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu ở dạng văn bản thuần. | FEAT 16.1 | **M** |
| **SUPL-F09** | Ngừng sử dụng / kích hoạt lại loại hợp đồng | Hệ thống phải cho phép chuyển loại hợp đồng đã được tham chiếu trong dữ liệu nghiệp vụ sang trạng thái ngừng sử dụng hoặc kích hoạt lại mà không làm mất liên kết dữ liệu lịch sử; loại hợp đồng đã được tham chiếu không được xóa. | FEAT 4.5 | **M** |

### Độ đo và tiêu chuẩn đáp ứng

| SUPL | Yếu tố chất lượng | Độ đo yêu cầu | Tiêu chuẩn đáp ứng |
| --- | --- | --- | --- |
| **SUPL-F01** | Tính đúng đắn – Khả năng kiểm toán | (1) Tỷ lệ thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) Tỷ lệ bản ghi có đủ 9 trường bắt buộc. | (1) 100% thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) 100% bản ghi có đủ 9/9 trường bắt buộc. |
| **SUPL-F02** | Tính đúng đắn | (1) Tỷ lệ mã cán bộ bị trùng; (2) Tỷ lệ mã được sinh đúng mẫu; (3) Tỷ lệ hồ sơ mới được cấp mã ngay khi tạo. | (1) 0% mã cán bộ bị trùng; (2) 100% mã được sinh đúng mẫu đang áp dụng; (3) 100% hồ sơ mới được cấp mã ngay khi tạo thành công. |
| **SUPL-F03** | Tính đúng đắn – Tự động hóa | Thời gian từ lần tương tác cuối cùng của người dùng đến khi hệ thống đăng xuất phiên làm việc. | Hệ thống tự động đăng xuất sau 30 phút không có tương tác của người dùng trên giao diện, với sai số không quá ±30 giây. |
| **SUPL-F04** | Tính đúng đắn – Tự động hóa | (1) Thời gian từ khi nhân sự được đánh dấu thôi việc đến khi tài khoản bị khóa; (2) Tỷ lệ tài khoản liên kết được khóa tự động đúng quy tắc. | (1) Tài khoản bị khóa trong không quá 1 phút; (2) 100% tài khoản liên kết của nhân sự thôi việc bị khóa tự động. |
| **SUPL-F05** | Tính đúng đắn – Tự động hóa | (1) Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái "Chờ gia hạn"; (2) Độ trễ từ thời điểm hợp đồng chạm ngưỡng đến khi trạng thái được cập nhật. | (1) 100% hợp đồng đủ điều kiện được chuyển đúng trạng thái; (2) Việc cập nhật hoàn tất trong không quá 24 giờ kể từ thời điểm đủ điều kiện. |
| **SUPL-F06** | Tính đúng đắn – Tự động hóa | (1) Tỷ lệ đăng ký của khóa đang ở trạng thái "Đã đăng ký" được cập nhật đúng trạng thái khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang "Đang đào tạo"; (2) Độ trễ từ thời điểm khóa đào tạo đổi trạng thái đến khi cập nhật xong toàn bộ đăng ký. | (1) 100% đăng ký của khóa đang ở trạng thái "Đã đăng ký" được chuyển sang "Đang học"; (2) Hoàn tất cập nhật trong không quá 1 phút. |
| **SUPL-F07** | Tính toàn vẹn | (1) Tỷ lệ loại phụ cấp đã được tham chiếu vẫn bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) Số loại phụ cấp đã được tham chiếu nhưng vẫn bị xóa. | (1) 100% loại phụ cấp đã được tham chiếu bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) 0 loại phụ cấp đã được tham chiếu bị xóa. |
| **SUPL-F08** | Bảo mật – Tính bí mật | (1) Tỷ lệ mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; (2) Số mật khẩu được lưu ở dạng văn bản thuần. | (1) 100% mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; (2) 0 mật khẩu được lưu ở dạng văn bản thuần. |
| **SUPL-F09** | Tính toàn vẹn | (1) Tỷ lệ loại hợp đồng đã được tham chiếu vẫn bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) Số loại hợp đồng đã được tham chiếu nhưng vẫn bị xóa. | (1) 100% loại hợp đồng đã được tham chiếu bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) 0 loại hợp đồng đã được tham chiếu bị xóa. |

## 6.2 Design Constraints — Phúc

### Danh sách yêu cầu

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
| --- | --- | --- | --- | --- |
| **SUPL-DC01** | Kiến trúc Client-Server SPA + RESTful API | Hệ thống phải xây dựng theo mô hình Client-Server, frontend dạng SPA (Single Page Application) giao tiếp với backend qua RESTful API. | FEAT 14.1 | **M** |
| **SUPL-DC02** | Cơ cấu tổ chức dạng cây | Hệ thống phải biểu diễn cơ cấu tổ chức dưới dạng cây cha-con với một nút gốc duy nhất là Trường Đại học Thủy Lợi; hệ thống cho phép đánh dấu đơn vị là đơn vị nút (leaf node) để ngăn chặn việc tạo đơn vị con trực thuộc. | FEAT 15.1 | **M** |
| **SUPL-DC03** | Phân quyền theo vai trò | Hệ thống phải áp dụng phân quyền theo vai trò; mỗi chức năng và API chỉ cho phép truy cập bởi vai trò được cấp quyền. | FEAT 2.4 | **M** |

### Độ đo và tiêu chuẩn đáp ứng

| SUPL | Yếu tố chất lượng | Độ đo yêu cầu | Tiêu chuẩn đáp ứng |
| --- | --- | --- | --- |
| **SUPL-DC01** | Ràng buộc thiết kế – Kiến trúc | (1) Số endpoint giao tiếp client-server không sử dụng RESTful API; (2) Số trang frontend yêu cầu full-page reload (ngoại trừ lần tải đầu tiên). | (1) 0 endpoint giao tiếp client-server ngoài RESTful API (JSON); (2) 0 trang frontend yêu cầu full-page reload (ngoại trừ lần tải đầu tiên). |
| **SUPL-DC02** | Ràng buộc thiết kế – Mô hình dữ liệu | (1) Số nút gốc trong cây tổ chức; (2) Số chu trình trong quan hệ cha-con; (3) Tỷ lệ đơn vị có liên kết cha-con hợp lệ; (4) Số đơn vị nút có đơn vị con trực thuộc. | (1) Có đúng 1 nút gốc là Trường Đại học Thủy Lợi; (2) 0 chu trình; (3) 100% đơn vị có liên kết cha-con hợp lệ; (4) 0 đơn vị nút có đơn vị con trực thuộc. |
| **SUPL-DC03** | Ràng buộc thiết kế – Phân quyền | (1) Số vai trò được định nghĩa trong mô hình phân quyền; (2) Tỷ lệ chức năng và API có ma trận quyền rõ ràng; (3) Số trường hợp truy cập trái quyền. | (1) Định nghĩa đúng 4 vai trò: Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự; (2) 100% chức năng và API có ma trận quyền rõ ràng; (3) 0 trường hợp truy cập trái quyền. |

## 6.3 Legal/Regulatory — Phúc

### Danh sách yêu cầu

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
| --- | --- | --- | --- | --- |
| **SUPL-LR01** | Quản lý sự đồng ý thu thập dữ liệu | Hệ thống phải cho phép ghi nhận, xem lịch sử và thu hồi sự đồng ý thu thập dữ liệu cá nhân cho từng cán bộ, theo Nghị định 13/2023/NĐ-CP. | FEAT 13.1 | **M** |
| **SUPL-LR02** | Danh mục loại hợp đồng được phê duyệt | Hệ thống chỉ cho phép cấu hình và sử dụng loại hợp đồng thuộc danh mục được nhà trường phê duyệt. | FEAT 4.5 | **M** |
| **SUPL-LR03** | Lưu trữ hồ sơ nhân sự 75 năm | Hồ sơ nhân sự phải được lưu trữ tối thiểu 75 năm kể từ ngày tạo hồ sơ. | FEAT 7.3 | **M** |
| **SUPL-LR04** | Ẩn danh hóa dữ liệu cá nhân | Hệ thống phải xử lý yêu cầu ẩn danh hóa dữ liệu cá nhân (thay thế thông tin định danh bằng dữ liệu ẩn danh) khi có yêu cầu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên, theo Nghị định 13/2023/NĐ-CP. | FEAT 13.2 | **M** |
| **SUPL-LR05** | Danh mục loại phụ cấp được phê duyệt | Hệ thống chỉ cho phép cấu hình và sử dụng loại phụ cấp thuộc danh mục được nhà trường phê duyệt. | FEAT 4.4 | **M** |
| **SUPL-LR06** | Lưu trữ hợp đồng lao động 10 năm | Hợp đồng lao động phải được lưu trữ tối thiểu 10 năm sau khi hợp đồng chấm dứt. | FEAT 5.1 | **M** |
| **SUPL-LR07** | Lưu trữ đánh giá khen thưởng/kỷ luật 10 năm | Lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu 10 năm kể từ bản ghi đánh giá cuối cùng. | FEAT 6.1 | **M** |

### Độ đo và tiêu chuẩn đáp ứng

| SUPL | Yếu tố chất lượng | Độ đo yêu cầu | Tiêu chuẩn đáp ứng |
| --- | --- | --- | --- |
| **SUPL-LR01** | Ràng buộc pháp lý – Bảo vệ dữ liệu | (1) Tỷ lệ hồ sơ nhân sự có bản ghi đồng ý hợp lệ trước khi thu thập dữ liệu cá nhân; (2) Số thao tác ghi nhận, xem lịch sử, thu hồi đồng ý không khả dụng trên giao diện. | (1) 100% hồ sơ nhân sự có bản ghi đồng ý hợp lệ trước khi thu thập dữ liệu cá nhân; (2) 0 thao tác ghi nhận, xem lịch sử, thu hồi đồng ý bị thiếu trên giao diện. |
| **SUPL-LR02** | Ràng buộc pháp lý – Danh mục nghiệp vụ | (1) Tỷ lệ loại hợp đồng trong danh mục được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số loại hợp đồng ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. | (1) 100% loại hợp đồng trong danh mục được phê duyệt có thể cấu hình và sử dụng; (2) 0 loại hợp đồng ngoài danh mục được phê duyệt được phép sử dụng. |
| **SUPL-LR03** | Ràng buộc pháp lý – Lưu trữ | (1) Số hồ sơ nhân sự bị xóa hoặc mất trước 75 năm kể từ ngày tạo; (2) Số thao tác xóa hồ sơ nhân sự chưa hết thời hạn lưu trữ không bị hệ thống chặn. | (1) 0 hồ sơ nhân sự bị xóa hoặc mất trước 75 năm; (2) 0 thao tác xóa hồ sơ nhân sự chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |
| **SUPL-LR04** | Ràng buộc pháp lý – Bảo vệ dữ liệu | (1) Tỷ lệ yêu cầu ẩn danh hóa dữ liệu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên được thực hiện thành công và có lưu vết xử lý; (2) Số trường hợp thông tin định danh chưa được thay thế bằng dữ liệu ẩn danh sau khi yêu cầu hợp lệ đã được xử lý. | (1) 100% yêu cầu ẩn danh hóa hợp lệ được thực hiện thành công và lưu vết xử lý; (2) 0 trường hợp thông tin định danh chưa được thay thế sau khi yêu cầu hợp lệ đã được xử lý. |
| **SUPL-LR05** | Ràng buộc pháp lý – Danh mục nghiệp vụ | (1) Tỷ lệ loại phụ cấp trong danh mục được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số loại phụ cấp ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. | (1) 100% loại phụ cấp trong danh mục được phê duyệt có thể cấu hình và sử dụng; (2) 0 loại phụ cấp ngoài danh mục được phê duyệt được phép sử dụng. |
| **SUPL-LR06** | Ràng buộc pháp lý – Lưu trữ | (1) Số hợp đồng lao động bị xóa hoặc mất trước 10 năm kể từ ngày chấm dứt hợp đồng; (2) Số thao tác xóa hợp đồng chưa hết thời hạn lưu trữ không bị hệ thống chặn. | (1) 0 hợp đồng lao động bị xóa hoặc mất trước 10 năm kể từ ngày chấm dứt; (2) 0 thao tác xóa hợp đồng chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |
| **SUPL-LR07** | Ràng buộc pháp lý – Lưu trữ | (1) Số bản ghi đánh giá khen thưởng/kỷ luật bị xóa hoặc mất trước 10 năm kể từ bản ghi đánh giá cuối cùng; (2) Số thao tác xóa bản ghi đánh giá chưa hết thời hạn lưu trữ không bị hệ thống chặn. | (1) 0 bản ghi đánh giá bị xóa hoặc mất trước 10 năm; (2) 0 thao tác xóa bản ghi đánh giá chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |

## 6.4 Usability — Ninh

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-U01 | Hệ thống phải hiển thị nhãn, menu và nút thao tác bằng tiếng Việt trên các màn hình hồ sơ nhân sự, hợp đồng lao động, đào tạo, đánh giá và danh mục cấu hình. | FEAT 5.2, FEAT 6.2, FEAT 7.1, FEAT 8.3, FEAT 9.1, FEAT 4.4, FEAT 4.5 |
| 2 | SUPL-U02 | Trên các màn hình hồ sơ nhân sự, hợp đồng lao động, đào tạo, đánh giá và danh mục cấu hình, hệ thống phải dùng cùng font chữ mặc định. | FEAT 5.2, FEAT 6.2, FEAT 7.1, FEAT 8.3, FEAT 9.1, FEAT 4.4, FEAT 4.5 |
| 3 | SUPL-U03 | Trên các màn hình hồ sơ nhân sự, hợp đồng lao động, đào tạo, đánh giá và danh mục cấu hình, hệ thống phải dùng màu hiển thị nhất quán cho từng loại thông báo thành công, cảnh báo và lỗi. | FEAT 5.2, FEAT 6.2, FEAT 7.1, FEAT 8.3, FEAT 9.1, FEAT 4.4, FEAT 4.5 |
| 4 | SUPL-U04 | Trên các biểu mẫu cùng loại thuộc các màn hình hồ sơ nhân sự, hợp đồng lao động, đào tạo, đánh giá và danh mục cấu hình, hệ thống phải đặt nút xác nhận ở bên phải nút hủy hoặc quay lại. | FEAT 5.2, FEAT 6.2, FEAT 7.1, FEAT 8.3, FEAT 9.1, FEAT 4.4, FEAT 4.5 |
| 5 | SUPL-U05 | Sau tối đa 2 giờ hướng dẫn, ít nhất 95% người chưa từng sử dụng hệ thống trước đó và thuộc vai trò Phòng Tổ chức – Cán bộ (TCCB) phải hoàn thành tác vụ tìm kiếm hồ sơ nhân sự, xem chi tiết hồ sơ và cập nhật hồ sơ mà không cần người hướng dẫn trả lời câu hỏi, nhắc bước tiếp theo hoặc thao tác hộ trong khi thực hiện. | FEAT 7.1, FEAT 7.4, FEAT 8.7 |
| 6 | SUPL-U06 | Sau tối đa 2 giờ hướng dẫn, ít nhất 95% người chưa từng sử dụng hệ thống trước đó và thuộc vai trò Phòng Tài chính – Kế toán (TCKT) phải hoàn thành tác vụ tìm kiếm hồ sơ nhân sự, xem chi tiết hồ sơ và xuất hồ sơ nhân sự mà không cần người hướng dẫn trả lời câu hỏi, nhắc bước tiếp theo hoặc thao tác hộ trong khi thực hiện. | FEAT 7.1, FEAT 8.7, FEAT 8.8 |
| 7 | SUPL-U07 | Hệ thống phải hiển thị bằng tiếng Việt thông báo cho mỗi lỗi kiểm tra dữ liệu đầu vào và mỗi lỗi nghiệp vụ; mỗi thông báo phải nêu rõ ít nhất một trong các thông tin sau về nguyên nhân lỗi: trường dữ liệu, quy tắc nghiệp vụ hoặc điều kiện gây lỗi, đồng thời nêu rõ bước người dùng phải thực hiện để tiếp tục thao tác. | FEAT 5.1, FEAT 5.3, FEAT 6.1, FEAT 7.3, FEAT 7.4, FEAT 8.1, FEAT 8.2, FEAT 9.1, FEAT 4.4, FEAT 4.5 |
| 8 | SUPL-U08 | Hệ thống phải hiển thị thông báo lỗi hệ thống bằng tiếng Việt và mỗi thông báo phải kèm mã tra cứu duy nhất cho lần phát sinh lỗi để bộ phận kỹ thuật đối chiếu nhật ký hệ thống. | FEAT 12.1, FEAT 12.2 |
| 9 | SUPL-U09 | Hệ thống phải cho phép người dùng kết hợp ít nhất 3 tiêu chí lọc khi tìm kiếm hồ sơ nhân sự. | FEAT 7.1, FEAT 7.2 |
| 10 | SUPL-U10 | Từ danh sách hồ sơ nhân sự, người dùng phải mở được trang chi tiết của một hồ sơ trong tối đa 3 bước chức năng: nhập ít nhất một điều kiện tìm kiếm hoặc lọc, thực hiện lệnh tìm kiếm và chọn hồ sơ cần mở. | FEAT 7.1, FEAT 8.7 |
| 11 | SUPL-U11 | Ở độ phân giải 1366×768 trở lên, trên các màn hình hồ sơ nhân sự, hợp đồng lao động, đào tạo, đánh giá và danh mục cấu hình, hệ thống phải hiển thị tiêu đề trang, bộ lọc hoặc ô tìm kiếm (nếu có), vùng nội dung chính, nút thao tác chính và phân trang hoặc nút điều hướng (nếu có) trong vùng hiển thị mà không cần cuộn ngang. | FEAT 5.2, FEAT 6.2, FEAT 7.1, FEAT 8.3, FEAT 9.1, FEAT 4.4, FEAT 4.5 |
| 12 | SUPL-U12 | Ở độ phân giải từ 1024×768 đến dưới 1366×768, hệ thống phải cho phép thực hiện các tác vụ tìm kiếm hồ sơ, xem chi tiết hồ sơ, thêm mới hồ sơ và chỉnh sửa hồ sơ mà không cần cuộn ngang hoặc phóng to. | FEAT 7.1, FEAT 7.3, FEAT 7.4, FEAT 8.7 |
| 13 | SUPL-U13 | Hệ thống phải cho phép di chuyển bằng phím Tab theo thứ tự từ trên xuống dưới, từ trái sang phải của các trường nhập có thể thao tác trên các biểu mẫu thêm mới và chỉnh sửa hồ sơ nhân sự, hợp đồng lao động, khóa đào tạo, loại phụ cấp và loại hợp đồng. | FEAT 5.1, FEAT 5.3, FEAT 7.3, FEAT 7.4, FEAT 8.1, FEAT 8.2, FEAT 4.4, FEAT 4.5 |
| 14 | SUPL-U14 | Trên các biểu mẫu thêm mới và chỉnh sửa hồ sơ nhân sự, hợp đồng lao động, khóa đào tạo, loại phụ cấp và loại hợp đồng, khi con trỏ đang ở bất kỳ trường nhập nào, phím Enter phải kích hoạt nút hành động chính của biểu mẫu (Lưu, Thêm mới hoặc Cập nhật). | FEAT 5.1, FEAT 5.3, FEAT 7.3, FEAT 7.4, FEAT 8.1, FEAT 8.2, FEAT 4.4, FEAT 4.5 |
| 15 | SUPL-U15 | Hệ thống phải hiển thị đường dẫn điều hướng phân cấp (breadcrumb) trên mọi trang có cấu trúc danh sách → chi tiết → chỉnh sửa; mỗi mục breadcrumb phải mở đúng cấp trang tương ứng. | FEAT 5.2, FEAT 5.3, FEAT 7.1, FEAT 7.4, FEAT 8.7, FEAT 8.2, FEAT 8.3, FEAT 4.4, FEAT 4.5 |
| 16 | SUPL-U16 | Hệ thống phải hiển thị hộp thoại xác nhận trước khi thực hiện các thao tác khóa hoặc mở khóa tài khoản, giải thể hoặc sáp nhập đơn vị, chấm dứt hợp đồng trước hạn, đánh dấu thôi việc, xóa hệ số lương, thay đổi trạng thái loại phụ cấp và thay đổi trạng thái loại hợp đồng. | FEAT 2.5, FEAT 3.3, FEAT 5.4, FEAT 7.4, FEAT 9.3, FEAT 4.4, FEAT 4.5 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-U01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Ngôn ngữ giao diện |
| **Độ đo yêu cầu** | Tỷ lệ nhãn, menu và nút thao tác ở các màn hình thuộc phạm vi yêu cầu hiển thị bằng tiếng Việt. |
| **Tiêu chuẩn đáp ứng** | 100% nhãn, menu và nút thao tác ở các màn hình thuộc phạm vi yêu cầu hiển thị bằng tiếng Việt. |

#### SUPL-U02

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Tính nhất quán giao diện |
| **Độ đo yêu cầu** | Tỷ lệ màn hình thuộc phạm vi yêu cầu dùng cùng font chữ mặc định. |
| **Tiêu chuẩn đáp ứng** | 100% màn hình thuộc phạm vi yêu cầu dùng cùng font chữ mặc định. |

#### SUPL-U03

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Tính nhất quán giao diện |
| **Độ đo yêu cầu** | Tỷ lệ màn hình thuộc phạm vi yêu cầu dùng màu hiển thị nhất quán cho từng loại thông báo thành công, cảnh báo và lỗi. |
| **Tiêu chuẩn đáp ứng** | 100% màn hình thuộc phạm vi yêu cầu dùng màu hiển thị nhất quán cho từng loại thông báo thành công, cảnh báo và lỗi. |

#### SUPL-U04

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Tính nhất quán giao diện |
| **Độ đo yêu cầu** | Tỷ lệ biểu mẫu cùng loại đặt nút xác nhận ở bên phải nút hủy hoặc quay lại. |
| **Tiêu chuẩn đáp ứng** | 100% biểu mẫu cùng loại đặt nút xác nhận ở bên phải nút hủy hoặc quay lại. |

#### SUPL-U05

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Dễ học |
| **Độ đo yêu cầu** | (1) Thời gian hướng dẫn cho mỗi người dùng mới thuộc vai trò TCCB; (2) Tỷ lệ người dùng mới thuộc vai trò TCCB hoàn thành đủ 3 tác vụ đã nêu mà không cần người hướng dẫn trả lời câu hỏi, nhắc bước tiếp theo hoặc thao tác hộ trong khi thực hiện. |
| **Tiêu chuẩn đáp ứng** | (1) Thời gian hướng dẫn không quá 2 giờ/người; (2) Ít nhất 95% người dùng mới thuộc vai trò TCCB hoàn thành đủ 3 tác vụ đã nêu mà không cần người hướng dẫn trả lời câu hỏi, nhắc bước tiếp theo hoặc thao tác hộ trong khi thực hiện. |

#### SUPL-U06

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Dễ học |
| **Độ đo yêu cầu** | (1) Thời gian hướng dẫn cho mỗi người dùng mới thuộc vai trò TCKT; (2) Tỷ lệ người dùng mới thuộc vai trò TCKT hoàn thành đủ 3 tác vụ đã nêu mà không cần người hướng dẫn trả lời câu hỏi, nhắc bước tiếp theo hoặc thao tác hộ trong khi thực hiện. |
| **Tiêu chuẩn đáp ứng** | (1) Thời gian hướng dẫn không quá 2 giờ/người; (2) Ít nhất 95% người dùng mới thuộc vai trò TCKT hoàn thành đủ 3 tác vụ đã nêu mà không cần người hướng dẫn trả lời câu hỏi, nhắc bước tiếp theo hoặc thao tác hộ trong khi thực hiện. |

#### SUPL-U07

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Xử lý lỗi |
| **Độ đo yêu cầu** | (1) Tỷ lệ lỗi kiểm tra dữ liệu đầu vào và lỗi nghiệp vụ có thông báo bằng tiếng Việt; (2) Tỷ lệ thông báo nêu rõ ít nhất một trong các thông tin về nguyên nhân lỗi: trường dữ liệu, quy tắc nghiệp vụ hoặc điều kiện gây lỗi; (3) Tỷ lệ thông báo nêu rõ bước người dùng phải thực hiện để tiếp tục thao tác. |
| **Tiêu chuẩn đáp ứng** | (1) 100% lỗi kiểm tra dữ liệu đầu vào và lỗi nghiệp vụ có thông báo bằng tiếng Việt; (2) 100% thông báo nêu rõ ít nhất một trong các thông tin về nguyên nhân lỗi: trường dữ liệu, quy tắc nghiệp vụ hoặc điều kiện gây lỗi; (3) 100% thông báo nêu rõ bước người dùng phải thực hiện để tiếp tục thao tác. |

#### SUPL-U08

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Hỗ trợ chẩn đoán lỗi |
| **Độ đo yêu cầu** | (1) Tỷ lệ lỗi hệ thống có thông báo bằng tiếng Việt; (2) Tỷ lệ lỗi hệ thống có mã tra cứu duy nhất cho lần phát sinh lỗi. |
| **Tiêu chuẩn đáp ứng** | (1) 100% lỗi hệ thống có thông báo bằng tiếng Việt; (2) 100% lỗi hệ thống có mã tra cứu duy nhất cho lần phát sinh lỗi. |

#### SUPL-U09

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Hiệu quả thao tác |
| **Độ đo yêu cầu** | Số tiêu chí lọc có thể kết hợp đồng thời khi tìm kiếm hồ sơ nhân sự. |
| **Tiêu chuẩn đáp ứng** | Người dùng kết hợp được tối thiểu 3 tiêu chí lọc đồng thời khi tìm kiếm hồ sơ nhân sự. |

#### SUPL-U10

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Hiệu quả thao tác |
| **Độ đo yêu cầu** | Số bước chức năng từ lúc người dùng nhập ít nhất một điều kiện tìm kiếm hoặc lọc đến lúc mở trang chi tiết hồ sơ. |
| **Tiêu chuẩn đáp ứng** | Người dùng mở được trang chi tiết của một hồ sơ trong tối đa 3 bước chức năng. |

#### SUPL-U11

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Hiển thị trên desktop |
| **Độ đo yêu cầu** | Tỷ lệ màn hình thuộc phạm vi yêu cầu hiển thị tiêu đề trang, bộ lọc hoặc ô tìm kiếm (nếu có), vùng nội dung chính, nút thao tác chính và phân trang hoặc nút điều hướng (nếu có) trong vùng hiển thị mà không cần cuộn ngang ở độ phân giải 1366×768 trở lên. |
| **Tiêu chuẩn đáp ứng** | 100% màn hình thuộc phạm vi yêu cầu hiển thị tiêu đề trang, bộ lọc hoặc ô tìm kiếm (nếu có), vùng nội dung chính, nút thao tác chính và phân trang hoặc nút điều hướng (nếu có) trong vùng hiển thị mà không cần cuộn ngang ở độ phân giải 1366×768 trở lên. |

#### SUPL-U12

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Hiển thị trên tablet |
| **Độ đo yêu cầu** | (1) Tỷ lệ tác vụ thuộc phạm vi yêu cầu thực hiện được ở độ phân giải từ 1024×768 đến dưới 1366×768; (2) Số lần phải cuộn ngang hoặc phóng to trong mỗi tác vụ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% tác vụ thuộc phạm vi yêu cầu thực hiện được ở độ phân giải từ 1024×768 đến dưới 1366×768; (2) 0 lần phải cuộn ngang hoặc phóng to trong mỗi tác vụ. |

#### SUPL-U13

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Điều hướng bằng bàn phím |
| **Độ đo yêu cầu** | Tỷ lệ biểu mẫu thuộc phạm vi yêu cầu có thứ tự Tab theo thứ tự từ trên xuống dưới, từ trái sang phải của các trường nhập có thể thao tác. |
| **Tiêu chuẩn đáp ứng** | 100% biểu mẫu thuộc phạm vi yêu cầu có thứ tự Tab theo thứ tự từ trên xuống dưới, từ trái sang phải của các trường nhập có thể thao tác. |

#### SUPL-U14

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Điều hướng bằng bàn phím |
| **Độ đo yêu cầu** | Tỷ lệ biểu mẫu thuộc phạm vi yêu cầu mà phím Enter kích hoạt đúng nút hành động chính của biểu mẫu (Lưu, Thêm mới hoặc Cập nhật). |
| **Tiêu chuẩn đáp ứng** | 100% biểu mẫu thuộc phạm vi yêu cầu mà phím Enter kích hoạt đúng nút hành động chính của biểu mẫu (Lưu, Thêm mới hoặc Cập nhật). |

#### SUPL-U15

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Điều hướng giao diện |
| **Độ đo yêu cầu** | (1) Tỷ lệ trang thuộc phạm vi yêu cầu có đường dẫn điều hướng phân cấp (breadcrumb) hiển thị; (2) Tỷ lệ mục breadcrumb điều hướng đúng trang tương ứng. |
| **Tiêu chuẩn đáp ứng** | (1) 100% trang thuộc phạm vi yêu cầu có đường dẫn điều hướng phân cấp (breadcrumb) hiển thị; (2) 100% mục breadcrumb điều hướng đúng trang tương ứng. |

#### SUPL-U16

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả dụng – Ngăn ngừa lỗi |
| **Độ đo yêu cầu** | Tỷ lệ thao tác thuộc danh sách yêu cầu có hộp thoại xác nhận trước khi hệ thống thực thi. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác thuộc danh sách yêu cầu có hộp thoại xác nhận trước khi hệ thống thực thi. |

## 6.5 Supportability — Ninh

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-S01 | Hệ thống phải cho phép quản trị viên thêm mới, chỉnh sửa và thay đổi trạng thái hệ số lương, loại phụ cấp và loại hợp đồng qua giao diện cấu hình. | FEAT 9.1, FEAT 9.2, FEAT 9.3, FEAT 4.4, FEAT 4.5 |
| 2 | SUPL-S02 | Bộ tài liệu giao diện lập trình ứng dụng (API) của hệ thống phải mô tả 100% các API mà giao diện web đang sử dụng, bao gồm phương thức, đường dẫn truy cập (URL), tham số, dữ liệu trả về và mã lỗi. | FEAT 14.1 |
| 3 | SUPL-S03 | Bộ tài liệu triển khai của hệ thống phải bao gồm các mục: yêu cầu môi trường, cài đặt, cấu hình, khởi động, sao lưu, khôi phục và mục xử lý lỗi triển khai. | FEAT 14.1 |
| 4 | SUPL-S04 | Bộ tài liệu hướng dẫn sử dụng phải có phần riêng cho các vai trò Quản trị viên, Phòng Tổ chức – Cán bộ (TCCB), Phòng Tài chính – Kế toán (TCKT) và nhóm người dùng Cán bộ/Giảng viên/Nhân viên. | FEAT 2.4, FEAT 7.1, FEAT 10.1, FEAT 11.1 |
| 5 | SUPL-S05 | Trong không quá 1 phút kể từ khi quản trị viên lưu thay đổi cấu hình hệ số lương, loại phụ cấp hoặc loại hợp đồng, hệ thống phải hiển thị giá trị mới đã lưu của danh mục đó trên màn hình cấu hình tương ứng và trong danh sách chọn của các màn hình thêm mới hoặc chỉnh sửa hồ sơ nhân sự và hợp đồng lao động sử dụng danh mục đó. | FEAT 5.1, FEAT 5.3, FEAT 7.3, FEAT 7.4, FEAT 9.1, FEAT 9.2, FEAT 9.3, FEAT 4.4, FEAT 4.5 |
| 6 | SUPL-S06 | Hệ thống phải phân loại và ghi nhật ký máy chủ (log) ở tối thiểu 4 mức: ERROR, WARNING, INFO và DEBUG. | FEAT 12.1, FEAT 12.2 |
| 7 | SUPL-S07 | Mỗi bản ghi log mức ERROR phải chứa thời điểm ghi nhận (timestamp), mức độ nghiêm trọng (severity), mã yêu cầu xử lý (request ID) và vết ngăn xếp lỗi (stack trace). | FEAT 12.1, FEAT 12.2 |
| 8 | SUPL-S08 | Ít nhất 95% bản ghi log phát sinh trong phiên đã xác thực phải chứa định danh người dùng (user ID). | FEAT 12.1, FEAT 12.2 |
| 9 | SUPL-S09 | Khi chạy đồng thời trên tối thiểu 2 nút ứng dụng trong cùng một môi trường, hệ thống phải cho phép người dùng đăng nhập thành công và hiển thị màn hình đầu tiên sau đăng nhập chứa các chức năng được phép của vai trò đã đăng nhập. | FEAT 1.1 |
| 10 | SUPL-S10 | Khi chạy đồng thời trên tối thiểu 2 nút ứng dụng trong cùng một môi trường, hệ thống phải trả về danh sách hồ sơ nhân sự khớp với điều kiện tìm kiếm đã nhập. | FEAT 7.1 |
| 11 | SUPL-S11 | Khi chạy đồng thời trên tối thiểu 2 nút ứng dụng trong cùng một môi trường, khi người dùng chọn một hồ sơ từ danh sách hồ sơ nhân sự, hệ thống phải hiển thị đúng hồ sơ đã chọn. | FEAT 8.7 |
| 12 | SUPL-S12 | Khi chạy đồng thời trên tối thiểu 2 nút ứng dụng trong cùng một môi trường, hệ thống phải lưu thành công hồ sơ nhân sự mới và hồ sơ đó phải xuất hiện trong danh sách tìm kiếm. | FEAT 7.3 |
| 13 | SUPL-S13 | Khi chạy đồng thời trên tối thiểu 2 nút ứng dụng trong cùng một môi trường, hệ thống phải lưu thành công các giá trị chỉnh sửa của hồ sơ nhân sự và hiển thị lại đúng các giá trị đó. | FEAT 7.4 |
| 14 | SUPL-S14 | Khi chạy đồng thời trên tối thiểu 2 nút ứng dụng trong cùng một môi trường, hệ thống phải lưu thành công trạng thái mới của loại hợp đồng và hiển thị lại đúng trạng thái đó trong danh sách loại hợp đồng. | FEAT 4.5 |
| 15 | SUPL-S15 | Trong bài kiểm thử 30 phút với tối thiểu 2 nút ứng dụng, 100% phiên người dùng đã xác thực phải duy trì được trạng thái đăng nhập khi các yêu cầu xử lý liên tiếp của cùng một phiên đi qua các nút khác nhau. | FEAT 1.1 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-S01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng thay đổi |
| **Độ đo yêu cầu** | Số nhóm danh mục thuộc phạm vi yêu cầu mà quản trị viên thực hiện được đầy đủ 3 thao tác thêm mới, chỉnh sửa và thay đổi trạng thái qua giao diện cấu hình. |
| **Tiêu chuẩn đáp ứng** | Cả 3 nhóm danh mục thuộc phạm vi yêu cầu cho phép quản trị viên thực hiện đầy đủ 3 thao tác thêm mới, chỉnh sửa và thay đổi trạng thái qua giao diện cấu hình. |

#### SUPL-S02

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Tài liệu API |
| **Độ đo yêu cầu** | Tỷ lệ các API mà giao diện web đang sử dụng có tài liệu mô tả đầy đủ phương thức, đường dẫn truy cập (URL), tham số, dữ liệu trả về và mã lỗi. |
| **Tiêu chuẩn đáp ứng** | 100% các API mà giao diện web đang sử dụng có tài liệu mô tả đầy đủ phương thức, đường dẫn truy cập (URL), tham số, dữ liệu trả về và mã lỗi. |

#### SUPL-S03

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Tài liệu triển khai |
| **Độ đo yêu cầu** | Số mục bắt buộc trong bộ tài liệu triển khai được mô tả đầy đủ: yêu cầu môi trường, cài đặt, cấu hình, khởi động, sao lưu, khôi phục và xử lý lỗi triển khai. |
| **Tiêu chuẩn đáp ứng** | Bộ tài liệu triển khai mô tả đầy đủ cả 7 mục bắt buộc: yêu cầu môi trường, cài đặt, cấu hình, khởi động, sao lưu, khôi phục và xử lý lỗi triển khai. |

#### SUPL-S04

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Tài liệu sử dụng |
| **Độ đo yêu cầu** | Số nhóm vai trò hoặc người dùng có phần hướng dẫn sử dụng riêng trong phạm vi yêu cầu. |
| **Tiêu chuẩn đáp ứng** | Có đủ 4 phần hướng dẫn sử dụng riêng cho các vai trò Quản trị viên, TCCB, TCKT và nhóm người dùng Cán bộ/Giảng viên/Nhân viên. |

#### SUPL-S05

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Cấu hình |
| **Độ đo yêu cầu** | Tỷ lệ thay đổi cấu hình thuộc phạm vi yêu cầu mà giá trị mới đã lưu xuất hiện trên màn hình cấu hình tương ứng và trong danh sách chọn của các màn hình thêm mới hoặc chỉnh sửa hồ sơ nhân sự, hợp đồng lao động sử dụng danh mục đó trong không quá 1 phút kể từ khi lưu. |
| **Tiêu chuẩn đáp ứng** | 100% thay đổi cấu hình thuộc phạm vi yêu cầu làm cho giá trị mới đã lưu xuất hiện trên màn hình cấu hình tương ứng và trong danh sách chọn của các màn hình thêm mới hoặc chỉnh sửa hồ sơ nhân sự, hợp đồng lao động sử dụng danh mục đó trong không quá 1 phút kể từ khi lưu. |

#### SUPL-S06

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Ghi log |
| **Độ đo yêu cầu** | Số mức nhật ký máy chủ (log) mà hệ thống phân loại và ghi nhận. |
| **Tiêu chuẩn đáp ứng** | Hệ thống phân loại và ghi nhận nhật ký máy chủ (log) ở tối thiểu 4 mức: ERROR, WARNING, INFO và DEBUG. |

#### SUPL-S07

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Chẩn đoán lỗi |
| **Độ đo yêu cầu** | Tỷ lệ bản ghi log mức ERROR chứa đủ thời điểm ghi nhận (timestamp), mức độ nghiêm trọng (severity), mã yêu cầu xử lý (request ID) và vết ngăn xếp lỗi (stack trace). |
| **Tiêu chuẩn đáp ứng** | 100% bản ghi log mức ERROR chứa đủ thời điểm ghi nhận (timestamp), mức độ nghiêm trọng (severity), mã yêu cầu xử lý (request ID) và vết ngăn xếp lỗi (stack trace). |

#### SUPL-S08

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Chẩn đoán lỗi |
| **Độ đo yêu cầu** | Tỷ lệ bản ghi log phát sinh trong phiên đã xác thực chứa định danh người dùng (user ID). |
| **Tiêu chuẩn đáp ứng** | Ít nhất 95% bản ghi log phát sinh trong phiên đã xác thực chứa định danh người dùng (user ID). |

#### SUPL-S09

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng mở rộng |
| **Độ đo yêu cầu** | Tỷ lệ lần đăng nhập thành công mà hệ thống hiển thị màn hình đầu tiên sau đăng nhập chứa các chức năng được phép của vai trò đã đăng nhập khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | 100% lần đăng nhập thành công làm cho hệ thống hiển thị màn hình đầu tiên sau đăng nhập chứa các chức năng được phép của vai trò đã đăng nhập khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |

#### SUPL-S10

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng mở rộng |
| **Độ đo yêu cầu** | Tỷ lệ truy vấn tìm kiếm hồ sơ nhân sự trả về danh sách đúng với điều kiện tìm kiếm khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | 100% truy vấn tìm kiếm hồ sơ nhân sự trả về danh sách đúng với điều kiện tìm kiếm khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |

#### SUPL-S11

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng mở rộng |
| **Độ đo yêu cầu** | Tỷ lệ thao tác mở chi tiết hồ sơ nhân sự hiển thị đúng hồ sơ đã chọn khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác mở chi tiết hồ sơ nhân sự hiển thị đúng hồ sơ đã chọn khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |

#### SUPL-S12

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng mở rộng |
| **Độ đo yêu cầu** | Tỷ lệ thao tác thêm mới hồ sơ nhân sự lưu thành công và làm cho hồ sơ mới xuất hiện trong danh sách tìm kiếm khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác thêm mới hồ sơ nhân sự lưu thành công và làm cho hồ sơ mới xuất hiện trong danh sách tìm kiếm khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |

#### SUPL-S13

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng mở rộng |
| **Độ đo yêu cầu** | Tỷ lệ thao tác chỉnh sửa hồ sơ nhân sự lưu thành công và hiển thị lại đúng các giá trị đã chỉnh sửa khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác chỉnh sửa hồ sơ nhân sự lưu thành công và hiển thị lại đúng các giá trị đã chỉnh sửa khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |

#### SUPL-S14

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng mở rộng |
| **Độ đo yêu cầu** | Tỷ lệ thao tác thay đổi trạng thái loại hợp đồng lưu thành công và hiển thị lại đúng trạng thái mới khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác thay đổi trạng thái loại hợp đồng lưu thành công và hiển thị lại đúng trạng thái mới khi hệ thống chạy đồng thời trên tối thiểu 2 nút ứng dụng. |

#### SUPL-S15

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Khả năng hỗ trợ – Khả năng mở rộng |
| **Độ đo yêu cầu** | (1) Thời lượng bài kiểm thử; (2) Tỷ lệ phiên người dùng đã xác thực duy trì được trạng thái đăng nhập khi các yêu cầu xử lý liên tiếp của cùng một phiên đi qua các nút ứng dụng khác nhau. |
| **Tiêu chuẩn đáp ứng** | (1) Bài kiểm thử kéo dài 30 phút; (2) 100% phiên người dùng đã xác thực duy trì được trạng thái đăng nhập khi các yêu cầu xử lý liên tiếp của cùng một phiên đi qua các nút ứng dụng khác nhau. |

## 6.6 Performance — Tùng

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-P01 | Hệ thống phải giữ P95 Response Time của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự trong các ngưỡng quy định theo 3 mức tải đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 2 | SUPL-P02 | Hệ thống phải giữ Time to Interactive (TTI) của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự trong các ngưỡng quy định theo 3 mức tải đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 3 | SUPL-P03 | Hệ thống phải hỗ trợ tối thiểu 100 người dùng đồng thời trong giờ cao điểm mà thời gian phản hồi của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa không tăng quá 50% so với tải một người dùng trong cùng điều kiện đo. | FEAT 7.1–8.9 |
| 4 | SUPL-P04 | Hệ thống phải trả kết quả tìm kiếm và lọc hồ sơ nhân sự trong tối đa 2 giây với tập dữ liệu không quá 10.000 bản ghi hoặc tối đa 5 giây với tập dữ liệu không quá 50.000 bản ghi, tại mức không quá 50 người dùng đồng thời. | FEAT 8.1, FEAT 8.2 |
| 5 | SUPL-P05 | Hệ thống phải hoàn thành upload tệp đính kèm trong tối đa 5 giây và download trong tối đa 3 giây với file không quá 5 MB, hoặc upload tối đa 10 giây và download tối đa 6 giây với file trên 5 MB đến 10 MB, trên mạng LAN 1 Gbps và ở mức không quá 10 người dùng đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 6 | SUPL-P06 | Hệ thống phải khôi phục dịch vụ để phục vụ lại request đầu tiên thành công trong tối đa 15 phút sau sự cố crash hoặc mất dịch vụ ngoài kế hoạch của hệ thống mà không yêu cầu phục hồi từ bản sao lưu gần nhất. | FEAT 7.1–8.9 |
| 7 | SUPL-P07 | Hệ thống phải đưa toàn bộ stack về trạng thái sẵn sàng phục vụ trong tối đa 10 phút sau lệnh restart có chủ đích. | FEAT 7.1–8.9 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-P01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | P95 Response Time cho các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự tại 3 mức tải: 0–10, 11–50 và 51–100 người dùng đồng thời. |
| **Tiêu chuẩn đáp ứng** | (1) 0–10 người dùng đồng thời: P95 Response Time ≤ 1 giây; (2) 11–50 người dùng đồng thời: P95 Response Time ≤ 2 giây; (3) 51–100 người dùng đồng thời: P95 Response Time ≤ 5 giây. |

#### SUPL-P02

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian tương tác giao diện |
| **Độ đo yêu cầu** | Time to Interactive (TTI) cho các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự tại 3 mức tải: 0–10, 11–50 và 51–100 người dùng đồng thời. |
| **Tiêu chuẩn đáp ứng** | (1) 0–10 người dùng đồng thời: TTI ≤ 1,5 giây; (2) 11–50 người dùng đồng thời: TTI ≤ 3 giây; (3) 51–100 người dùng đồng thời: TTI ≤ 6 giây. |

#### SUPL-P03

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Sức chứa |
| **Độ đo yêu cầu** | (1) Số người dùng đồng thời tối đa hệ thống hỗ trợ trong giờ cao điểm; (2) Tỷ lệ tăng thời gian phản hồi của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa khi so sánh mức 100 người dùng đồng thời với mức 1 người dùng trong cùng điều kiện đo. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời trong giờ cao điểm; (2) Thời gian phản hồi của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa tại mức 100 người dùng đồng thời không tăng quá 50% so với tải một người dùng trong cùng điều kiện đo. |

#### SUPL-P04

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | (1) Thời gian trả kết quả tìm kiếm; (2) Thời gian áp dụng bộ lọc, tương ứng với hai quy mô dữ liệu: không quá 10.000 bản ghi và không quá 50.000 bản ghi. |
| **Tiêu chuẩn đáp ứng** | (1) Với tập dữ liệu ≤ 10.000 bản ghi: thời gian tìm kiếm và lọc đều ≤ 2 giây tại mức ≤ 50 người dùng đồng thời; (2) Với tập dữ liệu ≤ 50.000 bản ghi: thời gian tìm kiếm và lọc đều ≤ 5 giây tại mức ≤ 50 người dùng đồng thời. |

#### SUPL-P05

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | (1) Thời gian upload file; (2) Thời gian download file; (3) Kích thước file kiểm thử trong hai khoảng: ≤ 5 MB và > 5 MB đến ≤ 10 MB, trên mạng LAN 1 Gbps. |
| **Tiêu chuẩn đáp ứng** | (1) Với file ≤ 5 MB: Upload ≤ 5 giây, Download ≤ 3 giây tại mức ≤ 10 người dùng đồng thời; (2) Với file > 5 MB đến ≤ 10 MB: Upload ≤ 10 giây, Download ≤ 6 giây tại mức ≤ 10 người dùng đồng thời. |

#### SUPL-P06

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian khôi phục dịch vụ |
| **Độ đo yêu cầu** | Thời gian từ lúc hệ thống gặp sự cố crash hoặc mất dịch vụ ngoài kế hoạch của hệ thống mà không yêu cầu phục hồi từ bản sao lưu gần nhất đến khi hệ thống phục vụ lại được request đầu tiên thành công. |
| **Tiêu chuẩn đáp ứng** | Hệ thống phục vụ lại được request đầu tiên thành công trong tối đa 15 phút sau sự cố crash hoặc mất dịch vụ ngoài kế hoạch của hệ thống mà không yêu cầu phục hồi từ bản sao lưu gần nhất. |

#### SUPL-P07

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian khởi động lại hệ thống |
| **Độ đo yêu cầu** | Thời gian từ lúc phát lệnh restart có chủ đích đến khi toàn bộ stack khởi động thành công và sẵn sàng phục vụ request theo health check kỹ thuật. |
| **Tiêu chuẩn đáp ứng** | Toàn bộ stack sẵn sàng phục vụ trong tối đa 10 phút sau lệnh restart có chủ đích. |

### Ghi chú phạm vi

- `SUPL-P01` gốc được tách thành `SUPL-P01` và `SUPL-P02` để tách riêng ngưỡng **P95 Response Time** và **TTI**, giúp requirement atomic hơn.
- Các chỉ tiêu thời gian hiển thị chi tiết hồ sơ, chuẩn bị dữ liệu in và tạo file xuất Excel được đặt tại **Yêu cầu đặc biệt** của UC 4.35 và UC 4.36 vì chỉ áp dụng cho các use case cụ thể, không giữ trong fragment Supplementary Specification này.
- `SUPL-R02` gốc được đổi thành `SUPL-P06` và `SUPL-P07` để khớp với section **Hiệu năng** và yếu tố chất lượng chính của hai requirement này.
- Ngoài `SUPL-P07`, hiện không có thêm yêu cầu nghiệm thu riêng cho thời gian khởi động ban đầu hoặc tắt an toàn trong fragment này.
- **Resource utilization:** N/A trong fragment này vì stakeholder chưa đưa ra ràng buộc CPU, RAM, băng thông hoặc dung lượng lưu trữ cụ thể cho môi trường triển khai.

## 6.7 Reliability — Tùng

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-R01 | Hệ thống phải duy trì uptime tối thiểu 99,5% theo tháng trong khung giờ 7:00–22:00 hằng ngày, không tính bảo trì theo kế hoạch. | FEAT 7.1–8.9 |
| 2 | SUPL-R02 | Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi 24 giờ. | FEAT 7.1–8.9 |
| 3 | SUPL-R03 | Hệ thống phải phục hồi từ bản sao lưu gần nhất và sẵn sàng phục vụ trong tối đa 4 giờ. | FEAT 7.1–8.9 |
| 4 | SUPL-R04 | Hệ thống phải lưu giữ bản sao lưu tối thiểu 30 ngày. | FEAT 7.1–8.9 |
| 5 | SUPL-R05 | Hệ thống phải đạt tỷ lệ backup thành công tối thiểu 99%. | FEAT 7.1–8.9 |
| 6 | SUPL-R06 | Hệ thống phải bảo đảm các thao tác tạo/chỉnh sửa hồ sơ nhân sự, tạo/chỉnh sửa/chấm dứt hợp đồng và cập nhật trạng thái thôi việc không để lại dữ liệu dở dang hoặc bất nhất khi có lỗi. | FEAT 7.1, FEAT 7.3, FEAT 7.4, FEAT 8.3, FEAT 8.4, FEAT 8.5, FEAT 8.6 |
| 7 | SUPL-R07 | Hệ thống phải hiển thị cảnh báo tối thiểu 5 phút trước khi phiên tự động hết hạn trong 100% phiên được kiểm thử đối với các form có dữ liệu đã nhập nhưng chưa lưu. | FEAT 7.1–8.9 |
| 8 | SUPL-R08 | Hệ thống phải khôi phục dữ liệu nháp sau khi người dùng đăng nhập lại trong ít nhất 95% trường hợp kiểm thử. | FEAT 7.1–8.9 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-R01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Tính sẵn sàng |
| **Độ đo yêu cầu** | (1) Tỷ lệ uptime theo tháng trong khung giờ 7:00–22:00 hằng ngày; (2) Tỷ lệ downtime trên tổng thời lượng phục vụ trong cùng kỳ đo. |
| **Tiêu chuẩn đáp ứng** | (1) Uptime đạt tối thiểu 99,5% mỗi tháng trong khung giờ 7:00–22:00 hằng ngày; (2) Downtime không vượt quá 0,5% tổng thời lượng phục vụ trong cùng kỳ đo, không tính bảo trì theo kế hoạch. |

#### SUPL-R02

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | RPO (Recovery Point Objective), đo theo thời gian từ thời điểm backup gần nhất đến thời điểm kiểm tra. |
| **Tiêu chuẩn đáp ứng** | Hệ thống sao lưu dữ liệu tự động ít nhất mỗi 24 giờ, tương ứng RPO không vượt quá 24 giờ. |

#### SUPL-R03

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Thời gian phục hồi từ bản sao lưu |
| **Độ đo yêu cầu** | RTO (Recovery Time Objective) khi phục hồi từ bản sao lưu gần nhất. |
| **Tiêu chuẩn đáp ứng** | Hệ thống sẵn sàng phục vụ trở lại trong tối đa 4 giờ sau khi thực hiện phục hồi từ bản sao lưu gần nhất. |

#### SUPL-R04

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Thời gian lưu giữ của mỗi bản sao lưu trước khi bị xóa hoặc ghi đè. |
| **Tiêu chuẩn đáp ứng** | Mỗi bản sao lưu được lưu giữ tối thiểu 30 ngày. |

#### SUPL-R05

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Tỷ lệ backup thành công trên tổng số lần backup được lên lịch trong mỗi tháng. |
| **Tiêu chuẩn đáp ứng** | Tỷ lệ backup thành công đạt tối thiểu 99% trên tổng số lần backup được lên lịch trong mỗi tháng. |

#### SUPL-R06

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Tính đúng đắn dữ liệu |
| **Độ đo yêu cầu** | (1) Số trường hợp phát sinh dữ liệu dở dang hoặc bất nhất sau lỗi; (2) Tỷ lệ các nhóm nghiệp vụ trọng yếu trong phạm vi FEAT 7.1, FEAT 7.3, FEAT 7.4, FEAT 8.3, FEAT 8.4, FEAT 8.5, FEAT 8.6 được bảo vệ khỏi cập nhật dở dang hoặc bất nhất. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp dữ liệu dở dang hoặc bất nhất sau lỗi; (2) 100% các nhóm nghiệp vụ tạo/chỉnh sửa hồ sơ nhân sự, tạo/chỉnh sửa/chấm dứt hợp đồng và cập nhật trạng thái thôi việc không phát sinh dữ liệu dở dang hoặc bất nhất khi có lỗi. |

#### SUPL-R07

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | (1) Tỷ lệ phiên được hiển thị cảnh báo trước khi hết hạn đối với form có dữ liệu đã nhập nhưng chưa lưu; (2) Thời gian cảnh báo trước khi tự động đăng xuất. |
| **Tiêu chuẩn đáp ứng** | (1) 100% phiên được kiểm thử có hiển thị cảnh báo trước khi hết hạn đối với form có dữ liệu đã nhập nhưng chưa lưu; (2) Cảnh báo xuất hiện tối thiểu 5 phút trước khi tự động đăng xuất. |

#### SUPL-R08

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Tỷ lệ khôi phục dữ liệu nháp khi người dùng đăng nhập lại sau khi phiên hết hạn. |
| **Tiêu chuẩn đáp ứng** | Hệ thống khôi phục dữ liệu nháp trong ít nhất 95% trường hợp kiểm thử đối với form có dữ liệu đã nhập nhưng chưa lưu. |

### Ghi chú phạm vi

- **Robustness:** N/A trong fragment này vì yêu cầu xử lý dữ liệu nhập sai và phản ứng với input bất thường đang được đặc tả tại các phần validation/giao diện của nhóm khác.
- **Fault tolerance:** N/A trong fragment này vì hiện chưa có yêu cầu vận hành về chế độ suy giảm hoặc tiếp tục phục vụ khi một thành phần phụ trợ bị lỗi.
- **Safety:** N/A vì HRMS là hệ thống quản lý nghiệp vụ nội bộ, không trực tiếp điều khiển thiết bị vật lý hoặc tạo rủi ro an toàn cho con người/môi trường.
- **Security:** Các yêu cầu bảo mật về xác thực, phân quyền, timeout phiên và kiểm soát truy cập được đặc tả ở section bảo mật của nhóm; fragment Reliability này chỉ xét khía cạnh hạn chế mất dữ liệu đang nhập khi phiên hết hạn.
- **Accuracy / Correctness ngoài phạm vi tính nhất quán dữ liệu khi lỗi:** Chưa được đặc tả riêng trong fragment này; `SUPL-R06` chỉ bao phủ yêu cầu không để lại dữ liệu dở dang hoặc bất nhất khi thao tác cập nhật gặp lỗi.

## 6.8 Security — Khánh

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-SE01 | Mọi truy cập vào hệ thống phải qua xác thực bằng tài khoản/mật khẩu; mật khẩu phải có tối thiểu 8 ký tự, bao gồm chữ hoa, chữ thường và chữ số. | Toàn hệ thống |
| 2 | SUPL-SE02 | Hệ thống phải phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Người dùng); mỗi chức năng và API chỉ cho phép truy cập bởi vai trò được cấp quyền. | Toàn hệ thống |
| 3 | SUPL-SE03 | Hệ thống phải khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp, thời gian khóa tối thiểu 15 phút và có ghi cảnh báo bảo mật. | Toàn hệ thống |
| 4 | SUPL-SE04 | Toàn bộ giao tiếp giữa client và server phải dùng HTTPS với TLS 1.2 trở lên, đồng thời tự động chuyển hướng HTTP sang HTTPS. | Toàn hệ thống |
| 5 | SUPL-SE05 | Dữ liệu nhạy cảm (CCCD, BHXH, thông tin ngân hàng) chỉ hiển thị cho vai trò được phép và mọi truy cập phải được ghi audit log. | Toàn hệ thống |
| 6 | SUPL-SE06 | Hệ thống phải ngăn chặn tấn công web (CSRF, XSS) trên các chức năng nhập liệu và thao tác thay đổi dữ liệu. | Toàn hệ thống |
| 7 | SUPL-SE07 | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu bằng cơ chế truy vấn tham số hóa hoặc tương đương. | Toàn hệ thống |
| 8 | SUPL-SE08 | Chỉ vai trò được ủy quyền mới được cấu hình ẩn/hiện mục khen thưởng/kỷ luật; mọi thay đổi phải lưu vết audit đầy đủ. | FEAT 8.9 |
| 9 | SUPL-SE09 | Chỉ người dùng có quyền mới được chấm dứt hợp đồng trước hạn; mọi thao tác phải được ghi audit log đầy đủ thông tin nghiệp vụ. | FEAT 7.4 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-SE01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authentication (Xác thực) |
| **Độ đo yêu cầu** | (1) Số quy tắc mật khẩu bắt buộc được kiểm tra; (2) Số lớp xác thực trước khi truy cập hệ thống; (3) Trạng thái bảo vệ phiên và thời gian hết hạn không hoạt động. |
| **Tiêu chuẩn đáp ứng** | (1) Mật khẩu có ít nhất 8 ký tự và thỏa 3/3 quy tắc: chữ hoa, chữ thường, chữ số; (2) Áp dụng 01 lớp xác thực bằng tên đăng nhập/mật khẩu; (3) Phiên đăng nhập được bảo vệ và tự hết hiệu lực sau tối đa 30 phút không hoạt động. |

#### SUPL-SE02

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authorization (Phân quyền truy cập) |
| **Độ đo yêu cầu** | (1) Số trường hợp truy cập trái phép qua kiểm thử phân quyền; (2) Tỷ lệ API endpoint có kiểm tra quyền; (3) Số vai trò được định nghĩa trong mô hình RBAC. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp truy cập trái phép vào chức năng hoặc API không được cấp quyền; (2) 100% API endpoint có cơ chế kiểm tra quyền trước khi xử lý; (3) Hệ thống có đúng 4 vai trò: Admin, TCCB, TCKT, Người dùng. |

#### SUPL-SE03

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công tự động |
| **Độ đo yêu cầu** | (1) Ngưỡng số lần đăng nhập sai liên tiếp trước khi khóa tài khoản; (2) Thời gian khóa tạm thời; (3) Trạng thái ghi log cảnh báo brute-force. |
| **Tiêu chuẩn đáp ứng** | (1) Tài khoản bị khóa sau đúng 5 lần đăng nhập sai liên tiếp; (2) Thời gian khóa tối thiểu 15 phút; (3) Có bản ghi cảnh báo gồm tối thiểu IP, thời gian và tài khoản bị tác động. |

#### SUPL-SE04

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Confidentiality (Bảo mật truyền tải) |
| **Độ đo yêu cầu** | (1) Phiên bản TLS đang sử dụng; (2) Tỷ lệ kết nối HTTPS trên tổng kết nối; (3) Trạng thái tự động chuyển hướng HTTP sang HTTPS. |
| **Tiêu chuẩn đáp ứng** | (1) Chỉ chấp nhận TLS 1.2 trở lên; (2) 100% kết nối sử dụng HTTPS, 0% kết nối HTTP không mã hóa được xử lý trực tiếp; (3) Mọi truy cập HTTP được tự động chuyển hướng sang HTTPS. |

#### SUPL-SE05

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Confidentiality (Bảo mật dữ liệu) |
| **Độ đo yêu cầu** | (1) Số trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được phép; (2) Tỷ lệ lượt truy cập dữ liệu nhạy cảm được ghi audit log. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được cấp quyền; (2) 100% lượt truy cập các trường CCCD, BHXH và thông tin ngân hàng được ghi audit log. |

#### SUPL-SE06

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công web |
| **Độ đo yêu cầu** | (1) Số lỗ hổng CSRF phát hiện qua kiểm thử; (2) Số lỗ hổng XSS phát hiện qua kiểm thử; (3) Tỷ lệ request POST/PUT/DELETE có cơ chế chống giả mạo. |
| **Tiêu chuẩn đáp ứng** | (1) 0 lỗ hổng CSRF; (2) 0 lỗ hổng XSS; (3) 100% request POST/PUT/DELETE và form thay đổi dữ liệu vượt qua kiểm thử chống CSRF, 100% dữ liệu người dùng hiển thị lại trên giao diện vượt qua kiểm thử XSS. |

#### SUPL-SE07

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu |
| **Độ đo yêu cầu** | (1) Số lỗ hổng SQL Injection phát hiện qua kiểm thử; (2) Tỷ lệ truy vấn có dữ liệu đầu vào được bảo vệ bằng cơ chế tách dữ liệu khỏi câu lệnh SQL. |
| **Tiêu chuẩn đáp ứng** | (1) 0 lỗ hổng SQL Injection; (2) 100% truy vấn có dữ liệu đầu vào từ người dùng được bảo vệ bằng truy vấn tham số hóa hoặc ORM tương đương. |

#### SUPL-SE08

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Độ đo yêu cầu** | (1) Số thay đổi cấu hình ẩn/hiện mục khen thưởng/kỷ luật trái phép; (2) Tỷ lệ thay đổi cấu hình hợp lệ được ghi audit log; (3) Độ đầy đủ bản ghi audit theo 4 trường bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 0 thay đổi cấu hình do người dùng không được ủy quyền thực hiện thành công; (2) 100% thay đổi cấu hình hợp lệ được ghi audit log; (3) Mỗi bản ghi audit đạt 4/4 trường bắt buộc: người thực hiện, thời gian, giá trị trước, giá trị sau. |

#### SUPL-SE09

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Độ đo yêu cầu** | (1) Số trường hợp chấm dứt hợp đồng trước hạn trái phép; (2) Tỷ lệ thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log; (3) Độ đầy đủ bản ghi audit theo 7 trường bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp chấm dứt hợp đồng trước hạn được thực hiện bởi người dùng không có quyền; (2) 100% thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log; (3) Mỗi bản ghi audit đạt 7/7 trường bắt buộc: mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau. |

## 6.9 Implementation Constraints — Khánh

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-IC01 | Hệ thống phải sử dụng stack công nghệ: frontend React.js (TypeScript), backend Laravel/PHP và cơ sở dữ liệu MySQL/MariaDB trong các môi trường triển khai chính thức. | Toàn hệ thống |
| 2 | SUPL-IC02 | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox và Edge. | Toàn hệ thống |
| 3 | SUPL-IC03 | Toàn bộ hệ thống phải sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ tiếng Việt có dấu trên giao diện, API, cơ sở dữ liệu và dữ liệu trao đổi. | Toàn hệ thống |
| 4 | SUPL-IC04 | Hệ thống chỉ hỗ trợ file PDF cho hồ sơ đính kèm và file Excel cho import/export nhân sự, với kích thước tối đa 10MB mỗi file. | Toàn hệ thống |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-IC01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi công nghệ) - Công nghệ triển khai |
| **Độ đo yêu cầu** | (1) Tỷ lệ module frontend dùng React.js + TypeScript; (2) Tỷ lệ thành phần backend dùng Laravel/PHP; (3) Tỷ lệ môi trường chính thức dùng MySQL/MariaDB. |
| **Tiêu chuẩn đáp ứng** | (1) 100% module frontend sử dụng React.js kết hợp TypeScript; (2) 100% thành phần backend sử dụng Laravel/PHP; (3) 100% môi trường triển khai chính thức sử dụng MySQL hoặc MariaDB, 0 thành phần production dùng hệ quản trị cơ sở dữ liệu ngoài phạm vi yêu cầu. |

#### SUPL-IC02

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Compatibility (Tính tương thích) - Trình duyệt |
| **Độ đo yêu cầu** | (1) Độ phủ kiểm thử trên tập trình duyệt/phiên bản mục tiêu; (2) Tỷ lệ chức năng nghiệp vụ chính chạy đúng theo từng trình duyệt; (3) Số lỗi mức nghiêm trọng theo trình duyệt. |
| **Tiêu chuẩn đáp ứng** | (1) 100% phạm vi kiểm thử bao gồm Chrome bản mới nhất và 2 phiên bản gần nhất, Firefox bản ổn định hiện hành, Edge bản ổn định hiện hành tại thời điểm nghiệm thu; (2) 100% chức năng chính hoạt động đúng trên Chrome, ≥95% trên Firefox và Edge; (3) 0 lỗi mức Nghiêm trọng/Critical trên các trình duyệt mục tiêu. |

#### SUPL-IC03

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi) - Mã hóa dữ liệu |
| **Độ đo yêu cầu** | (1) Tỷ lệ thành phần hệ thống dùng UTF-8; (2) Số lỗi hiển thị tiếng Việt có dấu khi nhập, lưu, tìm kiếm và hiển thị dữ liệu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% thành phần của hệ thống dùng UTF-8; (2) 0 lỗi hiển thị sai tiếng Việt có dấu trên giao diện, dữ liệu lưu trữ, dữ liệu xuất và dữ liệu tải lại từ hệ thống. |

#### SUPL-IC04

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn) - File đính kèm |
| **Độ đo yêu cầu** | (1) Tỷ lệ file PDF/Excel hợp lệ được xử lý thành công; (2) Ngưỡng kích thước file tối đa hệ thống cho phép; (3) Tỷ lệ file sai định dạng hoặc vượt dung lượng bị từ chối. |
| **Tiêu chuẩn đáp ứng** | (1) 100% file PDF hợp lệ dùng cho bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động được upload/download thành công và 100% file Excel hợp lệ dùng cho import/export nhân sự được xử lý thành công; (2) Kích thước tối đa được chấp nhận là 10MB/file; (3) 100% file sai định dạng hoặc lớn hơn 10MB bị từ chối và hệ thống hiển thị thông báo lỗi rõ ràng. |

## Tóm tắt truy vết SUPL → FEAT

| SUPL | FEAT | Chủ sở hữu FEAT | Ghi chú |
| --- | --- | --- | --- |
| SUPL-F01 | FEAT 12.1 | Ninh | Ghi vết tác vụ — SUPL thêm yêu cầu 9 trường bắt buộc |
| SUPL-F02 | FEAT 7.3 | Tùng | Tạo hồ sơ nhân sự — SUPL ràng buộc tự động cấp mã |
| SUPL-F03 | FEAT 1.3 | Phúc | Đăng xuất tự động — SUPL cụ thể hóa ngưỡng 30 phút |
| SUPL-F04 | FEAT 2.6 | Phúc | Tự động khóa tài khoản — SUPL ràng buộc sự kiện thôi việc |
| SUPL-F05 | FEAT 5.1 | Tùng | Tạo/gia hạn hợp đồng — SUPL ràng buộc auto chuyển trạng thái |
| SUPL-F06 | FEAT 8.2 | Khánh | Chỉnh sửa khóa đào tạo — SUPL ràng buộc auto cập nhật đăng ký |
| SUPL-F07 | FEAT 4.4 | Ninh | Danh mục phụ cấp — SUPL ràng buộc soft-delete |
| SUPL-F08 | FEAT 16.1 | Phúc | Bảo vệ mật khẩu lưu trữ — SUPL ràng buộc mật khẩu không thể khôi phục nguyên văn |
| SUPL-F09 | FEAT 4.5 | Ninh | Danh mục hợp đồng — SUPL ràng buộc soft-delete |
| SUPL-DC01 | FEAT 14.1 | Phúc | Ràng buộc kiến trúc SPA + RESTful API |
| SUPL-DC02 | FEAT 15.1 | Phúc | Ràng buộc mô hình cây tổ chức |
| SUPL-DC03 | FEAT 2.4 | Phúc | Ràng buộc phân quyền theo vai trò |
| SUPL-LR01 | FEAT 13.1 | Phúc | Ràng buộc pháp lý — quản lý đồng ý (Nghị định 13/2023) |
| SUPL-LR02 | FEAT 4.5 | Ninh | Ràng buộc pháp lý — danh mục hợp đồng phê duyệt |
| SUPL-LR03 | FEAT 7.3 | Tùng | Ràng buộc pháp lý — lưu trữ hồ sơ nhân sự 75 năm |
| SUPL-LR04 | FEAT 13.2 | Phúc | Ràng buộc pháp lý — ẩn danh hóa dữ liệu (Nghị định 13/2023) |
| SUPL-LR05 | FEAT 4.4 | Ninh | Ràng buộc pháp lý — danh mục phụ cấp phê duyệt |
| SUPL-LR06 | FEAT 5.1 | Tùng | Ràng buộc pháp lý — lưu trữ hợp đồng 10 năm |
| SUPL-LR07 | FEAT 6.1 | Khánh | Ràng buộc pháp lý — lưu trữ đánh giá 10 năm |
