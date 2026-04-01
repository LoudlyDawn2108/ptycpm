# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng của Ngô Quang Tùng

> Cột **FEAT liên quan** dùng để ghi các FEAT mà mỗi SUPL truy vết tới.

## 6.6. Yêu cầu về Hiệu năng (Performance)

> Người thực hiện: Ngô Quang Tùng

### 6.6.1. Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-P01 | Hệ thống phải giữ P95 Response Time của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự trong các ngưỡng quy định theo 3 mức tải đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 2 | SUPL-P01b | Hệ thống phải giữ Time to Interactive (TTI) của các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự trong các ngưỡng quy định theo 3 mức tải đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 3 | SUPL-P02 | Hệ thống phải hỗ trợ tối thiểu 100 người dùng đồng thời trong giờ cao điểm mà không làm thời gian phản hồi tăng quá 50% so với tải một người dùng. | FEAT 7.1–8.9 |
| 4 | SUPL-P03a | Hệ thống phải hiển thị chi tiết hồ sơ nhân sự tổng hợp trong tối đa 5 giây ở mức không quá 10 người dùng đồng thời. | FEAT 8.7 |
| 5 | SUPL-P03b | Hệ thống phải chuẩn bị dữ liệu in hồ sơ nhân sự trong tối đa 10 giây ở mức không quá 10 người dùng đồng thời. | FEAT 8.8 |
| 6 | SUPL-P04 | Hệ thống phải trả kết quả tìm kiếm và lọc hồ sơ nhân sự trong tối đa 2 giây với tập dữ liệu không quá 10.000 bản ghi hoặc tối đa 5 giây với tập dữ liệu không quá 50.000 bản ghi, tại mức không quá 50 người dùng đồng thời. | FEAT 8.1, FEAT 8.2 |
| 7 | SUPL-P05 | Hệ thống phải hoàn thành upload/download tệp đính kèm trong tối đa 5/3 giây với file không quá 5 MB hoặc tối đa 10/6 giây với file trên 5 MB đến 10 MB, trên mạng LAN 1 Gbps và ở mức không quá 10 người dùng đồng thời. | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 8 | SUPL-P06 | Hệ thống phải xuất dữ liệu hồ sơ nhân sự ra Excel trong tối đa 10 giây với tập dữ liệu không quá 1.000 bản ghi hoặc tối đa 30 giây với tập dữ liệu không quá 10.000 bản ghi, tại mức không quá 10 người dùng đồng thời. | FEAT 8.8 |
| 9 | SUPL-P07a | Hệ thống phải phục hồi khả năng phục vụ sau sự cố trong tối đa 15 phút. | FEAT 7.1–8.9 |
| 10 | SUPL-P07b | Hệ thống phải khởi động lại toàn bộ stack trong tối đa 10 phút sau sự cố crash hoặc restart có chủ đích. | FEAT 7.1–8.9 |

### 6.6.2. Độ đo và tiêu chuẩn đáp ứng

#### SUPL-P01
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | P95 Response Time cho các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự tại 3 mức tải: 0–10, 11–50 và 51–100 người dùng đồng thời. |
| **Tiêu chuẩn đáp ứng** | (1) 0–10 người dùng đồng thời: P95 Response Time ≤ 1 giây; (2) 11–50 người dùng đồng thời: P95 Response Time ≤ 2 giây; (3) 51–100 người dùng đồng thời: P95 Response Time ≤ 5 giây. |

#### SUPL-P01b
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian tương tác giao diện |
| **Độ đo yêu cầu** | Time to Interactive (TTI) cho các thao tác xem danh sách, xem chi tiết, thêm mới và chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự tại 3 mức tải: 0–10, 11–50 và 51–100 người dùng đồng thời. |
| **Tiêu chuẩn đáp ứng** | (1) 0–10 người dùng đồng thời: TTI ≤ 1,5 giây; (2) 11–50 người dùng đồng thời: TTI ≤ 3 giây; (3) 51–100 người dùng đồng thời: TTI ≤ 6 giây. |

