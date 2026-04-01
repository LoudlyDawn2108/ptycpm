# Nguyễn Hồng Phúc — Nội dung đóng góp

## Part A: STRQs and FEATs (for Section II)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 1.1:** Hệ thống cho phép người dùng đăng nhập bằng tài khoản. * **FEAT 1.2:** Hệ thống cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng. * **FEAT 1.3:** Hệ thống tự động đăng xuất khỏi phiên làm việc nếu người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web trong 30 phút. * **FEAT 1.4:** Hệ thống cho phép người dùng đổi mật khẩu tài khoản đang sử dụng. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 2.1:** Hệ thống cho phép quản trị viên tìm kiếm tài khoản người dùng. * **FEAT 2.2:** Hệ thống cho phép quản trị viên thêm mới tài khoản người dùng. * **FEAT 2.3:** Hệ thống cho phép quản trị viên sửa tài khoản người dùng. * **FEAT 2.4:** Hệ thống cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống theo các vai trò chức năng được định nghĩa sẵn: Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự (Cán bộ/Giảng viên/Nhân viên). * **FEAT 2.5:** Hệ thống cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Đang hoạt động/Bị khóa). * **FEAT 2.6:** Hệ thống tự động khóa tài khoản của nhân sự đã được đánh dấu thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | * Phân tách * Làm cho đầy đủ | * **FEAT 3.2:** Hệ thống cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự. * **FEAT 3.3:** Hệ thống cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự. * **FEAT 3.4:** Hệ thống cho phép quản trị viên và phòng TCCB giải thể đơn vị tổ chức nhân sự; khi giải thể, hệ thống chuyển hợp đồng đang hiệu lực sang trạng thái Hết hiệu lực, trạng thái hợp đồng nhân sự sang Chưa hợp đồng, trạng thái làm việc sang Đang chờ xét và xóa liên kết đơn vị công tác khỏi hồ sơ nhân sự. * **FEAT 3.5:** Hệ thống cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. * **FEAT 3.6:** Hệ thống cho phép quản trị viên và phòng TCCB sáp nhập đơn vị tổ chức nhân sự vào đơn vị nhận sáp nhập; hệ thống chuyển nhân sự và đơn vị con sang đơn vị nhận sáp nhập với trạng thái hợp đồng và trạng thái làm việc giữ nguyên. |
| **STRQ 13:** Hệ thống phải tuân thủ các quy định về bảo vệ dữ liệu cá nhân theo Nghị định 13/2023/NĐ-CP, bao gồm quản lý sự đồng ý thu thập dữ liệu và xử lý yêu cầu ẩn danh hóa dữ liệu khi có yêu cầu hợp lệ. | * Làm cho đầy đủ * Phân tách | * **FEAT 13.1:** Hệ thống cho phép ghi nhận, xem lịch sử và thu hồi sự đồng ý thu thập dữ liệu cá nhân cho từng cán bộ, theo Nghị định 13/2023/NĐ-CP. * **FEAT 13.2:** Hệ thống phải xử lý yêu cầu ẩn danh hóa dữ liệu cá nhân (thay thế thông tin định danh bằng dữ liệu ẩn danh) khi có yêu cầu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên, theo Nghị định 13/2023/NĐ-CP. |
| **STRQ 14:** Hệ thống cần được triển khai dưới dạng ứng dụng web để toàn bộ cán bộ, nhân viên có thể truy cập từ trình duyệt trên máy tính văn phòng mà không cần cài đặt phần mềm riêng. | * Thêm chi tiết | * **FEAT 1.5:** Hệ thống được cung cấp dưới dạng ứng dụng web nhiều người dùng; frontend dạng SPA giao tiếp với backend thông qua RESTful API của hệ thống. |
| **STRQ 15:** Cơ cấu tổ chức của trường cần được thể hiện theo cấu trúc phân cấp từ cấp trường xuống các đơn vị trực thuộc, phản ánh đúng mối quan hệ quản lý giữa các đơn vị. | * Thêm chi tiết | * **FEAT 3.1:** Hệ thống cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi. |
| **STRQ 16:** Mật khẩu người dùng phải được bảo vệ an toàn khi lưu trữ, không cho phép khôi phục nguyên văn nhằm ngăn ngừa rò rỉ dữ liệu xác thực khi cơ sở dữ liệu bị xâm nhập. | * Thêm chi tiết | * **FEAT 16.1:** Hệ thống phải lưu trữ mọi mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu ở dạng văn bản thuần. |

## Part B: UC Model Entries (for Section III)

- UC 4.1: Đăng nhập
- UC 4.2: Đăng xuất
- UC 4.3: Đổi mật khẩu
- UC 4.4: Tìm kiếm tài khoản người dùng
- UC 4.5: Thêm mới tài khoản người dùng
- UC 4.6: Sửa thông tin tài khoản người dùng
- UC 4.7: Thay đổi trạng thái cho tài khoản người dùng
- UC 4.8: Tạo mới đơn vị tổ chức nhân sự
- UC 4.9: Sửa thông tin đơn vị tổ chức nhân sự
- UC 4.10: Giải thể đơn vị tổ chức nhân sự
- UC 4.11: Xem chi tiết thông tin đơn vị tổ chức nhân sự
- UC 4.12: Sáp nhập đơn vị tổ chức nhân sự

## Part C: FEAT→UC Traceability (for Section III)

| FEAT | UC tương ứng |
|------|-------------|
| FEAT 1.1 | UC 4.1 (Đăng nhập) |
| FEAT 1.2 | UC 4.2 (Đăng xuất) |
| FEAT 1.3 | Ràng buộc hệ thống — hiện thực hóa bởi SUPL-F03 (không tách UC riêng) |
| FEAT 1.4 | UC 4.3 (Đổi mật khẩu) |
| FEAT 1.5 | Ràng buộc thiết kế — hiện thực hóa bởi SUPL-DC01 (không tách UC riêng) |
| FEAT 2.1 | UC 4.4 (Tìm kiếm tài khoản người dùng) |
| FEAT 2.2 | UC 4.5 (Thêm mới tài khoản người dùng) |
| FEAT 2.3 | UC 4.6 (Sửa thông tin tài khoản người dùng) |
| FEAT 2.4 | Ràng buộc thiết kế — hiện thực hóa bởi SUPL-DC03 (không tách UC riêng); gán vai trò tích hợp trong UC 4.5 và UC 4.6 |
| FEAT 2.5 | UC 4.7 (Thay đổi trạng thái cho tài khoản người dùng) |
| FEAT 2.6 | Ràng buộc hệ thống — hiện thực hóa bởi SUPL-F04 (không tách UC riêng) |
| FEAT 3.1 | Ràng buộc thiết kế — hiện thực hóa bởi SUPL-DC02 (không tách UC riêng) |
| FEAT 3.2 | UC 4.8 (Tạo mới đơn vị tổ chức nhân sự) |
| FEAT 3.3 | UC 4.9 (Sửa thông tin đơn vị tổ chức nhân sự) |
| FEAT 3.4 | UC 4.10 (Giải thể đơn vị tổ chức nhân sự) |
| FEAT 3.5 | UC 4.11 (Xem chi tiết thông tin đơn vị tổ chức nhân sự) |
| FEAT 3.6 | UC 4.12 (Sáp nhập đơn vị tổ chức nhân sự) |
| FEAT 13.1 | Ràng buộc pháp lý — được hiện thực hóa bởi SUPL-LR01 (không tách UC riêng) |
| FEAT 13.2 | Ràng buộc pháp lý — được hiện thực hóa bởi SUPL-LR04 (không tách UC riêng) |
| FEAT 16.1 | Ràng buộc bảo mật — hiện thực hóa bởi SUPL-F08 (không tách UC riêng); áp dụng tại UC 4.3 và UC 4.5 |

