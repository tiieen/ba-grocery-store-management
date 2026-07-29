# 🛒 GSMS – Grocery Store Management System

### Hệ thống Quản lý Bán hàng – Cửa hàng Tạp hóa Chị Thành (Ms. Thanh's Grocery Store)

> Dự án cá nhân — Business Analysis Portfolio
> Tác giả: Võ Huỳnh Thủy Tiên

> Vai trò: Business Analyst
> Phiên bản: 1.0 — Tháng 7/2026

\---

## 📌 Giới thiệu

Đây là bộ tài liệu phân tích nghiệp vụ (Business Analysis) hoàn chỉnh cho một dự án giả lập:
xây dựng hệ thống quản lý bán hàng cho **Cửa hàng Tạp hóa Chị Thành (Ms. Thanh)** — một cửa hàng
tạp hóa quy mô nhỏ đang gặp khó khăn trong việc quản lý bán hàng, tồn kho và nhập hàng bằng
phương pháp thủ công (sổ sách, Excel).

Dự án được thực hiện với mục đích luyện tập và làm portfolio cá nhân khi ứng tuyển vị trí
**thực tập sinh Business Analyst**, mô phỏng đầy đủ quy trình phân tích nghiệp vụ từ thu thập
yêu cầu đến đặc tả chức năng, use case, quy trình nghiệp vụ và mô hình dữ liệu.

## 🎯 Bối cảnh dự án

Chị Thành hiện đang quản lý cửa hàng tạp hóa của mình bằng sổ sách và Excel. Việc này gây ra:

* Khó kiểm soát chính xác tồn kho theo thời gian thực
* Không có cảnh báo khi hàng sắp hết hoặc sắp hết hạn sử dụng
* Mất nhiều thời gian tính doanh thu cuối ngày
* Không biết mặt hàng nào bán chạy để lên kế hoạch nhập hàng

→ Chị Thành mong muốn có một hệ thống phần mềm quản lý bán hàng (POS + quản lý kho) để
số hóa toàn bộ quy trình vận hành cửa hàng.

## 📂 Cấu trúc tài liệu

|Tài liệu|Nội dung|
|-|-|
|[01 – Tổng quan dự án](01-project-overview.md)|Bối cảnh, mục tiêu, phạm vi, stakeholder|
|[02 – BRD (Business Requirement Document)](02-brd.md)|Yêu cầu nghiệp vụ, tiêu chí thành công|
|[03 – FRD (Functional Requirement Document)](03-frd.md)|Yêu cầu chức năng \& phi chức năng chi tiết|
|[04 – Use Case Specifications](04-use-cases.md)|Danh sách actor, use case diagram, đặc tả chi tiết|
|[05 – Business Process Flow](05-process-flow.md)|Lưu đồ quy trình Bán hàng \& Nhập hàng (Mermaid/BPMN-style)|
|[06 – ERD (Entity Relationship Diagram)](06-erd.md)|Mô hình dữ liệu sơ bộ|
|[07 – Wireframes](07-wireframes.md)|Mô tả giao diện các màn hình chính|

## 🧰 Công cụ sử dụng (gợi ý khi mở rộng)

* **Draw.io / Lucidchart** – vẽ lại Use Case Diagram, BPMN dạng hình ảnh trực quan
* **Figma** – dựng wireframe/mockup thực tế từ mô tả trong `07-wireframes.md`
* **Mermaid** (đã dùng trong repo này) – biểu đồ dạng code, render trực tiếp trên GitHub

## 🏷️ Phạm vi (Scope)

**Trong phạm vi:** Bán hàng tại quầy (POS), quản lý sản phẩm \& tồn kho, quản lý nhập hàng,
quản lý khách hàng thân thiết (tích điểm), báo cáo \& thống kê, phân quyền người dùng.

**Ngoài phạm vi (giai đoạn 1):** Bán hàng đa kênh online, tích hợp cổng thanh toán bên thứ ba,
quản lý chuỗi cung ứng nhiều chi nhánh.

## 👤 Stakeholders chính

* **Chị Thành (Owner/Admin)** — chủ cửa hàng, ra quyết định kinh doanh
* **Cashier** — nhân viên bán hàng
* **Inventory Staff** — nhân viên kho
* **Customer** — khách hàng của cửa hàng
* **Supplier** — nhà cung cấp hàng hóa

\---

*Đây là dự án học tập/portfolio cá nhân, không phải sản phẩm thương mại thực tế.*

