## 6.8. Yêu cầu về Bảo mật (Security)

> Người thực hiện: Ngô Quang Tùng

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

#### SUPL-SE02: Phân quyền truy cập (Authorization)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization (Phân quyền truy cập) |
| **Mô tả yêu cầu** | Hệ thống phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Nhân sự) – mỗi vai trò chỉ truy cập được các chức năng được cấp quyền. Mọi request API phải kiểm tra quyền trước khi xử lý. |
| **Độ đo yêu cầu** | 1) **Số trường hợp truy cập trái phép** phát hiện qua kiểm thử phân quyền.<br>2) **Tỷ lệ API được bảo vệ** = số API endpoint có kiểm tra quyền / tổng số API endpoint.<br>3) **Số vai trò được định nghĩa** trong mô hình RBAC. |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường hợp truy cập trái phép vào chức năng hoặc API không được cấp quyền.<br>2) **100%** API endpoint có cơ chế kiểm tra quyền trước khi xử lý.<br>3) Hệ thống có đúng **4 vai trò**: Admin, TCCB, TCKT, Nhân sự. |
| **Phương pháp đo** | Kiểm thử xâm nhập theo ma trận quyền; rà soát middleware/guard trên route API; đối chiếu cấu hình vai trò và quyền trong hệ thống. |

#### SUPL-SE03: Bảo vệ chống tấn công brute-force
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công tự động |
| **Mô tả yêu cầu** | Khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp. Thời gian khóa tối thiểu 15 phút. |
| **Độ đo yêu cầu** | 1) **Ngưỡng khóa tài khoản**: số lần đăng nhập sai liên tiếp trước khi bị khóa.<br>2) **Thời gian khóa tạm thời**: số phút tài khoản bị khóa.<br>3) **Ghi log cảnh báo**: có/không bản ghi cảnh báo khi phát hiện hành vi brute-force. |
| **Tiêu chuẩn đáp ứng** | 1) Tài khoản bị khóa sau đúng **5 lần** đăng nhập sai liên tiếp.<br>2) Thời gian khóa tối thiểu **15 phút**.<br>3) Hệ thống phải ghi log cảnh báo, tối thiểu gồm **IP**, **thời gian** và **tài khoản bị tác động**. |
| **Phương pháp đo** | Thực hiện đăng nhập sai liên tiếp trên tài khoản thử nghiệm; đo thời gian khóa thực tế; kiểm tra bản ghi cảnh báo trong log bảo mật. |

#### SUPL-SE04: Mã hóa truyền tải dữ liệu (HTTPS)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật truyền tải) |
| **Mô tả yêu cầu** | Toàn bộ giao tiếp giữa client và server phải sử dụng giao thức HTTPS (TLS 1.2 trở lên). |
| **Độ đo yêu cầu** | 1) **Phiên bản TLS** đang sử dụng.<br>2) **Tỷ lệ kết nối HTTPS** = số kết nối HTTPS / tổng số kết nối đến hệ thống.<br>3) **Chuyển hướng HTTP sang HTTPS**: có/không cơ chế tự động chuyển hướng. |
| **Tiêu chuẩn đáp ứng** | 1) Hệ thống chỉ chấp nhận kết nối với **TLS 1.2 trở lên**.<br>2) **100%** kết nối sử dụng HTTPS; **0%** kết nối HTTP không mã hóa được xử lý trực tiếp.<br>3) Mọi truy cập HTTP phải được tự động chuyển hướng sang HTTPS. |
| **Phương pháp đo** | Kiểm tra cấu hình TLS bằng trình duyệt/curl hoặc công cụ SSL; đo lưu lượng truy cập thực tế; kiểm thử request HTTP để xác nhận chuyển hướng. |

#### SUPL-SE05: Bảo vệ dữ liệu nhạy cảm
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật dữ liệu) |
| **Mô tả yêu cầu** | Dữ liệu nhạy cảm (số CCCD, số BHXH, thông tin ngân hàng) phải được bảo vệ – chỉ hiển thị cho vai trò được phép, ghi log khi truy cập. |
| **Độ đo yêu cầu** | 1) **Số trường dữ liệu nhạy cảm bị lộ** cho vai trò không được phép.<br>2) **Tỷ lệ ghi audit log khi truy cập dữ liệu nhạy cảm** = số lần truy cập được ghi log / tổng số lần truy cập dữ liệu nhạy cảm. |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được cấp quyền.<br>2) **100%** lượt truy cập các trường CCCD, BHXH và thông tin ngân hàng được ghi audit log. |
| **Phương pháp đo** | Kiểm thử API/UI theo từng vai trò; kiểm tra payload trả về; đối chiếu nhật ký truy cập dữ liệu nhạy cảm với lịch sử thao tác thực tế. |

