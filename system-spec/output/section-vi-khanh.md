## 6.8. Yêu cầu về Bảo mật (Security)

> Người thực hiện: Ngô Đức Nam Khánh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-SE01 | Xác thực người dùng | Authentication (Xác thực) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 2 | SUPL-SE02 | Phân quyền truy cập | Authorization (Phân quyền truy cập) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 3 | SUPL-SE03 | Bảo vệ chống tấn công brute-force | Integrity (Toàn vẹn) - Chống tấn công tự động | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 4 | SUPL-SE04 | Mã hóa truyền tải dữ liệu (HTTPS) | Confidentiality (Bảo mật truyền tải) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 5 | SUPL-SE05 | Bảo vệ dữ liệu nhạy cảm | Confidentiality (Bảo mật dữ liệu) | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 6 | SUPL-SE06 | Ngăn chặn tấn công web trên chức năng nhập liệu và cập nhật dữ liệu | Integrity (Toàn vẹn) - Chống tấn công web | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 7 | SUPL-SE07 | Chống SQL Injection | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu | FEAT 1.1, FEAT 2.4, FEAT 6.1, FEAT 6.2, FEAT 7.4, FEAT 8.9, FEAT 10.2, FEAT 10.3 |
| 8 | SUPL-SE08 | Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) | FEAT 8.9 |
| 9 | SUPL-SE09 | Kiểm soát chấm dứt hợp đồng trước hạn | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) | FEAT 7.4 |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-SE01: Xác thực người dùng (Authentication)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authentication (Xác thực) |
| **Mô tả yêu cầu** | Mọi truy cập vào hệ thống phải qua xác thực bằng tài khoản/mật khẩu. Mật khẩu phải đáp ứng chính sách: tối thiểu 8 ký tự, bao gồm chữ hoa, chữ thường và số. |
| **Độ đo yêu cầu** | 1) **Mức độ mạnh mật khẩu**: số quy tắc mật khẩu được hệ thống kiểm tra bắt buộc.<br>2) **Số lớp xác thực**: số bước xác thực trước khi truy cập hệ thống.<br>3) **An toàn phiên đăng nhập**: trạng thái phiên có thuộc tính bảo vệ và thời gian hết hạn không hoạt động. |
| **Tiêu chuẩn đáp ứng** | 1) Mật khẩu có **ít nhất 8 ký tự** và thỏa **3/3 quy tắc**: chữ hoa, chữ thường, chữ số.<br>2) Hệ thống áp dụng **01 lớp xác thực** bằng tên đăng nhập/mật khẩu trước khi vào hệ thống.<br>3) Phiên đăng nhập phải được bảo vệ khỏi truy cập từ script phía client và tự hết hiệu lực sau tối đa **30 phút** không hoạt động. |
| **Phương pháp đo** | Kiểm thử chức năng đăng nhập/đổi mật khẩu; kiểm tra rule validation trên form; kiểm tra cấu hình cookie/token phiên (HttpOnly, Secure, thời gian hết hạn). |
| **Lý do chọn độ đo** | Ngưỡng **8 ký tự** phù hợp mức tối thiểu mà NIST SP 800-63B và OWASP Authentication Cheat Sheet thừa nhận cho xác thực bằng mật khẩu; dự án giữ thêm **3 nhóm ký tự** vì đây là chính sách đã chốt trong SUPL gốc nhằm tăng độ khó đoán cho tài khoản nội bộ HRMS chưa triển khai MFA. Chọn **01 lớp xác thực** vì hệ thống hiện là cổng nghiệp vụ nội bộ, chưa có yêu cầu MFA trong phạm vi đề tài. Mốc **30 phút không hoạt động** bám yêu cầu hệ thống về tự động đăng xuất, cân bằng giữa an toàn phiên và tính tiện dụng khi cán bộ thao tác hồ sơ nhân sự. |

