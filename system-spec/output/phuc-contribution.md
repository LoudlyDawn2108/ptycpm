# Nguyễn Hồng Phúc — Nội dung đóng góp đã đánh số lại

## Part A: STRQs and FEATs (for Section II)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | * Phân tách * Làm cho đầy đủ * Tổng quát hóa * Thêm chi tiết | * **FEAT 1.1:** Hệ thống cho phép người dùng đăng nhập bằng tài khoản. * **FEAT 1.2:** Hệ thống cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng. * **FEAT 1.3:** Hệ thống tự động đăng xuất khỏi phiên làm việc nếu người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web trong 30 phút. * **FEAT 1.4:** Hệ thống cho phép người dùng đổi mật khẩu tài khoản đang sử dụng. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 2.1:** Hệ thống cho phép quản trị viên tìm kiếm tài khoản người dùng. * **FEAT 2.2:** Hệ thống cho phép quản trị viên thêm mới tài khoản người dùng. * **FEAT 2.3:** Hệ thống cho phép quản trị viên sửa tài khoản người dùng. * **FEAT 2.4:** Hệ thống cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống tương ứng với các nhóm nghiệp vụ. * **FEAT 2.5:** Hệ thống cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Khóa/Mở khóa). * **FEAT 2.6:** Hệ thống tự động khóa tài khoản của nhân sự đã được đánh dấu thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 3.1:** Hệ thống cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi. * **FEAT 3.2:** Hệ thống cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự. * **FEAT 3.3:** Hệ thống cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự. * **FEAT 3.4:** Hệ thống cho phép quản trị viên và phòng TCCB thay đổi trạng thái của đơn vị tổ chức nhân sự (Trạng thái: Giải thể/Sáp nhập). * **FEAT 3.5:** Hệ thống cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. |

> **Ghi chú thiết kế – FEAT 2.4:** "Nhóm nghiệp vụ" trong FEAT 2.4 chỉ các vai trò chức năng được hệ thống định nghĩa sẵn, tương ứng với phân nhóm tác nhân: Quản trị viên, Phòng TCCB, Phòng TCKT, Người dùng (Cán bộ/Giảng viên/Nhân viên). Mỗi nhóm nghiệp vụ quy định tập quyền truy cập các chức năng hệ thống khác nhau.

## Part B: UC Model Entries (for Section III)

- UC 4.1: Đăng nhập
- UC 4.2: Đăng xuất
- UC 4.3: Đổi mật khẩu
- UC 4.4: Tìm kiếm tài khoản người dùng
- UC 4.5: Thêm mới tài khoản người dùng
- UC 4.6: Sửa thông tin tài khoản người dùng
- UC 4.7: Phân quyền tài khoản người dùng
- UC 4.8: Thay đổi trạng thái cho tài khoản người dùng
- UC 4.9: Tạo mới đơn vị tổ chức nhân sự
- UC 4.10: Sửa thông tin đơn vị tổ chức nhân sự
- UC 4.11: Cập nhật trạng thái cho đơn vị tổ chức nhân sự
- UC 4.12: Xem chi tiết thông tin đơn vị tổ chức nhân sự

## Part C: FEAT→UC Traceability (for Section III)

| FEAT | UC tương ứng |
|------|-------------|
| FEAT 1.1 | UC 4.1 (Đăng nhập) |
| FEAT 1.2 | UC 4.2 (Đăng xuất) |
| FEAT 1.3 | UC 4.2 A1 (Đăng xuất tự động) |
| FEAT 1.4 | UC 4.3 (Đổi mật khẩu) |
| FEAT 2.1 | UC 4.4 (Tìm kiếm tài khoản người dùng) |
| FEAT 2.2 | UC 4.5 (Thêm mới tài khoản người dùng) |
| FEAT 2.3 | UC 4.6 (Sửa thông tin tài khoản người dùng) |
| FEAT 2.4 | UC 4.7 (Phân quyền tài khoản người dùng) |
| FEAT 2.5 | UC 4.8 (Thay đổi trạng thái cho tài khoản người dùng) |
| FEAT 2.6 | UC 4.8 A2 (Tự động khóa tài khoản) |
| FEAT 3.1 | UC 4.9 (Tạo mới đơn vị tổ chức nhân sự) — cấu trúc cây |
| FEAT 3.2 | UC 4.9 (Tạo mới đơn vị tổ chức nhân sự) |
| FEAT 3.3 | UC 4.10 (Sửa thông tin đơn vị tổ chức nhân sự) |
| FEAT 3.4 | UC 4.11 (Cập nhật trạng thái cho đơn vị tổ chức nhân sự) |
| FEAT 3.5 | UC 4.12 (Xem chi tiết thông tin đơn vị tổ chức nhân sự) |

