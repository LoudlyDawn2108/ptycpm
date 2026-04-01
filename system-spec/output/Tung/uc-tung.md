# IV. ĐẶC TẢ CA SỬ DỤNG — Phần của Ngô Quang Tùng

> **Người thực hiện: Ngô Quang Tùng**
> 
> UC 4.25–4.37 (13 Use Cases)
> 
> **Skill AI:** `use-case-specification`

---

## 4.25. Use Case: Thêm mới Hợp đồng lao động (FEAT 7.1)

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tạo mới hợp đồng lao động cho nhân sự với quản lý trạng thái và ràng buộc nghiệp vụ. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng "Thêm mới hợp đồng". |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã được tạo |
| Điều kiện thành công  (Post-condition) | Hợp đồng lao động mới được tạo và gắn với hồ sơ nhân sự.  Trạng thái hợp đồng của nhân sự được cập nhật theo hợp đồng mới nhất. |
| Điều kiện thất bại | Hợp đồng không được tạo do vi phạm ràng buộc nghiệp vụ hoặc lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB chọn mục "Thêm mới hợp đồng".  2. Hệ thống yêu cầu nhập mã nhân sự  3. Phòng TCCB nhập Mã nhân sự.  4.  Hệ thống kiểm tra: Mã nhân sự có tồn tại không và nếu tồn tại chỉ cho phép tạo hợp đồng mới nếu nhân viên có trạng thái hợp đồng "Chưa hợp đồng" hoặc "Chờ gia hạn" hoặc "Còn hiệu lực" với thời gian còn lại nằm trong thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20).  5.  Phòng TCCB chọn `Loại hợp đồng`.  6.  Hệ thống kiểm tra số lần ký tối đa cho loại hợp đồng.  7.  Phòng TCCB nhập thông tin hợp đồng:Số HĐ   * Ngày ký * Ngày hiệu lực * Ngày hết hạn * Đơn vị công tác theo hợp đồng * Nội dung hợp đồng (rich text editor - nhập điều khoản, mô tả công việc, quyền lợi...) * Upload PDF bản hợp đồng giấy (tải lên bản scan/file gốc đã ký)   8.  Hệ thống validate thời hạn Thời gian tối thiểu/ Thời gian tối đa của loại hợp đồng.  9.  Phòng TCCB nhấn "Lưu".  10. Hệ thống xác định trạng thái hợp đồng: nếu Ngày hiệu lực > Ngày hiện tại → trạng thái hợp đồng = "Chưa có hiệu lực"; nếu Ngày hiệu lực ≤ Ngày hiện tại → trạng thái hợp đồng = "Còn hiệu lực". Đồng thời cập nhật trạng thái hợp đồng của nhân sự theo trạng thái hợp đồng mới nhất.  11. Hệ thống lưu hợp đồng vào hồ sơ cá nhân và thông báo thành công. *Lưu ý: Xem UC 4.26 (Xem hợp đồng), UC 4.27 (Sửa hợp đồng lao động) và UC 4.28 (Chấm dứt hợp đồng lao động trước hạn) cho các tác vụ liên quan.* |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không đủ điều kiện tạo hợp đồng mới do hợp đồng hiện tại còn hiệu lực**   1. Tại bước 4, hệ thống phát hiện nhân sự không tồn tại hoặc nhân sự đang có hợp đồng ở trạng thái "Còn hiệu lực" và thời gian còn lại > thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20). 2. Hệ thống từ chối tạo hợp đồng mới. 3. Hệ thống hiển thị thông báo: *"Không thể tạo hợp đồng mới"*. Use case kết thúc.   **E2: Vượt quá số lần ký hợp đồng cho phép**   1. Tại bước 6, hệ thống kiểm tra số lần ký hợp đồng theo loại hợp đồng đã chọn của nhân sự. 2. Hệ thống không cho phép tiếp tục tạo hợp đồng. 3. Hiển thị thông báo: *"Vui lòng chọn loại hợp đồng khác."* Phòng TCCB quay lại bước 5.   **E3: Thời gian hợp đồng không hợp lệ hoặc trùng lặp**   1. Tại bước 8, hệ thống phát hiện: Thời hạn hợp đồng không nằm trong khoảng Min/Max theo quy định hoặc ngày hiệu lực của hợp đồng mới ≤ ngày hết hạn của hợp đồng cũ chưa chấm dứt. Các trường dữ liệu chưa đầy đủ 2. Hệ thống hiển thị thông báo: "Thời gian hợp đồng không hợp lệ hoặc bị trùng với hợp đồng trước" 3. Phòng TCCB quay lại bước 5   **E4: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn "Hủy". 2. Quay lại màn hình danh sách nhân sự. |

