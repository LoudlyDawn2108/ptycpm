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

### 2.2.1. Phần đóng góp của Nguyễn Hồng Phúc (STRQ 1–3)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | \* Phân tách  \* Làm cho đầy đủ  \* Tổng quát hóa  \* Thêm chi tiết | \* **FEAT 1.1:** Hệ thống phải cho phép người dùng đăng nhập bằng tài khoản.  \* **FEAT 1.2:** Hệ thống phải cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng.  \* **FEAT 1.3:** Hệ thống phải tự động đăng xuất khỏi phiên làm việc nếu người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web trong 30 phút.  \* **FEAT 1.4:** Hệ thống phải cho phép người dùng đổi mật khẩu tài khoản đang sử dụng. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 2.1:** Hệ thống phải cho phép quản trị viên tìm kiếm tài khoản người dùng.  \* **FEAT 2.2:** Hệ thống phải cho phép quản trị viên thêm mới tài khoản người dùng.  \* **FEAT 2.3:** Hệ thống phải cho phép quản trị viên sửa tài khoản người dùng.  \* **FEAT 2.4:** Hệ thống phải cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống tương ứng với các nhóm nghiệp vụ.  \* **FEAT 2.5:** Hệ thống phải cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Khóa/Mở khóa).  \* **FEAT 2.6:** Hệ thống phải tự động khóa tài khoản của nhân sự đã được đánh dấu thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | \* Phân tách  \* Làm cho đầy đủ  \* Thêm chi tiết | \* **FEAT 3.1:** Hệ thống phải cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi.  \* **FEAT 3.2:** Hệ thống phải cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự.  \* **FEAT 3.3:** Hệ thống phải cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự.  \* **FEAT 3.4:** Hệ thống phải cho phép quản trị viên và phòng TCCB thay đổi trạng thái của đơn vị tổ chức nhân sự (Trạng thái: Giải thể/Sáp nhập).  \* **FEAT 3.5:** Hệ thống phải cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. |

**Ghi chú thiết kế – FEAT 2.4:** “Nhóm nghiệp vụ” trong FEAT 2.4 chỉ các vai trò chức năng được hệ thống định nghĩa sẵn, tương ứng với phân nhóm tác nhân: Quản trị viên, Phòng TCCB, Phòng TCKT, Người dùng (Cán bộ/Giảng viên/Nhân viên). Mỗi nhóm nghiệp vụ quy định tập quyền truy cập các chức năng hệ thống khác nhau.

### 2.2.2. Phần đóng góp của Nguyễn Hải Ninh (STRQ 4–6)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 4:** Phòng TCCB có thể cấu hình lương, loại phụ cấp, loại hợp đồng. | \* Phân tách  \* Làm cho đầy đủ | \* **FEAT 4.1:** Hệ thống cho phép phòng TCCB thêm mới hệ số lương (Hệ số lương được thêm sẽ được dùng làm thông tin cho hồ sơ).  \* **FEAT 4.2:** Hệ thống cho phép phòng TCCB sửa thông tin đối với hệ số lương chưa được hồ sơ nào sử dụng, phục vụ sửa chữa nhập liệu lỗi.  \* **FEAT 4.4:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại phụ cấp.  \* **FEAT 4.5:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại hợp đồng. |

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 5:** Phòng TCKT và TCCB muốn thống kê chi tiết về nhân sự. | \* Phân tách  \* Thêm chi tiết | \* **FEAT 5.1:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê tổng quan nhân sự và biến động nhân sự.  \* **FEAT 5.2:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh.  \* **FEAT 5.3:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê hợp đồng, tình trạng làm việc, đánh giá cán bộ.  \* **FEAT 5.4:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê đào tạo, phát triển, bổ nhiệm nhân sự. |
| **STRQ 6:** Hệ thống yêu cầu tự động log dấu vết hoạt động người dùng (System Logging). | \* Phân tách  \* Thêm chi tiết | \* **FEAT 6.1:** Hệ thống tự động ghi vết tất cả các tác vụ truy cập tài khoản, thay đổi/cập nhật hệ thống hoặc dữ liệu.  \* **FEAT 6.2:** Hệ thống cho phép quản trị viên truy xuất xem và xuất Audit log (Nhật ký hệ thống) nhằm truy vết hoạt động. |

### 2.2.3. Phần đóng góp của Ngô Quang Tùng (STRQ 7–8)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 7:** Phòng TCCB có thể tạo hợp đồng lao động của nhân sự. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 7.1:** Hệ thống cho phép phòng TCCB tạo hợp đồng cho nhân sự không có hợp đồng hoặc cần gia hạn hợp đồng.  \* **FEAT 7.2:** Hệ thống cho phép phòng TCCB chi tiết hợp đồng lao động của nhân sự.  \* **FEAT 7.3:** Hệ thống cho phép phòng TCCB chỉnh sửa hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực.  \* **FEAT 7.4:** Hệ thống cho phép phòng TCCB chấm dứt hợp đồng lao động trước hạn của nhân sự. |
| **STRQ 8:** Phòng TCCB muốn quản lý hồ sơ nhân sự như thêm, sửa hồ sơ và cho phép đánh dấu thôi việc nếu nhân sự không còn làm việc, có thêm phương pháp tìm kiếm và lọc để tiện quản lý. | \* Phân tách  \* Làm rõ  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 8.1:** Hệ thống cho phép phòng TCCB và phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa.  \* **FEAT 8.2:** Hệ thống cho phép phòng TCCB và phòng TCKT lọc đa tiêu chí hồ sơ nhân sự.  \* **FEAT 8.3:** Hệ thống cho phép phòng TCCB thêm mới hồ sơ nhân sự (gồm nhập tay hoặc upload từ Excel).  \* **FEAT 8.4:** Hệ thống cho phép phòng TCCB chỉnh sửa hồ sơ nhân sự (thông tin cá nhân, trình độ học vấn, khen thưởng/kỷ luật, quá trình công tác, thông tin hợp đồng).  \* **FEAT 8.5:** Hệ thống cho phép phòng TCCB đánh dấu thôi việc nhân sự.  \* **FEAT 8.6:** Hệ thống tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng.  \* **FEAT 8.7:** Hệ thống cho phép phòng TCCB và phòng TCKT xem chi tiết hồ sơ nhân sự theo từng chế độ xem.  \* **FEAT 8.8:** Hệ thống cho phép phòng TCCB và phòng TCKT in hoặc xuất Excel hồ sơ nhân sự.  \* **FEAT 8.9:** Hệ thống cho phép phòng TCCB cấu hình ẩn/hiện các mục khen thưởng, kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc phòng TCCB. |

### 2.2.4. Phần đóng góp của Ngô Đức Nam Khánh (STRQ 9–12)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 9:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 9.1:** Hệ thống phải cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự.  \* **FEAT 9.2:** Hệ thống phải cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác.  \* **FEAT 9.3:** Hệ thống phải cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 10:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 10.1:** Hệ thống phải cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật).  \* **FEAT 10.2:** Hệ thống phải cho phép phòng TCCB xem lịch sử đánh giá khen thưởng và kỷ luật của nhân sự.  \* **FEAT 10.3:** Hệ thống phải cho phép phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo nhân sự, loại đánh giá, hoặc khoảng thời gian. |
| **STRQ 11:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | \* Phân tách  \* Làm cho đầy đủ  \* Thêm chi tiết | \* **FEAT 11.1:** Hệ thống phải cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ.  \* **FEAT 11.2:** Hệ thống phải cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành).  \* **FEAT 11.3:** Hệ thống phải cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký.  \* **FEAT 11.4:** Hệ thống phải cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
| **STRQ 12:** Người dùng phần mềm có thể xem hồ sơ cá nhân, xem thông tin đơn vị đang công tác và thực hiện các luồng tác vụ cá nhân. | \* Phân tách  \* Làm rõ  \* Thêm chi tiết | \* **FEAT 12.1:** Hệ thống phải cho phép người dùng xem thông tin cá nhân của bản thân.  \* **FEAT 12.2:** Hệ thống phải cho phép người dùng xem thông tin đơn vị mình đang công tác và cơ cấu các thành phần đơn vị trực thuộc.  \* **FEAT 12.3:** Hệ thống phải cho phép người dùng đăng ký hoặc hủy đăng ký tham gia khóa học/đào tạo được nhà trường phê duyệt mở.  \* **FEAT 12.4:** Hệ thống phải cho phép người dùng xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. |

**Ghi chú thiết kế – FEAT 12.3/12.4:** “Luồng tác vụ cá nhân” trong STRQ 12 được giới hạn phạm vi ở đăng ký đào tạo trong phiên bản hiện tại. Các tác vụ cá nhân khác (ví dụ: yêu cầu cập nhật thông tin, đề xuất nghỉ phép) có thể được bổ sung trong các phiên bản sau nếu có yêu cầu từ stakeholder.

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

**Ghi chú:** Tổng cộng hệ thống bao gồm **47 Use Case** (UC 4.1 – UC 4.48), được phân nhóm theo chức năng như sau:

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

* UC Quản lý danh mục Hệ số lương (Thêm mới, Sửa, Thay đổi trạng thái)
* UC Quản lý danh mục Loại phụ cấp (Thêm mới, Sửa, Thay đổi trạng thái)
* UC Quản lý danh mục Loại hợp đồng (Thêm mới, Sửa, Thay đổi trạng thái)

**► Nhóm UC Quản lý Hồ sơ & Nhân sự:**

* UC Tìm kiếm hồ sơ nhân sự
* UC Lọc danh sách hồ sơ nhân sự
* UC Thêm mới Hồ sơ nhân sự
* UC Chỉnh sửa trong chi tiết hồ sơ nhân sự
* UC Xem Chi tiết thông tin hồ sơ nhân sự / In hồ sơ / Xuất Excel
* UC Đánh dấu thôi việc nhân sự
* UC Thêm mới Hợp đồng lao động
* UC Ghi nhận đánh giá khen thưởng/kỷ luật nhân sự
* UC chi tiết hợp đồng lao động
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

**c. Phân rã cho Phòng Tài chính - Kế toán**

* **Tác nhân**: Phòng Tài chính - Kế toán
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Chế độ xem: Tìm kiếm, Xem và Lọc chi tiết hồ sơ nhân sự
  + Xem chi tiết các thống kê
  + Nhóm UC Cá nhân (Self-service): Xem hồ sơ cá nhân, Xem đơn vị công tác, Thay đổi trạng thái đăng ký đào tạo, Xem khóa đào tạo đã đăng ký *(kế thừa quyền Người dùng)*

**d. Phân rã cho Người dùng (Cán bộ/Giảng viên/Nhân viên)**

* **Tác nhân**: Người dùng
* **Các Use Case liên kết**:
  + Đăng nhập / Đăng xuất / Đổi mật khẩu
  + Xem hồ sơ cá nhân
  + Xem thông tin chi tiết đơn vị công tác
  + Thay đổi trạng thái đăng ký đào tạo
  + Xem danh sách các khóa đào tạo đã đăng ký

### 3.3.3. Bảng phân công thành viên cho Use Case

| Thành viên | UCs |
| --- | --- |
| Nguyễn Hồng Phúc | 4.1–4.12 (12) |
| Nguyễn Hải Ninh | 4.13–4.24 (12) |
| Ngô Quang Tùng | 4.25–4.35 (11) |
| Ngô Đức Nam Khánh | 4.36–4.48 (13) |

### 3.3.4. Danh mục Use Case đã đánh số lại

* UC 4.1: Đăng nhập
* UC 4.2: Đăng xuất
* UC 4.3: Đổi mật khẩu
* UC 4.4: Tìm kiếm tài khoản người dùng
* UC 4.5: Thêm mới tài khoản người dùng
* UC 4.6: Sửa thông tin tài khoản người dùng
* UC 4.7: Phân quyền tài khoản người dùng
* UC 4.8: Thay đổi trạng thái cho tài khoản người dùng
* UC 4.9: Tạo mới đơn vị tổ chức nhân sự
* UC 4.10: Sửa thông tin đơn vị tổ chức nhân sự
* UC 4.11: Cập nhật trạng thái cho đơn vị tổ chức nhân sự
* UC 4.12: Xem chi tiết thông tin đơn vị tổ chức nhân sự
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
* UC 4.26: Xem chi tiết hợp đồng lao động
* UC 4.27: Chỉnh sửa hợp đồng lao động chưa có hiệu lực
* UC 4.28: Chấm dứt hợp đồng lao động trước hạn
* UC 4.29: Tìm kiếm hồ sơ nhân sự
* UC 4.30: Lọc danh sách hồ sơ nhân sự
* UC 4.31: Thêm mới Hồ sơ nhân sự
* UC 4.32: Chỉnh sửa trong chi tiết hồ sơ nhân sự
* UC 4.33: Đánh dấu thôi việc nhân sự
* UC 4.34: Xem Chi tiết thông tin hồ sơ nhân sự
* UC 4.35: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật
* UC 4.36: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự
* UC 4.37: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự
* UC 4.38: Ghi nhận đánh giá cho nhân sự
* UC 4.39: Xem lịch sử đánh giá khen thưởng/kỷ luật
* UC 4.40: Tìm kiếm và lọc danh sách đánh giá
* UC 4.41: Mở khóa đào tạo cho cán bộ giảng viên
* UC 4.42: Sửa thông tin khóa đào tạo đã mở
* UC 4.43: Xem chi tiết thông tin khóa đào tạo đã mở
* UC 4.44: Ghi nhận kết quả đào tạo của cán bộ giảng viên
* UC 4.45: Xem các thông tin trong hồ sơ cá nhân của nhân sự
* UC 4.46: Xem thông tin chi tiết đơn vị đang công tác
* UC 4.47: Thay đổi trạng thái đăng ký khóa đào tạo
* UC 4.48: Xem danh sách các khóa đào tạo đã đăng ký

## 3.4. Ma trận truy vết yêu cầu (Traceability Matrix)

| FEAT | UC tương ứng |
| --- | --- |
| FEAT 1.1 | UC 4.1 (Đăng nhập) |
| FEAT 1.2 | UC 4.2 (Đăng xuất) |
| FEAT 1.3 | UC 4.2 A1 (Đăng xuất tự động) |
| FEAT 1.4 | UC 4.3 (Đổi mật khẩu) |
| FEAT 2.1 | UC 4.4 (Tìm kiếm tài khoản người dùng) |
| FEAT 2.2 | UC 4.5 (Thêm mới tài khoản người dùng) |
| FEAT 2.3 | UC 4.6 (Sửa thông tin tài khoản người dùng) |
| FEAT 2.5 | UC 4.8 (Thay đổi trạng thái cho tài khoản người dùng) |
| FEAT 2.6 | UC 4.8 A2 (Tự động khóa tài khoản) |
| FEAT 3.1 | UC 4.9 (Tạo mới đơn vị tổ chức nhân sự) — cấu trúc cây |
| FEAT 3.2 | UC 4.9 (Tạo mới đơn vị tổ chức nhân sự) |
| FEAT 3.3 | UC 4.10 (Sửa thông tin đơn vị tổ chức nhân sự) |
| FEAT 3.4 | UC 4.11 (Cập nhật trạng thái cho đơn vị tổ chức nhân sự) |
| FEAT 3.5 | UC 4.12 (Xem chi tiết thông tin đơn vị tổ chức nhân sự) |
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
| FEAT 7.2 | UC 4.26 (Xem chi tiết hợp đồng lao động) |
| FEAT 7.3 | UC 4.27 (Chỉnh sửa hợp đồng lao động chưa có hiệu lực) |
| FEAT 7.4 | UC 4.28 (Chấm dứt hợp đồng lao động trước hạn) |
| FEAT 8.1 | UC 4.29 (Tìm kiếm hồ sơ nhân sự) |
| FEAT 8.2 | UC 4.30 (Lọc danh sách hồ sơ nhân sự) |
| FEAT 8.3 | UC 4.31 (Thêm mới Hồ sơ nhân sự) |
| FEAT 8.4 | UC 4.32 (Chỉnh sửa trong chi tiết hồ sơ nhân sự) |
| FEAT 8.5 | UC 4.33 (Đánh dấu thôi việc nhân sự) |
| FEAT 8.6 | UC 4.33 A1 (Thôi việc nhân sự tự động) |
| FEAT 8.7 | UC 4.34 (Xem Chi tiết thông tin hồ sơ nhân sự) |
| FEAT 8.8 | UC 4.34 A1/A2 (In hồ sơ / Xuất Excel) |
| FEAT 8.9 | UC 4.35 (Cấu hình ẩn/hiện mục khen thưởng/kỷ luật) |
| FEAT 9.1 | UC 4.36 (Bổ nhiệm nhân sự vào đơn vị tổ chức nhân sự) |
| FEAT 9.2 | UC 4.36 (Điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác) |
| FEAT 9.3 | UC 4.37 (Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự) |
| FEAT 10.1 | UC 4.38 (Ghi nhận đánh giá cho nhân sự) |
| FEAT 10.2 | UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) |
| FEAT 10.3 | UC 4.40 (Tìm kiếm và lọc danh sách đánh giá) |
| FEAT 11.1 | UC 4.41 (Mở khóa đào tạo cho cán bộ giảng viên) |
| FEAT 11.2 | UC 4.42 (Sửa thông tin khóa đào tạo đã mở) |
| FEAT 11.3 | UC 4.43 (Xem chi tiết thông tin khóa đào tạo đã mở) |
| FEAT 11.4 | UC 4.44 (Ghi nhận kết quả đào tạo của cán bộ giảng viên) |
| FEAT 12.1 | UC 4.45 (Xem các thông tin trong hồ sơ cá nhân của nhân sự) |
| FEAT 12.2 | UC 4.46 (Xem thông tin chi tiết đơn vị đang công tác) |
| FEAT 12.3 | UC 4.47 (Thay đổi trạng thái đăng ký khóa đào tạo) |
| FEAT 12.4 | UC 4.48 (Xem danh sách các khóa đào tạo đã đăng ký) |

# IV. ĐẶC TẢ CA SỬ DỤNG

## 4.1 Phần đóng góp của Nguyễn Hồng Phúc (UC 4.1–4.12)

### 4.1. Use Case: Đăng nhập (Nguyễn Hồng Phúc)

|  |  |
| --- | --- |
| **Tên use case** | **Đăng nhập** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng xác thực và truy cập vào hệ thống dựa trên thông tin tài khoản được cấp. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Ấn “Đăng nhập” |
| Điều kiện tiên quyết (Precondition) | Người dùng đã được cấp tài khoản. Hệ thống đang hoạt động bình thường. |
| Điều kiện thành công (Post-condition) | Người dùng được chuyển đến trang chủ (Dashboard) tương ứng với vai trò của mình. |
| Điều kiện thất bại | Tác nhân đăng nhập vào tài khoản thất bại |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng truy cập vào địa chỉ web của hệ thống.  2. Hệ thống hiển thị màn hình Đăng nhập. 3. Người dùng nhập Tên đăng nhập (Mã nhân viên) và Mật khẩu.  4. Người dùng nhấn nút “Đăng nhập”.  5. Hệ thống kiểm tra tính hợp lệ của dữ liệu nhập (không được để trống).  6. Hệ thống xác thực thông tin tài khoản với cơ sở dữ liệu.  7. Hệ thống kiểm tra trạng thái tài khoản (Active/ Lock).  8. Hệ thống xác định vai trò của người dùng.  9. Hệ thống chuyển hướng người dùng đến Dashboard tương ứng. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Đăng nhập khi đã có session**  1. Tại bước 1, Người dùng truy cập trang đăng nhập khi đã có session hợp lệ,  2. Hệ thống tự động chuyển hướng vào Dashboard. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Sai Tên đăng nhập hoặc Mật khẩu** 1. Tại bước 6, hệ thống kiểm tra thông tin không khớp.  2. Hệ thống hiển thị thông báo “Tên đăng nhập hoặc mật khẩu không đúng”.  3. Quay về bước 3  **E2: Tài khoản bị khóa**  1. Tại bước 7, nếu tài khoản bị khóa,  2. Hệ thống hiển thị thông báo “Tài khoản của bạn đã bị khóa. Vui lòng liên hệ Quản trị viên”.  **E3: Không hợp lệ Tên đăng nhập hoặc Mật khẩu**  1. Tại bước 5, hệ thống kiểm tra không hợp lệ  2. Hệ thống hiển thị thông báo “Vui lòng nhập tên đăng nhập và mật khẩu hợp lệ”  3. Quay lại bước 3 |

### 4.2. Use Case: Đăng xuất

|  |  |
| --- | --- |
| **Tên use case** | **Đăng xuất** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự, Hệ thống |
| Mục đích (mô tả) | Cho phép người dùng thoát khỏi phiên làm việc hiện tại một cách an toàn. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Ấn “Đăng xuất” |
| Điều kiện tiên quyết (Precondition) | Người dùng đang trong phiên đăng nhập hợp lệ. |
| Điều kiện thành công (Post-condition) | Phiên làm việc bị hủy bỏ. Người dùng được chuyển về màn hình Đăng nhập. |
| Điều kiện thất bại | Không có |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng chọn “Đăng xuất”.  2. Hệ thống yêu cầu xác nhận đăng xuất  3. Người dùng xác nhận đăng xuất.  4. Hệ thống hủy session hiện tại.  5. Hệ thống chuyển hướng về trang Đăng nhập. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Đăng xuất tự động**  1. Hệ thống giám sát việc người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web.  2. Nếu người dùng không có tương tác giao diện với trang web trong **30 phút**  3. Hệ thống tự động hủy session.  4. Hệ thống hiển thị thông báo “Phiên làm việc đã hết hạn” và chuyển về trang Đăng nhập. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.3. Use Case: Đổi mật khẩu

|  |  |
| --- | --- |
| **Tên use case** | **Đổi mật khẩu** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng đã đăng nhập thay đổi mật khẩu hiện tại sang một mật khẩu mới để tăng cường bảo mật. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Ấn “Đổi mật khẩu” |
| Điều kiện tiên quyết (Precondition) | Người dùng đang đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Mật khẩu được đổi thành công |
| Điều kiện thất bại | Đổi mật khẩu thất bại |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng chọn “Đổi mật khẩu”.  2. Hệ thống hiển thị các trường thông tin: Mật khẩu cũ, mật khẩu mới, xác nhận mật khẩu mới  3. Người dùng nhập dữ liệu.  4. Hệ thống yêu cầu xác nhận.  5. Người dùng xác nhận đổi mật khẩu.  6. Hệ thống kiểm tra dữ liệu  - Kiểm tra “Mật khẩu hiện tại” có khớp với mật khẩu trong CSDL không.  - Kiểm tra “Mật khẩu mới” có đúng quy tắc bảo mật (Độ dài, ký tự đặc biệt) không.  - Kiểm tra “Mật khẩu mới” và “Xác nhận mật khẩu” có khớp nhau không.  - Kiểm tra “Mật khẩu mới” có khác “Mật khẩu hiện tại” không.  7. Hệ thống cập nhật mật khẩu, lưu lịch sử thay đổi và thông báo đổi mật khẩu thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Sai thông tin trường dữ liệu**  1. Tại bước 6, hệ thống phát hiện các lỗi tại các trường thông tin  2. Hệ thống thông báo lỗi  3. Hệ thống từ chối lưu dữ liệu.  **E2: Hủy thao tác**  1. Tại bước 2, người dùng nhấn “Hủy”  2. Hệ thống quay lại màn hình chính. |

### 4.4. Use Case: Tìm kiếm tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên tìm kiếm tài khoản người dùng |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên nhập từ khóa tìm kiếm và thực hiện tìm kiếm trong menu “Quản lý tài khoản người dùng” |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công (Post-condition) | Danh sách tài khoản người dùng thỏa điều kiện tìm kiếm được hiển thị. |
| Điều kiện thất bại | Hệ thống không xử lý được yêu cầu tìm kiếm |
| Luồng sự kiện chính (Basic Flow) | 1. Quản trị viên chọn menu “Quản lý tài khoản người dùng”.  2. Hệ thống hiển thị danh sách người dùng (phân trang).  3. Quản trị viên nhập từ khóa vào ô tìm kiếm (Mã nhân sự, Họ tên, Email).  4. Quản trị viên chọn lọc các thông tin theo dropdown:  - **Vai trò**: Tất cả (Mặc định), Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự  - **Trạng thái**: Tất cả, Hoạt động (Mặc định), Không hoạt động  5. Quản trị viên nhấn nút tìm kiếm.  6. Hệ thống lọc và hiển thị danh sách kết quả tương ứng bao gồm các cột:  - STT  - Mã nhân sự  - Họ tên  - Email  - Vai trò  - Trạng thái |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Không nhập từ khóa**  1. Tại bước 3, Quản trị viên không nhập từ khóa  2. Hệ thống hiển thị toàn bộ danh sách người dùng |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không tìm thấy kết quả**  1. Tại bước 6, Hệ thống không tìm thấy người dùng phù hợp  2. Hệ thống hiển thị thông báo “Không có người dùng” |

### 4.5. Use Case: Thêm mới tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên thêm mới tài khoản người dùng. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên nhấn nút “Thêm mới người dùng”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công (Post-condition) | Tài khoản người dùng mới được tạo và lưu trong cơ sở dữ liệu. |
| Điều kiện thất bại | Tài khoản người dùng không được tạo do dữ liệu không hợp lệ hoặc trùng lặp |
| Luồng sự kiện chính (Basic Flow) | 1. Tại màn hình danh sách, Quản trị viên nhấn nút “Thêm mới”.  2. Hệ thống hiển thị form thêm người dùng.  3. Quản trị viên nhập thông tin: Email, Nhân sự, Vai trò (UC 4.7).  4. Quản trị viên nhấn “Lưu”.  5. Hệ thống validate dữ liệu (Đầy đủ các trường thông tin, Email đúng định dạng và duy nhất, Nhân sự tồn tại và chưa có tài khoản liên kết, Vai trò tồn tại)  6. Hệ thống tự động tạo mật khẩu ngẫu nhiên và gửi mật khẩu đã tạo cho email tương ứng.  7. Hệ thống lưu thông tin.  8. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện các trường thông tin không hợp lệ.  2. Hệ thống thông báo lỗi tương ứng  3. Dữ liệu không được lưu  **E2: Quản trị viên hủy thao tác**  1. Tại bước 2, Quản trị viên nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách người dùng |

### 4.6. Use Case: Sửa thông tin tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên cập nhật thông tin tài khoản người dùng. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên chọn một tài khoản và nhấn nút “Sửa”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. Tài khoản cần chỉnh sửa đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin tài khoản người dùng được cập nhật trong cơ sở dữ liệu. |
| Điều kiện thất bại | Không có thay đổi nào được lưu vào hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Tại danh sách, Quản trị viên nhấn “Sửa” trên một dòng user.  2. Hệ thống hiển thị form cập nhật.  3. Quản trị viên thay đổi Email, Vai trò (UC 4.7).  4. Quản trị viên nhấn “Lưu”.  5. Hệ thống validate dữ liệu (Đầy đủ các trường thông tin, Email đúng định dạng và duy nhất, Vai trò tồn tại).  6. Hệ thống lưu thay đổi.  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện trường dữ liệu không hợp lệ.  2. Hệ thống thông báo lỗi  3. Dữ liệu không được lưu  **E2: Quản trị viên** **hủy thao tác**  1. Tại bước 2, Quản trị viên nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách người dùng |

### 4.8. Use Case: Thay đổi trạng thái cho tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái cho tài khoản người dùng** |
| Tác nhân chính | Quản trị viên, Hệ thống |
| Mục đích (mô tả) | Cho phép Quản trị viên thay đổi trạng thái tài khoản người dùng (Khóa/Mở khóa) |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên chọn chức năng thay đổi trạng thái khóa tài khoản người dùng. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công (Post-condition) | Trạng thái tài khoản người dùng được cập nhật thành Hoạt động hoặc Bị khóa |
| Điều kiện thất bại | Trạng thái tài khoản người dùng không thay đổi. |
| Luồng sự kiện chính (Basic Flow) | 1. Tại danh sách, Quản trị viên nhấn icon “Khóa” trên dòng user có trạng thái ‘Đang hoạt động’(mặc định) .  2. Hệ thống hiển thị xác nhận.  3. Quản trị viên xác nhận.  4. Hệ thống cập nhật trạng thái ‘Bị khóa’ cho tài khoản.  5. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Mở khóa tài khoản**  1. Tại bước 1, Quản trị viên nhấn icon “Mở khóa” trên dòng user tại danh sách. 2. Hệ thống hiển thị xác nhận.  3. Quản trị viên xác nhận  4. Hệ thống cập nhật trạng thái ‘Đang hoạt động’ cho tài khoản.  **A2: Tự động khóa tài khoản**  1. Hệ thống phát hiện nhân sự liên kết với tài khoản đã được đánh dấu thôi việc.  2. Hệ thống cập nhật trạng thái ‘Bị khóa’ cho tài khoản. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không thể khóa tài khoản đang đăng nhập** 1. Tại bước 1, Quản trị viên chọn khóa tài khoản đang sử dụng 2. Hệ thống từ chối thao tác 3. Hiển thị thông báo “Không thể khóa tài khoản đang sử dụng” |

