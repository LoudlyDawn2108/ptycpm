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
| **Lý do chọn độ đo** | Các ngưỡng này bám theo mốc cảm nhận kinh điển của **Jakob Nielsen**: khoảng **1 giây** là ngưỡng vẫn giữ được mạch suy nghĩ của người dùng, còn khoảng **10 giây** là giới hạn trước khi người dùng mất tập trung. Với HRMS nội bộ, thao tác CRUD thông thường ở tải thấp cần nằm trong khoảng **1–2 giây** để tạo cảm giác phản hồi nhanh; khi tăng lên **51–100 người dùng đồng thời**, ngưỡng **5 giây** được xem là mức chấp nhận được cho **P95** trong giờ cao điểm; mức **10 giây** chỉ là trần chịu tải trong tình huống stress, không phải mục tiêu vận hành thường xuyên. **TTI** được đặt cao hơn response time vì còn bao gồm thời gian render giao diện phía trình duyệt. |
| **Phương pháp đo** | Dùng công cụ load test (**JMeter**, **k6**) để đo phân vị 95 của thời gian từ lúc gửi request đến lúc nhận response; đo **TTI** trên trình duyệt từ thời điểm người dùng click đến khi giao diện sẵn sàng tương tác. |
| **Đại lượng thay thế (nếu cần)** | Không cần đại lượng thay thế vì yêu cầu đo trực tiếp được bằng công cụ kiểm thử tải. |

#### SUPL-P02: Số lượng người dùng đồng thời
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Capacity (Khả năng chịu tải) |
| **Mô tả yêu cầu** | Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời mà không suy giảm hiệu năng đáng kể (thời gian phản hồi tăng không quá 50% so với tải thấp). |
| **Độ đo yêu cầu** | - **Max Concurrent Users** (số người)<br>- **Throughput** (transactions/giây)<br>- **Degradation Rate** (%) |
| **Tiêu chuẩn đáp ứng** | - **Max Concurrent Users ≥ 100 người**<br>- **Throughput ≥ 20 tx/s** tại mức **100 concurrent users**<br>- **Degradation Rate ≤ 50%** khi so sánh thời gian phản hồi ở mức **100 users** với mức **1 user** |
| **Lý do chọn độ đo** | Hệ thống HRMS của trường là hệ thống nội bộ, số người dùng hoạt động đồng thời chủ yếu tập trung ở **Phòng TCCB, Phòng TCKT, quản trị viên** và một phần người dùng tra cứu. Với quy mô khoảng **500–2000 hồ sơ nhân sự**, giả định giờ cao điểm có khoảng **5–10%** người dùng cùng thao tác thì mức **100 người dùng đồng thời** là đủ bao phủ các đợt cao điểm như rà soát hợp đồng, thống kê và xuất dữ liệu. Mức **20 tx/s** tương ứng với tình huống 100 người dùng, trung bình mỗi người thực hiện khoảng 1 thao tác có ý nghĩa trong 4–5 giây, phù hợp hơn với đặc thù nghiệp vụ hành chính so với các hệ thống giao dịch thời gian thực. Ngưỡng suy giảm **≤ 50%** là cách đặt phổ biến để bảo đảm hệ thống vẫn dùng được dưới tải cao mà không đòi hỏi hạ tầng quá lớn. |
| **Phương pháp đo** | Thực hiện **stress test** để tăng dần số kết nối đồng thời cho đến khi response time vượt ngưỡng; dùng **load test** để đếm số giao dịch hoàn thành mỗi giây; so sánh response time giữa tải cao và tải thấp để tính tỷ lệ suy giảm. |
| **Đại lượng thay thế (nếu cần)** | **Số kết nối TCP/WebSocket mà server duy trì ổn định**, đo qua hệ thống giám sát máy chủ. |