## Part D: UC Specifications (for Section IV)

### 4.1. Use Case: Đăng nhập

|  |  |
| --- | --- |
| **Tên use case** | **Đăng nhập** |
| Tác nhân chính | Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng xác thực và truy cập vào hệ thống dựa trên thông tin tài khoản được cấp. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng truy cập địa chỉ web của hệ thống. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã được cấp tài khoản. |
| Điều kiện thành công (Post-condition) | Người dùng được chuyển đến trang chủ tương ứng với vai trò. |
| Điều kiện thất bại | Người dùng không đăng nhập được và vẫn ở màn hình Đăng nhập. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng truy cập địa chỉ web của hệ thống. 2. Hệ thống hiển thị màn hình Đăng nhập. 3. Người dùng nhập Tên đăng nhập (Mã cán bộ) và Mật khẩu. 4. Người dùng nhấn nút "Đăng nhập". 5. Hệ thống kiểm tra tính hợp lệ của dữ liệu nhập (không được để trống). 6. Hệ thống xác thực thông tin tài khoản với cơ sở dữ liệu. 7. Hệ thống kiểm tra trạng thái tài khoản (Đang hoạt động / Bị khóa). 8. Hệ thống xác định vai trò của người dùng. 9. Hệ thống chuyển hướng người dùng đến trang chủ tương ứng. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Đăng nhập khi đã có phiên hợp lệ** A1.1. Tại bước 1, người dùng truy cập trang Đăng nhập khi đã có phiên đăng nhập hợp lệ. A1.2. Hệ thống tự động chuyển hướng người dùng đến trang chủ tương ứng. A1.3. Use case kết thúc. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Sai Tên đăng nhập hoặc Mật khẩu** E1.1. Tại bước 6, hệ thống xác thực thông tin không khớp. E1.2. Hệ thống hiển thị thông báo "Tên đăng nhập hoặc mật khẩu không đúng". E1.3. Luồng quay lại bước 3. **E2: Tài khoản bị khóa** E2.1. Tại bước 7, hệ thống phát hiện tài khoản ở trạng thái "Bị khóa". E2.2. Hệ thống hiển thị thông báo "Tài khoản của bạn đã bị khóa. Vui lòng liên hệ Quản trị viên". E2.3. Use case kết thúc. **E3: Thiếu thông tin đăng nhập** E3.1. Tại bước 5, hệ thống phát hiện Tên đăng nhập hoặc Mật khẩu bị để trống. E3.2. Hệ thống hiển thị thông báo "Vui lòng nhập đầy đủ Tên đăng nhập và Mật khẩu". E3.3. Luồng quay lại bước 3. |

### 4.2. Use Case: Đăng xuất

|  |  |
| --- | --- |
| **Tên use case** | **Đăng xuất** |
| Tác nhân chính | Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng thoát khỏi phiên làm việc hiện tại một cách an toàn. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn "Đăng xuất". |
| Điều kiện tiên quyết (Precondition) | Người dùng đang trong phiên đăng nhập hợp lệ. |
| Điều kiện thành công (Post-condition) | Phiên đăng nhập hiện tại bị hủy và người dùng được chuyển về màn hình Đăng nhập. |
| Điều kiện thất bại | Phiên đăng nhập không được hủy do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng chọn "Đăng xuất". 2. Hệ thống hiển thị hộp thoại yêu cầu xác nhận đăng xuất. 3. Người dùng xác nhận đăng xuất. 4. Hệ thống hủy phiên đăng nhập hiện tại. 5. Hệ thống chuyển hướng về màn hình Đăng nhập. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Hủy đăng xuất** A1.1. Tại bước 3, người dùng chọn "Hủy". A1.2. Hệ thống đóng hộp thoại xác nhận. A1.3. Use case kết thúc. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Lỗi hệ thống khi hủy phiên** E1.1. Tại bước 4, hệ thống gặp lỗi khi hủy phiên đăng nhập. E1.2. Hệ thống hiển thị thông báo "Không thể đăng xuất. Vui lòng thử lại sau." E1.3. Use case kết thúc. |

### 4.3. Use Case: Đổi mật khẩu

|  |  |
| --- | --- |
| **Tên use case** | **Đổi mật khẩu** |
| Tác nhân chính | Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng thay đổi mật khẩu hiện tại sang mật khẩu mới để tăng cường bảo mật tài khoản. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn "Đổi mật khẩu". |
| Điều kiện tiên quyết (Precondition) | Người dùng đang đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Mật khẩu mới được lưu thành công; lịch sử thay đổi mật khẩu được ghi nhận. |
| Điều kiện thất bại | Mật khẩu không được thay đổi. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng chọn "Đổi mật khẩu". 2. Hệ thống hiển thị biểu mẫu với các trường: Mật khẩu hiện tại, Mật khẩu mới, Xác nhận mật khẩu mới. 3. Người dùng nhập dữ liệu. 4. Người dùng nhấn "Lưu". 5. Hệ thống kiểm tra dữ liệu: Mật khẩu hiện tại khớp với cơ sở dữ liệu; Mật khẩu mới đạt quy tắc bảo mật (độ dài, ký tự đặc biệt); Mật khẩu mới và Xác nhận mật khẩu khớp nhau; Mật khẩu mới khác Mật khẩu hiện tại. 6. Hệ thống hiển thị yêu cầu xác nhận đổi mật khẩu. 7. Người dùng xác nhận. 8. Hệ thống cập nhật mật khẩu, lưu lịch sử thay đổi và thông báo đổi mật khẩu thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu nhập không hợp lệ** E1.1. Tại bước 5, hệ thống phát hiện lỗi: Mật khẩu hiện tại không đúng, Mật khẩu mới không đạt quy tắc bảo mật, Xác nhận mật khẩu không khớp, hoặc Mật khẩu mới trùng Mật khẩu hiện tại. E1.2. Hệ thống hiển thị thông báo lỗi tương ứng. E1.3. Luồng quay lại bước 3. **E2: Hủy thao tác** E2.1. Trước bước 4, người dùng nhấn "Hủy". E2.2. Hệ thống quay lại màn hình trước đó mà không lưu thay đổi. E2.3. Use case kết thúc. |

