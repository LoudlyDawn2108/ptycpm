# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng của Nguyễn Hồng Phúc

## 6.1. Yêu cầu về chức năng (Functionality)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-F01 | Ghi nhật ký hệ thống tự động (Auto Logging) | Correctness – Auditability | FEAT 6.1; Toàn bộ hệ thống |
| 2 | SUPL-F02 | Tự động sinh mã nhân sự | Correctness | FEAT 8.3 |
| 3 | SUPL-F03 | Tự động đăng xuất phiên không hoạt động | Correctness – Tự động hóa | FEAT 1.3; Toàn bộ hệ thống |
| 4 | SUPL-F04 | Tự động khóa tài khoản nhân sự thôi việc | Correctness – Tự động hóa | FEAT 2.6; FEAT 8.5; FEAT 8.6 |
| 5 | SUPL-F05 | Tự động chuyển trạng thái hợp đồng | Correctness – Tự động hóa | FEAT 7.1; FEAT 7.2; FEAT 7.3; FEAT 7.4; FEAT 8.6 |
| 6 | SUPL-F06 | Tự động cập nhật trạng thái tham gia đào tạo | Correctness – Tự động hóa | FEAT 11.2 |
| 7 | SUPL-F07 | Quy tắc nghiệp vụ chung về xóa/thay đổi trạng thái | Integrity | FEAT 4.3; FEAT 4.4; FEAT 4.5 |
| 8 | SUPL-F08 | Bảo vệ mật khẩu lưu trữ | Security – Confidentiality | FEAT 1.1; Toàn bộ hệ thống xác thực |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-F01: Ghi nhật ký hệ thống tự động (Auto Logging)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness – Auditability (Tính đúng đắn và khả năng kiểm toán) |
| **Mô tả yêu cầu** | Hệ thống tự động ghi lại mọi hành động truy cập, thêm/sửa/xóa dữ liệu và thay đổi cấu hình với đầy đủ các thông tin: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. |
| **Độ đo yêu cầu** | (1) Tỷ lệ hành động truy cập/CRUD/thay đổi cấu hình được ghi log; (2) Mức đầy đủ trường dữ liệu trên mỗi bản ghi log (9/9 trường bắt buộc). |
| **Tiêu chuẩn đáp ứng** | (1) 100% hành động thuộc phạm vi yêu cầu phải có bản ghi log; (2) 100% bản ghi log có đủ 9/9 trường bắt buộc. |
| **Phương pháp đo** | Thực hiện kiểm thử trên các luồng đăng nhập, truy cập, thêm/sửa/xóa và thay đổi cấu hình; đối chiếu số hành động phát sinh với bảng audit log và kiểm tra cấu trúc từng bản ghi. |

#### SUPL-F02: Tự động sinh mã nhân sự
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn) |
| **Mô tả yêu cầu** | Khi tạo mới hồ sơ nhân sự, hệ thống tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. |
| **Độ đo yêu cầu** | (1) Tỷ lệ mã nhân sự sinh tự động bị trùng lặp; (2) Tỷ lệ mã sinh ra tuân thủ đúng mẫu mã đang cấu hình; (3) Tỷ lệ hồ sơ mới được cấp mã ngay tại thời điểm tạo. |
| **Tiêu chuẩn đáp ứng** | (1) 0% mã nhân sự bị trùng lặp; (2) 100% mã sinh ra đúng mẫu mã đang áp dụng; (3) 100% hồ sơ nhân sự mới được cấp mã ngay khi tạo thành công. |
| **Phương pháp đo** | Tạo thử nhiều hồ sơ nhân sự mới với các cấu hình mẫu mã khác nhau, kiểm tra tính duy nhất của mã trong cơ sở dữ liệu và đối chiếu chuỗi mã với mẫu cấu hình hiện hành. |

#### SUPL-F03: Tự động đăng xuất phiên không hoạt động
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Hệ thống tự động đăng xuất phiên làm việc nếu người dùng không thao tác trong 30 phút. Tham chiếu FEAT 1.3. |
| **Độ đo yêu cầu** | Thời gian từ thao tác cuối cùng của người dùng đến khi hệ thống tự động đăng xuất phiên. |
| **Tiêu chuẩn đáp ứng** | Hệ thống tự động đăng xuất chính xác sau 30 phút không hoạt động, sai số cho phép không quá ±30 giây. |
| **Phương pháp đo** | Tạo phiên đăng nhập thử nghiệm, ghi nhận thời điểm thao tác cuối cùng, để phiên ở trạng thái không tương tác và đo thời điểm hệ thống hủy phiên/chuyển về màn hình đăng nhập. |