#### SUPL-P03: Thời gian tạo báo cáo thống kê
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ xử lý và hiển thị báo cáo) |
| **Mô tả yêu cầu** | Dashboard thống kê và báo cáo tổng hợp (**FEAT 5.1**) phải hoàn thành tải và hiển thị trong các ngưỡng thời gian quy định. |
| **Độ đo yêu cầu** | - **Dashboard Load Time** (giây)<br>- **Complex Report Generation Time** (giây)<br>- **Single Chart Render Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - **Dashboard Load Time ≤ 5 giây**<br>- **Complex Report Generation Time ≤ 15 giây**<br>- **Single Chart Render Time ≤ 3 giây/biểu đồ** |
| **Lý do chọn độ đo** | Dashboard là màn hình vào việc nên cần phản hồi nhanh hơn báo cáo tổng hợp; vì vậy ngưỡng **5 giây** được chọn để người dùng vẫn cảm thấy hệ thống phản hồi trong một lần chờ ngắn. Với **biểu đồ đơn lẻ**, mức **3 giây** gần với ngưỡng tải trang tốt theo **Google Web Vitals (LCP ≤ 2,5 giây)** nhưng nới thêm một phần do dashboard thống kê còn phải xử lý dữ liệu nghiệp vụ. Riêng **báo cáo tổng hợp phức tạp** cho phép tới **15 giây** vì đây là tác vụ phân tích theo lô, thường gom nhiều truy vấn/tập dữ liệu và là một “điểm dừng tự nhiên” trong công việc; vượt quá mức này thì người dùng bắt đầu thấy chờ lâu và cần hiển thị trạng thái tiến trình. |
| **Phương pháp đo** | Đo thời gian từ lúc điều hướng đến dashboard đến khi toàn bộ biểu đồ sẵn sàng hiển thị; đo thời gian từ lúc nhấn **“Tạo báo cáo”** đến khi báo cáo hiển thị hoặc tải xuống hoàn tất; đo riêng thời gian render từng biểu đồ thống kê. |
| **Đại lượng thay thế (nếu cần)** | **Thời gian truy vấn SQL của các query thống kê**, mục tiêu **≤ 2 giây/query**, đo qua **slow query log**. |

#### SUPL-P04: Hiệu năng tìm kiếm và lọc
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ truy vấn dữ liệu) |
| **Mô tả yêu cầu** | Tìm kiếm và lọc danh sách nhân sự, danh sách đánh giá khen thưởng/kỷ luật (**FEAT 10.3, FEAT 8.1, FEAT 8.2**) trên tập dữ liệu lớn phải trả kết quả trong các ngưỡng thời gian quy định theo quy mô dữ liệu. |
| **Độ đo yêu cầu** | - **Search Response Time** (giây)<br>- **Filter Apply Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - Với tập dữ liệu **≤ 10.000 bản ghi**: **Search Response Time ≤ 2 giây**, **Filter Apply Time ≤ 2 giây**<br>- Với tập dữ liệu **≤ 50.000 bản ghi**: **Search Response Time ≤ 5 giây**, **Filter Apply Time ≤ 5 giây** |
| **Lý do chọn độ đo** | Tìm kiếm/lọc là thao tác tương tác trực tiếp nên phải gần ngưỡng “giữ được luồng làm việc” của người dùng; vì vậy mức **≤ 2 giây** cho **≤ 10.000 bản ghi** là phù hợp với danh sách chính có đánh chỉ mục tốt. Mức **≤ 50.000 bản ghi** được dùng để bao phủ các bảng lịch sử như hợp đồng, đánh giá, biến động và các truy vấn có kết hợp nhiều điều kiện; với quy mô này, ngưỡng **≤ 5 giây** vẫn chấp nhận được cho hệ thống nội bộ trong giờ cao điểm. Proxy **≤ 500 ms** cho truy vấn SQL được chọn vì trong một yêu cầu web hoàn chỉnh còn có thời gian mạng, serialization, phân quyền và render giao diện; như vậy phần truy vấn cơ sở dữ liệu nên chỉ chiếm một phần nhỏ của tổng thời gian phản hồi. |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng gửi yêu cầu tìm kiếm đến khi danh sách kết quả hiển thị; đo thời gian từ lúc áp dụng bộ lọc đến khi danh sách được cập nhật hoàn chỉnh. |
| **Đại lượng thay thế (nếu cần)** | **Execution time của truy vấn SQL LIKE/FULLTEXT** đo bằng **EXPLAIN ANALYZE**, mục tiêu **≤ 500 ms** với tập dữ liệu **≤ 10.000 bản ghi**. |

