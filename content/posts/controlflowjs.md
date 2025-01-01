---
title: "Luồng điều khiển trong JavaScript"
date: 2024-12-25T10:00:00+06:00
description: "Hướng dẫn về luồng điều khiển với câu lệnh điều kiện và vòng lặp trong JavaScript"
menu:
  sidebar:
    name: Luồng Điều Khiển
    identifier: ControlFlowJS
    weight: 40
tags: ["Beginner"]
categories: ["JavaScript"]
math: true
---

# Luồng Điều Khiển trong JavaScript

JavaScript cung cấp các công cụ mạnh mẽ để điều khiển luồng thực thi của chương trình, bao gồm các câu lệnh điều kiện và vòng lặp. Những công cụ này giúp lập trình viên tạo ra các ứng dụng động và linh hoạt.

---

## 4.0. Conditional Execution

Câu lệnh điều kiện cho phép bạn kiểm tra các điều kiện và thực thi mã dựa trên kết quả của điều kiện đó.

### Ví dụ If-Else:
```javascript
const age = 18;
if (age >= 18) {
  console.log("Bạn đủ tuổi để bỏ phiếu.");
} else {
  console.log("Bạn chưa đủ tuổi để bỏ phiếu.");
}
```

### Ví dụ Switch:
```javascript
const day = "Monday";
switch (day) {
  case "Monday":
    console.log("Hôm nay là thứ Hai.");
    break;
  case "Tuesday":
    console.log("Hôm nay là thứ Ba.");
    break;
  default:
    console.log("Không phải ngày trong tuần được hỗ trợ.");
}
```

---

## 4.1. Loops

Vòng lặp cho phép bạn thực thi một đoạn mã nhiều lần dựa trên một điều kiện nhất định.

### Ví dụ For Loop:
```javascript
for (let i = 0; i < 5; i++) {
  console.log(`Lần lặp thứ ${i}`);
}
```

### Ví dụ While Loop:
```javascript
let count = 0;
while (count < 5) {
  console.log(`Đếm: ${count}`);
  count++;
}
```

### Ví dụ Do-While Loop:
```javascript
let number = 0;
do {
  console.log(`Số hiện tại: ${number}`);
  number++;
} while (number < 3);
```
---