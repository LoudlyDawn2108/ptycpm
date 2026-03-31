# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng của Nguyễn Hồng Phúc

> Cột **FEAT liên quan** dùng để ghi FEAT duy nhất mà mỗi SUPL truy vết tới.

## 6.1. Yêu cầu về chức năng (Functionality)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-F01 | Hệ thống phải tự động ghi nhật ký cho mọi thao tác truy cập tài khoản, thay đổi dữ liệu, thay đổi trạng thái và thay đổi cấu hình, kèm thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả chi tiết và địa chỉ IP. | FEAT 12.1 |
| 2 | SUPL-F02 | Khi tạo mới hồ sơ nhân sự, hệ thống phải tự động cấp một mã cán bộ duy nhất theo mẫu mã đang được cấu hình áp dụng toàn hệ thống tại thời điểm tạo hồ sơ. | FEAT 7.3 |
| 3 | SUPL-F03 | Hệ thống phải tự động đăng xuất phiên làm việc sau 30 phút không có tương tác của người dùng trên giao diện. | FEAT 1.3 |
| 4 | SUPL-F04 | Khi nhân sự được chuyển sang trạng thái thôi việc, hệ thống phải tự động khóa tài khoản liên kết của nhân sự đó. | FEAT 2.6 |
| 5 | SUPL-F05 | Hệ thống phải tự động chuyển hợp đồng từ trạng thái "Còn hiệu lực" sang "Chờ gia hạn" khi thời hạn còn lại nhỏ hơn hoặc bằng ngưỡng chờ gia hạn được cấu hình. | FEAT 5.1 |
| 6 | SUPL-F06 | Khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang trạng thái "Đang đào tạo", hệ thống phải tự động cập nhật tất cả đăng ký tương ứng từ trạng thái "Đã đăng ký" sang "Đang học". | FEAT 8.2 |
| 7 | SUPL-F07 | Hệ thống phải cho phép chuyển loại phụ cấp đã được tham chiếu trong dữ liệu nghiệp vụ sang trạng thái ngừng sử dụng hoặc kích hoạt lại mà không làm mất liên kết dữ liệu lịch sử; loại phụ cấp đã được tham chiếu không được xóa. | FEAT 9.4 |
| 8 | SUPL-F08 | Hệ thống phải lưu trữ mật khẩu người dùng dưới dạng không thể khôi phục nguyên văn và không được lưu mật khẩu ở dạng văn bản thuần. | FEAT 1.4 |
| 9 | SUPL-F09 | Hệ thống phải cho phép chuyển loại hợp đồng đã được tham chiếu trong dữ liệu nghiệp vụ sang trạng thái ngừng sử dụng hoặc kích hoạt lại mà không làm mất liên kết dữ liệu lịch sử; loại hợp đồng đã được tham chiếu không được xóa. | FEAT 9.5 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-F01
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính đúng đắn – Khả năng kiểm toán |
| **Độ đo yêu cầu** | (1) Tỷ lệ thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) Tỷ lệ bản ghi có đủ 9 trường bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 100% thao tác thuộc phạm vi yêu cầu có bản ghi log; (2) 100% bản ghi có đủ 9/9 trường bắt buộc. |

#### SUPL-F02
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính đúng đắn |
| **Độ đo yêu cầu** | (1) Tỷ lệ mã cán bộ bị trùng; (2) Tỷ lệ mã được sinh đúng mẫu; (3) Tỷ lệ hồ sơ mới được cấp mã ngay khi tạo. |
| **Tiêu chuẩn đáp ứng** | (1) 0% mã cán bộ bị trùng; (2) 100% mã được sinh đúng mẫu đang áp dụng; (3) 100% hồ sơ mới được cấp mã ngay khi tạo thành công. |

#### SUPL-F03
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính đúng đắn – Tự động hóa |
| **Độ đo yêu cầu** | Thời gian từ lần tương tác cuối cùng của người dùng đến khi hệ thống đăng xuất phiên làm việc. |
| **Tiêu chuẩn đáp ứng** | Hệ thống tự động đăng xuất sau 30 phút không có tương tác của người dùng trên giao diện, với sai số không quá ±30 giây. |

