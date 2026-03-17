# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng

## 6.6. Yêu cầu về Hiệu năng (Performance)

> Người thực hiện: Nguyễn Hải Ninh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|-------------|-------------------|----------------|
| 1 | SUPL-P01 | Thời gian phản hồi giao diện | Performance → Speed (Tốc độ phản hồi) | Toàn bộ FEAT; nhấn mạnh FEAT 7.2, FEAT 7.3, FEAT 10.2 |
| 2 | SUPL-P02 | Số lượng người dùng đồng thời | Performance → Capacity (Khả năng chịu tải) | Toàn bộ hệ thống |
| 3 | SUPL-P03 | Thời gian tạo báo cáo thống kê | Performance → Speed (Tốc độ xử lý và hiển thị báo cáo) | FEAT 5.1 |
| 4 | SUPL-P04 | Hiệu năng tìm kiếm và lọc | Performance → Speed (Tốc độ truy vấn dữ liệu) | FEAT 10.3, FEAT 8.1, FEAT 8.2 |
| 5 | SUPL-P05 | Hiệu năng upload/download file | Performance → Speed (Tốc độ truyền file) | Các FEAT có thao tác upload/download tệp đính kèm của hồ sơ nhân sự và hợp đồng |
| 6 | SUPL-P06 | Hiệu năng xuất Excel | Performance → Speed (Tốc độ xuất dữ liệu) | FEAT 8.8 |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-P01: Thời gian phản hồi giao diện
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ phản hồi) |
| **Mô tả yêu cầu** | Các thao tác CRUD cơ bản (xem danh sách, xem chi tiết, thêm/sửa) trên các màn hình nhân sự, hợp đồng lao động và đánh giá khen thưởng/kỷ luật phải hoàn thành hiển thị trong thời gian phản hồi chấp nhận được tùy số người dùng đồng thời. |
| **Độ đo yêu cầu** | - **P95 Response Time cho CRUD** (giây)<br>- **Time to Interactive (TTI)** (giây)<br>- **Contract List Load Time** (giây)<br>- **Contract Detail Load Time** (giây)<br>- **Contract Termination Response Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - **0–10 người dùng đồng thời:** P95 Response Time ≤ **1 giây**, TTI ≤ **1,5 giây**<br>- **11–50 người dùng đồng thời:** P95 Response Time ≤ **2 giây**, TTI ≤ **3 giây**<br>- **51–100 người dùng đồng thời:** P95 Response Time ≤ **5 giây**, TTI ≤ **6 giây**<br>- **Trên 100 người dùng đồng thời:** P95 Response Time ≤ **10 giây**, TTI ≤ **12 giây**<br>- Các ngưỡng trên áp dụng cho toàn bộ thao tác xem/thêm/sửa cơ bản trên hệ thống; riêng các chức năng thuộc **FEAT 7.2**, **FEAT 7.3** và **FEAT 10.2** kế thừa trực tiếp ngưỡng tương ứng theo tải đồng thời. |
| **Phương pháp đo** | Dùng công cụ load test (**JMeter**, **k6**) để đo phân vị 95 của thời gian từ lúc gửi request đến lúc nhận response; đo **TTI** trên trình duyệt từ thời điểm người dùng click đến khi giao diện sẵn sàng tương tác. |
| **Đại lượng thay thế (nếu cần)** | Không cần đại lượng thay thế vì yêu cầu đo trực tiếp được bằng công cụ kiểm thử tải. |

#### SUPL-P02: Số lượng người dùng đồng thời
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Capacity (Khả năng chịu tải) |
| **Mô tả yêu cầu** | Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời mà không suy giảm hiệu năng đáng kể (thời gian phản hồi tăng không quá 50% so với tải thấp). |
| **Độ đo yêu cầu** | - **Max Concurrent Users** (số người)<br>- **Throughput** (transactions/giây)<br>- **Degradation Rate** (%) |
| **Tiêu chuẩn đáp ứng** | - **Max Concurrent Users ≥ 100 người**<br>- **Throughput ≥ 50 tx/s** tại mức **100 concurrent users**<br>- **Degradation Rate ≤ 50%** khi so sánh thời gian phản hồi ở mức **100 users** với mức **1 user** |
| **Phương pháp đo** | Thực hiện **stress test** để tăng dần số kết nối đồng thời cho đến khi response time vượt ngưỡng; dùng **load test** để đếm số giao dịch hoàn thành mỗi giây; so sánh response time giữa tải cao và tải thấp để tính tỷ lệ suy giảm. |
| **Đại lượng thay thế (nếu cần)** | **Số kết nối TCP/WebSocket mà server duy trì ổn định**, đo qua hệ thống giám sát máy chủ. |

