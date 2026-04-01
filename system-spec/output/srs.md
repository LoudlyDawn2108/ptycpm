# VII. ĐẶC TẢ YÊU CẦU PHẦN MỀM (SRS)

## Hệ thống Quản lý Nhân sự (HRMS) — Trường Đại học Thủy Lợi

---

> **⚠️ BẢNG PHÂN CÔNG (XÓA TRƯỚC KHI NỘP)**
>
> | Thành viên | Section | Nội dung |
> |------------|---------|----------|
> | Nguyễn Hồng Phúc | 7.1 + 7.2 | Giới thiệu + Mô tả chung |
> | Nguyễn Hải Ninh | 7.3.1 + 7.3.2 | Yêu cầu giao diện + Yêu cầu chức năng |
> | Ngô Quang Tùng | 7.3.3 | Yêu cầu bổ sung (NFR) |
> | Ngô Đức Nam Khánh | 7.3.4 + 7.4 | Yêu cầu khác + Kết luận |

---

## 7.1. Giới thiệu

> **Người thực hiện: Nguyễn Hồng Phúc**

### 7.1.1. Phạm vi

**Hệ thống Quản lý Nhân sự (HRMS)** là hệ thống ứng dụng web nhiều người dùng phục vụ lĩnh vực quản lý nhân sự trong môi trường giáo dục đại học tại Trường Đại học Thủy Lợi. Hệ thống được xây dựng để tập trung hóa hoạt động quản lý nhân sự cho các đơn vị đào tạo, đơn vị nghiên cứu khoa học, các phòng ban chức năng và các đơn vị trực thuộc nhà trường.

Ở mức phạm vi sản phẩm, hệ thống bao phủ các chức năng chính sau:

- xác thực người dùng, quản lý tài khoản và phân quyền theo vai trò;
- quản lý cơ cấu tổ chức theo mô hình cây cha–con;
- quản lý hồ sơ nhân sự, hợp đồng lao động, đánh giá khen thưởng/kỷ luật;
- quản lý bổ nhiệm, điều chuyển, bãi nhiệm nhân sự theo đơn vị;
- quản lý khóa đào tạo, kết quả đào tạo và chứng chỉ;
- quản lý danh mục tham chiếu như hệ số lương, loại phụ cấp, loại hợp đồng;
- cung cấp báo cáo, thống kê nhân sự;
- hỗ trợ chức năng tự phục vụ cho cán bộ, giảng viên, nhân viên;
- ghi vết hoạt động và hỗ trợ truy vết kiểm toán.

Ngoài phạm vi sản phẩm của phiên bản hiện tại:

- các luồng tác vụ cá nhân khác ngoài xem thông tin cá nhân, xem đơn vị công tác, đăng ký đào tạo và xem các khóa đào tạo đã đăng ký cùng trạng thái/kết quả;
- các chức năng chưa được phản ánh trong baseline FEAT hiện tại của dự án, như quản lý nghỉ phép, chấm công, tính lương hoặc tuyển dụng.

### 7.1.2. Tổng quan về tài liệu

Tài liệu SRS này được tổ chức như sau:

- **Mục 7.1** mô tả phạm vi và cách tài liệu được tổ chức.
- **Mục 7.2** trình bày bối cảnh sản phẩm, nhóm người dùng, tác nhân hệ thống và các chức năng chính ở mức tổng quan.
- **Mục 7.3.1** mô tả các yêu cầu giao diện áp dụng ở mức toàn hệ thống.
- **Mục 7.3.2** mô tả các yêu cầu chức năng chính của hệ thống.
- **Mục 7.3.3** mô tả các yêu cầu bổ sung, yêu cầu phi chức năng và ràng buộc kỹ thuật.
- **Mục 7.3.4** mô tả các quy tắc truy vết, tổ chức requirement, thuộc tính requirement và các giả định/phụ thuộc dùng để quản lý bộ yêu cầu.

SRS này là tài liệu tổng hợp ở mức hệ thống. Tài liệu không thay thế các nguồn chi tiết như bộ **Use Case Specification (UCS)** hay tài liệu **supplementary requirements/metrics**; các tài liệu đó vẫn là nguồn chuẩn cho hành vi chi tiết và các ngưỡng xác minh tương ứng.

Về quan hệ tài liệu, SRS này tổng hợp nội dung ở mức hệ thống từ các nguồn **STR**, **VIS**, **UCS** và **SS** để phục vụ đặc tả và quản lý yêu cầu thống nhất trong dự án.

Các tài liệu nền tảng liên quan đến SRS này gồm:

