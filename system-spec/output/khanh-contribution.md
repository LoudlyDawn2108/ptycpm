## Part A: STRQs and FEATs (for Section II)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 4:** Phòng TCCB có thể cấu hình lương, loại phụ cấp, loại hợp đồng. | * Phân tách * Làm cho đầy đủ | * **FEAT 4.1:** Hệ thống cho phép phòng TCCB thêm mới hệ số lương (Hệ số lương được thêm sẽ được dùng làm thông tin cho hồ sơ). * **FEAT 4.2:** Hệ thống cho phép phòng TCCB sửa thông tin đối với hệ số lương chưa được hồ sơ nào sử dụng, phục vụ sửa chữa nhập liệu lỗi. * **FEAT 4.3:** Hệ thống cho phép phòng TCCB xóa hệ số lương khi không được hồ sơ nào sử dụng, hoặc thay đổi trạng thái (đưa vào trạng thái ngừng sử dụng hoặc kích hoạt lại) nếu đã được sử dụng. * **FEAT 4.4:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại phụ cấp. * **FEAT 4.5:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại hợp đồng. |

> **Ghi chú thiết kế – FEAT 4.4/4.5:** Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ thao tác "Thay đổi trạng thái" (chuyển đổi giữa "Đang sử dụng" và "Ngừng sử dụng") mà không hỗ trợ "Xóa" (khác với hệ số lương ở FEAT 4.3 có hỗ trợ xóa khi chưa được sử dụng). Thiết kế này nhằm đảm bảo tính toàn vẹn dữ liệu và phục vụ kiểm toán – các loại phụ cấp/hợp đồng đã từng được sử dụng trong hệ thống cần được lưu giữ lịch sử.

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 5:** Phòng TCKT và TCCB muốn thống kê chi tiết về nhân sự. | * Phân tách * Thêm chi tiết | * **FEAT 5.1:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê tổng quan nhân sự và biến động nhân sự. * **FEAT 5.2:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh. * **FEAT 5.3:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê hợp đồng, tình trạng làm việc, đánh giá cán bộ. * **FEAT 5.4:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê đào tạo, phát triển, bổ nhiệm nhân sự. |
| **STRQ 6:** Hệ thống yêu cầu tự động log dấu vết hoạt động người dùng (System Logging). | * Phân tách * Thêm chi tiết | * **FEAT 6.1:** Hệ thống tự động ghi vết tất cả các tác vụ truy cập tài khoản, thay đổi/cập nhật hệ thống hoặc dữ liệu. * **FEAT 6.2:** Hệ thống cho phép quản trị viên truy xuất xem và xuất Audit log (Nhật ký hệ thống) nhằm truy vết hoạt động. |

## Part B: UC Model Entries (for Section III)

- UC 4.13: Thêm mới danh mục hệ số lương
- UC 4.14: Sửa danh mục hệ số lương
- UC 4.15: Xóa danh mục hệ số lương
- UC 4.16: Thay đổi trạng thái danh mục hệ số lương
- UC 4.17: Thêm mới danh mục loại phụ cấp
- UC 4.18: Sửa danh mục loại phụ cấp
- UC 4.19: Thay đổi trạng thái danh mục loại phụ cấp
- UC 4.20: Thêm mới danh mục loại hợp đồng
- UC 4.21: Sửa danh mục loại hợp đồng
- UC 4.22: Thay đổi trạng thái danh mục loại hợp đồng
- UC 4.23: Xem chi tiết các thống kê
- UC 4.24: Xem nhật ký hệ thống (Audit Log)

## Part C: FEAT→UC Traceability (for Section III)

