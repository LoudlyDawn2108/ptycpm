# Mục VI — Yêu cầu bổ sung / yêu cầu phi chức năng

## 6.6. Yêu cầu về Hiệu năng (Performance)

> Người thực hiện: Ngô Quang Tùng

### Danh sách yêu cầu

| STT | ID | Yêu cầu (mô tả ngắn) | Yếu tố chất lượng chính | FEAT liên quan |
|-----|----|----------------------|--------------------------|----------------|
| 1 | SUPL-P01 | Hệ thống phải hoàn thành thao tác xem/thêm/sửa hồ sơ nhân sự và hợp đồng với P95 Response Time ≤ 1–5 giây và TTI ≤ 1,5–6 giây theo 3 mức tải đồng thời | Performance → Response time | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 2 | SUPL-P02 | Hệ thống phải hỗ trợ tối thiểu 100 người dùng đồng thời với mức suy giảm thời gian phản hồi không quá 50% so với tải một người dùng | Performance → Capacity | FEAT 7.1–8.9 |
| 3 | SUPL-P03a | Hệ thống phải hiển thị chi tiết hồ sơ nhân sự tổng hợp trong tối đa 5 giây ở mức ≤ 10 người dùng đồng thời | Performance → Response time | FEAT 8.7 |
| 4 | SUPL-P03b | Hệ thống phải chuẩn bị dữ liệu in hồ sơ nhân sự trong tối đa 10 giây ở mức ≤ 10 người dùng đồng thời | Performance → Response time | FEAT 8.8 |
| 5 | SUPL-P04 | Hệ thống phải trả kết quả tìm kiếm và lọc hồ sơ nhân sự trong tối đa 2–5 giây tùy quy mô dữ liệu ở mức ≤ 50 người dùng đồng thời | Performance → Response time | FEAT 8.1, FEAT 8.2 |
| 6 | SUPL-P05 | Hệ thống phải hoàn thành upload/download tệp đính kèm trong tối đa 3–10 giây trên mạng LAN 1 Gbps ở mức ≤ 10 người dùng đồng thời, tùy kích thước tệp | Performance → Response time | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| 7 | SUPL-P06 | Hệ thống phải xuất dữ liệu hồ sơ nhân sự ra Excel trong tối đa 10–30 giây tùy số lượng bản ghi ở mức ≤ 10 người dùng đồng thời | Performance → Response time | FEAT 8.8 |
| 8 | SUPL-R02 | Hệ thống phải phục hồi khả năng phục vụ sau sự cố trong tối đa 15 phút và khởi động lại toàn bộ stack trong tối đa 10 phút | Performance → Recovery time | FEAT 7.1–8.9 |
| 9 | SUPL-R03b | Hệ thống phải phục hồi từ bản sao lưu gần nhất và sẵn sàng phục vụ trong tối đa 4 giờ | Performance → Recovery time | FEAT 7.1–8.9 |

