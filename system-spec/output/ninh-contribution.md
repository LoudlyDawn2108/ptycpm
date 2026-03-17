# Nguyễn Hải Ninh

## Part A: STRQs and FEATs (for Section II)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 7:** Phòng TCCB có thể tạo hợp đồng lao động của nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 7.1:** Hệ thống cho phép phòng TCCB tạo hợp đồng cho nhân sự không có hợp đồng hoặc cần gia hạn hợp đồng. * **FEAT 7.2:** Hệ thống cho phép phòng TCCB xem danh sách và chi tiết hợp đồng lao động của nhân sự. * **FEAT 7.3:** Hệ thống cho phép phòng TCCB chỉnh sửa hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực. * **FEAT 7.4:** Hệ thống cho phép phòng TCCB chấm dứt hợp đồng lao động trước hạn của nhân sự. |
| **STRQ 8:** Phòng TCCB muốn quản lý hồ sơ nhân sự như thêm, sửa hồ sơ và cho phép đánh dấu thôi việc nếu nhân sự không còn làm việc, có thêm phương pháp tìm kiếm và lọc để tiện quản lý. | * Phân tách * Làm rõ * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 8.1:** Hệ thống cho phép phòng TCCB và phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa. * **FEAT 8.2:** Hệ thống cho phép phòng TCCB và phòng TCKT lọc đa tiêu chí hồ sơ nhân sự. * **FEAT 8.3:** Hệ thống cho phép phòng TCCB thêm mới hồ sơ nhân sự (gồm nhập tay hoặc upload từ Excel). * **FEAT 8.4:** Hệ thống cho phép phòng TCCB chỉnh sửa hồ sơ nhân sự (thông tin cá nhân, trình độ học vấn, khen thưởng/kỷ luật, quá trình công tác, thông tin hợp đồng). * **FEAT 8.5:** Hệ thống cho phép phòng TCCB đánh dấu thôi việc nhân sự. * **FEAT 8.6:** Hệ thống tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. * **FEAT 8.7:** Hệ thống cho phép phòng TCCB và phòng TCKT xem chi tiết hồ sơ nhân sự theo từng chế độ xem. * **FEAT 8.8:** Hệ thống cho phép phòng TCCB và phòng TCKT in hoặc xuất Excel hồ sơ nhân sự. * **FEAT 8.9:** Hệ thống cho phép phòng TCCB cấu hình ẩn/hiện các mục khen thưởng, kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc phòng TCCB. |

## Part B: UC Model Entries (for Section III)

- UC 4.25: Thêm mới Hợp đồng lao động
- UC 4.26: Xem danh sách và chi tiết hợp đồng lao động
- UC 4.27: Chỉnh sửa hợp đồng lao động chưa có hiệu lực
- UC 4.28: Chấm dứt hợp đồng lao động trước hạn
- UC 4.29: Tìm kiếm hồ sơ nhân sự
- UC 4.30: Lọc danh sách hồ sơ nhân sự
- UC 4.31: Thêm mới Hồ sơ nhân sự
- UC 4.32: Chỉnh sửa trong chi tiết hồ sơ nhân sự
- UC 4.33: Đánh dấu thôi việc nhân sự
- UC 4.34: Xem Chi tiết thông tin hồ sơ nhân sự
- UC 4.35: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật

## Part C: FEAT→UC Traceability (for Section III)

| FEAT | UC tương ứng |
|------|-------------|
| FEAT 7.1 | UC 4.25 (Thêm mới Hợp đồng lao động) |
| FEAT 7.2 | UC 4.26 (Xem danh sách và chi tiết hợp đồng lao động) |
| FEAT 7.3 | UC 4.27 (Chỉnh sửa hợp đồng lao động chưa có hiệu lực) |
| FEAT 7.4 | UC 4.28 (Chấm dứt hợp đồng lao động trước hạn) |
| FEAT 8.1 | UC 4.29 (Tìm kiếm hồ sơ nhân sự) |
| FEAT 8.2 | UC 4.30 (Lọc danh sách hồ sơ nhân sự) |
| FEAT 8.3 | UC 4.31 (Thêm mới Hồ sơ nhân sự) |
| FEAT 8.4 | UC 4.32 (Chỉnh sửa trong chi tiết hồ sơ nhân sự) |
| FEAT 8.5 | UC 4.33 (Đánh dấu thôi việc nhân sự) |
| FEAT 8.6 | UC 4.33 A1 (Thôi việc nhân sự tự động) |
| FEAT 8.7 | UC 4.34 (Xem Chi tiết thông tin hồ sơ nhân sự) |
| FEAT 8.8 | UC 4.34 A1/A2 (In hồ sơ / Xuất Excel) |
| FEAT 8.9 | UC 4.35 (Cấu hình ẩn/hiện mục khen thưởng/kỷ luật) |