#### SUPL-F04
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính đúng đắn – Tự động hóa |
| **Độ đo yêu cầu** | (1) Thời gian từ khi nhân sự được đánh dấu thôi việc đến khi tài khoản bị khóa; (2) Tỷ lệ tài khoản liên kết được khóa tự động đúng quy tắc. |
| **Tiêu chuẩn đáp ứng** | (1) Tài khoản bị khóa trong không quá 1 phút; (2) 100% tài khoản liên kết của nhân sự thôi việc bị khóa tự động. |

#### SUPL-F05
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính đúng đắn – Tự động hóa |
| **Độ đo yêu cầu** | (1) Tỷ lệ hợp đồng đủ điều kiện được chuyển sang trạng thái "Chờ gia hạn"; (2) Độ trễ từ thời điểm hợp đồng chạm ngưỡng đến khi trạng thái được cập nhật. |
| **Tiêu chuẩn đáp ứng** | (1) 100% hợp đồng đủ điều kiện được chuyển đúng trạng thái; (2) Việc cập nhật hoàn tất trong không quá 24 giờ kể từ thời điểm đủ điều kiện. |

#### SUPL-F06
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính đúng đắn – Tự động hóa |
| **Độ đo yêu cầu** | (1) Tỷ lệ đăng ký của khóa đang ở trạng thái "Đã đăng ký" được cập nhật đúng trạng thái khi khóa đào tạo chuyển từ trạng thái "Đang mở đăng ký" sang "Đang đào tạo"; (2) Độ trễ từ thời điểm khóa đào tạo đổi trạng thái đến khi cập nhật xong toàn bộ đăng ký. |
| **Tiêu chuẩn đáp ứng** | (1) 100% đăng ký của khóa đang ở trạng thái "Đã đăng ký" được chuyển sang "Đang học"; (2) Hoàn tất cập nhật trong không quá 1 phút. |

#### SUPL-F07
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính toàn vẹn |
| **Độ đo yêu cầu** | (1) Tỷ lệ loại phụ cấp đã được tham chiếu vẫn bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) Số loại phụ cấp đã được tham chiếu nhưng vẫn bị xóa. |
| **Tiêu chuẩn đáp ứng** | (1) 100% loại phụ cấp đã được tham chiếu bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) 0 loại phụ cấp đã được tham chiếu bị xóa. |

#### SUPL-F08
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Bảo mật – Tính bí mật |
| **Độ đo yêu cầu** | (1) Tỷ lệ mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; (2) Số mật khẩu được lưu ở dạng văn bản thuần. |
| **Tiêu chuẩn đáp ứng** | (1) 100% mật khẩu được lưu ở dạng không thể khôi phục nguyên văn; (2) 0 mật khẩu được lưu ở dạng văn bản thuần. |

#### SUPL-F09
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Tính toàn vẹn |
| **Độ đo yêu cầu** | (1) Tỷ lệ loại hợp đồng đã được tham chiếu vẫn bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) Số loại hợp đồng đã được tham chiếu nhưng vẫn bị xóa. |
| **Tiêu chuẩn đáp ứng** | (1) 100% loại hợp đồng đã được tham chiếu bảo toàn liên kết dữ liệu lịch sử sau khi ngừng sử dụng hoặc kích hoạt lại; (2) 0 loại hợp đồng đã được tham chiếu bị xóa. |

