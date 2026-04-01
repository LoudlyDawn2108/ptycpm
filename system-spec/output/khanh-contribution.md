# Ngô Đức Nam Khánh — Nội dung đóng góp đã đánh số lại

## Part A: STRQs and FEATs (for Section II)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 9:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 9.1:** Hệ thống cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự. * **FEAT 9.2:** Hệ thống cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác. * **FEAT 9.3:** Hệ thống cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 10:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 10.1:** Hệ thống cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật). * **FEAT 10.2:** Hệ thống cho phép phòng TCCB xem lịch sử đánh giá khen thưởng và kỷ luật của nhân sự. * **FEAT 10.3:** Hệ thống cho phép phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo nhân sự, loại đánh giá, hoặc khoảng thời gian. |
| **STRQ 11:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 11.1:** Hệ thống cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ. * **FEAT 11.2:** Hệ thống cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành); khi khóa đào tạo được chuyển sang trạng thái "Đang đào tạo", hệ thống phải tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang "Đang học". * **FEAT 11.3:** Hệ thống cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký. * **FEAT 11.4:** Hệ thống cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
| **STRQ 12:** Người dùng phần mềm có thể xem hồ sơ cá nhân, xem thông tin đơn vị đang công tác và thực hiện các luồng tác vụ cá nhân. | * Phân tách * Làm rõ * Thêm chi tiết | * **FEAT 12.1:** Hệ thống cho phép người dùng xem thông tin cá nhân của bản thân. * **FEAT 12.2:** Hệ thống cho phép người dùng xem thông tin đơn vị mình đang công tác và cơ cấu các thành phần đơn vị trực thuộc. * **FEAT 12.3:** Hệ thống cho phép người dùng đăng ký hoặc hủy đăng ký tham gia khóa học/đào tạo được nhà trường phê duyệt mở. * **FEAT 12.4:** Hệ thống cho phép người dùng xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. |

> **Ghi chú thiết kế – FEAT 12.3/12.4:** Trong baseline hiện tại, "luồng tác vụ cá nhân" của STRQ 12 được cụ thể hóa bằng nhóm chức năng đăng ký đào tạo, hủy đăng ký và xem các khóa đào tạo đã đăng ký. Các tác vụ cá nhân khác nằm ngoài phạm vi của bộ FEAT hiện tại.

## Part B: UC Model Entries (for Section III)

- UC 4.38: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự
- UC 4.39: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự
- UC 4.40: Ghi nhận đánh giá cho nhân sự
- UC 4.41: Xem lịch sử đánh giá khen thưởng/kỷ luật
- UC 4.42: Tìm kiếm và lọc danh sách đánh giá
- UC 4.43: Mở khóa đào tạo cho cán bộ giảng viên
- UC 4.44: Sửa thông tin khóa đào tạo đã mở
- UC 4.45: Xem chi tiết thông tin khóa đào tạo đã mở
- UC 4.46: Ghi nhận kết quả đào tạo của cán bộ giảng viên
- UC 4.47: Xem các thông tin trong hồ sơ cá nhân của nhân sự
- UC 4.48: Xem thông tin chi tiết đơn vị đang công tác
- UC 4.49: Thay đổi trạng thái đăng ký khóa đào tạo
- UC 4.50: Xem danh sách các khóa đào tạo đã đăng ký

## Part C: FEAT→UC Traceability (for Section III)

| FEAT | UC tương ứng |
|------|-------------|
| FEAT 9.1 | UC 4.38 (Bổ nhiệm nhân sự vào đơn vị tổ chức nhân sự) |
| FEAT 9.2 | UC 4.38 (Điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác) |
| FEAT 9.3 | UC 4.39 (Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự) |
| FEAT 10.1 | UC 4.40 (Ghi nhận đánh giá cho nhân sự) |
| FEAT 10.2 | UC 4.41 (Xem lịch sử đánh giá khen thưởng/kỷ luật) |
| FEAT 10.3 | UC 4.42 (Tìm kiếm và lọc danh sách đánh giá) |
| FEAT 11.1 | UC 4.43 (Mở khóa đào tạo cho cán bộ giảng viên) |
| FEAT 11.2 | UC 4.44 (Sửa thông tin khóa đào tạo đã mở) |
| FEAT 11.3 | UC 4.45 (Xem chi tiết thông tin khóa đào tạo đã mở) |
| FEAT 11.4 | UC 4.46 (Ghi nhận kết quả đào tạo của cán bộ giảng viên) |
| FEAT 12.1 | UC 4.47 (Xem các thông tin trong hồ sơ cá nhân của nhân sự) |
| FEAT 12.2 | UC 4.48 (Xem thông tin chi tiết đơn vị đang công tác) |
| FEAT 12.3 | UC 4.49 (Thay đổi trạng thái đăng ký khóa đào tạo) |
| FEAT 12.4 | UC 4.50 (Xem danh sách các khóa đào tạo đã đăng ký) |

## Part D: UC Specifications (for Section IV)

### 4.38. Use Case: Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bổ nhiệm và điều chuyển nhân sự cho đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB bổ nhiệm nhân sự vào các đơn vị tổ chức. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng bổ nhiệm trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống. Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức. Nhân sự phải có trạng thái hợp đồng “Còn hiệu lực” hoặc “Chờ gia hạn” và trạng thái làm việc “Đang chờ xét” hoặc “Đang công tác”. |
| Điều kiện thành công (Post-condition) | Nhân sự được bổ nhiệm nhân sự vào đơn vị. Thông tin nhân sự của đơn vị được cập nhật. |
| Điều kiện thất bại | Việc bổ nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức. 2. Phòng TCCB chọn bổ nhiệm nhân sự chưa công tác. 3. Hệ thống hiển thị danh sách nhân sự ở trạng thái “Đang chờ xét” và trạng thái hợp đồng “Còn hiệu lực”. 4. Phòng TCCB chọn nhân sự và nhập thông tin như Chức vụ, Ngày bắt đầu. 5. Hệ thống kiểm tra hợp lệ Ngày bắt đầu. 6. Hệ thống thay đổi danh sách nhân sự, trạng thái công việc của nhân sự chuyển thành “Đang công tác” và thông báo thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Bổ nhiệm nhân sự đang công tác ở đơn vị khác** A1.1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức. A1.2. Phòng TCCB chọn bổ nhiệm nhân sự đang công tác tại đơn vị khác. A1.3. Hệ thống yêu cầu chọn đơn vị, chọn nhân sự từ đơn vị được chọn. A1.4. Phòng TCCB chọn nhân sự và nhập thông tin như Chức vụ, Ngày bắt đầu. A1.5. Hệ thống kiểm tra hợp lệ Ngày bắt đầu. A1.6. Hệ thống gỡ nhân sự khỏi đơn vị cũ, thêm vào đơn vị mới, cập nhật danh sách nhân sự của cả hai đơn vị và thông báo thành công. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu không hợp lệ** E1.1. Tại bước 5 hoặc A1.5, hệ thống phát hiện Ngày bắt đầu nhỏ hơn ngày hiện tại. E1.2. Hệ thống yêu cầu nhập lại và không lưu dữ liệu. **E2: Không được phép tiếp tục** E2.1. Tại bước 1, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. E2.2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục cập nhật bổ nhiệm. |

