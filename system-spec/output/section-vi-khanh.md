## 6.4. Yêu cầu về Khả dụng (Usability)

> Người thực hiện: Ngô Đức Nam Khánh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-U01 | Giao diện tiếng Việt và nhất quán | Usability – Tính nhất quán giao diện (Consistency) | Toàn bộ FEAT/UC |
| 2 | SUPL-U02 | Dễ học cho người dùng mới | Usability – Dễ học (Learnability) | Toàn bộ FEAT/UC |
| 3 | SUPL-U03 | Thông báo lỗi rõ ràng | Usability – Xử lý lỗi (Error Handling) | Toàn bộ FEAT/UC |
| 4 | SUPL-U04 | Hỗ trợ tìm kiếm và lọc đa tiêu chí | Usability – Hiệu quả thao tác (Efficiency) | Toàn bộ FEAT/UC |
| 5 | SUPL-U05 | Hiển thị ổn định trên desktop và tablet | Usability – Khả năng truy cập đa thiết bị (Accessibility) | Toàn bộ FEAT/UC |
| 6 | SUPL-U06 | Điều hướng nhanh bằng bàn phím và breadcrumb | Usability – Hiệu quả thao tác (Efficiency) | Toàn bộ FEAT/UC |
| 7 | SUPL-U07 | Xác nhận trước thao tác quan trọng | Usability – Ngăn ngừa lỗi (Error Prevention) | Toàn bộ FEAT/UC |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-U01: Giao diện tiếng Việt và nhất quán
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Tính nhất quán giao diện (Consistency) |
| **Mô tả yêu cầu** | 100% màn hình phải sử dụng Tiếng Việt, trừ thuật ngữ kỹ thuật; đồng thời bố cục, màu sắc và font chữ phải được áp dụng thống nhất trên toàn bộ hệ thống. |
| **Độ đo yêu cầu** | (1) Tỷ lệ màn hình sử dụng Tiếng Việt; (2) Số màn hình vi phạm design system về bố cục, màu sắc hoặc font chữ. |
| **Tiêu chuẩn đáp ứng** | (1) Tỷ lệ màn hình sử dụng Tiếng Việt = 100% (ngoại trừ thuật ngữ kỹ thuật thống nhất toàn hệ thống); (2) Số màn hình vi phạm design system = 0. |
| **Phương pháp đo** | Rà soát toàn bộ màn hình theo checklist UI/UX; đối chiếu nội dung hiển thị với bộ quy chuẩn giao diện và ghi nhận số màn hình vi phạm. |
| **Đại lượng thay thế (nếu cần)** | Số component sử dụng hardcoded style ngoài design token hoặc ngoài thư viện giao diện chuẩn của hệ thống. |

#### SUPL-U02: Dễ học cho người dùng mới
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Dễ học (Learnability) |
| **Mô tả yêu cầu** | Sau tối đa 2 giờ đào tạo hướng dẫn, ít nhất 95% người dùng mới thuộc phòng TCCB phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự; ít nhất 95% người dùng mới thuộc phòng TCKT phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. |
| **Độ đo yêu cầu** | (1) Thời gian đào tạo trung bình cho người dùng mới; (2) Tỷ lệ người dùng mới phòng TCCB hoàn thành bộ tác vụ tìm kiếm – xem chi tiết – cập nhật hồ sơ nhân sự; (3) Tỷ lệ người dùng mới phòng TCKT hoàn thành bộ tác vụ tìm kiếm – xem chi tiết – xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. |
| **Tiêu chuẩn đáp ứng** | (1) Thời gian đào tạo ≤ 2 giờ/người; (2) Tỷ lệ hoàn thành của nhóm TCCB ≥ 95%; (3) Tỷ lệ hoàn thành của nhóm TCKT ≥ 95%. |
| **Phương pháp đo** | Tổ chức usability test với người dùng mới đại diện cho hai phòng ban sau buổi hướng dẫn chuẩn; ghi nhận thời gian đào tạo, tỷ lệ hoàn thành tác vụ và số lần cần trợ giúp trực tiếp. |
| **Đại lượng thay thế (nếu cần)** | Khối lượng tài liệu/hướng dẫn đào tạo cho mỗi vai trò không vượt quá 30 trang để tránh tăng gánh nặng học sử dụng. |

