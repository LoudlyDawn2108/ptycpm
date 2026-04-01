# II. PHỎNG VẤN BÊN LIÊN QUAN

## 2.1. Bảng phân công thành viên

| Thành viên | STRQs | FEATs |
| --- | --- | --- |
| Nguyễn Hồng Phúc | 1–3 | 1.1–3.5 (15) |
| Nguyễn Hải Ninh | 4–6 | 4.1–6.2 (11) |
| Ngô Quang Tùng | 7–8 | 7.1–8.9 (13) |
| Ngô Đức Nam Khánh | 9–12 | 9.1–12.4 (14) |

## 2.2. Nội dung tổng hợp STRQ và FEAT theo thành viên

### 2.2.1. Phần đóng góp của Nguyễn Hồng Phúc (STRQ 1–3)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | \* Phân tách  \* Làm cho đầy đủ  \* Tổng quát hóa  \* Thêm chi tiết | \* **FEAT 1.1:** Hệ thống phải cho phép người dùng đăng nhập bằng tài khoản.  \* **FEAT 1.2:** Hệ thống phải cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng.  \* **FEAT 1.3:** Hệ thống phải tự động đăng xuất khỏi phiên làm việc nếu người dùng không có tương tác giao diện (nhấn chuột, nhập liệu, điều hướng) với trang web trong 30 phút.  \* **FEAT 1.4:** Hệ thống phải cho phép người dùng đổi mật khẩu tài khoản đang sử dụng. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 2.1:** Hệ thống phải cho phép quản trị viên tìm kiếm tài khoản người dùng.  \* **FEAT 2.2:** Hệ thống phải cho phép quản trị viên thêm mới tài khoản người dùng.  \* **FEAT 2.3:** Hệ thống phải cho phép quản trị viên sửa tài khoản người dùng.  \* **FEAT 2.4:** Hệ thống phải cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống tương ứng với các nhóm nghiệp vụ.  \* **FEAT 2.5:** Hệ thống phải cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Khóa/Mở khóa).  \* **FEAT 2.6:** Hệ thống phải tự động khóa tài khoản của nhân sự đã được đánh dấu thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | \* Phân tách  \* Làm cho đầy đủ  \* Thêm chi tiết | \* **FEAT 3.1:** Hệ thống phải cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi.  \* **FEAT 3.2:** Hệ thống phải cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự.  \* **FEAT 3.3:** Hệ thống phải cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự.  \* **FEAT 3.4:** Hệ thống phải cho phép quản trị viên và phòng TCCB thay đổi trạng thái của đơn vị tổ chức nhân sự (Trạng thái: Giải thể/Sáp nhập).  \* **FEAT 3.5:** Hệ thống phải cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. |

**Ghi chú thiết kế – FEAT 2.4:** “Nhóm nghiệp vụ” trong FEAT 2.4 chỉ các vai trò chức năng được hệ thống định nghĩa sẵn, tương ứng với phân nhóm tác nhân: Quản trị viên, Phòng TCCB, Phòng TCKT, Người dùng (Cán bộ/Giảng viên/Nhân viên). Mỗi nhóm nghiệp vụ quy định tập quyền truy cập các chức năng hệ thống khác nhau.

### 2.2.2. Phần đóng góp của Nguyễn Hải Ninh (STRQ 4–6)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 4:** Phòng TCCB có thể cấu hình lương, loại phụ cấp, loại hợp đồng. | \* Phân tách  \* Làm cho đầy đủ | \* **FEAT 4.1:** Hệ thống cho phép phòng TCCB thêm mới hệ số lương (Hệ số lương được thêm sẽ được dùng làm thông tin cho hồ sơ).  \* **FEAT 4.2:** Hệ thống cho phép phòng TCCB sửa thông tin đối với hệ số lương chưa được hồ sơ nào sử dụng, phục vụ sửa chữa nhập liệu lỗi.  \* **FEAT 4.4:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại phụ cấp.  \* **FEAT 4.5:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại hợp đồng. |

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 5:** Phòng TCKT và TCCB muốn thống kê chi tiết về nhân sự. | \* Phân tách  \* Thêm chi tiết | \* **FEAT 5.1:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê tổng quan nhân sự và biến động nhân sự.  \* **FEAT 5.2:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh.  \* **FEAT 5.3:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê hợp đồng, tình trạng làm việc, đánh giá cán bộ.  \* **FEAT 5.4:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê đào tạo, phát triển, bổ nhiệm nhân sự. |
| **STRQ 6:** Hệ thống yêu cầu tự động log dấu vết hoạt động người dùng (System Logging). | \* Phân tách  \* Thêm chi tiết | \* **FEAT 6.1:** Hệ thống tự động ghi vết tất cả các tác vụ truy cập tài khoản, thay đổi/cập nhật hệ thống hoặc dữ liệu.  \* **FEAT 6.2:** Hệ thống cho phép quản trị viên truy xuất xem và xuất Audit log (Nhật ký hệ thống) nhằm truy vết hoạt động. |