### 4.39. Use Case: Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Bãi nhiệm nhân sự khỏi đơn vị tổ chức nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB thực hiện bãi nhiệm nhân sự trong đơn vị tổ chức, nhằm cập nhật chính xác tình trạng nhân sự và phục vụ công tác quản lý nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng bãi nhiệm nhân sự của đơn vị trong menu “Cơ cấu tổ chức”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Đơn vị tổ chức đã tồn tại trong cây cơ cấu tổ chức. |
| Điều kiện thành công (Post-condition) | Nhân sự được miễn nhiệm khỏi chức vụ. Trạng thái công việc của nhân sự được cập nhật thành “Đang chờ xét”. Nhân sự được xóa khỏi danh sách của đơn vị tổ chức. |
| Điều kiện thất bại | Việc bãi nhiệm không được thực hiện do vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập một đơn vị trong cơ cấu tổ chức. 2. Hệ thống hiển thị danh sách nhân sự. 3. Phòng TCCB chọn chức năng bãi nhiệm từ trong một nhân sự trong danh sách. 4. Hệ thống yêu cầu xác nhận thao tác. 5. Phòng TCCB xác nhận thao tác miễn nhiệm. 6. Hệ thống cập nhật trạng thái công việc của nhân sự là “Đang chờ xét” và xóa nhân sự khỏi danh sách của đơn vị tổ chức. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Không được phép tiếp tục** E1.1. Tại bước 3, nếu đơn vị đang ở trạng thái “Giải thể” hoặc “Sáp nhập”. E1.2. Hệ thống hiển thị thông báo từ chối cho phép tiếp tục thực hiện bãi nhiệm. |

### 4.40. Use Case: Ghi nhận đánh giá cho nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận đánh giá cho nhân sự** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Ghi nhận các quyết định đánh giá khen thưởng hoặc kỷ luật đối với nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Thêm đánh giá khen thưởng hoặc kỷ luật”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ TCCB đã đăng nhập hệ thống. Hồ sơ nhân sự đã được tạo. Nhân sự không ở trạng thái làm việc “Đã thôi việc”. |
| Điều kiện thành công (Post-condition) | Hồ sơ nhân sự được cập nhật. Lịch sử thay đổi được ghi lại. |
| Điều kiện thất bại | Dữ liệu đánh giá không được ghi nhận vào hệ thống do thiếu các trường thông tin bắt buộc, hoặc do lỗi kết nối cơ sở dữ liệu hoặc phiên đăng nhập hết hạn. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn tab “Thêm đánh giá khen thưởng hoặc kỷ luật”. 2. Hệ thống yêu cầu nhập mã nhân sự và chọn loại đánh giá. 3. Phòng TCCB nhập mã nhân sự và chọn loại đánh giá (Khen thưởng/Kỷ luật). 4. Hệ thống hiển thị giao diện nhập liệu: nếu chọn loại đánh giá là khen thưởng thì gồm Loại khen thưởng, Tên khen thưởng, Ngày quyết định, Số quyết định, Nội dung, Số tiền thưởng (nếu có); nếu chọn loại đánh giá là kỷ luật thì gồm Loại kỷ luật, Tên kỷ luật, Ngày quyết định, Lý do, Hình thức xử lý. 5. Phòng TCCB nhấn “Lưu”. 6. Hệ thống kiểm tra dữ liệu hợp lệ. 7. Hệ thống lưu dữ liệu, đẩy vào hồ sơ cá nhân và thông báo thành công. Lưu ý: xem UC 4.41 và UC 4.42 cho các tác vụ tra cứu liên quan. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Mã nhân sự không hợp lệ** E1.1. Tại bước 3, hệ thống phát hiện mã nhân sự không tồn tại. E1.2. Hệ thống từ chối tiếp tục tạo bản đánh giá. **E2: Dữ liệu không hợp lệ** E2.1. Tại bước 6, hệ thống phát hiện dữ liệu không đầy đủ các trường thông tin. E2.2. Hệ thống từ chối lưu thông tin và thông báo lỗi. **E3: Hủy thao tác** E3.1. Tại bước 2, Phòng TCCB chọn “Hủy”. E3.2. Quay lại màn hình danh sách nhân sự. **E4: Nhân sự đã thôi việc** E4.1. Tại bước 3, hệ thống phát hiện nhân sự đang ở trạng thái làm việc “Đã thôi việc”. E4.2. Hệ thống từ chối ghi nhận đánh giá và hiển thị thông báo: “Không thể ghi nhận đánh giá cho nhân sự đã thôi việc.” |

### 4.41. Use Case: Xem lịch sử đánh giá khen thưởng/kỷ luật

|  |  |
| --- | --- |
| **Tên use case** | **Xem lịch sử đánh giá khen thưởng/kỷ luật** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem lịch sử toàn bộ các bản ghi đánh giá khen thưởng và kỷ luật của một nhân sự theo trình tự thời gian, phục vụ tra cứu, đối chiếu và theo dõi hồ sơ đánh giá của nhân sự. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn tab “Khen thưởng/Kỷ luật” trong màn hình chi tiết hồ sơ nhân sự. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Hồ sơ nhân sự đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Lịch sử đánh giá khen thưởng/kỷ luật của nhân sự được hiển thị đầy đủ, chính xác và không làm thay đổi dữ liệu trong hệ thống. |
| Điều kiện thất bại | Không thể hiển thị lịch sử đánh giá do lỗi hệ thống hoặc hồ sơ nhân sự không tồn tại. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập màn hình chi tiết hồ sơ nhân sự của một nhân sự (tham chiếu UC 4.35). 2. Hệ thống hiển thị màn hình chi tiết hồ sơ ở chế độ chỉ đọc. 3. Phòng TCCB chọn tab “Khen thưởng/Kỷ luật”. 4. Hệ thống hiển thị danh sách toàn bộ bản ghi đánh giá của nhân sự theo thứ tự thời gian, bao gồm các thông tin: Ngày quyết định, Loại đánh giá (Khen thưởng/Kỷ luật), Tên đánh giá, Số quyết định, Mô tả ngắn/Nội dung. 5. Phòng TCCB chọn một bản ghi đánh giá trong danh sách. 6. Hệ thống hiển thị chi tiết bản ghi đã chọn, bao gồm đầy đủ thông tin đã được ghi nhận từ UC 4.40. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Nhân sự chưa có lịch sử đánh giá** A1.1. Tại bước 3, nếu hồ sơ nhân sự chưa có bản ghi khen thưởng hoặc kỷ luật nào. A1.2. Hệ thống hiển thị tab “Khen thưởng/Kỷ luật” ở trạng thái trống và thông báo: “Nhân sự chưa có lịch sử đánh giá khen thưởng/kỷ luật.” |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có. |

### 4.42. Use Case: Tìm kiếm và lọc danh sách đánh giá

|  |  |
| --- | --- |
| **Tên use case** | **Tìm kiếm và lọc danh sách đánh giá** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB tìm kiếm và lọc danh sách các bản ghi khen thưởng/kỷ luật theo nhân sự, loại đánh giá hoặc khoảng thời gian nhằm phục vụ công tác tra cứu, thống kê và đối chiếu dữ liệu đánh giá. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB truy cập chức năng quản lý đánh giá khen thưởng/kỷ luật. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Danh sách các bản ghi đánh giá phù hợp với điều kiện tìm kiếm/lọc được hiển thị đầy đủ, chính xác. Phòng TCCB có thể tiếp tục xem chi tiết từng bản ghi. |
| Điều kiện thất bại | Hệ thống không thể xử lý yêu cầu tìm kiếm/lọc do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập chức năng quản lý đánh giá khen thưởng/kỷ luật. 2. Hệ thống hiển thị danh sách các bản ghi đánh giá và vùng bộ lọc tìm kiếm. 3. Phòng TCCB nhập từ khóa tìm kiếm và/hoặc chọn các tiêu chí lọc, bao gồm: Nhân sự (Mã cán bộ/Họ tên), Loại đánh giá (Khen thưởng/Kỷ luật), Khoảng thời gian (Từ ngày – Đến ngày). 4. Phòng TCCB nhấn “Tìm kiếm” hoặc “Áp dụng bộ lọc”. 5. Hệ thống hiển thị danh sách kết quả phù hợp với tiêu chí đã chọn, bao gồm các thông tin: Mã cán bộ, Họ tên, Loại đánh giá, Tên đánh giá, Ngày quyết định, Số quyết định. 6. Phòng TCCB có thể chọn một bản ghi bất kỳ trong danh sách kết quả. 7. Hệ thống hiển thị chi tiết bản ghi đánh giá đã chọn (tham chiếu UC 4.41). |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Không có kết quả phù hợp** A1.1. Tại bước 5, nếu không có bản ghi nào phù hợp với tiêu chí tìm kiếm/lọc. A1.2. Hệ thống hiển thị thông báo: “Không tìm thấy đánh giá phù hợp với tiêu chí tìm kiếm.” |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có. |