| FEAT | UC tương ứng |
|------|-------------|
| FEAT 4.1 | UC 4.13 (Thêm mới danh mục hệ số lương) |
| FEAT 4.2 | UC 4.14 (Sửa danh mục hệ số lương) |
| FEAT 4.3 | UC 4.15 (Xóa danh mục hệ số lương), UC 4.16 (Thay đổi trạng thái danh mục hệ số lương) |
| FEAT 4.4 | UC 4.17 (Thêm mới danh mục loại phụ cấp), UC 4.18 (Sửa danh mục loại phụ cấp), UC 4.19 (Thay đổi trạng thái danh mục loại phụ cấp) |
| FEAT 4.5 | UC 4.20 (Thêm mới danh mục loại hợp đồng), UC 4.21 (Sửa danh mục loại hợp đồng), UC 4.22 (Thay đổi trạng thái danh mục loại hợp đồng) |
| FEAT 5.1 | UC 4.23 (Thống kê tổng quan nhân sự và biến động nhân sự) |
| FEAT 5.2 | UC 4.23 (Cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh) |
| FEAT 5.3 | UC 4.23 (Hợp đồng, tình trạng làm việc, đánh giá cán bộ) |
| FEAT 5.4 | UC 4.23 (Đào tạo, phát triển, bổ nhiệm nhân sự) |
| FEAT 6.1 | SUPL Ghi nhật ký (auto logging) |
| FEAT 6.2 | UC 4.24 (Xem nhật ký hệ thống — Audit Log) — truy xuất |

## Part D: UC Specifications (for Section IV)

### 4.13. Use Case: Thêm mới danh mục hệ số lương (Ngô Đức Nam Khánh)

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB thiết lập hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công  (Post-condition) | Thiết lập hệ số lương theo ngạch/bậc thành công |
| Điều kiện thất bại | Hệ số lương không được cập nhật mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm hệ số lương.  2.  Hệ thống hiển thị màn hình nhập hệ số lương.  3.  Phòng TCCB nhập các các thông tin   * Ngạch viên chức * Bậc lương * Hệ số lương   4.  Phòng TCCB xác nhận lưu thông tin  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống thêm thông tin.  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Bậc lương trong cùng ngạch đã tồn tại * Hệ số lương phải là số thực, không được nhỏ hơn 0 * Bậc lương phải là số nguyên * Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi 3. Dữ liệu không được lưu   **E2: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách bậc lương. |

### 4.14. Use Case: Sửa danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu như nhập liệu sai sót. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục hệ số lương cần chỉnh sửa đã tồn tại trong hệ thống.  Danh mục hệ số lương đang ở trạng thái “Đang sử dụng”.  Hệ số lương chưa được hồ sơ nhân sự nào sử dụng. |
| Điều kiện thành công  (Post-condition) | Sửa hệ số lương theo ngạch/bậc thành công |
| Điều kiện thất bại | Hệ số lương không được cập nhật trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa hệ số lương của một bản ghi hệ số lương đã được cấu hình.  2.  Hệ thống hiển thị màn hình nhập hệ số lương.  3.  Phòng TCCB sửa các các thông tin   * Ngạch viên chức * Bậc lương * Hệ số lương mỗi bậc   4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống cập nhật thông tin.  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Bậc lương trong cùng ngạch đã tồn tại * Hệ số lương phải là số thực, không được nhỏ hơn 0 * Bậc lương phải là số nguyên * Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi 3. Dữ liệu không được lưu   **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, hệ thống phát hiện danh mục hệ số lương đang ở trạng thái “Ngừng sử dụng”. 2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”   **E3: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách bậc lương   **E4: Hệ số lương đã được hồ sơ nhân sự sử dụng**   1. Tại bước 1, hệ thống phát hiện hệ số lương đã được ít nhất một hồ sơ nhân sự sử dụng. 2. Hệ thống hiển thị thông báo: “Không thể chỉnh sửa hệ số lương đã được sử dụng trong hồ sơ nhân sự.” 3. Hệ thống vô hiệu hóa nút “Sửa”. |