#### SUPL-P03: Thời gian tạo báo cáo thống kê
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ xử lý và hiển thị báo cáo) |
| **Mô tả yêu cầu** | Dashboard thống kê và báo cáo tổng hợp (**FEAT 5.1**) phải hoàn thành tải và hiển thị trong các ngưỡng thời gian quy định. |
| **Độ đo yêu cầu** | - **Dashboard Load Time** (giây)<br>- **Complex Report Generation Time** (giây)<br>- **Single Chart Render Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - **Dashboard Load Time ≤ 5 giây**<br>- **Complex Report Generation Time ≤ 15 giây**<br>- **Single Chart Render Time ≤ 3 giây/biểu đồ** |
| **Phương pháp đo** | Đo thời gian từ lúc điều hướng đến dashboard đến khi toàn bộ biểu đồ sẵn sàng hiển thị; đo thời gian từ lúc nhấn **“Tạo báo cáo”** đến khi báo cáo hiển thị hoặc tải xuống hoàn tất; đo riêng thời gian render từng biểu đồ thống kê. |
| **Đại lượng thay thế (nếu cần)** | **Thời gian truy vấn SQL của các query thống kê**, mục tiêu **≤ 2 giây/query**, đo qua **slow query log**. |

#### SUPL-P04: Hiệu năng tìm kiếm và lọc
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ truy vấn dữ liệu) |
| **Mô tả yêu cầu** | Tìm kiếm và lọc danh sách nhân sự, danh sách đánh giá khen thưởng/kỷ luật (**FEAT 10.3, FEAT 8.1, FEAT 8.2**) trên tập dữ liệu lớn phải trả kết quả trong các ngưỡng thời gian quy định theo quy mô dữ liệu. |
| **Độ đo yêu cầu** | - **Search Response Time** (giây)<br>- **Filter Apply Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - Với tập dữ liệu **≤ 10.000 bản ghi**: **Search Response Time ≤ 2 giây**, **Filter Apply Time ≤ 2 giây**<br>- Với tập dữ liệu **≤ 50.000 bản ghi**: **Search Response Time ≤ 5 giây**, **Filter Apply Time ≤ 5 giây** |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng gửi yêu cầu tìm kiếm đến khi danh sách kết quả hiển thị; đo thời gian từ lúc áp dụng bộ lọc đến khi danh sách được cập nhật hoàn chỉnh. |
| **Đại lượng thay thế (nếu cần)** | **Execution time của truy vấn SQL LIKE/FULLTEXT** đo bằng **EXPLAIN ANALYZE**, mục tiêu **≤ 500 ms** với tập dữ liệu **≤ 10.000 bản ghi**. |

#### SUPL-P05: Hiệu năng upload/download file
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ truyền file) |
| **Mô tả yêu cầu** | Việc tải lên và tải xuống các tệp đính kèm dung lượng đến **5 MB** phải hoàn thành trong các ngưỡng thời gian quy định trên môi trường mạng LAN. |
| **Độ đo yêu cầu** | - **Upload Time** (giây)<br>- **Download Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - **Upload Time ≤ 5 giây** cho file **≤ 5 MB** trên mạng LAN<br>- **Download Time ≤ 3 giây** cho file **≤ 5 MB** trên mạng LAN |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng chọn file đến khi server xác nhận lưu thành công; đo thời gian từ lúc nhấn tải xuống đến khi file sẵn sàng mở hoặc hoàn tất tải về. |
| **Đại lượng thay thế (nếu cần)** | **Tốc độ ghi file vào đĩa (MB/s)**, đo qua hệ thống giám sát I/O máy chủ. |