### 4.43. Use Case: Mở khóa đào tạo cho cán bộ giảng viên

|  |  |
| --- | --- |
| **Tên use case** | **Mở khóa đào tạo cho cán bộ giảng viên** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Cán bộ TCCB tạo mới và thiết lập thông tin một khóa đào tạo dành cho cán bộ, giảng viên; cấu hình hình thức đào tạo, thời gian, kinh phí và điều kiện đăng ký, làm cơ sở cho việc đăng ký tham gia và quản lý đào tạo sau này. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng mở khóa học trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết (Precondition) | Phòng TCCB đã đăng nhập hệ thống. |
| Điều kiện thành công (Post-condition) | Khóa đào tạo được tạo mới và lưu thành công. Trạng thái khóa đào tạo được thiết lập theo cấu hình. |
| Điều kiện thất bại | Khóa đào tạo không được tạo do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn menu “Đào tạo & Phát triển”. 2. Phòng TCCB nhấn “Tạo khóa đào tạo mới”. 3. Hệ thống hiển thị thông tin nhập. 4. Phòng TCCB nhập thông tin: Tên khóa đào tạo, Loại khóa đào tạo (theo cấu hình), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo (Tên chứng chỉ, Loại chứng chỉ). 5. Phòng TCCB thiết lập thời gian mở đăng ký từ ngày – đến ngày, Giới hạn số người tham gia. 6. Phòng TCCB nhấn “Lưu”. 7. Hệ thống kiểm tra dữ liệu hợp lệ. 8. Hệ thống yêu cầu xác nhận tạo khóa đào tạo. 9. Phòng TCCB xác nhận. 10. Hệ thống lưu khóa đào tạo và thiết lập trạng thái ban đầu là “Đang mở đăng ký”. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Dữ liệu lưu không hợp lệ** E1.1. Tại bước 7, hệ thống phát hiện thiếu các trường bắt buộc (Tên khóa, Loại khóa, Thời gian), hoặc thời gian mở đăng ký kết thúc sau ngày bắt đầu đào tạo. E1.2. Hệ thống hiển thị cảnh báo và yêu cầu chỉnh sửa. **E2: Hủy thao tác** E2.1. Tại bước 4, Phòng TCCB chọn “Hủy”. E2.2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.44. Use Case: Sửa thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Sửa thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB chỉnh sửa các thông tin của khóa đào tạo đã được tạo nhằm cập nhật kế hoạch đào tạo phù hợp với thực tế, đồng thời đảm bảo không vi phạm các ràng buộc nghiệp vụ đối với khóa đào tạo đã mở đăng ký hoặc đã có người tham gia. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Sửa thông tin khóa đào tạo” tại một khóa đào tạo trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Khóa đào tạo đã tồn tại trong hệ thống. Khóa đào tạo đang ở trạng thái "Đang mở đăng ký" hoặc "Đang đào tạo". |
| Điều kiện thành công (Post-condition) | Thông tin khóa đào tạo được cập nhật thành công. Các thay đổi được ghi nhận và áp dụng ngay cho khóa đào tạo. |
| Điều kiện thất bại | Thông tin khóa đào tạo không được cập nhật do vi phạm ràng buộc nghiệp vụ hoặc dữ liệu không hợp lệ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB chọn menu “Đào tạo & Phát triển”. 2. Hệ thống hiển thị danh sách các khóa đào tạo. 3. Phòng TCCB chọn một khóa đào tạo và nhấn “Sửa thông tin”. 4. Hệ thống hiển thị màn hình chỉnh sửa thông tin khóa đào tạo. 5. Phòng TCCB chỉnh sửa các thông tin cho phép: Tên khóa đào tạo, Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Thông tin chứng chỉ sau đào tạo, Trạng thái khóa đào tạo, Thời gian mở đăng ký và giới hạn số người tham gia (nếu được phép). 6. Phòng TCCB nhấn “Lưu”. 7. Hệ thống kiểm tra tính hợp lệ và ràng buộc nghiệp vụ, bao gồm kiểm tra chuyển trạng thái khóa đào tạo phải tuân theo thứ tự: Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước. 8. Hệ thống yêu cầu xác nhận cập nhật. 9. Phòng TCCB xác nhận. 10. Hệ thống cập nhật thông tin khóa đào tạo và thông báo thành công. Lưu ý: Khi trạng thái khóa đào tạo được chuyển sang “Đang đào tạo”, hệ thống tự động batch-update tất cả đăng ký tham gia có trạng thái “Đã đăng ký” sang “Đang học”. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Chỉnh sửa khi khóa đào tạo đang diễn ra** A1.1. Tại bước 4, nếu khóa đào tạo ở trạng thái “Đang đào tạo”, hệ thống chỉ cho phép chỉnh sửa: Địa điểm, Kinh phí, Cam kết sau đào tạo, Thông tin chứng chỉ sau đào tạo. A1.2. Hệ thống khóa không cho phép chỉnh sửa: Tên khóa đào tạo, Loại khóa đào tạo, Thời gian mở đăng ký, Giới hạn số người tham gia. A1.3. Tiếp tục từ bước 6. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Chuyển trạng thái không hợp lệ** E1.1. Tại bước 7, hệ thống phát hiện trạng thái mới được chọn vi phạm thứ tự chuyển đổi (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành; không cho phép chuyển ngược hoặc bỏ qua bước). E1.2. Hệ thống hiển thị thông báo: “Chuyển trạng thái không hợp lệ.” và yêu cầu chọn lại. **E2: Vi phạm ràng buộc đăng ký** E2.1. Tại bước 7, hệ thống phát hiện nếu Giảm giới hạn số người tham gia nhỏ hơn số lượng đã đăng ký. E2.2. Hệ thống hiển thị cảnh báo và không cho phép lưu. **E3: Dữ liệu không hợp lệ** E3.1. Tại bước 7, hệ thống phát hiện thiếu trường bắt buộc hoặc thời gian không hợp lệ. E3.2. Hệ thống yêu cầu chỉnh sửa lại thông tin. **E4: Hủy thao tác** E4.1. Tại bước 5, Phòng TCCB chọn “Hủy”. E4.2. Quay lại màn hình danh sách khóa đào tạo. |

### 4.45. Use Case: Xem chi tiết thông tin khóa đào tạo đã mở