---

## 4.26. Use Case: Xem danh sách và chi tiết hợp đồng lao động (FEAT 7.2)

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách và chi tiết hợp đồng lao động** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem danh sách toàn bộ hợp đồng lao động đã gắn với một hồ sơ nhân sự và xem chi tiết từng hợp đồng nhằm phục vụ tra cứu, đối chiếu và quản lý thông tin hợp đồng của nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn tab "Hợp đồng" trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách hợp đồng và thông tin chi tiết của hợp đồng được hiển thị đầy đủ, chính xác theo dữ liệu đã lưu.  Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin hợp đồng do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.35).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **"Hợp đồng"**.  4. Hệ thống hiển thị danh sách tất cả hợp đồng lao động của nhân sự, bao gồm các thông tin: Số hợp đồng, Loại hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Trạng thái hợp đồng.  5. Phòng TCCB chọn một hợp đồng trong danh sách.  6. Hệ thống hiển thị chi tiết hợp đồng đã chọn, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, Thông tin lương/quyền lợi theo hợp đồng (nếu có), File PDF đính kèm và Trạng thái hợp đồng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Nhân sự chưa có hợp đồng lao động**   1. Tại bước 3, nếu hồ sơ nhân sự chưa có hợp đồng nào được lưu. 2. Hệ thống hiển thị tab **"Hợp đồng"** ở trạng thái trống và thông báo: *"Nhân sự chưa có hợp đồng lao động."* Use case kết thúc. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

---

## 4.27. Use Case: Chỉnh sửa hợp đồng lao động chưa có hiệu lực (FEAT 7.3)

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa hợp đồng lao động chưa có hiệu lực** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa thông tin hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực, nhằm sửa sai sót nhập liệu hoặc cập nhật nội dung trước thời điểm hợp đồng bắt đầu áp dụng, đồng thời bảo đảm toàn vẹn dữ liệu hợp đồng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng "Sửa hợp đồng" tại màn hình chi tiết hợp đồng của nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hợp đồng lao động của nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin hợp đồng được cập nhật thành công.  Lịch sử thay đổi hợp đồng được ghi nhận. |
| Điều kiện thất bại | Hợp đồng không được cập nhật do vi phạm ràng buộc nghiệp vụ, dữ liệu không hợp lệ hoặc hợp đồng không thuộc trạng thái cho phép chỉnh sửa. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động của nhân sự từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Nếu hợp đồng đang ở trạng thái **"Chưa có hiệu lực"**, hệ thống hiển thị nút **"Sửa hợp đồng"**.  4. Phòng TCCB chọn **"Sửa hợp đồng"**.  5. Hệ thống hiển thị màn hình chỉnh sửa và cho phép cập nhật các thông tin của hợp đồng, bao gồm: Loại hợp đồng, Số hợp đồng, Ngày ký, Ngày hiệu lực, Ngày hết hạn, Đơn vị công tác theo hợp đồng, Nội dung hợp đồng, File PDF đính kèm.  6. Phòng TCCB chỉnh sửa thông tin và nhấn **"Lưu"**.  7. Hệ thống kiểm tra dữ liệu hợp lệ và kiểm tra ràng buộc nghiệp vụ: hợp đồng vẫn phải ở trạng thái **"Chưa có hiệu lực"**, thời gian hợp đồng hợp lệ, không trùng lặp với các hợp đồng khác của cùng nhân sự.  8. Hệ thống cập nhật thông tin hợp đồng, lưu lịch sử thay đổi và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hợp đồng đã có hiệu lực hoặc đã hết hiệu lực**   1. Tại bước 3, nếu hợp đồng không ở trạng thái **"Chưa có hiệu lực"**. 2. Hệ thống ẩn hoặc vô hiệu hóa nút **"Sửa hợp đồng"** và hiển thị thông báo: *"Chỉ được chỉnh sửa hợp đồng chưa có hiệu lực."* Use case kết thúc. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu chỉnh sửa không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu thông tin bắt buộc, thời gian hợp đồng không hợp lệ hoặc dữ liệu bị trùng lặp. 2. Hệ thống hiển thị cảnh báo và yêu cầu Phòng TCCB chỉnh sửa lại thông tin. Quay lại bước 5. |