### 4.15. Use Case: Xóa danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Xóa danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB xóa hệ số lương theo bậc và ngạch phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu như nhập liệu sai sót trong trường hợp hệ số lương chưa từng được sử dụng trong hồ sơ nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Xóa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục hệ số lương cần xóa đã tồn tại trong hệ thống.  Danh mục hệ số lương chưa được sử dụng trong bất kỳ hồ sơ nhân sự nào. |
| Điều kiện thành công  (Post-condition) | Danh mục hệ số lương được xóa hoàn toàn khỏi hệ thống. |
| Điều kiện thất bại | Danh mục hệ số lương không được xóa. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục hệ số lương trong danh sách.  2. Phòng TCCB chọn chức năng “Xóa”.  3. Hệ thống hiển thị hộp thoại xác nhận xóa.  4. Phòng TCCB xác nhận thao tác xóa.  5. Hệ thống kiểm tra điều kiện sử dụng của hệ số lương.  6. Hệ thống xóa danh mục hệ số lương thành công.  7. Hệ thống lưu lịch sử thay đổi và thông báo xóa thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Danh mục hệ số lương đã được sử dụng**   1. Tại bước 5, hệ thống phát hiện hệ số lương đã được gán cho ít nhất một hồ sơ nhân sự. 2. Hệ thống thông báo không thể xóa danh mục đã được sử dụng 3. Dữ liệu không bị xóa.   **E2: Hủy thao tác xóa**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.16. Use Case: Thay đổi trạng thái danh mục hệ số lương

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục hệ số lương** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục hệ số lương giữa "Đang sử dụng" và "Ngừng sử dụng", nhằm kiểm soát việc áp dụng hệ số lương cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục hệ số lương, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục hệ số lương cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh mục hệ số lương được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”).  Nếu chuyển sang “Ngừng sử dụng”: hệ số lương không còn được chọn khi tạo hoặc chỉnh sửa hồ sơ nhân sự mới; các hồ sơ nhân sự đã sử dụng hệ số lương này không bị ảnh hưởng.  Nếu chuyển sang “Đang sử dụng”: hệ số lương được phép chọn lại khi tạo hoặc chỉnh sửa hồ sơ nhân sự. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục hệ số lương đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục hệ số lương thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, Phòng TCCB chọn một danh mục hệ số lương đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục hệ số lương thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.17. Use Case: Thêm mới danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB thêm mới loại phụ cấp phục vụ cho việc quản lý và nhập liệu thông tin nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công  (Post-condition) | Danh mục loại phụ cấp được thêm thành công |
| Điều kiện thất bại | Loại phụ cấp  không được cập nhật mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm mới danh mục loại phụ cấp.  2.  Hệ thống hiển thị màn hình nhập danh mục loại phụ cấp.  3.  Phòng TCCB thêm các các thông tin   * Tên loại phụ cấp * Mô tả * Cách tính   4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **Không có** |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Tên loại phụ cấp dài quá 200 từ, có ký tự đặc biệt không hợp lệ. * Thông tin bắt buộc đầy đủ  2. Hệ thống báo lỗi 3. Dữ liệu không được lưu   **E2: Hủy thao tác**   1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách. |

### 4.18. Use Case: Sửa danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa loại phụ cấp phục vụ cho việc quản lý và nhập liệu thông tin nhân sự nếu có nhập liệu danh mục sai sót |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục loại phụ cấp cần chỉnh sửa đã tồn tại trong hệ thống.  Danh mục loại phụ cấp đang ở trạng thái “Đang sử dụng”. |
| Điều kiện thành công  (Post-condition) | Danh mục loại phụ cấp được sửa thành công |
| Điều kiện thất bại | Loại phụ cấp không được cập nhật trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa loại phụ cấp đã tồn tại.  2.  Hệ thống hiển thị màn hình sửa danh mục loại phụ cấp.  3.  Phòng TCCB sửa các các thông tin   * Tên loại phụ cấp * Mô tả * Cách tính   4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi: 2. Tên loại phụ cấp dài quá 200 từ, có ký tự đặc biệt không hợp lệ. 3. Thông tin bắt buộc đầy đủ  4. Hệ thống báo lỗi 5. Dữ liệu không được lưu   **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, hệ thống phát hiện danh mục loại phụ cấp đang ở trạng thái “Ngừng sử dụng”. 2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”   **E3: Hủy thao tác**   1. Tại bước 2, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách. |

