---
title: "Biến, Kiểu Dữ Liệu, Ép Kiểu, và Ghi Chú trong JavaScript"
date: 2024-12-25T10:00:00+06:00
description: "Hướng dẫn chi tiết về cách sử dụng biến, kiểu dữ liệu, ép kiểu, và ghi chú trong JavaScript"
menu:
  sidebar:
    name: Biến và Kiểu Dữ Liệu
    identifier: VariablesDataTypes
    weight: 20
tags: ["Beginner"]
categories: ["JavaScript"]
math: true
---

# Tìm Hiểu Về Biến, Kiểu Dữ Liệu, Ép Kiểu, và Ghi Chú Trong JavaScript

JavaScript là một ngôn ngữ linh hoạt cho phép bạn làm việc với nhiều kiểu dữ liệu và cách quản lý biến. Bài viết này sẽ hướng dẫn bạn cách khai báo biến, hiểu các kiểu dữ liệu, thực hiện ép kiểu, và sử dụng ghi chú hiệu quả.

---

## 2.0. Section 1 – Variables

### Biến (Variables)

Biến trong JavaScript được sử dụng để lưu trữ giá trị. Bạn có thể khai báo biến bằng các từ khóa `var`, `let`, hoặc `const`.

#### Ví dụ:
```javascript
let age = 25; // Khai báo biến có thể thay đổi giá trị
const name = "Alice"; // Khai báo biến không thể thay đổi giá trị
var isStudent = true; // Khai báo biến theo cách cũ
```

---

## 2.1. Section 2 – Data types and type casting – Part 1

### Kiểu Dữ Liệu (Data Types)

JavaScript hỗ trợ nhiều kiểu dữ liệu cơ bản:
- **String**: Chuỗi ký tự.
- **Number**: Số.
- **Boolean**: Giá trị đúng/sai.
- **Undefined**: Biến chưa được gán giá trị.
- **Null**: Giá trị rỗng.

#### Ví dụ:
```javascript
let text = "Hello, World!"; // String
let number = 42; // Number
let isActive = false; // Boolean
let notAssigned; // Undefined
let emptyValue = null; // Null
```

### Ép Kiểu (Type Casting)

Ép kiểu cho phép chuyển đổi một kiểu dữ liệu sang kiểu khác.

#### Ví dụ:
```javascript
let num = "123";
let convertedNum = Number(num); // Ép kiểu String thành Number
console.log(convertedNum); // 123

let boolValue = Boolean(0); // Ép kiểu Number thành Boolean
console.log(boolValue); // false
```

---

## 2.2. Section 3 – Data types and type casting – Part 2

### Chuyển Đổi Tự Động (Implicit Casting)

JavaScript có thể tự động chuyển đổi kiểu dữ liệu trong một số trường hợp.

#### Ví dụ:
```javascript
let result = "5" + 2; // Chuyển đổi Number thành String
console.log(result); // "52"

let subtraction = "10" - 2; // Chuyển đổi String thành Number
console.log(subtraction); // 8
```

### So Sánh Chặt Chẽ và Lỏng Lẻo (Strict vs. Loose Equality)

- **So sánh lỏng lẻo (`==`)** cho phép chuyển đổi kiểu dữ liệu.
- **So sánh chặt chẽ (`===`)** không cho phép chuyển đổi kiểu dữ liệu.

#### Ví dụ:
```javascript
console.log(5 == "5"); // true
console.log(5 === "5"); // false
```

---

## 2.3. Section 4 – Comments

### Ghi Chú (Comments)

Ghi chú trong JavaScript giúp bạn giải thích mã hoặc vô hiệu hóa mã mà không cần xóa.

#### Loại Ghi Chú:
- **Ghi chú một dòng:** Sử dụng `//`.
- **Ghi chú nhiều dòng:** Sử dụng `/* */`.

#### Ví dụ:
```javascript
// Đây là ghi chú một dòng

/*
  Đây là ghi chú nhiều dòng
  Dùng để giải thích các khối mã phức tạp
*/
```

---

### Tổng Kết

Biến, kiểu dữ liệu, ép kiểu, và ghi chú là những khái niệm cơ bản nhưng rất quan trọng trong JavaScript. Hiểu rõ chúng sẽ giúp bạn viết mã rõ ràng và hiệu quả hơn.