## Part D: UC Specifications (for Section IV)

### 4.1. Use Case: Đăng nhập (Nguyễn Hồng Phúc)

|  |  |
| --- | --- |
| **Tên use case** | **Đăng nhập** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng xác thực và truy cập vào hệ thống dựa trên thông tin tài khoản được cấp. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Ấn “Đăng nhập” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã được cấp tài khoản.  Hệ thống đang hoạt động bình thường. |
| Điều kiện thành công  (Post-condition) | Người dùng được chuyển đến trang chủ (Dashboard) tương ứng với vai trò của mình. |
| Điều kiện thất bại | Tác nhân đăng nhập vào tài khoản thất bại |
| Luồng sự kiện chính  (Basic Flow) | 1.  Người dùng truy cập vào địa chỉ web của hệ thống.  2.  Hệ thống hiển thị màn hình Đăng nhập.  3.  Người dùng nhập `Tên đăng nhập` (Mã nhân viên) và `Mật khẩu`.  4.  Người dùng nhấn nút "Đăng nhập".  5.  Hệ thống kiểm tra tính hợp lệ của dữ liệu nhập (không được để trống).  6.  Hệ thống xác thực thông tin tài khoản với cơ sở dữ liệu.  7.  Hệ thống kiểm tra trạng thái tài khoản (Active/ Lock).  8.  Hệ thống xác định vai trò của người dùng.  9.  Hệ thống chuyển hướng người dùng đến Dashboard tương ứng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Đăng nhập khi đã có session**   1. Tại bước 1, Người dùng truy cập trang đăng nhập khi đã có session hợp lệ, 2. Hệ thống tự động chuyển hướng vào Dashboard. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Sai Tên đăng nhập hoặc Mật khẩu**   1. Tại bước 6, hệ thống kiểm tra thông tin không khớp. 2. Hệ thống hiển thị thông báo "Tên đăng nhập hoặc mật khẩu không đúng". 3. Quay về bước 3   **E2: Tài khoản bị khóa**   1. Tại bước 7, nếu tài khoản bị khóa, 2. Hệ thống hiển thị thông báo "Tài khoản của bạn đã bị khóa. Vui lòng liên hệ Quản trị viên".   **E3: Không hợp lệ Tên đăng nhập hoặc Mật khẩu**   1. Tại bước 5, hệ thống kiểm tra không hợp lệ 2. Hệ thống hiển thị thông báo “Vui lòng nhập tên đăng nhập và mật khẩu hợp lệ” 3. Quay lại bước 3 |

### 4.2. Use Case: Đăng xuất

|  |  |
| --- | --- |
| **Tên use case** | **Đăng xuất** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự, Hệ thống |
| Mục đích (mô tả) | Cho phép người dùng thoát khỏi phiên làm việc hiện tại một cách an toàn. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Ấn “Đăng xuất” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đang trong phiên đăng nhập hợp lệ. |
| Điều kiện thành công  (Post-condition) | Phiên làm việc bị hủy bỏ.  Người dùng được chuyển về màn hình Đăng nhập. |
| Điều kiện thất bại | Không có |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng chọn "Đăng xuất".  2. Hệ thống yêu cầu xác nhận đăng xuất  3. Người dùng xác nhận đăng xuất.  4. Hệ thống hủy session hiện tại.  5. Hệ thống chuyển hướng về trang Đăng nhập. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Đăng xuất tự động**  1.  Hệ thống giám sát việc người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web.  2.  Nếu người dùng không có tương tác giao diện với trang web trong **30 phút**  3.  Hệ thống tự động hủy session.  4.  Hệ thống hiển thị thông báo "Phiên làm việc đã hết hạn" và chuyển về trang Đăng nhập. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.3. Use Case: Đổi mật khẩu