#### SUPL-SE02: Phân quyền truy cập (Authorization)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization (Phân quyền truy cập) |
| **Mô tả yêu cầu** | Hệ thống phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Nhân sự) – mỗi vai trò chỉ truy cập được các chức năng được cấp quyền. Mọi request API phải kiểm tra quyền trước khi xử lý. |
| **Độ đo yêu cầu** | 1) **Số trường hợp truy cập trái phép** phát hiện qua kiểm thử phân quyền.<br>2) **Tỷ lệ API được bảo vệ** = số API endpoint có kiểm tra quyền / tổng số API endpoint.<br>3) **Số vai trò được định nghĩa** trong mô hình RBAC. |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường hợp truy cập trái phép vào chức năng hoặc API không được cấp quyền.<br>2) **100%** API endpoint có cơ chế kiểm tra quyền trước khi xử lý.<br>3) Hệ thống có đúng **4 vai trò**: Admin, TCCB, TCKT, Nhân sự. |
| **Phương pháp đo** | Kiểm thử xâm nhập theo ma trận quyền; rà soát middleware/guard trên route API; đối chiếu cấu hình vai trò và quyền trong hệ thống. |
| **Lý do chọn độ đo** | Với bài toán phân quyền, nguyên tắc **least privilege** của NIST SP 800-53 AC-6 và OWASP Broken Access Control yêu cầu không chấp nhận truy cập vượt quyền, nên ngưỡng đúng phải là **0 trường hợp trái phép** và **100% endpoint được kiểm tra quyền**. Con số **4 vai trò** không phải chọn tùy ý mà xuất phát trực tiếp từ mô hình nghiệp vụ đã xác định trong đặc tả: Admin, TCCB, TCKT, Nhân sự. |

#### SUPL-SE03: Bảo vệ chống tấn công brute-force
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công tự động |
| **Mô tả yêu cầu** | Khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp. Thời gian khóa tối thiểu 15 phút. |
| **Độ đo yêu cầu** | 1) **Ngưỡng khóa tài khoản**: số lần đăng nhập sai liên tiếp trước khi bị khóa.<br>2) **Thời gian khóa tạm thời**: số phút tài khoản bị khóa.<br>3) **Ghi log cảnh báo**: có/không bản ghi cảnh báo khi phát hiện hành vi brute-force. |
| **Tiêu chuẩn đáp ứng** | 1) Tài khoản bị khóa sau đúng **5 lần** đăng nhập sai liên tiếp.<br>2) Thời gian khóa tối thiểu **15 phút**.<br>3) Hệ thống phải ghi log cảnh báo, tối thiểu gồm **IP**, **thời gian** và **tài khoản bị tác động**. |
| **Phương pháp đo** | Thực hiện đăng nhập sai liên tiếp trên tài khoản thử nghiệm; đo thời gian khóa thực tế; kiểm tra bản ghi cảnh báo trong log bảo mật. |
| **Lý do chọn độ đo** | OWASP Authentication Cheat Sheet khuyến nghị **login throttling/account lockout** để chống brute-force. Ngưỡng **5 lần sai liên tiếp** là mức cấu hình rất phổ biến trong hệ thống doanh nghiệp vì đủ thấp để chặn thử mật khẩu tự động nhưng chưa gây khóa nhầm quá sớm cho người dùng thật. Mốc **15 phút** là thời gian làm chậm đáng kể tấn công online mà vẫn không buộc cán bộ phải nhờ quản trị viên mở khóa trong hầu hết trường hợp. Ba trường log **IP, thời gian, tài khoản** là tập tối thiểu để truy vết mẫu tấn công và đối chiếu sự cố. |

