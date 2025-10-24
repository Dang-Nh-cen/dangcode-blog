---
title: "Câu lệnh điều kiện if/else trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","IfElse","Điều kiện","Feynman"]
featured_image: "/images/if_else.jpeg"
draft: false
weight: 5
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
      Trong lập trình, **câu lệnh điều kiện** là công cụ giúp chương trình Java **ra quyết định** dựa trên các tình huống khác nhau. Đây là một trong những khái niệm cơ bản nhưng mạnh mẽ nhất. Mình học bằng phương pháp Feynman: **“Điều kiện = ngã rẽ đường”**. Bài viết này sẽ giúp bạn nắm vững câu lệnh `if/else` trong Java.
  </p>

  <div style="text-align: center; margin-bottom: 40px;">
      <img src="/dangcode-blog/images/if_else.png" alt="Java IfElse" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
      1. Cấu trúc if và if-else cơ bản
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>Câu lệnh `if` kiểm tra một điều kiện logic. Nếu điều kiện đó là `true`, khối lệnh bên trong `if` sẽ được thực thi. Ngược lại, khối lệnh trong `else` (nếu có) sẽ được thực thi.</p>
      
      <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ đơn giản: Kiểm tra Đậu/Rớt</p>
  </div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
int score = 8;
final int PASS_SCORE = 5;

if (score >= PASS_SCORE) {
    System.out.println("Chúc mừng! Bạn Đậu môn học."); // Điều kiện đúng
} else {
    System.out.println("Xin lỗi! Bạn Rớt môn học.");   // Điều kiện sai
}
// Output: Chúc mừng! Bạn Đậu môn học.
</code>
</pre>

  <div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
      <em>Feynman tip:</em> **Ngã rẽ đường.** Câu lệnh `if` hỏi: "Ngã rẽ này đi được không?". Nếu câu trả lời là **YES** (`true`), ta rẽ vào; nếu câu trả lời là **NO** (`false`), ta đi thẳng hoặc rẽ sang `else`.
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      2. Xử lý nhiều trường hợp với else-if
  </h2>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
      Cấu trúc if-else if-else
  </h3>
  <div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
      <p>Khi bạn có nhiều hơn hai khả năng (A, B, C, D), bạn cần dùng `else if`. Chương trình sẽ kiểm tra điều kiện tuần tự, và **chỉ thực thi khối lệnh đầu tiên** đúng.</p>
  </div>

  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Xếp loại học lực</p>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
int diem = 75;

if (diem >= 90) {
    System.out.println("Xuất sắc (A)");
} else if (diem >= 70) {
    System.out.println("Khá (B)"); // Điều kiện này được thực thi
} else if (diem >= 50) {
    System.out.println("Trung bình (C)");
} else {
    System.out.println("Kém (D)");
}
</code>
</pre>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
      If lồng nhau (Nested If)
  </h3>
  <div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
      <p>Đây là khi bạn đặt một câu lệnh `if` bên trong khối lệnh của một câu lệnh `if` hoặc `else` khác. Nó dùng để kiểm tra các điều kiện **phụ thuộc** vào nhau.</p>
      <p style="font-weight: 600; margin-top: 15px;">Ví dụ: Phải đủ tuổi **VÀ** có bằng lái mới được thuê xe.</p>
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      3. Trải nghiệm học và Kết luận
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <ul style="list-style-type: none; padding-left: 0;">
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">❌ Sai lầm ban đầu:</span> Mình từng nhầm lẫn cú pháp và quên mất rằng điều kiện trong `if` phải luôn là một biểu thức trả về `boolean`. Viết lại giải thích bằng Feynman giúp mình **hiểu ngay** nguyên lý logic của nó.</li>
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">✅ Thực hành nhiều ví dụ:</span> Cách tốt nhất để nắm vững `if/else` là thực hành với các bài toán thực tế (ví dụ: tính lương theo cấp bậc, xác định năm nhuận). Thực hành giúp **ghi nhớ lâu** các quy tắc ưu tiên.</li>
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">📝 Dùng dấu ngoặc nhọn:</span> Luôn dùng dấu ngoặc nhọn `{}` cho khối lệnh, ngay cả khi chỉ có một dòng lệnh, để tránh nhầm lẫn và giúp code dễ đọc hơn.</li>
      </ul>
  </div>

  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
      Tóm lại, `if/else` là nền tảng lập trình quyết định, giúp chương trình của bạn linh hoạt và thông minh hơn.
  </p>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:20px; font-size:1.2em; margin-bottom: 40px;">
      🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
      <p style="margin-top: 10px;"><em>— Đăng Nguyễn Hải</em></p>
  </div>
</div>