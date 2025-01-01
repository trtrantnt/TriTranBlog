---
title: "Đối tượng tích hợp trong JavaScript"
date: 2024-12-25T10:00:00+06:00
description: "Hướng dẫn chi tiết về các đối tượng tích hợp sẵn trong JavaScript"
menu:
  sidebar:
    name: Đối Tượng Tích Hợp
    identifier: BuiltInObjects
    weight: 40
tags: ["Intermediate"]
categories: ["JavaScript"]
math: true
---

# Tìm Hiểu Về Đối Tượng Tích Hợp Trong JavaScript

JavaScript cung cấp nhiều đối tượng tích hợp sẵn giúp xử lý các tác vụ phổ biến như thao tác dữ liệu, tính toán toán học, và làm việc với JSON. Bài viết này sẽ khám phá các loại đối tượng tích hợp và cách sử dụng chúng.

---

## 3.0. Section 0 – Built-in Objects

Đối tượng tích hợp sẵn (built-in objects) trong JavaScript là các công cụ mạnh mẽ được cung cấp để thực hiện các tác vụ lập trình thông thường.

---

## 3.1. Kiểu Dữ Liệu Đơn Giản (Simple Data Types)

Các kiểu dữ liệu đơn giản bao gồm các đối tượng như `String`, `Number`, và `Boolean`. Những đối tượng này cho phép bạn làm việc với các giá trị cơ bản một cách dễ dàng.

### Ví dụ về String:
```javascript
const message = "Hello, World!";
console.log(message.toUpperCase()); // "HELLO, WORLD!"
```

### Ví dụ về Number:
```javascript
const number = 42;
console.log(number.toString()); // "42"
```

---

## 3.2. Kiểu Dữ Liệu Phức Hợp (Composite Data Types)

Kiểu dữ liệu phức hợp bao gồm các đối tượng như `Array` và `Object`, giúp bạn lưu trữ và quản lý dữ liệu phức tạp.

### Ví dụ về Array:
```javascript
const fruits = ["Apple", "Banana", "Cherry"];
fruits.push("Date");
console.log(fruits); // ["Apple", "Banana", "Cherry", "Date"]
```

### Ví dụ về Object:
```javascript
const person = {
  name: "Alice",
  age: 30,
};
console.log(person.name); // "Alice"
```

---

## 3.3. JSON, Math và RegExp

### JSON
Đối tượng JSON (JavaScript Object Notation) được sử dụng để làm việc với dữ liệu dạng JSON.

```javascript
const jsonString = '{"name":"Alice","age":30}';
const data = JSON.parse(jsonString);
console.log(data.name); // "Alice"
```

### Math
Đối tượng Math cung cấp các phương thức và hằng số toán học.

```javascript
console.log(Math.sqrt(16)); // 4
console.log(Math.PI); // 3.141592653589793
```

### RegExp
Đối tượng RegExp cho phép làm việc với các biểu thức chính quy.

```javascript
const pattern = /hello/i;
console.log(pattern.test("Hello, World!")); // true
```

---

## 3.4. Mở Rộng Các Kiểu Tích Hợp (Extending Built-in Types)

Bạn có thể mở rộng các đối tượng tích hợp để thêm chức năng mới, nhưng hãy cẩn thận để không ghi đè các phương thức mặc định.

### Ví dụ mở rộng Array:
```javascript
Array.prototype.last = function() {
  return this[this.length - 1];
};

const numbers = [1, 2, 3];
console.log(numbers.last()); // 3
```
