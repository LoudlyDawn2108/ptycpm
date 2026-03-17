# Ngô Quang Tùng — Renumbered Contribution

## Part A: STRQs and FEATs (for Section II)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 9:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 9.1:** Hệ thống cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự. * **FEAT 9.2:** Hệ thống cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác. * **FEAT 9.3:** Hệ thống cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 10:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 10.1:** Hệ thống cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật). * **FEAT 10.2:** Hệ thống cho phép phòng TCCB xem lịch sử đánh giá khen thưởng và kỷ luật của nhân sự. * **FEAT 10.3:** Hệ thống cho phép phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo nhân sự, loại đánh giá, hoặc khoảng thời gian. |
| **STRQ 11:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 11.1:** Hệ thống cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ. * **FEAT 11.2:** Hệ thống cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành). * **FEAT 11.3:** Hệ thống cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký. * **FEAT 11.4:** Hệ thống cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
| **STRQ 12:** Người dùng phần mềm có thể xem hồ sơ cá nhân, xem thông tin đơn vị đang công tác và thực hiện các luồng tác vụ cá nhân. | * Phân tách * Làm rõ * Thêm chi tiết | * **FEAT 12.1:** Hệ thống cho phép người dùng xem thông tin cá nhân của bản thân. * **FEAT 12.2:** Hệ thống cho phép người dùng xem thông tin đơn vị mình đang công tác và cơ cấu các thành phần đơn vị trực thuộc. * **FEAT 12.3:** Hệ thống cho phép người dùng đăng ký hoặc hủy đăng ký tham gia khóa học/đào tạo được nhà trường phê duyệt mở. * **FEAT 12.4:** Hệ thống cho phép người dùng xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. |

> **Ghi chú thiết kế – FEAT 12.3/12.4:** "Luồng tác vụ cá nhân" trong STRQ 12 được giới hạn phạm vi ở đăng ký đào tạo trong phiên bản hiện tại. Các tác vụ cá nhân khác (ví dụ: yêu cầu cập nhật thông tin, đề xuất nghỉ phép) có thể được bổ sung trong các phiên bản sau nếu có yêu cầu từ stakeholder.

## Part B: UC Model Entries (for Section III)

- UC 4.36: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự
- UC 4.37: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự
- UC 4.38: Ghi nhận đánh giá cho nhân sự
- UC 4.39: Xem lịch sử đánh giá khen thưởng/kỷ luật
- UC 4.40: Tìm kiếm và lọc danh sách đánh giá
- UC 4.41: Mở khóa đào tạo cho cán bộ giảng viên
- UC 4.42: Sửa thông tin khóa đào tạo đã mở
- UC 4.43: Xem chi tiết thông tin khóa đào tạo đã mở
- UC 4.44: Ghi nhận kết quả đào tạo của cán bộ giảng viên
- UC 4.45: Xem các thông tin trong hồ sơ cá nhân của nhân sự
- UC 4.46: Xem thông tin chi tiết đơn vị đang công tác
- UC 4.47: Thay đổi trạng thái đăng ký khóa đào tạo
- UC 4.48: Xem danh sách các khóa đào tạo đã đăng ký

## Part C: FEAT→UC Traceability (for Section III)

| FEAT | UC tương ứng |
|------|-------------|
| FEAT 9.1 | UC 4.36 (Bổ nhiệm nhân sự vào đơn vị tổ chức nhân sự) |
| FEAT 9.2 | UC 4.36 (Điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác) |
| FEAT 9.3 | UC 4.37 (Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự) |
| FEAT 10.1 | UC 4.38 (Ghi nhận đánh giá cho nhân sự) |
| FEAT 10.2 | UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) |
| FEAT 10.3 | UC 4.40 (Tìm kiếm và lọc danh sách đánh giá) |
| FEAT 11.1 | UC 4.41 (Mở khóa đào tạo cho cán bộ giảng viên) |
| FEAT 11.2 | UC 4.42 (Sửa thông tin khóa đào tạo đã mở) |
| FEAT 11.3 | UC 4.43 (Xem chi tiết thông tin khóa đào tạo đã mở) |
| FEAT 11.4 | UC 4.44 (Ghi nhận kết quả đào tạo của cán bộ giảng viên) |
| FEAT 12.1 | UC 4.45 (Xem các thông tin trong hồ sơ cá nhân của nhân sự) |
| FEAT 12.2 | UC 4.46 (Xem thông tin chi tiết đơn vị đang công tác) |
| FEAT 12.3 | UC 4.47 (Thay đổi trạng thái đăng ký khóa đào tạo) |
| FEAT 12.4 | UC 4.48 (Xem danh sách các khóa đào tạo đã đăng ký) |

## Part D: UC Specifications (for Section IV)

