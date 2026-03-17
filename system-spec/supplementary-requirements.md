# ĐẶC TẢ YÊU CẦU BỔ SUNG (Supplementary Requirements Specification)

## Hệ thống Quản lý Nhân sự (HRMS) — Trường Đại học Thủy Lợi

> **Mã tài liệu:** HRMS-SUPL-001
> **Ngày lập:** 13/03/2026
> **Phiên bản:** 1.0
> **Tham chiếu:** Kế hoạch Quản lý Yêu cầu (RMP), Đặc tả Ca sử dụng (UCS)

---

## Mục lục

1. [Giới thiệu](#1-giới-thiệu)
2. [Danh sách yêu cầu bổ sung / yêu cầu phi chức năng](#2-danh-sách-yêu-cầu-bổ-sung--yêu-cầu-phi-chức-năng)
3. [Thiết lập độ đo và tiêu chuẩn đáp ứng](#3-thiết-lập-độ-đo-và-tiêu-chuẩn-đáp-ứng)
4. [Ma trận truy vết NFR → FEAT/UC](#4-ma-trận-truy-vết-nfr--featuc)
5. [Phân tích Softgoals và Trade-offs](#5-phân-tích-softgoals-và-trade-offs)

---

## 1. Giới thiệu

### 1.1. Mục đích

Tài liệu này mô tả chi tiết các **yêu cầu bổ sung (Supplementary Requirements)** và **yêu cầu phi chức năng (Non-Functional Requirements - NFR)** của Hệ thống Quản lý Nhân sự (HRMS) phục vụ Trường Đại học Thủy Lợi. Các yêu cầu này **không được thể hiện** trong mô hình ca sử dụng (Use Case) nhưng vẫn là điều kiện thiết yếu để đảm bảo chất lượng và khả năng vận hành của hệ thống.

### 1.2. Phạm vi

Tài liệu bao gồm:
- Các yêu cầu phi chức năng được phân loại theo mô hình **FURPS+** (Functionality, Usability, Reliability, Performance, Supportability + Constraints)
- Các **yếu tố chất lượng** (Quality Factors) liên quan
- Các **độ đo yêu cầu** (Metrics) cụ thể, lượng hóa được
- Các **tiêu chuẩn đáp ứng** (Acceptance Criteria) cho từng độ đo
- Các **đại lượng thay thế** (Proxies) khi NFR khó đo trực tiếp

### 1.3. Phương pháp phân loại

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

### 1.4. Mức độ ưu tiên

| Ký hiệu | Mức độ | Ý nghĩa |
|----------|--------|----------|
| **M** | Mandatory (Bắt buộc) | Không thể thiếu, hệ thống không đạt nghiệm thu nếu thiếu |
| **E** | Expected (Mong đợi) | Nên có, được kỳ vọng bởi phần lớn stakeholders |
| **N** | Nice to have (Có thì tốt) | Tùy chọn, không ảnh hưởng nghiệm thu |

---

## 2. Danh sách yêu cầu bổ sung / yêu cầu phi chức năng

### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F01** | Ghi nhật ký hệ thống tự động (Auto Logging) | Hệ thống tự động ghi lại mọi hành động truy cập, thêm mới/cập nhật dữ liệu, thay đổi trạng thái và thay đổi cấu hình với đầy đủ các thông tin: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. Tham chiếu FEAT 12.1. | **M** |
| **SUPL-F02** | Tự động sinh mã nhân sự | Khi tạo mới hồ sơ nhân sự, hệ thống tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. | **M** |
| **SUPL-F03** | Tự động đăng xuất phiên không hoạt động | Hệ thống tự động đăng xuất phiên làm việc nếu người dùng không thao tác trong 30 phút. Tham chiếu FEAT 1.3. | **M** |
| **SUPL-F04** | Tự động khóa tài khoản nhân sự thôi việc | Khi nhân sự được đánh dấu thôi việc (FEAT 7.5/7.6), hệ thống tự động chuyển tài khoản của nhân sự đó sang trạng thái khóa. Tham chiếu FEAT 2.6. | **M** |
| **SUPL-F05** | Tự động chuyển trạng thái hợp đồng | Hệ thống tự động chuyển trạng thái hợp đồng từ "Còn hiệu lực" sang "Chờ gia hạn" khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. | **M** |
| **SUPL-F06** | Tự động cập nhật trạng thái tham gia đào tạo | Khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang trạng thái "Đang đào tạo", hệ thống tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang trạng thái "Đang học". | **M** |
| **SUPL-F07** | Quy tắc nghiệp vụ chung về thay đổi trạng thái | Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ thao tác thay đổi trạng thái theo quy tắc nghiệp vụ để đảm bảo tính toàn vẹn dữ liệu và phục vụ kiểm toán. | **M** |
| **SUPL-F08** | Bảo vệ mật khẩu lưu trữ | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. | **M** |

### 2.2. Usability – Tính dễ sử dụng

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-U01** | Giao diện tiếng Việt và nhất quán | 100% màn hình phải sử dụng Tiếng Việt, trừ thuật ngữ kỹ thuật; đồng thời bố cục, màu sắc và font chữ phải được áp dụng thống nhất trên toàn bộ hệ thống. | **M** |
| **SUPL-U02** | Dễ học cho người dùng mới | Sau tối đa 2 giờ đào tạo hướng dẫn, ít nhất 95% người dùng mới thuộc phòng TCCB phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự; ít nhất 95% người dùng mới thuộc phòng TCKT phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. | **E** |
| **SUPL-U03** | Thông báo lỗi rõ ràng | Mọi lỗi nhập liệu hoặc lỗi hệ thống phải hiển thị thông báo bằng Tiếng Việt, rõ ràng, mô tả nguyên nhân và hướng dẫn khắc phục. | **M** |
| **SUPL-U04** | Hỗ trợ tìm kiếm và lọc đa tiêu chí | Các danh sách dữ liệu (nhân sự, hợp đồng, đơn vị) phải hỗ trợ tìm kiếm theo từ khóa và lọc đa tiêu chí để giảm thời gian thao tác. | **M** |
| **SUPL-U05** | Hiển thị ổn định trên desktop và tablet | Ở độ phân giải desktop từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang; trên tablet 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện các thao tác chính mà không cần phóng to. | **E** |
| **SUPL-U06** | Điều hướng nhanh bằng bàn phím và breadcrumb | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập; trên 100% form có nút xác nhận mặc định, phím Enter phải kích hoạt nút đó; 100% trang phải hiển thị breadcrumb để người dùng quay lại cấp điều hướng trước. | **N** |
| **SUPL-U07** | Xác nhận trước thao tác quan trọng | Hệ thống hiển thị hộp thoại xác nhận trước các thao tác quan trọng: khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng lao động trước hạn, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương. | **M** |

### 2.3. Reliability – Độ tin cậy

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-R01** | Tính sẵn sàng cao (High Availability) | Hệ thống phải sẵn sàng phục vụ trong khung thời gian 7:00–22:00 hằng ngày với tỷ lệ uptime tối thiểu 99.5% trên tổng thời gian phục vụ trong tháng, không tính thời gian bảo trì theo kế hoạch. | **M** |
| **SUPL-R02** | Khả năng phục hồi sau sự cố | Hệ thống có khả năng khởi động lại và phục hồi hoạt động bình thường trong tối đa 15 phút sau sự cố crash/restart. | **M** |
| **SUPL-R03** | Sao lưu dữ liệu tự động | Dữ liệu nghiệp vụ và tệp đính kèm của hệ thống phải được sao lưu tự động ít nhất mỗi 24 giờ và các bản sao lưu phải được lưu giữ tối thiểu 30 ngày. | **M** |
| **SUPL-R04** | Toàn vẹn dữ liệu | Hệ thống phải bảo đảm các thao tác cập nhật dữ liệu quan trọng được thực hiện theo nguyên tắc toàn bộ hoặc không thực hiện phần nào; nếu có lỗi ở bất kỳ bước nào, dữ liệu phải được khôi phục về trạng thái trước khi thao tác bắt đầu. | **M** |
| **SUPL-R05** | Không mất dữ liệu khi phiên hết hạn | Đối với form có dữ liệu đã nhập nhưng chưa lưu, hệ thống phải cảnh báo cho người dùng trước 5 phút khi phiên làm việc sắp hết hạn và phải khôi phục lại dữ liệu đã nhập gần nhất sau khi người dùng đăng nhập lại. | **E** |

### 2.4. Performance – Hiệu năng

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-P01** | Thời gian phản hồi giao diện | Các thao tác nghiệp vụ cơ bản (xem danh sách, xem chi tiết, thêm/sửa, thay đổi trạng thái khi được hỗ trợ) trên các màn hình nhân sự, hợp đồng lao động và đánh giá khen thưởng/kỷ luật phải hoàn thành hiển thị trong thời gian phản hồi chấp nhận được tùy số người dùng đồng thời. | **M** |
| **SUPL-P02** | Số lượng người dùng đồng thời | Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời mà không suy giảm hiệu năng đáng kể (thời gian phản hồi tăng ≤ 50% so với tải thấp). | **M** |
| **SUPL-P03** | Thời gian tạo báo cáo thống kê | Dashboard thống kê và báo cáo tổng hợp (FEAT 10.1) phải hoàn thành render trong thời gian chấp nhận được. | **E** |
| **SUPL-P04** | Hiệu năng tìm kiếm và lọc | Tìm kiếm và lọc danh sách nhân sự, danh sách đánh giá khen thưởng/kỷ luật (FEAT 6.3, FEAT 7.1, FEAT 7.2) trên tập dữ liệu lớn phải trả kết quả nhanh chóng. | **M** |
| **SUPL-P05** | Hiệu năng upload/download file | Upload và download file đính kèm (PDF bằng cấp, chứng chỉ, hợp đồng) phải hoàn thành trong thời gian hợp lý. | **E** |
| **SUPL-P06** | Hiệu năng xuất Excel | Xuất danh sách nhân sự ra file Excel (FEAT 7.8) phải hoàn thành trong thời gian chấp nhận được. | **E** |

### 2.5. Security – Bảo mật

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-SE01** | Xác thực người dùng (Authentication) | Mọi truy cập vào hệ thống phải qua xác thực bằng tài khoản/mật khẩu. Mật khẩu phải đáp ứng chính sách: tối thiểu 8 ký tự, bao gồm chữ hoa, chữ thường và số. | **M** |
| **SUPL-SE02** | Phân quyền truy cập (Authorization) | Hệ thống phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Nhân sự) – mỗi vai trò chỉ truy cập được các chức năng được cấp quyền. Mọi request API phải kiểm tra quyền trước khi xử lý. | **M** |
| **SUPL-SE03** | Bảo vệ chống tấn công brute-force | Khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp. Thời gian khóa tối thiểu 15 phút. | **M** |
| **SUPL-SE04** | Mã hóa truyền tải dữ liệu (HTTPS) | Toàn bộ giao tiếp giữa client và server phải sử dụng giao thức HTTPS (TLS 1.2 trở lên). | **M** |
| **SUPL-SE05** | Bảo vệ dữ liệu nhạy cảm | Dữ liệu nhạy cảm (số CCCD, số BHXH, thông tin ngân hàng) phải được bảo vệ – chỉ hiển thị cho vai trò được phép, ghi log khi truy cập. | **M** |
| **SUPL-SE06** | Ngăn chặn tấn công web trên chức năng nhập liệu và cập nhật dữ liệu | Hệ thống phải ngăn chặn các tấn công web làm giả yêu cầu hoặc chèn mã thực thi trên các chức năng nhập liệu và thao tác thay đổi dữ liệu. | **M** |
| **SUPL-SE07** | Chống SQL Injection | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu. | **M** |
| **SUPL-SE08** | Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật | Chỉ các vai trò được ủy quyền mới được phép cấu hình ẩn/hiện các mục khen thưởng/kỷ luật ở mức toàn hệ thống; mọi thay đổi cấu hình phải được ghi audit log với người thực hiện, thời gian, giá trị trước/sau. Tham chiếu FEAT 7.9. | **M** |
| **SUPL-SE09** | Kiểm soát chấm dứt hợp đồng trước hạn | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; hệ thống phải ghi audit log đầy đủ cho thao tác này gồm mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian và giá trị trước/sau. Tham chiếu FEAT 5.4. | **M** |

### 2.6. Supportability – Khả năng hỗ trợ & Bảo trì

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-S01** | Kiến trúc module hóa | Hệ thống phải được tổ chức thành các module chức năng có giao diện tích hợp rõ ràng để có thể nâng cấp hoặc thay thế từng module mà không buộc sửa đổi toàn bộ hệ thống. | **M** |
| **SUPL-S02** | Tài liệu kỹ thuật đầy đủ | Cung cấp tài liệu API cho backend, hướng dẫn triển khai và hướng dẫn sử dụng cho từng vai trò. | **E** |
| **SUPL-S03** | Khả năng mở rộng danh mục cấu hình | Hệ thống cho phép mở rộng các danh mục cấu hình (loại phụ cấp, loại hợp đồng, hệ số lương) mà không cần thay đổi mã nguồn. | **M** |
| **SUPL-S04** | Hỗ trợ gỡ lỗi (Debugging) | Hệ thống ghi log lỗi phía server theo nhiều cấp độ (ERROR, WARNING, INFO, DEBUG). Log phải bao gồm timestamp, request ID, stack trace. | **E** |
| **SUPL-S05** | Khả năng mở rộng quy mô (Scalability) | Hệ thống phải duy trì đầy đủ chức năng khi năng lực xử lý được mở rộng bằng cách bổ sung thêm nút ứng dụng trong cùng một môi trường khai thác. | **N** |

### 2.7. Design Constraints – Ràng buộc thiết kế

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-DC01** | Kiến trúc Client-Server | Hệ thống phải xây dựng theo mô hình Client-Server, frontend dạng SPA (Single Page Application) giao tiếp với backend qua RESTful API. | **M** |
| **SUPL-DC02** | Cơ cấu tổ chức dạng cây | Cơ cấu tổ chức đơn vị phải được mô hình hóa dưới dạng cấu trúc cây cha-con với gốc là Trường Đại học Thủy Lợi (FEAT 3.1). | **M** |
| **SUPL-DC03** | Tách biệt quyền theo vai trò | Thiết kế hệ thống phải đảm bảo phân tách quyền rõ ràng theo 4 vai trò đã xác định, sử dụng cơ chế Role-Based Access Control (RBAC). | **M** |

### 2.8. Implementation Constraints – Ràng buộc triển khai

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-IC01** | Ngôn ngữ và framework | Frontend: React.js (TypeScript). Backend: Laravel/PHP. Database: MySQL/MariaDB. | **M** |
| **SUPL-IC02** | Trình duyệt hỗ trợ | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox, Edge. | **M** |
| **SUPL-IC03** | Chuẩn mã hóa ký tự | Toàn bộ hệ thống sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ Tiếng Việt có dấu. | **M** |
| **SUPL-IC04** | Định dạng file đính kèm | Hệ thống hỗ trợ upload/download file PDF (bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động) và Excel (import/export nhân sự). Kích thước file tối đa: 10MB. | **M** |

### 2.9. Legal / Regulatory – Pháp lý

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-LR01** | Tuân thủ quy định bảo vệ dữ liệu cá nhân | Hệ thống phải hỗ trợ quản lý sự đồng ý thu thập dữ liệu cá nhân và xử lý yêu cầu hợp lệ về ẩn dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP. | **M** |
| **SUPL-LR02** | Tuân thủ quy chế quản lý nhân sự | Hệ thống phải cho phép cấu hình và sử dụng bộ danh mục loại hợp đồng, phụ cấp và chức danh theo danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt trên cơ sở quy định hiện hành của Bộ GD&ĐT và Bộ NN&PTNT. | **M** |
| **SUPL-LR03** | Lưu trữ hồ sơ theo quy định | Hồ sơ nhân sự, hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu theo thời gian quy định của pháp luật lao động Việt Nam và quy chế lưu trữ hiện hành. | **M** |

---

## 3. Thiết lập độ đo và tiêu chuẩn đáp ứng

### 3.1. Functionality — Yêu cầu chức năng bổ sung

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-F01** | Correctness (Tính đúng đắn) – Khả năng kiểm toán (Auditability) | Tỷ lệ hành động truy cập, thêm mới/cập nhật dữ liệu, thay đổi trạng thái và thay đổi cấu hình được ghi log / Tổng số hành động tương ứng phát sinh trên hệ thống | ≥ 100% các hành động truy cập, thêm mới/cập nhật dữ liệu, thay đổi trạng thái và thay đổi cấu hình đều được ghi log. Log phải bao gồm đầy đủ 9 trường thông tin (thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả, IP). |
| **SUPL-F02** | Correctness (Tính đúng đắn) | Tỷ lệ mã sinh tự động trùng lặp; Tỷ lệ mã tuân thủ mẫu mã đang áp dụng | 0% trùng lặp mã cán bộ. 100% hồ sơ nhân sự mới được cấp mã ngay khi tạo và 100% mã sinh ra tuân thủ mẫu mã đang áp dụng. |
| **SUPL-F03** | Correctness (Tính đúng đắn) – Tự động hóa | Thời gian phát hiện phiên không hoạt động | Hệ thống phát hiện và đăng xuất chính xác sau 30 phút (±30 giây) không hoạt động. |
| **SUPL-F04** | Correctness (Tính đúng đắn) – Tự động hóa | Thời gian khóa tài khoản sau khi đánh dấu thôi việc | Tài khoản bị khóa tự động trong ≤ 1 phút sau khi nhân sự được đánh dấu thôi việc. |
| **SUPL-F05** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái Chờ gia hạn đúng hạn | 100% hợp đồng đủ điều kiện được chuyển trạng thái trong ≤ 24 giờ kể từ thời điểm đủ điều kiện. |
| **SUPL-F06** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ bản ghi đăng ký được cập nhật đúng khi khóa đào tạo chuyển trạng thái | 100% bản ghi đăng ký thuộc khóa đào tạo đó được chuyển từ trạng thái "Đã đăng ký" sang "Đang học" trong ≤ 1 phút kể từ khi khóa đào tạo chuyển sang trạng thái "Đang đào tạo". |
| **SUPL-F07** | Integrity (Tính toàn vẹn) | Tỷ lệ thao tác thay đổi trạng thái của danh mục loại phụ cấp/loại hợp đồng tuân thủ đúng quy tắc; Số trường hợp thay đổi trạng thái làm sai lệch dữ liệu tham chiếu lịch sử | 100% thao tác thay đổi trạng thái của danh mục loại phụ cấp/loại hợp đồng tuân thủ đúng quy tắc nghiệp vụ. 0 trường hợp thay đổi trạng thái làm sai lệch dữ liệu tham chiếu lịch sử. |
| **SUPL-F08** | Security (Bảo mật) | Tỷ lệ mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; Số mật khẩu lưu dạng plaintext | 100% mật khẩu được lưu ở dạng không thể khôi phục nguyên văn. 0 mật khẩu lưu dạng plaintext. |

### 3.2. Usability — Tính dễ sử dụng

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-U01** | Usability – Tính nhất quán (Consistency) | Tỷ lệ màn hình sử dụng Tiếng Việt; Số cặp màn hình cùng loại có khác biệt về bố cục, màu sắc hoặc font chữ | 100% màn hình sử dụng Tiếng Việt (trừ thuật ngữ kỹ thuật). 0 cặp màn hình cùng loại có khác biệt về bố cục, màu sắc hoặc font chữ. |
| **SUPL-U02** | Usability – Learnability (Dễ học) | Thời gian đào tạo cho người dùng mới; Tỷ lệ người dùng mới hoàn thành bộ tác vụ cơ bản theo vai trò mà không cần trợ giúp trực tiếp | ≤ 2 giờ đào tạo. ≥ 95% người dùng mới phòng TCCB hoàn thành tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự; ≥ 95% người dùng mới phòng TCKT hoàn thành tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự. |
| **SUPL-U03** | Usability – Error Handling | Tỷ lệ lỗi có thông báo Tiếng Việt rõ ràng / Tổng số loại lỗi | 100% lỗi validation, lỗi nghiệp vụ, lỗi hệ thống đều có thông báo Tiếng Việt. Mỗi thông báo lỗi phải có ≥ 1 gợi ý khắc phục. |
| **SUPL-U04** | Usability – Efficiency (Hiệu quả thao tác) | Số bước thao tác để tìm kiếm và xem chi tiết 1 nhân sự | ≤ 3 bước (nhập từ khóa → tìm kiếm → click xem). Bộ lọc đa tiêu chí cho phép kết hợp ≥ 3 tiêu chí đồng thời. |
| **SUPL-U05** | Usability – Accessibility | Tỷ lệ màn hình không bị cắt nội dung, chồng lấn thành phần hoặc yêu cầu cuộn ngang ở 1366×768; Tỷ lệ màn hình cho phép thực hiện thao tác chính trên tablet 1024×768 mà không cần phóng to | 100% màn hình đạt tiêu chí ở độ phân giải 1366×768. ≥ 80% màn hình đạt tiêu chí trên tablet 1024×768. |
| **SUPL-U06** | Usability – Efficiency (Hiệu quả thao tác) | Tỷ lệ form hỗ trợ Tab navigation; Tỷ lệ form có nút xác nhận mặc định hỗ trợ phím Enter; Tỷ lệ trang hiển thị breadcrumb | ≥ 90% form nhập liệu hỗ trợ Tab navigation. 100% form có nút xác nhận mặc định hỗ trợ phím Enter. 100% trang có breadcrumb. |
| **SUPL-U07** | Usability – Error Prevention | Số thao tác quan trọng có hộp thoại xác nhận | 100% thao tác khóa tài khoản, thôi việc, chấm dứt hợp đồng trước hạn, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương đều có confirmation dialog. |

### 3.3. Reliability — Độ tin cậy

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-R01** | Availability (Tính sẵn sàng) | Uptime (%) = (Tổng thời gian hệ thống sẵn sàng phục vụ trong khung 7:00–22:00 / Tổng thời gian phục vụ dự kiến trong cùng khung giờ) × 100 | ≥ 99.5%/tháng trong khung 7:00–22:00, không tính bảo trì theo kế hoạch. |
| **SUPL-R02** | Recoverability (Khả năng phục hồi) | MTTR (Mean Time To Repair/Restart) | ≤ 15 phút từ lúc crash đến khi hệ thống phục vụ được request đầu tiên. |
| **SUPL-R03** | Recoverability (Khả năng phục hồi) – Sao lưu | Tần suất sao lưu; Thời gian lưu giữ bản sao lưu; RPO (Recovery Point Objective); RTO (Recovery Time Objective) | Thực hiện tối thiểu 1 bản sao lưu mỗi 24 giờ. Lưu giữ backup ≥ 30 ngày. RPO ≤ 24 giờ. RTO ≤ 4 giờ. |
| **SUPL-R04** | Integrity (Tính toàn vẹn dữ liệu) | Số trường hợp dữ liệu bất nhất quán sau thao tác lỗi; Tỷ lệ thao tác cập nhật quan trọng được khôi phục hoàn toàn khi lỗi xảy ra | 0 trường hợp dữ liệu bất nhất quán. 100% thao tác cập nhật quan trọng hoặc hoàn tất toàn bộ, hoặc không làm thay đổi dữ liệu khi có lỗi. |
| **SUPL-R05** | Fault Tolerance (Chịu lỗi) | Tỷ lệ form có dữ liệu nhập dở được khôi phục sau khi phiên hết hạn; Tỷ lệ phiên hết hạn có cảnh báo trước | ≥ 95% form có dữ liệu nhập dở được khôi phục sau khi người dùng đăng nhập lại. 100% phiên hết hạn hiển thị cảnh báo trước 5 phút. |

### 3.4. Performance — Hiệu năng

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-P01** | Speed (Tốc độ phản hồi) | Response time (giây) – P95 response time cho các thao tác nghiệp vụ cơ bản | Theo bảng tải: **0–10 người dùng:** ≤ 1 giây; **11–50 người dùng:** ≤ 2 giây; **51–100 người dùng:** ≤ 5 giây; **>100 người dùng:** ≤ 10 giây. |
| **SUPL-P02** | Capacity (Dung lượng / Khả năng chịu tải) | Số người dùng đồng thời tối đa mà hệ thống phục vụ được | ≥ 100 concurrent users. Tại 100 users, response time tăng ≤ 50% so với tải 1 user. Throughput ≥ 50 transactions/second. |
| **SUPL-P03** | Speed (Tốc độ) – Báo cáo | Thời gian render dashboard/báo cáo | Dashboard: ≤ 5 giây. Báo cáo tổng hợp phức tạp: ≤ 15 giây. Biểu đồ thống kê: ≤ 3 giây/biểu đồ. |
| **SUPL-P04** | Speed (Tốc độ) – Tìm kiếm | Thời gian trả kết quả tìm kiếm/lọc | ≤ 2 giây trên tập dữ liệu ≤ 10.000 bản ghi. ≤ 5 giây trên tập dữ liệu ≤ 50.000 bản ghi. |
| **SUPL-P05** | Speed (Tốc độ) – File I/O | Thời gian upload/download file | Upload: ≤ 5 giây cho file ≤ 5MB. Download: ≤ 3 giây cho file ≤ 5MB (trên mạng LAN). |
| **SUPL-P06** | Speed (Tốc độ) – Xuất dữ liệu | Thời gian xuất Excel | ≤ 10 giây cho ≤ 1.000 bản ghi. ≤ 30 giây cho ≤ 10.000 bản ghi. |

### 3.5. Security — Bảo mật

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-SE01** | Authentication (Xác thực) | Chính sách mật khẩu; Số level xác thực | Mật khẩu ≥ 8 ký tự, chứa chữ hoa + chữ thường + số. 1 level xác thực (username/password). Token-based session management (JWT hoặc session cookie). |
| **SUPL-SE02** | Authorization (Phân quyền) | Số trường hợp truy cập trái phép (unauthorized access) phát hiện qua penetration test | 0 trường hợp unauthorized access. 100% API endpoint có middleware kiểm tra quyền. 4 vai trò phân quyền rõ ràng (RBAC). |
| **SUPL-SE03** | Integrity (Tính toàn vẹn) – Chống brute-force | Số lần đăng nhập sai trước khi khóa; Thời gian khóa | Khóa tài khoản sau 5 lần sai liên tiếp. Thời gian khóa: 15 phút. Ghi log cảnh báo khi phát hiện brute-force. |
| **SUPL-SE04** | Confidentiality (Bảo mật truyền tải) | Phiên bản TLS; Tỷ lệ kết nối sử dụng HTTPS | TLS ≥ 1.2. 100% kết nối qua HTTPS. 0 kết nối HTTP không mã hóa được phép. |
| **SUPL-SE05** | Confidentiality (Bảo mật dữ liệu) | Số trường dữ liệu nhạy cảm không được bảo vệ | 0 trường nhạy cảm hiển thị cho vai trò không được phép. 100% truy cập dữ liệu nhạy cảm (CCCD, BHXH, ngân hàng) được ghi audit log. |
| **SUPL-SE06** | Integrity – Chống tấn công web | Số lỗ hổng tấn công web phát hiện qua kiểm thử bảo mật | 0 lỗ hổng CSRF. 0 lỗ hổng XSS. 100% chức năng POST/PUT/PATCH và các request thay đổi trạng thái tương đương vượt qua kiểm thử chống CSRF và 100% dữ liệu hiển thị từ input người dùng vượt qua kiểm thử XSS. |
| **SUPL-SE07** | Integrity – Chống tấn công database | Số lỗ hổng SQL Injection phát hiện qua kiểm thử | 0 lỗ hổng SQL Injection. 100% truy vấn truy cập dữ liệu tách dữ liệu đầu vào khỏi câu lệnh thực thi SQL. |
| **SUPL-SE08** | Authorization + Auditability (Phân quyền + Kiểm toán) | Số thay đổi cấu hình ẩn/hiện không hợp lệ; Tỷ lệ thay đổi cấu hình được ghi log đầy đủ | 0 thay đổi cấu hình ẩn/hiện do vai trò không được phép thực hiện. 100% thay đổi cấu hình ẩn/hiện khen thưởng/kỷ luật được ghi audit log với user ID, thời gian, giá trị trước/sau. |
| **SUPL-SE09** | Authorization + Auditability (Phân quyền + Kiểm toán) – Chấm dứt hợp đồng | Số trường hợp chấm dứt hợp đồng trước hạn trái phép; Tỷ lệ thao tác được ghi log đầy đủ | 0 trường hợp chấm dứt hợp đồng trước hạn trái phép. 100% thao tác chấm dứt hợp đồng trước hạn được ghi audit log với mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước/sau. |

### 3.6. Supportability — Khả năng hỗ trợ & Bảo trì

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-S01** | Maintainability – Modularity (Tính module) | Mức phụ thuộc liên module; Số thay đổi lan truyền khi sửa 1 module | Thay đổi 1 module không yêu cầu thay đổi ≥ 2 module khác. 100% giao diện tích hợp giữa các module được đặc tả và kiểm thử độc lập. |
| **SUPL-S02** | Maintainability – Understandability | Tỷ lệ API có tài liệu; Tỷ lệ trang có hướng dẫn sử dụng | ≥ 90% API endpoint có mô tả trong tài liệu. 100% chức năng chính có hướng dẫn sử dụng. |
| **SUPL-S03** | Flexibility (Tính linh hoạt) | Số danh mục cấu hình có thể mở rộng không cần sửa code | ≥ 3 loại danh mục (hệ số lương, loại phụ cấp, loại hợp đồng) mở rộng qua giao diện quản trị. 0 thay đổi mã nguồn cần thiết khi thêm danh mục mới. |
| **SUPL-S04** | Testability (Khả năng kiểm thử) – Logging | Số cấp độ log được hỗ trợ; Thông tin trong mỗi log entry | ≥ 4 cấp độ (ERROR, WARNING, INFO, DEBUG). Mỗi entry có: timestamp, request ID, user ID, stack trace (cho ERROR). |
| **SUPL-S05** | Scalability (Khả năng mở rộng) | Số nút ứng dụng có thể chạy song song; Tỷ lệ request liên tiếp hoạt động đúng qua nhiều nút | Hỗ trợ ≥ 2 nút ứng dụng chạy song song trong cùng môi trường. 100% request liên tiếp của cùng người dùng hoạt động đúng khi được phân phối qua các nút ứng dụng khác nhau. |

### 3.7. Constraints — Ràng buộc

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-DC01** | Portability – Kiến trúc | Tuân thủ mô hình Client-Server, RESTful API | 100% giao tiếp client-server qua RESTful API (JSON). Frontend là SPA (Single Page Application). |
| **SUPL-DC02** | Correctness – Mô hình dữ liệu | Kiểm tra cấu trúc cây đơn vị | 100% đơn vị tổ chức nằm trong cấu trúc cây cha-con hợp lệ. Gốc duy nhất: Trường ĐHTL. Không có cycle. |
| **SUPL-DC03** | Security – Thiết kế | Số vai trò được định nghĩa; Mô hình phân quyền | RBAC với 4 vai trò. 100% chức năng có ma trận phân quyền rõ ràng. |
| **SUPL-IC01** | Portability – Công nghệ | Stack công nghệ tuân thủ | React.js (TypeScript) + Laravel/PHP + MySQL/MariaDB. |
| **SUPL-IC02** | Compatibility – Trình duyệt | Số trình duyệt hỗ trợ; Tỷ lệ chức năng hoạt động đúng | ≥ 3 trình duyệt (Chrome, Firefox, Edge). 100% chức năng hoạt động trên Chrome mới nhất. ≥ 95% trên Firefox và Edge. |
| **SUPL-IC03** | Portability – Mã hóa | Encoding sử dụng | UTF-8 trên toàn bộ hệ thống. 0 lỗi hiển thị Tiếng Việt có dấu. |
| **SUPL-IC04** | Correctness – File | Định dạng và kích thước file hỗ trợ | PDF và Excel. Kích thước tối đa: 10MB/file. Thông báo lỗi nếu vượt quá. |
| **SUPL-LR01** | Legal – Bảo vệ dữ liệu | Tỷ lệ trường hợp xử lý dữ liệu có bản ghi đồng ý hợp lệ; Tỷ lệ yêu cầu ẩn dữ liệu được xử lý đúng | 100% trường hợp thuộc diện phải xin đồng ý có bản ghi đồng ý hợp lệ trước khi xử lý dữ liệu. 100% yêu cầu hợp lệ về ẩn dữ liệu cá nhân được thực hiện và lưu vết xử lý. |
| **SUPL-LR02** | Legal – Quy chế nhân sự | Tỷ lệ mục trong bộ danh mục phê duyệt được cấu hình và sử dụng được; Số mục trái danh mục phê duyệt | 100% loại hợp đồng, phụ cấp và chức danh trong bộ danh mục nhân sự phê duyệt được cấu hình và sử dụng được trên hệ thống. 0 mục trái bộ danh mục phê duyệt được đưa vào nghiệm thu. |
| **SUPL-LR03** | Legal – Lưu trữ | Thời gian lưu trữ tối thiểu | Hồ sơ nhân sự lưu ≥ 75 năm (theo Luật Lưu trữ). Hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật lưu ≥ 10 năm sau khi kết thúc hoặc sau bản ghi cuối cùng. |

---

## 4. Ma trận truy vết NFR → FEAT/UC

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F01 | FEAT 12.1, UC Auto Logging | System Timer |
| | SUPL-F02 | FEAT 7.3, UC 4.25 | TCCB |
| | SUPL-F03 | FEAT 1.3, UC 4.2 A1 | System Timer |
| | SUPL-F04 | FEAT 2.6, UC 4.8 A2 | System Timer |
| | SUPL-F05 | FEAT 5.1–5.4, FEAT 7.6; UC 4.22, UC 4.43–4.45 | System Timer, TCCB |
| | SUPL-F06 | FEAT 8.2, UC 4.34 | System Timer, TCCB |
| | SUPL-F07 | FEAT 9.4, 9.5 | TCCB |
| | SUPL-F08 | FEAT 1.1, UC 4.1 | Tất cả |
| **Usability** | SUPL-U01 → U07 | Toàn bộ FEAT/UC | Tất cả |
| **Reliability** | SUPL-R01 → R05 | Toàn bộ hệ thống | Phòng CNTT |
| **Performance** | SUPL-P01 | Toàn bộ FEAT/UC; FEAT 5.2, 5.3, 6.2; UC 4.43, 4.44, 4.46 | Tất cả |
| | SUPL-P02 | Toàn bộ hệ thống | Phòng CNTT |
| | SUPL-P03 | FEAT 10.1, UC 4.37 | TCCB, TCKT |
| | SUPL-P04 | FEAT 6.3, FEAT 7.1, FEAT 7.2; UC 4.23, UC 4.24, UC 4.47 | TCCB, TCKT |
| | SUPL-P05 | BangCap, ChungChi, HopDong files | TCCB |
| | SUPL-P06 | FEAT 7.8, UC 4.28 A2 | TCCB, TCKT |
| **Security** | SUPL-SE01 → SE09 | FEAT 1.1, 2.4, 5.4, 6.2, 6.3, 7.9, 12.1, 12.2; UC 4.45–4.48 | Admin, TCCB, TCKT, System |
| **Supportability** | SUPL-S01 → S05 | Toàn bộ hệ thống | Nhóm phát triển |
| **Constraints** | SUPL-DC01 → IC04, LR01 → LR03 | Toàn bộ hệ thống; FEAT 6.2, UC 4.46 | Tất cả stakeholders |

---

## 5. Phân tích Softgoals và Trade-offs

### 5.1. Các Softgoal chính của hệ thống HRMS

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

### 5.2. Phân tích Trade-offs

| Trade-off | Softgoal A | Softgoal B | Quyết định |
|-----------|------------|------------|------------|
| **Bảo mật vs Dễ sử dụng** | Mật khẩu phức tạp + tự động đăng xuất 30 phút | Người dùng phải đăng nhập lại thường xuyên | Ưu tiên bảo mật (M) – bù bằng cảnh báo 5 phút trước khi hết phiên |
| **Bảo mật vs Hiệu năng** | Kiểm tra quyền trên mọi API request | Tăng overhead cho mỗi request | Ưu tiên bảo mật (M) – tối ưu bằng caching quyền theo phiên |
| **Toàn vẹn dữ liệu vs Linh hoạt** | Quản lý danh mục cũ bằng thay đổi trạng thái để giữ nguyên lịch sử | Người dùng muốn tối giản dữ liệu hiển thị trên màn hình | Ưu tiên toàn vẹn (M) – hỗ trợ "Ngừng sử dụng" thay thế |
| **Audit Log đầy đủ vs Hiệu năng** | Ghi log 100% hành động | Tăng I/O database | Ưu tiên audit (M) – sử dụng async logging hoặc separate log table |
| **Responsive design vs Thời gian phát triển** | Hỗ trợ đa thiết bị | Tăng effort thiết kế/kiểm thử | Ưu tiên desktop (M) – tablet hỗ trợ cơ bản (E) |

### 5.3. Minh họa mô hình McCall áp dụng cho HRMS

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

## Phụ lục A: Bảng tổng hợp nhanh — Quality Factor × Metric × Acceptance Criteria

> Bảng tóm tắt dạng đặc tả bổ sung (Supplementary Specification Table) theo format bài tập nhóm.

| # | Quality Factor | Metric | Acceptance Criteria | Priority |
|---|---------------|--------|---------------------|----------|
| 1 | **Performance – Speed** | P95 Response time (xem/thêm/sửa/chuyển trạng thái) | ≤ 2s (≤50 users), ≤ 5s (≤100 users) | M |
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
| 25 | **Usability – Confirmation** | Critical actions with dialog | 100% khóa tài khoản/thôi việc/chấm dứt trước hạn/thay đổi trạng thái | M |
| 26 | **Supportability – Modularity** | Module coupling | Change in 1 module → ≤ 1 other module affected | M |
| 27 | **Supportability – Documentation** | API doc coverage | ≥ 90% endpoints documented | E |
| 28 | **Supportability – Flexibility** | Config categories extendable via UI | ≥ 3 categories, 0 code changes needed | M |
| 29 | **Supportability – Logging** | Log levels supported | ≥ 4 levels (ERROR/WARN/INFO/DEBUG) | E |
| 30 | **Supportability – Scalability** | Horizontal scaling support | ≥ 2 instances behind load balancer | N |
| 31 | **Correctness – Auto Logging** | Action log coverage | 100% hành động truy cập/thêm-sửa/thay đổi trạng thái được ghi log với 9 trường | M |
| 32 | **Correctness – Auto Processes** | Auto status transition accuracy | 100% correct, ≤ 24h delay | M |
| 33 | **Integrity – Status Transition Governance** | Catalog status-change rule compliance | 100% đúng quy tắc, 0 sai lệch dữ liệu lịch sử | M |
| 34 | **Legal – Data Privacy** | Compliance with ND 13/2023 | Full compliance | M |
| 35 | **Legal – Records Retention** | Retention period for HR/contract/evaluation history | Hồ sơ nhân sự ≥ 75 năm; hợp đồng và lịch sử đánh giá/khen thưởng/kỷ luật ≥ 10 năm | M |
| 36 | **Compatibility – Browser** | Supported browsers | Chrome + Firefox + Edge, 100% on Chrome | M |
| 37 | **Portability – Encoding** | UTF-8 compliance | 0 Vietnamese display errors | M |

---

> **Ghi chú cuối:** Tài liệu này bổ sung cho Đặc tả Ca sử dụng (UCS) và phải được đọc cùng với tài liệu RMP và các UC 4.1–4.48 để có cái nhìn toàn diện về yêu cầu hệ thống.