---

## 4.28. Use Case: Chấm dứt hợp đồng lao động trước hạn (FEAT 7.4)

|  |  |
| --- | --- |
| **Tên use case** | **Chấm dứt hợp đồng lao động trước hạn** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chấm dứt trước hạn một hợp đồng lao động đang còn hiệu lực của nhân sự, cập nhật lại trạng thái hợp đồng và hỗ trợ xem xét nghiệp vụ thôi việc khi nhân sự không còn hợp đồng còn hiệu lực nào. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng "Chấm dứt trước hạn" tại màn hình chi tiết hợp đồng. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hợp đồng lao động cần chấm dứt đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Hợp đồng được cập nhật trạng thái **"Hết hiệu lực"** kèm thông tin ngày chấm dứt và lý do chấm dứt trước hạn.  Trạng thái hợp đồng hiện tại của nhân sự được cập nhật tương ứng. |
| Điều kiện thất bại | Không thể chấm dứt hợp đồng trước hạn do hợp đồng không ở trạng thái cho phép, dữ liệu không hợp lệ hoặc người dùng không xác nhận thao tác. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chi tiết một hợp đồng lao động từ UC 4.26.  2. Hệ thống hiển thị chi tiết hợp đồng.  3. Phòng TCCB chọn một hợp đồng đang ở trạng thái **"Còn hiệu lực"** và nhấn **"Chấm dứt trước hạn"**.  4. Hệ thống hiển thị biểu mẫu yêu cầu nhập **Ngày chấm dứt trước hạn** và **Lý do chấm dứt**.  5. Phòng TCCB nhập thông tin và nhấn xác nhận.  6. Hệ thống hiển thị hộp thoại xác nhận thao tác chấm dứt trước hạn.  7. Phòng TCCB xác nhận thao tác.  8. Hệ thống cập nhật hợp đồng sang trạng thái **"Hết hiệu lực"**, lưu ngày chấm dứt và lý do chấm dứt trước hạn.  9. Hệ thống cập nhật trạng thái hợp đồng hiện tại của nhân sự theo dữ liệu mới.  10. Nếu đây là hợp đồng còn hiệu lực duy nhất của nhân sự, hệ thống hiển thị thông báo để Phòng TCCB xem xét tiếp tục thực hiện UC 4.33 **"Đánh dấu thôi việc nhân sự"** nếu phù hợp nghiệp vụ. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hủy thao tác chấm dứt trước hạn**   1. Tại bước 6, Phòng TCCB chọn **"Hủy"**. 2. Hệ thống đóng hộp thoại xác nhận và không cập nhật dữ liệu hợp đồng. Use case kết thúc.   **A2: Hợp đồng không ở trạng thái còn hiệu lực**   1. Tại bước 3, nếu hợp đồng không ở trạng thái **"Còn hiệu lực"**. 2. Hệ thống không cho phép thực hiện chức năng **"Chấm dứt trước hạn"** và hiển thị thông báo phù hợp. Use case kết thúc. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

---

## 4.29. Use Case: Tìm kiếm hồ sơ nhân sự (FEAT 8.1)

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích  (mô tả) | Cho phép cán bộ Phòng TCCB, phòng TCKT tìm kiếm hồ sơ nhân sự nhanh chóng dựa trên từ khóa như tên, mã nhân sự, số CCCD, email hoặc số điện thoại nhằm phục vụ công tác quản lý và tra cứu thông tin. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Người dùng nhập từ khóa tìm kiếm và thực hiện tìm kiếm trong menu "Quản lý hồ sơ nhân sự" |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách nhân sự thỏa mãn điều kiện được hiển thị |
| Điều kiện thất bại | Hệ thống không xử lý yêu cầu tìm kiếm |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB, phòng TCKT chọn menu "Quản lý Hồ sơ".  2.  Hệ thống hiển thị danh sách hồ sơ nhân viên (Mã, Họ tên, CCCD, Giới tính, Địa chỉ, SĐT liên hệ, Chức danh khoa học, Đơn vị công tác, Chức vụ đơn vị, Trạng thái công việc, Trạng thái hợp đồng) có phân trang.  3.  Phòng TCCB, phòng TCKT **nhập từ khóa** vào ô tìm kiếm (Tên, Mã, CCCD, Email, SĐT).  4.  Hệ thống hiển thị kết quả tìm kiếm theo từ khóa (real-time). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Từ khóa tìm kiếm rỗng**   1. Tại bước 3, nếu phòng TCCB, phòng TCKT không nhập từ khóa 2. Hệ thống hiển thị toàn bộ danh sách hồ sơ nhân sự Use case kết thúc.   **A2: Không có kết quả tìm kiếm**   1. Tại bước 4, nếu không có hồ sơ nào phù hợp với từ khóa 2. Hệ thống hiển thị thông báo: *"Không tìm thấy hồ sơ phù hợp."* Use case kết thúc. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

