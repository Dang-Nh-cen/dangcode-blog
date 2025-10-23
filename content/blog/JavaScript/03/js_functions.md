---
title: "Hàm và phạm vi (Scope) trong JavaScript"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["JavaScript", "Hàm", "Scope"]
featured_image: "/images/js_functions_cover.png"
draft: false
weight: 14
---

![Function Illustration](/images/js_functions.png)

**Hàm (Function)** là khối mã thực hiện một nhiệm vụ cụ thể, giúp code ngắn gọn, tái sử dụng dễ dàng.
**Phạm vi (Scope)** quyết định nơi bạn có thể truy cập biến.<!--More-->

## 1. Định nghĩa hàm

```javascript
function greet(name) {
  console.log(`Xin chào, ${name}!`);
}

greet("Đăng"); // Kết quả: Xin chào, Đăng!

```
💡 Feynman Tip: Hãy nghĩ hàm như một chiếc máy — bạn đưa vào “nguyên liệu” (tham số) và nhận lại “sản phẩm” (giá trị trả về).

## 2. Arrow Function

```java
const sum = (a, b) => a + b;
console.log(sum(2, 3)); // 5

```

Ngắn gọn hơn, thích hợp cho xử lý nhanh.

## 3. Phạm vi biến

```java
let x = 10;
function test() {
  let x = 5;
  console.log(x); // 5
}
test();
console.log(x); // 10

```

👉 Biến x trong hàm không ảnh hưởng đến x bên ngoài.

## 4. Học bằng Feynman

Tự giải thích “Hàm hoạt động thế nào?”

Tự viết ví dụ rồi giải thích lại bằng lời.
Điều này giúp bạn nhớ lâu hơn thay vì chỉ đọc qua.


---
<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:15px; font-size:1.1em;">
🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
<br><em>— Đăng Nguyễn Hải</em>
</div>
