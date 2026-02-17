Rất tốt.
Mình sẽ viết cho bạn một **mẫu Notion chuyên nghiệp – dùng để học PD1**, không phải kiểu ghi chép chung chung.

Bạn có thể copy toàn bộ cấu trúc này vào Notion.

---

# 📘 Salesforce Data Model – Knowledge Base

---

# 1️⃣ Tổng quan Data Model

## 🔹 Data Model là gì?

Data Model trong Salesforce là cách tổ chức:

* Object (Bảng)
* Field (Cột)
* Record (Dòng)
* Relationship (Quan hệ)

Mục tiêu:

* Lưu trữ dữ liệu đúng cấu trúc
* Kiểm soát quyền truy cập
* Tối ưu automation & performance

---

# 2️⃣ Object Types

## 🔹 Standard Object

Ví dụ:

* Account
* Contact
* Opportunity
* Lead

Đặc điểm:

* Có sẵn
* Không thể xóa
* Có logic business mặc định

---

## 🔹 Custom Object

Ký hiệu: `__c`

Ví dụ:

* Project__c
* Milestone__c

Tạo khi:

* Business requirement không nằm trong Standard Object

---

# 3️⃣ Field Types

## 🔹 Standard Field

Có sẵn (Name, CreatedDate…)

## 🔹 Custom Field

Tự tạo

### Field Type phổ biến

| Field Type      | Khi nào dùng                 |
| --------------- | ---------------------------- |
| Text            | Tên, mô tả                   |
| Number          | Số lượng                     |
| Currency        | Giá tiền                     |
| Picklist        | Trạng thái                   |
| Checkbox        | True/False                   |
| Formula         | Tính toán                    |
| Roll-up Summary | Chỉ dùng trong Master-Detail |

---

# 4️⃣ Relationship Types (Rất Quan Trọng)

---

## 🔹 Lookup Relationship

### Đặc điểm:

* Quan hệ lỏng
* Parent có thể bị xóa (child không bắt buộc xóa)
* Không có Roll-up Summary
* Không ảnh hưởng ownership

### Khi nào dùng?

* Quan hệ tham chiếu
* Không cần phụ thuộc chặt

---

## 🔹 Master-Detail Relationship

### Đặc điểm:

* Quan hệ chặt
* Child phụ thuộc parent
* Xóa parent → xóa child
* Có Roll-up Summary
* Sharing & ownership kế thừa parent

### Khi nào dùng?

* Child không tồn tại độc lập
* Cần tổng hợp dữ liệu

---

## 🔥 So sánh Master-Detail vs Lookup

| Tiêu chí      | Master-Detail | Lookup         |
| ------------- | ------------- | -------------- |
| Ownership     | Theo parent   | Riêng          |
| Roll-up       | Có            | Không          |
| Delete Parent | Xóa child     | Không bắt buộc |
| Required      | Bắt buộc      | Không bắt buộc |

---

# 5️⃣ Schema Design Nguyên Tắc

## 🔹 1. Tránh tạo quá nhiều Object

Hỏi:

* Có thể dùng Record Type không?
* Có thể dùng Picklist không?

---

## 🔹 2. Tối ưu Query

* Tránh nhiều relationship sâu
* Tránh circular reference

---

## 🔹 3. Chuẩn hóa dữ liệu

* Không lưu text trùng lặp
* Dùng lookup thay vì text field

---

# 6️⃣ SOQL & Relationship

## 🔹 Parent → Child Query

```sql
SELECT Name,
       (SELECT Name FROM Tasks__r)
FROM Project__c
```

---

## 🔹 Child → Parent Query

```sql
SELECT Name, Project__r.Name
FROM Task__c
```

---

# 7️⃣ Security & Data Model (Quan hệ quan trọng)

Data Model ảnh hưởng trực tiếp đến:

* Record-Level Security
* Sharing Model
* Role Hierarchy

Master-Detail sẽ kế thừa security từ parent.

---

# 8️⃣ Governor Limits liên quan Data Model

* Tối đa 100 SOQL per transaction
* 50k record query limit
* Query relationship nhiều cấp ảnh hưởng performance

---

# 9️⃣ Sai lầm thường gặp (Exam Trap)

* Nhầm Master-Detail với Lookup
* Không hiểu ownership thay đổi thế nào
* Không biết Roll-up chỉ dùng Master-Detail
* Không tính tới security khi thiết kế

---

# 🔟 Mini Case Study (Bạn phải tự làm)

Thiết kế:

Project__c
Task__c
TimeLog__c

Yêu cầu:

* Project có nhiều Task
* Task có nhiều TimeLog
* Tổng giờ của Task hiển thị ở Project

Hỏi:

* Quan hệ nào dùng Master-Detail?
* Quan hệ nào dùng Lookup?
* Có cần Roll-up Summary?

---

# 📊 Cuối Trang – Self Check

Trả lời không nhìn tài liệu:

1. Master-Detail ảnh hưởng security thế nào?
2. Khi nào không nên dùng Master-Detail?
3. Roll-up Summary hoạt động ra sao?
4. SOQL parent-child viết như thế nào?

Nếu không trả lời trôi chảy → chưa hiểu sâu.

---

Nếu bạn muốn, mình có thể:

* Viết tiếp mẫu Notion cho Security Model
* Hoặc viết template chuẩn để bạn dùng suốt 5 tháng
* Hoặc làm version nâng cao có phần “Interview explanation mode”

Bạn muốn nâng cấp theo hướng nào?
