# ĐẶC TẢ YÊU CẦU PHẦN MỀM (SRS)

## Hệ thống Quản lý Nhân sự (HRMS) — Trường Đại học Thủy Lợi

---

## 1. Giới thiệu

### 1.1. Phạm vi

Tài liệu này đặc tả các yêu cầu phần mềm của **Hệ thống Quản lý Nhân sự (HRMS)** phục vụ Trường Đại học Thủy Lợi. Hệ thống được xây dựng để tập trung hóa hoạt động quản lý nhân sự cho các đơn vị đào tạo, đơn vị nghiên cứu khoa học, các phòng ban chức năng và các đơn vị trực thuộc nhà trường.

Phạm vi chức năng của hệ thống bao gồm:

- xác thực người dùng, quản lý tài khoản và phân quyền theo vai trò;
- quản lý cơ cấu tổ chức theo mô hình cây cha–con;
- quản lý hồ sơ nhân sự, hợp đồng lao động, đánh giá khen thưởng/kỷ luật;
- quản lý bổ nhiệm, điều chuyển, bãi nhiệm nhân sự theo đơn vị;
- quản lý khóa đào tạo, kết quả đào tạo và chứng chỉ;
- quản lý danh mục tham chiếu như hệ số lương, loại phụ cấp, loại hợp đồng;
- cung cấp báo cáo, thống kê nhân sự;
- hỗ trợ chức năng tự phục vụ cho cán bộ, giảng viên, nhân viên;
- ghi vết hoạt động và hỗ trợ truy vết kiểm toán.

Ngoài phạm vi của phiên bản hiện tại:

- các luồng tác vụ cá nhân khác ngoài xem thông tin cá nhân, xem đơn vị công tác, đăng ký đào tạo và xem lịch sử đào tạo;
- các artefact thiết kế và kiểm thử chi tiết như class diagram, sequence diagram, test case matrix.

### 1.2. Tổng quan về tài liệu

Tài liệu SRS này được tổ chức như sau:

- **Phần 1** mô tả phạm vi và cách tài liệu được tổ chức.
- **Phần 2** trình bày bối cảnh sản phẩm, nhóm người dùng và các chức năng chính ở mức tổng quan.
- **Phần 3.1** mô tả các yêu cầu giao diện áp dụng ở mức toàn hệ thống.
- **Phần 3.2** mô tả các yêu cầu chức năng chính của hệ thống.
- **Phần 3.3** mô tả các yêu cầu bổ sung, yêu cầu phi chức năng và ràng buộc kỹ thuật.
- **Phần 3.4** mô tả các quy tắc truy vết, tổ chức requirement, thuộc tính requirement và các giả định/phụ thuộc dùng để quản lý bộ yêu cầu.

Các tài liệu nền tảng liên quan đến SRS này gồm:

| Tài liệu | Vai trò |
| --- | --- |
| Kế hoạch quản lý yêu cầu (RMP) | Định nghĩa loại requirement, thuộc tính, truy vết và tổ chức bộ tài liệu |
| Tài liệu thu thập yêu cầu từ stakeholder | Nguồn chuẩn cho STRQ và FEAT |
| Mô hình hóa yêu cầu và bộ Use Case Specification | Nguồn chuẩn cho tác nhân, nhóm use case và hành vi chức năng chi tiết |
| Đặc tả yêu cầu bổ sung và tài liệu độ đo | Nguồn chuẩn cho SUPL, metric và acceptance criteria |

Các chữ viết tắt sử dụng trong tài liệu:

| Viết tắt | Diễn giải |
| --- | --- |
| HRMS | Human Resource Management System |
| TCCB | Phòng Tổ chức – Cán bộ |
| TCKT | Phòng Tài chính – Kế toán |
| STRQ | Stakeholder Request |
| FEAT | Feature |
| UC | Use Case |
| SUPL | Supplementary Requirement |

---

## 2. Mô tả chung

### 2.1. Mô tả chung về giao diện

