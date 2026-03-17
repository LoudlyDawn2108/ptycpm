# THIẾT LẬP ĐỘ ĐO YÊU CẦU VÀ TIÊU CHUẨN ĐÁP ỨNG

## Hệ thống HRMS — Trường Đại học Thủy Lợi

> Tài liệu này trình bày chi tiết việc **thiết lập độ đo** (Metrics), **xác định yếu tố chất lượng** (Quality Factors) và **tiêu chuẩn đáp ứng** (Acceptance Criteria) cho từng yêu cầu bổ sung/phi chức năng đã được liệt kê trong [supplementary-requirements.md](./supplementary-requirements.md). Khi NFR khó đo trực tiếp, sử dụng **đại lượng thay thế** (Proxy).
>
> **Ghi chú cập nhật phạm vi:** Các độ đo có phạm vi áp dụng kiểu **toàn bộ FEAT/UC**, **toàn bộ hệ thống**, hoặc **mọi hành động truy cập, thêm mới/cập nhật dữ liệu và thay đổi trạng thái** mặc nhiên bao phủ cả các use case được bổ sung sau mở rộng phạm vi, bao gồm **UC 4.43 – UC 4.48** tương ứng **FEAT 5.2 – 5.4, FEAT 6.2 – 6.3, FEAT 7.9**. Với các độ đo đang tham chiếu FEAT/UC cụ thể, phạm vi áp dụng được cập nhật tường minh trong tài liệu này để tránh thiếu bao phủ truy vết.

---

## 1. SUPL-P01 — Thời gian phản hồi giao diện

**Yêu cầu gốc:** Các thao tác nghiệp vụ cơ bản (xem danh sách, xem chi tiết, thêm/sửa, thay đổi trạng thái khi được hỗ trợ) phải đáp ứng các ngưỡng P95 Response Time và Time to Interactive (TTI) theo tải đồng thời được quy định tại phần tiêu chuẩn đáp ứng.

### Yếu tố chất lượng
- **Nhóm:** Performance (Hiệu năng)
- **Yếu tố:** Speed — Tốc độ phản hồi (Response Time)
- **Mô hình tham chiếu:** ISO 25010 → Performance Efficiency → Time Behaviour

### Độ đo yêu cầu (Metrics)
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| P95 Response Time cho thao tác nghiệp vụ cơ bản | Giây (s) | Đo bằng công cụ load test (JMeter, k6) — lấy phân vị 95 của thời gian từ lúc gửi request đến nhận response |
| Time to Interactive (TTI) | Giây (s) | Đo trên trình duyệt — thời gian từ click đến giao diện sẵn sàng tương tác |
| Contract List Load Time | Giây (s) | Thời gian từ mở màn hình danh sách hợp đồng đến khi danh sách hiển thị đầy đủ và sẵn sàng tương tác |
| Contract Detail Load Time | Giây (s) | Thời gian từ click một hợp đồng đến khi màn hình chi tiết hợp đồng hiển thị ổn định |
| Contract Termination Response Time | Giây (s) | Thời gian từ xác nhận chấm dứt hợp đồng trước hạn đến khi hệ thống ghi nhận thành công và cập nhật trạng thái |

### Tiêu chuẩn đáp ứng

| Số người dùng đồng thời | P95 Response Time tối đa | TTI tối đa |
|--------------------------|--------------------------|------------|
| 0 – 10 | ≤ 1 giây | ≤ 1.5 giây |
| 11 – 50 | ≤ 2 giây | ≤ 3 giây |
| 51 – 100 | ≤ 5 giây | ≤ 6 giây |
| > 100 | ≤ 10 giây | ≤ 12 giây |

- Các ngưỡng trên được áp dụng cho toàn bộ thao tác xem/thêm/sửa cơ bản trên hệ thống, bao gồm cả **FEAT 5.2 – 5.4 / UC 4.43 – UC 4.45**.
- **Contract List Load Time**, **Contract Detail Load Time** và **Contract Termination Response Time** kế thừa trực tiếp ngưỡng **P95 Response Time** và **TTI** theo tải đồng thời tương ứng trong bảng trên.

### Đại lượng thay thế (Proxy)
- Không cần proxy — có thể đo trực tiếp bằng load test tool.

---

## 2. SUPL-P02 — Số lượng người dùng đồng thời

**Yêu cầu gốc:** Hệ thống hỗ trợ tối thiểu 100 người dùng đồng thời.

### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Capacity — Khả năng chịu tải
- **Mô hình tham chiếu:** ISO 25010 → Performance Efficiency → Capacity

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Max Concurrent Users | Số người | Stress test — tăng dần số kết nối đồng thời cho đến khi response time vượt ngưỡng |
| Throughput | Transactions/giây (tx/s) | Load test — đếm số giao dịch hoàn thành trong 1 giây |
| Degradation Rate | % | So sánh response time tại tải cao vs tải thấp |

