# 🎯 **MỤC TIÊU KHÓA HỌC PD1**

PD1 kiểm tra kiến thức về:

*   Apex cơ bản → trung cấp
*   SOQL, DML
*   Triggers
*   Governor Limits
*   LWC cơ bản (kiến thức foundational)
*   Security trong code
*   Testing (unit tests)
*   Asynchronous Apex

***

# 🟩 **PHẦN 1 – Nền tảng Salesforce (1–2 tuần)**

*Giúp bạn có đủ kiến thức nền trước khi vào Apex.*

### ✔ Học các khái niệm core:

*   Objects, Fields
*   Relationship (Lookup, Master-Detail)
*   Validation Rules
*   Permission, Profile, Role
*   Process Automation: Flow (cơ bản)

### ✔ Tài liệu:

*   Trailhead: *“Prepare for Your Salesforce Platform Developer I Credential”*

***

# 🟧 **PHẦN 2 – Apex căn bản (2–3 tuần)**

### ✔ Nội dung cần nắm:

*   Cú pháp Apex (giống Java)
*   Variables, Data Types
*   Collections (List, Set, Map)
*   SObject, DML (Insert, Update, Delete, Undelete)
*   SOQL cơ bản
*   SOSL cơ bản

### ✔ Thực hành mẫu:

```apex
List<Account> accs = [SELECT Id, Name FROM Account LIMIT 10];
for(Account a : accs){
    a.Name = a.Name + ' - updated';
}
update accs;
```

***

# 🟨 **PHẦN 3 – Triggers & Governor Limits (2–3 tuần)**

### ✔ Kiến thức trọng tâm:

*   Trigger context (before/after, insert/update/delete/undelete)
*   Best practices: **One trigger per object**
*   Bulkify code
*   Avoid SOQL/DML inside loops
*   Governor limits (SOQL limit, DML limit, heap size…)

### ✔ Ví dụ mẫu:

```apex
trigger AccountTrigger on Account (before insert) {
    for(Account a : Trigger.new){
        if(a.Name == ''){
            a.Name = 'Default Name';
        }
    }
}
```

***

# 🟦 **PHẦN 4 – SOQL nâng cao (1–2 tuần)**

*   Relationship queries
*   Aggregate SOQL
*   Subquery (Parent-to-Child)
*   Semi-join, Anti-join

***

# 🟪 **PHẦN 5 – LWC cơ bản (1–2 tuần)**

PD1 chỉ hỏi LWC ở mức:

*   Component structure
*   Communication: @api, @track
*   Lightning Data Service
*   Calling Apex from LWC (@wire, imperative call)

Không cần build UI phức tạp.

***

# 🟥 **PHẦN 6 – Asynchronous Apex (1–2 tuần)**

PD1 hỏi khá nhiều.

### ✔ Cần nắm:

*   **Future methods**
*   **Queueable**
*   **Scheduled Apex**
*   **Batch Apex (cơ bản)**

***

# 🟫 **PHẦN 7 – Testing (1–2 tuần)**

RẤT quan trọng (chiếm 12–20% bài thi)

### ✔ Kiến thức chính:

*   @isTest
*   Test Data
*   Test.startTest(), Test.stopTest()
*   Test về async Apex
*   Test trigger bulk

***

# 🟩 **PHẦN 8 – Giải bài thi mẫu (2–3 tuần)**

*   Làm mock exam 200–300 câu
*   Ghi lại câu sai → ôn từng topic
*   PD1 pass: **65%** (60 câu trắc nghiệm)

***

# 📘 **LỘ TRÌNH HỌC TÓM TẮT (theo thời gian)**

## ⏱ **Lộ trình nhanh – 1.5 đến 2 tháng**

| Thời gian | Nội dung                                   |
| --------- | ------------------------------------------ |
| Tuần 1    | Salesforce fundamentals + SOQL căn bản     |
| Tuần 2–3  | Apex cơ bản + Collections + DML            |
| Tuần 4    | Trigger + Best practices + Governor limits |
| Tuần 5    | SOQL nâng cao + LWC cơ bản                 |
| Tuần 6    | Async Apex + Testing                       |
| Tuần 7–8  | Mock exam + Ôn tập                         |

***

# 🛠 **Tài liệu học tốt nhất**

### 📙 1. **Trailhead**

> Search: *PD1 Trailmix – “Prepare for Platform Developer I”*

### 📘 2. Apex Developer Guide (official)

→ Rất chuẩn cho PD1

### 🎥 3. YouTube: SFDCFacts, Apex Hours

→ Học Apex cực dễ hiểu

### 📝 4. Mock exams

*   Focus on Force (tốt nhất)
*   Quizlet (free – nhưng nên kiểm tra lại)

***

# 🎯 Bạn muốn mình tạo:

✔ Lộ trình học **tùy chỉnh theo thời gian của bạn (1 tháng / 3 tháng)**
✔ Checklist từng ngày
✔ Bộ 200 câu PD1 mock exam (câu giải thích)
✔ Gợi ý bài tập thực hành Apex + Trigger để luyện phỏng vấn/dev

Bạn muốn học PD1 theo **tốc độ nhanh**, **chuẩn bài thi**, hay **vừa học vừa làm dự án**?