> **Ghi chú phân loại:** `SUPL-R02` và `SUPL-R03b` được giữ nguyên tiền tố ID gốc để tránh phá vỡ tham chiếu ở các tài liệu liên quan, nhưng **primary classification** của hai yêu cầu này thuộc **Performance → Recovery time** vì trọng tâm đo kiểm là **thời gian phục hồi dịch vụ**.
>
> **Ghi chú tách yêu cầu để tăng tính atomic:** `SUPL-P03` trong tài liệu tổng hợp được tách thành `SUPL-P03a` và `SUPL-P03b` trong fragment này; `SUPL-R05` ở mục 6.7 được tách thành `SUPL-R05a` và `SUPL-R05b`. Việc tách này chỉ nhằm làm rõ các nghĩa vụ kiểm thử độc lập, không làm thay đổi ý nghĩa gốc của requirement cha.
>
> **Quy ước đo kiểm trong nhóm Performance:** `SUPL-P01` dùng **P95 Response Time** và **TTI**; các yêu cầu `SUPL-P03a–SUPL-P06` dùng **thời gian hoàn tất tối đa quan sát được** trong điều kiện kiểm thử nêu kèm từng yêu cầu.

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-P01: Hệ thống phải hoàn thành thao tác xem/thêm/sửa hồ sơ nhân sự và hợp đồng với P95 Response Time ≤ 1–5 giây và TTI ≤ 1,5–6 giây theo 3 mức tải đồng thời
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Response time |
| **Mô tả yêu cầu** | Hệ thống phải hoàn thành thao tác xem danh sách, xem chi tiết, thêm mới hoặc chỉnh sửa trên các màn hình hợp đồng và hồ sơ nhân sự với **P95 Response Time ≤ 1 giây và TTI ≤ 1,5 giây** ở mức **0–10 người dùng đồng thời**, **P95 Response Time ≤ 2 giây và TTI ≤ 3 giây** ở mức **11–50 người dùng đồng thời**, và **P95 Response Time ≤ 5 giây và TTI ≤ 6 giây** ở mức **51–100 người dùng đồng thời**. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| **Độ đo yêu cầu** | - **P95 Response Time** cho thao tác nghiệp vụ cơ bản (giây)<br>- **Time to Interactive (TTI)** trên giao diện web (giây) |
| **Tiêu chuẩn đáp ứng** | - **0–10 người dùng đồng thời:** P95 Response Time ≤ **1 giây**, TTI ≤ **1,5 giây**<br>- **11–50 người dùng đồng thời:** P95 Response Time ≤ **2 giây**, TTI ≤ **3 giây**<br>- **51–100 người dùng đồng thời:** P95 Response Time ≤ **5 giây**, TTI ≤ **6 giây** |
| **Lý do chọn độ đo** | Các mốc này bám theo ngưỡng cảm nhận phổ biến của người dùng web nghiệp vụ: thao tác thường xuyên cần phản hồi ở mức 1–2 giây để không làm đứt mạch công việc; trong giờ cao điểm, ngưỡng 5 giây ở P95 vẫn còn chấp nhận được cho hệ thống nội bộ. TTI được giữ cao hơn response time vì còn bao gồm thời gian render giao diện phía trình duyệt. |
| **Phương pháp đo** | Dùng công cụ load test như **JMeter** hoặc **k6** để đo P95 Response Time; đo TTI trên trình duyệt từ lúc người dùng thực hiện thao tác đến khi giao diện sẵn sàng tương tác lại. |
| **Đại lượng thay thế (nếu cần)** | Không dùng đại lượng thay thế vì có thể đo trực tiếp bằng công cụ kiểm thử tải. |

#### SUPL-P02: Hệ thống phải hỗ trợ tối thiểu 100 người dùng đồng thời với mức suy giảm thời gian phản hồi không quá 50% so với tải một người dùng
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Capacity |
| **Mô tả yêu cầu** | Hệ thống phải hỗ trợ tối thiểu **100 người dùng đồng thời** trong giờ cao điểm mà không làm thời gian phản hồi tăng quá **50%** so với tải một người dùng; chỉ số **Throughput ≥ 50 tx/s** được dùng như chỉ số nghiệm thu dẫn xuất cho cùng kịch bản kiểm thử tải. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **Max Concurrent Users** (số người)<br>- **Throughput** (transactions/giây)<br>- **Degradation Rate** (%) |
| **Tiêu chuẩn đáp ứng** | - **Max Concurrent Users ≥ 100 người**<br>- **Throughput ≥ 50 tx/s** tại mức **100 concurrent users**<br>- **Degradation Rate ≤ 50%** khi so sánh response time ở mức **100 users** với mức **1 user** |
| **Lý do chọn độ đo** | Với HRMS nội bộ của trường, tải cao điểm cho phạm vi của Tùng tập trung ở các đợt rà soát hợp đồng, cập nhật hồ sơ và tra cứu hồ sơ nhân sự. Mức 100 người dùng đồng thời bao phủ được các tình huống này; throughput 50 tx/s được dùng như **chỉ số dẫn xuất** để xác nhận hệ thống vẫn vận hành ổn định dưới mức tải mục tiêu này. |
| **Phương pháp đo** | Thực hiện stress test để tăng dần số kết nối đồng thời cho đến khi response time vượt ngưỡng; dùng load test để đo throughput và so sánh response time giữa tải cao với tải thấp để tính tỷ lệ suy giảm. |
| **Đại lượng thay thế (nếu cần)** | Số kết nối TCP/WebSocket mà máy chủ duy trì ổn định, đo qua hệ thống giám sát hạ tầng. |

