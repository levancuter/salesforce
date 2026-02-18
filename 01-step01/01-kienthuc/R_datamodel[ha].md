## 1. Data Model là gì?

Data Model (mô hình dữ liệu) là cách tổ chức, mô tả và quản lý dữ liệu để máy tính hiểu và xử lý được.
Nói đơn giản: Data Model giống như bản thiết kế cho dữ liệu trong hệ thống hoặc ứng dụng.
Nó trả lời các câu hỏi:
・Dữ liệu được lưu như thế nào?
・Các bảng/đối tượng quan hệ với nhau ra sao?
・Quy tắc nào kiểm soát dữ liệu?

## 2. Các loại mô hình dữ liệu phổ biến

 có 3 loại mô hình dữ liệu phổ biến:

 ## 2.1. Conceptual Data Model(Mô hình dữ liệu khái niệm)
 >Mức trừu tượng cao nhất
 >Tập chung vào cái gì chứ không phải lưu thế nào
 >Dành cho business và kiến trúc sư dữ liệu

 Ví dụ:
 >Khách hàng---Đơn hàng---Sản phẩm
 >Chỉ thể hiện các thực thể và quan hệ
 *Công cụ thể hiện:ERD*(Entity-Relationship Diagram)

 ## 2.2. Logical Dât Model(Mô hình dữ liệu logic)
> Chi tiết hơn conceptual
> Định nghĩa:
 -Thuộc tính của entity
 -Primary key, foreign key
 -Cardinality (1-1, 1-n, n-n)
> Không phụ thuộc vào công nghệ(SQL hay NoSQL)