#### SUPL-U03: Thông báo lỗi rõ ràng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Xử lý lỗi (Error Handling) |
| **Mô tả yêu cầu** | Mọi lỗi nhập liệu hoặc lỗi hệ thống phải hiển thị thông báo bằng Tiếng Việt, rõ ràng, mô tả nguyên nhân và hướng dẫn khắc phục. |
| **Độ đo yêu cầu** | (1) Tỷ lệ loại lỗi có thông báo bằng Tiếng Việt rõ ràng; (2) Tỷ lệ thông báo lỗi có nêu nguyên nhân; (3) Tỷ lệ thông báo lỗi có ít nhất 1 gợi ý khắc phục. |
| **Tiêu chuẩn đáp ứng** | (1) 100% lỗi validation, lỗi nghiệp vụ và lỗi hệ thống có thông báo bằng Tiếng Việt; (2) 100% thông báo lỗi nêu được nguyên nhân chính; (3) 100% thông báo lỗi có ít nhất 1 gợi ý khắc phục. |
| **Phương pháp đo** | Lập danh mục các lỗi điển hình theo từng nhóm, kích hoạt lỗi trên môi trường kiểm thử và đối chiếu nội dung thông báo với checklist: đúng tiếng Việt, có nguyên nhân, có hướng dẫn xử lý. |
| **Đại lượng thay thế (nếu cần)** | Số thông báo lỗi hiển thị bằng tiếng Anh hoặc chỉ hiển thị mã kỹ thuật = 0. |

#### SUPL-U04: Hỗ trợ tìm kiếm và lọc đa tiêu chí
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Các danh sách dữ liệu (nhân sự, hợp đồng, đơn vị) phải hỗ trợ tìm kiếm theo từ khóa và lọc đa tiêu chí để giảm thời gian thao tác. |
| **Độ đo yêu cầu** | (1) Số bước thao tác để tìm kiếm và mở chi tiết 1 hồ sơ nhân sự; (2) Số tiêu chí lọc có thể kết hợp đồng thời trên một danh sách dữ liệu. |
| **Tiêu chuẩn đáp ứng** | (1) Tìm kiếm và mở chi tiết 1 hồ sơ nhân sự trong ≤ 3 bước (nhập từ khóa → tìm kiếm → mở chi tiết); (2) Bộ lọc hỗ trợ kết hợp ≥ 3 tiêu chí đồng thời. |
| **Phương pháp đo** | Thực hiện walkthrough trên các màn hình danh sách chính, đếm số thao tác thực tế và kiểm tra khả năng kết hợp đồng thời các tiêu chí lọc trên cùng một truy vấn. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể đo trực tiếp qua thao tác người dùng trên giao diện. |

#### SUPL-U05: Hiển thị ổn định trên desktop và tablet
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Khả năng truy cập đa thiết bị (Accessibility) |
| **Mô tả yêu cầu** | Ở độ phân giải desktop từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang; trên tablet 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện các thao tác chính mà không cần phóng to. |
| **Độ đo yêu cầu** | (1) Tỷ lệ màn hình hiển thị đúng ở độ phân giải desktop ≥ 1366×768; (2) Tỷ lệ màn hình cho phép thực hiện thao tác chính trên tablet 1024×768 mà không cần phóng to. |
| **Tiêu chuẩn đáp ứng** | (1) Desktop Compatibility Rate = 100%; (2) Tablet Compatibility Rate ≥ 80%. |
| **Phương pháp đo** | Kiểm thử giao diện trên trình duyệt desktop chuẩn và thiết bị giả lập/tablet 1024×768; ghi nhận các lỗi cắt nội dung, chồng lấn thành phần, cuộn ngang và thao tác cần phóng to. |
| **Đại lượng thay thế (nếu cần)** | Hệ thống giao diện có tối thiểu 2 breakpoint rõ ràng cho desktop và tablet để hỗ trợ responsive layout. |

#### SUPL-U06: Điều hướng nhanh bằng bàn phím và breadcrumb
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập; trên 100% form có nút xác nhận mặc định, phím Enter phải kích hoạt nút đó; 100% trang phải hiển thị breadcrumb để người dùng quay lại cấp điều hướng trước. |
| **Độ đo yêu cầu** | (1) Tỷ lệ form nhập liệu hỗ trợ Tab navigation đúng thứ tự; (2) Tỷ lệ form có nút xác nhận mặc định hỗ trợ phím Enter; (3) Tỷ lệ trang có hiển thị breadcrumb và cho phép quay lại cấp điều hướng trước. |
| **Tiêu chuẩn đáp ứng** | (1) ≥ 90% form nhập liệu cho phép di chuyển bằng phím Tab theo đúng thứ tự trường nhập; (2) 100% form có nút xác nhận mặc định hỗ trợ phím Enter; (3) 100% trang hiển thị breadcrumb hợp lệ. |
| **Phương pháp đo** | Thực hiện kiểm thử thủ công bằng bàn phím trên toàn bộ form nhập liệu và trang chức năng; ghi nhận thứ tự focus, hành vi của phím Enter và sự hiện diện của breadcrumb. |
| **Đại lượng thay thế (nếu cần)** | Tỷ lệ trường nhập liệu có thứ tự focus được xác định rõ ràng trong thiết kế/triển khai ≥ 95%. |

