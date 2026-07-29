# 6. Entity Relationship Diagram (ERD)

## 6.1. Sơ đồ quan hệ thực thể

```mermaid
erDiagram
    CATEGORY ||--o{ PRODUCT : "phân loại"
    PRODUCT ||--o{ ORDER_DETAIL : "xuất hiện trong"
    PRODUCT ||--o{ IMPORT_DETAIL : "xuất hiện trong"
    ORDER ||--|{ ORDER_DETAIL : "gồm"
    ORDER }o--|| CUSTOMER : "thuộc về"
    ORDER }o--|| USER : "được tạo bởi"
    IMPORT_RECEIPT ||--|{ IMPORT_DETAIL : "gồm"
    IMPORT_RECEIPT }o--|| SUPPLIER : "từ"
    IMPORT_RECEIPT }o--|| USER : "được tạo bởi"
    ORDER }o--|| PROMOTION : "áp dụng (tùy chọn)"

    CATEGORY {
        int CategoryID PK
        string CategoryName
    }
    PRODUCT {
        int ProductID PK
        string Name
        int CategoryID FK
        string Unit
        decimal SellPrice
        decimal CostPrice
        date ExpiryDate
        int MinStockLevel
        int CurrentStock
    }
    ORDER {
        int OrderID PK
        int UserID FK
        int CustomerID FK
        int PromotionID FK
        datetime OrderDate
        decimal TotalAmount
        string PaymentMethod
    }
    ORDER_DETAIL {
        int OrderDetailID PK
        int OrderID FK
        int ProductID FK
        int Quantity
        decimal UnitPrice
    }
    IMPORT_RECEIPT {
        int ImportID PK
        int SupplierID FK
        int UserID FK
        datetime ImportDate
        decimal TotalValue
    }
    IMPORT_DETAIL {
        int ImportDetailID PK
        int ImportID FK
        int ProductID FK
        int Quantity
        decimal ImportPrice
    }
    SUPPLIER {
        int SupplierID PK
        string Name
        string ContactInfo
    }
    CUSTOMER {
        int CustomerID PK
        string Name
        string Phone
        int LoyaltyPoints
    }
    USER {
        int UserID PK
        string Username
        string PasswordHash
        string Role
    }
    PROMOTION {
        int PromotionID PK
        string Name
        string DiscountType
        decimal DiscountValue
        date StartDate
        date EndDate
    }
```

## 6.2. Mô tả thực thể

| Thực thể | Thuộc tính chính | Quan hệ |
|---|---|---|
| **Product** | ProductID, Name, Category, Unit, SellPrice, CostPrice, ExpiryDate, MinStockLevel, CurrentStock | 1 Product thuộc 1 Category; xuất hiện trong nhiều OrderDetail và ImportDetail |
| **Category** | CategoryID, CategoryName | 1 Category có nhiều Product |
| **Order** | OrderID, UserID, CustomerID, OrderDate, TotalAmount, PaymentMethod | Thuộc 1 User (Cashier), có thể thuộc 1 Customer; có nhiều OrderDetail |
| **OrderDetail** | OrderDetailID, OrderID, ProductID, Quantity, UnitPrice | Thuộc 1 Order và 1 Product |
| **ImportReceipt** | ImportID, SupplierID, UserID, ImportDate, TotalValue | Thuộc 1 Supplier và 1 User (Inventory Staff); có nhiều ImportDetail |
| **ImportDetail** | ImportDetailID, ImportID, ProductID, Quantity, ImportPrice | Thuộc 1 ImportReceipt và 1 Product |
| **Supplier** | SupplierID, Name, ContactInfo | 1 Supplier có nhiều ImportReceipt |
| **Customer** | CustomerID, Name, Phone, LoyaltyPoints | 1 Customer có nhiều Order |
| **User** | UserID, Username, PasswordHash, Role (Owner/Cashier/InventoryStaff) | 1 User có nhiều Order hoặc ImportReceipt tùy vai trò |
| **Promotion** | PromotionID, Name, DiscountType, DiscountValue, StartDate, EndDate | Có thể áp dụng cho nhiều Order |

---
⬅️ [Trước: Business Process Flow](05-process-flow.md) | ➡️ [Tiếp theo: Wireframes](07-wireframes.md)
