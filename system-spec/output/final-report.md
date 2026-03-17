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

### 1.1.3. Tổng quan tài liệu

Tài liệu RMP này được tổ chức theo các phần như sau:

- **Mục 1.2** mô tả các công cụ, hạ tầng và môi trường được sử dụng để quản lý yêu cầu.
- **Mục 1.2.2** định nghĩa các kiểu yêu cầu được sử dụng trong dự án.
- **Mục 1.2.3** liệt kê các loại tài liệu yêu cầu và ánh xạ tới kiểu yêu cầu tương ứng.
- **Mục 1.3 – 1.4** mô tả các nhân tố tham gia dự án và bảng liên lạc với các bên liên quan chính.
- **Mục 1.5** xác định phương pháp phát triển phần mềm được áp dụng.
- **Mục 1.6** mô tả quy trình quản lý thay đổi yêu cầu.
- **Mục 1.7** định nghĩa cấu trúc truy vết giữa các kiểu yêu cầu, bao gồm sơ đồ, ràng buộc và quy trình phát hiện khoảng trống.
- **Mục 1.8** định nghĩa các thuộc tính cho từng kiểu yêu cầu, bao gồm tập giá trị cho phép và ý nghĩa cụ thể trong ngữ cảnh dự án.
- **Mục 1.9** mô tả các báo cáo và chế độ xem dùng để giám sát độ bao phủ yêu cầu.

## 1.2. Công cụ sử dụng và các kiểu yêu cầu

### 1.2.1. Các công cụ, môi trường và hạ tầng quản lý yêu cầu

| STT | Công cụ / Hạ tầng | Mục đích sử dụng |
| --- | --- | --- |
| 1 | Microsoft Word | Soạn thảo và chỉnh sửa các tài liệu quản lý yêu cầu như RMP, SRS |
| 2 | StarUML / Draw.io | Mô hình hóa tiến trình công việc qua các sơ đồ GANTT, đường Găng. Mô hình hóa hệ thống thông qua các sơ đồ Use Case, các sơ đồ UML liên quan. |
| 3 | Discord / Họp nhóm trực tiếp | Trao đổi thông tin, thảo luận và xác nhận yêu cầu giữa các thành viên trong nhóm và các bên liên quan |
| 4 | Google Drive / Thư mục dự án dùng chung | Lưu trữ tập trung tất cả tài liệu yêu cầu (RMP, STR, VIS, UCS, SS). Các thành viên truy cập tài liệu thông qua thư mục chia sẻ với quyền đọc/ghi theo vai trò. |
| 5 | GitHub Issues / Trello | Theo dõi các yêu cầu thay đổi (Change Request), phân công nhiệm vụ và ghi nhận trạng thái xử lý yêu cầu. |

**Quy định truy cập:**

- Các thành viên không có quyền chỉnh sửa trực tiếp sẽ được cung cấp bản xuất PDF hoặc liên kết chỉ đọc (read-only) tới các tài liệu yêu cầu.
- Mọi thay đổi tài liệu yêu cầu phải được thực hiện thông qua quy trình quản lý thay đổi (xem Mục 1.6).

### 1.2.2. Các kiểu yêu cầu cho dự án

| Loại yêu cầu | Viết tắt | Loại tài liệu | Mô tả |
| --- | --- | --- | --- |
| Yêu cầu của các bên liên quan | STRQ | Yêu cầu của các bên liên quan (STR) | Mô tả các nhu cầu, mong đợi và mục tiêu chính của người dùng và các bên liên quan đối với hệ thống. Thuộc miền vấn đề (problem domain). |
| Yêu cầu tính năng | FEAT | Tài liệu tầm nhìn (VIS) | Mô tả các điều kiện, khả năng và các tính năng tổng quát mà hệ thống cần cung cấp. Thuộc miền giải pháp (solution domain). |
| Ca sử dụng | UC | Đặc tả ca sử dụng (UCS) | Mô tả chi tiết các ca sử dụng dưới dạng tương tác giữa tác nhân và hệ thống, phản ánh các yêu cầu chức năng. Mỗi UC có một tài liệu đặc tả riêng. |
| Kịch bản | SCEN | Đặc tả ca sử dụng (UCS) | Mô tả các đường đi hợp lệ qua một ca sử dụng (luồng cơ bản và luồng thay thế). Là cầu nối giữa UC và ca kiểm thử (TC), hỗ trợ triển khai lặp theo từng kịch bản. |
| Yêu cầu bổ sung | SUPL | Đặc tả bổ sung (SS) | Mô tả các yêu cầu phi chức năng và các ràng buộc của hệ thống không được thể hiện trong mô hình ca sử dụng. |
| Thuật ngữ | TERM | Bảng thuật ngữ (GLS) | Định nghĩa các thuật ngữ chuyên ngành và từ vựng chung được sử dụng trong dự án nhằm đảm bảo sự thống nhất trong giao tiếp. |

### 1.2.3. Loại tài liệu yêu cầu cho dự án

| Loại tài liệu | Viết tắt | Mô tả | Loại yêu cầu mặc định |
| --- | --- | --- | --- |
| Kế hoạch quản lý yêu cầu | RMP | Tài liệu mô tả phương pháp, quy trình và công cụ quản lý yêu cầu của dự án. | Không áp dụng |
| Yêu cầu của các bên liên quan | STR | Tập hợp các yêu cầu nghiệp vụ và mong đợi chính từ các bên liên quan. | Yêu cầu bên liên quan (STRQ) |
| Tài liệu tầm nhìn | VIS | Mô tả tổng quan hệ thống, phạm vi và các mục tiêu chính của dự án. | Yêu cầu tính năng (FEAT) |
| Đặc tả ca sử dụng | UCS | Mô tả chi tiết các ca sử dụng và cách người dùng tương tác với hệ thống. Mỗi UC có một tài liệu UCS riêng. | Ca sử dụng (UC) và Kịch bản (SCEN) |
| Đặc tả bổ sung | SS | Mô tả các yêu cầu phi chức năng và các ràng buộc của hệ thống. | Yêu cầu bổ sung (SUPL) |
| Bảng thuật ngữ | GLS | Định nghĩa từ vựng chung và thuật ngữ chuyên ngành nhân sự (hệ số lương, phụ cấp, bổ nhiệm, điều chuyển, v.v.) nhằm đảm bảo sự thống nhất trong trao đổi giữa các bên. | Thuật ngữ (TERM) |

## 1.3. Các nhân tố tham gia dự án phần mềm

| Team | Vai trò | Số lượng | Nhiệm vụ chính |
| --- | --- | --- | --- |
| Team 1 | BA / PM | 2 | Phân tích yêu cầu, lập kế hoạch và quản lý tiến độ dự án |
| Team 2 | SA / Design | 4 | Thiết kế kiến trúc hệ thống, cơ sở dữ liệu và giao diện người dùng (UI/UX) |
| Team 3 | Dev | 4 | Phát triển hệ thống Backend và Frontend theo thiết kế |
| Team 4 | Test | 2 | Xây dựng và thực hiện kiểm thử, đảm bảo chất lượng phần mềm |
| Team 5 | Deploy | 2 | Triển khai hệ thống, cấu hình môi trường và thiết lập quy trình CI/CD |
| **Tổng** |  | **14** |  |

## 1.4. Bảng liên lạc với các nhân tố chính (Stakeholder)

### 1.4.1. Các nhân tố chính

| STT | Nhân tố chính | Vai trò trong dự án | Đơn vị | Trách nhiệm chính | Hình thức liên lạc |
| --- | --- | --- | --- | --- | --- |
| 1 | Ban Giám hiệu | Nhà tài trợ / Phê duyệt | Ban Giám hiệu | Phê duyệt yêu cầu, xem xét báo cáo tổng hợp | Họp định kỳ, báo cáo |
| 2 | Phòng Tổ chức – Cán bộ | Khách hàng nghiệp vụ | Phòng TCCB | Cung cấp yêu cầu quản lý hồ sơ nhân sự | Họp, email |
| 3 | Phòng Tài chính – Kế toán | Khách hàng nghiệp vụ | Phòng TCKT | Cung cấp yêu cầu về lương, phụ cấp | Họp, trao đổi trực tiếp |
| 4 | Phòng CNTT | Đơn vị kỹ thuật | Phòng CNTT | Tư vấn kỹ thuật, hạ tầng, bảo mật | Họp kỹ thuật |
| 5 | Trưởng khoa / phòng | Người sử dụng chính | Các khoa / phòng | Góp ý, xác nhận yêu cầu quản lý nhân sự đơn vị | Họp, khảo sát |
| 6 | Nhóm phát triển | Thực hiện dự án | Nhóm dự án | Phân tích, thiết kế và triển khai hệ thống | Họp nhóm, công cụ trực tuyến |

### 1.4.2. Các bên liên quan khác

| STT | Bên liên quan | Vai trò / Mối liên hệ |
| --- | --- | --- |
| 1 | Bộ Nông nghiệp và Phát triển Nông thôn | Cơ quan quản lý nhà nước, ban hành quy định nhân sự, chế độ |
| 2 | Bộ Giáo dục và Đào tạo | Cơ quan quản lý chuyên ngành, quy định tiêu chuẩn cán bộ |
| 3 | Cơ quan Bảo hiểm xã hội | Đơn vị phối hợp quản lý bảo hiểm, chế độ người lao động |
| 4 | Cơ quan Thuế | Đơn vị phối hợp quản lý nghĩa vụ thuế thu nhập cá nhân |

## 1.5. Phương pháp phát triển phần mềm

Dự án HRMS áp dụng **phương pháp phát triển lặp (Iterative Development)** theo mô hình **Unified Process (UP)**, bao gồm bốn giai đoạn chính:

| Giai đoạn | Mô tả | Sản phẩm chính |
| --- | --- | --- |
| Khởi đầu (Inception) | Xác định phạm vi dự án, các bên liên quan chính, rủi ro lớn và tầm nhìn hệ thống. | Tài liệu tầm nhìn (VIS), Bản kế hoạch quản lý yêu cầu (RMP), Danh sách STRQ ban đầu |
| Phân tích chi tiết (Elaboration) | Thu thập, phân tích và đặc tả yêu cầu chi tiết; xây dựng kiến trúc hệ thống cơ sở. | Đặc tả ca sử dụng (UCS), Đặc tả bổ sung (SS), Kiến trúc cơ sở |
| Xây dựng (Construction) | Thiết kế, lập trình và kiểm thử các tính năng theo từng iteration. Các UC được triển khai theo kịch bản (SCEN), dần hoàn thiện toàn bộ UC qua các lần lặp. | Mã nguồn, Kết quả kiểm thử, Tài liệu thiết kế |
| Chuyển giao (Transition) | Triển khai hệ thống, đào tạo người dùng, nghiệm thu và bàn giao. | Hệ thống hoàn chỉnh, Tài liệu hướng dẫn sử dụng |

**Quy tắc đường cơ sở yêu cầu (Baseline):**

- Yêu cầu được đưa vào đường cơ sở khi đạt trạng thái **Approved** (Đã phê duyệt).
- Mọi thay đổi đối với yêu cầu đã vào đường cơ sở phải thông qua quy trình quản lý thay đổi (xem Mục 1.6).
- Việc kiểm tra truy vết (traceability verification) được thực hiện tại cuối mỗi iteration.

## 1.6. Quy trình quản lý thay đổi yêu cầu

### 1.6.1. Quy trình xử lý yêu cầu thay đổi

Mọi yêu cầu thay đổi (Change Request – CR) đối với yêu cầu đã được phê duyệt (trạng thái Approved trở lên) phải tuân thủ quy trình sau:

| Bước | Hoạt động | Người thực hiện | Sản phẩm |
| --- | --- | --- | --- |
| 1 | **Gửi yêu cầu thay đổi**: Mô tả nội dung thay đổi, lý do và yêu cầu liên quan (STRQ/FEAT/UC/SUPL bị ảnh hưởng). | Bất kỳ thành viên dự án hoặc bên liên quan | Phiếu CR (tạo trên GitHub Issues / Trello) |
| 2 | **Phân tích tác động**: Đánh giá ảnh hưởng của thay đổi tới các yêu cầu liên quan thông qua chuỗi truy vết (STRQ → FEAT → UC/SUPL), ước lượng công sức và rủi ro. | Team BA/PM (Team 1) | Báo cáo phân tích tác động |
| 3 | **Phê duyệt hoặc từ chối**: Quyết định chấp nhận, hoãn hoặc từ chối yêu cầu thay đổi. | Ban Giám hiệu (thay đổi lớn về phạm vi) hoặc PM (thay đổi nhỏ trong phạm vi đã duyệt) | Trạng thái CR cập nhật |
| 4 | **Cập nhật yêu cầu**: Nếu được phê duyệt, cập nhật các tài liệu yêu cầu liên quan (STR, VIS, UCS, SS) và cập nhật ma trận truy vết. | Team BA/PM (Team 1) | Tài liệu yêu cầu cập nhật, Ma trận truy vết cập nhật |
| 5 | **Xác minh cập nhật**: Kiểm tra lại tính nhất quán và truy vết sau thay đổi. | Team BA/PM (Team 1) | Kết quả kiểm tra truy vết |

### 1.6.2. Phân loại mức độ thay đổi

| Mức độ | Mô tả | Người phê duyệt |
| --- | --- | --- |
| Nhỏ | Sửa lỗi chính tả, làm rõ mô tả mà không thay đổi ý nghĩa yêu cầu | PM (Team 1) |
| Trung bình | Thay đổi nội dung yêu cầu nhưng không ảnh hưởng phạm vi dự án tổng thể | PM (Team 1) với sự đồng ý của Team SA/Design (Team 2) |
| Lớn | Thêm/xóa STRQ, FEAT hoặc UC; thay đổi phạm vi dự án | Ban Giám hiệu |

## 1.7. Cấu trúc truy vết yêu cầu

### 1.7.1. Sơ đồ truy vết

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

### 1.7.2. Chi tiết các đường truy vết

| Từ | Đến | Quan hệ | Ràng buộc bắt buộc |
| --- | --- | --- | --- |
| STRQ | FEAT | Nhiều-nhiều (thông thường 1 STRQ → nhiều FEAT) | Mỗi STRQ ở trạng thái **Approved** phải truy vết tới ít nhất một FEAT hoặc SUPL. |
| STRQ | SUPL | Nhiều-nhiều | (Nằm trong ràng buộc bao phủ STRQ ở trên) |
| FEAT | UC | Nhiều-nhiều | Mỗi FEAT ở trạng thái **Approved** phải truy vết tới ít nhất một UC hoặc SUPL. |
| FEAT | SUPL | Nhiều-nhiều | (Nằm trong ràng buộc bao phủ FEAT ở trên) |
| UC | FEAT | Truy vết ngược | UC truy vết ngược về FEAT mà nó hiện thực hóa. |
| SUPL | FEAT | Truy vết ngược | SUPL truy vết ngược về FEAT mà nó hỗ trợ. |
| UC | SCEN | Một-nhiều | Mỗi UC có ít nhất một SCEN (luồng cơ bản). |

### 1.7.3. Quy trình phát hiện khoảng trống truy vết (Gap Detection)

Tại cuối mỗi iteration, nhóm BA/PM thực hiện các kiểm tra sau:

**Kiểm tra truy vết xuôi (Forward-trace gaps) — yêu cầu thiếu bao phủ downstream:**

| Kiểm tra | Ý nghĩa |
| --- | --- |
| Tất cả STRQ chưa truy vết tới FEAT nào | Nhu cầu bên liên quan chưa có tính năng tương ứng |
| Tất cả FEAT chưa truy vết tới UC hoặc SUPL nào | Tính năng chưa được hiện thực hóa bằng yêu cầu cụ thể |
| Tất cả UC chưa truy vết tới artefact Design nào | Ca sử dụng chưa được phản ánh vào thiết kế |
| Tất cả UC chưa truy vết tới TC nào | Ca sử dụng chưa có kiểm thử xác minh |
| Tất cả SUPL chưa truy vết tới TC hoặc acceptance check nào | Yêu cầu bổ sung chưa có cơ chế kiểm chứng |

**Kiểm tra truy vết ngược (Back-trace gaps) — yêu cầu thiếu nguồn gốc upstream:**

| Kiểm tra | Ý nghĩa |
| --- | --- |
| Tất cả FEAT không được truy vết từ STRQ nào | Tính năng không có nhu cầu bên liên quan làm căn cứ |
| Tất cả UC không được truy vết từ FEAT nào | Ca sử dụng không có tính năng làm căn cứ |
| Tất cả SUPL không được truy vết từ FEAT nào | Yêu cầu bổ sung không có tính năng làm căn cứ |
| Tất cả artefact Design không được truy vết từ UC nào | Thành phần thiết kế không có căn cứ yêu cầu rõ ràng |
| Tất cả TC không được truy vết từ UC hoặc SUPL nào | Ca kiểm thử không có nguồn gốc yêu cầu rõ ràng |

Kết quả kiểm tra khoảng trống được ghi nhận trong báo cáo khoảng trống (Gap Report) — xem Mục 1.9.

## 1.8. Thuộc tính yêu cầu

Phần này định nghĩa các thuộc tính cho từng kiểu yêu cầu, bao gồm tập giá trị cho phép và ý nghĩa cụ thể trong ngữ cảnh dự án HRMS.

### 1.8.1. Thuộc tính cho FEAT (Yêu cầu tính năng)

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
| **Medium** (Trung bình — giá trị chuyển tiếp trong baseline hiện tại) | Giá trị kinh doanh ở mức trung bình. Giá trị này đang xuất hiện trong một số FEAT hiện hữu tại `stakeholder-interviews.md`; khi rà soát baseline, BA/PM có thể chuẩn hóa về **Important** hoặc **Useful** tùy ngữ cảnh nghiệp vụ. |
| **Low** (Thấp — giá trị chuyển tiếp trong baseline hiện tại) | Giá trị kinh doanh thấp, thiên về tính hỗ trợ hoặc nice-to-have. Khi rà soát baseline, nên ưu tiên chuẩn hóa về **Useful** nếu không cần duy trì mức phân biệt riêng. |

**Ghi chú chuẩn hóa:** Bộ giá trị khái niệm ưu tiên dùng cho Benefit vẫn là **Critical / Important / Useful**. Tuy nhiên, để bảo đảm nhất quán với baseline dữ liệu FEAT hiện đang lưu trong `stakeholder-interviews.md`, RMP tạm thời chấp nhận thêm các giá trị chuyển tiếp **Medium** và **Low** cho FEAT cho đến khi hoàn tất lần chuẩn hóa kế tiếp.

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

### 1.8.2. Thuộc tính cho STRQ (Yêu cầu của các bên liên quan)

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

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.8.1.

---

### 1.8.3. Thuộc tính cho UC (Ca sử dụng)

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

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.8.1.

---

### 1.8.4. Thuộc tính cho SUPL (Yêu cầu bổ sung)

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

Ý nghĩa của từng giá trị tương tự như định nghĩa tại Mục 1.8.1.

---

### 1.8.5. Bảng tổng hợp thuộc tính theo kiểu yêu cầu

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

## 1.9. Báo cáo và chế độ xem

Phần này xác định các báo cáo sẽ được tạo ra để giám sát độ bao phủ và trạng thái của yêu cầu trong suốt vòng đời dự án.

### 1.9.1. Ma trận thuộc tính (Attribute Matrices)

Mỗi kiểu yêu cầu có một ma trận thuộc tính liệt kê toàn bộ yêu cầu thuộc kiểu đó kèm giá trị các thuộc tính:

| Ma trận | Nội dung |
| --- | --- |
| Ma trận thuộc tính STRQ | Tất cả STRQ kèm Status, Priority, Benefit, Effort, Risk, Stability, Reason |
| Ma trận thuộc tính FEAT | Tất cả FEAT kèm Status, Priority, Benefit, Risk, Stability, Difficulty, Effort, Target Release, Assigned To, Reason, Transformation |
| Ma trận thuộc tính UC | Tất cả UC kèm Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason, Actor |
| Ma trận thuộc tính SUPL | Tất cả SUPL kèm Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason |

### 1.9.2. Ma trận truy vết (Traceability Matrices)

Thể hiện ánh xạ giữa các yêu cầu thuộc các kiểu khác nhau:

| Ma trận | Nội dung |
| --- | --- |
| Ma trận STRQ → FEAT | Mỗi STRQ ánh xạ tới (các) FEAT mà nó dẫn xuất |
| Ma trận STRQ → SUPL | Mỗi STRQ ánh xạ tới (các) SUPL phi chức năng/ràng buộc mà nó dẫn xuất trực tiếp |
| Ma trận FEAT → UC | Mỗi FEAT ánh xạ tới (các) UC hiện thực hóa tính năng đó |
| Ma trận FEAT → SUPL | Mỗi FEAT ánh xạ tới (các) SUPL hỗ trợ tính năng đó |
| Ma trận UC → Design | Mỗi UC ánh xạ tới (các) artefact thiết kế tương ứng; trong baseline hiện tại neo chính là `class-diagram.md` |
| Ma trận UC → TC | Mỗi UC ánh xạ tới (các) TC/bộ kiểm thử xác minh hành vi |
| Ma trận SUPL → TC | Mỗi SUPL ánh xạ tới (các) TC, acceptance check hoặc độ đo xác minh tương ứng |

### 1.9.3. Báo cáo khoảng trống (Gap Reports)

Xác định các yêu cầu thiếu truy vết — cần được xử lý trước khi kết thúc mỗi iteration:

| Báo cáo | Nội dung | Ý nghĩa |
| --- | --- | --- |
| STRQ chưa truy vết tới FEAT | Tất cả STRQ không truy vết tới bất kỳ FEAT nào | Nhu cầu bên liên quan chưa được chuyển đổi thành tính năng hệ thống |
| FEAT chưa truy vết tới UC hoặc SUPL | Tất cả FEAT không truy vết tới bất kỳ UC hoặc SUPL nào | Tính năng chưa có yêu cầu triển khai cụ thể |
| FEAT không được truy vết từ STRQ | Tất cả FEAT không được truy vết ngược từ bất kỳ STRQ nào | Tính năng thiếu căn cứ nhu cầu từ bên liên quan |
| UC không được truy vết từ FEAT | Tất cả UC không được truy vết ngược từ bất kỳ FEAT nào | Ca sử dụng thiếu căn cứ tính năng |
| SUPL không được truy vết từ FEAT | Tất cả SUPL không được truy vết ngược từ bất kỳ FEAT nào | Yêu cầu bổ sung thiếu căn cứ tính năng |
| UC chưa truy vết tới Design | Tất cả UC chưa có artefact thiết kế tương ứng trong baseline thiết kế | Ca sử dụng chưa được phản ánh vào thiết kế |
| UC chưa truy vết tới TC | Tất cả UC chưa có TC/bộ kiểm thử tương ứng | Ca sử dụng chưa được kiểm thử xác minh |
| SUPL chưa truy vết tới TC | Tất cả SUPL chưa có TC, acceptance check hoặc độ đo xác minh | Yêu cầu bổ sung chưa có cơ chế kiểm chứng |

### 1.9.4. Cây truy vết (Traceability Trees)

Cung cấp chế độ xem phân cấp toàn bộ chuỗi truy vết:

| Cây truy vết | Hướng | Mô tả |
| --- | --- | --- |
| Cây truy vết từ STRQ | Từ trên xuống (top-down) | STRQ → FEAT → UC/SUPL: Từ nhu cầu bên liên quan xuống tính năng, rồi tới ca sử dụng và yêu cầu bổ sung |
| Cây truy vết tới UC | Từ dưới lên (bottom-up) | UC → FEAT → STRQ: Từ ca sử dụng ngược lên tính năng, rồi tới nhu cầu bên liên quan |
| Cây truy vết tới SUPL | Từ dưới lên (bottom-up) | SUPL → FEAT → STRQ: Từ yêu cầu bổ sung ngược lên tính năng, rồi tới nhu cầu bên liên quan |
| Cây truy vết tới Design | Từ trên xuống / dưới lên | STRQ → FEAT → UC → Design và Design → UC → FEAT → STRQ: Dùng để kiểm tra độ bao phủ thiết kế từ yêu cầu và truy nguyên ngược artefact thiết kế |
| Cây truy vết tới TC | Từ trên xuống / dưới lên | STRQ → FEAT → UC/SUPL → TC và TC → UC/SUPL → FEAT → STRQ: Dùng để kiểm tra độ bao phủ kiểm thử |

### 1.9.5. Báo cáo bao phủ thiết kế và kiểm thử

Ngoài các ma trận truy vết chuẩn, dự án duy trì các báo cáo chuyên biệt sau để theo dõi đoạn cuối của chuỗi truy vết **STRQ → FEAT → UC → Design/Test**:

| Báo cáo | Phạm vi | Mục đích |
| --- | --- | --- |
| Báo cáo bao phủ UC → Design | Tất cả UC so với `class-diagram.md` và các artefact thiết kế liên quan | Xác định UC nào chưa được phản ánh vào thiết kế hoặc thiết kế nào chưa có UC nguồn |
| Báo cáo bao phủ UC → Test | Tất cả UC so với TC/bộ kiểm thử chức năng | Xác định UC nào chưa có kiểm thử xác minh |
| Báo cáo bao phủ SUPL → Test | Tất cả SUPL so với TC phi chức năng, acceptance check và độ đo trong `supplementary-metrics.md` | Xác định SUPL nào chưa có cơ chế xác minh |

### 1.9.6. Báo cáo tổng hợp baseline yêu cầu (Baseline Counts Summary)

Báo cáo này được tạo tại thời điểm chốt baseline và sau mỗi CR lớn để kiểm tra nhanh quy mô bộ yêu cầu:

| Kiểu / Artefact | Số lượng baseline | Nguồn đối soát |
| --- | ---: | --- |
| STRQ | 12 | `stakeholder-interviews.md` |
| FEAT | 53 | `stakeholder-interviews.md` |
| UC | 48 | `requirement-modeling.md` và các file `uc*.md` |
| SUPL | n | `supplementary-requirements.md` |
| Design artefacts chính | Theo baseline thiết kế hiện hành | `class-diagram.md` |
| Test artefacts / TC | Theo iteration và baseline kiểm thử hiện hành | Tài liệu/bảng kiểm thử được tạo theo iteration |

# II. PHỎNG VẤN BÊN LIÊN QUAN

## 2.1. Bảng phân công thành viên

| Thành viên | STRQs | FEATs |
|---|---|---|
| Nguyễn Hồng Phúc | 1–3 | 1.1–3.5 (15) |
| Ngô Đức Nam Khánh | 4–6 | 4.1–6.2 (11) |
| Nguyễn Hải Ninh | 7–8 | 7.1–8.9 (13) |
| Ngô Quang Tùng | 9–12 | 9.1–12.4 (14) |

## 2.2. Nội dung tổng hợp STRQ và FEAT theo thành viên