### 4.19. Use Case: Thay đổi trạng thái danh mục loại phụ cấp

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục loại phụ cấp** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục loại phụ cấp giữa “Đang sử dụng” và “Ngừng sử dụng”, nhằm kiểm soát việc áp dụng loại phụ cấp cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại phụ cấp, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại phụ cấp cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh mục loại phụ cấp được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”).  Nếu chuyển sang “Ngừng sử dụng”: loại phụ cấp không còn được chọn khi tạo hoặc chỉnh sửa hồ sơ nhân sự mới; các loại phụ cấp được hồ sơ nhân sự đã sử dụng sẽ được hiển thị khác với các loại phụ cấp ở trạng thái “Đang sử dụng”.  Nếu chuyển sang “Đang sử dụng”: loại phụ cấp được phép chọn lại khi tạo hoặc chỉnh sửa hồ sơ nhân sự. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục loại phụ cấp đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại phụ cấp thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, Phòng TCCB chọn một danh mục loại phụ cấp đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại phụ cấp thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.20. Use Case: Thêm mới danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB cấu hình loại hợp đồng theo quy định nhà nước phục vụ cho việc quản lý và nhập liệu hợp đồng nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Thêm”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. |
| Điều kiện thành công  (Post-condition) | Thiết lập loại hợp đồng thành công |
| Điều kiện thất bại | Loại hợp đồng không được cập nhật mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng thêm loại hợp đồng.  2.  Hệ thống hiển thị các trường thông tin (Tên loại hợp đồng, Số tháng tối thiểu, Số tháng tối đa, Số lần gia hạn tối đa, thời gian theo ngày chờ gia hạn).  3. Phòng TCCB nhập đầy đủ thông tin  4.  Phòng TCCB xác nhận lưu thông tin  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo thêm thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Số tháng, số lần gia hạn, thời gian chờ gia hạn phải là số nguyên * Thông tin bắt buộc đầy đủ * Hệ thống báo lỗi * Dữ liệu không được lưu   **E2: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách loại hợp đồng |

### 4.21. Use Case: Sửa danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Sửa danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Phòng TCCB sửa cấu hình loại hợp đồng theo quy định nhà nước phục vụ cho việc quản lý và nhập liệu hợp đồng nhân sự nếu như nhập liệu sai sót. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Sửa”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB.  Danh mục loại hợp đồng cần chỉnh sửa đã tồn tại trong hệ thống.  Danh mục loại hợp đồng đang ở trạng thái “Đang sử dụng”. |
| Điều kiện thành công  (Post-condition) | Sửa loại hợp đồng  thành công |
| Điều kiện thất bại | Loại hợp đồng  không được cập nhật trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB truy cập chức năng sửa loại hợp đồng của một loại hợp đồng đã được cấu hình.  2.  Hệ thống hiển thị màn hình sửa loại hợp đồng và các trường thông tin  (Tên loại hợp đồng, Số tháng tối thiểu, Số tháng tối đa, Số lần gia hạn tối đa, thời gian theo ngày chờ gia hạn).  3.  Phòng TCCB sửa các các thông tin  4.  Phòng TCCB bấm lưu  5. Hệ thống kiểm tra dữ liệu hợp lệ  6. Hệ thống lưu thông tin thành công  7. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 5, Hệ thống validate phát hiện lỗi:  * Số tháng, số lần gia hạn, thời gian chờ gia hạn phải là số nguyên * Thông tin bắt buộc đầy đủ   + Hệ thống báo lỗi   + Dữ liệu không được lưu   **E2: Danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, hệ thống phát hiện danh mục loại hợp đồng đang ở trạng thái “Ngừng sử dụng”. 2. Hệ thống vô hiệu hóa nút “Sửa” hoặc hiển thị thông báo: “Không thể chỉnh sửa danh mục đã ngừng sử dụng.”   **E3: Phòng TCCB hủy thao tác**   1. Tại bước 2, Phòng TCCB nhấn “Hủy” 2. Hệ thống quay lại màn hình danh sách loại hợp đồng |