#### SUPL-SE06: Ngăn chặn tấn công web trên chức năng nhập liệu và cập nhật dữ liệu
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công web |
| **Mô tả yêu cầu** | Hệ thống phải ngăn chặn các tấn công web làm giả yêu cầu hoặc chèn mã thực thi trên các chức năng nhập liệu và thao tác thay đổi dữ liệu. |
| **Độ đo yêu cầu** | 1) **Số lỗ hổng CSRF** phát hiện qua kiểm thử bảo mật.<br>2) **Số lỗ hổng XSS** phát hiện qua kiểm thử bảo mật.<br>3) **Tỷ lệ request thay đổi dữ liệu được bảo vệ** = số request POST/PUT/DELETE có cơ chế chống giả mạo / tổng số request POST/PUT/DELETE. |
| **Tiêu chuẩn đáp ứng** | 1) **0** lỗ hổng CSRF.<br>2) **0** lỗ hổng XSS.<br>3) **100%** chức năng POST/PUT/DELETE và các form thay đổi dữ liệu vượt qua kiểm thử chống CSRF; **100%** dữ liệu do người dùng nhập khi hiển thị lại trên giao diện vượt qua kiểm thử XSS. |
| **Phương pháp đo** | Kiểm thử bảo mật bằng OWASP ZAP hoặc công cụ tương đương; rà soát cơ chế CSRF token; kiểm tra escaping/sanitizing dữ liệu đầu vào và đầu ra. |

#### SUPL-SE07: Chống SQL Injection
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu |
| **Mô tả yêu cầu** | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu. |
| **Độ đo yêu cầu** | 1) **Số lỗ hổng SQL Injection** phát hiện qua kiểm thử.<br>2) **Tỷ lệ truy vấn được bảo vệ** = số truy vấn sử dụng dữ liệu đầu vào có cơ chế tách dữ liệu khỏi câu lệnh SQL / tổng số truy vấn sử dụng dữ liệu đầu vào. |
| **Tiêu chuẩn đáp ứng** | 1) **0** lỗ hổng SQL Injection.<br>2) **100%** truy vấn có dữ liệu đầu vào từ người dùng được bảo vệ bằng cơ chế truy vấn tham số hóa hoặc ORM tương đương. |
| **Phương pháp đo** | Kiểm thử bằng sqlmap hoặc công cụ tương đương; rà soát code các truy vấn SQL/ORM; kiểm tra không có truy vấn ghép chuỗi trực tiếp từ dữ liệu đầu vào. |

#### SUPL-SE08: Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Mô tả yêu cầu** | Chỉ các vai trò được ủy quyền mới được phép cấu hình ẩn/hiện các mục khen thưởng/kỷ luật ở mức toàn hệ thống; mọi thay đổi cấu hình phải được ghi audit log với người thực hiện, thời gian, giá trị trước/sau. Tham chiếu FEAT 8.9. |
| **Độ đo yêu cầu** | 1) **Số thay đổi cấu hình trái phép** đối với chức năng ẩn/hiện mục khen thưởng/kỷ luật.<br>2) **Tỷ lệ thay đổi cấu hình được ghi audit log** = số thay đổi được lưu log / tổng số thay đổi cấu hình hợp lệ.<br>3) **Độ đầy đủ bản ghi audit** = số trường bắt buộc được ghi nhận / 4 trường bắt buộc (người thực hiện, thời gian, giá trị trước, giá trị sau). |
| **Tiêu chuẩn đáp ứng** | 1) **0** thay đổi cấu hình do người dùng không được ủy quyền thực hiện thành công.<br>2) **100%** thay đổi cấu hình hợp lệ được ghi audit log.<br>3) Mỗi bản ghi audit phải đạt **4/4 trường bắt buộc**: người thực hiện, thời gian, giá trị trước, giá trị sau. |
| **Phương pháp đo** | Kiểm thử phân quyền trên giao diện và API cấu hình; thực hiện thay đổi cấu hình thử nghiệm; đối chiếu lịch sử thay đổi với audit log của hệ thống. |

#### SUPL-SE09: Kiểm soát chấm dứt hợp đồng trước hạn
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Mô tả yêu cầu** | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; hệ thống phải ghi audit log đầy đủ cho thao tác này gồm mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian và giá trị trước/sau. Tham chiếu FEAT 7.4. |
| **Độ đo yêu cầu** | 1) **Số trường hợp chấm dứt hợp đồng trước hạn trái phép** phát hiện qua kiểm thử quyền truy cập.<br>2) **Tỷ lệ thao tác chấm dứt hợp đồng được ghi audit log** = số thao tác được lưu log / tổng số thao tác chấm dứt hợp đồng trước hạn hợp lệ.<br>3) **Độ đầy đủ bản ghi audit** = số trường bắt buộc được ghi nhận / 7 trường bắt buộc (mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau). |
| **Tiêu chuẩn đáp ứng** | 1) **0** trường hợp chấm dứt hợp đồng trước hạn được thực hiện bởi người dùng không có quyền.<br>2) **100%** thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log.<br>3) Mỗi bản ghi audit phải đạt **7/7 trường bắt buộc**. |
| **Phương pháp đo** | Kiểm thử chức năng chấm dứt hợp đồng với nhiều vai trò; rà soát log nghiệp vụ và audit log; đối chiếu dữ liệu trước/sau khi thao tác được thực hiện. |