#### SUPL-P02
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Sức chứa |
| **Độ đo yêu cầu** | (1) Số người dùng đồng thời tối đa hệ thống hỗ trợ; (2) Throughput tại mức tải mục tiêu; (3) Tỷ lệ suy giảm thời gian phản hồi khi so sánh mức 100 người dùng với mức 1 người dùng. |
| **Tiêu chuẩn đáp ứng** | (1) Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời; (2) Throughput đạt tối thiểu 50 tx/s tại mức 100 người dùng đồng thời; (3) Thời gian phản hồi tăng không quá 50% so với tải một người dùng. |

#### SUPL-P03a
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | Thời gian tải trang chi tiết hồ sơ nhân sự tổng hợp. |
| **Tiêu chuẩn đáp ứng** | Trang chi tiết hồ sơ nhân sự tổng hợp hiển thị hoàn chỉnh trong tối đa 5 giây tại mức không quá 10 người dùng đồng thời. |

#### SUPL-P03b
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | Thời gian chuẩn bị dữ liệu in hồ sơ nhân sự. |
| **Tiêu chuẩn đáp ứng** | Dữ liệu in hồ sơ nhân sự được chuẩn bị xong trong tối đa 10 giây tại mức không quá 10 người dùng đồng thời. |

#### SUPL-P04
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | (1) Thời gian trả kết quả tìm kiếm; (2) Thời gian áp dụng bộ lọc, tương ứng với hai quy mô dữ liệu: không quá 10.000 bản ghi và không quá 50.000 bản ghi. |
| **Tiêu chuẩn đáp ứng** | (1) Với tập dữ liệu ≤ 10.000 bản ghi: thời gian tìm kiếm và lọc đều ≤ 2 giây tại mức ≤ 50 người dùng đồng thời; (2) Với tập dữ liệu ≤ 50.000 bản ghi: thời gian tìm kiếm và lọc đều ≤ 5 giây tại mức ≤ 50 người dùng đồng thời. |

#### SUPL-P05
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | (1) Thời gian upload file; (2) Thời gian download file; (3) Kích thước file kiểm thử trong hai khoảng: ≤ 5 MB và > 5 MB đến ≤ 10 MB, trên mạng LAN 1 Gbps. |
| **Tiêu chuẩn đáp ứng** | (1) Với file ≤ 5 MB: Upload ≤ 5 giây, Download ≤ 3 giây tại mức ≤ 10 người dùng đồng thời; (2) Với file > 5 MB đến ≤ 10 MB: Upload ≤ 10 giây, Download ≤ 6 giây tại mức ≤ 10 người dùng đồng thời. |

#### SUPL-P06
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phản hồi |
| **Độ đo yêu cầu** | Thời gian xuất dữ liệu hồ sơ nhân sự ra Excel với hai quy mô dữ liệu: ≤ 1.000 bản ghi và ≤ 10.000 bản ghi. |
| **Tiêu chuẩn đáp ứng** | (1) Với tập dữ liệu ≤ 1.000 bản ghi: thời gian xuất Excel ≤ 10 giây tại mức ≤ 10 người dùng đồng thời; (2) Với tập dữ liệu ≤ 10.000 bản ghi: thời gian xuất Excel ≤ 30 giây tại mức ≤ 10 người dùng đồng thời. |

#### SUPL-P07a
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phục hồi dịch vụ |
| **Độ đo yêu cầu** | Thời gian từ lúc hệ thống gặp sự cố đến khi phục vụ lại được request đầu tiên thành công. |
| **Tiêu chuẩn đáp ứng** | Hệ thống phục hồi khả năng phục vụ trong tối đa 15 phút sau sự cố crash hoặc restart. |

#### SUPL-P07b
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian khởi động lại |
| **Độ đo yêu cầu** | Thời gian từ lúc phát hiện crash hoặc phát lệnh restart đến khi toàn bộ stack khởi động thành công theo health check kỹ thuật. |
| **Tiêu chuẩn đáp ứng** | Toàn bộ stack khởi động lại trong tối đa 10 phút sau sự cố crash hoặc restart có chủ đích. |

