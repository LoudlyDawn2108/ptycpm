# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng của Nguyễn Hồng Phúc

> Cột **FEAT liên quan** dùng để ghi các FEAT mà mỗi SUPL truy vết tới.

## 6.1. Yêu cầu về chức năng (Functionality)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-F01 | Hệ thống phải tự động ghi nhật ký cho mọi thao tác truy cập tài khoản, thay đổi dữ liệu, thay đổi trạng thái và thay đổi cấu hình, kèm thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. | FEAT 12.1 |
| 2 | SUPL-F02 | Khi tạo mới hồ sơ nhân sự, hệ thống phải tự động cấp một mã cán bộ duy nhất theo mẫu mã đang áp dụng tại thời điểm tạo. | FEAT 7.3 |
| 3 | SUPL-F03 | Hệ thống phải tự động đăng xuất phiên làm việc sau 30 phút không có tương tác của người dùng trên giao diện. | FEAT 1.3 |
| 4 | SUPL-F04 | Khi nhân sự được chuyển sang trạng thái thôi việc, hệ thống phải tự động khóa tài khoản liên kết của nhân sự đó. | FEAT 2.6, FEAT 7.5, FEAT 7.6 |
| 5 | SUPL-F05 | Hệ thống phải tự động chuyển hợp đồng từ trạng thái “Còn hiệu lực” sang “Chờ gia hạn” khi thời gian còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn của loại hợp đồng. | FEAT 5.1, FEAT 7.6, FEAT 9.5 |
| 6 | SUPL-F06 | Khi khóa đào tạo chuyển sang trạng thái “Đang đào tạo”, hệ thống phải tự động cập nhật mọi đăng ký của khóa đó đang ở trạng thái “Đã đăng ký” sang “Đang học”. | FEAT 8.2 |
| 7 | SUPL-F07 | Hệ thống phải cho phép chuyển loại phụ cấp và loại hợp đồng đã được tham chiếu trong dữ liệu nghiệp vụ sang trạng thái ngừng sử dụng hoặc kích hoạt lại mà không làm mất liên kết dữ liệu lịch sử; các danh mục này không được xóa. | FEAT 9.4, FEAT 9.5 |
| 8 | SUPL-F08 | Hệ thống phải lưu mật khẩu người dùng dưới dạng giá trị xác thực một chiều và không được lưu ở dạng văn bản thuần. | FEAT 1.1, FEAT 1.4 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-F01
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) Tỷ lệ bản ghi có đủ 9 trường bắt buộc. | Tính đúng đắn – Khả năng kiểm toán |
| **Tiêu chuẩn đáp ứng** | (1) 100% thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) 100% bản ghi có đủ 9/9 trường bắt buộc. | Tính đúng đắn – Khả năng kiểm toán |

#### SUPL-F02
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ mã cán bộ bị trùng; (2) Tỷ lệ mã được sinh đúng mẫu; (3) Tỷ lệ hồ sơ mới được cấp mã ngay khi tạo. | Tính đúng đắn |
| **Tiêu chuẩn đáp ứng** | (1) 0% mã cán bộ bị trùng; (2) 100% mã được sinh đúng mẫu đang áp dụng; (3) 100% hồ sơ mới được cấp mã ngay khi tạo thành công. | Tính đúng đắn |

#### SUPL-F03
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | Thời gian từ lần tương tác cuối cùng của người dùng đến khi hệ thống đăng xuất phiên làm việc. | Tính đúng đắn – Tự động hóa |
| **Tiêu chuẩn đáp ứng** | Hệ thống tự động đăng xuất sau 30 phút không có tương tác của người dùng trên giao diện, với sai số không quá ±30 giây. | Tính đúng đắn – Tự động hóa |

#### SUPL-F04
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Thời gian từ khi nhân sự được đánh dấu thôi việc đến khi tài khoản bị khóa; (2) Tỷ lệ tài khoản liên kết được khóa tự động đúng quy tắc. | Tính đúng đắn – Tự động hóa |
| **Tiêu chuẩn đáp ứng** | (1) Tài khoản bị khóa trong không quá 1 phút; (2) 100% tài khoản liên kết của nhân sự thôi việc bị khóa tự động. | Tính đúng đắn – Tự động hóa |

