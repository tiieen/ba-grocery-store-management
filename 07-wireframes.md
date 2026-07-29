# 7. Wireframes & UI Mockups

Phần này trình bày các giao diện chính của **GSMS – Grocery Store Management System**.

Các mockup được thiết kế trên **Figma**, dựa trên yêu cầu nghiệp vụ và nhu cầu sử dụng của chủ cửa hàng, nhân viên bán hàng và nhân viên quản lý kho.

Mục tiêu thiết kế là tạo ra giao diện đơn giản, trực quan, dễ thao tác và phù hợp với hoạt động của cửa hàng tạp hóa quy mô nhỏ.


## 7.1. Màn hình Bán hàng – POS Screen

![Màn hình bán hàng POS](../assets/pos-ban-hang.png)

### Mục đích

Màn hình POS hỗ trợ nhân viên bán hàng tìm kiếm sản phẩm, thêm sản phẩm vào giỏ hàng, áp dụng khuyến mãi và thực hiện thanh toán cho khách hàng.

### Chức năng chính

- Tìm kiếm sản phẩm theo tên hoặc mã sản phẩm.
- Hỗ trợ quét mã vạch.
- Thêm sản phẩm vào giỏ hàng.
- Điều chỉnh số lượng sản phẩm.
- Hiển thị đơn giá và thành tiền.
- Chọn khách hàng thành viên.
- Nhập mã khuyến mãi.
- Lựa chọn phương thức thanh toán.
- Tính tổng tiền và tiền thừa.
- Tạo hóa đơn sau khi thanh toán thành công.
- Tự động cập nhật số lượng tồn kho.


## 7.2. Màn hình Quản lý Sản phẩm & Tồn kho

![Màn hình quản lý sản phẩm và tồn kho](../assets/san-pham-ton-kho.png)

### Mục đích

Màn hình hỗ trợ chủ cửa hàng và nhân viên kho quản lý danh sách sản phẩm, theo dõi số lượng tồn, hạn sử dụng và trạng thái hàng hóa.

### Chức năng chính

- Tìm kiếm sản phẩm theo tên hoặc mã sản phẩm.
- Lọc sản phẩm theo danh mục.
- Lọc theo trạng thái tồn kho.
- Theo dõi số lượng tồn hiện tại.
- Theo dõi hạn sử dụng.
- Cảnh báo sản phẩm sắp hết hàng.
- Cảnh báo sản phẩm sắp hết hạn.
- Thêm, xem, chỉnh sửa hoặc xóa sản phẩm.

### Quy ước trạng thái

| Trạng thái | Ý nghĩa |
|---|---|
| 🟢 Bình thường | Số lượng tồn vẫn ở mức an toàn |
| 🟡 Sắp hết hạn | Sản phẩm cần được ưu tiên xử lý |
| 🟠 Sắp hết hàng | Số lượng tồn bằng hoặc thấp hơn mức tối thiểu |
| 🔴 Hết hàng | Số lượng tồn kho bằng 0 |


## 7.3. Modal Thêm sản phẩm

![Modal thêm sản phẩm](../assets/modal-them-san-pham.png)

Modal được hiển thị khi người dùng chọn chức năng **Thêm sản phẩm** tại màn hình quản lý sản phẩm và tồn kho.

### Thông tin nhập liệu

- Mã sản phẩm.
- Tên sản phẩm.
- Mã vạch.
- Danh mục.
- Đơn vị tính.
- Giá nhập.
- Giá bán.
- Số lượng tồn ban đầu.
- Mức tồn kho tối thiểu.
- Hạn sử dụng.
- Nhà cung cấp.
- Hình ảnh sản phẩm.

### Quy tắc kiểm tra

- Mã sản phẩm không được để trống hoặc trùng lặp.
- Mã vạch không được trùng với sản phẩm đã tồn tại.
- Giá nhập và giá bán phải lớn hơn 0.
- Số lượng tồn không được là số âm.
- Các trường bắt buộc phải được nhập đầy đủ trước khi lưu.

## 7.4. Màn hình Nhập hàng

![Màn hình nhập hàng](../assets/nhap-hang.png)

### Mục đích

Màn hình nhập hàng hỗ trợ chủ cửa hàng hoặc nhân viên kho tạo phiếu nhập, ghi nhận hàng hóa từ nhà cung cấp và cập nhật số lượng tồn kho.

