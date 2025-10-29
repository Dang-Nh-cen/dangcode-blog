---
title: "Hàm, Overloading và Parameter Passing trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Hàm","Function","Overloading","Feynman"]
featured_image: "/images/ham.jpg"
draft: false
weight: 8
summary: "Trong lập trình Java, **Hàm (Method)** là công cụ cốt lõi giúp bạn **tổ chức code thành các khối nhỏ logic, dễ quản lý và tái sử dụng**. Cùng với **Overloading** và **Parameter Passing**, hàm giúp code của chúng ta trở nên mạnh mẽ và linh hoạt hơn rất nhiều."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
      Trong lập trình Java, **Hàm (Method)** là công cụ cốt lõi giúp bạn **tổ chức code thành các khối nhỏ logic, dễ quản lý và tái sử dụng**. Cùng với **Overloading** và **Parameter Passing**, hàm giúp code của chúng ta trở nên mạnh mẽ và linh hoạt hơn rất nhiều.
  </p>
  
  <div style="text-align: center; margin-bottom: 40px;">
      <img src="/dangcode-blog/images/func.png" alt="Java Functions" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
      1. Hàm (Method) cơ bản
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>Hàm là một khối lệnh thực hiện một nhiệm vụ cụ thể. Việc sử dụng hàm giúp chương trình trở nên module hóa (chia nhỏ), dễ đọc, dễ kiểm thử và sửa lỗi hơn.</p>
      
  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Hàm tính tổng đơn giản</p>
  </div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
// Khai báo hàm sum nhận hai tham số int và trả về tổng
public static int sum(int a, int b){
  return a + b; // Trả về kết quả
}

// Sử dụng hàm
int result = sum(10, 5); // result = 15
</code>
</pre>

<div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
    <em>Feynman tip:</em> Hàm giống như một **“robot thực hiện nhiệm vụ”**. Bạn giao cho nó đầu vào (tham số), nó làm công việc (khối lệnh), và trả lại kết quả (`return`).
</div>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
    2. Overloading (Nạp chồng hàm)
</h2>
<div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
    <p>Overloading là khả năng cho phép nhiều hàm **có cùng tên** tồn tại trong một Class, miễn là chúng có **danh sách tham số (parameter list) khác nhau**. Khác biệt có thể là về số lượng tham số hoặc kiểu dữ liệu của tham số.</p>
    <p style="font-weight: 600;">Lưu ý: Kiểu trả về (return type) không làm nên sự khác biệt của Overloading.</p>

  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Hàm tính tổng linh hoạt</p>
</div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
// 1. Tính tổng 2 số nguyên
int sum(int a, int b){ return a + b; } 

// 2. Tính tổng 2 số thực (Overloading dựa trên kiểu dữ liệu)
double sum(double a, double b){ return a + b; } 

// 3. Tính tổng 3 số nguyên (Overloading dựa trên số lượng tham số)
int sum(int a, int b, int c){ return a + b + c; }

// Khi gọi hàm, Java tự động xác định hàm nào nên được gọi dựa vào kiểu dữ liệu bạn truyền vào.
</code>
</pre>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #e91e63; border-bottom: 3px solid #fce4ec; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
    3. Parameter Passing (Truyền tham số)
</h2>
<div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
    <p>Đây là một khái niệm cực kỳ quan trọng, quyết định hàm có thể thay đổi giá trị gốc của biến bên ngoài nó hay không.</p>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
        Luật vàng của Java: Pass-by-Value
  </h3>
  <p>Java **luôn sử dụng cơ chế Pass-by-Value** (truyền theo giá trị), nhưng cách hoạt động khác nhau tùy theo loại biến:</p>

  <ul style="list-style-type: disc; padding-left: 20px;">
        <li>**Kiểu nguyên thủy (int, double, boolean):** Hàm nhận **một bản sao** giá trị gốc. Mọi thay đổi bên trong hàm sẽ không ảnh hưởng đến biến gốc bên ngoài.</li>
        <li>**Kiểu tham chiếu (Object, Array):** Hàm nhận **một bản sao của tham chiếu** (địa chỉ bộ nhớ) của Object. Vì cả tham chiếu gốc và bản sao đều trỏ đến **cùng một Object** trong bộ nhớ, nên bạn **có thể thay đổi nội dung** (state) của Object đó. Tuy nhiên, bạn không thể làm cho tham chiếu gốc trỏ đến một Object mới.</li>
  </ul>
</div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
public static void modifyNumber(int num) {
    num = 100; // Thay đổi bản sao, không ảnh hưởng biến gốc
}

// Giả sử có Class MyObject { int value; }
public static void modifyObject(MyObject obj) {
    obj.value = 200; // Thay đổi nội dung của Object gốc (ĐƯỢC)
}

// KHÔNG THỂ thay đổi tham chiếu gốc:
// public static void reassignObject(MyObject obj) {
//     obj = new MyObject(); // Bản sao tham chiếu trỏ đến Object mới, Gốc không bị ảnh hưởng
// }
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      4. Trải nghiệm học & Kết luận
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <ul style="list-style-type: none; padding-left: 0;">
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">✅ Viết nhiều hàm khác nhau:</span> Luôn nghĩ về hàm như một robot chuyên biệt. Việc viết nhiều hàm giúp bạn nắm được quy tắc khai báo, tham số, và kiểu trả về.</li>
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">🧠 Thử Overloading:</span> Hãy thử viết 5 hàm có cùng tên, chỉ khác nhau về tham số. Điều này giúp bạn ghi nhớ sự khác biệt và nguyên lý hoạt động của Overloading.</li>
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">💡 Thực hành Pass-by-Value:</span> Viết một chương trình nhỏ để kiểm tra cả kiểu nguyên thủy và Object để chứng minh "Luật vàng" của Java: **luôn là Pass-by-Value**.</li>
      </ul>
  </div>

  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
      Hàm và Overloading giúp tổ chức code hiệu quả, còn việc hiểu Parameter Passing là nền tảng để tránh các lỗi logic phức tạp trong các dự án lớn.
  </p>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:20px; font-size:1.2em; margin-bottom: 40px;">
      🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
      <p style="margin-top: 10px;"><em>— Đăng Nguyễn Hải</em></p>
  </div>
</div>