#### SUPL-P06: Hiệu năng xuất Excel
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ xuất dữ liệu) |
| **Mô tả yêu cầu** | Chức năng xuất dữ liệu ra Excel của **FEAT 8.8** phải hoàn thành trong các ngưỡng thời gian quy định theo số lượng bản ghi. |
| **Độ đo yêu cầu** | - **Export Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - Với **≤ 1.000 bản ghi**: **Export Time ≤ 10 giây**<br>- Với **≤ 10.000 bản ghi**: **Export Time ≤ 30 giây** |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng nhấn **“Xuất Excel”** đến khi file tải xuống hoàn tất. |
| **Đại lượng thay thế (nếu cần)** | **Thời gian server sinh file Excel** (không tính thời gian download), đo qua **API response time**. |

## 6.7. Yêu cầu về Độ tin cậy (Reliability)

> Người thực hiện: Nguyễn Hải Ninh

### Danh sách yêu cầu

| STT | ID | Tên yêu cầu | Yếu tố chất lượng | FEAT liên quan |
|-----|----|-------------|-------------------|----------------|
| 1 | SUPL-R01 | Tính sẵn sàng cao (High Availability) | Reliability → Availability (Tính sẵn sàng) | Toàn bộ hệ thống |
| 2 | SUPL-R02 | Khả năng phục hồi sau sự cố | Reliability → Recoverability (Khả năng phục hồi) | Toàn bộ hệ thống |
| 3 | SUPL-R03 | Sao lưu dữ liệu tự động | Reliability → Recoverability (Sao lưu và phục hồi dữ liệu) | Toàn bộ hệ thống |
| 4 | SUPL-R04 | Toàn vẹn dữ liệu | Reliability → Integrity (Tính toàn vẹn dữ liệu) | Toàn bộ hệ thống |
| 5 | SUPL-R05 | Không mất dữ liệu khi phiên hết hạn | Reliability → Fault Tolerance (Chịu lỗi) | Toàn bộ hệ thống |

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-R01: Tính sẵn sàng cao (High Availability)
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Availability (Tính sẵn sàng) |
| **Mô tả yêu cầu** | Hệ thống phải sẵn sàng phục vụ trong khung thời gian **7:00–22:00** hằng ngày với tỷ lệ **uptime tối thiểu 99,5%** trên tổng thời gian phục vụ trong tháng, không tính thời gian bảo trì theo kế hoạch. |
| **Độ đo yêu cầu** | - **Uptime** (%)<br>- **MTBF (Mean Time Between Failures)** (giờ)<br>- **Downtime** (giờ/tháng) |
| **Tiêu chuẩn đáp ứng** | - **Uptime ≥ 99,5%/tháng** trong khung giờ **7:00–22:00**<br>- **MTBF ≥ 720 giờ** (tương đương 30 ngày)<br>- **Downtime ≤ 2,25 giờ/tháng**, không tính bảo trì theo kế hoạch |
| **Phương pháp đo** | Tính tỷ lệ uptime theo công thức **(Tổng thời gian hoạt động / Tổng thời gian dự kiến) × 100**; theo dõi số lần failure để tính MTBF; tổng hợp tổng thời gian hệ thống không truy cập được trong tháng để tính downtime. |
| **Đại lượng thay thế (nếu cần)** | **Tỷ lệ health check endpoint trả lỗi / tổng số health check**, đo qua công cụ giám sát uptime như **UptimeRobot**. |

#### SUPL-R02: Khả năng phục hồi sau sự cố
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Recoverability (Khả năng phục hồi) |
| **Mô tả yêu cầu** | Sau sự cố **crash** hoặc **restart**, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa **15 phút**. |
| **Độ đo yêu cầu** | - **MTTR (Mean Time To Repair)** (phút)<br>- **Restart Time** (phút) |
| **Tiêu chuẩn đáp ứng** | - **MTTR ≤ 15 phút**<br>- **Restart Time ≤ 10 phút** |
| **Phương pháp đo** | Đo thời gian từ thời điểm hệ thống bị crash đến khi phục vụ được request đầu tiên thành công; đo riêng thời gian khởi động lại toàn bộ stack (**database + backend + frontend**). |
| **Đại lượng thay thế (nếu cần)** | Không cần đại lượng thay thế vì có thể đo trực tiếp bằng **drill test** hoặc mô phỏng sự cố. |