HRMS là hệ thống **ứng dụng web nhiều người dùng**. Người dùng truy cập hệ thống qua trình duyệt, thao tác nghiệp vụ trên giao diện web, và toàn bộ xử lý nghiệp vụ được thực hiện thông qua các API của hệ thống.

Các nhóm người dùng chính của hệ thống gồm:

| Nhóm người dùng | Vai trò sử dụng chính |
| --- | --- |
| Quản trị viên (Admin) | Quản lý tài khoản, phân quyền, quản lý cơ cấu tổ chức, xem nhật ký hệ thống |
| Phòng TCCB | Thực hiện nghiệp vụ quản lý hồ sơ, hợp đồng, đào tạo, đánh giá, điều chuyển/bổ nhiệm, cấu hình danh mục |
| Phòng TCKT | Tra cứu hồ sơ, xem dữ liệu phục vụ lương/phụ cấp, xem và xuất báo cáo thống kê |
| Cán bộ / Giảng viên / Nhân viên | Xem thông tin cá nhân, xem đơn vị công tác, đăng ký đào tạo, xem lịch sử đào tạo |
| Hệ thống (System Timer / Auto-Job) | Thực hiện các tác vụ tự động như đăng xuất, khóa tài khoản, cập nhật trạng thái |

Đặc điểm giao diện ở mức tổng quan:

- giao diện sử dụng tiếng Việt và điều hướng theo vai trò;
- sau đăng nhập, người dùng được đưa đến dashboard phù hợp với quyền hạn;
- hệ thống sử dụng các mẫu màn hình chính: danh sách có tìm kiếm/lọc, form nhập liệu, màn hình chi tiết, màn hình thống kê, hộp thoại xác nhận và chức năng import/export;
- hệ thống ưu tiên khai thác trên máy tính để bàn, đồng thời hỗ trợ một phần thao tác chính trên máy tính bảng;
- hệ thống hỗ trợ thao tác với tệp PDF và Excel cho các nghiệp vụ cần đính kèm hoặc xuất dữ liệu.

### 2.2. Các chức năng chính

| Nhóm chức năng | Mô tả tổng quan | Truy vết chính |
| --- | --- | --- |
| Quản lý truy cập | Đăng nhập, đăng xuất, đổi mật khẩu, quản lý phiên làm việc | FEAT 1.1–1.4 |
| Quản trị tài khoản | Tìm kiếm, thêm, sửa, khóa/mở khóa tài khoản, phân quyền | FEAT 2.1–2.6 |
| Quản lý cơ cấu tổ chức | Thiết lập cây đơn vị, cập nhật thông tin đơn vị, giải thể/sáp nhập | FEAT 3.1–3.5 |
| Bố trí nhân sự theo đơn vị | Bổ nhiệm, điều chuyển, bãi nhiệm nhân sự trong cơ cấu tổ chức | FEAT 4.1–4.3 |
| Quản lý hợp đồng | Tạo, xem, sửa, chấm dứt hợp đồng lao động | FEAT 5.1–5.4 |
| Quản lý đánh giá | Ghi nhận và tra cứu khen thưởng/kỷ luật | FEAT 6.1–6.3 |
| Quản lý hồ sơ nhân sự | Tìm kiếm, lọc, tạo mới, chỉnh sửa, xem chi tiết, in/xuất, đánh dấu thôi việc | FEAT 7.1–7.9 |
| Quản lý đào tạo | Mở khóa đào tạo, chỉnh sửa, xem khóa học, ghi nhận kết quả | FEAT 8.1–8.4 |
| Cấu hình danh mục | Quản lý hệ số lương, loại phụ cấp, loại hợp đồng | FEAT 9.1–9.5 |
| Báo cáo và thống kê | Xem và xuất thống kê nhân sự, hợp đồng, đào tạo, bổ nhiệm | FEAT 10.1–10.4 |
| Tự phục vụ cá nhân | Xem hồ sơ cá nhân, xem đơn vị công tác, đăng ký đào tạo, xem lịch sử đào tạo | FEAT 11.1–11.4 |
| Ghi vết và kiểm toán | Ghi log tự động và truy xuất audit log | FEAT 12.1–12.2 |

