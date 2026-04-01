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