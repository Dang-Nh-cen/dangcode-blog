---
title: "Exception Handling trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Exception","Error","TryCatch","Feynman"]
featured_image: "/images/ex.jpg"
draft: false
weight: 10
summary: "Trong lập trình Java, **Xử lý ngoại lệ (Exception Handling)** là kỹ thuật cốt lõi giúp bạn **bắt lỗi và duy trì chương trình chạy ổn định** ngay cả khi có sự cố xảy ra. Thay vì bị dừng đột ngột, chương trình có thể cứu hộ và tiếp tục công việc."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
<p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
    Trong lập trình Java, **Xử lý ngoại lệ (Exception Handling)** là kỹ thuật cốt lõi giúp bạn **bắt lỗi và duy trì chương trình chạy ổn định** ngay cả khi có sự cố xảy ra. Thay vì bị dừng đột ngột, chương trình có thể "cứu hộ" và tiếp tục công việc.
</p>

<div style="text-align: center; margin-bottom: 40px;">
    <img src="/dangcode-blog/images/exc.png" alt="Java Exception" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
</div>

<div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
    Mình học bằng phương pháp Feynman: 
    > **“Exception = tín hiệu cảnh báo bất ngờ, Catch = đội cứu hộ phản ứng nhanh.”**
</div>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
    1. Cấu trúc Try-Catch và Phân loại ngoại lệ
</h2>
<div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
    <p>
        Khối `try` chứa đoạn code có nguy cơ gây lỗi (ngoại lệ). Nếu lỗi xảy ra, khối `try` sẽ ngừng chạy và chương trình chuyển đến khối `catch` phù hợp để xử lý.
    </p>
    
  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
        Phân loại cơ bản
  </h3>
  <ul style="list-style-type: disc; padding-left: 20px;">
        <li>**Checked Exceptions:** Lỗi mà Java yêu cầu lập trình viên phải xử lý (ví dụ: `IOException` khi làm việc với file).</li>
        <li>**Unchecked Exceptions:** Lỗi xảy ra do lỗi logic lập trình và không bắt buộc phải xử lý (ví dụ: `NullPointerException`, `ArithmeticException`).</li>
   </ul>

  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Bắt lỗi chia cho 0 (`ArithmeticException`)</p>
</div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
try {
  // Đoạn code có thể gây lỗi
  int result = 5 / 0; 
  System.out.println("Kết quả: " + result); // Lệnh này KHÔNG BAO GIỜ chạy
} catch(ArithmeticException e) {
  // Khối này được kích hoạt khi lỗi ArithmeticException xảy ra
  System.err.println("Lỗi chia cho 0 đã xảy ra! Mã lỗi: " + e.getMessage());
}

System.out.println("Chương trình tiếp tục chạy bình thường.");
// Output: Lỗi chia cho 0 đã xảy ra!... Chương trình tiếp tục chạy bình thường.
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      2. Finally và Xử lý đa ngoại lệ
  </h2>
  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
      Khối Finally
  </h3>
  <div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
      <p>Khối `finally` chứa các lệnh **luôn được thực thi**, bất kể khối `try` có xảy ra lỗi hay không. Nó thường được dùng để giải phóng tài nguyên (đóng kết nối database, đóng file) nhằm đảm bảo hệ thống không bị rò rỉ.</p>
  </div>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
      Xử lý đa ngoại lệ (Multiple Catch)
  </h3>
  <div style="font-size: 1.25em; line-height: 1.8; margin-left: 15px;">
      <p>Bạn có thể sử dụng nhiều khối `catch` để xử lý các loại ngoại lệ khác nhau một cách riêng biệt.</p>
  </div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
try {
  // Giả sử có code đọc file và tính toán
  String name = null;
  name.length(); // Gây ra NullPointerException
} catch (NullPointerException e) {
  // Xử lý lỗi Null
  System.out.println("Lỗi: Đối tượng chưa được khởi tạo.");
} catch (Exception e) {
  // Bắt tất cả các loại lỗi còn lại (Phải đặt ở cuối)
  System.out.println("Lỗi chung khác: " + e.toString());
} finally {
  // Khối này LUÔN LUÔN chạy, dù có lỗi hay không
  System.out.println("Luôn chạy: Đóng kết nối file/database.");
}
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      3. Trải nghiệm học & Kết luận
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <ul style="list-style-type: disc; padding-left: 20px;">
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">✅ Thực hành nhiều lỗi thường gặp:</span> Cố ý tạo ra các lỗi như `ArrayIndexOutOfBoundsException`, `NumberFormatException` để thực hành bắt và xử lý chúng. Việc này giúp bạn **dễ nhớ** các loại Exception hơn.</li>
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">💡 Sử dụng `finally`:</span> Tập thói quen dùng `finally` khi làm việc với tài nguyên bên ngoài (file, network) để đảm bảo chương trình không làm rò rỉ tài nguyên.</li>
      </ul>
  </div>
  
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
      Exception Handling là kỹ năng bắt buộc để viết phần mềm chuyên nghiệp. Nó giúp chương trình của bạn không chỉ hoạt động đúng mà còn **duy trì sự ổn định và an toàn** khi gặp sự cố bất ngờ.
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