#### SUPL-P05: Hiệu năng upload/download file
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ truyền file) |
| **Mô tả yêu cầu** | Việc tải lên và tải xuống các tệp đính kèm phải hoàn thành trong các ngưỡng thời gian quy định trên môi trường mạng LAN; ngưỡng đánh giá bao phủ cả kích thước thường gặp và kích thước tối đa hệ thống cho phép. |
| **Độ đo yêu cầu** | - **Upload Time** (giây)<br>- **Download Time** (giây)<br>- **Kích thước file kiểm thử** (MB) |
| **Tiêu chuẩn đáp ứng** | - Với file **≤ 5 MB**: **Upload Time ≤ 5 giây**, **Download Time ≤ 3 giây** trên mạng LAN<br>- Với file **> 5 MB đến ≤ 10 MB**: **Upload Time ≤ 10 giây**, **Download Time ≤ 6 giây** trên mạng LAN |
| **Lý do chọn độ đo** | Trong HRMS, phần lớn tệp đính kèm như hợp đồng scan, bằng cấp, chứng chỉ PDF thường nằm trong khoảng **1–5 MB**; vì vậy ngưỡng **5 MB** được dùng cho “mức sử dụng thường xuyên”. Tuy nhiên hệ thống cho phép tối đa **10 MB/file**, nên cần thêm ngưỡng cho khoảng **5–10 MB** để tránh mâu thuẫn với ràng buộc triển khai. Trên mạng LAN văn phòng (thường từ **100 Mbps** trở lên), thời gian truyền lý thuyết của 5 MB khá nhỏ; phần thời gian còn lại chủ yếu đến từ quét file, ghi đĩa, xác thực và phản hồi ứng dụng. Do đó các mức **3–5 giây** cho file thường gặp và **6–10 giây** cho file cận ngưỡng tối đa là chặt nhưng vẫn khả thi. |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng chọn file đến khi server xác nhận lưu thành công; đo thời gian từ lúc nhấn tải xuống đến khi file sẵn sàng mở hoặc hoàn tất tải về. |
| **Đại lượng thay thế (nếu cần)** | **Tốc độ ghi file vào đĩa (MB/s)**, đo qua hệ thống giám sát I/O máy chủ. |

#### SUPL-P06: Hiệu năng xuất Excel
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Performance → Speed (Tốc độ xuất dữ liệu) |
| **Mô tả yêu cầu** | Chức năng xuất dữ liệu ra Excel của **FEAT 8.8** phải hoàn thành trong các ngưỡng thời gian quy định theo số lượng bản ghi. |
| **Độ đo yêu cầu** | - **Export Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - Với **≤ 1.000 bản ghi**: **Export Time ≤ 10 giây**<br>- Với **≤ 10.000 bản ghi**: **Export Time ≤ 30 giây** |
| **Lý do chọn độ đo** | Xuất Excel là tác vụ xử lý theo lô, không yêu cầu “tức thì” như CRUD nhưng vẫn phải đủ nhanh để người dùng không rời bỏ tác vụ. Mức **≤ 10 giây** cho **≤ 1.000 bản ghi** phù hợp với nhu cầu xuất danh sách nhân sự theo đơn vị hoặc bộ lọc thông thường. Mức **≤ 30 giây** cho **≤ 10.000 bản ghi** bao phủ trường hợp xuất dữ liệu lớn hơn, gồm nhiều cột và định dạng Excel, đồng thời vẫn nằm trong khoảng chờ có thể chấp nhận cho thao tác báo cáo nội bộ. Các mốc này cũng nhất quán với logic **Nielsen**: thao tác vượt **10 giây** chỉ nên xuất hiện ở tác vụ batch rõ ràng như export, không phải ở tương tác duyệt màn hình. |
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
| **Tiêu chuẩn đáp ứng** | - **Uptime ≥ 99,5%/tháng** trong khung giờ **7:00–22:00**<br>- **MTBF ≥ 225 giờ** trong khung giờ phục vụ<br>- **Downtime ≤ 2,25 giờ/tháng**, không tính bảo trì theo kế hoạch |
| **Lý do chọn độ đo** | HRMS của trường là hệ thống quan trọng trong giờ làm việc nhưng không phải hệ thống **24/7** như ngân hàng hay cấp cứu, vì vậy mức **99,5%** là phù hợp hơn mức 99,9% vốn đòi hỏi hạ tầng dự phòng tốn kém. Với khung phục vụ **7:00–22:00** tương đương khoảng **450 giờ/tháng**, ngưỡng **99,5%** suy ra downtime tối đa khoảng **2,25 giờ/tháng** trong thời gian phục vụ. Chỉ số **MTBF ≥ 225 giờ** được chọn để phản ánh mục tiêu không quá khoảng **2 sự cố nghiêm trọng/tháng** trong khung phục vụ; con số này bám sát bối cảnh vận hành nội bộ hơn mức 720 giờ tính theo 24/7. |
| **Phương pháp đo** | Tính tỷ lệ uptime theo công thức **(Tổng thời gian hoạt động / Tổng thời gian dự kiến) × 100**; theo dõi số lần failure để tính MTBF; tổng hợp tổng thời gian hệ thống không truy cập được trong tháng để tính downtime. |
| **Đại lượng thay thế (nếu cần)** | **Tỷ lệ health check endpoint trả lỗi / tổng số health check**, đo qua công cụ giám sát uptime như **UptimeRobot**. |