## Part D: UC Specifications (for Section IV)

### 4.25. Use Case: Thêm mới Hợp đồng lao động

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Tạo mới hợp đồng với quản lý trạng thái và ràng buộc nghiệp vụ. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Thêm mới hợp đồng”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã được tạo |
| Điều kiện thành công  (Post-condition) | Hợp đồng lao động mới được tạo và gắn với hồ sơ nhân sự.  Trạng thái hợp đồng của nhân sự được cập nhật theo hợp đồng mới nhất. |
| Điều kiện thất bại | Hợp đồng không được tạo do vi phạm ràng buộc nghiệp vụ hoặc lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB chọn mục “Thêm mới hợp đồng”.  2. Hệ thống yêu cầu nhập mã nhân sự  3. Phòng TCCB nhập Mã nhân sự.  4.  Hệ thống kiểm tra: Mã nhân sự có tồn tại không và nếu tồn tại chỉ cho phép tạo hợp đồng mới nếu nhân viên có trạng thái hợp đồng "Chưa hợp đồng" hoặc “Chờ gia hạn” hoặc “Còn hiệu lực” với thời gian còn lại nằm trong thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20).  5.  Chọn `Loại hợp đồng`.  6.  Hệ thống kiểm tra số lần ký tối đa cho loại hợp đồng.  7.  Nhập thông tin hợp đồng:Số HĐ   * Ngày ký * Ngày hiệu lực * Ngày hết hạn * Đơn vị công tác theo hợp đồng * Nội dung hợp đồng (rich text editor - nhập điều khoản, mô tả công việc, quyền lợi...) * Upload PDF bản hợp đồng giấy (tải lên bản scan/file gốc đã ký)   8.  Hệ thống validate thời hạn Thời gian tối thiểu/ Thời gian tối đa của loại hợp đồng.  9.  Nhấn "Lưu".  10. Hệ thống cập nhật hợp đồng mới với trạng thái mặc định 'Còn hiệu lực', đồng thời cập nhật trạng thái hợp đồng của nhân sự thành 'Còn hiệu lực'.  11. Hệ thống lưu hợp đồng vào hồ sơ cá nhân và thông báo thành công. *Lưu ý: Xem UC 4.26 (Xem hợp đồng), UC 4.27 (Sửa hợp đồng lao động) và UC 4.28 (Chấm dứt hợp đồng lao động trước hạn) cho các tác vụ liên quan.* |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không đủ điều kiện tạo hợp đồng mới do hợp đồng hiện tại còn hiệu lực**   1. Tại bước 4, hệ thống phát hiện nhân sự không tồn tại hoặc nhân sự đang có hợp đồng ở trạng thái “Còn hiệu lực” và thời gian còn lại > thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20). 2. Hệ thống từ chối tạo hợp đồng mới. 3. Hệ thống hiển thị thông báo: *“Không thể tạo hợp đồng mới”*   **E2: Vượt quá số lần ký hợp đồng cho phép**   1. Tại bước 5, hệ thống kiểm tra số lần ký hợp đồng theo loại hợp đồng đã chọn của nhân sự. 2. Hệ thống không cho phép tiếp tục tạo hợp đồng. 3. Hiển thị thông báo: *“Vui lòng chọn loại hợp đồng khác.”*   **E3: Thời gian hợp đồng không hợp lệ hoặc trùng lặp**   1. Tại bước 8, hệ thống phát hiện: Thời hạn hợp đồng không nằm trong khoảng Min/Max theo quy định hoặc ngày hiệu lực của hợp đồng mới ≤ ngày hết hạn của hợp đồng cũ chưa chấm dứt. Các trường dữ liệu chưa đầy đủ 2. Hệ thống hiển thị thông báo: “Thời gian hợp đồng không hợp lệ hoặc bị trùng với hợp đồng trước” 3. Phòng TCCB quay lại bước 5   **E4: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. |