#### SUPL-F05
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái “Chờ gia hạn”; (2) Độ trễ từ thời điểm hợp đồng chạm ngưỡng đến khi trạng thái được cập nhật. | Tính đúng đắn – Tự động hóa |
| **Tiêu chuẩn đáp ứng** | (1) 100% hợp đồng đủ điều kiện được chuyển đúng trạng thái; (2) Việc cập nhật hoàn tất trong không quá 24 giờ kể từ thời điểm đủ điều kiện. | Tính đúng đắn – Tự động hóa |

#### SUPL-F06
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ đăng ký của khóa đang ở trạng thái “Đã đăng ký” được cập nhật đúng trạng thái; (2) Độ trễ từ thời điểm khóa đào tạo đổi trạng thái đến khi cập nhật xong toàn bộ đăng ký. | Tính đúng đắn – Tự động hóa |
| **Tiêu chuẩn đáp ứng** | (1) 100% đăng ký của khóa đang ở trạng thái “Đã đăng ký” được chuyển sang “Đang học”; (2) Hoàn tất cập nhật trong không quá 1 phút. | Tính đúng đắn – Tự động hóa |

#### SUPL-F07
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ danh mục đã được tham chiếu vẫn bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) Số danh mục đã được tham chiếu nhưng vẫn bị xóa. | Tính toàn vẹn |
| **Tiêu chuẩn đáp ứng** | (1) 100% danh mục đã được tham chiếu bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) 0 danh mục đã được tham chiếu bị xóa. | Tính toàn vẹn |

#### SUPL-F08
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ mật khẩu được lưu dưới dạng giá trị xác thực một chiều; (2) Số mật khẩu được lưu ở dạng văn bản thuần. | Bảo mật – Tính bí mật |
| **Tiêu chuẩn đáp ứng** | (1) 100% mật khẩu được lưu dưới dạng giá trị xác thực một chiều; (2) 0 mật khẩu được lưu ở dạng văn bản thuần. | Bảo mật – Tính bí mật |

## 6.2. Ràng buộc thiết kế (Design Constraints)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-DC01 | Hệ thống phải tổ chức frontend và backend theo mô hình client-server; mọi trao đổi dữ liệu nghiệp vụ giữa frontend và backend phải thực hiện thông qua các API do backend cung cấp. | FEAT 1.5 |
| 2 | SUPL-DC02 | Hệ thống phải biểu diễn cơ cấu tổ chức dưới dạng cây cha-con với một nút gốc duy nhất là Trường Đại học Thủy Lợi. | FEAT 3.1 |
| 3 | SUPL-DC03 | Hệ thống phải áp dụng phân quyền theo vai trò; mỗi chức năng và API chỉ cho phép truy cập bởi vai trò được cấp quyền. | FEAT 2.4 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-DC01
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ yêu cầu nghiệp vụ giữa frontend và backend đi qua API; (2) Số luồng nghiệp vụ truy cập dữ liệu mà không qua backend. | Ràng buộc thiết kế – Kiến trúc |
| **Tiêu chuẩn đáp ứng** | (1) 100% yêu cầu nghiệp vụ đi qua API; (2) 0 luồng nghiệp vụ truy cập dữ liệu trực tiếp mà không qua backend. | Ràng buộc thiết kế – Kiến trúc |

#### SUPL-DC02
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Số nút gốc trong cây tổ chức; (2) Số chu trình trong quan hệ cha-con; (3) Tỷ lệ đơn vị có liên kết cha-con hợp lệ. | Ràng buộc thiết kế – Mô hình dữ liệu |
| **Tiêu chuẩn đáp ứng** | (1) Có đúng 1 nút gốc là Trường Đại học Thủy Lợi; (2) 0 chu trình; (3) 100% đơn vị có liên kết cha-con hợp lệ. | Ràng buộc thiết kế – Mô hình dữ liệu |

