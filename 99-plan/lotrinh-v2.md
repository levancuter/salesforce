
Vì bạn **không thi ADM 201**, nên lộ trình sẽ phải:

* Bù phần nền tảng data model & security mà Admin thường học
* Tập trung sâu vào Apex, LWC, automation
* Có hệ thống đo lường rõ ràng

Chứng chỉ bạn hướng tới:

👉 Salesforce Platform Developer I

---

# I. Tổng quan chiến lược (Quan trọng)

PD1 kiểm tra 4 nhóm lớn:

1. Fundamentals (Data Model, Security, Logic)
2. Process Automation & Logic
3. User Interface
4. Testing, Debugging, Deployment

Sai lầm lớn nhất khi không học ADM trước:

* Không hiểu rõ Sharing model
* Không hiểu OWD / Role / Profile
* Không nắm chắc Data Model

👉 Vì vậy tháng đầu tiên sẽ xây nền tảng platform.

---

# II. Tổng thời gian: 20 tuần (5 tháng)

Mỗi tuần = 1 chu kỳ R-P-D-C
Mỗi tháng = 1 mục tiêu năng lực

---

# III. Thiết kế theo 3 TẦNG + R-P-D-C

---

# 🔹 Giai đoạn 1 (Tuần 1–4)

## NỀN TẢNG PLATFORM (Admin-level core nhưng dành cho Developer)

---

## 🎯 Mục tiêu tháng 1

* Hiểu Data Model
* Hiểu Security Model
* Thành thạo SOQL cơ bản
* Nắm được Automation nền tảng

---

## 🔹 Tầng 1 – Kiến thức (Input)

Tài liệu chính thống:

1. Salesforce Trailhead:

   * Platform Developer I Trailmix (Official)
   * Data Modeling
   * Security Specialist
   * Apex Basics & Database

2. Tài liệu chính thức:

   * Salesforce Developer Guide
   * Apex Developer Guide

Trang chính:
Salesforce

---

## 🔹 Tầng 2 – Thực hành (Output)

Tạo 1 Dev Org riêng.

Thực hành bắt buộc:

* Tạo Custom Object (Project, Task)
* Thiết kế:

  * Lookup
  * Master-Detail
  * Roll-up Summary
* Cấu hình:

  * OWD
  * Role Hierarchy
  * Profile
* Viết SOQL:

  * Parent-child query
  * Aggregate query

👉 Viết lại kiến thức mỗi tuần bằng Notion:

* Security model hoạt động thế nào?
* Sharing Rule chạy khi nào?

Giải thích lại cho người khác = bạn hiểu thật.

---

## 🔹 Tầng 3 – Đo lường

Cuối tháng 1:

* Làm 100 câu practice về Data & Security
* Tự vẽ lại Data model không nhìn tài liệu
* Viết được 10 câu SOQL không tra cứu

Nếu không đạt → chưa sang tháng 2.

---

# 🔹 Giai đoạn 2 (Tuần 5–10)

## APEX CORE + GOVERNOR LIMITS

---

## 🎯 Mục tiêu

* Thành thạo Apex syntax
* Hiểu Governor Limits
* Bulkification
* Trigger framework cơ bản

---

## 🔹 Tầng 1 – Input

Trailhead:

* Apex Triggers
* Asynchronous Apex
* Apex Testing

Đọc:

* Apex Best Practices
* Governor Limits section

---

## 🔹 Tầng 2 – Output

Bắt buộc làm:

1. Viết:

   * Before Insert Trigger
   * After Update Trigger
   * Bulkified Trigger

2. Viết:

   * Batch Apex
   * Future method
   * Queueable

3. Unit Test:

   * 75% coverage
   * TestSetup method

4. Làm 1 mini project:

Ví dụ:

* Khi Opportunity = Closed Won
  → Tạo Project
  → Gửi Email
  → Log lịch sử

---

## 🔹 Tầng 3 – Đo lường

* Viết trigger không bị SOQL in loop
* Tự giải thích:

  * Difference between before & after
  * When to use Batch vs Queueable
* Làm 150 câu practice Apex

Nếu điểm < 75% → học lại.

---

# 🔹 Giai đoạn 3 (Tuần 11–15)

## UI + LWC + Automation

---

## 🎯 Mục tiêu

* Biết khi nào dùng:

  * Flow
  * Process Builder
  * Apex
* Biết LWC cơ bản

---

## 🔹 Tầng 1 – Input

Trailhead:

* Lightning Web Components Basics
* Flow Builder
* Platform App Builder fundamentals

---

## 🔹 Tầng 2 – Output

Bắt buộc làm:

1. Tạo:

   * 1 LWC component gọi Apex
   * 1 Flow auto create record
   * 1 Screen Flow

2. So sánh:

   * Flow vs Apex (viết bảng phân tích)

3. Tạo 1 App hoàn chỉnh:

   * Custom object
   * LWC
   * Automation
   * Security

---

## 🔹 Tầng 3 – Đo lường

* Hiểu rõ Order of Execution
* Làm 200 câu practice mixed
* Tự mock 1 đề 60 câu trong 105 phút

---

# 🔹 Giai đoạn 4 (Tuần 16–20)

## TESTING – DEBUG – DEPLOYMENT – ÔN TẬP

---

## 🎯 Mục tiêu

* Nắm vững:

  * Test class
  * Debug log
  * Change Set
  * Metadata API basics

---

## 🔹 Tầng 1 – Input

Đọc:

* Testing Best Practices
* Deployment Overview

---

## 🔹 Tầng 2 – Output

Làm:

* Viết test cho toàn bộ mini project
* Deploy qua Change Set
* Fix lỗi coverage
* Phân tích Debug Log

---

## 🔹 Tầng 3 – Đo lường

Tuần 18:

* Mock test 1

Tuần 19:

* Mock test 2

Tuần 20:

* Mock test 3

Điểm ổn định ≥ 80% mới đăng ký thi.

---

# IV. Lịch học mẫu mỗi tuần (R-P-D-C)

## Thứ 2–3: R (Research)

Đọc Trailhead + Doc

## Thứ 4–5: P (Practice)

Code + cấu hình

## Thứ 6: D (Document)

Viết lại kiến thức

## Chủ nhật: C (Check)

* Làm practice test
* Review sai ở đâu

---

# V. Thời lượng đề xuất

Mỗi tuần:

* 10–15 giờ
* Nếu < 8 giờ → kéo dài thành 6 tháng

---

# VI. Cảnh báo thực tế (quan trọng)

PD1 không phải chứng chỉ dễ nếu:

* Không làm project thật
* Chỉ học lý thuyết
* Không bulkify

Nếu bạn làm đúng lộ trình trên, xác suất pass > 80%.

---

Nếu bạn muốn, mình có thể:

* Thiết kế cho bạn một roadmap dạng bảng tuần chi tiết 20 tuần
* Hoặc thiết kế mini project thực tế sát đề thi
* Hoặc tạo checklist đánh giá năng lực từng giai đoạn

Bạn muốn mình đi sâu theo hướng nào tiếp?