### 4.26. Use Case: Xem danh sách và chi tiết hợp đồng lao động (FEAT 7.2)

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách và chi tiết hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem danh sách toàn bộ hợp đồng lao động đã gắn với một hồ sơ nhân sự và xem chi tiết từng hợp đồng nhằm phục vụ tra cứu, đối chiếu và quản lý thông tin hợp đồng của nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn tab “Hợp đồng” trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách hợp đồng và thông tin chi tiết của hợp đồng được hiển thị đầy đủ, chính xác theo dữ liệu đã lưu.  Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin hợp đồng do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.34).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **“Hợp đồng”**.  4. Hệ thống hiển thị danh sách tất cả hợp đồng lao động của nhân sự, bao gồm các thông tin: Số hợp đồng, Loại hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Trạng thái hợp đồng.  5. Phòng TCCB chọn một hợp đồng trong danh sách.  6. Hệ thống hiển thị chi tiết hợp đồng đã chọn, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, Thông tin lương/quyền lợi theo hợp đồng (nếu có), File PDF đính kèm và Trạng thái hợp đồng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Nhân sự chưa có hợp đồng lao động**   1. Tại bước 3, nếu hồ sơ nhân sự chưa có hợp đồng nào được lưu. 2. Hệ thống hiển thị tab **“Hợp đồng”** ở trạng thái trống và thông báo: *“Nhân sự chưa có hợp đồng lao động.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.27. Use Case: Chỉnh sửa hợp đồng lao động chưa có hiệu lực (FEAT 7.3)

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa hợp đồng lao động chưa có hiệu lực** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa thông tin hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực, nhằm sửa sai sót nhập liệu hoặc cập nhật nội dung trước thời điểm hợp đồng bắt đầu áp dụng, đồng thời bảo đảm toàn vẹn dữ liệu hợp đồng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Sửa hợp đồng” tại màn hình chi tiết hợp đồng của nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hợp đồng lao động của nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin hợp đồng được cập nhật thành công.  Lịch sử thay đổi hợp đồng được ghi nhận. |
| Điều kiện thất bại | Hợp đồng không được cập nhật do vi phạm ràng buộc nghiệp vụ, dữ liệu không hợp lệ hoặc hợp đồng không thuộc trạng thái cho phép chỉnh sửa. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động của nhân sự từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Nếu hợp đồng đang ở trạng thái **“Chưa có hiệu lực”**, hệ thống hiển thị nút **“Sửa hợp đồng”**.  4. Phòng TCCB chọn **“Sửa hợp đồng”**.  5. Hệ thống hiển thị màn hình chỉnh sửa và cho phép cập nhật các thông tin của hợp đồng, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, File PDF đính kèm.  6. Phòng TCCB chỉnh sửa thông tin và nhấn **“Lưu”**.  7. Hệ thống kiểm tra dữ liệu hợp lệ và kiểm tra ràng buộc nghiệp vụ: hợp đồng vẫn phải ở trạng thái **“Chưa có hiệu lực”**, thời gian hợp đồng hợp lệ, không trùng lặp với các hợp đồng khác của cùng nhân sự.  8. Hệ thống cập nhật thông tin hợp đồng, lưu lịch sử thay đổi và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hợp đồng đã có hiệu lực hoặc đã hết hiệu lực**   1. Tại bước 3, nếu hợp đồng không ở trạng thái **“Chưa có hiệu lực”**. 2. Hệ thống ẩn hoặc vô hiệu hóa nút **“Sửa hợp đồng”** và hiển thị thông báo: *“Chỉ được chỉnh sửa hợp đồng chưa có hiệu lực.”*   **A2: Dữ liệu chỉnh sửa không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu thông tin bắt buộc, thời gian hợp đồng không hợp lệ hoặc dữ liệu bị trùng lặp. 2. Hệ thống hiển thị cảnh báo và yêu cầu Phòng TCCB chỉnh sửa lại thông tin. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.28. Use Case: Chấm dứt hợp đồng lao động trước hạn (FEAT 7.4)