| Tài liệu | Vai trò |
| --- | --- |
| Kế hoạch quản lý yêu cầu (RMP) | Định nghĩa loại requirement, thuộc tính, truy vết và tổ chức bộ tài liệu |
| Yêu cầu của các bên liên quan (STR) | Nguồn chuẩn cho STRQ; trong baseline hiện tại nội dung STRQ và FEAT đang được gộp trong `stakeholder-interviews.md` |
| Tài liệu tầm nhìn (VIS) | Vai trò logic là nguồn chuẩn cho FEAT và phạm vi sản phẩm; trong baseline hiện tại chưa tách thành file riêng và đang được gộp trong `stakeholder-interviews.md`; riêng mã FEAT trình bày trong SRS được chuẩn hóa theo baseline hợp nhất đang dùng trong bộ tài liệu output |
| Mô hình hóa yêu cầu và bộ Use Case Specification (UCS) | Nguồn chuẩn cho tác nhân, nhóm use case, SCEN và hành vi chức năng chi tiết; riêng mã UC trình bày trong SRS tuân theo baseline UCS hợp nhất đang dùng trong các tài liệu output |
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

---

## 7.2. Mô tả chung

> **Người thực hiện: Nguyễn Hồng Phúc**

### 7.2.1. Mô tả chung về giao diện

HRMS là hệ thống **ứng dụng web nhiều người dùng**. Người dùng truy cập hệ thống qua trình duyệt, thao tác nghiệp vụ trên giao diện web, và toàn bộ xử lý nghiệp vụ được thực hiện thông qua các API của hệ thống. Người dùng chủ yếu là cán bộ, giảng viên và nhân viên hành chính tại trường Đại học Thủy Lợi, thao tác trên máy tính để bàn trong môi trường mạng nội bộ hoặc Internet.

Các nhóm người dùng và tác nhân hệ thống chính của HRMS gồm:

| Nhóm người dùng / tác nhân | Vai trò sử dụng chính |
| --- | --- |
| Quản trị viên (Admin) | Quản lý tài khoản, phân quyền, quản lý cơ cấu tổ chức, xem nhật ký hệ thống |
| Phòng TCCB | Thực hiện nghiệp vụ quản lý hồ sơ, hợp đồng, đào tạo, đánh giá, điều chuyển/bổ nhiệm, cấu hình danh mục |
| Phòng TCKT | Tra cứu hồ sơ, xem dữ liệu phục vụ lương/phụ cấp, xem và xuất báo cáo thống kê |
| Cán bộ / Giảng viên / Nhân viên | Xem thông tin cá nhân, xem đơn vị công tác, đăng ký đào tạo, xem các khóa đào tạo đã đăng ký cùng trạng thái tham gia và kết quả |
| Hệ thống (System Timer / Auto-Job) | Thực hiện các tác vụ tự động: đăng xuất phiên hết hạn (FEAT 1.3), khóa tài khoản nhân sự thôi việc (FEAT 2.6), tự động đánh dấu thôi việc khi hợp đồng hết hạn (FEAT 8.6), ghi vết hoạt động (FEAT 6.1) |

Đặc điểm giao diện ở mức tổng quan:

- giao diện sử dụng tiếng Việt và điều hướng theo vai trò;
- sau đăng nhập, người dùng được đưa đến trang chính với nội dung phù hợp vai trò được phân quyền;
- hệ thống sử dụng các mẫu màn hình chính: danh sách có tìm kiếm/lọc, form nhập liệu, màn hình chi tiết, màn hình thống kê, hộp thoại xác nhận và chức năng import/export;
- hệ thống ưu tiên khai thác trên máy tính để bàn; yêu cầu hỗ trợ máy tính bảng được quy định chi tiết tại Mục 7.3.1 (UI-05, UI-06);
- hệ thống hỗ trợ nhập dữ liệu từ tệp Excel và xuất dữ liệu ra định dạng PDF, Excel theo quy định tại NFR-IC04.

### 7.2.2. Các chức năng chính

