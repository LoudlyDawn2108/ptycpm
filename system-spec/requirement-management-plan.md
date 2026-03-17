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

# II. THU THẬP YÊU CẦU TỪ CÁC STAKEHOLDERS (Xác định STRQ, FEAT)

[stakeholder-interviews.md](./stakeholder-interviews.md)

> **Ghi chú:** File này hiện là nguồn chuẩn chứa chung **STRQ** và **FEAT**, thay cho việc tách riêng tài liệu STR và VIS.

# III. MÔ HÌNH HOÁ YÊU CẦU

[requirement-modeling.md](./requirement-modeling.md)

> **Ghi chú:** File này chứa danh mục **48 UC**, mô hình tác nhân và ma trận truy vết **FEAT → UC**.

# IV. Luồng sự kiện và các UCs chính

[uc1-10.md](./uc1-10.md)

[uc11-20.md](./uc11-20.md)

[uc21-30.md](./uc21-30.md)

[uc31-42.md](./uc31-42.md)

> **Ghi chú:** Mặc dù tên file là `uc31-42.md`, file này hiện đang chứa **UC 4.31 – UC 4.48**. Nếu tái cấu trúc bộ tài liệu, nên đổi tên thành `uc31-48.md` để phản ánh đúng phạm vi nội dung.

# V. YÊU CẦU BỔ SUNG VÀ THIẾT LẬP ĐỘ ĐO

[supplementary-requirements.md](./supplementary-requirements.md)

> **Ghi chú:** File này chứa các **SUPL**, các nhóm NFR và ma trận truy vết NFR → FEAT/UC.

[supplementary-metrics.md](./supplementary-metrics.md)

> **Ghi chú:** File này chứa độ đo, tiêu chuẩn đáp ứng và proxy dùng để xác minh **SUPL**; là nguồn chính cho truy vết **SUPL → Test/Acceptance Check**.

# VI. XÁC ĐỊNH CÁC LỚP, XÂY DỰNG BIỂU ĐỒ LỚP

[class-diagram.md](./class-diagram.md)

> **Ghi chú:** Đây là artefact thiết kế chính hiện tại để neo đường truy vết **UC → Design** trong baseline thiết kế.
