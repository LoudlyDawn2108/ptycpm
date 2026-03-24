# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng của Nguyễn Hải Ninh

## 6.4. Yêu cầu về khả dụng (Usability)

> Người thực hiện: Nguyễn Hải Ninh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-U01 | Giao diện tiếng Việt và nhất quán | Usability – Tính nhất quán giao diện (UI consistency) | Toàn bộ giao diện hệ thống |
| 2 | SUPL-U02 | Dễ học cho người dùng mới | Usability – Dễ học (Learnability) | FEAT 7.1; FEAT 7.4; FEAT 7.7; FEAT 7.8; FEAT 10.1; FEAT 10.2; FEAT 10.3; FEAT 10.4 |
| 3 | SUPL-U03 | Thông báo lỗi rõ ràng | Usability – Xử lý lỗi (Error handling) | FEAT 5.1; FEAT 6.1; FEAT 7.3; FEAT 7.4; FEAT 7.5; FEAT 8.1; FEAT 9.4; FEAT 9.5 |
| 4 | SUPL-U04a | Hỗ trợ tìm kiếm và lọc đa tiêu chí | Usability – Hiệu quả thao tác (Efficiency) | FEAT 6.3; FEAT 7.1; FEAT 7.2 |
| 5 | SUPL-U04b | Mở nhanh hồ sơ nhân sự | Usability – Hiệu quả thao tác (Efficiency) | FEAT 7.1; FEAT 7.7 |
| 6 | SUPL-U05 | Hiển thị ổn định trên desktop và tablet | Usability – Khả năng truy cập đa thiết bị (Accessibility) | Toàn bộ giao diện hệ thống |
| 7 | SUPL-U06a | Điều hướng nhanh bằng bàn phím | Usability – Ergonomics (Thao tác bằng bàn phím) | Toàn bộ form nhập liệu chính |
| 8 | SUPL-U06b | Điều hướng bằng breadcrumb | Usability – Dễ sử dụng (Ease of use) | Toàn bộ trang có phân cấp điều hướng |
| 9 | SUPL-U07 | Xác nhận trước thao tác quan trọng | Usability – Ngăn ngừa lỗi (Error prevention) | FEAT 2.5; FEAT 2.6; FEAT 3.4; FEAT 5.4; FEAT 7.5; FEAT 9.3; FEAT 9.4; FEAT 9.5 |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-U01: Giao diện tiếng Việt và nhất quán
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Tính nhất quán giao diện (UI consistency) |
| **Mô tả yêu cầu** | Hệ thống phải sử dụng tiếng Việt trên 100% nhãn, menu, nút thao tác và thông báo ở các màn hình nghiệp vụ chính; thuật ngữ kỹ thuật chỉ được giữ nguyên khi đã thống nhất cách dùng trong toàn hệ thống. |
| **Độ đo yêu cầu** | (1) Tỷ lệ thành phần giao diện dùng tiếng Việt; (2) Tỷ lệ màn hình nghiệp vụ chính tuân thủ cùng quy ước bố cục, màu sắc và font chữ. |
| **Tiêu chuẩn đáp ứng** | (1) 100% nhãn, menu, nút thao tác và thông báo ở màn hình nghiệp vụ chính dùng tiếng Việt; (2) ≥ 95% màn hình nghiệp vụ chính tuân thủ cùng một design system. |
| **Lý do chọn độ đo** | Ngôn ngữ hiển thị và độ nhất quán giao diện ảnh hưởng trực tiếp đến khả năng hiểu và giảm lỗi thao tác của cán bộ hành chính. Ngưỡng 100% cho nhãn/menu/thông báo ở màn hình nghiệp vụ chính là cần thiết, còn ≥ 95% cho tuân thủ design system là thực tế hơn cho một bài tập lớn sinh viên. |
| **Phương pháp đo** | Rà soát checklist giao diện trên các màn hình đại diện của nhóm hồ sơ, thống kê và self-service. |

