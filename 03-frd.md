# 3. Functional Requirement Document (FRD)

## 3.1. Yêu cầu chức năng (Functional Requirements)

### 3.1.1. Module Bán hàng (POS)

| Mã | Chức năng | Mô tả chi tiết |
|---|---|---|
| FR-01 | Tạo đơn hàng | Cho phép Cashier tìm kiếm sản phẩm (theo tên/mã barcode), thêm vào giỏ hàng, điều chỉnh số lượng |
| FR-02 | Áp dụng khuyến mãi | Cho phép áp dụng mã giảm giá hoặc chương trình khuyến mãi đang hoạt động vào đơn hàng |
| FR-03 | Thanh toán | Hỗ trợ thanh toán tiền mặt và chuyển khoản; tính tiền thối lại tự động |
| FR-04 | In hóa đơn | Xuất hóa đơn dạng giấy hoặc điện tử sau khi thanh toán thành công |
| FR-05 | Hủy/hoàn đơn hàng | Cho phép hủy đơn hàng trong ca làm việc hoặc hoàn trả sản phẩm, hoàn tồn kho tương ứng |

### 3.1.2. Module Quản lý sản phẩm & Tồn kho

| Mã | Chức năng | Mô tả chi tiết |
|---|---|---|
| FR-06 | Quản lý danh mục sản phẩm | Thêm/sửa/xóa sản phẩm với các thuộc tính: tên, mã, danh mục, đơn vị tính, giá bán, giá vốn, hạn sử dụng |
| FR-07 | Cập nhật tồn kho tự động | Tồn kho được trừ/cộng tự động khi có giao dịch bán/nhập/hoàn hàng |
| FR-08 | Cảnh báo tồn kho thấp | Gửi cảnh báo trên hệ thống khi số lượng tồn kho ≤ ngưỡng tối thiểu đã cấu hình |
| FR-09 | Cảnh báo hạn sử dụng | Gửi cảnh báo khi sản phẩm còn cách hạn sử dụng ≤ số ngày cấu hình (VD: 7 ngày) |
| FR-10 | Kiểm kê kho | Cho phép nhân viên kho đối chiếu tồn kho thực tế với hệ thống và điều chỉnh chênh lệch |

### 3.1.3. Module Nhập hàng

| Mã | Chức năng | Mô tả chi tiết |
|---|---|---|
| FR-11 | Quản lý nhà cung cấp | Thêm/sửa/xóa thông tin nhà cung cấp: tên, liên hệ, sản phẩm cung cấp |
| FR-12 | Tạo phiếu nhập hàng | Tạo phiếu nhập với danh sách sản phẩm, số lượng, đơn giá nhập, nhà cung cấp |
| FR-13 | Xác nhận nhập kho | Sau khi xác nhận phiếu nhập, hệ thống tự động cộng số lượng vào tồn kho |

### 3.1.4. Module Khách hàng

| Mã | Chức năng | Mô tả chi tiết |
|---|---|---|
| FR-14 | Đăng ký thành viên | Lưu thông tin khách hàng: tên, số điện thoại; cấp mã thành viên |
| FR-15 | Tích điểm & đổi điểm | Cộng điểm dựa trên giá trị đơn hàng; cho phép quy đổi điểm thành giảm giá |
| FR-16 | Lịch sử mua hàng | Xem lại lịch sử các đơn hàng của một khách hàng cụ thể |

### 3.1.5. Module Báo cáo

| Mã | Chức năng | Mô tả chi tiết |
|---|---|---|
| FR-17 | Báo cáo doanh thu | Thống kê doanh thu theo ngày/tuần/tháng, theo nhân viên, theo danh mục sản phẩm |
| FR-18 | Báo cáo tồn kho | Thống kê tồn kho hiện tại, sản phẩm sắp hết, sản phẩm sắp hết hạn |
| FR-19 | Báo cáo sản phẩm bán chạy | Xếp hạng top sản phẩm theo số lượng bán hoặc doanh thu |

## 3.2. Yêu cầu phi chức năng (Non-Functional Requirements)

| Mã | Loại yêu cầu | Mô tả |
|---|---|---|
| NFR-01 | Hiệu năng (Performance) | Thời gian xử lý một giao dịch bán hàng không quá 2 giây |
| NFR-02 | Khả dụng (Availability) | Hệ thống hoạt động ổn định trong giờ mở cửa (uptime ≥ 99%) |
| NFR-03 | Bảo mật (Security) | Mật khẩu người dùng được mã hóa; phân quyền rõ ràng theo vai trò |
| NFR-04 | Khả năng mở rộng (Scalability) | Hệ thống có thể mở rộng thêm chi nhánh mới trong tương lai |
| NFR-05 | Tính dễ sử dụng (Usability) | Giao diện đơn giản, nhân viên mới có thể thao tác thành thạo sau 30 phút đào tạo |
| NFR-06 | Sao lưu dữ liệu (Backup) | Dữ liệu được sao lưu tự động hàng ngày |

---
⬅️ [Trước: BRD](02-brd.md) | ➡️ [Tiếp theo: Use Cases](04-use-cases.md)
