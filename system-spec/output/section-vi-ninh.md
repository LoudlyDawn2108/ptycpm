## 6.4. Yêu cầu về Khả dụng (Usability)

> Người thực hiện: Nguyễn Hải Ninh

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
| **Độ đo yêu cầu** | (1) Tỷ lệ nhãn, menu, thông báo và nút thao tác trên các màn hình nghiệp vụ chính sử dụng Tiếng Việt; (2) Tỷ lệ màn hình nghiệp vụ chính đạt checklist design system về bố cục, màu sắc, font chữ và cách đặt tên; (3) Số vi phạm nghiêm trọng làm người dùng hiểu sai chức năng. |
| **Tiêu chuẩn đáp ứng** | (1) 100% nhãn, menu, thông báo và nút thao tác trên các màn hình nghiệp vụ chính dùng Tiếng Việt, trừ thuật ngữ kỹ thuật thống nhất; (2) ≥ 95% màn hình nghiệp vụ chính đạt checklist design system; (3) 0 vi phạm nghiêm trọng. |
| **Phương pháp đo** | Rà soát toàn bộ màn hình nghiệp vụ chính theo checklist UI/UX; đối chiếu ngôn ngữ hiển thị và bộ quy chuẩn giao diện trước nghiệm thu. |
| **Lý do chọn độ đo** | Theo heuristic **Consistency and Standards** và **Match Between the System and the Real World** của Nielsen Norman Group, giao diện phải dùng ngôn ngữ quen thuộc và nhất quán để giảm tải nhận thức. Với HRMS của trường đại học, người dùng chủ yếu là cán bộ hành chính nên ngưỡng **100% cho nhãn/menu/thông báo ở màn hình chính** là cần thiết; còn ngưỡng **≥ 95% tuân thủ design system** thực tế hơn so với ép 100% toàn bộ màn hình vì vẫn có thể tồn tại vài thành phần kỹ thuật hoặc thư viện dùng thuật ngữ gốc. |
| **Đại lượng thay thế (nếu cần)** | Số component sử dụng hardcoded style ngoài design token hoặc ngoài thư viện giao diện chuẩn của hệ thống. |

#### SUPL-U02: Dễ học cho người dùng mới
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Dễ học (Learnability) |
| **Mô tả yêu cầu** | Sau tối đa 2 giờ đào tạo hướng dẫn, ít nhất 95% người dùng mới thuộc phòng TCCB phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và cập nhật hồ sơ nhân sự; ít nhất 95% người dùng mới thuộc phòng TCKT phải hoàn thành được các tác vụ tìm kiếm, xem chi tiết và xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. |
| **Độ đo yêu cầu** | (1) Thời gian đào tạo trung bình cho người dùng mới; (2) Tỷ lệ người dùng mới phòng TCCB hoàn thành bộ tác vụ tìm kiếm – xem chi tiết – cập nhật hồ sơ nhân sự mà không cần trợ giúp trực tiếp; (3) Tỷ lệ người dùng mới phòng TCKT hoàn thành bộ tác vụ tìm kiếm – xem chi tiết – xuất dữ liệu nhân sự mà không cần trợ giúp trực tiếp. |
| **Tiêu chuẩn đáp ứng** | (1) Thời gian đào tạo ≤ 2 giờ/người; (2) Tỷ lệ hoàn thành của nhóm TCCB ≥ 95%; (3) Tỷ lệ hoàn thành của nhóm TCKT ≥ 95%. |
| **Phương pháp đo** | Tổ chức usability test với người dùng mới đại diện cho hai phòng ban sau buổi hướng dẫn chuẩn; ghi nhận thời gian đào tạo, tỷ lệ hoàn thành tác vụ và số lần cần trợ giúp trực tiếp. |
| **Lý do chọn độ đo** | NN/g nêu rằng **learnability** nên đo bằng **time on task** và **task completion rate**. Trong bối cảnh trường đại học, đào tạo người dùng thường chỉ bố trí được trong một buổi ngắn; vì vậy ngưỡng **≤ 2 giờ** tương ứng một buổi hướng dẫn cơ bản là phù hợp triển khai. Mức **≥ 95%** bảo đảm đa số tuyệt đối người dùng mới có thể làm việc độc lập ngay sau tập huấn, nhưng vẫn chừa sai số nhỏ cho khác biệt về kỹ năng cá nhân. |
| **Đại lượng thay thế (nếu cần)** | Khối lượng tài liệu/hướng dẫn đào tạo cho mỗi vai trò không vượt quá 30 trang để tránh tăng gánh nặng học sử dụng. |

