---
title: "Classes trong JavaScript"
date: 2024-12-25T10:00:00+06:00
description: "Hướng dẫn chi tiết về cách sử dụng Classes trong JavaScript"
menu:
  sidebar:
    name: Classes JavaScript
    identifier: Classes
    weight: 30
tags: ["Intermediate"]
categories: ["JavaScript"]
math: true
---

# Tìm Hiểu Về Classes Trong JavaScript

Classes trong JavaScript là một cách hiện đại để tạo và quản lý các đối tượng, giúp mã dễ đọc hơn và mạnh mẽ hơn. Trong bài viết này, chúng ta sẽ tìm hiểu các khái niệm cơ bản về Classes.

---

## 2.1. Class Declaration

Classes được khai báo bằng từ khóa `class`, cho phép chúng ta định nghĩa một blueprint cho các đối tượng.

### 2.1.1. Class Declaration

```javascript
class Car {
  constructor(brand) {
    this.brand = brand;
  }
  drive() {
    console.log(`${this.brand} is driving.`);
  }
}

// Tạo một instance của Car
const myCar = new Car('Toyota');
myCar.drive(); // Output: Toyota is driving.
```

### 2.1.2 Class Expression

Câu lệnh lớp (class expression) cho phép bạn định nghĩa một lớp bên trong một biểu thức, và lớp đó có thể được gán cho một biến.

```javascript
const Person = class {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  
  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
};
```

### 2.1.3 The Instance of Operator

Toán tử `instanceof` được sử dụng để kiểm tra xem một đối tượng có phải là một thể hiện (instance) của một lớp cụ thể hay không..

```javascript
const john = new Person("John", 30);
console.log(john instanceof Person); // true
```

---

## 2.2. Section 2 – Properties

### 2.2.1 Properties

Các thuộc tính trong một lớp là những đặc điểm mô tả các thể hiện (instance) của lớp đó. Chúng thường được định nghĩa trong hàm khởi tạo (constructor).

```javascript
class Car {
  constructor(make, model) {
    this.make = make;
    this.model = model;
  }
}
```

### 2.2.2 Định nghĩa thuộc tính bên trong các phương thức của lớp

Thuộc tính cũng có thể được định nghĩa và sửa đổi trong các phương thức của lớp.

```javascript
class Rectangle {
  constructor(width, height) {
    this.width = width;
    this.height = height;
  }

  setDimensions(width, height) {
    this.width = width;
    this.height = height;
  }
}
```

### 2.2.3 Khai báo trực tiếp trong thân lớp

Bạn có thể khai báo các thuộc tính trực tiếp trong thân lớp bằng cách sử dụng trường lớp công khai (public class fields).

```javascript
class User {
  name = "Alice";
  age = 25;
}
```

---

## 2.3. Section 3 – Getters and Setters

### 2.3.1 Getters and Setters

Getters và setters là các phương thức cho phép bạn định nghĩa cách lấy và thiết lập giá trị của các thuộc tính đối tượng. Getters được sử dụng để truy cập giá trị của thuộc tính, trong khi setters được sử dụng để thay đổi giá trị của chúng.

```javascript
class Circle {
  constructor(radius) {
    this._radius = radius;
  }

  get radius() {
    return this._radius;
  }

  set radius(value) {
    if (value > 0) {
      this._radius = value;
    }
  }
}
```

---

## 2.4. Section 4 – Inheritance

### 2.4.1 Inheritance

Kế thừa cho phép một lớp kế thừa các thuộc tính và phương thức từ lớp khác. Điều này được thực hiện bằng cách sử dụng từ khóa extends.

```javascript
class Animal {
  speak() {
    console.log("Animal makes a sound");
  }
}

class Dog extends Animal {
  speak() {
    console.log("Dog barks");
  }
}
```

### 2.4.2 Shadowing

Shadowing xảy ra khi một phương thức hoặc thuộc tính của lớp con có cùng tên với một phương thức hoặc thuộc tính trong lớp cha, làm ẩn đi việc triển khai của lớp cha.

```javascript
class Animal {
  speak() {
    console.log("Animal makes a sound");
  }
}

class Dog extends Animal {
  speak() {
    super.speak(); // Call parent class method
    console.log("Dog barks");
  }
}
```

### 2.4.3 Inheritance from a Constructor Function

Các lớp cũng có thể kế thừa từ các hàm khởi tạo (constructor functions), cho phép kết hợp giữa lập trình hướng đối tượng và lập trình hàm.

```javascript
function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function() {
  console.log(`${this.name} makes a sound`);
};

function Dog(name) {
  Animal.call(this, name);
}

Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;
```

---

## 2.5. Section 5 – Static Members

### 2.5.1 Static Members

Các thành viên tĩnh (Static members) là các thuộc tính hoặc phương thức thuộc về chính lớp, không phải các thể hiện (instances) của lớp. Chúng được định nghĩa bằng cách sử dụng từ khóa `static`.

```javascript
class MathHelper {
  static add(a, b) {
    return a + b;
  }
}

console.log(MathHelper.add(2, 3)); // 5
```

---

## 2.6. Section 6 – Classes vs. Constructors

### 2.6.1 Classes vs. Constructors

Các lớp cung cấp một cú pháp hiện đại và sạch sẽ hơn để định nghĩa các hàm khởi tạo và phương thức. Chúng thực chất là "đường kính ngữ" (syntactic sugar) trên các hàm khởi tạo (constructor functions) và cung cấp các tính năng như kế thừa, getters, setters và phương thức tĩnh. Các hàm khởi tạo là cách cũ hơn để định nghĩa đối tượng và phương thức.

```javascript
// Constructor function
function Person(name, age) {
  this.name = name;
  this.age = age;
}

Person.prototype.greet = function() {
  console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
};

// Class syntax
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}