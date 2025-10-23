---
title: "Mảng và Collection trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Mảng","Collection","Array","List","Feynman"]
featured_image: "/images/array.png"
draft: false
weight: 7
---

Mảng và Collection giúp **lưu trữ nhiều giá trị cùng lúc**. Mình học bằng Feynman: “Mảng = hộp nhiều ngăn, Collection = tủ đồ linh hoạt”.<!--more-->

![Java Array Collection](/dangcode-blog/images/a_c.jpeg)




## 1. Mảng (Array)

```java
int[] numbers = {1,2,3,4,5};
for(int n : numbers){
  System.out.println(n);
}
```

## 2. Collection (ArrayList)

```java
import java.util.ArrayList;

ArrayList<String> fruits = new ArrayList<>();
fruits.add("Táo");
fruits.add("Cam");
System.out.println(fruits);
```
## 3. Trải nghiệm học

- Thực hành thêm xóa, sắp xếp mảng và ArrayList

- Vẽ sơ đồ Feynman: mảng = ngăn hộp, ArrayList = tủ đồ mở rộng → dễ hình dung

## 4. Kết luận

- Mảng & Collection là công cụ lưu trữ dữ liệu cơ bản và nâng cao

---
<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:15px; font-size:1.1em;">
🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
<br><em>— Đăng Nguyễn Hải</em>
</div>