### Tiêu chuẩn đáp ứng
- Max Concurrent Users ≥ **100 người**
- Throughput ≥ **50 tx/s** tại 100 concurrent users
- Degradation Rate ≤ **50%** (response time tại 100 users so với 1 user)

### Đại lượng thay thế
- **Proxy:** Số kết nối TCP/WebSocket mà server duy trì ổn định (đo trên server monitoring)

---

## 3. SUPL-P03 — Thời gian tạo báo cáo thống kê

**Yêu cầu gốc:** Dashboard và báo cáo tổng hợp (FEAT 10.1) phải hoàn thành tải và hiển thị trong các ngưỡng thời gian quy định tại phần tiêu chuẩn đáp ứng.

### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ xử lý và hiển thị báo cáo

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Dashboard Load Time | Giây | Thời gian từ navigate đến dashboard sẵn sàng hiển thị đầy đủ biểu đồ |
| Complex Report Generation Time | Giây | Thời gian từ click "Tạo báo cáo" đến hiển thị/download hoàn tất |
| Single Chart Render Time | Giây | Thời gian render 1 biểu đồ thống kê |

### Tiêu chuẩn đáp ứng
- Dashboard Load Time ≤ **5 giây**
- Complex Report Generation ≤ **15 giây**
- Single Chart Render ≤ **3 giây**

### Đại lượng thay thế
- **Proxy:** Thời gian truy vấn SQL của các query thống kê (đo qua slow query log) — mục tiêu ≤ 2 giây/query

---

## 4. SUPL-P04 — Hiệu năng tìm kiếm và lọc

**Yêu cầu gốc:** Tìm kiếm và lọc trên các danh sách chính của hệ thống phải trả kết quả trong các ngưỡng thời gian quy định theo quy mô dữ liệu tại phần tiêu chuẩn đáp ứng.

### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ truy vấn dữ liệu

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Search Response Time | Giây | Thời gian từ submit tìm kiếm đến hiển thị kết quả — áp dụng cho danh sách nhân sự, hợp đồng và đánh giá nếu chức năng có hỗ trợ tìm kiếm/lọc |
| Filter Apply Time | Giây | Thời gian từ áp dụng bộ lọc đến danh sách cập nhật — áp dụng cho danh sách nhân sự, hợp đồng và đánh giá nếu chức năng có hỗ trợ tìm kiếm/lọc |

### Tiêu chuẩn đáp ứng

| Quy mô dữ liệu | Search Response Time | Filter Apply Time |
|------------------|----------------------|--------------------|
| ≤ 10.000 bản ghi | ≤ 2 giây | ≤ 2 giây |
| ≤ 50.000 bản ghi | ≤ 5 giây | ≤ 5 giây |

- **Ghi chú phạm vi:** Các độ đo Search Response Time và Filter Apply Time áp dụng cho danh sách nhân sự, hợp đồng và đánh giá nếu chức năng có hỗ trợ tìm kiếm/lọc. Trong đó **FEAT 6.3 / UC 4.47** thuộc phạm vi bắt buộc áp dụng; các màn hình hợp đồng thuộc **FEAT 5.2 – 5.4 / UC 4.43 – UC 4.45** kế thừa độ đo này nếu bổ sung bộ lọc hoặc ô tìm kiếm.

### Đại lượng thay thế
- **Proxy:** Execution time của câu truy vấn SQL LIKE/FULLTEXT (qua EXPLAIN ANALYZE) — mục tiêu ≤ 500ms cho ≤ 10K records

---

## 5. SUPL-P05 — Hiệu năng upload/download file

**Yêu cầu gốc:** Việc tải lên và tải xuống tệp đính kèm dung lượng đến 5 MB phải hoàn thành trong các ngưỡng thời gian quy định tại phần tiêu chuẩn đáp ứng trên mạng LAN.

### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ truyền file (File I/O)

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Upload Time | Giây | Thời gian từ chọn file đến server xác nhận lưu thành công |
| Download Time | Giây | Thời gian từ click download đến file sẵn sàng mở |

### Tiêu chuẩn đáp ứng
- Upload ≤ **5 giây** cho file ≤ 5MB (trên mạng LAN)
- Download ≤ **3 giây** cho file ≤ 5MB (trên mạng LAN)

### Đại lượng thay thế
- **Proxy:** Tốc độ ghi file vào disk (MB/s) — đo qua server I/O monitoring

---

## 6. SUPL-P06 — Hiệu năng xuất Excel

**Yêu cầu gốc:** Chức năng xuất dữ liệu ra Excel phải hoàn thành trong các ngưỡng thời gian quy định theo số bản ghi tại phần tiêu chuẩn đáp ứng.

### Yếu tố chất lượng
- **Nhóm:** Performance
- **Yếu tố:** Speed — Tốc độ xuất dữ liệu

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Export Time | Giây | Thời gian từ click "Xuất Excel" đến file download hoàn tất |

