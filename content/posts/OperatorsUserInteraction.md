---
title: "Toán tử và Tương tác Người dùng trong JavaScript"
date: 2024-12-25T10:00:00+06:00
description: "Hướng dẫn chi tiết về các toán tử và cách tương tác với người dùng trong JavaScript"
menu:
  sidebar:
    name: Toán tử và Tương tác
    identifier: OperatorsUserInteraction
    weight: 20
tags: ["Beginner"]
categories: ["JavaScript"]
math: true
---

# Toán tử và Tương tác Người dùng trong JavaScript

Trong JavaScript, các toán tử là các công cụ quan trọng giúp thực hiện các phép tính và thao tác trên dữ liệu. Bên cạnh đó, JavaScript cung cấp cách thức để tương tác trực tiếp với người dùng thông qua giao diện console hoặc các hộp thoại. Hãy cùng khám phá các khái niệm này.

---

## 3.0. Section 1 – Assignment, Arithmetic, and Logical Operators

### Toán tử Gán (Assignment Operators)
Toán tử gán được sử dụng để gán giá trị cho một biến.

```javascript
let x = 10; // Gán giá trị 10 cho biến x
x += 5;    // Tương đương với x = x + 5
```

### Toán tử Số học (Arithmetic Operators)
Các toán tử số học giúp thực hiện các phép toán cơ bản.

```javascript
let a = 10;
let b = 3;
console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.333...
console.log(a % b); // 1 (phần dư)
```

### Toán tử Logic (Logical Operators)
Toán tử logic được sử dụng để thực hiện các phép toán boolean.

```javascript
let isTrue = true;
let isFalse = false;
console.log(isTrue && isFalse); // false
console.log(isTrue || isFalse); // true
console.log(!isTrue);           // false
```

---

## 3.1. Section 2 – String, Comparison, and Other JS Operators

### Toán tử Chuỗi (String Operators)
Toán tử `+` có thể được sử dụng để nối chuỗi.

```javascript
let firstName = "Alice";
let lastName = "Smith";
console.log(firstName + " " + lastName); // "Alice Smith"
```

### Toán tử So Sánh (Comparison Operators)
Các toán tử so sánh được sử dụng để so sánh hai giá trị.

```javascript
let x = 10;
let y = 20;
console.log(x > y);  // false
console.log(x < y);  // true
console.log(x == 10); // true
console.log(x === "10"); // false (so sánh kiểu dữ liệu)
```

### Các Toán tử Khác (Other Operators)
#### Toán tử Điều kiện (Ternary Operator)
Toán tử điều kiện cho phép thực hiện các kiểm tra nhanh.

```javascript
let age = 18;
let isAdult = (age >= 18) ? "Yes" : "No";
console.log(isAdult); // "Yes"
```

#### Toán tử typeof
Toán tử `typeof` trả về kiểu dữ liệu của một biến.

```javascript
console.log(typeof 42); // "number"
console.log(typeof "Hello"); // "string"
console.log(typeof true); // "boolean"
```

---

## 3.2. Section 3 – Interacting with the User

### `alert()` – Hiển thị thông báo
Hàm `alert()` hiển thị một hộp thoại thông báo.

```javascript
alert("Welcome to JavaScript!");
```

### `prompt()` – Lấy dữ liệu từ người dùng
Hàm `prompt()` yêu cầu người dùng nhập dữ liệu.

```javascript
let name = prompt("What is your name?");
alert("Hello, " + name + "!");
```

### `confirm()` – Yêu cầu xác nhận từ người dùng
Hàm `confirm()` hiển thị một hộp thoại xác nhận với hai tùy chọn: OK và Cancel.

```javascript
let isConfirmed = confirm("Do you agree?");
if (isConfirmed) {
  console.log("User agreed.");
} else {
  console.log("User did not agree.");
}
