---
title: "Exception Handling trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Exception","Error","TryCatch","Feynman"]
featured_image: "/images/ex.jpg"
draft: false
weight: 10
---

Exception giúp **bắt lỗi và duy trì chương trình chạy ổn định**.  <!--more-->

![Java Exception](/dangcode-blog/images/exc.png)

## 1. Try-Catch

```java
try {
  int a = 5/0;
} catch(ArithmeticException e) {
  System.out.println("Lỗi chia cho 0: " + e.getMessage());
}

```
## 2. Finally
   
```java
try{ ... } catch(Exception e){ ... } finally{
  System.out.println("Luôn chạy đoạn này");
}

```
## 3. Trải nghiệm học
Thực hành nhiều lỗi thường gặp → dễ nhớ

Feynman tip: “Exception = tín hiệu cảnh báo, catch = cứu hộ”

## 4. Kết luận
Exception giúp chương trình an toàn hơn

---
<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:15px; font-size:1.1em;">
🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
<br><em>— Đăng Nguyễn Hải</em>
</div>