## 6.2. Ràng buộc thiết kế (Design Constraints)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-DC01 | Hệ thống phải xây dựng theo mô hình Client-Server, frontend dạng SPA (Single Page Application) giao tiếp với backend qua RESTful API. | FEAT 1.5 |
| 2 | SUPL-DC02 | Hệ thống phải biểu diễn cơ cấu tổ chức dưới dạng cây cha-con với một nút gốc duy nhất là Trường Đại học Thủy Lợi. | FEAT 3.1 |
| 3 | SUPL-DC03 | Hệ thống phải áp dụng phân quyền theo vai trò; mỗi chức năng và API chỉ cho phép truy cập bởi vai trò được cấp quyền. | FEAT 2.4 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-DC01
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Portability – Kiến trúc |
| **Độ đo yêu cầu** | (1) Số endpoint giao tiếp client-server không sử dụng RESTful API; (2) Số trang frontend yêu cầu full-page reload (ngoại trừ lần tải đầu tiên). |
| **Tiêu chuẩn đáp ứng** | (1) 0 endpoint giao tiếp client-server ngoài RESTful API (JSON); (2) 0 trang frontend yêu cầu full-page reload (ngoại trừ lần tải đầu tiên). |

#### SUPL-DC02
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc thiết kế – Mô hình dữ liệu |
| **Độ đo yêu cầu** | (1) Số nút gốc trong cây tổ chức; (2) Số chu trình trong quan hệ cha-con; (3) Tỷ lệ đơn vị có liên kết cha-con hợp lệ. |
| **Tiêu chuẩn đáp ứng** | (1) Có đúng 1 nút gốc là Trường Đại học Thủy Lợi; (2) 0 chu trình; (3) 100% đơn vị có liên kết cha-con hợp lệ. |

#### SUPL-DC03
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc thiết kế – Phân quyền |
| **Độ đo yêu cầu** | (1) Số vai trò được định nghĩa trong mô hình phân quyền; (2) Tỷ lệ chức năng và API có ma trận quyền rõ ràng; (3) Số trường hợp truy cập trái quyền. |
| **Tiêu chuẩn đáp ứng** | (1) Định nghĩa đúng 4 vai trò: Quản trị viên, TCCB, TCKT, Nhân sự; (2) 100% chức năng và API có ma trận quyền rõ ràng; (3) 0 trường hợp truy cập trái quyền. |

## 6.3. Ràng buộc pháp lý (Legal/Regulatory)

> Người thực hiện: Nguyễn Hồng Phúc

### Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-LR01 | Hệ thống phải cho phép ghi nhận, xem lịch sử và thu hồi sự đồng ý thu thập dữ liệu cá nhân cho từng cán bộ, theo Nghị định 13/2023/NĐ-CP. | FEAT 13.1 |
| 2 | SUPL-LR02 | Hệ thống chỉ cho phép cấu hình và sử dụng loại hợp đồng thuộc danh mục được nhà trường phê duyệt. | FEAT 9.5 |
| 3 | SUPL-LR03 | Hồ sơ nhân sự phải được lưu trữ tối thiểu 75 năm kể từ ngày tạo hồ sơ. | FEAT 7.3 |
| 4 | SUPL-LR04 | Hệ thống phải xử lý yêu cầu ẩn danh hóa dữ liệu cá nhân (thay thế thông tin định danh bằng dữ liệu ẩn danh) khi có yêu cầu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên, theo Nghị định 13/2023/NĐ-CP. | FEAT 13.2 |
| 5 | SUPL-LR05 | Hệ thống chỉ cho phép cấu hình và sử dụng loại phụ cấp thuộc danh mục được nhà trường phê duyệt. | FEAT 9.4 |
| 6 | SUPL-LR06 | Hợp đồng lao động phải được lưu trữ tối thiểu 10 năm sau khi hợp đồng chấm dứt. | FEAT 5.1 |
| 7 | SUPL-LR07 | Lịch sử đánh giá khen thưởng/kỷ luật phải được lưu trữ tối thiểu 10 năm kể từ bản ghi đánh giá cuối cùng. | FEAT 6.1 |

### Độ đo và tiêu chuẩn đáp ứng

#### SUPL-LR01
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc pháp lý – Bảo vệ dữ liệu |
| **Độ đo yêu cầu** | (1) Tỷ lệ hồ sơ nhân sự có bản ghi đồng ý hợp lệ trước khi thu thập dữ liệu cá nhân; (2) Số thao tác ghi nhận, xem lịch sử, thu hồi đồng ý không khả dụng trên giao diện. |
| **Tiêu chuẩn đáp ứng** | (1) 100% hồ sơ nhân sự có bản ghi đồng ý hợp lệ trước khi thu thập dữ liệu cá nhân; (2) 0 thao tác ghi nhận, xem lịch sử, thu hồi đồng ý bị thiếu trên giao diện. |