#### SUPL-P03a: Hệ thống phải hiển thị chi tiết hồ sơ nhân sự tổng hợp trong tối đa 5 giây ở mức ≤ 10 người dùng đồng thời
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Response time |
| **Mô tả yêu cầu** | Hệ thống phải hiển thị trang chi tiết hồ sơ nhân sự tổng hợp nhiều nhóm thông tin trong tối đa **5 giây** tại mức **≤ 10 người dùng đồng thời**. |
| **Importance** | Desirable |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 8.7 |
| **Độ đo yêu cầu** | - **Employee Profile Detail Load Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - **Employee Profile Detail Load Time ≤ 5 giây** tại mức **≤ 10 người dùng đồng thời** |
| **Lý do chọn độ đo** | FEAT 8.7 thuộc phạm vi hồ sơ nhân sự do Tùng phụ trách, và trang chi tiết hồ sơ là màn hình tổng hợp nhiều nhóm thông tin hơn các thao tác CRUD thông thường. Việc tách requirement này khỏi thao tác in hồ sơ giúp mỗi nghĩa vụ kiểm thử chỉ còn một ngưỡng phản hồi duy nhất. |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng mở hồ sơ chi tiết đến khi toàn bộ dữ liệu hồ sơ sẵn sàng hiển thị và người dùng có thể tiếp tục thao tác trên trang. |
| **Đại lượng thay thế (nếu cần)** | Thời gian truy vấn và tổng hợp dữ liệu hồ sơ nhân sự ở phía máy chủ, đo qua application log hoặc APM. |

#### SUPL-P03b: Hệ thống phải chuẩn bị dữ liệu in hồ sơ nhân sự trong tối đa 10 giây ở mức ≤ 10 người dùng đồng thời
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Response time |
| **Mô tả yêu cầu** | Hệ thống phải chuẩn bị dữ liệu phục vụ **in hồ sơ nhân sự** trong tối đa **10 giây** tại mức **≤ 10 người dùng đồng thời**. |
| **Importance** | Desirable |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 8.8 |
| **Độ đo yêu cầu** | - **Profile Print Preparation Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - **Profile Print Preparation Time ≤ 10 giây** tại mức **≤ 10 người dùng đồng thời** |
| **Lý do chọn độ đo** | Chuẩn bị dữ liệu in hồ sơ là một thao tác hậu xử lý riêng, khác với việc mở trang chi tiết hồ sơ. Việc tách thành requirement độc lập giúp đánh giá đúng chi phí xử lý dữ liệu trước khi in và tránh nhập nhằng kết quả kiểm thử với thời gian tải trang chi tiết. |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng chọn in hồ sơ đến khi dữ liệu sẵn sàng cho bước in hoặc sinh tài liệu đầu ra. |
| **Đại lượng thay thế (nếu cần)** | Thời gian tổng hợp dữ liệu in hồ sơ ở phía máy chủ, đo qua application log hoặc APM. |

#### SUPL-P04: Hệ thống phải trả kết quả tìm kiếm và lọc hồ sơ nhân sự trong tối đa 2–5 giây tùy quy mô dữ liệu ở mức ≤ 50 người dùng đồng thời
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Response time |
| **Mô tả yêu cầu** | Hệ thống phải trả kết quả tìm kiếm và lọc danh sách hồ sơ nhân sự trong tối đa **2 giây** đối với tập dữ liệu **≤ 10.000 bản ghi** và trong tối đa **5 giây** đối với tập dữ liệu **≤ 50.000 bản ghi**, tại mức **≤ 50 người dùng đồng thời**. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 8.1, FEAT 8.2 |
| **Độ đo yêu cầu** | - **Search Response Time** (giây)<br>- **Filter Apply Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - Với tập dữ liệu **≤ 10.000 bản ghi**: **Search Response Time ≤ 2 giây**, **Filter Apply Time ≤ 2 giây**, tại mức **≤ 50 người dùng đồng thời**<br>- Với tập dữ liệu **≤ 50.000 bản ghi**: **Search Response Time ≤ 5 giây**, **Filter Apply Time ≤ 5 giây**, tại mức **≤ 50 người dùng đồng thời** |
| **Lý do chọn độ đo** | Tìm kiếm và lọc là thao tác tương tác trực tiếp, nên mục tiêu cần đủ thấp để người dùng giữ được luồng công việc. Hai mức 10.000 và 50.000 bản ghi phản ánh lần lượt tình huống danh sách thông thường và tình huống dữ liệu lịch sử lớn hơn trong hệ thống nội bộ; việc thêm điều kiện tải giúp kết quả kiểm thử có ý nghĩa vận hành rõ ràng hơn. |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng gửi yêu cầu tìm kiếm đến khi danh sách kết quả hiển thị; đo thời gian từ lúc áp dụng bộ lọc đến khi danh sách được cập nhật hoàn chỉnh. |
| **Đại lượng thay thế (nếu cần)** | Execution time của truy vấn SQL LIKE/FULLTEXT đo bằng **EXPLAIN ANALYZE**, mục tiêu **≤ 500 ms** với tập dữ liệu **≤ 10.000 bản ghi**. |