#### SUPL-SE04: Mã hóa truyền tải dữ liệu (HTTPS)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật truyền tải) |
| **Mô tả yêu cầu** | Toàn bộ giao tiếp giữa client và server phải sử dụng giao thức HTTPS (TLS 1.2 trở lên). |
| **Độ đo yêu cầu** | 1) **Phiên bản TLS** đang sử dụng.<br>2) **Tỷ lệ kết nối HTTPS** = số kết nối HTTPS / tổng số kết nối đến hệ thống.<br>3) **Chuyển hướng HTTP sang HTTPS**: có/không cơ chế tự động chuyển hướng. |
| **Tiêu chuẩn đáp ứng** | 1) Hệ thống chỉ chấp nhận kết nối với **TLS 1.2 trở lên**.<br>2) **100%** kết nối sử dụng HTTPS; **0%** kết nối HTTP không mã hóa được xử lý trực tiếp.<br>3) Mọi truy cập HTTP phải được tự động chuyển hướng sang HTTPS. |
| **Phương pháp đo** | Kiểm tra cấu hình TLS bằng trình duyệt/curl hoặc công cụ SSL; đo lưu lượng truy cập thực tế; kiểm thử request HTTP để xác nhận chuyển hướng. |
| **Lý do chọn độ đo** | NIST SP 800-52 Rev.2 yêu cầu tối thiểu phải hỗ trợ **TLS 1.2** và khuyến nghị tiến tới TLS 1.3; RFC **8996** của IETF đã chính thức loại bỏ TLS 1.0/1.1. Vì HRMS truyền thông tin tài khoản, CCCD, BHXH và dữ liệu hợp đồng, ngưỡng đúng phải là **100% HTTPS** và **0% HTTP thuần** để loại bỏ hoàn toàn kênh truyền không mã hóa. Yêu cầu chuyển hướng HTTP sang HTTPS giúp tránh lỗi cấu hình và giảm nguy cơ người dùng truy cập nhầm URL không an toàn. |

#### SUPL-SE05: Bảo vệ dữ liệu nhạy cảm
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật dữ liệu) |
| **Mô tả yêu cầu** | Dữ liệu nhạy cảm (số CCCD, số BHXH, thông tin ngân hàng) phải được bảo vệ – chỉ hiển thị cho vai trò được phép, ghi log khi truy cập. |
| **Độ đo yêu cầu** | 1) **Số trường dữ liệu nhạy cảm bị lộ** cho vai trò không được phép.<br>2) **Tỷ lệ ghi audit log khi truy cập dữ liệu nhạy cảm** = số lần truy cập được ghi log / tổng số lần truy cập dữ liệu nhạy cảm. |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được cấp quyền.<br>2) **100%** lượt truy cập các trường CCCD, BHXH và thông tin ngân hàng được ghi audit log. |
| **Phương pháp đo** | Kiểm thử API/UI theo từng vai trò; kiểm tra payload trả về; đối chiếu nhật ký truy cập dữ liệu nhạy cảm với lịch sử thao tác thực tế. |
| **Lý do chọn độ đo** | Nghị định **13/2023/NĐ-CP** yêu cầu dữ liệu cá nhân phải được xử lý đúng mục đích, trong phạm vi cần thiết và có biện pháp bảo vệ tương ứng; riêng HRMS của trường còn chứa dữ liệu định danh và tài chính như **CCCD, BHXH, tài khoản ngân hàng**. Do đây là nhóm dữ liệu có rủi ro pháp lý và riêng tư cao, ngưỡng chấp nhận phải là **0 lộ lọt cho vai trò không có quyền**. Chọn **100% ghi audit log** vì mọi lần truy cập dữ liệu nhạy cảm đều phải truy vết được khi kiểm tra nội bộ hoặc xử lý sự cố theo tinh thần trách nhiệm giải trình của Nghị định 13. |