| Nhóm chức năng | Mô tả tổng quan | Truy vết chính |
| --- | --- | --- |
| Quản lý truy cập | Đăng nhập, đăng xuất, đổi mật khẩu, tự động đăng xuất khi không tương tác trong 30 phút | FEAT 1.1–1.4 |
| Nền tảng truy cập web | Cung cấp ứng dụng web nhiều người dùng; mọi thao tác nghiệp vụ được xử lý qua API | FEAT 1.5 |
| Quản trị tài khoản | Tìm kiếm, thêm, sửa, khóa/mở khóa tài khoản, phân quyền | FEAT 2.1–2.6 |
| Quản lý cơ cấu tổ chức | Thiết lập cây đơn vị, cập nhật thông tin đơn vị, giải thể/sáp nhập | FEAT 3.1–3.5 |
| Bố trí nhân sự theo đơn vị | Bổ nhiệm, điều chuyển, bãi nhiệm nhân sự trong cơ cấu tổ chức | FEAT 9.1–9.3 |
| Quản lý hợp đồng | Tạo, xem, sửa, chấm dứt hợp đồng lao động | FEAT 7.1–7.4 |
| Quản lý đánh giá | Ghi nhận và tra cứu khen thưởng/kỷ luật | FEAT 10.1–10.3 |
| Quản lý hồ sơ nhân sự | Tìm kiếm, lọc, tạo mới, chỉnh sửa, xem chi tiết, in/xuất, đánh dấu thôi việc, cấu hình ẩn/hiện mục khen thưởng – kỷ luật | FEAT 8.1–8.9 |
| Quản lý đào tạo | Mở khóa đào tạo, chỉnh sửa, xem khóa học, ghi nhận kết quả | FEAT 11.1–11.4 |
| Cấu hình danh mục | Quản lý hệ số lương, loại phụ cấp, loại hợp đồng | FEAT 4.1–4.5 |
| Báo cáo và thống kê | Xem và xuất thống kê nhân sự, hợp đồng, đào tạo, bổ nhiệm | FEAT 5.1–5.4 |
| Tự phục vụ cá nhân | Xem hồ sơ cá nhân, xem đơn vị công tác, đăng ký đào tạo, xem các khóa đào tạo đã đăng ký cùng trạng thái tham gia và kết quả | FEAT 12.1–12.4 |
| Ghi vết và kiểm toán | Tự động ghi nhật ký hoạt động (audit log) và cho phép quản trị viên truy xuất nhật ký | FEAT 6.1–6.2 |

---

## 7.3. Các yêu cầu cụ thể

### 7.3.1. Các yêu cầu về giao diện

> **Người thực hiện: Nguyễn Hải Ninh**

| Mã | Yêu cầu | Mức ưu tiên | Truy vết nguồn |
| --- | --- | --- | --- |
| UI-01 | Hệ thống phải sử dụng tiếng Việt trên 100% màn hình, trừ các thuật ngữ kỹ thuật. | M | SUPL-U01 |
| UI-02 | Hệ thống phải áp dụng thống nhất bố cục, màu sắc và font chữ trên toàn hệ thống; số cặp màn hình thuộc cùng một mẫu giao diện có khác biệt về bố cục, màu sắc hoặc font chữ phải bằng 0. | M | SUPL-U01 |
| UI-03 | Hệ thống phải hiển thị 100% lỗi nhập liệu và lỗi nghiệp vụ bằng tiếng Việt, kèm mô tả nguyên nhân và ít nhất một gợi ý khắc phục. | M | SUPL-U03 |
| UI-04 | Hệ thống phải hiển thị 100% lỗi hệ thống bằng tiếng Việt và thông báo lỗi phải cho biết người dùng cần thử lại thao tác hay liên hệ bộ phận hỗ trợ. | M | SUPL-U03 |
| UI-05 | Ở độ phân giải từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang. | E | SUPL-U05 |
| UI-06 | Trên tablet 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện thao tác chính mà không cần phóng to. | E | SUPL-U05 |
| UI-07a | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập. | N | SUPL-U06 |
| UI-07b | Trên 100% form có nút xác nhận mặc định, phím Enter phải kích hoạt nút đó. | N | SUPL-U06 |
| UI-07c | 100% trang phải hiển thị breadcrumb để người dùng quay lại cấp điều hướng trước. | N | SUPL-U06 |
| UI-08 | Hệ thống phải hiển thị hộp thoại xác nhận trước 100% thao tác khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng trước hạn, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái làm mất hiệu lực dữ liệu hoặc quyền truy cập. | M | SUPL-U07 |

### 7.3.2. Các yêu cầu chức năng

> **Người thực hiện: Nguyễn Hải Ninh**

