---
title: "Hàm, Overloading và Parameter Passing trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Hàm","Function","Overloading","Feynman"]
featured_image: "/images/java_cover_16.png"
draft: false
weight: 8
---

Hàm giúp **tổ chức và tái sử dụng code**. Overloading và Parameter Passing làm code linh hoạt hơn. <!--more--> 

![Java Functions](/images/java_functions.png)

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