### 4.4. Use Case: Tìm kiếm tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên tra cứu tài khoản người dùng theo từ khóa và các bộ lọc vai trò, trạng thái. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên chọn menu "Quản lý tài khoản người dùng". |
| Điều kiện tiên quyết (Precondition) | Quản trị viên đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Danh sách tài khoản người dùng thỏa điều kiện tìm kiếm được hiển thị. |
| Điều kiện thất bại | Hệ thống không xử lý được yêu cầu tìm kiếm. |
| Luồng sự kiện chính (Basic Flow) | 1. Quản trị viên chọn menu "Quản lý tài khoản người dùng". 2. Hệ thống hiển thị danh sách tài khoản người dùng (phân trang). 3. Quản trị viên nhập từ khóa vào ô tìm kiếm (Mã cán bộ, Họ tên, Email); từ khóa là tùy chọn — nếu để trống, hệ thống lọc theo bộ lọc đã chọn. 4. Quản trị viên chọn bộ lọc: Vai trò (Tất cả — mặc định, Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự); Trạng thái (Tất cả, Đang hoạt động — mặc định, Bị khóa). 5. Quản trị viên nhấn nút tìm kiếm. 6. Hệ thống lọc và hiển thị danh sách kết quả bao gồm: STT, Mã cán bộ, Họ tên, Email, Vai trò, Trạng thái. Nếu không có bản ghi phù hợp, hệ thống hiển thị danh sách rỗng kèm thông báo "Không có tài khoản phù hợp". |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Lỗi hệ thống** E1.1. Tại bước 6, hệ thống gặp lỗi khi xử lý yêu cầu tìm kiếm. E1.2. Hệ thống hiển thị thông báo "Không thể xử lý yêu cầu tìm kiếm. Vui lòng thử lại sau." E1.3. Use case kết thúc. |

### 4.5. Use Case: Thêm mới tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên tạo mới tài khoản người dùng trong hệ thống. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên nhấn nút "Thêm mới người dùng". |
| Điều kiện tiên quyết (Precondition) | Quản trị viên đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Tài khoản mới được tạo, gán vai trò hợp lệ và lưu trong cơ sở dữ liệu; thông tin mật khẩu tạm thời được gửi đến email người dùng. |
| Điều kiện thất bại | Tài khoản không được tạo do dữ liệu không hợp lệ hoặc trùng lặp. |
| Luồng sự kiện chính (Basic Flow) | 1. Tại màn hình danh sách, Quản trị viên nhấn nút "Thêm mới". 2. Hệ thống hiển thị biểu mẫu thêm tài khoản. 3. Quản trị viên nhập thông tin: Email, Hồ sơ nhân sự liên kết, Vai trò. 4. Quản trị viên nhấn "Lưu". 5. Hệ thống kiểm tra tính hợp lệ: các trường bắt buộc đã điền đầy đủ, Email đúng định dạng và duy nhất, Hồ sơ nhân sự tồn tại và chưa có tài khoản liên kết, Vai trò hợp lệ. 6. Hệ thống lưu thông tin tài khoản. 7. Hệ thống tạo mật khẩu tạm thời và gửi đến email tương ứng. 8. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu nhập không hợp lệ** E1.1. Tại bước 5, hệ thống phát hiện trường thông tin không hợp lệ (Email sai định dạng, Email trùng, Hồ sơ nhân sự không tồn tại hoặc đã liên kết tài khoản, Vai trò không hợp lệ). E1.2. Hệ thống hiển thị thông báo lỗi tương ứng. E1.3. Luồng quay lại bước 3. **E2: Hủy thao tác** E2.1. Trước bước 4, Quản trị viên nhấn "Hủy". E2.2. Hệ thống quay lại màn hình danh sách tài khoản. E2.3. Use case kết thúc. **E3: Gửi email thất bại** E3.1. Tại bước 7, hệ thống không thể gửi email chứa mật khẩu tạm thời đến người dùng. E3.2. Hệ thống vẫn lưu tài khoản đã tạo và hiển thị thông báo "Tài khoản đã được tạo nhưng không thể gửi email mật khẩu. Vui lòng thử gửi lại sau." E3.3. Use case kết thúc. |

### 4.6. Use Case: Sửa thông tin tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên cập nhật thông tin tài khoản người dùng. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên chọn một tài khoản và nhấn nút "Sửa". |
| Điều kiện tiên quyết (Precondition) | Quản trị viên đã đăng nhập hệ thống. Tài khoản cần chỉnh sửa tồn tại trong hệ thống (bất kể trạng thái Đang hoạt động hay Bị khóa). |
| Điều kiện thành công (Post-condition) | Thông tin tài khoản người dùng được cập nhật trong cơ sở dữ liệu. |
| Điều kiện thất bại | Không có thay đổi nào được lưu vào hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Tại danh sách, Quản trị viên nhấn "Sửa" trên một dòng tài khoản người dùng. 2. Hệ thống hiển thị biểu mẫu cập nhật với thông tin hiện tại. 3. Quản trị viên thay đổi Email, Vai trò. 4. Quản trị viên nhấn "Lưu". 5. Hệ thống kiểm tra tính hợp lệ: các trường bắt buộc đã điền đầy đủ, Email đúng định dạng và duy nhất, Vai trò hợp lệ. 6. Hệ thống lưu thay đổi. 7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu nhập không hợp lệ** E1.1. Tại bước 5, hệ thống phát hiện trường dữ liệu không hợp lệ (Email sai định dạng hoặc trùng, Vai trò không hợp lệ). E1.2. Hệ thống hiển thị thông báo lỗi tương ứng. E1.3. Luồng quay lại bước 3. **E2: Hủy thao tác** E2.1. Trước bước 4, Quản trị viên nhấn "Hủy". E2.2. Hệ thống quay lại màn hình danh sách tài khoản. E2.3. Use case kết thúc. |

### 4.7. Use Case: Thay đổi trạng thái cho tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái cho tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên khóa hoặc mở khóa tài khoản người dùng. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Quản trị viên chọn chức năng thay đổi trạng thái tài khoản. |
| Điều kiện tiên quyết (Precondition) | Quản trị viên đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Trạng thái tài khoản được cập nhật thành "Đang hoạt động" hoặc "Bị khóa". |
| Điều kiện thất bại | Trạng thái tài khoản không thay đổi. |
| Luồng sự kiện chính (Basic Flow) | 1. Tại danh sách, Quản trị viên nhấn biểu tượng "Khóa" trên dòng tài khoản có trạng thái "Đang hoạt động". 2. Hệ thống hiển thị hộp thoại yêu cầu xác nhận. 3. Quản trị viên xác nhận. 4. Hệ thống cập nhật trạng thái tài khoản thành "Bị khóa". 5. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Mở khóa tài khoản** A1.1. Tại bước 1, Quản trị viên nhấn biểu tượng "Mở khóa" trên dòng tài khoản có trạng thái "Bị khóa". A1.2. Hệ thống hiển thị hộp thoại yêu cầu xác nhận. A1.3. Quản trị viên xác nhận. A1.4. Hệ thống cập nhật trạng thái tài khoản thành "Đang hoạt động", lưu lịch sử thay đổi và thông báo thành công. A1.5. Use case kết thúc. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không thể khóa tài khoản đang đăng nhập** E1.1. Tại bước 1, Quản trị viên chọn khóa tài khoản đang sử dụng. E1.2. Hệ thống từ chối thao tác và hiển thị thông báo "Không thể khóa tài khoản đang sử dụng". E1.3. Use case kết thúc. |

