---
title: "Object trong Javascript"
date: 2024-12-25T08:06:25+06:00
description: Object trong Javascript
menu:
  sidebar:
    name: Object Javascript
    identifier: Object
    weight: 30
tags: ["Basic"]
categories: ["Basic"]
math: true
---

Tìm Hiểu Về Đối Tượng Trong JavaScript

Đối tượng là một trong những khái niệm quan trọng nhất trong JavaScript, giúp bạn tổ chức dữ liệu và logic một cách hiệu quả. Trong bài viết này, chúng ta sẽ khám phá các khía cạnh chính của đối tượng, từ cách tạo đến cách sử dụng.

---
## 1.1. Đối tượng là gì?

Đối tượng (Object) là một cấu trúc dữ liệu phức tạp, giúp lưu trữ nhiều giá trị liên quan. Nó có thể bao gồm các thuộc tính (properties) và phương thức (methods).

### 1.1.1. Kiểu dữ liệu nguyên thủy (Primitive Data Types):

Các giá trị như <mark>number</mark>, <mark>string</mark>, <mark>boolean</mark> là kiểu nguyên thủy.

```javascript
let num = 10; // Kiểu số
let str = "Hello"; // Kiểu chuỗi
let bool = true; // Kiểu boolean
```

### 1.1.2. Mảng là kiểu phức tạp (Array as a Complex Type):

Mảng cũng là một đối tượng đặc biệt trong JavaScript.

```javascript
let arr = [1, 2, 3];
console.log(typeof arr); // "object"
```

### 1.1.3. Đối tượng như một kiểu khác của mảng (Object as a Different Type of Array):

Đối tượng có cấu trúc <mark>key: value</mark>, khác biệt với mảng dựa trên chỉ số.

```javascript
let obj = { name: "Alice", age: 25 };
```

---
## 1.2. Cách tạo và xóa đối tượng

### 1.2.1. Cách tạo cơ bản (Basic Way to Create Objects):

```javascript
let person = {
  name: "John",
  age: 30,
};
```

### 1.2.2. Xóa đối tượng (Deleting Objects):

Sử dụng từ khóa `delete` để xóa thuộc tính.

```javascript
delete person.age;
console.log(person); // { name: "John" }
```

---
## 1.3. Thuộc tính của đối tượng

### 1.3.1. Loại thuộc tính (Types):

Giá trị thuộc tính có thể là bất kỳ kiểu dữ liệu nào.

```javascript
let car = {
  brand: "Toyota",
  model: 2020,
  isAvailable: true,
};
```

### 1.3.2. Thuộc tính lồng nhau (Nested Properties):

```javascript
let company = {
  name: "TechCorp",
  address: { city: "New York", zip: "10001" },
};
```

### 1.3.3. Hàm như một thuộc tính (Function as a Property – Method):

```javascript
let calculator = {
  add: function (a, b) {
    return a + b;
  },
};
console.log(calculator.add(2, 3)); // 5
```

### 1.3.4. Thêm thuộc tính mới (Adding a New Property):

```javascript
person.gender = "male";
```

### 1.3.5. Sửa đổi thuộc tính (Modifying a Property):

```javascript
person.name = "Doe";
```

### 1.3.6. Xóa thuộc tính (Deleting a Property):

```javascript
delete person.gender;
```

---
## 1.4. Dot Notation vs. Bracket Notation

### 1.4.1. Khóa nhiều từ (Multi-word Keys):

Sử dụng bracket notation khi khóa có khoảng trắng.

```javascript
let obj = { "first name": "Alice" };
console.log(obj["first name"]); // Alice
```

### 1.4.2. Khóa tính toán (Computed Keys):

```javascript
let key = "age";
let user = { [key]: 25 };
console.log(user.age); // 25
```

---
## 1.5. Kiểm tra và liệt kê thuộc tính

### 1.5.1. Kiểm tra tồn tại (Existence Test):

```javascript
console.log("name" in person); // true
```

### 1.5.2. Vòng lặp "for...in" (Enumeration):

```javascript
for (let key in person) {
  console.log(key); // name, age
}
```

### 1.5.3. Phương thức `Object.keys`:

```javascript
console.log(Object.keys(person)); // ["name", "age"]
```

---
## 1.6. Tham chiếu và sao chép

### 1.6.1. Tham chiếu (References):

Đối tượng lưu trữ tham chiếu, không phải giá trị.

### 1.6.4. Sao chép đối tượng (Cloning and Merging):

```javascript
let clone = { ...person };
```

---
## 1.7. Phương thức (Methods)

### 1.7.2. Từ khóa `this`:

```javascript
let user = {
  name: "John",
  greet() {
    console.log(`Hello, ${this.name}`);
  },
};
user.greet(); // Hello, John
```

---
## 1.9. Các cách khác để tạo đối tượng

### 1.9.3. Constructor và `new`:

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}
let john = new Person("John", 30);
```

---
## 1.10. Prototype

### 1.10.1. Prototype và kế thừa:

Prototype giúp chia sẻ thuộc tính và phương thức.

```javascript
let obj = { a: 1 };
console.log(obj.__proto__);