---

## 4.30. Use Case: Lọc danh sách hồ sơ nhân sự (FEAT 8.2)

|  |  |
| --- | --- |
| **Tên use case** | **Lọc danh sách hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT lọc danh sách hồ sơ nhân sự dựa trên nhiều tiêu chí nhằm thu hẹp phạm vi dữ liệu phục vụ công tác quản lý. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB, phòng TCKT chọn tiêu chí lọc trong menu "Quản lý hồ sơ nhân sự" |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách hồ sơ nhân sự được hiển thị đúng theo các tiêu chí lọc đã chọn |
| Điều kiện thất bại | Hệ thống không hiển thị yêu cầu lọc danh sách theo tiêu chí đã chọn do lỗi hệ thống |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB, phòng TCKT nhấn "Bộ lọc nâng cao".  2.  Hệ thống hiển thị panel lọc với nhiều tiêu chí:   * **Đơn vị công tác:** Chọn Khoa, Phòng, Ban, Bộ môn * **Chức danh khoa học:** GS, PGS, Không có * **Chức vụ đơn vị:**Trưởng khoa, Phó khoa, Không chức vụ * **Trạng thái làm việc:** Đang chờ xét,Đang công tác, Đã thôi việc * **Trạng thái hợp đồng:** Chưa hợp đồng, Còn hiệu lực, Hết hiệu lực, Chờ gia hạn. * **Giới tính:** Nam, Nữ   3.  Phòng TCCB, phòng TCKT chọn các tiêu chí lọc.  4.  Nhấn "Áp dụng bộ lọc".  5.  Hệ thống hiển thị kết quả lọc đa tiêu chí. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không có kết quả lọc**   1. Tại bước 5, nếu không có hồ sơ nào thỏa mãn tiêu chí đã chọn 2. Hệ thống hiển thị thông báo *"Không có hồ sơ phù hợp với tiêu chí lọc."* Use case kết thúc. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

---

## 4.31. Use Case: Thêm mới Hồ sơ nhân sự (FEAT 8.3)

