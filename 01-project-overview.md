# 1. Tổng quan dự án

## 1.1. Bối cảnh nghiệp vụ (Business Background)

**Cửa hàng Tạp hóa Chị Thành (Ms. Thanh's Grocery Store)** là một cửa hàng quy mô nhỏ, hiện
đang quản lý hoạt động bán hàng, nhập hàng và tồn kho chủ yếu bằng phương pháp thủ công
(sổ sách, Excel). Cách làm này dẫn đến nhiều vấn đề:

- Khó kiểm soát chính xác số lượng tồn kho theo thời gian thực
- Không có cảnh báo khi hàng sắp hết hoặc sắp hết hạn sử dụng
- Mất nhiều thời gian tính toán doanh thu cuối ngày
- Khó phân tích được mặt hàng nào bán chạy để lên kế hoạch nhập hàng hợp lý

Chị Thành mong muốn xây dựng một hệ thống phần mềm quản lý bán hàng (kết hợp POS –
Point of Sale và quản lý kho) nhằm số hóa toàn bộ quy trình vận hành, giảm thiểu sai sót và
thất thoát, đồng thời cung cấp báo cáo hỗ trợ ra quyết định kinh doanh.

## 1.2. Mục tiêu dự án (Business Objectives)

- Số hóa quy trình bán hàng, giảm thời gian thanh toán cho mỗi giao dịch xuống dưới 1 phút.
- Kiểm soát tồn kho chính xác theo thời gian thực, giảm thất thoát hàng hóa do sai sót kiểm đếm thủ công.
- Cảnh báo tự động khi hàng sắp hết hoặc sắp hết hạn sử dụng để giảm hàng hóa hư hỏng, hết hạn.
- Cung cấp báo cáo doanh thu, báo cáo tồn kho theo ngày/tuần/tháng giúp Chị Thành ra quyết định nhanh và chính xác.
- Xây dựng chương trình khách hàng thân thiết (tích điểm) để tăng tỷ lệ khách hàng quay lại.

## 1.3. Phạm vi dự án (Project Scope)

### Trong phạm vi (In-scope)
- Quản lý bán hàng tại quầy (POS): tạo đơn hàng, thanh toán, in hóa đơn, áp dụng khuyến mãi/giảm giá.
- Quản lý danh mục sản phẩm: thêm/sửa/xóa sản phẩm, phân loại, quản lý giá bán, giá vốn.
- Quản lý tồn kho: cập nhật tồn kho theo thời gian thực, cảnh báo tồn kho thấp, cảnh báo hạn sử dụng.
- Quản lý nhập hàng: tạo phiếu nhập từ nhà cung cấp, cập nhật tồn kho tự động sau khi nhập.
- Quản lý khách hàng: lưu thông tin khách hàng, tích lũy điểm thưởng, xem lịch sử mua hàng.
- Báo cáo & thống kê: doanh thu theo thời gian, top sản phẩm bán chạy, báo cáo tồn kho.
- Phân quyền người dùng: Owner (Chị Thành), Cashier, Inventory Staff.

### Ngoài phạm vi (Out-of-scope, giai đoạn 1)
- Bán hàng đa kênh (online/website thương mại điện tử).
- Tích hợp thanh toán trực tuyến qua cổng thanh toán bên thứ ba.
- Quản lý chuỗi cung ứng phức tạp giữa nhiều chi nhánh/kho trung tâm.

## 1.4. Danh sách Stakeholders

| Vai trò | Mô tả | Quyền lợi / Trách nhiệm |
|---|---|---|
| **Chị Thành (Owner/Admin)** | Chủ cửa hàng, người ra quyết định kinh doanh, đầu tư hệ thống | Xem báo cáo tổng hợp, quản lý nhân viên, cấu hình hệ thống, phê duyệt khuyến mãi |
| **Cashier** | Nhân viên bán hàng, trực tiếp thao tác tại quầy | Tạo đơn hàng, thanh toán, in hóa đơn, tra cứu sản phẩm |
| **Inventory Staff** | Nhân viên kho | Tạo phiếu nhập hàng, kiểm kê, cập nhật thông tin sản phẩm |
| **Customer** | Khách hàng mua sắm tại cửa hàng | Mua hàng, tích điểm thành viên, nhận ưu đãi |
| **Supplier** | Nhà cung cấp hàng hóa | Cung cấp thông tin sản phẩm, đơn giá nhập |
| **Business Analyst** | Người phân tích và tài liệu hóa yêu cầu | Thu thập, phân tích, đặc tả yêu cầu; đảm bảo giải pháp đáp ứng đúng nhu cầu nghiệp vụ |
| **Dev Team** | Lập trình viên, kiểm thử viên | Xây dựng và kiểm thử hệ thống theo đặc tả |

---
⬅️ [Về README](../README.md) | ➡️ [Tiếp theo: BRD](02-brd.md)