### 4.8. Use Case: Tạo mới đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Tạo mới đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, Phòng TCCB |
| Mục đích (mô tả) | Cho phép Quản trị viên hoặc Phòng TCCB tạo mới một đơn vị tổ chức trong cơ cấu tổ chức nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng "Thêm mới đơn vị" trong menu "Cơ cấu tổ chức". |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Phòng TCCB. Hệ thống đã tồn tại đơn vị gốc "Trường Đại học Thủy Lợi". |
| Điều kiện thành công (Post-condition) | Đơn vị mới được lưu thành công, gắn đúng vào cây cơ cấu tổ chức và hiển thị trên sơ đồ. |
| Điều kiện thất bại | Đơn vị không được tạo do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại. 2. Người dùng chọn một đơn vị làm đơn vị cha. 3. Người dùng nhấn chức năng "Thêm mới đơn vị" dưới cấp của đơn vị đã chọn. 4. Hệ thống hiển thị biểu mẫu nhập thông tin đơn vị mới. 5. Người dùng nhập thông tin cơ bản: Tên đơn vị, Mã đơn vị, Loại đơn vị (Hội đồng, Ban, Khoa, Phòng, Bộ môn, Phòng thí nghiệm, Trung tâm), Đơn vị cha (mặc định là đơn vị đã chọn ở bước 2). 6. Người dùng nhập thông tin liên hệ: Ngày thành lập, Địa chỉ, Địa chỉ văn phòng, Email, Số điện thoại, Website (tùy chọn). 7. Người dùng chọn thuộc tính "Đơn vị nút" nếu đơn vị không được phép có đơn vị con. 8. Người dùng nhấn "Lưu". 9. Hệ thống kiểm tra tính hợp lệ dữ liệu (các trường bắt buộc đã điền đầy đủ). 10. Hệ thống hiển thị yêu cầu xác nhận lưu. 11. Người dùng xác nhận. 12. Hệ thống lưu đơn vị mới với trạng thái mặc định "Đang hoạt động". 13. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Trùng mã đơn vị** E1.1. Tại bước 9, hệ thống phát hiện mã đơn vị đã tồn tại. E1.2. Hệ thống hiển thị thông báo "Mã đơn vị đã tồn tại. Vui lòng nhập mã khác." E1.3. Luồng quay lại bước 5. **E2: Thiếu thông tin bắt buộc** E2.1. Tại bước 9, hệ thống phát hiện thiếu các trường bắt buộc (Tên đơn vị, Mã đơn vị, Loại đơn vị). E2.2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. E2.3. Luồng quay lại bước 5. **E3: Đơn vị cha không hợp lệ** E3.1. Tại bước 3, hệ thống phát hiện đơn vị cha đang ở trạng thái "Giải thể" hoặc "Sáp nhập". E3.2. Hệ thống hiển thị thông báo "Không thể tạo đơn vị trực thuộc đơn vị đã giải thể hoặc sáp nhập." E3.3. Use case kết thúc. **E4: Hủy thao tác** E4.1. Trước bước 8, người dùng chọn "Hủy". E4.2. Hệ thống quay lại sơ đồ cơ cấu tổ chức. E4.3. Use case kết thúc. **E5: Đơn vị cha là đơn vị nút** E5.1. Tại bước 3, hệ thống phát hiện đơn vị cha đã được đánh dấu là đơn vị nút. E5.2. Hệ thống vô hiệu hóa chức năng "Thêm mới đơn vị" và hiển thị thông báo "Đơn vị này đã được đánh dấu là đơn vị nút, không thể thêm đơn vị con." E5.3. Use case kết thúc. |

### 4.9. Use Case: Sửa thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, Phòng TCCB |
| Mục đích (mô tả) | Cho phép Quản trị viên hoặc Phòng TCCB chỉnh sửa thông tin đơn vị tổ chức nhân sự trong cơ cấu tổ chức. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng "Sửa thông tin đơn vị" tại màn hình chi tiết đơn vị. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Phòng TCCB. Đơn vị tổ chức cần chỉnh sửa đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin đơn vị được cập nhật thành công. Sơ đồ cơ cấu tổ chức phản ánh dữ liệu mới. |
| Điều kiện thất bại | Thông tin đơn vị không được cập nhật do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ đơn vị hiện tại. 2. Người dùng chọn chức năng "Sửa thông tin đơn vị" của một đơn vị. 3. Hệ thống hiển thị biểu mẫu chỉnh sửa với thông tin hiện tại: Thông tin cơ bản (Tên đơn vị, Mã đơn vị — không được sửa, Loại đơn vị); Thông tin liên hệ (Địa chỉ, Địa chỉ văn phòng, Email, Số điện thoại, Website). 4. Người dùng chỉnh sửa các thông tin cần thiết. 5. Người dùng nhấn "Lưu". 6. Hệ thống kiểm tra tính hợp lệ của dữ liệu. 7. Hệ thống hiển thị yêu cầu xác nhận lưu thay đổi. 8. Người dùng xác nhận. 9. Hệ thống cập nhật thông tin đơn vị. 10. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu không hợp lệ** E1.1. Tại bước 6, hệ thống phát hiện thiếu dữ liệu bắt buộc hoặc định dạng không hợp lệ. E1.2. Hệ thống hiển thị cảnh báo và không cho phép lưu. E1.3. Luồng quay lại bước 4. **E2: Không được phép chỉnh sửa** E2.1. Tại bước 2, nếu đơn vị đang ở trạng thái "Giải thể" hoặc "Sáp nhập". E2.2. Hệ thống hiển thị thông báo từ chối chỉnh sửa. E2.3. Use case kết thúc. **E3: Hủy thao tác** E3.1. Trước bước 5, người dùng chọn "Hủy". E3.2. Hệ thống quay lại sơ đồ cơ cấu tổ chức. E3.3. Use case kết thúc. |