#### SUPL-SE06: Ngăn chặn tấn công web trên chức năng nhập liệu và cập nhật dữ liệu
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công web |
| **Mô tả yêu cầu** | Hệ thống phải ngăn chặn các tấn công web làm giả yêu cầu hoặc chèn mã thực thi trên các chức năng nhập liệu và thao tác thay đổi dữ liệu. |
| **Độ đo yêu cầu** | 1) **Số lỗ hổng CSRF** phát hiện qua kiểm thử bảo mật.<br>2) **Số lỗ hổng XSS** phát hiện qua kiểm thử bảo mật.<br>3) **Tỷ lệ request thay đổi dữ liệu được bảo vệ** = số request POST/PUT/DELETE có cơ chế chống giả mạo / tổng số request POST/PUT/DELETE. |
| **Tiêu chuẩn đáp ứng** | 1) **0** lỗ hổng CSRF.<br>2) **0** lỗ hổng XSS.<br>3) **100%** chức năng POST/PUT/DELETE và các form thay đổi dữ liệu vượt qua kiểm thử chống CSRF; **100%** dữ liệu do người dùng nhập khi hiển thị lại trên giao diện vượt qua kiểm thử XSS. |
| **Phương pháp đo** | Kiểm thử bảo mật bằng OWASP ZAP hoặc công cụ tương đương; rà soát cơ chế CSRF token; kiểm tra escaping/sanitizing dữ liệu đầu vào và đầu ra. |
| **Lý do chọn độ đo** | OWASP Top 10:2021 xem các lỗi chèn mã và kiểm soát truy cập đầu vào/đầu ra là nhóm rủi ro trọng yếu; OWASP **CSRF Prevention Cheat Sheet** và **XSS Prevention Cheat Sheet** đều coi chỉ cần **một** điểm không bảo vệ là có thể khai thác được. Vì vậy các độ đo bảo mật này có dạng **sharp requirement**: **0 lỗ hổng** và **100% request thay đổi trạng thái được bảo vệ**. Với hệ thống HRMS có nhiều form thêm/sửa hồ sơ, mọi endpoint POST/PUT/DELETE đều phải có CSRF token và mọi dữ liệu phản chiếu lên UI đều phải được encode/sanitize. |

#### SUPL-SE07: Chống SQL Injection
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu |
| **Mô tả yêu cầu** | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu. |
| **Độ đo yêu cầu** | 1) **Số lỗ hổng SQL Injection** phát hiện qua kiểm thử.<br>2) **Tỷ lệ truy vấn được bảo vệ** = số truy vấn sử dụng dữ liệu đầu vào có cơ chế tách dữ liệu khỏi câu lệnh SQL / tổng số truy vấn sử dụng dữ liệu đầu vào. |
| **Tiêu chuẩn đáp ứng** | 1) **0** lỗ hổng SQL Injection.<br>2) **100%** truy vấn có dữ liệu đầu vào từ người dùng được bảo vệ bằng cơ chế truy vấn tham số hóa hoặc ORM tương đương. |
| **Phương pháp đo** | Kiểm thử bằng sqlmap hoặc công cụ tương đương; rà soát code các truy vấn SQL/ORM; kiểm tra không có truy vấn ghép chuỗi trực tiếp từ dữ liệu đầu vào. |
| **Lý do chọn độ đo** | OWASP Top 10:2021 **A03 - Injection**, CWE-**89** và OWASP **SQL Injection Prevention Cheat Sheet** đều chỉ ra biện pháp chính là **prepared statements/parameterized queries**. Vì chỉ một truy vấn ghép chuỗi cũng đủ mở đường cho khai thác, nên tiêu chuẩn phù hợp phải là **0 lỗ hổng SQLi** và **100% truy vấn có input người dùng được tham số hóa**. Đây là ngưỡng có thể kiểm chứng rõ ràng bằng code review và penetration test. |

#### SUPL-SE08: Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Mô tả yêu cầu** | Chỉ các vai trò được ủy quyền mới được phép cấu hình ẩn/hiện các mục khen thưởng/kỷ luật ở mức toàn hệ thống; mọi thay đổi cấu hình phải được ghi audit log với người thực hiện, thời gian, giá trị trước/sau. Tham chiếu FEAT 8.9. |
| **Độ đo yêu cầu** | 1) **Số thay đổi cấu hình trái phép** đối với chức năng ẩn/hiện mục khen thưởng/kỷ luật.<br>2) **Tỷ lệ thay đổi cấu hình được ghi audit log** = số thay đổi được lưu log / tổng số thay đổi cấu hình hợp lệ.<br>3) **Độ đầy đủ bản ghi audit** = số trường bắt buộc được ghi nhận / 4 trường bắt buộc (người thực hiện, thời gian, giá trị trước, giá trị sau). |
| **Tiêu chuẩn đáp ứng** | 1) **0** thay đổi cấu hình do người dùng không được ủy quyền thực hiện thành công.<br>2) **100%** thay đổi cấu hình hợp lệ được ghi audit log.<br>3) Mỗi bản ghi audit phải đạt **4/4 trường bắt buộc**: người thực hiện, thời gian, giá trị trước, giá trị sau. |
| **Phương pháp đo** | Kiểm thử phân quyền trên giao diện và API cấu hình; thực hiện thay đổi cấu hình thử nghiệm; đối chiếu lịch sử thay đổi với audit log của hệ thống. |
| **Lý do chọn độ đo** | Chức năng ẩn/hiện mục khen thưởng/kỷ luật tác động trực tiếp tới việc ai được nhìn thấy thông tin đánh giá nhân sự, nên đây là một cấu hình bảo mật cấp hệ thống. Vì vậy ngưỡng **0 thay đổi trái phép** là bắt buộc, không thể đặt mức dung sai. Chọn **100% audit log** vì mọi thay đổi cấu hình phải truy ngược được khi rà soát trách nhiệm. Bộ **4 trường** được chọn không tùy ý mà suy ra trực tiếp từ yêu cầu gốc: người thực hiện, thời gian, giá trị trước, giá trị sau là mức tối thiểu để chứng minh ai đổi gì và đổi khi nào. |