### Tiêu chuẩn đáp ứng
| Số bản ghi | Export Time tối đa |
|------------|---------------------|
| ≤ 1.000 | ≤ 10 giây |
| ≤ 10.000 | ≤ 30 giây |

### Đại lượng thay thế
- **Proxy:** Thời gian server sinh file Excel (không tính download) — đo qua API response time

---

## 7. SUPL-R01 — Tính sẵn sàng cao (Availability)

**Yêu cầu gốc:** Hệ thống phải đạt uptime tối thiểu 99,5% trong khung giờ 7:00–22:00 hằng ngày và tổng downtime ngoài bảo trì kế hoạch không được vượt quá 2,25 giờ/tháng.

### Yếu tố chất lượng
- **Nhóm:** Reliability (Độ tin cậy)
- **Yếu tố:** Availability — Tính sẵn sàng
- **Mô hình McCall:** Product Operation → Reliability

### Độ đo yêu cầu
| Độ đo | Đơn vị | Công thức / Phương pháp đo |
|-------|--------|----------------------------|
| Uptime | % | (Tổng thời gian hoạt động / Tổng thời gian dự kiến) × 100 |
| MTBF (Mean Time Between Failures) | Giờ | Tổng thời gian hoạt động / Số lần failure |
| Downtime | Giờ/tháng | Tổng thời gian hệ thống không truy cập được (không tính bảo trì kế hoạch) |

### Tiêu chuẩn đáp ứng
- Uptime ≥ **99.5%/tháng** (trong khung giờ 7:00–22:00)
- MTBF ≥ **720 giờ** (tương đương 30 ngày)
- Downtime ≤ **2.25 giờ/tháng** (không tính bảo trì kế hoạch)

### Đại lượng thay thế
- **Proxy:** Số lần health check endpoint trả về lỗi / Tổng số health check (đo qua uptime monitoring tool như UptimeRobot)

---

## 8. SUPL-R02 — Khả năng phục hồi sau sự cố

**Yêu cầu gốc:** Sau sự cố crash hoặc restart, hệ thống phải phục hồi khả năng phục vụ request thành công trong tối đa 15 phút.

### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Recoverability — Khả năng phục hồi

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| MTTR (Mean Time To Repair) | Phút | Thời gian từ lúc crash đến khi hệ thống phục vụ được request đầu tiên thành công |
| Restart Time | Phút | Thời gian restart toàn bộ stack (DB + Backend + Frontend) |

### Tiêu chuẩn đáp ứng
- MTTR ≤ **15 phút**
- Restart Time ≤ **10 phút**

### Đại lượng thay thế
- Không cần — có thể đo trực tiếp qua drill test (mô phỏng sự cố)

---

## 9. SUPL-R03 — Sao lưu dữ liệu tự động

**Yêu cầu gốc:** Hệ thống phải sao lưu dữ liệu tự động ít nhất mỗi 24 giờ, lưu giữ bản sao lưu tối thiểu 30 ngày và phục hồi được từ bản sao lưu trong tối đa 4 giờ.

### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Recoverability — Sao lưu và phục hồi dữ liệu

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| RPO (Recovery Point Objective) | Giờ | Khoảng thời gian dữ liệu có thể mất tối đa khi phục hồi từ backup |
| RTO (Recovery Time Objective) | Giờ | Thời gian tối đa để phục hồi hệ thống từ backup |
| Backup Retention Period | Ngày | Số ngày lưu giữ bản sao lưu |
| Backup Success Rate | % | Số lần backup thành công / Tổng số lần backup chạy |

### Tiêu chuẩn đáp ứng
- RPO ≤ **24 giờ**
- RTO ≤ **4 giờ**
- Backup Retention ≥ **30 ngày**
- Backup Success Rate ≥ **99%**

### Đại lượng thay thế
- **Proxy cho RTO:** Thời gian restore database từ backup gần nhất trên môi trường staging

---

## 10. SUPL-R04 — Toàn vẹn dữ liệu

**Yêu cầu gốc:** Các thao tác cập nhật dữ liệu quan trọng phải bảo toàn tính nhất quán; nếu một bước thất bại, hệ thống không được ghi nhận thay đổi dở dang.

### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Integrity — Tính toàn vẹn dữ liệu
- **Mô hình McCall:** Product Operation → Integrity

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Data Inconsistency Count | Số trường hợp | Kiểm tra dữ liệu bất nhất quán sau thao tác lỗi (failure-injection test) |
| Integrity Protection Coverage | % | Tỷ lệ thao tác cập nhật quan trọng được kiểm thử lỗi giữa chừng mà không phát sinh cập nhật dở dang |

### Tiêu chuẩn đáp ứng
- Data Inconsistency Count = **0**
- Integrity Protection Coverage = **100%** cho hợp đồng, bổ nhiệm, đánh giá, chuyển trạng thái
- Không được ghi nhận thay đổi một phần khi có lỗi giữa chừng

