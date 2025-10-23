---
title: "Hàm, Overloading và Parameter Passing trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Hàm","Function","Overloading","Feynman"]
featured_image: "/images/ham.jpg"
draft: false
weight: 8
---

Hàm giúp **tổ chức và tái sử dụng code**. Overloading và Parameter Passing làm code linh hoạt hơn. <!--more--> 

![Java Functions](/dangcode-blog/images/func.png)

## 1. Hàm cơ bản

```java
int sum(int a, int b){
  return a + b;
}
```

## 2. Overloading

```java
int sum(int a, int b){ return a+b; }
double sum(double a, double b){ return a+b; }
```

## 3. Parameter Passing

- Java sử dụng pass-by-value cho kiểu nguyên thủy

- Tham chiếu cho object giúp thay đổi nội dung object

## 4. Trải nghiệm học

- Viết nhiều hàm khác nhau → Feynman: “Hàm = robot thực hiện nhiệm vụ”

- Thử Overloading → ghi nhớ sự khác biệt

## 5. Kết luận

- Hàm & Overloading giúp tổ chức code hiệu quả

---
<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:15px; font-size:1.1em;">
🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
<br><em>— Đăng Nguyễn Hải</em>
</div>