### 4.22. Use Case: Thay đổi trạng thái danh mục loại hợp đồng

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái danh mục loại hợp đồng** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thay đổi trạng thái của danh mục loại hợp đồng giữa “Đang sử dụng” và “Ngừng sử dụng”, nhằm kiểm soát việc áp dụng loại hợp đồng cho hồ sơ nhân sự mới, đồng thời bảo toàn dữ liệu và liên kết với các hồ sơ đã tồn tại. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Tại màn hình danh sách danh mục loại hợp đồng, Phòng TCCB chọn chức năng “Thay đổi trạng thái”. |
| Điều kiện tiên quyết  (Precondition) | Người dùng đăng nhập với vai trò Phòng TCCB. Danh mục loại hợp đồng cần thay đổi trạng thái đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh mục loại hợp đồng được cập nhật sang trạng thái mới (“Đang sử dụng” ↔ “Ngừng sử dụng”).  Nếu chuyển sang “Ngừng sử dụng”: loại hợp đồng không còn được chọn khi tạo hoặc chỉnh sửa hợp đồng lao động mới; các loại hợp đồng đã được sử dụng trong hợp đồng lao động sẽ được hiển thị khác với các loại hợp đồng ở trạng thái “Đang sử dụng”.  Nếu chuyển sang “Đang sử dụng”: loại hợp đồng được phép chọn lại khi tạo hoặc chỉnh sửa hợp đồng lao động. |
| Điều kiện thất bại | Không thể cập nhật trạng thái mới trong CSDL |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn một danh mục loại hợp đồng đang ở trạng thái “Đang sử dụng” trong danh sách.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Ngừng sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại hợp đồng thành “Ngừng sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Kích hoạt lại danh mục đang ở trạng thái “Ngừng sử dụng”**   1. Tại bước 1, Phòng TCCB chọn một danh mục loại hợp đồng đang ở trạng thái “Ngừng sử dụng”.  2. Phòng TCCB chọn chức năng “Thay đổi trạng thái”.  3. Hệ thống hiển thị hộp thoại xác nhận chuyển trạng thái sang “Đang sử dụng”.  4. Phòng TCCB xác nhận thao tác.  5. Hệ thống cập nhật trạng thái danh mục loại hợp đồng thành “Đang sử dụng”.  6. Hệ thống lưu lịch sử thay đổi và thông báo cập nhật thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Hệ thống đóng hộp thoại xác nhận và quay lại màn hình danh sách. |

### 4.23. Use Case: Xem chi tiết các thống kê

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết các thống kê** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cung cấp cho Phòng TCCB, Phòng TCKT có các báo cáo tổng hợp, thống kê trực quan về tình hình nhân sự, cơ cấu tổ chức, đào tạo và biến động nhân sự theo thời gian; hỗ trợ theo dõi, phân tích và ra quyết định quản lý. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng chọn menu “Báo cáo và Thống kê” trên hệ thống. |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB hoặc Phòng TCKT đã đăng nhập hệ thống.  Dữ liệu nhân sự, đơn vị, đào tạo đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Các báo cáo thống kê được hiển thị đầy đủ, chính xác. Người dùng có thể xem chi tiết, lọc dữ liệu và xuất báo cáo theo nhu cầu. |
| Điều kiện thất bại | Không hiển thị được báo cáo do lỗi dữ liệu hoặc hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Người dùng truy cập menu **“Báo cáo và Thống kê”**.  2. Hệ thống hiển thị **Danh sách nhóm báo cáo**.  3. Người dùng chọn từng nhóm báo cáo để xem chi tiết.   * Báo cáo tổng quan nhân sự * Báo cáo biến động nhân sự * Báo cáo cơ cấu nhân sự theo đơn vị * Báo cáo cơ cấu nhân sự theo trình độ, học hàm, chức danh * Báo cáo bổ nhiệm nhân sự * Báo cáo đào tạo và phát triển * Báo cáo hợp đồng và tình trạng làm việc * Báo cáo đánh giá của cán bộ với khóa đào tạo   4. Hệ thống hiển thị dữ liệu thống kê tương ứng dưới dạng biểu đồ và bảng đa dạng theo thời gian, đơn vị, loại nhân sự. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Xuất báo cáo**   1. Tại bước 4, Người dùng chọn chức năng “Xuất báo cáo” (Định dạng xuất: PDF / Excel, Phạm vi dữ liệu (theo bộ lọc hiện tại)) 2. Người dùng xác nhận xuất 3. Hệ thống tạo file báo cáo và cho phép tải về |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.24. Use Case: Xem nhật ký hệ thống (Audit Log)