---

## 3. Các yêu cầu cụ thể

### 3.1. Các yêu cầu về giao diện

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| UI-01 | Hệ thống phải sử dụng tiếng Việt trên 100% màn hình, trừ các thuật ngữ kỹ thuật không thể thay thế hợp lý. | SUPL-U01 |
| UI-02 | Hệ thống phải áp dụng thống nhất bố cục, màu sắc và font chữ trên toàn bộ giao diện; số cặp màn hình cùng loại có khác biệt về bố cục, màu sắc hoặc font chữ phải bằng 0. | SUPL-U01 |
| UI-03 | Hệ thống phải hiển thị mọi lỗi nhập liệu, lỗi nghiệp vụ và lỗi hệ thống bằng tiếng Việt, kèm mô tả nguyên nhân và ít nhất một gợi ý khắc phục. | SUPL-U03 |
| UI-04 | Hệ thống phải hỗ trợ tìm kiếm theo từ khóa và lọc đa tiêu chí trên các danh sách nhân sự, hợp đồng, đơn vị và đánh giá khi chức năng đó được cung cấp. | SUPL-U04 |
| UI-05 | Ở độ phân giải từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang. | SUPL-U05 |
| UI-06 | Trên thiết bị 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện thao tác chính mà không cần phóng to. | SUPL-U05 |
| UI-07 | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập; 100% form có nút xác nhận mặc định phải hỗ trợ phím Enter; 100% trang phải hiển thị breadcrumb. | SUPL-U06 |
| UI-08 | Hệ thống phải hiển thị hộp thoại xác nhận trước các thao tác khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng trước hạn, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương. | SUPL-U07 |
| UI-09 | Hệ thống phải hỗ trợ Chrome (bản mới nhất và 2 bản gần nhất), Firefox và Edge; 100% chức năng phải hoạt động đúng trên Chrome bản mới nhất và tối thiểu 95% chức năng phải hoạt động đúng trên Firefox và Edge. | SUPL-IC02 |

### 3.2. Các yêu cầu chức năng

#### 3.2.1. Hệ thống và tài khoản

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-ACC-01 | Hệ thống phải cho phép người dùng đăng nhập bằng tài khoản hợp lệ và chuyển hướng đến dashboard tương ứng với vai trò của người dùng. | Tất cả người dùng | FEAT 1.1, UC 4.1 |
| FR-ACC-02 | Hệ thống phải cho phép người dùng đăng xuất chủ động và phải tự động đăng xuất khi phiên làm việc không có tương tác trong 30 phút. | Tất cả người dùng, Hệ thống | FEAT 1.2, FEAT 1.3, UC 4.2 |
| FR-ACC-03 | Hệ thống phải cho phép người dùng đã đăng nhập đổi mật khẩu của tài khoản đang sử dụng. | Tất cả người dùng | FEAT 1.4, UC 4.3 |
| FR-ACC-04 | Hệ thống phải cho phép Quản trị viên tìm kiếm, thêm mới và cập nhật tài khoản người dùng. | Quản trị viên | FEAT 2.1, FEAT 2.2, FEAT 2.3 |
| FR-ACC-05 | Hệ thống phải cho phép Quản trị viên gán tài khoản vào các nhóm nghiệp vụ được hệ thống định nghĩa sẵn. | Quản trị viên | FEAT 2.4, UC 4.7 |
| FR-ACC-06 | Hệ thống phải cho phép Quản trị viên khóa hoặc mở khóa tài khoản, và phải tự động khóa tài khoản gắn với nhân sự đã thôi việc. | Quản trị viên, Hệ thống | FEAT 2.5, FEAT 2.6, UC 4.8 |
| FR-ACC-07 | Hệ thống phải cho phép Quản trị viên xem, tìm kiếm, lọc và xuất nhật ký hệ thống để phục vụ truy vết hoạt động. | Quản trị viên | FEAT 12.2 |