### Đại lượng thay thế
- **Proxy:** Số Foreign Key violations và orphaned records phát hiện qua integrity check script

---

## 11. SUPL-R05 — Không mất dữ liệu khi phiên hết hạn

**Yêu cầu gốc:** Trước khi phiên tự động hết hạn, hệ thống phải cảnh báo tối thiểu 5 phút; nếu phiên vẫn hết hạn, tỷ lệ mất dữ liệu biểu mẫu chưa lưu không được vượt quá 5%.

### Yếu tố chất lượng
- **Nhóm:** Reliability
- **Yếu tố:** Fault Tolerance — Chịu lỗi

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Data Loss Rate | % | Tỷ lệ trường hợp mất dữ liệu form khi phiên hết hạn (user testing) |
| Warning Lead Time | Phút | Thời gian cảnh báo trước khi phiên hết hạn |

### Tiêu chuẩn đáp ứng
- Data Loss Rate ≤ **5%**
- Warning Lead Time ≥ **5 phút** trước khi tự động đăng xuất

### Đại lượng thay thế
- **Proxy:** Có/Không hiển thị popup cảnh báo (binary kiểm thử) — thay vì đo tỷ lệ mất dữ liệu thực tế

---

## 12. SUPL-SE01 — Xác thực người dùng (Authentication)

**Yêu cầu gốc:** Mọi truy cập vào hệ thống phải được xác thực bằng tên đăng nhập và mật khẩu; mật khẩu phải có ít nhất 8 ký tự và bao gồm chữ hoa, chữ thường, chữ số.

### Yếu tố chất lượng
- **Nhóm:** Security (Bảo mật)
- **Yếu tố:** Authentication — Xác thực danh tính
- **Mô hình McCall:** Product Operation → Integrity

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Password Strength Level | Số quy tắc | Đếm số quy tắc mật khẩu được enforce (độ dài, chữ hoa, chữ thường, số) |
| Authentication Levels | Số level | Số lớp xác thực trước khi truy cập hệ thống |
| Session Security | Có/Không | Kiểm tra cơ chế phiên có chặn truy cập từ script phía client và có thời điểm hết hiệu lực |

### Tiêu chuẩn đáp ứng
- Mật khẩu ≥ **8 ký tự**, chứa chữ hoa + chữ thường + số (3 quy tắc)
- **1 level** xác thực (tên đăng nhập/mật khẩu)
- Phiên xác thực phải chặn truy cập từ script phía client và tự hết hiệu lực sau tối đa **30 phút** không hoạt động

### Đại lượng thay thế
- **Proxy cho Password Strength:** Số mật khẩu yếu trong hệ thống (kiểm tra bằng password audit script)

---

## 13. SUPL-SE02 — Phân quyền truy cập (Authorization)

**Yêu cầu gốc:** Hệ thống phải phân quyền theo 4 vai trò (Admin, TCCB, TCKT, Nhân sự); mỗi vai trò chỉ được truy cập các chức năng được cấp quyền và mọi request API phải được kiểm tra quyền trước khi xử lý.

### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Authorization — Kiểm soát truy cập

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Unauthorized Access Count | Số trường hợp | Penetration test — thử truy cập chức năng ngoài quyền |
| API Protection Coverage | % | Tỷ lệ API endpoint có middleware kiểm tra quyền |
| Role Count | Số vai trò | Đếm số vai trò được định nghĩa trong hệ thống |

### Tiêu chuẩn đáp ứng
- Unauthorized Access = **0 trường hợp**
- API Protection Coverage = **100%**
- Role Count = **4** (Admin, TCCB, TCKT, Nhân sự) theo mô hình **RBAC**

### Đại lượng thay thế
- **Proxy:** Số API route không có middleware auth (đo qua route audit script)

---

## 14. SUPL-SE03 — Chống tấn công brute-force

**Yêu cầu gốc:** Hệ thống phải khóa tạm thời tài khoản sau 5 lần đăng nhập sai liên tiếp trong ít nhất 15 phút và phải ghi log cảnh báo khi phát hiện dấu hiệu brute-force.

### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Integrity — Chống tấn công tự động

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Lock Threshold | Số lần | Số lần đăng nhập sai liên tiếp trước khi khóa |
| Lock Duration | Phút | Thời gian khóa tài khoản tạm thời |
| Alert Logging | Có/Không | Kiểm tra log cảnh báo khi phát hiện brute-force |

### Tiêu chuẩn đáp ứng
- Lock Threshold = **5 lần** sai liên tiếp
- Lock Duration ≥ **15 phút**
- Alert Logging = **Có** — ghi log cảnh báo với IP, thời gian, tài khoản bị tấn công

### Đại lượng thay thế
- Không cần — đo trực tiếp qua test đăng nhập sai liên tiếp

---

## 15. SUPL-SE04 — Mã hóa truyền tải (HTTPS)

