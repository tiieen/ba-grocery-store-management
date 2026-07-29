# 2. Business Requirement Document (BRD)

## 2.1. Vấn đề nghiệp vụ hiện tại

- Việc kiểm đếm tồn kho thủ công tốn nhiều thời gian và dễ sai sót.
- Không có cảnh báo khi sản phẩm sắp hết hàng, dẫn đến gián đoạn kinh doanh.
- Không kiểm soát được hạn sử dụng, gây thất thoát do hàng hóa hết hạn.
- Việc tính toán doanh thu, lợi nhuận cuối ngày/tháng thực hiện thủ công, mất thời gian và thiếu chính xác.
- Không có dữ liệu để phân tích hành vi mua hàng của khách hàng thân thiết.

## 2.2. Yêu cầu nghiệp vụ (Business Requirements)

| Mã | Yêu cầu nghiệp vụ | Độ ưu tiên |
|---|---|---|
| BR-01 | Hệ thống phải cho phép tạo và xử lý đơn bán hàng tại quầy một cách nhanh chóng, chính xác | Cao |
| BR-02 | Hệ thống phải tự động cập nhật tồn kho ngay khi có giao dịch bán hoặc nhập hàng | Cao |
| BR-03 | Hệ thống phải cảnh báo khi tồn kho của một sản phẩm xuống dưới ngưỡng tối thiểu | Cao |
| BR-04 | Hệ thống phải cảnh báo sản phẩm sắp hết hạn sử dụng (trong vòng X ngày) | Cao |
| BR-05 | Hệ thống phải cung cấp báo cáo doanh thu theo ngày, tuần, tháng | Cao |
| BR-06 | Hệ thống phải hỗ trợ chương trình tích điểm cho khách hàng thân thiết | Trung bình |
| BR-07 | Hệ thống phải phân quyền truy cập theo vai trò người dùng | Cao |
| BR-08 | Hệ thống phải lưu trữ lịch sử giao dịch để tra cứu và đối soát | Trung bình |

## 2.3. Tiêu chí thành công (Success Criteria)

- Giảm thời gian thanh toán trung bình mỗi đơn hàng xuống dưới 60 giây.
- Giảm tỷ lệ thất thoát hàng hóa do hết hạn/kiểm đếm sai xuống dưới 2%/tháng.
- 100% giao dịch bán hàng và nhập hàng được ghi nhận và đối soát tự động trên hệ thống.
- Chị Thành có thể xem báo cáo doanh thu bất kỳ lúc nào trong vòng dưới 5 giây.

---
⬅️ [Trước: Tổng quan dự án](01-project-overview.md) | ➡️ [Tiếp theo: FRD](03-frd.md)
