# II. THU THẬP YÊU CẦU TỪ CÁC STAKEHOLDERS (Xác định STRQ, FEAT)

## 2.1. Xác định các STRQ, FEAT

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 1:** Cần hệ thống cho phép đăng nhập, đăng xuất, đổi mật khẩu tương tự các hệ thống phần mềm nhân sự khác, với tài khoản có phân quyền cho nhiều người dùng. | * Phân tách * Làm cho đầy đủ * Tổng quát hóa | * **FEAT 1.1:** Hệ thống cho phép người dùng đăng nhập bằng tài khoản. * **FEAT 1.2:** Hệ thống cho phép người dùng đăng xuất khỏi tài khoản đang sử dụng. * **FEAT 1.3:** Hệ thống tự động đăng xuất khỏi phiên làm việc nếu người dùng không thao tác với trang web trong 30 phút. * **FEAT 1.4:** Hệ thống cho phép người dùng đổi mật khẩu tài khoản đang sử dụng. |
| **STRQ 2:** Quản trị viên là người có thể quản lý tài khoản như thêm, sửa, khóa hoặc phân quyền người dùng. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 2.1:** Hệ thống cho phép quản trị viên tìm kiếm tài khoản người dùng. * **FEAT 2.2:** Hệ thống cho phép quản trị viên thêm mới tài khoản người dùng. * **FEAT 2.3:** Hệ thống cho phép quản trị viên sửa tài khoản người dùng. * **FEAT 2.4:** Hệ thống cho phép quản trị viên phân quyền cho tài khoản thành viên hệ thống tương ứng với các nhóm nghiệp vụ. * **FEAT 2.5:** Hệ thống cho phép quản trị viên thay đổi trạng thái của tài khoản người dùng (Trạng thái: Khóa/Mở khóa). * **FEAT 2.6:** Hệ thống tự động khóa tài khoản của nhân sự đã thôi việc. |
| **STRQ 3:** Quản trị viên và phòng TCCB có thể quản lý cơ cấu tổ chức, thêm vào các đơn vị mới, chỉnh sửa thông tin hoặc thông báo giải thể, sáp nhập đơn vị. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 3.1:** Hệ thống cung cấp cơ cấu tổ chức phân cấp đơn vị theo dạng cha-con có gốc là trường Đại học Thủy Lợi. * **FEAT 3.2:** Hệ thống cho phép quản trị viên và phòng TCCB thêm mới đơn vị tổ chức nhân sự. * **FEAT 3.3:** Hệ thống cho phép quản trị viên và phòng TCCB sửa thông tin đơn vị tổ chức nhân sự. * **FEAT 3.4:** Hệ thống cho phép quản trị viên và phòng TCCB thay đổi trạng thái của đơn vị tổ chức nhân sự (Trạng thái: Giải thể/Sáp nhập). * **FEAT 3.5:** Hệ thống cho phép quản trị viên và phòng TCCB xem chi tiết thông tin đơn vị tổ chức nhân sự. |
| **STRQ 4:** Phòng TCCB có thể điều chuyển và bổ nhiệm nhân sự vào các đơn vị. | * Phân tách * Thêm chi tiết * Làm cho đầy đủ | * **FEAT 4.1:** Hệ thống cho phép phòng TCCB bổ nhiệm nhân sự vào một đơn vị tổ chức nhân sự. * **FEAT 4.2:** Hệ thống cho phép phòng TCCB điều chuyển nhân sự sang đơn vị tổ chức nhân sự khác. * **FEAT 4.3:** Hệ thống cho phép phòng TCCB bãi nhiệm nhân sự khỏi đơn vị tổ chức đó. |
| **STRQ 5:** Phòng TCCB có thể tạo hợp đồng lao động của nhân sự. | * Thêm chi tiết | * **FEAT 5.1:** Hệ thống cho phép phòng TCCB tạo hợp đồng cho nhân sự không có hợp đồng hoặc cần gia hạn hợp đồng. |
| **STRQ 6:** Phòng TCCB có thể ghi nhận đánh giá nhân sự. | * Thêm chi tiết | * **FEAT 6.1:** Hệ thống cho phép phòng TCCB ghi đánh giá cho nhân sự (Loại đánh giá: Khen thưởng/Kỷ luật). |
| **STRQ 7:** Phòng TCCB muốn quản lý hồ sơ nhân sự như thêm, sửa hồ sơ và cho phép đánh dấu thôi việc nếu nhân sự không còn làm việc, có thêm phương pháp tìm kiếm và lọc để tiện quản lý. | * Phân tách * Làm cho rõ ràng * Thêm chi tiết * Làm cho đầy đủ * Làm rõ | * **FEAT 7.1:** Hệ thống cho phép phòng TCCB và phòng TCKT tìm kiếm hồ sơ nhân sự bằng nhiều từ khóa. * **FEAT 7.2:** Hệ thống cho phép phòng TCCB và phòng TCKT lọc đa tiêu chí hồ sơ nhân sự. * **FEAT 7.3:** Hệ thống cho phép phòng TCCB thêm mới hồ sơ nhân sự (gồm nhập tay hoặc upload từ Excel). * **FEAT 7.4:** Hệ thống cho phép phòng TCCB chỉnh sửa hồ sơ nhân sự (thông tin cá nhân, trình độ học vấn, khen thưởng/kỷ luật, quá trình công tác, thông tin hợp đồng), bao gồm ẩn/hiện các mục khen thưởng, kỷ luật đối với các vai trò khác. * **FEAT 7.5:** Hệ thống cho phép phòng TCCB đánh dấu thôi việc nhân sự. * **FEAT 7.6:** Hệ thống tự động đánh dấu thôi việc nhân sự khi hợp đồng hết hạn quá thời gian cho phép của loại hợp đồng. * **FEAT 7.7:** Hệ thống cho phép phòng TCCB và phòng TCKT xem chi tiết hồ sơ nhân sự theo từng chế độ xem. * **FEAT 7.8:** Hệ thống cho phép phòng TCCB và phòng TCKT in hoặc xuất Excel hồ sơ nhân sự. |
| **STRQ 8:** Phòng TCCB cần hệ thống cho phép mở khóa đào tạo, quản lý khóa đào tạo cho nhân sự. | * Phân tách * Làm cho đầy đủ * Thêm chi tiết | * **FEAT 8.1:** Hệ thống cho phép phòng TCCB mở khóa đào tạo (cấu hình chuyên sâu về thời gian, địa điểm, chứng chỉ) cho cán bộ. * **FEAT 8.2:** Hệ thống cho phép phòng TCCB chỉnh sửa khóa đào tạo đã mở cho cán bộ tùy theo trạng thái chưa diễn ra hay đang diễn ra, bao gồm thay đổi trạng thái khóa đào tạo (Đang mở đăng ký → Đang đào tạo → Đã hoàn thành). * **FEAT 8.3:** Hệ thống cho phép phòng TCCB xem thông tin khóa đào tạo đã mở cho cán bộ kèm danh sách người đã đăng ký. * **FEAT 8.4:** Hệ thống cho phép phòng TCCB ghi nhận kết quả đào tạo cho cán bộ đã tham gia và lưu trực tiếp chứng chỉ vào hồ sơ nhân sự. |
| **STRQ 9:** Phòng TCCB có thể cấu hình lương, loại phụ cấp, loại hợp đồng. | * Phân tách * Làm cho đầy đủ | * **FEAT 9.1:** Hệ thống cho phép phòng TCCB thêm mới hệ số lương (Hệ số lương được thêm sẽ được dùng làm thông tin cho hồ sơ). * **FEAT 9.2:** Hệ thống cho phép phòng TCCB sửa thông tin đối với hệ số lương mới được tạo phục vụ sửa chữa nhập liệu lỗi. * **FEAT 9.3:** Hệ thống cho phép phòng TCCB xóa hệ số lương khi không được hồ sơ nào sử dụng, hoặc thay đổi trạng thái (đưa vào trạng thái ngừng sử dụng hoặc kích hoạt lại) nếu đã được sử dụng. * **FEAT 9.4:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại phụ cấp. * **FEAT 9.5:** Hệ thống cho phép phòng TCCB cấu hình (Thêm/Sửa/Thay đổi trạng thái) danh mục loại hợp đồng. |