|  |  |
| --- | --- |
| **Tên use case** | **Thêm mới Hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tạo mới và lưu trữ đầy đủ thông tin hồ sơ nhân sự trên hệ thống. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng thêm trong menu "Quản lý hồ sơ nhân sự" |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được tạo mới với Mã cán bộ tự động sinh, Trạng thái hợp đồng = "Chưa hợp đồng", Trạng thái làm việc = "Đang chờ xét". |
| Điều kiện thất bại | Hệ thống không thể tạo mới hồ sơ do lỗi hệ thống hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB nhấn "Thêm mới".  2.  Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3.  Phòng TCCB nhập các trường thông tin:   * **Thông tin chung bắt buộc**: Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ. * **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn "Người nước ngoài", hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động. * **Thông tin gia đình  (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình. * **Thông tin ngân hàng  (bắt buộc)**: Tên Ngân hàng, Số tài khoản. * **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**. * **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết. * **Upload ảnh chân dung  (bắt buộc).** * **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học. * **Thông tin các bằng cấp  (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf. * **Thông tin các chứng chỉ  (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf. * **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình).   4. Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5. Phòng TCCB nhấn "Lưu".  6. Hệ thống tự động sinh Mã cán bộ theo mẫu mã đang được cấu hình áp dụng tại thời điểm tạo hồ sơ và gán Trạng thái hợp đồng mặc định là "Chưa hợp đồng", Trạng thái làm việc là "Đang chờ xét".  7. Hệ thống lưu hồ sơ, lịch sử tạo hồ sơ và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Tạo mới hồ sơ nhân sự từ file Excel**  1. Tại bước 1 của Luồng sự kiện chính, Phòng TCCB chọn chức năng **"Thêm mới từ Excel"**.  2. Hệ thống hiển thị màn hình tải lên file Excel và cung cấp **file mẫu** theo định dạng quy định.  3. Phòng TCCB tải lên file Excel chứa danh sách hồ sơ nhân sự.  4. Hệ thống kiểm tra: Định dạng file, Cấu trúc cột dữ liệu, Các trường thông tin bắt buộc, và tính hợp lệ logic của dữ liệu từng dòng  5. Tiếp tục bước 5 của luồng chính |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**   1. Tại bước 4, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ. 2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ. Quay lại bước 3.   **E2: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn "Hủy". 2. Quay lại màn hình danh sách nhân sự. |

---

## 4.32. Use Case: Chỉnh sửa trong chi tiết hồ sơ nhân sự (FEAT 8.4)

|  |  |
| --- | --- |
| **Tên use case** | **Chỉnh sửa trong chi tiết hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB sửa và lưu lại đầy đủ thông tin hồ sơ nhân sự trên hệ thống nếu có thay đổi hoặc sai sót trong nhập liệu. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng sửa trong một nhân sự trong menu "Quản lý hồ sơ nhân sự" |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự có trạng thái làm việc "Đang chờ xét", "Đang công tác" |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được cập nhật.  Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Hồ sơ nhân sự không được cập nhật và thay đổi |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, Phòng TCCB nhấn "Sửa" một nhân sự tại danh sách.  2.  Hệ thống hiển thị form nhập liệu chia thành các tabs/bước.  3.  Phòng TCCB có thể sửa các trường thông tin:   * **Thông tin chung bắt buộc**: Mã cán bộ (không thể sửa), Họ tên, Ngày sinh, Giới tính, CCCD, Quê quán, Địa chỉ, Mã số thuế (Không bắt buộc), Số Bảo hiểm xã hội (Không bắt buộc), Số bảo hiểm y tế (Không bắt buộc), Email, SĐT liên hệ. * **[MỞ RỘNG - Nếu là người nước ngoài],** Cán bộ TCCB tick chọn "Người nước ngoài", hệ thống hiển thị thêm các trường bắt buộc: Số Visa, Ngày hết hạn Visa, Số Hộ chiếu, Ngày hết hạn Hộ chiếu, Số giấy phép lao động, Ngày hết hạn giấy phép lao động, Upload PDF giấy phép lao động. * **Thông tin gia đình  (bắt buộc)**: Cha/Mẹ, Vợ/chồng, con, người phụ thuộc, thông tin chi tiết về gia đình. * **Thông tin ngân hàng  (bắt buộc)**: Tên Ngân hàng, Số tài khoản. * **Quá trình công tác** trước khi về trường: Nơi công tác, thời gian công tác **(bắt buộc)**. * **Thông tin Đảng/Đoàn (bắt buộc):** Ngày vào Đoàn/Đảng, Thông tin chi tiết. * **Upload ảnh chân dung  (bắt buộc).** * **Trình độ học vấn (bắt buộc):** Trình độ văn hóa, Trình độ đào tạo, Chức danh nghề nghiệp, Chức danh khoa học. * **Thông tin các bằng cấp  (bắt buộc)**: Tên bằng, Trường, Ngành, Năm tốt nghiệp, Xếp loại, Bản pdf. * **Thông tin các chứng chỉ  (bắt buộc):** Tên chứng chỉ, Nơi cấp, Ngày cấp, Ngày hết hạn, Bản pdf. * **Lương & Phụ cấp (bắt buộc):** Hệ số lương (đã được cấu hình), Phụ cấp(đã được cấu hình). * *Lưu ý: Thông tin hợp đồng được quản lý qua UC 4.25–4.28. Thông tin đánh giá (khen thưởng/kỷ luật) được quản lý qua UC 4.40–4.42. Xem UC 4.37 (Cấu hình ẩn/hiện mục khen thưởng/kỷ luật) cho cấu hình hiển thị.*   4.  Hệ thống kiểm tra tính đầy đủ, hợp lệ và tính logic của các thông tin bắt buộc  5.  Phòng TCCB nhấn "Lưu".  6.  Hệ thống lưu và thông báo cập nhật thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ hoặc thiếu thông tin bắt buộc**   1. Tại bước 4, hệ thống phát hiện thiếu thông tin bắt buộc, định dạng dữ liệu sai hoặc các trường thời gian không hợp lệ. 2. Hệ thống hiển thị cảnh báo, đánh dấu các tab còn thiếu hoặc sai dữ liệu và không cho phép lưu hồ sơ. Quay lại bước 3.   **E2: Hủy thao tác**   1. Tại bước 3, Phòng TCCB chọn "Hủy". 2. Quay lại màn hình danh sách nhân sự.   **E3: Hồ sơ ở trạng thái "Đã thôi việc"**   1. Tại bước 1, hệ thống phát hiện hồ sơ nhân sự đang ở trạng thái làm việc "Đã thôi việc". 2. Hệ thống hiển thị thông báo: "Không thể chỉnh sửa hồ sơ nhân sự đã thôi việc." và vô hiệu hóa nút "Sửa". Use case kết thúc. |

---

## 4.33. Use Case: Đánh dấu thôi việc nhân sự (FEAT 8.5)

|  |  |
| --- | --- |
| **Tên use case** | **Đánh dấu thôi việc nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép phòng TCCB cập nhật trạng thái làm việc "Đã thôi việc" cho hồ sơ nhân sự |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng đánh dấu thôi việc trong một nhân sự trong menu "Quản lý hồ sơ nhân sự" |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. Nhân sự cần đánh dấu thôi việc đang ở trạng thái làm việc khác "Đã thôi việc". |
| Điều kiện thành công  (Post-condition) | Trạng thái của nhân sự được cập nhật thành "Đã thôi việc" trong hồ sơ nhân sự thành công.Trạng thái hợp đồng được cập nhật thành "Hết hiệu lực" (nếu nhân sự có hợp đồng ở trạng thái "Còn hiệu lực" hoặc "Chờ gia hạn"). Nhân sự được gỡ khỏi đơn vị công tác. Tài khoản liên kết được tự động khóa. |
| Điều kiện thất bại | Trạng thái làm việc "Đã thôi việc" không được cập nhật |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại màn hình danh sách, phòng TCCB chọn chức năng "Đánh dấu thôi việc" một nhân sự.  2.  Hệ thống yêu cầu xác nhận và nhập ngày, lý do thôi việc.  3.  Phòng TCCB xác nhận.  4.  Hệ thống cập nhật trạng thái làm việc thành "Đã thôi việc", trạng thái hợp đồng thành "Hết hiệu lực" (nếu có hợp đồng đang hiệu lực hoặc chờ gia hạn), nhân sự được cập nhật rời khỏi đơn vị công tác.  5. Hệ thống tự động khóa tài khoản liên kết của nhân sự (cập nhật trạng thái tài khoản thành 'Bị khóa'). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Thôi việc khi hợp đồng còn hiệu lực (thanh lý trước hạn)**   1. Tại bước 1, hệ thống phát hiện nhân sự có hợp đồng ở trạng thái "Còn hiệu lực". 2. Hệ thống hiển thị cảnh báo: "Nhân sự này vẫn còn hợp đồng đang có hiệu lực. Tiếp tục sẽ thanh lý hợp đồng trước hạn." 3. Hệ thống yêu cầu nhập lý do thanh lý hợp đồng trước hạn (ngoài ngày và lý do thôi việc ở bước 2 Basic Flow). 4. Phòng TCCB xác nhận. 5. Tiếp tục bước 4 của Basic Flow. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Nhân sự đã ở trạng thái "Đã thôi việc"**   1. Tại bước 1, hệ thống phát hiện nhân sự đã có trạng thái làm việc "Đã thôi việc". 2. Hệ thống vô hiệu hóa nút "Đánh dấu thôi việc" hoặc hiển thị cảnh báo: *"Nhân sự này đã được đánh dấu thôi việc trước đó."* Use case kết thúc.   **E2: Nhân sự chưa bãi nhiệm chức vụ**   1. Tại bước 1, hệ thống phát hiện nhân sự đang giữ chức vụ quản lý (Trưởng khoa, Trưởng bộ môn...). 2. Hệ thống chặn thao tác và thông báo: "Vui lòng bãi nhiệm chức vụ của nhân sự trước khi đánh dấu thôi việc." Use case kết thúc.   **E3: Hủy thao tác**   1. Tại bước 2, Phòng TCCB chọn "Hủy". 2. Hệ thống quay lại màn hình danh sách nhân sự. |

---

## 4.34. Use Case: Thôi việc nhân sự tự động (FEAT 8.6)

|  |  |
| --- | --- |
| **Tên use case** | **Thôi việc nhân sự tự động** |
| Tác nhân chính | Hệ thống |
| Mục đích (mô tả) | Hệ thống tự động chuyển trạng thái hợp đồng sang "Chờ gia hạn" khi sắp hết hạn, và tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn mà không được gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Hệ thống (System Timer) định kỳ kiểm tra trạng thái hợp đồng của nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Hệ thống đang hoạt động bình thường. Tồn tại hợp đồng lao động ở trạng thái "Chưa có hiệu lực", "Còn hiệu lực" hoặc "Chờ gia hạn". |
| Điều kiện thành công  (Post-condition) | Hợp đồng ở trạng thái "Chưa có hiệu lực" được chuyển sang "Còn hiệu lực" khi đến ngày hiệu lực. Hợp đồng sắp hết hạn được chuyển sang trạng thái "Chờ gia hạn". Hoặc: Hợp đồng đã quá hạn gia hạn được chuyển sang "Hết hiệu lực", nhân sự được đánh dấu "Đã thôi việc", gỡ khỏi đơn vị công tác và tài khoản liên kết bị khóa. |
| Điều kiện thất bại | Hệ thống không thể cập nhật trạng thái do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Hệ thống (System Timer) định kỳ kiểm tra các hợp đồng đang ở trạng thái "Chưa có hiệu lực" và "Còn hiệu lực". 2. Với các hợp đồng ở trạng thái "Chưa có hiệu lực": nếu Ngày hiệu lực ≤ Ngày hiện tại, hệ thống tự động chuyển trạng thái hợp đồng sang "Còn hiệu lực" và cập nhật trạng thái hợp đồng của nhân sự thành "Còn hiệu lực". 3. Với các hợp đồng ở trạng thái "Còn hiệu lực": nếu thời gian còn lại của hợp đồng ≤ thời gian chờ gia hạn được cấu hình của loại hợp đồng tương ứng (tham chiếu thuộc tính `thoiGianChoGiaHan` tại UC 4.20): 4. Hệ thống tự động cập nhật trạng thái hợp đồng từ "Còn hiệu lực" sang "Chờ gia hạn". 5. Hệ thống tự động cập nhật trạng thái hợp đồng của nhân sự thành "Chờ gia hạn". |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Tự động thôi việc khi hết hạn gia hạn**   1. Tại bước 1, khi hệ thống kiểm tra hợp đồng ở trạng thái "Chờ gia hạn" đã quá thời gian gia hạn được cấu hình và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng, hệ thống tự động cập nhật trạng thái hợp đồng thành "Hết hiệu lực". 2. Hệ thống tự động cập nhật trạng thái làm việc cho nhân sự vừa bị cập nhật trạng thái hợp đồng "Hết hiệu lực" thành "Đã thôi việc". 3. Hệ thống tự động gỡ nhân sự khỏi đơn vị công tác hiện tại. 4. Hệ thống tự động cập nhật trạng thái tài khoản liên kết thành "Bị khóa". |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

---

## 4.35. Use Case: Xem Chi tiết thông tin hồ sơ nhân sự (FEAT 8.7)

|  |  |
| --- | --- |
| **Tên use case** | **Xem Chi tiết thông tin hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT xem chi tiết toàn bộ thông tin hồ sơ nhân sự theo từng chế độ xem. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB, phòng TCKT chọn chức năng xem chi tiết trong một nhân sự trong menu "Quản lý hồ sơ nhân sự" |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB, phòng TCKT đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết hồ sơ nhân sự được hiển thị đầy đủ, chính xác ở chế độ chỉ đọc. |
| Điều kiện thất bại | Hệ thống không hiển thị được thông tin hồ sơ do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Tại danh sách, Phòng TCCB, phòng TCKT nhấn vào nhấn "Xem chi tiết" tại một nhân sự.  2.  Hệ thống hiển thị màn hình Chi tiết hồ sơ ở chế độ chỉ đọc.  3.  Hệ thống hiển thị đầy đủ thông tin theo các tab:   * **Tab "Thông tin chung":** Mã cán bộ,Lý lịch, liên hệ, gia đình, ảnh chân dung * **Tab "Trình độ & Chức danh":** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác. * **Tab "Thông tin Đảng/ Đoàn":** Thông tin Đảng/ Đoàn đã được lưu. * **Tab "Lương & Phụ cấp":** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng * **Tab "Hợp đồng":** Thông tin về các loại hợp đồng đồng đã ký * **Tab "Khen thưởng/Kỷ luật":** Hệ thống hiển thị mục khen thưởng/kỷ luật tùy theo cấu hình ẩn/hiện (xem UC 4.37, FEAT 8.9) và vai trò người dùng hiện tại * **Tab "Công tác":** Quá trình công tác trước khi về trường đã được ghi |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

---

## 4.36. Use Case: In và xuất Excel hồ sơ nhân sự (FEAT 8.8)

|  |  |
| --- | --- |
| **Tên use case** | **In và xuất Excel hồ sơ nhân sự** |
| Tác nhân chính | Phòng TCCB, Phòng TCKT |
| Mục đích (mô tả) | Cho phép phòng TCCB, phòng TCKT in hồ sơ nhân sự dưới định dạng PDF hoặc xuất toàn bộ thông tin hồ sơ ra file Excel để phục vụ lưu trữ, báo cáo và đối chiếu. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB hoặc phòng TCKT chọn chức năng "In hồ sơ" hoặc "Xuất Excel" tại màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB hoặc phòng TCKT đã đăng nhập hệ thống. Hồ sơ nhân sự đã tồn tại trong hệ thống. Người dùng đang ở màn hình chi tiết hồ sơ nhân sự (tham chiếu UC 4.35). |
| Điều kiện thành công  (Post-condition) | File PDF hoặc Excel chứa thông tin hồ sơ nhân sự được tạo và tải về thành công. Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Hệ thống không thể tạo file do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB hoặc phòng TCKT đang ở màn hình chi tiết hồ sơ nhân sự (từ UC 4.35). 2. Người dùng chọn chức năng **"In hồ sơ"**. 3. Hệ thống tạo bản xem trước hồ sơ ở định dạng PDF bao gồm toàn bộ thông tin hồ sơ nhân sự. 4. Người dùng xác nhận in hoặc tải về file PDF. 5. Hệ thống thực hiện in hoặc tải file PDF về máy người dùng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Xuất ra Excel**   1. Tại bước 2, người dùng chọn chức năng **"Xuất Excel"** thay vì "In hồ sơ". 2. Hệ thống tạo file Excel chứa tất cả thông tin hồ sơ nhân sự. 3. Hệ thống tải file Excel về máy người dùng. Use case kết thúc. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

---

## 4.37. Use Case: Cấu hình ẩn/hiện mục khen thưởng/kỷ luật (FEAT 8.9)

|  |  |
| --- | --- |
| **Tên use case** | **Cấu hình ẩn/hiện mục khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB cấu hình ở mức toàn hệ thống việc ẩn/hiện các mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự đối với các vai trò không thuộc Phòng TCCB, nhằm kiểm soát phạm vi hiển thị thông tin theo vai trò sử dụng. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng cấu hình hiển thị hồ sơ nhân sự trong menu cấu hình hệ thống. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống và có quyền cấu hình hệ thống. |
| Điều kiện thành công  (Post-condition) | Cấu hình ẩn/hiện mục **Khen thưởng/Kỷ luật** được lưu thành công và áp dụng ngay ở mức hệ thống cho các màn hình xem hồ sơ liên quan (tham chiếu UC 4.35 và UC 4.47).  Các vai trò được cấu hình là **"Ẩn"** sẽ không nhìn thấy mục **Khen thưởng/Kỷ luật** trong hồ sơ nhân sự.  Phòng TCCB luôn nhìn thấy đầy đủ các mục này bất kể cấu hình. |
| Điều kiện thất bại | Cấu hình không được cập nhật do lỗi hệ thống hoặc người dùng không lưu thay đổi. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **cấu hình hệ thống**.  2. Hệ thống hiển thị danh sách nhóm cấu hình.  3. Phòng TCCB chọn nhóm cấu hình **"Hiển thị hồ sơ nhân sự"**.  4. Hệ thống hiển thị các vai trò không thuộc Phòng TCCB (ví dụ: Phòng TCKT, Cán bộ/Giảng viên/Người dùng) cùng các tùy chọn ẩn/hiện đối với mục **Khen thưởng** và **Kỷ luật**.  5. Phòng TCCB bật/tắt cấu hình hiển thị cho từng vai trò.  6. Phòng TCCB nhấn **"Lưu"**.  7. Hệ thống lưu cấu hình, thông báo thành công và áp dụng ngay cho các màn hình xem hồ sơ nhân sự tương ứng. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không thay đổi cấu hình**   1. Tại bước 5, Phòng TCCB không thực hiện thay đổi nào và chọn **"Hủy"** hoặc thoát màn hình. 2. Hệ thống không cập nhật cấu hình và giữ nguyên thiết lập hiện tại. Use case kết thúc. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |
