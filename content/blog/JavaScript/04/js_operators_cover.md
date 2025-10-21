---
title: "Toán tử và biểu thức trong JavaScript"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["JavaScript", "Toán tử", "Biểu thức"]
featured_image: "/images/js_operators_cover.png"
draft: false
weight: 15
---

![Operators](/images/js_operators.png)

Trong JavaScript, **toán tử (operator)** là ký hiệu thực hiện phép tính hoặc thao tác trên dữ liệu.<!--More-->

## 1. Toán tử cơ bản

```javascript
let a = 5, b = 2;
console.log(a + b); // 7
console.log(a * b); // 10
console.log(a / b); // 2.5

```

## 2. Toán tử so sánh

```javascript

console.log(5 == "5");  // true (so sánh giá trị)
console.log(5 === "5"); // false (so sánh giá trị + kiểu)
💡 Feynman Tip: Hãy nghĩ “==” như so sánh bằng mắt, còn “===” như so sánh bằng kính hiển vi (so cả chi tiết kiểu dữ liệu).

```

## 3. Toán tử logic

```javascript

let x = true, y = false;
console.log(x && y); // false
console.log(x || y); // true
console.log(!x);     // false

```

## 4. Thực hành nhỏ
Viết chương trình kiểm tra tuổi hợp lệ:

```javascript
let age = 18;
let valid = (age >= 18) ? "Đủ tuổi" : "Chưa đủ tuổi";
console.log(valid);

```