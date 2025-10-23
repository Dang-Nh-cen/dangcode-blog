---
title: "Java Input/Output (I/O)"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","I/O","File","Scanner","Feynman"]
featured_image: "/images/io.gif"
draft: false
weight: 11
---

Java I/O giúp **đọc/ghi dữ liệu từ file hoặc console**.  <!--more-->

![Java IO](/dangcode-blog/images/io-ins.gif)

## 1. Nhập dữ liệu từ console

```java
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
System.out.print("Nhập tên: ");
String name = sc.nextLine();
System.out.println("Chào " + name);
```

## 2. Đọc/ghi file

```java
import java.io.*;
BufferedReader br = new BufferedReader(new FileReader("input.txt"));
String line;
while((line = br.readLine()) != null){
  System.out.println(line);
}
br.close();
```

## 3. Trải nghiệm học
Thực hành nhiều ví dụ console và file → hiểu rõ Input/Output

Feynman tip: “Input = nhận dữ liệu, Output = trả dữ liệu”

## 4. Kết luận
I/O là khả năng giao tiếp của chương trình

---
<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:15px; font-size:1.1em;">
🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
<br><em>— Đăng Nguyễn Hải</em>
</div>