#### SUPL-U03: Thông báo lỗi rõ ràng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Xử lý lỗi (Error Handling) |
| **Mô tả yêu cầu** | Mọi lỗi nhập liệu hoặc lỗi hệ thống phải hiển thị thông báo bằng Tiếng Việt, rõ ràng, mô tả nguyên nhân và hướng dẫn khắc phục. |
| **Độ đo yêu cầu** | (1) Tỷ lệ lỗi validation và lỗi nghiệp vụ có thông báo bằng Tiếng Việt rõ ràng; (2) Tỷ lệ thông báo lỗi có nêu nguyên nhân; (3) Tỷ lệ thông báo lỗi validation/nghiệp vụ có ít nhất 1 gợi ý khắc phục; (4) Tỷ lệ lỗi hệ thống hiển thị thông báo thân thiện kèm mã tra cứu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% lỗi validation và lỗi nghiệp vụ có thông báo bằng Tiếng Việt; (2) 100% thông báo lỗi nêu được nguyên nhân chính; (3) ≥ 95% thông báo lỗi validation/nghiệp vụ có ít nhất 1 gợi ý khắc phục; (4) 100% lỗi hệ thống hiển thị thông báo thân thiện và có mã tra cứu/log reference. |
| **Phương pháp đo** | Lập danh mục các lỗi điển hình theo từng nhóm, kích hoạt lỗi trên môi trường kiểm thử và đối chiếu nội dung thông báo với checklist: đúng tiếng Việt, có nguyên nhân, có hướng dẫn xử lý hoặc mã tra cứu. |
| **Lý do chọn độ đo** | Theo heuristic **Help Users Recognize, Diagnose, and Recover from Errors** của Nielsen và bài **Error-Message Guidelines**, lỗi tốt phải dùng ngôn ngữ dễ hiểu, chỉ rõ vấn đề và gợi ý cách xử lý. Vì lỗi validation/nghiệp vụ là các tình huống dự đoán được nên đặt ngưỡng **100%** là hợp lý; riêng gợi ý khắc phục dùng **≥ 95%** để tránh quá cứng với một số lỗi biên hiếm gặp. Với lỗi hệ thống, người dùng cuối không cần stack trace mà cần thông báo thân thiện và mã tra cứu để bộ phận kỹ thuật xử lý nhanh. |
| **Đại lượng thay thế (nếu cần)** | Số thông báo lỗi hiển thị bằng tiếng Anh hoặc chỉ hiển thị mã kỹ thuật = 0. |

#### SUPL-U04: Hỗ trợ tìm kiếm và lọc đa tiêu chí
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Các danh sách dữ liệu (nhân sự, hợp đồng, đơn vị) phải hỗ trợ tìm kiếm theo từ khóa và lọc đa tiêu chí để giảm thời gian thao tác. |
| **Độ đo yêu cầu** | (1) Số bước thao tác để tìm kiếm và mở chi tiết 1 hồ sơ nhân sự; (2) Số tiêu chí lọc có thể kết hợp đồng thời trên một danh sách dữ liệu chính. |
| **Tiêu chuẩn đáp ứng** | (1) Tìm kiếm và mở chi tiết 1 hồ sơ nhân sự trong ≤ 3 bước (nhập từ khóa → tìm kiếm → mở chi tiết); (2) Bộ lọc hỗ trợ kết hợp ≥ 3 tiêu chí đồng thời trên các danh sách dữ liệu chính. |
| **Phương pháp đo** | Thực hiện walkthrough trên các màn hình danh sách chính, đếm số thao tác thực tế và kiểm tra khả năng kết hợp đồng thời các tiêu chí lọc trên cùng một truy vấn. |
| **Lý do chọn độ đo** | Theo heuristic **Recognition Rather than Recall** và **Flexibility and Efficiency of Use** của NN/g, người dùng nên nhìn thấy ngay công cụ tìm kiếm/lọc thay vì phải nhớ nhiều đường đi thao tác. Với HRMS nội bộ, cán bộ thường tra cứu nhanh hồ sơ theo vài thuộc tính như mã, đơn vị, trạng thái; vì vậy ngưỡng **≤ 3 bước** phản ánh luồng tra cứu tối giản, còn **≥ 3 tiêu chí lọc đồng thời** là đủ cho phần lớn truy vấn nghiệp vụ mà không làm giao diện quá phức tạp. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể đo trực tiếp qua thao tác người dùng trên giao diện. |