### 4.10. Use Case: Giải thể đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Giải thể đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, Phòng TCCB |
| Mục đích (mô tả) | Cho phép Quản trị viên hoặc Phòng TCCB giải thể một đơn vị tổ chức trong cơ cấu tổ chức nhân sự và xử lý phái sinh đối với nhân sự, hợp đồng và đơn vị con trực thuộc. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng "Giải thể" đối với một đơn vị tại menu "Cơ cấu tổ chức". |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Phòng TCCB. Đơn vị tổ chức cần giải thể đã tồn tại và đang ở trạng thái "Đang hoạt động". |
| Điều kiện thành công (Post-condition) | Trạng thái đơn vị là "Giải thể"; hợp đồng đang hiệu lực chuyển thành "Hết hiệu lực"; trạng thái hợp đồng nhân sự chuyển thành "Chưa hợp đồng"; trạng thái làm việc chuyển thành "Đang chờ xét"; liên kết đơn vị công tác bị xóa khỏi hồ sơ nhân sự; đơn vị con được xử lý theo phương án đã chọn; lịch sử thay đổi được ghi nhận. |
| Điều kiện thất bại | Việc giải thể không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại. 2. Người dùng chọn một đơn vị đang ở trạng thái "Đang hoạt động". 3. Người dùng chọn chức năng "Giải thể đơn vị". 4. Hệ thống hiển thị biểu mẫu giải thể, đồng thời hiển thị cảnh báo danh sách các đơn vị con trực thuộc (nếu có). 5. Người dùng nhập thông tin bắt buộc: Ngày hiệu lực (ngày giải thể); Quyết định (Số quyết định, Ngày quyết định, File đính kèm); Lý do (Giải thể / Tái cơ cấu / Khác). 6. Xử lý đơn vị con (nếu có): Người dùng chọn phương án — Tùy chọn A: Giải thể toàn bộ đơn vị con; Tùy chọn B: Điều chuyển đơn vị con sang đơn vị cha khác (chọn đơn vị cha mới từ danh sách). 7. Người dùng nhấn "Lưu xác nhận". 8. Hệ thống kiểm tra tính hợp lệ dữ liệu đầu vào. 9. Hệ thống thực hiện giải thể: cập nhật trạng thái đơn vị thành "Giải thể"; xử lý đơn vị con theo phương án đã chọn ở bước 6; cập nhật nhân sự thuộc đơn vị: tất cả hợp đồng đang hiệu lực chuyển thành "Hết hiệu lực", trạng thái hợp đồng nhân sự chuyển thành "Chưa hợp đồng", trạng thái làm việc chuyển thành "Đang chờ xét", xóa liên kết đơn vị công tác khỏi hồ sơ nhân sự. 10. Hệ thống lưu lịch sử thay đổi và hiển thị thông báo "Giải thể thành công". |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Đơn vị không hợp lệ để giải thể** E1.1. Tại bước 2, nếu đơn vị đang ở trạng thái "Giải thể" hoặc "Sáp nhập". E1.2. Hệ thống vô hiệu hóa chức năng và hiển thị thông báo "Đơn vị này không còn hoạt động". E1.3. Use case kết thúc. **E2: Dữ liệu không hợp lệ** E2.1. Tại bước 8, nếu thiếu thông tin bắt buộc, ngày hiệu lực sai định dạng hoặc chưa đính kèm file Quyết định. E2.2. Hệ thống chặn thao tác lưu, đánh dấu các trường bị lỗi và yêu cầu nhập lại. E2.3. Luồng quay lại bước 5. **E3: Chưa xử lý đơn vị con** E3.1. Tại bước 6, nếu đơn vị có đơn vị con nhưng người dùng chọn Tùy chọn B mà không chọn Đơn vị cha mới. E3.2. Hệ thống hiển thị cảnh báo "Vui lòng chọn đơn vị quản lý mới cho các đơn vị trực thuộc trước khi giải thể." E3.3. Luồng quay lại bước 6. **E4: Ràng buộc chức vụ quản lý** E4.1. Tại bước 8, nếu đơn vị đang có nhân sự giữ chức vụ quản lý (ví dụ: Trưởng phòng, Trưởng khoa). E4.2. Hệ thống chặn thao tác và hiển thị thông báo "Vui lòng thực hiện bãi nhiệm chức vụ quản lý của đơn vị trước khi thực hiện giải thể." E4.3. Use case kết thúc. **E5: Hủy thao tác** E5.1. Trước bước 7, người dùng chọn "Hủy". E5.2. Hệ thống quay lại sơ đồ cơ cấu tổ chức. E5.3. Use case kết thúc. |

### 4.11. Use Case: Xem chi tiết thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, Phòng TCCB |
| Mục đích (mô tả) | Cho phép Quản trị viên hoặc Phòng TCCB xem đầy đủ thông tin của một đơn vị tổ chức trong cơ cấu tổ chức. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng xem chi tiết một đơn vị trong menu "Cơ cấu tổ chức". |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Phòng TCCB. Đơn vị tổ chức đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin chi tiết của đơn vị được hiển thị từ dữ liệu hiện có trong hệ thống; không có dữ liệu nào bị thay đổi. |
| Điều kiện thất bại | Không hiển thị được dữ liệu do lỗi hệ thống hoặc đơn vị không tồn tại. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức. 2. Người dùng chọn một đơn vị trong cây. 3. Hệ thống hiển thị thông tin chi tiết đơn vị gồm các tab: Tab "Tổng quan" (Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại: Đang hoạt động / Sáp nhập / Giải thể); Tab "Nhân sự" (Danh sách nhân sự thuộc đơn vị: Họ tên, Mã cán bộ, Chức vụ, Ngày bắt đầu); Tab "Đơn vị trực thuộc" (Danh sách các đơn vị con trực thuộc); Tab "Lịch sử" (Lịch sử bổ nhiệm/miễn nhiệm chức vụ và lịch sử thay đổi tổ chức: thành lập, sáp nhập, giải thể). |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Đơn vị không tồn tại hoặc không có quyền truy cập** E1.1. Tại bước 2, nếu đơn vị không tồn tại hoặc người dùng không có quyền truy cập. E1.2. Hệ thống hiển thị thông báo phù hợp. E1.3. Use case kết thúc. **E2: Lỗi tải dữ liệu** E2.1. Tại bước 3, nếu xảy ra lỗi khi tải dữ liệu đơn vị. E2.2. Hệ thống hiển thị thông báo "Không thể tải thông tin đơn vị. Vui lòng thử lại sau." E2.3. Use case kết thúc. |

