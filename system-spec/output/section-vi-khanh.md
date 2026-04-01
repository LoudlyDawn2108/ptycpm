# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng của Ngô Đức Nam Khánh

> Cột **FEAT liên quan** dùng để ghi các FEAT hoặc phạm vi chức năng mà mỗi SUPL truy vết tới.

## 6.8. Yêu cầu về bảo mật (Security)

> Người thực hiện: Ngô Đức Nam Khánh

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
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
|---|---|
| **Yếu tố chất lượng** | Authentication (Xác thực) |
| **Độ đo yêu cầu** | (1) Số quy tắc mật khẩu bắt buộc được kiểm tra; (2) Số lớp xác thực trước khi truy cập hệ thống; (3) Trạng thái bảo vệ phiên và thời gian hết hạn không hoạt động. |
| **Tiêu chuẩn đáp ứng** | (1) Mật khẩu có ít nhất 8 ký tự và thỏa 3/3 quy tắc: chữ hoa, chữ thường, chữ số; (2) Áp dụng 01 lớp xác thực bằng tên đăng nhập/mật khẩu; (3) Phiên đăng nhập được bảo vệ và tự hết hiệu lực sau tối đa 30 phút không hoạt động. |

#### SUPL-SE02

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization (Phân quyền truy cập) |
| **Độ đo yêu cầu** | (1) Số trường hợp truy cập trái phép qua kiểm thử phân quyền; (2) Tỷ lệ API endpoint có kiểm tra quyền; (3) Số vai trò được định nghĩa trong mô hình RBAC. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp truy cập trái phép vào chức năng hoặc API không được cấp quyền; (2) 100% API endpoint có cơ chế kiểm tra quyền trước khi xử lý; (3) Hệ thống có đúng 4 vai trò: Admin, TCCB, TCKT, Người dùng. |

#### SUPL-SE03

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công tự động |
| **Độ đo yêu cầu** | (1) Ngưỡng số lần đăng nhập sai liên tiếp trước khi khóa tài khoản; (2) Thời gian khóa tạm thời; (3) Trạng thái ghi log cảnh báo brute-force. |
| **Tiêu chuẩn đáp ứng** | (1) Tài khoản bị khóa sau đúng 5 lần đăng nhập sai liên tiếp; (2) Thời gian khóa tối thiểu 15 phút; (3) Có bản ghi cảnh báo gồm tối thiểu IP, thời gian và tài khoản bị tác động. |

#### SUPL-SE04

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật truyền tải) |
| **Độ đo yêu cầu** | (1) Phiên bản TLS đang sử dụng; (2) Tỷ lệ kết nối HTTPS trên tổng kết nối; (3) Trạng thái tự động chuyển hướng HTTP sang HTTPS. |
| **Tiêu chuẩn đáp ứng** | (1) Chỉ chấp nhận TLS 1.2 trở lên; (2) 100% kết nối sử dụng HTTPS, 0% kết nối HTTP không mã hóa được xử lý trực tiếp; (3) Mọi truy cập HTTP được tự động chuyển hướng sang HTTPS. |

#### SUPL-SE05

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật dữ liệu) |
| **Độ đo yêu cầu** | (1) Số trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được phép; (2) Tỷ lệ lượt truy cập dữ liệu nhạy cảm được ghi audit log. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được cấp quyền; (2) 100% lượt truy cập các trường CCCD, BHXH và thông tin ngân hàng được ghi audit log. |

#### SUPL-SE06

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công web |
| **Độ đo yêu cầu** | (1) Số lỗ hổng CSRF phát hiện qua kiểm thử; (2) Số lỗ hổng XSS phát hiện qua kiểm thử; (3) Tỷ lệ request POST/PUT/DELETE có cơ chế chống giả mạo. |
| **Tiêu chuẩn đáp ứng** | (1) 0 lỗ hổng CSRF; (2) 0 lỗ hổng XSS; (3) 100% request POST/PUT/DELETE và form thay đổi dữ liệu vượt qua kiểm thử chống CSRF, 100% dữ liệu người dùng hiển thị lại trên giao diện vượt qua kiểm thử XSS. |

#### SUPL-SE07

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu |
| **Độ đo yêu cầu** | (1) Số lỗ hổng SQL Injection phát hiện qua kiểm thử; (2) Tỷ lệ truy vấn có dữ liệu đầu vào được bảo vệ bằng cơ chế tách dữ liệu khỏi câu lệnh SQL. |
| **Tiêu chuẩn đáp ứng** | (1) 0 lỗ hổng SQL Injection; (2) 100% truy vấn có dữ liệu đầu vào từ người dùng được bảo vệ bằng truy vấn tham số hóa hoặc ORM tương đương. |

