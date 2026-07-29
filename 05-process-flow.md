# 5. Business Process Flow

## 5.1. Quy trình Bán hàng (Sales Process)

```mermaid
flowchart TD
    Start(["Bắt đầu: Khách hàng mang sản phẩm đến quầy"]) --> Scan["Cashier quét mã vạch / tìm sản phẩm"]
    Scan --> Check{"Đủ tồn kho?"}
    Check -- Không --> Reject["Thông báo hết hàng"] --> End1(["Kết thúc"])
    Check -- Có --> Add["Thêm vào giỏ hàng"]
    Add --> IsMember{"Khách hàng là thành viên?"}
    IsMember -- Có --> ApplyPoint["Nhập mã thành viên"]
    IsMember -- Không --> Promo
    ApplyPoint --> Promo["Áp dụng khuyến mãi (nếu có)"]
    Promo --> Total["Hệ thống tính tổng tiền"]
    Total --> Pay["Khách hàng thanh toán (tiền mặt / chuyển khoản)"]
    Pay --> Update["Trừ tồn kho, cộng điểm thành viên, in hóa đơn"]
    Update --> End2(["Kết thúc giao dịch"])
```

> **Ghi chú trình bày:** khi làm portfolio, nên vẽ lại quy trình này theo đúng chuẩn ký hiệu
> BPMN (Start Event tròn, Task hình chữ nhật bo góc, Gateway hình thoi, End Event tròn viền đậm)
> bằng draw.io hoặc Lucidchart để đúng chuẩn nghiệp vụ hơn.

## 5.2. Quy trình Nhập hàng (Procurement Process)

```mermaid
flowchart TD
    Start(["Bắt đầu: Nhận hàng từ nhà cung cấp"]) --> Receive["Inventory Staff nhận hàng kèm hóa đơn/phiếu giao hàng"]
    Receive --> Compare["Đối chiếu số lượng thực nhận với phiếu giao hàng"]
    Compare --> Diff{"Có chênh lệch?"}
    Diff -- Có --> Report["Ghi chú chênh lệch, báo cáo Chị Thành"]
    Diff -- Không --> Create
    Report --> Create["Tạo phiếu nhập kho trên hệ thống"]
    Create --> Confirm["Inventory Staff xác nhận phiếu nhập"]
    Confirm --> UpdateStock["Hệ thống tự động cộng tồn kho"]
    UpdateStock --> End(["Kết thúc quy trình nhập hàng"])
```

## 5.3. Quy trình Cảnh báo tự động (Alert Process)

```mermaid
flowchart TD
    Trigger(["Trigger: định kỳ hoặc sau mỗi giao dịch"]) --> CheckStock{"Tồn kho ≤ ngưỡng tối thiểu?"}
    CheckStock -- Có --> AlertLow["Tạo cảnh báo 'Sắp hết hàng'"]
    CheckStock -- Không --> CheckExpiry{"Còn ≤ X ngày hết hạn?"}
    AlertLow --> CheckExpiry
    CheckExpiry -- Có --> AlertExp["Tạo cảnh báo 'Sắp hết hạn'"]
    CheckExpiry -- Không --> Done(["Không có cảnh báo mới"])
    AlertExp --> Show["Hiển thị trên Dashboard cho Chị Thành / Inventory Staff"]
    Show --> Done2(["Kết thúc"])
```

---
⬅️ [Trước: Use Cases](04-use-cases.md) | ➡️ [Tiếp theo: ERD](06-erd.md)
