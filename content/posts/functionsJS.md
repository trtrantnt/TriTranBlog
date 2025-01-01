---
title: "Functions in JavaScript"
date: 2024-12-25T10:00:00+06:00
description: "Hướng dẫn về hàm trong JavaScript"
menu:
  sidebar:
    name: Functions
    identifier: FunctionsJS
    weight: 50
tags: ["Beginner", "JavaScript"]
categories: ["JavaScript"]
math: true
---

# Functions in JavaScript

Hàm là một phần quan trọng trong JavaScript, giúp tái sử dụng mã và thực hiện các tác vụ lặp lại. Dưới đây là hướng dẫn chi tiết về các khái niệm và cách sử dụng hàm trong JavaScript.

---

## 5.0. Functions – Part 1

### 5.0.1 Functions

Hàm là một khối mã có thể được gọi để thực thi một tác vụ cụ thể. Các hàm giúp tách biệt mã thành các phần nhỏ hơn, dễ quản lý hơn.

### 5.0.2 Declaring functions

Có thể khai báo hàm theo nhiều cách khác nhau trong JavaScript. Dưới đây là ví dụ về khai báo hàm thông qua cách thông thường.

```javascript
function greet(name) {
  console.log("Hello, " + name);
}
```
### 5.0.3 Calling functions

Sau khi khai báo hàm, bạn có thể gọi hàm đó để thực thi.

```javascript
greet("Alice"); // Kết quả: Hello, Alice
```
### 5.0.4 Functions – local variables

Biến trong hàm thường chỉ có phạm vi trong hàm đó. Các biến này được gọi là biến cục bộ.

```javascript
function example() {
  let localVar = "I am local";
  console.log(localVar);
}

```
### 5.0.5 The return statement

Câu lệnh return được sử dụng để trả về một giá trị từ hàm.

```javascript
function add(a, b) {
  return a + b;
}
console.log(add(2, 3)); // Kết quả: 5

```
### 5.0.6 Parameters

Các tham số được truyền vào hàm để hàm có thể sử dụng trong quá trình thực thi.

```javascript
function greet(name, age) {
  console.log(name + " is " + age + " years old.");
}
greet("Bob", 25);

```
### 5.0.7 Shadowing

Shadowing xảy ra khi một biến trong phạm vi con (local) có tên trùng với biến trong phạm vi ngoài (global).

```javascript
let x = 10;
function test() {
  let x = 5;
  console.log(x); // Kết quả: 5 (biến x trong hàm shadowing biến x ngoài hàm)
}
test();
```
---

## 5.1. Functions – Part 2

### 5.1.1 Parameters validation

Kiểm tra và xác nhận các tham số đầu vào trước khi sử dụng trong hàm.

```javascript
function divide(a, b) {
  if (b === 0) {
    console.log("Không thể chia cho 0");
  } else {
    return a / b;
  }
}
console.log(divide(10, 0)); // Kết quả: Không thể chia cho 0
```

### 5.1.2 Recursion

Đệ quy là khi một hàm gọi lại chính nó. Đây là một kỹ thuật mạnh mẽ trong lập trình.

```javascript
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // Kết quả: 120
```

### 5.1.3 Functions as first-class members

Hàm trong JavaScript là các đối tượng bậc nhất, có thể được gán cho biến, truyền làm đối số và trả về từ hàm.

```javascript
const greet = function(name) {
  console.log("Hello, " + name);
};
greet("Charlie");
```
### 5.1.4 Function expressions

Biểu thức hàm là khi một hàm được khai báo như một biểu thức và có thể gán cho một biến.

```javascript
const square = function(x) {
  return x * x;
};
console.log(square(4)); // Kết quả: 16

```
### 5.1.5 Callbacks

Callback là một hàm được truyền vào một hàm khác như một đối số và được gọi lại khi hoàn thành một tác vụ.

```javascript
function fetchData(callback) {
  setTimeout(() => {
    callback("Dữ liệu đã được tải");
  }, 1000);
}

fetchData(function(data) {
  console.log(data);
});
```

### 5.1.6 Asynchronous callbacks

Callback bất đồng bộ giúp xử lý các tác vụ không đồng bộ như gọi API.

```javascript
function fetchData(callback) {
  setTimeout(() => {
    callback("Dữ liệu đã được tải");
  }, 2000);
}

fetchData(function(data) {
  console.log(data);
});

```

### 5.1.7 setTimeout and setInterval functions

<mark>setTimeout</mark> và <mark>setInterval</mark> là hai hàm giúp trì hoãn hoặc lặp lại hành động sau một khoảng thời gian nhất định.

```javascript
setTimeout(() => {
  console.log("Đã trễ 2 giây");
}, 2000);

setInterval(() => {
  console.log("Lặp lại mỗi giây");
}, 1000);

```

### 5.1.8 Arrow functions

Arrow functions cung cấp cú pháp ngắn gọn để khai báo hàm.

```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // Kết quả: 5

```
---