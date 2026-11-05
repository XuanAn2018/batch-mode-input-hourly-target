[CHANGELOG.md](https://github.com/user-attachments/files/34423769/CHANGELOG.md)
# Nhật ký thay đổi

## [3.3.0] - 2026-11-05
### Đã thêm
- Nâng cấp toàn diện giao diện theo chuẩn **Modern Enterprise Dashboard**: thiết kế phẳng tinh tế, độ tương phản cao, tối ưu cho môi trường sản xuất công nghiệp.
- **Dropdown chọn ca & giờ trực tiếp trên từng Card**: tích hợp sẵn các tùy chọn `☀️ Ca sáng (7.5h)`, `🌙 OT 3 giờ (3h)`, `🌙 OT 11 giờ (11h)` và `⚙️ Tùy chỉnh`. Người dùng chọn là áp dụng ngay mà không bắt buộc phải mở drawer.
- **Khu vực cấu hình chi tiết chuyển sang góc dưới bên PHẢI**: nằm thẳng hàng ngay dưới dropdown ca, giúp thao tác bấm chuột tự nhiên và tiện tay, loại bỏ hoàn toàn việc phải rê chuột sang góc trái màn hình.
- **Đưa 2 nút hành động chính "Bỏ chọn" và "Xử lý" lên thanh công cụ phía trên**: nằm ngay cạnh nhóm gán ca, có chỉ báo số lượng gói đã chọn và tự động kích hoạt/vô hiệu hóa theo ngữ cảnh.
- Nhúng hệ phông chữ hiện đại **Inter** và **JetBrains Mono** với tính năng `tabular-nums` giúp số liệu căn lề thẳng tắp, không bị rung lắc khi cập nhật thời gian thực.
- Thêm **Mini Progress Bar** và nhãn phần trăm tiến độ `(X%)` ngay trong từng card gói sản xuất, giúp nhận diện ngay gói đạt/thiếu chỉ trong 1 giây.
- Hỗ trợ phím tắt tiện lợi: `Ctrl + F` hoặc `/` để tìm kiếm gói tức thì, `Esc` để đóng modal hoặc thoát ô tìm kiếm.

### Đã sửa
- **Sửa triệt để lỗi không đặt lại Cấu hình ca/giờ khi bỏ chọn**: khi người dùng bỏ tick riêng lẻ, bỏ chọn theo Line hoặc bấm "Bỏ chọn tất cả", toàn bộ cấu hình trong bộ nhớ lẫn giao diện DOM (dropdown ca, ô nhập giờ, nút ca sáng/OT) đều được đặt lại hoàn toàn về **Ca sáng (7.5h)** ngay lập tức mà không cần phải tải lại trang.
- **Sửa lỗi modal thông báo bị lệch góc**: loại bỏ popup `bottom-end` cũ gây méo giao diện góc màn hình; thay bằng hộp thoại xác nhận căn giữa chuẩn và Toast thông báo tinh gọn góc trên bên phải.

### Đã thay đổi
- **Loại bỏ hoàn toàn thanh Dock ở đáy màn hình**: giải phóng 100% diện tích chiều dọc để cuộn và quan sát danh sách gói sản xuất mà không bị thanh nổi che khuất nội dung.
- Chuyển đổi toàn bộ bảng màu sang hệ Slate Neutral chuyên nghiệp cùng màu trạng thái phân cấp chuẩn (Emerald Đạt, Amber Thiếu, Sky Vượt, Violet OT).
- Tinh giản Header theo phong cách Titanium tối màu sang trọng, đồng bộ hiển thị FA Robot, nút Nhập thủ công và phiên bản.
- Tối ưu thanh điều khiển Command Bar 2 tầng: tách biệt rõ ràng khu vực Cấu hình & KPI tổng thể với khu vực Lọc & Tìm kiếm.
- Tối ưu hóa cảm ứng cho Tablet và Chế độ Desktop Android: kích thước vùng chạm (touch target) tối thiểu 40px, checkbox rõ ràng, tránh bấm nhầm.

## [Unreleased]
### Đã thêm
- Biểu tượng trang web (favicon SVG) và màu chủ đề trình duyệt
- Thống kê OT đã chọn, tách riêng OT 3 giờ và OT 11 giờ
- Thanh tổng kết lựa chọn cố định ở đáy màn hình
- Chip cảnh báo số gói đang chọn nhưng nằm ngoài bộ lọc hiện tại
- Chọn / bỏ chọn toàn bộ theo từng Line
- Số lượng gói hiển thị trong bộ lọc Line, trạng thái và OT
- Nút áp dụng nhanh OT 11 giờ cho các gói đã chọn

### Đã thay đổi
- Tái cấu trúc giao diện theo hướng chuyên nghiệp: gộp 3 tầng thống kê còn 1 KPI bar 5 chỉ số
- Thay banner tổng kết lớn bằng data strip mảnh, có thanh tiến độ thực tế / target
- Card gói gọn lại; cấu hình ca/giờ mở rộng khi bấm vào nút ca
- Sắp xếp lại toolbar và action bar cho màn hình 1024px, thêm breakpoint 1100px
- Chuẩn hóa thuật ngữ: Ca sáng / OT 3 giờ / OT 11 giờ / OT đã đạt
- Chuẩn hóa định dạng số và giờ theo vi-VN
- Giảm màu trang trí, dùng màu trạng thái cho Thiếu / Đủ / Vượt
- Chỉ còn một hành động chính "Xử lý" ở thanh chọn phía dưới
- Checkbox chọn gói lớn hơn, dễ thao tác trên tablet
- Nút "Sáng" / "OT 3 giờ" / "OT 11 giờ" cảnh báo khi chưa chọn gói thay vì im lặng
- Nút "Tất cả" đổi thành "Chọn hiển thị" để rõ phạm vi
- Reset không còn render lại toàn bộ danh sách

### Đã sửa
- Tách nhãn "OT khả dụng" (dữ liệu API) khỏi "OT đã chọn" (cấu hình batch)
- Bỏ chọn tất cả có xác nhận và hỗ trợ hoàn tác trong 6 giây
- Đóng cấu hình ca/giờ khi bỏ chọn gói
- Đồng bộ aria-expanded cho nút mở cấu hình ca

## [2.4.0] - 2026-02-02
### Đã thêm
- Nút nhập liệu thủ công trong tiêu đề
- Cải tiến thiết kế cửa sổ bật lên kết quả
- Hỗ trợ Chế độ Máy tính để bàn Android
- Cải thiện thiết kế đáp ứng

### Đã thay đổi
- Sắp xếp lại bố cục khu vực tóm tắt
- Cập nhật văn bản cửa sổ bật lên xem trước hàng loạt
- Cải thiện kiểu phông chữ cho nút hành động

### Đã sửa
- Sự cố xử lý sự kiện hộp kiểm
- Cải thiện bố cục trên thiết bị di động
- Tối ưu hóa hiệu suất