#### SUPL-U05: Hiển thị ổn định trên desktop và tablet
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Khả năng truy cập đa thiết bị (Accessibility) |
| **Mô tả yêu cầu** | Ở độ phân giải desktop từ 1366×768 trở lên, 100% màn hình phải hiển thị đầy đủ nội dung, không chồng lấn thành phần và không yêu cầu cuộn ngang; trên tablet 1024×768, tối thiểu 80% màn hình phải cho phép thực hiện các thao tác chính mà không cần phóng to. |
| **Độ đo yêu cầu** | (1) Tỷ lệ màn hình nghiệp vụ chính hiển thị đúng ở độ phân giải desktop ≥ 1366×768; (2) Tỷ lệ màn hình nghiệp vụ chính sử dụng được trên tablet 1024×768; (3) Tỷ lệ tác vụ cốt lõi thực hiện được trên tablet 1024×768 mà không cần phóng to hoặc cuộn ngang. |
| **Tiêu chuẩn đáp ứng** | (1) 100% màn hình nghiệp vụ chính đạt tiêu chí ở desktop ≥ 1366×768; (2) ≥ 90% màn hình nghiệp vụ chính dùng được ở tablet 1024×768; (3) 100% tác vụ cốt lõi trên tablet 1024×768 không cần phóng to hoặc cuộn ngang. |
| **Phương pháp đo** | Kiểm thử giao diện trên trình duyệt desktop chuẩn và thiết bị giả lập/tablet 1024×768; ghi nhận các lỗi cắt nội dung, chồng lấn thành phần, cuộn ngang và thao tác cần phóng to. |
| **Lý do chọn độ đo** | Hệ thống HRMS của trường chủ yếu được dùng trên desktop tại phòng ban, nên ngưỡng **100% cho desktop 1366×768** là bắt buộc vì đây là mức phân giải văn phòng phổ biến. Tablet chỉ là kênh hỗ trợ cho tra cứu hoặc phê duyệt nhanh, nên đặt **≥ 90% màn hình chính** và **100% tác vụ cốt lõi** là hợp lý hơn việc yêu cầu 100% trên mọi màn hình phụ; cách này vẫn bảo đảm khả năng dùng thực tế mà phù hợp định hướng desktop-first của hệ thống nội bộ. |
| **Đại lượng thay thế (nếu cần)** | Hệ thống giao diện có tối thiểu 2 breakpoint rõ ràng cho desktop và tablet để hỗ trợ responsive layout. |

#### SUPL-U06: Điều hướng nhanh bằng bàn phím và breadcrumb
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Trên ít nhất 90% form nhập liệu, phím Tab phải di chuyển tuần tự giữa các trường có thể nhập; trên 100% form có nút xác nhận mặc định, phím Enter phải kích hoạt nút đó; 100% trang phải hiển thị breadcrumb để người dùng quay lại cấp điều hướng trước. |
| **Độ đo yêu cầu** | (1) Tỷ lệ form nhập liệu chính hỗ trợ Tab navigation đúng thứ tự; (2) Tỷ lệ form có nút xác nhận mặc định hỗ trợ phím Enter; (3) Tỷ lệ trang có cấu trúc phân cấp danh sách → chi tiết → chỉnh sửa hiển thị breadcrumb hợp lệ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% form nhập liệu chính cho phép di chuyển bằng phím Tab theo đúng thứ tự trường nhập; (2) 100% form có nút xác nhận mặc định hỗ trợ phím Enter; (3) 100% trang có cấu trúc phân cấp danh sách → chi tiết → chỉnh sửa hiển thị breadcrumb hợp lệ. |
| **Phương pháp đo** | Thực hiện kiểm thử thủ công bằng bàn phím trên toàn bộ form nhập liệu chính và các trang chức năng có phân cấp điều hướng; ghi nhận thứ tự focus, hành vi của phím Enter và sự hiện diện của breadcrumb. |
| **Lý do chọn độ đo** | WCAG 2.2 **SC 2.1.1 Keyboard** yêu cầu mọi chức năng khả dụng qua bàn phím; với hệ thống nhập liệu nhiều như HRMS, điều này giúp tăng năng suất cho người dùng thường xuyên. Tôi thu hẹp phạm vi thành **form nhập liệu chính** và **trang có cấu trúc phân cấp**, nhờ đó ngưỡng **100%** trở nên khả thi và dễ nghiệm thu hơn so với áp dụng máy móc cho mọi modal hoặc dashboard. Breadcrumb được giữ ở mức 100% cho các trang phân cấp vì nó trực tiếp hỗ trợ định hướng và giảm nhầm lẫn khi người dùng quay lui. |
| **Đại lượng thay thế (nếu cần)** | Tỷ lệ trường nhập liệu có thứ tự focus được xác định rõ ràng trong thiết kế/triển khai = 100% trên các form chính. |