#### SUPL-U02: Dễ học cho người dùng mới
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Dễ học (Learnability) |
| **Mô tả yêu cầu** | Sau tối đa 2 giờ hướng dẫn chuẩn, ít nhất 95% người dùng mới ở vai trò TCCB và TCKT phải hoàn thành được bộ tác vụ cơ bản của vai trò mình mà không cần trợ giúp trực tiếp. |
| **Độ đo yêu cầu** | (1) Thời gian hướng dẫn cho mỗi người dùng mới; (2) Tỷ lệ hoàn thành bộ tác vụ cơ bản của TCCB; (3) Tỷ lệ hoàn thành bộ tác vụ cơ bản của TCKT. |
| **Tiêu chuẩn đáp ứng** | (1) Thời gian hướng dẫn ≤ 2 giờ/người; (2) Tỷ lệ hoàn thành bộ tác vụ cơ bản của TCCB ≥ 95%; (3) Tỷ lệ hoàn thành bộ tác vụ cơ bản của TCKT ≥ 95%. |
| **Lý do chọn độ đo** | Learnability nên đo bằng thời gian làm quen và tỷ lệ hoàn thành tác vụ sau hướng dẫn. Mốc ≤ 2 giờ phù hợp một buổi tập huấn ngắn của hệ thống nội bộ; mức ≥ 95% cho thấy đa số người dùng mới có thể làm việc độc lập. |
| **Phương pháp đo** | Tổ chức usability test sau buổi hướng dẫn chuẩn và ghi nhận thời gian học, tỷ lệ hoàn thành, số lần cần trợ giúp. |

#### SUPL-U03: Thông báo lỗi rõ ràng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Xử lý lỗi (Error handling) |
| **Mô tả yêu cầu** | Hệ thống phải hiển thị thông báo lỗi bằng tiếng Việt; lỗi validation và lỗi nghiệp vụ phải nêu nguyên nhân chính và cách xử lý, còn lỗi hệ thống phải hiển thị thông báo thân thiện kèm mã tra cứu. |
| **Độ đo yêu cầu** | (1) Tỷ lệ lỗi validation và lỗi nghiệp vụ có thông báo tiếng Việt nêu nguyên nhân; (2) Tỷ lệ lỗi validation và lỗi nghiệp vụ có ít nhất 1 gợi ý khắc phục; (3) Tỷ lệ lỗi hệ thống có thông báo thân thiện kèm mã tra cứu. |
| **Tiêu chuẩn đáp ứng** | (1) 100% lỗi validation và lỗi nghiệp vụ có thông báo tiếng Việt nêu nguyên nhân chính; (2) ≥ 95% lỗi validation và lỗi nghiệp vụ có ít nhất 1 gợi ý khắc phục; (3) 100% lỗi hệ thống có thông báo thân thiện và mã tra cứu. |
| **Lý do chọn độ đo** | Thông báo lỗi tốt phải giúp người dùng nhận biết và khắc phục lỗi, nên độ đo tập trung vào ngôn ngữ hiển thị, nguyên nhân và gợi ý xử lý. Các lỗi dự đoán được phải đạt gần như tuyệt đối, còn lỗi hệ thống cần mã tra cứu để hỗ trợ bộ phận kỹ thuật. |
| **Phương pháp đo** | Kích hoạt các lỗi điển hình trên môi trường kiểm thử và đối chiếu nội dung thông báo với checklist nghiệm thu. |

#### SUPL-U04a: Hỗ trợ tìm kiếm và lọc đa tiêu chí
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Các màn hình danh sách có chức năng tra cứu phải hỗ trợ tìm theo từ khóa và kết hợp ít nhất 3 tiêu chí lọc. |
| **Độ đo yêu cầu** | Số tiêu chí lọc có thể kết hợp đồng thời trên một màn hình có chức năng lọc. |
| **Tiêu chuẩn đáp ứng** | Bộ lọc hỗ trợ kết hợp ≥ 3 tiêu chí đồng thời. |
| **Lý do chọn độ đo** | Hiệu quả tra cứu phụ thuộc trực tiếp vào khả năng kết hợp tiêu chí lọc. Mốc ≥ 3 tiêu chí đủ cho phần lớn truy vấn nhân sự mà vẫn giữ giao diện gọn và phù hợp phạm vi bài tập lớn. |
| **Phương pháp đo** | Thực hiện walkthrough trên các màn hình tra cứu và đếm số thao tác thực tế cùng số tiêu chí lọc kết hợp được. |