|  |  |
| --- | --- |
| **Tên use case** | **Đổi mật khẩu** |
| Tác nhân chính | Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự |
| Mục đích (mô tả) | Cho phép người dùng đã đăng nhập thay đổi mật khẩu hiện tại sang một mật khẩu mới để tăng cường bảo mật. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Ấn “Đổi mật khẩu” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đang đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Mật khẩu được đổi thành công |
| Điều kiện thất bại | Đổi mật khẩu thất bại |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng chọn "Đổi mật khẩu".  2. Hệ thống hiển thị các trường thông tin: Mật khẩu cũ, mật khẩu mới, xác nhận mật khẩu mới  3. Người dùng nhập dữ liệu.  4. Hệ thống yêu cầu xác nhận.  5. Người dùng xác nhận đổi mật khẩu.  6. Hệ thống kiểm tra dữ liệu  -  Kiểm tra "Mật khẩu hiện tại" có khớp với mật khẩu trong CSDL không.  -  Kiểm tra "Mật khẩu mới" có đúng quy tắc bảo mật (Độ dài, ký tự đặc biệt) không.  -   Kiểm tra "Mật khẩu mới" và "Xác nhận mật khẩu" có khớp nhau không.  -   Kiểm tra "Mật khẩu mới" có khác "Mật khẩu hiện tại" không.  7. Hệ thống cập nhật mật khẩu, lưu lịch sử thay đổi và thông báo đổi mật khẩu thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Sai thông tin trường dữ liệu**  1.  Tại bước 6, hệ thống phát hiện các lỗi tại các trường thông tin  2.  Hệ thống thông báo lỗi  3. Hệ thống từ chối lưu dữ liệu.  **E2: Hủy thao tác**   1. Tại bước 2, người dùng nhấn “Hủy” 2. Hệ thống quay lại màn hình chính. |

### 4.4. Use Case: Tìm kiếm tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên tìm kiếm tài khoản người dùng |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên nhập từ khóa tìm kiếm và thực hiện tìm kiếm trong menu “Quản lý tài khoản người dùng” |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách tài khoản người dùng thỏa điều kiện tìm kiếm được hiển thị. |
| Điều kiện thất bại | Hệ thống không xử lý được yêu cầu tìm kiếm |
| Luồng sự kiện chính  (Basic Flow) | 1.  Quản trị viên chọn menu "Quản lý tài khoản người dùng".  2.  Hệ thống hiển thị danh sách người dùng (phân trang).  3.  Quản trị viên nhập từ khóa vào ô tìm kiếm (Mã nhân sự, Họ tên, Email).  4. Quản trị viên chọn lọc các thông tin theo dropdown:  - **Vai trò**: Tất cả (Mặc định), Quản trị viên, Cán bộ TCCB, Cán bộ TCKT, Cán bộ nhân sự  - **Trạng thái**: Tất cả, Hoạt động (Mặc định), Không hoạt động  5.  Quản trị viên nhấn nút tìm kiếm.  6.  Hệ thống lọc và hiển thị danh sách kết quả tương ứng bao gồm các cột:  - STT  - Mã nhân sự  - Họ tên  - Email  - Vai trò  - Trạng thái |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không nhập từ khóa**   1. Tại bước 3, Quản trị viên không nhập từ khóa 2. Hệ thống hiển thị toàn bộ danh sách người dùng |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không tìm thấy kết quả**   1. Tại bước 6, Hệ thống không tìm thấy người dùng phù hợp 2. Hệ thống hiển thị thông báo “Không có người dùng” |

### 4.5. Use Case: Thêm mới tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên thêm mới tài khoản người dùng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên nhấn nút “Thêm mới người dùng”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Tài khoản người dùng mới được tạo và lưu trong cơ sở dữ liệu. |
| Điều kiện thất bại | Tài khoản người dùng không được tạo do dữ liệu không hợp lệ hoặc trùng lặp |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Quản trị viên nhấn nút "Thêm mới".  2.  Hệ thống hiển thị form thêm người dùng.  3.  Quản trị viên nhập thông tin: Email, Nhân sự, Vai trò (UC 4.7).  4.  Quản trị viên nhấn "Lưu".  5.  Hệ thống validate dữ liệu (Đầy đủ các trường thông tin, Email đúng định dạng và duy nhất, Nhân sự tồn tại và chưa có tài khoản liên kết, Vai trò tồn tại)  6. Hệ thống tự động tạo mật khẩu ngẫu nhiên và gửi mật khẩu đã tạo cho email tương ứng.  7.  Hệ thống lưu thông tin.  8.  Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện các trường thông tin không hợp lệ. 2. Hệ thống thông báo lỗi tương ứng 3. Dữ liệu không được lưu   **E2: Quản trị viên hủy thao tác**   1. Tại bước 2, Quản trị viên nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách người dùng |