#### SUPL-U07: Xác nhận trước thao tác quan trọng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Ngăn ngừa lỗi (Error Prevention) |
| **Mô tả yêu cầu** | Hệ thống hiển thị hộp thoại xác nhận trước các thao tác quan trọng như xóa dữ liệu, khóa tài khoản, đánh dấu thôi việc, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương. |
| **Độ đo yêu cầu** | Tỷ lệ thao tác quan trọng có hộp thoại xác nhận trước khi hệ thống thực thi thao tác. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác quan trọng có confirmation dialog; tối thiểu bao gồm: xóa dữ liệu, khóa tài khoản, đánh dấu thôi việc, thay đổi trạng thái đơn vị và chấm dứt hợp đồng lao động trước hạn (nếu chức năng được cung cấp trên hệ thống). |
| **Phương pháp đo** | Lập danh sách thao tác quan trọng theo nghiệp vụ, kích hoạt từng thao tác trên môi trường kiểm thử và kiểm tra sự xuất hiện của hộp thoại xác nhận trước khi dữ liệu bị thay đổi. |
| **Lý do chọn độ đo** | Theo heuristic **Error Prevention** của Nielsen và hướng dẫn của NN/g về **confirmation dialog**, xác nhận chỉ nên dùng cho hành động có hậu quả nghiêm trọng và khó hoàn tác. Các thao tác như xóa, khóa tài khoản, thôi việc hoặc đổi trạng thái đơn vị đều có rủi ro cao đối với dữ liệu nhân sự, nên ngưỡng **100%** là phù hợp vì đây là yêu cầu kiểu “sharp”: thiếu xác nhận ở một trường hợp cũng có thể gây lỗi nghiệp vụ lớn. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể kiểm thử trực tiếp theo từng thao tác trọng yếu. |

## 6.5. Yêu cầu về Hỗ trợ (Supportability)

> Người thực hiện: Nguyễn Hải Ninh

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
| **Độ đo yêu cầu** | (1) Số module khác cần sửa khi thực hiện một thay đổi nghiệp vụ thông thường trong 1 module; (2) Tỷ lệ module có interface/service contract được mô tả rõ ràng; (3) Số phụ thuộc vòng giữa các module nghiệp vụ chính. |
| **Tiêu chuẩn đáp ứng** | (1) Thay đổi nghiệp vụ thông thường trong 1 module không làm phát sinh sửa đổi ở quá 2 module khác; (2) 100% module nghiệp vụ chính có interface/service contract rõ ràng; (3) Số phụ thuộc vòng giữa các module nghiệp vụ chính = 0. |
| **Phương pháp đo** | Phân tích dependency giữa các module, rà soát tài liệu interface và thực hiện impact analysis đối với một thay đổi nghiệp vụ điển hình ở từng module chính. |
| **Lý do chọn độ đo** | ISO/IEC 25010 xem **modularity** là một thành phần của maintainability, còn ISO/IEC/IEEE 42010 yêu cầu mô tả kiến trúc đủ rõ để kiểm soát ranh giới module. Tôi dùng ngưỡng **≤ 2 module bị ảnh hưởng** thay cho ≤ 1 vì thực tế hệ thống web thường vẫn có lan truyền sang lớp API hoặc UI; tuy nhiên vượt quá 2 module cho một thay đổi thông thường cho thấy coupling bắt đầu cao. Điều kiện **0 phụ thuộc vòng** giúp kiến trúc dễ thay thế, kiểm thử và bảo trì hơn. |
| **Đại lượng thay thế (nếu cần)** | Số dependency cross-module ngoài interface công khai phải ở mức tối thiểu và được kiểm soát qua báo cáo phân tích phụ thuộc. |

