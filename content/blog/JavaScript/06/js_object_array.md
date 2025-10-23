---
title: "Làm việc với Object và Array trong JavaScript"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["JavaScript", "Object", "Array"]
featured_image: "/images/js_object_array_cover.png"
draft: false
weight: 17
---

![Objects and Arrays](/images/js_objects_arrays.png)

Trong JavaScript, **Object** và **Array** là 2 kiểu dữ liệu “linh hồn” của ngôn ngữ.<!--More-->

## 1. Object
```javascript
let student = {
  name: "Đăng",
  age: 21,
  study: function() {
    console.log(`${this.name} đang học JavaScript`);
  }
};
student.study();

```

## 2. Array

```javascript
let scores = [8, 9, 10];
scores.push(7);
console.log(scores);

```
## 3. Lặp qua mảng

```javascript
scores.forEach(s => console.log(`Điểm: ${s}`));

```

💡 Feynman Tip: Object là “tủ hồ sơ” (có nhãn – giá trị),
còn Array là “danh sách số thứ tự”.

---

<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:15px; font-size:1.1em;">
🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
<br><em>— Đăng Nguyễn Hải</em>
</div>