### 4.9. Use Case: Tạo mới đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Tạo mới đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép Người dùng tạo mới một đơn vị tổ chức trong hệ thống, xác định mối quan hệ đơn vị cha – đơn vị con, phục vụ việc xây dựng và quản lý cơ cấu tổ chức nhân sự và nhập liệu thông tin đơn vị đang công tác cho nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng “Thêm mới đơn vị” trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Cán bộ TCCB. Hệ thống đã tồn tại đơn vị gốc “Trường đại học Thủy lợi”. |
| Điều kiện thành công (Post-condition) | Đơn vị tổ chức mới được tạo và lưu thành công trong hệ thống. Đơn vị mới được gắn đúng vào cây cơ cấu tổ chức theo quan hệ cha – con. Sơ đồ cơ cấu tổ chức được cập nhật và hiển thị ngay sau khi tạo. Đơn vị mới có thể được sử dụng để gán thông tin đơn vị công tác cho hồ sơ nhân sự. |
| Điều kiện thất bại | Đơn vị không được tạo do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại.  2. Người dùng chọn một đơn vị làm đơn vị cha (hoặc chọn “đơn vị gốc”).  3. Người dùng nhấn chức năng “Thêm mới đơn vị” dưới cấp của đơn vị đã chọn. 4. Hệ thống hiển thị màn hình nhập thông tin đơn vị mới.  5. Người dùng nhập các thông tin:  \* Tên đơn vị  \* Mã đơn vị  \* Loại đơn vị (Hội đồng, Ban, Khoa, Phòng, Bộ môn, Phòng thí nghiệm, Trung tâm)  \* Đơn vị cha (mặc định là đơn vị đã chọn ở bước 3)  \* Thông tin liên hệ (Ngày thành lập, Địa chỉ, Địa chỉ văn phòng, Email, Số điện thoại, link website(tùy chọn))  \* Xác nhận đơn vị nút (Nếu xác nhận thì ta sẽ không thể thêm mới đơn vị con dưới đơn vị này)  6. Người dùng nhấn “Lưu”.  7. Hệ thống kiểm tra dữ liệu hợp lệ (Dữ liệu cần đầy đủ các trường bắt buộc).  8. Hệ thống xác nhận lưu  9. Người dùng xác nhận  10. Hệ thống lưu đơn vị mới vào cơ sở dữ liệu và trạng thái của đơn vị mặc định là “Đang hoạt động”.  11. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Trùng mã đơn vị**  1. Tại bước 7, hệ thống phát hiện mã đơn vị đã tồn tại.  2. Hệ thống hiển thị thông báo: “Mã đơn vị đã tồn tại. Vui lòng nhập mã khác.”  **E2: Thiếu thông tin bắt buộc**  1. Tại bước 7, hệ thống phát hiện thiếu các trường bắt buộc (Tên đơn vị, Mã đơn vị, Loại đơn vị).  2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung.  3. Quay lại bước 6.  **E3: Đơn vị cha không hợp lệ**  1. Tại bước 3, hệ thống phát hiện người dùng muốn thêm mới tại đơn vị cha đang ở trạng thái Giải thể/Bị sáp nhập.  2. Hệ thống hiển thị thông báo: “Không thể tạo đơn vị trực thuộc đơn vị đã giải thể/ bị sáp nhập”  **E4: Hủy thao tác**  1. Tại bước 5, Người dùng chọn “Hủy”.  2. Quay lại sơ đồ cơ cấu tổ chức.  **E5: Đơn vị cha là đơn vị nút**  1. Tại bước 3, hệ thống phát hiện đơn vị cha đã được xác nhận là đơn vị nút.  2. Hệ thống ẩn/vô hiệu hóa chức năng “Thêm mới đơn vị” dưới cấp đơn vị này và hiển thị thông báo nếu người dùng cố truy cập. |

### 4.10. Use Case: Sửa thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép Người dùng chỉnh sửa thông tin của đơn vị trong cơ cấu tổ chức nhằm đảm bảo dữ liệu luôn chính xác và cập nhật theo thực tế. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng “Sửa thông tin đơn vị” tại màn hình chi tiết đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Cán bộ TCCB. Đơn vị tổ chức cần chỉnh sửa đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin đơn vị được cập nhật thành công. Sơ đồ cơ cấu tổ chức phản ánh dữ liệu mới. |
| Điều kiện thất bại | Thông tin đơn vị không được cập nhật do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ đơn vị hiện tại 2. Người dùng chọn chức năng “Sửa thông tin đơn vị”của một đơn vị.  3. Hệ thống hiển thị form chỉnh sửa với các thông tin hiện tại của đơn vị, bao gồm: **- Thông tin cơ bản:** Tên đơn vị, Mã đơn vị (Không được sửa), Loại đơn vị;  **- Thông tin liên hệ:** Địa chỉ, Địa chỉ văn phòng, Email, Số điện thoại, Website.  4. Người dùng chỉnh sửa các thông tin cần thiết.  5. Người dùng nhấn **“Lưu”**.  6. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  7. Hệ thống xác nhận lưu  8. Người dùng xác nhận.  9. Hệ thống cập nhật thông tin đơn vị.  10. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu không hợp lệ**  1. Tại bước 6, hệ thống phát hiện thiếu dữ liệu bắt buộc hoặc định dạng không hợp lệ.  2. Hệ thống hiển thị cảnh báo và không cho phép lưu.  **E2: Không được phép chỉnh sửa**  1. Tại bước 2, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”.  2. Hệ thống hiển thị thông báo từ chối cho phép chỉnh sửa.  **E3: Hủy thao tác**  1. Tại bước 5, Người dùng chọn “Hủy”.  2. Quay lại sơ đồ cơ cấu tổ chức. |

### 4.11. Use Case: Cập nhật trạng thái cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Cập nhật trạng thái cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép người dùng cập nhật trạng thái hoạt động của đơn vị tổ chức (Giải thể hoặc Sáp nhập), đồng thời xử lý các đơn vị con trực thuộc và tự động cập nhật dữ liệu nhân sự, hợp đồng lao động nhằm đảm bảo tính nhất quán của hệ thống. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng “Cập nhật trạng thái” đối với một đơn vị cụ thể tại menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với quyền Quản trị viên hoặc Phòng TCCB. Đơn vị tổ chức cần cập nhật đã tồn tại và đang ở trạng thái “Đang hoạt động”. |
| Điều kiện thành công (Post-condition) | Trạng thái đơn vị được cập nhật thành “Giải thể” hoặc “Sáp nhập”. Lịch sử thay đổi trạng thái đơn vị được ghi nhận đầy đủ. Dữ liệu nhân sự, hợp đồng lao động và trạng thái làm việc của nhân sự được cập nhật tự động theo quy định nghiệp vụ. |
| Điều kiện thất bại | Việc cập nhật trạng thái đơn vị không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại.  2. Người dùng chọn một đơn vị đang ở trạng thái “Đang hoạt động”.  3. Người dùng chọn chức năng “Cập nhật trạng thái đơn vị”.  4. Hệ thống hiển thị form cập nhật, đồng thời **hiển thị cảnh báo danh sách các đơn vị con trực thuộc** (nếu có).  5. Người dùng chọn loại sự kiện: **Giải thể**. 6. Người dùng nhập các thông tin bắt buộc:  6.1. Ngày hiệu lực (ngày giải thể).  6.2. Quyết định (Số quyết định, Ngày quyết định, File đính kèm).  6.3. Lý do (Giải thể / Tái cơ cấu / Khác). 7. **Xử lý đơn vị con (Nếu có):** Người dùng chọn phương án xử lý cho các đơn vị trực thuộc:  7.1. *Tùy chọn A:* Giải thể toàn bộ đơn vị con.  7.2. *Tùy chọn B:* Điều chuyển đơn vị con sang trực thuộc một đơn vị cha khác (yêu cầu chọn đơn vị cha mới từ danh sách).  8. Người dùng nhấn nút **“Lưu xác nhận”**. 9. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.  10. Hệ thống thực hiện cập nhật đồng loạt: 10.1. Cập nhật trạng thái đơn vị đang thao tác từ “Đang hoạt động” → **“Giải thể”**. 10.2. **Đối với đơn vị con:** Thực hiện Giải thể hoặc Cập nhật đơn vị quản lý cấp trên mới tùy theo lựa chọn tại Bước 7.  10.3. **Đối với nhân sự:**  1. Tất cả hợp đồng đang hiệu lực → “Hết hiệu lực”.  2. Trạng thái hợp đồng của nhân sự → “Chưa hợp đồng”.  3. Trạng thái làm việc của nhân sự → “Đang chờ xét”.  4. Xóa thông tin đơn vị công tác hiện tại của các nhân sự thuộc đơn vị bị giải thể. 11. Hệ thống lưu lịch sử thay đổi và hiển thị thông báo “Cập nhật thành công”. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1.5:** Người dùng chọn loại sự kiện: **Sáp nhập** thay vì Giải thể.  **A1.6:** Người dùng nhập thông tin bắt buộc: Ngày hiệu lực, Quyết định, Lý do và **chọn Đơn vị nhận sáp nhập** từ danh sách đơn vị đang hoạt động.  **A1.7:** **Xử lý đơn vị con:** Hệ thống tự động thiết lập chuyển toàn bộ các đơn vị con trực thuộc sang làm đơn vị con của Đơn vị nhận sáp nhập.  **A1.8:** Người dùng nhấn nút **“Lưu xác nhận”**.  **A1.9:** Hệ thống kiểm tra tính hợp lệ của dữ liệu.  **A1.10:** Hệ thống thực hiện cập nhật đồng loạt: Cập nhật trạng thái đơn vị đang thao tác từ “Đang hoạt động” → **“Sáp nhập”**. **Đối với đơn vị con:** Cập nhật “Đơn vị quản lý cấp trên” sang Đơn vị nhận sáp nhập. **Đối với nhân sự:** Tự động chuyển toàn bộ nhân sự sang Đơn vị nhận sáp nhập (Trạng thái hợp đồng giữ nguyên; Trạng thái làm việc giữ nguyên “Đang công tác”; Thông tin đơn vị mới được cập nhật).  **A1.11:** Hệ thống lưu lịch sử thay đổi và hiển thị thông báo “Cập nhật thành công”. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Đơn vị không hợp lệ để cập nhật trạng thái** \* Tại bước 2, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”.  \* Hệ thống vô hiệu hóa nút chức năng và hiển thị thông báo “Đơn vị này không còn hoạt động”.  **E2: Dữ liệu không hợp lệ**  \* Tại bước 9 hoặc A1.9, nếu thiếu thông tin bắt buộc, ngày hiệu lực sai định dạng hoặc chưa đính kèm file Quyết định.  \* Hệ thống chặn thao tác lưu, bôi đỏ các trường bị lỗi và yêu cầu nhập lại.  **E3: Chưa xử lý đơn vị con khi Giải thể** \* Tại bước 7, nếu đơn vị có đơn vị con nhưng người dùng chọn Tùy chọn B (Điều chuyển) mà không chọn Đơn vị cha mới.  \* Hệ thống cảnh báo: *“Vui lòng chọn đơn vị quản lý mới cho các đơn vị trực thuộc trước khi giải thể.”*  **E4: Ràng buộc chức vụ quản lý**  \* Tại bước 7, nếu đơn vị bị giải thể đang có nhân sự giữ chức vụ quản lý (Trưởng phòng, Trưởng khoa…).  \* Hệ thống chặn thao tác và thông báo: *“Vui lòng thực hiện bãi nhiệm chức vụ quản lý của đơn vị trước khi thực hiện giải thể.”* |

### 4.12. Use Case: Xem chi tiết thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB, Quản trị viên |
| Mục đích (mô tả) | Cho phép Phòng TCCB hoặc Quản trị viên xem đầy đủ thông tin của một đơn vị tổ chức trong cơ cấu tổ chức, bao gồm:  \* Thông tin cơ bản và trạng thái đơn vị  \* Danh sách nhân sự và chức vụ hiện tại  \* Lịch sử bổ nhiệm, miễn nhiệm chức vụ \* Lịch sử thay đổi tổ chức (thành lập, sáp nhập, giải thể) Nhằm phục vụ công tác theo dõi, quản lý và tra cứu dữ liệu tổ chức nhân sự theo thời gian |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB hoặc Quản trị viên chọn chức năng xem chi tiết một đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB hoặc Quản trị viên đã đăng nhập hệ thống. Đơn vị tổ chức đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Toàn bộ thông tin chi tiết của đơn vị được hiển thị chính xác. Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được dữ liệu do lỗi hệ thống hoặc không tồn tại đơn vị. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức.  2. Người dùng chọn một đơn vị trong cây. 3. Hệ thống hiển thị chi tiết thông tin các đơn vị, bao gồm:  \* Tab **“Tổng quan”**, bao gồm: Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị (Đang hoạt động / Sáp nhập / Giải thể)  \* Tab **“Nhân sự”**: Hệ thống hiển thị danh sách các nhân sự, Tên chức vụ, hệ thống hiển thị: Họ tên nhân sự, Mã cán bộ, Ngày bắt đầu. Hệ thống hiển thị danh sách nhân sự thuộc đơn vị  \* Tab **“Đơn vị trực thuộc”**: Hệ thống hiển thị danh sách các đơn vị dưới cấp trực thuộc đơn vị đang xem.  \* Tab **“Lịch sử”**: Hệ thống hiển thị lịch sử bổ nhiệm, miễn nhiệm chức vụ và lịch sử thay đổi tổ chức (thành lập, sáp nhập, giải thể). |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

## 4.2 Phần đóng góp của Nguyễn Hải Ninh (UC 4.13–4.24)

### 4.13. Use Case: Thêm mới danh mục hệ số lương (Nguyễn Hải Ninh)

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB thiết lập hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công (Post-condition) | Thiết lập hệ số lương theo ngạch/bậc thành công |
| Điều kiện thất bại | Hệ số lương không được cập nhật mới trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm hệ số lương.  2.  Hệ thống hiển thị màn hình nhập hệ số lương.  3.  Phòng TCCB nhập các các thông tin  \* Ngạch viên chức  \* Bậc lương  \* Hệ số lương  4.  Phòng TCCB xác nhận lưu thông tin  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống thêm thông tin.  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện lỗi:  \* Bậc lương trong cùng ngạch đã tồn tại  \* Hệ số lương phải là số thực, không được nhỏ hơn 0  \* Bậc lương phải là số nguyên  \* Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi  3. Dữ liệu không được lưu  **E2: Phòng TCCB hủy thao tác**  1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách bậc lương. |

### 4.14. Use Case: Sửa danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu như nhập liệu sai sót. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục hệ số lương cần chỉnh sửa đã tồn tại trong hệ thống. Danh mục hệ số lương đang ở trạng thái “Đang sử dụng”. Hệ số lương chưa được hồ sơ nhân sự nào sử dụng. |
| Điều kiện thành công (Post-condition) | Sửa hệ số lương theo ngạch/bậc thành công |
| Điều kiện thất bại | Hệ số lương không được cập nhật trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa hệ số lương của một bản ghi hệ số lương đã được cấu hình.  2.  Hệ thống hiển thị màn hình nhập hệ số lương.  3.  Phòng TCCB sửa các các thông tin  \* Ngạch viên chức  \* Bậc lương  \* Hệ số lương mỗi bậc  4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống cập nhật thông tin.  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện lỗi:  \* Bậc lương trong cùng ngạch đã tồn tại  \* Hệ số lương phải là số thực, không được nhỏ hơn 0  \* Bậc lương phải là số nguyên  \* Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi  3. Dữ liệu không được lưu  **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**  1. Tại bước 1, hệ thống phát hiện danh mục hệ số lương đang ở trạng thái “Ngừng sử dụng”.  2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”  **E3: Phòng TCCB hủy thao tác**  1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách bậc lương  **E4: Hệ số lương đã được hồ sơ nhân sự sử dụng**  1. Tại bước 1, hệ thống phát hiện hệ số lương đã được ít nhất một hồ sơ nhân sự sử dụng.  2. Hệ thống hiển thị thông báo: “Không thể chỉnh sửa hệ số lương đã được sử dụng trong hồ sơ nhân sự.”  3. Hệ thống vô hiệu hóa nút “Sửa”. |

### 4.16. Use Case: Thay đổi trạng thái danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục hệ số lương giữa “Đang sử dụng” và “Ngừng sử dụng”, nhằm kiểm soát việc áp dụng hệ số lương cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục hệ số lương cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Danh mục hệ số lương được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”). Nếu chuyển sang “Ngừng sử dụng”: hệ số lương không còn được chọn khi tạo hoặc chỉnh sửa hồ sơ nhân sự mới; các hồ sơ nhân sự đã sử dụng hệ số lương này không bị ảnh hưởng. Nếu chuyển sang “Đang sử dụng”: hệ số lương được phép chọn lại khi tạo hoặc chỉnh sửa hồ sơ nhân sự. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn một danh mục hệ số lương đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”. 4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục hệ số lương thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**  1. Tại bước 1, Phòng TCCB chọn một danh mục hệ số lương đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục hệ số lương thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Hủy thao tác**  1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.17. Use Case: Thêm mới danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB thêm mới loại phụ cấp phục vụ cho việc quản lý và nhập liệu thông tin nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công (Post-condition) | Danh mục loại phụ cấp được thêm thành công |
| Điều kiện thất bại | Loại phụ cấp  không được cập nhật mới trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm mới danh mục loại phụ cấp.  2.  Hệ thống hiển thị màn hình nhập danh mục loại phụ cấp.  3.  Phòng TCCB thêm các các thông tin  \* Tên loại phụ cấp  \* Mô tả  \* Cách tính  4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **Không có** |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện lỗi: \* Tên loại phụ cấp dài quá 200 từ, có ký tự đặc biệt không hợp lệ. \* Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi  3. Dữ liệu không được lưu  **E2: Hủy thao tác**  1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách. |

### 4.18. Use Case: Sửa danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa loại phụ cấp phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu có nhập liệu danh mục sai sót |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại phụ cấp cần chỉnh sửa đã tồn tại trong hệ thống. Danh mục loại phụ cấp đang ở trạng thái “Đang sử dụng”. |
| Điều kiện thành công (Post-condition) | Danh mục loại phụ cấp được sửa thành công |
| Điều kiện thất bại | Loại phụ cấp không được cập nhật trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa loại phụ cấp đã tồn tại.  2.  Hệ thống hiển thị màn hình sửa danh mục loại phụ cấp.  3.  Phòng TCCB sửa các các thông tin  \* Tên loại phụ cấp  \* Mô tả  \* Cách tính 4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện lỗi:  2. Tên loại phụ cấp dài quá 200 từ, có ký tự đặc biệt không hợp lệ.  3. Thông tin bắt buộc đầy đủ  4. Hệ thống báo lỗi  5. Dữ liệu không được lưu  **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**  1. Tại bước 1, hệ thống phát hiện danh mục loại phụ cấp đang ở trạng thái “Ngừng sử dụng”.  2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”  **E3: Hủy thao tác**  1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách. |

### 4.19. Use Case: Thay đổi trạng thái danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục loại phụ cấp giữa “Đang sử dụng” và “Ngừng sử dụng”, nhằm kiểm soát việc áp dụng loại phụ cấp cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại phụ cấp cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Danh mục loại phụ cấp được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”). Nếu chuyển sang “Ngừng sử dụng”: loại phụ cấp không còn được chọn khi tạo hoặc chỉnh sửa hồ sơ nhân sự mới; các loại phụ cấp được hồ sơ nhân sự đã sử dụng sẽ được hiển thị khác với các loại phụ cấp ở trạng thái “Đang sử dụng”. Nếu chuyển sang “Đang sử dụng”: loại phụ cấp được phép chọn lại khi tạo hoặc chỉnh sửa hồ sơ nhân sự. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn một danh mục loại phụ cấp đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”. 4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại phụ cấp thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”** 1. Tại bước 1, Phòng TCCB chọn một danh mục loại phụ cấp đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại phụ cấp thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Hủy thao tác**  1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.20. Use Case: Thêm mới danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB cấu hình loại hợp đồng theo quy định nhà nước phục vụ cho việc quản lý và nhập liệu hợp đồng nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công (Post-condition) | Thiết lập loại hợp đồng thành công |
| Điều kiện thất bại | Loại hợp đồng không được cập nhật mới trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm loại hợp đồng.  2.  Hệ thống hiển thị các trường thông tin (Tên loại hợp đồng, Số tháng tối thiểu, Số tháng tối đa, Số lần gia hạn tối đa, thời gian theo ngày chờ gia hạn).  3. Phòng TCCB nhập đầy đủ thông tin 4.  Phòng TCCB xác nhận lưu thông tin  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện lỗi:  \* Số tháng, số lần gia hạn, thời gian chờ gia hạn phải là số nguyên  \* Thông tin bắt buộc đầy đủ  \* Hệ thống báo lỗi  \* Dữ liệu không được lưu  **E2: Phòng TCCB hủy thao tác**  1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách loại hợp đồng |

### 4.21. Use Case: Sửa danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa cấu hình loại hợp đồng theo quy định nhà nước phục vụ cho việc quản lý và nhập liệu hợp đồng nhân sự nếu như nhập liệu sai sót. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại hợp đồng cần chỉnh sửa đã tồn tại trong hệ thống. Danh mục loại hợp đồng đang ở trạng thái “Đang sử dụng”. |
| Điều kiện thành công (Post-condition) | Sửa loại hợp đồng  thành công |
| Điều kiện thất bại | Loại hợp đồng  không được cập nhật trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa loại hợp đồng của một loại hợp đồng đã được cấu hình.  2.  Hệ thống hiển thị màn hình sửa loại hợp đồng và các trường thông tin  (Tên loại hợp đồng, Số tháng tối thiểu, Số tháng tối đa, Số lần gia hạn tối đa, thời gian theo ngày chờ gia hạn).  3.  Phòng TCCB sửa các các thông tin 4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 5, Hệ thống validate phát hiện lỗi: \* Số tháng, số lần gia hạn, thời gian chờ gia hạn phải là số nguyên  \* Thông tin bắt buộc đầy đủ + Hệ thống báo lỗi + Dữ liệu không được lưu  **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**  1. Tại bước 1, hệ thống phát hiện danh mục loại hợp đồng đang ở trạng thái “Ngừng sử dụng”.  2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”  **E3: Phòng TCCB hủy thao tác**  1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách loại hợp đồng |

### 4.22. Use Case: Thay đổi trạng thái danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục loại hợp đồng giữa “Đang sử dụng” và “Ngừng sử dụng”, nhằm kiểm soát việc áp dụng loại hợp đồng cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại hợp đồng cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Danh mục loại hợp đồng được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”). Nếu chuyển sang “Ngừng sử dụng”: loại hợp đồng không còn được chọn khi tạo hoặc chỉnh sửa hợp đồng lao động mới; các loại hợp đồng đã được sử dụng trong hợp đồng lao động sẽ được hiển thị khác với các loại hợp đồng ở trạng thái “Đang sử dụng”. Nếu chuyển sang “Đang sử dụng”: loại hợp đồng được phép chọn lại khi tạo hoặc chỉnh sửa hợp đồng lao động. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn một danh mục loại hợp đồng đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”. 4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại hợp đồng thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**  1. Tại bước 1, Phòng TCCB chọn một danh mục loại hợp đồng đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại hợp đồng thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Hủy thao tác**  1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.23. Use Case: Xem chi tiết các thống kê

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết các thống kê** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cung cấp cho Phòng TCCB, Phòng TCKT có các báo cáo tổng hợp, thống kê trực quan về tình hình nhân sự, cơ cấu tổ chức, đào tạo và biến động nhân sự theo thời gian; hỗ trợ theo dõi, phân tích và ra quyết định quản lý. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn menu “Báo cáo và Thống kê” trên hệ thống. |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB hoặc Phòng TCKT đã đăng nhập hệ thống. Dữ liệu nhân sự, đơn vị, đào tạo đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Các báo cáo thống kê được hiển thị đầy đủ, chính xác. Người dùng có thể xem chi tiết, lọc dữ liệu và xuất báo cáo theo nhu cầu. |
| Điều kiện thất bại | Không hiển thị được báo cáo do lỗi dữ liệu hoặc hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng truy cập menu **“Báo cáo và Thống kê”**.  2. Hệ thống hiển thị **Danh sách nhóm báo cáo**.  3. Người dùng chọn từng nhóm báo cáo để xem chi tiết.  \* Báo cáo tổng quan nhân sự  \* Báo cáo biến động nhân sự  \* Báo cáo cơ cấu nhân sự theo đơn vị  \* Báo cáo cơ cấu nhân sự theo trình độ, học hàm, chức danh  \* Báo cáo bổ nhiệm nhân sự  \* Báo cáo đào tạo và phát triển  \* Báo cáo hợp đồng và tình trạng làm việc \* Báo cáo đánh giá của cán bộ với khóa đào tạo  4. Hệ thống hiển thị dữ liệu thống kê tương ứng dưới dạng biểu đồ và bảng đa dạng theo thời gian, đơn vị, loại nhân sự. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Xuất báo cáo**  1. Tại bước 4, Người dùng chọn chức năng “Xuất báo cáo” (Định dạng xuất: PDF / Excel, Phạm vi dữ liệu (theo bộ lọc hiện tại))  2. Người dùng xác nhận xuất  3. Hệ thống tạo file báo cáo và cho phép tải về |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.24. Use Case: Xem nhật ký hệ thống (Audit Log)

|  |  |
| --- | --- |
| **Tên use case** | **Xem nhật ký hệ thống (Audit Log)** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên xem, tìm kiếm và lọc nhật ký ghi lại toàn bộ các thao tác quan trọng trên hệ thống (đăng nhập, thêm/sửa/xóa dữ liệu, phân quyền, thay đổi trạng thái…) nhằm phục vụ công tác giám sát, kiểm tra an ninh và truy vết sự cố. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên chọn menu “Nhật ký hệ thống” (Audit Log). |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. Hệ thống đã ghi nhận các bản ghi nhật ký từ hoạt động của người dùng. |
| Điều kiện thành công (Post-condition) | Danh sách nhật ký hệ thống được hiển thị đầy đủ, chính xác theo tiêu chí lọc. Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được nhật ký do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Quản trị viên chọn menu “Nhật ký hệ thống”.  2. Hệ thống hiển thị danh sách nhật ký (phân trang), mỗi bản ghi bao gồm:  \* Thời gian thao tác,  \* Tài khoản thực hiện (Username),  \* Họ tên người thực hiện,  \* Vai trò,  \* Loại hành động (Đăng nhập / Đăng xuất / Thêm / Sửa / Xóa / Phân quyền / Thay đổi trạng thái),  \* Đối tượng bị tác động (Tên module, Mã đối tượng),  \* Mô tả chi tiết thay đổi,  \* Địa chỉ IP.  3. Quản trị viên có thể lọc nhật ký theo các tiêu chí:  \* Khoảng thời gian: Từ ngày – Đến ngày \* Tài khoản thực hiện: Nhập Username hoặc Họ tên  \* Loại hành động: Tất cả (Mặc định), Đăng nhập, Đăng xuất, Thêm, Sửa, Xóa, Phân quyền, Thay đổi trạng thái  \* Module: Tất cả (Mặc định), Quản lý tài khoản, Hồ sơ nhân sự, Cơ cấu tổ chức, Hợp đồng, Đào tạo, Danh mục cấu hình  4. Quản trị viên nhấn “Tìm kiếm” hoặc “Áp dụng bộ lọc”.  5. Hệ thống hiển thị kết quả nhật ký phù hợp với tiêu chí đã chọn.  6. Quản trị viên có thể nhấn vào một bản ghi để xem chi tiết thay đổi (giá trị trước và sau khi thay đổi). |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Xuất nhật ký**  1. Tại bước 5, Quản trị viên chọn chức năng “Xuất nhật ký”.  2. Hệ thống cho phép xuất danh sách nhật ký theo bộ lọc hiện tại dưới định dạng Excel hoặc PDF.  3. Quản trị viên xác nhận xuất.  4. Hệ thống tạo file và cho phép tải về. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không tìm thấy kết quả**  1. Tại bước 5, nếu không có bản ghi nhật ký nào phù hợp với tiêu chí lọc, Hệ thống hiển thị thông báo: “Không tìm thấy nhật ký phù hợp với tiêu chí tìm kiếm.” |

## 4.3 Phần đóng góp của Ngô Quang Tùng (UC 4.25–4.35)

### 4.25. Use Case: Thêm mới Hợp đồng lao động

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Tạo mới hợp đồng với quản lý trạng thái và ràng buộc nghiệp vụ. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Thêm mới hợp đồng”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống. Hồ sơ nhân sự đã được tạo |
| Điều kiện thành công (Post-condition) | Hợp đồng lao động mới được tạo và gắn với hồ sơ nhân sự. Trạng thái hợp đồng của nhân sự được cập nhật theo hợp đồng mới nhất. |
| Điều kiện thất bại | Hợp đồng không được tạo do vi phạm ràng buộc nghiệp vụ hoặc lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn mục “Thêm mới hợp đồng”.  2. Hệ thống yêu cầu nhập mã nhân sự  3. Phòng TCCB nhập Mã nhân sự.  4. Hệ thống kiểm tra: Mã nhân sự có tồn tại không và nếu tồn tại chỉ cho phép tạo hợp đồng mới nếu nhân viên có trạng thái hợp đồng “Chưa hợp đồng” hoặc “Chờ gia hạn” hoặc “Còn hiệu lực” với thời gian còn lại nằm trong thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính thoiGianChoGiaHan tại UC 4.20).  5. Chọn Loại hợp đồng.  6. Hệ thống kiểm tra số lần ký tối đa cho loại hợp đồng.  7. Nhập thông tin hợp đồng:   * Số HĐ * Ngày ký * Ngày hiệu lực * Ngày hết hạn * Đơn vị công tác theo hợp đồng * Nội dung hợp đồng (rich text editor - nhập điều khoản, mô tả công việc, quyền lợi…) * Upload PDF bản hợp đồng giấy (tải lên bản scan/file gốc đã ký)   8. Hệ thống validate thời hạn Thời gian tối thiểu/ Thời gian tối đa của loại hợp đồng. 9. Nhấn “Lưu”.  10. Hệ thống cập nhật hợp đồng mới với trạng thái mặc định ‘Còn hiệu lực’, đồng thời cập nhật trạng thái hợp đồng của nhân sự thành ‘Còn hiệu lực’.  11. Hệ thống lưu hợp đồng vào hồ sơ cá nhân và thông báo thành công. *Lưu ý: Xem UC 4.26 (Xem hợp đồng), UC 4.27 (Sửa hợp đồng lao động) và UC 4.28 (Chấm dứt hợp đồng lao động trước hạn) cho các tác vụ liên quan.* |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không đủ điều kiện tạo hợp đồng mới do hợp đồng hiện tại còn hiệu lực**  1. Tại bước 4, hệ thống phát hiện nhân sự không tồn tại hoặc nhân sự đang có hợp đồng ở trạng thái “Còn hiệu lực” và thời gian còn lại > thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính thoiGianChoGiaHan tại UC 4.20).  2. Hệ thống từ chối tạo hợp đồng mới.  3. Hệ thống hiển thị thông báo: *“Không thể tạo hợp đồng mới”*  **E2: Vượt quá số lần ký hợp đồng cho phép**  1. Tại bước 5, hệ thống kiểm tra số lần ký hợp đồng theo loại hợp đồng đã chọn của nhân sự.  2. Hệ thống không cho phép tiếp tục tạo hợp đồng.  3. Hiển thị thông báo: *“Vui lòng chọn loại hợp đồng khác.”*  **E3: Thời gian hợp đồng không hợp lệ hoặc trùng lặp**  1. Tại bước 8, hệ thống phát hiện: Thời hạn hợp đồng không nằm trong khoảng Min/Max theo quy định hoặc ngày hiệu lực của hợp đồng mới ≤ ngày hết hạn của hợp đồng cũ chưa chấm dứt. Các trường dữ liệu chưa đầy đủ  2. Hệ thống hiển thị thông báo: “Thời gian hợp đồng không hợp lệ hoặc bị trùng với hợp đồng trước”  3. Phòng TCCB quay lại bước 5  **E4: Hủy thao tác**  1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. |