#### SUPL-F04: Tự động khóa tài khoản nhân sự thôi việc
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Khi nhân sự được đánh dấu thôi việc, hệ thống tự động chuyển tài khoản của nhân sự đó sang trạng thái khóa. Cơ chế này gắn với FEAT 2.6 và phát sinh từ các nghiệp vụ thôi việc tương ứng FEAT 8.5, FEAT 8.6. |
| **Độ đo yêu cầu** | (1) Thời gian từ lúc hồ sơ nhân sự chuyển sang trạng thái thôi việc đến khi tài khoản liên kết bị khóa; (2) Tỷ lệ tài khoản liên kết được khóa tự động đúng quy tắc. |
| **Tiêu chuẩn đáp ứng** | (1) Tài khoản bị khóa trong không quá 1 phút kể từ khi nhân sự được đánh dấu thôi việc; (2) 100% tài khoản liên kết với nhân sự thôi việc được tự động chuyển sang trạng thái khóa. |
| **Phương pháp đo** | Thực hiện thao tác đánh dấu thôi việc trên hồ sơ nhân sự có tài khoản liên kết, đo độ trễ cập nhật trạng thái tài khoản và kiểm tra kết quả trong bảng tài khoản/audit log. |

#### SUPL-F05: Tự động chuyển trạng thái hợp đồng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Hệ thống tự động chuyển trạng thái hợp đồng từ “Còn hiệu lực” sang “Chờ gia hạn” khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. |
| **Độ đo yêu cầu** | (1) Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái “Chờ gia hạn”; (2) Độ trễ chuyển trạng thái kể từ thời điểm hợp đồng chạm ngưỡng cấu hình. |
| **Tiêu chuẩn đáp ứng** | (1) 100% hợp đồng đủ điều kiện được chuyển đúng trạng thái; (2) Việc chuyển trạng thái hoàn tất trong không quá 24 giờ kể từ thời điểm đủ điều kiện. |
| **Phương pháp đo** | Cấu hình ngưỡng chờ gia hạn, tạo dữ liệu hợp đồng mẫu với các mốc thời gian khác nhau, chạy cơ chế nền/scheduler và đối chiếu thời điểm đủ điều kiện với thời điểm trạng thái được cập nhật. |

#### SUPL-F06: Tự động cập nhật trạng thái tham gia đào tạo
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness – Tự động hóa |
| **Mô tả yêu cầu** | Khi khóa đào tạo chuyển từ trạng thái “Đang mở đăng ký” sang trạng thái “Đang đào tạo”, hệ thống tự động cập nhật tất cả đăng ký tương ứng từ trạng thái “Đã đăng ký” sang “Đang học”. |
| **Độ đo yêu cầu** | (1) Tỷ lệ bản ghi đăng ký của khóa đào tạo được cập nhật đúng trạng thái; (2) Độ trễ cập nhật kể từ thời điểm khóa đào tạo đổi trạng thái. |
| **Tiêu chuẩn đáp ứng** | (1) 100% bản ghi đăng ký thuộc khóa đào tạo đó được chuyển từ “Đã đăng ký” sang “Đang học”; (2) Hoàn tất cập nhật trong không quá 1 phút kể từ khi khóa đào tạo chuyển sang “Đang đào tạo”. |
| **Phương pháp đo** | Tạo khóa đào tạo mẫu với nhiều đăng ký ở trạng thái “Đã đăng ký”, chuyển trạng thái khóa đào tạo và đối chiếu trạng thái của toàn bộ bản ghi đăng ký sau khi hệ thống xử lý. |

#### SUPL-F07: Quy tắc nghiệp vụ chung về xóa/thay đổi trạng thái
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Tính toàn vẹn dữ liệu) |
| **Mô tả yêu cầu** | Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ “Thay đổi trạng thái” (không hỗ trợ “Xóa”) để bảo đảm tính toàn vẹn dữ liệu và phục vụ kiểm toán. Hệ số lương cho phép xóa khi chưa được hồ sơ nào sử dụng. |
| **Độ đo yêu cầu** | (1) Số trường hợp danh mục đã được sử dụng nhưng vẫn bị xóa; (2) Tỷ lệ danh mục loại phụ cấp/loại hợp đồng đã sử dụng chỉ cho phép đổi trạng thái; (3) Tỷ lệ hệ số lương chưa được sử dụng có thể xóa hợp lệ. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp danh mục đã sử dụng bị xóa; (2) 100% loại phụ cấp và loại hợp đồng đã sử dụng chỉ hỗ trợ thay đổi trạng thái; (3) 100% hệ số lương chưa được hồ sơ nào sử dụng có thể xóa thành công. |
| **Phương pháp đo** | Chuẩn bị các bản ghi danh mục ở cả hai trạng thái đã dùng/chưa dùng, thực hiện kiểm thử âm và dương đối với thao tác xóa/thay đổi trạng thái, sau đó đối chiếu dữ liệu lưu vết trong cơ sở dữ liệu. |

