---
title: "Lập trình hướng đối tượng nâng cao: Class, Inheritance, Polymorphism"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","OOP","Class","Inheritance","Polymorphism","Feynman"]
featured_image: "/images/class.jpg"
draft: false
weight: 9
---

Java là ngôn ngữ **hướng đối tượng (OOP)**. Class, Inheritance, Polymorphism là nền tảng.  
Mình học bằng Feynman: “Class = bản thiết kế, Object = sản phẩm, Inheritance = thừa kế bản thiết kế, Polymorphism = nhiều hình thái sản phẩm”.<!--more-->

![Java OOP](/dangcode-blog/images/oop.jpg)

## 1. Class và Object

```java
class Animal {
  String name;
  void sound(){ System.out.println("Some sound"); }
}

Animal dog = new Animal();
dog.name = "Dog";
dog.sound();
```

## 2. Inheritance

```java
class Dog extends Animal {
  void sound(){ System.out.println("Woof"); }
}
```

## 3. Polymorphism

```java
Animal a = new Dog();
a.sound(); // Woof
```

## 4. Trải nghiệm học

- Vẽ sơ đồ OOP → dễ hiểu mối quan hệ Class/Object

- Thực hành nhiều ví dụ Polymorphism → ghi nhớ nhanh

## 5. Kết luận

- OOP giúp tổ chức code lớn dễ dàng và linh hoạt

---
<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:15px; font-size:1.1em;">
🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
<br><em>— Đăng Nguyễn Hải</em>
</div>