### 4.26. Use Case: Xem chi tiết hợp đồng lao động (FEAT 7.2)

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem danh sách toàn bộ hợp đồng lao động đã gắn với một hồ sơ nhân sự và xem chi tiết từng hợp đồng nhằm phục vụ tra cứu, đối chiếu và quản lý thông tin hợp đồng của nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn tab “Hợp đồng” trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Danh sách hợp đồng và thông tin chi tiết của hợp đồng được hiển thị đầy đủ, chính xác theo dữ liệu đã lưu. Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin hợp đồng do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.34).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **“Hợp đồng”**.  4. Hệ thống hiển thị danh sách tất cả hợp đồng lao động của nhân sự, bao gồm các thông tin: Số hợp đồng, Loại hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Trạng thái hợp đồng.  5. Phòng TCCB chọn một hợp đồng trong danh sách.  6. Hệ thống hiển thị chi tiết hợp đồng đã chọn, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, Thông tin lương/quyền lợi theo hợp đồng (nếu có), File PDF đính kèm và Trạng thái hợp đồng. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Nhân sự chưa có hợp đồng lao động** 1. Tại bước 3, nếu hồ sơ nhân sự chưa có hợp đồng nào được lưu.  2. Hệ thống hiển thị tab **“Hợp đồng”** ở trạng thái trống và thông báo: *“Nhân sự chưa có hợp đồng lao động.”* |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.27. Use Case: Chỉnh sửa hợp đồng lao động chưa có hiệu lực (FEAT 7.3)

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa hợp đồng lao động chưa có hiệu lực** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa thông tin hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực, nhằm sửa sai sót nhập liệu hoặc cập nhật nội dung trước thời điểm hợp đồng bắt đầu áp dụng, đồng thời bảo đảm toàn vẹn dữ liệu hợp đồng. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Sửa hợp đồng” tại màn hình chi tiết hợp đồng của nhân sự. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Hợp đồng lao động của nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin hợp đồng được cập nhật thành công. Lịch sử thay đổi hợp đồng được ghi nhận. |
| Điều kiện thất bại | Hợp đồng không được cập nhật do vi phạm ràng buộc nghiệp vụ, dữ liệu không hợp lệ hoặc hợp đồng không thuộc trạng thái cho phép chỉnh sửa. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động của nhân sự từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Nếu hợp đồng đang ở trạng thái **“Chưa có hiệu lực”**, hệ thống hiển thị nút **“Sửa hợp đồng”**.  4. Phòng TCCB chọn **“Sửa hợp đồng”**.  5. Hệ thống hiển thị màn hình chỉnh sửa và cho phép cập nhật các thông tin của hợp đồng, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, File PDF đính kèm. 6. Phòng TCCB chỉnh sửa thông tin và nhấn **“Lưu”**.  7. Hệ thống kiểm tra dữ liệu hợp lệ và kiểm tra ràng buộc nghiệp vụ: hợp đồng vẫn phải ở trạng thái **“Chưa có hiệu lực”**, thời gian hợp đồng hợp lệ, không trùng lặp với các hợp đồng khác của cùng nhân sự.  8. Hệ thống cập nhật thông tin hợp đồng, lưu lịch sử thay đổi và thông báo thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Hợp đồng đã có hiệu lực hoặc đã hết hiệu lực**  1. Tại bước 3, nếu hợp đồng không ở trạng thái **“Chưa có hiệu lực”**.  2. Hệ thống ẩn hoặc vô hiệu hóa nút **“Sửa hợp đồng”** và hiển thị thông báo: *“Chỉ được chỉnh sửa hợp đồng chưa có hiệu lực.”*  **A2: Dữ liệu chỉnh sửa không hợp lệ**  1. Tại bước 7, hệ thống phát hiện thiếu thông tin bắt buộc, thời gian hợp đồng không hợp lệ hoặc dữ liệu bị trùng lặp.  2. Hệ thống hiển thị cảnh báo và yêu cầu Phòng TCCB chỉnh sửa lại thông tin. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.28. Use Case: Chấm dứt hợp đồng lao động trước hạn (FEAT 7.4)

|  |  |
| --- | --- |
| **Tên use case** | **Chấm dứt hợp đồng lao động trước hạn** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chấm dứt trước hạn một hợp đồng lao động đang còn hiệu lực của nhân sự, cập nhật lại trạng thái hợp đồng và hỗ trợ xem xét nghiệp vụ thôi việc khi nhân sự không còn hợp đồng còn hiệu lực nào. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Chấm dứt trước hạn” tại màn hình chi tiết hợp đồng. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Hợp đồng lao động cần chấm dứt đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Hợp đồng được cập nhật trạng thái **“Hết hiệu lực”** kèm thông tin ngày chấm dứt và lý do chấm dứt trước hạn. Trạng thái hợp đồng hiện tại của nhân sự được cập nhật tương ứng. |
| Điều kiện thất bại | Không thể chấm dứt hợp đồng trước hạn do hợp đồng không ở trạng thái cho phép, dữ liệu không hợp lệ hoặc người dùng không xác nhận thao tác. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Phòng TCCB chọn một hợp đồng đang ở trạng thái **“Còn hiệu lực”** và nhấn **“Chấm dứt trước hạn”**.  4. Hệ thống hiển thị biểu mẫu yêu cầu nhập **Ngày chấm dứt trước hạn** và **Lý do chấm dứt**.  5. Phòng TCCB nhập thông tin và nhấn xác nhận.  6. Hệ thống hiển thị hộp thoại xác nhận thao tác chấm dứt trước hạn.  7. Phòng TCCB xác nhận thao tác.  8. Hệ thống cập nhật hợp đồng sang trạng thái **“Hết hiệu lực”**, lưu ngày chấm dứt và lý do chấm dứt trước hạn.  9. Hệ thống cập nhật trạng thái hợp đồng hiện tại của nhân sự theo dữ liệu mới.  10. Nếu đây là hợp đồng còn hiệu lực duy nhất của nhân sự, hệ thống hiển thị thông báo để Phòng TCCB xem xét tiếp tục thực hiện UC 4.33 **“Đánh dấu thôi việc nhân sự”** nếu phù hợp nghiệp vụ. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Hủy thao tác chấm dứt trước hạn**  1. Tại bước 6, Phòng TCCB chọn **“Hủy”**. 2. Hệ thống đóng hộp thoại xác nhận và không cập nhật dữ liệu hợp đồng.  **A2: Hợp đồng không ở trạng thái còn hiệu lực**  1. Tại bước 3, nếu hợp đồng không ở trạng thái **“Còn hiệu lực”**.  2. Hệ thống không cho phép thực hiện chức năng **“Chấm dứt trước hạn”** và hiển thị thông báo phù hợp. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.29. Use Case: Tìm kiếm hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích (mô tả) | Cho phép cán bộ Phòng TCCB, phòng TCKT tìm kiếm hồ sơ nhân sự nhanh chóng dựa trên từ khóa như tên, mã nhân sự, số CCCD, email hoặc số điện thoại nhằm phục vụ công tác quản lý và tra cứu thông tin. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng nhập từ khóa tìm kiếm và thực hiện tìm kiếm trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết (Precondition) | Cán bộ TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Danh sách nhân sự thỏa mãn điều kiện được hiển thị |
| Điều kiện thất bại | Hệ thống không xử lý yêu cầu tìm kiếm |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB, phòng TCKT chọn menu “Quản lý Hồ sơ”.  2. Hệ thống hiển thị danh sách hồ sơ nhân viên (Mã, Họ tên, CCCD, Giới tính, Địa chỉ, SĐT liên hệ, Chức danh khoa học, Đơn vị công tác, Chức vụ đơn vị, Trạng thái công việc, Trạng thái hợp đồng) có phân trang.  3. Phòng TCCB, phòng TCKT **nhập từ khóa** vào ô tìm kiếm (Tên, Mã, CCCD, SĐT).  4. Hệ thống hiển thị kết quả tìm kiếm theo từ khóa (real-time). |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Từ khóa tìm kiếm rỗng**  1. Tại bước 3, nếu phòng TCCB, phòng TCKT không nhập từ khóa  2. Hệ thống hiển thị toàn bộ danh sách hồ sơ nhân sự |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không có kết quả tìm kiếm**  1. Tại bước 4, nếu không có hồ sơ nào phù hợp với từ khóa  2. Hệ thống hiển thị thông báo: *“Không tìm thấy hồ sơ phù hợp.”* |

### 4.30. Use Case: Lọc danh sách hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Lọc danh sách hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT lọc danh sách hồ sơ nhân sự dựa trên nhiều tiêu chí nhằm thu hẹp phạm vi dữ liệu phục vụ công tác quản lý. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB, phòng TCKT chọn tiêu chí lọc trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Danh sách hồ sơ nhân sự được hiển thị đúng theo các tiêu chí lọc đã chọn |
| Điều kiện thất bại | Hệ thống không hiển thị yêu cầu lọc danh sách theo tiêu chí đã chọn do lỗi hệ thống |
| Luồng sự kiện chính (Basic Flow) | 1. Tại màn hình danh sách, Phòng TCCB, phòng TCKT nhấn “Bộ lọc nâng cao”.  2. Hệ thống hiển thị panel lọc với nhiều tiêu chí:  \* **Đơn vị công tác:** Chọn Khoa, Phòng, Ban, Bộ môn  \* **Chức danh khoa học:** GS, PGS, Không có  \* **Chức vụ đơn vị:**Trưởng khoa, Phó khoa, Không chức vụ  \* **Trạng thái làm việc:** Đang chờ xét,Đang công tác, Đã thôi việc  \* **Trạng thái hợp đồng:** Chưa hợp đồng, Còn hiệu lực, Hết hiệu lực, Chờ gia hạn.  \* **Giới tính:** Nam, Nữ  3. Phòng TCCB, phòng TCKT chọn các tiêu chí lọc.  4. Nhấn “Áp dụng bộ lọc”.  5. Hệ thống hiển thị kết quả lọc đa tiêu chí. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không có kết quả lọc**  1. Tại bước 5, nếu không có hồ sơ nào thỏa mãn tiêu chí đã chọn  2. Hệ thống hiển thị thông báo *“Không có hồ sơ phù hợp với tiêu chí lọc.”* |