**Yêu cầu gốc:** Toàn bộ giao tiếp giữa client và server phải sử dụng HTTPS với TLS 1.2 trở lên.

### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Confidentiality — Bảo mật truyền tải

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| TLS Version | Phiên bản | Kiểm tra certificate và protocol qua SSL Labs hoặc curl |
| HTTPS Coverage | % | Tỷ lệ kết nối sử dụng HTTPS / Tổng kết nối |
| HTTP Redirect | Có/Không | Kiểm tra HTTP request có tự động redirect sang HTTPS |

### Tiêu chuẩn đáp ứng
- TLS ≥ **1.2**
- HTTPS Coverage = **100%**
- HTTP Redirect = **Có** (auto-redirect 301)

### Đại lượng thay thế
- **Proxy:** SSL Labs Score (A/B/C/D/F) — mục tiêu đạt **A** hoặc **A+**

---

## 16. SUPL-SE05 — Bảo vệ dữ liệu nhạy cảm

**Yêu cầu gốc:** Dữ liệu nhạy cảm như CCCD, BHXH và thông tin ngân hàng chỉ được hiển thị cho vai trò được phép và mọi truy cập phải được ghi audit log.

### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Confidentiality — Bảo mật dữ liệu cá nhân

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Exposed Sensitive Fields | Số trường | Kiểm tra API response cho vai trò không được phép — đếm trường nhạy cảm bị lộ |
| Audit Log Coverage for Sensitive Data | % | Tỷ lệ truy cập dữ liệu nhạy cảm được ghi audit log |

### Tiêu chuẩn đáp ứng
- Exposed Sensitive Fields = **0** cho vai trò không được phép
- Audit Log Coverage = **100%** cho CCCD, BHXH, thông tin ngân hàng

### Đại lượng thay thế
- **Proxy:** Số API endpoint trả về dữ liệu nhạy cảm mà không kiểm tra vai trò (code review audit)

---

## 17. SUPL-SE06 — Phòng chống CSRF và XSS

**Yêu cầu gốc:** Hệ thống phải ngăn chặn yêu cầu giả mạo làm thay đổi dữ liệu và không được hiển thị nội dung thực thi do người dùng chèn vào giao diện.

### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Integrity — Chống tấn công web

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| CSRF Vulnerabilities | Số lỗ hổng | Penetration test (OWASP ZAP hoặc tương đương) |
| XSS Vulnerabilities | Số lỗ hổng | Penetration test + code review cơ chế xử lý dữ liệu đầu vào/đầu ra |
| State-changing Request Protection Coverage | % | Tỷ lệ form POST/PUT/PATCH hoặc request thay đổi trạng thái tương đương được bảo vệ chống giả mạo yêu cầu |

### Tiêu chuẩn đáp ứng
- CSRF Vulnerabilities = **0**
- XSS Vulnerabilities = **0**
- State-changing Request Protection Coverage = **100%**

### Đại lượng thay thế
- **Proxy:** Số điểm nhập liệu không được xử lý an toàn trước khi hiển thị lại trong giao diện (đo qua static code analysis)

---

## 18. SUPL-SE07 — Chống SQL Injection

**Yêu cầu gốc:** Mọi truy vấn sử dụng dữ liệu đầu vào từ người dùng phải ngăn chặn việc chèn lệnh SQL.

### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Integrity — Chống tấn công database

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| SQLi Vulnerabilities | Số lỗ hổng | sqlmap scan hoặc penetration test |
| Query Protection Coverage | % | Tỷ lệ truy vấn có sử dụng dữ liệu đầu vào được bảo vệ khỏi chèn lệnh SQL (code review) |

### Tiêu chuẩn đáp ứng
- SQLi Vulnerabilities = **0**
- Query Protection Coverage = **100%**

### Đại lượng thay thế
- **Proxy:** Số truy vấn ghép chuỗi trực tiếp dữ liệu đầu vào trong codebase — mục tiêu **0**

---

## 19. SUPL-U01 — Giao diện thân thiện và nhất quán

**Yêu cầu gốc:** Giao diện người dùng phải sử dụng tiếng Việt và tuân thủ thống nhất design system về bố cục, màu sắc và font chữ trên toàn bộ hệ thống.

### Yếu tố chất lượng
- **Nhóm:** Usability (Tính dễ sử dụng)
- **Yếu tố:** Consistency — Tính nhất quán giao diện

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| UI Violation Count | Số trang | Rà soát giao diện — đếm trang vi phạm design system (font, màu, layout) |
| Vietnamese Content Rate | % | Tỷ lệ nội dung giao diện sử dụng Tiếng Việt |

### Tiêu chuẩn đáp ứng
- UI Violation Count = **0 trang**
- Vietnamese Content Rate = **100%** (trừ thuật ngữ kỹ thuật quốc tế)

### Đại lượng thay thế
- **Proxy:** Số component sử dụng hardcoded style (không theo design token) — đo qua code review

---