#### 3.2.2. Cơ cấu tổ chức và bố trí nhân sự

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-ORG-01 | Hệ thống phải cho phép khai thác và quản lý cơ cấu tổ chức theo mô hình cây cha–con. | Quản trị viên, TCCB | FEAT 3.1 |
| FR-ORG-02 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB thêm mới, sửa thông tin và xem chi tiết đơn vị tổ chức nhân sự. | Quản trị viên, TCCB | FEAT 3.2, FEAT 3.3, FEAT 3.5 |
| FR-ORG-03 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB thay đổi trạng thái đơn vị tổ chức nhân sự sang giải thể hoặc sáp nhập theo quy tắc nghiệp vụ. | Quản trị viên, TCCB | FEAT 3.4 |
| FR-ORG-04 | Hệ thống phải cho phép Phòng TCCB bổ nhiệm, điều chuyển và bãi nhiệm nhân sự trong các đơn vị tổ chức. | TCCB | FEAT 4.1–4.3 |

#### 3.2.3. Danh mục tham chiếu và hồ sơ nhân sự

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-CFG-01 | Hệ thống phải cho phép Phòng TCCB thêm mới, sửa, xóa hoặc thay đổi trạng thái hệ số lương theo tình trạng sử dụng của danh mục. | TCCB | FEAT 9.1–9.3 |
| FR-CFG-02 | Hệ thống phải cho phép Phòng TCCB thêm mới, sửa và thay đổi trạng thái danh mục loại phụ cấp và danh mục loại hợp đồng. | TCCB | FEAT 9.4, FEAT 9.5 |
| FR-HR-01 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa và lọc hồ sơ theo nhiều tiêu chí. | TCCB, TCKT | FEAT 7.1, FEAT 7.2 |
| FR-HR-02 | Hệ thống phải cho phép Phòng TCCB tạo mới hồ sơ nhân sự bằng nhập tay hoặc import từ Excel. | TCCB | FEAT 7.3 |
| FR-HR-03 | Khi tạo mới hồ sơ nhân sự, hệ thống phải tự động sinh mã cán bộ, đặt trạng thái hợp đồng mặc định là “Chưa hợp đồng” và trạng thái làm việc mặc định là “Đang chờ xét”. | Hệ thống | FEAT 7.3, SUPL-F02 |
| FR-HR-04 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa hồ sơ nhân sự đang ở trạng thái làm việc hợp lệ và phải từ chối chỉnh sửa hồ sơ đã thôi việc. | TCCB | FEAT 7.4 |
| FR-HR-05 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xem chi tiết hồ sơ nhân sự theo quyền hạn, đồng thời hỗ trợ in hoặc xuất Excel hồ sơ khi chức năng được cấp quyền. | TCCB, TCKT | FEAT 7.7, FEAT 7.8 |
| FR-HR-06 | Hệ thống phải cho phép Phòng TCCB đánh dấu thôi việc cho nhân sự và cập nhật các trạng thái liên quan theo quy tắc nghiệp vụ. | TCCB | FEAT 7.5 |
| FR-HR-07 | Hệ thống phải tự động đánh dấu thôi việc cho nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. | Hệ thống | FEAT 7.6 |
| FR-HR-08 | Hệ thống phải cho phép Phòng TCCB cấu hình ẩn/hiện các mục khen thưởng và kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc Phòng TCCB. | TCCB | FEAT 7.9 |

