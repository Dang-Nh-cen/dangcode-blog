---
title: "Vòng lặp trong Java: for, while, do-while"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Vòng lặp","For","While","Feynman"]
featured_image: "/images/vong_lap.png"
draft: false
weight: 6
summary: "Vòng lặp (Loops) là tính năng cốt lõi, giúp chương trình của bạn thực hiện một hành động lặp đi lặp lại nhiều lần mà không cần viết lại cùng một đoạn mã. Nó giống như một con robot làm việc lặp lại."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
      Vòng lặp (Loops) là tính năng cốt lõi, giúp chương trình của bạn **thực hiện một hành động lặp đi lặp lại nhiều lần** mà không cần viết lại cùng một đoạn mã. Đây là cách để máy tính làm việc hiệu quả nhất.
  </p>
  
  <div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
      Hiểu đơn giản theo phương pháp Feynman: 
      > **“Vòng lặp giống như một con robot, làm đi làm lại cùng một công việc cho đến khi bạn bảo nó dừng.”**
  </div>

  <div style="text-align: center; margin-bottom: 40px;">
      <img src="/dangcode-blog/images/lopp.png" alt="Java Loops" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
      1. Vòng lặp `for`
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 20px;">
      <p>Sử dụng `for` khi bạn **biết trước số lần lặp** hoặc phạm vi giá trị cần duyệt. Cấu trúc của nó gói gọn mọi thông tin điều khiển vòng lặp trong một dòng duy nhất.</p>
      
  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
          🧩 Cấu trúc cơ bản
      </h3>
  </div>
    
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
for (khởi_tạo; điều_kiện; bước_nhảy) {
    // khối lệnh được lặp
}
</code>
</pre>
    
  <p style="font-size: 1.25em; font-weight: 600; margin-top: 25px;">🧠 Ví dụ 1: In các số từ 1 đến 5</p>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
for (int i = 1; i <= 5; i++) {
    System.out.println("Số thứ " + i);
}
// Giải thích:
// int i = 1  → Bắt đầu từ 1
// i <= 5     → Điều kiện lặp (khi i > 5, vòng lặp dừng)
// i++        → Sau mỗi lần lặp, tăng i lên 1
</code>
</pre>

  <p style="font-size: 1.25em; font-weight: 600; margin-top: 30px;">💡 Mẹo nhỏ:</p>
  <ul style="font-size: 1.25em; line-height: 1.8; padding-left: 20px;">
      <li>Sử dụng `for` khi bạn biết trước số lần lặp.</li>
      <li>Thường dùng để duyệt mảng, danh sách hoặc phạm vi giá trị.</li>
  </ul>

  <p style="font-size: 1.25em; font-weight: 600; margin-top: 30px;">🧩 Ví dụ 2: Duyệt qua mảng</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
int[] numbers = {10, 20, 30, 40, 50};

for (int i = 0; i < numbers.length; i++) {
    System.out.println("Phần tử thứ " + (i+1) + ": " + numbers[i]);
}
</code>
</pre>

  <p style="font-size: 1.25em; font-weight: 600; margin-top: 30px;">🧩 Ví dụ 3: Vòng lặp lồng nhau (Nested Loop)</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 2; j++) {
        System.out.println("Lần lặp i=" + i + ", j=" + j);
    }
}
// Vòng lặp bên ngoài chạy 3 lần, vòng lặp bên trong chạy 2 lần.
// Tổng cộng khối lệnh chạy 3 * 2 = 6 lần.
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      2. Vòng lặp `while`
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 20px;">
      <p>Sử dụng `while` khi bạn **không biết trước số lần lặp**, mà chỉ biết điều kiện để vòng lặp tiếp tục. `while` kiểm tra điều kiện **trước** khi chạy khối lệnh.</p>

      <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
          🧩 Cấu trúc cơ bản
      </h3>
  </div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
while (điều_kiện) {
    // khối lệnh được lặp
    // PHẢI CÓ câu lệnh làm thay đổi điều kiện
}
</code>
</pre>

  <p style="font-size: 1.25em; font-weight: 600; margin-top: 25px;">🧠 Ví dụ 1: In số từ 1 đến 5</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
int i = 1;
while (i <= 5) {
    System.out.println("Giá trị i: " + i);
    i++; // Nếu thiếu dòng này sẽ xảy ra Vòng lặp vô hạn (Infinite Loop)
}
</code>
</pre>
    
  <p style="font-size: 1.25em; font-weight: 600; margin-top: 30px;">🧩 Ví dụ 2: Nhập dữ liệu từ người dùng cho đến khi nhập “quit”</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
import java.util.Scanner;