> **Ghi chú thiết kế – FEAT 9.4/9.5:** Danh mục loại phụ cấp và loại hợp đồng chỉ hỗ trợ thao tác "Thay đổi trạng thái" (chuyển đổi giữa "Đang sử dụng" và "Ngừng sử dụng") mà không hỗ trợ "Xóa" (khác với hệ số lương ở FEAT 9.3 có hỗ trợ xóa khi chưa được sử dụng). Thiết kế này nhằm đảm bảo tính toàn vẹn dữ liệu và phục vụ kiểm toán – các loại phụ cấp/hợp đồng đã từng được sử dụng trong hệ thống cần được lưu giữ lịch sử.

| Yêu cầu (STRQ) | Kỹ thuật xác định FEAT | Tính năng (FEAT) |
| --- | --- | --- |
| **STRQ 10:** Phòng TCKT và TCCB muốn thống kê chi tiết về nhân sự. | * Phân tách * Thêm chi tiết | * **FEAT 10.1:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê tổng quan nhân sự và biến động nhân sự. * **FEAT 10.2:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất cơ cấu nhân sự theo đơn vị, trình độ, học hàm, chức danh. * **FEAT 10.3:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê hợp đồng, tình trạng làm việc, đánh giá cán bộ. * **FEAT 10.4:** Hệ thống cho phép phòng TCCB và phòng TCKT xem và xuất thống kê đào tạo, phát triển, bổ nhiệm nhân sự. |
| **STRQ 11:** Người dùng phần mềm có thể xem hồ sơ cá nhân, xem thông tin đơn vị đang công tác và thực hiện các luồng tác vụ cá nhân. | * Phân tách * Làm cho rõ ràng * Thêm chi tiết | * **FEAT 11.1:** Hệ thống cho phép người dùng xem thông tin cá nhân của bản thân. * **FEAT 11.2:** Hệ thống cho phép người dùng xem thông tin đơn vị mình đang công tác và cơ cấu các thành phần đơn vị trực thuộc. * **FEAT 11.3:** Hệ thống cho phép người dùng đăng ký hoặc hủy đăng ký tham gia khóa học/đào tạo được nhà trường phê duyệt mở. * **FEAT 11.4:** Hệ thống cho phép người dùng xem danh sách các khóa đào tạo đã đăng ký và lịch sử đào tạo đã tham gia. |
| **STRQ 12:** Hệ thống yêu cầu tự động log dấu vết hoạt động người dùng (System Logging). | * Phân tách * Thêm chi tiết | * **FEAT 12.1:** Hệ thống tự động ghi vết tất cả các tác vụ truy cập tài khoản, thay đổi/cập nhật hệ thống hoặc dữ liệu. * **FEAT 12.2:** Hệ thống cho phép quản trị viên truy xuất xem và xuất Audit log (Nhật ký hệ thống) nhằm truy vết hoạt động. |

