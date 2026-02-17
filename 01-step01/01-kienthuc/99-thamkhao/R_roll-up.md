Dưới đây là **giải thích đơn giản – dễ hiểu – chính xác** về **Roll-up Summary** trong Salesforce, dựa trên tài liệu chính thức.

***

# ⭐ Roll-up Summary là gì?

**Roll-up Summary** là *một loại trường (field) trên Salesforce* dùng để **tự động tính toán và tổng hợp dữ liệu** từ các bản ghi con (child records) rồi hiển thị kết quả lên bản ghi cha (parent record).  
→ Nó chỉ hoạt động khi hai object có **mối quan hệ Master–Detail**.

**Các phép tính hỗ trợ gồm:**

*   **SUM** – cộng tổng giá trị số
*   **MIN** – lấy giá trị nhỏ nhất
*   **MAX** – lấy giá trị lớn nhất
*   **COUNT** – đếm số lượng bản ghi con

📌 Theo định nghĩa chính thức:  
Roll-up Summary là một trường “tính toán dữ liệu từ các bản ghi detail (child) và hiển thị lên bản ghi master (parent)” trong quan hệ master-detail. [\[sfdcdevelopers.com\]](https://sfdcdevelopers.com/2025/10/08/what-is-a-roll-up-summary-field-in-salesforce/)

***

# ⭐ Ví dụ dễ hiểu

Bạn muốn hiển thị **tổng doanh số (Amount)** của tất cả **Opportunity (Closed Won)** trên **Account**.  
→ Tạo Roll-up Summary trên object **Account**:  
**Total\_Closed\_Won\_Opportunity\_Amount = SUM(Opportunity.Amount WHERE Stage = 'Closed Won')**    [\[sfdcdevelopers.com\]](https://sfdcdevelopers.com/2025/10/08/what-is-a-roll-up-summary-field-in-salesforce/)

***

# ⭐ Roll-up Summary hoạt động như thế nào?

*   Salesforce **tự động cập nhật** giá trị Roll-up Summary khi bản ghi child được tạo, sửa hoặc xóa.  
    citeturn2search10
*   Bạn có thể thêm **filter conditions** để chỉ tính những bản ghi child thỏa điều kiện.    [\[sfdcdevelopers.com\]](https://sfdcdevelopers.com/2025/10/08/what-is-a-roll-up-summary-field-in-salesforce/)

***

# ⭐ Hạn chế của Roll-up Summary

Roll-up Summary **chỉ sử dụng được khi**:  
✔ Quan hệ là **Master–Detail**  
❌ **Không dùng được** cho Lookup Relationship (trừ khi dùng Apex/Flow hoặc DLRS).

Nguồn: Roll-up Summary fields chỉ hoạt động trên master-detail relationships. [\[sfdcdevelopers.com\]](https://sfdcdevelopers.com/2025/10/08/what-is-a-roll-up-summary-field-in-salesforce/)

***

# ⭐ Nếu object chỉ là Lookup thì làm sao?

Nếu object không phải Master–Detail, bạn có thể dùng:

*   **Apex Trigger**
*   **Record-Triggered Flow**
*   **DLRS (Declarative Lookup Rollup Summaries)** — một công cụ trên AppExchange  
    DLRS cho phép bạn tạo roll-up giữa Lookup relationships mà không cần code.    [\[salesforceben.com\]](https://www.salesforceben.com/guide-to-salesforce-dlrs-declarative-lookup-roll-up-summaries/), [\[appexchang...sforce.com\]](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N3000000B45gWEAR)

***

# ⭐ Tóm tắt nhanh

| Nội dung         | Mô tả                                                 |
| ---------------- | ----------------------------------------------------- |
| Roll-up Summary  | Trường tính toán dữ liệu từ record con lên record cha |
| Quan hệ yêu cầu  | Master–Detail                                         |
| Phép tính        | SUM, MIN, MAX, COUNT                                  |
| Tự động cập nhật | Có                                                    |
| Không hỗ trợ     | Lookup relationship (nếu không dùng Apex/Flow/DLRS)   |

***

Nếu bạn muốn, mình có thể giải thích thêm:  
✅ Sự khác nhau giữa **Master–Detail và Lookup**  
✅ Khi nào nên dùng Apex vs Flow vs DLRS  
✅ Ví dụ nâng cao về Roll-up Summary trong thực tế

Bạn muốn tìm hiểu phần nào tiếp theo?