|  |  |
| --- | --- |
| **Tên use case** | **Xem chi tiết thông tin khóa đào tạo đã mở** |
| Tác nhân chính | Phòng TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB xem đầy đủ thông tin chi tiết của một khóa đào tạo đã được tạo, bao gồm trạng thái khóa học, thông tin tổ chức đào tạo, danh sách cán bộ – giảng viên đăng ký tham gia, và tình trạng tham gia của từng nhân sự, nhằm phục vụ công tác quản lý, theo dõi và ra quyết định điều chỉnh khóa đào tạo khi cần thiết. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn một khóa đào tạo và nhấn chức năng “Xem chi tiết” trong menu “Đào tạo & Phát triển”. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Khóa đào tạo đã tồn tại trong hệ thống. |
| Điều kiện thành công (Post-condition) | Thông tin chi tiết của khóa đào tạo được hiển thị đầy đủ và chính xác. Phòng TCCB có thể theo dõi tình trạng khóa học và danh sách nhân sự tham gia. |
| Điều kiện thất bại | Không thể hiển thị thông tin khóa đào tạo do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập menu “Đào tạo & Phát triển”. 2. Hệ thống hiển thị danh sách các khóa đào tạo. 3. Phòng TCCB chọn một khóa đào tạo và nhấn “Xem chi tiết”. 4. Hệ thống hiển thị màn hình chi tiết khóa đào tạo, hiển thị đầy đủ thông tin theo yêu cầu bao gồm các thông tin: Thông tin chung khóa đào tạo: Tên khóa đào tạo, Loại khóa đào tạo, Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), Thời gian đào tạo (từ ngày – đến ngày), Địa điểm, Kinh phí (nếu có), Cam kết sau đào tạo (nếu có), Chứng chỉ sau đào tạo. Thông tin đăng ký: Thời gian mở đăng ký, Giới hạn số lượng người tham gia, Số lượng đã đăng ký / số lượng tối đa. Danh sách tham gia: Hệ thống hiển thị danh sách cán bộ, giảng viên đã đăng ký khóa đào tạo, bao gồm Họ và tên, Mã cán bộ, Đơn vị đang công tác, Thời điểm đăng ký, Trạng thái tham gia. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có. |

### 4.46. Use Case: Ghi nhận kết quả đào tạo của cán bộ giảng viên

|  |  |
| --- | --- |
| **Tên use case** | **Ghi nhận kết quả đào tạo của cán bộ giảng viên** |
| Tác nhân chính | Cán bộ TCCB |
| Mục đích (mô tả) | Cho phép Phòng TCCB ghi nhận kết quả tham gia khóa đào tạo của cán bộ, giảng viên sau khi khóa học kết thúc; cập nhật trạng thái hoàn thành, không đạt và lưu trữ chứng chỉ đào tạo vào hồ sơ nhân sự nhằm phục vụ công tác quản lý và đánh giá năng lực. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Phòng TCCB chọn chức năng “Ghi nhận kết quả đào tạo” tại tab “Danh sách học viên” của một khóa đào tạo. |
| Điều kiện tiên quyết (Precondition) | Cán bộ Phòng TCCB đã đăng nhập hệ thống. Khóa đào tạo đã tồn tại trong hệ thống. Trạng thái khóa đào tạo là “Đã hoàn thành”. Khóa đào tạo có danh sách học viên đã đăng ký. |
| Điều kiện thành công (Post-condition) | Kết quả đào tạo của từng học viên được ghi nhận thành công. Trạng thái tham gia của học viên được cập nhật. Chứng chỉ đào tạo (nếu có) được lưu vào hồ sơ cá nhân của nhân sự. Lịch sử đào tạo của nhân sự được cập nhật. |
| Điều kiện thất bại | Kết quả đào tạo không được ghi nhận do dữ liệu không hợp lệ hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Phòng TCCB truy cập menu “Đào tạo & Phát triển”. 2. Chọn xem chi tiết tab “Danh sách học viên” của một khóa đào tạo có trạng thái “Đã hoàn thành”. 3. Hệ thống hiển thị danh sách học viên tham gia khóa đào tạo, bao gồm Họ tên, Mã cán bộ, Đơn vị công tác, Trạng thái tham gia hiện tại (Đang học). 4. Phòng TCCB chọn một học viên và nhấn “Ghi nhận kết quả”. 5. Hệ thống hiển thị form ghi nhận kết quả, bao gồm: Trạng thái kết quả (Hoàn thành/Không đạt), Ngày hoàn thành (mặc định là ngày kết thúc khóa học), File chứng chỉ (PDF) (tùy chọn, bắt buộc nếu trạng thái là “Hoàn thành”). 6. Phòng TCCB nhập thông tin và nhấn “Lưu”. 7. Hệ thống kiểm tra tính hợp lệ của dữ liệu. 8. Hệ thống cập nhật trạng thái học viên: nếu Hoàn thành thì ghi nhận kết quả đào tạo và lưu chứng chỉ vào hồ sơ nhân sự; nếu Không đạt thì chỉ lưu trạng thái kết quả và thông báo ghi nhận thành công. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Ghi nhận kết quả cho nhiều học viên** A1.1. Tại bước 4, Phòng TCCB có thể chọn nhiều học viên. A1.2. Hệ thống cho phép ghi nhận kết quả hàng loạt với cùng trạng thái. A1.3. Luồng tiếp tục từ bước 5. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Khóa đào tạo chưa hoàn thành** E1.1. Tại bước 4, nếu trạng thái khóa đào tạo khác “Đã hoàn thành”. E1.2. Hệ thống hiển thị thông báo: “Chỉ có thể ghi nhận kết quả khi khóa đào tạo đã hoàn thành.” **E2: Thiếu chứng chỉ khi hoàn thành, dữ liệu không hợp lệ** E2.1. Tại bước 8, hệ thống phát hiện thiếu thông tin bắt buộc, file không đúng định dạng hoặc học viên được đánh dấu “Hoàn thành” nhưng không upload file chứng chỉ trong trường hợp bắt buộc. E2.2. Hệ thống hiển thị cảnh báo và yêu cầu bổ sung. |

### 4.47. Use Case: Xem các thông tin trong hồ sơ cá nhân của nhân sự

|  |  |
| --- | --- |
| **Tên use case** | **Xem các thông tin trong hồ sơ cá nhân của nhân sự** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng xem toàn bộ thông tin hồ sơ cá nhân của mình đang được lưu trong hệ thống, tra cứu lịch sử hợp đồng, hệ số, bậc lương, các quyết định khen thưởng và kỷ luật của bản thân. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng “Hồ sơ cá nhân” trên giao diện hệ thống. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập. |
| Điều kiện thành công (Post-condition) | Thông tin hồ sơ cá nhân được hiển thị đầy đủ cho người dùng. |
| Điều kiện thất bại | Không thể hiển thị thông tin hồ sơ cá nhân do lỗi hệ thống. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng chọn chức năng xem hồ sơ cá nhân. 2. Hệ thống hiển thị đầy đủ thông tin theo các tab: Tab “Thông tin chung” (Mã cán bộ, lý lịch, liên hệ, gia đình, ảnh chân dung); Tab “Trình độ & Chức danh” (Bằng cấp, chứng chỉ, chức danh khoa học, chức vụ, đơn vị công tác); Tab “Thông tin Đảng/Đoàn”; Tab “Lương & Phụ cấp” (ngạch, bậc, hệ số lương, thông tin ngân hàng); Tab “Hợp đồng”; Tab “Khen thưởng/Kỷ luật” (chỉ hiển thị nếu Phòng TCCB đã cấu hình cho phép, tham chiếu UC 4.35 và FEAT 8.9); Tab “Công tác”. |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có. |

### 4.48. Use Case: Xem thông tin chi tiết đơn vị đang công tác

|  |  |
| --- | --- |
| **Tên use case** | **Xem thông tin chi tiết đơn vị đang công tác** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng xem thông tin chi tiết về đơn vị tổ chức mà mình đang công tác trong cơ cấu tổ chức của đơn vị, bao gồm thông tin cơ bản của đơn vị, danh sách chức vụ và nhân sự hiện tại trong đơn vị. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn chức năng xem thông tin đơn vị công tác từ hồ sơ cá nhân hoặc menu liên quan. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống. Người dùng đã được gán đơn vị công tác trong hệ thống. Đơn vị tổ chức đang tồn tại trong cơ cấu tổ chức. |
| Điều kiện thành công (Post-condition) | Thông tin chi tiết của đơn vị công tác được hiển thị đầy đủ và chính xác. Không có thay đổi dữ liệu trong hệ thống (chỉ đọc). |
| Điều kiện thất bại | Không hiển thị được thông tin do lỗi hệ thống hoặc không xác định được đơn vị công tác của người dùng. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng truy cập chức năng xem thông tin đơn vị công tác. 2. Hệ thống xác định đơn vị mà người dùng đang trực thuộc. 3. Hệ thống hiển thị thông tin chi tiết của đơn vị, bao gồm: Tab “Tổng quan” (Tên đơn vị, Mã đơn vị, Loại đơn vị, Đơn vị cha, Ngày thành lập, Thông tin liên hệ, Trạng thái hiện tại của đơn vị); Tab “Nhân sự” (danh sách nhân sự, chức vụ, mã cán bộ, ngày bắt đầu); Tab “Đơn vị trực thuộc” (danh sách các đơn vị con trực thuộc đơn vị đang xem). |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có. |