#### SUPL-LR02
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc pháp lý – Danh mục nghiệp vụ |
| **Độ đo yêu cầu** | (1) Tỷ lệ loại hợp đồng trong danh mục được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số loại hợp đồng ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. |
| **Tiêu chuẩn đáp ứng** | (1) 100% loại hợp đồng trong danh mục được phê duyệt có thể cấu hình và sử dụng; (2) 0 loại hợp đồng ngoài danh mục được phê duyệt được phép sử dụng. |

#### SUPL-LR03
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc pháp lý – Lưu trữ |
| **Độ đo yêu cầu** | (1) Số hồ sơ nhân sự bị xóa hoặc mất trước 75 năm kể từ ngày tạo; (2) Số thao tác xóa hồ sơ nhân sự chưa hết thời hạn lưu trữ không bị hệ thống chặn. |
| **Tiêu chuẩn đáp ứng** | (1) 0 hồ sơ nhân sự bị xóa hoặc mất trước 75 năm; (2) 0 thao tác xóa hồ sơ nhân sự chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |

#### SUPL-LR04
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc pháp lý – Bảo vệ dữ liệu |
| **Độ đo yêu cầu** | (1) Tỷ lệ yêu cầu ẩn danh hóa dữ liệu hợp lệ từ chủ thể dữ liệu hoặc quản trị viên được thực hiện thành công và có lưu vết xử lý; (2) Số trường hợp thông tin định danh chưa được thay thế bằng dữ liệu ẩn danh sau khi yêu cầu hợp lệ đã được xử lý. |
| **Tiêu chuẩn đáp ứng** | (1) 100% yêu cầu ẩn danh hóa hợp lệ được thực hiện thành công và lưu vết xử lý; (2) 0 trường hợp thông tin định danh chưa được thay thế sau khi yêu cầu hợp lệ đã được xử lý. |

#### SUPL-LR05
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc pháp lý – Danh mục nghiệp vụ |
| **Độ đo yêu cầu** | (1) Tỷ lệ loại phụ cấp trong danh mục được phê duyệt có thể cấu hình và sử dụng trên hệ thống; (2) Số loại phụ cấp ngoài danh mục được phê duyệt nhưng vẫn được phép sử dụng. |
| **Tiêu chuẩn đáp ứng** | (1) 100% loại phụ cấp trong danh mục được phê duyệt có thể cấu hình và sử dụng; (2) 0 loại phụ cấp ngoài danh mục được phê duyệt được phép sử dụng. |

#### SUPL-LR06
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc pháp lý – Lưu trữ |
| **Độ đo yêu cầu** | (1) Số hợp đồng lao động bị xóa hoặc mất trước 10 năm kể từ ngày chấm dứt hợp đồng; (2) Số thao tác xóa hợp đồng chưa hết thời hạn lưu trữ không bị hệ thống chặn. |
| **Tiêu chuẩn đáp ứng** | (1) 0 hợp đồng lao động bị xóa hoặc mất trước 10 năm kể từ ngày chấm dứt; (2) 0 thao tác xóa hợp đồng chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |

#### SUPL-LR07
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Ràng buộc pháp lý – Lưu trữ |
| **Độ đo yêu cầu** | (1) Số bản ghi đánh giá khen thưởng/kỷ luật bị xóa hoặc mất trước 10 năm kể từ bản ghi đánh giá cuối cùng; (2) Số thao tác xóa bản ghi đánh giá chưa hết thời hạn lưu trữ không bị hệ thống chặn. |
| **Tiêu chuẩn đáp ứng** | (1) 0 bản ghi đánh giá bị xóa hoặc mất trước 10 năm; (2) 0 thao tác xóa bản ghi đánh giá chưa hết thời hạn lưu trữ mà không bị hệ thống chặn. |