#### SUPL-F08: Bảo vệ mật khẩu lưu trữ
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Security – Confidentiality (Bảo mật dữ liệu lưu trữ) |
| **Mô tả yêu cầu** | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. |
| **Độ đo yêu cầu** | (1) Mức tuân thủ cơ chế băm một chiều thích ứng đối với mật khẩu; (2) Tham số độ khó của cơ chế băm; (3) Số mật khẩu tồn tại ở dạng văn bản thuần trong dữ liệu lưu trữ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% mật khẩu được lưu dưới dạng băm một chiều thích ứng; (2) Tham số độ khó tối thiểu tương đương bcrypt cost 10; (3) 0 mật khẩu lưu ở dạng plaintext. |
| **Phương pháp đo** | Kiểm tra cấu hình bảo mật và mã nguồn xử lý đăng nhập/đổi mật khẩu, đối chiếu định dạng dữ liệu trong cột mật khẩu của cơ sở dữ liệu và thực hiện audit mẫu trên dữ liệu lưu trữ. |

## 6.2. Ràng buộc thiết kế (Design Constraints)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-DC01 | Kiến trúc Client-Server | Portability – Kiến trúc | Toàn bộ hệ thống |
| 2 | SUPL-DC02 | Cơ cấu tổ chức dạng cây | Correctness – Mô hình dữ liệu | FEAT 3.1 |
| 3 | SUPL-DC03 | Tách biệt quyền theo vai trò | Security – Thiết kế phân quyền | Toàn bộ hệ thống |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-DC01: Kiến trúc Client-Server
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability – Kiến trúc |
| **Mô tả yêu cầu** | Hệ thống phải xây dựng theo mô hình Client-Server, frontend dạng SPA (Single Page Application) giao tiếp với backend qua RESTful API. |
| **Độ đo yêu cầu** | (1) Tỷ lệ request nghiệp vụ giữa client và server sử dụng RESTful API/JSON; (2) Số luồng nghiệp vụ phía client truy cập dữ liệu mà không đi qua backend API. |
| **Tiêu chuẩn đáp ứng** | (1) 100% request nghiệp vụ client-server sử dụng RESTful API với dữ liệu trao đổi chuẩn JSON; (2) 0 luồng nghiệp vụ truy cập dữ liệu trực tiếp mà không qua backend API; frontend được triển khai dưới một SPA thống nhất. |
| **Phương pháp đo** | Rà soát kiến trúc hệ thống, tài liệu API và lưu đồ triển khai; dùng browser devtools/network trace trên các luồng chính để xác nhận frontend giao tiếp với backend qua REST API. |

#### SUPL-DC02: Cơ cấu tổ chức dạng cây
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness – Mô hình dữ liệu |
| **Mô tả yêu cầu** | Cơ cấu tổ chức đơn vị phải được mô hình hóa dưới dạng cấu trúc cây cha-con với gốc là Trường Đại học Thủy Lợi. Tham chiếu FEAT 3.1. |
| **Độ đo yêu cầu** | (1) Số nút gốc trong cây tổ chức; (2) Số chu trình (cycle) phát hiện trong quan hệ cha-con; (3) Tỷ lệ đơn vị có liên kết cha-con hợp lệ trong mô hình dữ liệu. |
| **Tiêu chuẩn đáp ứng** | (1) Có đúng 1 nút gốc là “Trường Đại học Thủy Lợi”; (2) 0 chu trình trong cấu trúc cây; (3) 100% đơn vị tổ chức nằm trong quan hệ cha-con hợp lệ. |
| **Phương pháp đo** | Kiểm tra mô hình dữ liệu và thực hiện truy vấn/thuật toán duyệt cây để xác minh số nút gốc, phát hiện cycle và kiểm tra tính hợp lệ của toàn bộ quan hệ đơn vị. |

#### SUPL-DC03: Tách biệt quyền theo vai trò
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Security – Thiết kế phân quyền |
| **Mô tả yêu cầu** | Thiết kế hệ thống phải bảo đảm phân tách quyền rõ ràng theo 4 vai trò đã xác định, sử dụng cơ chế Role-Based Access Control (RBAC). |
| **Độ đo yêu cầu** | (1) Số vai trò được định nghĩa trong mô hình phân quyền; (2) Tỷ lệ chức năng/API có ma trận phân quyền rõ ràng; (3) Số trường hợp vai trò không được phép vẫn truy cập được chức năng khi kiểm thử phân quyền. |
| **Tiêu chuẩn đáp ứng** | (1) Định nghĩa đúng 4 vai trò: Admin, TCCB, TCKT, Nhân sự; (2) 100% chức năng và API có ma trận RBAC rõ ràng; (3) 0 trường hợp truy cập trái quyền trong kiểm thử phân quyền. |
| **Phương pháp đo** | Đối chiếu tài liệu phân quyền với danh sách chức năng/API của hệ thống, kiểm tra cấu hình role-permission và thực hiện kiểm thử truy cập chéo giữa các vai trò. |