#### SUPL-U04b: Mở nhanh hồ sơ nhân sự
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Hiệu quả thao tác (Efficiency) |
| **Mô tả yêu cầu** | Trên danh sách hồ sơ nhân sự, người dùng phải mở được một hồ sơ trong tối đa 3 bước. |
| **Độ đo yêu cầu** | Số bước để tìm và mở một hồ sơ nhân sự. |
| **Tiêu chuẩn đáp ứng** | Mở một hồ sơ nhân sự trong ≤ 3 bước (nhập từ khóa → tìm kiếm → mở chi tiết). |
| **Lý do chọn độ đo** | Số bước để mở hồ sơ là chỉ số trực tiếp của hiệu quả thao tác. Ngưỡng ≤ 3 bước phản ánh một luồng tra cứu nhanh, phù hợp với nhu cầu tra cứu thường xuyên trong hệ thống HRMS nội bộ. |
| **Phương pháp đo** | Thực hiện walkthrough trên danh sách hồ sơ nhân sự và đếm số thao tác từ lúc nhập từ khóa đến lúc mở chi tiết. |

#### SUPL-U05: Hiển thị ổn định trên desktop và tablet
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Khả năng truy cập đa thiết bị (Accessibility) |
| **Mô tả yêu cầu** | Hệ thống phải hiển thị đầy đủ nội dung trên desktop từ 1366×768 trở lên và cho phép thực hiện các tác vụ trong bộ smoke test trên tablet 1024×768 mà không cần cuộn ngang hoặc phóng to. |
| **Độ đo yêu cầu** | (1) Tỷ lệ màn hình nghiệp vụ chính hiển thị đúng trên desktop ≥ 1366×768; (2) Tỷ lệ màn hình nghiệp vụ chính sử dụng được trên tablet 1024×768; (3) Tỷ lệ tác vụ trong bộ smoke test trên tablet không cần cuộn ngang hoặc phóng to. |
| **Tiêu chuẩn đáp ứng** | (1) 100% màn hình nghiệp vụ chính hiển thị đúng trên desktop ≥ 1366×768; (2) ≥ 80% màn hình nghiệp vụ chính sử dụng được trên tablet 1024×768; (3) 100% tác vụ trong bộ smoke test trên tablet không cần cuộn ngang hoặc phóng to. |
| **Lý do chọn độ đo** | Desktop là môi trường sử dụng chính nên phải đạt 100%; tablet chỉ là kênh hỗ trợ nên dùng ngưỡng thấp hơn nhưng vẫn phải vượt qua bộ smoke test. Cách chọn này cân bằng giữa tính khả dụng và phạm vi của một bài tập lớn sinh viên. |
| **Phương pháp đo** | Kiểm thử giao diện trên desktop chuẩn và tablet 1024×768 hoặc thiết bị giả lập tương đương. |

