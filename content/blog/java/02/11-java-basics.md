---
title: "Java cơ bản: Biến, kiểu dữ liệu và hằng số"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Cơ bản","Biến","Kiểu dữ liệu"]
featured_image: "/images/java_11.png"
draft: false
weight: 3
summary: "Java là ngôn ngữ **có kiểu dữ liệu tĩnh (statically typed)**, nghĩa là bạn phải khai báo rõ ràng kiểu dữ liệu cho mỗi biến trước khi sử dụng."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
<p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
        Java là ngôn ngữ **có kiểu dữ liệu tĩnh (statically typed)**, nghĩa là bạn phải khai báo rõ ràng kiểu dữ liệu cho mỗi biến trước khi sử dụng. Đây là nền tảng đầu tiên mà mọi lập trình viên Java cần nắm vững. Trong bài viết này, mình sẽ cùng nhau khám phá **biến (variables), kiểu dữ liệu (data types) và hằng số (constants)** trong Java bằng cách giải thích theo phương pháp Feynman!
            </p>

<div style="text-align: center; margin-bottom: 40px;">
        <img src="/dangcode-blog/images/java_11.png" alt="Java Basics" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
    </div>
    <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">
    <h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
        1. Biến (Variables) và Kiểu Dữ liệu (Data Types)
    </h2>
    <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
        <p>Trong Java, biến là tên của một vị trí trong bộ nhớ dùng để lưu trữ dữ liệu. Mỗi biến đều phải có một kiểu dữ liệu xác định. Java chia thành hai nhóm kiểu dữ liệu chính:</p>
                <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
            Nhóm 1: Kiểu dữ liệu nguyên thủy (Primitive Types)
        </h3>
        <p>Đây là 8 kiểu cơ bản, lưu trữ giá trị đơn lẻ, không phải là đối tượng.</p>
        <ul style="list-style-type: disc; padding-left: 20px;">
            <li>**Số nguyên:** `byte`, `short`, **`int`** (thường dùng nhất), `long`.</li>
            <li>**Số thực:** **`float`**, **`double`** (thường dùng nhất, độ chính xác cao hơn).</li>
            <li>**Ký tự:** **`char`** (lưu một ký tự đơn, ví dụ: 'A').</li>
            <li>**Logic:** **`boolean`** (chỉ lưu hai giá trị: `true` hoặc `false`).</li>
        </ul>
        
<h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
            Nhóm 2: Kiểu dữ liệu tham chiếu (Reference Types)
        </h3>
        <p>Các kiểu này không lưu trữ trực tiếp giá trị mà lưu địa chỉ của đối tượng trong bộ nhớ. Ví dụ điển hình là **`String`** và các **Class** bạn tự định nghĩa.</p>
     <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ khai báo biến:</p>
    </div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
int age = 21;                 // Biến số nguyên (tuổi)
double score = 9.5;           // Biến số thực (điểm số)
boolean passed = true;        // Biến logic (trạng thái đậu/rớt)
String name = "Đăng Hải";     // Biến tham chiếu (tên)
char firstInitial = 'N';      // Biến ký tự
</code>
</pre>

<div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
        <em>Feynman tip:</em> Biến giống như **hộp đựng đồ có dán nhãn** trong kho. Mỗi loại hộp (`int`, `double`, `String`) có dung tích và chỉ được phép chứa một loại nội dung nhất định. Nếu bạn cố gắng bỏ số vào hộp chỉ chứa chữ, Java sẽ báo lỗi!
    </div>

<hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
        2. Hằng số (Constants)
    </h2>
    <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
        <p>Trong Java, hằng số là một biến có giá trị **không thể thay đổi** sau khi được khởi tạo. Chúng ta dùng từ khóa **`final`** để khai báo hằng số. Quy ước đặt tên hằng số là viết hoa toàn bộ và phân cách bằng dấu gạch dưới (`_`).</p>
        
 <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ khai báo hằng số:</p>
</div>
    
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
// Hằng số PI
final double PI = 3.14159; 

// Hằng số đại diện cho một giá trị cố định
final int MAX_USERS = 1000;

// Lỗi nếu cố gắng thay đổi hằng số:
// PI = 3.14; // Lỗi biên dịch (Compile-time error)
</code>
</pre>

  <div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
        <em>Feynman tip:</em> Hằng số giống như **biển báo cố định** trên đường (ví dụ: tốc độ tối đa 60km/h), giá trị của nó đã được niêm phong và **không ai có thể thay đổi** trong suốt quá trình chạy chương trình.
    </div>

 <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

<h2 style="color: #e91e63; border-bottom: 3px solid #fce4ec; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
        3. Trải nghiệm và Phương pháp học hiệu quả
    </h2>
    <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
        <ul style="list-style-type: none; padding-left: 0;">
            <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #e91e63;">✅ Thực hành khai báo:</span> Cách tốt nhất để nắm vững kiểu dữ liệu là tự tay khai báo biến với nhiều kiểu khác nhau (`int`, `double`, `boolean`, `String`). Việc làm này sẽ giúp bạn nhớ lâu hơn về cú pháp và kích thước bộ nhớ của từng loại.</li>
            <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #e91e63;">🧠 Vẽ sơ đồ tư duy:</span> Hãy thử vẽ một sơ đồ cây (mind map) về các kiểu dữ liệu (Primitive -> Số nguyên, Số thực, Logic, Ký tự; Reference -> String, Class). Việc trực quan hóa giúp bộ não bạn xử lý thông tin nhanh hơn.</li>
            <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #e91e63;">❓ Đặt câu hỏi:</span> Luôn tự hỏi: "Tại sao tôi phải dùng `double` thay vì `int` ở đây?" hoặc "Dùng `final` ở đây có ý nghĩa gì?".</li>
        </ul>
    </div>

 <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

 <h2 style="color: #00bcd4; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
        4. Kết luận
    </h2>
    <ul style="font-size: 1.25em; line-height: 2.0; padding-left: 20px;">
        <li>Biến, kiểu dữ liệu và hằng số là **nền tảng bất di bất dịch** của mọi ngôn ngữ lập trình, đặc biệt là Java.</li>
        <li>Nắm vững **Java Virtual Machine (JVM)** và tính độc lập nền tảng là chìa khóa để hiểu Java.</li>
        <li>Áp dụng **phương pháp Feynman kết hợp thực hành liên tục** sẽ giúp bạn ghi nhớ lâu và hiểu sâu các khái niệm này một cách tự nhiên.</li>
    </ul>
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