### Chức năng chính

- Tạo mã phiếu nhập tự động.
- Chọn nhà cung cấp.
- Chọn ngày nhập hàng.
- Thêm sản phẩm vào phiếu nhập.
- Nhập số lượng và đơn giá nhập.
- Ghi nhận hạn sử dụng.
- Tính thành tiền cho từng sản phẩm.
- Tính tổng giá trị phiếu nhập.
- Lưu nháp hoặc xác nhận phiếu nhập.

### Luồng thao tác

1. Người dùng chọn nhà cung cấp.
2. Người dùng thêm sản phẩm vào phiếu nhập.
3. Nhập số lượng, giá nhập và hạn sử dụng.
4. Hệ thống tính thành tiền và tổng giá trị phiếu.
5. Người dùng kiểm tra thông tin.
6. Người dùng xác nhận nhập hàng.
7. Hệ thống cập nhật tồn kho và lưu lịch sử nhập hàng.


## 7.5. Modal Xác nhận nhập hàng

![Modal xác nhận nhập hàng](../assets/modal-xac-nhan-nhap.png)

Modal được hiển thị khi người dùng chọn **Xác nhận nhập hàng**.

Mục đích của modal là yêu cầu người dùng kiểm tra lại thao tác trước khi hệ thống cập nhật tồn kho.

### Hành động

- **Quay lại:** Đóng modal và tiếp tục chỉnh sửa phiếu nhập.
- **Xác nhận:** Hoàn tất phiếu nhập và cập nhật số lượng tồn kho.

Sau khi xác nhận thành công, phiếu nhập không được chỉnh sửa trực tiếp để bảo đảm tính chính xác của dữ liệu.


## 7.6. Dashboard Tổng quan

![Dashboard tổng quan](../assets/dashboard-tong-quan.png)

### Mục đích

Dashboard hỗ trợ chủ cửa hàng theo dõi nhanh tình hình kinh doanh và những vấn đề cần xử lý.

### Các chỉ số chính

- Tổng doanh thu.
- Tổng số đơn hàng.
- Lợi nhuận ước tính.
- Giá trị đơn hàng trung bình.
- Tỷ lệ tăng hoặc giảm so với kỳ trước.

### Nội dung phân tích

- Doanh thu theo thời gian.
- Lợi nhuận theo thời gian.
- Doanh thu theo danh mục.
- Top sản phẩm bán chạy.
- Danh sách sản phẩm tồn kho thấp.
- Danh sách sản phẩm sắp hết hạn.

### Bộ lọc thời gian

- Hôm nay.
- Tuần này.
- Tháng này.
- Khoảng thời gian tùy chỉnh.


## 7.7. Một số quyết định thiết kế

| Quyết định thiết kế | Lý do |
|---|---|
| Thanh tìm kiếm được đặt ở đầu màn hình POS | Giúp nhân viên tiếp cận nhanh chức năng được sử dụng nhiều nhất |
| Khu vực thanh toán được đặt bên phải | Phù hợp với luồng thao tác từ trái sang phải |
| Nút Thanh toán được làm nổi bật | Giúp phân biệt hành động chính với hành động phụ |
| Trạng thái tồn kho được phân biệt bằng màu sắc | Giúp người dùng nhanh chóng phát hiện sản phẩm cần xử lý |
| Dashboard sử dụng các KPI dạng card | Giúp chủ cửa hàng nắm bắt thông tin nhanh |
| Có modal xác nhận trước khi nhập hàng | Hạn chế thao tác nhầm và cập nhật sai số lượng tồn kho |


## 7.8. Công cụ thiết kế

- **Figma:** Thiết kế UI mockup và prototype.
- **Mermaid:** Mô hình hóa quy trình nghiệp vụ.
- **Draw.io:** Thiết kế Use Case Diagram, Process Flow và ERD.
- **GitHub:** Lưu trữ và trình bày tài liệu dự án.

---

> Các giao diện được xây dựng cho mục đích học tập và mô phỏng giải pháp. Thiết kế có thể được điều chỉnh thêm sau quá trình thu thập phản hồi và kiểm thử khả năng sử dụng.

---

⬅️ [Trước: ERD](06-erd.md) | 🏠 [Về README](../README.md)