### 4.31. Use Case: Thêm mới Hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tạo mới và lưu trữ đầy đủ thông tin hồ sơ nhân sự trên hệ thống. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng thêm trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Hồ sơ nhân sự được tạo mới |
| Điều kiện thất bại | Hệ thống không thể tạo mới hồ sơ do lỗi hệ thống hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Tại màn hình danh sách, Phòng TCCB nhấn “Thêm mới”.  2. Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3. Phòng TCCB nhập các trường thông tin:  \* **Thông tin chung bắt buộc**: Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ.  \* **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn “Người nước ngoài”, hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động.  \* **Thông tin gia đình (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình.  \* **Thông tin ngân hàng (bắt buộc)**: Tên Ngân hàng, Số tài khoản.  \* **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**.  \* **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết.  \* **Upload ảnh chân dung (bắt buộc).**  \* **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học.  \* **Thông tin các bằng cấp (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf.  \* **Thông tin các chứng chỉ (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf.  \* **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình).  4. Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5. Phòng TCCB nhấn “Lưu”.  6. Hệ thống tự động sinh Mã cán bộ và Trạng thái hợp đồng mặc định là “Chưa hợp đồng”, Trạng thái làm việc là “Đang chờ xét”.  7. Hệ thống lưu hồ sơ, lịch sử tạo hồ sơ và thông báo thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Tạo mới hồ sơ nhân sự từ file Excel** 1. Tại bước 1 của Luồng sự kiện chính, Phòng TCCB chọn chức năng **“Thêm mới từ Excel”**.  2. Hệ thống hiển thị màn hình tải lên file Excel và cung cấp **file mẫu** theo định dạng quy định.  3. Phòng TCCB tải lên file Excel chứa danh sách hồ sơ nhân sự.  4. Hệ thống kiểm tra: Định dạng file, Cấu trúc cột dữ liệu, Các trường thông tin bắt buộc, và tính hợp lệ logic của dữ liệu từng dòng  5. Tiếp tục bước 5 của luồng chính |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**  1. Tại bước 4, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ.  2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ.  **E2: Hủy thao tác**  1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. |

### 4.32. Use Case: Chỉnh sửa trong chi tiết hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa trong chi tiết hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB sửa và lưu lại đầy đủ thông tin hồ sơ nhân sự trên hệ thống nếu có thay đổi hoặc sai sót trong nhập liệu. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng sửa trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB đã đăng nhập hệ thống. Hồ sơ nhân sự có trạng thái làm việc “Đang chờ xét”, “Đang công tác” |
| Điều kiện thành công (Post-condition) | Hồ sơ nhân sự được cập nhật. Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Hồ sơ nhân sự không được cập nhật và thay đổi |
| Luồng sự kiện chính (Basic Flow) | 1. Tại màn hình danh sách, Phòng TCCB nhấn “Sửa” một nhân sự tại danh sách.  2. Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3. Phòng TCCB có thể sửa các trường thông tin:  \* **Thông tin chung bắt buộc**: Mã cán bộ (không thể sửa), Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ.  \* **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn “Người nước ngoài”, hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động.  \* **Thông tin gia đình (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình.  \* **Thông tin ngân hàng (bắt buộc)**: Tên Ngân hàng, Số tài khoản.  \* **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**.  \* **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết.  \* **Upload ảnh chân dung (bắt buộc).**  \* **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học.  \* **Thông tin các bằng cấp (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf.  \* **Thông tin các chứng chỉ (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf.  \* **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình).  \* *Lưu ý: Thông tin hợp đồng được quản lý qua UC 4.25 (Thêm mới Hợp đồng lao động), UC 4.26 (Xem hợp đồng), UC 4.27 (Sửa hợp đồng lao động), UC 4.28 (Chấm dứt hợp đồng lao động trước hạn). Thông tin đánh giá (khen thưởng/kỷ luật) được quản lý qua UC 4.38 (Ghi nhận đánh giá cho nhân sự), UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) và UC 4.40 (Tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật). Xem UC 4.35 (Cấu hình ẩn/hiện mục khen thưởng/kỷ luật) cho chức năng ẩn/hiện — tách ra từ FEAT 8.9.* 4. Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5. Cán bộ TCCB nhấn “Lưu”.  6. Hệ thống lưu hồ sơ, lịch sử tạo hồ sơ và thông báo thành công |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**  1. Tại bước 5, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ.  2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ.  **E2: Hủy thao tác**  1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. **E3: Hồ sơ ở trạng thái “Đã thôi việc”**  1. Tại bước 1, hệ thống phát hiện hồ sơ nhân sự đang ở trạng thái làm việc “Đã thôi việc”.  2. Hệ thống hiển thị thông báo: “Không thể chỉnh sửa hồ sơ nhân sự đã thôi việc.” và vô hiệu hóa nút “Sửa”. |

### 4.33. Use Case: Đánh dấu thôi việc nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Đánh dấu thôi việc nhân sự** |
| Tác nhân chính | Phòng TCCB, Hệ thống |
| Mục đích (mô tả) | Cho phép phòng TCCB cập nhật trạng thái làm việc “Đã thôi việc” cho hồ sơ nhân sự |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng đánh dấu thôi việc trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB đã đăng nhập hệ thống. Nhân sự cần đánh dấu thôi việc đang ở trạng thái làm việc khác “Đã thôi việc”. |
| Điều kiện thành công (Post-condition) | Trạng thái của nhân sự được cập nhật thành “Đã thôi việc” trong hồ sơ nhân sự thành công.Trạng thái hợp đồng được cập nhật thành “Hết hiệu lực” (nếu nhân sự có hợp đồng ở trạng thái “Còn hiệu lực” hoặc “Chờ gia hạn”). Nhân sự được gỡ khỏi đơn vị công tác. Tài khoản liên kết được tự động khóa. |
| Điều kiện thất bại | Trạng thái làm việc “Đã thôi việc” không được cập nhật |
| Luồng sự kiện chính (Basic Flow) | 1. Tại màn hình danh sách, phòng TCCB chọn chức năng “Đánh dấu thôi việc” một nhân sự.  2. Hệ thống yêu cầu xác nhận và nhập ngày, lý do thôi việc.  3. Phòng TCCB xác nhận.  4. Hệ thống cập nhật trạng thái làm việc thành “Đã thôi việc”, trạng thái hợp đồng thành “Hết hiệu lực” (nếu có hợp đồng đang hiệu lực hoặc chờ gia hạn), nhân sự được cập nhật rời khỏi đơn vị công tác.  5. Hệ thống tự động khóa tài khoản liên kết của nhân sự (cập nhật trạng thái tài khoản thành ‘Bị khóa’). |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Thôi việc nhân sự tự động**  1. Hệ thống tự động cập nhật trạng thái hợp đồng “Hết hiệu lực” cho loại hợp đồng ở trạng thái “Chờ gia hạn” khi đã quá thời gian gia hạn được cấu hình và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng.  2. Hệ thống tự động cập nhật trạng thái làm việc cho nhân sự vừa bị cập nhật trạng thái hợp đồng “Hết hiệu lực” thành “Đã thôi việc”.  3. Hệ thống tự động gỡ nhân sự khỏi đơn vị công tác hiện tại.  4. Hệ thống tự động cập nhật trạng thái tài khoản liên kết thành “Bị khóa”.  **A2: Thôi việc khi hợp đồng còn hiệu lực (thanh lý trước hạn)**  1. Tại bước 1, hệ thống phát hiện nhân sự có hợp đồng ở trạng thái “Còn hiệu lực”. 2. Hệ thống hiển thị cảnh báo: “Nhân sự này vẫn còn hợp đồng đang có hiệu lực. Tiếp tục sẽ thanh lý hợp đồng trước hạn.” 3. Hệ thống yêu cầu nhập lý do thanh lý hợp đồng trước hạn (ngoài ngày và lý do thôi việc ở bước 2 Basic Flow).  4. Phòng TCCB xác nhận.  5. Tiếp tục bước 4 của Basic Flow.  **A3: Tự động chuyển trạng thái hợp đồng sang “Chờ gia hạn”**  1. Hệ thống (System Timer) định kỳ kiểm tra các hợp đồng đang ở trạng thái “Còn hiệu lực”.  2. Nếu thời gian còn lại của hợp đồng ≤ thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính thoiGianChoGiaHan tại UC 4.20)  3. Hệ thống tự động cập nhật trạng thái hợp đồng từ “Còn hiệu lực” sang “Chờ gia hạn”.  4. Hệ thống tự động cập nhật trạng thái hợp đồng của nhân sự thành “Chờ gia hạn”. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Nhân sự đã ở trạng thái “Đã thôi việc”**  1. Tại bước 1, hệ thống phát hiện nhân sự đã có trạng thái làm việc “Đã thôi việc”.  2. Hệ thống vô hiệu hóa nút “Đánh dấu thôi việc” hoặc hiển thị cảnh báo: *“Nhân sự này đã được đánh dấu thôi việc trước đó.”*  **E2: Nhân sự chưa bãi nhiệm chức vụ**  1. Tại bước 1, hệ thống phát hiện nhân sự đang giữ chức vụ quản lý (Trưởng khoa, Trưởng bộ môn…).  2. Hệ thống chặn thao tác và thông báo: “Vui lòng bãi nhiệm chức vụ của nhân sự trước khi đánh dấu thôi việc.”  **E3: Hủy thao tác**  1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Hệ thống quay lại màn hình danh sách nhân sự. |

### 4.34. Use Case: Xem Chi tiết thông tin hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem Chi tiết thông tin hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT xem chi tiết toàn bộ thông tin hồ sơ nhân sự, có thể thực hiện in hồ sơ |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB, phòng TCKT chọn chức năng xem chi tiết trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin chi tiết hồ sơ nhân sự được hiển thị đầy đủ, chính xác ở chế độ chỉ đọc. |
| Điều kiện thất bại | Hệ thống không hiển thị được thông tin hồ sơ do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính (Basic Flow) | 1. Tại danh sách, Phòng TCCB, phòng TCKT nhấn vào nhấn “Xem chi tiết” tại một nhân sự.  2. Hệ thống hiển thị màn hình Chi tiết hồ sơ ở chế độ chỉ đọc.  3. Hệ thống hiển thị đầy đủ thông tin theo các tab:  \* **Tab “Thông tin chung”:** Mã cán bộ,Lý lịch, liên hệ, gia đình, ảnh chân dung  \* **Tab “Trình độ & Chức danh”:** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác.  \* **Tab “Thông tin Đảng/ Đoàn”:** Thông tin Đảng/ Đoàn đã được lưu.  \* **Tab “Lương & Phụ cấp”:** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng  \* **Tab “Hợp đồng”:** Thông tin về các loại hợp đồng đồng đã ký  \* **Tab “Khen thưởng/Kỷ luật”:** Hệ thống hiển thị mục khen thưởng/kỷ luật tùy theo cấu hình ẩn/hiện (xem UC 4.35, FEAT 8.9) và vai trò người dùng hiện tại  \* **Tab “Công tác”:** Quá trình công tác trước khi về trường đã được ghi |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: In hồ sơ**  1. Tiếp tục bước 3, Phòng TCCB và TCKT có thể in ra hồ sơ ở định dạng PDF  **A2: Xuất ra Excel**  1. Tiếp tục bước 3, Phòng TCCB và TCKT có thể xuất ra file chứa tất cả thông tin dưới định dạng file Excel |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.35. Use Case: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật (FEAT 8.9)

|  |  |
| --- | --- |
| **Tên use case** | **Cấu hình ẩn/hiện mục khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB cấu hình ở mức toàn hệ thống việc ẩn/hiện các mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự đối với các vai trò không thuộc Phòng TCCB, nhằm kiểm soát phạm vi hiển thị thông tin theo vai trò sử dụng. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng cấu hình hiển thị hồ sơ nhân sự trong menu cấu hình hệ thống. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống và có quyền cấu hình hệ thống. |
| Điều kiện thành công (Post-condition) | Cấu hình ẩn/hiện mục **Khen thưởng/Kỷ luật** được lưu thành công và áp dụng ngay ở mức hệ thống cho các màn hình xem hồ sơ liên quan (tham chiếu UC 4.34 và UC 4.45). Các vai trò được cấu hình là **“Ẩn”** sẽ không nhìn thấy mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự. Phòng TCCB luôn nhìn thấy đầy đủ các mục này bất kể cấu hình. |
| Điều kiện thất bại | Cấu hình không được cập nhật do lỗi hệ thống hoặc người dùng không lưu thay đổi. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập menu **cấu hình hệ thống**.  2. Hệ thống hiển thị danh sách nhóm cấu hình.  3. Phòng TCCB chọn nhóm cấu hình **“Hiển thị hồ sơ nhân sự”**.  4. Hệ thống hiển thị các vai trò không thuộc Phòng TCCB (ví dụ: Phòng TCKT, Cán bộ/Giảng viên/Người dùng) cùng các tùy chọn ẩn/hiện đối với mục **Khen thưởng** và **Kỷ luật**.  5. Phòng TCCB bật/tắt cấu hình hiển thị cho từng vai trò.  6. Phòng TCCB nhấn **“Lưu”**.  7. Hệ thống lưu cấu hình, thông báo thành công và áp dụng ngay cho các màn hình xem hồ sơ nhân sự tương ứng. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Không thay đổi cấu hình**  1. Tại bước 5, Phòng TCCB không thực hiện thay đổi nào và chọn **“Hủy”** hoặc thoát màn hình.  2. Hệ thống không cập nhật cấu hình và giữ nguyên thiết lập hiện tại. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

## 4.4 Phần đóng góp của Ngô Đức Nam Khánh (UC 4.36–4.48)

### 4.36. Use Case: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB bổ nhiệm nhân sự vào các đơn vị tổ chức |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng bổ nhiệm trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống. Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức. Nhân sự phải có trạng thái hợp đồng ‘Còn hiệu lực’ hoặc ‘Chờ gia hạn’ và trạng thái làm việc ‘Đang chờ xét’ hoặc ‘Đang công tác’. |
| Điều kiện thành công (Post-condition) | Nhân sự được bổ nhiệm nhân sự vào đơn vị. Thông tin nhân sự của đơn vị được cập nhật. |
| Điều kiện thất bại | Việc bổ nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Phòng TCCB chọn bổ nhiệm nhân sự chưa công tác  3. Hệ thống hiển thị danh sách nhân sự ở trạng thái “Đang chờ xét” và trạng thái hợp đồng “Còn hiệu lực”.  4. Phòng TCCB chọn nhân sự và nhập thông tin như (Chức vụ, Ngày bắt đầu)  5. Hệ thống kiểm tra hợp lệ (Ngày bắt đầu).  6. Hệ thống thay đổi danh sách nhân sự, trạng thái công việc của nhân sự chuyển thành “Đang công tác ”và thông báo thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Bổ nhiệm nhân sự đang công tác ở đơn vị khác**   1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức. 2. Phòng TCCB chọn bổ nhiệm nhân sự đang công tác tại đơn vị khác. 3. Hệ thống yêu cầu chọn đơn vị, chọn nhân sự từ đơn vị được chọn. 4. Phòng TCCB chọn nhân sự và nhập thông tin như (Chức vụ, Ngày bắt đầu) 5. Hệ thống kiểm tra hợp lệ (Ngày bắt đầu). 6. Hệ thống gỡ nhân sự khỏi đơn vị cũ, thêm vào đơn vị mới, cập nhật danh sách nhân sự của cả hai đơn vị và thông báo thành công. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu không hợp lệ**  1. Tại bước 5, Hệ thống kiểm tra phát hiện:  \* Ngày bắt đầu < ngày hiện tại  2. Hệ thống yêu cầu nhập lại và không lưu dữ liệu.  **E2: Không được phép tiếp tục**  1. Tại bước 1, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”.  2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục cập nhật bổ nhiệm. |

### 4.37. Use Case: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thực hiện bãi nhiệm nhân sự trong đơn vị tổ chức, nhằm cập nhật chính xác tình trạng nhân sự và phục vụ công tác quản lý nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng bãi nhiệm nhân sự của đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức. |
| Điều kiện thành công (Post-condition) | Nhân sự được miễn nhiệm khỏi chức vụ. Trạng thái công việc của nhân sự được cập nhật thành “Đang chờ xét”. Nhân sự được xóa khỏi danh sách của đơn vị tổ chức. |
| Điều kiện thất bại | Việc bãi nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Hệ thống hiển thị danh sách nhân sự  3. Phòng TCCB chọn chức năng bãi nhiệm từ trong một nhân sự trong danh sách.  4. Hệ thống yêu cầu xác nhận thao tác.  5. Phòng TCCB xác nhận thao tác miễn nhiệm.  6. Hệ thống cập nhật trạng thái công việc của nhân sự là “Đang chờ xét”  và xóa nhân sự khỏi danh sách của đơn vị tổ chức. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không được phép tiếp tục**  1. Tại bước 3, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”.  2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục thực hiện bãi nhiệm. |

### 4.38. Use Case: Ghi nhận đánh giá cho nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận đánh giá cho nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Ghi nhận các quyết định đánh giá đối với nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Thêm đánh giá khen thưởng hoặc kỷ luật” |
| Điều kiện tiên quyết (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống. Hồ sơ nhân sự đã được tạo Nhân sự không ở trạng thái làm việc ‘Đã thôi việc’. |
| Điều kiện thành công (Post-condition) | Hồ sơ nhân sự được cập nhật. Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Dữ liệu đánh giá không được ghi nhận vào hệ thống do thiếu các trường thông tin bắt buộc, hoặc do lỗi kết nối cơ sở dữ liệu/phiên đăng nhập hết hạn |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn tab ” Thêm đánh giá khen thưởng hoặc kỷ luật”.  2. Hệ thống yêu cầu nhập mã nhân sự và chọn loại đánh giá  3. Phòng TCCB nhập mã nhân sự và chọn loại đánh giá (Khen thưởng/ Kỷ luật) 4.  Hệ thống hiển thị giao diện nhập liệu:   * Nếu chọn loại đánh giá là khen thưởng: ‘Loại khen thưởng’, ‘Tên khen thưởng’, ‘Ngày quyết định’, ‘Số quyết định’, ‘Nội dung’, ‘Số tiền thưởng (nếu có)’. * Nếu chọn loại đánh giá là kỷ luật: Loại kỷ luật, ‘Tên kỷ luật’,  Ngày quyết định, Lý do, Hình thức xử lý.   5. Nhấn “Lưu”.  6. Hệ thống kiểm tra dữ liệu hợp lệ (Đầy đủ các trường thông tin)  7. Hệ thống lưu dữ liệu và đẩy vào hồ sơ cá nhân và thông báo thành công.  *Lưu ý: Xem UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) và UC 4.40 (Tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật) cho các tác vụ tra cứu liên quan.* |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Mã nhân sự không hợp lệ**  1. Tại bước 3, Hệ thống phát hiện mã nhân sự không tồn tại.  2. Hệ thống từ chối tiếp tục tạo bản đánh giá.  **E2: Dữ liệu không hợp lệ**  1. Tại bước 6, Hệ thống phát hiện dữ liệu không đầy đủ các trường thông tin.  2. Hệ thống từ chối lưu thông tin và thông báo lỗi.  **E3: Hủy thao tác**  1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. **E4: Nhân sự đã thôi việc**  1. Tại bước 3, hệ thống phát hiện nhân sự đang ở trạng thái làm việc “Đã thôi việc”. 2. Hệ thống từ chối ghi nhận đánh giá và hiển thị thông báo: “Không thể ghi nhận đánh giá cho nhân sự đã thôi việc.” |

### 4.39. Use Case: Xem lịch sử đánh giá khen thưởng/kỷ luật (FEAT 10.2)

|  |  |
| --- | --- |
| **Tên use case** | **Xem lịch sử đánh giá khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem lịch sử toàn bộ các bản ghi đánh giá khen thưởng và kỷ luật của một nhân sự theo trình tự thời gian, phục vụ tra cứu, đối chiếu và theo dõi hồ sơ đánh giá của nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn tab “Khen thưởng/Kỷ luật” trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Lịch sử đánh giá khen thưởng/kỷ luật của nhân sự được hiển thị đầy đủ, chính xác. Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không thể hiển thị lịch sử đánh giá do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.34).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **“Khen thưởng/Kỷ luật”**.  4. Hệ thống hiển thị danh sách toàn bộ bản ghi đánh giá của nhân sự theo thứ tự thời gian, bao gồm các thông tin: Ngày quyết định, Loại đánh giá (Khen thưởng/Kỷ luật), Tên đánh giá, Số quyết định, Mô tả ngắn/Nội dung.  5. Phòng TCCB chọn một bản ghi đánh giá trong danh sách.  6. Hệ thống hiển thị chi tiết bản ghi đã chọn, bao gồm đầy đủ thông tin đã được ghi nhận từ UC 4.38. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Nhân sự chưa có lịch sử đánh giá**  1. Tại bước 3, nếu hồ sơ nhân sự chưa có bản ghi khen thưởng hoặc kỷ luật nào.  2. Hệ thống hiển thị tab **“Khen thưởng/Kỷ luật”** ở trạng thái trống và thông báo: *“Nhân sự chưa có lịch sử đánh giá khen thưởng/kỷ luật.”* |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.40. Use Case: Tìm kiếm và lọc danh sách đánh giá (FEAT 10.3)

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm và lọc danh sách đánh giá** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tìm kiếm và lọc danh sách các bản ghi khen thưởng/kỷ luật theo nhân sự, loại đánh giá hoặc khoảng thời gian nhằm phục vụ công tác tra cứu, thống kê và đối chiếu dữ liệu đánh giá. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB truy cập chức năng quản lý đánh giá khen thưởng/kỷ luật. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Danh sách các bản ghi đánh giá phù hợp với điều kiện tìm kiếm/lọc được hiển thị đầy đủ, chính xác. Phòng TCCB có thể tiếp tục xem chi tiết từng bản ghi. |
| Điều kiện thất bại | Hệ thống không thể xử lý yêu cầu tìm kiếm/lọc do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập chức năng **quản lý đánh giá khen thưởng/kỷ luật**.  2. Hệ thống hiển thị danh sách các bản ghi đánh giá và vùng bộ lọc tìm kiếm.  3. Phòng TCCB nhập từ khóa tìm kiếm và/hoặc chọn các tiêu chí lọc, bao gồm: Nhân sự (Mã cán bộ/Họ tên), Loại đánh giá (Khen thưởng/Kỷ luật), Khoảng thời gian (Từ ngày – Đến ngày).  4. Phòng TCCB nhấn **“Tìm kiếm”** hoặc **“Áp dụng bộ lọc”**.  5. Hệ thống hiển thị danh sách kết quả phù hợp với tiêu chí đã chọn, bao gồm các thông tin: Mã cán bộ, Họ tên, Loại đánh giá, Tên đánh giá, Ngày quyết định, Số quyết định.  6. Phòng TCCB có thể chọn một bản ghi bất kỳ trong danh sách kết quả.  7. Hệ thống hiển thị chi tiết bản ghi đánh giá đã chọn (tham chiếu UC 4.39). |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Không có kết quả phù hợp** 1. Tại bước 5, nếu không có bản ghi nào phù hợp với tiêu chí tìm kiếm/lọc.  2. Hệ thống hiển thị thông báo: *“Không tìm thấy đánh giá phù hợp với tiêu chí tìm kiếm.”* |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.41. Use Case: Mở khóa đào tạo cho cán bộ giảng viên

|  |  |
| --- | --- |
| **Tên use case** | **Mở khóa đào tạo cho cán bộ giảng viên** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Cán bộ TCCB tạo mới và thiết lập thông tin một khóa đào tạo dành cho cán bộ, giảng viên; cấu hình hình thức đào tạo, thời gian, kinh phí và điều kiện đăng ký, làm cơ sở cho việc đăng ký tham gia và quản lý đào tạo sau này. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng mở khóa học trong menu “Đào tạo & Phát triển” |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Khóa đào tạo được tạo mới và lưu thành công. Trạng thái khóa đào tạo được thiết lập theo cấu hình. |
| Điều kiện thất bại | Khóa đào tạo không được tạo do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1.  Phòng TCCB chọn menu “Đào tạo & Phát triển”.  2.  Phòng TCCB nhấn “Tạo khóa đào tạo mới”.  3. Hệ thống hiển thị thông tin nhập 4.  Phòng TCCB nhập thông tin: Tên khóa đào tạo, Loại khóa đào tạo (theo cấu hình), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo (Tên chứng chỉ, Loại chứng chỉ). 5.  Phòng TCCB thiết lập thời gian mở đăng ký từ ngày - đến ngày, Giới hạn số người tham gia.  6. Phòng TCCB nhấn “Lưu”.  7. Hệ thống kiểm tra dữ liệu hợp lệ.  8. Hệ thống yêu cầu xác nhận tạo khóa đào tạo.  9. Phòng TCCB xác nhận.  10. Hệ thống lưu khóa đào tạo và thiết lập trạng thái ban đầu là “Đang mở đăng ký” |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**  1. Tại bước 7, hệ thống phát hiện thiếu các trường bắt buộc (Tên khóa, Loại khóa, Thời gian), thời gian mở đăng ký kết thúc sau ngày bắt đầu đào tạo.  2. Hệ thống hiển thị cảnh báo và yêu cầu chỉnh sửa.  **E2: Hủy thao tác**  1. Tại bước 4, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.42. Use Case: Sửa thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa các thông tin của khóa đào tạo đã được tạo nhằm cập nhật kế hoạch đào tạo phù hợp với thực tế, đồng thời đảm bảo không vi phạm các ràng buộc nghiệp vụ đối với khóa đào tạo đã mở đăng ký hoặc đã có người tham gia |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Sửa thông tin khóa đào tạo” tại một khóa đào tạo trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Khóa đào tạo đã tồn tại trong hệ thống. Khóa đào tạo đang ở trạng thái “Đang mở đăng ký” hoặc “Đang đào tạo”. |
| Điều kiện thành công (Post-condition) | Thông tin khóa đào tạo được cập nhật thành công. Các thay đổi được ghi nhận và áp dụng ngay cho khóa đào tạo. |
| Điều kiện thất bại | Thông tin khóa đào tạo không được cập nhật do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo.  3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Sửa thông tin”**.  4. Hệ thống hiển thị màn hình chỉnh sửa thông tin khóa đào tạo.  5. Phòng TCCB chỉnh sửa các thông tin cho phép:   * Tên khóa đào tạo * Địa điểm * Kinh phí (nếu có) * Cam kết sau đào tạo (nếu có) * Thông tin chứng chỉ sau đào tạo * Trạng thái khóa đào tạo * Thời gian mở đăng ký và giới hạn số người tham gia (nếu được phép)   6. Phòng TCCB nhấn **“Lưu”**.  7. Hệ thống kiểm tra tính hợp lệ và ràng buộc nghiệp vụ (bao gồm kiểm tra chuyển trạng thái khóa đào tạo phải tuân theo thứ tự: Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước).  8. Hệ thống yêu cầu xác nhận cập nhật.  9. Phòng TCCB xác nhận.  10. Hệ thống cập nhật thông tin khóa đào tạo và thông báo thành công.  *Lưu ý: Khi trạng thái khóa đào tạo được chuyển sang “Đang đào tạo”, hệ thống tự động batch-update tất cả đăng ký tham gia có trạng thái “Đã đăng ký” sang “Đang học”.* |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Chỉnh sửa khi khóa đào tạo đang diễn ra**  1. Tại bước 4, nếu khóa đào tạo ở trạng thái “Đang đào tạo”, hệ thống chỉ cho phép chỉnh sửa: Địa điểm, Kinh phí, Cam kết sau đào tạo, Thông tin chứng chỉ sau đào tạo.  2. Hệ thống khóa không cho phép chỉnh sửa: Tên khóa đào tạo, Loại khóa đào tạo, Thời gian mở đăng ký, Giới hạn số người tham gia.  3. Tiếp tục từ bước 6. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Chuyển trạng thái không hợp lệ**  1. Tại bước 7, hệ thống phát hiện trạng thái mới được chọn vi phạm thứ tự chuyển đổi (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước).  2. Hệ thống hiển thị thông báo: *“Chuyển trạng thái không hợp lệ.”* và yêu cầu chọn lại.  **E2: Vi phạm ràng buộc đăng ký**  1. Tại bước 7, hệ thống phát hiện nếu: Giảm giới hạn số người tham gia nhỏ hơn số lượng đã đăng ký.  2. Hệ thống hiển thị cảnh báo và không cho phép lưu.  **E3: Dữ liệu không hợp lệ**  1. Tại bước 7, hệ thống phát hiện thiếu trường bắt buộc hoặc thời gian không hợp lệ.  2. Hệ thống yêu cầu chỉnh sửa lại thông tin.  **E4: Hủy thao tác**  1. Tại bước 5, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.43. Use Case: Xem chi tiết thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem đầy đủ thông tin chi tiết của một khóa đào tạo đã được tạo, bao gồm trạng thái khóa học, thông tin tổ chức đào tạo, danh sách cán bộ – giảng viên đăng ký tham gia, và tình trạng tham gia của từng nhân sự, nhằm phục vụ công tác quản lý, theo dõi và ra quyết định điều chỉnh khóa đào tạo khi cần thiết. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn một khóa đào tạo và nhấn chức năng “Xem chi tiết” trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Khóa đào tạo đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin chi tiết của khóa đào tạo được hiển thị đầy đủ và chính xác. Phòng TCCB có thể theo dõi tình trạng khóa học và danh sách nhân sự tham gia. |
| Điều kiện thất bại | Không thể hiển thị thông tin khóa đào tạo do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo.  3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Xem chi tiết”**.  4. Hệ thống hiển thị màn hình chi tiết khóa đào tạo, hiển thị đầy đủ thông tin theo yêu cầu bao gồm các thông tin:   * **Thông tin chung khóa đào tạo**: Tên khóa đào tạo, Loại khóa đào tạo, Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo. * **Thông tin đăng ký**: Thời gian mở đăng ký, Giới hạn số lượng người tham gia, Số lượng đã đăng ký / số lượng tối đa * **Danh sách tham gia**: Hệ thống hiển thị danh sách cán bộ, giảng viên đã đăng ký khóa đào tạo, bao gồm (Họ và tên, Mã cán bộ, Đơn vị đang công tác, Thời điểm đăng ký, Trạng thái tham gia |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.44. Use Case: Ghi nhận kết quả đào tạo của cán bộ giảng viên

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận kết quả đào tạo của cán bộ giảng viên** |
| Tác nhân chính | Cán bộ TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB ghi nhận kết quả tham gia khóa đào tạo của cán bộ, giảng viên sau khi khóa học kết thúc; cập nhật trạng thái hoàn thành, không đạt và lưu trữ chứng chỉ đào tạo vào hồ sơ nhân sự nhằm phục vụ công tác quản lý và đánh giá năng lực. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Ghi nhận kết quả đào tạo” tại tab “Danh sách học viên” của một khóa đào tạo. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Khóa đào tạo đã tồn tại trong hệ thống. Trạng thái khóa đào tạo là “Đã hoàn thành”. Khóa đào tạo có danh sách học viên đã đăng ký. |
| Điều kiện thành công (Post-condition) | Kết quả đào tạo của từng học viên được ghi nhận thành công. Trạng thái tham gia của học viên được cập nhật (Hoàn thành / Không đạt). Chứng chỉ đào tạo (nếu có) được lưu vào hồ sơ cá nhân của nhân sự. Lịch sử đào tạo của nhân sự được cập nhật. |
| Điều kiện thất bại | Kết quả đào tạo không được ghi nhận do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2. Chọn xem chi tiết “Danh sách học viên” có một khóa đào tạo có trạng thái “Đã hoàn thành”.  3. Hệ thống hiển thị danh sách học viên tham gia khóa đào tạo, bao gồm: Họ tên, Mã cán bộ, Đơn vị công tác, Trạng thái tham gia hiện tại (Đang học)  4. Phòng TCCB chọn một học viên và nhấn **“Ghi nhận kết quả”**.  5. Hệ thống hiển thị form ghi nhận kết quả, bao gồm: Trạng thái kết quả: Hoàn thành/ Không đạt, Ngày hoàn thành (mặc định là ngày kết thúc khóa học), File chứng chỉ (PDF) (tùy chọn, bắt buộc nếu trạng thái là “Hoàn thành”)  6. Phòng TCCB nhập thông tin và nhấn **“Lưu”**.  7. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  8. Hệ thống cập nhật trạng thái học viên:   * Nếu **Hoàn thành** (Ghi nhận kết quả đào tạo, Lưu chứng chỉ vào hồ sơ nhân sự). * Nếu **Không đạt** (Chỉ lưu trạng thái kết quả, không cập nhật chứng chỉ, Hệ thống thông báo ghi nhận kết quả thành công). |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Ghi nhận kết quả cho nhiều học viên**  1. Tại bước 4, Phòng TCCB có thể chọn nhiều học viên.  2. Hệ thống cho phép ghi nhận kết quả hàng loạt với cùng trạng thái.  3. Tiếp tục bước 5 |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Khóa đào tạo chưa hoàn thành**  1. Tại bước 4, nếu trạng thái khóa đào tạo khác “Đã hoàn thành”.  2. Hệ thống hiển thị thông báo: *“Chỉ có thể ghi nhận kết quả khi khóa đào tạo đã hoàn thành.”*  **E2: Thiếu chứng chỉ khi hoàn thành, Dữ liệu không hợp lệ**  1. Tại bước 8, Hệ thống phát hiện thiếu thông tin bắt buộc hoặc file không đúng định dạng hoặc nếu học viên được đánh dấu “Hoàn thành” nhưng không upload file chứng chỉ (trong trường hợp bắt buộc).  2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. |

### 4.45. Use Case: Xem các thông tin trong hồ sơ cá nhân của nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem các thông tin trong hồ sơ cá nhân của nhân sự** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép CBGV xem toàn bộ thông tin hồ sơ cá nhân của mình đang được lưu trong hệ thống, tra cứu lịch sử hợp đồng, hệ số, bậc lương, các quyết định khen thưởng và kỷ luật của bản thân.. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | CB/GV chọn chức năng “Hồ sơ cá nhân” trên giao diện hệ thống |
| Điều kiện tiên quyết (Precondition) | CB/GV đã đăng nhập. |
| Điều kiện thành công (Post-condition) | Thông tin hồ sơ cá nhân được hiển thị đầy đủ cho CBGV. |
| Điều kiện thất bại | Không thể hiển thị thông tin hồ sơ cá nhân do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1.  CB/GV chọn các mục kích hoạt chức năng xem hồ sơ nhân sự  2.  Hệ thống hiển thị đầy đủ thông tin theo các tab:   * **Tab “Thông tin chung”:** Mã cán bộ,Lý lịch, liên hệ, gia đình, ảnh chân dung \* * **Tab “Trình độ & Chức danh”:** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác. * **Tab “Thông tin Đảng/ Đoàn”:** Thông tin Đảng/ Đoàn đã được lưu. * **Tab “Lương & Phụ cấp”:** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng \* **Tab “Hợp đồng”:** Thông tin về các loại hợp đồng đã ký * **Tab “Khen thưởng/Kỷ luật”:** Mục khen thưởng/kỷ luật chỉ hiển thị nếu phòng TCCB đã cấu hình cho phép (xem UC 4.35, FEAT 8.9) * **Tab “Công tác”:** Quá trình công tác |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.46. Use Case: Xem thông tin chi tiết đơn vị đang công tác

|  |  |
| --- | --- |
| **Tên use case** | **Xem thông tin chi tiết đơn vị đang công tác** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên xem thông tin chi tiết về đơn vị tổ chức mà mình đang công tác trong cơ cấu tổ chức của đơn vị, bao gồm thông tin cơ bản của đơn vị, danh sách chức vụ và nhân sự hiện tại trong đơn vị. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Cán bộ/Giảng viên chọn chức năng xem thông tin đơn vị công tác từ hồ sơ cá nhân hoặc menu liên quan. |
| Điều kiện tiên quyết (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống. Cán bộ/Giảng viên đã được gán đơn vị công tác trong hệ thống. Đơn vị tổ chức đang tồn tại trong cơ cấu tổ chức. |
| Điều kiện thành công (Post-condition) | Thông tin chi tiết của đơn vị công tác được hiển thị đầy đủ và chính xác. Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin do lỗi hệ thống hoặc không xác định được đơn vị công tác của CBGV. |
| Luồng sự kiện chính (Basic Flow) | 1. Cán bộ/Giảng viên truy cập chức năng xem thông tin đơn vị công tác.  2. Hệ thống xác định đơn vị mà Cán bộ/Giảng viên đang trực thuộc.  3. Hệ thống hiển thị thông tin chi tiết của đơn vị, bao gồm:   * Tab **“Tổng quan”**, bao gồm: Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị (Đang hoạt động / Sáp nhập / Giải thể) * Tab **“Nhân sự”**: Hệ thống hiển thị danh sách các nhân sự, Tên chức vụ, hệ thống hiển thị: Họ tên nhân sự, Mã cán bộ, Ngày bắt đầu. Hệ thống hiển thị danh sách nhân sự thuộc đơn vị * Tab **“Đơn vị trực thuộc”**: Hệ thống hiển thị danh sách các đơn vị dưới cấp trực thuộc đơn vị đang xem. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

### 4.47. Use Case: Thay đổi trạng thái đăng ký khóa đào tạo

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái đăng ký khóa đào tạo** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên đăng ký hoặc hủy đăng ký tham gia các khóa đào tạo do nhà trường tổ chức đang trong thời gian mở đăng ký, làm cơ sở cho việc quản lý học viên, theo dõi quá trình và ghi nhận kết quả đào tạo. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Cán bộ/Giảng viên chọn menu “Đào tạo”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống. Khóa đào tạo tồn tại và đang ở trạng thái **“Đang mở đăng ký”**. Thời điểm hiện tại nằm trong khoảng **Thời gian mở đăng ký**. |
| Điều kiện thành công (Post-condition) | Đăng ký tham gia khóa đào tạo của CBGV được ghi nhận trong hệ thống (trường hợp đăng ký). Bản ghi đăng ký của CBGV được xóa khỏi hệ thống (trường hợp hủy đăng ký). |
| Điều kiện thất bại | Không thể thay đổi trạng thái đăng ký do khóa đào tạo không hợp lệ, hết hạn đăng ký hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Cán bộ/Giảng viên truy cập menu “Đào tạo”.  2. Hệ thống hiển thị danh sách các khóa đào tạo ở trạng thái Đang mở đăng ký.  3. Cán bộ/Giảng viên chọn một khóa đào tạo để xem chi tiết thông tin.  4. Hệ thống hiển thị thông tin chi tiết khóa đào tạo. Nếu CBGV chưa đăng ký, hiển thị nút “Đăng ký tham gia”. Nếu CBGV đã đăng ký (trạng thái tham gia là “Đã đăng ký”), hiển thị nút “Hủy đăng ký”.  5. Cán bộ/Giảng viên nhấn nút “Đăng ký tham gia”.  6. Hệ thống kiểm tra các điều kiện đăng ký (thời gian mở đăng ký, số lượng đăng ký chưa đạt giới hạn, trạng thái khóa đào tạo).  7. Hệ thống tạo bản ghi đăng ký đào tạo và thiết lập trạng thái tham gia là “Đã đăng ký”.  8. Hệ thống thông báo đăng ký thành công cho Cán bộ/Giảng viên. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Hủy đăng ký khóa đào tạo**  1. Tại bước 4, CBGV đã đăng ký khóa đào tạo này với trạng thái tham gia “Đã đăng ký”. Hệ thống hiển thị nút “Hủy đăng ký”.  2. Cán bộ/Giảng viên nhấn nút “Hủy đăng ký”.  3. Hệ thống yêu cầu xác nhận hủy đăng ký.  4. Cán bộ/Giảng viên xác nhận.  5. Hệ thống kiểm tra trạng thái tham gia phải là “Đã đăng ký” và khóa đào tạo phải đang ở trạng thái “Đang mở đăng ký”.  6. Hệ thống xóa bản ghi đăng ký đào tạo của CBGV.  7. Hệ thống thông báo hủy đăng ký thành công. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Hết thời gian đăng ký**  1. Tại bước 4, nếu thời gian hiện tại nằm ngoài khoảng mở đăng ký.  2. Hệ thống ẩn nút “Đăng ký tham gia” và “Hủy đăng ký”, hiển thị thông báo: *“Khóa đào tạo đã hết thời gian đăng ký.”*  **E2: Đã đủ số lượng người tham gia**  1. Tại bước 6, nếu số lượng đăng ký đã đạt giới hạn.  2. Hệ thống hiển thị thông báo: *“Khóa đào tạo đã đủ số lượng đăng ký.”*  **E3: Không thể hủy đăng ký**  1. Tại bước A1.5, nếu trạng thái tham gia không phải “Đã đăng ký” (ví dụ: đã chuyển sang “Đang học” do khóa đào tạo đã bắt đầu) hoặc khóa đào tạo không còn ở trạng thái “Đang mở đăng ký”.  2. Hệ thống hiển thị thông báo: *“Không thể hủy đăng ký do khóa đào tạo đã chuyển sang giai đoạn tiếp theo.”* |

### 4.48. Use Case: Xem danh sách các khóa đào tạo đã đăng ký

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách các khóa đào tạo đã đăng ký** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên xem danh sách tất cả các khóa đào tạo mà mình đã đăng ký tham gia, theo dõi trạng thái tham gia và kết quả đào tạo của từng khóa (Đang học, Hoàn thành, Không đạt), phục vụ việc tra cứu, theo dõi quá trình học tập và kết quả đào tạo cá nhân. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Chọn menu “Đào tạo” |
| Điều kiện tiên quyết (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống. Cán bộ/Giảng viên đã từng đăng ký ít nhất một khóa đào tạo |
| Điều kiện thành công (Post-condition) | Danh sách các khóa đào tạo đã đăng ký của Cán bộ/Giảng viên được hiển thị đầy đủ và chính xác. Trạng thái tham gia và kết quả đào tạo của từng khóa được hiển thị đúng theo dữ liệu do Phòng TCCB ghi nhận. |
| Điều kiện thất bại | Không hiển thị được danh sách do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính (Basic Flow) | 1. Cán bộ/Giảng viên truy cập chức năng **“Khóa đào tạo đã đăng ký”**.  2. Hệ thống truy xuất danh sách các khóa đào tạo mà Cán bộ/Giảng viên đã đăng ký. 3. Hệ thống hiển thị danh sách khóa đào tạo, bao gồm các thông tin:   * Tên khóa đào tạo * Loại khóa đào tạo * Thời gian đào tạo (từ ngày – đến ngày) * Đơn vị/địa điểm tổ chức * Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành) * Trạng thái tham gia của cá nhân (Đã đăng ký, Đang học, Hoàn thành, Không đạt) |
| Luồng sự kiện thay thế (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có |

# VI. CÁC YÊU CẦU BỔ SUNG

## 6.1. Yêu cầu về chức năng (Functionality)

Người thực hiện: Nguyễn Hồng Phúc

### 6.1.1. Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
| --- | --- | --- | --- | --- |
| 1 | SUPL-F01 | Ghi nhật ký hệ thống tự động (Auto Logging) | Correctness – Auditability | FEAT 6.1 |
| 2 | SUPL-F02 | Tự động sinh mã nhân sự | Correctness | FEAT 8.3 |
| 3 | SUPL-F03 | Tự động đăng xuất phiên không hoạt động | Correctness – Tự động hóa | FEAT 1.3 |
| 4 | SUPL-F04 | Tự động khóa tài khoản nhân sự thôi việc | Correctness – Tự động hóa | FEAT 2.6; FEAT 8.5; FEAT 8.6 |
| 5 | SUPL-F05 | Tự động chuyển trạng thái hợp đồng | Correctness – Tự động hóa | FEAT 7.1; FEAT 7.2; FEAT 7.3; FEAT 7.4; FEAT 8.6 |
| 6 | SUPL-F06 | Tự động cập nhật trạng thái tham gia đào tạo | Correctness – Tự động hóa | FEAT 11.2 |
| 7 | SUPL-F07 | Quy tắc nghiệp vụ chung về xóa/thay đổi trạng thái | Integrity | FEAT 4.4; FEAT 4.5 |
| 8 | SUPL-F08 | Bảo vệ mật khẩu lưu trữ | Security – Confidentiality | FEAT 1.1 |

### 6.1.2. Chi tiết độ đo và tiêu chuẩn đáp ứng

#### 6.1.2.1. SUPL-F01: Ghi nhật ký hệ thống tự động (Auto Logging)

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness – Auditability (Tính đúng đắn và khả năng kiểm toán) |
| **Mô tả yêu cầu** | Hệ thống tự động ghi lại mọi hành động truy cập, thêm/sửa/xóa dữ liệu và thay đổi cấu hình với đầy đủ các thông tin: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. |
| **Độ đo yêu cầu** | (1) Tỷ lệ hành động truy cập/CRUD/thay đổi cấu hình được ghi log;  (2) Mức đầy đủ trường dữ liệu trên mỗi bản ghi log (9/9 trường bắt buộc). |
| **Tiêu chuẩn đáp ứng** | (1) 100% hành động thuộc phạm vi yêu cầu phải có bản ghi log;  (2) 100% bản ghi log có đủ 9/9 trường bắt buộc. |
| **Lý do chọn độ đo** | Ghi log kiểm toán là yêu cầu kiểu “đạt hoặc không đạt”, nên ngưỡng 100% là bắt buộc; nếu thiếu 1 hành động hoặc thiếu 1 trường thì chuỗi truy vết bị đứt. Bộ 9 trường được chọn từ yêu cầu nguồn và tương thích với khuyến nghị OWASP Logging về tối thiểu phải ghi được when/who/what/where để phục vụ hậu kiểm trong hệ thống HRMS có dữ liệu nhân sự nhạy cảm. |
| **Phương pháp đo** | Thực hiện kiểm thử trên các luồng đăng nhập, truy cập, thêm/sửa/xóa và thay đổi cấu hình; đối chiếu số hành động phát sinh với bảng audit log và kiểm tra cấu trúc từng bản ghi. |

#### 6.1.2.2. SUPL-F02: Tự động sinh mã nhân sự

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn) |
| **Mô tả yêu cầu** | Khi tạo mới hồ sơ nhân sự, hệ thống tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. |
| **Độ đo yêu cầu** | (1) Tỷ lệ mã nhân sự sinh tự động bị trùng lặp;  (2) Tỷ lệ mã sinh ra tuân thủ đúng mẫu mã đang cấu hình;  (3) Tỷ lệ hồ sơ mới được cấp mã ngay tại thời điểm tạo. |
| **Tiêu chuẩn đáp ứng** | (1) 0% mã nhân sự bị trùng lặp;  (2) 100% mã sinh ra đúng mẫu mã đang áp dụng;  (3) 100% hồ sơ nhân sự mới được cấp mã ngay khi tạo thành công. |
| **Phương pháp đo** | Tạo thử nhiều hồ sơ nhân sự mới với các cấu hình mẫu mã khác nhau, kiểm tra tính duy nhất của mã trong cơ sở dữ liệu và đối chiếu chuỗi mã với mẫu cấu hình hiện hành. |

#### 6.1.2.3. SUPL-F03: Tự động đăng xuất phiên không hoạt động

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Hệ thống tự động đăng xuất phiên làm việc nếu người dùng không thao tác trong 30 phút. Tham chiếu FEAT 1.3. |
| **Độ đo yêu cầu** | Thời gian từ thao tác cuối cùng của người dùng đến khi hệ thống tự động đăng xuất phiên. |
| **Tiêu chuẩn đáp ứng** | Hệ thống tự động đăng xuất chính xác sau 30 phút không hoạt động, sai số cho phép không quá ±30 giây. |
| **Phương pháp đo** | Tạo phiên đăng nhập thử nghiệm, ghi nhận thời điểm thao tác cuối cùng, để phiên ở trạng thái không tương tác và đo thời điểm hệ thống hủy phiên/chuyển về màn hình đăng nhập. |

#### 6.1.2.4. SUPL-F04: Tự động khóa tài khoản nhân sự thôi việc

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Khi nhân sự được đánh dấu thôi việc, hệ thống tự động chuyển tài khoản của nhân sự đó sang trạng thái khóa. Cơ chế này gắn với FEAT 2.6 và phát sinh từ các nghiệp vụ thôi việc tương ứng FEAT 8.5, FEAT 8.6. |
| **Độ đo yêu cầu** | (1) Thời gian từ lúc hồ sơ nhân sự chuyển sang trạng thái thôi việc đến khi tài khoản liên kết bị khóa;  (2) Tỷ lệ tài khoản liên kết được khóa tự động đúng quy tắc. |
| **Tiêu chuẩn đáp ứng** | (1) Tài khoản bị khóa trong không quá 1 phút kể từ khi nhân sự được đánh dấu thôi việc;  (2) 100% tài khoản liên kết với nhân sự thôi việc được tự động chuyển sang trạng thái khóa. |
| **Phương pháp đo** | Thực hiện thao tác đánh dấu thôi việc trên hồ sơ nhân sự có tài khoản liên kết, đo độ trễ cập nhật trạng thái tài khoản và kiểm tra kết quả trong bảng tài khoản/audit log. |

#### 6.1.2.5. SUPL-F05: Tự động chuyển trạng thái hợp đồng

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Hệ thống tự động chuyển trạng thái hợp đồng từ “Còn hiệu lực” sang “Chờ gia hạn” khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. |
| **Độ đo yêu cầu** | (1) Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái “Chờ gia hạn”;  (2) Độ trễ chuyển trạng thái kể từ thời điểm hợp đồng chạm ngưỡng cấu hình. |
| **Tiêu chuẩn đáp ứng** | (1) 100% hợp đồng đủ điều kiện được chuyển đúng trạng thái;  (2) Việc chuyển trạng thái hoàn tất trong không quá 24 giờ kể từ thời điểm đủ điều kiện. |
| **Phương pháp đo** | Cấu hình ngưỡng chờ gia hạn, tạo dữ liệu hợp đồng mẫu với các mốc thời gian khác nhau, chạy cơ chế nền/scheduler và đối chiếu thời điểm đủ điều kiện với thời điểm trạng thái được cập nhật. |

#### 6.1.2.6. SUPL-F06: Tự động cập nhật trạng thái tham gia đào tạo

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Khi khóa đào tạo chuyển từ trạng thái “Đang mở đăng ký” sang trạng thái “Đang đào tạo”, hệ thống tự động cập nhật tất cả đăng ký tương ứng từ trạng thái “Đã đăng ký” sang “Đang học”. |
| **Độ đo yêu cầu** | (1) Tỷ lệ bản ghi đăng ký của khóa đào tạo được cập nhật đúng trạng thái;  (2) Độ trễ cập nhật kể từ thời điểm khóa đào tạo đổi trạng thái. |
| **Tiêu chuẩn đáp ứng** | (1) 100% bản ghi đăng ký thuộc khóa đào tạo đó được chuyển từ “Đã đăng ký” sang “Đang học”;  (2) Hoàn tất cập nhật trong không quá 1 phút kể từ khi khóa đào tạo chuyển sang “Đang đào tạo”. |
| **Phương pháp đo** | Tạo khóa đào tạo mẫu với nhiều đăng ký ở trạng thái “Đã đăng ký”, chuyển trạng thái khóa đào tạo và đối chiếu trạng thái của toàn bộ bản ghi đăng ký sau khi hệ thống xử lý. |

#### 6.1.2.7. SUPL-F07: Quy tắc nghiệp vụ chung về thay đổi trạng thái

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Integrity (Tính toàn vẹn dữ liệu) |
| **Mô tả yêu cầu** | Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ thao tác thay đổi trạng thái theo quy tắc nghiệp vụ để bảo đảm tính toàn vẹn dữ liệu và phục vụ kiểm toán. |
| **Độ đo yêu cầu** | (1) Tỷ lệ thao tác thay đổi trạng thái của danh mục loại phụ cấp/loại hợp đồng tuân thủ đúng quy tắc nghiệp vụ;  (2) Số trường hợp thay đổi trạng thái làm sai lệch hoặc mất liên kết dữ liệu lịch sử. |
| **Tiêu chuẩn đáp ứng** | (1) 100% thao tác thay đổi trạng thái của loại phụ cấp và loại hợp đồng tuân thủ đúng quy tắc nghiệp vụ;  (2) 0 trường hợp thay đổi trạng thái làm sai lệch hoặc mất liên kết dữ liệu lịch sử. |
| **Phương pháp đo** | Chuẩn bị các bản ghi danh mục ở nhiều trạng thái nghiệp vụ, thực hiện kiểm thử dương và âm đối với thao tác thay đổi trạng thái, sau đó đối chiếu dữ liệu lưu vết và liên kết tham chiếu trong cơ sở dữ liệu. |

#### 6.1.2.8. SUPL-F08: Bảo vệ mật khẩu lưu trữ

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Security – Confidentiality (Bảo mật dữ liệu lưu trữ) |
| **Mô tả yêu cầu** | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. |
| **Độ đo yêu cầu** | (1) Mức tuân thủ cơ chế băm một chiều thích ứng đối với mật khẩu;  (2) Tham số độ khó của cơ chế băm;  (3) Số mật khẩu tồn tại ở dạng văn bản thuần trong dữ liệu lưu trữ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% mật khẩu được lưu dưới dạng băm một chiều thích ứng;  (2) Tham số độ khó tối thiểu tương đương bcrypt cost 10;  (3) 0 mật khẩu lưu ở dạng plaintext. |
| **Phương pháp đo** | Kiểm tra cấu hình bảo mật và mã nguồn xử lý đăng nhập/đổi mật khẩu, đối chiếu định dạng dữ liệu trong cột mật khẩu của cơ sở dữ liệu và thực hiện audit mẫu trên dữ liệu lưu trữ. |

## 6.2. Ràng buộc thiết kế (Design Constraints)

Người thực hiện: Nguyễn Hồng Phúc

### 6.2.1. Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
| --- | --- | --- | --- | --- |
| 2 | SUPL-DC02 | Cơ cấu tổ chức dạng cây | Correctness – Mô hình dữ liệu | FEAT 3.1 |
| 3 | SUPL-DC03 | Tách biệt quyền theo vai trò | Security – Thiết kế phân quyền | FEAT 2.4 |

### 6.2.2. Chi tiết độ đo và tiêu chuẩn đáp ứng

#### 6.2.2.2. SUPL-DC02: Cơ cấu tổ chức dạng cây

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness – Mô hình dữ liệu |
| **Mô tả yêu cầu** | Cơ cấu tổ chức đơn vị phải được mô hình hóa dưới dạng cấu trúc cây cha-con với gốc là Trường Đại học Thủy Lợi. Tham chiếu FEAT 3.1. |
| **Độ đo yêu cầu** | (1) Số nút gốc trong cây tổ chức;  (2) Số chu trình (cycle) phát hiện trong quan hệ cha-con;  (3) Tỷ lệ đơn vị có liên kết cha-con hợp lệ trong mô hình dữ liệu. |
| **Tiêu chuẩn đáp ứng** | (1) Có đúng 1 nút gốc là “Trường Đại học Thủy Lợi”;  (2) 0 chu trình trong cấu trúc cây;  (3) 100% đơn vị tổ chức nằm trong quan hệ cha-con hợp lệ. |
| **Phương pháp đo** | Kiểm tra mô hình dữ liệu và thực hiện truy vấn/thuật toán duyệt cây để xác minh số nút gốc, phát hiện cycle và kiểm tra tính hợp lệ của toàn bộ quan hệ đơn vị. |

#### 6.2.2.3. SUPL-DC03: Tách biệt quyền theo vai trò

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Security – Thiết kế phân quyền |
| **Mô tả yêu cầu** | Thiết kế hệ thống phải bảo đảm phân tách quyền rõ ràng theo 4 vai trò đã xác định, sử dụng cơ chế Role-Based Access Control (RBAC). |
| **Độ đo yêu cầu** | (1) Số vai trò được định nghĩa trong mô hình phân quyền;  (2) Tỷ lệ chức năng/API có ma trận phân quyền rõ ràng;  (3) Số trường hợp vai trò không được phép vẫn truy cập được chức năng khi kiểm thử phân quyền. |
| **Tiêu chuẩn đáp ứng** | (1) Định nghĩa đúng 4 vai trò: Admin, TCCB, TCKT, Nhân sự;  (2) 100% chức năng và API có ma trận RBAC rõ ràng;  (3) 0 trường hợp truy cập trái quyền trong kiểm thử phân quyền. |
| **Phương pháp đo** | Đối chiếu tài liệu phân quyền với danh sách chức năng/API của hệ thống, kiểm tra cấu hình role-permission và thực hiện kiểm thử truy cập chéo giữa các vai trò. |

## 6.3. Ràng buộc pháp lý (Legal/Regulatory)

Người thực hiện: Nguyễn Hồng Phúc

### 6.3.1. Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
| --- | --- | --- | --- | --- |
| 1 | SUPL-LR01 | Tuân thủ quy định bảo vệ dữ liệu cá nhân | Legal – Bảo vệ dữ liệu | FEAT 8.3; FEAT 8.4; FEAT 8.7; FEAT 12.1 |
| 2 | SUPL-LR02 | Tuân thủ quy chế quản lý nhân sự | Legal – Quy chế nhân sự | FEAT 4.4; FEAT 4.5; FEAT 7.1 |
| 3 | SUPL-LR03 | Lưu trữ hồ sơ theo quy định | Legal – Lưu trữ | FEAT 7.1; FEAT 8.3; FEAT 10.1 |

### 6.3.2. Chi tiết độ đo và tiêu chuẩn đáp ứng

#### 6.3.2.1. SUPL-LR01: Tuân thủ quy định bảo vệ dữ liệu cá nhân

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Legal – Bảo vệ dữ liệu |
| **Mô tả yêu cầu** | Hệ thống phải hỗ trợ quản lý sự đồng ý thu thập dữ liệu cá nhân và xử lý yêu cầu hợp lệ về ẩn dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP. |
| **Độ đo yêu cầu** | (1) Tỷ lệ trường hợp xử lý dữ liệu cá nhân thuộc diện phải xin đồng ý có bản ghi đồng ý hợp lệ trước khi xử lý; (2) Tỷ lệ yêu cầu hợp lệ về ẩn dữ liệu cá nhân được xử lý và lưu vết đầy đủ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% trường hợp thuộc diện phải xin đồng ý có bản ghi đồng ý hợp lệ trước khi xử lý dữ liệu;  (2) 100% yêu cầu hợp lệ về ẩn dữ liệu cá nhân được thực hiện và có lưu vết xử lý. |
| **Phương pháp đo** | Kiểm tra hồ sơ đồng ý của chủ thể dữ liệu, đối chiếu nhật ký xử lý yêu cầu ẩn dữ liệu với các yêu cầu hợp lệ và rà soát mẫu dữ liệu cá nhân trước/sau xử lý. |

#### 6.3.2.2. SUPL-LR02: Tuân thủ quy chế quản lý nhân sự

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Legal – Quy chế nhân sự |
| **Mô tả yêu cầu** | Hệ thống phải cho phép cấu hình và sử dụng bộ danh mục loại hợp đồng, phụ cấp và chức danh theo danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt trên cơ sở quy định hiện hành của Bộ GD&ĐT và Bộ NN&PTNT. |
| **Độ đo yêu cầu** | (1) Tỷ lệ mục trong bộ danh mục nhân sự đã được phê duyệt có thể cấu hình và sử dụng trên hệ thống;  (2) Số mục trái danh mục phê duyệt xuất hiện trong phạm vi nghiệm thu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% loại hợp đồng, phụ cấp và chức danh trong bộ danh mục phê duyệt được cấu hình và sử dụng được trên hệ thống; (2) 0 mục trái bộ danh mục phê duyệt được đưa vào nghiệm thu. |
| **Phương pháp đo** | Đối chiếu danh mục được phê duyệt của nhà trường với danh mục cấu hình trên hệ thống, thực hiện kiểm thử chọn/sử dụng các giá trị này trong các nghiệp vụ nhân sự liên quan. |

#### 6.3.2.3. SUPL-LR03: Lưu trữ hồ sơ theo quy định

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Legal – Lưu trữ |
| **Mô tả yêu cầu** | Hồ sơ nhân sự, hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu theo thời gian quy định của pháp luật lao động Việt Nam và quy chế lưu trữ hiện hành. |
| **Độ đo yêu cầu** | (1) Thời gian lưu trữ tối thiểu đối với từng nhóm hồ sơ;  (2) Tỷ lệ hồ sơ mẫu còn truy xuất được trong toàn bộ thời hạn lưu trữ bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) Hồ sơ nhân sự được lưu tối thiểu 75 năm; hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật được lưu tối thiểu 10 năm sau khi kết thúc hoặc sau bản ghi cuối cùng;  (2) 100% hồ sơ mẫu trong thời hạn lưu trữ bắt buộc còn truy xuất được. |
| **Phương pháp đo** | Kiểm tra chính sách lưu trữ, cấu hình lưu trữ/archiving và thử truy xuất hồ sơ mẫu của từng nhóm tài liệu để xác nhận hệ thống không xóa hoặc làm mất dữ liệu trước hạn. |

## 6.4. Yêu cầu về Khả dụng (Usability)

Người thực hiện: Nguyễn Hải Ninh

### 6.4.1. Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
| --- | --- | --- | --- | --- |
| 1 | SUPL-U01 | Giao diện tiếng Việt và nhất quán | Usability – Tính nhất quán giao diện (Consistency) | Toàn bộ FEAT/UC |
| 2 | SUPL-U02 | Dễ học cho người dùng mới | Usability – Dễ học (Learnability) | Toàn bộ FEAT/UC |
| 3 | SUPL-U03 | Thông báo lỗi rõ ràng | Usability – Xử lý lỗi (Error Handling) | Toàn bộ FEAT/UC |
| 4 | SUPL-U04 | Hỗ trợ tìm kiếm và lọc đa tiêu chí | Usability – Hiệu quả thao tác (Efficiency) | Toàn bộ FEAT/UC |
| 5 | SUPL-U05 | Hiển thị ổn định trên desktop và tablet | Usability – Khả năng truy cập đa thiết bị (Accessibility) | Toàn bộ FEAT/UC |
| 6 | SUPL-U06 | Điều hướng nhanh bằng bàn phím và breadcrumb | Usability – Hiệu quả thao tác (Efficiency) | Toàn bộ FEAT/UC |
| 7 | SUPL-U07 | Xác nhận trước thao tác quan trọng | Usability – Ngăn ngừa lỗi (Error Prevention) | Toàn bộ FEAT/UC |

### 6.4.2. Chi tiết độ đo và tiêu chuẩn đáp ứng

#### 6.4.2.1. SUPL-U01: Giao diện tiếng Việt và nhất quán

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Usability – Tính nhất quán giao diện (Consistency) |
| **Mô tả yêu cầu** | 100% màn hình phải sử dụng Tiếng Việt, trừ thuật ngữ kỹ thuật; đồng thời bố cục, màu sắc và font chữ phải được áp dụng thống nhất trên toàn bộ hệ thống. |
| **Độ đo yêu cầu** | (1) Tỷ lệ nhãn, menu, thông báo và nút thao tác trên các màn hình nghiệp vụ chính sử dụng Tiếng Việt;  (2) Tỷ lệ màn hình nghiệp vụ chính đạt checklist design system về bố cục, màu sắc, font chữ và cách đặt tên;  (3) Số vi phạm nghiêm trọng làm người dùng hiểu sai chức năng. |
| **Tiêu chuẩn đáp ứng** | (1) 100% nhãn, menu, thông báo và nút thao tác trên các màn hình nghiệp vụ chính dùng Tiếng Việt, trừ thuật ngữ kỹ thuật thống nhất;  (2) ≥ 95% màn hình nghiệp vụ chính đạt checklist design system;  (3) 0 vi phạm nghiêm trọng. |
| **Phương pháp đo** | Rà soát toàn bộ màn hình nghiệp vụ chính theo checklist UI/UX; đối chiếu ngôn ngữ hiển thị và bộ quy chuẩn giao diện trước nghiệm thu. |
| **Lý do chọn độ đo** | Theo heuristic **Consistency and Standards** và **Match Between the System and the Real World** của Nielsen Norman Group, giao diện phải dùng ngôn ngữ quen thuộc và nhất quán để giảm tải nhận thức. Với HRMS của trường đại học, người dùng chủ yếu là cán bộ hành chính nên ngưỡng **100% cho nhãn/menu/thông báo ở màn hình chính** là cần thiết; còn ngưỡng **≥ 95% tuân thủ design system** thực tế hơn so với ép 100% toàn bộ màn hình vì vẫn có thể tồn tại vài thành phần kỹ thuật hoặc thư viện dùng thuật ngữ gốc. |
| **Đại lượng thay thế (nếu cần)** | Số component sử dụng hardcoded style ngoài design token hoặc ngoài thư viện giao diện chuẩn của hệ thống. |

#### 6.4.2.2. SUPL-U02: Dễ học cho người dùng mới

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Usability – Dễ học (Learnability) |
| **Mô tả yêu cầu** | Sau tối đa 2 giờ đào tạo hướng dẫn, ít nhất 95% người dùng mới thuộc phòng TCCB phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự; ít nhất 95% người dùng mới thuộc phòng TCKT phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. |
| **Độ đo yêu cầu** | (1) Thời gian đào tạo trung bình cho người dùng mới;  (2) Tỷ lệ người dùng mới phòng TCCB hoàn thành bộ tác vụ tìm kiếm – xem chi tiết – cập nhật hồ sơ nhân sự mà không cần trợ giúp trực tiếp;  (3) Tỷ lệ người dùng mới phòng TCKT hoàn thành bộ tác vụ tìm kiếm – xem chi tiết – xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. |
| **Tiêu chuẩn đáp ứng** | (1) Thời gian đào tạo ≤ 2 giờ/người;  (2) Tỷ lệ hoàn thành của nhóm TCCB ≥ 95%;  (3) Tỷ lệ hoàn thành của nhóm TCKT ≥ 95%. |
| **Phương pháp đo** | Tổ chức usability test với người dùng mới đại diện cho hai phòng ban sau buổi hướng dẫn chuẩn; ghi nhận thời gian đào tạo, tỷ lệ hoàn thành tác vụ và số lần cần trợ giúp trực tiếp. |
| **Lý do chọn độ đo** | NN/g nêu rằng **learnability** nên đo bằng **time on task** và **task completion rate**. Trong bối cảnh trường đại học, đào tạo người dùng thường chỉ bố trí được trong một buổi ngắn; vì vậy ngưỡng **≤ 2 giờ** tương ứng một buổi hướng dẫn cơ bản là phù hợp triển khai. Mức **≥ 95%** bảo đảm đa số tuyệt đối người dùng mới có thể làm việc độc lập ngay sau tập huấn, nhưng vẫn chừa sai số nhỏ cho khác biệt về kỹ năng cá nhân. |
| **Đại lượng thay thế (nếu cần)** | Khối lượng tài liệu/hướng dẫn đào tạo cho mỗi vai trò không vượt quá 30 trang để tránh tăng gánh nặng học sử dụng. |

#### 6.4.2.3. SUPL-U03: Thông báo lỗi rõ ràng

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Usability – Xử lý lỗi (Error Handling) |
| **Mô tả yêu cầu** | Mọi lỗi nhập liệu hoặc lỗi hệ thống phải hiển thị thông báo bằng Tiếng Việt, rõ ràng, mô tả nguyên nhân và hướng dẫn khắc phục. |
| **Độ đo yêu cầu** | (1) Tỷ lệ lỗi validation và lỗi nghiệp vụ có thông báo bằng Tiếng Việt rõ ràng;  (2) Tỷ lệ thông báo lỗi có nêu nguyên nhân;  (3) Tỷ lệ thông báo lỗi validation/nghiệp vụ có ít nhất 1 gợi ý khắc phục;  (4) Tỷ lệ lỗi hệ thống hiển thị thông báo thân thiện kèm mã tra cứu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% lỗi validation và lỗi nghiệp vụ có thông báo bằng Tiếng Việt;  (2) 100% thông báo lỗi nêu được nguyên nhân chính;  (3) ≥ 95% thông báo lỗi validation/nghiệp vụ có ít nhất 1 gợi ý khắc phục;  (4) 100% lỗi hệ thống hiển thị thông báo thân thiện và có mã tra cứu/log reference. |
| **Phương pháp đo** | Lập danh mục các lỗi điển hình theo từng nhóm, kích hoạt lỗi trên môi trường kiểm thử và đối chiếu nội dung thông báo với checklist: đúng tiếng Việt, có nguyên nhân, có hướng dẫn xử lý hoặc mã tra cứu. |
| **Lý do chọn độ đo** | Theo heuristic **Help Users Recognize, Diagnose, and Recover from Errors** của Nielsen và bài **Error-Message Guidelines**, lỗi tốt phải dùng ngôn ngữ dễ hiểu, chỉ rõ vấn đề và gợi ý cách xử lý. Vì lỗi validation/nghiệp vụ là các tình huống dự đoán được nên đặt ngưỡng **100%** là hợp lý; riêng gợi ý khắc phục dùng **≥ 95%** để tránh quá cứng với một số lỗi biên hiếm gặp. Với lỗi hệ thống, người dùng cuối không cần stack trace mà cần thông báo thân thiện và mã tra cứu để bộ phận kỹ thuật xử lý nhanh. |
| **Đại lượng thay thế (nếu cần)** | Số thông báo lỗi hiển thị bằng tiếng Anh hoặc chỉ hiển thị mã kỹ thuật = 0. |

#### 6.4.2.4. SUPL-U04: Hỗ trợ tìm kiếm và lọc đa tiêu chí

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Các danh sách dữ liệu (nhân sự, hợp đồng, đơn vị) phải hỗ trợ tìm kiếm theo từ khóa và lọc đa tiêu chí để giảm thời gian thao tác. |
| **Độ đo yêu cầu** | (1) Số bước thao tác để tìm kiếm và mở chi tiết 1 hồ sơ nhân sự;  (2) Số tiêu chí lọc có thể kết hợp đồng thời trên một danh sách dữ liệu chính. |
| **Tiêu chuẩn đáp ứng** | (1) Tìm kiếm và mở chi tiết 1 hồ sơ nhân sự trong ≤ 3 bước (nhập từ khóa → tìm kiếm → mở chi tiết);  (2) Bộ lọc hỗ trợ kết hợp ≥ 3 tiêu chí đồng thời trên các danh sách dữ liệu chính. |
| **Phương pháp đo** | Thực hiện walkthrough trên các màn hình danh sách chính, đếm số thao tác thực tế và kiểm tra khả năng kết hợp đồng thời các tiêu chí lọc trên cùng một truy vấn. |
| **Lý do chọn độ đo** | Theo heuristic **Recognition Rather than Recall** và **Flexibility and Efficiency of Use** của NN/g, người dùng nên nhìn thấy ngay công cụ tìm kiếm/lọc thay vì phải nhớ nhiều đường đi thao tác. Với HRMS nội bộ, cán bộ thường tra cứu nhanh hồ sơ theo vài thuộc tính như mã, đơn vị, trạng thái; vì vậy ngưỡng **≤ 3 bước** phản ánh luồng tra cứu tối giản, còn **≥ 3 tiêu chí lọc đồng thời** là đủ cho phần lớn truy vấn nghiệp vụ mà không làm giao diện quá phức tạp. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể đo trực tiếp qua thao tác người dùng trên giao diện. |

#### 6.4.2.5. SUPL-U05: Hiển thị ổn định trên desktop và tablet

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Usability – Khả năng truy cập đa thiết bị (Accessibility) |
| **Mô tả yêu cầu** | Ở độ phân giải desktop từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang; trên tablet 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện các thao tác chính mà không cần phóng to. |
| **Độ đo yêu cầu** | (1) Tỷ lệ màn hình nghiệp vụ chính hiển thị đúng ở độ phân giải desktop ≥ 1366×768;  (2) Tỷ lệ màn hình nghiệp vụ chính sử dụng được trên tablet 1024×768;  (3) Tỷ lệ tác vụ cốt lõi thực hiện được trên tablet 1024×768 mà không cần phóng to hoặc cuộn ngang. |
| **Tiêu chuẩn đáp ứng** | (1) 100% màn hình nghiệp vụ chính đạt tiêu chí ở desktop ≥ 1366×768;  (2) ≥ 90% màn hình nghiệp vụ chính dùng được ở tablet 1024×768;  (3) 100% tác vụ cốt lõi trên tablet 1024×768 không cần phóng to hoặc cuộn ngang. |
| **Phương pháp đo** | Kiểm thử giao diện trên trình duyệt desktop chuẩn và thiết bị giả lập/tablet 1024×768; ghi nhận các lỗi cắt nội dung, chồng lấn thành phần, cuộn ngang và thao tác cần phóng to. |
| **Lý do chọn độ đo** | Hệ thống HRMS của trường chủ yếu được dùng trên desktop tại phòng ban, nên ngưỡng **100% cho desktop 1366×768** là bắt buộc vì đây là mức phân giải văn phòng phổ biến. Tablet chỉ là kênh hỗ trợ cho tra cứu hoặc phê duyệt nhanh, nên đặt **≥ 90% màn hình chính** và **100% tác vụ cốt lõi** là hợp lý hơn việc yêu cầu 100% trên mọi màn hình phụ; cách này vẫn bảo đảm khả năng dùng thực tế mà phù hợp định hướng desktop-first của hệ thống nội bộ. |
| **Đại lượng thay thế (nếu cần)** | Hệ thống giao diện có tối thiểu 2 breakpoint rõ ràng cho desktop và tablet để hỗ trợ responsive layout. |

#### 6.4.2.6. SUPL-U06: Điều hướng nhanh bằng bàn phím và breadcrumb

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập; trên 100% form có nút xác nhận mặc định, phím Enter phải kích hoạt nút đó; 100% trang phải hiển thị breadcrumb để người dùng quay lại cấp điều hướng trước. |
| **Độ đo yêu cầu** | (1) Tỷ lệ form nhập liệu chính hỗ trợ Tab navigation đúng thứ tự;  (2) Tỷ lệ form có nút xác nhận mặc định hỗ trợ phím Enter;  (3) Tỷ lệ trang có cấu trúc phân cấp danh sách → chi tiết → chỉnh sửa hiển thị breadcrumb hợp lệ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% form nhập liệu chính cho phép di chuyển bằng phím Tab theo đúng thứ tự trường nhập;  (2) 100% form có nút xác nhận mặc định hỗ trợ phím Enter;  (3) 100% trang có cấu trúc phân cấp danh sách → chi tiết → chỉnh sửa hiển thị breadcrumb hợp lệ. |
| **Phương pháp đo** | Thực hiện kiểm thử thủ công bằng bàn phím trên toàn bộ form nhập liệu chính và các trang chức năng có phân cấp điều hướng; ghi nhận thứ tự focus, hành vi của phím Enter và sự hiện diện của breadcrumb. |
| **Lý do chọn độ đo** | WCAG 2.2 **SC 2.1.1 Keyboard** yêu cầu mọi chức năng khả dụng qua bàn phím; với hệ thống nhập liệu nhiều như HRMS, điều này giúp tăng năng suất cho người dùng thường xuyên. Tôi thu hẹp phạm vi thành **form nhập liệu chính** và **trang có cấu trúc phân cấp**, nhờ đó ngưỡng **100%** trở nên khả thi và dễ nghiệm thu hơn so với áp dụng máy móc cho mọi modal hoặc dashboard. Breadcrumb được giữ ở mức 100% cho các trang phân cấp vì nó trực tiếp hỗ trợ định hướng và giảm nhầm lẫn khi người dùng quay lui. |
| **Đại lượng thay thế (nếu cần)** | Tỷ lệ trường nhập liệu có thứ tự focus được xác định rõ ràng trong thiết kế/triển khai = 100% trên các form chính. |

#### 6.4.2.7. SUPL-U07: Xác nhận trước thao tác quan trọng

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Usability – Ngăn ngừa lỗi (Error Prevention) |
| **Mô tả yêu cầu** | Hệ thống hiển thị hộp thoại xác nhận trước các thao tác quan trọng như khóa tài khoản, đánh dấu thôi việc, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương. |
| **Độ đo yêu cầu** | Tỷ lệ thao tác quan trọng có hộp thoại xác nhận trước khi hệ thống thực thi thao tác. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác quan trọng có confirmation dialog; tối thiểu bao gồm: khóa tài khoản, đánh dấu thôi việc, thay đổi trạng thái đơn vị và chấm dứt hợp đồng lao động trước hạn (nếu chức năng được cung cấp trên hệ thống). |
| **Phương pháp đo** | Lập danh sách thao tác quan trọng theo nghiệp vụ, kích hoạt từng thao tác trên môi trường kiểm thử và kiểm tra sự xuất hiện của hộp thoại xác nhận trước khi dữ liệu bị thay đổi. |
| **Lý do chọn độ đo** | Theo heuristic **Error Prevention** của Nielsen và hướng dẫn của NN/g về **confirmation dialog**, xác nhận chỉ nên dùng cho hành động có hậu quả nghiêm trọng và khó hoàn tác. Các thao tác như khóa tài khoản, thôi việc hoặc đổi trạng thái đơn vị đều có rủi ro cao đối với dữ liệu nhân sự, nên ngưỡng **100%** là phù hợp vì đây là yêu cầu kiểu “sharp”: thiếu xác nhận ở một trường hợp cũng có thể gây lỗi nghiệp vụ lớn. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể kiểm thử trực tiếp theo từng thao tác trọng yếu. |

## 6.5. Yêu cầu về Hỗ trợ (Supportability)

Người thực hiện: Nguyễn Hải Ninh

### 6.5.1. Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
| --- | --- | --- | --- | --- |
| 1 | SUPL-S01 | Kiến trúc module hóa | Supportability – Tính bảo trì, tính module hóa (Maintainability/Modularity) | Toàn bộ hệ thống |
| 2 | SUPL-S02 | Tài liệu kỹ thuật đầy đủ | Supportability – Khả năng hiểu và vận hành (Understandability) | Toàn bộ hệ thống |
| 3 | SUPL-S03 | Khả năng mở rộng danh mục cấu hình | Supportability – Tính linh hoạt cấu hình (Flexibility/Configurability) | Toàn bộ hệ thống |
| 4 | SUPL-S04 | Hỗ trợ gỡ lỗi (Debugging) | Supportability – Khả năng chẩn đoán và kiểm thử (Maintainability/Testability) | Toàn bộ hệ thống |
| 5 | SUPL-S05 | Khả năng mở rộng quy mô (Scalability) | Supportability – Khả năng mở rộng quy mô (Scalability) | Toàn bộ hệ thống |

### 6.5.2. Chi tiết độ đo và tiêu chuẩn đáp ứng

#### 6.5.2.1. SUPL-S01: Kiến trúc module hóa

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Supportability – Tính bảo trì, tính module hóa (Maintainability/Modularity) |
| **Mô tả yêu cầu** | Hệ thống phải được tổ chức thành các module chức năng có giao diện tích hợp rõ ràng để có thể nâng cấp hoặc thay thế từng module mà không buộc sửa đổi toàn bộ hệ thống. |
| **Độ đo yêu cầu** | (1) Số module khác cần sửa khi thực hiện một thay đổi nghiệp vụ thông thường trong 1 module;  (2) Tỷ lệ module có interface/service contract được mô tả rõ ràng;  (3) Số phụ thuộc vòng giữa các module nghiệp vụ chính. |
| **Tiêu chuẩn đáp ứng** | (1) Thay đổi nghiệp vụ thông thường trong 1 module không làm phát sinh sửa đổi ở quá 2 module khác;  (2) 100% module nghiệp vụ chính có interface/service contract rõ ràng;  (3) Số phụ thuộc vòng giữa các module nghiệp vụ chính = 0. |
| **Phương pháp đo** | Phân tích dependency giữa các module, rà soát tài liệu interface và thực hiện impact analysis đối với một thay đổi nghiệp vụ điển hình ở từng module chính. |
| **Lý do chọn độ đo** | ISO/IEC 25010 xem **modularity** là một thành phần của maintainability, còn ISO/IEC/IEEE 42010 yêu cầu mô tả kiến trúc đủ rõ để kiểm soát ranh giới module. Tôi dùng ngưỡng **≤ 2 module bị ảnh hưởng** thay cho ≤ 1 vì thực tế hệ thống web thường vẫn có lan truyền sang lớp API hoặc UI; tuy nhiên vượt quá 2 module cho một thay đổi thông thường cho thấy coupling bắt đầu cao. Điều kiện **0 phụ thuộc vòng** giúp kiến trúc dễ thay thế, kiểm thử và bảo trì hơn. |
| **Đại lượng thay thế (nếu cần)** | Số dependency cross-module ngoài interface công khai phải ở mức tối thiểu và được kiểm soát qua báo cáo phân tích phụ thuộc. |

#### 6.5.2.2. SUPL-S02: Tài liệu kỹ thuật đầy đủ

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Supportability – Khả năng hiểu và vận hành (Understandability) |
| **Mô tả yêu cầu** | Cung cấp tài liệu API cho backend, hướng dẫn triển khai và hướng dẫn sử dụng cho từng vai trò. |
| **Độ đo yêu cầu** | (1) Tỷ lệ API public hoặc API nội bộ đang được frontend sử dụng có tài liệu mô tả đầy đủ phương thức, URL, tham số, dữ liệu trả về và mã lỗi;  (2) Tỷ lệ vai trò người dùng có hướng dẫn sử dụng riêng cho các chức năng chính; (3) Tỷ lệ tài liệu triển khai có đủ các mục bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 100% API public hoặc API nội bộ đang được frontend sử dụng có tài liệu đầy đủ;  (2) 100% vai trò sử dụng hệ thống có hướng dẫn sử dụng tương ứng;  (3) 100% tài liệu triển khai có tối thiểu các mục: yêu cầu môi trường, cài đặt, cấu hình, khởi động, sao lưu/khôi phục và xử lý lỗi thường gặp. |
| **Phương pháp đo** | Đối chiếu danh mục endpoint thực tế với bộ tài liệu API; rà soát tài liệu theo checklist vai trò và checklist triển khai trước nghiệm thu. |
| **Lý do chọn độ đo** | IEEE **1063-2001** nêu tài liệu người dùng phải có cấu trúc và nội dung tối thiểu, còn ISO/IEC/IEEE **42010** nhấn mạnh việc mô tả kiến trúc và triển khai theo stakeholder concern. Với hệ thống nội bộ, endpoint đang được frontend gọi mà thiếu tài liệu sẽ làm tăng ngay chi phí sửa lỗi và bàn giao, vì vậy chọn **100% cho API đang sử dụng** thay vì 90%. Tương tự, mọi vai trò nghiệp vụ đều cần hướng dẫn riêng để tránh phụ thuộc vào truyền miệng khi vận hành lâu dài. |
| **Đại lượng thay thế (nếu cần)** | Số endpoint chưa được tài liệu hóa và số vai trò chưa có hướng dẫn sử dụng riêng. |

#### 6.5.2.3. SUPL-S03: Khả năng mở rộng danh mục cấu hình

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Supportability – Tính linh hoạt cấu hình (Flexibility/Configurability) |
| **Mô tả yêu cầu** | Hệ thống cho phép mở rộng các danh mục cấu hình (loại phụ cấp, loại hợp đồng, hệ số lương) mà không cần thay đổi mã nguồn. |
| **Độ đo yêu cầu** | (1) Số loại danh mục cấu hình có thể mở rộng qua giao diện quản trị;  (2) Số dòng mã nguồn phải sửa khi thêm một danh mục mới;  (3) Có/không yêu cầu deploy lại hệ thống sau khi thêm mới giá trị cấu hình. |
| **Tiêu chuẩn đáp ứng** | (1) Có ít nhất 3 loại danh mục master data mở rộng được qua giao diện quản trị: hệ số lương, loại phụ cấp, loại hợp đồng;  (2) Số dòng mã nguồn cần sửa khi thêm danh mục mới = 0;  (3) Không cần deploy lại hệ thống khi thêm mới giá trị cấu hình. |
| **Phương pháp đo** | Thực hiện thử nghiệm thêm mới/sửa danh mục cấu hình trên giao diện quản trị và kiểm tra thay đổi mã nguồn, quy trình build/deploy trong suốt quá trình cấu hình. |
| **Lý do chọn độ đo** | Theo nguyên tắc **Config** của **The Twelve-Factor App**, các thông số thay đổi theo môi trường hoặc chính sách không nên bị hard-code trong chương trình. Với HRMS của trường đại học, ba nhóm danh mục này là những danh mục biến động trực tiếp theo quy định nội bộ và quy định nhà nước, nên chọn **≥ 3 danh mục** là sát nhu cầu thực tế. Điều kiện **0 sửa code** và **không cần deploy lại** bảo đảm hệ thống thực sự linh hoạt chứ không chỉ “cấu hình được” trên lý thuyết. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể kiểm chứng trực tiếp qua thao tác cấu hình trên hệ thống. |

#### 6.5.2.4. SUPL-S04: Hỗ trợ gỡ lỗi (Debugging)

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Supportability – Khả năng chẩn đoán và kiểm thử (Maintainability/Testability) |
| **Mô tả yêu cầu** | Hệ thống ghi log lỗi phía server theo nhiều cấp độ (ERROR, WARNING, INFO, DEBUG). Log phải bao gồm timestamp, request ID, stack trace. |
| **Độ đo yêu cầu** | (1) Số cấp độ log được hệ thống hỗ trợ; (2) Tỷ lệ log mức ERROR có đủ timestamp, severity, request ID và stack trace;  (3) Tỷ lệ log lỗi/nghiệp vụ phát sinh trong phiên xác thực có gắn user ID hoặc actor ID. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 4 cấp độ log: ERROR, WARNING, INFO, DEBUG;  2) 100% log mức ERROR có đủ timestamp, severity, request ID và stack trace;  (3) ≥ 95% log lỗi/nghiệp vụ phát sinh trong phiên xác thực có user ID hoặc actor ID. |
| **Phương pháp đo** | Kích hoạt các tình huống lỗi điển hình trên môi trường kiểm thử, trích xuất log server và đối chiếu từng bản ghi với checklist trường thông tin bắt buộc và cấp độ log. |
| **Lý do chọn độ đo** | **OWASP Logging Cheat Sheet** khuyến nghị log phải trả lời được các câu hỏi **when, where, who, what**; **RFC 5424** cũng chuẩn hóa severity level cho log. Vì vậy chỉ đếm số level là chưa đủ, nên tôi bổ sung yêu cầu về **severity, request ID, user ID** để phục vụ truy vết thật sự. Ngưỡng **100% cho log ERROR** là hợp lý vì mọi lỗi server đều phải chẩn đoán được; còn **≥ 95% với user ID** thực tế hơn trong các trường hợp ngoại lệ xảy ra trước khi phiên xác thực hoàn chỉnh. |
| **Đại lượng thay thế (nếu cần)** | Số log ERROR thiếu một trong các trường bắt buộc (timestamp, severity, request ID, stack trace) phải bằng 0. |

#### 6.5.2.5. SUPL-S05: Khả năng mở rộng quy mô (Scalability)

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Supportability – Khả năng mở rộng quy mô (Scalability) |
| **Mô tả yêu cầu** | Hệ thống phải duy trì đầy đủ chức năng khi năng lực xử lý được mở rộng bằng cách bổ sung thêm nút ứng dụng trong cùng một môi trường khai thác. |
| **Độ đo yêu cầu** | (1) Số nút ứng dụng có thể vận hành song song trong cùng môi trường;  (2) Tỷ lệ phiên người dùng tiếp tục hoạt động đúng khi request liên tiếp được phân phối qua các nút khác nhau trong bài kiểm thử scale-out 30 phút;  (3) Tỷ lệ ca smoke test chức năng chính vẫn đạt sau khi bổ sung nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 2 nút ứng dụng chạy song song trong cùng môi trường;  (2) 100% phiên người dùng trong bài kiểm thử 30 phút vẫn hoạt động đúng khi request liên tiếp đi qua các nút khác nhau; (3) 100% ca smoke test của các chức năng chính vẫn đạt sau khi bổ sung nút ứng dụng. |
| **Phương pháp đo** | Triển khai thử nghiệm cấu hình nhiều nút ứng dụng sau load balancer, chạy kiểm thử phiên liên tiếp trong 30 phút và thực hiện bộ smoke test/regression cho các chức năng chính của hệ thống. |
| **Lý do chọn độ đo** | **The Twelve-Factor App** (mục **Processes** và **Concurrency**) xem scale ngang là mở rộng bằng cách bổ sung process/instance thay vì chỉ tăng tài nguyên cho một nút. Với HRMS cấp trường, tải đồng thời thường không lớn như hệ thống công cộng, nên ngưỡng **tối thiểu 2 nút** là đủ để chứng minh hệ thống có thể scale-out và có dự phòng cơ bản. Bài kiểm thử **30 phút** đủ dài để quan sát lỗi phiên, lỗi sticky-session hoặc lỗi chia sẻ trạng thái mà không làm tăng chi phí kiểm thử quá mức. |
| **Đại lượng thay thế (nếu cần)** | Số lỗi phiên làm việc hoặc lỗi điều hướng phát sinh khi request được chuyển giữa các nút ứng dụng phải bằng 0. |

## 6.6. Yêu cầu về Hiệu năng (Performance)

Người thực hiện: Ngô Quang Tùng

### 6.6.1. Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-P01 | Hệ thống phải giữ P95 Response Time của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự trong các ngưỡng quy định theo 3 mức tải đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 2 | SUPL-P01b | Hệ thống phải giữ Time to Interactive (TTI) của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự trong các ngưỡng quy định theo 3 mức tải đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 3 | SUPL-P02 | Hệ thống phải hỗ trợ tối thiểu 100 người dùng đồng thời trong giờ cao điểm mà không làm thời gian phản hồi tăng quá 50% so với tải một người dùng. | FEAT 7.1–8.9 |
| 4 | SUPL-P03a | Hệ thống phải hiển thị chi tiết hồ sơ nhân sự tổng hợp trong tối đa 5 giây ở mức không quá 10 người dùng đồng thời. | FEAT 8.7 |
| 5 | SUPL-P03b | Hệ thống phải chuẩn bị dữ liệu in hồ sơ nhân sự trong tối đa 10 giây ở mức không quá 10 người dùng đồng thời. | FEAT 8.8 |
| 6 | SUPL-P04 | Hệ thống phải trả kết quả tìm kiếm và lọc hồ sơ nhân sự trong tối đa 2 giây với tập dữ liệu không quá 10.000 bản ghi hoặc tối đa 5 giây với tập dữ liệu không quá 50.000 bản ghi, tại mức không quá 50 người dùng đồng thời. | FEAT 8.1, FEAT 8.2 |
| 7 | SUPL-P05 | Hệ thống phải hoàn thành upload/download tệp đính kèm trong tối đa 5/3 giây với file không quá 5 MB hoặc tối đa 10/6 giây với file trên 5 MB đến 10 MB, trên mạng LAN 1 Gbps và ở mức không quá 10 người dùng đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 8 | SUPL-P06 | Hệ thống phải xuất dữ liệu hồ sơ nhân sự ra Excel trong tối đa 10 giây với tập dữ liệu không quá 1.000 bản ghi hoặc tối đa 30 giây với tập dữ liệu không quá 10.000 bản ghi, tại mức không quá 10 người dùng đồng thời. | FEAT 8.8 |
| 9 | SUPL-P07a | Hệ thống phải phục hồi khả năng phục vụ sau sự cố trong tối đa 15 phút. | FEAT 7.1–8.9 |
| 10 | SUPL-P07b | Hệ thống phải khởi động lại toàn bộ stack trong tối đa 10 phút sau sự cố crash hoặc restart có chủ đích. | FEAT 7.1–8.9 |

### 6.6.2. Độ đo và tiêu chuẩn đáp ứng

#### SUPL-P01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | P95 Response Time cho các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự tại 3 mức tải: 0–10, 11–50 và 51–100 người dùng đồng thời. |
| **Tiêu chuẩn đáp ứng** | (1) 0–10 người dùng đồng thời: P95 Response Time ≤ 1 giây; (2) 11–50 người dùng đồng thời: P95 Response Time ≤ 2 giây; (3) 51–100 người dùng đồng thời: P95 Response Time ≤ 5 giây. |

#### SUPL-P01b

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian tương tác giao diện |
| **Độ đo yêu cầu** | Time to Interactive (TTI) cho các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự tại 3 mức tải: 0–10, 11–50 và 51–100 người dùng đồng thời. |
| **Tiêu chuẩn đáp ứng** | (1) 0–10 người dùng đồng thời: TTI ≤ 1,5 giây; (2) 11–50 người dùng đồng thời: TTI ≤ 3 giây; (3) 51–100 người dùng đồng thời: TTI ≤ 6 giây. |

#### SUPL-P02

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Sức chứa |
| **Độ đo yêu cầu** | (1) Số người dùng đồng thời tối đa hệ thống hỗ trợ; (2) Throughput tại mức tải mục tiêu; (3) Tỷ lệ suy giảm thời gian phản hồi khi so sánh mức 100 người dùng với mức 1 người dùng. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời; (2) Throughput đạt tối thiểu 50 tx/s tại mức 100 người dùng đồng thời; (3) Thời gian phản hồi tăng không quá 50% so với tải một người dùng. |

#### SUPL-P03a

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | Thời gian tải trang chi tiết hồ sơ nhân sự tổng hợp. |
| **Tiêu chuẩn đáp ứng** | Trang chi tiết hồ sơ nhân sự tổng hợp hiển thị hoàn chỉnh trong tối đa 5 giây tại mức không quá 10 người dùng đồng thời. |

#### SUPL-P03b

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | Thời gian chuẩn bị dữ liệu in hồ sơ nhân sự. |
| **Tiêu chuẩn đáp ứng** | Dữ liệu in hồ sơ nhân sự được chuẩn bị xong trong tối đa 10 giây tại mức không quá 10 người dùng đồng thời. |

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
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | Thời gian xuất dữ liệu hồ sơ nhân sự ra Excel với hai quy mô dữ liệu: ≤ 1.000 bản ghi và ≤ 10.000 bản ghi. |
| **Tiêu chuẩn đáp ứng** | (1) Với tập dữ liệu ≤ 1.000 bản ghi: thời gian xuất Excel ≤ 10 giây tại mức ≤ 10 người dùng đồng thời; (2) Với tập dữ liệu ≤ 10.000 bản ghi: thời gian xuất Excel ≤ 30 giây tại mức ≤ 10 người dùng đồng thời. |

#### SUPL-P07a

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phục hồi dịch vụ |
| **Độ đo yêu cầu** | Thời gian từ lúc hệ thống gặp sự cố đến khi phục vụ lại được request đầu tiên thành công. |
| **Tiêu chuẩn đáp ứng** | Hệ thống phục hồi khả năng phục vụ trong tối đa 15 phút sau sự cố crash hoặc restart. |

#### SUPL-P07b

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian khởi động lại |
| **Độ đo yêu cầu** | Thời gian từ lúc phát hiện crash hoặc phát lệnh restart đến khi toàn bộ stack khởi động thành công theo health check kỹ thuật. |
| **Tiêu chuẩn đáp ứng** | Toàn bộ stack khởi động lại trong tối đa 10 phút sau sự cố crash hoặc restart có chủ đích. |

### 6.6.3. Ghi chú phạm vi trong nhóm Performance

* SUPL-P01 gốc được tách thành SUPL-P01 và SUPL-P01b để tách riêng ngưỡng **P95 Response Time** và **TTI**, giúp requirement atomic hơn.
* SUPL-R02 gốc được đổi thành SUPL-P07a và SUPL-P07b để khớp với section **Hiệu năng** và yếu tố chất lượng chính của hai requirement này.
* Ngoài SUPL-P07b, hiện không có thêm yêu cầu nghiệm thu riêng cho thời gian khởi động mới hoặc tắt an toàn trong fragment này.
* **Resource utilization:** N/A trong fragment này vì stakeholder chưa đưa ra ràng buộc CPU, RAM, băng thông hoặc dung lượng lưu trữ cụ thể cho môi trường triển khai.

## 6.7. Yêu cầu về Độ tin cậy (Reliability)

Người thực hiện: Ngô Quang Tùng

### 6.7.1. Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
| --- | --- | --- | --- |
| 1 | SUPL-R01 | Hệ thống phải duy trì uptime tối thiểu 99,5% trong khung giờ 7:00–22:00 hằng ngày, không tính bảo trì theo kế hoạch. | FEAT 7.1–8.9 |
| 2 | SUPL-R03a | Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi 24 giờ. | FEAT 7.1–8.9 |
| 3 | SUPL-R03b | Hệ thống phải phục hồi từ bản sao lưu gần nhất và sẵn sàng phục vụ trong tối đa 4 giờ. | FEAT 7.1–8.9 |
| 4 | SUPL-R03c | Hệ thống phải lưu giữ bản sao lưu tối thiểu 30 ngày. | FEAT 7.1–8.9 |
| 5 | SUPL-R03d | Hệ thống phải đạt tỷ lệ backup thành công tối thiểu 99%. | FEAT 7.1–8.9 |
| 6 | SUPL-R04 | Hệ thống phải bảo đảm các thao tác tạo/chỉnh sửa hồ sơ nhân sự, hợp đồng và thay đổi trạng thái không để lại dữ liệu dở dang khi có lỗi. | FEAT 7.1–8.9 |
| 7 | SUPL-R05a | Hệ thống phải cảnh báo tối thiểu 5 phút trước khi phiên tự động hết hạn trên 100% phiên được kiểm thử. | FEAT 7.1–8.9 |
| 8 | SUPL-R05b | Hệ thống phải khôi phục dữ liệu nháp sau khi người dùng đăng nhập lại trong ít nhất 95% trường hợp kiểm thử. | FEAT 7.1–8.9 |

SUPL-R03 gốc được tách thành cụm SUPL-R03a, SUPL-R03b, SUPL-R03c, SUPL-R03d để phần sao lưu/phục hồi được trình bày liền mạch trong cùng một cụm requirement. Trong đó SUPL-R03b vẫn mang **yếu tố chất lượng chính là Hiệu năng – Thời gian phục hồi**.

### 6.7.2. Độ đo và tiêu chuẩn đáp ứng

#### SUPL-R01

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Tính sẵn sàng |
| **Độ đo yêu cầu** | (1) Tỷ lệ uptime theo tháng trong khung giờ 7:00–22:00; (2) Tổng downtime trong tháng; (3) MTBF. |
| **Tiêu chuẩn đáp ứng** | (1) Uptime đạt tối thiểu 99,5% mỗi tháng trong khung giờ 7:00–22:00; (2) Downtime không quá 2,25 giờ/tháng, không tính bảo trì theo kế hoạch; (3) MTBF đạt tối thiểu 720 giờ. |

#### SUPL-R03a

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | RPO (Recovery Point Objective), đo theo thời gian từ thời điểm backup gần nhất đến thời điểm kiểm tra. |
| **Tiêu chuẩn đáp ứng** | Hệ thống sao lưu dữ liệu tự động ít nhất mỗi 24 giờ, tương ứng RPO không vượt quá 24 giờ. |

#### SUPL-R03b

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phục hồi từ bản sao lưu |
| **Độ đo yêu cầu** | RTO (Recovery Time Objective) khi phục hồi từ bản sao lưu gần nhất. |
| **Tiêu chuẩn đáp ứng** | Hệ thống sẵn sàng phục vụ trở lại trong tối đa 4 giờ sau khi thực hiện phục hồi từ bản sao lưu gần nhất. |

#### SUPL-R03c

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Thời gian lưu giữ của mỗi bản sao lưu trước khi bị xóa hoặc ghi đè. |
| **Tiêu chuẩn đáp ứng** | Mỗi bản sao lưu được lưu giữ tối thiểu 30 ngày. |

#### SUPL-R03d

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Tỷ lệ backup thành công trên tổng số lần backup được lên lịch trong mỗi tháng. |
| **Tiêu chuẩn đáp ứng** | Tỷ lệ backup thành công đạt tối thiểu 99% trên tổng số lần backup được lên lịch trong mỗi tháng. |

#### SUPL-R04

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Tính toàn vẹn dữ liệu |
| **Độ đo yêu cầu** | (1) Số trường hợp phát sinh dữ liệu bất nhất quán sau lỗi; (2) Tỷ lệ các nhóm nghiệp vụ trọng yếu trong phạm vi FEAT 7.1–8.9 được bảo vệ khỏi cập nhật dở dang. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp dữ liệu bất nhất quán; (2) 100% các nhóm nghiệp vụ tạo/chỉnh sửa hồ sơ nhân sự, tạo/chỉnh sửa/chấm dứt hợp đồng và thay đổi trạng thái nghiệp vụ không phát sinh cập nhật dở dang khi có lỗi. |

#### SUPL-R05a

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | (1) Tỷ lệ phiên được hiển thị cảnh báo trước khi hết hạn; (2) Thời gian cảnh báo trước khi tự động đăng xuất. |
| **Tiêu chuẩn đáp ứng** | (1) 100% phiên được kiểm thử có cảnh báo trước khi hết hạn; (2) Cảnh báo xuất hiện tối thiểu 5 phút trước khi tự động đăng xuất. |

#### SUPL-R05b

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Tỷ lệ khôi phục dữ liệu nháp khi người dùng đăng nhập lại sau khi phiên hết hạn. |
| **Tiêu chuẩn đáp ứng** | Hệ thống khôi phục dữ liệu nháp trong ít nhất 95% trường hợp kiểm thử đối với form có dữ liệu đã nhập nhưng chưa lưu. |

### 6.7.3. Ghi chú phạm vi trong nhóm Reliability

* **Robustness:** N/A trong fragment này vì yêu cầu xử lý dữ liệu nhập sai và phản ứng với input bất thường đang được đặc tả tại các phần validation/giao diện của nhóm khác.
* **Fault tolerance:** N/A trong fragment này vì hiện chưa có yêu cầu vận hành về chế độ suy giảm hoặc tiếp tục phục vụ khi một thành phần phụ trợ bị lỗi.
* **Safety:** N/A vì HRMS là hệ thống quản lý nghiệp vụ nội bộ, không trực tiếp điều khiển thiết bị vật lý hoặc tạo rủi ro an toàn cho con người/môi trường.
* **Security:** Covered elsewhere trong các section bảo mật của nhóm, nên không lặp lại trong fragment Reliability này.
* **Accuracy / Correctness ngoài phạm vi Integrity:** Covered by SUPL-R04 đối với các thao tác cập nhật dữ liệu trọng yếu; các yêu cầu đúng/sai nghiệp vụ chi tiết theo từng use case sẽ được đặc tả ở tài liệu use case hoặc section chức năng tương ứng.

## 6.8. Yêu cầu về Bảo mật (Security)

Người thực hiện: Ngô Đức Nam Khánh

### 6.8.1. Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
| --- | --- | --- | --- | --- |
| 1 | SUPL-SE01 | Xác thực người dùng | Authentication (Xác thực) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 2 | SUPL-SE02 | Phân quyền truy cập | Authorization (Phân quyền truy cập) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 3 | SUPL-SE03 | Bảo vệ chống tấn công brute-force | Integrity (Toàn vẹn) - Chống tấn công tự động | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 4 | SUPL-SE04 | Mã hóa truyền tải dữ liệu (HTTPS) | Confidentiality (Bảo mật truyền tải) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 5 | SUPL-SE05 | Bảo vệ dữ liệu nhạy cảm | Confidentiality (Bảo mật dữ liệu) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 6 | SUPL-SE06 | Ngăn chặn tấn công web trên chức năng nhập liệu và cập nhật dữ liệu | Integrity (Toàn vẹn) - Chống tấn công web | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 7 | SUPL-SE07 | Chống SQL Injection | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 8 | SUPL-SE08 | Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) | FEAT 8.9 |
| 9 | SUPL-SE09 | Kiểm soát chấm dứt hợp đồng trước hạn | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) | FEAT 7.4 |