> **Ghi chú thiết kế – FEAT 7.1/7.2/7.7/7.8:** STRQ 7 chỉ đề cập phòng TCCB, nhưng các FEAT 7.1, 7.2, 7.7, 7.8 bổ sung thêm "phòng TCKT" với vai trò chỉ-đọc (tìm kiếm, lọc, xem, in/xuất) nhằm phục vụ nghiệp vụ đối soát lương – phụ cấp mà không cho phép phòng TCKT chỉnh sửa hồ sơ. Kỹ thuật áp dụng: *Làm cho đầy đủ* (Completion).

## 2.2. Ma trận thuộc tính STRQ

> Mô tả chi tiết của từng STRQ được trình bày tại Mục 2.1. Ý nghĩa các giá trị thuộc tính được định nghĩa tại Mục 1.8.2.

| STRQ | Status | Priority | Benefit | Risk | Stability | Effort (ngày-người) | Reason |
| --- | --- | --- | --- | --- | --- | ---: | --- |
| STRQ 1 | Approved | High | Critical | Low | High | 5 | Yêu cầu cơ bản — xác thực và bảo mật phiên làm việc |
| STRQ 2 | Approved | High | Critical | Low | High | 8 | Yêu cầu quản trị hệ thống — quản lý tài khoản và phân quyền |
| STRQ 3 | Approved | High | Critical | Medium | Medium | 10 | Phỏng vấn Phòng TCCB và Quản trị viên — quản lý cơ cấu tổ chức |
| STRQ 4 | Approved | High | Important | Medium | Medium | 5 | Phỏng vấn Phòng TCCB — nghiệp vụ bổ nhiệm và điều chuyển |
| STRQ 5 | Approved | High | Critical | Medium | Medium | 5 | Phỏng vấn Phòng TCCB — quản lý hợp đồng lao động |
| STRQ 6 | Approved | Medium | Important | Low | High | 3 | Phỏng vấn Phòng TCCB — đánh giá khen thưởng / kỷ luật |
| STRQ 7 | Approved | High | Critical | Medium | Medium | 20 | Phỏng vấn Phòng TCCB — quản lý toàn diện hồ sơ nhân sự |
| STRQ 8 | Approved | Medium | Important | Medium | Medium | 12 | Phỏng vấn Phòng TCCB — quản lý đào tạo và phát triển nhân sự |
| STRQ 9 | Approved | High | Important | Low | High | 8 | Phỏng vấn Phòng TCCB — cấu hình tham chiếu hệ thống (lương, phụ cấp, hợp đồng) |
| STRQ 10 | Approved | Medium | Important | Medium | Low | 10 | Phỏng vấn Phòng TCCB và Phòng TCKT — báo cáo thống kê phục vụ quản lý |
| STRQ 11 | Approved | Medium | Useful | Low | High | 6 | Phỏng vấn người dùng cuối — tự phục vụ thông tin cá nhân |
| STRQ 12 | Approved | High | Critical | Low | High | 5 | Yêu cầu bảo mật — ghi vết hoạt động hệ thống và kiểm toán |