#### SUPL-SE09: Kiểm soát chấm dứt hợp đồng trước hạn
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Mô tả yêu cầu** | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; hệ thống phải ghi audit log đầy đủ cho thao tác này gồm mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian và giá trị trước/sau. Tham chiếu FEAT 7.4. |
| **Độ đo yêu cầu** | 1) **Số trường hợp chấm dứt hợp đồng trước hạn trái phép** phát hiện qua kiểm thử quyền truy cập.<br>2) **Tỷ lệ thao tác chấm dứt hợp đồng được ghi audit log** = số thao tác được lưu log / tổng số thao tác chấm dứt hợp đồng trước hạn hợp lệ.<br>3) **Độ đầy đủ bản ghi audit** = số trường bắt buộc được ghi nhận / 7 trường bắt buộc (mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau). |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường hợp chấm dứt hợp đồng trước hạn được thực hiện bởi người dùng không có quyền.<br>2) **100%** thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log.<br>3) Mỗi bản ghi audit phải đạt **7/7 trường bắt buộc**. |
| **Phương pháp đo** | Kiểm thử chức năng chấm dứt hợp đồng với nhiều vai trò; rà soát log nghiệp vụ và audit log; đối chiếu dữ liệu trước/sau khi thao tác được thực hiện. |
| **Lý do chọn độ đo** | Theo **Bộ luật Lao động 2019** (nhóm điều về chấm dứt hợp đồng lao động và nghĩa vụ khi chấm dứt), thao tác chấm dứt hợp đồng trước hạn có hậu quả pháp lý trực tiếp đối với người lao động và nhà trường. Vì vậy ngưỡng đúng phải là **0 thao tác trái phép** và **100% được lưu vết**. Bộ **7 trường** được chọn bám sát hồ sơ cần có để kiểm tra tính hợp lệ của quyết định: mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau. Nếu thiếu một trường, việc đối chiếu pháp lý và kiểm toán nội bộ sẽ không đầy đủ. |

## 6.9. Ràng buộc triển khai (Implementation Constraints)