|  |  |
| --- | --- |
| **Tên use case** | **Xem nhật ký hệ thống (Audit Log)** |
| Tác nhân chính | Quản trị viên |
| Mục đích (mô tả) | Cho phép Quản trị viên xem, tìm kiếm và lọc nhật ký ghi lại toàn bộ các thao tác quan trọng trên hệ thống (đăng nhập, thêm/sửa/xóa dữ liệu, phân quyền, thay đổi trạng thái…) nhằm phục vụ công tác giám sát, kiểm tra an ninh và truy vết sự cố. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Quản trị viên chọn menu "Nhật ký hệ thống" (Audit Log). |
| Điều kiện tiên quyết  (Precondition) | Người dùng đã đăng nhập với vai trò Quản trị viên hệ thống. Hệ thống đã ghi nhận các bản ghi nhật ký từ hoạt động của người dùng. |
| Điều kiện thành công  (Post-condition) | Danh sách nhật ký hệ thống được hiển thị đầy đủ, chính xác theo tiêu chí lọc. Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được nhật ký do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Quản trị viên chọn menu "Nhật ký hệ thống".  2. Hệ thống hiển thị danh sách nhật ký (phân trang), mỗi bản ghi bao gồm:   * Thời gian thao tác, * Tài khoản thực hiện (Username), * Họ tên người thực hiện, * Vai trò, * Loại hành động (Đăng nhập / Đăng xuất / Thêm / Sửa / Xóa / Phân quyền / Thay đổi trạng thái), * Đối tượng bị tác động (Tên module, Mã đối tượng), * Mô tả chi tiết thay đổi, * Địa chỉ IP.   3. Quản trị viên có thể lọc nhật ký theo các tiêu chí:   * Khoảng thời gian: Từ ngày – Đến ngày * Tài khoản thực hiện: Nhập Username hoặc Họ tên * Loại hành động: Tất cả (Mặc định), Đăng nhập, Đăng xuất, Thêm, Sửa, Xóa, Phân quyền, Thay đổi trạng thái * Module: Tất cả (Mặc định), Quản lý tài khoản, Hồ sơ nhân sự, Cơ cấu tổ chức, Hợp đồng, Đào tạo, Danh mục cấu hình   4. Quản trị viên nhấn "Tìm kiếm" hoặc "Áp dụng bộ lọc".  5. Hệ thống hiển thị kết quả nhật ký phù hợp với tiêu chí đã chọn.  6. Quản trị viên có thể nhấn vào một bản ghi để xem chi tiết thay đổi (giá trị trước và sau khi thay đổi). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Xuất nhật ký**   1. Tại bước 5, Quản trị viên chọn chức năng "Xuất nhật ký". 2. Hệ thống cho phép xuất danh sách nhật ký theo bộ lọc hiện tại dưới định dạng Excel hoặc PDF. 3. Quản trị viên xác nhận xuất. 4. Hệ thống tạo file và cho phép tải về. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không tìm thấy kết quả**   1. Tại bước 5, nếu không có bản ghi nhật ký nào phù hợp với tiêu chí lọc, Hệ thống hiển thị thông báo: "Không tìm thấy nhật ký phù hợp với tiêu chí tìm kiếm." |

## Part E: FEAT-specific SUPLs

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F01** | Ghi nhật ký hệ thống tự động (Auto Logging) | Hệ thống tự động ghi lại mọi hành động truy cập, thêm/sửa/xóa dữ liệu và thay đổi cấu hình với đầy đủ các thông tin: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. Tham chiếu FEAT 6.1. | **M** |
| **SUPL-F07** | Quy tắc nghiệp vụ chung về xóa/thay đổi trạng thái | Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ "Thay đổi trạng thái" (không hỗ trợ "Xóa") để đảm bảo tính toàn vẹn dữ liệu và phục vụ kiểm toán. Hệ số lương cho phép xóa khi chưa được hồ sơ nào sử dụng. | **M** |
| **SUPL-P03** | Thời gian tạo báo cáo thống kê | Dashboard thống kê và báo cáo tổng hợp (FEAT 5.1) phải hoàn thành render trong thời gian chấp nhận được. | **E** |

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F01 | FEAT 6.1, UC Auto Logging | System Timer |
| | SUPL-F07 | FEAT 4.3, 4.4, 4.5 | TCCB |
| **Performance** | SUPL-P03 | FEAT 5.1, UC 4.23 | TCCB, TCKT |