#### SUPL-P05: Hệ thống phải hoàn thành upload/download tệp đính kèm trong tối đa 3–10 giây trên mạng LAN 1 Gbps ở mức ≤ 10 người dùng đồng thời, tùy kích thước tệp
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Response time |
| **Mô tả yêu cầu** | Hệ thống phải hoàn thành **upload** và **download** các tệp đính kèm của hồ sơ nhân sự và hợp đồng trên môi trường **mạng LAN 1 Gbps** trong tối đa **5 giây** và **3 giây** tương ứng đối với tệp **≤ 5 MB**, và trong tối đa **10 giây** và **6 giây** tương ứng đối với tệp **> 5 MB đến ≤ 10 MB**, tại mức **≤ 10 người dùng đồng thời** thực hiện tác vụ upload/download. |
| **Importance** | Desirable |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 7.1, FEAT 7.2, FEAT 7.3, FEAT 8.3, FEAT 8.4, FEAT 8.7 |
| **Độ đo yêu cầu** | - **Upload Time** (giây)<br>- **Download Time** (giây)<br>- **Kích thước file kiểm thử** (MB) |
| **Tiêu chuẩn đáp ứng** | - Với file **≤ 5 MB**: **Upload Time ≤ 5 giây**, **Download Time ≤ 3 giây** trên mạng **LAN 1 Gbps**, tại mức **≤ 10 người dùng đồng thời**<br>- Với file **> 5 MB đến ≤ 10 MB**: **Upload Time ≤ 10 giây**, **Download Time ≤ 6 giây** trên mạng **LAN 1 Gbps**, tại mức **≤ 10 người dùng đồng thời** |
| **Lý do chọn độ đo** | Phần lớn tệp đính kèm của HRMS như hợp đồng scan, bằng cấp và chứng chỉ nằm trong khoảng 1–5 MB; tuy nhiên hệ thống cho phép tối đa 10 MB/file nên cần có thêm ngưỡng cho khoảng 5–10 MB để đặc tả không mâu thuẫn với ràng buộc triển khai. |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng chọn file đến khi máy chủ xác nhận lưu thành công; đo thời gian từ lúc nhấn tải xuống đến khi file sẵn sàng mở hoặc tải về hoàn tất. |
| **Đại lượng thay thế (nếu cần)** | Tốc độ ghi file vào đĩa (MB/s), đo qua hệ thống giám sát I/O máy chủ. |

