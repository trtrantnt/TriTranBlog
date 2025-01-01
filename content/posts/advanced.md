---
title: "Sử Dụng Hàm Nâng Cao trong JavaScript"
date: 2024-12-26T10:00:00+06:00
description: "Hướng dẫn chi tiết về cách sử dụng hàm nâng cao trong JavaScript"
menu:
  sidebar:
    name: Hàm Nâng Cao
    identifier: AdvancedFunctions
    weight: 50
tags: ["Advanced"]
categories: ["JavaScript"]
math: true
---

# Sử Dụng Hàm Nâng Cao trong JavaScript

JavaScript cung cấp nhiều tính năng mạnh mẽ cho phép bạn sử dụng các hàm một cách linh hoạt và hiệu quả hơn. Trong bài viết này, chúng ta sẽ tìm hiểu về các khái niệm nâng cao liên quan đến hàm.

---

## 4.0. Một Chút Về Hàm

Hàm là một phần quan trọng trong JavaScript, cho phép bạn tái sử dụng mã và tổ chức logic một cách hiệu quả. Việc hiểu sâu hơn về hàm sẽ giúp bạn viết mã sạch hơn và dễ bảo trì hơn.

---

## 4.1. Hàm Nâng Cao và Decorators

Hàm nâng cao bao gồm các khái niệm như hàm lồng nhau, hàm mũi tên, và closures. Decorators là một tính năng mạnh mẽ cho phép bạn sửa đổi hoặc bổ sung chức năng cho các hàm hoặc lớp.

### Ví dụ về Closure:
```javascript
function makeCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = makeCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

### Decorators:
Decorators thường được sử dụng trong các framework như Angular để thêm chức năng cho các lớp hoặc phương thức.

---

## 4.2. Generators và Iterators

Generators và iterators cho phép bạn tạo ra các trình lặp (iterable) và kiểm soát luồng dữ liệu một cách linh hoạt.

### Ví dụ về Generator:
```javascript
function* generateSequence() {
  yield 1;
  yield 2;
  yield 3;
}

const generator = generateSequence();
console.log(generator.next().value); // 1
console.log(generator.next().value); // 2
console.log(generator.next().value); // 3
```

### Iterator:
```javascript
const iterable = {
  items: ["a", "b", "c"],
  [Symbol.iterator]() {
    let index = 0;
    return {
      next: () => {
        if (index < this.items.length) {
          return { value: this.items[index++], done: false };
        } else {
          return { done: true };
        }
      }
    };
  }
};

for (const item of iterable) {
  console.log(item); // "a", "b", "c"
}
```

---

## 4.3. Section 3 – Lập Trình Bất Đồng Bộ

Lập trình bất đồng bộ (asynchronous programming) trong JavaScript giúp bạn xử lý các tác vụ không đồng bộ như gọi API hoặc đọc file mà không làm gián đoạn luồng chính của ứng dụng.

### Promises:
```javascript
const fetchData = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Dữ liệu đã tải"), 1000);
});

fetchData.then(data => console.log(data));
```

### Async/Await:
```javascript
async function getData() {
  const data = await fetchData;
  console.log(data);
}

getData();
```

---