Phần này tổng hợp các hành vi tương tác giữa tác nhân và hệ thống ở mức SRS, được rút gọn từ bộ **Use Case Specification (UCS)** của dự án. Điều kiện kích hoạt, tiền điều kiện, luồng cơ bản/luồng thay thế và các yêu cầu đặc thù chi tiết tiếp tục được quản lý tại các tài liệu UCS tương ứng; các mã **FR-*** dưới đây chỉ là mã trình bày cục bộ để nhóm nội dung trong SRS. Trong baseline SRS hiện tại, mã **FEAT** và **UC** dùng trong mục này tuân theo danh mục hợp nhất đang được dùng cùng bộ UCS đã tích hợp vào tài liệu.

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
| FR-ACC-10 | Hệ thống phải tự động khóa tài khoản liên kết khi nhân sự tương ứng được cập nhật sang trạng thái thôi việc. | Hệ thống | FEAT 2.6, UC 4.8 A2 |
| FR-ACC-11 | Hệ thống phải cho phép Quản trị viên xem, tìm kiếm và lọc nhật ký hệ thống theo các tiêu chí được hỗ trợ. | Quản trị viên | FEAT 6.2, UC 4.24 |
| FR-ACC-12 | Hệ thống phải cho phép Quản trị viên xuất nhật ký hệ thống theo phạm vi dữ liệu đang được áp dụng. | Quản trị viên | FEAT 6.2, UC 4.24 A1 |

#### 7.3.2.2. Cơ cấu tổ chức và bố trí nhân sự

Nhóm yêu cầu này khai thác cơ cấu tổ chức dưới dạng cây cha–con ở mức hành vi nghiệp vụ. Ràng buộc tính hợp lệ của cây tổ chức được quy định tại mục 7.3.3 (NFR-DC02).

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-ORG-01 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB tạo mới đơn vị tổ chức trong cơ cấu cây cha–con của hệ thống. | Quản trị viên, Phòng TCCB | FEAT 3.1, FEAT 3.2, UC 4.9 |
| FR-ORG-02 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB cập nhật thông tin của đơn vị tổ chức đã tồn tại. | Quản trị viên, Phòng TCCB | FEAT 3.3, UC 4.10 |
| FR-ORG-03 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB thay đổi trạng thái đơn vị tổ chức sang giải thể hoặc sáp nhập theo quy tắc nghiệp vụ. | Quản trị viên, Phòng TCCB | FEAT 3.4, UC 4.11 |
| FR-ORG-04 | Hệ thống phải cho phép Quản trị viên và Phòng TCCB xem chi tiết thông tin của một đơn vị tổ chức, bao gồm trạng thái, nhân sự trực thuộc và lịch sử liên quan. | Quản trị viên, Phòng TCCB | FEAT 3.5, UC 4.12 |
| FR-ORG-05 | Hệ thống phải cho phép Phòng TCCB bổ nhiệm nhân sự vào đơn vị tổ chức khi nhân sự có trạng thái làm việc là “Đang chờ xét”, trạng thái hợp đồng là “Còn hiệu lực”, và đơn vị đích không ở trạng thái giải thể hoặc sáp nhập. | Phòng TCCB | FEAT 9.1, UC 4.38 |
| FR-ORG-06 | Hệ thống phải cho phép Phòng TCCB điều chuyển nhân sự đang ở trạng thái làm việc “Đang công tác” và có trạng thái hợp đồng là “Còn hiệu lực” hoặc “Chờ gia hạn” sang đơn vị tổ chức khác; hệ thống phải từ chối thao tác nếu đơn vị liên quan ở trạng thái giải thể hoặc sáp nhập. | Phòng TCCB | FEAT 9.2, UC 4.38 A1 |
| FR-ORG-07 | Hệ thống phải cho phép Phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức khi đơn vị chưa ở trạng thái giải thể hoặc sáp nhập, đồng thời cập nhật trạng thái công việc của nhân sự thành “Đang chờ xét”. | Phòng TCCB | FEAT 9.3, UC 4.39 |