### 4.12. Use Case: Sáp nhập đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Sáp nhập đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, Phòng TCCB |
| Mục đích (mô tả) | Cho phép Quản trị viên hoặc Phòng TCCB sáp nhập một đơn vị tổ chức vào đơn vị nhận sáp nhập, chuyển nhân sự và đơn vị con trực thuộc sang đơn vị nhận. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng "Sáp nhập" đối với một đơn vị tại menu "Cơ cấu tổ chức". |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Phòng TCCB. Đơn vị tổ chức cần sáp nhập đã tồn tại và đang ở trạng thái "Đang hoạt động". |
| Điều kiện thành công (Post-condition) | Trạng thái đơn vị là "Sáp nhập"; nhân sự được chuyển sang đơn vị nhận sáp nhập với trạng thái hợp đồng và trạng thái làm việc giữ nguyên; đơn vị con trực thuộc được chuyển sang làm đơn vị con của đơn vị nhận sáp nhập; lịch sử thay đổi được ghi nhận. |
| Điều kiện thất bại | Việc sáp nhập không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại. 2. Người dùng chọn một đơn vị đang ở trạng thái "Đang hoạt động". 3. Người dùng chọn chức năng "Sáp nhập đơn vị". 4. Hệ thống hiển thị biểu mẫu sáp nhập, đồng thời hiển thị danh sách đơn vị con trực thuộc (nếu có). 5. Người dùng nhập thông tin bắt buộc: Ngày hiệu lực; Quyết định (Số quyết định, Ngày quyết định, File đính kèm); Lý do; Đơn vị nhận sáp nhập (chọn từ danh sách đơn vị đang hoạt động). 6. Hệ thống tự động thiết lập chuyển toàn bộ đơn vị con trực thuộc sang làm đơn vị con của Đơn vị nhận sáp nhập. 7. Người dùng nhấn "Lưu xác nhận". 8. Hệ thống kiểm tra tính hợp lệ dữ liệu đầu vào. 9. Hệ thống thực hiện sáp nhập: cập nhật trạng thái đơn vị thành "Sáp nhập"; cập nhật đơn vị quản lý cấp trên của đơn vị con sang Đơn vị nhận sáp nhập; chuyển toàn bộ nhân sự sang Đơn vị nhận sáp nhập (trạng thái hợp đồng giữ nguyên, trạng thái làm việc giữ nguyên "Đang công tác", thông tin đơn vị mới được cập nhật). 10. Hệ thống lưu lịch sử thay đổi và hiển thị thông báo "Sáp nhập thành công". |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Đơn vị không hợp lệ để sáp nhập** E1.1. Tại bước 2, nếu đơn vị đang ở trạng thái "Giải thể" hoặc "Sáp nhập". E1.2. Hệ thống vô hiệu hóa chức năng và hiển thị thông báo "Đơn vị này không còn hoạt động". E1.3. Use case kết thúc. **E2: Dữ liệu không hợp lệ** E2.1. Tại bước 8, nếu thiếu thông tin bắt buộc, ngày hiệu lực sai định dạng hoặc chưa đính kèm file Quyết định. E2.2. Hệ thống chặn thao tác lưu, đánh dấu các trường bị lỗi và yêu cầu nhập lại. E2.3. Luồng quay lại bước 5. **E3: Ràng buộc chức vụ quản lý** E3.1. Tại bước 8, nếu đơn vị đang có nhân sự giữ chức vụ quản lý (ví dụ: Trưởng phòng, Trưởng khoa). E3.2. Hệ thống chặn thao tác và hiển thị thông báo "Vui lòng thực hiện bãi nhiệm chức vụ quản lý của đơn vị trước khi thực hiện sáp nhập." E3.3. Use case kết thúc. **E4: Hủy thao tác** E4.1. Trước bước 7, người dùng chọn "Hủy". E4.2. Hệ thống quay lại sơ đồ cơ cấu tổ chức. E4.3. Use case kết thúc. |

## Part E: FEAT-specific SUPLs

> Mục này liệt kê toàn bộ yêu cầu bổ sung (SUPL) do Nguyễn Hồng Phúc phụ trách. Mỗi SUPL truy vết đến đúng một FEAT trong tài liệu master (stakeholder-interviews.md). Các FEAT thuộc phạm vi đóng góp của thành viên khác được ghi chú rõ.

### 6.1. Functionality – Yêu cầu chức năng bổ sung

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
|----|----------|-----------------|------|---------|
| **SUPL-F01** | Ghi nhật ký kiểm toán tự động | Hệ thống phải tự động ghi nhật ký cho mọi thao tác truy cập tài khoản, thay đổi dữ liệu, thay đổi trạng thái và thay đổi cấu hình, kèm thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. | FEAT 12.1 (Ninh) | **M** |
| **SUPL-F02** | Tự động cấp mã cán bộ | Khi tạo mới hồ sơ nhân sự, hệ thống phải tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. | FEAT 7.3 (Tung) | **M** |
| **SUPL-F03** | Tự động đăng xuất phiên không hoạt động | Hệ thống phải tự động đăng xuất phiên làm việc sau 30 phút không có tương tác của người dùng trên giao diện. | FEAT 1.3 (Phúc) | **M** |
| **SUPL-F04** | Tự động khóa tài khoản nhân sự thôi việc | Khi nhân sự được chuyển sang trạng thái thôi việc, hệ thống phải tự động khóa tài khoản liên kết của nhân sự đó. | FEAT 2.6 (Phúc) | **M** |
| **SUPL-F05** | Tự động chuyển trạng thái hợp đồng | Hệ thống phải tự động chuyển hợp đồng từ trạng thái "Còn hiệu lực" sang "Chờ gia hạn" khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. | FEAT 5.1 (Tung) | **M** |
| **SUPL-F06** | Tự động cập nhật trạng thái đăng ký đào tạo | Khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang trạng thái "Đang đào tạo", hệ thống phải tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang "Đang học". | FEAT 8.2 (Khanh) | **M** |
| **SUPL-F07** | Ngừng sử dụng / kích hoạt lại loại phụ cấp | Hệ thống phải cho phép chuyển loại phụ cấp đã được tham chiếu trong dữ liệu nghiệp vụ sang trạng thái ngừng sử dụng hoặc kích hoạt lại mà không làm mất liên kết dữ liệu lịch sử; loại phụ cấp đã được tham chiếu không được xóa. | FEAT 9.4 (Ninh) | **M** |
| **SUPL-F08** | Bảo vệ mật khẩu lưu trữ | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. | FEAT 16.1 (Phúc) | **M** |
| **SUPL-F09** | Ngừng sử dụng / kích hoạt lại loại hợp đồng | Hệ thống phải cho phép chuyển loại hợp đồng đã được tham chiếu trong dữ liệu nghiệp vụ sang trạng thái ngừng sử dụng hoặc kích hoạt lại mà không làm mất liên kết dữ liệu lịch sử; loại hợp đồng đã được tham chiếu không được xóa. | FEAT 9.5 (Ninh) | **M** |

#### Độ đo và tiêu chuẩn đáp ứng