### 2.2.1. Phần đóng góp của Nguyễn Hồng Phúc (STRQ 1–3)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | * Phân tách * Làm cho đầy đủ * Tổng quát hóa * Thêm chi tiết | * **FEAT 1.1:** Hệ thống cho phép người dùng đăng nhập bằng tài khoản. * **FEAT 1.2:** Hệ thống cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng. * **FEAT 1.3:** Hệ thống tự động đăng xuất khỏi phiên làm việc nếu người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web trong 30 phút. * **FEAT 1.4:** Hệ thống cho phép người dùng đổi mật khẩu tài khoản đang sử dụng. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 2.1:** Hệ thống cho phép quản trị viên tìm kiếm tài khoản người dùng. * **FEAT 2.2:** Hệ thống cho phép quản trị viên thêm mới tài khoản người dùng. * **FEAT 2.3:** Hệ thống cho phép quản trị viên sửa tài khoản người dùng. * **FEAT 2.4:** Hệ thống cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống tương ứng với các nhóm nghiệp vụ. * **FEAT 2.5:** Hệ thống cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Khóa/Mở khóa). * **FEAT 2.6:** Hệ thống tự động khóa tài khoản của nhân sự đã được đánh dấu thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 3.1:** Hệ thống cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi. * **FEAT 3.2:** Hệ thống cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự. * **FEAT 3.3:** Hệ thống cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự. * **FEAT 3.4:** Hệ thống cho phép quản trị viên và phòng TCCB thay đổi trạng thái của đơn vị tổ chức nhân sự (Trạng thái: Giải thể/Sáp nhập). * **FEAT 3.5:** Hệ thống cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. |

> **Ghi chú thiết kế – FEAT 2.4:** "Nhóm nghiệp vụ" trong FEAT 2.4 chỉ các vai trò chức năng được hệ thống định nghĩa sẵn, tương ứng với phân nhóm tác nhân: Quản trị viên, Phòng TCCB, Phòng TCKT, Người dùng (Cán bộ/Giảng viên/Nhân viên). Mỗi nhóm nghiệp vụ quy định tập quyền truy cập các chức năng hệ thống khác nhau.

### 2.2.2. Phần đóng góp của Ngô Đức Nam Khánh (STRQ 4–6)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 4:** Phòng TCCB có thể cấu hình lương, loại phụ cấp, loại hợp đồng. | * Phân tách * Làm cho đầy đủ | * **FEAT 4.1:** Hệ thống cho phép phòng TCCB thêm mới hệ số lương (Hệ số lương được thêm sẽ được dùng làm thông tin cho hồ sơ). * **FEAT 4.2:** Hệ thống cho phép phòng TCCB sửa thông tin đối với hệ số lương chưa được hồ sơ nào sử dụng, phục vụ sửa chữa nhập liệu lỗi. * **FEAT 4.3:** Hệ thống cho phép phòng TCCB xóa hệ số lương khi không được hồ sơ nào sử dụng, hoặc thay đổi trạng thái (đưa vào trạng thái ngừng sử dụng hoặc kích hoạt lại) nếu đã được sử dụng. * **FEAT 4.4:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại phụ cấp. * **FEAT 4.5:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại hợp đồng. |

> **Ghi chú thiết kế – FEAT 4.4/4.5:** Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ thao tác "Thay đổi trạng thái" (chuyển đổi giữa "Đang sử dụng" và "Ngừng sử dụng") mà không hỗ trợ "Xóa" (khác với hệ số lương ở FEAT 4.3 có hỗ trợ xóa khi chưa được sử dụng). Thiết kế này nhằm đảm bảo tính toàn vẹn dữ liệu và phục vụ kiểm toán – các loại phụ cấp/hợp đồng đã từng được sử dụng trong hệ thống cần được lưu giữ lịch sử.

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 5:** Phòng TCKT và TCCB muốn thống kê chi tiết về nhân sự. | * Phân tách * Thêm chi tiết | * **FEAT 5.1:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê tổng quan nhân sự và biến động nhân sự. * **FEAT 5.2:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh. * **FEAT 5.3:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê hợp đồng, tình trạng làm việc, đánh giá cán bộ. * **FEAT 5.4:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê đào tạo, phát triển, bổ nhiệm nhân sự. |
| **STRQ 6:** Hệ thống yêu cầu tự động log dấu vết hoạt động người dùng (System Logging). | * Phân tách * Thêm chi tiết | * **FEAT 6.1:** Hệ thống tự động ghi vết tất cả các tác vụ truy cập tài khoản, thay đổi/cập nhật hệ thống hoặc dữ liệu. * **FEAT 6.2:** Hệ thống cho phép quản trị viên truy xuất xem và xuất Audit log (Nhật ký hệ thống) nhằm truy vết hoạt động. |

### 2.2.3. Phần đóng góp của Nguyễn Hải Ninh (STRQ 7–8)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 7:** Phòng TCCB có thể tạo hợp đồng lao động của nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 7.1:** Hệ thống cho phép phòng TCCB tạo hợp đồng cho nhân sự không có hợp đồng hoặc cần gia hạn hợp đồng. * **FEAT 7.2:** Hệ thống cho phép phòng TCCB xem danh sách và chi tiết hợp đồng lao động của nhân sự. * **FEAT 7.3:** Hệ thống cho phép phòng TCCB chỉnh sửa hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực. * **FEAT 7.4:** Hệ thống cho phép phòng TCCB chấm dứt hợp đồng lao động trước hạn của nhân sự. |
| **STRQ 8:** Phòng TCCB muốn quản lý hồ sơ nhân sự như thêm, sửa hồ sơ và cho phép đánh dấu thôi việc nếu nhân sự không còn làm việc, có thêm phương pháp tìm kiếm và lọc để tiện quản lý. | * Phân tách * Làm rõ * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 8.1:** Hệ thống cho phép phòng TCCB và phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa. * **FEAT 8.2:** Hệ thống cho phép phòng TCCB và phòng TCKT lọc đa tiêu chí hồ sơ nhân sự. * **FEAT 8.3:** Hệ thống cho phép phòng TCCB thêm mới hồ sơ nhân sự (gồm nhập tay hoặc upload từ Excel). * **FEAT 8.4:** Hệ thống cho phép phòng TCCB chỉnh sửa hồ sơ nhân sự (thông tin cá nhân, trình độ học vấn, khen thưởng/kỷ luật, quá trình công tác, thông tin hợp đồng). * **FEAT 8.5:** Hệ thống cho phép phòng TCCB đánh dấu thôi việc nhân sự. * **FEAT 8.6:** Hệ thống tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. * **FEAT 8.7:** Hệ thống cho phép phòng TCCB và phòng TCKT xem chi tiết hồ sơ nhân sự theo từng chế độ xem. * **FEAT 8.8:** Hệ thống cho phép phòng TCCB và phòng TCKT in hoặc xuất Excel hồ sơ nhân sự. * **FEAT 8.9:** Hệ thống cho phép phòng TCCB cấu hình ẩn/hiện các mục khen thưởng, kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc phòng TCCB. |

### 2.2.4. Phần đóng góp của Ngô Quang Tùng (STRQ 9–12)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 9:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 9.1:** Hệ thống cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự. * **FEAT 9.2:** Hệ thống cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác. * **FEAT 9.3:** Hệ thống cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 10:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 10.1:** Hệ thống cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật). * **FEAT 10.2:** Hệ thống cho phép phòng TCCB xem lịch sử đánh giá khen thưởng và kỷ luật của nhân sự. * **FEAT 10.3:** Hệ thống cho phép phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo nhân sự, loại đánh giá, hoặc khoảng thời gian. |
| **STRQ 11:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 11.1:** Hệ thống cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ. * **FEAT 11.2:** Hệ thống cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành). * **FEAT 11.3:** Hệ thống cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký. * **FEAT 11.4:** Hệ thống cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
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

> **Ghi chú:** Tổng cộng hệ thống bao gồm **48 Use Case** (UC 4.1 – UC 4.48), được phân nhóm theo chức năng như sau:

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
* UC Xem Chi tiết thông tin hồ sơ nhân sự / In hồ sơ / Xuất Excel
* UC Đánh dấu thôi việc nhân sự
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
| Ngô Đức Nam Khánh | 4.13–4.24 (12) |
| Nguyễn Hải Ninh | 4.25–4.35 (11) |
| Ngô Quang Tùng | 4.36–4.48 (13) |

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
- UC 4.34: Xem Chi tiết thông tin hồ sơ nhân sự
- UC 4.35: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật
- UC 4.36: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự
- UC 4.37: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự
- UC 4.38: Ghi nhận đánh giá cho nhân sự
- UC 4.39: Xem lịch sử đánh giá khen thưởng/kỷ luật
- UC 4.40: Tìm kiếm và lọc danh sách đánh giá
- UC 4.41: Mở khóa đào tạo cho cán bộ giảng viên
- UC 4.42: Sửa thông tin khóa đào tạo đã mở
- UC 4.43: Xem chi tiết thông tin khóa đào tạo đã mở
- UC 4.44: Ghi nhận kết quả đào tạo của cán bộ giảng viên
- UC 4.45: Xem các thông tin trong hồ sơ cá nhân của nhân sự
- UC 4.46: Xem thông tin chi tiết đơn vị đang công tác
- UC 4.47: Thay đổi trạng thái đăng ký khóa đào tạo
- UC 4.48: Xem danh sách các khóa đào tạo đã đăng ký

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

## 4.2 Phần đóng góp của Ngô Đức Nam Khánh (UC 4.13–4.24)

### 4.13. Use Case: Thêm mới danh mục hệ số lương (Ngô Đức Nam Khánh)

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

### 4.15. Use Case: Xóa danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Xóa danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB xóa hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu như nhập liệu sai sót trong trường hợp hệ số lương chưa từng được sử dụng trong hồ sơ nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Xóa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục hệ số lương cần xóa đã tồn tại trong hệ thống.  Danh mục hệ số lương chưa được sử dụng trong bất kỳ hồ sơ nhân sự nào. |
| Điều kiện thành công  (Post-condition) | Danh mục hệ số lương được xóa hoàn toàn khỏi hệ thống. |
| Điều kiện thất bại | Danh mục hệ số lương không được xóa. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục hệ số lương trong danh sách.  2. Phòng TCCB chọn chức năng “Xóa”.  3. Hệ thống hiển thị hộp thoại xác nhận xóa.  4. Phòng TCCB xác nhận thao tác xóa.  5. Hệ thống kiểm tra điều kiện sử dụng của hệ số lương.  6. Hệ thống xóa danh mục hệ số lương thành công.  7. Hệ thống lưu lịch sử thay đổi và thông báo xóa thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Danh mục hệ số lương đã được sử dụng**   1. Tại bước 5, hệ thống phát hiện hệ số lương đã được gán cho ít nhất một hồ sơ nhân sự. 2. Hệ thống thông báo không thể xóa danh mục đã được sử dụng 3. Dữ liệu không bị xóa.   **E2: Hủy thao tác xóa**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

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

## 4.3 Phần đóng góp của Nguyễn Hải Ninh (UC 4.25–4.35)

### 4.25. Use Case: Thêm mới Hợp đồng lao động

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Tạo mới hợp đồng với quản lý trạng thái và ràng buộc nghiệp vụ. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Thêm mới hợp đồng”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã được tạo |
| Điều kiện thành công  (Post-condition) | Hợp đồng lao động mới được tạo và gắn với hồ sơ nhân sự.  Trạng thái hợp đồng của nhân sự được cập nhật theo hợp đồng mới nhất. |
| Điều kiện thất bại | Hợp đồng không được tạo do vi phạm ràng buộc nghiệp vụ hoặc lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB chọn mục “Thêm mới hợp đồng”.  2. Hệ thống yêu cầu nhập mã nhân sự  3. Phòng TCCB nhập Mã nhân sự.  4.  Hệ thống kiểm tra: Mã nhân sự có tồn tại không và nếu tồn tại chỉ cho phép tạo hợp đồng mới nếu nhân viên có trạng thái hợp đồng "Chưa hợp đồng" hoặc “Chờ gia hạn” hoặc “Còn hiệu lực” với thời gian còn lại nằm trong thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20).  5.  Chọn `Loại hợp đồng`.  6.  Hệ thống kiểm tra số lần ký tối đa cho loại hợp đồng.  7.  Nhập thông tin hợp đồng:Số HĐ   * Ngày ký * Ngày hiệu lực * Ngày hết hạn * Đơn vị công tác theo hợp đồng * Nội dung hợp đồng (rich text editor - nhập điều khoản, mô tả công việc, quyền lợi...) * Upload PDF bản hợp đồng giấy (tải lên bản scan/file gốc đã ký)   8.  Hệ thống validate thời hạn Thời gian tối thiểu/ Thời gian tối đa của loại hợp đồng.  9.  Nhấn "Lưu".  10. Hệ thống cập nhật hợp đồng mới với trạng thái mặc định 'Còn hiệu lực', đồng thời cập nhật trạng thái hợp đồng của nhân sự thành 'Còn hiệu lực'.  11. Hệ thống lưu hợp đồng vào hồ sơ cá nhân và thông báo thành công. *Lưu ý: Xem UC 4.26 (Xem hợp đồng), UC 4.27 (Sửa hợp đồng lao động) và UC 4.28 (Chấm dứt hợp đồng lao động trước hạn) cho các tác vụ liên quan.* |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không đủ điều kiện tạo hợp đồng mới do hợp đồng hiện tại còn hiệu lực**   1. Tại bước 4, hệ thống phát hiện nhân sự không tồn tại hoặc nhân sự đang có hợp đồng ở trạng thái “Còn hiệu lực” và thời gian còn lại > thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20). 2. Hệ thống từ chối tạo hợp đồng mới. 3. Hệ thống hiển thị thông báo: *“Không thể tạo hợp đồng mới”*   **E2: Vượt quá số lần ký hợp đồng cho phép**   1. Tại bước 5, hệ thống kiểm tra số lần ký hợp đồng theo loại hợp đồng đã chọn của nhân sự. 2. Hệ thống không cho phép tiếp tục tạo hợp đồng. 3. Hiển thị thông báo: *“Vui lòng chọn loại hợp đồng khác.”*   **E3: Thời gian hợp đồng không hợp lệ hoặc trùng lặp**   1. Tại bước 8, hệ thống phát hiện: Thời hạn hợp đồng không nằm trong khoảng Min/Max theo quy định hoặc ngày hiệu lực của hợp đồng mới ≤ ngày hết hạn của hợp đồng cũ chưa chấm dứt. Các trường dữ liệu chưa đầy đủ 2. Hệ thống hiển thị thông báo: “Thời gian hợp đồng không hợp lệ hoặc bị trùng với hợp đồng trước” 3. Phòng TCCB quay lại bước 5   **E4: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. |

### 4.26. Use Case: Xem danh sách và chi tiết hợp đồng lao động (FEAT 7.2)

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách và chi tiết hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem danh sách toàn bộ hợp đồng lao động đã gắn với một hồ sơ nhân sự và xem chi tiết từng hợp đồng nhằm phục vụ tra cứu, đối chiếu và quản lý thông tin hợp đồng của nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn tab “Hợp đồng” trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách hợp đồng và thông tin chi tiết của hợp đồng được hiển thị đầy đủ, chính xác theo dữ liệu đã lưu.  Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin hợp đồng do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.34).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **“Hợp đồng”**.  4. Hệ thống hiển thị danh sách tất cả hợp đồng lao động của nhân sự, bao gồm các thông tin: Số hợp đồng, Loại hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Trạng thái hợp đồng.  5. Phòng TCCB chọn một hợp đồng trong danh sách.  6. Hệ thống hiển thị chi tiết hợp đồng đã chọn, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, Thông tin lương/quyền lợi theo hợp đồng (nếu có), File PDF đính kèm và Trạng thái hợp đồng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Nhân sự chưa có hợp đồng lao động**   1. Tại bước 3, nếu hồ sơ nhân sự chưa có hợp đồng nào được lưu. 2. Hệ thống hiển thị tab **“Hợp đồng”** ở trạng thái trống và thông báo: *“Nhân sự chưa có hợp đồng lao động.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.27. Use Case: Chỉnh sửa hợp đồng lao động chưa có hiệu lực (FEAT 7.3)

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa hợp đồng lao động chưa có hiệu lực** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa thông tin hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực, nhằm sửa sai sót nhập liệu hoặc cập nhật nội dung trước thời điểm hợp đồng bắt đầu áp dụng, đồng thời bảo đảm toàn vẹn dữ liệu hợp đồng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Sửa hợp đồng” tại màn hình chi tiết hợp đồng của nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hợp đồng lao động của nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin hợp đồng được cập nhật thành công.  Lịch sử thay đổi hợp đồng được ghi nhận. |
| Điều kiện thất bại | Hợp đồng không được cập nhật do vi phạm ràng buộc nghiệp vụ, dữ liệu không hợp lệ hoặc hợp đồng không thuộc trạng thái cho phép chỉnh sửa. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động của nhân sự từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Nếu hợp đồng đang ở trạng thái **“Chưa có hiệu lực”**, hệ thống hiển thị nút **“Sửa hợp đồng”**.  4. Phòng TCCB chọn **“Sửa hợp đồng”**.  5. Hệ thống hiển thị màn hình chỉnh sửa và cho phép cập nhật các thông tin của hợp đồng, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, File PDF đính kèm.  6. Phòng TCCB chỉnh sửa thông tin và nhấn **“Lưu”**.  7. Hệ thống kiểm tra dữ liệu hợp lệ và kiểm tra ràng buộc nghiệp vụ: hợp đồng vẫn phải ở trạng thái **“Chưa có hiệu lực”**, thời gian hợp đồng hợp lệ, không trùng lặp với các hợp đồng khác của cùng nhân sự.  8. Hệ thống cập nhật thông tin hợp đồng, lưu lịch sử thay đổi và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hợp đồng đã có hiệu lực hoặc đã hết hiệu lực**   1. Tại bước 3, nếu hợp đồng không ở trạng thái **“Chưa có hiệu lực”**. 2. Hệ thống ẩn hoặc vô hiệu hóa nút **“Sửa hợp đồng”** và hiển thị thông báo: *“Chỉ được chỉnh sửa hợp đồng chưa có hiệu lực.”*   **A2: Dữ liệu chỉnh sửa không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu thông tin bắt buộc, thời gian hợp đồng không hợp lệ hoặc dữ liệu bị trùng lặp. 2. Hệ thống hiển thị cảnh báo và yêu cầu Phòng TCCB chỉnh sửa lại thông tin. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.28. Use Case: Chấm dứt hợp đồng lao động trước hạn (FEAT 7.4)

|  |  |
| --- | --- |
| **Tên use case** | **Chấm dứt hợp đồng lao động trước hạn** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chấm dứt trước hạn một hợp đồng lao động đang còn hiệu lực của nhân sự, cập nhật lại trạng thái hợp đồng và hỗ trợ xem xét nghiệp vụ thôi việc khi nhân sự không còn hợp đồng còn hiệu lực nào. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Chấm dứt trước hạn” tại màn hình chi tiết hợp đồng. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hợp đồng lao động cần chấm dứt đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Hợp đồng được cập nhật trạng thái **“Hết hiệu lực”** kèm thông tin ngày chấm dứt và lý do chấm dứt trước hạn.  Trạng thái hợp đồng hiện tại của nhân sự được cập nhật tương ứng. |
| Điều kiện thất bại | Không thể chấm dứt hợp đồng trước hạn do hợp đồng không ở trạng thái cho phép, dữ liệu không hợp lệ hoặc người dùng không xác nhận thao tác. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Phòng TCCB chọn một hợp đồng đang ở trạng thái **“Còn hiệu lực”** và nhấn **“Chấm dứt trước hạn”**.  4. Hệ thống hiển thị biểu mẫu yêu cầu nhập **Ngày chấm dứt trước hạn** và **Lý do chấm dứt**.  5. Phòng TCCB nhập thông tin và nhấn xác nhận.  6. Hệ thống hiển thị hộp thoại xác nhận thao tác chấm dứt trước hạn.  7. Phòng TCCB xác nhận thao tác.  8. Hệ thống cập nhật hợp đồng sang trạng thái **“Hết hiệu lực”**, lưu ngày chấm dứt và lý do chấm dứt trước hạn.  9. Hệ thống cập nhật trạng thái hợp đồng hiện tại của nhân sự theo dữ liệu mới.  10. Nếu đây là hợp đồng còn hiệu lực duy nhất của nhân sự, hệ thống hiển thị thông báo để Phòng TCCB xem xét tiếp tục thực hiện UC 4.33 **“Đánh dấu thôi việc nhân sự”** nếu phù hợp nghiệp vụ. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hủy thao tác chấm dứt trước hạn**   1. Tại bước 6, Phòng TCCB chọn **“Hủy”**. 2. Hệ thống đóng hộp thoại xác nhận và không cập nhật dữ liệu hợp đồng.   **A2: Hợp đồng không ở trạng thái còn hiệu lực**   1. Tại bước 3, nếu hợp đồng không ở trạng thái **“Còn hiệu lực”**. 2. Hệ thống không cho phép thực hiện chức năng **“Chấm dứt trước hạn”** và hiển thị thông báo phù hợp. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.29. Use Case: Tìm kiếm hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích  (mô tả) | Cho phép cán bộ Phòng TCCB, phòng TCKT tìm kiếm hồ sơ nhân sự nhanh chóng dựa trên từ khóa như tên, mã nhân sự, số CCCD, email hoặc số điện thoại nhằm phục vụ công tác quản lý và tra cứu thông tin. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng nhập từ khóa tìm kiếm và thực hiện tìm kiếm trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách nhân sự thỏa mãn điều kiện được hiển thị |
| Điều kiện thất bại | Hệ thống không xử lý yêu cầu tìm kiếm |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB, phòng TCKT chọn menu "Quản lý Hồ sơ".  2.  Hệ thống hiển thị danh sách hồ sơ nhân viên (Mã, Họ tên, CCCD, Giới tính, Địa chỉ, SĐT liên hệ, Chức danh khoa học, Đơn vị công tác, Chức vụ đơn vị, Trạng thái công việc, Trạng thái hợp đồng) có phân trang.  3.  Phòng TCCB, phòng TCKT **nhập từ khóa** vào ô tìm kiếm (Tên, Mã, CCCD, SĐT).  4.  Hệ thống hiển thị kết quả tìm kiếm theo từ khóa (real-time). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Từ khóa tìm kiếm rỗng**   1. Tại bước 3, nếu phòng TCCB, phòng TCKT không nhập từ khóa 2. Hệ thống hiển thị toàn bộ danh sách hồ sơ nhân sự |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không có kết quả tìm kiếm**   1. Tại bước 4, nếu không có hồ sơ nào phù hợp với từ khóa 2. Hệ thống hiển thị thông báo: *“Không tìm thấy hồ sơ phù hợp.”* |

### 4.30. Use Case: Lọc danh sách hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Lọc danh sách hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT lọc danh sách hồ sơ nhân sự dựa trên nhiều tiêu chí nhằm thu hẹp phạm vi dữ liệu phục vụ công tác quản lý. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB, phòng TCKT chọn tiêu chí lọc trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách hồ sơ nhân sự được hiển thị đúng theo các tiêu chí lọc đã chọn |
| Điều kiện thất bại | Hệ thống không hiển thị yêu cầu lọc danh sách theo tiêu chí đã chọn do lỗi hệ thống |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB, phòng TCKT nhấn "Bộ lọc nâng cao".  2.  Hệ thống hiển thị panel lọc với nhiều tiêu chí:   * **Đơn vị công tác:** Chọn Khoa, Phòng, Ban, Bộ môn * **Chức danh khoa học:** GS, PGS, Không có * **Chức vụ đơn vị:**Trưởng khoa, Phó khoa, Không chức vụ * **Trạng thái làm việc:** Đang chờ xét,Đang công tác, Đã thôi việc * **Trạng thái hợp đồng:** Chưa hợp đồng, Còn hiệu lực, Hết hiệu lực, Chờ gia hạn. * **Giới tính:** Nam, Nữ   3.  Phòng TCCB, phòng TCKT chọn các tiêu chí lọc.  4.  Nhấn "Áp dụng bộ lọc".  5.  Hệ thống hiển thị kết quả lọc đa tiêu chí. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không có kết quả lọc**   1. Tại bước 5, nếu không có hồ sơ nào thỏa mãn tiêu chí đã chọn 2. Hệ thống hiển thị thông báo *“Không có hồ sơ phù hợp với tiêu chí lọc.”* |

