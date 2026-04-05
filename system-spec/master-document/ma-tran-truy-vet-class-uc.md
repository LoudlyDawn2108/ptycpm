## 5.4. Ma trận truy vết UC → Design

| UC | Boundary chính | Controller chính | Entity/Enumeration chính | Ghi chú truy vết BCE |
| --- | --- | --- | --- | --- |
| UC 4.1 | DangNhapForm | AuthController, NhatKyController | TaiKhoan, NhatKyHeThong, TrangThaiTaiKhoan, LoaiHanhDong | Đăng nhập đi theo chuỗi Actor → Boundary → Controller → Entity, đồng thời ghi log đăng nhập. |
| UC 4.2 | DangNhapForm | AuthController, NhatKyController | TaiKhoan, NhatKyHeThong, LoaiHanhDong | Bao phủ đăng xuất thủ công và đăng xuất tự động theo timeout phiên. |
| UC 4.3 | DangNhapForm | AuthController, NhatKyController | TaiKhoan, NhatKyHeThong, LoaiHanhDong | Đổi mật khẩu dùng boundary riêng nhưng tái sử dụng controller xác thực. |
| UC 4.4 | QuanLyTaiKhoanPage | TaiKhoanController | TaiKhoan, HoSoNhanSu, VaiTro, TrangThaiTaiKhoan | Tìm kiếm tài khoản đi qua trang quản lý tài khoản và bộ điều phối tài khoản. |
| UC 4.5 | QuanLyTaiKhoanPage | TaiKhoanController, NhatKyController | TaiKhoan, HoSoNhanSu, VaiTro, LoaiHanhDong | Thêm tài khoản mới, liên kết hồ sơ nhân sự và ghi log thao tác thêm. |
| UC 4.6 | QuanLyTaiKhoanPage | TaiKhoanController, NhatKyController | TaiKhoan, VaiTro, LoaiHanhDong | Sửa thông tin tài khoản bao gồm thay đổi email và vai trò (phân quyền), lưu vết thay đổi. |
| UC 4.7 | QuanLyTaiKhoanPage | TaiKhoanController, NhatKyController | TaiKhoan, TrangThaiTaiKhoan, LoaiHanhDong | Thay đổi trạng thái tài khoản: khóa/mở khóa thủ công và khóa tự động khi thôi việc. |
| UC 4.8 | CoCauToChucPage | ToChucController, NhatKyController | DonViToChuc, LoaiDonVi, TrangThaiDonVi, LoaiHanhDong | Tạo đơn vị mới trong cây cơ cấu tổ chức. |
| UC 4.9 | CoCauToChucPage | ToChucController, NhatKyController | DonViToChuc, LoaiDonVi, LoaiHanhDong | Sửa thông tin đơn vị và cập nhật cây tổ chức. |
| UC 4.10 | CoCauToChucPage | ToChucController, HopDongController, BoNhiemController, NhatKyController | DonViToChuc, HoSoNhanSu, HopDongLaoDong, BoNhiem, TrangThaiDonVi, TrangThaiHopDong, TrangThaiHopDongNhanSu, TrangThaiLamViec, LoaiHanhDong | Giải thể đơn vị kéo theo chấm dứt hợp đồng, gỡ bổ nhiệm và đồng bộ trạng thái nhân sự. |
| UC 4.11 | CoCauToChucPage | ToChucController, BoNhiemController | DonViToChuc, BoNhiem, HoSoNhanSu, TrangThaiDonVi | Xem chi tiết đơn vị gồm tab tổng quan, nhân sự, đơn vị trực thuộc và lịch sử bổ nhiệm. |
| UC 4.12 | CoCauToChucPage | ToChucController, BoNhiemController, NhatKyController | DonViToChuc, HoSoNhanSu, BoNhiem, TrangThaiDonVi, LoaiHanhDong | Sáp nhập đơn vị: chuyển nhân sự và đơn vị con trực thuộc sang đơn vị nhận sáp nhập. |
| UC 4.13 | DanhMucHeSoLuongPage | DanhMucController, NhatKyController | HeSoLuong, TrangThaiDanhMuc, LoaiHanhDong | Thêm mới hệ số lương. |
| UC 4.14 | DanhMucHeSoLuongPage | DanhMucController, NhatKyController | HeSoLuong, TrangThaiDanhMuc, LoaiHanhDong | Sửa danh mục hệ số lương. |
| UC 4.16 | DanhMucHeSoLuongPage | DanhMucController, NhatKyController | HeSoLuong, TrangThaiDanhMuc, LoaiHanhDong | Đổi trạng thái sử dụng của hệ số lương. |
| UC 4.17 | DanhMucPhuCapPage | DanhMucController, NhatKyController | LoaiPhuCap, TrangThaiDanhMuc, LoaiHanhDong | Thêm mới loại phụ cấp. |
| UC 4.18 | DanhMucPhuCapPage | DanhMucController, NhatKyController | LoaiPhuCap, TrangThaiDanhMuc, LoaiHanhDong | Sửa loại phụ cấp. |
| UC 4.19 | DanhMucPhuCapPage | DanhMucController, NhatKyController | LoaiPhuCap, TrangThaiDanhMuc, LoaiHanhDong | Đổi trạng thái loại phụ cấp. |
| UC 4.20 | DanhMucHopDongPage | DanhMucController, NhatKyController | LoaiHopDong, TrangThaiDanhMuc, LoaiHanhDong | Thêm mới loại hợp đồng. |
| UC 4.21 | DanhMucHopDongPage | DanhMucController, NhatKyController | LoaiHopDong, TrangThaiDanhMuc, LoaiHanhDong | Sửa loại hợp đồng. |
| UC 4.22 | DanhMucHopDongPage | DanhMucController, NhatKyController | LoaiHopDong, TrangThaiDanhMuc, LoaiHanhDong | Đổi trạng thái loại hợp đồng. |
| UC 4.23 | BaoCaoThongKePage | ThongKeController | HoSoNhanSu, DonViToChuc, HopDongLaoDong, DanhGia, KhoaDaoTao, DangKyDaoTao | Thống kê tổng hợp dữ liệu từ nhiều entity lõi. |
| UC 4.24 | NhatKyHeThongPage | NhatKyController | NhatKyHeThong, TaiKhoan, LoaiHanhDong, VaiTro | Bao phủ xem, lọc, xem chi tiết và xuất audit log. |
| UC 4.25 | HopDongLaoDongForm | HopDongController, NhatKyController | HopDongLaoDong, HoSoNhanSu, LoaiHopDong, TrangThaiHopDong, TrangThaiHopDongNhanSu, LoaiHanhDong | Tạo hợp đồng mới và đồng bộ trạng thái hợp đồng của nhân sự. |
| UC 4.26 | HopDongLaoDongForm | HopDongController | HopDongLaoDong, HoSoNhanSu, LoaiHopDong, TrangThaiHopDong | Xem danh sách và chi tiết hợp đồng lao động. |
| UC 4.27 | HopDongLaoDongForm | HopDongController, NhatKyController | HopDongLaoDong, LoaiHopDong, TrangThaiHopDong, LoaiHanhDong | Chỉnh sửa hợp đồng chưa có hiệu lực. |
| UC 4.28 | HopDongLaoDongForm | HopDongController, NhatKyController | HopDongLaoDong, HoSoNhanSu, TrangThaiHopDong, TrangThaiHopDongNhanSu, LoaiHanhDong | Chấm dứt hợp đồng lao động trước hạn. |
| UC 4.29 | DanhSachNhanSuPage | HoSoNhanSuController | HoSoNhanSu, GioiTinh, TrangThaiLamViec, TrangThaiHopDongNhanSu | Tìm kiếm hồ sơ nhân sự theo từ khóa. |
| UC 4.30 | DanhSachNhanSuPage | HoSoNhanSuController | HoSoNhanSu, GioiTinh, TrangThaiLamViec, TrangThaiHopDongNhanSu | Lọc danh sách hồ sơ theo nhiều tiêu chí. |
| UC 4.31 | HoSoNhanSuForm | HoSoNhanSuController, NhatKyController | HoSoNhanSu, ThongTinNguoiNuocNgoai, ThongTinGiaDinh, ThongTinNganHang, QuaTrinhCongTac, BangCap, ChungChi, HeSoLuong, PhuCapNhanSu, LoaiHanhDong | Thêm mới hồ sơ nhân sự và các thành phần cấu thành hồ sơ. |
| UC 4.32 | HoSoNhanSuForm | HoSoNhanSuController, NhatKyController | HoSoNhanSu, ThongTinNguoiNuocNgoai, ThongTinGiaDinh, ThongTinNganHang, QuaTrinhCongTac, BangCap, ChungChi, HeSoLuong, PhuCapNhanSu, LoaiHanhDong | Chỉnh sửa chi tiết hồ sơ nhân sự. |
| UC 4.33 | HoSoNhanSuForm | HoSoNhanSuController, TaiKhoanController, HopDongController, NhatKyController | HoSoNhanSu, TaiKhoan, HopDongLaoDong, TrangThaiLamViec, TrangThaiHopDongNhanSu, TrangThaiTaiKhoan, LoaiHanhDong | Đánh dấu thôi việc kéo theo khóa tài khoản và đồng bộ hợp đồng. |
| UC 4.34 | *(System Timer — không qua Boundary)* | HopDongController, HoSoNhanSuController, TaiKhoanController | HopDongLaoDong, HoSoNhanSu, TaiKhoan, LoaiHopDong, TrangThaiHopDong, TrangThaiLamViec, TrangThaiHopDongNhanSu, TrangThaiTaiKhoan | Hệ thống tự động chuyển trạng thái hợp đồng và đánh dấu thôi việc khi hết hạn gia hạn. |
| UC 4.35 | HoSoNhanSuForm | HoSoNhanSuController | HoSoNhanSu, ThongTinGiaDinh, ThongTinNganHang, QuaTrinhCongTac, BangCap, ChungChi, HeSoLuong, PhuCapNhanSu | Xem chi tiết hồ sơ nhân sự ở chế độ chỉ đọc. |
| UC 4.36 | HoSoNhanSuForm | HoSoNhanSuController | HoSoNhanSu, ThongTinGiaDinh, ThongTinNganHang, QuaTrinhCongTac, BangCap, ChungChi, HeSoLuong, PhuCapNhanSu | In PDF hoặc xuất Excel hồ sơ nhân sự từ màn hình chi tiết. |
| UC 4.37 | CauHinhHeThongPage | CauHinhController, NhatKyController | CauHinhHeThong, VaiTro, LoaiHanhDong | Cấu hình ẩn/hiện mục khen thưởng/kỷ luật theo vai trò. |
| UC 4.38 | CoCauToChucPage | BoNhiemController, NhatKyController | BoNhiem, HoSoNhanSu, DonViToChuc, TrangThaiLamViec, LoaiHanhDong | Bổ nhiệm/điều chuyển nhân sự cho đơn vị, cập nhật trạng thái làm việc. |
| UC 4.39 | CoCauToChucPage | BoNhiemController, NhatKyController | BoNhiem, HoSoNhanSu, DonViToChuc, TrangThaiLamViec, LoaiHanhDong | Bãi nhiệm nhân sự khỏi đơn vị tổ chức, trạng thái chuyển về "Đang chờ xét". |
| UC 4.40 | DanhGiaForm | DanhGiaController, NhatKyController | DanhGia, KhenThuong, KyLuat, HoSoNhanSu, LoaiHanhDong | Ghi nhận đánh giá dùng kế thừa thay cho enum loại đánh giá. |
| UC 4.41 | DanhGiaForm | DanhGiaController | DanhGia, KhenThuong, KyLuat, HoSoNhanSu, CauHinhHeThong | Xem lịch sử đánh giá theo mô hình kế thừa và cấu hình hiển thị. |
| UC 4.42 | DanhGiaForm | DanhGiaController | DanhGia, KhenThuong, KyLuat, HoSoNhanSu | Tìm kiếm và lọc danh sách đánh giá. |
| UC 4.43 | KhoaDaoTaoPage | DaoTaoController, NhatKyController | KhoaDaoTao, TrangThaiKhoaDaoTao, LoaiHanhDong | Mở khóa đào tạo mới. |
| UC 4.44 | KhoaDaoTaoPage | DaoTaoController, NhatKyController | KhoaDaoTao, DangKyDaoTao, TrangThaiKhoaDaoTao, LoaiHanhDong | Sửa thông tin khóa đào tạo đã mở. |
| UC 4.45 | KhoaDaoTaoPage | DaoTaoController | KhoaDaoTao, DangKyDaoTao, TrangThaiKhoaDaoTao, TrangThaiThamGia | Xem chi tiết khóa đào tạo và danh sách học viên. |
| UC 4.46 | KhoaDaoTaoPage | DaoTaoController, NhatKyController | DangKyDaoTao, KhoaDaoTao, ChungChi, TrangThaiThamGia, LoaiHanhDong | Ghi nhận kết quả đào tạo và lưu chứng chỉ vào hồ sơ. |
| UC 4.47 | HoSoNhanSuForm | HoSoNhanSuController, CauHinhController | HoSoNhanSu, HopDongLaoDong, DanhGia, CauHinhHeThong | Self-service hồ sơ cá nhân vẫn tuân thủ chuỗi BCE và chịu tác động cấu hình hiển thị. |
| UC 4.48 | CoCauToChucPage | ToChucController | DonViToChuc, BoNhiem, HoSoNhanSu | Xem thông tin chi tiết đơn vị đang công tác của CBGV. |
| UC 4.49 | KhoaDaoTaoPage | DaoTaoController, NhatKyController | DangKyDaoTao, KhoaDaoTao, TrangThaiThamGia, LoaiHanhDong | Đăng ký/hủy đăng ký khóa đào tạo; chỉ cho phép hủy khi trạng thái 'Đã đăng ký'. |
| UC 4.50 | KhoaDaoTaoPage | DaoTaoController | DangKyDaoTao, KhoaDaoTao, TrangThaiThamGia | Xem danh sách các khóa đào tạo đã đăng ký. |