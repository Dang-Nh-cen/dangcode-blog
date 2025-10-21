---
title: "Câu điều kiện và vòng lặp trong JavaScript"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["JavaScript", "Điều kiện", "Vòng lặp"]
featured_image: "/images/js_loops_cover.png"
draft: false
weight: 16
---

![Loops](/images/js_loops.png)

Câu điều kiện và vòng lặp giúp **máy tính ra quyết định** và **lặp lại công việc** tự động.<!--More-->

## 1. If...else

```javascript
let score = 80;
if (score >= 85) console.log("Xuất sắc");
else if (score >= 65) console.log("Khá");
else console.log("Cần cố gắng");

```
## 2. Switch

```javascript

let day = 3;
switch(day) {
  case 1: console.log("Thứ hai"); break;
  case 7: console.log("Chủ nhật"); break;
  default: console.log("Một ngày khác");
}

```

## 3. Vòng lặp for, while

```javascript

for (let i = 1; i <= 5; i++) console.log(i);
javascript
Sao chép mã
let n = 1;
while (n <= 5) {
  console.log(n);
  n++;
}

```
💡 Feynman Tip: Hãy tưởng tượng for loop là người làm việc theo kế hoạch có sẵn,
còn while là người làm đến khi “xong việc”.