#### SUPL-P06: Hệ thống phải xuất dữ liệu hồ sơ nhân sự ra Excel trong tối đa 10–30 giây tùy số lượng bản ghi ở mức ≤ 10 người dùng đồng thời
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Response time |
| **Mô tả yêu cầu** | Hệ thống phải hoàn thành xuất dữ liệu hồ sơ nhân sự ra Excel trong tối đa **10 giây** đối với tập **≤ 1.000 bản ghi** và trong tối đa **30 giây** đối với tập **≤ 10.000 bản ghi**, tại mức **≤ 10 người dùng đồng thời** thực hiện tác vụ xuất dữ liệu. |
| **Importance** | Desirable |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 8.8 |
| **Độ đo yêu cầu** | - **Export Time** (giây) |
| **Tiêu chuẩn đáp ứng** | - Với **≤ 1.000 bản ghi**: **Export Time ≤ 10 giây** tại mức **≤ 10 người dùng đồng thời** thực hiện xuất dữ liệu<br>- Với **≤ 10.000 bản ghi**: **Export Time ≤ 30 giây** tại mức **≤ 10 người dùng đồng thời** thực hiện xuất dữ liệu |
| **Lý do chọn độ đo** | Xuất Excel là tác vụ xử lý theo lô nên không cần nhanh như CRUD, nhưng vẫn phải đủ ngắn để người dùng không rời bỏ tác vụ. Hai mức 1.000 và 10.000 bản ghi phù hợp với tình huống xuất danh sách hồ sơ đã lọc và xuất dữ liệu nhân sự quy mô lớn hơn trong phạm vi FEAT 8.8; việc thêm điều kiện tải giúp giới hạn chấp nhận rõ ràng hơn khi nghiệm thu. |
| **Phương pháp đo** | Đo thời gian từ lúc người dùng nhấn **Xuất Excel** đến khi file tải xuống hoàn tất. |
| **Đại lượng thay thế (nếu cần)** | Thời gian máy chủ sinh file Excel, không tính thời gian download, đo qua **API response time**. |

#### SUPL-R02: Hệ thống phải phục hồi khả năng phục vụ sau sự cố trong tối đa 15 phút và khởi động lại toàn bộ stack trong tối đa 10 phút
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Recovery time |
| **Mô tả yêu cầu** | Sau sự cố **crash** hoặc **restart**, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa **15 phút**, với thời gian khởi động lại toàn bộ stack không quá **10 phút**. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Sharp |
| **Verification** | Test |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **Time to Restore Service** (phút)<br>- **Restart Time** (phút) |
| **Tiêu chuẩn đáp ứng** | - **Time to Restore Service ≤ 15 phút**<br>- **Restart Time ≤ 10 phút** |
| **Lý do chọn độ đo** | Đây là yêu cầu về **tốc độ khôi phục dịch vụ**, nên trọng tâm nằm ở thời gian resume service hơn là trạng thái dữ liệu được giữ lại. Với hệ thống nội bộ phục vụ nghiệp vụ nhân sự, thời gian gián đoạn trên 15 phút bắt đầu ảnh hưởng rõ rệt đến thao tác hành chính liên tục như cập nhật hồ sơ, tra cứu hợp đồng và xuất báo cáo. |
| **Phương pháp đo** | Đo thời gian từ thời điểm hệ thống bị crash đến khi phục vụ được request đầu tiên thành công; đo riêng thời gian khởi động lại toàn bộ stack. |
| **Đại lượng thay thế (nếu cần)** | Không cần đại lượng thay thế vì có thể đo trực tiếp bằng **drill test** hoặc mô phỏng sự cố. |

#### SUPL-R03b: Hệ thống phải phục hồi từ bản sao lưu gần nhất và sẵn sàng phục vụ trong tối đa 4 giờ
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Performance → Recovery time |
| **Mô tả yêu cầu** | Sau sự cố **mất dữ liệu nghiêm trọng** hoặc **hỏng cơ sở dữ liệu** buộc phải phục hồi từ bản sao lưu gần nhất, hệ thống phải sẵn sàng phục vụ trở lại trong tối đa **4 giờ**. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Sharp |
| **Verification** | Test |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **RTO (Recovery Time Objective)** (giờ) |
| **Tiêu chuẩn đáp ứng** | - **RTO ≤ 4 giờ** |
| **Lý do chọn độ đo** | Thời gian phục hồi từ backup là một chỉ số **recovery time** điển hình vì phản ánh bao lâu hệ thống mới quay lại trạng thái phục vụ sau thảm họa hoặc mất dữ liệu nghiêm trọng. Mốc 4 giờ bảo đảm hệ thống vẫn có thể được phục hồi trong cùng ngày làm việc. |
| **Phương pháp đo** | Thực hiện bài kiểm thử restore từ bản sao lưu gần nhất và đo thời gian từ lúc bắt đầu phục hồi đến khi hệ thống sẵn sàng phục vụ request thành công. |
| **Đại lượng thay thế (nếu cần)** | Thời gian restore database từ bản backup gần nhất trên môi trường staging dùng làm proxy khi chưa thể kiểm thử toàn stack trên môi trường vận hành. |