#### 3.2.4. Hợp đồng, đánh giá, đào tạo, báo cáo và tự phục vụ

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-CON-01 | Hệ thống phải cho phép Phòng TCCB tạo hợp đồng lao động mới cho nhân sự đủ điều kiện theo loại hợp đồng, thời hạn và số lần ký được cấu hình. | TCCB | FEAT 5.1 |
| FR-CON-02 | Hệ thống phải cho phép Phòng TCCB xem danh sách và chi tiết hợp đồng lao động của nhân sự. | TCCB | FEAT 5.2 |
| FR-CON-03 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa hợp đồng khi hợp đồng chưa có hiệu lực và chấm dứt hợp đồng trước hạn khi người thực hiện có thẩm quyền. | TCCB | FEAT 5.3, FEAT 5.4 |
| FR-EVA-01 | Hệ thống phải cho phép Phòng TCCB ghi nhận đánh giá khen thưởng hoặc kỷ luật cho nhân sự đang còn làm việc. | TCCB | FEAT 6.1 |
| FR-EVA-02 | Hệ thống phải cho phép Phòng TCCB xem lịch sử và tìm kiếm/lọc danh sách đánh giá khen thưởng/kỷ luật. | TCCB | FEAT 6.2, FEAT 6.3 |
| FR-TRN-01 | Hệ thống phải cho phép Phòng TCCB mở khóa đào tạo, chỉnh sửa khóa đào tạo theo trạng thái và xem chi tiết khóa đào tạo cùng danh sách người đã đăng ký. | TCCB | FEAT 8.1, FEAT 8.2, FEAT 8.3 |
| FR-TRN-02 | Hệ thống phải cho phép Phòng TCCB ghi nhận kết quả đào tạo và lưu chứng chỉ vào hồ sơ nhân sự của người tham gia. | TCCB | FEAT 8.4 |
| FR-RPT-01 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xem và xuất báo cáo, thống kê về nhân sự, hợp đồng, đánh giá, đào tạo và bổ nhiệm. | TCCB, TCKT | FEAT 10.1–10.4 |
| FR-SELF-01 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem thông tin cá nhân của bản thân, đồng thời xem thông tin đơn vị đang công tác và cơ cấu các đơn vị trực thuộc. | Người dùng | FEAT 11.1, FEAT 11.2 |
| FR-SELF-02 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên đăng ký hoặc hủy đăng ký tham gia khóa đào tạo được nhà trường phê duyệt mở. | Người dùng | FEAT 11.3 |
| FR-SELF-03 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. | Người dùng | FEAT 11.4 |

### 3.3. Các yêu cầu bổ sung

#### 3.3.1. Các yêu cầu chức năng bổ sung toàn hệ thống

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| SR-F01 | Hệ thống phải tự động ghi nhật ký cho 100% hành động truy cập, thêm mới/cập nhật dữ liệu, thay đổi trạng thái và thay đổi cấu hình; mỗi bản ghi phải có đủ thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. | SUPL-F01 |
| SR-F02 | Hệ thống phải tự động cập nhật trạng thái hợp đồng sang “Chờ gia hạn” khi hợp đồng đủ điều kiện theo ngưỡng chờ gia hạn được cấu hình. | SUPL-F05 |
| SR-F03 | Khi khóa đào tạo chuyển sang trạng thái “Đang đào tạo”, hệ thống phải tự động cập nhật trạng thái tham gia của tất cả đăng ký liên quan từ “Đã đăng ký” sang “Đang học”. | SUPL-F06 |
| SR-F04 | Hệ thống phải áp dụng quy tắc thay đổi trạng thái đối với danh mục loại phụ cấp và loại hợp đồng để bảo toàn dữ liệu lịch sử, thay vì xóa dữ liệu đã được sử dụng. | SUPL-F07 |
| SR-F05 | Hệ thống phải lưu trữ mật khẩu người dùng ở dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. | SUPL-F08 |

#### 3.3.2. Yêu cầu về độ tin cậy

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-R01 | Hệ thống phải đạt uptime tối thiểu 99,5% mỗi tháng trong khung giờ phục vụ 7:00–22:00, không tính thời gian bảo trì theo kế hoạch. | SUPL-R01 |
| NFR-R02 | Sau sự cố crash hoặc restart, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa 15 phút. | SUPL-R02 |
| NFR-R03 | Hệ thống phải sao lưu dữ liệu ít nhất mỗi 24 giờ, lưu giữ bản sao lưu tối thiểu 30 ngày, bảo đảm RPO không quá 24 giờ và RTO không quá 4 giờ. | SUPL-R03 |
| NFR-R04 | Các thao tác cập nhật dữ liệu quan trọng phải tuân thủ nguyên tắc toàn bộ hoặc không thực hiện phần nào; số trường hợp dữ liệu bất nhất quán sau lỗi phải bằng 0. | SUPL-R04 |
| NFR-R05 | Đối với form có dữ liệu nhập dở, hệ thống phải cảnh báo trước 5 phút khi phiên sắp hết hạn và phải khôi phục được tối thiểu 95% dữ liệu gần nhất sau khi người dùng đăng nhập lại. | SUPL-R05 |