### 6.8.2. Chi tiết độ đo và tiêu chuẩn đáp ứng

#### 6.8.2.1. SUPL-SE01: Xác thực người dùng (Authentication)

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authentication (Xác thực) |
| **Mô tả yêu cầu** | Mọi truy cập vào hệ thống phải qua xác thực bằng tài khoản/mật khẩu. Mật khẩu phải đáp ứng chính sách: tối thiểu 8 ký tự, bao gồm chữ hoa, chữ thường và số. |
| **Độ đo yêu cầu** | 1) **Mức độ mạnh mật khẩu**: số quy tắc mật khẩu được hệ thống kiểm tra bắt buộc.  2) **Số lớp xác thực**: số bước xác thực trước khi truy cập hệ thống.  3) **An toàn phiên đăng nhập**: trạng thái phiên có thuộc tính bảo vệ và thời gian hết hạn không hoạt động. |
| **Tiêu chuẩn đáp ứng** | 1) Mật khẩu có **ít nhất 8 ký tự** và thỏa **3/3 quy tắc**: chữ hoa, chữ thường, chữ số.  2) Hệ thống áp dụng **01 lớp xác thực** bằng tên đăng nhập/mật khẩu trước khi vào hệ thống.  3) Phiên đăng nhập phải được bảo vệ khỏi truy cập từ script phía client và tự hết hiệu lực sau tối đa **30 phút** không hoạt động. |
| **Phương pháp đo** | Kiểm thử chức năng đăng nhập/đổi mật khẩu; kiểm tra rule validation trên form; kiểm tra cấu hình cookie/token phiên (HttpOnly, Secure, thời gian hết hạn). |
| **Lý do chọn độ đo** | Ngưỡng **8 ký tự** phù hợp mức tối thiểu mà NIST SP 800-63B và OWASP Authentication Cheat Sheet thừa nhận cho xác thực bằng mật khẩu; dự án giữ thêm **3 nhóm ký tự** vì đây là chính sách đã chốt trong SUPL gốc nhằm tăng độ khó đoán cho tài khoản nội bộ HRMS chưa triển khai MFA. Chọn **01 lớp xác thực** vì hệ thống hiện là cổng nghiệp vụ nội bộ, chưa có yêu cầu MFA trong phạm vi đề tài. Mốc **30 phút không hoạt động** bám yêu cầu hệ thống về tự động đăng xuất, cân bằng giữa an toàn phiên và tính tiện dụng khi cán bộ thao tác hồ sơ nhân sự. |