> Người thực hiện: Ngô Đức Nam Khánh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-IC01 | Ngôn ngữ và framework | Portability (Khả năng chuyển đổi công nghệ) - Công nghệ triển khai | Toàn hệ thống |
| 2 | SUPL-IC02 | Trình duyệt hỗ trợ | Compatibility (Tính tương thích) - Trình duyệt | Toàn hệ thống |
| 3 | SUPL-IC03 | Chuẩn mã hóa ký tự | Portability (Khả năng chuyển đổi) - Mã hóa dữ liệu | Toàn hệ thống |
| 4 | SUPL-IC04 | Định dạng file đính kèm | Correctness (Tính đúng đắn) - File đính kèm | Toàn hệ thống |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-IC01: Ngôn ngữ và framework
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi công nghệ) - Công nghệ triển khai |
| **Mô tả yêu cầu** | Frontend: React.js (TypeScript). Backend: Laravel/PHP. Database: MySQL/MariaDB. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ tuân thủ stack frontend** = số module giao diện build bằng React.js + TypeScript / tổng số module frontend.<br>2) **Tỷ lệ tuân thủ stack backend** = số service/backend module triển khai bằng Laravel/PHP / tổng số service backend.<br>3) **Mức tuân thủ cơ sở dữ liệu** = số môi trường triển khai chính thức sử dụng MySQL/MariaDB / tổng số môi trường triển khai chính thức. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** module frontend sử dụng React.js kết hợp TypeScript.<br>2) **100%** thành phần backend sử dụng Laravel/PHP.<br>3) **100%** môi trường triển khai chính thức sử dụng MySQL hoặc MariaDB; **0** thành phần production dùng hệ quản trị cơ sở dữ liệu ngoài phạm vi yêu cầu. |
| **Phương pháp đo** | Rà soát package.json, tsconfig, composer.json, cấu trúc source code, file cấu hình triển khai và cấu hình kết nối cơ sở dữ liệu của hệ thống. |
| **Lý do chọn độ đo** | Đây là **ràng buộc triển khai**, nên bản chất là điều kiện nhị phân: hoặc tuân thủ, hoặc không tuân thủ. Vì vậy ngưỡng hợp lý phải là **100% đúng stack** và **0 thành phần production ngoài stack đã phê duyệt**. Bộ công nghệ React + TypeScript, Laravel/PHP, MySQL/MariaDB được giữ nguyên theo đặc tả nguồn vì phù hợp năng lực nhóm, tài nguyên triển khai của bài toán web nội bộ trường đại học, đồng thời giúp đồng nhất tài liệu, bảo trì và chấm nghiệm thu. |

#### SUPL-IC02: Trình duyệt hỗ trợ
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Compatibility (Tính tương thích) - Trình duyệt |
| **Mô tả yêu cầu** | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox, Edge. |
| **Độ đo yêu cầu** | 1) **Độ phủ trình duyệt mục tiêu** = số trình duyệt/phiên bản mục tiêu được kiểm thử / tổng số trình duyệt/phiên bản mục tiêu.<br>2) **Tỷ lệ chức năng chính đạt** = số chức năng nghiệp vụ chính chạy đúng trên từng trình duyệt / tổng số chức năng chính cần kiểm thử.<br>3) **Số lỗi nghiêm trọng theo trình duyệt** phát hiện trong kiểm thử tương thích. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** phạm vi kiểm thử phải bao gồm Chrome bản mới nhất và **2 phiên bản gần nhất**, Firefox bản ổn định hiện hành và Edge bản ổn định hiện hành tại thời điểm nghiệm thu.<br>2) **100%** chức năng chính hoạt động đúng trên Chrome; **≥ 95%** chức năng chính hoạt động đúng trên Firefox và Edge.<br>3) **0** lỗi mức Nghiêm trọng/Critical trên các trình duyệt mục tiêu. |
| **Phương pháp đo** | Thực hiện kiểm thử tương thích chéo trình duyệt bằng test thủ công/kịch bản tự động trên môi trường nghiệm thu; ghi nhận lỗi theo từng trình duyệt và từng phiên bản. |
| **Lý do chọn độ đo** | Chính sách **“bản mới nhất + 2 phiên bản gần nhất”** là cách hỗ trợ phổ biến với các trình duyệt evergreen vì cân bằng được độ phủ người dùng và chi phí kiểm thử. Chrome được đặt ngưỡng **100%** vì theo xu hướng sử dụng desktop tại Việt Nam (nguồn tham khảo: StatCounter Global Stats), đây là trình duyệt ưu tiên cao nhất trong môi trường hành chính - giáo dục. Firefox và Edge được đặt **≥95%** để vẫn bảo đảm tương thích thực tế nhưng tránh chi phí tối ưu hóa quá mức cho các khác biệt nhỏ không ảnh hưởng nghiệp vụ. Riêng lỗi **Critical = 0** vì chỉ cần một lỗi nghiêm trọng trên trình duyệt mục tiêu cũng có thể làm gián đoạn nghiệp vụ nhân sự. |