public class InputExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input;

        // Vòng lặp vô hạn, nhưng có câu lệnh thoát (break)
        while (true) {
            System.out.print("Nhập lệnh (hoặc 'quit' để thoát): ");
            input = scanner.nextLine();

            if (input.equalsIgnoreCase("quit")) {
                break; // Thoát khỏi vòng lặp
            }
            System.out.println("Bạn vừa nhập: " + input);
        }
        System.out.println("Chương trình kết thúc!");
    }
}
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #e91e63; border-bottom: 3px solid #fce4ec; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      3. Vòng lặp `do-while`
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 20px;">
      <p>Đây là vòng lặp ít được dùng nhất. Điểm khác biệt mấu chốt là `do-while` kiểm tra điều kiện **sau** khi thực hiện khối lệnh. Điều này đảm bảo khối lệnh **luôn chạy ít nhất 1 lần**, kể cả khi điều kiện sai ngay từ đầu.</p>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
          🧩 Cấu trúc cơ bản
      </h3>
  </div>

<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
do {
    // khối lệnh được lặp (luôn chạy lần đầu)
} while (điều_kiện);
</code>
</pre>

  <p style="font-size: 1.25em; font-weight: 600; margin-top: 25px;">🧩 Ví dụ: Menu tương tác cơ bản</p>
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
import java.util.Scanner;

public class MenuExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice;

        do {
            System.out.println("====== MENU ======");
            System.out.println("1. Hiển thị lời chào");
            System.out.println("2. Thoát");
            System.out.print("Chọn: ");
            choice = scanner.nextInt();

            // Khối switch/case này luôn chạy ít nhất 1 lần
            switch (choice) {
                case 1:
                    System.out.println("Xin chào bạn!");
                    break;
                case 2:
                    System.out.println("Tạm biệt!");
                    break;
                default:
                    System.out.println("Lựa chọn không hợp lệ!");
            }
        } while (choice != 2); // Lặp lại cho đến khi người dùng chọn 2
    }
}
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      4. Tóm tắt nhanh và Trải nghiệm học
  </h2>

  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">So sánh các loại vòng lặp:</p>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px; overflow-x: auto;">
      <table style="width: 100%; border-collapse: collapse; text-align: left;">
          <thead>
              <tr style="background-color: #f2f2f2;">
                  <th style="padding: 10px; border: 1px solid #ddd;">Loại vòng lặp</th>
                  <th style="padding: 10px; border: 1px solid #ddd;">Khi nào dùng</th>
                  <th style="padding: 10px; border: 1px solid #ddd;">Kiểm tra điều kiện</th>
                  <th style="padding: 10px; border: 1px solid #ddd;">Ví dụ điển hình</th>
              </tr>
          </thead>
          <tbody>
              <tr>
                  <td style="padding: 10px; border: 1px solid #ddd;">`for`</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Biết trước số lần lặp</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Trước khi lặp</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Duyệt mảng, đếm từ 1 đến N</td>
              </tr>
              <tr>
                  <td style="padding: 10px; border: 1px solid #ddd;">`while`</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Không biết trước số lần lặp</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Trước khi lặp</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Nhập dữ liệu cho đến khi thỏa mãn điều kiện</td>
              </tr>
              <tr>
                  <td style="padding: 10px; border: 1px solid #ddd;">`do-while`</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Cần thực hiện ít nhất 1 lần</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Sau khi lặp</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Menu tương tác, xác nhận hành động ban đầu</td>
              </tr>
          </tbody>
      </table>
  </div>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
      Trải nghiệm học của mình 🎓
  </h3>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <ul style="list-style-type: disc; padding-left: 20px;">
          <li>**Viết thật nhiều ví dụ:** Thay đổi điều kiện và bước nhảy để xem chương trình phản ứng ra sao. Điều này giúp bạn tránh được lỗi **vòng lặp vô hạn**.</li>
          <li>**Vẽ sơ đồ flow trên giấy:** Giúp thấy rõ **“luồng chạy”** của chương trình, đặc biệt là sự khác biệt giữa `while` (kiểm tra trước) và `do-while` (kiểm tra sau).</li>
          <li>**Thử lồng vòng lặp:** Các bài toán in bảng cửu chương, vẽ hình chữ nhật sao bằng dấu `*` là cách tuyệt vời để củng cố kiến thức về vòng lặp lồng nhau.</li>
      </ul>
  </div>
  
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
      Vòng lặp là một trong những nền tảng quan trọng nhất. Khi hiểu được cách nó hoạt động, bạn có thể làm mọi thứ lặp lại theo ý muốn — từ in dữ liệu, duyệt mảng, đến xây dựng thuật toán phức tạp.
  </p>


<h2 style="color: #4CAF50; border-bottom: 3px solid #4CAF50; padding-bottom: 10px; margin-top: 40px; font-weight: 800; font-size: 2.2em; text-align: center;">
    🛠️ Test Code Với Java
</h2>

Hãy bắt đầu với đoạn mã đầu tiên của bạn

    {{< java_code_button src="https://517438ca-0c49-467b-b6f4-22a68a0abaa4-00-1k8m3q9oydb9e.kirk.replit.dev/" height="480px" >}}
  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:20px; font-size:1.2em; margin-bottom: 40px;">
      🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀 
      <p style="margin-top: 10px;"><em>— Đăng Nguyễn Hải</em></p>
  </div>
</div>