#### 7.3.2.3. Danh mục tham chiếu và hồ sơ nhân sự

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-CFG-01 | Hệ thống phải cho phép Phòng TCCB thêm mới danh mục hệ số lương. | Phòng TCCB | FEAT 4.1, UC 4.13 |
| FR-CFG-02 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa danh mục hệ số lương chưa bị ràng buộc bởi các điều kiện từ chối của hệ thống. | Phòng TCCB | FEAT 4.2, UC 4.14 |
| FR-CFG-03a | Hệ thống phải cho phép Phòng TCCB xóa danh mục hệ số lương khi danh mục chưa được sử dụng và đáp ứng quy tắc nghiệp vụ. | Phòng TCCB | FEAT 4.3, UC 4.15 |
| FR-CFG-03b | Hệ thống phải cho phép Phòng TCCB thay đổi trạng thái danh mục hệ số lương theo tình trạng sử dụng và quy tắc nghiệp vụ. | Phòng TCCB | FEAT 4.3, UC 4.16 |
| FR-CFG-04a | Hệ thống phải cho phép Phòng TCCB thêm mới danh mục loại phụ cấp. | Phòng TCCB | FEAT 4.4, UC 4.17 |
| FR-CFG-04b | Hệ thống phải cho phép Phòng TCCB chỉnh sửa danh mục loại phụ cấp đang ở trạng thái cho phép chỉnh sửa. | Phòng TCCB | FEAT 4.4, UC 4.18 |
| FR-CFG-04c | Hệ thống phải cho phép Phòng TCCB thay đổi trạng thái danh mục loại phụ cấp theo quy tắc nghiệp vụ. | Phòng TCCB | FEAT 4.4, UC 4.19 |
| FR-CFG-05a | Hệ thống phải cho phép Phòng TCCB thêm mới danh mục loại hợp đồng, bao gồm tên loại hợp đồng, số tháng tối thiểu, số tháng tối đa, số lần gia hạn tối đa và thời gian chờ gia hạn. | Phòng TCCB | FEAT 4.5, UC 4.20 |
| FR-CFG-05b | Hệ thống phải cho phép Phòng TCCB chỉnh sửa các thông tin cấu hình của danh mục loại hợp đồng, bao gồm số tháng tối thiểu, số tháng tối đa, số lần gia hạn tối đa và thời gian chờ gia hạn, khi danh mục đang ở trạng thái cho phép chỉnh sửa. | Phòng TCCB | FEAT 4.5, UC 4.21 |
| FR-CFG-05c | Hệ thống phải cho phép Phòng TCCB thay đổi trạng thái danh mục loại hợp đồng giữa “Đang sử dụng” và “Ngừng sử dụng” theo quy tắc nghiệp vụ. | Phòng TCCB | FEAT 4.5, UC 4.22 |
| FR-HR-01 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT tìm kiếm hồ sơ nhân sự bằng các từ khóa được hệ thống hỗ trợ. | Phòng TCCB, Phòng TCKT | FEAT 8.1, UC 4.29 |
| FR-HR-02 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT lọc danh sách hồ sơ nhân sự theo nhiều tiêu chí nghiệp vụ. | Phòng TCCB, Phòng TCKT | FEAT 8.2, UC 4.30 |
| FR-HR-03 | Hệ thống phải cho phép Phòng TCCB tạo mới hồ sơ nhân sự bằng nhập tay hoặc import từ Excel theo mẫu dữ liệu được hệ thống hỗ trợ. | Phòng TCCB | FEAT 8.3, UC 4.31 |
| FR-HR-04 | Khi tạo mới hồ sơ nhân sự, hệ thống phải tự động cấp mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng, đồng thời khởi tạo trạng thái hợp đồng là “Chưa hợp đồng” và trạng thái làm việc là “Đang chờ xét”. | Phòng TCCB, Hệ thống | FEAT 8.3, SUPL-F02, UC 4.31 |
| FR-HR-05 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa hồ sơ nhân sự chỉ khi hồ sơ đang ở trạng thái làm việc “Đang chờ xét” hoặc “Đang công tác”; hệ thống phải từ chối chỉnh sửa hồ sơ ở trạng thái “Đã thôi việc”. | Phòng TCCB | FEAT 8.4, UC 4.32 |
| FR-HR-06 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xem chi tiết hồ sơ nhân sự theo quyền hạn được cấp. | Phòng TCCB, Phòng TCKT | FEAT 8.7, UC 4.35 |
| FR-HR-07a | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT in hồ sơ nhân sự theo quyền được cấp. | Phòng TCCB, Phòng TCKT | FEAT 8.8, UC 4.36 |
| FR-HR-07b | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xuất hồ sơ nhân sự ra Excel theo quyền được cấp. | Phòng TCCB, Phòng TCKT | FEAT 8.8, UC 4.36 |
| FR-HR-08 | Hệ thống phải cho phép Phòng TCCB đánh dấu thôi việc cho nhân sự sau khi nhập ngày thôi việc và lý do thôi việc; hệ thống phải từ chối thao tác nếu nhân sự đang giữ chức vụ quản lý chưa được bãi nhiệm và phải cập nhật các trạng thái liên quan theo quy tắc nghiệp vụ khi thao tác thành công. | Phòng TCCB | FEAT 8.5, UC 4.33 |
| FR-HR-09 | Hệ thống phải tự động đánh dấu thôi việc cho nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. | Hệ thống | FEAT 8.6, UC 4.34 |
| FR-HR-10 | Hệ thống phải cho phép Phòng TCCB cấu hình ẩn/hiện các mục khen thưởng và kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc Phòng TCCB. | Phòng TCCB | FEAT 8.9, UC 4.37 |