### Ghi chú phạm vi trong nhóm Performance

- **Startup / shutdown time:** **N/A** trong fragment này vì hiện không có yêu cầu nghiệm thu riêng cho thời gian khởi động mới hoặc tắt an toàn ngoài các chỉ số **Recovery time** đã đặc tả ở `SUPL-R02` và `SUPL-R03b`.
- **Resource utilization:** **N/A** trong fragment này vì stakeholder chưa đưa ra ràng buộc CPU, RAM, băng thông hoặc dung lượng lưu trữ cụ thể cho môi trường triển khai.

## 6.7. Yêu cầu về Độ tin cậy (Reliability)

> Người thực hiện: Ngô Quang Tùng

### Danh sách yêu cầu

| STT | ID | Yêu cầu (mô tả ngắn) | Yếu tố chất lượng chính | FEAT liên quan |
|-----|----|----------------------|--------------------------|----------------|
| 1 | SUPL-R01 | Hệ thống phải duy trì uptime tối thiểu 99,5% trong khung giờ 7:00–22:00 hằng ngày, không tính bảo trì theo kế hoạch | Reliability → Availability | FEAT 7.1–8.9 |
| 2 | SUPL-R03a | Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi 24 giờ, lưu giữ bản sao lưu tối thiểu 30 ngày và đạt tỷ lệ backup thành công tối thiểu 99% | Reliability → Recoverability | FEAT 7.1–8.9 |
| 3 | SUPL-R04 | Hệ thống phải bảo đảm các thao tác tạo/chỉnh sửa hồ sơ nhân sự, hợp đồng và thay đổi trạng thái không để lại dữ liệu dở dang khi có lỗi | Reliability → Integrity | FEAT 7.1–8.9 |
| 4 | SUPL-R05a | Hệ thống phải cảnh báo tối thiểu 5 phút trước khi phiên tự động hết hạn trên 100% phiên được kiểm thử | Reliability → Recoverability | FEAT 7.1–8.9 |
| 5 | SUPL-R05b | Hệ thống phải khôi phục dữ liệu nháp sau khi người dùng đăng nhập lại trong ít nhất 95% trường hợp kiểm thử | Reliability → Recoverability | FEAT 7.1–8.9 |

> **Ghi chú phân loại:** `SUPL-R02` và phần **RTO** của `SUPL-R03` gốc đã được chuyển sang **Section 6.6** vì primary concern của chúng là **thời gian khôi phục dịch vụ**; `SUPL-R03a` giữ lại phần yêu cầu về **chu kỳ sao lưu, thời gian lưu giữ và tỷ lệ backup thành công**.

### Chi tiết độ đo và tiêu chuẩn đáp ứng

#### SUPL-R01: Hệ thống phải duy trì uptime tối thiểu 99,5% trong khung giờ 7:00–22:00 hằng ngày, không tính bảo trì theo kế hoạch
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Reliability → Availability |
| **Mô tả yêu cầu** | Hệ thống phải sẵn sàng phục vụ trong khung giờ **7:00–22:00** hằng ngày với tỷ lệ **uptime tối thiểu 99,5%** trên tổng thời gian phục vụ trong tháng, không tính thời gian bảo trì theo kế hoạch. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Sharp |
| **Verification** | Analysis |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **Uptime** (%)<br>- **Downtime** (giờ/tháng trong khung giờ phục vụ)<br>- **MTBF (Mean Time Between Failures)** (giờ) |
| **Tiêu chuẩn đáp ứng** | - **Uptime ≥ 99,5%/tháng** trong khung giờ **7:00–22:00**<br>- **Downtime ≤ 2,25 giờ/tháng**, không tính bảo trì theo kế hoạch<br>- **MTBF ≥ 720 giờ** |
| **Lý do chọn độ đo** | HRMS của trường là hệ thống quan trọng trong giờ làm việc nhưng không phải hệ thống 24/7 như các hệ thống giao dịch thời gian thực. Mức 99,5% phản ánh kỳ vọng vận hành nghiêm túc nhưng vẫn phù hợp hơn 99,9% vốn đòi hỏi hạ tầng dự phòng tốn kém hơn đáng kể. |
| **Phương pháp đo** | Tính tỷ lệ uptime theo công thức **(Tổng thời gian hoạt động / Tổng thời gian dự kiến) × 100**; tổng hợp tổng thời gian hệ thống không truy cập được trong tháng để tính downtime. |
| **Đại lượng thay thế (nếu cần)** | Tỷ lệ health check endpoint trả lỗi trên tổng số health check, đo qua công cụ giám sát uptime như **UptimeRobot**. |

