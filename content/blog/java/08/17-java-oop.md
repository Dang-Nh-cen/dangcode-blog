---
title: "Lập trình hướng đối tượng nâng cao: Class, Inheritance, Polymorphism"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","OOP","Class","Inheritance","Polymorphism","Feynman"]
featured_image: "/images/class.jpg"
draft: false
weight: 9
summary: "Java là ngôn ngữ **hướng đối tượng (OOP) thuần túy**. Nắm vững các trụ cột của OOP như **Class, Object, Inheritance (Kế thừa), và Polymorphism (Đa hình)** là chìa khóa để xây dựng các ứng dụng lớn, có cấu trúc và dễ bảo trì."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
      Java là ngôn ngữ **hướng đối tượng (OOP) thuần túy**. Nắm vững các trụ cột của OOP như **Class, Object, Inheritance (Kế thừa), và Polymorphism (Đa hình)** là chìa khóa để xây dựng các ứng dụng lớn, có cấu trúc và dễ bảo trì.
  </p>
  
  <div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
      Mình học bằng phương pháp Feynman: 
      > **“Class = bản thiết kế, Object = sản phẩm, Inheritance = thừa kế bản thiết kế, Polymorphism = nhiều hình thái sản phẩm”.**
  </div>

  <div style="text-align: center; margin-bottom: 40px;">
      <img src="/dangcode-blog/images/oop.jpg" alt="Java OOP" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
      1. Class (Lớp) và Object (Đối tượng)
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>
          **Class** là bản thiết kế (blueprint) hoặc khuôn mẫu để tạo ra các đối tượng. Nó định nghĩa các **thuộc tính (variables)** và **hành vi (methods)** chung cho nhóm đối tượng đó.
      </p>
      <p>
          **Object** là thể hiện cụ thể (instance) của một Class. Nó là sản phẩm thực tế được tạo ra từ bản thiết kế đó.
      </p>
  </div>

  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Class Animal và Object dog</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
// 1. Bản thiết kế (Class)
class Animal {
  String name; // Thuộc tính (dữ liệu)
  
  void sound(){ // Hành vi (hàm)
    System.out.println("Some general sound"); 
  }
}

// 2. Sản phẩm thực tế (Object)
Animal dog = new Animal(); // Tạo Object
dog.name = "Husky";       // Truy cập thuộc tính
dog.sound();              // Gọi hành vi (Output: Some general sound)
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      2. Inheritance (Tính Kế thừa)
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>
          Kế thừa cho phép một Class (Class con/Subclass) **thừa hưởng** các thuộc tính và phương thức của một Class khác (Class cha/Superclass). Điều này giúp **tái sử dụng code** và tạo ra mối quan hệ *is-a* (là một) giữa các Class.
      </p>
      <p style="font-weight: 600;">Từ khóa: Java sử dụng từ khóa **`extends`** để thực hiện kế thừa.</p>
  </div>

  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Dog kế thừa từ Animal</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
class Dog extends Animal {
    // Dog tự động thừa kế thuộc tính 'name' và hàm 'sound()' từ Animal
    
    // Ghi đè (Override) hàm sound() của Class cha
    @Override
    void sound(){ 
        System.out.println("Woof Woof!"); 
    }
    
    void fetch() { 
        System.out.println("Dog is fetching the ball."); 
    }
}

// Sử dụng:
Dog myDog = new Dog();
myDog.name = "Pug"; // Thừa kế thuộc tính
myDog.sound();     // Output: Woof Woof! (Vì đã bị ghi đè)
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #e91e63; border-bottom: 3px solid #fce4ec; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      3. Polymorphism (Tính Đa hình)
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>
          Polymorphism (Đa hình) nghĩa đen là **"nhiều hình thái"**. Trong Java, nó cho phép một đối tượng có thể được tham chiếu bởi nhiều kiểu khác nhau (kiểu Class cha hoặc Interface mà nó triển khai).
      </p>
      <p>
          **Đa hình Runtime** (thường xảy ra với Ghi đè - Overriding) là dạng quan trọng nhất. Nó cho phép chương trình gọi đúng phương thức của Class con tại thời điểm chạy, ngay cả khi tham chiếu đang ở kiểu Class cha.
      </p>
  </div>

  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Đa hình Runtime</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
// Tham chiếu 'a' có kiểu là Animal, nhưng Object thực tế là Dog.
Animal a = new Dog(); 
Animal b = new Animal();

// Khi gọi hàm sound(), JVM biết phải gọi hàm sound() đã được ghi đè của Dog
a.sound(); // Output: Woof Woof! (Hành vi của Class con)

// Khi gọi hàm sound() của b, nó gọi hàm của Animal
b.sound(); // Output: Some general sound

// => Một tham chiếu (Animal) có thể có nhiều hình thái (Dog, Cat,...)
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      4. Trải nghiệm học & Kết luận
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <ul style="list-style-type: none; padding-left: 0;">
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">🧠 Vẽ sơ đồ OOP:</span> Luôn vẽ sơ đồ mối quan hệ giữa Class cha và Class con (mô hình cây gia phả) để dễ hiểu mối quan hệ **Inheritance**.</li>
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">✅ Thực hành Polymorphism:</span> Viết một hàm nhận tham số kiểu Class cha (`Animal`) nhưng truyền vào các Object Class con (`Dog`, `Cat`). Điều này giúp bạn ghi nhớ nhanh nguyên tắc Đa hình.</li>
      </ul>
  </div>

  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
      OOP giúp tổ chức code lớn dễ dàng, tạo tính tái sử dụng cao, và giúp chương trình của bạn linh hoạt, dễ mở rộng hơn trong tương lai.
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