### 4.49. Use Case: Thay đổi trạng thái đăng ký khóa đào tạo

|  |  |
| --- | --- |
| **Tên use case** | **Thay đổi trạng thái đăng ký khóa đào tạo** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng đăng ký hoặc hủy đăng ký tham gia các khóa đào tạo do nhà trường tổ chức đang trong thời gian mở đăng ký, làm cơ sở cho việc quản lý học viên, theo dõi quá trình và ghi nhận kết quả đào tạo. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Người dùng chọn menu “Đào tạo”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống. Khóa đào tạo tồn tại và đang ở trạng thái “Đang mở đăng ký”. Thời điểm hiện tại nằm trong khoảng Thời gian mở đăng ký. |
| Điều kiện thành công (Post-condition) | Đăng ký tham gia khóa đào tạo của người dùng được ghi nhận trong hệ thống (trường hợp đăng ký). Bản ghi đăng ký của người dùng được xóa khỏi hệ thống (trường hợp hủy đăng ký). |
| Điều kiện thất bại | Không thể thay đổi trạng thái đăng ký do khóa đào tạo không hợp lệ, hết hạn đăng ký hoặc vi phạm ràng buộc nghiệp vụ. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng truy cập menu “Đào tạo”. 2. Hệ thống hiển thị danh sách các khóa đào tạo ở trạng thái “Đang mở đăng ký”. 3. Người dùng chọn một khóa đào tạo để xem chi tiết thông tin. 4. Hệ thống hiển thị thông tin chi tiết khóa đào tạo. Nếu người dùng chưa đăng ký, hiển thị nút “Đăng ký tham gia”. Nếu người dùng đã đăng ký với trạng thái “Đã đăng ký”, hiển thị nút “Hủy đăng ký”. 5. Người dùng nhấn nút “Đăng ký tham gia”. 6. Hệ thống kiểm tra các điều kiện đăng ký (thời gian mở đăng ký, số lượng đăng ký chưa đạt giới hạn, trạng thái khóa đào tạo). 7. Hệ thống tạo bản ghi đăng ký đào tạo và thiết lập trạng thái tham gia là “Đã đăng ký”. 8. Hệ thống thông báo đăng ký thành công cho người dùng. |
| Luồng sự kiện thay thế (Alternative Flow) | **A1: Hủy đăng ký khóa đào tạo** A1.1. Tại bước 4, người dùng đã đăng ký khóa đào tạo này với trạng thái tham gia “Đã đăng ký”. Hệ thống hiển thị nút “Hủy đăng ký”. A1.2. Người dùng nhấn nút “Hủy đăng ký”. A1.3. Hệ thống yêu cầu xác nhận hủy đăng ký. A1.4. Người dùng xác nhận. A1.5. Hệ thống kiểm tra trạng thái tham gia phải là “Đã đăng ký” và khóa đào tạo phải đang ở trạng thái “Đang mở đăng ký”. A1.6. Hệ thống xóa bản ghi đăng ký đào tạo của người dùng. A1.7. Hệ thống thông báo hủy đăng ký thành công. |
| Luồng sự kiện ngoại lệ (Exception Flow) | **E1: Hết thời gian đăng ký** E1.1. Tại bước 4, nếu thời gian hiện tại nằm ngoài khoảng mở đăng ký. E1.2. Hệ thống ẩn nút “Đăng ký tham gia” và “Hủy đăng ký”, hiển thị thông báo: “Khóa đào tạo đã hết thời gian đăng ký.” **E2: Đã đủ số lượng người tham gia** E2.1. Tại bước 6, nếu số lượng đăng ký đã đạt giới hạn. E2.2. Hệ thống hiển thị thông báo: “Khóa đào tạo đã đủ số lượng đăng ký.” **E3: Không thể hủy đăng ký** E3.1. Tại bước A1.5, nếu trạng thái tham gia không phải “Đã đăng ký” (ví dụ: đã chuyển sang “Đang học” do khóa đào tạo đã bắt đầu) hoặc khóa đào tạo không còn ở trạng thái “Đang mở đăng ký”. E3.2. Hệ thống hiển thị thông báo: “Không thể hủy đăng ký do khóa đào tạo đã chuyển sang giai đoạn tiếp theo.” |

### 4.50. Use Case: Xem danh sách các khóa đào tạo đã đăng ký

|  |  |
| --- | --- |
| **Tên use case** | **Xem danh sách các khóa đào tạo đã đăng ký** |
| Tác nhân chính | Người dùng (Cán bộ/Giảng viên/Nhân viên) |
| Mục đích (mô tả) | Cho phép người dùng xem danh sách tất cả các khóa đào tạo mà mình đã đăng ký tham gia, theo dõi trạng thái tham gia và kết quả đào tạo của từng khóa (Đang học, Hoàn thành, Không đạt), phục vụ việc tra cứu, theo dõi quá trình học tập và kết quả đào tạo cá nhân. |
| Mức độ ưu tiên (Priority) | Bắt buộc |
| Điều kiện kích hoạt (Trigger) | Chọn menu “Đào tạo”. |
| Điều kiện tiên quyết (Precondition) | Người dùng đã đăng nhập hệ thống. Người dùng đã từng đăng ký ít nhất một khóa đào tạo. |
| Điều kiện thành công (Post-condition) | Danh sách các khóa đào tạo đã đăng ký của người dùng được hiển thị đầy đủ và chính xác. Trạng thái tham gia và kết quả đào tạo của từng khóa được hiển thị đúng theo dữ liệu do Phòng TCCB ghi nhận. |
| Điều kiện thất bại | Không hiển thị được danh sách do lỗi hệ thống hoặc dữ liệu không tồn tại. |
| Luồng sự kiện chính (Basic Flow) | 1. Người dùng truy cập chức năng “Khóa đào tạo đã đăng ký”. 2. Hệ thống truy xuất danh sách các khóa đào tạo mà người dùng đã đăng ký. 3. Hệ thống hiển thị danh sách khóa đào tạo, bao gồm các thông tin: Tên khóa đào tạo, Loại khóa đào tạo, Thời gian đào tạo (từ ngày – đến ngày), Đơn vị/địa điểm tổ chức, Trạng thái khóa đào tạo (Đang mở đăng ký / Đang đào tạo / Đã hoàn thành), Trạng thái tham gia của cá nhân (Đã đăng ký, Đang học, Hoàn thành, Không đạt). |
| Luồng sự kiện thay thế (Alternative Flow) | Không có. |
| Luồng sự kiện ngoại lệ (Exception Flow) | Không có. |

## Part E: FEAT-specific SUPLs

> Mục này liệt kê toàn bộ yêu cầu bổ sung (SUPL) do Ngô Đức Nam Khánh phụ trách. Các SUPL áp dụng toàn hệ thống được giữ nguyên nhãn **Toàn hệ thống** theo source baseline tại `section-vi-khanh.md`; các SUPL gắn trực tiếp với FEAT cụ thể được ghi rõ.