### 4.6. Use Case: Sửa thông tin tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên cập nhật thông tin tài khoản người dùng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên chọn một tài khoản và nhấn nút “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống.  Tài khoản cần chỉnh sửa đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin tài khoản người dùng được cập nhật trong cơ sở dữ liệu. |
| Điều kiện thất bại | Không có thay đổi nào được lưu vào hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại danh sách, Quản trị viên nhấn "Sửa" trên một dòng user.  2.  Hệ thống hiển thị form cập nhật.  3.  Quản trị viên thay đổi Email, Vai trò (UC 4.7).  4.  Quản trị viên nhấn "Lưu".  5.  Hệ thống validate dữ liệu (Đầy đủ các trường thông tin, Email đúng định dạng và duy nhất, Vai trò tồn tại).  6.  Hệ thống lưu thay đổi.  7.  Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện trường dữ liệu không hợp lệ. 2. Hệ thống thông báo lỗi 3. Dữ liệu không được lưu   **E2: Quản trị viên** **hủy thao tác**   1. Tại bước 2, Quản trị viên nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách người dùng |

### 4.7. Use Case: Phân quyền tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Phân quyền tài khoản người dùng** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên phân quyền tài khoản người dùng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên nhấn “Phân quyền người dùng”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Tài khoản người dùng được đổi quyền thành công. |
| Điều kiện thất bại | Tài khoản người dùng được đổi quyền thất bại. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Quản trị viên bấm dropdown chọn vai trò.  2. Hệ thống hiển thị các Vai trò cho người dùng kèm các chi tiết quyền hạn cho vai trò được chọn.  **Quản trị viên** (Quản trị viên)   * Quản lý đơn vị nhân sự. * Quản lý tài khoản người dùng.   **Nhân sự phòng Tổ chức Cán bộ** (TCCB)   * Cấu hình một số danh mục: hệ số lương, loại phụ cấp và một số danh mục có thể được cấu hình trong tương lai. * Quản lý lưu trữ hợp đồng lao động của nhân sự * Quản lý hồ sơ nhân sự (thông tin cơ bản nhân sự, thông tin lương, thông tin khen thưởng/kỷ luật, thông tin, hợp đồng) * Quản lý các thông tin về đơn vị nhân sự * Quản lý các khóa đào tạo.   **Nhân sự phòng Tài chính kế toán**(TCKT)   * Xem hồ sơ nhân sự (thông tin nhân sự - thông tin hồ sơ, hợp đồng, đánh giá, lương & phụ cấp)   **Cán bộ** (Employee)   * Xem thông tin hồ sơ * Xem thông tin đơn vị đang công tác * Đăng ký các khóa đào tạo và xem thông tin khóa đào tạo đã đăng ký.   3. Quản trị viên chọn vai trò.  4. Quản trị viên nhấn **"Lưu"**.  5. Hệ thống kiểm tra tính hợp lệ của thay đổi vai trò.  6. Hệ thống lưu thay đổi vai trò, ghi lịch sử thay đổi và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Phân quyền khi được gọi từ UC 4.5 (Thêm tài khoản) hoặc UC 4.6 (Sửa tài khoản)**   1. UC 4.5 hoặc UC 4.6 gọi UC 4.7 thông qua quan hệ <<include>>. 2. Hệ thống hiển thị phần chọn vai trò (dropdown) được nhúng trực tiếp trong form thêm/sửa tài khoản. 3. Người dùng chọn vai trò cho tài khoản. 4. Hệ thống ghi nhận vai trò đã chọn như một phần của luồng thêm/sửa tài khoản. 5. Kết quả phân quyền được lưu cùng với thao tác lưu tài khoản tại UC gọi. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Quản trị viên nhấn "Hủy". 2. Hệ thống quay lại màn hình trước đó mà không lưu thay đổi. |