### 4.36. Use Case: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB bổ nhiệm nhân sự vào các đơn vị tổ chức |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng bổ nhiệm trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức.  Nhân sự phải có trạng thái hợp đồng 'Còn hiệu lực' hoặc 'Chờ gia hạn' và trạng thái làm việc 'Đang chờ xét' hoặc 'Đang công tác'. |
| Điều kiện thành công  (Post-condition) | Nhân sự được bổ nhiệm nhân sự vào đơn vị.  Thông tin nhân sự của đơn vị được cập nhật. |
| Điều kiện thất bại | Việc bổ nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Phòng TCCB chọn bổ nhiệm nhân sự chưa công tác  3. Hệ thống hiển thị danh sách nhân sự ở trạng thái “Đang chờ xét” và trạng thái hợp đồng “Còn hiệu lực”.  4. Phòng TCCB chọn nhân sự và nhập thông tin như (Chức vụ, Ngày bắt đầu)  5. Hệ thống kiểm tra hợp lệ (Ngày bắt đầu).  6. Hệ thống thay đổi danh sách nhân sự, trạng thái công việc của nhân sự chuyển thành “Đang công tác ”và thông báo thành công. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Bổ nhiệm nhân sự đang công tác ở đơn vị khác**  1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Phòng TCCB chọn bổ nhiệm nhân sự đang công tác tại đơn vị khác.  3. Hệ thống yêu cầu chọn đơn vị, chọn nhân sự từ đơn vị được chọn.  4. Phòng TCCB chọn nhân sự và nhập thông tin như (Chức vụ, Ngày bắt đầu)  5. Hệ thống kiểm tra hợp lệ (Ngày bắt đầu).  6. Hệ thống gỡ nhân sự khỏi đơn vị cũ, thêm vào đơn vị mới, cập nhật danh sách nhân sự của cả hai đơn vị và thông báo thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu không hợp lệ**   1. Tại bước 5, Hệ thống kiểm tra phát hiện:  * Ngày bắt đầu < ngày hiện tại  2. Hệ thống yêu cầu nhập lại và không lưu dữ liệu.   **E2: Không được phép tiếp tục**   1. Tại bước 1, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục cập nhật bổ nhiệm. |

### 4.37. Use Case: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thực hiện bãi nhiệm nhân sự trong đơn vị tổ chức, nhằm cập nhật chính xác tình trạng nhân sự và phục vụ công tác quản lý nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng bãi nhiệm nhân sự của đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức. |
| Điều kiện thành công  (Post-condition) | Nhân sự được miễn nhiệm khỏi chức vụ. Trạng thái công việc của nhân sự được cập nhật thành “Đang chờ xét”. Nhân sự được xóa khỏi danh sách của đơn vị tổ chức. |
| Điều kiện thất bại | Việc bãi nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức.  2. Hệ thống hiển thị danh sách nhân sự  3. Phòng TCCB chọn chức năng bãi nhiệm từ trong một nhân sự trong danh sách.  4. Hệ thống yêu cầu xác nhận thao tác.  5. Phòng TCCB xác nhận thao tác miễn nhiệm. 6. Hệ thống cập nhật trạng thái công việc của nhân sự là “Đang chờ xét”  và xóa nhân sự khỏi danh sách của đơn vị tổ chức. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Không được phép tiếp tục**   1. Tại bước 3, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. 2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục thực hiện bãi nhiệm. |