#### SUPL-S02: Tài liệu kỹ thuật đầy đủ
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Khả năng hiểu và vận hành (Understandability) |
| **Mô tả yêu cầu** | Cung cấp tài liệu API cho backend, hướng dẫn triển khai và hướng dẫn sử dụng cho từng vai trò. |
| **Độ đo yêu cầu** | (1) Tỷ lệ API public hoặc API nội bộ đang được frontend sử dụng có tài liệu mô tả đầy đủ phương thức, URL, tham số, dữ liệu trả về và mã lỗi; (2) Tỷ lệ vai trò người dùng có hướng dẫn sử dụng riêng cho các chức năng chính; (3) Tỷ lệ tài liệu triển khai có đủ các mục bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 100% API public hoặc API nội bộ đang được frontend sử dụng có tài liệu đầy đủ; (2) 100% vai trò sử dụng hệ thống có hướng dẫn sử dụng tương ứng; (3) 100% tài liệu triển khai có tối thiểu các mục: yêu cầu môi trường, cài đặt, cấu hình, khởi động, sao lưu/khôi phục và xử lý lỗi thường gặp. |
| **Phương pháp đo** | Đối chiếu danh mục endpoint thực tế với bộ tài liệu API; rà soát tài liệu theo checklist vai trò và checklist triển khai trước nghiệm thu. |
| **Lý do chọn độ đo** | IEEE **1063-2001** nêu tài liệu người dùng phải có cấu trúc và nội dung tối thiểu, còn ISO/IEC/IEEE **42010** nhấn mạnh việc mô tả kiến trúc và triển khai theo stakeholder concern. Với hệ thống nội bộ, endpoint đang được frontend gọi mà thiếu tài liệu sẽ làm tăng ngay chi phí sửa lỗi và bàn giao, vì vậy chọn **100% cho API đang sử dụng** thay vì 90%. Tương tự, mọi vai trò nghiệp vụ đều cần hướng dẫn riêng để tránh phụ thuộc vào truyền miệng khi vận hành lâu dài. |
| **Đại lượng thay thế (nếu cần)** | Số endpoint chưa được tài liệu hóa và số vai trò chưa có hướng dẫn sử dụng riêng. |

#### SUPL-S03: Khả năng mở rộng danh mục cấu hình
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Tính linh hoạt cấu hình (Flexibility/Configurability) |
| **Mô tả yêu cầu** | Hệ thống cho phép mở rộng các danh mục cấu hình (loại phụ cấp, loại hợp đồng, hệ số lương) mà không cần thay đổi mã nguồn. |
| **Độ đo yêu cầu** | (1) Số loại danh mục cấu hình có thể mở rộng qua giao diện quản trị; (2) Số dòng mã nguồn phải sửa khi thêm một danh mục mới; (3) Có/không yêu cầu deploy lại hệ thống sau khi thêm mới giá trị cấu hình. |
| **Tiêu chuẩn đáp ứng** | (1) Có ít nhất 3 loại danh mục master data mở rộng được qua giao diện quản trị: hệ số lương, loại phụ cấp, loại hợp đồng; (2) Số dòng mã nguồn cần sửa khi thêm danh mục mới = 0; (3) Không cần deploy lại hệ thống khi thêm mới giá trị cấu hình. |
| **Phương pháp đo** | Thực hiện thử nghiệm thêm mới/sửa danh mục cấu hình trên giao diện quản trị và kiểm tra thay đổi mã nguồn, quy trình build/deploy trong suốt quá trình cấu hình. |
| **Lý do chọn độ đo** | Theo nguyên tắc **Config** của **The Twelve-Factor App**, các thông số thay đổi theo môi trường hoặc chính sách không nên bị hard-code trong chương trình. Với HRMS của trường đại học, ba nhóm danh mục này là những danh mục biến động trực tiếp theo quy định nội bộ và quy định nhà nước, nên chọn **≥ 3 danh mục** là sát nhu cầu thực tế. Điều kiện **0 sửa code** và **không cần deploy lại** bảo đảm hệ thống thực sự linh hoạt chứ không chỉ “cấu hình được” trên lý thuyết. |
| **Đại lượng thay thế (nếu cần)** | Không cần, vì có thể kiểm chứng trực tiếp qua thao tác cấu hình trên hệ thống. |