#### 6.8.2.2. SUPL-SE02: Phân quyền truy cập (Authorization)

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authorization (Phân quyền truy cập) |
| **Mô tả yêu cầu** | Hệ thống phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Nhân sự) – mỗi vai trò chỉ truy cập được các chức năng được cấp quyền. Mọi request API phải kiểm tra quyền trước khi xử lý. |
| **Độ đo yêu cầu** | 1) **Số trường hợp truy cập trái phép** phát hiện qua kiểm thử phân quyền.  2) **Tỷ lệ API được bảo vệ** = số API endpoint có kiểm tra quyền / tổng số API endpoint.  3) **Số vai trò được định nghĩa** trong mô hình RBAC. |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường hợp truy cập trái phép vào chức năng hoặc API không được cấp quyền.  2) **100%** API endpoint có cơ chế kiểm tra quyền trước khi xử lý.  3) Hệ thống có đúng **4 vai trò**: Admin, TCCB, TCKT, Nhân sự. |
| **Phương pháp đo** | Kiểm thử xâm nhập theo ma trận quyền; rà soát middleware/guard trên route API; đối chiếu cấu hình vai trò và quyền trong hệ thống. |
| **Lý do chọn độ đo** | Với bài toán phân quyền, nguyên tắc **least privilege** của NIST SP 800-53 AC-6 và OWASP Broken Access Control yêu cầu không chấp nhận truy cập vượt quyền, nên ngưỡng đúng phải là **0 trường hợp trái phép** và **100% endpoint được kiểm tra quyền**. Con số **4 vai trò** không phải chọn tùy ý mà xuất phát trực tiếp từ mô hình nghiệp vụ đã xác định trong đặc tả: Admin, TCCB, TCKT, Nhân sự. |

#### 6.8.2.3. SUPL-SE03: Bảo vệ chống tấn công brute-force

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công tự động |
| **Mô tả yêu cầu** | Khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp. Thời gian khóa tối thiểu 15 phút. |
| **Độ đo yêu cầu** | 1) **Ngưỡng khóa tài khoản**: số lần đăng nhập sai liên tiếp trước khi bị khóa.  2) **Thời gian khóa tạm thời**: số phút tài khoản bị khóa.  3) **Ghi log cảnh báo**: có/không bản ghi cảnh báo khi phát hiện hành vi brute-force. |
| **Tiêu chuẩn đáp ứng** | 1) Tài khoản bị khóa sau đúng **5 lần** đăng nhập sai liên tiếp.  2) Thời gian khóa tối thiểu **15 phút**.  3) Hệ thống phải ghi log cảnh báo, tối thiểu gồm **IP**, **thời gian** và **tài khoản bị tác động**. |
| **Phương pháp đo** | Thực hiện đăng nhập sai liên tiếp trên tài khoản thử nghiệm; đo thời gian khóa thực tế; kiểm tra bản ghi cảnh báo trong log bảo mật. |
| **Lý do chọn độ đo** | OWASP Authentication Cheat Sheet khuyến nghị **login throttling/account lockout** để chống brute-force. Ngưỡng **5 lần sai liên tiếp** là mức cấu hình rất phổ biến trong hệ thống doanh nghiệp vì đủ thấp để chặn thử mật khẩu tự động nhưng chưa gây khóa nhầm quá sớm cho người dùng thật. Mốc **15 phút** là thời gian làm chậm đáng kể tấn công online mà vẫn không buộc cán bộ phải nhờ quản trị viên mở khóa trong hầu hết trường hợp. Ba trường log **IP, thời gian, tài khoản** là tập tối thiểu để truy vết mẫu tấn công và đối chiếu sự cố. |

#### 6.8.2.4. SUPL-SE04: Mã hóa truyền tải dữ liệu (HTTPS)

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Confidentiality (Bảo mật truyền tải) |
| **Mô tả yêu cầu** | Toàn bộ giao tiếp giữa client và server phải sử dụng giao thức HTTPS (TLS 1.2 trở lên). |
| **Độ đo yêu cầu** | 1) **Phiên bản TLS** đang sử dụng.  2) **Tỷ lệ kết nối HTTPS** = số kết nối HTTPS / tổng số kết nối đến hệ thống.  3) **Chuyển hướng HTTP sang HTTPS**: có/không cơ chế tự động chuyển hướng. |
| **Tiêu chuẩn đáp ứng** | 1) Hệ thống chỉ chấp nhận kết nối với **TLS 1.2 trở lên**.  2) **100%** kết nối sử dụng HTTPS; **0%** kết nối HTTP không mã hóa được xử lý trực tiếp.  3) Mọi truy cập HTTP phải được tự động chuyển hướng sang HTTPS. |
| **Phương pháp đo** | Kiểm tra cấu hình TLS bằng trình duyệt/curl hoặc công cụ SSL; đo lưu lượng truy cập thực tế; kiểm thử request HTTP để xác nhận chuyển hướng. |
| **Lý do chọn độ đo** | NIST SP 800-52 Rev.2 yêu cầu tối thiểu phải hỗ trợ **TLS 1.2** và khuyến nghị tiến tới TLS 1.3; RFC **8996** của IETF đã chính thức loại bỏ TLS 1.0/1.1. Vì HRMS truyền thông tin tài khoản, CCCD, BHXH và dữ liệu hợp đồng, ngưỡng đúng phải là **100% HTTPS** và **0% HTTP thuần** để loại bỏ hoàn toàn kênh truyền không mã hóa. Yêu cầu chuyển hướng HTTP sang HTTPS giúp tránh lỗi cấu hình và giảm nguy cơ người dùng truy cập nhầm URL không an toàn. |

#### 6.8.2.5. SUPL-SE05: Bảo vệ dữ liệu nhạy cảm

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Confidentiality (Bảo mật dữ liệu) |
| **Mô tả yêu cầu** | Dữ liệu nhạy cảm (số CCCD, số BHXH, thông tin ngân hàng) phải được bảo vệ – chỉ hiển thị cho vai trò được phép, ghi log khi truy cập. |
| **Độ đo yêu cầu** | 1) **Số trường dữ liệu nhạy cảm bị lộ** cho vai trò không được phép.  2) **Tỷ lệ ghi audit log khi truy cập dữ liệu nhạy cảm** = số lần truy cập được ghi log / tổng số lần truy cập dữ liệu nhạy cảm. |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được cấp quyền.  2) **100%** lượt truy cập các trường CCCD, BHXH và thông tin ngân hàng được ghi audit log. |
| **Phương pháp đo** | Kiểm thử API/UI theo từng vai trò; kiểm tra payload trả về; đối chiếu nhật ký truy cập dữ liệu nhạy cảm với lịch sử thao tác thực tế. |
| **Lý do chọn độ đo** | Nghị định **13/2023/NĐ-CP** yêu cầu dữ liệu cá nhân phải được xử lý đúng mục đích, trong phạm vi cần thiết và có biện pháp bảo vệ tương ứng; riêng HRMS của trường còn chứa dữ liệu định danh và tài chính như **CCCD, BHXH, tài khoản ngân hàng**. Do đây là nhóm dữ liệu có rủi ro pháp lý và riêng tư cao, ngưỡng chấp nhận phải là **0 lộ lọt cho vai trò không có quyền**. Chọn **100% ghi audit log** vì mọi lần truy cập dữ liệu nhạy cảm đều phải truy vết được khi kiểm tra nội bộ hoặc xử lý sự cố theo tinh thần trách nhiệm giải trình của Nghị định 13. |