### 6.6.3. Ghi chú phạm vi trong nhóm Performance

- `SUPL-P01` gốc được tách thành `SUPL-P01` và `SUPL-P01b` để tách riêng ngưỡng **P95 Response Time** và **TTI**, giúp requirement atomic hơn.
- `SUPL-R02` gốc được đổi thành `SUPL-P07a` và `SUPL-P07b` để khớp với section **Hiệu năng** và yếu tố chất lượng chính của hai requirement này.
- Ngoài `SUPL-P07b`, hiện không có thêm yêu cầu nghiệm thu riêng cho thời gian khởi động mới hoặc tắt an toàn trong fragment này.
- **Resource utilization:** N/A trong fragment này vì stakeholder chưa đưa ra ràng buộc CPU, RAM, băng thông hoặc dung lượng lưu trữ cụ thể cho môi trường triển khai.

## 6.7. Yêu cầu về Độ tin cậy (Reliability)

> Người thực hiện: Ngô Quang Tùng

### 6.7.1. Danh sách yêu cầu

| STT | ID | Nội dung yêu cầu | FEAT liên quan |
|-----|----|------------------|----------------|
| 1 | SUPL-R01 | Hệ thống phải duy trì uptime tối thiểu 99,5% trong khung giờ 7:00–22:00 hằng ngày, không tính bảo trì theo kế hoạch. | FEAT 7.1–8.9 |
| 2 | SUPL-R03a | Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi 24 giờ. | FEAT 7.1–8.9 |
| 3 | SUPL-R03b | Hệ thống phải phục hồi từ bản sao lưu gần nhất và sẵn sàng phục vụ trong tối đa 4 giờ. | FEAT 7.1–8.9 |
| 4 | SUPL-R03c | Hệ thống phải lưu giữ bản sao lưu tối thiểu 30 ngày. | FEAT 7.1–8.9 |
| 5 | SUPL-R03d | Hệ thống phải đạt tỷ lệ backup thành công tối thiểu 99%. | FEAT 7.1–8.9 |
| 6 | SUPL-R04 | Hệ thống phải bảo đảm các thao tác tạo/chỉnh sửa hồ sơ nhân sự, hợp đồng và thay đổi trạng thái không để lại dữ liệu dở dang khi có lỗi. | FEAT 7.1–8.9 |
| 7 | SUPL-R05a | Hệ thống phải cảnh báo tối thiểu 5 phút trước khi phiên tự động hết hạn trên 100% phiên được kiểm thử. | FEAT 7.1–8.9 |
| 8 | SUPL-R05b | Hệ thống phải khôi phục dữ liệu nháp sau khi người dùng đăng nhập lại trong ít nhất 95% trường hợp kiểm thử. | FEAT 7.1–8.9 |

> `SUPL-R03` gốc được tách thành cụm `SUPL-R03a`, `SUPL-R03b`, `SUPL-R03c`, `SUPL-R03d` để phần sao lưu/phục hồi được trình bày liền mạch trong cùng một cụm requirement. Trong đó `SUPL-R03b` vẫn mang **yếu tố chất lượng chính là Hiệu năng – Thời gian phục hồi**.

### 6.7.2. Độ đo và tiêu chuẩn đáp ứng

#### SUPL-R01
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Độ tin cậy – Tính sẵn sàng |
| **Độ đo yêu cầu** | (1) Tỷ lệ uptime theo tháng trong khung giờ 7:00–22:00; (2) Tổng downtime trong tháng; (3) MTBF. |
| **Tiêu chuẩn đáp ứng** | (1) Uptime đạt tối thiểu 99,5% mỗi tháng trong khung giờ 7:00–22:00; (2) Downtime không quá 2,25 giờ/tháng, không tính bảo trì theo kế hoạch; (3) MTBF đạt tối thiểu 720 giờ. |

#### SUPL-R03a
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | RPO (Recovery Point Objective), đo theo thời gian từ thời điểm backup gần nhất đến thời điểm kiểm tra. |
| **Tiêu chuẩn đáp ứng** | Hệ thống sao lưu dữ liệu tự động ít nhất mỗi 24 giờ, tương ứng RPO không vượt quá 24 giờ. |