#### SUPL-U06a: Điều hướng nhanh bằng bàn phím
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Ergonomics (Thao tác bằng bàn phím) |
| **Mô tả yêu cầu** | Hệ thống phải cho phép thao tác trên các form nhập liệu chính bằng bàn phím: phím Tab di chuyển đúng thứ tự trường và phím Enter kích hoạt nút xác nhận mặc định khi có. |
| **Độ đo yêu cầu** | (1) Tỷ lệ form nhập liệu chính có thứ tự Tab đúng; (2) Tỷ lệ form có nút xác nhận mặc định hỗ trợ phím Enter. |
| **Tiêu chuẩn đáp ứng** | (1) 100% form nhập liệu chính cho phép di chuyển bằng phím Tab theo đúng thứ tự; (2) 100% form có nút xác nhận mặc định hỗ trợ phím Enter. |
| **Lý do chọn độ đo** | Các form nhập liệu là nơi người dùng thao tác thường xuyên nên điều hướng bàn phím ảnh hưởng trực tiếp đến tốc độ nhập liệu. Ngưỡng 100% trên form chính giúp kiểm thử rõ ràng và tránh lỗi focus hoặc gửi nhầm thao tác. |
| **Phương pháp đo** | Kiểm thử thủ công bằng bàn phím trên các form nhập liệu chính của hồ sơ, đào tạo và danh mục cấu hình. |

#### SUPL-U06b: Điều hướng bằng breadcrumb
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Dễ sử dụng (Ease of use) |
| **Mô tả yêu cầu** | Hệ thống phải hiển thị breadcrumb hợp lệ trên 100% trang có cấu trúc danh sách → chi tiết → chỉnh sửa để người dùng quay lại cấp điều hướng trước một cách rõ ràng. |
| **Độ đo yêu cầu** | Tỷ lệ trang có cấu trúc danh sách → chi tiết → chỉnh sửa hiển thị breadcrumb hợp lệ. |
| **Tiêu chuẩn đáp ứng** | 100% trang có cấu trúc danh sách → chi tiết → chỉnh sửa hiển thị breadcrumb hợp lệ. |
| **Lý do chọn độ đo** | Breadcrumb là công cụ định hướng trên các trang phân cấp; chỉ cần thiếu ở một trang cũng gây khó quay lại màn trước. Vì vậy độ đo dùng tỷ lệ hiện diện hợp lệ với ngưỡng 100% để dễ kiểm tra và dễ nghiệm thu. |
| **Phương pháp đo** | Rà soát các trang có phân cấp điều hướng và đối chiếu breadcrumb với đường dẫn nghiệp vụ thực tế. |

#### SUPL-U07: Xác nhận trước thao tác quan trọng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Usability – Ngăn ngừa lỗi (Error prevention) |
| **Mô tả yêu cầu** | Hệ thống phải yêu cầu xác nhận trước khi thực hiện các thao tác làm mất dữ liệu hoặc thay đổi trạng thái có rủi ro cao. |
| **Độ đo yêu cầu** | Tỷ lệ thao tác rủi ro cao có hộp thoại xác nhận trước khi thực thi. |
| **Tiêu chuẩn đáp ứng** | 100% thao tác rủi ro cao có hộp thoại xác nhận; tối thiểu gồm: xóa hệ số lương khi được phép, khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng trước hạn, thay đổi trạng thái đơn vị, loại phụ cấp và loại hợp đồng. |
| **Lý do chọn độ đo** | Đây là yêu cầu nhị phân: thao tác rủi ro cao phải có xác nhận, thiếu một trường hợp cũng có thể gây sai lệch dữ liệu. Vì vậy dùng tỷ lệ bao phủ confirmation dialog và đặt ngưỡng 100%. |
| **Phương pháp đo** | Lập danh sách thao tác rủi ro cao, kích hoạt từng thao tác trên môi trường kiểm thử và kiểm tra sự xuất hiện của hộp thoại xác nhận. |

## 6.5. Yêu cầu về hỗ trợ (Supportability)