## 6.3. Ràng buộc pháp lý (Legal/Regulatory)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-LR01 | Tuân thủ quy định bảo vệ dữ liệu cá nhân | Legal – Bảo vệ dữ liệu | Toàn bộ hệ thống |
| 2 | SUPL-LR02 | Tuân thủ quy chế quản lý nhân sự | Legal – Quy chế nhân sự | Toàn bộ hệ thống |
| 3 | SUPL-LR03 | Lưu trữ hồ sơ theo quy định | Legal – Lưu trữ | Toàn bộ hệ thống |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-LR01: Tuân thủ quy định bảo vệ dữ liệu cá nhân
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Legal – Bảo vệ dữ liệu |
| **Mô tả yêu cầu** | Hệ thống phải hỗ trợ quản lý sự đồng ý thu thập dữ liệu cá nhân và xử lý yêu cầu hợp lệ về ẩn hoặc xóa dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP. |
| **Độ đo yêu cầu** | (1) Tỷ lệ trường hợp xử lý dữ liệu cá nhân thuộc diện phải xin đồng ý có bản ghi đồng ý hợp lệ trước khi xử lý; (2) Tỷ lệ yêu cầu hợp lệ về ẩn/xóa dữ liệu cá nhân được xử lý và lưu vết đầy đủ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% trường hợp thuộc diện phải xin đồng ý có bản ghi đồng ý hợp lệ trước khi xử lý dữ liệu; (2) 100% yêu cầu hợp lệ về ẩn hoặc xóa dữ liệu cá nhân được thực hiện và có lưu vết xử lý. |
| **Phương pháp đo** | Kiểm tra hồ sơ đồng ý của chủ thể dữ liệu, đối chiếu nhật ký xử lý yêu cầu ẩn/xóa với các yêu cầu hợp lệ và rà soát mẫu dữ liệu cá nhân trước/sau xử lý. |

#### SUPL-LR02: Tuân thủ quy chế quản lý nhân sự
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Legal – Quy chế nhân sự |
| **Mô tả yêu cầu** | Hệ thống phải cho phép cấu hình và sử dụng bộ danh mục loại hợp đồng, phụ cấp và chức danh theo danh mục nhân sự do Trường Đại học Thủy Lợi phê duyệt trên cơ sở quy định hiện hành của Bộ GD&ĐT và Bộ NN&PTNT. |
| **Độ đo yêu cầu** | (1) Tỷ lệ mục trong bộ danh mục nhân sự đã được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số mục trái danh mục phê duyệt xuất hiện trong phạm vi nghiệm thu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% loại hợp đồng, phụ cấp và chức danh trong bộ danh mục phê duyệt được cấu hình và sử dụng được trên hệ thống; (2) 0 mục trái bộ danh mục phê duyệt được đưa vào nghiệm thu. |
| **Phương pháp đo** | Đối chiếu danh mục được phê duyệt của nhà trường với danh mục cấu hình trên hệ thống, thực hiện kiểm thử chọn/sử dụng các giá trị này trong các nghiệp vụ nhân sự liên quan. |

#### SUPL-LR03: Lưu trữ hồ sơ theo quy định
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Legal – Lưu trữ |
| **Mô tả yêu cầu** | Hồ sơ nhân sự, hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu theo thời gian quy định của pháp luật lao động Việt Nam và quy chế lưu trữ hiện hành. |
| **Độ đo yêu cầu** | (1) Thời gian lưu trữ tối thiểu đối với từng nhóm hồ sơ; (2) Tỷ lệ hồ sơ mẫu còn truy xuất được trong toàn bộ thời hạn lưu trữ bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) Hồ sơ nhân sự được lưu tối thiểu 75 năm; hợp đồng lao động và lịch sử đánh giá khen thưởng/kỷ luật được lưu tối thiểu 10 năm sau khi kết thúc hoặc sau bản ghi cuối cùng; (2) 100% hồ sơ mẫu trong thời hạn lưu trữ bắt buộc còn truy xuất được. |
| **Phương pháp đo** | Kiểm tra chính sách lưu trữ, cấu hình lưu trữ/archiving và thử truy xuất hồ sơ mẫu của từng nhóm tài liệu để xác nhận hệ thống không xóa hoặc làm mất dữ liệu trước hạn. |