### 4.31. Use Case: Thêm mới Hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tạo mới và lưu trữ đầy đủ thông tin hồ sơ nhân sự trên hệ thống. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng thêm trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được tạo mới |
| Điều kiện thất bại | Hệ thống không thể tạo mới hồ sơ do lỗi hệ thống hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB nhấn "Thêm mới".  2.  Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3.  Phòng TCCB nhập các trường thông tin:   * **Thông tin chung bắt buộc**: Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ. * **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn "Người nước ngoài", hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động. * **Thông tin gia đình  (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình. * **Thông tin ngân hàng  (bắt buộc)**: Tên Ngân hàng, Số tài khoản. * **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**. * **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết. * **Upload ảnh chân dung  (bắt buộc).** * **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học. * **Thông tin các bằng cấp  (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf. * **Thông tin các chứng chỉ  (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf. * **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình).   4. Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5. Phòng TCCB nhấn "Lưu".  6. Hệ thống tự động sinh Mã cán bộ và Trạng thái hợp đồng mặc định là “Chưa hợp đồng”, Trạng thái làm việc là “Đang chờ xét”.  7. Hệ thống lưu hồ sơ, lịch sử tạo hồ sơ và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Tạo mới hồ sơ nhân sự từ file Excel**  1. Tại bước 1 của Luồng sự kiện chính, Phòng TCCB chọn chức năng **“Thêm mới từ Excel”**.  2. Hệ thống hiển thị màn hình tải lên file Excel và cung cấp **file mẫu** theo định dạng quy định.  3. Phòng TCCB tải lên file Excel chứa danh sách hồ sơ nhân sự.  4. Hệ thống kiểm tra: Định dạng file, Cấu trúc cột dữ liệu, Các trường thông tin bắt buộc, và tính hợp lệ logic của dữ liệu từng dòng  5. Tiếp tục bước 5 của luồng chính |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**   1. Tại bước 4, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ. 2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ.   **E2: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. |

### 4.32. Use Case: Chỉnh sửa trong chi tiết hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa trong chi tiết hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB sửa và lưu lại đầy đủ thông tin hồ sơ nhân sự trên hệ thống nếu có thay đổi hoặc sai sót trong nhập liệu. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng sửa trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự có trạng thái làm việc “Đang chờ xét”, “Đang công tác” |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được cập nhật.  Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Hồ sơ nhân sự không được cập nhật và thay đổi |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB nhấn "Sửa" một nhân sự tại danh sách.  2.  Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3.  Phòng TCCB có thể sửa các trường thông tin:   * **Thông tin chung bắt buộc**: Mã cán bộ (không thể sửa), Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ. * **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn "Người nước ngoài", hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động. * **Thông tin gia đình  (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình. * **Thông tin ngân hàng  (bắt buộc)**: Tên Ngân hàng, Số tài khoản. * **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**. * **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết. * **Upload ảnh chân dung  (bắt buộc).** * **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học. * **Thông tin các bằng cấp  (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf. * **Thông tin các chứng chỉ  (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf. * **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình). * *Lưu ý: Thông tin hợp đồng được quản lý qua UC 4.25 (Thêm mới Hợp đồng lao động), UC 4.26 (Xem hợp đồng), UC 4.27 (Sửa hợp đồng lao động), UC 4.28 (Chấm dứt hợp đồng lao động trước hạn). Thông tin đánh giá (khen thưởng/kỷ luật) được quản lý qua UC 4.38 (Ghi nhận đánh giá cho nhân sự), UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) và UC 4.40 (Tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật). Xem UC 4.35 (Cấu hình ẩn/hiện mục khen thưởng/kỷ luật) cho chức năng ẩn/hiện — tách ra từ FEAT 8.9.*   4. Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5. Cán bộ TCCB nhấn "Lưu".  6. Hệ thống lưu hồ sơ, lịch sử tạo hồ sơ và thông báo thành công |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**   1. Tại bước 5, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ. 2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ.   **E2: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự.   **E3: Hồ sơ ở trạng thái “Đã thôi việc”**   1. Tại bước 1, hệ thống phát hiện hồ sơ nhân sự đang ở trạng thái làm việc “Đã thôi việc”. 2. Hệ thống hiển thị thông báo: “Không thể chỉnh sửa hồ sơ nhân sự đã thôi việc.” và vô hiệu hóa nút “Sửa”. |

### 4.33. Use Case: Đánh dấu thôi việc nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Đánh dấu thôi việc nhân sự** |
| Tác nhân chính | Phòng TCCB, Hệ thống |
| Mục đích (mô tả) | Cho phép phòng TCCB cập nhật trạng thái làm việc “Đã thôi việc” cho hồ sơ nhân sự |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng đánh dấu thôi việc trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. Nhân sự cần đánh dấu thôi việc đang ở trạng thái làm việc khác “Đã thôi việc”. |
| Điều kiện thành công  (Post-condition) | Trạng thái của nhân sự được cập nhật thành “Đã thôi việc” trong hồ sơ nhân sự thành công.Trạng thái hợp đồng được cập nhật thành "Hết hiệu lực" (nếu nhân sự có hợp đồng ở trạng thái "Còn hiệu lực" hoặc "Chờ gia hạn"). Nhân sự được gỡ khỏi đơn vị công tác. Tài khoản liên kết được tự động khóa. |
| Điều kiện thất bại | Trạng thái làm việc “Đã thôi việc” không được cập nhật |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, phòng TCCB chọn chức năng "Đánh dấu thôi việc" một nhân sự.  2.  Hệ thống yêu cầu xác nhận và nhập ngày, lý do thôi việc.  3.  Phòng TCCB xác nhận.  4.  Hệ thống cập nhật trạng thái làm việc thành "Đã thôi việc", trạng thái hợp đồng thành “Hết hiệu lực” (nếu có hợp đồng đang hiệu lực hoặc chờ gia hạn), nhân sự được cập nhật rời khỏi đơn vị công tác.  5. Hệ thống tự động khóa tài khoản liên kết của nhân sự (cập nhật trạng thái tài khoản thành 'Bị khóa'). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Thôi việc nhân sự tự động**   1. Hệ thống tự động cập nhật trạng thái hợp đồng “Hết hiệu lực” cho loại hợp đồng ở trạng thái “Chờ gia hạn” khi đã quá thời gian gia hạn được cấu hình và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. 2. Hệ thống tự động cập nhật trạng thái làm việc cho nhân sự vừa bị cập nhật trạng thái hợp đồng “Hết hiệu lực” thành “Đã thôi việc”. 3. Hệ thống tự động gỡ nhân sự khỏi đơn vị công tác hiện tại. 4. Hệ thống tự động cập nhật trạng thái tài khoản liên kết thành "Bị khóa". **A2: Thôi việc khi hợp đồng còn hiệu lực (thanh lý trước hạn)**   1. Tại bước 1, hệ thống phát hiện nhân sự có hợp đồng ở trạng thái "Còn hiệu lực". 2. Hệ thống hiển thị cảnh báo: "Nhân sự này vẫn còn hợp đồng đang có hiệu lực. Tiếp tục sẽ thanh lý hợp đồng trước hạn." 3. Hệ thống yêu cầu nhập lý do thanh lý hợp đồng trước hạn (ngoài ngày và lý do thôi việc ở bước 2 Basic Flow). 4. Phòng TCCB xác nhận. 5. Tiếp tục bước 4 của Basic Flow. **A3: Tự động chuyển trạng thái hợp đồng sang “Chờ gia hạn”**   1. Hệ thống (System Timer) định kỳ kiểm tra các hợp đồng đang ở trạng thái “Còn hiệu lực”. 2. Nếu thời gian còn lại của hợp đồng ≤ thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20): 3. Hệ thống tự động cập nhật trạng thái hợp đồng từ “Còn hiệu lực” sang “Chờ gia hạn”. 4. Hệ thống tự động cập nhật trạng thái hợp đồng của nhân sự thành “Chờ gia hạn”. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Nhân sự đã ở trạng thái "Đã thôi việc"**   1. Tại bước 1, hệ thống phát hiện nhân sự đã có trạng thái làm việc "Đã thôi việc". 2. Hệ thống vô hiệu hóa nút "Đánh dấu thôi việc" hoặc hiển thị cảnh báo: *"Nhân sự này đã được đánh dấu thôi việc trước đó."*   **E2: Nhân sự chưa bãi nhiệm chức vụ**   1. Tại bước 1, hệ thống phát hiện nhân sự đang giữ chức vụ quản lý (Trưởng khoa, Trưởng bộ môn...). 2. Hệ thống chặn thao tác và thông báo: "Vui lòng bãi nhiệm chức vụ của nhân sự trước khi đánh dấu thôi việc."   **E3: Hủy thao tác**   1. Tại bước 2, Phòng TCCB chọn "Hủy". 2. Hệ thống quay lại màn hình danh sách nhân sự. |

### 4.34. Use Case: Xem Chi tiết thông tin hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem Chi tiết thông tin hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT xem chi tiết toàn bộ thông tin hồ sơ nhân sự, có thể thực hiện in hồ sơ |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB, phòng TCKT chọn chức năng xem chi tiết trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết hồ sơ nhân sự được hiển thị đầy đủ, chính xác ở chế độ chỉ đọc. |
| Điều kiện thất bại | Hệ thống không hiển thị được thông tin hồ sơ do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại danh sách, Phòng TCCB, phòng TCKT nhấn vào nhấn "Xem chi tiết" tại một nhân sự.  2.  Hệ thống hiển thị màn hình Chi tiết hồ sơ ở chế độ chỉ đọc.  3.  Hệ thống hiển thị đầy đủ thông tin theo các tab:   * **Tab "Thông tin chung":** Mã cán bộ,Lý lịch, liên hệ, gia đình, ảnh chân dung * **Tab "Trình độ & Chức danh":** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác. * **Tab "Thông tin Đảng/ Đoàn":** Thông tin Đảng/ Đoàn đã được lưu. * **Tab "Lương & Phụ cấp":** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng * **Tab "Hợp đồng":** Thông tin về các loại hợp đồng đồng đã ký * **Tab "Khen thưởng/Kỷ luật":** Hệ thống hiển thị mục khen thưởng/kỷ luật tùy theo cấu hình ẩn/hiện (xem UC 4.35, FEAT 8.9) và vai trò người dùng hiện tại * **Tab "Công tác":** Quá trình công tác trước khi về trường đã được ghi |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: In hồ sơ**   1. Tiếp tục bước 3, Phòng TCCB và TCKT có thể in ra hồ sơ ở định dạng PDF   **A2: Xuất ra Excel**   1. Tiếp tục bước 3, Phòng TCCB và TCKT có thể xuất ra file chứa tất cả thông tin dưới định dạng file Excel |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.35. Use Case: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật (FEAT 8.9)

|  |  |
| --- | --- |
| **Tên use case** | **Cấu hình ẩn/hiện mục khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB cấu hình ở mức toàn hệ thống việc ẩn/hiện các mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự đối với các vai trò không thuộc Phòng TCCB, nhằm kiểm soát phạm vi hiển thị thông tin theo vai trò sử dụng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng cấu hình hiển thị hồ sơ nhân sự trong menu cấu hình hệ thống. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống và có quyền cấu hình hệ thống. |
| Điều kiện thành công  (Post-condition) | Cấu hình ẩn/hiện mục **Khen thưởng/Kỷ luật** được lưu thành công và áp dụng ngay ở mức hệ thống cho các màn hình xem hồ sơ liên quan (tham chiếu UC 4.34 và UC 4.45).  Các vai trò được cấu hình là **“Ẩn”** sẽ không nhìn thấy mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự.  Phòng TCCB luôn nhìn thấy đầy đủ các mục này bất kể cấu hình. |
| Điều kiện thất bại | Cấu hình không được cập nhật do lỗi hệ thống hoặc người dùng không lưu thay đổi. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **cấu hình hệ thống**.  2. Hệ thống hiển thị danh sách nhóm cấu hình.  3. Phòng TCCB chọn nhóm cấu hình **“Hiển thị hồ sơ nhân sự”**.  4. Hệ thống hiển thị các vai trò không thuộc Phòng TCCB (ví dụ: Phòng TCKT, Cán bộ/Giảng viên/Người dùng) cùng các tùy chọn ẩn/hiện đối với mục **Khen thưởng** và **Kỷ luật**.  5. Phòng TCCB bật/tắt cấu hình hiển thị cho từng vai trò.  6. Phòng TCCB nhấn **“Lưu”**.  7. Hệ thống lưu cấu hình, thông báo thành công và áp dụng ngay cho các màn hình xem hồ sơ nhân sự tương ứng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không thay đổi cấu hình**   1. Tại bước 5, Phòng TCCB không thực hiện thay đổi nào và chọn **“Hủy”** hoặc thoát màn hình. 2. Hệ thống không cập nhật cấu hình và giữ nguyên thiết lập hiện tại. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

## 4.4 Phần đóng góp của Ngô Quang Tùng (UC 4.36–4.48)

### 4.36. Use Case: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB bổ nhiệm nhân sự vào các đơn vị tổ chức |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng bổ nhiệm trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức.  Nhân sự phải có trạng thái hợp đồng 'Còn hiệu lực' hoặc 'Chờ gia hạn' và trạng thái làm việc 'Đang chờ xét' hoặc 'Đang công tác'. |
| Điều kiện thành công  (Post-condition) | Nhân sự được bổ nhiệm nhân sự vào đơn vị.  Thông tin nhân sự của đơn vị được cập nhật. |
| Điều kiện thất bại | Việc bổ nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Phòng TCCB chọn bổ nhiệm nhân sự chưa công tác  3. Hệ thống hiển thị danh sách nhân sự ở trạng thái “Đang chờ xét” và trạng thái hợp đồng “Còn hiệu lực”.  4. Phòng TCCB chọn nhân sự và nhập thông tin như (Chức vụ, Ngày bắt đầu)  5. Hệ thống kiểm tra hợp lệ (Ngày bắt đầu).  6. Hệ thống thay đổi danh sách nhân sự, trạng thái công việc của nhân sự chuyển thành “Đang công tác ”và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Bổ nhiệm nhân sự đang công tác ở đơn vị khác**  1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Phòng TCCB chọn bổ nhiệm nhân sự đang công tác tại đơn vị khác.  3. Hệ thống yêu cầu chọn đơn vị, chọn nhân sự từ đơn vị được chọn.  4. Phòng TCCB chọn nhân sự và nhập thông tin như (Chức vụ, Ngày bắt đầu)  5. Hệ thống kiểm tra hợp lệ (Ngày bắt đầu).  6. Hệ thống gỡ nhân sự khỏi đơn vị cũ, thêm vào đơn vị mới, cập nhật danh sách nhân sự của cả hai đơn vị và thông báo thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ**   1. Tại bước 5, Hệ thống kiểm tra phát hiện:  * Ngày bắt đầu < ngày hiện tại  2. Hệ thống yêu cầu nhập lại và không lưu dữ liệu.   **E2: Không được phép tiếp tục**   1. Tại bước 1, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục cập nhật bổ nhiệm. |

### 4.37. Use Case: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự

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
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Hệ thống hiển thị danh sách nhân sự  3. Phòng TCCB chọn chức năng bãi nhiệm từ trong một nhân sự trong danh sách.  4. Hệ thống yêu cầu xác nhận thao tác.  5. Phòng TCCB xác nhận thao tác miễn nhiệm. 6. Hệ thống cập nhật trạng thái công việc của nhân sự là “Đang chờ xét”  và xóa nhân sự khỏi danh sách của đơn vị tổ chức. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không được phép tiếp tục**   1. Tại bước 3, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục thực hiện bãi nhiệm. |

### 4.38. Use Case: Ghi nhận đánh giá cho nhân sự

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
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn tab " Thêm đánh giá khen thưởng hoặc kỷ luật".  2. Hệ thống yêu cầu nhập mã nhân sự và chọn loại đánh giá  3. Phòng TCCB nhập mã nhân sự và chọn loại đánh giá (Khen thưởng/ Kỷ luật)  4.  Hệ thống hiển thị giao diện nhập liệu:   * Nếu chọn loại đánh giá là khen thưởng: `Loại khen thưởng`, ‘Tên khen thưởng’, `Ngày quyết định`, `Số quyết định`, `Nội dung`, `Số tiền thưởng` (nếu có). * Nếu chọn loại đánh giá là kỷ luật: `Loại kỷ luật`, ‘Tên kỷ luật’,  `Ngày quyết định`, `Lý do`, `Hình thức xử lý`.   5.  Nhấn "Lưu".  6. Hệ thống kiểm tra dữ liệu hợp lệ (Đầy đủ các trường thông tin)  7. Hệ thống lưu dữ liệu và đẩy vào hồ sơ cá nhân và thông báo thành công. *Lưu ý: Xem UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) và UC 4.40 (Tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật) cho các tác vụ tra cứu liên quan.* |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Mã nhân sự không hợp lệ**   1. Tại bước 3, Hệ thống phát hiện mã nhân sự không tồn tại. 2. Hệ thống từ chối tiếp tục tạo bản đánh giá.   **E2: Dữ liệu không hợp lệ**   1. Tại bước 6, Hệ thống phát hiện dữ liệu không đầy đủ các trường thông tin. 2. Hệ thống từ chối lưu thông tin và thông báo lỗi.   **E3: Hủy thao tác**  1. Tại bước 2, Phòng TCCB chọn “Hủy”.  2. Quay lại màn hình danh sách nhân sự. **E4: Nhân sự đã thôi việc**   1. Tại bước 3, hệ thống phát hiện nhân sự đang ở trạng thái làm việc “Đã thôi việc”. 2. Hệ thống từ chối ghi nhận đánh giá và hiển thị thông báo: “Không thể ghi nhận đánh giá cho nhân sự đã thôi việc.” |

### 4.39. Use Case: Xem lịch sử đánh giá khen thưởng/kỷ luật (FEAT 10.2)

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
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.34).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **“Khen thưởng/Kỷ luật”**.  4. Hệ thống hiển thị danh sách toàn bộ bản ghi đánh giá của nhân sự theo thứ tự thời gian, bao gồm các thông tin: Ngày quyết định, Loại đánh giá (Khen thưởng/Kỷ luật), Tên đánh giá, Số quyết định, Mô tả ngắn/Nội dung.  5. Phòng TCCB chọn một bản ghi đánh giá trong danh sách.  6. Hệ thống hiển thị chi tiết bản ghi đã chọn, bao gồm đầy đủ thông tin đã được ghi nhận từ UC 4.38. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Nhân sự chưa có lịch sử đánh giá**   1. Tại bước 3, nếu hồ sơ nhân sự chưa có bản ghi khen thưởng hoặc kỷ luật nào. 2. Hệ thống hiển thị tab **“Khen thưởng/Kỷ luật”** ở trạng thái trống và thông báo: *“Nhân sự chưa có lịch sử đánh giá khen thưởng/kỷ luật.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.40. Use Case: Tìm kiếm và lọc danh sách đánh giá (FEAT 10.3)

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
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chức năng **quản lý đánh giá khen thưởng/kỷ luật**.  2. Hệ thống hiển thị danh sách các bản ghi đánh giá và vùng bộ lọc tìm kiếm.  3. Phòng TCCB nhập từ khóa tìm kiếm và/hoặc chọn các tiêu chí lọc, bao gồm: Nhân sự (Mã cán bộ/Họ tên), Loại đánh giá (Khen thưởng/Kỷ luật), Khoảng thời gian (Từ ngày – Đến ngày).  4. Phòng TCCB nhấn **“Tìm kiếm”** hoặc **“Áp dụng bộ lọc”**.  5. Hệ thống hiển thị danh sách kết quả phù hợp với tiêu chí đã chọn, bao gồm các thông tin: Mã cán bộ, Họ tên, Loại đánh giá, Tên đánh giá, Ngày quyết định, Số quyết định.  6. Phòng TCCB có thể chọn một bản ghi bất kỳ trong danh sách kết quả.  7. Hệ thống hiển thị chi tiết bản ghi đánh giá đã chọn (tham chiếu UC 4.39). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không có kết quả phù hợp**   1. Tại bước 5, nếu không có bản ghi nào phù hợp với tiêu chí tìm kiếm/lọc. 2. Hệ thống hiển thị thông báo: *“Không tìm thấy đánh giá phù hợp với tiêu chí tìm kiếm.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.41. Use Case: Mở khóa đào tạo cho cán bộ giảng viên (Ngô Quang Tùng)

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

