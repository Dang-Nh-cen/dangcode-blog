---
title: "Java Input/Output (I/O): Làm việc với Console và File"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","I/O","File","Scanner","Feynman"]
featured_image: "/images/io.gif"
draft: false
weight: 11
summary: "Java I/O (Input/Output) là hệ thống giúp chương trình của bạn **đọc/ghi dữ liệu từ các nguồn bên ngoài** như file, console, hoặc kết nối mạng. Đây là khả năng giao tiếp cơ bản nhất của mọi ứng dụng."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
      Java I/O (Input/Output) là hệ thống giúp chương trình của bạn **đọc/ghi dữ liệu từ các nguồn bên ngoài** như file, console, hoặc kết nối mạng. Đây là khả năng giao tiếp cơ bản nhất của mọi ứng dụng.
  </p>
  
  <div style="text-align: center; margin-bottom: 40px;">
      <img src="/dangcode-blog/images/io-ins.gif" alt="Java IO" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
  </div>

  <div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
      Mình học bằng phương pháp Feynman: 
      > **“Input = nhận dữ liệu từ nguồn bên ngoài, Output = trả dữ liệu ra ngoài.”**
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
      1. Nhập/Xuất Console và Khái niệm Stream
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>Tất cả I/O trong Java đều dựa trên **Stream (Luồng)**. Stream là một chuỗi dữ liệu mà chương trình có thể đọc từ đó (Input Stream) hoặc ghi vào đó (Output Stream).</p>
      
  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
          Nhập dữ liệu từ Console bằng Scanner
    </h3>
      <p>Class **`Scanner`** là công cụ mạnh mẽ và dễ dùng nhất để đọc dữ liệu thô từ bàn phím (`System.in`) theo các kiểu dữ liệu khác nhau (số nguyên, chuỗi, số thực).</p>
      
  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">Ví dụ: Nhận và in tên người dùng</p>
  </div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
import java.util.Scanner;

public class ConsoleInput {
    public static void main(String[] args) {
        // Tạo đối tượng Scanner, dùng System.in (Input Stream từ bàn phím)
        Scanner sc = new Scanner(System.in); 
        
        System.out.print("Nhập tên của bạn: ");
        String name = sc.nextLine(); // Đọc toàn bộ dòng (bao gồm khoảng trắng)
        
        System.out.print("Nhập tuổi của bạn: ");
        int age = sc.nextInt(); // Đọc số nguyên

        System.out.println("Chào " + name + "! Bạn " + age + " tuổi.");
        sc.close(); // Quan trọng: Luôn đóng Scanner khi kết thúc
    }
}
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      2. Đọc/Ghi File: Character Streams và Byte Streams
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>Khi làm việc với file, Java chia thành hai loại Stream chính:</p>
      <ul style="list-style-type: disc; padding-left: 20px;">
          <li>**Byte Streams:** Dùng cho dữ liệu nhị phân (hình ảnh, video, âm thanh). Ví dụ: `FileInputStream`, `FileOutputStream`.</li>
          <li>**Character Streams:** Dùng cho dữ liệu văn bản (text files). Ví dụ: `FileReader`, `FileWriter`.</li>
      </ul>
      
  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
          Đọc File Văn bản bằng BufferedReader
      </h3>
      <p>Sử dụng **`BufferedReader`** giúp việc đọc file theo từng dòng trở nên hiệu quả hơn nhiều so với việc đọc từng ký tự một.</p>
  </div>
  
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
import java.io.*;

public class FileReadExample {
    public static void main(String[] args) throws IOException {
        // Chuẩn bị Stream: FileReader đọc từ file, BufferedReader đệm dữ liệu
        BufferedReader br = new BufferedReader(new FileReader("input.txt")); 
        String line;

        // Vòng lặp đọc từng dòng cho đến khi hết file (line == null)
        while((line = br.readLine()) != null){
          System.out.println(line);
        }
        
        // Quan trọng: Luôn đóng Stream để giải phóng tài nguyên hệ thống
        br.close(); 
    }
}
</code>
</pre>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
        Ghi dữ liệu vào File bằng PrintWriter
    </h3>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
import java.io.*;

public class FileWriteExample {
    public static void main(String[] args) throws IOException {
        // PrintWriter giúp ghi văn bản dễ dàng (tương tự System.out.println)
        PrintWriter writer = new PrintWriter(new FileWriter("output.txt"));
        
        writer.println("Dòng này được ghi vào file.");
        writer.printf("Giá trị: %d", 123);

        writer.close(); // Phải đóng để đảm bảo dữ liệu được ghi hết vào file
    }
}
</code>
</pre>


  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      3. Trải nghiệm học & Kết luận
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <ul style="list-style-type: none; padding-left: 0;">
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">✅ Thực hành nhiều ví dụ I/O:</span> Hãy tự viết một chương trình đơn giản: đọc tên và tuổi từ console, sau đó ghi thông tin đó vào một file mới. Điều này giúp bạn hiểu rõ luồng **Input/Output** thực tế.</li>
          <li style="margin-bottom: 15px;"><span style="font-weight: 600; color: #ff9800;">💡 Luôn nhớ đóng Stream:</span> Việc đóng `Scanner`, `BufferedReader`, `PrintWriter`, v.v., là cực kỳ quan trọng để tránh **rò rỉ tài nguyên hệ thống**.</li>
      </ul>
  </div>
  
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
      I/O là khả năng giao tiếp của chương trình với thế giới bên ngoài. Nắm vững cách quản lý Stream và xử lý file là nền tảng để bạn xây dựng mọi ứng dụng thực tế.
  </p>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:20px; font-size:1.2em; margin-bottom: 40px;">
      🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
      <p style="margin-top: 10px;"><em>— Đăng Nguyễn Hải</em></p>
  </div>
</div>