|  |  |
| --- | --- |
| **Tên use case** | **Chấm dứt hợp đồng lao động trước hạn** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chấm dứt trước hạn một hợp đồng lao động đang còn hiệu lực của nhân sự, cập nhật lại trạng thái hợp đồng và hỗ trợ xem xét nghiệp vụ thôi việc khi nhân sự không còn hợp đồng còn hiệu lực nào. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Chấm dứt trước hạn” tại màn hình chi tiết hợp đồng. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hợp đồng lao động cần chấm dứt đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Hợp đồng được cập nhật trạng thái **“Hết hiệu lực”** kèm thông tin ngày chấm dứt và lý do chấm dứt trước hạn.  Trạng thái hợp đồng hiện tại của nhân sự được cập nhật tương ứng. |
| Điều kiện thất bại | Không thể chấm dứt hợp đồng trước hạn do hợp đồng không ở trạng thái cho phép, dữ liệu không hợp lệ hoặc người dùng không xác nhận thao tác. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Phòng TCCB chọn một hợp đồng đang ở trạng thái **“Còn hiệu lực”** và nhấn **“Chấm dứt trước hạn”**.  4. Hệ thống hiển thị biểu mẫu yêu cầu nhập **Ngày chấm dứt trước hạn** và **Lý do chấm dứt**.  5. Phòng TCCB nhập thông tin và nhấn xác nhận.  6. Hệ thống hiển thị hộp thoại xác nhận thao tác chấm dứt trước hạn.  7. Phòng TCCB xác nhận thao tác.  8. Hệ thống cập nhật hợp đồng sang trạng thái **“Hết hiệu lực”**, lưu ngày chấm dứt và lý do chấm dứt trước hạn.  9. Hệ thống cập nhật trạng thái hợp đồng hiện tại của nhân sự theo dữ liệu mới.  10. Nếu đây là hợp đồng còn hiệu lực duy nhất của nhân sự, hệ thống hiển thị thông báo để Phòng TCCB xem xét tiếp tục thực hiện UC 4.33 **“Đánh dấu thôi việc nhân sự”** nếu phù hợp nghiệp vụ. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hủy thao tác chấm dứt trước hạn**   1. Tại bước 6, Phòng TCCB chọn **“Hủy”**. 2. Hệ thống đóng hộp thoại xác nhận và không cập nhật dữ liệu hợp đồng.   **A2: Hợp đồng không ở trạng thái còn hiệu lực**   1. Tại bước 3, nếu hợp đồng không ở trạng thái **“Còn hiệu lực”**. 2. Hệ thống không cho phép thực hiện chức năng **“Chấm dứt trước hạn”** và hiển thị thông báo phù hợp. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.29. Use Case: Tìm kiếm hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích  (mô tả) | Cho phép cán bộ Phòng TCCB, phòng TCKT tìm kiếm hồ sơ nhân sự nhanh chóng dựa trên từ khóa như tên, mã nhân sự, số CCCD, email hoặc số điện thoại nhằm phục vụ công tác quản lý và tra cứu thông tin. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng nhập từ khóa tìm kiếm và thực hiện tìm kiếm trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách nhân sự thỏa mãn điều kiện được hiển thị |
| Điều kiện thất bại | Hệ thống không xử lý yêu cầu tìm kiếm |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB, phòng TCKT chọn menu "Quản lý Hồ sơ".  2.  Hệ thống hiển thị danh sách hồ sơ nhân viên (Mã, Họ tên, CCCD, Giới tính, Địa chỉ, SĐT liên hệ, Chức danh khoa học, Đơn vị công tác, Chức vụ đơn vị, Trạng thái công việc, Trạng thái hợp đồng) có phân trang.  3.  Phòng TCCB, phòng TCKT **nhập từ khóa** vào ô tìm kiếm (Tên, Mã, CCCD, SĐT).  4.  Hệ thống hiển thị kết quả tìm kiếm theo từ khóa (real-time). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Từ khóa tìm kiếm rỗng**   1. Tại bước 3, nếu phòng TCCB, phòng TCKT không nhập từ khóa 2. Hệ thống hiển thị toàn bộ danh sách hồ sơ nhân sự |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không có kết quả tìm kiếm**   1. Tại bước 4, nếu không có hồ sơ nào phù hợp với từ khóa 2. Hệ thống hiển thị thông báo: *“Không tìm thấy hồ sơ phù hợp.”* |