#### 7.3.2.4. Hợp đồng, đánh giá, đào tạo, báo cáo và tự phục vụ

| Mã | Yêu cầu | Tác nhân chính | Truy vết nguồn |
| --- | --- | --- | --- |
| FR-CON-01 | Hệ thống phải cho phép Phòng TCCB tạo hợp đồng lao động mới cho nhân sự đủ điều kiện theo loại hợp đồng, thời hạn, số lần ký và thời gian chờ gia hạn được cấu hình. | Phòng TCCB | FEAT 7.1, UC 4.25 |
| FR-CON-02 | Hệ thống phải cho phép Phòng TCCB xem danh sách và chi tiết hợp đồng lao động của nhân sự. | Phòng TCCB | FEAT 7.2, UC 4.26 |
| FR-CON-03 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa hợp đồng lao động khi hợp đồng đang ở trạng thái chưa có hiệu lực. | Phòng TCCB | FEAT 7.3, UC 4.27 |
| FR-CON-04 | Hệ thống phải cho phép Phòng TCCB chấm dứt trước hạn hợp đồng lao động đang còn hiệu lực sau khi nhập ngày chấm dứt và lý do chấm dứt hợp lệ, đồng thời cập nhật trạng thái hợp đồng tương ứng. | Phòng TCCB | FEAT 7.4, UC 4.28 |
| FR-EVA-01 | Hệ thống phải cho phép Phòng TCCB ghi nhận đánh giá khen thưởng hoặc kỷ luật cho nhân sự đang còn làm việc. | Phòng TCCB | FEAT 10.1, UC 4.40 |
| FR-EVA-02 | Hệ thống phải cho phép Phòng TCCB xem lịch sử đánh giá khen thưởng/kỷ luật của từng nhân sự. | Phòng TCCB | FEAT 10.2, UC 4.41 |
| FR-EVA-03 | Hệ thống phải cho phép Phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo tiêu chí được hỗ trợ. | Phòng TCCB | FEAT 10.3, UC 4.42 |
| FR-TRN-01 | Hệ thống phải cho phép Phòng TCCB mở khóa đào tạo mới cho cán bộ, giảng viên. | Phòng TCCB | FEAT 11.1, UC 4.43 |
| FR-TRN-02 | Hệ thống phải cho phép Phòng TCCB chỉnh sửa khóa đào tạo theo trạng thái và ràng buộc nghiệp vụ của khóa học. | Phòng TCCB | FEAT 11.2, UC 4.44 |
| FR-TRN-03 | Hệ thống phải cho phép Phòng TCCB xem chi tiết khóa đào tạo và danh sách người đã đăng ký. | Phòng TCCB | FEAT 11.3, UC 4.45 |
| FR-TRN-04 | Hệ thống phải cho phép Phòng TCCB ghi nhận kết quả đào tạo và lưu chứng chỉ vào hồ sơ nhân sự của người tham gia. | Phòng TCCB | FEAT 11.4, UC 4.46 |
| FR-RPT-01 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xem các báo cáo, thống kê về nhân sự, hợp đồng, đánh giá, đào tạo và bổ nhiệm. | Phòng TCCB, Phòng TCKT | FEAT 5.1–5.4, UC 4.23 |
| FR-RPT-02 | Hệ thống phải cho phép Phòng TCCB và Phòng TCKT xuất báo cáo, thống kê theo phạm vi dữ liệu đang được áp dụng. | Phòng TCCB, Phòng TCKT | FEAT 5.1–5.4, UC 4.23 A1 |
| FR-SELF-01 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem thông tin cá nhân của chính mình. | Người dùng (Cán bộ/Giảng viên/Nhân viên) | FEAT 12.1, UC 4.47 |
| FR-SELF-02 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem thông tin chi tiết đơn vị đang công tác và cơ cấu trực thuộc liên quan. | Người dùng (Cán bộ/Giảng viên/Nhân viên) | FEAT 12.2, UC 4.48 |
| FR-SELF-03 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên đăng ký hoặc hủy đăng ký tham gia khóa đào tạo đang mở đăng ký, còn chỉ tiêu và đáp ứng quy tắc nghiệp vụ. | Người dùng (Cán bộ/Giảng viên/Nhân viên) | FEAT 12.3, UC 4.49 |
| FR-SELF-04 | Hệ thống phải cho phép cán bộ, giảng viên và nhân viên xem danh sách các khóa đào tạo đã đăng ký, trạng thái tham gia, kết quả đào tạo và lịch sử đào tạo của mình. | Người dùng (Cán bộ/Giảng viên/Nhân viên) | FEAT 12.4, UC 4.50 |