> Người thực hiện: Nguyễn Hải Ninh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|--------------|--------------------|----------------|
| 1 | SUPL-S01 | Kiến trúc module hóa | Supportability – Maintainability/Modularity | Toàn bộ hệ thống |
| 2 | SUPL-S02 | Tài liệu kỹ thuật đầy đủ | Supportability – Understandability | Toàn bộ hệ thống |
| 3 | SUPL-S03 | Khả năng mở rộng danh mục cấu hình | Supportability – Configurability | FEAT 9.1; FEAT 9.2; FEAT 9.3; FEAT 9.4; FEAT 9.5 |
| 4 | SUPL-S04 | Hỗ trợ gỡ lỗi (Debugging) | Supportability – Analyzability | FEAT 12.1; FEAT 12.2 |
| 5 | SUPL-S05 | Khả năng mở rộng quy mô (Scalability) | Supportability – Scalability | Toàn bộ hệ thống |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-S01: Kiến trúc module hóa
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Maintainability/Modularity |
| **Mô tả yêu cầu** | Hệ thống phải được tách thành các module nghiệp vụ có hợp đồng giao tiếp rõ ràng; một thay đổi nghiệp vụ thông thường trong một module không được làm phát sinh sửa đổi ở quá 2 module khác. |
| **Độ đo yêu cầu** | (1) Số module khác phải sửa khi thực hiện một thay đổi nghiệp vụ thông thường trong một module; (2) Tỷ lệ module nghiệp vụ chính có service contract hoặc interface rõ ràng; (3) Số phụ thuộc vòng giữa các module nghiệp vụ chính. |
| **Tiêu chuẩn đáp ứng** | (1) Một thay đổi nghiệp vụ thông thường trong một module không làm phát sinh sửa đổi ở quá 2 module khác; (2) 100% module nghiệp vụ chính có service contract hoặc interface rõ ràng; (3) Số phụ thuộc vòng giữa các module nghiệp vụ chính = 0. |
| **Lý do chọn độ đo** | Khả năng bảo trì của kiến trúc thể hiện rõ qua phạm vi ảnh hưởng thay đổi, ranh giới module và phụ thuộc vòng. Ba độ đo này giúp kiểm tra trực tiếp mức coupling của hệ thống mà không cần phân tích kiến trúc quá phức tạp. |
| **Phương pháp đo** | Phân tích phụ thuộc giữa các module và thực hiện impact analysis trên một thay đổi nghiệp vụ điển hình của từng module chính. |

#### SUPL-S02: Tài liệu kỹ thuật đầy đủ
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Understandability |
| **Mô tả yêu cầu** | Hệ thống phải đi kèm bộ tài liệu kỹ thuật tối thiểu gồm tài liệu API, hướng dẫn triển khai và hướng dẫn sử dụng theo vai trò. |
| **Độ đo yêu cầu** | (1) Tỷ lệ API đang được frontend sử dụng có tài liệu đầy đủ; (2) Tỷ lệ vai trò sử dụng hệ thống có hướng dẫn sử dụng riêng; (3) Tỷ lệ hướng dẫn triển khai có đủ các mục bắt buộc. |
| **Tiêu chuẩn đáp ứng** | (1) 100% API đang được frontend sử dụng có tài liệu mô tả phương thức, URL, tham số, dữ liệu trả về và mã lỗi; (2) 100% vai trò sử dụng hệ thống có hướng dẫn sử dụng tương ứng; (3) 100% hướng dẫn triển khai có tối thiểu các mục: yêu cầu môi trường, cài đặt, cấu hình, khởi động, sao lưu/khôi phục và lỗi thường gặp. |
| **Lý do chọn độ đo** | Tài liệu kỹ thuật chỉ hữu ích khi bao phủ đúng API, đúng vai trò và đủ nội dung triển khai. Vì đây là tài liệu phục vụ bàn giao và vận hành nên dùng ngưỡng 100% để tránh phụ thuộc vào truyền miệng hoặc suy đoán. |
| **Phương pháp đo** | Đối chiếu danh mục endpoint và vai trò thực tế với bộ tài liệu trước nghiệm thu. |