| SUPL | Yếu tố chất lượng | Độ đo yêu cầu | Tiêu chuẩn đáp ứng |
|------|-------------------|----------------|---------------------|
| **SUPL-F01** | Tính đúng đắn – Khả năng kiểm toán | (1) Tỷ lệ thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) Tỷ lệ bản ghi có đủ 9 trường bắt buộc. | (1) 100% thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) 100% bản ghi có đủ 9/9 trường bắt buộc. |
| **SUPL-F02** | Tính đúng đắn | (1) Tỷ lệ mã cán bộ bị trùng; (2) Tỷ lệ mã được sinh đúng mẫu; (3) Tỷ lệ hồ sơ mới được cấp mã ngay khi tạo. | (1) 0% mã cán bộ bị trùng; (2) 100% mã được sinh đúng mẫu đang áp dụng; (3) 100% hồ sơ mới được cấp mã ngay khi tạo thành công. |
| **SUPL-F03** | Tính đúng đắn – Tự động hóa | Thời gian từ lần tương tác cuối cùng của người dùng đến khi hệ thống đăng xuất phiên làm việc. | Hệ thống tự động đăng xuất sau 30 phút không có tương tác của người dùng trên giao diện, với sai số không quá ±30 giây. |
| **SUPL-F04** | Tính đúng đắn – Tự động hóa | (1) Thời gian từ khi nhân sự được đánh dấu thôi việc đến khi tài khoản bị khóa; (2) Tỷ lệ tài khoản liên kết được khóa tự động đúng quy tắc. | (1) Tài khoản bị khóa trong không quá 1 phút; (2) 100% tài khoản liên kết của nhân sự thôi việc bị khóa tự động. |
| **SUPL-F05** | Tính đúng đắn – Tự động hóa | (1) Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái "Chờ gia hạn"; (2) Độ trễ từ thời điểm hợp đồng chạm ngưỡng đến khi trạng thái được cập nhật. | (1) 100% hợp đồng đủ điều kiện được chuyển đúng trạng thái; (2) Việc cập nhật hoàn tất trong không quá 24 giờ kể từ thời điểm đủ điều kiện. |
| **SUPL-F06** | Tính đúng đắn – Tự động hóa | (1) Tỷ lệ đăng ký của khóa đang ở trạng thái "Đã đăng ký" được cập nhật đúng trạng thái khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang "Đang đào tạo"; (2) Độ trễ từ thời điểm khóa đào tạo đổi trạng thái đến khi cập nhật xong toàn bộ đăng ký. | (1) 100% đăng ký của khóa đang ở trạng thái "Đã đăng ký" được chuyển sang "Đang học"; (2) Hoàn tất cập nhật trong không quá 1 phút. |
| **SUPL-F07** | Tính toàn vẹn | (1) Tỷ lệ loại phụ cấp đã được tham chiếu vẫn bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) Số loại phụ cấp đã được tham chiếu nhưng vẫn bị xóa. | (1) 100% loại phụ cấp đã được tham chiếu bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) 0 loại phụ cấp đã được tham chiếu bị xóa. |
| **SUPL-F08** | Bảo mật – Tính bí mật | (1) Tỷ lệ mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; (2) Số mật khẩu được lưu ở dạng văn bản thuần. | (1) 100% mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; (2) 0 mật khẩu được lưu ở dạng văn bản thuần. |
| **SUPL-F09** | Tính toàn vẹn | (1) Tỷ lệ loại hợp đồng đã được tham chiếu vẫn bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) Số loại hợp đồng đã được tham chiếu nhưng vẫn bị xóa. | (1) 100% loại hợp đồng đã được tham chiếu bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) 0 loại hợp đồng đã được tham chiếu bị xóa. |

### 6.2. Design Constraints – Ràng buộc thiết kế

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
|----|----------|-----------------|------|---------|
| **SUPL-DC01** | Kiến trúc Client-Server SPA + RESTful API | Hệ thống phải xây dựng theo mô hình Client-Server, frontend dạng SPA (Single Page Application) giao tiếp với backend qua RESTful API. | FEAT 1.5 (Phúc) | **M** |
| **SUPL-DC02** | Cơ cấu tổ chức dạng cây | Hệ thống phải biểu diễn cơ cấu tổ chức dưới dạng cây cha-con với một nút gốc duy nhất là Trường Đại học Thủy Lợi; hệ thống cho phép đánh dấu đơn vị là đơn vị nút (leaf node) để ngăn chặn việc tạo đơn vị con trực thuộc. | FEAT 3.1 (Phúc) | **M** |
| **SUPL-DC03** | Phân quyền theo vai trò | Hệ thống phải áp dụng phân quyền theo vai trò; mỗi chức năng và API chỉ cho phép truy cập bởi vai trò được cấp quyền. | FEAT 2.4 (Phúc) | **M** |

#### Độ đo và tiêu chuẩn đáp ứng

| SUPL | Yếu tố chất lượng | Độ đo yêu cầu | Tiêu chuẩn đáp ứng |
|------|-------------------|----------------|---------------------|
| **SUPL-DC01** | Ràng buộc thiết kế – Kiến trúc | (1) Số endpoint giao tiếp client-server không sử dụng RESTful API; (2) Số trang frontend yêu cầu full-page reload (ngoại trừ lần tải đầu tiên). | (1) 0 endpoint giao tiếp client-server ngoài RESTful API (JSON); (2) 0 trang frontend yêu cầu full-page reload (ngoại trừ lần tải đầu tiên). |
| **SUPL-DC02** | Ràng buộc thiết kế – Mô hình dữ liệu | (1) Số nút gốc trong cây tổ chức; (2) Số chu trình trong quan hệ cha-con; (3) Tỷ lệ đơn vị có liên kết cha-con hợp lệ; (4) Số đơn vị nút có đơn vị con trực thuộc. | (1) Có đúng 1 nút gốc là Trường Đại học Thủy Lợi; (2) 0 chu trình; (3) 100% đơn vị có liên kết cha-con hợp lệ; (4) 0 đơn vị nút có đơn vị con trực thuộc. |
| **SUPL-DC03** | Ràng buộc thiết kế – Phân quyền | (1) Số vai trò được định nghĩa trong mô hình phân quyền; (2) Tỷ lệ chức năng và API có ma trận quyền rõ ràng; (3) Số trường hợp truy cập trái quyền. | (1) Định nghĩa đúng 4 vai trò: Quản trị viên, Phòng TCCB, Phòng TCKT, Cán bộ nhân sự; (2) 100% chức năng và API có ma trận quyền rõ ràng; (3) 0 trường hợp truy cập trái quyền. |

### 6.3. Legal/Regulatory – Ràng buộc pháp lý

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
|----|----------|-----------------|------|---------|
| **SUPL-LR01** | Quản lý sự đồng ý thu thập dữ liệu | Hệ thống phải cho phép ghi nhận, xem lịch sử và thu hồi sự đồng ý thu thập dữ liệu cá nhân cho từng cán bộ, theo Nghị định 13/2023/NĐ-CP. | FEAT 13.1 (Phúc) | **M** |
| **SUPL-LR02** | Danh mục loại hợp đồng được phê duyệt | Hệ thống chỉ cho phép cấu hình và sử dụng loại hợp đồng thuộc danh mục được nhà trường phê duyệt. | FEAT 9.5 (Ninh) | **M** |
| **SUPL-LR03** | Lưu trữ hồ sơ nhân sự 75 năm | Hồ sơ nhân sự phải được lưu trữ tối thiểu 75 năm kể từ ngày tạo hồ sơ. | FEAT 7.3 (Tung) | **M** |
| **SUPL-LR04** | Ẩn danh hóa dữ liệu cá nhân | Hệ thống phải xử lý yêu cầu ẩn danh hóa dữ liệu cá nhân (thay thế thông tin định danh bằng dữ liệu ẩn danh) khi có yêu cầu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên, theo Nghị định 13/2023/NĐ-CP. | FEAT 13.2 (Phúc) | **M** |
| **SUPL-LR05** | Danh mục loại phụ cấp được phê duyệt | Hệ thống chỉ cho phép cấu hình và sử dụng loại phụ cấp thuộc danh mục được nhà trường phê duyệt. | FEAT 9.4 (Ninh) | **M** |
| **SUPL-LR06** | Lưu trữ hợp đồng lao động 10 năm | Hợp đồng lao động phải được lưu trữ tối thiểu 10 năm sau khi hợp đồng chấm dứt. | FEAT 5.1 (Tung) | **M** |
| **SUPL-LR07** | Lưu trữ đánh giá khen thưởng/kỷ luật 10 năm | Lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu 10 năm kể từ bản ghi đánh giá cuối cùng. | FEAT 6.1 (Khanh) | **M** |