### 4.30. Use Case: Lọc danh sách hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Lọc danh sách hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT lọc danh sách hồ sơ nhân sự dựa trên nhiều tiêu chí nhằm thu hẹp phạm vi dữ liệu phục vụ công tác quản lý. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB, phòng TCKT chọn tiêu chí lọc trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách hồ sơ nhân sự được hiển thị đúng theo các tiêu chí lọc đã chọn |
| Điều kiện thất bại | Hệ thống không hiển thị yêu cầu lọc danh sách theo tiêu chí đã chọn do lỗi hệ thống |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB, phòng TCKT nhấn "Bộ lọc nâng cao".  2.  Hệ thống hiển thị panel lọc với nhiều tiêu chí:   * **Đơn vị công tác:** Chọn Khoa, Phòng, Ban, Bộ môn * **Chức danh khoa học:** GS, PGS, Không có * **Chức vụ đơn vị:**Trưởng khoa, Phó khoa, Không chức vụ * **Trạng thái làm việc:** Đang chờ xét,Đang công tác, Đã thôi việc * **Trạng thái hợp đồng:** Chưa hợp đồng, Còn hiệu lực, Hết hiệu lực, Chờ gia hạn. * **Giới tính:** Nam, Nữ   3.  Phòng TCCB, phòng TCKT chọn các tiêu chí lọc.  4.  Nhấn "Áp dụng bộ lọc".  5.  Hệ thống hiển thị kết quả lọc đa tiêu chí. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không có kết quả lọc**   1. Tại bước 5, nếu không có hồ sơ nào thỏa mãn tiêu chí đã chọn 2. Hệ thống hiển thị thông báo *“Không có hồ sơ phù hợp với tiêu chí lọc.”* |