#### 6.8.2.6. SUPL-SE06: Ngăn chặn tấn công web trên chức năng nhập liệu và cập nhật dữ liệu

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công web |
| **Mô tả yêu cầu** | Hệ thống phải ngăn chặn các tấn công web làm giả yêu cầu hoặc chèn mã thực thi trên các chức năng nhập liệu và thao tác thay đổi dữ liệu. |
| **Độ đo yêu cầu** | 1) **Số lỗ hổng CSRF** phát hiện qua kiểm thử bảo mật.  2) **Số lỗ hổng XSS** phát hiện qua kiểm thử bảo mật.  3) **Tỷ lệ request thay đổi dữ liệu được bảo vệ** = số request POST/PUT/DELETE có cơ chế chống giả mạo / tổng số request POST/PUT/DELETE. |
| **Tiêu chuẩn đáp ứng** | 1) **0** lỗ hổng CSRF.  2) **0** lỗ hổng XSS.  3) **100%** chức năng POST/PUT/DELETE và các form thay đổi dữ liệu vượt qua kiểm thử chống CSRF; **100%** dữ liệu do người dùng nhập khi hiển thị lại trên giao diện vượt qua kiểm thử XSS. |
| **Phương pháp đo** | Kiểm thử bảo mật bằng OWASP ZAP hoặc công cụ tương đương; rà soát cơ chế CSRF token; kiểm tra escaping/sanitizing dữ liệu đầu vào và đầu ra. |
| **Lý do chọn độ đo** | OWASP Top 10:2021 xem các lỗi chèn mã và kiểm soát truy cập đầu vào/đầu ra là nhóm rủi ro trọng yếu; OWASP **CSRF Prevention Cheat Sheet** và **XSS Prevention Cheat Sheet** đều coi chỉ cần **một** điểm không bảo vệ là có thể khai thác được. Vì vậy các độ đo bảo mật này có dạng **sharp requirement**: **0 lỗ hổng** và **100% request thay đổi trạng thái được bảo vệ**. Với hệ thống HRMS có nhiều form thêm/sửa hồ sơ, mọi endpoint POST/PUT/DELETE đều phải có CSRF token và mọi dữ liệu phản chiếu lên UI đều phải được encode/sanitize. |

#### 6.8.2.7. SUPL-SE07: Chống SQL Injection

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu |
| **Mô tả yêu cầu** | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu. |
| **Độ đo yêu cầu** | 1) **Số lỗ hổng SQL Injection** phát hiện qua kiểm thử.  2) **Tỷ lệ truy vấn được bảo vệ** = số truy vấn sử dụng dữ liệu đầu vào có cơ chế tách dữ liệu khỏi câu lệnh SQL / tổng số truy vấn sử dụng dữ liệu đầu vào. |
| **Tiêu chuẩn đáp ứng** | 1) **0** lỗ hổng SQL Injection.  2) **100%** truy vấn có dữ liệu đầu vào từ người dùng được bảo vệ bằng cơ chế truy vấn tham số hóa hoặc ORM tương đương. |
| **Phương pháp đo** | Kiểm thử bằng sqlmap hoặc công cụ tương đương; rà soát code các truy vấn SQL/ORM; kiểm tra không có truy vấn ghép chuỗi trực tiếp từ dữ liệu đầu vào. |
| **Lý do chọn độ đo** | OWASP Top 10:2021 **A03 - Injection**, CWE-**89** và OWASP **SQL Injection Prevention Cheat Sheet** đều chỉ ra biện pháp chính là **prepared statements/parameterized queries**. Vì chỉ một truy vấn ghép chuỗi cũng đủ mở đường cho khai thác, nên tiêu chuẩn phù hợp phải là **0 lỗ hổng SQLi** và **100% truy vấn có input người dùng được tham số hóa**. Đây là ngưỡng có thể kiểm chứng rõ ràng bằng code review và penetration test. |

#### 6.8.2.8. SUPL-SE08: Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Mô tả yêu cầu** | Chỉ các vai trò được ủy quyền mới được phép cấu hình ẩn/hiện các mục khen thưởng/kỷ luật ở mức toàn hệ thống; mọi thay đổi cấu hình phải được ghi audit log với người thực hiện, thời gian, giá trị trước/sau. Tham chiếu FEAT 8.9. |
| **Độ đo yêu cầu** | 1) **Số thay đổi cấu hình trái phép** đối với chức năng ẩn/hiện mục khen thưởng/kỷ luật.  2) **Tỷ lệ thay đổi cấu hình được ghi audit log** = số thay đổi được lưu log / tổng số thay đổi cấu hình hợp lệ.  3) **Độ đầy đủ bản ghi audit** = số trường bắt buộc được ghi nhận / 4 trường bắt buộc (người thực hiện, thời gian, giá trị trước, giá trị sau). |
| **Tiêu chuẩn đáp ứng** | 1) **0** thay đổi cấu hình do người dùng không được ủy quyền thực hiện thành công.  2) **100%** thay đổi cấu hình hợp lệ được ghi audit log.  3) Mỗi bản ghi audit phải đạt **4/4 trường bắt buộc**: người thực hiện, thời gian, giá trị trước, giá trị sau. |
| **Phương pháp đo** | Kiểm thử phân quyền trên giao diện và API cấu hình; thực hiện thay đổi cấu hình thử nghiệm; đối chiếu lịch sử thay đổi với audit log của hệ thống. |
| **Lý do chọn độ đo** | Chức năng ẩn/hiện mục khen thưởng/kỷ luật tác động trực tiếp tới việc ai được nhìn thấy thông tin đánh giá nhân sự, nên đây là một cấu hình bảo mật cấp hệ thống. Vì vậy ngưỡng **0 thay đổi trái phép** là bắt buộc, không thể đặt mức dung sai. Chọn **100% audit log** vì mọi thay đổi cấu hình phải truy ngược được khi rà soát trách nhiệm. Bộ **4 trường** được chọn không tùy ý mà suy ra trực tiếp từ yêu cầu gốc: người thực hiện, thời gian, giá trị trước, giá trị sau là mức tối thiểu để chứng minh ai đổi gì và đổi khi nào. |

#### 6.8.2.9. SUPL-SE09: Kiểm soát chấm dứt hợp đồng trước hạn

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Mô tả yêu cầu** | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; hệ thống phải ghi audit log đầy đủ cho thao tác này gồm mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian và giá trị trước/sau. Tham chiếu FEAT 7.4. |
| **Độ đo yêu cầu** | 1) **Số trường hợp chấm dứt hợp đồng trước hạn trái phép** phát hiện qua kiểm thử quyền truy cập.  2) **Tỷ lệ thao tác chấm dứt hợp đồng được ghi audit log** = số thao tác được lưu log / tổng số thao tác chấm dứt hợp đồng trước hạn hợp lệ.  3) **Độ đầy đủ bản ghi audit** = số trường bắt buộc được ghi nhận / 7 trường bắt buộc (mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau). |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường hợp chấm dứt hợp đồng trước hạn được thực hiện bởi người dùng không có quyền.  2) **100%** thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log.  3) Mỗi bản ghi audit phải đạt **7/7 trường bắt buộc**. |
| **Phương pháp đo** | Kiểm thử chức năng chấm dứt hợp đồng với nhiều vai trò; rà soát log nghiệp vụ và audit log; đối chiếu dữ liệu trước/sau khi thao tác được thực hiện. |
| **Lý do chọn độ đo** | Theo **Bộ luật Lao động 2019** (nhóm điều về chấm dứt hợp đồng lao động và nghĩa vụ khi chấm dứt), thao tác chấm dứt hợp đồng trước hạn có hậu quả pháp lý trực tiếp đối với người lao động và nhà trường. Vì vậy ngưỡng đúng phải là **0 thao tác trái phép** và **100% được lưu vết**. Bộ **7 trường** được chọn bám sát hồ sơ cần có để kiểm tra tính hợp lệ của quyết định: mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau. Nếu thiếu một trường, việc đối chiếu pháp lý và kiểm toán nội bộ sẽ không đầy đủ. |

## 6.9. Ràng buộc triển khai (Implementation Constraints)

Người thực hiện: Ngô Đức Nam Khánh

### 6.9.1. Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
| --- | --- | --- | --- | --- |
| 1 | SUPL-IC01 | Ngôn ngữ và framework | Portability (Khả năng chuyển đổi công nghệ) - Công nghệ triển khai | Toàn hệ thống |
| 2 | SUPL-IC02 | Trình duyệt hỗ trợ | Compatibility (Tính tương thích) - Trình duyệt | Toàn hệ thống |
| 3 | SUPL-IC03 | Chuẩn mã hóa ký tự | Portability (Khả năng chuyển đổi) - Mã hóa dữ liệu | Toàn hệ thống |
| 4 | SUPL-IC04 | Định dạng file đính kèm | Correctness (Tính đúng đắn) - File đính kèm | Toàn hệ thống |

### 6.9.2. Chi tiết độ đo và tiêu chuẩn đáp ứng

#### 6.9.2.1. SUPL-IC01: Ngôn ngữ và framework

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi công nghệ)  - Công nghệ triển khai |
| **Mô tả yêu cầu** | Frontend: React.js (TypeScript). Backend: Laravel/PHP. Database: MySQL/MariaDB. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ tuân thủ stack frontend** = số module giao diện build bằng React.js + TypeScript / tổng số module frontend.  2) **Tỷ lệ tuân thủ stack backend** = số service/backend module triển khai bằng Laravel/PHP / tổng số service backend.  3) **Mức tuân thủ cơ sở dữ liệu** = số môi trường triển khai chính thức sử dụng MySQL/MariaDB / tổng số môi trường triển khai chính thức. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** module frontend sử dụng React.js kết hợp TypeScript.  2) **100%** thành phần backend sử dụng Laravel/PHP.  3) **100%** môi trường triển khai chính thức sử dụng MySQL hoặc MariaDB; **0** thành phần production dùng hệ quản trị cơ sở dữ liệu ngoài phạm vi yêu cầu. |
| **Phương pháp đo** | Rà soát package.json, tsconfig, composer.json, cấu trúc source code, file cấu hình triển khai và cấu hình kết nối cơ sở dữ liệu của hệ thống. |
| **Lý do chọn độ đo** | Đây là **ràng buộc triển khai**, nên bản chất là điều kiện nhị phân: hoặc tuân thủ, hoặc không tuân thủ. Vì vậy ngưỡng hợp lý phải là **100% đúng stack** và **0 thành phần production ngoài stack đã phê duyệt**. Bộ công nghệ React + TypeScript, Laravel/PHP, MySQL/MariaDB được giữ nguyên theo đặc tả nguồn vì phù hợp năng lực nhóm, tài nguyên triển khai của bài toán web nội bộ trường đại học, đồng thời giúp đồng nhất tài liệu, bảo trì và chấm nghiệm thu. |

#### 6.9.2.2. SUPL-IC02: Trình duyệt hỗ trợ

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Compatibility (Tính tương thích)  - Trình duyệt |
| **Mô tả yêu cầu** | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox, Edge. |
| **Độ đo yêu cầu** | 1) **Độ phủ trình duyệt mục tiêu** = số trình duyệt/phiên bản mục tiêu được kiểm thử / tổng số trình duyệt/phiên bản mục tiêu.  2) **Tỷ lệ chức năng chính đạt** = số chức năng nghiệp vụ chính chạy đúng trên từng trình duyệt / tổng số chức năng chính cần kiểm thử.  3) **Số lỗi nghiêm trọng theo trình duyệt** phát hiện trong kiểm thử tương thích. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** phạm vi kiểm thử phải bao gồm Chrome bản mới nhất và **2 phiên bản gần nhất**, Firefox bản ổn định hiện hành và Edge bản ổn định hiện hành tại thời điểm nghiệm thu.  2) **100%** chức năng chính hoạt động đúng trên Chrome; **≥ 95%** chức năng chính hoạt động đúng trên Firefox và Edge.  3) **0** lỗi mức Nghiêm trọng/Critical trên các trình duyệt mục tiêu. |
| **Phương pháp đo** | Thực hiện kiểm thử tương thích chéo trình duyệt bằng test thủ công/kịch bản tự động trên môi trường nghiệm thu; ghi nhận lỗi theo từng trình duyệt và từng phiên bản. |
| **Lý do chọn độ đo** | Chính sách **“bản mới nhất + 2 phiên bản gần nhất”** là cách hỗ trợ phổ biến với các trình duyệt evergreen vì cân bằng được độ phủ người dùng và chi phí kiểm thử. Chrome được đặt ngưỡng **100%** vì theo xu hướng sử dụng desktop tại Việt Nam (nguồn tham khảo: StatCounter Global Stats), đây là trình duyệt ưu tiên cao nhất trong môi trường hành chính - giáo dục. Firefox và Edge được đặt **≥95%** để vẫn bảo đảm tương thích thực tế nhưng tránh chi phí tối ưu hóa quá mức cho các khác biệt nhỏ không ảnh hưởng nghiệp vụ. Riêng lỗi **Critical = 0** vì chỉ cần một lỗi nghiêm trọng trên trình duyệt mục tiêu cũng có thể làm gián đoạn nghiệp vụ nhân sự. |

#### 6.9.2.3. SUPL-IC03: Chuẩn mã hóa ký tự

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi)  - Mã hóa dữ liệu |
| **Mô tả yêu cầu** | Toàn bộ hệ thống sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ Tiếng Việt có dấu. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ thành phần dùng UTF-8** = số thành phần kiểm tra đạt UTF-8 / tổng số thành phần cần kiểm tra (giao diện, API response, cơ sở dữ liệu, file import/export).  2) **Số lỗi hiển thị tiếng Việt có dấu** phát hiện khi nhập, lưu, tìm kiếm và hiển thị dữ liệu tiếng Việt. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** thành phần của hệ thống dùng UTF-8.  2) **0** lỗi hiển thị sai tiếng Việt có dấu trên giao diện, dữ liệu lưu trữ, dữ liệu xuất và dữ liệu tải lại từ hệ thống. |
| **Phương pháp đo** | Kiểm tra cấu hình charset/collation của cơ sở dữ liệu, header phản hồi HTTP, cấu hình file nguồn; kiểm thử với bộ dữ liệu mẫu có đầy đủ ký tự tiếng Việt có dấu. |
| **Lý do chọn độ đo** | W3C khuyến nghị nhà phát triển **luôn chọn UTF-8** cho nội dung và dữ liệu web; với hệ thống HRMS tiếng Việt, đây gần như là lựa chọn bắt buộc để bảo toàn dấu tiếng Việt trong tên người, địa chỉ, đơn vị, quyết định, hợp đồng. Vì mã hóa là thuộc tính nền tảng của toàn hệ thống, mức chấp nhận phù hợp là **100% thành phần dùng UTF-8** và **0 lỗi hiển thị**; chỉ một điểm lệch charset cũng có thể gây lỗi dây chuyền khi nhập, tìm kiếm, lưu và xuất dữ liệu. |

#### 6.9.2.4. SUPL-IC04: Định dạng file đính kèm

| Thuộc tính | Nội dung |
| --- | --- |
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn)  - File đính kèm |
| **Mô tả yêu cầu** | Hệ thống hỗ trợ upload/download file PDF (bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động) và Excel (import/export nhân sự). Kích thước file tối đa: 10MB. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ file đúng định dạng được xử lý thành công** = số file PDF/Excel hợp lệ được upload, download, import hoặc export thành công / tổng số file hợp lệ được thử nghiệm.  2) **Ngưỡng kích thước file tối đa** hệ thống cho phép xử lý.  3) **Tỷ lệ từ chối file không hợp lệ** = số file sai định dạng hoặc vượt dung lượng bị từ chối / tổng số file sai định dạng hoặc vượt dung lượng được thử nghiệm. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** file PDF hợp lệ dùng cho bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động được upload/download thành công; **100%** file Excel hợp lệ dùng cho import/export nhân sự được xử lý thành công.  2) Kích thước tối đa được chấp nhận là **10MB/file**.  3) **100%** file sai định dạng hoặc lớn hơn **10MB** bị từ chối và hệ thống hiển thị thông báo lỗi rõ ràng. |
| **Phương pháp đo** | Kiểm thử upload/download/import/export với tập file mẫu hợp lệ và không hợp lệ; kiểm tra MIME type, phần mở rộng file và phản hồi lỗi của hệ thống. |
| **Lý do chọn độ đo** | **PDF** và **Excel** được chọn vì bám đúng nhu cầu nghiệp vụ đã mô tả trong use case: hồ sơ quét/đính kèm cần dạng tài liệu cố định (PDF), còn nhập/xuất danh sách nhân sự cần dạng bảng tính (Excel). Mốc **10MB/file** là ngưỡng thực dụng cho môi trường trường đại học: đủ chứa bản scan hợp đồng, bằng cấp, chứng chỉ ở chất lượng đọc rõ, nhưng vẫn kiểm soát được dung lượng lưu trữ, băng thông và thời gian tải tệp. Các tỷ lệ **100% file hợp lệ xử lý thành công** và **100% file không hợp lệ bị từ chối** được chọn vì đây là ràng buộc đúng/sai rõ ràng của chức năng kiểm tra định dạng, không phải mục tiêu tối ưu mềm. |

# VII. ĐẶC TẢ YÊU CẦU PHẦN MỀM (SRS)

## 7.1. Giới thiệu

### 7.1.1. Phạm vi

**Hệ thống Quản lý Nhân sự (HRMS)** là hệ thống ứng dụng web nhiều người dùng phục vụ lĩnh vực quản lý nhân sự trong môi trường giáo dục đại học tại Trường Đại học Thủy Lợi. Hệ thống được xây dựng để tập trung hóa hoạt động quản lý nhân sự cho các đơn vị đào tạo, đơn vị nghiên cứu khoa học, các phòng ban chức năng và các đơn vị trực thuộc nhà trường.

Ở mức phạm vi sản phẩm, hệ thống bao phủ các chức năng chính sau:

* xác thực người dùng, quản lý tài khoản và phân quyền theo vai trò;
* quản lý cơ cấu tổ chức theo mô hình cây cha–con;
* quản lý hồ sơ nhân sự, hợp đồng lao động, đánh giá khen thưởng/kỷ luật;
* quản lý bổ nhiệm, điều chuyển, bãi nhiệm nhân sự theo đơn vị;
* quản lý khóa đào tạo, kết quả đào tạo và chứng chỉ;
* quản lý danh mục tham chiếu như hệ số lương, loại phụ cấp, loại hợp đồng;
* cung cấp báo cáo, thống kê nhân sự;
* hỗ trợ chức năng tự phục vụ cho cán bộ, giảng viên, nhân viên;
* ghi vết hoạt động và hỗ trợ truy vết kiểm toán.

Ngoài phạm vi sản phẩm của phiên bản hiện tại:

* các luồng tác vụ cá nhân khác ngoài xem thông tin cá nhân, xem đơn vị công tác, đăng ký đào tạo và xem các khóa đào tạo đã đăng ký cùng trạng thái/kết quả;
* các chức năng chưa được phản ánh trong baseline FEAT hiện tại của dự án, như quản lý nghỉ phép, chấm công, tính lương hoặc tuyển dụng.

### 7.1.2. Tổng quan về tài liệu

Tài liệu SRS này được tổ chức như sau:

* **Mục 7.1** mô tả phạm vi và cách tài liệu được tổ chức.
* **Mục 7.2** trình bày bối cảnh sản phẩm, nhóm người dùng, tác nhân hệ thống và các chức năng chính ở mức tổng quan.
* **Mục 7.3.1** mô tả các yêu cầu giao diện áp dụng ở mức toàn hệ thống.
* **Mục 7.3.2** mô tả các yêu cầu chức năng chính của hệ thống.
* **Mục 7.3.3** mô tả các yêu cầu bổ sung, yêu cầu phi chức năng và ràng buộc kỹ thuật.
* **Mục 7.3.4** mô tả các quy tắc truy vết, tổ chức requirement, thuộc tính requirement và các giả định/phụ thuộc dùng để quản lý bộ yêu cầu.

SRS này là tài liệu tổng hợp ở mức hệ thống. Tài liệu không thay thế các nguồn chi tiết như bộ **Use Case Specification (UCS)** hay tài liệu **supplementary requirements/metrics**; các tài liệu đó vẫn là nguồn chuẩn cho hành vi chi tiết và các ngưỡng xác minh tương ứng.

Về quan hệ tài liệu, SRS này tổng hợp nội dung ở mức hệ thống từ các nguồn **STR**, **VIS**, **UCS** và **SS** để phục vụ đặc tả và quản lý yêu cầu thống nhất trong dự án.

Các tài liệu nền tảng liên quan đến SRS này gồm:

| Tài liệu | Vai trò |
| --- | --- |
| Kế hoạch quản lý yêu cầu (RMP) | Định nghĩa loại requirement, thuộc tính, truy vết và tổ chức bộ tài liệu |
| Yêu cầu của các bên liên quan (STR) | Nguồn chuẩn cho STRQ; trong baseline hiện tại nội dung STRQ và FEAT đang được gộp trong stakeholder-interviews.md |
| Tài liệu tầm nhìn (VIS) | Vai trò logic là nguồn chuẩn cho FEAT và phạm vi sản phẩm; trong baseline hiện tại chưa tách thành file riêng và đang được gộp trong stakeholder-interviews.md |
| Mô hình hóa yêu cầu và bộ Use Case Specification (UCS) | Nguồn chuẩn cho tác nhân, nhóm use case, SCEN và hành vi chức năng chi tiết |
| Đặc tả yêu cầu bổ sung (SS) và tài liệu độ đo | Nguồn chuẩn cho SUPL, metric và acceptance criteria |

Các chữ viết tắt sử dụng trong tài liệu:

| Viết tắt | Diễn giải |
| --- | --- |
| HRMS | Human Resource Management System |
| SRS | Software Requirements Specification |
| RMP | Requirements Management Plan |
| STR | Stakeholder Requests Document |
| VIS | Vision Document |
| UCS | Use Case Specification |
| SS | Supplementary Specification |
| TCCB | Phòng Tổ chức – Cán bộ |
| TCKT | Phòng Tài chính – Kế toán |
| STRQ | Stakeholder Request |
| FEAT | Feature |
| UC | Use Case |
| SCEN | Scenario |
| SUPL | Supplementary Requirement |

## 7.2. Mô tả chung

### 7.2.1. Mô tả chung về giao diện

HRMS là hệ thống **ứng dụng web nhiều người dùng**. Người dùng truy cập hệ thống qua trình duyệt, thao tác nghiệp vụ trên giao diện web, và toàn bộ xử lý nghiệp vụ được thực hiện thông qua các API của hệ thống. Người dùng chủ yếu là cán bộ, giảng viên và nhân viên hành chính tại trường Đại học Thủy Lợi, thao tác trên máy tính để bàn trong môi trường mạng nội bộ hoặc Internet.

Các nhóm người dùng và tác nhân hệ thống chính của HRMS gồm:

| Nhóm người dùng / tác nhân | Vai trò sử dụng chính |
| --- | --- |
| Quản trị viên (Admin) | Quản lý tài khoản, phân quyền, quản lý cơ cấu tổ chức, xem nhật ký hệ thống |
| Phòng TCCB | Thực hiện nghiệp vụ quản lý hồ sơ, hợp đồng, đào tạo, đánh giá, điều chuyển/bổ nhiệm, cấu hình danh mục |
| Phòng TCKT | Tra cứu hồ sơ, xem dữ liệu phục vụ lương/phụ cấp, xem và xuất báo cáo thống kê |
| Cán bộ / Giảng viên / Nhân viên | Xem thông tin cá nhân, xem đơn vị công tác, đăng ký đào tạo, xem các khóa đào tạo đã đăng ký cùng trạng thái tham gia và kết quả |
| Hệ thống (System Timer / Auto-Job) | Thực hiện các tác vụ tự động: đăng xuất phiên hết hạn (FEAT 1.3), khóa tài khoản nhân sự thôi việc (FEAT 2.6), tự động đánh dấu thôi việc khi hợp đồng hết hạn (FEAT 7.6), ghi vết hoạt động (FEAT 12.1) |

Đặc điểm giao diện ở mức tổng quan:

* giao diện sử dụng tiếng Việt và điều hướng theo vai trò;
* sau đăng nhập, người dùng được đưa đến trang chính với nội dung phù hợp vai trò được phân quyền;
* hệ thống sử dụng các mẫu màn hình chính: danh sách có tìm kiếm/lọc, form nhập liệu, màn hình chi tiết, màn hình thống kê, hộp thoại xác nhận và chức năng import/export;
* hệ thống ưu tiên khai thác trên máy tính để bàn; yêu cầu hỗ trợ máy tính bảng được quy định chi tiết tại Mục 7.3.1 (UI-05, UI-06);
* hệ thống hỗ trợ nhập dữ liệu từ tệp Excel và xuất dữ liệu ra định dạng PDF, Excel theo quy định tại NFR-IC04.

### 7.2.2. Các chức năng chính

| Nhóm chức năng | Mô tả tổng quan | Truy vết chính |
| --- | --- | --- |
| Quản lý truy cập | Đăng nhập, đăng xuất, đổi mật khẩu, tự động đăng xuất khi không tương tác trong 30 phút | FEAT 1.1–1.4 |
| Nền tảng truy cập web | Cung cấp ứng dụng web nhiều người dùng; mọi thao tác nghiệp vụ được xử lý qua API | FEAT 1.5 |
| Quản trị tài khoản | Tìm kiếm, thêm, sửa, khóa/mở khóa tài khoản, phân quyền | FEAT 2.1–2.6 |
| Quản lý cơ cấu tổ chức | Thiết lập cây đơn vị, cập nhật thông tin đơn vị, giải thể/sáp nhập | FEAT 3.1–3.5 |
| Bố trí nhân sự theo đơn vị | Bổ nhiệm, điều chuyển, bãi nhiệm nhân sự trong cơ cấu tổ chức | FEAT 4.1–4.3 |
| Quản lý hợp đồng | Tạo, xem, sửa, chấm dứt hợp đồng lao động | FEAT 5.1–5.4 |
| Quản lý đánh giá | Ghi nhận và tra cứu khen thưởng/kỷ luật | FEAT 6.1–6.3 |
| Quản lý hồ sơ nhân sự | Tìm kiếm, lọc, tạo mới, chỉnh sửa, xem chi tiết, in/xuất, đánh dấu thôi việc, cấu hình ẩn/hiện mục khen thưởng – kỷ luật | FEAT 7.1–7.9 |
| Quản lý đào tạo | Mở khóa đào tạo, chỉnh sửa, xem khóa học, ghi nhận kết quả | FEAT 8.1–8.4 |
| Cấu hình danh mục | Quản lý hệ số lương, loại phụ cấp, loại hợp đồng | FEAT 9.1–9.5 |
| Báo cáo và thống kê | Xem và xuất thống kê nhân sự, hợp đồng, đào tạo, bổ nhiệm | FEAT 10.1–10.4 |
| Tự phục vụ cá nhân | Xem hồ sơ cá nhân, xem đơn vị công tác, đăng ký đào tạo, xem các khóa đào tạo đã đăng ký cùng trạng thái tham gia và kết quả | FEAT 11.1–11.4 |
| Ghi vết và kiểm toán | Tự động ghi nhật ký hoạt động (audit log) và cho phép quản trị viên truy xuất nhật ký | FEAT 12.1–12.2 |

## 7.3. Các yêu cầu cụ thể

### 7.3.1. Các yêu cầu về giao diện

| Mã | Yêu cầu | Mức ưu tiên | Truy vết nguồn |
| --- | --- | --- | --- |
| UI-01 | Hệ thống phải sử dụng tiếng Việt trên 100% màn hình, trừ các thuật ngữ kỹ thuật. | M | SUPL-U01 |
| UI-02 | Hệ thống phải áp dụng thống nhất bố cục, màu sắc và font chữ theo bộ quy chuẩn giao diện của hệ thống; số cặp màn hình thuộc cùng một mẫu giao diện có khác biệt ngoài bộ quy chuẩn này phải bằng 0. | M | SUPL-U01 |
| UI-03 | Hệ thống phải hiển thị mọi lỗi nhập liệu, lỗi nghiệp vụ và lỗi hệ thống bằng tiếng Việt, kèm mô tả nguyên nhân và ít nhất một gợi ý khắc phục. | M | SUPL-U03 |
| UI-05 | Ở độ phân giải từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang. | E | SUPL-U05 |
| UI-06 | Trên tablet 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện thao tác chính mà không cần phóng to. | E | SUPL-U05 |
| UI-07a | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập. | N | SUPL-U06 |
| UI-07b | Trên 100% form có nút xác nhận mặc định, phím Enter phải kích hoạt nút đó. | N | SUPL-U06 |
| UI-07c | 100% trang phải hiển thị breadcrumb để người dùng quay lại cấp điều hướng trước. | N | SUPL-U06 |
| UI-08 | Hệ thống phải hiển thị hộp thoại xác nhận trước 100% thao tác khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng trước hạn, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái làm mất hiệu lực dữ liệu hoặc quyền truy cập. | M | SUPL-U07 |

### 7.3.2. Các yêu cầu chức năng

Phần này tổng hợp các hành vi tương tác giữa tác nhân và hệ thống ở mức SRS, được rút gọn từ bộ **Use Case Specification (UCS)** của dự án. Điều kiện kích hoạt, tiền điều kiện, luồng cơ bản/luồng thay thế và các yêu cầu đặc thù chi tiết tiếp tục được quản lý tại các tài liệu UCS tương ứng; các mã **FR-**\* dưới đây chỉ là mã trình bày cục bộ để nhóm nội dung trong SRS.