## 2.3. Ma trận thuộc tính FEAT

> Mô tả chi tiết của từng FEAT được trình bày tại Mục 2.1. Ý nghĩa các giá trị thuộc tính được định nghĩa tại Mục 1.8.1. Cột "Assigned To" sử dụng tên nhóm chức năng — thay bằng tên cá nhân cụ thể khi có phân công chính thức.

| FEAT | Status | Priority | Benefit | Risk | Stability | Effort (ngày-người) | Target Release | Assigned To | Reason |
| --- | --- | --- | --- | --- | --- | ---: | --- | --- | --- |
| FEAT 1.1 | Approved | High | Critical | Low | High | 3 | Iteration 1 | Team 1 (BA) | STRQ 1 |
| FEAT 1.2 | Approved | High | Critical | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 1 |
| FEAT 1.3 | Approved | Medium | Important | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 1 |
| FEAT 1.4 | Approved | High | Critical | Low | High | 3 | Iteration 1 | Team 1 (BA) | STRQ 1 |
| FEAT 2.1 | Approved | High | Important | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 2 |
| FEAT 2.2 | Approved | High | Critical | Low | High | 3 | Iteration 1 | Team 1 (BA) | STRQ 2 |
| FEAT 2.3 | Approved | High | Critical | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 2 |
| FEAT 2.4 | Approved | High | Critical | Medium | Medium | 5 | Iteration 1 | Team 1 (BA) | STRQ 2 |
| FEAT 2.5 | Approved | High | Important | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 2 |
| FEAT 2.6 | Approved | Medium | Important | Medium | Medium | 3 | Iteration 2 | Team 1 (BA) | STRQ 2 |
| FEAT 3.1 | Approved | High | Critical | Medium | Medium | 5 | Iteration 1 | Team 1 (BA) | STRQ 3 |
| FEAT 3.2 | Approved | High | Critical | Low | High | 3 | Iteration 1 | Team 1 (BA) | STRQ 3 |
| FEAT 3.3 | Approved | High | Important | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 3 |
| FEAT 3.4 | Approved | Medium | Important | Medium | Medium | 3 | Iteration 1 | Team 1 (BA) | STRQ 3 |
| FEAT 3.5 | Approved | High | Important | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 3 |
| FEAT 4.1 | Approved | High | Critical | Medium | Medium | 3 | Iteration 2 | Team 1 (BA) | STRQ 4 |
| FEAT 4.2 | Approved | High | Critical | Medium | Medium | 2 | Iteration 2 | Team 1 (BA) | STRQ 4 |
| FEAT 4.3 | Approved | High | Important | Medium | Medium | 3 | Iteration 2 | Team 1 (BA) | STRQ 4 |
| FEAT 5.1 | Approved | High | Critical | Medium | Medium | 5 | Iteration 2 | Team 1 (BA) | STRQ 5 |
| FEAT 6.1 | Approved | Medium | Important | Low | High | 3 | Iteration 2 | Team 1 (BA) | STRQ 6 |
| FEAT 7.1 | Approved | High | Critical | Low | High | 3 | Iteration 2 | Team 1 (BA) | STRQ 7 |
| FEAT 7.2 | Approved | High | Important | Low | Medium | 3 | Iteration 2 | Team 1 (BA) | STRQ 7 |
| FEAT 7.3 | Approved | High | Critical | Medium | Medium | 8 | Iteration 2 | Team 1 (BA) | STRQ 7 |
| FEAT 7.4 | Approved | High | Critical | Medium | Medium | 8 | Iteration 2 | Team 1 (BA) | STRQ 7 |
| FEAT 7.5 | Approved | High | Important | Low | High | 2 | Iteration 2 | Team 1 (BA) | STRQ 7 |
| FEAT 7.6 | Approved | Medium | Important | Medium | Medium | 4 | Iteration 3 | Team 1 (BA) | STRQ 7 |
| FEAT 7.7 | Approved | High | Critical | Low | High | 3 | Iteration 2 | Team 1 (BA) | STRQ 7 |
| FEAT 7.8 | Approved | Medium | Important | Medium | High | 5 | Iteration 3 | Team 1 (BA) | STRQ 7 |
| FEAT 8.1 | Approved | Medium | Important | Medium | Medium | 5 | Iteration 3 | Team 1 (BA) | STRQ 8 |
| FEAT 8.2 | Approved | Medium | Important | Medium | Medium | 4 | Iteration 3 | Team 1 (BA) | STRQ 8 |
| FEAT 8.3 | Approved | Medium | Useful | Low | High | 2 | Iteration 3 | Team 1 (BA) | STRQ 8 |
| FEAT 8.4 | Approved | Medium | Important | Medium | Medium | 4 | Iteration 3 | Team 1 (BA) | STRQ 8 |
| FEAT 9.1 | Approved | High | Important | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 9 |
| FEAT 9.2 | Approved | High | Important | Low | High | 2 | Iteration 1 | Team 1 (BA) | STRQ 9 |
| FEAT 9.3 | Approved | High | Important | Low | High | 3 | Iteration 1 | Team 1 (BA) | STRQ 9 |
| FEAT 9.4 | Approved | High | Important | Low | High | 3 | Iteration 1 | Team 1 (BA) | STRQ 9 |
| FEAT 9.5 | Approved | High | Important | Low | High | 3 | Iteration 1 | Team 1 (BA) | STRQ 9 |
| FEAT 10.1 | Approved | Medium | Important | Medium | Low | 3 | Iteration 3 | Team 1 (BA) | STRQ 10 |
| FEAT 10.2 | Approved | Medium | Important | Medium | Low | 3 | Iteration 3 | Team 1 (BA) | STRQ 10 |
| FEAT 10.3 | Approved | Medium | Medium | Medium | Low | 2 | Iteration 3 | Team 1 (BA) | STRQ 10 |
| FEAT 10.4 | Approved | Medium | Low | Medium | Low | 2 | Iteration 3 | Team 1 (BA) | STRQ 10 |
| FEAT 11.1 | Approved | Medium | Useful | Low | High | 3 | Iteration 4 | Team 1 (BA) | STRQ 11 |
| FEAT 11.2 | Approved | Medium | Useful | Low | High | 2 | Iteration 4 | Team 1 (BA) | STRQ 11 |
| FEAT 11.3 | Approved | Medium | Useful | Low | High | 3 | Iteration 4 | Team 1 (BA) | STRQ 11 |
| FEAT 11.4 | Approved | Low | Useful | Low | High | 2 | Iteration 4 | Team 1 (BA) | STRQ 11 |
| FEAT 12.1 | Approved | High | Critical | Medium | High | 5 | Iteration 1 | Team 1 (BA) | STRQ 12 |
| FEAT 12.2 | Approved | High | Important | Low | High | 3 | Iteration 4 | Team 1 (BA) | STRQ 12 |

**Tổng hợp phân bổ theo iteration:**

| Iteration | Số FEAT | Tổng Effort (ngày-người) | Trọng tâm |
| --- | ---: | ---: | --- |
| Iteration 1 | 20 | 57 | Xác thực, quản lý tài khoản, cơ cấu tổ chức, danh mục cấu hình, hạ tầng ghi vết |
| Iteration 2 | 12 | 46 | Quản lý hồ sơ nhân sự, hợp đồng, đánh giá, điều chuyển / bổ nhiệm |
| Iteration 3 | 10 | 34 | Đào tạo, báo cáo thống kê, tính năng tự động, xuất dữ liệu |
| Iteration 4 | 5 | 13 | Tự phục vụ cá nhân, xem nhật ký hệ thống |
| **Tổng** | **47** | **150** | |