#### SUPL-DC03
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Số vai trò được định nghĩa trong mô hình phân quyền; (2) Tỷ lệ chức năng và API có ma trận quyền rõ ràng; (3) Số trường hợp truy cập trái quyền. | Ràng buộc thiết kế – Phân quyền |
| **Tiêu chuẩn đáp ứng** | (1) Định nghĩa đúng 4 vai trò: Quản trị viên, TCCB, TCKT, Nhân sự; (2) 100% chức năng và API có ma trận quyền rõ ràng; (3) 0 trường hợp truy cập trái quyền. | Ràng buộc thiết kế – Phân quyền |

## 6.3. Ràng buộc pháp lý (Legal/Regulatory)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-LR01 | Hệ thống phải lưu căn cứ xử lý dữ liệu cá nhân cho từng trường hợp xử lý; nếu xử lý dựa trên sự đồng ý, hệ thống phải lưu hồ sơ đồng ý theo quy định trước khi xử lý và cho phép truy xuất hồ sơ đó để đối chiếu. | FEAT 7.3, FEAT 7.4, FEAT 11.1 |
| 2 | SUPL-LR02 | Hệ thống chỉ cho phép cấu hình và sử dụng loại hợp đồng, loại phụ cấp thuộc danh mục được nhà trường phê duyệt. | FEAT 9.4, FEAT 9.5 |
| 3 | SUPL-LR03 | Hệ thống phải áp dụng thời hạn lưu giữ theo từng loại hồ sơ nhân sự theo pháp luật hiện hành và quy định lưu trữ nội bộ được phê duyệt, đồng thời không cho phép xóa hồ sơ trước thời hạn đó. | FEAT 5.1, FEAT 6.1, FEAT 7.3, FEAT 7.4 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-LR01
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ trường hợp xử lý dữ liệu cá nhân có căn cứ xử lý được lưu; (2) Tỷ lệ trường hợp xử lý dựa trên sự đồng ý có hồ sơ đồng ý được lưu trước khi xử lý; (3) Tỷ lệ hồ sơ đồng ý có thể truy xuất để đối chiếu. | Ràng buộc pháp lý – Bảo vệ dữ liệu cá nhân |
| **Tiêu chuẩn đáp ứng** | (1) 100% trường hợp xử lý dữ liệu cá nhân có căn cứ xử lý được lưu; (2) 100% trường hợp xử lý dựa trên sự đồng ý có hồ sơ đồng ý được lưu trước khi xử lý; (3) 100% hồ sơ đồng ý có thể truy xuất để đối chiếu. | Ràng buộc pháp lý – Bảo vệ dữ liệu cá nhân |

#### SUPL-LR02
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ mục trong danh mục được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số mục ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. | Ràng buộc pháp lý – Danh mục nghiệp vụ |
| **Tiêu chuẩn đáp ứng** | (1) 100% mục trong danh mục được phê duyệt có thể cấu hình và sử dụng; (2) 0 mục ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. | Ràng buộc pháp lý – Danh mục nghiệp vụ |

#### SUPL-LR03
| Thuộc tính | Nội dung | Yếu tố chất lượng |
|---|---|---|
| **Độ đo yêu cầu** | (1) Tỷ lệ loại hồ sơ có thời hạn lưu giữ được cấu hình; (2) Tỷ lệ hồ sơ mẫu còn truy xuất được trong thời hạn lưu giữ; (3) Số trường hợp xóa hồ sơ trước hạn. | Ràng buộc pháp lý – Lưu trữ |
| **Tiêu chuẩn đáp ứng** | (1) 100% loại hồ sơ thuộc phạm vi yêu cầu có thời hạn lưu giữ được cấu hình; (2) 100% hồ sơ mẫu còn truy xuất được trong thời hạn lưu giữ; (3) 0 trường hợp xóa hồ sơ trước hạn. | Ràng buộc pháp lý – Lưu trữ |