### 4.31. Use Case: Thêm mới Hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tạo mới và lưu trữ đầy đủ thông tin hồ sơ nhân sự trên hệ thống. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng thêm trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được tạo mới |
| Điều kiện thất bại | Hệ thống không thể tạo mới hồ sơ do lỗi hệ thống hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB nhấn "Thêm mới".  2.  Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3.  Phòng TCCB nhập các trường thông tin:   * **Thông tin chung bắt buộc**: Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ. * **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn "Người nước ngoài", hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động. * **Thông tin gia đình  (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình. * **Thông tin ngân hàng  (bắt buộc)**: Tên Ngân hàng, Số tài khoản. * **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**. * **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết. * **Upload ảnh chân dung  (bắt buộc).** * **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học. * **Thông tin các bằng cấp  (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf. * **Thông tin các chứng chỉ  (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf. * **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình).   4. Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5. Phòng TCCB nhấn "Lưu".  6. Hệ thống tự động sinh Mã cán bộ và Trạng thái hợp đồng mặc định là “Chưa hợp đồng”, Trạng thái làm việc là “Đang chờ xét”.  7. Hệ thống lưu hồ sơ, lịch sử tạo hồ sơ và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Tạo mới hồ sơ nhân sự từ file Excel**  1. Tại bước 1 của Luồng sự kiện chính, Phòng TCCB chọn chức năng **“Thêm mới từ Excel”**.  2. Hệ thống hiển thị màn hình tải lên file Excel và cung cấp **file mẫu** theo định dạng quy định.  3. Phòng TCCB tải lên file Excel chứa danh sách hồ sơ nhân sự.  4. Hệ thống kiểm tra: Định dạng file, Cấu trúc cột dữ liệu, Các trường thông tin bắt buộc, và tính hợp lệ logic của dữ liệu từng dòng  5. Tiếp tục bước 5 của luồng chính |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**   1. Tại bước 4, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ. 2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ.   **E2: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự. |

### 4.32. Use Case: Chỉnh sửa trong chi tiết hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa trong chi tiết hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB sửa và lưu lại đầy đủ thông tin hồ sơ nhân sự trên hệ thống nếu có thay đổi hoặc sai sót trong nhập liệu. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng sửa trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự có trạng thái làm việc “Đang chờ xét”, “Đang công tác” |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được cập nhật.  Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Hồ sơ nhân sự không được cập nhật và thay đổi |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB nhấn "Sửa" một nhân sự tại danh sách.  2.  Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3.  Phòng TCCB có thể sửa các trường thông tin:   * **Thông tin chung bắt buộc**: Mã cán bộ (không thể sửa), Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ. * **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn "Người nước ngoài", hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động. * **Thông tin gia đình  (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình. * **Thông tin ngân hàng  (bắt buộc)**: Tên Ngân hàng, Số tài khoản. * **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**. * **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết. * **Upload ảnh chân dung  (bắt buộc).** * **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học. * **Thông tin các bằng cấp  (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf. * **Thông tin các chứng chỉ  (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf. * **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình). * *Lưu ý: Thông tin hợp đồng được quản lý qua UC 4.25 (Thêm mới Hợp đồng lao động), UC 4.26 (Xem hợp đồng), UC 4.27 (Sửa hợp đồng lao động), UC 4.28 (Chấm dứt hợp đồng lao động trước hạn). Thông tin đánh giá (khen thưởng/kỷ luật) được quản lý qua UC 4.38 (Ghi nhận đánh giá cho nhân sự), UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) và UC 4.40 (Tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật). Xem UC 4.35 (Cấu hình ẩn/hiện mục khen thưởng/kỷ luật) cho chức năng ẩn/hiện — tách ra từ FEAT 8.9.*   4. Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5. Cán bộ TCCB nhấn "Lưu".  6. Hệ thống lưu hồ sơ, lịch sử tạo hồ sơ và thông báo thành công |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**   1. Tại bước 5, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ. 2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ.   **E2: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách nhân sự.   **E3: Hồ sơ ở trạng thái “Đã thôi việc”**   1. Tại bước 1, hệ thống phát hiện hồ sơ nhân sự đang ở trạng thái làm việc “Đã thôi việc”. 2. Hệ thống hiển thị thông báo: “Không thể chỉnh sửa hồ sơ nhân sự đã thôi việc.” và vô hiệu hóa nút “Sửa”. |

### 4.33. Use Case: Đánh dấu thôi việc nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Đánh dấu thôi việc nhân sự** |
| Tác nhân chính | Phòng TCCB, Hệ thống |
| Mục đích (mô tả) | Cho phép phòng TCCB cập nhật trạng thái làm việc “Đã thôi việc” cho hồ sơ nhân sự |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng đánh dấu thôi việc trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. Nhân sự cần đánh dấu thôi việc đang ở trạng thái làm việc khác “Đã thôi việc”. |
| Điều kiện thành công  (Post-condition) | Trạng thái của nhân sự được cập nhật thành “Đã thôi việc” trong hồ sơ nhân sự thành công.Trạng thái hợp đồng được cập nhật thành "Hết hiệu lực" (nếu nhân sự có hợp đồng ở trạng thái "Còn hiệu lực" hoặc "Chờ gia hạn"). Nhân sự được gỡ khỏi đơn vị công tác. Tài khoản liên kết được tự động khóa. |
| Điều kiện thất bại | Trạng thái làm việc “Đã thôi việc” không được cập nhật |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, phòng TCCB chọn chức năng "Đánh dấu thôi việc" một nhân sự.  2.  Hệ thống yêu cầu xác nhận và nhập ngày, lý do thôi việc.  3.  Phòng TCCB xác nhận.  4.  Hệ thống cập nhật trạng thái làm việc thành "Đã thôi việc", trạng thái hợp đồng thành “Hết hiệu lực” (nếu có hợp đồng đang hiệu lực hoặc chờ gia hạn), nhân sự được cập nhật rời khỏi đơn vị công tác.  5. Hệ thống tự động khóa tài khoản liên kết của nhân sự (cập nhật trạng thái tài khoản thành 'Bị khóa'). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Thôi việc nhân sự tự động**   1. Hệ thống tự động cập nhật trạng thái hợp đồng “Hết hiệu lực” cho loại hợp đồng ở trạng thái “Chờ gia hạn” khi đã quá thời gian gia hạn được cấu hình và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. 2. Hệ thống tự động cập nhật trạng thái làm việc cho nhân sự vừa bị cập nhật trạng thái hợp đồng “Hết hiệu lực” thành “Đã thôi việc”. 3. Hệ thống tự động gỡ nhân sự khỏi đơn vị công tác hiện tại. 4. Hệ thống tự động cập nhật trạng thái tài khoản liên kết thành "Bị khóa". **A2: Thôi việc khi hợp đồng còn hiệu lực (thanh lý trước hạn)**   1. Tại bước 1, hệ thống phát hiện nhân sự có hợp đồng ở trạng thái "Còn hiệu lực". 2. Hệ thống hiển thị cảnh báo: "Nhân sự này vẫn còn hợp đồng đang có hiệu lực. Tiếp tục sẽ thanh lý hợp đồng trước hạn." 3. Hệ thống yêu cầu nhập lý do thanh lý hợp đồng trước hạn (ngoài ngày và lý do thôi việc ở bước 2 Basic Flow). 4. Phòng TCCB xác nhận. 5. Tiếp tục bước 4 của Basic Flow. **A3: Tự động chuyển trạng thái hợp đồng sang “Chờ gia hạn”**   1. Hệ thống (System Timer) định kỳ kiểm tra các hợp đồng đang ở trạng thái “Còn hiệu lực”. 2. Nếu thời gian còn lại của hợp đồng ≤ thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20): 3. Hệ thống tự động cập nhật trạng thái hợp đồng từ “Còn hiệu lực” sang “Chờ gia hạn”. 4. Hệ thống tự động cập nhật trạng thái hợp đồng của nhân sự thành “Chờ gia hạn”. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Nhân sự đã ở trạng thái "Đã thôi việc"**   1. Tại bước 1, hệ thống phát hiện nhân sự đã có trạng thái làm việc "Đã thôi việc". 2. Hệ thống vô hiệu hóa nút "Đánh dấu thôi việc" hoặc hiển thị cảnh báo: *"Nhân sự này đã được đánh dấu thôi việc trước đó."*   **E2: Nhân sự chưa bãi nhiệm chức vụ**   1. Tại bước 1, hệ thống phát hiện nhân sự đang giữ chức vụ quản lý (Trưởng khoa, Trưởng bộ môn...). 2. Hệ thống chặn thao tác và thông báo: "Vui lòng bãi nhiệm chức vụ của nhân sự trước khi đánh dấu thôi việc."   **E3: Hủy thao tác**   1. Tại bước 2, Phòng TCCB chọn "Hủy". 2. Hệ thống quay lại màn hình danh sách nhân sự. |

### 4.34. Use Case: Xem Chi tiết thông tin hồ sơ nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem Chi tiết thông tin hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT xem chi tiết toàn bộ thông tin hồ sơ nhân sự, có thể thực hiện in hồ sơ |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB, phòng TCKT chọn chức năng xem chi tiết trong một nhân sự trong menu “Quản lý hồ sơ nhân sự” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết hồ sơ nhân sự được hiển thị đầy đủ, chính xác ở chế độ chỉ đọc. |
| Điều kiện thất bại | Hệ thống không hiển thị được thông tin hồ sơ do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại danh sách, Phòng TCCB, phòng TCKT nhấn vào nhấn "Xem chi tiết" tại một nhân sự.  2.  Hệ thống hiển thị màn hình Chi tiết hồ sơ ở chế độ chỉ đọc.  3.  Hệ thống hiển thị đầy đủ thông tin theo các tab:   * **Tab "Thông tin chung":** Mã cán bộ,Lý lịch, liên hệ, gia đình, ảnh chân dung * **Tab "Trình độ & Chức danh":** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác. * **Tab "Thông tin Đảng/ Đoàn":** Thông tin Đảng/ Đoàn đã được lưu. * **Tab "Lương & Phụ cấp":** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng * **Tab "Hợp đồng":** Thông tin về các loại hợp đồng đồng đã ký * **Tab "Khen thưởng/Kỷ luật":** Hệ thống hiển thị mục khen thưởng/kỷ luật tùy theo cấu hình ẩn/hiện (xem UC 4.35, FEAT 8.9) và vai trò người dùng hiện tại * **Tab "Công tác":** Quá trình công tác trước khi về trường đã được ghi |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: In hồ sơ**   1. Tiếp tục bước 3, Phòng TCCB và TCKT có thể in ra hồ sơ ở định dạng PDF   **A2: Xuất ra Excel**   1. Tiếp tục bước 3, Phòng TCCB và TCKT có thể xuất ra file chứa tất cả thông tin dưới định dạng file Excel |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.35. Use Case: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật (FEAT 8.9)

|  |  |
| --- | --- |
| **Tên use case** | **Cấu hình ẩn/hiện mục khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB cấu hình ở mức toàn hệ thống việc ẩn/hiện các mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự đối với các vai trò không thuộc Phòng TCCB, nhằm kiểm soát phạm vi hiển thị thông tin theo vai trò sử dụng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng cấu hình hiển thị hồ sơ nhân sự trong menu cấu hình hệ thống. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống và có quyền cấu hình hệ thống. |
| Điều kiện thành công  (Post-condition) | Cấu hình ẩn/hiện mục **Khen thưởng/Kỷ luật** được lưu thành công và áp dụng ngay ở mức hệ thống cho các màn hình xem hồ sơ liên quan (tham chiếu UC 4.34 và UC 4.45).  Các vai trò được cấu hình là **“Ẩn”** sẽ không nhìn thấy mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự.  Phòng TCCB luôn nhìn thấy đầy đủ các mục này bất kể cấu hình. |
| Điều kiện thất bại | Cấu hình không được cập nhật do lỗi hệ thống hoặc người dùng không lưu thay đổi. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **cấu hình hệ thống**.  2. Hệ thống hiển thị danh sách nhóm cấu hình.  3. Phòng TCCB chọn nhóm cấu hình **“Hiển thị hồ sơ nhân sự”**.  4. Hệ thống hiển thị các vai trò không thuộc Phòng TCCB (ví dụ: Phòng TCKT, Cán bộ/Giảng viên/Người dùng) cùng các tùy chọn ẩn/hiện đối với mục **Khen thưởng** và **Kỷ luật**.  5. Phòng TCCB bật/tắt cấu hình hiển thị cho từng vai trò.  6. Phòng TCCB nhấn **“Lưu”**.  7. Hệ thống lưu cấu hình, thông báo thành công và áp dụng ngay cho các màn hình xem hồ sơ nhân sự tương ứng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không thay đổi cấu hình**   1. Tại bước 5, Phòng TCCB không thực hiện thay đổi nào và chọn **“Hủy”** hoặc thoát màn hình. 2. Hệ thống không cập nhật cấu hình và giữ nguyên thiết lập hiện tại. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

## Part E: FEAT-specific SUPLs

### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F02** | Tự động sinh mã nhân sự | Khi tạo mới hồ sơ nhân sự, hệ thống tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. | **M** |
| **SUPL-F05** | Tự động chuyển trạng thái hợp đồng | Hệ thống tự động chuyển trạng thái hợp đồng từ "Còn hiệu lực" sang "Chờ gia hạn" khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. | **M** |

### 2.4. Performance – Hiệu năng

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-P06** | Hiệu năng xuất Excel | Xuất danh sách nhân sự ra file Excel (FEAT 8.8) phải hoàn thành trong thời gian chấp nhận được. | **E** |

### 2.5. Security – Bảo mật

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-SE08** | Kiểm soát cấu hình ẩn/hiện mục khen thưởng/kỷ luật | Chỉ các vai trò được ủy quyền mới được phép cấu hình ẩn/hiện các mục khen thưởng/kỷ luật ở mức toàn hệ thống; mọi thay đổi cấu hình phải được ghi audit log với người thực hiện, thời gian, giá trị trước/sau. Tham chiếu FEAT 8.9. | **M** |
| **SUPL-SE09** | Kiểm soát chấm dứt hợp đồng trước hạn | Chỉ người dùng có quyền mới được phép chấm dứt hợp đồng lao động trước hạn; hệ thống phải ghi audit log đầy đủ cho thao tác này gồm mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian và giá trị trước/sau. Tham chiếu FEAT 7.4. | **M** |

### 3.1. Functionality — Yêu cầu chức năng bổ sung

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-F02** | Correctness (Tính đúng đắn) | Tỷ lệ mã sinh tự động trùng lặp; Tỷ lệ mã tuân thủ mẫu mã đang áp dụng | 0% trùng lặp mã cán bộ. 100% hồ sơ nhân sự mới được cấp mã ngay khi tạo và 100% mã sinh ra tuân thủ mẫu mã đang áp dụng. |
| **SUPL-F05** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái Chờ gia hạn đúng hạn | 100% hợp đồng đủ điều kiện được chuyển trạng thái trong ≤ 24 giờ kể từ thời điểm đủ điều kiện. |

### 3.4. Performance — Hiệu năng

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-P06** | Speed (Tốc độ) – Xuất dữ liệu | Thời gian xuất Excel | ≤ 10 giây cho ≤ 1.000 bản ghi. ≤ 30 giây cho ≤ 10.000 bản ghi. |

### 3.5. Security — Bảo mật

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-SE08** | Authorization + Auditability (Phân quyền + Kiểm toán) | Số thay đổi cấu hình ẩn/hiện không hợp lệ; Tỷ lệ thay đổi cấu hình được ghi log đầy đủ | 0 thay đổi cấu hình ẩn/hiện do vai trò không được phép thực hiện. 100% thay đổi cấu hình ẩn/hiện khen thưởng/kỷ luật được ghi audit log với user ID, thời gian, giá trị trước/sau. |
| **SUPL-SE09** | Authorization + Auditability (Phân quyền + Kiểm toán) – Chấm dứt hợp đồng | Số trường hợp chấm dứt hợp đồng trước hạn trái phép; Tỷ lệ thao tác được ghi log đầy đủ | 0 trường hợp chấm dứt hợp đồng trước hạn trái phép. 100% thao tác chấm dứt hợp đồng trước hạn được ghi audit log với mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước/sau. |

### 4. Ma trận truy vết NFR → FEAT/UC

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F02 | FEAT 8.3, UC 4.31 | TCCB |
| | SUPL-F05 | FEAT 7.1–7.4, FEAT 8.6; UC 4.25, UC 4.26–4.28 | System Timer, TCCB |
| **Performance** | SUPL-P06 | FEAT 8.8, UC 4.34 A2 | TCCB, TCKT |