## 20. SUPL-U02 — Thời gian đào tạo sử dụng ngắn

**Yêu cầu gốc:** Người dùng mới thuộc phòng TCCB và TCKT phải hoàn thành được các chức năng cơ bản sau tối đa 2 giờ đào tạo.

### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Learnability — Dễ học, dễ tiếp cận

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Average Training Time | Giờ | User test — đo thời gian đào tạo trung bình cho người dùng mới |
| Task Completion Rate After Training | % | Tỷ lệ người dùng hoàn thành thao tác cơ bản (thêm/sửa nhân sự) sau đào tạo |

### Tiêu chuẩn đáp ứng
- Average Training Time ≤ **2 giờ** cho các chức năng cơ bản
- Task Completion Rate ≥ **95%** cho phòng TCCB sau đào tạo

### Đại lượng thay thế
- **Proxy:** Khối lượng tài liệu đào tạo (số trang) — mục tiêu ≤ 30 trang cho mỗi vai trò

---

## 21. SUPL-U03 — Thông báo lỗi rõ ràng

**Yêu cầu gốc:** Mọi lỗi nhập liệu, lỗi nghiệp vụ và lỗi hệ thống phải hiển thị thông báo bằng tiếng Việt, nêu nguyên nhân và có ít nhất 1 gợi ý khắc phục.

### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Error Handling — Xử lý lỗi thân thiện

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Vietnamese Error Message Coverage | % | Tỷ lệ loại lỗi có thông báo Tiếng Việt rõ ràng / Tổng loại lỗi |
| Fix Suggestion Rate | % | Tỷ lệ thông báo lỗi có kèm gợi ý khắc phục |

### Tiêu chuẩn đáp ứng
- Vietnamese Error Message Coverage = **100%** (validation, nghiệp vụ, hệ thống)
- Fix Suggestion Rate = **100%** (mỗi thông báo lỗi ≥ 1 gợi ý khắc phục)

### Đại lượng thay thế
- **Proxy:** Số error code/message hiển thị bằng tiếng Anh hoặc mã kỹ thuật — mục tiêu **0**

---

## 22. SUPL-U04 — Tìm kiếm và lọc đa tiêu chí

**Yêu cầu gốc:** Các danh sách dữ liệu phải hỗ trợ tìm kiếm theo từ khóa và kết hợp ít nhất 3 tiêu chí lọc đồng thời; người dùng phải tìm và mở chi tiết 1 nhân sự trong tối đa 3 bước.

### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Efficiency — Hiệu quả thao tác

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Steps to Search & View | Số bước | Đếm số click/thao tác để tìm và xem chi tiết 1 nhân sự |
| Max Concurrent Filter Criteria | Số tiêu chí | Đếm số tiêu chí lọc có thể kết hợp đồng thời |

### Tiêu chuẩn đáp ứng
- Steps to Search & View ≤ **3 bước** (nhập từ khóa → tìm → click xem)
- Max Concurrent Filter ≥ **3 tiêu chí** đồng thời

### Đại lượng thay thế
- Không cần — đo trực tiếp qua usability test

---

## 23. SUPL-U05 — Giao diện responsive

**Yêu cầu gốc:** Giao diện phải hiển thị đúng trên desktop từ 1366×768 trở lên và phải sử dụng được trên tablet 1024×768 theo các tỷ lệ trang quy định tại phần tiêu chuẩn đáp ứng.

### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Accessibility — Khả năng truy cập đa thiết bị

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Desktop Compatibility Rate | % | Tỷ lệ trang hiển thị đúng trên desktop ≥ 1366×768 |
| Tablet Compatibility Rate | % | Tỷ lệ trang sử dụng được trên tablet 1024×768 |

### Tiêu chuẩn đáp ứng
- Desktop Compatibility = **100%** (≥ 1366×768)
- Tablet Compatibility ≥ **80%** (1024×768)

### Đại lượng thay thế
- **Proxy:** Số CSS breakpoint được định nghĩa — mục tiêu ≥ 2 (desktop + tablet)

---

## 24. SUPL-U07 — Xác nhận trước thao tác quan trọng

**Yêu cầu gốc:** Hệ thống phải hiển thị hộp thoại xác nhận trước các thao tác khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng lao động trước hạn, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương.

### Yếu tố chất lượng
- **Nhóm:** Usability
- **Yếu tố:** Error Prevention — Ngăn ngừa lỗi do thao tác nhầm

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Confirmation Dialog Coverage | % | Tỷ lệ thao tác quan trọng có hộp thoại xác nhận |

### Tiêu chuẩn đáp ứng
- Confirmation Dialog Coverage = **100%** cho: khóa tài khoản, đánh dấu thôi việc, chấm dứt hợp đồng lao động trước hạn, thay đổi trạng thái đơn vị và các thao tác thay đổi trạng thái có rủi ro tương đương

### Đại lượng thay thế
- Không cần — kiểm thử trực tiếp từng thao tác

---