### 4.42. Use Case: Sửa thông tin khóa đào tạo đã mở

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
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo. 3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Sửa thông tin”**.  4. Hệ thống hiển thị màn hình chỉnh sửa thông tin khóa đào tạo.  5. Phòng TCCB chỉnh sửa các thông tin cho phép:   * Tên khóa đào tạo * Địa điểm * Kinh phí (nếu có) * Cam kết sau đào tạo (nếu có) * Thông tin chứng chỉ sau đào tạo * Trạng thái khóa đào tạo * Thời gian mở đăng ký và giới hạn số người tham gia (nếu được phép)   6. Phòng TCCB nhấn **“Lưu”**. 7. Hệ thống kiểm tra tính hợp lệ và ràng buộc nghiệp vụ (bao gồm kiểm tra chuyển trạng thái khóa đào tạo phải tuân theo thứ tự: Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước).  8. Hệ thống yêu cầu xác nhận cập nhật.  9. Phòng TCCB xác nhận.  10. Hệ thống cập nhật thông tin khóa đào tạo và thông báo thành công.  *Lưu ý: Khi trạng thái khóa đào tạo được chuyển sang "Đang đào tạo", hệ thống tự động batch-update tất cả đăng ký tham gia có trạng thái "Đã đăng ký" sang "Đang học".* |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Chỉnh sửa khi khóa đào tạo đang diễn ra**   1. Tại bước 4, nếu khóa đào tạo ở trạng thái "Đang đào tạo", hệ thống chỉ cho phép chỉnh sửa: Địa điểm, Kinh phí, Cam kết sau đào tạo, Thông tin chứng chỉ sau đào tạo. 2. Hệ thống khóa không cho phép chỉnh sửa: Tên khóa đào tạo, Loại khóa đào tạo, Thời gian mở đăng ký, Giới hạn số người tham gia. 3. Tiếp tục từ bước 6. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Chuyển trạng thái không hợp lệ**   1. Tại bước 7, hệ thống phát hiện trạng thái mới được chọn vi phạm thứ tự chuyển đổi (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước). 2. Hệ thống hiển thị thông báo: *"Chuyển trạng thái không hợp lệ."* và yêu cầu chọn lại.   **E2: Vi phạm ràng buộc đăng ký**   1. Tại bước 7, hệ thống phát hiện nếu: Giảm giới hạn số người tham gia nhỏ hơn số lượng đã đăng ký. 2. Hệ thống hiển thị cảnh báo và không cho phép lưu.   **E3: Dữ liệu không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu trường bắt buộc hoặc thời gian không hợp lệ. 2. Hệ thống yêu cầu chỉnh sửa lại thông tin.   **E4: Hủy thao tác**   1. Tại bước 5, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.43. Use Case: Xem chi tiết thông tin khóa đào tạo đã mở

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
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo.  3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Xem chi tiết”**.  4. Hệ thống hiển thị màn hình chi tiết khóa đào tạo, hiển thị đầy đủ thông tin theo yêu cầu bao gồm các thông tin:   * **Thông tin chung khóa đào tạo**: Tên khóa đào tạo, Loại khóa đào tạo, Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo. * **Thông tin đăng ký**: Thời gian mở đăng ký, Giới hạn số lượng người tham gia, Số lượng đã đăng ký / số lượng tối đa * **Danh sách tham gia**: Hệ thống hiển thị danh sách cán bộ, giảng viên đã đăng ký khóa đào tạo, bao gồm (Họ và tên, Mã cán bộ, Đơn vị đang công tác, Thời điểm đăng ký, Trạng thái tham gia |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.44. Use Case: Ghi nhận kết quả đào tạo của cán bộ giảng viên

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
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2 Chọn xem chi tiết “Danh sách học viên” có một khóa đào tạo có trạng thái “Đã hoàn thành”.  3. Hệ thống hiển thị danh sách học viên tham gia khóa đào tạo, bao gồm: Họ tên, Mã cán bộ, Đơn vị công tác, Trạng thái tham gia hiện tại (Đang học)  4. Phòng TCCB chọn một học viên và nhấn **“Ghi nhận kết quả”**.  5. Hệ thống hiển thị form ghi nhận kết quả, bao gồm: Trạng thái kết quả: Hoàn thành/ Không đạt,Ngày hoàn thành (mặc định là ngày kết thúc khóa học), File chứng chỉ (PDF) (tùy chọn, bắt buộc nếu trạng thái là “Hoàn thành”) 6. Phòng TCCB nhập thông tin và nhấn **“Lưu”**. 7. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  8. Hệ thống cập nhật trạng thái học viên:   * Nếu **Hoàn thành** (Ghi nhận kết quả đào tạo, Lưu chứng chỉ vào hồ sơ nhân sự). * Nếu **Không đạt** (Chỉ lưu trạng thái kết quả, không cập nhật chứng chỉ, Hệ thống thông báo ghi nhận kết quả thành công). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Ghi nhận kết quả cho nhiều học viên**   1. Tại bước 4, Phòng TCCB có thể chọn nhiều học viên. 2. Hệ thống cho phép ghi nhận kết quả hàng loạt với cùng trạng thái. 3. Tiếp tục bước 5 |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Khóa đào tạo chưa hoàn thành**   1. Tại bước 4, nếu trạng thái khóa đào tạo khác “Đã hoàn thành”. 2. Hệ thống hiển thị thông báo: *“Chỉ có thể ghi nhận kết quả khi khóa đào tạo đã hoàn thành.”*   **E2: Thiếu chứng chỉ khi hoàn thành, Dữ liệu không hợp lệ**   1. Tại bước 8, Hệ thống phát hiện thiếu thông tin bắt buộc hoặc file không đúng định dạng hoặc nếu học viên được đánh dấu “Hoàn thành” nhưng không upload file chứng chỉ (trong trường hợp bắt buộc). 2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. |

### 4.45. Use Case: Xem các thông tin trong hồ sơ cá nhân của nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem các thông tin trong hồ sơ cá nhân của nhân sự** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép CBGV xem toàn bộ thông tin hồ sơ cá nhân của mình đang được lưu trong hệ thống, tra cứu lịch sử hợp đồng, hệ số, bậc lương, các quyết định khen thưởng và kỷ luật của bản thân.. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | CB/GV chọn chức năng “Hồ sơ cá nhân” trên giao diện hệ thống |
| Điều kiện tiên quyết  (Precondition) | CB/GV đã đăng nhập. |
| Điều kiện thành công  (Post-condition) | Thông tin hồ sơ cá nhân được hiển thị đầy đủ cho CBGV. |
| Điều kiện thất bại | Không thể hiển thị thông tin hồ sơ cá nhân do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1.  CB/GV chọn các mục kích hoạt chức năng xem hồ sơ nhân sự  2.  Hệ thống hiển thị đầy đủ thông tin theo các tab:   * **Tab "Thông tin chung":** Mã cán bộ,Lý lịch, liên hệ, gia đình, ảnh chân dung * **Tab "Trình độ & Chức danh":** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác. * **Tab "Thông tin Đảng/ Đoàn":** Thông tin Đảng/ Đoàn đã được lưu. * **Tab "Lương & Phụ cấp":** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng * **Tab "Hợp đồng":** Thông tin về các loại hợp đồng đã ký * **Tab "Khen thưởng/Kỷ luật":** Mục khen thưởng/kỷ luật chỉ hiển thị nếu phòng TCCB đã cấu hình cho phép (xem UC 4.35, FEAT 8.9) * **Tab "Công tác":** Quá trình công tác |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.46. Use Case: Xem thông tin chi tiết đơn vị đang công tác

|  |  |
| --- | --- |
| **Tên use case** | **Xem thông tin chi tiết đơn vị đang công tác** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên xem thông tin chi tiết về đơn vị tổ chức mà mình đang công tác trong cơ cấu tổ chức của đơn vị, bao gồm thông tin cơ bản của đơn vị, danh sách chức vụ và nhân sự hiện tại trong đơn vị. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Cán bộ/Giảng viên chọn chức năng xem thông tin đơn vị công tác từ hồ sơ cá nhân hoặc menu liên quan. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống.  Cán bộ/Giảng viên đã được gán đơn vị công tác trong hệ thống.  Đơn vị tổ chức đang tồn tại trong cơ cấu tổ chức. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết của đơn vị công tác được hiển thị đầy đủ và chính xác.  Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin do lỗi hệ thống hoặc không xác định được đơn vị công tác của CBGV. |
| Luồng sự kiện chính  (Basic Flow) | 1. Cán bộ/Giảng viên truy cập chức năng xem thông tin đơn vị công tác. 2. Hệ thống xác định đơn vị mà Cán bộ/Giảng viên đang trực thuộc.  3. Hệ thống hiển thị thông tin chi tiết của đơn vị, bao gồm:   * Tab **“Tổng quan”**, bao gồm: Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị (Đang hoạt động / Sáp nhập / Giải thể) * Tab **“Nhân sự”**: Hệ thống hiển thị danh sách các nhân sự, Tên chức vụ, hệ thống hiển thị: Họ tên nhân sự, Mã cán bộ, Ngày bắt đầu. Hệ thống hiển thị danh sách nhân sự thuộc đơn vị * Tab **“Đơn vị trực thuộc”**: Hệ thống hiển thị danh sách các đơn vị dưới cấp trực thuộc đơn vị đang xem. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.47. Use Case: Thay đổi trạng thái đăng ký khóa đào tạo

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái đăng ký khóa đào tạo** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên đăng ký hoặc hủy đăng ký tham gia các khóa đào tạo do nhà trường tổ chức đang trong thời gian mở đăng ký, làm cơ sở cho việc quản lý học viên, theo dõi quá trình và ghi nhận kết quả đào tạo. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Cán bộ/Giảng viên chọn menu “Đào tạo”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống.  Khóa đào tạo tồn tại và đang ở trạng thái **“Đang mở đăng ký”**.  Thời điểm hiện tại nằm trong khoảng **Thời gian mở đăng ký**. |
| Điều kiện thành công  (Post-condition) | Đăng ký tham gia khóa đào tạo của CBGV được ghi nhận trong hệ thống (trường hợp đăng ký). Bản ghi đăng ký của CBGV được xóa khỏi hệ thống (trường hợp hủy đăng ký). |
| Điều kiện thất bại | Không thể thay đổi trạng thái đăng ký do khóa đào tạo không hợp lệ, hết hạn đăng ký hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Cán bộ/Giảng viên truy cập menu “Đào tạo”.  2. Hệ thống hiển thị danh sách các khóa đào tạo ở trạng thái Đang mở đăng ký.  3. Cán bộ/Giảng viên chọn một khóa đào tạo để xem chi tiết thông tin.  4. Hệ thống hiển thị thông tin chi tiết khóa đào tạo. Nếu CBGV chưa đăng ký, hiển thị nút “Đăng ký tham gia”. Nếu CBGV đã đăng ký (trạng thái tham gia là “Đã đăng ký”), hiển thị nút “Hủy đăng ký”.  5. Cán bộ/Giảng viên nhấn nút “Đăng ký tham gia”.  6. Hệ thống kiểm tra các điều kiện đăng ký (thời gian mở đăng ký, số lượng đăng ký chưa đạt giới hạn, trạng thái khóa đào tạo).  7. Hệ thống tạo bản ghi đăng ký đào tạo và thiết lập trạng thái tham gia là “Đã đăng ký”.  8. Hệ thống thông báo đăng ký thành công cho Cán bộ/Giảng viên. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hủy đăng ký khóa đào tạo**   1. Tại bước 4, CBGV đã đăng ký khóa đào tạo này với trạng thái tham gia “Đã đăng ký”. Hệ thống hiển thị nút “Hủy đăng ký”. 2. Cán bộ/Giảng viên nhấn nút “Hủy đăng ký”. 3. Hệ thống yêu cầu xác nhận hủy đăng ký. 4. Cán bộ/Giảng viên xác nhận. 5. Hệ thống kiểm tra trạng thái tham gia phải là “Đã đăng ký” và khóa đào tạo phải đang ở trạng thái “Đang mở đăng ký”. 6. Hệ thống xóa bản ghi đăng ký đào tạo của CBGV. 7. Hệ thống thông báo hủy đăng ký thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hết thời gian đăng ký**   1. Tại bước 4, nếu thời gian hiện tại nằm ngoài khoảng mở đăng ký. 2. Hệ thống ẩn nút “Đăng ký tham gia” và “Hủy đăng ký”, hiển thị thông báo: *“Khóa đào tạo đã hết thời gian đăng ký.”*   **E2: Đã đủ số lượng người tham gia**   1. Tại bước 6, nếu số lượng đăng ký đã đạt giới hạn. 2. Hệ thống hiển thị thông báo: *“Khóa đào tạo đã đủ số lượng đăng ký.”*   **E3: Không thể hủy đăng ký**   1. Tại bước A1.5, nếu trạng thái tham gia không phải “Đã đăng ký” (ví dụ: đã chuyển sang “Đang học” do khóa đào tạo đã bắt đầu) hoặc khóa đào tạo không còn ở trạng thái “Đang mở đăng ký”. 2. Hệ thống hiển thị thông báo: *“Không thể hủy đăng ký do khóa đào tạo đã chuyển sang giai đoạn tiếp theo.”* |

### 4.48. Use Case: Xem danh sách các khóa đào tạo đã đăng ký

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách các khóa đào tạo đã đăng ký** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên xem danh sách tất cả các khóa đào tạo mà mình đã đăng ký tham gia, theo dõi trạng thái tham gia và kết quả đào tạo của từng khóa (Đang học, Hoàn thành, Không đạt), phục vụ việc tra cứu, theo dõi quá trình học tập và kết quả đào tạo cá nhân. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Chọn menu "Đào tạo" |
| Điều kiện tiên quyết  (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống.  Cán bộ/Giảng viên đã từng đăng ký ít nhất một khóa đào tạo |
| Điều kiện thành công  (Post-condition) | Danh sách các khóa đào tạo đã đăng ký của Cán bộ/Giảng viên được hiển thị đầy đủ và chính xác.  Trạng thái tham gia và kết quả đào tạo của từng khóa được hiển thị đúng theo dữ liệu do Phòng TCCB ghi nhận. |
| Điều kiện thất bại | Không hiển thị được danh sách do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Cán bộ/Giảng viên truy cập chức năng **“Khóa đào tạo đã đăng ký”**.  2. Hệ thống truy xuất danh sách các khóa đào tạo mà Cán bộ/Giảng viên đã đăng ký.  3. Hệ thống hiển thị danh sách khóa đào tạo, bao gồm các thông tin:   * Tên khóa đào tạo, * Loại khóa đào tạo, * Thời gian đào tạo (từ ngày – đến ngày), * Đơn vị/địa điểm tổ chức, * Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), * Trạng thái tham gia của cá nhân (Đã đăng ký, Đang học, Hoàn thành, Không đạt). |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

# V. BIỂU ĐỒ LỚP & ĐẶC TẢ BỔ SUNG

## 5.1. Xác định các lớp — Biểu đồ lớp Hệ thống HRMS

> **Phạm vi biểu đồ cập nhật:** Biểu đồ này mô tả đồng thời lớp miền nghiệp vụ (Entity), lớp biên tương tác (Boundary) và lớp điều khiển nghiệp vụ (Controller) để bảo đảm truy vết đầy đủ cho 48 Use Case, bao gồm các UC 4.43 – 4.48 mới được bổ sung.

**Các lớp liệt kê (Enumeration)**

### 5.1.1. VaiTro (Vai trò)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | QUAN\_TRI\_VIEN | enum | Quản trị viên |
| 2 | CAN\_BO\_TCCB | enum | Cán bộ Tổ chức Cán bộ |
| 3 | CAN\_BO\_TCKT | enum | Cán bộ Tài chính Kế toán |
| 4 | CAN\_BO\_NHAN\_SU | enum | Cán bộ / Nhân sự |

### 5.1.2. TrangThaiTaiKhoan (Trạng thái tài khoản)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | DANG\_HOAT\_DONG | enum | Đang hoạt động |
| 2 | BI\_KHOA | enum | Bị khóa |

### 5.1.3. TrangThaiLamViec (Trạng thái làm việc)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | DANG\_CHO\_XET | enum | Đang chờ xét |
| 2 | DANG\_CONG\_TAC | enum | Đang công tác |
| 3 | DA\_THOI\_VIEC | enum | Đã thôi việc |

### 5.1.4. TrangThaiHopDongNS (Trạng thái hợp đồng nhân sự)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | CHUA\_HOP\_DONG | enum | Chưa có hợp đồng |
| 2 | CON\_HIEU\_LUC | enum | Còn hiệu lực |
| 3 | HET\_HIEU\_LUC | enum | Hết hiệu lực |
| 4 | CHO\_GIA\_HAN | enum | Chờ gia hạn |

> **Ghi chú thiết kế – Tự động chuyển trạng thái hợp đồng:** Hệ thống sử dụng bộ hẹn giờ (System Timer / Scheduled Job) để tự động chuyển trạng thái hợp đồng nhân sự từ "Còn hiệu lực" (`CON_HIEU_LUC`) sang "Chờ gia hạn" (`CHO_GIA_HAN`) khi thời gian còn lại của hợp đồng ≤ giá trị `thoiGianChoGiaHan` được cấu hình trong loại hợp đồng tương ứng (xem UC 4.19). Quá trình này chạy định kỳ hàng ngày và không yêu cầu thao tác thủ công từ người dùng.

> **Ghi chú thiết kế – Tự động thôi việc theo hợp đồng:** Khi hợp đồng hết hiệu lực và không có gia hạn hợp lệ trong thời gian cho phép, `SystemTimer` phối hợp với xử lý nghiệp vụ hợp đồng để cập nhật `NhanSu.trangThaiHopDong`, tự động đánh dấu thôi việc theo FEAT 7.6 / UC 4.27 A1, đồng thời làm đầu vào cho cơ chế tự động khóa tài khoản theo FEAT 2.6. Các UC liên quan trực tiếp: UC 4.43, UC 4.44, UC 4.45.

### 5.1.5. LoaiDonVi (Loại đơn vị)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | HOI\_DONG | enum | Hội đồng |
| 2 | BAN | enum | Ban |
| 3 | KHOA | enum | Khoa |
| 4 | PHONG | enum | Phòng |
| 5 | BO\_MON | enum | Bộ môn |
| 6 | PHONG\_THI\_NGHIEM | enum | Phòng thí nghiệm |
| 7 | TRUNG\_TAM | enum | Trung tâm |

### 5.1.6. TrangThaiDonVi (Trạng thái đơn vị)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | DANG\_HOAT\_DONG | enum | Đang hoạt động |
| 2 | GIAI\_THE | enum | Giải thể |
| 3 | SAP\_NHAP | enum | Sáp nhập |

### 5.1.7. TrangThaiHopDong (Trạng thái hợp đồng)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | CHUA\_HIEU\_LUC | enum | Chưa có hiệu lực |
| 2 | CON\_HIEU\_LUC | enum | Còn hiệu lực |
| 3 | HET\_HIEU\_LUC | enum | Hết hiệu lực |
| 4 | CHAM\_DUT\_TRUOC\_HAN | enum | Chấm dứt trước hạn |

> **Ghi chú thiết kế – Trạng thái hợp đồng chi tiết:** Trạng thái `CHUA_HIEU_LUC` được dùng để hỗ trợ UC 4.44 (chỉnh sửa hợp đồng chưa có hiệu lực). Trạng thái `CHAM_DUT_TRUOC_HAN` được dùng để phân biệt rõ trường hợp hợp đồng bị chấm dứt chủ động theo UC 4.45 / FEAT 5.4, thay vì hết hạn tự nhiên.

### 5.1.8. TrangThaiDanhMuc (Trạng thái danh mục)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | DANG\_SU\_DUNG | enum | Đang sử dụng |
| 2 | NGUNG\_SU\_DUNG | enum | Ngừng sử dụng |

### 5.1.9. TrangThaiKhoaDaoTao (Trạng thái khóa đào tạo)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | DANG\_MO\_DANG\_KY | enum | Đang mở đăng ký |
| 2 | DANG\_DAO\_TAO | enum | Đang đào tạo |
| 3 | DA\_HOAN\_THANH | enum | Đã hoàn thành |

### 5.1.10. TrangThaiThamGia (Trạng thái tham gia)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | DA\_DANG\_KY | enum | Đã đăng ký |
| 2 | DANG\_HOC | enum | Đang học |
| 3 | HOAN\_THANH | enum | Hoàn thành |
| 4 | KHONG\_DAT | enum | Không đạt |

> **Ghi chú thiết kế – Tự động chuyển trạng thái tham gia:** Khi phòng TCCB chuyển trạng thái khóa đào tạo từ "Đang mở đăng ký" (`DANG_MO_DANG_KY`) sang "Đang đào tạo" (`DANG_DAO_TAO`) thông qua UC 4.34, hệ thống tự động batch-update tất cả bản ghi `DangKyDaoTao` có `trangThaiThamGia = DA_DANG_KY` sang `DANG_HOC`. Quá trình này đảm bảo không còn khoảng trống logic giữa trạng thái "Đã đăng ký" và "Đang học".

**Các lớp thực thể (Entity)**

### 5.1.11. TaiKhoan (Tài khoản)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | maCanBo | String | Mã cán bộ |
| 2 | email | String | Email nhận mật khẩu |
| 3 | matKhau | String | Mật khẩu (đã mã hóa) |
| 4 | vaiTro | VaiTro | Vai trò người dùng |
| 5 | trangThai | TrangThaiTaiKhoan | Trạng thái tài khoản |

### 5.1.12. NhanSu (Nhân sự)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | maCanBo | String | Mã cán bộ |
| 2 | hoTen | String | Họ và tên |
| 3 | ngaySinh | Date | Ngày sinh |
| 4 | gioiTinh | String | Giới tính |
| 5 | soCCCD | String | Số CCCD/CMND |
| 6 | queQuan | String | Quê quán |
| 7 | diaChi | String | Địa chỉ |
| 8 | maSoThue | String | Mã số thuế |
| 9 | soBHXH | String | Số Bảo hiểm xã hội |
| 10 | soBHYT | String | Số Bảo hiểm y tế |
| 11 | email | String | Email |
| 12 | soDienThoai | String | Số điện thoại |
| 13 | anhChanDung | File | Ảnh chân dung |
| 14 | trinhDoVanHoa | String | Trình độ văn hóa |
| 15 | trinhDoDaoTao | String | Trình độ đào tạo |
| 16 | chucDanhNgheNghiep | String | Chức danh nghề nghiệp |
| 17 | chucDanhKhoaHoc | String | Chức danh khoa học (Học hàm) |
| 18 | laNguoiNuocNgoai | Boolean | Là người nước ngoài |
| 19 | trangThaiLamViec | TrangThaiLamViec | Trạng thái làm việc |
| 20 | trangThaiHopDong | TrangThaiHopDongNS | Trạng thái hợp đồng |
| 21 | ngayThoiViec | Date | Ngày thôi việc (nếu có) |
| 22 | lyDoThoiViec | String | Lý do thôi việc (nếu có) |

> **Các thao tác chính:** `themMoi()`, `chinhSua()`, `danhDauThoiViec()`, `xemChiTiet()`, `inHoSo()`, `xuatExcel()`, `cauHinhAnHien()`.

> **Ghi chú thiết kế – Hiển thị hồ sơ:** Việc ẩn/hiện mục khen thưởng/kỷ luật khi xem hồ sơ được điều khiển bởi lớp cấu hình `CauHinhHienThiHoSo` theo UC 4.48 / FEAT 7.9; `NhanSu` là đối tượng dữ liệu chịu tác động của cấu hình này ở các UC 4.28 và 4.38.

### 5.1.13. ThongTinNguoiNuocNgoai (Thông tin người nước ngoài)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | soVisa | String | Số visa |
| 2 | ngayHetHanVisa | Date | Ngày hết hạn visa |
| 3 | soHoChieu | String | Số hộ chiếu |
| 4 | ngayHetHanHoChieu | Date | Ngày hết hạn hộ chiếu |
| 5 | soGiayPhepLaoDong | String | Số giấy phép lao động |
| 6 | ngayHetHanGPLD | Date | Ngày hết hạn GPLD |
| 7 | fileGPLD | File | File giấy phép lao động |

### 5.1.14. ThongTinGiaDinh (Thông tin gia đình)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | moiQuanHe | String | Mối quan hệ |
| 2 | hoTen | String | Họ và tên |
| 3 | thongTinChiTiet | String | Thông tin chi tiết |

### 5.1.15. ThongTinNganHang (Thông tin ngân hàng)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | tenNganHang | String | Tên ngân hàng |
| 2 | soTaiKhoan | String | Số tài khoản |

### 5.1.16. QuaTrinhCongTac (Quá trình công tác)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | noiCongTac | String | Nơi công tác |
| 2 | thoiGianCongTac | String | Thời gian công tác |

### 5.1.17. ThongTinDangDoan (Thông tin Đảng / Đoàn)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | ngayVaoDoan | Date | Ngày vào Đoàn |
| 2 | ngayVaoDang | Date | Ngày vào Đảng |
| 3 | thongTinChiTiet | String | Thông tin chi tiết |

### 5.1.18. BangCap (Bằng cấp)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | tenBang | String | Tên bằng cấp |
| 2 | truong | String | Trường |
| 3 | nganh | String | Ngành |
| 4 | namTotNghiep | Int | Năm tốt nghiệp |
| 5 | xepLoai | String | Xếp loại |
| 6 | filePDF | File | File bằng cấp (PDF) |

### 5.1.19. ChungChi (Chứng chỉ)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | tenChungChi | String | Tên chứng chỉ |
| 2 | noiCap | String | Nơi cấp |
| 3 | ngayCap | Date | Ngày cấp |
| 4 | ngayHetHan | Date | Ngày hết hạn |
| 5 | filePDF | File | File chứng chỉ (PDF) |

### 5.1.20. DonViToChuc (Đơn vị tổ chức)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | maDonVi | String | Mã đơn vị |
| 2 | tenDonVi | String | Tên đơn vị |
| 3 | loaiDonVi | LoaiDonVi | Loại đơn vị |
| 4 | ngayThanhLap | Date | Ngày thành lập |
| 5 | diaChi | String | Địa chỉ |
| 6 | diaChiVanPhong | String | Địa chỉ văn phòng |
| 7 | email | String | Email |
| 8 | soDienThoai | String | Số điện thoại |
| 9 | website | String | Website |
| 10 | laDonViNut | Boolean | Là đơn vị nút (lá) |
| 11 | trangThai | TrangThaiDonVi | Trạng thái đơn vị |

### 5.1.21. QuyetDinhDonVi (Quyết định đơn vị)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | ngayHieuLuc | Date | Ngày hiệu lực |
| 2 | soQuyetDinh | String | Số quyết định |
| 3 | ngayQuyetDinh | Date | Ngày quyết định |
| 4 | fileDinhKem | File | File đính kèm |
| 5 | lyDo | String | Lý do |
| 6 | loaiSuKien | String | Loại sự kiện (Giải thể/Sáp nhập) |

### 5.1.22. BoNhiem (Bổ nhiệm)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | chucVu | String | Chức vụ |
| 2 | ngayBatDau | Date | Ngày bắt đầu |

### 5.1.23. HeSoLuong (Hệ số lương)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | ngachVienChuc | String | Ngạch viên chức |
| 2 | bacLuong | Int | Bậc lương |
| 3 | heSoLuong | Double | Hệ số lương |
| 4 | trangThai | TrangThaiDanhMuc | Trạng thái danh mục |

### 5.1.24. LoaiPhuCap (Loại phụ cấp)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | tenLoaiPhuCap | String | Tên loại phụ cấp |
| 2 | moTa | String | Mô tả |
| 3 | cachTinh | String | Cách tính phụ cấp |
| 4 | trangThai | TrangThaiDanhMuc | Trạng thái danh mục |

### 5.1.25. LoaiHopDong (Loại hợp đồng)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | tenLoaiHopDong | String | Tên loại hợp đồng |
| 2 | soThangToiThieu | Int | Số tháng tối thiểu |
| 3 | soThangToiDa | Int | Số tháng tối đa |
| 4 | soLanGiaHanToiDa | Int | Số lần gia hạn tối đa |
| 5 | thoiGianChoGiaHan | Int | Thời gian chờ gia hạn (ngày) |
| 6 | trangThai | TrangThaiDanhMuc | Trạng thái danh mục |

### 5.1.26. HopDongLaoDong (Hợp đồng lao động)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | soHopDong | String | Số hợp đồng |
| 2 | ngayKy | Date | Ngày ký hợp đồng |
| 3 | ngayHieuLuc | Date | Ngày hiệu lực |
| 4 | ngayHetHan | Date | Ngày hết hạn |
| 5 | donViCongTac | String | Đơn vị công tác |
| 6 | noiDung | String | Nội dung hợp đồng |
| 7 | filePDF | File | File hợp đồng (PDF) |
| 8 | trangThai | TrangThaiHopDong | Trạng thái hợp đồng |

> **Các thao tác chính:** `taoMoi()`, `capNhatTrangThai()`, `xemDanhSach()`, `xemChiTiet()`, `chinhSua()`, `chamDutTruocHan()`.

> **Ghi chú thiết kế – Truy vết UC hợp đồng:** Lớp `HopDongLaoDong` bao phủ các UC 4.22, 4.43, 4.44, 4.45 tương ứng với FEAT 5.1 – 5.4; việc chấm dứt trước hạn được lưu bổ sung qua lớp `BanGhiChamDutHopDong`.

### 5.1.27. PhuLucHopDong (Phụ lục hợp đồng)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | ngayHieuLuc | Date | Ngày hiệu lực |
| 2 | dieuKhoanBoSung | String | Điều khoản bổ sung |
| 3 | quyDinhMoi | String | Quy định mới |
| 4 | luuYQuanTrong | String | Lưu ý quan trọng |

### 5.1.28. DanhGia (Đánh giá) — *<>*

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | ngayQuyetDinh | Date | Ngày quyết định |
| 2 | dangHoatDong | Boolean | Đang hoạt động |

> **Các thao tác chính:** `ghiNhanDanhGia()`, `xemLichSu()`, `timKiem()`, `loc()`.

> **Ghi chú thiết kế – Truy vết UC đánh giá:** `DanhGia` là thực thể lõi cho UC 4.29, UC 4.46 và UC 4.47; các thao tác xem lịch sử, tìm kiếm và lọc được điều phối qua `DanhGiaController` và có thể trả về lớp bao `DanhSachKetQuaDanhGia`.

### 5.1.29. KhenThuong (Khen thưởng) — *kế thừa DanhGia*

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | loaiKhenThuong | String | Loại khen thưởng |
| 2 | tenKhenThuong | String | Tên khen thưởng |
| 3 | soQuyetDinh | String | Số quyết định |
| 4 | noiDung | String | Nội dung khen thưởng |
| 5 | soTienThuong | Double | Số tiền thưởng |

### 5.1.30. KyLuat (Kỷ luật) — *kế thừa DanhGia*

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | loaiKyLuat | String | Loại kỷ luật |
| 2 | tenKyLuat | String | Tên kỷ luật |
| 3 | lyDo | String | Lý do kỷ luật |
| 4 | hinhThucXuLy | String | Hình thức xử lý |

### 5.1.31. KhoaDaoTao (Khóa đào tạo)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | tenKhoaDaoTao | String | Tên khóa đào tạo |
| 2 | loaiKhoaDaoTao | String | Loại khóa đào tạo |
| 3 | thoiGianBatDau | Date | Thời gian bắt đầu |
| 4 | thoiGianKetThuc | Date | Thời gian kết thúc |
| 5 | diaDiem | String | Địa điểm |
| 6 | kinhPhi | Double | Kinh phí |
| 7 | camKetSauDaoTao | String | Cam kết sau đào tạo |
| 8 | tenChungChi | String | Tên chứng chỉ |
| 9 | loaiChungChi | String | Loại chứng chỉ |
| 10 | thoiGianMoDangKy\_Tu | Date | Thời gian mở đăng ký (từ) |
| 11 | thoiGianMoDangKy\_Den | Date | Thời gian mở đăng ký (đến) |
| 12 | gioiHanSoNguoi | Int | Giới hạn số người |
| 13 | trangThai | TrangThaiKhoaDaoTao | Trạng thái khóa đào tạo |

### 5.1.32. DangKyDaoTao (Đăng ký đào tạo)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | thoiDiemDangKy | Date | Thời điểm đăng ký |
| 2 | trangThaiThamGia | TrangThaiThamGia | Trạng thái tham gia |
| 3 | ngayHoanThanh | Date | Ngày hoàn thành |
| 4 | fileChungChi | File | File chứng chỉ |

### 5.1.33. NhatKyHeThong (Nhật ký hệ thống)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | thoiGian | DateTime | Thời gian ghi nhật ký |
| 2 | taiKhoan | String | Tài khoản thực hiện |
| 3 | hoTen | String | Họ tên người thực hiện |
| 4 | vaiTro | String | Vai trò người thực hiện |
| 5 | loaiHanhDong | String | Loại hành động |
| 6 | doiTuong | String | Đối tượng |
| 7 | maDoiTuong | String | Mã đối tượng |
| 8 | moTaChiTiet | String | Mô tả chi tiết |
| 9 | diaChiIP | String | Địa chỉ IP |

### 5.1.34. BanGhiChamDutHopDong (Bản ghi chấm dứt hợp đồng)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | lyDo | String | Lý do chấm dứt trước hạn |
| 2 | ngayQuyetDinh | Date | Ngày ra quyết định chấm dứt |
| 3 | ngayHieuLuc | Date | Ngày chấm dứt có hiệu lực |
| 4 | nguoiThucHien | String | Người thực hiện thao tác chấm dứt |
| 5 | ghiChu | String | Ghi chú bổ sung |

> **Ghi chú thiết kế:** Lớp này được thêm để lưu vết UC 4.45 / FEAT 5.4, tách riêng dữ liệu chấm dứt trước hạn khỏi bản thân hợp đồng lao động.

### 5.1.35. DanhSachKetQuaDanhGia (Danh sách kết quả đánh giá)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | tuKhoa | String | Từ khóa tìm kiếm hiện tại |
| 2 | tongSoBanGhi | Int | Tổng số bản ghi phù hợp |
| 3 | trangHienTai | Int | Trang hiện tại |
| 4 | kichThuocTrang | Int | Kích thước trang |

> **Ghi chú thiết kế:** Lớp bao kết quả được dùng cho UC 4.46 – 4.47 để gom danh sách bản ghi đánh giá và thông tin phân trang/lọc.

### 5.1.36. CauHinhHienThiHoSo (Cấu hình hiển thị hồ sơ)

| STT | Tên thuộc tính | Kiểu dữ liệu | Mô tả |
| --- | --- | --- | --- |
| 1 | vaiTro | VaiTro | Vai trò được áp dụng cấu hình |
| 2 | anKhenThuong | Boolean | Ẩn/hiện mục khen thưởng |
| 3 | anKyLuat | Boolean | Ẩn/hiện mục kỷ luật |

> **Ghi chú thiết kế:** Đây là cấu hình mức toàn hệ thống cho UC 4.48 / FEAT 7.9. Cấu hình này áp dụng khi hiển thị `NhanSu`, nhưng không làm thay đổi dữ liệu đánh giá gốc.

### 5.1.37. ManHinhHopDongLaoDong (Boundary)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | chonTabHopDong() | Người dùng truy cập tab hợp đồng trong hồ sơ nhân sự |
| 2 | hienThiDanhSachHopDong() | Hiển thị danh sách hợp đồng lao động |
| 3 | hienThiChiTietHopDong() | Hiển thị chi tiết hợp đồng được chọn |
| 4 | moFormChinhSua() | Mở biểu mẫu chỉnh sửa hợp đồng chưa có hiệu lực |
| 5 | moFormChamDutTruocHan() | Mở biểu mẫu chấm dứt hợp đồng trước hạn |

### 5.1.38. ManHinhDanhGia (Boundary)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | chonTabDanhGia() | Người dùng truy cập tab khen thưởng/kỷ luật |
| 2 | hienThiLichSuDanhGia() | Hiển thị lịch sử đánh giá theo thời gian |
| 3 | nhapTieuChiTimKiem() | Nhập từ khóa và tiêu chí tìm kiếm/lọc |
| 4 | hienThiKetQuaLoc() | Hiển thị danh sách kết quả phù hợp |
| 5 | hienThiChiTietDanhGia() | Hiển thị chi tiết bản ghi đánh giá |

### 5.1.39. ManHinhCauHinhHienThiHoSo (Boundary)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | hienThiDanhSachVaiTro() | Hiển thị các vai trò và trạng thái ẩn/hiện tương ứng |
| 2 | capNhatAnHien() | Bật/tắt hiển thị khen thưởng/kỷ luật theo vai trò |
| 3 | luuCauHinh() | Lưu cấu hình hiển thị hồ sơ |

### 5.1.40. HopDongController (Controller)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | xemDanhSachHopDong() | Điều phối lấy danh sách hợp đồng của nhân sự |
| 2 | xemChiTietHopDong() | Điều phối lấy chi tiết hợp đồng |
| 3 | chinhSuaHopDongChuaHieuLuc() | Xử lý chỉnh sửa hợp đồng chưa có hiệu lực |
| 4 | chamDutHopDongTruocHan() | Xử lý chấm dứt hợp đồng trước hạn |
| 5 | dongBoTrangThaiNhanSu() | Đồng bộ trạng thái hợp đồng/thôi việc của nhân sự |

### 5.1.41. DanhGiaController (Controller)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | xemLichSuDanhGia() | Điều phối xem lịch sử đánh giá của nhân sự |
| 2 | timKiemDanhGia() | Điều phối tìm kiếm đánh giá |
| 3 | locDanhGia() | Điều phối lọc danh sách đánh giá |
| 4 | taiChiTietDanhGia() | Lấy chi tiết bản ghi đánh giá |

### 5.1.42. CauHinhHoSoController (Controller)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | taiCauHinhHienThi() | Tải cấu hình hiển thị hồ sơ hiện hành |
| 2 | luuCauHinhHienThi() | Lưu cấu hình ẩn/hiện khen thưởng/kỷ luật |
| 3 | apDungCauHinhAnHien() | Áp dụng cấu hình khi hiển thị hồ sơ nhân sự |

### 5.1.43. TaiKhoanController (Controller)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | khoaTaiKhoanTheoTrangThaiNhanSu() | Khóa tài khoản khi nhân sự đã thôi việc |
| 2 | dongBoTrangThaiTaiKhoan() | Đồng bộ trạng thái tài khoản với hồ sơ nhân sự |

### 5.1.44. SystemTimer (Controller)

| STT | Tên thao tác | Mô tả |
| --- | --- | --- |
| 1 | kiemTraHopDongSapHetHan() | Kiểm tra và chuyển hợp đồng sang trạng thái chờ gia hạn |
| 2 | kiemTraHopDongHetHan() | Kiểm tra hợp đồng hết hiệu lực và kích hoạt xử lý tiếp theo |
| 3 | tuDongDanhDauThoiViec() | Tự động đánh dấu thôi việc theo FEAT 7.6 |
| 4 | tuDongKhoaTaiKhoan() | Tự động khóa tài khoản theo FEAT 2.6 |

**Quan hệ giữa các lớp**

| STT | Lớp nguồn | Quan hệ | Lớp đích | Mô tả |
| --- | --- | --- | --- | --- |
| 1 | TaiKhoan | 1 → 1 | NhanSu | Một tài khoản liên kết một nhân sự |
| 2 | NhanSu | 1 ◆ 0..1 | ThongTinNguoiNuocNgoai | Nhân sự có tối đa một thông tin người nước ngoài |
| 3 | NhanSu | 1 ◆ 0..\* | ThongTinGiaDinh | Nhân sự có nhiều thông tin gia đình |
| 4 | NhanSu | 1 ◆ 1 | ThongTinNganHang | Nhân sự có một tài khoản ngân hàng |
| 5 | NhanSu | 1 ◆ 0..\* | QuaTrinhCongTac | Nhân sự có nhiều quá trình công tác |
| 6 | NhanSu | 1 ◆ 0..1 | ThongTinDangDoan | Nhân sự có tối đa một thông tin Đảng/Đoàn |
| 7 | NhanSu | 1 ◆ 0..\* | BangCap | Nhân sự có nhiều bằng cấp |
| 8 | NhanSu | 1 ◆ 0..\* | ChungChi | Nhân sự có nhiều chứng chỉ |
| 9 | NhanSu | 0..\* → 0..1 | HeSoLuong | Nhân sự áp dụng một hệ số lương |
| 10 | NhanSu | 0..\* → 0..\* | LoaiPhuCap | Nhân sự hưởng nhiều loại phụ cấp |
| 11 | NhanSu | 1 ◆ 0..\* | HopDongLaoDong | Nhân sự ký nhiều hợp đồng |
| 12 | HopDongLaoDong | 0..\* → 1 | LoaiHopDong | Hợp đồng thuộc một loại hợp đồng |
| 13 | HopDongLaoDong | 1 ◆ 0..\* | PhuLucHopDong | Hợp đồng có nhiều phụ lục |
| 14 | DanhGia | ◁— | KhenThuong | KhenThuong kế thừa DanhGia |
| 15 | DanhGia | ◁— | KyLuat | KyLuat kế thừa DanhGia |
| 16 | NhanSu | 1 ◆ 0..\* | DanhGia | Nhân sự nhận nhiều đánh giá |
| 17 | DonViToChuc | 0..1 ◇ 0..\* | DonViToChuc | Đơn vị cha chứa nhiều đơn vị con |
| 18 | DonViToChuc | 1 ◆ 0..\* | QuyetDinhDonVi | Đơn vị có nhiều quyết định |
| 19 | BoNhiem | 0..\* → 1 | NhanSu | Bổ nhiệm cho nhân sự |
| 20 | BoNhiem | 0..\* → 1 | DonViToChuc | Bổ nhiệm tại đơn vị |
| 21 | DangKyDaoTao | 0..\* → 1 | NhanSu | Người đăng ký đào tạo |
| 22 | DangKyDaoTao | 0..\* → 1 | KhoaDaoTao | Đăng ký khóa đào tạo |
| 23 | TaiKhoan | 1 → 0..\* | NhatKyHeThong | Tài khoản tạo nhiều nhật ký |
| 24 | HopDongLaoDong | 1 ◆ 0..1 | BanGhiChamDutHopDong | Hợp đồng có tối đa một bản ghi chấm dứt trước hạn |
| 25 | DanhSachKetQuaDanhGia | 1 ◇ 0..\* | DanhGia | Kết quả tìm kiếm/lọc bao gồm nhiều bản ghi đánh giá |
| 26 | CauHinhHienThiHoSo | 0..\* → 1 | VaiTro | Cấu hình hiển thị được thiết lập theo vai trò |
| 27 | CauHinhHienThiHoSo | 0..\* → 0..\* | NhanSu | Cấu hình chi phối hiển thị mục khen thưởng/kỷ luật khi xem hồ sơ |
| 28 | ManHinhHopDongLaoDong | 1 → 1 | HopDongController | Màn hình hợp đồng gọi controller nghiệp vụ hợp đồng |
| 29 | HopDongController | 1 → 0..\* | HopDongLaoDong | Controller xử lý xem/sửa/chấm dứt hợp đồng |
| 30 | HopDongController | 1 → 0..\* | BanGhiChamDutHopDong | Controller ghi nhận chấm dứt trước hạn |
| 31 | HopDongController | 1 → 0..\* | NhanSu | Controller đồng bộ trạng thái hợp đồng và trạng thái thôi việc |
| 32 | ManHinhDanhGia | 1 → 1 | DanhGiaController | Màn hình đánh giá gọi controller nghiệp vụ đánh giá |
| 33 | DanhGiaController | 1 → 0..\* | DanhGia | Controller xử lý xem lịch sử, tìm kiếm, lọc đánh giá |
| 34 | DanhGiaController | 1 → 0..\* | DanhSachKetQuaDanhGia | Controller trả về tập kết quả đánh giá |
| 35 | ManHinhCauHinhHienThiHoSo | 1 → 1 | CauHinhHoSoController | Màn hình cấu hình gọi controller cấu hình hồ sơ |
| 36 | CauHinhHoSoController | 1 → 0..\* | CauHinhHienThiHoSo | Controller quản lý cấu hình ẩn/hiện hồ sơ |
| 37 | CauHinhHoSoController | 1 → 0..\* | NhanSu | Controller áp dụng cấu hình khi hiển thị hồ sơ |
| 38 | SystemTimer | 1 → 1 | HopDongController | Bộ hẹn giờ điều phối tự động xử lý hợp đồng |
| 39 | SystemTimer | 1 → 1 | TaiKhoanController | Bộ hẹn giờ điều phối tự động khóa tài khoản |
| 40 | TaiKhoanController | 1 → 0..\* | TaiKhoan | Controller khóa/mở và đồng bộ trạng thái tài khoản |
| 41 | TaiKhoanController | 1 → 0..\* | NhanSu | Controller đọc trạng thái thôi việc của nhân sự |

## 5.2. Xây dựng biểu đồ lớp

```mermaid
classDiagram
    direction TB

    %% ===== ENUMERATIONS =====

    class VaiTro {
        <<enumeration>>
        QUAN_TRI_VIEN
        CAN_BO_TCCB
        CAN_BO_TCKT
        CAN_BO_NHAN_SU
    }

    class TrangThaiTaiKhoan {
        <<enumeration>>
        DANG_HOAT_DONG
        BI_KHOA
    }

    class TrangThaiLamViec {
        <<enumeration>>
        DANG_CHO_XET
        DANG_CONG_TAC
        DA_THOI_VIEC
    }

    class TrangThaiHopDongNS {
        <<enumeration>>
        CHUA_HOP_DONG
        CON_HIEU_LUC
        HET_HIEU_LUC
        CHO_GIA_HAN
    }

    class LoaiDonVi {
        <<enumeration>>
        HOI_DONG
        BAN
        KHOA
        PHONG
        BO_MON
        PHONG_THI_NGHIEM
        TRUNG_TAM
    }

    class TrangThaiDonVi {
        <<enumeration>>
        DANG_HOAT_DONG
        GIAI_THE
        SAP_NHAP
    }

    class TrangThaiHopDong {
        <<enumeration>>
        CHUA_HIEU_LUC
        CON_HIEU_LUC
        HET_HIEU_LUC
        CHAM_DUT_TRUOC_HAN
    }

    class TrangThaiDanhMuc {
        <<enumeration>>
        DANG_SU_DUNG
        NGUNG_SU_DUNG
    }

    class TrangThaiKhoaDaoTao {
        <<enumeration>>
        DANG_MO_DANG_KY
        DANG_DAO_TAO
        DA_HOAN_THANH
    }

    class TrangThaiThamGia {
        <<enumeration>>
        DA_DANG_KY
        DANG_HOC
        HOAN_THANH
        KHONG_DAT
    }

    %% ===== CORE ENTITIES =====

    class TaiKhoan {
        -String email
        -String matKhau
        -VaiTro vaiTro
        -TrangThaiTaiKhoan trangThai
        +dangNhap()
        +dangXuat()
        +doiMatKhau()
        +khoaTaiKhoan()
        +moKhoaTaiKhoan()
        +phanQuyen()
    }

    class NhanSu {
        -String maCanBo
        -String hoTen
        -Date ngaySinh
        -String gioiTinh
        -String soCCCD
        -String queQuan
        -String diaChi
        -String maSoThue
        -String soBHXH
        -String soBHYT
        -String email
        -String soDienThoai
        -File anhChanDung
        -String trinhDoVanHoa
        -String trinhDoDaoTao
        -String chucDanhNgheNghiep
        -String chucDanhKhoaHoc
        -Boolean laNguoiNuocNgoai
        -TrangThaiLamViec trangThaiLamViec
        -TrangThaiHopDongNS trangThaiHopDong
        -Date ngayThoiViec
        -String lyDoThoiViec
        +themMoi()
        +chinhSua()
        +danhDauThoiViec()
        +xemChiTiet()
        +inHoSo()
        +xuatExcel()
        +cauHinhAnHien()
    }

    class ThongTinNguoiNuocNgoai {
        -String soVisa
        -Date ngayHetHanVisa
        -String soHoChieu
        -Date ngayHetHanHoChieu
        -String soGiayPhepLaoDong
        -Date ngayHetHanGPLD
        -File fileGPLD
    }

    class ThongTinGiaDinh {
        -String moiQuanHe
        -String hoTen
        -String thongTinChiTiet
    }

    class ThongTinNganHang {
        -String tenNganHang
        -String soTaiKhoan
    }

    class QuaTrinhCongTac {
        -String noiCongTac
        -String thoiGianCongTac
    }

    class ThongTinDangDoan {
        -Date ngayVaoDoan
        -Date ngayVaoDang
        -String thongTinChiTiet
    }

    class BangCap {
        -String tenBang
        -String truong
        -String nganh
        -Int namTotNghiep
        -String xepLoai
        -File filePDF
    }

    class ChungChi {
        -String tenChungChi
        -String noiCap
        -Date ngayCap
        -Date ngayHetHan
        -File filePDF
    }

    %% ===== ORGANIZATIONAL STRUCTURE =====

    class DonViToChuc {
        -String maDonVi
        -String tenDonVi
        -LoaiDonVi loaiDonVi
        -Date ngayThanhLap
        -String diaChi
        -String diaChiVanPhong
        -String email
        -String soDienThoai
        -String website
        -Boolean laDonViNut
        -TrangThaiDonVi trangThai
        +themMoi()
        +suaThongTin()
        +giaiThe()
        +sapNhap()
        +xemChiTiet()
    }

    class QuyetDinhDonVi {
        -Date ngayHieuLuc
        -String soQuyetDinh
        -Date ngayQuyetDinh
        -File fileDinhKem
        -String lyDo
        -String loaiSuKien
    }

    class BoNhiem {
        -String chucVu
        -Date ngayBatDau
        +boNhiem()
        +baiNhiem()
    }

    %% ===== SALARY & ALLOWANCE =====

    class HeSoLuong {
        -String ngachVienChuc
        -String bacLuong
        -Double heSoLuong
        -TrangThaiDanhMuc trangThai
        +themMoi()
        +sua()
        +xoa()
        +ngungSuDung()
    }

    class LoaiPhuCap {
        -String tenLoaiPhuCap
        -String moTa
        -String cachTinh
        -TrangThaiDanhMuc trangThai
        +themMoi()
        +sua()
        +ngungSuDung()
    }

    %% ===== CONTRACT =====

    class LoaiHopDong {
        -String tenLoaiHopDong
        -Int soThangToiThieu
        -Int soThangToiDa
        -Int soLanGiaHanToiDa
        -Int thoiGianChoGiaHan
        -TrangThaiDanhMuc trangThai
        +themMoi()
        +sua()
        +ngungSuDung()
    }

    class HopDongLaoDong {
        -String soHopDong
        -Date ngayKy
        -Date ngayHieuLuc
        -Date ngayHetHan
        -String donViCongTac
        -String noiDung
        -File filePDF
        -TrangThaiHopDong trangThai
        +taoMoi()
        +capNhatTrangThai()
        +xemDanhSach()
        +xemChiTiet()
        +chinhSua()
        +chamDutTruocHan()
    }

    class PhuLucHopDong {
        -Date ngayHieuLuc
        -String dieuKhoanBoSung
        -String quyDinhMoi
        -String luuYQuanTrong
    }

    class BanGhiChamDutHopDong {
        <<entity>>
        -String lyDo
        -Date ngayQuyetDinh
        -Date ngayHieuLuc
        -String nguoiThucHien
        -String ghiChu
    }

    %% ===== EVALUATION =====

    class DanhGia {
        <<abstract>>
        -Date ngayQuyetDinh
        -Boolean dangHoatDong
        +ghiNhanDanhGia()*
        +xemLichSu()
        +timKiem()
        +loc()
    }

    class KhenThuong {
        -String loaiKhenThuong
        -String tenKhenThuong
        -String soQuyetDinh
        -String noiDung
        -Double soTienThuong
    }

    class KyLuat {
        -String loaiKyLuat
        -String tenKyLuat
        -String lyDo
        -String hinhThucXuLy
    }

    class DanhSachKetQuaDanhGia {
        <<entity>>
        -String tuKhoa
        -Int tongSoBanGhi
        -Int trangHienTai
        -Int kichThuocTrang
    }

    class CauHinhHienThiHoSo {
        <<configuration>>
        -VaiTro vaiTro
        -Boolean anKhenThuong
        -Boolean anKyLuat
    }

    %% ===== BOUNDARY / CONTROLLER =====

    class ManHinhHopDongLaoDong {
        <<boundary>>
        +chonTabHopDong()
        +hienThiDanhSachHopDong()
        +hienThiChiTietHopDong()
        +moFormChinhSua()
        +moFormChamDutTruocHan()
    }

    class ManHinhDanhGia {
        <<boundary>>
        +chonTabDanhGia()
        +hienThiLichSuDanhGia()
        +nhapTieuChiTimKiem()
        +hienThiKetQuaLoc()
        +hienThiChiTietDanhGia()
    }

    class ManHinhCauHinhHienThiHoSo {
        <<boundary>>
        +hienThiDanhSachVaiTro()
        +capNhatAnHien()
        +luuCauHinh()
    }

    class HopDongController {
        <<control>>
        +xemDanhSachHopDong()
        +xemChiTietHopDong()
        +chinhSuaHopDongChuaHieuLuc()
        +chamDutHopDongTruocHan()
        +dongBoTrangThaiNhanSu()
    }

    class DanhGiaController {
        <<control>>
        +xemLichSuDanhGia()
        +timKiemDanhGia()
        +locDanhGia()
        +taiChiTietDanhGia()
    }

    class CauHinhHoSoController {
        <<control>>
        +taiCauHinhHienThi()
        +luuCauHinhHienThi()
        +apDungCauHinhAnHien()
    }

    class TaiKhoanController {
        <<control>>
        +khoaTaiKhoanTheoTrangThaiNhanSu()
        +dongBoTrangThaiTaiKhoan()
    }

    class SystemTimer {
        <<control>>
        +kiemTraHopDongSapHetHan()
        +kiemTraHopDongHetHan()
        +tuDongDanhDauThoiViec()
        +tuDongKhoaTaiKhoan()
    }

    %% ===== TRAINING =====

    class KhoaDaoTao {
        -String tenKhoaDaoTao
        -String loaiKhoaDaoTao
        -Date thoiGianBatDau
        -Date thoiGianKetThuc
        -String diaDiem
        -Double kinhPhi
        -String camKetSauDaoTao
        -String tenChungChi
        -String loaiChungChi
        -Date thoiGianMoDangKy_Tu
        -Date thoiGianMoDangKy_Den
        -Int gioiHanSoNguoi
        -TrangThaiKhoaDaoTao trangThai
        +moKhoaDaoTao()
        +suaThongTin()
        +xemChiTiet()
    }

    class DangKyDaoTao {
        -Date thoiDiemDangKy
        -TrangThaiThamGia trangThaiThamGia
        -Date ngayHoanThanh
        -File fileChungChi
        +dangKy()
        +ghiNhanKetQua()
    }

    %% ===== AUDIT =====

    class NhatKyHeThong {
        -DateTime thoiGian
        -String taiKhoan
        -String hoTen
        -String vaiTro
        -String loaiHanhDong
        -String doiTuong
        -String maDoiTuong
        -String moTaChiTiet
        -String diaChiIP
    }

    %% ========================================
    %% RELATIONSHIPS
    %% ========================================

    %% --- Account & Personnel ---
    TaiKhoan "1" --> "1" NhanSu : lienKetVoi

    %% --- Personnel Compositions (value objects owned by NhanSu) ---
    NhanSu "1" *-- "0..1" ThongTinNguoiNuocNgoai : co
    NhanSu "1" *-- "0..*" ThongTinGiaDinh : co
    NhanSu "1" *-- "1" ThongTinNganHang : co
    NhanSu "1" *-- "0..*" QuaTrinhCongTac : co
    NhanSu "1" *-- "0..1" ThongTinDangDoan : co
    NhanSu "1" *-- "0..*" BangCap : co
    NhanSu "1" *-- "0..*" ChungChi : co

    %% --- Salary & Allowance ---
    NhanSu "0..*" --> "0..1" HeSoLuong : apDung
    NhanSu "0..*" --> "0..*" LoaiPhuCap : huong

    %% --- Contract ---
    NhanSu "1" *-- "0..*" HopDongLaoDong : ky
    HopDongLaoDong "0..*" --> "1" LoaiHopDong : thuocLoai
    HopDongLaoDong "1" *-- "0..*" PhuLucHopDong : boSung
    HopDongLaoDong "1" *-- "0..1" BanGhiChamDutHopDong : chamDutBang

    %% --- Evaluation (Inheritance) ---
    DanhGia <|-- KhenThuong
    DanhGia <|-- KyLuat
    NhanSu "1" *-- "0..*" DanhGia : nhanDuoc
    DanhSachKetQuaDanhGia "1" o-- "0..*" DanhGia : baoGom

    %% --- Visibility Configuration ---
    CauHinhHienThiHoSo "0..*" --> "1" VaiTro : apDungCho
    CauHinhHienThiHoSo "0..*" --> "0..*" NhanSu : chiPhoiHienThi

    %% --- Organization ---
    DonViToChuc "0..1" o-- "0..*" DonViToChuc : donViCha
    DonViToChuc "1" *-- "0..*" QuyetDinhDonVi : co

    %% --- Appointment (Association Class) ---
    BoNhiem "0..*" --> "1" NhanSu : boNhiemCho
    BoNhiem "0..*" --> "1" DonViToChuc : taiDonVi

    %% --- Training (Association Class) ---
    DangKyDaoTao "0..*" --> "1" NhanSu : nguoiDangKy
    DangKyDaoTao "0..*" --> "1" KhoaDaoTao : khoaHoc

    %% --- Audit Log ---
    TaiKhoan "1" --> "0..*" NhatKyHeThong : taoRa

    %% --- Boundary / Controller ---
    ManHinhHopDongLaoDong "1" --> "1" HopDongController : goi
    HopDongController "1" --> "0..*" HopDongLaoDong : xuLy
    HopDongController "1" --> "0..*" BanGhiChamDutHopDong : ghiNhan
    HopDongController "1" --> "0..*" NhanSu : dongBoTrangThai

    ManHinhDanhGia "1" --> "1" DanhGiaController : goi
    DanhGiaController "1" --> "0..*" DanhGia : truyVan
    DanhGiaController "1" --> "0..*" DanhSachKetQuaDanhGia : traVe

    ManHinhCauHinhHienThiHoSo "1" --> "1" CauHinhHoSoController : goi
    CauHinhHoSoController "1" --> "0..*" CauHinhHienThiHoSo : quanLy
    CauHinhHoSoController "1" --> "0..*" NhanSu : apDungChoHienThi

    %% --- Automation ---
    SystemTimer "1" --> "1" HopDongController : kichHoatFEAT76
    SystemTimer "1" --> "1" TaiKhoanController : kichHoatFEAT26
    TaiKhoanController "1" --> "0..*" TaiKhoan : dongBoKhoa
    TaiKhoanController "1" --> "0..*" NhanSu : docTrangThaiThoiViec

    note for SystemTimer "Chạy định kỳ để hỗ trợ FEAT 7.6 (tự động thôi việc) và FEAT 2.6 (tự động khóa tài khoản)."
```

## 5.3. FEAT-specific SUPLs theo phần đóng góp của các thành viên

### 5.3.1. Phần đóng góp của Nguyễn Hồng Phúc

### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F03** | Tự động đăng xuất phiên không hoạt động | Hệ thống tự động đăng xuất phiên làm việc nếu người dùng không thao tác trong 30 phút. Tham chiếu FEAT 1.3. | **M** |
| **SUPL-F04** | Tự động khóa tài khoản nhân sự thôi việc | Khi nhân sự được đánh dấu thôi việc (FEAT 8.5/8.6), hệ thống tự động chuyển tài khoản của nhân sự đó sang trạng thái khóa. Tham chiếu FEAT 2.6. | **M** |
| **SUPL-F08** | Bảo vệ mật khẩu lưu trữ | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. | **M** |

### 2.7. Design Constraints – Ràng buộc thiết kế

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-DC02** | Cơ cấu tổ chức dạng cây | Cơ cấu tổ chức đơn vị phải được mô hình hóa dưới dạng cấu trúc cây cha-con với gốc là Trường Đại học Thủy Lợi (FEAT 3.1). | **M** |

### 5.3.2. Phần đóng góp của Ngô Đức Nam Khánh

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F01** | Ghi nhật ký hệ thống tự động (Auto Logging) | Hệ thống tự động ghi lại mọi hành động truy cập, thêm/sửa/xóa dữ liệu và thay đổi cấu hình với đầy đủ các thông tin: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. Tham chiếu FEAT 6.1. | **M** |
| **SUPL-F07** | Quy tắc nghiệp vụ chung về xóa/thay đổi trạng thái | Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ "Thay đổi trạng thái" (không hỗ trợ "Xóa") để đảm bảo tính toàn vẹn dữ liệu và phục vụ kiểm toán. Hệ số lương cho phép xóa khi chưa được hồ sơ nào sử dụng. | **M** |
| **SUPL-P03** | Thời gian tạo báo cáo thống kê | Dashboard thống kê và báo cáo tổng hợp (FEAT 5.1) phải hoàn thành render trong thời gian chấp nhận được. | **E** |

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F01 | FEAT 6.1, UC Auto Logging | System Timer |
| | SUPL-F07 | FEAT 4.3, 4.4, 4.5 | TCCB |
| **Performance** | SUPL-P03 | FEAT 5.1, UC 4.23 | TCCB, TCKT |

### 5.3.3. Phần đóng góp của Nguyễn Hải Ninh

### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F02** | Tự động sinh mã nhân sự | Khi tạo mới hồ sơ nhân sự, hệ thống tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. | **M** |
| **SUPL-F05** | Tự động chuyển trạng thái hợp đồng | Hệ thống tự động chuyển trạng thái hợp đồng từ "Còn hiệu lực" sang "Chờ gia hạn" khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. | **M** |

### 2.4. Performance – Hiệu năng

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-P06** | Hiệu năng xuất Excel | Xuất danh sách nhân sự ra file Excel (FEAT 8.8) phải hoàn thành trong thời gian chấp nhận được. | **E** |

### 2.5. Security – Bảo mật

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-SE08** | Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật | Chỉ các vai trò được ủy quyền mới được phép cấu hình ẩn/hiện các mục khen thưởng/kỷ luật ở mức toàn hệ thống; mọi thay đổi cấu hình phải được ghi audit log với người thực hiện, thời gian, giá trị trước/sau. Tham chiếu FEAT 8.9. | **M** |
| **SUPL-SE09** | Kiểm soát chấm dứt hợp đồng trước hạn | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; hệ thống phải ghi audit log đầy đủ cho thao tác này gồm mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian và giá trị trước/sau. Tham chiếu FEAT 7.4. | **M** |

### 3.1. Functionality — Yêu cầu chức năng bổ sung

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-F02** | Correctness (Tính đúng đắn) | Tỷ lệ mã sinh tự động trùng lặp; Tỷ lệ mã tuân thủ mẫu mã đang áp dụng | 0% trùng lặp mã cán bộ. 100% hồ sơ nhân sự mới được cấp mã ngay khi tạo và 100% mã sinh ra tuân thủ mẫu mã đang áp dụng. |
| **SUPL-F05** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái Chờ gia hạn đúng hạn | 100% hợp đồng đủ điều kiện được chuyển trạng thái trong ≤ 24 giờ kể từ thời điểm đủ điều kiện. |

### 3.4. Performance — Hiệu năng

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-P06** | Speed (Tốc độ) – Xuất dữ liệu | Thời gian xuất Excel | ≤ 10 giây cho ≤ 1.000 bản ghi. ≤ 30 giây cho ≤ 10.000 bản ghi. |

### 3.5. Security — Bảo mật

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-SE08** | Authorization + Auditability (Phân quyền + Kiểm toán) | Số thay đổi cấu hình ẩn/hiện không hợp lệ; Tỷ lệ thay đổi cấu hình được ghi log đầy đủ | 0 thay đổi cấu hình ẩn/hiện do vai trò không được phép thực hiện. 100% thay đổi cấu hình ẩn/hiện khen thưởng/kỷ luật được ghi audit log với user ID, thời gian, giá trị trước/sau. |
| **SUPL-SE09** | Authorization + Auditability (Phân quyền + Kiểm toán) – Chấm dứt hợp đồng | Số trường hợp chấm dứt hợp đồng trước hạn trái phép; Tỷ lệ thao tác được ghi log đầy đủ | 0 trường hợp chấm dứt hợp đồng trước hạn trái phép. 100% thao tác chấm dứt hợp đồng trước hạn được ghi audit log với mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước/sau. |

### 4. Ma trận truy vết NFR → FEAT/UC

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F02 | FEAT 8.3, UC 4.31 | TCCB |
| | SUPL-F05 | FEAT 7.1–7.4, FEAT 8.6; UC 4.25, UC 4.26–4.28 | System Timer, TCCB |
| **Performance** | SUPL-P06 | FEAT 8.8, UC 4.34 A2 | TCCB, TCKT |

### 5.3.4. Phần đóng góp của Ngô Quang Tùng

### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F06** | Tự động cập nhật trạng thái tham gia đào tạo | Khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang trạng thái "Đang đào tạo", hệ thống tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang trạng thái "Đang học". | **M** |

### 3.1. Functionality — Yêu cầu chức năng bổ sung

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-F06** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ bản ghi đăng ký được cập nhật đúng khi khóa đào tạo chuyển trạng thái | 100% bản ghi đăng ký thuộc khóa đào tạo đó được chuyển từ trạng thái "Đã đăng ký" sang "Đang học" trong ≤ 1 phút kể từ khi khóa đào tạo chuyển sang trạng thái "Đang đào tạo". |

### 4. Ma trận truy vết NFR → FEAT/UC

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F06 | FEAT 11.2, UC 4.42 | System Timer, TCCB |

## ĐẶC TẢ YÊU CẦU BỔ SUNG (Supplementary Requirements Specification)

### Hệ thống Quản lý Nhân sự (HRMS) — Trường Đại học Thủy Lợi

> **Mã tài liệu:** HRMS-SUPL-001
> **Ngày lập:** 13/03/2026
> **Phiên bản:** 1.0
> **Tham chiếu:** Kế hoạch Quản lý Yêu cầu (RMP), Đặc tả Ca sử dụng (UCS)

---

### Mục lục

1. [Giới thiệu](#1-giới-thiệu)
2. [Danh sách yêu cầu bổ sung / yêu cầu phi chức năng](#2-danh-sách-yêu-cầu-bổ-sung--yêu-cầu-phi-chức-năng)
3. [Thiết lập độ đo và tiêu chuẩn đáp ứng](#3-thiết-lập-độ-đo-và-tiêu-chuẩn-đáp-ứng)
4. [Ma trận truy vết NFR → FEAT/UC](#4-ma-trận-truy-vết-nfr--featuc)
5. [Phân tích Softgoals và Trade-offs](#5-phân-tích-softgoals-và-trade-offs)

---

### 1. Giới thiệu

#### 1.1. Mục đích

Tài liệu này mô tả chi tiết các **yêu cầu bổ sung (Supplementary Requirements)** và **yêu cầu phi chức năng (Non-Functional Requirements - NFR)** của Hệ thống Quản lý Nhân sự (HRMS) phục vụ Trường Đại học Thủy Lợi. Các yêu cầu này **không được thể hiện** trong mô hình ca sử dụng (Use Case) nhưng vẫn là điều kiện thiết yếu để đảm bảo chất lượng và khả năng vận hành của hệ thống.

#### 1.2. Phạm vi

Tài liệu bao gồm:
- Các yêu cầu phi chức năng được phân loại theo mô hình **FURPS+** (Functionality, Usability, Reliability, Performance, Supportability + Constraints)
- Các **yếu tố chất lượng** (Quality Factors) liên quan
- Các **độ đo yêu cầu** (Metrics) cụ thể, lượng hóa được
- Các **tiêu chuẩn đáp ứng** (Acceptance Criteria) cho từng độ đo
- Các **đại lượng thay thế** (Proxies) khi NFR khó đo trực tiếp

#### 1.3. Phương pháp phân loại

Phân loại theo mô hình **FURPS+** kết hợp tham chiếu **ISO 25010**:

```
FURPS+ Classification
├── F - Functionality (Chức năng bổ sung - không thuộc UC)
├── U - Usability (Tính dễ sử dụng)
├── R - Reliability (Độ tin cậy)
├── P - Performance (Hiệu năng)
├── S - Supportability (Khả năng hỗ trợ / Bảo trì)
└── + Constraints (Các ràng buộc)
    ├── Design Constraints (Ràng buộc thiết kế)
    ├── Implementation Constraints (Ràng buộc triển khai)
    ├── Legal/Licensing (Pháp lý / Bản quyền)
    └── Physical Constraints (Ràng buộc vật lý)
```

#### 1.4. Mức độ ưu tiên

| Ký hiệu | Mức độ | Ý nghĩa |
|----------|--------|----------|
| **M** | Mandatory (Bắt buộc) | Không thể thiếu, hệ thống không đạt nghiệm thu nếu thiếu |
| **E** | Expected (Mong đợi) | Nên có, được kỳ vọng bởi phần lớn stakeholders |
| **N** | Nice to have (Có thì tốt) | Tùy chọn, không ảnh hưởng nghiệm thu |

---

### 2. Danh sách yêu cầu bổ sung / yêu cầu phi chức năng

#### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F01** | Ghi nhật ký hệ thống tự động (Auto Logging) | Hệ thống tự động ghi lại mọi hành động truy cập, thêm/sửa/xóa dữ liệu và thay đổi cấu hình với đầy đủ các thông tin: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. Tham chiếu FEAT 6.1. | **M** |
| **SUPL-F02** | Tự động sinh mã nhân sự | Khi tạo mới hồ sơ nhân sự, hệ thống tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. | **M** |
| **SUPL-F03** | Tự động đăng xuất phiên không hoạt động | Hệ thống tự động đăng xuất phiên làm việc nếu người dùng không thao tác trong 30 phút. Tham chiếu FEAT 1.3. | **M** |
| **SUPL-F04** | Tự động khóa tài khoản nhân sự thôi việc | Khi nhân sự được đánh dấu thôi việc (FEAT 8.5/8.6), hệ thống tự động chuyển tài khoản của nhân sự đó sang trạng thái khóa. Tham chiếu FEAT 2.6. | **M** |
| **SUPL-F05** | Tự động chuyển trạng thái hợp đồng | Hệ thống tự động chuyển trạng thái hợp đồng từ "Còn hiệu lực" sang "Chờ gia hạn" khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. | **M** |
| **SUPL-F06** | Tự động cập nhật trạng thái tham gia đào tạo | Khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang trạng thái "Đang đào tạo", hệ thống tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang trạng thái "Đang học". | **M** |
| **SUPL-F07** | Quy tắc nghiệp vụ chung về xóa/thay đổi trạng thái | Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ "Thay đổi trạng thái" (không hỗ trợ "Xóa") để đảm bảo tính toàn vẹn dữ liệu và phục vụ kiểm toán. Hệ số lương cho phép xóa khi chưa được hồ sơ nào sử dụng. | **M** |
| **SUPL-F08** | Bảo vệ mật khẩu lưu trữ | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. | **M** |

#### 2.2. Usability – Tính dễ sử dụng

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-U01** | Giao diện tiếng Việt và nhất quán | 100% màn hình phải sử dụng Tiếng Việt, trừ thuật ngữ kỹ thuật; đồng thời bố cục, màu sắc và font chữ phải được áp dụng thống nhất trên toàn bộ hệ thống. | **M** |
| **SUPL-U02** | Dễ học cho người dùng mới | Sau tối đa 2 giờ đào tạo hướng dẫn, ít nhất 95% người dùng mới thuộc phòng TCCB phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự; ít nhất 95% người dùng mới thuộc phòng TCKT phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. | **E** |
| **SUPL-U03** | Thông báo lỗi rõ ràng | Mọi lỗi nhập liệu hoặc lỗi hệ thống phải hiển thị thông báo bằng Tiếng Việt, rõ ràng, mô tả nguyên nhân và hướng dẫn khắc phục. | **M** |
| **SUPL-U04** | Hỗ trợ tìm kiếm và lọc đa tiêu chí | Các danh sách dữ liệu (nhân sự, hợp đồng, đơn vị) phải hỗ trợ tìm kiếm theo từ khóa và lọc đa tiêu chí để giảm thời gian thao tác. | **M** |
| **SUPL-U05** | Hiển thị ổn định trên desktop và tablet | Ở độ phân giải desktop từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang; trên tablet 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện các thao tác chính mà không cần phóng to. | **E** |
| **SUPL-U06** | Điều hướng nhanh bằng bàn phím và breadcrumb | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập; trên 100% form có nút xác nhận mặc định, phím Enter phải kích hoạt nút đó; 100% trang phải hiển thị breadcrumb để người dùng quay lại cấp điều hướng trước. | **N** |
| **SUPL-U07** | Xác nhận trước thao tác quan trọng | Hệ thống hiển thị hộp thoại xác nhận trước các thao tác quan trọng: xóa dữ liệu, khóa tài khoản, đánh dấu thôi việc, thay đổi trạng thái đơn vị. | **M** |

#### 2.3. Reliability – Độ tin cậy

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-R01** | Tính sẵn sàng cao (High Availability) | Hệ thống phải sẵn sàng phục vụ trong khung thời gian 7:00–22:00 hằng ngày với tỷ lệ uptime tối thiểu 99.5% trên tổng thời gian phục vụ trong tháng, không tính thời gian bảo trì theo kế hoạch. | **M** |
| **SUPL-R02** | Khả năng phục hồi sau sự cố | Hệ thống có khả năng khởi động lại và phục hồi hoạt động bình thường trong tối đa 15 phút sau sự cố crash/restart. | **M** |
| **SUPL-R03** | Sao lưu dữ liệu tự động | Dữ liệu nghiệp vụ và tệp đính kèm của hệ thống phải được sao lưu tự động ít nhất mỗi 24 giờ và các bản sao lưu phải được lưu giữ tối thiểu 30 ngày. | **M** |
| **SUPL-R04** | Toàn vẹn dữ liệu | Hệ thống phải bảo đảm các thao tác cập nhật dữ liệu quan trọng được thực hiện theo nguyên tắc toàn bộ hoặc không thực hiện phần nào; nếu có lỗi ở bất kỳ bước nào, dữ liệu phải được khôi phục về trạng thái trước khi thao tác bắt đầu. | **M** |
| **SUPL-R05** | Không mất dữ liệu khi phiên hết hạn | Đối với form có dữ liệu đã nhập nhưng chưa lưu, hệ thống phải cảnh báo cho người dùng trước 5 phút khi phiên làm việc sắp hết hạn và phải khôi phục lại dữ liệu đã nhập gần nhất sau khi người dùng đăng nhập lại. | **E** |

#### 2.4. Performance – Hiệu năng

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-P01** | Thời gian phản hồi giao diện | Các thao tác CRUD cơ bản (xem danh sách, xem chi tiết, thêm/sửa) trên các màn hình nhân sự, hợp đồng lao động và đánh giá khen thưởng/kỷ luật phải hoàn thành hiển thị trong thời gian phản hồi chấp nhận được tùy số người dùng đồng thời. | **M** |
| **SUPL-P02** | Số lượng người dùng đồng thời | Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời mà không suy giảm hiệu năng đáng kể (thời gian phản hồi tăng ≤ 50% so với tải thấp). | **M** |
| **SUPL-P03** | Thời gian tạo báo cáo thống kê | Dashboard thống kê và báo cáo tổng hợp (FEAT 5.1) phải hoàn thành render trong thời gian chấp nhận được. | **E** |
| **SUPL-P04** | Hiệu năng tìm kiếm và lọc | Tìm kiếm và lọc danh sách nhân sự, danh sách đánh giá khen thưởng/kỷ luật (FEAT 10.3, FEAT 8.1, FEAT 8.2) trên tập dữ liệu lớn phải trả kết quả nhanh chóng. | **M** |
| **SUPL-P05** | Hiệu năng upload/download file | Upload và download file đính kèm (PDF bằng cấp, chứng chỉ, hợp đồng) phải hoàn thành trong thời gian hợp lý. | **E** |
| **SUPL-P06** | Hiệu năng xuất Excel | Xuất danh sách nhân sự ra file Excel (FEAT 7.8) phải hoàn thành trong thời gian chấp nhận được. | **E** |

#### 2.5. Security – Bảo mật

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-SE01** | Xác thực người dùng (Authentication) | Mọi truy cập vào hệ thống phải qua xác thực bằng tài khoản/mật khẩu. Mật khẩu phải đáp ứng chính sách: tối thiểu 8 ký tự, bao gồm chữ hoa, chữ thường và số. | **M** |
| **SUPL-SE02** | Phân quyền truy cập (Authorization) | Hệ thống phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Nhân sự) – mỗi vai trò chỉ truy cập được các chức năng được cấp quyền. Mọi request API phải kiểm tra quyền trước khi xử lý. | **M** |
| **SUPL-SE03** | Bảo vệ chống tấn công brute-force | Khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp. Thời gian khóa tối thiểu 15 phút. | **M** |
| **SUPL-SE04** | Mã hóa truyền tải dữ liệu (HTTPS) | Toàn bộ giao tiếp giữa client và server phải sử dụng giao thức HTTPS (TLS 1.2 trở lên). | **M** |
| **SUPL-SE05** | Bảo vệ dữ liệu nhạy cảm | Dữ liệu nhạy cảm (số CCCD, số BHXH, thông tin ngân hàng) phải được bảo vệ – chỉ hiển thị cho vai trò được phép, ghi log khi truy cập. | **M** |
| **SUPL-SE06** | Ngăn chặn tấn công web trên chức năng nhập liệu và cập nhật dữ liệu | Hệ thống phải ngăn chặn các tấn công web làm giả yêu cầu hoặc chèn mã thực thi trên các chức năng nhập liệu và thao tác thay đổi dữ liệu. | **M** |
| **SUPL-SE07** | Chống SQL Injection | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu. | **M** |
| **SUPL-SE08** | Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật | Chỉ các vai trò được ủy quyền mới được phép cấu hình ẩn/hiện các mục khen thưởng/kỷ luật ở mức toàn hệ thống; mọi thay đổi cấu hình phải được ghi audit log với người thực hiện, thời gian, giá trị trước/sau. Tham chiếu FEAT 8.9. | **M** |
| **SUPL-SE09** | Kiểm soát chấm dứt hợp đồng trước hạn | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; hệ thống phải ghi audit log đầy đủ cho thao tác này gồm mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian và giá trị trước/sau. Tham chiếu FEAT 7.4. | **M** |

#### 2.6. Supportability – Khả năng hỗ trợ & Bảo trì

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-S01** | Kiến trúc module hóa | Hệ thống phải được tổ chức thành các module chức năng có giao diện tích hợp rõ ràng để có thể nâng cấp hoặc thay thế từng module mà không buộc sửa đổi toàn bộ hệ thống. | **M** |
| **SUPL-S02** | Tài liệu kỹ thuật đầy đủ | Cung cấp tài liệu API cho backend, hướng dẫn triển khai và hướng dẫn sử dụng cho từng vai trò. | **E** |
| **SUPL-S03** | Khả năng mở rộng danh mục cấu hình | Hệ thống cho phép mở rộng các danh mục cấu hình (loại phụ cấp, loại hợp đồng, hệ số lương) mà không cần thay đổi mã nguồn. | **M** |
| **SUPL-S04** | Hỗ trợ gỡ lỗi (Debugging) | Hệ thống ghi log lỗi phía server theo nhiều cấp độ (ERROR, WARNING, INFO, DEBUG). Log phải bao gồm timestamp, request ID, stack trace. | **E** |
| **SUPL-S05** | Khả năng mở rộng quy mô (Scalability) | Hệ thống phải duy trì đầy đủ chức năng khi năng lực xử lý được mở rộng bằng cách bổ sung thêm nút ứng dụng trong cùng một môi trường khai thác. | **N** |

#### 2.7. Design Constraints – Ràng buộc thiết kế

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-DC01** | Kiến trúc Client-Server | Hệ thống phải xây dựng theo mô hình Client-Server, frontend dạng SPA (Single Page Application) giao tiếp với backend qua RESTful API. | **M** |
| **SUPL-DC02** | Cơ cấu tổ chức dạng cây | Cơ cấu tổ chức đơn vị phải được mô hình hóa dưới dạng cấu trúc cây cha-con với gốc là Trường Đại học Thủy Lợi (FEAT 3.1). | **M** |
| **SUPL-DC03** | Tách biệt quyền theo vai trò | Thiết kế hệ thống phải đảm bảo phân tách quyền rõ ràng theo 4 vai trò đã xác định, sử dụng cơ chế Role-Based Access Control (RBAC). | **M** |

#### 2.8. Implementation Constraints – Ràng buộc triển khai

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-IC01** | Ngôn ngữ và framework | Frontend: React.js (TypeScript). Backend: Laravel/PHP. Database: MySQL/MariaDB. | **M** |
| **SUPL-IC02** | Trình duyệt hỗ trợ | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox, Edge. | **M** |
| **SUPL-IC03** | Chuẩn mã hóa ký tự | Toàn bộ hệ thống sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ Tiếng Việt có dấu. | **M** |
| **SUPL-IC04** | Định dạng file đính kèm | Hệ thống hỗ trợ upload/download file PDF (bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động) và Excel (import/export nhân sự). Kích thước file tối đa: 10MB. | **M** |

#### 2.9. Legal / Regulatory – Pháp lý

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-LR01** | Tuân thủ quy định bảo vệ dữ liệu cá nhân | Hệ thống phải hỗ trợ quản lý sự đồng ý thu thập dữ liệu cá nhân và xử lý yêu cầu hợp lệ về ẩn hoặc xóa dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP. | **M** |
| **SUPL-LR02** | Tuân thủ quy chế quản lý nhân sự | Hệ thống phải cho phép cấu hình và sử dụng bộ danh mục loại hợp đồng, phụ cấp và chức danh theo danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt trên cơ sở quy định hiện hành của Bộ GD&ĐT và Bộ NN&PTNT. | **M** |
| **SUPL-LR03** | Lưu trữ hồ sơ theo quy định | Hồ sơ nhân sự, hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu theo thời gian quy định của pháp luật lao động Việt Nam và quy chế lưu trữ hiện hành. | **M** |

---

### 3. Thiết lập độ đo và tiêu chuẩn đáp ứng

#### 3.1. Functionality — Yêu cầu chức năng bổ sung

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-F01** | Correctness (Tính đúng đắn) – Khả năng kiểm toán (Auditability) | Tỷ lệ hành động truy cập, CRUD và thay đổi cấu hình được ghi log / Tổng số hành động tương ứng phát sinh trên hệ thống | ≥ 100% các hành động truy cập, CRUD và thay đổi cấu hình đều được ghi log. Log phải bao gồm đầy đủ 9 trường thông tin (thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả, IP). |
| **SUPL-F02** | Correctness (Tính đúng đắn) | Tỷ lệ mã sinh tự động trùng lặp; Tỷ lệ mã tuân thủ mẫu mã đang áp dụng | 0% trùng lặp mã cán bộ. 100% hồ sơ nhân sự mới được cấp mã ngay khi tạo và 100% mã sinh ra tuân thủ mẫu mã đang áp dụng. |
| **SUPL-F03** | Correctness (Tính đúng đắn) – Tự động hóa | Thời gian phát hiện phiên không hoạt động | Hệ thống phát hiện và đăng xuất chính xác sau 30 phút (±30 giây) không hoạt động. |
| **SUPL-F04** | Correctness (Tính đúng đắn) – Tự động hóa | Thời gian khóa tài khoản sau khi đánh dấu thôi việc | Tài khoản bị khóa tự động trong ≤ 1 phút sau khi nhân sự được đánh dấu thôi việc. |
| **SUPL-F05** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái Chờ gia hạn đúng hạn | 100% hợp đồng đủ điều kiện được chuyển trạng thái trong ≤ 24 giờ kể từ thời điểm đủ điều kiện. |
| **SUPL-F06** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ bản ghi đăng ký được cập nhật đúng khi khóa đào tạo chuyển trạng thái | 100% bản ghi đăng ký thuộc khóa đào tạo đó được chuyển từ trạng thái "Đã đăng ký" sang "Đang học" trong ≤ 1 phút kể từ khi khóa đào tạo chuyển sang trạng thái "Đang đào tạo". |
| **SUPL-F07** | Integrity (Tính toàn vẹn) | Số trường hợp mất dữ liệu lịch sử do xóa danh mục | 0 trường hợp. Danh mục đã sử dụng không thể bị xóa, chỉ được thay đổi trạng thái. |
| **SUPL-F08** | Security (Bảo mật) | Tỷ lệ mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; Số mật khẩu lưu dạng plaintext | 100% mật khẩu được lưu ở dạng không thể khôi phục nguyên văn. 0 mật khẩu lưu dạng plaintext. |

#### 3.2. Usability — Tính dễ sử dụng

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-U01** | Usability – Tính nhất quán (Consistency) | Tỷ lệ màn hình sử dụng Tiếng Việt; Số cặp màn hình cùng loại có khác biệt về bố cục, màu sắc hoặc font chữ | 100% màn hình sử dụng Tiếng Việt (trừ thuật ngữ kỹ thuật). 0 cặp màn hình cùng loại có khác biệt về bố cục, màu sắc hoặc font chữ. |
| **SUPL-U02** | Usability – Learnability (Dễ học) | Thời gian đào tạo cho người dùng mới; Tỷ lệ người dùng mới hoàn thành bộ tác vụ cơ bản theo vai trò mà không cần trợ giúp trực tiếp | ≤ 2 giờ đào tạo. ≥ 95% người dùng mới phòng TCCB hoàn thành tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự; ≥ 95% người dùng mới phòng TCKT hoàn thành tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự. |
| **SUPL-U03** | Usability – Error Handling | Tỷ lệ lỗi có thông báo Tiếng Việt rõ ràng / Tổng số loại lỗi | 100% lỗi validation, lỗi nghiệp vụ, lỗi hệ thống đều có thông báo Tiếng Việt. Mỗi thông báo lỗi phải có ≥ 1 gợi ý khắc phục. |
| **SUPL-U04** | Usability – Efficiency (Hiệu quả thao tác) | Số bước thao tác để tìm kiếm và xem chi tiết 1 nhân sự | ≤ 3 bước (nhập từ khóa → tìm kiếm → click xem). Bộ lọc đa tiêu chí cho phép kết hợp ≥ 3 tiêu chí đồng thời. |
| **SUPL-U05** | Usability – Accessibility | Tỷ lệ màn hình không bị cắt nội dung, chồng lấn thành phần hoặc yêu cầu cuộn ngang ở 1366×768; Tỷ lệ màn hình cho phép thực hiện thao tác chính trên tablet 1024×768 mà không cần phóng to | 100% màn hình đạt tiêu chí ở độ phân giải 1366×768. ≥ 80% màn hình đạt tiêu chí trên tablet 1024×768. |
| **SUPL-U06** | Usability – Efficiency (Hiệu quả thao tác) | Tỷ lệ form hỗ trợ Tab navigation; Tỷ lệ form có nút xác nhận mặc định hỗ trợ phím Enter; Tỷ lệ trang hiển thị breadcrumb | ≥ 90% form nhập liệu hỗ trợ Tab navigation. 100% form có nút xác nhận mặc định hỗ trợ phím Enter. 100% trang có breadcrumb. |
| **SUPL-U07** | Usability – Error Prevention | Số thao tác quan trọng có hộp thoại xác nhận | 100% thao tác xóa, khóa tài khoản, thôi việc, thay đổi trạng thái đơn vị đều có confirmation dialog. |

#### 3.3. Reliability — Độ tin cậy

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-R01** | Availability (Tính sẵn sàng) | Uptime (%) = (Tổng thời gian hệ thống sẵn sàng phục vụ trong khung 7:00–22:00 / Tổng thời gian phục vụ dự kiến trong cùng khung giờ) × 100 | ≥ 99.5%/tháng trong khung 7:00–22:00, không tính bảo trì theo kế hoạch. |
| **SUPL-R02** | Recoverability (Khả năng phục hồi) | MTTR (Mean Time To Repair/Restart) | ≤ 15 phút từ lúc crash đến khi hệ thống phục vụ được request đầu tiên. |
| **SUPL-R03** | Recoverability (Khả năng phục hồi) – Sao lưu | Tần suất sao lưu; Thời gian lưu giữ bản sao lưu; RPO (Recovery Point Objective); RTO (Recovery Time Objective) | Thực hiện tối thiểu 1 bản sao lưu mỗi 24 giờ. Lưu giữ backup ≥ 30 ngày. RPO ≤ 24 giờ. RTO ≤ 4 giờ. |
| **SUPL-R04** | Integrity (Tính toàn vẹn dữ liệu) | Số trường hợp dữ liệu bất nhất quán sau thao tác lỗi; Tỷ lệ thao tác cập nhật quan trọng được khôi phục hoàn toàn khi lỗi xảy ra | 0 trường hợp dữ liệu bất nhất quán. 100% thao tác cập nhật quan trọng hoặc hoàn tất toàn bộ, hoặc không làm thay đổi dữ liệu khi có lỗi. |
| **SUPL-R05** | Fault Tolerance (Chịu lỗi) | Tỷ lệ form có dữ liệu nhập dở được khôi phục sau khi phiên hết hạn; Tỷ lệ phiên hết hạn có cảnh báo trước | ≥ 95% form có dữ liệu nhập dở được khôi phục sau khi người dùng đăng nhập lại. 100% phiên hết hạn hiển thị cảnh báo trước 5 phút. |

#### 3.4. Performance — Hiệu năng

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-P01** | Speed (Tốc độ phản hồi) | Response time (giây) – P95 response time cho các thao tác CRUD | Theo bảng tải: **0–10 người dùng:** ≤ 1 giây; **11–50 người dùng:** ≤ 2 giây; **51–100 người dùng:** ≤ 5 giây; **>100 người dùng:** ≤ 10 giây. |
| **SUPL-P02** | Capacity (Dung lượng / Khả năng chịu tải) | Số người dùng đồng thời tối đa mà hệ thống phục vụ được | ≥ 100 concurrent users. Tại 100 users, response time tăng ≤ 50% so với tải 1 user. Throughput ≥ 50 transactions/second. |
| **SUPL-P03** | Speed (Tốc độ) – Báo cáo | Thời gian render dashboard/báo cáo | Dashboard: ≤ 5 giây. Báo cáo tổng hợp phức tạp: ≤ 15 giây. Biểu đồ thống kê: ≤ 3 giây/biểu đồ. |
| **SUPL-P04** | Speed (Tốc độ) – Tìm kiếm | Thời gian trả kết quả tìm kiếm/lọc | ≤ 2 giây trên tập dữ liệu ≤ 10.000 bản ghi. ≤ 5 giây trên tập dữ liệu ≤ 50.000 bản ghi. |
| **SUPL-P05** | Speed (Tốc độ) – File I/O | Thời gian upload/download file | Upload: ≤ 5 giây cho file ≤ 5MB. Download: ≤ 3 giây cho file ≤ 5MB (trên mạng LAN). |
| **SUPL-P06** | Speed (Tốc độ) – Xuất dữ liệu | Thời gian xuất Excel | ≤ 10 giây cho ≤ 1.000 bản ghi. ≤ 30 giây cho ≤ 10.000 bản ghi. |

#### 3.5. Security — Bảo mật

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-SE01** | Authentication (Xác thực) | Chính sách mật khẩu; Số level xác thực | Mật khẩu ≥ 8 ký tự, chứa chữ hoa + chữ thường + số. 1 level xác thực (username/password). Token-based session management (JWT hoặc session cookie). |
| **SUPL-SE02** | Authorization (Phân quyền) | Số trường hợp truy cập trái phép (unauthorized access) phát hiện qua penetration test | 0 trường hợp unauthorized access. 100% API endpoint có middleware kiểm tra quyền. 4 vai trò phân quyền rõ ràng (RBAC). |
| **SUPL-SE03** | Integrity (Tính toàn vẹn) – Chống brute-force | Số lần đăng nhập sai trước khi khóa; Thời gian khóa | Khóa tài khoản sau 5 lần sai liên tiếp. Thời gian khóa: 15 phút. Ghi log cảnh báo khi phát hiện brute-force. |
| **SUPL-SE04** | Confidentiality (Bảo mật truyền tải) | Phiên bản TLS; Tỷ lệ kết nối sử dụng HTTPS | TLS ≥ 1.2. 100% kết nối qua HTTPS. 0 kết nối HTTP không mã hóa được phép. |
| **SUPL-SE05** | Confidentiality (Bảo mật dữ liệu) | Số trường dữ liệu nhạy cảm không được bảo vệ | 0 trường nhạy cảm hiển thị cho vai trò không được phép. 100% truy cập dữ liệu nhạy cảm (CCCD, BHXH, ngân hàng) được ghi audit log. |
| **SUPL-SE06** | Integrity – Chống tấn công web | Số lỗ hổng tấn công web phát hiện qua kiểm thử bảo mật | 0 lỗ hổng CSRF. 0 lỗ hổng XSS. 100% chức năng POST/PUT/DELETE vượt qua kiểm thử chống CSRF và 100% dữ liệu hiển thị từ input người dùng vượt qua kiểm thử XSS. |
| **SUPL-SE07** | Integrity – Chống tấn công database | Số lỗ hổng SQL Injection phát hiện qua kiểm thử | 0 lỗ hổng SQL Injection. 100% truy vấn truy cập dữ liệu tách dữ liệu đầu vào khỏi câu lệnh thực thi SQL. |
| **SUPL-SE08** | Authorization + Auditability (Phân quyền + Kiểm toán) | Số thay đổi cấu hình ẩn/hiện không hợp lệ; Tỷ lệ thay đổi cấu hình được ghi log đầy đủ | 0 thay đổi cấu hình ẩn/hiện do vai trò không được phép thực hiện. 100% thay đổi cấu hình ẩn/hiện khen thưởng/kỷ luật được ghi audit log với user ID, thời gian, giá trị trước/sau. |
| **SUPL-SE09** | Authorization + Auditability (Phân quyền + Kiểm toán) – Chấm dứt hợp đồng | Số trường hợp chấm dứt hợp đồng trước hạn trái phép; Tỷ lệ thao tác được ghi log đầy đủ | 0 trường hợp chấm dứt hợp đồng trước hạn trái phép. 100% thao tác chấm dứt hợp đồng trước hạn được ghi audit log với mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước/sau. |

#### 3.6. Supportability — Khả năng hỗ trợ & Bảo trì

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-S01** | Maintainability – Modularity (Tính module) | Mức phụ thuộc liên module; Số thay đổi lan truyền khi sửa 1 module | Thay đổi 1 module không yêu cầu thay đổi ≥ 2 module khác. 100% giao diện tích hợp giữa các module được đặc tả và kiểm thử độc lập. |
| **SUPL-S02** | Maintainability – Understandability | Tỷ lệ API có tài liệu; Tỷ lệ trang có hướng dẫn sử dụng | ≥ 90% API endpoint có mô tả trong tài liệu. 100% chức năng chính có hướng dẫn sử dụng. |
| **SUPL-S03** | Flexibility (Tính linh hoạt) | Số danh mục cấu hình có thể mở rộng không cần sửa code | ≥ 3 loại danh mục (hệ số lương, loại phụ cấp, loại hợp đồng) mở rộng qua giao diện quản trị. 0 thay đổi mã nguồn cần thiết khi thêm danh mục mới. |
| **SUPL-S04** | Testability (Khả năng kiểm thử) – Logging | Số cấp độ log được hỗ trợ; Thông tin trong mỗi log entry | ≥ 4 cấp độ (ERROR, WARNING, INFO, DEBUG). Mỗi entry có: timestamp, request ID, user ID, stack trace (cho ERROR). |
| **SUPL-S05** | Scalability (Khả năng mở rộng) | Số nút ứng dụng có thể chạy song song; Tỷ lệ request liên tiếp hoạt động đúng qua nhiều nút | Hỗ trợ ≥ 2 nút ứng dụng chạy song song trong cùng môi trường. 100% request liên tiếp của cùng người dùng hoạt động đúng khi được phân phối qua các nút ứng dụng khác nhau. |

#### 3.7. Constraints — Ràng buộc

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-DC01** | Portability – Kiến trúc | Tuân thủ mô hình Client-Server, RESTful API | 100% giao tiếp client-server qua RESTful API (JSON). Frontend là SPA (Single Page Application). |
| **SUPL-DC02** | Correctness – Mô hình dữ liệu | Kiểm tra cấu trúc cây đơn vị | 100% đơn vị tổ chức nằm trong cấu trúc cây cha-con hợp lệ. Gốc duy nhất: Trường ĐHTL. Không có cycle. |
| **SUPL-DC03** | Security – Thiết kế | Số vai trò được định nghĩa; Mô hình phân quyền | RBAC với 4 vai trò. 100% chức năng có ma trận phân quyền rõ ràng. |
| **SUPL-IC01** | Portability – Công nghệ | Stack công nghệ tuân thủ | React.js (TypeScript) + Laravel/PHP + MySQL/MariaDB. |
| **SUPL-IC02** | Compatibility – Trình duyệt | Số trình duyệt hỗ trợ; Tỷ lệ chức năng hoạt động đúng | ≥ 3 trình duyệt (Chrome, Firefox, Edge). 100% chức năng hoạt động trên Chrome mới nhất. ≥ 95% trên Firefox và Edge. |
| **SUPL-IC03** | Portability – Mã hóa | Encoding sử dụng | UTF-8 trên toàn bộ hệ thống. 0 lỗi hiển thị Tiếng Việt có dấu. |
| **SUPL-IC04** | Correctness – File | Định dạng và kích thước file hỗ trợ | PDF và Excel. Kích thước tối đa: 10MB/file. Thông báo lỗi nếu vượt quá. |
| **SUPL-LR01** | Legal – Bảo vệ dữ liệu | Tỷ lệ trường hợp xử lý dữ liệu có bản ghi đồng ý hợp lệ; Tỷ lệ yêu cầu ẩn/xóa dữ liệu được xử lý đúng | 100% trường hợp thuộc diện phải xin đồng ý có bản ghi đồng ý hợp lệ trước khi xử lý dữ liệu. 100% yêu cầu hợp lệ về ẩn hoặc xóa dữ liệu cá nhân được thực hiện và lưu vết xử lý. |
| **SUPL-LR02** | Legal – Quy chế nhân sự | Tỷ lệ mục trong bộ danh mục phê duyệt được cấu hình và sử dụng được; Số mục trái danh mục phê duyệt | 100% loại hợp đồng, phụ cấp và chức danh trong bộ danh mục nhân sự phê duyệt được cấu hình và sử dụng được trên hệ thống. 0 mục trái bộ danh mục phê duyệt được đưa vào nghiệm thu. |
| **SUPL-LR03** | Legal – Lưu trữ | Thời gian lưu trữ tối thiểu | Hồ sơ nhân sự lưu ≥ 75 năm (theo Luật Lưu trữ). Hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật lưu ≥ 10 năm sau khi kết thúc hoặc sau bản ghi cuối cùng. |

---

### 4. Ma trận truy vết NFR → FEAT/UC

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F01 | FEAT 6.1, UC Auto Logging | System Timer |
| | SUPL-F02 | FEAT 8.3, UC 4.31 | TCCB |
| | SUPL-F03 | FEAT 1.3, UC 4.2 A1 | System Timer |
| | SUPL-F04 | FEAT 2.6, UC 4.8 A2 | System Timer |
| | SUPL-F05 | FEAT 7.1–7.4, FEAT 8.6; UC 4.25, UC 4.26–4.28 | System Timer, TCCB |
| | SUPL-F06 | FEAT 11.2, UC 4.42 | System Timer, TCCB |
| | SUPL-F07 | FEAT 4.3–4.5 | TCCB |
| | SUPL-F08 | FEAT 1.1, UC 4.1 | Tất cả |
| **Usability** | SUPL-U01 → U07 | Toàn bộ FEAT/UC | Tất cả |
| **Reliability** | SUPL-R01 → R05 | Toàn bộ hệ thống | Phòng CNTT |
| **Performance** | SUPL-P01 | Toàn bộ FEAT/UC; FEAT 7.2, 7.3, 10.2; UC 4.26, 4.27, 4.39 | Tất cả |
| | SUPL-P02 | Toàn bộ hệ thống | Phòng CNTT |
| | SUPL-P03 | FEAT 5.1, UC 4.23 | TCCB, TCKT |
| | SUPL-P04 | FEAT 10.3, FEAT 8.1, FEAT 8.2; UC 4.29, UC 4.30, UC 4.40 | TCCB, TCKT |
| | SUPL-P05 | BangCap, ChungChi, HopDong files | TCCB |
| | SUPL-P06 | FEAT 8.8, UC 4.34 A2 | TCCB, TCKT |
| **Security** | SUPL-SE01 → SE09 | FEAT 1.1, 2.4, 7.4, 10.2, 10.3, 8.9, 6.1, 6.2; UC 4.28, 4.35, 4.39–4.40 | Admin, TCCB, TCKT, System |
| **Supportability** | SUPL-S01 → S05 | Toàn bộ hệ thống | Nhóm phát triển |
| **Constraints** | SUPL-DC01 → IC04, LR01 → LR03 | Toàn bộ hệ thống; FEAT 10.2, UC 4.39 | Tất cả stakeholders |

---

### 5. Phân tích Softgoals và Trade-offs

#### 5.1. Các Softgoal chính của hệ thống HRMS

```
                 Chất lượng hệ thống HRMS
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
   Bảo mật cao     Hiệu năng tốt    Dễ sử dụng
   (Security)      (Performance)     (Usability)
        │                 │                 │
   ┌────┴────┐      ┌────┴────┐      ┌────┴────┐
   │         │      │         │      │         │
 Mã hóa   RBAC   Caching   Index  UI đơn   Tìm kiếm
 mạnh    chặt    dữ liệu  DB     giản     thông minh
```

#### 5.2. Phân tích Trade-offs

| Trade-off | Softgoal A | Softgoal B | Quyết định |
|-----------|------------|------------|------------|
| **Bảo mật vs Dễ sử dụng** | Mật khẩu phức tạp + tự động đăng xuất 30 phút | Người dùng phải đăng nhập lại thường xuyên | Ưu tiên bảo mật (M) – bù bằng cảnh báo 5 phút trước khi hết phiên |
| **Bảo mật vs Hiệu năng** | Kiểm tra quyền trên mọi API request | Tăng overhead cho mỗi request | Ưu tiên bảo mật (M) – tối ưu bằng caching quyền theo phiên |
| **Toàn vẹn dữ liệu vs Linh hoạt** | Không cho xóa danh mục đã sử dụng | Người dùng muốn dọn dẹp dữ liệu cũ | Ưu tiên toàn vẹn (M) – hỗ trợ "Ngừng sử dụng" thay thế |
| **Audit Log đầy đủ vs Hiệu năng** | Ghi log 100% hành động | Tăng I/O database | Ưu tiên audit (M) – sử dụng async logging hoặc separate log table |
| **Responsive design vs Thời gian phát triển** | Hỗ trợ đa thiết bị | Tăng effort thiết kế/kiểm thử | Ưu tiên desktop (M) – tablet hỗ trợ cơ bản (E) |

#### 5.3. Minh họa mô hình McCall áp dụng cho HRMS

```
Product Operation (Vận hành sản phẩm)
├── Correctness ───── SUPL-F01→F08, SUPL-DC02, SUPL-IC03, SUPL-IC04
├── Reliability ───── SUPL-R01→R05
├── Efficiency ────── SUPL-P01→P06
├── Integrity ─────── SUPL-SE01→SE07, SUPL-F07
└── Usability ─────── SUPL-U01→U07

Product Revision (Sửa đổi sản phẩm)
├── Maintainability ── SUPL-S01, SUPL-S02
├── Flexibility ────── SUPL-S03
└── Testability ────── SUPL-S04

Product Transition (Chuyển đổi sản phẩm)
├── Portability ────── SUPL-DC01, SUPL-IC01, SUPL-IC02, SUPL-IC03
├── Reusability ────── SUPL-S01 (kiến trúc module)
└── Interoperability ─ SUPL-IC04 (hỗ trợ Excel/PDF)
```

---

### Phụ lục A: Bảng tổng hợp nhanh — Quality Factor × Metric × Acceptance Criteria

> Bảng tóm tắt dạng đặc tả bổ sung (Supplementary Specification Table) theo format bài tập nhóm.

| # | Quality Factor | Metric | Acceptance Criteria | Priority |
|---|---------------|--------|---------------------|----------|
| 1 | **Performance – Speed** | P95 Response time (CRUD) | ≤ 2s (≤50 users), ≤ 5s (≤100 users) | M |
| 2 | **Performance – Capacity** | Concurrent users | ≥ 100 users, throughput ≥ 50 tx/s | M |
| 3 | **Performance – Search** | Search/filter response time | ≤ 2s (≤10K records) | M |
| 4 | **Performance – Report** | Dashboard render time | ≤ 5s dashboard, ≤ 15s complex report | E |
| 5 | **Performance – Export** | Excel export time | ≤ 10s (≤1K records), ≤ 30s (≤10K) | E |
| 6 | **Performance – File I/O** | Upload/download time (≤5MB) | Upload ≤ 5s, Download ≤ 3s | E |
| 7 | **Reliability – Availability** | Uptime percentage | ≥ 99.5%/month, MTBF ≥ 720h | M |
| 8 | **Reliability – Recoverability** | MTTR | ≤ 15 minutes | M |
| 9 | **Reliability – Backup** | RPO / RTO | RPO ≤ 24h, RTO ≤ 4h | M |
| 10 | **Reliability – Integrity** | Data inconsistency count | 0 cases | M |
| 11 | **Security – Authentication** | Password policy; session management | ≥ 8 chars (upper+lower+digit); token-based | M |
| 12 | **Security – Authorization** | Unauthorized access count | 0 cases, 100% endpoints protected | M |
| 13 | **Security – Brute-force** | Lock threshold | Lock after 5 failures, 15min cooldown | M |
| 14 | **Security – Encryption** | TLS version | ≥ TLS 1.2, 100% HTTPS | M |
| 15 | **Security – Data Protection** | Exposed sensitive fields | 0 fields exposed to unauthorized roles | M |
| 16 | **Security – Web Attacks** | CSRF/XSS vulnerabilities | 0 vulnerabilities | M |
| 17 | **Security – SQL Injection** | SQLi vulnerabilities | 0 vulnerabilities, 100% prepared statements | M |
| 18 | **Security – Visibility Configuration Control** | Unauthorized visibility config changes; audit coverage | 0 unauthorized changes, 100% changes logged with before/after values | M |
| 19 | **Security – Early Contract Termination Control** | Unauthorized early termination count; audit coverage | 0 unauthorized terminations, 100% thao tác được ghi log đầy đủ | M |
| 20 | **Usability – Consistency** | UI violations | 0 pages violating design system | M |
| 21 | **Usability – Learnability** | Training time | ≤ 2 hours for basic functions | E |
| 22 | **Usability – Error Handling** | Vietnamese error messages | 100% with fix suggestions | M |
| 23 | **Usability – Efficiency** | Steps to search+view employee | ≤ 3 steps | M |
| 24 | **Usability – Responsive** | Correct display at target resolutions | 100% at ≥1366×768 | E |
| 25 | **Usability – Confirmation** | Critical actions with dialog | 100% delete/lock/terminate actions | M |
| 26 | **Supportability – Modularity** | Module coupling | Change in 1 module → ≤ 1 other module affected | M |
| 27 | **Supportability – Documentation** | API doc coverage | ≥ 90% endpoints documented | E |
| 28 | **Supportability – Flexibility** | Config categories extendable via UI | ≥ 3 categories, 0 code changes needed | M |
| 29 | **Supportability – Logging** | Log levels supported | ≥ 4 levels (ERROR/WARN/INFO/DEBUG) | E |
| 30 | **Supportability – Scalability** | Horizontal scaling support | ≥ 2 instances behind load balancer | N |
| 31 | **Correctness – Auto Logging** | Action log coverage | 100% CRUD actions logged with 9 fields | M |
| 32 | **Correctness – Auto Processes** | Auto status transition accuracy | 100% correct, ≤ 24h delay | M |
| 33 | **Integrity – Data Retention** | Catalog deletion prevention | 0 used catalogs deletable | M |
| 34 | **Legal – Data Privacy** | Compliance with ND 13/2023 | Full compliance | M |
| 35 | **Legal – Records Retention** | Retention period for HR/contract/evaluation history | Hồ sơ nhân sự ≥ 75 năm; hợp đồng và lịch sử đánh giá/khen thưởng/kỷ luật ≥ 10 năm | M |
| 36 | **Compatibility – Browser** | Supported browsers | Chrome + Firefox + Edge, 100% on Chrome | M |
| 37 | **Portability – Encoding** | UTF-8 compliance | 0 Vietnamese display errors | M |

---

> **Ghi chú cuối:** Tài liệu này bổ sung cho Đặc tả Ca sử dụng (UCS) và phải được đọc cùng với tài liệu RMP và các UC 4.1–4.48 để có cái nhìn toàn diện về yêu cầu hệ thống.

## THIẾT LẬP ĐỘ ĐO YÊU CẦU VÀ TIÊU CHUẨN ĐÁP ỨNG

### Hệ thống HRMS — Trường Đại học Thủy Lợi

> Tài liệu này trình bày chi tiết việc **thiết lập độ đo** (Metrics), **xác định yếu tố chất lượng** (Quality Factors) và **tiêu chuẩn đáp ứng** (Acceptance Criteria) cho từng yêu cầu bổ sung/phi chức năng đã được liệt kê trong [supplementary-requirements.md](./supplementary-requirements.md). Khi NFR khó đo trực tiếp, sử dụng **đại lượng thay thế** (Proxy).
>
> **Ghi chú cập nhật phạm vi:** Các độ đo có phạm vi áp dụng kiểu **toàn bộ FEAT/UC**, **toàn bộ hệ thống**, hoặc **mọi hành động CRUD và truy cập** mặc nhiên bao phủ cả các use case được bổ sung sau mở rộng phạm vi, bao gồm **UC 4.43 – UC 4.48** tương ứng **FEAT 5.2 – 5.4, FEAT 6.2 – 6.3, FEAT 7.9**. Với các độ đo đang tham chiếu FEAT/UC cụ thể, phạm vi áp dụng được cập nhật tường minh trong tài liệu này để tránh thiếu bao phủ truy vết.

---

### 1. SUPL-P01 — Thời gian phản hồi giao diện

**Yêu cầu gốc:** Các thao tác CRUD cơ bản phải đáp ứng các ngưỡng P95 Response Time và Time to Interactive (TTI) theo tải đồng thời được quy định tại phần tiêu chuẩn đáp ứng.

#### Yếu tố chất lượng
- **Nhóm:** Performance (Hiệu năng)
- **Yếu tố:** Speed — Tốc độ phản hồi (Response Time)
- **Mô hình tham chiếu:** ISO 25010 → Performance Efficiency → Time Behaviour

#### Độ đo yêu cầu (Metrics)
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| P95 Response Time cho CRUD | Giây (s) | Đo bằng công cụ load test (JMeter, k6) — lấy phân vị 95 của thời gian từ lúc gửi request đến nhận response |
| Time to Interactive (TTI) | Giây (s) | Đo trên trình duyệt — thời gian từ click đến giao diện sẵn sàng tương tác |
| Contract List Load Time | Giây (s) | Thời gian từ mở màn hình danh sách hợp đồng đến khi danh sách hiển thị đầy đủ và sẵn sàng tương tác |
| Contract Detail Load Time | Giây (s) | Thời gian từ click một hợp đồng đến khi màn hình chi tiết hợp đồng hiển thị ổn định |
| Contract Termination Response Time | Giây (s) | Thời gian từ xác nhận chấm dứt hợp đồng trước hạn đến khi hệ thống ghi nhận thành công và cập nhật trạng thái |

#### Tiêu chuẩn đáp ứng

| Số người dùng đồng thời | P95 Response Time tối đa | TTI tối đa |
|--------------------------|--------------------------|------------|
| 0 – 10 | ≤ 1 giây | ≤ 1.5 giây |
| 11 – 50 | ≤ 2 giây | ≤ 3 giây |
| 51 – 100 | ≤ 5 giây | ≤ 6 giây |
| > 100 | ≤ 10 giây | ≤ 12 giây |

- Các ngưỡng trên được áp dụng cho toàn bộ thao tác xem/thêm/sửa cơ bản trên hệ thống, bao gồm cả **FEAT 5.2 – 5.4 / UC 4.43 – UC 4.45**.
- **Contract List Load Time**, **Contract Detail Load Time** và **Contract Termination Response Time** kế thừa trực tiếp ngưỡng **P95 Response Time** và **TTI** theo tải đồng thời tương ứng trong bảng trên.

#### Đại lượng thay thế (Proxy)
- Không cần proxy — có thể đo trực tiếp bằng load test tool.

---

### 2. SUPL-P02 — Số lượng người dùng đồng thời

**Yêu cầu gốc:** Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời.

#### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Capacity — Khả năng chịu tải
- **Mô hình tham chiếu:** ISO 25010 → Performance Efficiency → Capacity

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Max Concurrent Users | Số người | Stress test — tăng dần số kết nối đồng thời cho đến khi response time vượt ngưỡng |
| Throughput | Transactions/giây (tx/s) | Load test — đếm số giao dịch hoàn thành trong 1 giây |
| Degradation Rate | % | So sánh response time tại tải cao vs tải thấp |

#### Tiêu chuẩn đáp ứng
- Max Concurrent Users ≥ **100 người**
- Throughput ≥ **50 tx/s** tại 100 concurrent users
- Degradation Rate ≤ **50%** (response time tại 100 users so với 1 user)

#### Đại lượng thay thế
- **Proxy:** Số kết nối TCP/WebSocket mà server duy trì ổn định (đo trên server monitoring)

---

### 3. SUPL-P03 — Thời gian tạo báo cáo thống kê

**Yêu cầu gốc:** Dashboard và báo cáo tổng hợp (FEAT 10.1) phải hoàn thành tải và hiển thị trong các ngưỡng thời gian quy định tại phần tiêu chuẩn đáp ứng.

#### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ xử lý và hiển thị báo cáo

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Dashboard Load Time | Giây | Thời gian từ navigate đến dashboard sẵn sàng hiển thị đầy đủ biểu đồ |
| Complex Report Generation Time | Giây | Thời gian từ click "Tạo báo cáo" đến hiển thị/download hoàn tất |
| Single Chart Render Time | Giây | Thời gian render 1 biểu đồ thống kê |

#### Tiêu chuẩn đáp ứng
- Dashboard Load Time ≤ **5 giây**
- Complex Report Generation ≤ **15 giây**
- Single Chart Render ≤ **3 giây**

#### Đại lượng thay thế
- **Proxy:** Thời gian truy vấn SQL của các query thống kê (đo qua slow query log) — mục tiêu ≤ 2 giây/query

---

### 4. SUPL-P04 — Hiệu năng tìm kiếm và lọc

**Yêu cầu gốc:** Tìm kiếm và lọc trên các danh sách chính của hệ thống phải trả kết quả trong các ngưỡng thời gian quy định theo quy mô dữ liệu tại phần tiêu chuẩn đáp ứng.

#### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ truy vấn dữ liệu

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Search Response Time | Giây | Thời gian từ submit tìm kiếm đến hiển thị kết quả — áp dụng cho danh sách nhân sự, hợp đồng và đánh giá nếu chức năng có hỗ trợ tìm kiếm/lọc |
| Filter Apply Time | Giây | Thời gian từ áp dụng bộ lọc đến danh sách cập nhật — áp dụng cho danh sách nhân sự, hợp đồng và đánh giá nếu chức năng có hỗ trợ tìm kiếm/lọc |

#### Tiêu chuẩn đáp ứng

| Quy mô dữ liệu | Search Response Time | Filter Apply Time |
|------------------|----------------------|--------------------|
| ≤ 10.000 bản ghi | ≤ 2 giây | ≤ 2 giây |
| ≤ 50.000 bản ghi | ≤ 5 giây | ≤ 5 giây |

- **Ghi chú phạm vi:** Các độ đo Search Response Time và Filter Apply Time áp dụng cho danh sách nhân sự, hợp đồng và đánh giá nếu chức năng có hỗ trợ tìm kiếm/lọc. Trong đó **FEAT 6.3 / UC 4.47** thuộc phạm vi bắt buộc áp dụng; các màn hình hợp đồng thuộc **FEAT 5.2 – 5.4 / UC 4.43 – UC 4.45** kế thừa độ đo này nếu bổ sung bộ lọc hoặc ô tìm kiếm.

#### Đại lượng thay thế
- **Proxy:** Execution time của câu truy vấn SQL LIKE/FULLTEXT (qua EXPLAIN ANALYZE) — mục tiêu ≤ 500ms cho ≤ 10K records

---

### 5. SUPL-P05 — Hiệu năng upload/download file

**Yêu cầu gốc:** Việc tải lên và tải xuống tệp đính kèm dung lượng đến 5 MB phải hoàn thành trong các ngưỡng thời gian quy định tại phần tiêu chuẩn đáp ứng trên mạng LAN.

#### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ truyền file (File I/O)

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Upload Time | Giây | Thời gian từ chọn file đến server xác nhận lưu thành công |
| Download Time | Giây | Thời gian từ click download đến file sẵn sàng mở |

#### Tiêu chuẩn đáp ứng
- Upload ≤ **5 giây** cho file ≤ 5MB (trên mạng LAN)
- Download ≤ **3 giây** cho file ≤ 5MB (trên mạng LAN)

#### Đại lượng thay thế
- **Proxy:** Tốc độ ghi file vào disk (MB/s) — đo qua server I/O monitoring

---

### 6. SUPL-P06 — Hiệu năng xuất Excel

**Yêu cầu gốc:** Chức năng xuất dữ liệu ra Excel phải hoàn thành trong các ngưỡng thời gian quy định theo số bản ghi tại phần tiêu chuẩn đáp ứng.

#### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ xuất dữ liệu

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Export Time | Giây | Thời gian từ click "Xuất Excel" đến file download hoàn tất |

#### Tiêu chuẩn đáp ứng
| Số bản ghi | Export Time tối đa |
|------------|---------------------|
| ≤ 1.000 | ≤ 10 giây |
| ≤ 10.000 | ≤ 30 giây |

#### Đại lượng thay thế
- **Proxy:** Thời gian server sinh file Excel (không tính download) — đo qua API response time

---

### 7. SUPL-R01 — Tính sẵn sàng cao (Availability)

**Yêu cầu gốc:** Hệ thống phải đạt uptime tối thiểu 99,5% trong khung giờ 7:00–22:00 hằng ngày và tổng downtime ngoài bảo trì kế hoạch không được vượt quá 2,25 giờ/tháng.

#### Yếu tố chất lượng
- **Nhóm:** Reliability (Độ tin cậy)
- **Yếu tố:** Availability — Tính sẵn sàng
- **Mô hình McCall:** Product Operation → Reliability

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Công thức / Phương pháp đo |
|-------|--------|----------------------------|
| Uptime | % | (Tổng thời gian hoạt động / Tổng thời gian dự kiến) × 100 |
| MTBF (Mean Time Between Failures) | Giờ | Tổng thời gian hoạt động / Số lần failure |
| Downtime | Giờ/tháng | Tổng thời gian hệ thống không truy cập được (không tính bảo trì kế hoạch) |

#### Tiêu chuẩn đáp ứng
- Uptime ≥ **99.5%/tháng** (trong khung giờ 7:00–22:00)
- MTBF ≥ **720 giờ** (tương đương 30 ngày)
- Downtime ≤ **2.25 giờ/tháng** (không tính bảo trì kế hoạch)

#### Đại lượng thay thế
- **Proxy:** Số lần health check endpoint trả về lỗi / Tổng số health check (đo qua uptime monitoring tool như UptimeRobot)

---

### 8. SUPL-R02 — Khả năng phục hồi sau sự cố

**Yêu cầu gốc:** Sau sự cố crash hoặc restart, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa 15 phút.

#### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Recoverability — Khả năng phục hồi

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| MTTR (Mean Time To Repair) | Phút | Thời gian từ lúc crash đến khi hệ thống phục vụ được request đầu tiên thành công |
| Restart Time | Phút | Thời gian restart toàn bộ stack (DB + Backend + Frontend) |

#### Tiêu chuẩn đáp ứng
- MTTR ≤ **15 phút**
- Restart Time ≤ **10 phút**

#### Đại lượng thay thế
- Không cần — có thể đo trực tiếp qua drill test (mô phỏng sự cố)

---

### 9. SUPL-R03 — Sao lưu dữ liệu tự động

**Yêu cầu gốc:** Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi 24 giờ, lưu giữ bản sao lưu tối thiểu 30 ngày và phục hồi được từ bản sao lưu trong tối đa 4 giờ.

#### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Recoverability — Sao lưu và phục hồi dữ liệu

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| RPO (Recovery Point Objective) | Giờ | Khoảng thời gian dữ liệu có thể mất tối đa khi phục hồi từ backup |
| RTO (Recovery Time Objective) | Giờ | Thời gian tối đa để phục hồi hệ thống từ backup |
| Backup Retention Period | Ngày | Số ngày lưu giữ bản sao lưu |
| Backup Success Rate | % | Số lần backup thành công / Tổng số lần backup chạy |

#### Tiêu chuẩn đáp ứng
- RPO ≤ **24 giờ**
- RTO ≤ **4 giờ**
- Backup Retention ≥ **30 ngày**
- Backup Success Rate ≥ **99%**

#### Đại lượng thay thế
- **Proxy cho RTO:** Thời gian restore database từ backup gần nhất trên môi trường staging

---

### 10. SUPL-R04 — Toàn vẹn dữ liệu

**Yêu cầu gốc:** Các thao tác cập nhật dữ liệu quan trọng phải bảo toàn tính nhất quán; nếu một bước thất bại, hệ thống không được ghi nhận thay đổi dở dang.

#### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Integrity — Tính toàn vẹn dữ liệu
- **Mô hình McCall:** Product Operation → Integrity

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Data Inconsistency Count | Số trường hợp | Kiểm tra dữ liệu bất nhất quán sau thao tác lỗi (failure-injection test) |
| Integrity Protection Coverage | % | Tỷ lệ thao tác cập nhật quan trọng được kiểm thử lỗi giữa chừng mà không phát sinh cập nhật dở dang |

#### Tiêu chuẩn đáp ứng
- Data Inconsistency Count = **0**
- Integrity Protection Coverage = **100%** cho hợp đồng, bổ nhiệm, đánh giá, chuyển trạng thái
- Không được ghi nhận thay đổi một phần khi có lỗi giữa chừng

#### Đại lượng thay thế
- **Proxy:** Số Foreign Key violations và orphaned records phát hiện qua integrity check script

---

### 11. SUPL-R05 — Không mất dữ liệu khi phiên hết hạn

**Yêu cầu gốc:** Trước khi phiên tự động hết hạn, hệ thống phải cảnh báo tối thiểu 5 phút; nếu phiên vẫn hết hạn, tỷ lệ mất dữ liệu biểu mẫu chưa lưu không được vượt quá 5%.

#### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Fault Tolerance — Chịu lỗi

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Data Loss Rate | % | Tỷ lệ trường hợp mất dữ liệu form khi phiên hết hạn (user testing) |
| Warning Lead Time | Phút | Thời gian cảnh báo trước khi phiên hết hạn |

#### Tiêu chuẩn đáp ứng
- Data Loss Rate ≤ **5%**
- Warning Lead Time ≥ **5 phút** trước khi tự động đăng xuất

#### Đại lượng thay thế
- **Proxy:** Có/Không hiển thị popup cảnh báo (binary kiểm thử) — thay vì đo tỷ lệ mất dữ liệu thực tế

---

### 12. SUPL-SE01 — Xác thực người dùng (Authentication)

**Yêu cầu gốc:** Mọi truy cập vào hệ thống phải được xác thực bằng tên đăng nhập và mật khẩu; mật khẩu phải có ít nhất 8 ký tự và bao gồm chữ hoa, chữ thường, chữ số.

#### Yếu tố chất lượng
- **Nhóm:** Security (Bảo mật)
- **Yếu tố:** Authentication — Xác thực danh tính
- **Mô hình McCall:** Product Operation → Integrity

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Password Strength Level | Số quy tắc | Đếm số quy tắc mật khẩu được enforce (độ dài, chữ hoa, chữ thường, số) |
| Authentication Levels | Số level | Số lớp xác thực trước khi truy cập hệ thống |
| Session Security | Có/Không | Kiểm tra cơ chế phiên có chặn truy cập từ script phía client và có thời điểm hết hiệu lực |

#### Tiêu chuẩn đáp ứng
- Mật khẩu ≥ **8 ký tự**, chứa chữ hoa + chữ thường + số (3 quy tắc)
- **1 level** xác thực (tên đăng nhập/mật khẩu)
- Phiên xác thực phải chặn truy cập từ script phía client và tự hết hiệu lực sau tối đa **30 phút** không hoạt động

#### Đại lượng thay thế
- **Proxy cho Password Strength:** Số mật khẩu yếu trong hệ thống (kiểm tra bằng password audit script)

---

### 13. SUPL-SE02 — Phân quyền truy cập (Authorization)

**Yêu cầu gốc:** Hệ thống phải phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Nhân sự); mỗi vai trò chỉ được truy cập các chức năng được cấp quyền và mọi request API phải được kiểm tra quyền trước khi xử lý.

#### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Authorization — Kiểm soát truy cập

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Unauthorized Access Count | Số trường hợp | Penetration test — thử truy cập chức năng ngoài quyền |
| API Protection Coverage | % | Tỷ lệ API endpoint có middleware kiểm tra quyền |
| Role Count | Số vai trò | Đếm số vai trò được định nghĩa trong hệ thống |

#### Tiêu chuẩn đáp ứng
- Unauthorized Access = **0 trường hợp**
- API Protection Coverage = **100%**
- Role Count = **4** (Admin, TCCB, TCKT, Nhân sự) theo mô hình **RBAC**

#### Đại lượng thay thế
- **Proxy:** Số API route không có middleware auth (đo qua route audit script)

---

### 14. SUPL-SE03 — Chống tấn công brute-force

**Yêu cầu gốc:** Hệ thống phải khóa tạm thời tài khoản sau 5 lần đăng nhập sai liên tiếp trong ít nhất 15 phút và phải ghi log cảnh báo khi phát hiện dấu hiệu brute-force.

#### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Integrity — Chống tấn công tự động

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Lock Threshold | Số lần | Số lần đăng nhập sai liên tiếp trước khi khóa |
| Lock Duration | Phút | Thời gian khóa tài khoản tạm thời |
| Alert Logging | Có/Không | Kiểm tra log cảnh báo khi phát hiện brute-force |

#### Tiêu chuẩn đáp ứng
- Lock Threshold = **5 lần** sai liên tiếp
- Lock Duration ≥ **15 phút**
- Alert Logging = **Có** — ghi log cảnh báo với IP, thời gian, tài khoản bị tấn công

#### Đại lượng thay thế
- Không cần — đo trực tiếp qua test đăng nhập sai liên tiếp

---

### 15. SUPL-SE04 — Mã hóa truyền tải (HTTPS)

**Yêu cầu gốc:** Toàn bộ giao tiếp giữa client và server phải sử dụng HTTPS với TLS 1.2 trở lên.

#### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Confidentiality — Bảo mật truyền tải

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| TLS Version | Phiên bản | Kiểm tra certificate và protocol qua SSL Labs hoặc curl |
| HTTPS Coverage | % | Tỷ lệ kết nối sử dụng HTTPS / Tổng kết nối |
| HTTP Redirect | Có/Không | Kiểm tra HTTP request có tự động redirect sang HTTPS |

#### Tiêu chuẩn đáp ứng
- TLS ≥ **1.2**
- HTTPS Coverage = **100%**
- HTTP Redirect = **Có** (auto-redirect 301)

#### Đại lượng thay thế
- **Proxy:** SSL Labs Score (A/B/C/D/F) — mục tiêu đạt **A** hoặc **A+**

---

### 16. SUPL-SE05 — Bảo vệ dữ liệu nhạy cảm

**Yêu cầu gốc:** Dữ liệu nhạy cảm như CCCD, BHXH và thông tin ngân hàng chỉ được hiển thị cho vai trò được phép và mọi truy cập phải được ghi audit log.

#### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Confidentiality — Bảo mật dữ liệu cá nhân

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Exposed Sensitive Fields | Số trường | Kiểm tra API response cho vai trò không được phép — đếm trường nhạy cảm bị lộ |
| Audit Log Coverage for Sensitive Data | % | Tỷ lệ truy cập dữ liệu nhạy cảm được ghi audit log |

#### Tiêu chuẩn đáp ứng
- Exposed Sensitive Fields = **0** cho vai trò không được phép
- Audit Log Coverage = **100%** cho CCCD, BHXH, thông tin ngân hàng

#### Đại lượng thay thế
- **Proxy:** Số API endpoint trả về dữ liệu nhạy cảm mà không kiểm tra vai trò (code review audit)

---

### 17. SUPL-SE06 — Phòng chống CSRF và XSS

**Yêu cầu gốc:** Hệ thống phải ngăn chặn yêu cầu giả mạo làm thay đổi dữ liệu và không được hiển thị nội dung thực thi do người dùng chèn vào giao diện.

#### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Integrity — Chống tấn công web

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| CSRF Vulnerabilities | Số lỗ hổng | Penetration test (OWASP ZAP hoặc tương đương) |
| XSS Vulnerabilities | Số lỗ hổng | Penetration test + code review cơ chế xử lý dữ liệu đầu vào/đầu ra |
| State-changing Request Protection Coverage | % | Tỷ lệ form POST/PUT/DELETE hoặc request tương đương được bảo vệ chống giả mạo yêu cầu |

#### Tiêu chuẩn đáp ứng
- CSRF Vulnerabilities = **0**
- XSS Vulnerabilities = **0**
- State-changing Request Protection Coverage = **100%**

#### Đại lượng thay thế
- **Proxy:** Số điểm nhập liệu không được xử lý an toàn trước khi hiển thị lại trong giao diện (đo qua static code analysis)

---

### 18. SUPL-SE07 — Chống SQL Injection

**Yêu cầu gốc:** Mọi truy vấn sử dụng dữ liệu đầu vào từ người dùng phải ngăn chặn việc chèn lệnh SQL.

#### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Integrity — Chống tấn công database

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| SQLi Vulnerabilities | Số lỗ hổng | sqlmap scan hoặc penetration test |
| Query Protection Coverage | % | Tỷ lệ truy vấn có sử dụng dữ liệu đầu vào được bảo vệ khỏi chèn lệnh SQL (code review) |

#### Tiêu chuẩn đáp ứng
- SQLi Vulnerabilities = **0**
- Query Protection Coverage = **100%**

#### Đại lượng thay thế
- **Proxy:** Số truy vấn ghép chuỗi trực tiếp dữ liệu đầu vào trong codebase — mục tiêu **0**

---

### 19. SUPL-U01 — Giao diện thân thiện và nhất quán

**Yêu cầu gốc:** Giao diện người dùng phải sử dụng tiếng Việt và tuân thủ thống nhất design system về bố cục, màu sắc và font chữ trên toàn bộ hệ thống.

#### Yếu tố chất lượng
- **Nhóm:** Usability (Tính dễ sử dụng)
- **Yếu tố:** Consistency — Tính nhất quán giao diện

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| UI Violation Count | Số trang | Rà soát giao diện — đếm trang vi phạm design system (font, màu, layout) |
| Vietnamese Content Rate | % | Tỷ lệ nội dung giao diện sử dụng Tiếng Việt |

#### Tiêu chuẩn đáp ứng
- UI Violation Count = **0 trang**
- Vietnamese Content Rate = **100%** (trừ thuật ngữ kỹ thuật quốc tế)

#### Đại lượng thay thế
- **Proxy:** Số component sử dụng hardcoded style (không theo design token) — đo qua code review

---

### 20. SUPL-U02 — Thời gian đào tạo sử dụng ngắn

**Yêu cầu gốc:** Người dùng mới thuộc phòng TCCB và TCKT phải hoàn thành được các chức năng cơ bản sau tối đa 2 giờ đào tạo.

#### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Learnability — Dễ học, dễ tiếp cận

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Average Training Time | Giờ | User test — đo thời gian đào tạo trung bình cho người dùng mới |
| Task Completion Rate After Training | % | Tỷ lệ người dùng hoàn thành thao tác cơ bản (thêm/sửa nhân sự) sau đào tạo |

#### Tiêu chuẩn đáp ứng
- Average Training Time ≤ **2 giờ** cho các chức năng cơ bản
- Task Completion Rate ≥ **95%** cho phòng TCCB sau đào tạo

#### Đại lượng thay thế
- **Proxy:** Khối lượng tài liệu đào tạo (số trang) — mục tiêu ≤ 30 trang cho mỗi vai trò

---

### 21. SUPL-U03 — Thông báo lỗi rõ ràng

**Yêu cầu gốc:** Mọi lỗi nhập liệu, lỗi nghiệp vụ và lỗi hệ thống phải hiển thị thông báo bằng tiếng Việt, nêu nguyên nhân và có ít nhất 1 gợi ý khắc phục.

#### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Error Handling — Xử lý lỗi thân thiện

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Vietnamese Error Message Coverage | % | Tỷ lệ loại lỗi có thông báo Tiếng Việt rõ ràng / Tổng loại lỗi |
| Fix Suggestion Rate | % | Tỷ lệ thông báo lỗi có kèm gợi ý khắc phục |

#### Tiêu chuẩn đáp ứng
- Vietnamese Error Message Coverage = **100%** (validation, nghiệp vụ, hệ thống)
- Fix Suggestion Rate = **100%** (mỗi thông báo lỗi ≥ 1 gợi ý khắc phục)

#### Đại lượng thay thế
- **Proxy:** Số error code/message hiển thị bằng tiếng Anh hoặc mã kỹ thuật — mục tiêu **0**

---

### 22. SUPL-U04 — Tìm kiếm và lọc đa tiêu chí

**Yêu cầu gốc:** Các danh sách dữ liệu phải hỗ trợ tìm kiếm theo từ khóa và kết hợp ít nhất 3 tiêu chí lọc đồng thời; người dùng phải tìm và mở chi tiết 1 nhân sự trong tối đa 3 bước.

#### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Efficiency — Hiệu quả thao tác

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Steps to Search & View | Số bước | Đếm số click/thao tác để tìm và xem chi tiết 1 nhân sự |
| Max Concurrent Filter Criteria | Số tiêu chí | Đếm số tiêu chí lọc có thể kết hợp đồng thời |

#### Tiêu chuẩn đáp ứng
- Steps to Search & View ≤ **3 bước** (nhập từ khóa → tìm → click xem)
- Max Concurrent Filter ≥ **3 tiêu chí** đồng thời

#### Đại lượng thay thế
- Không cần — đo trực tiếp qua usability test

---

### 23. SUPL-U05 — Giao diện responsive

**Yêu cầu gốc:** Giao diện phải hiển thị đúng trên desktop từ 1366×768 trở lên và phải sử dụng được trên tablet 1024×768 theo các tỷ lệ trang quy định tại phần tiêu chuẩn đáp ứng.

#### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Accessibility — Khả năng truy cập đa thiết bị

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Desktop Compatibility Rate | % | Tỷ lệ trang hiển thị đúng trên desktop ≥ 1366×768 |
| Tablet Compatibility Rate | % | Tỷ lệ trang sử dụng được trên tablet 1024×768 |

#### Tiêu chuẩn đáp ứng
- Desktop Compatibility = **100%** (≥ 1366×768)
- Tablet Compatibility ≥ **80%** (1024×768)

#### Đại lượng thay thế
- **Proxy:** Số CSS breakpoint được định nghĩa — mục tiêu ≥ 2 (desktop + tablet)

---

### 24. SUPL-U07 — Xác nhận trước thao tác quan trọng

**Yêu cầu gốc:** Hệ thống phải hiển thị hộp thoại xác nhận trước các thao tác xóa dữ liệu, khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng lao động trước hạn và thay đổi trạng thái đơn vị.

#### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Error Prevention — Ngăn ngừa lỗi do thao tác nhầm

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Confirmation Dialog Coverage | % | Tỷ lệ thao tác quan trọng có hộp thoại xác nhận |

#### Tiêu chuẩn đáp ứng
- Confirmation Dialog Coverage = **100%** cho: xóa dữ liệu, khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng lao động trước hạn, thay đổi trạng thái đơn vị

#### Đại lượng thay thế
- Không cần — kiểm thử trực tiếp từng thao tác

---

### 25. SUPL-S01 — Kiến trúc module hóa

**Yêu cầu gốc:** Hệ thống phải được tách thành các module có giao diện trao đổi rõ ràng để việc thay đổi một module chỉ ảnh hưởng tối đa một module khác.

#### Yếu tố chất lượng
- **Nhóm:** Supportability (Khả năng bảo trì)
- **Yếu tố:** Maintainability → Modularity — Tính module
- **Mô hình McCall:** Product Revision → Maintainability

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Module Coupling | Số module bị ảnh hưởng | Khi thay đổi 1 module, đếm số module khác phải thay đổi theo |
| API Interface Separation | Có/Không | Kiểm tra frontend và backend giao tiếp hoàn toàn qua RESTful API |

#### Tiêu chuẩn đáp ứng
- Thay đổi 1 module → ảnh hưởng ≤ **1 module** khác
- Frontend ↔ Backend giao tiếp **100% qua API** (không shared code)

#### Đại lượng thay thế
- **Proxy:** Số import/dependency cross-module trong codebase — đo qua dependency analysis tool

---

### 26. SUPL-S03 — Khả năng mở rộng danh mục cấu hình

**Yêu cầu gốc:** Hệ thống phải cho phép mở rộng các danh mục dữ liệu chủ qua giao diện quản trị mà không cần sửa mã nguồn.

#### Yếu tố chất lượng
- **Nhóm:** Supportability
- **Yếu tố:** Flexibility — Tính linh hoạt

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Extendable Categories via UI | Số loại | Đếm số loại danh mục có thể thêm mới qua giao diện quản trị |
| Code Changes for New Category | Số dòng | Đếm số dòng code phải sửa khi thêm 1 danh mục mới |

#### Tiêu chuẩn đáp ứng
- Extendable Categories ≥ **3** (hệ số lương, loại phụ cấp, loại hợp đồng) đối với nhóm danh mục master data
- **Ghi chú phạm vi:** Chỉ số Extendable Categories áp dụng cho các danh mục dữ liệu chủ. Riêng cấu hình **ẩn/hiện mục khen thưởng/kỷ luật** (**FEAT 7.9 / UC 4.48**) được xem là một chiều cấu hình hiển thị độc lập và phải được quản trị qua UI mà không yêu cầu sửa mã nguồn.
- Code Changes = **0 dòng** khi thêm danh mục mới

#### Đại lượng thay thế
- Không cần — kiểm thử trực tiếp bằng cách thêm danh mục mới qua UI

---

### 27. SUPL-F01 — Ghi nhật ký hệ thống tự động

**Yêu cầu gốc:** Hệ thống phải tự động ghi nhật ký cho mọi hành động CRUD và truy cập, đồng thời mỗi bản ghi log phải có đầy đủ các trường thông tin bắt buộc.

#### Yếu tố chất lượng
- **Nhóm:** Functionality (bổ sung) + Correctness
- **Yếu tố:** Auditability — Khả năng kiểm toán
- **Mô hình McCall:** Product Operation → Correctness

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Action Log Coverage | % | (Số hành động được ghi log / Tổng hành động thực hiện) × 100 |
| Log Field Completeness | Số trường / 9 | Kiểm tra mỗi log entry có đủ 9 trường: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả, IP |

#### Tiêu chuẩn đáp ứng
- Action Log Coverage = **100%** cho mọi hành động CRUD và truy cập
- Log Field Completeness = **9/9 trường** cho mọi entry

#### Đại lượng thay thế
- **Proxy:** Số API controller không gọi audit service (code review) — mục tiêu **0**

---

### 28. SUPL-F08 — Băm mật khẩu

**Yêu cầu gốc:** Tất cả mật khẩu người dùng phải được lưu ở dạng băm một chiều thích ứng và không được tồn tại mật khẩu dạng rõ trong dữ liệu lưu trữ.

#### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Confidentiality — Bảo mật dữ liệu lưu trữ

#### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Hash Method Compliance | Có/Không | Kiểm tra cấu hình và mã nguồn để xác nhận mật khẩu được lưu bằng cơ chế băm một chiều thích ứng |
| Hash Difficulty Parameter | Số nguyên | Kiểm tra cấu hình tham số độ khó của cơ chế băm |
| Plaintext Password Count | Số mật khẩu | Query database kiểm tra mật khẩu không ở dạng hash |

#### Tiêu chuẩn đáp ứng
- Hash Method Compliance = **Có**
- Hash Difficulty Parameter ≥ **mức tương đương bcrypt cost 10**
- Plaintext Password Count = **0**

#### Đại lượng thay thế
- **Proxy:** Kết quả kiểm tra định dạng chuỗi lưu trong cột mật khẩu phải phù hợp với cơ chế băm đã cấu hình

---

### Tổng hợp: Bảng đặc tả bổ sung (Supplementary Specification Table)

> Format theo bài tập nhóm: **Quality Factor × Metric × Acceptance Criteria**

| # | Mã SUPL | Quality Factor | Metric | Acceptance Criteria | Proxy (nếu có) |
|---|---------|---------------|--------|---------------------|-----------------|
| 1 | P01 | Performance → Speed | P95 Response Time; Contract list/detail/termination response time | ≤ 2s (≤50 users), ≤ 5s (≤100 users); áp dụng cả UC 4.43–4.45 theo ngưỡng kế thừa | — |
| 2 | P02 | Performance → Capacity | Concurrent users, Throughput | ≥ 100 users, ≥ 50 tx/s | Số TCP connections ổn định |
| 3 | P03 | Performance → Speed | Dashboard/Report render time | Dashboard ≤ 5s, Report ≤ 15s | SQL query execution time |
| 4 | P04 | Performance → Speed | Search response time | ≤ 2s (≤10K records) cho nhân sự/đánh giá; ≤ 5s (≤50K records) cho tập dữ liệu lớn | SQL EXPLAIN time |
| 5 | P05 | Performance → Speed | Upload/Download time | Upload ≤ 5s, Download ≤ 3s (≤5MB) | Disk I/O speed |
| 6 | P06 | Performance → Speed | Excel export time | ≤ 10s (≤1K records), ≤ 30s (≤10K records) | API response time |
| 7 | R01 | Reliability → Availability | Uptime %, MTBF | ≥ 99.5%, MTBF ≥ 720h | Health check error rate |
| 8 | R02 | Reliability → Recoverability | MTTR | ≤ 15 phút | — |
| 9 | R03 | Reliability → Recoverability | RPO, RTO | RPO ≤ 24h, RTO ≤ 4h | Staging restore time |
| 10 | R04 | Reliability → Integrity | Data inconsistency count | 0 cases, 100% coverage bảo toàn nhất quán khi lỗi | FK violations count |
| 11 | R05 | Reliability → Fault Tolerance | Data loss rate | ≤ 5%, warning ≥ 5 phút trước | Popup hiển thị (binary) |
| 12 | SE01 | Security → Authentication | Password rules, Session security | ≥ 8 chars, 3 rules, phiên xác thực an toàn và tự hết hạn | Weak password count |
| 13 | SE02 | Security → Authorization | Unauthorized access count | 0 cases, 100% API protected | Unprotected route count |
| 14 | SE03 | Security → Integrity | Lock threshold, Duration | 5 failures → 15min lock | — |
| 15 | SE04 | Security → Confidentiality | TLS version, HTTPS coverage | TLS ≥ 1.2, 100% HTTPS | SSL Labs Score |
| 16 | SE05 | Security → Confidentiality | Exposed sensitive fields | 0 fields exposed | Unprotected API count |
| 17 | SE06 | Security → Integrity | CSRF/XSS vulnerabilities | 0 vulnerabilities | Unsanitized input count |
| 18 | SE07 | Security → Integrity | SQLi vulnerabilities | 0 vulnerabilities | Raw SQL query count |
| 19 | U01 | Usability → Consistency | UI violations, Vietnamese content | 0 pages, 100% tiếng Việt | Hardcoded style count |
| 20 | U02 | Usability → Learnability | Training time, Completion rate | ≤ 2h, ≥ 95% completion | Doc pages per role |
| 21 | U03 | Usability → Error Handling | Error message coverage | 100% Vietnamese, 100% fix suggestions | English error count |
| 22 | U04 | Usability → Efficiency | Steps to search+view | ≤ 3 steps, ≥ 3 filter criteria | — |
| 23 | U05 | Usability → Accessibility | Display compatibility | 100% desktop (≥1366×768), ≥ 80% tablet (1024×768) | CSS breakpoint count |
| 24 | U07 | Usability → Error Prevention | Confirmation dialog coverage | 100% critical actions, gồm chấm dứt hợp đồng trước hạn | — |
| 25 | S01 | Supportability → Modularity | Module coupling | ≤ 1 module affected | Cross-module imports |
| 26 | S03 | Supportability → Flexibility | Extendable categories | ≥ 3 danh mục master data, 0 code changes; cấu hình ẩn/hiện quản trị qua UI | — |
| 27 | F01 | Correctness → Auditability | Log coverage, Field completeness | 100% actions, 9/9 fields | Unaudited controllers |
| 28 | F08 | Security → Confidentiality | Hash compliance, Plaintext count | băm một chiều thích ứng, 0 plaintext | Regex check on DB |
