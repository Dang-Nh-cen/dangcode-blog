---
title: "Toán tử và biểu thức trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Toán tử","Biểu thức","Feynman"]
featured_image: "/images/toantu.png"
draft: false
weight: 4
summary: "Toán tử (Operators) là **công cụ xử lý dữ liệu** cơ bản nhất trong lập trình. Chúng cho phép chúng ta thực hiện các phép tính, so sánh giá trị, và kết hợp các điều kiện."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
<p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
    Toán tử (Operators) là **công cụ xử lý dữ liệu** cơ bản nhất trong lập trình. Chúng cho phép chúng ta thực hiện các phép tính, so sánh giá trị, và kết hợp các điều kiện. Mình học bằng cách giải thích theo Feynman: **“Toán tử = công cụ biến đổi dữ liệu”**. Bài viết này sẽ giúp bạn nắm vững các loại toán tử quan trọng nhất trong Java.
</p>

<div style="text-align: center; margin-bottom: 40px;">
    <img src="/dangcode-blog/images/toantu.png" alt="Java Operators" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
</div>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
    1. Toán tử số học (Arithmetic Operators)
</h2>
<div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
    <p>Đây là những toán tử quen thuộc nhất, dùng để thực hiện các phép tính cơ bản trên số nguyên và số thực:</p>
    <ul style="list-style-type: disc; padding-left: 20px;">
        <li>`+` (Cộng), `-` (Trừ), `*` (Nhân)</li>
        <li>`/` (Chia): **Lưu ý:** Nếu chia hai số nguyên, kết quả sẽ là số nguyên (ví dụ: `5 / 2 = 2`).</li>
        <li>`%` (Chia lấy dư - Modulus): Rất hữu ích khi kiểm tra số chẵn/lẻ.</li>
        <li>`++` (Tăng 1), `--` (Giảm 1): Dùng để tăng/giảm giá trị biến đi một đơn vị.</li>
    </ul>
</div>
    
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
int a = 5, b = 3;
int sum = a + b;             // sum = 8
int product = a * b;         // product = 15
int remainder = a % b;       // remainder = 2 (5 chia 3 dư 2)
int division = 5 / 2;        // division = 2 (chia số nguyên)

// Toán tử tăng/giảm
a++; // a = 6
b--; // b = 2
</code>
</pre>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
    2. Toán tử so sánh (Relational) & Logic (Logical)
</h2>

<h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
    Toán tử so sánh (Kết quả luôn là `boolean`)
</h3>
<div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
    <ul style="list-style-type: disc; padding-left: 20px;">
        <li>`==` (Bằng nhau), `!=` (Khác nhau)</li>
        <li>`>` (Lớn hơn), `<` (Nhỏ hơn)</li>
        <li>`>=` (Lớn hơn hoặc bằng), `<=` (Nhỏ hơn hoặc bằng)</li>
    </ul>
</div>

<h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
    Toán tử logic (Kết hợp các điều kiện `boolean`)
</h3>
<div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
    <ul style="list-style-type: disc; padding-left: 20px;">
        <li>`&&` (AND): Chỉ đúng khi **cả hai** điều kiện đều đúng.</li>
        <li>`||` (OR): Chỉ cần **một trong hai** điều kiện đúng là biểu thức đúng.</li>
        <li>`!` (NOT): Đảo ngược giá trị logic (`!true` là `false`).</li>
    </ul>
</div>
    
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
int a = 5, b = 3;
boolean isAGreater = (a > b);        // isAGreater = true
boolean isAEqualB = (a == b);        // isAEqualB = false

// Toán tử Logic: Điều kiện phức tạp
boolean result = (a > b) && (b < 10); // (true) && (true) = true

// Ví dụ về OR và NOT
boolean canEnter = (age >= 18) || (hasPermission); // Chỉ cần một điều kiện đúng
boolean isNotPassed = !passed;
</code>
</pre>

<div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
    <em>Feynman tip:</em> **“So sánh = câu hỏi, logic = ghép câu hỏi”**. Toán tử so sánh đặt câu hỏi (`a > b`?), còn toán tử logic giúp bạn ghép nhiều câu hỏi lại thành một quyết định lớn (`Đúng hay Sai`).
</div>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #e91e63; border-bottom: 3px solid #fce4ec; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
    3. Toán tử gán và Thứ tự ưu tiên
</h2>

<h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
    Toán tử gán (Assignment Operators)
</h3>
<div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
    <p>Toán tử gán (`=`) dùng để đặt giá trị vào biến. Ngoài ra, Java còn có các toán tử gán rút gọn:</p>
    <ul style="list-style-type: disc; padding-left: 20px;">
        <li>`+=` (Cộng rồi gán): `x += 5;` tương đương với `x = x + 5;`</li>
        <li>`-=` (Trừ rồi gán), `*=` (Nhân rồi gán), `/=` (Chia rồi gán), v.v.</li>
    </ul>
</div>

<h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
    Thứ tự ưu tiên (Operator Precedence)
</h3>
<div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
    <p>Giống như toán học, Java có quy tắc ưu tiên: nhân/chia/phần dư (`*`, `/`, `%`) được thực hiện trước cộng/trừ (`+`, `-`). **Luôn sử dụng dấu ngoặc đơn `()`** để đảm bảo biểu thức chạy theo đúng ý bạn muốn, đặc biệt với các phép toán phức tạp.</p>
    <p style="font-weight: 600; margin-top: 15px;">Ví dụ: `int result = 5 + 3 * 2;` sẽ cho kết quả là 11 (vì 3 * 2 = 6, sau đó 5 + 6 = 11).</p>
</div>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
    4. Trải nghiệm học & Kết luận
</h2>
<div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
    <ul style="list-style-type: none; padding-left: 0;">
        <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">✅ Thực hành biểu thức phức tạp:</span> Cách tốt nhất để nắm vững thứ tự ưu tiên là tự viết và giải các biểu thức phức tạp bằng tay trước khi chạy code. Điều này giúp bạn **nhớ lâu** và tránh lỗi logic.</li>
        <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">🧠 Vẽ sơ đồ toán tử:</span> Vẽ sơ đồ cây (tree diagram) cho các biểu thức logic giúp bạn **hiểu nhanh hơn** cách các điều kiện `&&` và `||` kết hợp.</li>
    </ul>
</div>

<p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
    Tóm lại, toán tử giúp chúng ta xử lý dữ liệu hiệu quả và là nền tảng để viết mọi thuật toán trong Java.
</p>


<h2 style="color: #4CAF50; border-bottom: 3px solid #4CAF50; padding-bottom: 10px; margin-top: 40px; font-weight: 800; font-size: 2.2em; text-align: center;">
    🛠️ Test Code Với Java
</h2>

Hãy bắt đầu với đoạn mã đầu tiên của bạn

    {{< java_code_button src="https://517438ca-0c49-467b-b6f4-22a68a0abaa4-00-1k8m3q9oydb9e.kirk.replit.dev/" height="480px" >}}
<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:20px; font-size:1.2em; margin-bottom: 40px;">
    🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
    <p style="margin-top: 10px;"><em>— Đăng Nguyễn Hải</em></p>
</div>
</div>  