### 4.8. Use Case: Thay đổi trạng thái cho tài khoản người dùng

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái cho tài khoản người dùng** |
| Tác nhân chính | Quản trị viên, Hệ thống |
| Mục đích (mô tả) | Cho phép Quản trị viên thay đổi trạng thái tài khoản người dùng (Khóa/Mở khóa) |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên chọn chức năng thay đổi trạng thái khóa tài khoản người dùng. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. |
| Điều kiện thành công  (Post-condition) | Trạng thái tài khoản người dùng được cập nhật thành Hoạt động hoặc Bị khóa |
| Điều kiện thất bại | Trạng thái tài khoản người dùng không thay đổi. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại danh sách, Quản trị viên nhấn icon "Khóa" trên dòng user có trạng thái ‘Đang hoạt động’(mặc định) .  2.  Hệ thống hiển thị xác nhận.  3.  Quản trị viên xác nhận.  4.  Hệ thống cập nhật trạng thái ‘Bị khóa’ cho tài khoản.  5.  Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Mở khóa tài khoản**   1. Tại bước 1, Quản trị viên nhấn icon "Mở khóa" trên dòng user tại danh sách. 2. Hệ thống hiển thị xác nhận. 3. Quản trị viên xác nhận 4. Hệ thống cập nhật trạng thái ‘Đang hoạt động’ cho tài khoản.   **A2: Tự động khóa tài khoản**   1. Hệ thống phát hiện nhân sự liên kết với tài khoản đã được đánh dấu thôi việc. 2. Hệ thống cập nhật trạng thái ‘Bị khóa’ cho tài khoản. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không thể khóa tài khoản đang đăng nhập**   1. Tại bước 1, Quản trị viên chọn khóa tài khoản đang sử dụng 2. Hệ thống từ chối thao tác 3. Hiển thị thông báo “Không thể khóa tài khoản đang sử dụng” |

### 4.9. Use Case: Tạo mới đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Tạo mới đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép Người dùng tạo mới một đơn vị tổ chức trong hệ thống, xác định mối quan hệ đơn vị cha – đơn vị con, phục vụ việc xây dựng và quản lý cơ cấu tổ chức nhân sự và nhập liệu thông tin đơn vị đang công tác cho nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng “Thêm mới đơn vị” trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Cán bộ TCCB.  Hệ thống đã tồn tại đơn vị gốc “Trường đại học Thủy lợi”. |
| Điều kiện thành công  (Post-condition) | Đơn vị tổ chức mới được tạo và lưu thành công trong hệ thống.  Đơn vị mới được gắn đúng vào cây cơ cấu tổ chức theo quan hệ cha – con.  Sơ đồ cơ cấu tổ chức được cập nhật và hiển thị ngay sau khi tạo.  Đơn vị mới có thể được sử dụng để gán thông tin đơn vị công tác cho hồ sơ nhân sự. |
| Điều kiện thất bại | Đơn vị không được tạo do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại.  2. Người dùng chọn một đơn vị làm đơn vị cha (hoặc chọn “đơn vị gốc”).  3. Người dùng nhấn chức năng “Thêm mới đơn vị” dưới cấp của đơn vị đã chọn.  4. Hệ thống hiển thị màn hình nhập thông tin đơn vị mới.  5. Người dùng nhập các thông tin:   * Tên đơn vị * Mã đơn vị * Loại đơn vị (Hội đồng, Ban, Khoa, Phòng, Bộ môn, Phòng thí nghiệm, Trung tâm) * Đơn vị cha (mặc định là đơn vị đã chọn ở bước 3) * Thông tin liên hệ (Ngày thành lập, Địa chỉ, Địa chỉ văn phòng,  Email, Số điện thoại, link website(tùy chọn)) * Xác nhận đơn vị nút (Nếu xác nhận thì ta sẽ không thể thêm mới đơn vị con dưới đơn vị này)   6. Người dùng nhấn “Lưu”.  7. Hệ thống kiểm tra dữ liệu hợp lệ (Dữ liệu cần đầy đủ các trường bắt buộc).  8. Hệ thống xác nhận lưu  9. Người dùng xác nhận  10. Hệ thống lưu đơn vị mới vào cơ sở dữ liệu và trạng thái của đơn vị mặc định là “Đang hoạt động”.  11. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Trùng mã đơn vị**   1. Tại bước 7, hệ thống phát hiện mã đơn vị đã tồn tại. 2. Hệ thống hiển thị thông báo: “Mã đơn vị đã tồn tại. Vui lòng nhập mã khác.”   **E2: Thiếu thông tin bắt buộc**   1. Tại bước 7, hệ thống phát hiện thiếu các trường bắt buộc (Tên đơn vị, Mã đơn vị, Loại đơn vị). 2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. 3. Quay lại bước 6.   **E3: Đơn vị cha không hợp lệ**   1. Tại bước 3, hệ thống phát hiện người dùng muốn thêm mới tại đơn vị cha đang ở trạng thái Giải thể/Bị sáp nhập. 2. Hệ thống hiển thị thông báo: “Không thể tạo đơn vị trực thuộc đơn vị đã giải thể/ bị sáp nhập”   **E4: Hủy thao tác**   1. Tại bước 5, Người dùng chọn “Hủy”. 2. Quay lại sơ đồ cơ cấu tổ chức. **E5: Đơn vị cha là đơn vị nút** 1. Tại bước 3, hệ thống phát hiện đơn vị cha đã được xác nhận là đơn vị nút. 2. Hệ thống ẩn/vô hiệu hóa chức năng "Thêm mới đơn vị" dưới cấp đơn vị này và hiển thị thông báo nếu người dùng cố truy cập. |