#### 3.3.3. Yêu cầu về hiệu năng

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-P01 | P95 response time của các thao tác nghiệp vụ cơ bản phải không vượt quá 1 giây với 0–10 người dùng đồng thời, 2 giây với 11–50 người dùng, 5 giây với 51–100 người dùng và 10 giây khi vượt quá 100 người dùng. | SUPL-P01 |
| NFR-P02 | Hệ thống phải hỗ trợ tối thiểu 100 người dùng đồng thời, throughput tối thiểu 50 giao dịch/giây tại tải 100 người dùng và mức suy giảm hiệu năng không vượt quá 50% so với tải 1 người dùng. | SUPL-P02 |
| NFR-P03 | Dashboard phải tải xong trong tối đa 5 giây, báo cáo tổng hợp phức tạp trong tối đa 15 giây và mỗi biểu đồ thống kê trong tối đa 3 giây. | SUPL-P03 |
| NFR-P04 | Chức năng tìm kiếm và lọc phải trả kết quả trong tối đa 2 giây với tập dữ liệu đến 10.000 bản ghi và tối đa 5 giây với tập dữ liệu đến 50.000 bản ghi. | SUPL-P04 |
| NFR-P05 | Upload tệp dung lượng đến 5MB trên mạng LAN phải hoàn thành trong tối đa 5 giây; download tệp dung lượng đến 5MB trên mạng LAN phải hoàn thành trong tối đa 3 giây. | SUPL-P05 |
| NFR-P06 | Xuất Excel phải hoàn thành trong tối đa 10 giây với tối đa 1.000 bản ghi và tối đa 30 giây với tối đa 10.000 bản ghi. | SUPL-P06 |

#### 3.3.4. Yêu cầu về bảo mật và quyền riêng tư

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
| NFR-LR01 | Hệ thống phải hỗ trợ quản lý sự đồng ý thu thập dữ liệu cá nhân và xử lý yêu cầu hợp lệ về ẩn dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP. | SUPL-LR01 |
| NFR-LR02 | Các danh mục được cấu hình và sử dụng trong hệ thống phải tuân theo bộ danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt trên cơ sở quy định hiện hành của cơ quan quản lý. | SUPL-LR02 |
| NFR-LR03 | Hồ sơ nhân sự phải được lưu trữ tối thiểu 75 năm; hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu 10 năm sau khi kết thúc hoặc sau bản ghi cuối cùng. | SUPL-LR03 |

#### 3.3.5. Yêu cầu về hỗ trợ, bảo trì và ràng buộc kỹ thuật