### 2.2.3. Phần đóng góp của Ngô Quang Tùng (STRQ 7–8)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 7:** Phòng TCCB có thể tạo hợp đồng lao động của nhân sự. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 7.1:** Hệ thống cho phép phòng TCCB tạo hợp đồng cho nhân sự không có hợp đồng hoặc cần gia hạn hợp đồng.  \* **FEAT 7.2:** Hệ thống cho phép phòng TCCB chi tiết hợp đồng lao động của nhân sự.  \* **FEAT 7.3:** Hệ thống cho phép phòng TCCB chỉnh sửa hợp đồng lao động của nhân sự khi hợp đồng chưa có hiệu lực.  \* **FEAT 7.4:** Hệ thống cho phép phòng TCCB chấm dứt hợp đồng lao động trước hạn của nhân sự. |
| **STRQ 8:** Phòng TCCB muốn quản lý hồ sơ nhân sự như thêm, sửa hồ sơ và cho phép đánh dấu thôi việc nếu nhân sự không còn làm việc, có thêm phương pháp tìm kiếm và lọc để tiện quản lý. | \* Phân tách  \* Làm rõ  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 8.1:** Hệ thống cho phép phòng TCCB và phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa.  \* **FEAT 8.2:** Hệ thống cho phép phòng TCCB và phòng TCKT lọc đa tiêu chí hồ sơ nhân sự.  \* **FEAT 8.3:** Hệ thống cho phép phòng TCCB thêm mới hồ sơ nhân sự (gồm nhập tay hoặc upload từ Excel).  \* **FEAT 8.4:** Hệ thống cho phép phòng TCCB chỉnh sửa hồ sơ nhân sự (thông tin cá nhân, trình độ học vấn, khen thưởng/kỷ luật, quá trình công tác, thông tin hợp đồng).  \* **FEAT 8.5:** Hệ thống cho phép phòng TCCB đánh dấu thôi việc nhân sự.  \* **FEAT 8.6:** Hệ thống tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn và không có gia hạn trong thời gian cho phép theo cấu hình loại hợp đồng.  \* **FEAT 8.7:** Hệ thống cho phép phòng TCCB và phòng TCKT xem chi tiết hồ sơ nhân sự theo từng chế độ xem.  \* **FEAT 8.8:** Hệ thống cho phép phòng TCCB và phòng TCKT in hoặc xuất Excel hồ sơ nhân sự.  \* **FEAT 8.9:** Hệ thống cho phép phòng TCCB cấu hình ẩn/hiện các mục khen thưởng, kỷ luật trong hồ sơ nhân sự đối với các vai trò không thuộc phòng TCCB. |

### 2.2.4. Phần đóng góp của Ngô Đức Nam Khánh (STRQ 9–12)

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 9:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 9.1:** Hệ thống phải cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự.  \* **FEAT 9.2:** Hệ thống phải cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác.  \* **FEAT 9.3:** Hệ thống phải cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 10:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | \* Phân tách  \* Thêm chi tiết  \* Làm cho đầy đủ | \* **FEAT 10.1:** Hệ thống phải cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật).  \* **FEAT 10.2:** Hệ thống phải cho phép phòng TCCB xem lịch sử đánh giá khen thưởng và kỷ luật của nhân sự.  \* **FEAT 10.3:** Hệ thống phải cho phép phòng TCCB tìm kiếm và lọc danh sách đánh giá khen thưởng/kỷ luật theo nhân sự, loại đánh giá, hoặc khoảng thời gian. |
| **STRQ 11:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | \* Phân tách  \* Làm cho đầy đủ  \* Thêm chi tiết | \* **FEAT 11.1:** Hệ thống phải cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ.  \* **FEAT 11.2:** Hệ thống phải cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành).  \* **FEAT 11.3:** Hệ thống phải cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký.  \* **FEAT 11.4:** Hệ thống phải cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
| **STRQ 12:** Người dùng phần mềm có thể xem hồ sơ cá nhân, xem thông tin đơn vị đang công tác và thực hiện các luồng tác vụ cá nhân. | \* Phân tách  \* Làm rõ  \* Thêm chi tiết | \* **FEAT 12.1:** Hệ thống phải cho phép người dùng xem thông tin cá nhân của bản thân.  \* **FEAT 12.2:** Hệ thống phải cho phép người dùng xem thông tin đơn vị mình đang công tác và cơ cấu các thành phần đơn vị trực thuộc.  \* **FEAT 12.3:** Hệ thống phải cho phép người dùng đăng ký hoặc hủy đăng ký tham gia khóa học/đào tạo được nhà trường phê duyệt mở.  \* **FEAT 12.4:** Hệ thống phải cho phép người dùng xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. |

**Ghi chú thiết kế – FEAT 12.3/12.4:** “Luồng tác vụ cá nhân” trong STRQ 12 được giới hạn phạm vi ở đăng ký đào tạo trong phiên bản hiện tại. Các tác vụ cá nhân khác (ví dụ: yêu cầu cập nhật thông tin, đề xuất nghỉ phép) có thể được bổ sung trong các phiên bản sau nếu có yêu cầu từ stakeholder.