### 4.10. Use Case: Sửa thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép Người dùng chỉnh sửa thông tin của đơn vị trong cơ cấu tổ chức nhằm đảm bảo dữ liệu luôn chính xác và cập nhật theo thực tế. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng “Sửa thông tin đơn vị” tại màn hình chi tiết đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống với vai trò Quản trị viên hoặc Cán bộ TCCB.  Đơn vị tổ chức cần chỉnh sửa đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin đơn vị được cập nhật thành công.  Sơ đồ cơ cấu tổ chức phản ánh dữ liệu mới. |
| Điều kiện thất bại | Thông tin đơn vị không được cập nhật do vi phạm ràng buộc dữ liệu hoặc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ đơn vị hiện tại  2. Người dùng chọn chức năng “Sửa thông tin đơn vị”của một đơn vị.  3. Hệ thống hiển thị form chỉnh sửa với các thông tin hiện tại của đơn vị, bao gồm:  **- Thông tin cơ bản:** Tên đơn vị, Mã đơn vị (Không được sửa), Loại đơn vị;  **- Thông tin liên hệ:** Địa chỉ, Địa chỉ văn phòng, Email, Số điện thoại, Website.  4. Người dùng chỉnh sửa các thông tin cần thiết.  5. Người dùng nhấn **“Lưu”**. 6. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  7. Hệ thống xác nhận lưu  8. Người dùng xác nhận.  9. Hệ thống cập nhật thông tin đơn vị.  10. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ**   1. Tại bước 6, hệ thống phát hiện thiếu dữ liệu bắt buộc hoặc định dạng không hợp lệ. 2. Hệ thống hiển thị cảnh báo và không cho phép lưu.   **E2: Không được phép chỉnh sửa**   1. Tại bước 2, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép chỉnh sửa.   **E3: Hủy thao tác**   1. Tại bước 5, Người dùng chọn “Hủy”. 2. Quay lại sơ đồ cơ cấu tổ chức. |