### 7.3.3. Các yêu cầu bổ sung

> **Người thực hiện: Ngô Quang Tùng**

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
| NFR-R02 | Sau sự cố crash hoặc restart, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa 15 phút. | SUPL-P07a (gốc: SUPL-R02) |
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

> **Người thực hiện: Ngô Đức Nam Khánh**

#### 7.3.4.1. Quy tắc truy vết

Chuỗi truy vết của bộ yêu cầu phải tuân theo cấu trúc sau:

```text
STRQ ──→ FEAT ──→ UC ──→ SCEN
  │         │
  │         └──→ SUPL
  └──→ SUPL
```

Chi tiết các đường truy vết tối thiểu:

| Từ | Đến | Quan hệ | Ràng buộc bắt buộc |
| --- | --- | --- | --- |
| STRQ | FEAT | Nhiều-nhiều | Mỗi STRQ ở trạng thái `Approved` phải truy vết tới ít nhất một FEAT hoặc SUPL. |
| STRQ | SUPL | Nhiều-nhiều | Nằm trong ràng buộc bao phủ STRQ ở trên. |
| FEAT | UC | Nhiều-nhiều | Mỗi FEAT ở trạng thái `Approved` phải truy vết tới ít nhất một UC hoặc SUPL. |
| FEAT | SUPL | Nhiều-nhiều | Nằm trong ràng buộc bao phủ FEAT ở trên. |
| UC | FEAT | Truy vết ngược | Mỗi UC phải truy vết ngược về FEAT mà nó hiện thực hóa. |
| SUPL | FEAT | Truy vết ngược | Mỗi SUPL phải truy vết ngược về FEAT mà nó hỗ trợ. |
| UC | SCEN | Một-nhiều | Mỗi UC phải có ít nhất một SCEN tương ứng với luồng cơ bản. |

Các quy tắc bao phủ bắt buộc:

- mỗi **STRQ** ở trạng thái `Approved` phải truy vết tới ít nhất một **FEAT** hoặc **SUPL**;
- mỗi **FEAT** ở trạng thái `Approved` phải truy vết tới ít nhất một **UC** hoặc **SUPL**;
- mỗi **UC** phải có ít nhất một **SCEN** tương ứng với luồng cơ bản;
- **UC** và **SUPL** phải hỗ trợ truy vết ngược về **FEAT** mà chúng hiện thực hóa hoặc hỗ trợ.

#### 7.3.4.2. Loại requirement và quy tắc đặt requirement

| Loại requirement / artefact quản lý | Viết tắt | Vai trò | Nguồn chuẩn logic / vị trí baseline hiện tại |
| --- | --- | --- | --- |
| Stakeholder Request | STRQ | Ghi nhận nhu cầu và mong đợi của stakeholder trong problem domain | Nguồn chuẩn logic: STR; baseline hiện tại: `stakeholder-interviews.md` |
| Feature | FEAT | Biểu diễn các capability ở mức sản phẩm trong solution domain | Nguồn chuẩn logic: VIS; baseline hiện tại: `stakeholder-interviews.md` |
| Use Case | UC | Mô tả hành vi chức năng chi tiết theo tương tác giữa tác nhân và hệ thống | Nguồn chuẩn logic: UCS; trong baseline hiện tại danh mục/mapping tổng hợp có trong `requirement-modeling.md`, còn đặc tả chi tiết nằm trong các tài liệu UCS tương ứng |
| Scenario | SCEN | Mô tả các đường đi hợp lệ của từng use case | Nguồn chuẩn: các tài liệu UCS tương ứng |
| Supplementary Requirement | SUPL | Mô tả yêu cầu cross-cutting, NFR và constraint | Nguồn chuẩn: `supplementary-requirements.md` |
| Metric / Acceptance Criteria | Metric | Lượng hóa cách xác minh SUPL | Nguồn chuẩn: `supplementary-metrics.md` |

Quy tắc đặt requirement trong bộ tài liệu:

