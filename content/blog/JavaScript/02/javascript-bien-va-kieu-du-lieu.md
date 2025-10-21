---
title: "Biến và kiểu dữ liệu trong JavaScript"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["JavaScript", "Cơ bản", "Biến", "Kiểu dữ liệu"]
featured_image: "/images/js_variables.png"
draft: false
weight: 13
---

![JS Variables](/images/js_variables.png)

Trong JavaScript, **biến** là nơi lưu trữ dữ liệu, còn **kiểu dữ liệu** xác định loại giá trị bạn đang lưu.<!--more-->

## 1. Khai báo biến
```javascript
let name = "Đăng";
const PI = 3.14;
var age = 21;

```
let → khai báo biến có thể thay đổi

const → biến hằng số

var → cú pháp cũ, nên hạn chế

💡 Feynman Tip: Hãy tưởng tượng biến là chiếc hộp.
const là hộp dán kín, let là hộp mở được nắp, còn var là hộp “cũ” dễ nhầm lẫn.


## 2. Các kiểu dữ liệu cơ bản

```java
String: "Hello"

Number: 123, 3.14

Boolean: true, false

Object: {name: "Đăng", age: 21}

Array: [1, 2, 3]

Undefined, Null, Symbol

```

## 3. Ví dụ

```java
let student = {
  name: "Hải",
  age: 20,
  isActive: true
};
console.log(`Tên: ${student.name}, Tuổi: ${student.age}`);

```

## 4. Ghi nhớ
Hãy dùng Feynman để tự hỏi:
“Nếu phải giải thích biến cho người 5 tuổi, tôi sẽ nói thế nào?”
→ “Là chỗ để cất giữ thông tin để dùng lại sau.”