#### SUPL-S04: Hỗ trợ gỡ lỗi (Debugging)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Khả năng chẩn đoán và kiểm thử (Maintainability/Testability) |
| **Mô tả yêu cầu** | Hệ thống ghi log lỗi phía server theo nhiều cấp độ (ERROR, WARNING, INFO, DEBUG). Log phải bao gồm timestamp, request ID, stack trace. |
| **Độ đo yêu cầu** | (1) Số cấp độ log được hệ thống hỗ trợ; (2) Tỷ lệ log mức ERROR có đủ timestamp, severity, request ID và stack trace; (3) Tỷ lệ log lỗi/nghiệp vụ phát sinh trong phiên xác thực có gắn user ID hoặc actor ID. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 4 cấp độ log: ERROR, WARNING, INFO, DEBUG; (2) 100% log mức ERROR có đủ timestamp, severity, request ID và stack trace; (3) ≥ 95% log lỗi/nghiệp vụ phát sinh trong phiên xác thực có user ID hoặc actor ID. |
| **Phương pháp đo** | Kích hoạt các tình huống lỗi điển hình trên môi trường kiểm thử, trích xuất log server và đối chiếu từng bản ghi với checklist trường thông tin bắt buộc và cấp độ log. |
| **Lý do chọn độ đo** | **OWASP Logging Cheat Sheet** khuyến nghị log phải trả lời được các câu hỏi **when, where, who, what**; **RFC 5424** cũng chuẩn hóa severity level cho log. Vì vậy chỉ đếm số level là chưa đủ, nên tôi bổ sung yêu cầu về **severity, request ID, user ID** để phục vụ truy vết thật sự. Ngưỡng **100% cho log ERROR** là hợp lý vì mọi lỗi server đều phải chẩn đoán được; còn **≥ 95% với user ID** thực tế hơn trong các trường hợp ngoại lệ xảy ra trước khi phiên xác thực hoàn chỉnh. |
| **Đại lượng thay thế (nếu cần)** | Số log ERROR thiếu một trong các trường bắt buộc (timestamp, severity, request ID, stack trace) phải bằng 0. |

#### SUPL-S05: Khả năng mở rộng quy mô (Scalability)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Khả năng mở rộng quy mô (Scalability) |
| **Mô tả yêu cầu** | Hệ thống phải duy trì đầy đủ chức năng khi năng lực xử lý được mở rộng bằng cách bổ sung thêm nút ứng dụng trong cùng một môi trường khai thác. |
| **Độ đo yêu cầu** | (1) Số nút ứng dụng có thể vận hành song song trong cùng môi trường; (2) Tỷ lệ phiên người dùng tiếp tục hoạt động đúng khi request liên tiếp được phân phối qua các nút khác nhau trong bài kiểm thử scale-out 30 phút; (3) Tỷ lệ ca smoke test chức năng chính vẫn đạt sau khi bổ sung nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 2 nút ứng dụng chạy song song trong cùng môi trường; (2) 100% phiên người dùng trong bài kiểm thử 30 phút vẫn hoạt động đúng khi request liên tiếp đi qua các nút khác nhau; (3) 100% ca smoke test của các chức năng chính vẫn đạt sau khi bổ sung nút ứng dụng. |
| **Phương pháp đo** | Triển khai thử nghiệm cấu hình nhiều nút ứng dụng sau load balancer, chạy kiểm thử phiên liên tiếp trong 30 phút và thực hiện bộ smoke test/regression cho các chức năng chính của hệ thống. |
| **Lý do chọn độ đo** | **The Twelve-Factor App** (mục **Processes** và **Concurrency**) xem scale ngang là mở rộng bằng cách bổ sung process/instance thay vì chỉ tăng tài nguyên cho một nút. Với HRMS cấp trường, tải đồng thời thường không lớn như hệ thống công cộng, nên ngưỡng **tối thiểu 2 nút** là đủ để chứng minh hệ thống có thể scale-out và có dự phòng cơ bản. Bài kiểm thử **30 phút** đủ dài để quan sát lỗi phiên, lỗi sticky-session hoặc lỗi chia sẻ trạng thái mà không làm tăng chi phí kiểm thử quá mức. |
| **Đại lượng thay thế (nếu cần)** | Số lỗi phiên làm việc hoặc lỗi điều hướng phát sinh khi request được chuyển giữa các nút ứng dụng phải bằng 0. |