#### 7.3.2.1. Hệ thống và tài khoản

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-ACC-01 | Hệ thống phải cho phép người dùng đăng nhập bằng tài khoản hợp lệ và chuyển hướng đến dashboard tương ứng với vai trò của người dùng. | Tất cả người dùng | FEAT 1.1, UC 4.1 |
| FR-ACC-02 | Hệ thống phải cho phép người dùng đăng xuất chủ động khỏi phiên làm việc hiện tại. | Tất cả người dùng | FEAT 1.2, UC 4.2 |
| FR-ACC-03 | Hệ thống phải tự động đăng xuất phiên làm việc khi không có tương tác trong 30 phút và đưa người dùng về màn hình đăng nhập. | Tất cả người dùng, Hệ thống | FEAT 1.3, UC 4.2 A1 |
| FR-ACC-04 | Hệ thống phải cho phép người dùng đã đăng nhập thay đổi mật khẩu của chính tài khoản đang sử dụng. | Tất cả người dùng | FEAT 1.4, UC 4.3 |
| FR-ACC-05 | Hệ thống phải cho phép Quản trị viên tìm kiếm tài khoản người dùng theo từ khóa và tiêu chí lọc được hệ thống hỗ trợ. | Quản trị viên | FEAT 2.1, UC 4.4 |
| FR-ACC-06 | Hệ thống phải cho phép Quản trị viên tạo mới tài khoản người dùng cho nhân sự đã tồn tại và chưa có tài khoản liên kết. | Quản trị viên | FEAT 2.2, UC 4.5 |
| FR-ACC-07 | Hệ thống phải cho phép Quản trị viên cập nhật thông tin của tài khoản người dùng đã tồn tại. | Quản trị viên | FEAT 2.3, UC 4.6 |
| FR-ACC-08 | Hệ thống phải cho phép Quản trị viên gán vai trò cho tài khoản người dùng theo mô hình phân quyền của hệ thống. | Quản trị viên | FEAT 2.4, UC 4.7 |
| FR-ACC-09 | Hệ thống phải cho phép Quản trị viên khóa hoặc mở khóa tài khoản người dùng theo quy tắc nghiệp vụ. | Quản trị viên | FEAT 2.5, UC 4.8 |
| FR-ACC-11 | Hệ thống phải cho phép Quản trị viên xem, tìm kiếm và lọc nhật ký hệ thống theo các tiêu chí được hỗ trợ. | Quản trị viên | FEAT 12.2, UC 4.42 |
| FR-ACC-12 | Hệ thống phải cho phép Quản trị viên xuất nhật ký hệ thống theo phạm vi dữ liệu đang được áp dụng. | Quản trị viên | FEAT 12.2, UC 4.42 A1 |

#### 7.3.2.2. Cơ cấu tổ chức và bố trí nhân sự

Nhóm yêu cầu này khai thác cơ cấu tổ chức dưới dạng cây cha–con ở mức hành vi nghiệp vụ. Ràng buộc tính hợp lệ của cây tổ chức được quy định tại mục 7.3.3 (NFR-DC02).

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-ORG-01 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB tạo mới đơn vị tổ chức trong cơ cấu cây cha–con của hệ thống. | Quản trị viên, TCCB | FEAT 3.1, FEAT 3.2, UC 4.9 |
| FR-ORG-02 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB cập nhật thông tin của đơn vị tổ chức đã tồn tại. | Quản trị viên, TCCB | FEAT 3.3, UC 4.10 |
| FR-ORG-03 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB thay đổi trạng thái đơn vị tổ chức sang giải thể hoặc sáp nhập theo quy tắc nghiệp vụ. | Quản trị viên, TCCB | FEAT 3.4, UC 4.11 |
| FR-ORG-04 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB xem chi tiết thông tin của một đơn vị tổ chức, bao gồm trạng thái, nhân sự trực thuộc và lịch sử liên quan. | Quản trị viên, TCCB | FEAT 3.5, UC 4.32 |
| FR-ORG-05 | Hệ thống phải cho phép Phòng TCCB bổ nhiệm nhân sự vào đơn vị tổ chức phù hợp với trạng thái làm việc và trạng thái hợp đồng của nhân sự. | TCCB | FEAT 4.1, UC 4.30 |
| FR-ORG-06 | Hệ thống phải cho phép Phòng TCCB điều chuyển nhân sự từ đơn vị hiện tại sang đơn vị tổ chức khác theo quy tắc nghiệp vụ. | TCCB | FEAT 4.2, UC 4.30 A1 |
| FR-ORG-07 | Hệ thống phải cho phép Phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức và cập nhật trạng thái công việc tương ứng. | TCCB | FEAT 4.3, UC 4.31 |

#### 7.3.2.3. Danh mục tham chiếu và hồ sơ nhân sự

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-CFG-01 | Hệ thống phải cho phép Phòng TCCB thêm mới danh mục hệ số lương. | TCCB | FEAT 9.1, UC 4.12 |
| FR-CFG-02 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa danh mục hệ số lương chưa bị ràng buộc bởi các điều kiện từ chối của hệ thống. | TCCB | FEAT 9.2, UC 4.13 |
| FR-CFG-03a | Hệ thống phải cho phép Phòng TCCB xóa danh mục hệ số lương khi danh mục chưa được sử dụng và đáp ứng quy tắc nghiệp vụ. | TCCB | FEAT 9.3, UC 4.14 |
| FR-CFG-03b | Hệ thống phải cho phép Phòng TCCB thay đổi trạng thái danh mục hệ số lương theo tình trạng sử dụng và quy tắc nghiệp vụ. | TCCB | FEAT 9.3, UC 4.15 |
| FR-CFG-04a | Hệ thống phải cho phép Phòng TCCB thêm mới danh mục loại phụ cấp. | TCCB | FEAT 9.4, UC 4.16 |
| FR-CFG-04b | Hệ thống phải cho phép Phòng TCCB chỉnh sửa danh mục loại phụ cấp đang ở trạng thái cho phép chỉnh sửa. | TCCB | FEAT 9.4, UC 4.17 |
| FR-CFG-04c | Hệ thống phải cho phép Phòng TCCB thay đổi trạng thái danh mục loại phụ cấp theo quy tắc nghiệp vụ. | TCCB | FEAT 9.4, UC 4.18 |
| FR-CFG-05a | Hệ thống phải cho phép Phòng TCCB thêm mới danh mục loại hợp đồng. | TCCB | FEAT 9.5, UC 4.19 |
| FR-CFG-05b | Hệ thống phải cho phép Phòng TCCB chỉnh sửa danh mục loại hợp đồng đang ở trạng thái cho phép chỉnh sửa. | TCCB | FEAT 9.5, UC 4.20 |
| FR-CFG-05c | Hệ thống phải cho phép Phòng TCCB thay đổi trạng thái danh mục loại hợp đồng theo quy tắc nghiệp vụ. | TCCB | FEAT 9.5, UC 4.21 |
| FR-HR-01 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT tìm kiếm hồ sơ nhân sự bằng các từ khóa được hệ thống hỗ trợ. | TCCB, TCKT | FEAT 7.1, UC 4.23 |
| FR-HR-02 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT lọc danh sách hồ sơ nhân sự theo nhiều tiêu chí nghiệp vụ. | TCCB, TCKT | FEAT 7.2, UC 4.24 |
| FR-HR-03 | Hệ thống phải cho phép Phòng TCCB tạo mới hồ sơ nhân sự bằng nhập tay hoặc import từ Excel và khởi tạo hồ sơ theo quy tắc nghiệp vụ. | TCCB | FEAT 7.3, UC 4.25 |
| FR-HR-05 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa hồ sơ nhân sự chỉ khi hồ sơ đang ở trạng thái làm việc hợp lệ, và phải từ chối chỉnh sửa hồ sơ đã thôi việc. | TCCB | FEAT 7.4, UC 4.26 |
| FR-HR-06 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xem chi tiết hồ sơ nhân sự theo quyền hạn được cấp. | TCCB, TCKT | FEAT 7.7, UC 4.28 |
| FR-HR-07a | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT in hồ sơ nhân sự theo quyền được cấp. | TCCB, TCKT | FEAT 7.8, UC 4.28 A1 |
| FR-HR-07b | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xuất hồ sơ nhân sự ra Excel theo quyền được cấp. | TCCB, TCKT | FEAT 7.8, UC 4.28 A2 |
| FR-HR-08 | Hệ thống phải cho phép Phòng TCCB đánh dấu thôi việc cho nhân sự và cập nhật các trạng thái liên quan theo quy tắc nghiệp vụ. | TCCB | FEAT 7.5, UC 4.27 |
| FR-HR-10 | Hệ thống phải cho phép Phòng TCCB cấu hình ẩn/hiện các mục khen thưởng và kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc Phòng TCCB. | TCCB | FEAT 7.9, UC 4.48 |

#### 7.3.2.4. Hợp đồng, đánh giá, đào tạo, báo cáo và tự phục vụ

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-CON-01 | Hệ thống phải cho phép Phòng TCCB tạo hợp đồng lao động mới cho nhân sự đủ điều kiện theo loại hợp đồng, thời hạn và số lần ký được cấu hình. | TCCB | FEAT 5.1, UC 4.22 |
| FR-CON-02 | Hệ thống phải cho phép Phòng TCCB xem danh sách và chi tiết hợp đồng lao động của nhân sự. | TCCB | FEAT 5.2, UC 4.43 |
| FR-CON-03 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa hợp đồng lao động khi hợp đồng đang ở trạng thái chưa có hiệu lực. | TCCB | FEAT 5.3, UC 4.44 |
| FR-CON-04 | Hệ thống phải cho phép Phòng TCCB chấm dứt trước hạn hợp đồng lao động đang còn hiệu lực và cập nhật trạng thái hợp đồng tương ứng. | TCCB | FEAT 5.4, UC 4.45 |
| FR-EVA-01 | Hệ thống phải cho phép Phòng TCCB ghi nhận đánh giá khen thưởng hoặc kỷ luật cho nhân sự đang còn làm việc. | TCCB | FEAT 6.1, UC 4.29 |
| FR-EVA-02 | Hệ thống phải cho phép Phòng TCCB xem lịch sử đánh giá khen thưởng/kỷ luật của từng nhân sự. | TCCB | FEAT 6.2, UC 4.46 |
| FR-EVA-03 | Hệ thống phải cho phép Phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo tiêu chí được hỗ trợ. | TCCB | FEAT 6.3, UC 4.47 |
| FR-TRN-01 | Hệ thống phải cho phép Phòng TCCB mở khóa đào tạo mới cho cán bộ, giảng viên. | TCCB | FEAT 8.1, UC 4.33 |
| FR-TRN-02 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa khóa đào tạo theo trạng thái và ràng buộc nghiệp vụ của khóa học. | TCCB | FEAT 8.2, UC 4.34 |
| FR-TRN-03 | Hệ thống phải cho phép Phòng TCCB xem chi tiết khóa đào tạo và danh sách người đã đăng ký. | TCCB | FEAT 8.3, UC 4.35 |
| FR-TRN-04 | Hệ thống phải cho phép Phòng TCCB ghi nhận kết quả đào tạo và lưu chứng chỉ vào hồ sơ nhân sự của người tham gia. | TCCB | FEAT 8.4, UC 4.36 |
| FR-RPT-01 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xem các báo cáo, thống kê về nhân sự, hợp đồng, đánh giá, đào tạo và bổ nhiệm. | TCCB, TCKT | FEAT 10.1–10.4, UC 4.37 |
| FR-RPT-02 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xuất báo cáo, thống kê theo phạm vi dữ liệu đang được áp dụng. | TCCB, TCKT | FEAT 10.1–10.4, UC 4.37 A1 |
| FR-SELF-01 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem thông tin cá nhân của chính mình. | Người dùng | FEAT 11.1, UC 4.38 |
| FR-SELF-02 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem thông tin chi tiết đơn vị đang công tác và cơ cấu trực thuộc liên quan. | Người dùng | FEAT 11.2, UC 4.39 |
| FR-SELF-03 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên đăng ký tham gia khóa đào tạo đang mở đăng ký, còn chỉ tiêu và đáp ứng quy tắc nghiệp vụ. | Người dùng | FEAT 11.3, UC 4.40 |
| FR-SELF-04 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem danh sách các khóa đào tạo đã đăng ký cùng trạng thái tham gia và kết quả đào tạo của mình. | Người dùng | FEAT 11.4, UC 4.41 |

### 7.3.3. Các yêu cầu bổ sung

#### 7.3.3.1. Các yêu cầu chức năng bổ sung toàn hệ thống

Tiểu mục này chỉ giữ các hành vi tự động hoặc cắt ngang nhiều use case có nguồn chuẩn chính tại Supplementary Specification. Những hành vi tự động chỉ là logic cục bộ của một use case cụ thể và không có nguồn chuẩn chính trong Supplementary Specification được giữ tại mục 7.3.2/UCS thay vì lặp lại tại đây.

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| SR-F01 | Hệ thống phải tự động ghi nhật ký cho 100% hành động truy cập, thêm mới/cập nhật dữ liệu, thay đổi trạng thái và thay đổi cấu hình; mỗi bản ghi phải có đủ thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. | SUPL-F01 |
| SR-F02 | Hệ thống phải tự động khóa tài khoản liên kết trong ≤ 1 phút sau khi nhân sự tương ứng được cập nhật sang trạng thái “Đã thôi việc”. | SUPL-F04 |
| SR-F03 | Hệ thống phải tự động cập nhật 100% hợp đồng đủ điều kiện sang trạng thái “Chờ gia hạn” trong ≤ 24 giờ kể từ thời điểm thỏa ngưỡng chờ gia hạn được cấu hình. | SUPL-F05 |
| SR-F04 | Khi khóa đào tạo chuyển sang trạng thái “Đang đào tạo”, hệ thống phải tự động cập nhật 100% đăng ký liên quan từ “Đã đăng ký” sang “Đang học” trong ≤ 1 phút. | SUPL-F06 |
| SR-F05 | Hệ thống phải áp dụng quy tắc thay đổi trạng thái đối với danh mục loại phụ cấp và loại hợp đồng để bảo toàn dữ liệu lịch sử, thay vì xóa dữ liệu đã được sử dụng. | SUPL-F07 |

#### 7.3.3.2. Yêu cầu về tính dễ sử dụng

Các yêu cầu về tính dễ sử dụng gắn trực tiếp với biểu hiện giao diện (ngôn ngữ, thông báo lỗi, khả năng thích ứng theo kích thước màn hình, điều hướng bằng bàn phím, breadcrumb, xác nhận thao tác) được quản lý tại mục 7.3.1. Tiểu mục này chỉ giữ các yêu cầu về tính dễ sử dụng không thuần trình bày.

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-U01 | Sau tối đa 2 giờ đào tạo hướng dẫn, ít nhất 95% người dùng mới thuộc phòng TCCB phải hoàn thành các tác vụ tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự mà không cần trợ giúp trực tiếp; ít nhất 95% người dùng mới thuộc phòng TCKT phải hoàn thành các tác vụ tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. | SUPL-U02 |
| NFR-U02 | Các danh sách nhân sự, hợp đồng và đơn vị phải hỗ trợ tìm kiếm theo từ khóa và lọc đa tiêu chí; bộ lọc phải cho phép kết hợp đồng thời ít nhất 3 tiêu chí; tác vụ tìm và mở chi tiết 1 hồ sơ nhân sự phải hoàn thành trong tối đa 3 bước. | SUPL-U04 |

#### 7.3.3.3. Yêu cầu về độ tin cậy

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-R01 | Hệ thống phải đạt uptime tối thiểu 99,5% mỗi tháng trong khung giờ phục vụ 7:00–22:00, không tính thời gian bảo trì theo kế hoạch. | SUPL-R01 |
| NFR-R02 | Sau sự cố crash hoặc restart, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa 15 phút. | SUPL-R02 |
| NFR-R03 | Hệ thống phải sao lưu dữ liệu ít nhất mỗi 24 giờ, lưu giữ bản sao lưu tối thiểu 30 ngày, bảo đảm RPO không quá 24 giờ và RTO không quá 4 giờ. | SUPL-R03 |
| NFR-R04 | Các thao tác cập nhật dữ liệu quan trọng phải tuân thủ nguyên tắc toàn bộ hoặc không thực hiện phần nào; số trường hợp dữ liệu bất nhất quán sau lỗi phải bằng 0. | SUPL-R04 |
| NFR-R05 | Đối với form có dữ liệu nhập dở, hệ thống phải cảnh báo trước 5 phút khi phiên sắp hết hạn và phải khôi phục được tối thiểu 95% dữ liệu gần nhất sau khi người dùng đăng nhập lại. | SUPL-R05 |

#### 7.3.3.4. Yêu cầu về hiệu năng

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-P01 | P95 response time của các thao tác nghiệp vụ cơ bản phải không vượt quá 1 giây với 0–10 người dùng đồng thời, 2 giây với 11–50 người dùng, 5 giây với 51–100 người dùng và 10 giây khi vượt quá 100 người dùng. | SUPL-P01 |
| NFR-P02 | Hệ thống phải hỗ trợ tối thiểu 100 người dùng đồng thời, throughput tối thiểu 50 giao dịch/giây tại tải 100 người dùng và mức suy giảm hiệu năng không vượt quá 50% so với tải 1 người dùng. | SUPL-P02 |
| NFR-P03 | Dashboard phải tải xong trong tối đa 5 giây, báo cáo tổng hợp phức tạp trong tối đa 15 giây và mỗi biểu đồ thống kê trong tối đa 3 giây. | SUPL-P03 |
| NFR-P04 | Chức năng tìm kiếm và lọc phải trả kết quả trong tối đa 2 giây với tập dữ liệu đến 10.000 bản ghi và tối đa 5 giây với tập dữ liệu đến 50.000 bản ghi. | SUPL-P04 |
| NFR-P05 | Upload tệp dung lượng đến 5MB trên mạng LAN phải hoàn thành trong tối đa 5 giây; download tệp dung lượng đến 5MB trên mạng LAN phải hoàn thành trong tối đa 3 giây. | SUPL-P05 |
| NFR-P06 | Xuất Excel phải hoàn thành trong tối đa 10 giây với tối đa 1.000 bản ghi và tối đa 30 giây với tối đa 10.000 bản ghi. | SUPL-P06 |

#### 7.3.3.5. Yêu cầu về bảo mật và quyền riêng tư

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-SE01 | Mọi truy cập vào hệ thống phải được xác thực bằng tài khoản/mật khẩu; mật khẩu phải có tối thiểu 8 ký tự, bao gồm chữ hoa, chữ thường và chữ số. | SUPL-SE01 |
| NFR-SE02 | Hệ thống phải áp dụng RBAC với 4 vai trò chính; 100% API endpoint phải kiểm tra quyền trước khi xử lý. | SUPL-SE02, SUPL-DC03 |
| NFR-SE03 | Hệ thống phải khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp trong ít nhất 15 phút và phải ghi log cảnh báo khi phát hiện hành vi brute-force. | SUPL-SE03 |
| NFR-SE04 | 100% giao tiếp giữa client và server phải sử dụng HTTPS với TLS phiên bản 1.2 trở lên. | SUPL-SE04 |
| NFR-SE05 | Dữ liệu nhạy cảm như CCCD, số BHXH và thông tin ngân hàng chỉ được hiển thị cho vai trò được phép; 100% truy cập các dữ liệu này phải được ghi audit log. | SUPL-SE05 |
| NFR-SE06 | Hệ thống phải ngăn chặn CSRF trên 100% chức năng POST, PUT, PATCH và các yêu cầu thay đổi trạng thái tương đương; mọi dữ liệu hiển thị có nguồn gốc từ input người dùng phải vượt qua kiểm thử XSS; số lỗ hổng CSRF và XSS phát hiện được phải bằng 0. | SUPL-SE06 |
| NFR-SE07 | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu; số lỗ hổng SQL Injection phát hiện được phải bằng 0. | SUPL-SE07 |
| NFR-SE08 | Chỉ vai trò được ủy quyền mới được phép cấu hình ẩn/hiện mục khen thưởng/kỷ luật; 100% thay đổi cấu hình phải được ghi audit log với giá trị trước/sau. | SUPL-SE08 |
| NFR-SE09 | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; 100% thao tác này phải được ghi audit log với mã hợp đồng, mã nhân sự, lý do, người thực hiện, thời gian và giá trị trước/sau. | SUPL-SE09 |
| NFR-SE10 | Mật khẩu người dùng phải được lưu bằng cơ chế băm một chiều thích ứng; tham số độ khó phải đạt tối thiểu mức tương đương bcrypt cost 10; số mật khẩu lưu ở dạng văn bản thuần phải bằng 0. | SUPL-F08 |
| NFR-LR01 | Hệ thống phải hỗ trợ quản lý sự đồng ý thu thập dữ liệu cá nhân và xử lý yêu cầu hợp lệ về ẩn dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP. | SUPL-LR01 |
| NFR-LR02 | Các danh mục loại hợp đồng, phụ cấp và chức danh được cấu hình và sử dụng trong hệ thống phải tuân theo bộ danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt trên cơ sở quy định hiện hành của cơ quan quản lý. | SUPL-LR02 |
| NFR-LR03 | Hồ sơ nhân sự phải được lưu trữ tối thiểu 75 năm; hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu 10 năm sau khi kết thúc hoặc sau bản ghi cuối cùng. | SUPL-LR03 |

#### 7.3.3.6. Yêu cầu về hỗ trợ, bảo trì và ràng buộc kỹ thuật

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-S01 | Hệ thống phải được tổ chức thành các module chức năng có giao diện tích hợp rõ ràng; thay đổi một module không được buộc sửa đổi từ 2 module khác trở lên. | SUPL-S01 |
| NFR-S02 | Hệ thống phải cung cấp tài liệu API cho backend, hướng dẫn triển khai và hướng dẫn sử dụng cho từng vai trò; tối thiểu 90% API endpoint phải có mô tả trong tài liệu và 100% chức năng chính phải có hướng dẫn sử dụng. | SUPL-S02 |
| NFR-S03 | Hệ thống phải cho phép mở rộng tối thiểu 3 danh mục cấu hình (hệ số lương, loại phụ cấp, loại hợp đồng) qua giao diện quản trị mà không cần thay đổi mã nguồn. | SUPL-S03 |
| NFR-S04 | Hệ thống phải hỗ trợ ít nhất 4 cấp độ log phía server gồm ERROR, WARNING, INFO và DEBUG; mỗi log lỗi phải có timestamp, request ID và stack trace. | SUPL-S04 |
| NFR-S05 | Hệ thống phải hỗ trợ tối thiểu 2 nút ứng dụng chạy song song trong cùng môi trường và bảo đảm các request liên tiếp của cùng người dùng vẫn hoạt động đúng khi được phân phối qua các nút khác nhau. | SUPL-S05 |
| NFR-DC01 | Hệ thống phải được xây dựng theo kiến trúc client–server; frontend là SPA và giao tiếp với backend qua RESTful API. | SUPL-DC01 |
| NFR-DC02 | Dữ liệu cơ cấu tổ chức phải luôn tạo thành một cây hợp lệ với một nút gốc duy nhất là Trường Đại học Thủy Lợi và không được tạo chu trình. | SUPL-DC02 |
| NFR-IC01 | Stack triển khai bắt buộc của hệ thống là React.js (TypeScript) cho frontend, Laravel/PHP cho backend và MySQL/MariaDB cho cơ sở dữ liệu. | SUPL-IC01 |
| NFR-IC02 | Hệ thống phải hỗ trợ Chrome (bản mới nhất và 2 bản ổn định gần nhất), Firefox và Edge; 100% chức năng phải hoạt động đúng trên Chrome bản mới nhất và tối thiểu 95% chức năng phải hoạt động đúng trên Firefox và Edge. | SUPL-IC02 |
| NFR-IC03 | Toàn bộ hệ thống phải sử dụng mã hóa UTF-8 và không được phát sinh lỗi hiển thị tiếng Việt có dấu. | SUPL-IC03 |
| NFR-IC04 | Hệ thống chỉ hỗ trợ tệp PDF cho upload/download đính kèm nghiệp vụ và tệp Excel cho import/export dữ liệu nhân sự; kích thước tối đa của mỗi tệp là 10MB và hệ thống phải thông báo lỗi khi vượt quá giới hạn. | SUPL-IC04 |

### 7.3.4. Các yêu cầu khác

#### 7.3.4.1. Quy tắc truy vết

Chuỗi truy vết của bộ yêu cầu phải tuân theo cấu trúc sau:

STRQ ──→ FEAT ──→ UC ──→ SCEN
 │ │
 │ └──→ SUPL
 └──→ SUPL

Chi tiết các đường truy vết tối thiểu:

| Từ | Đến | Quan hệ | Ràng buộc bắt buộc |
| --- | --- | --- | --- |
| STRQ | FEAT | Nhiều-nhiều | Mỗi STRQ ở trạng thái Approved phải truy vết tới ít nhất một FEAT hoặc SUPL. |
| STRQ | SUPL | Nhiều-nhiều | Nằm trong ràng buộc bao phủ STRQ ở trên. |
| FEAT | UC | Nhiều-nhiều | Mỗi FEAT ở trạng thái Approved phải truy vết tới ít nhất một UC hoặc SUPL. |
| FEAT | SUPL | Nhiều-nhiều | Nằm trong ràng buộc bao phủ FEAT ở trên. |
| UC | FEAT | Truy vết ngược | Mỗi UC phải truy vết ngược về FEAT mà nó hiện thực hóa. |
| SUPL | FEAT | Truy vết ngược | Mỗi SUPL phải truy vết ngược về FEAT mà nó hỗ trợ. |
| UC | SCEN | Một-nhiều | Mỗi UC phải có ít nhất một SCEN tương ứng với luồng cơ bản. |

Các quy tắc bao phủ bắt buộc:

* mỗi **STRQ** ở trạng thái Approved phải truy vết tới ít nhất một **FEAT** hoặc **SUPL**;
* mỗi **FEAT** ở trạng thái Approved phải truy vết tới ít nhất một **UC** hoặc **SUPL**;
* mỗi **UC** phải có ít nhất một **SCEN** tương ứng với luồng cơ bản;
* **UC** và **SUPL** phải hỗ trợ truy vết ngược về **FEAT** mà chúng hiện thực hóa hoặc hỗ trợ.

#### 7.3.4.2. Loại requirement và quy tắc đặt requirement

| Loại requirement / artefact quản lý | Viết tắt | Vai trò | Nguồn chuẩn logic / vị trí baseline hiện tại |
| --- | --- | --- | --- |
| Stakeholder Request | STRQ | Ghi nhận nhu cầu và mong đợi của stakeholder trong problem domain | Nguồn chuẩn logic: STR; baseline hiện tại: stakeholder-interviews.md |
| Feature | FEAT | Biểu diễn các capability ở mức sản phẩm trong solution domain | Nguồn chuẩn logic: VIS; baseline hiện tại: stakeholder-interviews.md |
| Use Case | UC | Mô tả hành vi chức năng chi tiết theo tương tác giữa tác nhân và hệ thống | Nguồn chuẩn logic: UCS; trong baseline hiện tại danh mục/mapping tổng hợp có trong requirement-modeling.md, còn đặc tả chi tiết nằm trong các tài liệu UCS tương ứng |
| Scenario | SCEN | Mô tả các đường đi hợp lệ của từng use case | Nguồn chuẩn: các tài liệu UCS tương ứng |
| Supplementary Requirement | SUPL | Mô tả yêu cầu cross-cutting, NFR và constraint | Nguồn chuẩn: supplementary-requirements.md |
| Metric / Acceptance Criteria | Metric | Lượng hóa cách xác minh SUPL | Nguồn chuẩn: supplementary-metrics.md |

Quy tắc đặt requirement trong bộ tài liệu:

* Các mã **UI-**, **FR-**, **SR-**, **NFR-** trong SRS chỉ là mã trình bày cục bộ để nhóm nội dung; mã truy vết chuẩn dùng để quản lý requirement trong dự án vẫn là **STRQ**, **FEAT**, **UC**, **SCEN** và **SUPL**.
* Nội dung mô tả giao diện ở mức tổng quan phải nằm tại mục **7.2.1**; các yêu cầu giao diện có thể kiểm thử và áp dụng toàn hệ thống được tổng hợp tại mục **7.3.1** của SRS, với nguồn chuẩn ở **SS** trừ khi yêu cầu chỉ gắn với một **UCS** cụ thể.
* Các yêu cầu chỉ áp dụng cho một use case hoặc một bước luồng cụ thể phải có nguồn chuẩn tại tài liệu **UCS** tương ứng thay vì nâng lên mục **7.3.3**.
* Các yêu cầu áp dụng toàn hệ thống, cắt ngang nhiều use case, phi chức năng hoặc ràng buộc kỹ thuật/pháp lý phải có nguồn chuẩn tại **SS**; mục **7.3.3** của SRS chỉ tổng hợp các yêu cầu này ở mức hệ thống.

#### 7.3.4.3. Thuộc tính requirement tối thiểu

| Loại requirement | Thuộc tính tối thiểu phải quản lý |
| --- | --- |
| STRQ | Status, Priority, Benefit, Effort, Risk, Stability, Reason |
| FEAT | Status, Priority, Benefit, Effort, Risk, Stability, Difficulty, Target Release, Assigned To, Reason, Transformation |
| UC | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason, Actor |
| SUPL | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason |

#### 7.3.4.4. Báo cáo và chế độ xem requirement

Các chế độ xem requirement tối thiểu phải duy trì trong baseline dự án gồm:

* ma trận thuộc tính cho STRQ, FEAT, UC và SUPL;
* ma trận truy vết STRQ → FEAT;
* ma trận truy vết STRQ → SUPL;
* ma trận truy vết FEAT → UC;
* ma trận truy vết FEAT → SUPL;
* ma trận truy vết UC → Design, với neo thiết kế chính hiện tại là class-diagram.md;
* báo cáo gap cho **STRQ** ở trạng thái Approved chưa truy vết tới **FEAT/SUPL**, **FEAT** ở trạng thái Approved chưa truy vết tới **UC/SUPL**, **UC** chưa có **SCEN** luồng cơ bản, và **UC/SUPL** chưa có truy vết ngược về **FEAT**;
* cây truy vết cho phép xem phân rã từ **STRQ** xuống **FEAT**, **UC**, **SCEN** và các **SUPL** liên quan theo chuỗi truy vết đã định nghĩa.

#### 7.3.4.5. Giả định, phụ thuộc và ghi chú chuẩn hóa nguồn

* Trong baseline hiện tại, **FEAT 1.5** được truy vết tới **SUPL-DC01** như một ràng buộc kiến trúc; mục này không có **UC** riêng.
* Tài liệu **stakeholder-interviews.md** hiện là nguồn chuẩn chứa chung STRQ và FEAT, thay cho việc tách riêng tài liệu STR và VIS.
* File **uc31-42.md** hiện đang chứa nội dung từ **UC 4.31 đến UC 4.48**; các tham chiếu đến UC 4.43–4.48 trong baseline hiện tại vẫn được đối chiếu tại file này cho đến khi bộ tài liệu được đổi tên đồng bộ.
* Khi cần đối chiếu quy tắc truy vết, thuộc tính requirement và mapping tài liệu, **requirement-management-plan.md** là nguồn chuẩn quản lý requirement của dự án.
* Khi cần đối chiếu nguồn nội dung, tài liệu thu thập stakeholder là nguồn chuẩn cho STRQ/FEAT, bộ UCS là nguồn chuẩn cho hành vi chức năng chi tiết, và bộ SUPL cùng tài liệu độ đo là nguồn chuẩn cho các ngưỡng NFR.

## 7.4. Kết luận

SRS này tổng hợp phạm vi, hành vi chức năng, yêu cầu giao diện, yêu cầu bổ sung và các quy tắc quản lý requirement cho HRMS của Trường Đại học Thủy Lợi. Tài liệu là cơ sở để tiếp tục thiết kế, triển khai, kiểm thử và kiểm soát thay đổi yêu cầu trong các giai đoạn tiếp theo của dự án.