### 4.11. Use Case: Cập nhật trạng thái cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Cập nhật trạng thái cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Quản trị viên, phòng TCCB |
| Mục đích (mô tả) | Cho phép người dùng cập nhật trạng thái hoạt động của đơn vị tổ chức (Giải thể hoặc Sáp nhập), đồng thời xử lý các đơn vị con trực thuộc và tự động cập nhật dữ liệu nhân sự, hợp đồng lao động nhằm đảm bảo tính nhất quán của hệ thống. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn chức năng “Cập nhật trạng thái” đối với một đơn vị cụ thể tại menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập hệ thống với quyền Quản trị viên hoặc Phòng TCCB.  Đơn vị tổ chức cần cập nhật đã tồn tại và đang ở trạng thái “Đang hoạt động”. |
| Điều kiện thành công  (Post-condition) | Trạng thái đơn vị được cập nhật thành “Giải thể” hoặc “Sáp nhập”.  Lịch sử thay đổi trạng thái đơn vị được ghi nhận đầy đủ.  Dữ liệu nhân sự, hợp đồng lao động và trạng thái làm việc của nhân sự được cập nhật tự động theo quy định nghiệp vụ. |
| Điều kiện thất bại | Việc cập nhật trạng thái đơn vị không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức hiện tại. 2. Người dùng chọn một đơn vị đang ở trạng thái "Đang hoạt động". 3. Người dùng chọn chức năng "Cập nhật trạng thái đơn vị". 4. Hệ thống hiển thị form cập nhật, đồng thời **hiển thị cảnh báo danh sách các đơn vị con trực thuộc** (nếu có). 5. Người dùng chọn loại sự kiện: **Giải thể**. 6. Người dùng nhập các thông tin bắt buộc: 6.1. Ngày hiệu lực (ngày giải thể). 6.2. Quyết định (Số quyết định, Ngày quyết định, File đính kèm). 6.3. Lý do (Giải thể / Tái cơ cấu / Khác). 7. **Xử lý đơn vị con (Nếu có):** Người dùng chọn phương án xử lý cho các đơn vị trực thuộc: 7.1. *Tùy chọn A:* Giải thể toàn bộ đơn vị con. 7.2. *Tùy chọn B:* Điều chuyển đơn vị con sang trực thuộc một đơn vị cha khác (yêu cầu chọn đơn vị cha mới từ danh sách). 8. Người dùng nhấn nút **"Lưu xác nhận"**. 9. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào. 10. Hệ thống thực hiện cập nhật đồng loạt: 10.1. Cập nhật trạng thái đơn vị đang thao tác từ “Đang hoạt động” → **“Giải thể”**. 10.2. **Đối với đơn vị con:** Thực hiện Giải thể hoặc Cập nhật đơn vị quản lý cấp trên mới tùy theo lựa chọn tại Bước 7. 10.3. **Đối với nhân sự:**     1. Tất cả hợp đồng đang hiệu lực → "Hết hiệu lực".     2. Trạng thái hợp đồng của nhân sự → "Chưa hợp đồng".     3. Trạng thái làm việc của nhân sự → "Đang chờ xét".     4. Xóa thông tin đơn vị công tác hiện tại của các nhân sự thuộc đơn vị bị giải thể. 11. Hệ thống lưu lịch sử thay đổi và hiển thị thông báo "Cập nhật thành công". |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1.5:** Người dùng chọn loại sự kiện: **Sáp nhập** thay vì Giải thể.  **A1.6:** Người dùng nhập thông tin bắt buộc: Ngày hiệu lực, Quyết định, Lý do và **chọn Đơn vị nhận sáp nhập** từ danh sách đơn vị đang hoạt động.  **A1.7:** **Xử lý đơn vị con:** Hệ thống tự động thiết lập chuyển toàn bộ các đơn vị con trực thuộc sang làm đơn vị con của Đơn vị nhận sáp nhập.  **A1.8:** Người dùng nhấn nút **"Lưu xác nhận"**.  **A1.9:** Hệ thống kiểm tra tính hợp lệ của dữ liệu.  **A1.10:** Hệ thống thực hiện cập nhật đồng loạt:  Cập nhật trạng thái đơn vị đang thao tác từ “Đang hoạt động” → **“Sáp nhập”**.  **Đối với đơn vị con:** Cập nhật "Đơn vị quản lý cấp trên" sang Đơn vị nhận sáp nhập.  **Đối với nhân sự:** Tự động chuyển toàn bộ nhân sự sang Đơn vị nhận sáp nhập (Trạng thái hợp đồng giữ nguyên; Trạng thái làm việc giữ nguyên "Đang công tác"; Thông tin đơn vị mới được cập nhật).  **A1.11:** Hệ thống lưu lịch sử thay đổi và hiển thị thông báo "Cập nhật thành công". |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Đơn vị không hợp lệ để cập nhật trạng thái**   * Tại bước 2, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. * Hệ thống vô hiệu hóa nút chức năng và hiển thị thông báo "Đơn vị này không còn hoạt động".   **E2: Dữ liệu không hợp lệ**   * Tại bước 9 hoặc A1.9, nếu thiếu thông tin bắt buộc, ngày hiệu lực sai định dạng hoặc chưa đính kèm file Quyết định. * Hệ thống chặn thao tác lưu, bôi đỏ các trường bị lỗi và yêu cầu nhập lại.   **E3: Chưa xử lý đơn vị con khi Giải thể**   * Tại bước 7, nếu đơn vị có đơn vị con nhưng người dùng chọn Tùy chọn B (Điều chuyển) mà không chọn Đơn vị cha mới. * Hệ thống cảnh báo: *"Vui lòng chọn đơn vị quản lý mới cho các đơn vị trực thuộc trước khi giải thể."*   **E4: Ràng buộc chức vụ quản lý**   * Tại bước 7, nếu đơn vị bị giải thể đang có nhân sự giữ chức vụ quản lý (Trưởng phòng, Trưởng khoa...). * Hệ thống chặn thao tác và thông báo: *"Vui lòng thực hiện bãi nhiệm chức vụ quản lý của đơn vị trước khi thực hiện giải thể."* |