### 4.38. Use Case: Ghi nhận đánh giá cho nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận đánh giá cho nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Ghi nhận các quyết định đánh giá đối với nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Thêm đánh giá khen thưởng hoặc kỷ luật” |
| Điều kiện tiên quyết  (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã được tạo Nhân sự không ở trạng thái làm việc 'Đã thôi việc'. |
| Điều kiện thành công  (Post-condition) | Hồ sơ nhân sự được cập nhật.  Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Dữ liệu đánh giá không được ghi nhận vào hệ thống do thiếu các trường thông tin bắt buộc, hoặc do lỗi kết nối cơ sở dữ liệu/phiên đăng nhập hết hạn |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn tab " Thêm đánh giá khen thưởng hoặc kỷ luật".  2. Hệ thống yêu cầu nhập mã nhân sự và chọn loại đánh giá  3. Phòng TCCB nhập mã nhân sự và chọn loại đánh giá (Khen thưởng/ Kỷ luật)  4.  Hệ thống hiển thị giao diện nhập liệu:   * Nếu chọn loại đánh giá là khen thưởng: `Loại khen thưởng`, ‘Tên khen thưởng’, `Ngày quyết định`, `Số quyết định`, `Nội dung`, `Số tiền thưởng` (nếu có). * Nếu chọn loại đánh giá là kỷ luật: `Loại kỷ luật`, ‘Tên kỷ luật’,  `Ngày quyết định`, `Lý do`, `Hình thức xử lý`.   5.  Nhấn "Lưu".  6. Hệ thống kiểm tra dữ liệu hợp lệ (Đầy đủ các trường thông tin)  7. Hệ thống lưu dữ liệu và đẩy vào hồ sơ cá nhân và thông báo thành công. *Lưu ý: Xem UC 4.39 (Xem lịch sử đánh giá khen thưởng/kỷ luật) và UC 4.40 (Tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật) cho các tác vụ tra cứu liên quan.* |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Mã nhân sự không hợp lệ**   1. Tại bước 3, Hệ thống phát hiện mã nhân sự không tồn tại. 2. Hệ thống từ chối tiếp tục tạo bản đánh giá.   **E2: Dữ liệu không hợp lệ**   1. Tại bước 6, Hệ thống phát hiện dữ liệu không đầy đủ các trường thông tin. 2. Hệ thống từ chối lưu thông tin và thông báo lỗi.   **E3: Hủy thao tác**  1. Tại bước 2, Phòng TCCB chọn “Hủy”.  2. Quay lại màn hình danh sách nhân sự. **E4: Nhân sự đã thôi việc**   1. Tại bước 3, hệ thống phát hiện nhân sự đang ở trạng thái làm việc “Đã thôi việc”. 2. Hệ thống từ chối ghi nhận đánh giá và hiển thị thông báo: “Không thể ghi nhận đánh giá cho nhân sự đã thôi việc.” |

### 4.39. Use Case: Xem lịch sử đánh giá khen thưởng/kỷ luật (FEAT 10.2)

|  |  |
| --- | --- |
| **Tên use case** | **Xem lịch sử đánh giá khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem lịch sử toàn bộ các bản ghi đánh giá khen thưởng và kỷ luật của một nhân sự theo trình tự thời gian, phục vụ tra cứu, đối chiếu và theo dõi hồ sơ đánh giá của nhân sự. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn tab “Khen thưởng/Kỷ luật” trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Lịch sử đánh giá khen thưởng/kỷ luật của nhân sự được hiển thị đầy đủ, chính xác.  Không làm thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không thể hiển thị lịch sử đánh giá do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập màn hình **chi tiết hồ sơ nhân sự** của một nhân sự (tham chiếu UC 4.34).  2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc.  3. Phòng TCCB chọn tab **“Khen thưởng/Kỷ luật”**.  4. Hệ thống hiển thị danh sách toàn bộ bản ghi đánh giá của nhân sự theo thứ tự thời gian, bao gồm các thông tin: Ngày quyết định, Loại đánh giá (Khen thưởng/Kỷ luật), Tên đánh giá, Số quyết định, Mô tả ngắn/Nội dung.  5. Phòng TCCB chọn một bản ghi đánh giá trong danh sách.  6. Hệ thống hiển thị chi tiết bản ghi đã chọn, bao gồm đầy đủ thông tin đã được ghi nhận từ UC 4.38. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Nhân sự chưa có lịch sử đánh giá**   1. Tại bước 3, nếu hồ sơ nhân sự chưa có bản ghi khen thưởng hoặc kỷ luật nào. 2. Hệ thống hiển thị tab **“Khen thưởng/Kỷ luật”** ở trạng thái trống và thông báo: *“Nhân sự chưa có lịch sử đánh giá khen thưởng/kỷ luật.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.40. Use Case: Tìm kiếm và lọc danh sách đánh giá (FEAT 10.3)

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm và lọc danh sách đánh giá** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tìm kiếm và lọc danh sách các bản ghi khen thưởng/kỷ luật theo nhân sự, loại đánh giá hoặc khoảng thời gian nhằm phục vụ công tác tra cứu, thống kê và đối chiếu dữ liệu đánh giá. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB truy cập chức năng quản lý đánh giá khen thưởng/kỷ luật. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Danh sách các bản ghi đánh giá phù hợp với điều kiện tìm kiếm/lọc được hiển thị đầy đủ, chính xác.  Phòng TCCB có thể tiếp tục xem chi tiết từng bản ghi. |
| Điều kiện thất bại | Hệ thống không thể xử lý yêu cầu tìm kiếm/lọc do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập chức năng **quản lý đánh giá khen thưởng/kỷ luật**.  2. Hệ thống hiển thị danh sách các bản ghi đánh giá và vùng bộ lọc tìm kiếm.  3. Phòng TCCB nhập từ khóa tìm kiếm và/hoặc chọn các tiêu chí lọc, bao gồm: Nhân sự (Mã cán bộ/Họ tên), Loại đánh giá (Khen thưởng/Kỷ luật), Khoảng thời gian (Từ ngày – Đến ngày).  4. Phòng TCCB nhấn **“Tìm kiếm”** hoặc **“Áp dụng bộ lọc”**.  5. Hệ thống hiển thị danh sách kết quả phù hợp với tiêu chí đã chọn, bao gồm các thông tin: Mã cán bộ, Họ tên, Loại đánh giá, Tên đánh giá, Ngày quyết định, Số quyết định.  6. Phòng TCCB có thể chọn một bản ghi bất kỳ trong danh sách kết quả.  7. Hệ thống hiển thị chi tiết bản ghi đánh giá đã chọn (tham chiếu UC 4.39). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Không có kết quả phù hợp**   1. Tại bước 5, nếu không có bản ghi nào phù hợp với tiêu chí tìm kiếm/lọc. 2. Hệ thống hiển thị thông báo: *“Không tìm thấy đánh giá phù hợp với tiêu chí tìm kiếm.”* |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.41. Use Case: Mở khóa đào tạo cho cán bộ giảng viên (Ngô Quang Tùng)

|  |  |
| --- | --- |
| **Tên use case** | **Mở khóa đào tạo cho cán bộ giảng viên** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Cán bộ TCCB tạo mới và thiết lập thông tin một khóa đào tạo dành cho cán bộ, giảng viên; cấu hình hình thức đào tạo, thời gian, kinh phí và điều kiện đăng ký, làm cơ sở cho việc đăng ký tham gia và quản lý đào tạo sau này. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng mở khóa học trong menu “Đào tạo & Phát triển” |
| Điều kiện tiên quyết  (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công  (Post-condition) | Khóa đào tạo được tạo mới và lưu thành công.  Trạng thái khóa đào tạo được thiết lập theo cấu hình. |
| Điều kiện thất bại | Khóa đào tạo không được tạo do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1.  Phòng TCCB chọn menu "Đào tạo & Phát triển".  2.  Phòng TCCB nhấn "Tạo khóa đào tạo mới".  3. Hệ thống hiển thị thông tin nhập  4.  Phòng TCCB nhập thông tin: Tên khóa đào tạo, Loại khóa đào tạo (theo cấu hình), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo (Tên chứng chỉ, Loại chứng chỉ).  5.  Phòng TCCB thiết lập thời gian mở đăng ký từ ngày - đến ngày, Giới hạn số người tham gia.  6. Phòng TCCB nhấn “Lưu”.  7. Hệ thống kiểm tra dữ liệu hợp lệ.  8. Hệ thống yêu cầu xác nhận tạo khóa đào tạo.  9. Phòng TCCB xác nhận.  10. Hệ thống lưu khóa đào tạo và thiết lập trạng thái ban đầu là “Đang mở đăng ký" |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu các trường bắt buộc (Tên khóa, Loại khóa, Thời gian), thời gian mở đăng ký kết thúc sau ngày bắt đầu đào tạo. 2. Hệ thống hiển thị cảnh báo và yêu cầu chỉnh sửa.   **E2: Hủy thao tác**   1. Tại bước 4, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.42. Use Case: Sửa thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa các thông tin của khóa đào tạo đã được tạo nhằm cập nhật kế hoạch đào tạo phù hợp với thực tế, đồng thời đảm bảo không vi phạm các ràng buộc nghiệp vụ đối với khóa đào tạo đã mở đăng ký hoặc đã có người tham gia |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Sửa thông tin khóa đào tạo” tại một khóa đào tạo trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Khóa đào tạo đã tồn tại trong hệ thống.  Khóa đào tạo đang ở trạng thái "Đang mở đăng ký" hoặc "Đang đào tạo". |
| Điều kiện thành công  (Post-condition) | Thông tin khóa đào tạo được cập nhật thành công. Các thay đổi được ghi nhận và áp dụng ngay cho khóa đào tạo. |
| Điều kiện thất bại | Thông tin khóa đào tạo không được cập nhật do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB chọn menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo. 3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Sửa thông tin”**.  4. Hệ thống hiển thị màn hình chỉnh sửa thông tin khóa đào tạo.  5. Phòng TCCB chỉnh sửa các thông tin cho phép:   * Tên khóa đào tạo * Địa điểm * Kinh phí (nếu có) * Cam kết sau đào tạo (nếu có) * Thông tin chứng chỉ sau đào tạo * Trạng thái khóa đào tạo * Thời gian mở đăng ký và giới hạn số người tham gia (nếu được phép)   6. Phòng TCCB nhấn **“Lưu”**. 7. Hệ thống kiểm tra tính hợp lệ và ràng buộc nghiệp vụ (bao gồm kiểm tra chuyển trạng thái khóa đào tạo phải tuân theo thứ tự: Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước).  8. Hệ thống yêu cầu xác nhận cập nhật.  9. Phòng TCCB xác nhận.  10. Hệ thống cập nhật thông tin khóa đào tạo và thông báo thành công.  *Lưu ý: Khi trạng thái khóa đào tạo được chuyển sang "Đang đào tạo", hệ thống tự động batch-update tất cả đăng ký tham gia có trạng thái "Đã đăng ký" sang "Đang học".* |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Chỉnh sửa khi khóa đào tạo đang diễn ra**   1. Tại bước 4, nếu khóa đào tạo ở trạng thái "Đang đào tạo", hệ thống chỉ cho phép chỉnh sửa: Địa điểm, Kinh phí, Cam kết sau đào tạo, Thông tin chứng chỉ sau đào tạo. 2. Hệ thống khóa không cho phép chỉnh sửa: Tên khóa đào tạo, Loại khóa đào tạo, Thời gian mở đăng ký, Giới hạn số người tham gia. 3. Tiếp tục từ bước 6. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Chuyển trạng thái không hợp lệ**   1. Tại bước 7, hệ thống phát hiện trạng thái mới được chọn vi phạm thứ tự chuyển đổi (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước). 2. Hệ thống hiển thị thông báo: *"Chuyển trạng thái không hợp lệ."* và yêu cầu chọn lại.   **E2: Vi phạm ràng buộc đăng ký**   1. Tại bước 7, hệ thống phát hiện nếu: Giảm giới hạn số người tham gia nhỏ hơn số lượng đã đăng ký. 2. Hệ thống hiển thị cảnh báo và không cho phép lưu.   **E3: Dữ liệu không hợp lệ**   1. Tại bước 7, hệ thống phát hiện thiếu trường bắt buộc hoặc thời gian không hợp lệ. 2. Hệ thống yêu cầu chỉnh sửa lại thông tin.   **E4: Hủy thao tác**   1. Tại bước 5, Phòng TCCB chọn “Hủy”. 2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.43. Use Case: Xem chi tiết thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem đầy đủ thông tin chi tiết của một khóa đào tạo đã được tạo, bao gồm trạng thái khóa học, thông tin tổ chức đào tạo, danh sách cán bộ – giảng viên đăng ký tham gia, và tình trạng tham gia của từng nhân sự, nhằm phục vụ công tác quản lý, theo dõi và ra quyết định điều chỉnh khóa đào tạo khi cần thiết. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn một khóa đào tạo và nhấn chức năng “Xem chi tiết” trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Khóa đào tạo đã tồn tại trong hệ thống. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết của khóa đào tạo được hiển thị đầy đủ và chính xác.  Phòng TCCB có thể theo dõi tình trạng khóa học và danh sách nhân sự tham gia. |
| Điều kiện thất bại | Không thể hiển thị thông tin khóa đào tạo do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2. Hệ thống hiển thị danh sách các khóa đào tạo.  3. Phòng TCCB chọn một khóa đào tạo và nhấn **“Xem chi tiết”**.  4. Hệ thống hiển thị màn hình chi tiết khóa đào tạo, hiển thị đầy đủ thông tin theo yêu cầu bao gồm các thông tin:   * **Thông tin chung khóa đào tạo**: Tên khóa đào tạo, Loại khóa đào tạo, Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo. * **Thông tin đăng ký**: Thời gian mở đăng ký, Giới hạn số lượng người tham gia, Số lượng đã đăng ký / số lượng tối đa * **Danh sách tham gia**: Hệ thống hiển thị danh sách cán bộ, giảng viên đã đăng ký khóa đào tạo, bao gồm (Họ và tên, Mã cán bộ, Đơn vị đang công tác, Thời điểm đăng ký, Trạng thái tham gia |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.44. Use Case: Ghi nhận kết quả đào tạo của cán bộ giảng viên

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận kết quả đào tạo của cán bộ giảng viên** |
| Tác nhân chính | Cán bộ TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB ghi nhận kết quả tham gia khóa đào tạo của cán bộ, giảng viên sau khi khóa học kết thúc; cập nhật trạng thái hoàn thành, không đạt và lưu trữ chứng chỉ đào tạo vào hồ sơ nhân sự nhằm phục vụ công tác quản lý và đánh giá năng lực. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Phòng TCCB chọn chức năng “Ghi nhận kết quả đào tạo” tại tab “Danh sách học viên” của một khóa đào tạo. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống.  Khóa đào tạo đã tồn tại trong hệ thống.  Trạng thái khóa đào tạo là “Đã hoàn thành”.  Khóa đào tạo có danh sách học viên đã đăng ký. |
| Điều kiện thành công  (Post-condition) | Kết quả đào tạo của từng học viên được ghi nhận thành công.  Trạng thái tham gia của học viên được cập nhật (Hoàn thành / Không đạt).  Chứng chỉ đào tạo (nếu có) được lưu vào hồ sơ cá nhân của nhân sự.  Lịch sử đào tạo của nhân sự được cập nhật. |
| Điều kiện thất bại | Kết quả đào tạo không được ghi nhận do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Phòng TCCB truy cập menu **“Đào tạo & Phát triển”**.  2 Chọn xem chi tiết “Danh sách học viên” có một khóa đào tạo có trạng thái “Đã hoàn thành”.  3. Hệ thống hiển thị danh sách học viên tham gia khóa đào tạo, bao gồm: Họ tên, Mã cán bộ, Đơn vị công tác, Trạng thái tham gia hiện tại (Đang học)  4. Phòng TCCB chọn một học viên và nhấn **“Ghi nhận kết quả”**.  5. Hệ thống hiển thị form ghi nhận kết quả, bao gồm: Trạng thái kết quả: Hoàn thành/ Không đạt,Ngày hoàn thành (mặc định là ngày kết thúc khóa học), File chứng chỉ (PDF) (tùy chọn, bắt buộc nếu trạng thái là “Hoàn thành”) 6. Phòng TCCB nhập thông tin và nhấn **“Lưu”**. 7. Hệ thống kiểm tra tính hợp lệ của dữ liệu.  8. Hệ thống cập nhật trạng thái học viên:   * Nếu **Hoàn thành** (Ghi nhận kết quả đào tạo, Lưu chứng chỉ vào hồ sơ nhân sự). * Nếu **Không đạt** (Chỉ lưu trạng thái kết quả, không cập nhật chứng chỉ, Hệ thống thông báo ghi nhận kết quả thành công). |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Ghi nhận kết quả cho nhiều học viên**   1. Tại bước 4, Phòng TCCB có thể chọn nhiều học viên. 2. Hệ thống cho phép ghi nhận kết quả hàng loạt với cùng trạng thái. 3. Tiếp tục bước 5 |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Khóa đào tạo chưa hoàn thành**   1. Tại bước 4, nếu trạng thái khóa đào tạo khác “Đã hoàn thành”. 2. Hệ thống hiển thị thông báo: *“Chỉ có thể ghi nhận kết quả khi khóa đào tạo đã hoàn thành.”*   **E2: Thiếu chứng chỉ khi hoàn thành, Dữ liệu không hợp lệ**   1. Tại bước 8, Hệ thống phát hiện thiếu thông tin bắt buộc hoặc file không đúng định dạng hoặc nếu học viên được đánh dấu “Hoàn thành” nhưng không upload file chứng chỉ (trong trường hợp bắt buộc). 2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. |

### 4.45. Use Case: Xem các thông tin trong hồ sơ cá nhân của nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem các thông tin trong hồ sơ cá nhân của nhân sự** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép CBGV xem toàn bộ thông tin hồ sơ cá nhân của mình đang được lưu trong hệ thống, tra cứu lịch sử hợp đồng, hệ số, bậc lương, các quyết định khen thưởng và kỷ luật của bản thân.. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | CB/GV chọn chức năng “Hồ sơ cá nhân” trên giao diện hệ thống |
| Điều kiện tiên quyết  (Precondition) | CB/GV đã đăng nhập. |
| Điều kiện thành công  (Post-condition) | Thông tin hồ sơ cá nhân được hiển thị đầy đủ cho CBGV. |
| Điều kiện thất bại | Không thể hiển thị thông tin hồ sơ cá nhân do lỗi hệ thống. |
| Luồng sự kiện chính  (Basic Flow) | 1.  CB/GV chọn các mục kích hoạt chức năng xem hồ sơ nhân sự  2.  Hệ thống hiển thị đầy đủ thông tin theo các tab:   * **Tab "Thông tin chung":** Mã cán bộ,Lý lịch, liên hệ, gia đình, ảnh chân dung * **Tab "Trình độ & Chức danh":** Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác. * **Tab "Thông tin Đảng/ Đoàn":** Thông tin Đảng/ Đoàn đã được lưu. * **Tab "Lương & Phụ cấp":** Thông tin về ngạch, bậc, hệ số lương, thông tin ngân hàng * **Tab "Hợp đồng":** Thông tin về các loại hợp đồng đã ký * **Tab "Khen thưởng/Kỷ luật":** Mục khen thưởng/kỷ luật chỉ hiển thị nếu phòng TCCB đã cấu hình cho phép (xem UC 4.35, FEAT 8.9) * **Tab "Công tác":** Quá trình công tác |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.46. Use Case: Xem thông tin chi tiết đơn vị đang công tác

|  |  |
| --- | --- |
| **Tên use case** | **Xem thông tin chi tiết đơn vị đang công tác** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên xem thông tin chi tiết về đơn vị tổ chức mà mình đang công tác trong cơ cấu tổ chức của đơn vị, bao gồm thông tin cơ bản của đơn vị, danh sách chức vụ và nhân sự hiện tại trong đơn vị. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Cán bộ/Giảng viên chọn chức năng xem thông tin đơn vị công tác từ hồ sơ cá nhân hoặc menu liên quan. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống.  Cán bộ/Giảng viên đã được gán đơn vị công tác trong hệ thống.  Đơn vị tổ chức đang tồn tại trong cơ cấu tổ chức. |
| Điều kiện thành công  (Post-condition) | Thông tin chi tiết của đơn vị công tác được hiển thị đầy đủ và chính xác.  Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin do lỗi hệ thống hoặc không xác định được đơn vị công tác của CBGV. |
| Luồng sự kiện chính  (Basic Flow) | 1. Cán bộ/Giảng viên truy cập chức năng xem thông tin đơn vị công tác. 2. Hệ thống xác định đơn vị mà Cán bộ/Giảng viên đang trực thuộc.  3. Hệ thống hiển thị thông tin chi tiết của đơn vị, bao gồm:   * Tab **“Tổng quan”**, bao gồm: Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị (Đang hoạt động / Sáp nhập / Giải thể) * Tab **“Nhân sự”**: Hệ thống hiển thị danh sách các nhân sự, Tên chức vụ, hệ thống hiển thị: Họ tên nhân sự, Mã cán bộ, Ngày bắt đầu. Hệ thống hiển thị danh sách nhân sự thuộc đơn vị * Tab **“Đơn vị trực thuộc”**: Hệ thống hiển thị danh sách các đơn vị dưới cấp trực thuộc đơn vị đang xem. |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

### 4.47. Use Case: Thay đổi trạng thái đăng ký khóa đào tạo

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái đăng ký khóa đào tạo** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên đăng ký hoặc hủy đăng ký tham gia các khóa đào tạo do nhà trường tổ chức đang trong thời gian mở đăng ký, làm cơ sở cho việc quản lý học viên, theo dõi quá trình và ghi nhận kết quả đào tạo. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Cán bộ/Giảng viên chọn menu “Đào tạo”. |
| Điều kiện tiên quyết  (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống.  Khóa đào tạo tồn tại và đang ở trạng thái **“Đang mở đăng ký”**.  Thời điểm hiện tại nằm trong khoảng **Thời gian mở đăng ký**. |
| Điều kiện thành công  (Post-condition) | Đăng ký tham gia khóa đào tạo của CBGV được ghi nhận trong hệ thống (trường hợp đăng ký). Bản ghi đăng ký của CBGV được xóa khỏi hệ thống (trường hợp hủy đăng ký). |
| Điều kiện thất bại | Không thể thay đổi trạng thái đăng ký do khóa đào tạo không hợp lệ, hết hạn đăng ký hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính  (Basic Flow) | 1. Cán bộ/Giảng viên truy cập menu “Đào tạo”.  2. Hệ thống hiển thị danh sách các khóa đào tạo ở trạng thái Đang mở đăng ký.  3. Cán bộ/Giảng viên chọn một khóa đào tạo để xem chi tiết thông tin.  4. Hệ thống hiển thị thông tin chi tiết khóa đào tạo. Nếu CBGV chưa đăng ký, hiển thị nút “Đăng ký tham gia”. Nếu CBGV đã đăng ký (trạng thái tham gia là “Đã đăng ký”), hiển thị nút “Hủy đăng ký”.  5. Cán bộ/Giảng viên nhấn nút “Đăng ký tham gia”.  6. Hệ thống kiểm tra các điều kiện đăng ký (thời gian mở đăng ký, số lượng đăng ký chưa đạt giới hạn, trạng thái khóa đào tạo).  7. Hệ thống tạo bản ghi đăng ký đào tạo và thiết lập trạng thái tham gia là “Đã đăng ký”.  8. Hệ thống thông báo đăng ký thành công cho Cán bộ/Giảng viên. |
| Luồng sự kiện thay thế  (Alternative Flow) | **A1: Hủy đăng ký khóa đào tạo**   1. Tại bước 4, CBGV đã đăng ký khóa đào tạo này với trạng thái tham gia “Đã đăng ký”. Hệ thống hiển thị nút “Hủy đăng ký”. 2. Cán bộ/Giảng viên nhấn nút “Hủy đăng ký”. 3. Hệ thống yêu cầu xác nhận hủy đăng ký. 4. Cán bộ/Giảng viên xác nhận. 5. Hệ thống kiểm tra trạng thái tham gia phải là “Đã đăng ký” và khóa đào tạo phải đang ở trạng thái “Đang mở đăng ký”. 6. Hệ thống xóa bản ghi đăng ký đào tạo của CBGV. 7. Hệ thống thông báo hủy đăng ký thành công. |
| Luồng sự kiện ngoại lệ  (Exception Flow) | **E1: Hết thời gian đăng ký**   1. Tại bước 4, nếu thời gian hiện tại nằm ngoài khoảng mở đăng ký. 2. Hệ thống ẩn nút “Đăng ký tham gia” và “Hủy đăng ký”, hiển thị thông báo: *“Khóa đào tạo đã hết thời gian đăng ký.”*   **E2: Đã đủ số lượng người tham gia**   1. Tại bước 6, nếu số lượng đăng ký đã đạt giới hạn. 2. Hệ thống hiển thị thông báo: *“Khóa đào tạo đã đủ số lượng đăng ký.”*   **E3: Không thể hủy đăng ký**   1. Tại bước A1.5, nếu trạng thái tham gia không phải “Đã đăng ký” (ví dụ: đã chuyển sang “Đang học” do khóa đào tạo đã bắt đầu) hoặc khóa đào tạo không còn ở trạng thái “Đang mở đăng ký”. 2. Hệ thống hiển thị thông báo: *“Không thể hủy đăng ký do khóa đào tạo đã chuyển sang giai đoạn tiếp theo.”* |

### 4.48. Use Case: Xem danh sách các khóa đào tạo đã đăng ký

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách các khóa đào tạo đã đăng ký** |
| Tác nhân chính | Cán bộ/Giảng viên (CBGV) |
| Mục đích (mô tả) | Cho phép Cán bộ/Giảng viên xem danh sách tất cả các khóa đào tạo mà mình đã đăng ký tham gia, theo dõi trạng thái tham gia và kết quả đào tạo của từng khóa (Đang học, Hoàn thành, Không đạt), phục vụ việc tra cứu, theo dõi quá trình học tập và kết quả đào tạo cá nhân. |
| Mức độ ưu tiên  (Priority) | Bắt buộc |
| Điều kiện kích hoạt  (Trigger) | Chọn menu "Đào tạo" |
| Điều kiện tiên quyết  (Precondition) | Cán bộ/Giảng viên đã đăng nhập hệ thống.  Cán bộ/Giảng viên đã từng đăng ký ít nhất một khóa đào tạo |
| Điều kiện thành công  (Post-condition) | Danh sách các khóa đào tạo đã đăng ký của Cán bộ/Giảng viên được hiển thị đầy đủ và chính xác.  Trạng thái tham gia và kết quả đào tạo của từng khóa được hiển thị đúng theo dữ liệu do Phòng TCCB ghi nhận. |
| Điều kiện thất bại | Không hiển thị được danh sách do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính  (Basic Flow) | 1. Cán bộ/Giảng viên truy cập chức năng **“Khóa đào tạo đã đăng ký”**.  2. Hệ thống truy xuất danh sách các khóa đào tạo mà Cán bộ/Giảng viên đã đăng ký.  3. Hệ thống hiển thị danh sách khóa đào tạo, bao gồm các thông tin:   * Tên khóa đào tạo, * Loại khóa đào tạo, * Thời gian đào tạo (từ ngày – đến ngày), * Đơn vị/địa điểm tổ chức, * Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), * Trạng thái tham gia của cá nhân (Đã đăng ký, Đang học, Hoàn thành, Không đạt). |
| Luồng sự kiện thay thế  (Alternative Flow) | Không có |
| Luồng sự kiện ngoại lệ  (Exception Flow) | Không có |

## Part E: FEAT-specific SUPLs

### 2.1. Functionality – Yêu cầu chức năng bổ sung (không thuộc UC)

| Mã | Yêu cầu | Mô tả chi tiết | Ưu tiên |
|----|----------|-----------------|---------|
| **SUPL-F06** | Tự động cập nhật trạng thái tham gia đào tạo | Khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang trạng thái "Đang đào tạo", hệ thống tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang trạng thái "Đang học". | **M** |

### 3.1. Functionality — Yêu cầu chức năng bổ sung

| Mã | Yếu tố chất lượng | Độ đo (Metric) | Tiêu chuẩn đáp ứng (Acceptance Criteria) |
|----|-------------------|----------------|------------------------------------------|
| **SUPL-F06** | Correctness (Tính đúng đắn) – Tự động hóa | Tỷ lệ bản ghi đăng ký được cập nhật đúng khi khóa đào tạo chuyển trạng thái | 100% bản ghi đăng ký thuộc khóa đào tạo đó được chuyển từ trạng thái "Đã đăng ký" sang "Đang học" trong ≤ 1 phút kể từ khi khóa đào tạo chuyển sang trạng thái "Đang đào tạo". |

### 4. Ma trận truy vết NFR → FEAT/UC

| Nhóm NFR | Mã SUPL | FEAT/UC liên quan | Tác nhân ảnh hưởng |
|----------|---------|--------------------|--------------------|
| **Functionality (bổ sung)** | SUPL-F06 | FEAT 11.2, UC 4.42 | System Timer, TCCB |