#### SUPL-SE08

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Độ đo yêu cầu** | (1) Số thay đổi cấu hình ẩn/hiện mục khen thưởng/kỷ luật trái phép; (2) Tỷ lệ thay đổi cấu hình hợp lệ được ghi audit log; (3) Độ đầy đủ bản ghi audit theo 4 trường bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 0 thay đổi cấu hình do người dùng không được ủy quyền thực hiện thành công; (2) 100% thay đổi cấu hình hợp lệ được ghi audit log; (3) Mỗi bản ghi audit đạt 4/4 trường bắt buộc: người thực hiện, thời gian, giá trị trước, giá trị sau. |

#### SUPL-SE09

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Độ đo yêu cầu** | (1) Số trường hợp chấm dứt hợp đồng trước hạn trái phép; (2) Tỷ lệ thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log; (3) Độ đầy đủ bản ghi audit theo 7 trường bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp chấm dứt hợp đồng trước hạn được thực hiện bởi người dùng không có quyền; (2) 100% thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log; (3) Mỗi bản ghi audit đạt 7/7 trường bắt buộc: mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau. |

## 6.9. Ràng buộc triển khai (Implementation Constraints)

> Người thực hiện: Ngô Đức Nam Khánh

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-IC01 | Hệ thống phải sử dụng stack công nghệ: frontend React.js (TypeScript), backend Laravel/PHP và cơ sở dữ liệu MySQL/MariaDB trong các môi trường triển khai chính thức. | Toàn hệ thống |
| 2 | SUPL-IC02 | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox và Edge. | Toàn hệ thống |
| 3 | SUPL-IC03 | Toàn bộ hệ thống phải sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ tiếng Việt có dấu trên giao diện, API, cơ sở dữ liệu và dữ liệu trao đổi. | Toàn hệ thống |
| 4 | SUPL-IC04 | Hệ thống chỉ hỗ trợ file PDF cho hồ sơ đính kèm và file Excel cho import/export nhân sự, với kích thước tối đa 10MB mỗi file. | Toàn hệ thống |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-IC01

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi công nghệ) - Công nghệ triển khai |
| **Độ đo yêu cầu** | (1) Tỷ lệ module frontend dùng React.js + TypeScript; (2) Tỷ lệ thành phần backend dùng Laravel/PHP; (3) Tỷ lệ môi trường chính thức dùng MySQL/MariaDB. |
| **Tiêu chuẩn đáp ứng** | (1) 100% module frontend sử dụng React.js kết hợp TypeScript; (2) 100% thành phần backend sử dụng Laravel/PHP; (3) 100% môi trường triển khai chính thức sử dụng MySQL hoặc MariaDB, 0 thành phần production dùng hệ quản trị cơ sở dữ liệu ngoài phạm vi yêu cầu. |

#### SUPL-IC02

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Compatibility (Tính tương thích) - Trình duyệt |
| **Độ đo yêu cầu** | (1) Độ phủ kiểm thử trên tập trình duyệt/phiên bản mục tiêu; (2) Tỷ lệ chức năng nghiệp vụ chính chạy đúng theo từng trình duyệt; (3) Số lỗi mức nghiêm trọng theo trình duyệt. |
| **Tiêu chuẩn đáp ứng** | (1) 100% phạm vi kiểm thử bao gồm Chrome bản mới nhất và 2 phiên bản gần nhất, Firefox bản ổn định hiện hành, Edge bản ổn định hiện hành tại thời điểm nghiệm thu; (2) 100% chức năng chính hoạt động đúng trên Chrome, ≥95% trên Firefox và Edge; (3) 0 lỗi mức Nghiêm trọng/Critical trên các trình duyệt mục tiêu. |

#### SUPL-IC03

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi) - Mã hóa dữ liệu |
| **Độ đo yêu cầu** | (1) Tỷ lệ thành phần hệ thống dùng UTF-8; (2) Số lỗi hiển thị tiếng Việt có dấu khi nhập, lưu, tìm kiếm và hiển thị dữ liệu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% thành phần của hệ thống dùng UTF-8; (2) 0 lỗi hiển thị sai tiếng Việt có dấu trên giao diện, dữ liệu lưu trữ, dữ liệu xuất và dữ liệu tải lại từ hệ thống. |

#### SUPL-IC04

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn) - File đính kèm |
| **Độ đo yêu cầu** | (1) Tỷ lệ file PDF/Excel hợp lệ được xử lý thành công; (2) Ngưỡng kích thước file tối đa hệ thống cho phép; (3) Tỷ lệ file sai định dạng hoặc vượt dung lượng bị từ chối. |
| **Tiêu chuẩn đáp ứng** | (1) 100% file PDF hợp lệ dùng cho bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động được upload/download thành công và 100% file Excel hợp lệ dùng cho import/export nhân sự được xử lý thành công; (2) Kích thước tối đa được chấp nhận là 10MB/file; (3) 100% file sai định dạng hoặc lớn hơn 10MB bị từ chối và hệ thống hiển thị thông báo lỗi rõ ràng. |