- Các mã **UI-**, **FR-**, **SR-**, **NFR-** trong SRS chỉ là mã trình bày cục bộ để nhóm nội dung; mã truy vết chuẩn dùng để quản lý requirement trong dự án vẫn là **STRQ**, **FEAT**, **UC**, **SCEN** và **SUPL**.
- Nội dung mô tả giao diện ở mức tổng quan phải nằm tại mục **7.2.1**; các yêu cầu giao diện có thể kiểm thử và áp dụng toàn hệ thống được tổng hợp tại mục **7.3.1** của SRS, với nguồn chuẩn ở **SS** trừ khi yêu cầu chỉ gắn với một **UCS** cụ thể.
- Các yêu cầu chỉ áp dụng cho một use case hoặc một bước luồng cụ thể phải có nguồn chuẩn tại tài liệu **UCS** tương ứng thay vì nâng lên mục **7.3.3**.
- Các yêu cầu áp dụng toàn hệ thống, cắt ngang nhiều use case, phi chức năng hoặc ràng buộc kỹ thuật/pháp lý phải có nguồn chuẩn tại **SS**; mục **7.3.3** của SRS chỉ tổng hợp các yêu cầu này ở mức hệ thống.

#### 7.3.4.3. Thuộc tính requirement tối thiểu

| Loại requirement | Thuộc tính tối thiểu phải quản lý |
| --- | --- |
| STRQ | Status, Priority, Benefit, Effort, Risk, Stability, Reason |
| FEAT | Status, Priority, Benefit, Effort, Risk, Stability, Difficulty, Target Release, Assigned To, Reason, Transformation |
| UC | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason, Actor |
| SUPL | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason |

#### 7.3.4.4. Báo cáo và chế độ xem requirement

Các chế độ xem requirement tối thiểu phải duy trì trong baseline dự án gồm:

- ma trận thuộc tính cho STRQ, FEAT, UC và SUPL;
- ma trận truy vết STRQ → FEAT;
- ma trận truy vết STRQ → SUPL;
- ma trận truy vết FEAT → UC;
- ma trận truy vết FEAT → SUPL;
- ma trận truy vết UC → Design, với neo thiết kế chính hiện tại là `class-diagram.md`;
- báo cáo gap cho **STRQ** ở trạng thái `Approved` chưa truy vết tới **FEAT/SUPL**, **FEAT** ở trạng thái `Approved` chưa truy vết tới **UC/SUPL**, **UC** chưa có **SCEN** luồng cơ bản, và **UC/SUPL** chưa có truy vết ngược về **FEAT**;
- cây truy vết cho phép xem phân rã từ **STRQ** xuống **FEAT**, **UC**, **SCEN** và các **SUPL** liên quan theo chuỗi truy vết đã định nghĩa.

#### 7.3.4.5. Giả định, phụ thuộc và ghi chú chuẩn hóa nguồn

- Trong baseline hiện tại, **FEAT 1.5** được truy vết tới **SUPL-DC01** như một ràng buộc kiến trúc; mục này không có **UC** riêng.
- Tài liệu **stakeholder-interviews.md** hiện là nguồn chuẩn chứa chung STRQ và nội dung FEAT, thay cho việc tách riêng tài liệu STR và VIS.
- Trong baseline SRS hợp nhất hiện tại, mã FEAT và mã UC dùng cho trình bày/truy vết trong SRS được chuẩn hóa theo danh mục đã tích hợp trong `output/final-report.md` và `output/Tung/uc-tung.md`.
- Trong baseline hiện tại, `requirement-modeling.md` giữ vai trò nguồn logic cho mô hình tác nhân và mapping tổng quan; nội dung UCS chi tiết đang được phân bố giữa `output/final-report.md` (UC 4.1–4.24 và UC 4.38–4.50) và `output/Tung/uc-tung.md` (UC 4.25–4.37).
- Khi cần đối chiếu quy tắc truy vết, thuộc tính requirement và mapping tài liệu, **requirement-management-plan.md** là nguồn chuẩn quản lý requirement của dự án.
- Khi cần đối chiếu nguồn nội dung, tài liệu thu thập stakeholder là nguồn chuẩn cho STRQ/FEAT, bộ UCS là nguồn chuẩn cho hành vi chức năng chi tiết, và bộ SUPL cùng tài liệu độ đo là nguồn chuẩn cho các ngưỡng NFR.

---

## 7.4. Kết luận

> **Người thực hiện: Ngô Đức Nam Khánh**

SRS này tổng hợp phạm vi, hành vi chức năng, yêu cầu giao diện, yêu cầu bổ sung và các quy tắc quản lý requirement cho HRMS của Trường Đại học Thủy Lợi. Tài liệu là cơ sở để tiếp tục thiết kế, triển khai, kiểm thử và kiểm soát thay đổi yêu cầu trong các giai đoạn tiếp theo của dự án.