#### Độ đo và tiêu chuẩn đáp ứng

| SUPL | Yếu tố chất lượng | Độ đo yêu cầu | Tiêu chuẩn đáp ứng |
|------|-------------------|----------------|---------------------|
| **SUPL-LR01** | Ràng buộc pháp lý – Bảo vệ dữ liệu | (1) Tỷ lệ hồ sơ nhân sự có bản ghi đồng ý hợp lệ trước khi thu thập dữ liệu cá nhân; (2) Số thao tác ghi nhận, xem lịch sử, thu hồi đồng ý không khả dụng trên giao diện. | (1) 100% hồ sơ nhân sự có bản ghi đồng ý hợp lệ trước khi thu thập dữ liệu cá nhân; (2) 0 thao tác ghi nhận, xem lịch sử, thu hồi đồng ý bị thiếu trên giao diện. |
| **SUPL-LR02** | Ràng buộc pháp lý – Danh mục nghiệp vụ | (1) Tỷ lệ loại hợp đồng trong danh mục được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số loại hợp đồng ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. | (1) 100% loại hợp đồng trong danh mục được phê duyệt có thể cấu hình và sử dụng; (2) 0 loại hợp đồng ngoài danh mục được phê duyệt được phép sử dụng. |
| **SUPL-LR03** | Ràng buộc pháp lý – Lưu trữ | (1) Số hồ sơ nhân sự bị xóa hoặc mất trước 75 năm kể từ ngày tạo; (2) Số thao tác xóa hồ sơ nhân sự chưa hết thời hạn lưu trữ không bị hệ thống chặn. | (1) 0 hồ sơ nhân sự bị xóa hoặc mất trước 75 năm; (2) 0 thao tác xóa hồ sơ nhân sự chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |
| **SUPL-LR04** | Ràng buộc pháp lý – Bảo vệ dữ liệu | (1) Tỷ lệ yêu cầu ẩn danh hóa dữ liệu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên được thực hiện thành công và có lưu vết xử lý; (2) Số trường hợp thông tin định danh chưa được thay thế bằng dữ liệu ẩn danh sau khi yêu cầu hợp lệ đã được xử lý. | (1) 100% yêu cầu ẩn danh hóa hợp lệ được thực hiện thành công và lưu vết xử lý; (2) 0 trường hợp thông tin định danh chưa được thay thế sau khi yêu cầu hợp lệ đã được xử lý. |
| **SUPL-LR05** | Ràng buộc pháp lý – Danh mục nghiệp vụ | (1) Tỷ lệ loại phụ cấp trong danh mục được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số loại phụ cấp ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. | (1) 100% loại phụ cấp trong danh mục được phê duyệt có thể cấu hình và sử dụng; (2) 0 loại phụ cấp ngoài danh mục được phê duyệt được phép sử dụng. |
| **SUPL-LR06** | Ràng buộc pháp lý – Lưu trữ | (1) Số hợp đồng lao động bị xóa hoặc mất trước 10 năm kể từ ngày chấm dứt hợp đồng; (2) Số thao tác xóa hợp đồng chưa hết thời hạn lưu trữ không bị hệ thống chặn. | (1) 0 hợp đồng lao động bị xóa hoặc mất trước 10 năm kể từ ngày chấm dứt; (2) 0 thao tác xóa hợp đồng chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |
| **SUPL-LR07** | Ràng buộc pháp lý – Lưu trữ | (1) Số bản ghi đánh giá khen thưởng/kỷ luật bị xóa hoặc mất trước 10 năm kể từ bản ghi đánh giá cuối cùng; (2) Số thao tác xóa bản ghi đánh giá chưa hết thời hạn lưu trữ không bị hệ thống chặn. | (1) 0 bản ghi đánh giá bị xóa hoặc mất trước 10 năm; (2) 0 thao tác xóa bản ghi đánh giá chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |

### Tóm tắt truy vết SUPL → FEAT

| SUPL | FEAT | Chủ sở hữu FEAT | Ghi chú |
|------|------|-----------------|---------|
| SUPL-F01 | FEAT 12.1 | Ninh | Ghi vết tác vụ — SUPL thêm yêu cầu 9 trường bắt buộc |
| SUPL-F02 | FEAT 7.3 | Tung | Tạo hồ sơ nhân sự — SUPL ràng buộc tự động cấp mã |
| SUPL-F03 | FEAT 1.3 | Phúc | Đăng xuất tự động — SUPL cụ thể hóa ngưỡng 30 phút |
| SUPL-F04 | FEAT 2.6 | Phúc | Tự động khóa tài khoản — SUPL ràng buộc sự kiện thôi việc |
| SUPL-F05 | FEAT 5.1 | Tung | Tạo/gia hạn hợp đồng — SUPL ràng buộc auto chuyển trạng thái |
| SUPL-F06 | FEAT 8.2 | Khanh | Chỉnh sửa khóa đào tạo — SUPL ràng buộc auto cập nhật đăng ký |
| SUPL-F07 | FEAT 9.4 | Ninh | Danh mục phụ cấp — SUPL ràng buộc soft-delete |
| SUPL-F08 | FEAT 16.1 | Phúc | Bảo vệ mật khẩu lưu trữ — SUPL ràng buộc mật khẩu không thể khôi phục nguyên văn |
| SUPL-F09 | FEAT 9.5 | Ninh | Danh mục hợp đồng — SUPL ràng buộc soft-delete |
| SUPL-DC01 | FEAT 1.5 | Phúc | Ràng buộc kiến trúc SPA + RESTful API |
| SUPL-DC02 | FEAT 3.1 | Phúc | Ràng buộc mô hình cây tổ chức |
| SUPL-DC03 | FEAT 2.4 | Phúc | Ràng buộc phân quyền theo vai trò |
| SUPL-LR01 | FEAT 13.1 | Phúc | Ràng buộc pháp lý — quản lý đồng ý (Nghị định 13/2023) |
| SUPL-LR02 | FEAT 9.5 | Ninh | Ràng buộc pháp lý — danh mục hợp đồng phê duyệt |
| SUPL-LR03 | FEAT 7.3 | Tung | Ràng buộc pháp lý — lưu trữ hồ sơ nhân sự 75 năm |
| SUPL-LR04 | FEAT 13.2 | Phúc | Ràng buộc pháp lý — ẩn danh hóa dữ liệu (Nghị định 13/2023) |
| SUPL-LR05 | FEAT 9.4 | Ninh | Ràng buộc pháp lý — danh mục phụ cấp phê duyệt |
| SUPL-LR06 | FEAT 5.1 | Tung | Ràng buộc pháp lý — lưu trữ hợp đồng 10 năm |
| SUPL-LR07 | FEAT 6.1 | Khanh | Ràng buộc pháp lý — lưu trữ đánh giá 10 năm |