#### SUPL-R03a: Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi 24 giờ, lưu giữ bản sao lưu tối thiểu 30 ngày và đạt tỷ lệ backup thành công tối thiểu 99%
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Reliability → Recoverability |
| **Mô tả yêu cầu** | Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi **24 giờ**, lưu giữ bản sao lưu tối thiểu **30 ngày** và đạt tỷ lệ backup thành công tối thiểu **99%**. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Sharp |
| **Verification** | Test |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **RPO (Recovery Point Objective)** (giờ)<br>- **Backup Retention Period** (ngày)<br>- **Backup Success Rate** (%) |
| **Tiêu chuẩn đáp ứng** | - **RPO ≤ 24 giờ**<br>- **Backup Retention Period ≥ 30 ngày**<br>- **Backup Success Rate ≥ 99%** |
| **Lý do chọn độ đo** | Dữ liệu HRMS chủ yếu phát sinh theo ca hành chính nên RPO 24 giờ phù hợp với chu kỳ sao lưu hằng ngày. Thời gian lưu giữ 30 ngày bám theo nhu cầu đối soát nghiệp vụ theo chu kỳ tháng; tỷ lệ backup thành công 99% giúp yêu cầu vẫn thực tế về vận hành nhưng đủ chặt để bảo đảm độ tin cậy của cơ chế sao lưu. |
| **Phương pháp đo** | Theo dõi chu kỳ sao lưu tự động, đối chiếu thời điểm backup gần nhất để tính RPO, đo thời gian lưu giữ bản sao lưu và thống kê tỷ lệ các lần backup chạy thành công trên tổng số lần backup. |
| **Đại lượng thay thế (nếu cần)** | Tỷ lệ bản ghi backup job thành công trên hệ thống scheduler hoặc monitoring backup. |

#### SUPL-R04: Hệ thống phải bảo đảm các thao tác tạo/chỉnh sửa hồ sơ nhân sự, hợp đồng và thay đổi trạng thái không để lại dữ liệu dở dang khi có lỗi
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Reliability → Integrity |
| **Mô tả yêu cầu** | Các thao tác **tạo mới hoặc chỉnh sửa hồ sơ nhân sự**, **tạo mới, chỉnh sửa hoặc chấm dứt hợp đồng**, và **các thao tác thay đổi trạng thái nghiệp vụ** phải bảo đảm nguyên tắc **toàn bộ hoặc không thực hiện phần nào**; nếu một bước thất bại, hệ thống không được ghi nhận thay đổi dở dang và phải khôi phục dữ liệu về trạng thái trước thao tác. |
| **Importance** | Mandatory |
| **Satisfaction Shape** | Sharp |
| **Verification** | Test |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **Data Inconsistency Count** (số trường hợp)<br>- **Integrity Protection Coverage** (%) |
| **Tiêu chuẩn đáp ứng** | - **Data Inconsistency Count = 0**<br>- **Integrity Protection Coverage = 100%** cho các nhóm nghiệp vụ: **tạo/chỉnh sửa hồ sơ nhân sự**, **tạo/chỉnh sửa/chấm dứt hợp đồng**, **thay đổi trạng thái nghiệp vụ** |
| **Lý do chọn độ đo** | Với dữ liệu nhân sự và hợp đồng, chỉ một bản ghi cập nhật dở dang cũng có thể dẫn đến sai lệch hồ sơ pháp lý hoặc sai thông tin quản lý. Vì vậy chỉ tiêu chấp nhận phù hợp là 0 trường hợp bất nhất quán và 100% bao phủ kiểm thử cho các nghiệp vụ trọng yếu trong phạm vi FEAT 7–8. |
| **Phương pháp đo** | Thực hiện **failure-injection test** để kiểm tra dữ liệu bất nhất quán sau lỗi; đo tỷ lệ thao tác cập nhật quan trọng được kiểm thử lỗi giữa chừng nhưng không phát sinh cập nhật dở dang. |
| **Đại lượng thay thế (nếu cần)** | Số vi phạm khóa ngoại và orphaned records phát hiện qua script kiểm tra toàn vẹn dữ liệu. |

