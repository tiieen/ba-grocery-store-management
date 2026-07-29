# 7. Wireframes (Mô tả giao diện)

> Đây là mô tả cấu trúc cho từng màn hình chính. Khuyến nghị dựng lại wireframe/mockup thực tế
> trên **Figma** để hoàn thiện portfolio với hình ảnh trực quan.

## 7.1. Màn hình Bán hàng (POS Screen)

```
┌──────────────────────────────────────────────────────────┐
│  🔍 Tìm sản phẩm / Quét mã vạch                            │
├─────────────────────────────────┬──────────────────────────┤
│  Giỏ hàng                       │  Khách hàng: [___________]│
│  ┌─────────────────────────┐    │  Mã KM:      [___________]│
│  │ Tên SP | SL | Đơn giá |TT│    │                          │
│  │ Mì gói |  2 | 5.000  |10k│    │  Tổng tiền:  120.000đ    │
│  │ Sữa    |  1 | 30.000 |30k│    │  Giảm giá:    10.000đ    │
│  │ ...                      │    │  Thành tiền: 110.000đ    │
│  └─────────────────────────┘    │                          │
│                                  │  [ 💳 THANH TOÁN ]        │
└─────────────────────────────────┴──────────────────────────┘
```

Ghi chú:
- Khu vực tìm kiếm sản phẩm ở trên cùng, hỗ trợ quét mã vạch.
- Danh sách giỏ hàng ở giữa/trái, dễ chỉnh sửa số lượng.
- Khu vực tổng tiền, mã khuyến mãi, thông tin thành viên ở bên phải.
- Nút "Thanh toán" nổi bật, dễ thao tác bằng một chạm.

## 7.2. Màn hình Quản lý sản phẩm & Tồn kho

```
┌──────────────────────────────────────────────────────────┐
│  Bộ lọc: [Danh mục ▾]  [Trạng thái tồn kho ▾]   [+ Thêm SP]│
├──────────────────────────────────────────────────────────┤
│ Mã SP | Tên SP  | Danh mục | Tồn kho | Hạn SD   | Trạng thái│
│ SP001 | Mì gói  | Thực phẩm|   50    | 12/2026  | 🟢 Bình thường│
│ SP002 | Sữa tươi| Đồ uống  |    3    | 08/2026  | 🔴 Sắp hết  │
│ SP003 | Bánh mì | Thực phẩm|   20    | 30/07/2026| 🟡 Sắp hết hạn│
└──────────────────────────────────────────────────────────┘
```

Ghi chú:
- Bảng danh sách sản phẩm với cột trạng thái được tô màu cảnh báo (đỏ/vàng/xanh).
- Bộ lọc theo danh mục và trạng thái tồn kho.
- Nút thêm/sửa/xóa sản phẩm rõ ràng.

## 7.3. Màn hình Nhập hàng

```
┌──────────────────────────────────────────────────────────┐
│ Nhà cung cấp: [Chọn NCC ▾]        Ngày nhập: [__/__/____]  │
├──────────────────────────────────────────────────────────┤
│ Sản phẩm | Số lượng | Đơn giá nhập | Hạn sử dụng | Thành tiền│
│ [+ Thêm dòng sản phẩm]                                     │
├──────────────────────────────────────────────────────────┤
│                                    Tổng giá trị: [________]│
│                              [ Lưu nháp ]  [ ✅ Xác nhận ]  │
└──────────────────────────────────────────────────────────┘
```

## 7.4. Màn hình Báo cáo (Dashboard)

```
┌──────────────────────────────────────────────────────────┐
│  📊 Doanh thu theo thời gian     [Ngày ▾][Tuần][Tháng][Tùy chỉnh]│
│  ┌────────────────────────────────────────────────────┐  │
│  │        📈 Biểu đồ doanh thu (line/bar chart)         │  │
│  └────────────────────────────────────────────────────┘  │
├───────────────────────────────┬────────────────────────────┤
│ ⚠️ Cảnh báo tồn kho & hết hạn  │ 🏆 Top sản phẩm bán chạy    │
│ - Sữa tươi: sắp hết hàng      │ 1. Mì gói                   │
│ - Bánh mì: sắp hết hạn        │ 2. Nước ngọt                │
└───────────────────────────────┴────────────────────────────┘
```

---
⬅️ [Trước: ERD](06-erd.md) | ➡️ [Về README](../README.md)