### 6.8. Security – Yêu cầu bảo mật

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
|----|----------|-----------------|------|---------|
| **SUPL-SE01** | Xác thực bằng tài khoản/mật khẩu | Mọi truy cập vào hệ thống phải qua xác thực bằng tài khoản/mật khẩu; mật khẩu phải có tối thiểu 8 ký tự, bao gồm chữ hoa, chữ thường và chữ số. | Toàn hệ thống | **M** |
| **SUPL-SE02** | Phân quyền theo vai trò | Hệ thống phải phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Người dùng); mỗi chức năng và API chỉ cho phép truy cập bởi vai trò được cấp quyền. | Toàn hệ thống | **M** |
| **SUPL-SE03** | Khóa tài khoản tạm thời | Hệ thống phải khóa tài khoản tạm thời sau 5 lần đăng nhập sai liên tiếp, thời gian khóa tối thiểu 15 phút và có ghi cảnh báo bảo mật. | Toàn hệ thống | **M** |
| **SUPL-SE04** | Bảo mật truyền tải HTTPS/TLS | Toàn bộ giao tiếp giữa client và server phải dùng HTTPS với TLS 1.2 trở lên, đồng thời tự động chuyển hướng HTTP sang HTTPS. | Toàn hệ thống | **M** |
| **SUPL-SE05** | Bảo vệ dữ liệu nhạy cảm | Dữ liệu nhạy cảm (CCCD, BHXH, thông tin ngân hàng) chỉ hiển thị cho vai trò được phép và mọi truy cập phải được ghi audit log. | Toàn hệ thống | **M** |
| **SUPL-SE06** | Chống CSRF/XSS | Hệ thống phải ngăn chặn tấn công web (CSRF, XSS) trên các chức năng nhập liệu và thao tác thay đổi dữ liệu. | Toàn hệ thống | **M** |
| **SUPL-SE07** | Chống SQL Injection | Hệ thống phải ngăn chặn SQL Injection trên toàn bộ chức năng truy vấn và cập nhật dữ liệu bằng cơ chế truy vấn tham số hóa hoặc tương đương. | Toàn hệ thống | **M** |
| **SUPL-SE08** | Phân quyền cấu hình ẩn/hiện khen thưởng-kỷ luật | Chỉ vai trò được ủy quyền mới được cấu hình ẩn/hiện mục khen thưởng/kỷ luật; mọi thay đổi phải lưu vết audit đầy đủ. | FEAT 8.9 (Tung) | **M** |
| **SUPL-SE09** | Phân quyền chấm dứt hợp đồng trước hạn | Chỉ người dùng có quyền mới được chấm dứt hợp đồng trước hạn; mọi thao tác phải được ghi audit log đầy đủ thông tin nghiệp vụ. | FEAT 7.4 (Tung) | **M** |

### 6.9. Implementation Constraints – Ràng buộc triển khai

| Mã | Yêu cầu | Mô tả chi tiết | FEAT | Ưu tiên |
|----|----------|-----------------|------|---------|
| **SUPL-IC01** | Stack công nghệ triển khai | Hệ thống phải sử dụng stack công nghệ: frontend React.js (TypeScript), backend Laravel/PHP và cơ sở dữ liệu MySQL/MariaDB trong các môi trường triển khai chính thức. | Toàn hệ thống | **M** |
| **SUPL-IC02** | Tương thích trình duyệt | Hệ thống phải hoạt động ổn định trên Chrome (bản mới nhất và 2 phiên bản gần nhất), Firefox và Edge. | Toàn hệ thống | **M** |
| **SUPL-IC03** | Mã hóa UTF-8 | Toàn bộ hệ thống phải sử dụng mã hóa UTF-8 để hỗ trợ đầy đủ tiếng Việt có dấu trên giao diện, API, cơ sở dữ liệu và dữ liệu trao đổi. | Toàn hệ thống | **M** |
| **SUPL-IC04** | Định dạng và dung lượng tệp hỗ trợ | Hệ thống chỉ hỗ trợ file PDF cho hồ sơ đính kèm và file Excel cho import/export nhân sự, với kích thước tối đa 10MB mỗi file. | Toàn hệ thống | **M** |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-SE01

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authentication (Xác thực) |
| **Độ đo yêu cầu** | (1) Số quy tắc mật khẩu bắt buộc được kiểm tra; (2) Số lớp xác thực trước khi truy cập hệ thống; (3) Trạng thái bảo vệ phiên và thời gian hết hạn không hoạt động. |
| **Tiêu chuẩn đáp ứng** | (1) Mật khẩu có ít nhất 8 ký tự và thỏa 3/3 quy tắc: chữ hoa, chữ thường, chữ số; (2) Áp dụng 01 lớp xác thực bằng tên đăng nhập/mật khẩu; (3) Phiên đăng nhập được bảo vệ và tự hết hiệu lực sau tối đa 30 phút không hoạt động. |

#### SUPL-SE02

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization (Phân quyền truy cập) |
| **Độ đo yêu cầu** | (1) Số trường hợp truy cập trái phép qua kiểm thử phân quyền; (2) Tỷ lệ API endpoint có kiểm tra quyền; (3) Số vai trò được định nghĩa trong mô hình RBAC. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp truy cập trái phép vào chức năng hoặc API không được cấp quyền; (2) 100% API endpoint có cơ chế kiểm tra quyền trước khi xử lý; (3) Hệ thống có đúng 4 vai trò: Admin, TCCB, TCKT, Người dùng. |

#### SUPL-SE03

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công tự động |
| **Độ đo yêu cầu** | (1) Ngưỡng số lần đăng nhập sai liên tiếp trước khi khóa tài khoản; (2) Thời gian khóa tạm thời; (3) Trạng thái ghi log cảnh báo brute-force. |
| **Tiêu chuẩn đáp ứng** | (1) Tài khoản bị khóa sau đúng 5 lần đăng nhập sai liên tiếp; (2) Thời gian khóa tối thiểu 15 phút; (3) Có bản ghi cảnh báo gồm tối thiểu IP, thời gian và tài khoản bị tác động. |

#### SUPL-SE04

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật truyền tải) |
| **Độ đo yêu cầu** | (1) Phiên bản TLS đang sử dụng; (2) Tỷ lệ kết nối HTTPS trên tổng kết nối; (3) Trạng thái tự động chuyển hướng HTTP sang HTTPS. |
| **Tiêu chuẩn đáp ứng** | (1) Chỉ chấp nhận TLS 1.2 trở lên; (2) 100% kết nối sử dụng HTTPS, 0% kết nối HTTP không mã hóa được xử lý trực tiếp; (3) Mọi truy cập HTTP được tự động chuyển hướng sang HTTPS. |

#### SUPL-SE05

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Confidentiality (Bảo mật dữ liệu) |
| **Độ đo yêu cầu** | (1) Số trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được phép; (2) Tỷ lệ lượt truy cập dữ liệu nhạy cảm được ghi audit log. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường dữ liệu nhạy cảm bị hiển thị cho vai trò không được cấp quyền; (2) 100% lượt truy cập các trường CCCD, BHXH và thông tin ngân hàng được ghi audit log. |

#### SUPL-SE06

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công web |
| **Độ đo yêu cầu** | (1) Số lỗ hổng CSRF phát hiện qua kiểm thử; (2) Số lỗ hổng XSS phát hiện qua kiểm thử; (3) Tỷ lệ request POST/PUT/DELETE có cơ chế chống giả mạo. |
| **Tiêu chuẩn đáp ứng** | (1) 0 lỗ hổng CSRF; (2) 0 lỗ hổng XSS; (3) 100% request POST/PUT/DELETE và form thay đổi dữ liệu vượt qua kiểm thử chống CSRF, 100% dữ liệu người dùng hiển thị lại trên giao diện vượt qua kiểm thử XSS. |