#### SUPL-R05a: Hệ thống phải cảnh báo tối thiểu 5 phút trước khi phiên tự động hết hạn trên 100% phiên được kiểm thử
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Reliability → Recoverability |
| **Mô tả yêu cầu** | Đối với form có dữ liệu đã nhập nhưng chưa lưu, hệ thống phải hiển thị cảnh báo tối thiểu **5 phút** trước khi phiên tự động hết hạn trên **100%** phiên được kiểm thử. |
| **Importance** | Desirable |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **Session Expiry Warning Coverage** (%)<br>- **Warning Lead Time** (phút) |
| **Tiêu chuẩn đáp ứng** | - **Session Expiry Warning Coverage = 100%** đối với các phiên sắp hết hạn<br>- **Warning Lead Time ≥ 5 phút** trước khi tự động đăng xuất |
| **Lý do chọn độ đo** | Cảnh báo trước khi hết phiên là biện pháp giảm nguy cơ mất công việc đang làm và giúp người dùng có thời gian quyết định lưu hoặc tiếp tục thao tác. Việc tách riêng requirement này giúp đánh giá độc lập hành vi cảnh báo, không lẫn với khả năng khôi phục dữ liệu nháp sau đăng nhập lại. |
| **Phương pháp đo** | Mô phỏng hết phiên trên các form nhập liệu dài để đo tỷ lệ xuất hiện cảnh báo và thời gian cảnh báo trước khi hệ thống tự động đăng xuất. |
| **Đại lượng thay thế (nếu cần)** | Kiểm thử nhị phân Có/Không đối với popup cảnh báo trước khi hết phiên. |

#### SUPL-R05b: Hệ thống phải khôi phục dữ liệu nháp sau khi người dùng đăng nhập lại trong ít nhất 95% trường hợp kiểm thử
| Thuộc tính | Nội dung |
|---|---|
| **Yếu tố chất lượng chính** | Reliability → Recoverability |
| **Mô tả yêu cầu** | Đối với form có dữ liệu đã nhập nhưng chưa lưu, hệ thống phải khôi phục dữ liệu nháp gần nhất sau khi người dùng đăng nhập lại trong ít nhất **95%** trường hợp kiểm thử. |
| **Importance** | Desirable |
| **Satisfaction Shape** | Medium |
| **Verification** | Test |
| **Source** | FEAT 7.1–8.9 |
| **Độ đo yêu cầu** | - **Draft Recovery Rate** (%) |
| **Tiêu chuẩn đáp ứng** | - **Draft Recovery Rate ≥ 95%** đối với form có dữ liệu nhập dở khi người dùng đăng nhập lại |
| **Lý do chọn độ đo** | Với biểu mẫu nhân sự nhiều trường, việc mất toàn bộ dữ liệu đã nhập là rất tốn thời gian và dễ gây bức xúc cho người dùng, nên hệ thống phải khôi phục bản nháp ở mức cao. Ngưỡng 95% thực tế hơn 100% tuyệt đối vì vẫn có thể có các tình huống ngoài kiểm soát như người dùng đóng tab cưỡng bức hoặc trình duyệt xóa dữ liệu cục bộ. |
| **Phương pháp đo** | Thực hiện user testing hoặc mô phỏng hết phiên trên các form nhập liệu dài để đo tỷ lệ khôi phục dữ liệu nháp sau khi đăng nhập lại. |
| **Đại lượng thay thế (nếu cần)** | Kiểm tra sự tồn tại của bản nháp lưu tạm trên trình duyệt hoặc máy chủ sau khi người dùng đăng nhập lại. |