#### SUPL-S03: Khả năng mở rộng danh mục cấu hình
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Configurability |
| **Mô tả yêu cầu** | Hệ thống phải cho phép quản trị viên mở rộng các danh mục dữ liệu chủ qua giao diện quản trị mà không cần sửa mã nguồn. |
| **Độ đo yêu cầu** | (1) Số loại danh mục dữ liệu chủ có thể mở rộng qua giao diện quản trị; (2) Số dòng mã nguồn cần sửa khi thêm danh mục hoặc giá trị cấu hình mới; (3) Có hoặc không yêu cầu triển khai lại hệ thống sau khi thêm mới giá trị cấu hình. |
| **Tiêu chuẩn đáp ứng** | (1) Có ít nhất 3 loại danh mục dữ liệu chủ mở rộng được qua giao diện quản trị: hệ số lương, loại phụ cấp, loại hợp đồng; (2) Số dòng mã nguồn cần sửa = 0; (3) Không cần triển khai lại hệ thống khi thêm mới giá trị cấu hình. |
| **Lý do chọn độ đo** | Nếu vẫn phải sửa code hoặc triển khai lại thì chưa thể coi là cấu hình linh hoạt. Vì vậy độ đo tập trung vào số danh mục mở rộng được, số dòng mã phải sửa và nhu cầu triển khai lại sau cấu hình. |
| **Phương pháp đo** | Thực hiện thử nghiệm thêm mới và chỉnh sửa danh mục cấu hình trên giao diện quản trị, đồng thời kiểm tra mã nguồn và quy trình triển khai. |

#### SUPL-S04: Hỗ trợ gỡ lỗi (Debugging)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Analyzability |
| **Mô tả yêu cầu** | Hệ thống phải ghi log chẩn đoán phía server theo nhiều mức và đủ thông tin để truy vết lỗi theo request và người thao tác. |
| **Độ đo yêu cầu** | (1) Số mức log hệ thống hỗ trợ; (2) Tỷ lệ log mức ERROR có đủ timestamp, severity, request ID và stack trace; (3) Tỷ lệ log phát sinh trong phiên xác thực có user ID hoặc actor ID. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 4 mức log: ERROR, WARNING, INFO, DEBUG; (2) 100% log mức ERROR có đủ timestamp, severity, request ID và stack trace; (3) ≥ 95% log phát sinh trong phiên xác thực có user ID hoặc actor ID. |
| **Lý do chọn độ đo** | Log chẩn đoán chỉ hữu ích khi đủ mức log và đủ thông tin để truy vết lỗi theo request và người dùng. Các độ đo này phản ánh trực tiếp khả năng phân tích lỗi khi hệ thống vận hành thực tế. |
| **Phương pháp đo** | Kích hoạt các tình huống lỗi điển hình, trích xuất log máy chủ và đối chiếu từng bản ghi với checklist trường thông tin bắt buộc. |

#### SUPL-S05: Khả năng mở rộng quy mô (Scalability)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Supportability – Scalability |
| **Mô tả yêu cầu** | Hệ thống phải duy trì đúng các chức năng trong bộ smoke test khi mở rộng theo chiều ngang bằng cách bổ sung thêm nút ứng dụng trong cùng môi trường khai thác. |
| **Độ đo yêu cầu** | (1) Số nút ứng dụng có thể chạy song song trong cùng môi trường; (2) Tỷ lệ phiên người dùng hoạt động đúng khi request liên tiếp đi qua các nút khác nhau trong bài kiểm thử scale-out 30 phút; (3) Tỷ lệ ca smoke test vẫn đạt sau khi bổ sung nút ứng dụng. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 2 nút ứng dụng chạy song song trong cùng môi trường; (2) 100% phiên người dùng trong bài kiểm thử 30 phút vẫn hoạt động đúng khi request liên tiếp đi qua các nút khác nhau; (3) 100% ca smoke test vẫn đạt sau khi bổ sung nút ứng dụng. |
| **Lý do chọn độ đo** | Khả năng scale-out cần được chứng minh bằng số nút chạy song song, tính đúng của phiên làm việc và kết quả smoke test sau mở rộng. Đây là các chỉ số quan sát được và phù hợp với một bài kiểm thử quy mô sinh viên. |
| **Phương pháp đo** | Triển khai thử nghiệm nhiều nút ứng dụng sau load balancer, chạy bài kiểm thử scale-out 30 phút và thực hiện bộ smoke test đã xác định. |