## 25. SUPL-S01 — Kiến trúc module hóa

**Yêu cầu gốc:** Hệ thống phải được tách thành các module có giao diện trao đổi rõ ràng để việc thay đổi một module chỉ ảnh hưởng tối đa một module khác.

### Yếu tố chất lượng
- **Nhóm:** Supportability (Khả năng bảo trì)
- **Yếu tố:** Maintainability → Modularity — Tính module
- **Mô hình McCall:** Product Revision → Maintainability

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Module Coupling | Số module bị ảnh hưởng | Khi thay đổi 1 module, đếm số module khác phải thay đổi theo |
| API Interface Separation | Có/Không | Kiểm tra frontend và backend giao tiếp hoàn toàn qua RESTful API |

### Tiêu chuẩn đáp ứng
- Thay đổi 1 module → ảnh hưởng ≤ **1 module** khác
- Frontend ↔ Backend giao tiếp **100% qua API** (không shared code)

### Đại lượng thay thế
- **Proxy:** Số import/dependency cross-module trong codebase — đo qua dependency analysis tool

---

## 26. SUPL-S03 — Khả năng mở rộng danh mục cấu hình

**Yêu cầu gốc:** Hệ thống phải cho phép mở rộng các danh mục dữ liệu chủ qua giao diện quản trị mà không cần sửa mã nguồn.

### Yếu tố chất lượng
- **Nhóm:** Supportability
- **Yếu tố:** Flexibility — Tính linh hoạt

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Extendable Categories via UI | Số loại | Đếm số loại danh mục có thể thêm mới qua giao diện quản trị |
| Code Changes for New Category | Số dòng | Đếm số dòng code phải sửa khi thêm 1 danh mục mới |

### Tiêu chuẩn đáp ứng
- Extendable Categories ≥ **3** (hệ số lương, loại phụ cấp, loại hợp đồng) đối với nhóm danh mục master data
- **Ghi chú phạm vi:** Chỉ số Extendable Categories áp dụng cho các danh mục dữ liệu chủ. Riêng cấu hình **ẩn/hiện mục khen thưởng/kỷ luật** (**FEAT 7.9 / UC 4.48**) được xem là một chiều cấu hình hiển thị độc lập và phải được quản trị qua UI mà không yêu cầu sửa mã nguồn.
- Code Changes = **0 dòng** khi thêm danh mục mới

### Đại lượng thay thế
- Không cần — kiểm thử trực tiếp bằng cách thêm danh mục mới qua UI

---

## 27. SUPL-F01 — Ghi nhật ký hệ thống tự động

**Yêu cầu gốc:** Hệ thống phải tự động ghi nhật ký cho mọi hành động truy cập, thêm mới/cập nhật dữ liệu, thay đổi trạng thái và thay đổi cấu hình, đồng thời mỗi bản ghi log phải có đầy đủ các trường thông tin bắt buộc.

### Yếu tố chất lượng
- **Nhóm:** Functionality (bổ sung) + Correctness
- **Yếu tố:** Auditability — Khả năng kiểm toán
- **Mô hình McCall:** Product Operation → Correctness

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Action Log Coverage | % | (Số hành động được ghi log / Tổng hành động thực hiện) × 100 |
| Log Field Completeness | Số trường / 9 | Kiểm tra mỗi log entry có đủ 9 trường: thời gian, tài khoản, họ tên, vai trò, loại hành động, đối tượng, mã đối tượng, mô tả, IP |

### Tiêu chuẩn đáp ứng
- Action Log Coverage = **100%** cho mọi hành động truy cập, thêm mới/cập nhật dữ liệu, thay đổi trạng thái và thay đổi cấu hình
- Log Field Completeness = **9/9 trường** cho mọi entry

### Đại lượng thay thế
- **Proxy:** Số API controller không gọi audit service (code review) — mục tiêu **0**

---

## 28. SUPL-F08 — Băm mật khẩu

**Yêu cầu gốc:** Tất cả mật khẩu người dùng phải được lưu ở dạng băm một chiều thích ứng và không được tồn tại mật khẩu dạng rõ trong dữ liệu lưu trữ.

### Yếu tố chất lượng
- **Nhóm:** Security
- **Yếu tố:** Confidentiality — Bảo mật dữ liệu lưu trữ

### Độ đo yêu cầu
| Độ đo | Đơn vị | Phương pháp đo |
|-------|--------|----------------|
| Hash Method Compliance | Có/Không | Kiểm tra cấu hình và mã nguồn để xác nhận mật khẩu được lưu bằng cơ chế băm một chiều thích ứng |
| Hash Difficulty Parameter | Số nguyên | Kiểm tra cấu hình tham số độ khó của cơ chế băm |
| Plaintext Password Count | Số mật khẩu | Query database kiểm tra mật khẩu không ở dạng hash |