| Mã | Yêu cầu | Truy vết nguồn |
| --- | --- | --- |
| NFR-S01 | Hệ thống phải được tổ chức thành các module chức năng có giao diện tích hợp rõ ràng; thay đổi một module không được buộc sửa đổi từ 2 module khác trở lên. | SUPL-S01 |
| NFR-S02 | Hệ thống phải cung cấp tài liệu API cho backend, hướng dẫn triển khai và hướng dẫn sử dụng cho từng vai trò; tối thiểu 90% API endpoint phải có mô tả trong tài liệu. | SUPL-S02 |
| NFR-S03 | Hệ thống phải cho phép mở rộng tối thiểu 3 danh mục cấu hình (hệ số lương, loại phụ cấp, loại hợp đồng) qua giao diện quản trị mà không cần thay đổi mã nguồn. | SUPL-S03 |
| NFR-S04 | Hệ thống phải hỗ trợ ít nhất 4 cấp độ log phía server gồm ERROR, WARNING, INFO và DEBUG; mỗi log lỗi phải có timestamp, request ID và stack trace. | SUPL-S04 |
| NFR-S05 | Hệ thống phải hỗ trợ tối thiểu 2 nút ứng dụng chạy song song trong cùng môi trường và bảo đảm các request liên tiếp của cùng người dùng vẫn hoạt động đúng khi được phân phối qua các nút khác nhau. | SUPL-S05 |
| NFR-DC01 | Hệ thống phải được xây dựng theo kiến trúc client–server; frontend là SPA và giao tiếp với backend qua RESTful API. | SUPL-DC01 |
| NFR-DC02 | Dữ liệu cơ cấu tổ chức phải luôn tạo thành một cây hợp lệ với một nút gốc duy nhất là Trường Đại học Thủy Lợi và không được tạo chu trình. | SUPL-DC02 |
| NFR-IC01 | Stack triển khai bắt buộc của hệ thống là React.js (TypeScript) cho frontend, Laravel/PHP cho backend và MySQL/MariaDB cho cơ sở dữ liệu. | SUPL-IC01 |
| NFR-IC02 | Toàn bộ hệ thống phải sử dụng mã hóa UTF-8 và không được phát sinh lỗi hiển thị tiếng Việt có dấu. | SUPL-IC03 |
| NFR-IC03 | Hệ thống chỉ hỗ trợ tệp PDF cho upload/download đính kèm nghiệp vụ và tệp Excel cho import/export dữ liệu; kích thước tối đa của mỗi tệp là 10MB và hệ thống phải thông báo lỗi khi vượt quá giới hạn. | SUPL-IC04 |

### 3.4. Các yêu cầu khác

#### 3.4.1. Quy tắc truy vết

Chuỗi truy vết của bộ yêu cầu phải tuân theo cấu trúc sau:

```text
STRQ ──→ FEAT ──→ UC ──→ SCEN
  │         │
  │         └──→ SUPL
  └──→ SUPL
```

Các quy tắc bao phủ bắt buộc:

- mỗi **STRQ** ở trạng thái `Approved` phải truy vết tới ít nhất một **FEAT** hoặc **SUPL**;
- mỗi **FEAT** ở trạng thái `Approved` phải truy vết tới ít nhất một **UC** hoặc **SUPL**;
- mỗi **UC** phải có ít nhất một **SCEN** tương ứng với luồng cơ bản;
- **UC** và **SUPL** phải hỗ trợ truy vết ngược về **FEAT** mà chúng hiện thực hóa hoặc hỗ trợ.

#### 3.4.2. Loại requirement và quy tắc đặt requirement

| Loại requirement / artefact | Vai trò | Nơi lưu trữ chính |
| --- | --- | --- |
| STRQ | Ghi nhận nhu cầu và mong đợi của stakeholder trong problem domain | Tài liệu thu thập yêu cầu từ stakeholder |
| FEAT | Biểu diễn các capability ở mức sản phẩm trong solution domain | Tài liệu thu thập yêu cầu từ stakeholder |
| UC | Mô tả hành vi chức năng chi tiết theo tương tác actor–system | Tài liệu mô hình hóa yêu cầu và các file UCS |
| SCEN | Mô tả các đường đi hợp lệ của từng use case | Tài liệu UCS tương ứng |
| SUPL | Mô tả yêu cầu cross-cutting, NFR và constraint | Tài liệu yêu cầu bổ sung |
| Metric / Acceptance Criteria | Lượng hóa cách xác minh SUPL | Tài liệu supplementary metrics |
| Design anchor | Neo truy vết từ yêu cầu sang thiết kế trong baseline hiện tại | `class-diagram.md` |

Quy tắc đặt requirement trong bộ tài liệu:

- Các mã **UI-**, **FR-**, **SR-**, **NFR-** trong SRS là mã trình bày cục bộ để nhóm nội dung; mã truy vết chuẩn của dự án vẫn là **STRQ**, **FEAT**, **UC**, **SCEN** và **SUPL**.
- Nội dung mô tả giao diện ở mức tổng quan phải nằm tại mục **2.1**; các yêu cầu giao diện có thể kiểm thử, đo được và áp dụng toàn hệ thống phải nằm tại mục **3.1**.
- Các yêu cầu chỉ áp dụng cho một use case hoặc một bước luồng cụ thể phải được giữ tại tài liệu **UCS** tương ứng thay vì đưa lên mục 3.3.
- Các yêu cầu áp dụng toàn hệ thống, cross-use-case, phi chức năng hoặc ràng buộc kỹ thuật/pháp lý phải nằm tại mục **3.3**.

#### 3.4.3. Thuộc tính requirement tối thiểu

| Loại requirement | Thuộc tính tối thiểu phải quản lý |
| --- | --- |
| STRQ | Status, Priority, Benefit, Effort, Risk, Stability, Reason |
| FEAT | Status, Priority, Benefit, Effort, Risk, Stability, Difficulty, Target Release, Assigned To, Reason, Transformation |
| UC | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason, Actor |
| SUPL | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason |

#### 3.4.4. Báo cáo và chế độ xem requirement

Các chế độ xem requirement tối thiểu phải duy trì trong baseline dự án gồm:

- ma trận thuộc tính cho STRQ, FEAT, UC và SUPL;
- ma trận truy vết STRQ → FEAT;
- ma trận truy vết STRQ → SUPL;
- ma trận truy vết FEAT → UC;
- ma trận truy vết FEAT → SUPL;
- ma trận truy vết UC → Design, với neo thiết kế chính hiện tại là `class-diagram.md`.

#### 3.4.5. Giả định, phụ thuộc và ghi chú chuẩn hóa nguồn

- Hệ thống được khai thác dưới dạng ứng dụng web nhiều người dùng trong môi trường vận hành của Trường Đại học Thủy Lợi.
- Các quy tắc nghiệp vụ về loại hợp đồng, phụ cấp, chức danh và lưu trữ hồ sơ phụ thuộc vào danh mục nội bộ đã được nhà trường phê duyệt và các quy định hiện hành của cơ quan quản lý.
- Trong phiên bản hiện tại, phạm vi tự phục vụ của người dùng được giới hạn ở xem thông tin cá nhân, xem đơn vị công tác, đăng ký đào tạo và xem lịch sử đào tạo.
- FEAT 1.5 về mô hình cung cấp hệ thống được truy vết tới **SUPL-DC01** thay vì được tách thành một use case riêng.
- Tài liệu **stakeholder-interviews.md** hiện là nguồn chuẩn chứa chung STRQ và FEAT, thay cho việc tách riêng tài liệu STR và VIS.
- File **uc31-42.md** hiện đang chứa nội dung từ **UC 4.31 đến UC 4.48**; các tham chiếu đến UC 4.43–4.48 trong baseline hiện tại vẫn được đối chiếu tại file này cho đến khi bộ tài liệu được đổi tên đồng bộ.
- Khi cần đối chiếu quy tắc truy vết, thuộc tính requirement và mapping tài liệu, **requirement-management-plan.md** là nguồn chuẩn quản lý requirement của dự án.
- Khi cần đối chiếu nguồn nội dung, tài liệu thu thập stakeholder là nguồn chuẩn cho STRQ/FEAT, bộ UCS là nguồn chuẩn cho hành vi chức năng chi tiết, và bộ SUPL cùng tài liệu độ đo là nguồn chuẩn cho các ngưỡng NFR.

---

## 4. Kết luận

SRS này tổng hợp phạm vi, hành vi chức năng, yêu cầu giao diện, yêu cầu bổ sung và các quy tắc quản lý requirement cho HRMS của Trường Đại học Thủy Lợi. Tài liệu là cơ sở để tiếp tục thiết kế, triển khai, kiểm thử và kiểm soát thay đổi yêu cầu trong các giai đoạn tiếp theo của dự án.