#### SUPL-IC03: Chuẩn mã hóa ký tự
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi) - Mã hóa dữ liệu |
| **Mô tả yêu cầu** | Toàn bộ hệ thống sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ Tiếng Việt có dấu. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ thành phần dùng UTF-8** = số thành phần kiểm tra đạt UTF-8 / tổng số thành phần cần kiểm tra (giao diện, API response, cơ sở dữ liệu, file import/export).<br>2) **Số lỗi hiển thị tiếng Việt có dấu** phát hiện khi nhập, lưu, tìm kiếm và hiển thị dữ liệu tiếng Việt. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** thành phần của hệ thống dùng UTF-8.<br>2) **0** lỗi hiển thị sai tiếng Việt có dấu trên giao diện, dữ liệu lưu trữ, dữ liệu xuất và dữ liệu tải lại từ hệ thống. |
| **Phương pháp đo** | Kiểm tra cấu hình charset/collation của cơ sở dữ liệu, header phản hồi HTTP, cấu hình file nguồn; kiểm thử với bộ dữ liệu mẫu có đầy đủ ký tự tiếng Việt có dấu. |
| **Lý do chọn độ đo** | W3C khuyến nghị nhà phát triển **luôn chọn UTF-8** cho nội dung và dữ liệu web; với hệ thống HRMS tiếng Việt, đây gần như là lựa chọn bắt buộc để bảo toàn dấu tiếng Việt trong tên người, địa chỉ, đơn vị, quyết định, hợp đồng. Vì mã hóa là thuộc tính nền tảng của toàn hệ thống, mức chấp nhận phù hợp là **100% thành phần dùng UTF-8** và **0 lỗi hiển thị**; chỉ một điểm lệch charset cũng có thể gây lỗi dây chuyền khi nhập, tìm kiếm, lưu và xuất dữ liệu. |

#### SUPL-IC04: Định dạng file đính kèm
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn) - File đính kèm |
| **Mô tả yêu cầu** | Hệ thống hỗ trợ upload/download file PDF (bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động) và Excel (import/export nhân sự). Kích thước file tối đa: 10MB. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ file đúng định dạng được xử lý thành công** = số file PDF/Excel hợp lệ được upload, download, import hoặc export thành công / tổng số file hợp lệ được thử nghiệm.<br>2) **Ngưỡng kích thước file tối đa** hệ thống cho phép xử lý.<br>3) **Tỷ lệ từ chối file không hợp lệ** = số file sai định dạng hoặc vượt dung lượng bị từ chối / tổng số file sai định dạng hoặc vượt dung lượng được thử nghiệm. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** file PDF hợp lệ dùng cho bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động được upload/download thành công; **100%** file Excel hợp lệ dùng cho import/export nhân sự được xử lý thành công.<br>2) Kích thước tối đa được chấp nhận là **10MB/file**.<br>3) **100%** file sai định dạng hoặc lớn hơn **10MB** bị từ chối và hệ thống hiển thị thông báo lỗi rõ ràng. |
| **Phương pháp đo** | Kiểm thử upload/download/import/export với tập file mẫu hợp lệ và không hợp lệ; kiểm tra MIME type, phần mở rộng file và phản hồi lỗi của hệ thống. |
| **Lý do chọn độ đo** | **PDF** và **Excel** được chọn vì bám đúng nhu cầu nghiệp vụ đã mô tả trong use case: hồ sơ quét/đính kèm cần dạng tài liệu cố định (PDF), còn nhập/xuất danh sách nhân sự cần dạng bảng tính (Excel). Mốc **10MB/file** là ngưỡng thực dụng cho môi trường trường đại học: đủ chứa bản scan hợp đồng, bằng cấp, chứng chỉ ở chất lượng đọc rõ, nhưng vẫn kiểm soát được dung lượng lưu trữ, băng thông và thời gian tải tệp. Các tỷ lệ **100% file hợp lệ xử lý thành công** và **100% file không hợp lệ bị từ chối** được chọn vì đây là ràng buộc đúng/sai rõ ràng của chức năng kiểm tra định dạng, không phải mục tiêu tối ưu mềm. |