#### SUPL-U07: Xác nhận trước thao tác quan trọng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Ngăn ngừa lỗi (Error Prevention) |
| **Mô tả yêu cầu** | Hệ thống hiển thị hộp thoại xác nhận trước các thao tác quan trọng như xóa dữ liệu, khóa tài khoản, đánh dấu thôi việc, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương. |
| **Độ đo yêu cầu** | Tỷ lệ thao tác quan trọng có hộp thoại xác nhận trước khi hệ thống thực thi thao tác. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác quan trọng có confirmation dialog; tối thiểu bao gồm: xóa dữ liệu, khóa tài khoản, đánh dấu thôi việc, thay đổi trạng thái đơn vị và chấm dứt hợp đồng lao động trước hạn (nếu chức năng được cung cấp trên hệ thống). |
| **Phương pháp đo** | Lập danh sách thao tác quan trọng theo nghiệp vụ, kích hoạt từng thao tác trên môi trường kiểm thử và kiểm tra sự xuất hiện của hộp thoại xác nhận trước khi dữ liệu bị thay đổi. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể kiểm thử trực tiếp theo từng thao tác trọng yếu. |

## 6.5. Yêu cầu về Hỗ trợ (Supportability)

> Người thực hiện: Ngô Đức Nam Khánh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-S01 | Kiến trúc module hóa | Supportability – Tính bảo trì, tính module hóa (Maintainability/Modularity) | Toàn bộ hệ thống |
| 2 | SUPL-S02 | Tài liệu kỹ thuật đầy đủ | Supportability – Khả năng hiểu và vận hành (Understandability) | Toàn bộ hệ thống |
| 3 | SUPL-S03 | Khả năng mở rộng danh mục cấu hình | Supportability – Tính linh hoạt cấu hình (Flexibility/Configurability) | Toàn bộ hệ thống |
| 4 | SUPL-S04 | Hỗ trợ gỡ lỗi (Debugging) | Supportability – Khả năng chẩn đoán và kiểm thử (Maintainability/Testability) | Toàn bộ hệ thống |
| 5 | SUPL-S05 | Khả năng mở rộng quy mô (Scalability) | Supportability – Khả năng mở rộng quy mô (Scalability) | Toàn bộ hệ thống |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-S01: Kiến trúc module hóa
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Tính bảo trì, tính module hóa (Maintainability/Modularity) |
| **Mô tả yêu cầu** | Hệ thống phải được tổ chức thành các module chức năng có giao diện tích hợp rõ ràng để có thể nâng cấp hoặc thay thế từng module mà không buộc sửa đổi toàn bộ hệ thống. |
| **Độ đo yêu cầu** | (1) Số module khác bị ảnh hưởng khi thay đổi 1 module; (2) Tỷ lệ giao diện tích hợp giữa các module được đặc tả rõ ràng và có thể kiểm thử độc lập. |
| **Tiêu chuẩn đáp ứng** | (1) Thay đổi 1 module không làm phát sinh thay đổi ở quá 1 module khác; (2) 100% giao diện tích hợp giữa các module được mô tả rõ ràng và kiểm thử độc lập; (3) Frontend và backend giao tiếp 100% qua giao diện API đã công bố. |
| **Phương pháp đo** | Phân tích dependency giữa các module, rà soát tài liệu interface và thực hiện impact analysis khi sửa đổi thử nghiệm một module chức năng. |
| **Đại lượng thay thế (nếu cần)** | Số dependency cross-module ngoài interface công khai phải ở mức tối thiểu và được kiểm soát qua báo cáo phân tích phụ thuộc. |

#### SUPL-S02: Tài liệu kỹ thuật đầy đủ
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Khả năng hiểu và vận hành (Understandability) |
| **Mô tả yêu cầu** | Cung cấp tài liệu API cho backend, hướng dẫn triển khai và hướng dẫn sử dụng cho từng vai trò. |
| **Độ đo yêu cầu** | (1) Tỷ lệ API endpoint backend có tài liệu mô tả đầy đủ phương thức, URL, tham số, dữ liệu trả về và mã lỗi; (2) Tỷ lệ vai trò người dùng có hướng dẫn sử dụng riêng cho các chức năng chính; (3) Tỷ lệ nội dung bắt buộc xuất hiện trong tài liệu triển khai. |
| **Tiêu chuẩn đáp ứng** | (1) ≥ 90% API endpoint backend có tài liệu đầy đủ; (2) 100% vai trò sử dụng hệ thống có hướng dẫn sử dụng tương ứng; (3) 100% tài liệu triển khai có tối thiểu các mục: yêu cầu môi trường, cài đặt, cấu hình, khởi động, sao lưu/khôi phục và xử lý lỗi thường gặp. |
| **Phương pháp đo** | Đối chiếu danh mục endpoint thực tế với bộ tài liệu API; rà soát tài liệu theo checklist vai trò và checklist triển khai trước nghiệm thu. |
| **Đại lượng thay thế (nếu cần)** | Số endpoint chưa được tài liệu hóa và số vai trò chưa có hướng dẫn sử dụng riêng. |