### 4.12. Use Case: Xem chi tiết thông tin đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB, Quản trị viên |
| Mục đích (mô tả) | Cho phép Phòng TCCB hoặc Quản trị viên xem đầy đủ thông tin của một đơn vị tổ chức trong cơ cấu tổ chức, bao gồm:   * Thông tin cơ bản và trạng thái đơn vị * Danh sách nhân sự và chức vụ hiện tại * Lịch sử bổ nhiệm, miễn nhiệm chức vụ * Lịch sử thay đổi tổ chức (thành lập, sáp nhập, giải thể)   Nhằm phục vụ công tác theo dõi, quản lý và tra cứu dữ liệu tổ chức nhân sự theo thời gian |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB hoặc Quản trị viên chọn  chức năng xem chi tiết một đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB hoặc Quản trị viên đã đăng nhập hệ thống.  Đơn vị tổ chức đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Toàn bộ thông tin chi tiết của đơn vị được hiển thị chính xác. Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được dữ liệu do lỗi hệ thống hoặc không tồn tại đơn vị. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống hiển thị sơ đồ cây cơ cấu tổ chức.  2. Người dùng chọn một đơn vị trong cây.  3. Hệ thống hiển thị chi tiết thông tin các đơn vị, bao gồm:   * Tab **“Tổng quan”**, bao gồm: Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị (Đang hoạt động / Sáp nhập / Giải thể) * Tab **“Nhân sự”**: Hệ thống hiển thị danh sách các nhân sự, Tên chức vụ, hệ thống hiển thị: Họ tên nhân sự, Mã cán bộ, Ngày bắt đầu. Hệ thống hiển thị danh sách nhân sự thuộc đơn vị * Tab **“Đơn vị trực thuộc”**: Hệ thống hiển thị danh sách các đơn vị dưới cấp trực thuộc đơn vị đang xem. * Tab **“Lịch sử”**: Hệ thống hiển thị lịch sử bổ nhiệm, miễn nhiệm chức vụ và lịch sử thay đổi tổ chức (thành lập, sáp nhập, giải thể). |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

## Part E: FEAT-specific SUPLs

### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F03** | Tự động đăng xuất phiên không hoạt động | Hệ thống tự động đăng xuất phiên làm việc nếu người dùng không thao tác trong 30 phút. Tham chiếu FEAT 1.3. | **M** |
| **SUPL-F04** | Tự động khóa tài khoản nhân sự thôi việc | Khi nhân sự được đánh dấu thôi việc (FEAT 8.5/8.6), hệ thống tự động chuyển tài khoản của nhân sự đó sang trạng thái khóa. Tham chiếu FEAT 2.6. | **M** |
| **SUPL-F08** | Bảo vệ mật khẩu lưu trữ | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. | **M** |

### 2.7. Design Constraints – Ràng buộc thiết kế

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-DC02** | Cơ cấu tổ chức dạng cây | Cơ cấu tổ chức đơn vị phải được mô hình hóa dưới dạng cấu trúc cây cha-con với gốc là Trường Đại học Thủy Lợi (FEAT 3.1). | **M** |