#### SUPL-R02: Khả năng phục hồi sau sự cố
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Recoverability (Khả năng phục hồi) |
| **Mô tả yêu cầu** | Sau sự cố **crash** hoặc **restart**, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa **15 phút**. |
| **Độ đo yêu cầu** | - **MTTR (Mean Time To Repair)** (phút)<br>- **Restart Time** (phút) |
| **Tiêu chuẩn đáp ứng** | - **MTTR ≤ 15 phút**<br>- **Restart Time ≤ 10 phút** |
| **Lý do chọn độ đo** | Với hệ thống nội bộ phục vụ nghiệp vụ nhân sự, thời gian gián đoạn trên **15 phút** bắt đầu ảnh hưởng rõ rệt đến tác vụ hành chính liên tục như cập nhật hồ sơ, tra cứu hợp đồng và xuất báo cáo. Mức **Restart Time ≤ 10 phút** được chọn để dành thêm khoảng đệm cho kiểm tra sức khỏe hệ thống, nạp cache và xác nhận hệ thống phục hồi ổn định trước khi tính đủ **MTTR ≤ 15 phút**. Đây là mức khắt khe vừa phải đối với năng lực của một bộ phận CNTT trường đại học, nhưng vẫn đủ bảo đảm khôi phục trong cùng phiên làm việc. |
| **Phương pháp đo** | Đo thời gian từ thời điểm hệ thống bị crash đến khi phục vụ được request đầu tiên thành công; đo riêng thời gian khởi động lại toàn bộ stack (**database + backend + frontend**). |
| **Đại lượng thay thế (nếu cần)** | Không cần đại lượng thay thế vì có thể đo trực tiếp bằng **drill test** hoặc mô phỏng sự cố. |

#### SUPL-R03: Sao lưu dữ liệu tự động
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Recoverability (Sao lưu và phục hồi dữ liệu) |
| **Mô tả yêu cầu** | Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi **24 giờ**, lưu giữ bản sao lưu tối thiểu **30 ngày** và phục hồi được từ bản sao lưu trong tối đa **4 giờ**. |
| **Độ đo yêu cầu** | - **RPO (Recovery Point Objective)** (giờ)<br>- **RTO (Recovery Time Objective)** (giờ)<br>- **Backup Retention Period** (ngày)<br>- **Backup Success Rate** (%) |
| **Tiêu chuẩn đáp ứng** | - **RPO ≤ 24 giờ**<br>- **RTO ≤ 4 giờ**<br>- **Backup Retention Period ≥ 30 ngày**<br>- **Backup Success Rate ≥ 99%** |
| **Lý do chọn độ đo** | Dữ liệu HRMS chủ yếu phát sinh theo ca hành chính chứ không phải giao dịch liên tục từng giây; do đó **RPO ≤ 24 giờ** tương ứng với chu kỳ sao lưu hằng ngày là cân bằng giữa an toàn dữ liệu và chi phí lưu trữ/vận hành. **RTO ≤ 4 giờ** bảo đảm nếu xảy ra sự cố, hệ thống vẫn có thể được phục hồi trong cùng ngày làm việc. Thời gian lưu giữ **≥ 30 ngày** bám theo chu kỳ nghiệp vụ tháng như đối soát hợp đồng, lương, phụ cấp và phát hiện sai sót muộn. Mức **Backup Success Rate ≥ 99%** đủ cao để coi sao lưu là đáng tin cậy nhưng vẫn thực tế hơn 100% tuyệt đối, vì vẫn có thể có các lần chạy lỗi do bảo trì hoặc sự cố hạ tầng cần chạy lại. |
| **Phương pháp đo** | Theo dõi chu kỳ sao lưu tự động; đo khoảng thời gian dữ liệu có thể mất tối đa khi phục hồi từ backup; đo thời gian thực hiện phục hồi hệ thống từ bản sao lưu; thống kê tỷ lệ các lần backup chạy thành công trên tổng số lần backup. |
| **Đại lượng thay thế (nếu cần)** | **Thời gian restore database từ bản backup gần nhất trên môi trường staging** dùng làm proxy cho RTO. |