#### SUPL-S03: Khả năng mở rộng danh mục cấu hình
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Tính linh hoạt cấu hình (Flexibility/Configurability) |
| **Mô tả yêu cầu** | Hệ thống cho phép mở rộng các danh mục cấu hình (loại phụ cấp, loại hợp đồng, hệ số lương) mà không cần thay đổi mã nguồn. |
| **Độ đo yêu cầu** | (1) Số loại danh mục cấu hình có thể mở rộng qua giao diện quản trị; (2) Số dòng mã nguồn phải sửa khi thêm một danh mục mới; (3) Khả năng quản trị các cấu hình hiển thị/danh mục tương tự qua giao diện. |
| **Tiêu chuẩn đáp ứng** | (1) Có ít nhất 3 loại danh mục master data mở rộng được qua giao diện quản trị: hệ số lương, loại phụ cấp, loại hợp đồng; (2) Số dòng mã nguồn cần sửa khi thêm danh mục mới = 0; (3) Các cấu hình hiển thị hoặc danh mục tương tự cũng phải được quản trị qua UI thay vì sửa code trực tiếp. |
| **Phương pháp đo** | Thực hiện thử nghiệm thêm mới/sửa danh mục cấu hình trên giao diện quản trị và kiểm tra nhật ký thay đổi mã nguồn trong quá trình cấu hình. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể kiểm chứng trực tiếp qua thao tác cấu hình trên hệ thống. |

#### SUPL-S04: Hỗ trợ gỡ lỗi (Debugging)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Khả năng chẩn đoán và kiểm thử (Maintainability/Testability) |
| **Mô tả yêu cầu** | Hệ thống ghi log lỗi phía server theo nhiều cấp độ (ERROR, WARNING, INFO, DEBUG). Log phải bao gồm timestamp, request ID, stack trace. |
| **Độ đo yêu cầu** | (1) Số cấp độ log được hệ thống hỗ trợ; (2) Tỷ lệ log lỗi mức ERROR chứa đủ timestamp, request ID và stack trace; (3) Tỷ lệ tình huống lỗi server được ghi nhận thành log phục vụ truy vết. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 4 cấp độ log: ERROR, WARNING, INFO, DEBUG; (2) 100% log mức ERROR có đủ timestamp, request ID và stack trace; (3) 100% lỗi server được kiểm thử phải sinh log lỗi tương ứng để phục vụ gỡ lỗi. |
| **Phương pháp đo** | Kích hoạt các tình huống lỗi điển hình trên môi trường kiểm thử, trích xuất log server và đối chiếu từng bản ghi với checklist trường thông tin bắt buộc và cấp độ log. |
| **Đại lượng thay thế (nếu cần)** | Số log ERROR thiếu một trong các trường bắt buộc (timestamp, request ID, stack trace) phải bằng 0. |

#### SUPL-S05: Khả năng mở rộng quy mô (Scalability)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Khả năng mở rộng quy mô (Scalability) |
| **Mô tả yêu cầu** | Hệ thống phải duy trì đầy đủ chức năng khi năng lực xử lý được mở rộng bằng cách bổ sung thêm nút ứng dụng trong cùng một môi trường khai thác. |
| **Độ đo yêu cầu** | (1) Số nút ứng dụng có thể vận hành song song trong cùng môi trường; (2) Tỷ lệ request liên tiếp của cùng người dùng hoạt động đúng khi được phân phối qua các nút khác nhau; (3) Tỷ lệ ca kiểm thử smoke test chức năng chính vẫn đạt khi hệ thống được scale-out. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 2 nút ứng dụng chạy song song trong cùng môi trường; (2) 100% request liên tiếp của cùng người dùng hoạt động đúng khi đi qua các nút khác nhau; (3) 100% ca smoke test của các chức năng chính vẫn đạt sau khi bổ sung nút ứng dụng. |
| **Phương pháp đo** | Triển khai thử nghiệm cấu hình nhiều nút ứng dụng, sử dụng load balancer để phân phối request và chạy bộ smoke test/regression cho các chức năng chính của hệ thống. |
| **Đại lượng thay thế (nếu cần)** | Số lỗi phiên làm việc hoặc lỗi điều hướng phát sinh khi request được chuyển giữa các nút ứng dụng phải bằng 0. |