### Tiêu chuẩn đáp ứng
- Hash Method Compliance = **Có**
- Hash Difficulty Parameter ≥ **mức tương đương bcrypt cost 10**
- Plaintext Password Count = **0**

### Đại lượng thay thế
- **Proxy:** Kết quả kiểm tra định dạng chuỗi lưu trong cột mật khẩu phải phù hợp với cơ chế băm đã cấu hình

---

## Tổng hợp: Bảng đặc tả bổ sung (Supplementary Specification Table)

> Format theo bài tập nhóm: **Quality Factor × Metric × Acceptance Criteria**

| # | Mã SUPL | Quality Factor | Metric | Acceptance Criteria | Proxy (nếu có) |
|---|---------|---------------|--------|---------------------|-----------------|
| 1 | P01 | Performance → Speed | P95 Response Time; Contract list/detail/termination response time | ≤ 2s (≤50 users), ≤ 5s (≤100 users); áp dụng cả UC 4.43–4.45 theo ngưỡng kế thừa | — |
| 2 | P02 | Performance → Capacity | Concurrent users, Throughput | ≥ 100 users, ≥ 50 tx/s | Số TCP connections ổn định |
| 3 | P03 | Performance → Speed | Dashboard/Report render time | Dashboard ≤ 5s, Report ≤ 15s | SQL query execution time |
| 4 | P04 | Performance → Speed | Search response time | ≤ 2s (≤10K records) cho nhân sự/đánh giá; ≤ 5s (≤50K records) cho tập dữ liệu lớn | SQL EXPLAIN time |
| 5 | P05 | Performance → Speed | Upload/Download time | Upload ≤ 5s, Download ≤ 3s (≤5MB) | Disk I/O speed |
| 6 | P06 | Performance → Speed | Excel export time | ≤ 10s (≤1K records), ≤ 30s (≤10K records) | API response time |
| 7 | R01 | Reliability → Availability | Uptime %, MTBF | ≥ 99.5%, MTBF ≥ 720h | Health check error rate |
| 8 | R02 | Reliability → Recoverability | MTTR | ≤ 15 phút | — |
| 9 | R03 | Reliability → Recoverability | RPO, RTO | RPO ≤ 24h, RTO ≤ 4h | Staging restore time |
| 10 | R04 | Reliability → Integrity | Data inconsistency count | 0 cases, 100% coverage bảo toàn nhất quán khi lỗi | FK violations count |
| 11 | R05 | Reliability → Fault Tolerance | Data loss rate | ≤ 5%, warning ≥ 5 phút trước | Popup hiển thị (binary) |
| 12 | SE01 | Security → Authentication | Password rules, Session security | ≥ 8 chars, 3 rules, phiên xác thực an toàn và tự hết hạn | Weak password count |
| 13 | SE02 | Security → Authorization | Unauthorized access count | 0 cases, 100% API protected | Unprotected route count |
| 14 | SE03 | Security → Integrity | Lock threshold, Duration | 5 failures → 15min lock | — |
| 15 | SE04 | Security → Confidentiality | TLS version, HTTPS coverage | TLS ≥ 1.2, 100% HTTPS | SSL Labs Score |
| 16 | SE05 | Security → Confidentiality | Exposed sensitive fields | 0 fields exposed | Unprotected API count |
| 17 | SE06 | Security → Integrity | CSRF/XSS vulnerabilities | 0 vulnerabilities | Unsanitized input count |
| 18 | SE07 | Security → Integrity | SQLi vulnerabilities | 0 vulnerabilities | Raw SQL query count |
| 19 | U01 | Usability → Consistency | UI violations, Vietnamese content | 0 pages, 100% tiếng Việt | Hardcoded style count |
| 20 | U02 | Usability → Learnability | Training time, Completion rate | ≤ 2h, ≥ 95% completion | Doc pages per role |
| 21 | U03 | Usability → Error Handling | Error message coverage | 100% Vietnamese, 100% fix suggestions | English error count |
| 22 | U04 | Usability → Efficiency | Steps to search+view | ≤ 3 steps, ≥ 3 filter criteria | — |
| 23 | U05 | Usability → Accessibility | Display compatibility | 100% desktop (≥1366×768), ≥ 80% tablet (1024×768) | CSS breakpoint count |
| 24 | U07 | Usability → Error Prevention | Confirmation dialog coverage | 100% critical actions, gồm chấm dứt hợp đồng trước hạn | — |
| 25 | S01 | Supportability → Modularity | Module coupling | ≤ 1 module affected | Cross-module imports |
| 26 | S03 | Supportability → Flexibility | Extendable categories | ≥ 3 danh mục master data, 0 code changes; cấu hình ẩn/hiện quản trị qua UI | — |
| 27 | F01 | Correctness → Auditability | Log coverage, Field completeness | 100% actions, 9/9 fields | Unaudited controllers |
| 28 | F08 | Security → Confidentiality | Hash compliance, Plaintext count | băm một chiều thích ứng, 0 plaintext | Regex check on DB |