#### SUPL-R03: Sao lưu dữ liệu tự động
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Recoverability (Sao lưu và phục hồi dữ liệu) |
| **Mô tả yêu cầu** | Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi **24 giờ**, lưu giữ bản sao lưu tối thiểu **30 ngày** và phục hồi được từ bản sao lưu trong tối đa **4 giờ**. |
| **Độ đo yêu cầu** | - **RPO (Recovery Point Objective)** (giờ)<br>- **RTO (Recovery Time Objective)** (giờ)<br>- **Backup Retention Period** (ngày)<br>- **Backup Success Rate** (%) |
| **Tiêu chuẩn đáp ứng** | - **RPO ≤ 24 giờ**<br>- **RTO ≤ 4 giờ**<br>- **Backup Retention Period ≥ 30 ngày**<br>- **Backup Success Rate ≥ 99%** |
| **Phương pháp đo** | Theo dõi chu kỳ sao lưu tự động; đo khoảng thời gian dữ liệu có thể mất tối đa khi phục hồi từ backup; đo thời gian thực hiện phục hồi hệ thống từ bản sao lưu; thống kê tỷ lệ các lần backup chạy thành công trên tổng số lần backup. |
| **Đại lượng thay thế (nếu cần)** | **Thời gian restore database từ bản backup gần nhất trên môi trường staging** dùng làm proxy cho RTO. |

#### SUPL-R04: Toàn vẹn dữ liệu
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Integrity (Tính toàn vẹn dữ liệu) |
| **Mô tả yêu cầu** | Các thao tác cập nhật dữ liệu quan trọng phải bảo đảm nguyên tắc **toàn bộ hoặc không thực hiện phần nào**; nếu một bước thất bại, hệ thống không được ghi nhận thay đổi dở dang và phải khôi phục dữ liệu về trạng thái trước thao tác. |
| **Độ đo yêu cầu** | - **Data Inconsistency Count** (số trường hợp)<br>- **Integrity Protection Coverage** (%) |
| **Tiêu chuẩn đáp ứng** | - **Data Inconsistency Count = 0**<br>- **Integrity Protection Coverage = 100%** cho các nhóm nghiệp vụ: **hợp đồng, bổ nhiệm, đánh giá, chuyển trạng thái**<br>- Không được ghi nhận **thay đổi một phần** khi có lỗi giữa chừng |
| **Phương pháp đo** | Thực hiện **failure-injection test** để kiểm tra dữ liệu bất nhất quán sau lỗi; đo tỷ lệ thao tác cập nhật quan trọng được kiểm thử lỗi giữa chừng nhưng không phát sinh cập nhật dở dang. |
| **Đại lượng thay thế (nếu cần)** | **Số vi phạm khóa ngoại (Foreign Key violations) và orphaned records** phát hiện qua script kiểm tra toàn vẹn dữ liệu. |

#### SUPL-R05: Không mất dữ liệu khi phiên hết hạn
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Fault Tolerance (Chịu lỗi) |
| **Mô tả yêu cầu** | Trước khi phiên tự động hết hạn, hệ thống phải cảnh báo tối thiểu **5 phút**; nếu phiên vẫn hết hạn thì tỷ lệ mất dữ liệu biểu mẫu chưa lưu không được vượt quá **5%**. |
| **Độ đo yêu cầu** | - **Data Loss Rate** (%)<br>- **Warning Lead Time** (phút) |
| **Tiêu chuẩn đáp ứng** | - **Data Loss Rate ≤ 5%**<br>- **Warning Lead Time ≥ 5 phút** trước khi tự động đăng xuất |
| **Phương pháp đo** | Thực hiện **user testing** để đo tỷ lệ mất dữ liệu form khi phiên hết hạn; đo thời gian hiển thị cảnh báo trước thời điểm hệ thống tự động đăng xuất. |
| **Đại lượng thay thế (nếu cần)** | **Kiểm thử nhị phân Có/Không đối với popup cảnh báo trước khi hết phiên**, dùng làm proxy khi chưa đo được tỷ lệ mất dữ liệu thực tế ở quy mô lớn. |