#### SUPL-SE07

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Integrity (Toàn vẹn) - Chống tấn công cơ sở dữ liệu |
| **Độ đo yêu cầu** | (1) Số lỗ hổng SQL Injection phát hiện qua kiểm thử; (2) Tỷ lệ truy vấn có dữ liệu đầu vào được bảo vệ bằng cơ chế tách dữ liệu khỏi câu lệnh SQL. |
| **Tiêu chuẩn đáp ứng** | (1) 0 lỗ hổng SQL Injection; (2) 100% truy vấn có dữ liệu đầu vào từ người dùng được bảo vệ bằng truy vấn tham số hóa hoặc ORM tương đương. |

#### SUPL-SE08

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Độ đo yêu cầu** | (1) Số thay đổi cấu hình ẩn/hiện mục khen thưởng/kỷ luật trái phép; (2) Tỷ lệ thay đổi cấu hình hợp lệ được ghi audit log; (3) Độ đầy đủ bản ghi audit theo 4 trường bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 0 thay đổi cấu hình do người dùng không được ủy quyền thực hiện thành công; (2) 100% thay đổi cấu hình hợp lệ được ghi audit log; (3) Mỗi bản ghi audit đạt 4/4 trường bắt buộc: người thực hiện, thời gian, giá trị trước, giá trị sau. |

#### SUPL-SE09

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Authorization + Auditability (Phân quyền + Khả năng kiểm toán) |
| **Độ đo yêu cầu** | (1) Số trường hợp chấm dứt hợp đồng trước hạn trái phép; (2) Tỷ lệ thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log; (3) Độ đầy đủ bản ghi audit theo 7 trường bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp chấm dứt hợp đồng trước hạn được thực hiện bởi người dùng không có quyền; (2) 100% thao tác chấm dứt hợp đồng trước hạn hợp lệ được ghi audit log; (3) Mỗi bản ghi audit đạt 7/7 trường bắt buộc: mã hợp đồng, mã nhân sự, lý do chấm dứt, người thực hiện, thời gian, giá trị trước, giá trị sau. |

#### SUPL-IC01

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi công nghệ) - Công nghệ triển khai |
| **Độ đo yêu cầu** | (1) Tỷ lệ module frontend dùng React.js + TypeScript; (2) Tỷ lệ thành phần backend dùng Laravel/PHP; (3) Tỷ lệ môi trường chính thức dùng MySQL/MariaDB. |
| **Tiêu chuẩn đáp ứng** | (1) 100% module frontend sử dụng React.js kết hợp TypeScript; (2) 100% thành phần backend sử dụng Laravel/PHP; (3) 100% môi trường triển khai chính thức sử dụng MySQL hoặc MariaDB, 0 thành phần production dùng hệ quản trị cơ sở dữ liệu ngoài phạm vi yêu cầu. |

#### SUPL-IC02

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Compatibility (Tính tương thích) - Trình duyệt |
| **Độ đo yêu cầu** | (1) Độ phủ kiểm thử trên tập trình duyệt/phiên bản mục tiêu; (2) Tỷ lệ chức năng nghiệp vụ chính chạy đúng theo từng trình duyệt; (3) Số lỗi mức nghiêm trọng theo trình duyệt. |
| **Tiêu chuẩn đáp ứng** | (1) 100% phạm vi kiểm thử bao gồm Chrome bản mới nhất và 2 phiên bản gần nhất, Firefox bản ổn định hiện hành, Edge bản ổn định hiện hành tại thời điểm nghiệm thu; (2) 100% chức năng chính hoạt động đúng trên Chrome, ≥95% trên Firefox và Edge; (3) 0 lỗi mức Nghiêm trọng/Critical trên các trình duyệt mục tiêu. |

#### SUPL-IC03

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability (Khả năng chuyển đổi) - Mã hóa dữ liệu |
| **Độ đo yêu cầu** | (1) Tỷ lệ thành phần hệ thống dùng UTF-8; (2) Số lỗi hiển thị tiếng Việt có dấu khi nhập, lưu, tìm kiếm và hiển thị dữ liệu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% thành phần của hệ thống dùng UTF-8; (2) 0 lỗi hiển thị sai tiếng Việt có dấu trên giao diện, dữ liệu lưu trữ, dữ liệu xuất và dữ liệu tải lại từ hệ thống. |

#### SUPL-IC04

| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Correctness (Tính đúng đắn) - File đính kèm |
| **Độ đo yêu cầu** | (1) Tỷ lệ file PDF/Excel hợp lệ được xử lý thành công; (2) Ngưỡng kích thước file tối đa hệ thống cho phép; (3) Tỷ lệ file sai định dạng hoặc vượt dung lượng bị từ chối. |
| **Tiêu chuẩn đáp ứng** | (1) 100% file PDF hợp lệ dùng cho bằng cấp, chứng chỉ, hợp đồng, giấy phép lao động được upload/download thành công và 100% file Excel hợp lệ dùng cho import/export nhân sự được xử lý thành công; (2) Kích thước tối đa được chấp nhận là 10MB/file; (3) 100% file sai định dạng hoặc lớn hơn 10MB bị từ chối và hệ thống hiển thị thông báo lỗi rõ ràng. |

### Tóm tắt truy vết SUPL → FEAT

| SUPL | FEAT | Chủ sở hữu FEAT | Ghi chú |
|------|------|-----------------|---------|
| SUPL-SE01 | Toàn hệ thống | — | Ràng buộc xác thực áp dụng cho toàn hệ thống |
| SUPL-SE02 | Toàn hệ thống | — | Ràng buộc phân quyền áp dụng cho toàn hệ thống |
| SUPL-SE03 | Toàn hệ thống | — | Ràng buộc khóa tài khoản tạm thời |
| SUPL-SE04 | Toàn hệ thống | — | Ràng buộc bảo mật truyền tải HTTPS/TLS |
| SUPL-SE05 | Toàn hệ thống | — | Ràng buộc bảo vệ dữ liệu nhạy cảm và audit log |
| SUPL-SE06 | Toàn hệ thống | — | Ràng buộc chống CSRF/XSS |
| SUPL-SE07 | Toàn hệ thống | — | Ràng buộc chống SQL Injection |
| SUPL-SE08 | FEAT 8.9 | Tung | Ràng buộc phân quyền và audit log cho cấu hình ẩn/hiện mục khen thưởng/kỷ luật |
| SUPL-SE09 | FEAT 7.4 | Tung | Ràng buộc phân quyền và audit log cho chấm dứt hợp đồng trước hạn |
| SUPL-IC01 | Toàn hệ thống | — | Ràng buộc stack công nghệ triển khai |
| SUPL-IC02 | Toàn hệ thống | — | Ràng buộc tương thích trình duyệt |
| SUPL-IC03 | Toàn hệ thống | — | Ràng buộc mã hóa UTF-8 |
| SUPL-IC04 | Toàn hệ thống | — | Ràng buộc định dạng và dung lượng tệp hỗ trợ |

## Appendix: SRS sections authored by Ngô Đức Nam Khánh

> Mục này chép đầy đủ phần nội dung do Ngô Đức Nam Khánh phụ trách trong `srs.md` (mục 7.3.4 và 7.4), đồng thời giữ nguyên cấu trúc Part A–E ở trên theo mẫu `phuc-contribution.md`.

### 7.3.4. Quy tắc quản lý requirement

> **Người thực hiện: Ngô Đức Nam Khánh**

#### 7.3.4.1. Quy tắc truy vết

Chuỗi truy vết của bộ yêu cầu phải tuân theo cấu trúc sau:

```text
STRQ ──→ FEAT ──→ UC ──→ SCEN
  │         │
  │         └──→ SUPL
  └──→ SUPL
```

Chi tiết các đường truy vết tối thiểu:

| Từ | Đến | Quan hệ | Ràng buộc bắt buộc |
| --- | --- | --- | --- |
| STRQ | FEAT | Nhiều-nhiều | Mỗi STRQ ở trạng thái `Approved` phải truy vết tới ít nhất một FEAT hoặc SUPL. |
| STRQ | SUPL | Nhiều-nhiều | Nằm trong ràng buộc bao phủ STRQ ở trên. |
| FEAT | UC | Nhiều-nhiều | Mỗi FEAT ở trạng thái `Approved` phải truy vết tới ít nhất một UC hoặc SUPL. |
| FEAT | SUPL | Nhiều-nhiều | Nằm trong ràng buộc bao phủ FEAT ở trên. |
| UC | FEAT | Truy vết ngược | Mỗi UC phải truy vết ngược về FEAT mà nó hiện thực hóa. |
| SUPL | FEAT | Truy vết ngược | Mỗi SUPL phải truy vết ngược về FEAT mà nó hỗ trợ. |
| UC | SCEN | Một-nhiều | Mỗi UC phải có ít nhất một SCEN tương ứng với luồng cơ bản. |

Các quy tắc bao phủ bắt buộc:

- mỗi **STRQ** ở trạng thái `Approved` phải truy vết tới ít nhất một **FEAT** hoặc **SUPL**;
- mỗi **FEAT** ở trạng thái `Approved` phải truy vết tới ít nhất một **UC** hoặc **SUPL**;
- mỗi **UC** phải có ít nhất một **SCEN** tương ứng với luồng cơ bản;
- **UC** và **SUPL** phải hỗ trợ truy vết ngược về **FEAT** mà chúng hiện thực hóa hoặc hỗ trợ.

#### 7.3.4.2. Loại requirement và quy tắc đặt requirement

| Loại requirement / artefact quản lý | Viết tắt | Vai trò | Nguồn chuẩn logic / vị trí baseline hiện tại |
| --- | --- | --- | --- |
| Stakeholder Request | STRQ | Ghi nhận nhu cầu và mong đợi của stakeholder trong problem domain | Nguồn chuẩn logic: STR; baseline hiện tại: `stakeholder-interviews.md` |
| Feature | FEAT | Biểu diễn các capability ở mức sản phẩm trong solution domain | Nguồn chuẩn logic: VIS; baseline hiện tại: `stakeholder-interviews.md` |
| Use Case | UC | Mô tả hành vi chức năng chi tiết theo tương tác giữa tác nhân và hệ thống | Nguồn chuẩn logic: UCS; trong baseline hiện tại danh mục/mapping tổng hợp có trong `requirement-modeling.md`, còn đặc tả chi tiết nằm trong các tài liệu UCS tương ứng |
| Scenario | SCEN | Mô tả các đường đi hợp lệ của từng use case | Nguồn chuẩn: các tài liệu UCS tương ứng |
| Supplementary Requirement | SUPL | Mô tả yêu cầu cross-cutting, NFR và constraint | Nguồn chuẩn: `supplementary-requirements.md` |
| Metric / Acceptance Criteria | Metric | Lượng hóa cách xác minh SUPL | Nguồn chuẩn: `supplementary-metrics.md` |

Quy tắc đặt requirement trong bộ tài liệu:

- Các mã **UI-**, **FR-**, **SR-**, **NFR-** trong SRS chỉ là mã trình bày cục bộ để nhóm nội dung; mã truy vết chuẩn dùng để quản lý requirement trong dự án vẫn là **STRQ**, **FEAT**, **UC**, **SCEN** và **SUPL**.
- Nội dung mô tả giao diện ở mức tổng quan phải nằm tại mục **7.2.1**; các yêu cầu giao diện có thể kiểm thử và áp dụng toàn hệ thống được tổng hợp tại mục **7.3.1** của SRS, với nguồn chuẩn ở **SS** trừ khi yêu cầu chỉ gắn với một **UCS** cụ thể.
- Các yêu cầu chỉ áp dụng cho một use case hoặc một bước luồng cụ thể phải có nguồn chuẩn tại tài liệu **UCS** tương ứng thay vì nâng lên mục **7.3.3**.
- Các yêu cầu áp dụng toàn hệ thống, cắt ngang nhiều use case, phi chức năng hoặc ràng buộc kỹ thuật/pháp lý phải có nguồn chuẩn tại **SS**; mục **7.3.3** của SRS chỉ tổng hợp các yêu cầu này ở mức hệ thống.

#### 7.3.4.3. Thuộc tính requirement tối thiểu

| Loại requirement | Thuộc tính tối thiểu phải quản lý |
| --- | --- |
| STRQ | Status, Priority, Benefit, Effort, Risk, Stability, Reason |
| FEAT | Status, Priority, Benefit, Effort, Risk, Stability, Difficulty, Target Release, Assigned To, Reason, Transformation |
| UC | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason, Actor |
| SUPL | Status, Priority, Benefit, Effort, Risk, Stability, Target Release, Reason |

#### 7.3.4.4. Báo cáo và chế độ xem requirement

Các chế độ xem requirement tối thiểu phải duy trì trong baseline dự án gồm:

- ma trận thuộc tính cho STRQ, FEAT, UC và SUPL;
- ma trận truy vết STRQ → FEAT;
- ma trận truy vết STRQ → SUPL;
- ma trận truy vết FEAT → UC;
- ma trận truy vết FEAT → SUPL;
- ma trận truy vết UC → Design, với neo thiết kế chính hiện tại là `class-diagram.md`;
- báo cáo gap cho **STRQ** ở trạng thái `Approved` chưa truy vết tới **FEAT/SUPL**, **FEAT** ở trạng thái `Approved` chưa truy vết tới **UC/SUPL**, **UC** chưa có **SCEN** luồng cơ bản, và **UC/SUPL** chưa có truy vết ngược về **FEAT**;
- cây truy vết cho phép xem phân rã từ **STRQ** xuống **FEAT**, **UC**, **SCEN** và các **SUPL** liên quan theo chuỗi truy vết đã định nghĩa.

#### 7.3.4.5. Giả định, phụ thuộc và ghi chú chuẩn hóa nguồn

- Trong baseline hiện tại, **FEAT 1.5** được truy vết tới **SUPL-DC01** như một ràng buộc kiến trúc; mục này không có **UC** riêng.
- Tài liệu **stakeholder-interviews.md** hiện là nguồn chuẩn chứa chung STRQ và nội dung FEAT, thay cho việc tách riêng tài liệu STR và VIS.
- Trong baseline SRS hợp nhất hiện tại, mã FEAT và mã UC dùng cho trình bày/truy vết trong SRS được chuẩn hóa theo danh mục đã tích hợp trong `output/final-report.md`, `output/khanh/uc-khanh.md` và `output/Tung/uc-tung.md`.
- Trong baseline hiện tại, `requirement-modeling.md` giữ vai trò nguồn logic cho mô hình tác nhân và mapping tổng quan; nội dung UCS chi tiết đang được phân bố giữa `output/final-report.md` (UC 4.1–4.24), `output/khanh/uc-khanh.md` (UC 4.38–4.50) và `output/Tung/uc-tung.md` (UC 4.25–4.37).
- Khi cần đối chiếu quy tắc truy vết, thuộc tính requirement và mapping tài liệu, **requirement-management-plan.md** là nguồn chuẩn quản lý requirement của dự án.
- Khi cần đối chiếu nguồn nội dung, tài liệu thu thập stakeholder là nguồn chuẩn cho STRQ/FEAT, bộ UCS là nguồn chuẩn cho hành vi chức năng chi tiết, và bộ SUPL cùng tài liệu độ đo là nguồn chuẩn cho các ngưỡng NFR.

### 7.4. Kết luận

> **Người thực hiện: Ngô Đức Nam Khánh**

SRS này tổng hợp phạm vi, hành vi chức năng, yêu cầu giao diện, yêu cầu bổ sung và các quy tắc quản lý requirement cho HRMS của Trường Đại học Thủy Lợi. Tài liệu là cơ sở để tiếp tục thiết kế, triển khai, kiểm thử và kiểm soát thay đổi yêu cầu trong các giai đoạn tiếp theo của dự án.