## 6.9. Ràng buộc triển khai (Implementation Constraints)

> Người thực hiện: Ngô Quang Tùng

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

#### SUPL-IC02: Trình duyệt hỗ trợ
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Compatibility (Tính tương thích) - Trình duyệt |
| **Mô tả yêu cầu** | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox, Edge. |
| **Độ đo yêu cầu** | 1) **Độ phủ trình duyệt mục tiêu** = số trình duyệt/phiên bản mục tiêu được kiểm thử / tổng số trình duyệt/phiên bản mục tiêu.<br>2) **Tỷ lệ chức năng chính đạt** = số chức năng nghiệp vụ chính chạy đúng trên từng trình duyệt / tổng số chức năng chính cần kiểm thử.<br>3) **Số lỗi nghiêm trọng theo trình duyệt** phát hiện trong kiểm thử tương thích. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** phạm vi kiểm thử phải bao gồm Chrome bản mới nhất và **2 phiên bản gần nhất**, Firefox bản ổn định hiện hành và Edge bản ổn định hiện hành tại thời điểm nghiệm thu.<br>2) **100%** chức năng chính hoạt động đúng trên Chrome; **≥ 95%** chức năng chính hoạt động đúng trên Firefox và Edge.<br>3) **0** lỗi mức Nghiêm trọng/Critical trên các trình duyệt mục tiêu. |
| **Phương pháp đo** | Thực hiện kiểm thử tương thích chéo trình duyệt bằng test thủ công/kịch bản tự động trên môi trường nghiệm thu; ghi nhận lỗi theo từng trình duyệt và từng phiên bản. |

#### SUPL-IC03: Chuẩn mã hóa ký tự
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi) - Mã hóa dữ liệu |
| **Mô tả yêu cầu** | Toàn bộ hệ thống sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ Tiếng Việt có dấu. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ thành phần dùng UTF-8** = số thành phần kiểm tra đạt UTF-8 / tổng số thành phần cần kiểm tra (giao diện, API response, cơ sở dữ liệu, file import/export).<br>2) **Số lỗi hiển thị tiếng Việt có dấu** phát hiện khi nhập, lưu, tìm kiếm và hiển thị dữ liệu tiếng Việt. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** thành phần của hệ thống dùng UTF-8.<br>2) **0** lỗi hiển thị sai tiếng Việt có dấu trên giao diện, dữ liệu lưu trữ, dữ liệu xuất và dữ liệu tải lại từ hệ thống. |
| **Phương pháp đo** | Kiểm tra cấu hình charset/collation của cơ sở dữ liệu, header phản hồi HTTP, cấu hình file nguồn; kiểm thử với bộ dữ liệu mẫu có đầy đủ ký tự tiếng Việt có dấu. |

#### SUPL-IC04: Định dạng file đính kèm
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn) - File đính kèm |
| **Mô tả yêu cầu** | Hệ thống hỗ trợ upload/download file PDF (bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động) và Excel (import/export nhân sự). Kích thước file tối đa: 10MB. |
| **Độ đo yêu cầu** | 1) **Tỷ lệ file đúng định dạng được xử lý thành công** = số file PDF/Excel hợp lệ được upload, download, import hoặc export thành công / tổng số file hợp lệ được thử nghiệm.<br>2) **Ngưỡng kích thước file tối đa** hệ thống cho phép xử lý.<br>3) **Tỷ lệ từ chối file không hợp lệ** = số file sai định dạng hoặc vượt dung lượng bị từ chối / tổng số file sai định dạng hoặc vượt dung lượng được thử nghiệm. |
| **Tiêu chuẩn đáp ứng** | 1) **100%** file PDF hợp lệ dùng cho bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động được upload/download thành công; **100%** file Excel hợp lệ dùng cho import/export nhân sự được xử lý thành công.<br>2) Kích thước tối đa được chấp nhận là **10MB/file**.<br>3) **100%** file sai định dạng hoặc lớn hơn **10MB** bị từ chối và hệ thống hiển thị thông báo lỗi rõ ràng. |
| **Phương pháp đo** | Kiểm thử upload/download/import/export với tập file mẫu hợp lệ và không hợp lệ; kiểm tra MIME type, phần mở rộng file và phản hồi lỗi của hệ thống. |