#### SUPL-R04: Toàn vẹn dữ liệu
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Integrity (Tính toàn vẹn dữ liệu) |
| **Mô tả yêu cầu** | Các thao tác cập nhật dữ liệu quan trọng phải bảo đảm nguyên tắc **toàn bộ hoặc không thực hiện phần nào**; nếu một bước thất bại, hệ thống không được ghi nhận thay đổi dở dang và phải khôi phục dữ liệu về trạng thái trước thao tác. |
| **Độ đo yêu cầu** | - **Data Inconsistency Count** (số trường hợp)<br>- **Integrity Protection Coverage** (%) |
| **Tiêu chuẩn đáp ứng** | - **Data Inconsistency Count = 0**<br>- **Integrity Protection Coverage = 100%** cho các nhóm nghiệp vụ: **hợp đồng, bổ nhiệm, đánh giá, chuyển trạng thái**<br>- Không được ghi nhận **thay đổi một phần** khi có lỗi giữa chừng |
| **Lý do chọn độ đo** | Với dữ liệu nhân sự, hợp đồng và đánh giá, yêu cầu về toàn vẹn gần như không có vùng “chấp nhận sai số”; chỉ cần một bản ghi cập nhật dở dang cũng có thể dẫn đến sai lệch hồ sơ pháp lý hoặc sai báo cáo. Vì vậy **Data Inconsistency Count = 0** là mục tiêu bắt buộc, phù hợp với nguyên tắc **ACID transaction** của cơ sở dữ liệu quan hệ. Mức **100% coverage** cho các nghiệp vụ trọng yếu được chọn vì đây là nhóm thao tác có rủi ro cao nhất nếu xảy ra cập nhật nửa chừng; các phép đo thấp hơn sẽ khó thuyết phục trong bối cảnh dữ liệu nhân sự cần độ chính xác tuyệt đối. |
| **Phương pháp đo** | Thực hiện **failure-injection test** để kiểm tra dữ liệu bất nhất quán sau lỗi; đo tỷ lệ thao tác cập nhật quan trọng được kiểm thử lỗi giữa chừng nhưng không phát sinh cập nhật dở dang. |
| **Đại lượng thay thế (nếu cần)** | **Số vi phạm khóa ngoại (Foreign Key violations) và orphaned records** phát hiện qua script kiểm tra toàn vẹn dữ liệu. |

#### SUPL-R05: Không mất dữ liệu khi phiên hết hạn
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng** | Reliability → Fault Tolerance (Chịu lỗi) |
| **Mô tả yêu cầu** | Trước khi phiên tự động hết hạn, hệ thống phải cảnh báo tối thiểu **5 phút**; nếu phiên vẫn hết hạn thì tỷ lệ mất dữ liệu biểu mẫu chưa lưu không được vượt quá **5%**. |
| **Độ đo yêu cầu** | - **Draft Recovery Rate** (%)<br>- **Session Expiry Warning Coverage** (%)<br>- **Warning Lead Time** (phút) |
| **Tiêu chuẩn đáp ứng** | - **Draft Recovery Rate ≥ 95%** đối với form có dữ liệu nhập dở khi người dùng đăng nhập lại<br>- **Session Expiry Warning Coverage = 100%** đối với các phiên sắp hết hạn<br>- **Warning Lead Time ≥ 5 phút** trước khi tự động đăng xuất |
| **Lý do chọn độ đo** | Với biểu mẫu nhân sự nhiều trường, việc mất toàn bộ dữ liệu đã nhập là rất tốn thời gian và dễ gây bức xúc cho người dùng, nên hệ thống phải cảnh báo trước và khôi phục bản nháp ở mức cao. Ngưỡng cảnh báo **5 phút** đủ để người dùng hoàn tất thao tác lưu hoặc chủ động gia hạn phiên, đồng thời phù hợp với phiên timeout **30 phút** của hệ thống. Mức **100% warning coverage** là hợp lý vì đây là chức năng do chính hệ thống kiểm soát. Riêng **Draft Recovery Rate ≥ 95%** được chọn thay vì 100% tuyệt đối vì khả năng khôi phục còn phụ thuộc các tình huống ngoài kiểm soát như người dùng đóng tab cưỡng bức, trình duyệt xóa session/local storage hoặc sự cố máy trạm; 95% là ngưỡng cao nhưng vẫn thực tế và kiểm thử được. |
| **Phương pháp đo** | Thực hiện **user testing** hoặc mô phỏng hết phiên trên các form nhập liệu dài để đo tỷ lệ khôi phục dữ liệu nháp sau khi đăng nhập lại; đo tỷ lệ xuất hiện cảnh báo và thời gian cảnh báo trước khi hệ thống tự động đăng xuất. |
| **Đại lượng thay thế (nếu cần)** | **Kiểm thử nhị phân Có/Không đối với popup cảnh báo trước khi hết phiên** và kiểm tra sự tồn tại của bản nháp lưu tạm trên trình duyệt/máy chủ. |