#### SUPL-R03b
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Hiệu năng – Thời gian phục hồi từ bản sao lưu |
| **Độ đo yêu cầu** | RTO (Recovery Time Objective) khi phục hồi từ bản sao lưu gần nhất. |
| **Tiêu chuẩn đáp ứng** | Hệ thống sẵn sàng phục vụ trở lại trong tối đa 4 giờ sau khi thực hiện phục hồi từ bản sao lưu gần nhất. |

#### SUPL-R03c
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Thời gian lưu giữ của mỗi bản sao lưu trước khi bị xóa hoặc ghi đè. |
| **Tiêu chuẩn đáp ứng** | Mỗi bản sao lưu được lưu giữ tối thiểu 30 ngày. |

#### SUPL-R03d
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Tỷ lệ backup thành công trên tổng số lần backup được lên lịch trong mỗi tháng. |
| **Tiêu chuẩn đáp ứng** | Tỷ lệ backup thành công đạt tối thiểu 99% trên tổng số lần backup được lên lịch trong mỗi tháng. |

#### SUPL-R04
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Độ tin cậy – Tính toàn vẹn dữ liệu |
| **Độ đo yêu cầu** | (1) Số trường hợp phát sinh dữ liệu bất nhất quán sau lỗi; (2) Tỷ lệ các nhóm nghiệp vụ trọng yếu trong phạm vi FEAT 7.1–8.9 được bảo vệ khỏi cập nhật dở dang. |
| **Tiêu chuẩn đáp ứng** | (1) 0 trường hợp dữ liệu bất nhất quán; (2) 100% các nhóm nghiệp vụ tạo/chỉnh sửa hồ sơ nhân sự, tạo/chỉnh sửa/chấm dứt hợp đồng và thay đổi trạng thái nghiệp vụ không phát sinh cập nhật dở dang khi có lỗi. |

#### SUPL-R05a
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | (1) Tỷ lệ phiên được hiển thị cảnh báo trước khi hết hạn; (2) Thời gian cảnh báo trước khi tự động đăng xuất. |
| **Tiêu chuẩn đáp ứng** | (1) 100% phiên được kiểm thử có cảnh báo trước khi hết hạn; (2) Cảnh báo xuất hiện tối thiểu 5 phút trước khi tự động đăng xuất. |

#### SUPL-R05b
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Độ tin cậy – Khả năng phục hồi |
| **Độ đo yêu cầu** | Tỷ lệ khôi phục dữ liệu nháp khi người dùng đăng nhập lại sau khi phiên hết hạn. |
| **Tiêu chuẩn đáp ứng** | Hệ thống khôi phục dữ liệu nháp trong ít nhất 95% trường hợp kiểm thử đối với form có dữ liệu đã nhập nhưng chưa lưu. |

### 6.7.3. Ghi chú phạm vi trong nhóm Reliability

- **Robustness:** N/A trong fragment này vì yêu cầu xử lý dữ liệu nhập sai và phản ứng với input bất thường đang được đặc tả tại các phần validation/giao diện của nhóm khác.
- **Fault tolerance:** N/A trong fragment này vì hiện chưa có yêu cầu vận hành về chế độ suy giảm hoặc tiếp tục phục vụ khi một thành phần phụ trợ bị lỗi.
- **Safety:** N/A vì HRMS là hệ thống quản lý nghiệp vụ nội bộ, không trực tiếp điều khiển thiết bị vật lý hoặc tạo rủi ro an toàn cho con người/môi trường.
- **Security:** Covered elsewhere trong các section bảo mật của nhóm, nên không lặp lại trong fragment Reliability này.
- **Accuracy / Correctness ngoài phạm vi Integrity:** Covered by `SUPL-R04` đối với các thao tác cập nhật dữ liệu trọng yếu; các yêu cầu đúng/sai nghiệp vụ chi tiết theo từng use case sẽ được đặc tả ở tài liệu use case hoặc section chức năng tương ứng.
