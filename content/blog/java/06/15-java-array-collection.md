---
title: "Mảng và Collection trong Java"
date: 2025-10-20T09:00:00+07:00
author: "Đăng Nguyễn Hải"
tags: ["Java","Mảng","Collection","Array","List","Feynman"]
featured_image: "/images/array.png"
draft: false
weight: 7
summary: "Mảng (Array) và Collection là hai công cụ chính giúp bạn **lưu trữ và quản lý nhiều giá trị cùng lúc** trong Java. Nắm vững hai khái niệm này là chìa khóa để xử lý dữ liệu quy mô lớn hơn một biến đơn lẻ. Mình học bằng phương pháp Feynman."
---

<div style="max-width: 950px; margin: 0 auto; padding: 0 10px;">
    
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px;">
      Mảng (Array) và Collection là hai công cụ chính giúp bạn **lưu trữ và quản lý nhiều giá trị cùng lúc** trong Java. Nắm vững hai khái niệm này là chìa khóa để xử lý dữ liệu quy mô lớn hơn một biến đơn lẻ. Mình học bằng phương pháp Feynman: 
  </p>
  
  <div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
      > **“Mảng = hộp nhiều ngăn cố định, Collection = tủ đồ linh hoạt có thể mở rộng.”**
  </div>

  <div style="text-align: center; margin-bottom: 40px;">
      <img src="/dangcode-blog/images/a_c.jpeg" alt="Java Array Collection" style="max-width: 90%; height: auto; border-radius: 10px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);">
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #007bff; border-bottom: 3px solid #e0f7fa; padding-bottom: 10px; margin-top: 50px; font-weight: 700; font-size: 2.0em;">
      1. Mảng (Array)
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>Mảng là một **cấu trúc dữ liệu có kích thước cố định**, dùng để lưu trữ các phần tử cùng kiểu dữ liệu (ví dụ: tất cả đều là `int`, hoặc tất cả đều là `String`). Mảng được truy cập thông qua **chỉ mục (index)** bắt đầu từ `0`.</p>
      
      <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
          Thao tác cơ bản với Mảng
      </h3>
  </div>
    
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
// Khai báo và khởi tạo mảng số nguyên
int[] numbers = {1, 2, 3, 4, 5};

// Truy cập phần tử (lấy giá trị ở index 0)
System.out.println("Phần tử đầu tiên: " + numbers[0]); // Output: 1

// Thay đổi giá trị
numbers[4] = 10; // Đặt giá trị 10 vào vị trí cuối cùng

// Duyệt mảng bằng vòng lặp For-Each
System.out.println("Các phần tử:");
for(int n : numbers){
    System.out.println(n);
}
</code>
</pre>

  <div style="padding: 15px; border-left: 5px solid #ff9800; background-color: #fff8e1; margin: 30px 0; font-size: 1.25em;">
      ⚠️ **Lưu ý quan trọng:** Kích thước của mảng được quyết định ngay khi tạo và không thể thay đổi sau đó. Nếu cố gắng truy cập chỉ mục nằm ngoài phạm vi (`numbers[5]`), chương trình sẽ bị lỗi `ArrayIndexOutOfBoundsException`.
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #4CAF50; border-bottom: 3px solid #e8f5e9; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      2. Collection Framework (Ví dụ: ArrayList)
  </h2>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <p>Collection là một tập hợp các interface và class giúp quản lý dữ liệu linh hoạt hơn. **`ArrayList`** là class thường dùng nhất, nó cung cấp một mảng động (Dynamic Array) với khả năng **tự động mở rộng kích thước** khi cần.</p>
      
      <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
          Thao tác cơ bản với ArrayList
      </h3>
  </div>
    
<pre style="background-color: #282c34; color: #abb2bf; padding: 1.5em; border-radius: 8px; overflow-x: auto; font-size: 1.1em; line-height: 1.6;">
<code class="language-java">
import java.util.ArrayList;

ArrayList<String> fruits = new ArrayList<>();
fruits.add("Táo");          // Thêm phần tử
fruits.add("Cam");
fruits.add("Xoài");

// Lấy kích thước hiện tại
System.out.println("Kích thước: " + fruits.size()); // Output: 3

// Thêm phần tử vào vị trí cụ thể (tự động dời các phần tử khác)
fruits.add(1, "Quýt");

// Xóa phần tử
fruits.remove("Táo");

// Lấy phần tử theo index
String cam = fruits.get(1); // Lấy Cam

System.out.println(fruits);
</code>
</pre>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #ff9800; border-bottom: 3px solid #fff3e0; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      3. So sánh nhanh và Trải nghiệm học
  </h2>
  
  <p style="font-size: 1.3em; font-weight: 600; margin-top: 25px;">So sánh Mảng và ArrayList:</p>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px; overflow-x: auto;">
      <table style="width: 100%; border-collapse: collapse; text-align: left;">
          <thead>
              <tr style="background-color: #f2f2f2;">
                  <th style="padding: 10px; border: 1px solid #ddd;">Tiêu chí</th>
                  <th style="padding: 10px; border: 1px solid #ddd; color: #007bff;">Mảng (Array)</th>
                  <th style="padding: 10px; border: 1px solid #ddd; color: #4CAF50;">Collection (ArrayList)</th>
              </tr>
          </thead>
          <tbody>
              <tr>
                  <td style="padding: 10px; border: 1px solid #ddd; font-weight: 600;">Kích thước</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Cố định, không thể thay đổi.</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Linh hoạt, tự động mở rộng.</td>
              </tr>
              <tr>
                  <td style="padding: 10px; border: 1px solid #ddd; font-weight: 600;">Kiểu dữ liệu</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Chứa cả Primitive và Reference.</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Chỉ chứa Object (Reference Types).</td>
              </tr>
              <tr>
                  <td style="padding: 10px; border: 1px solid #ddd; font-weight: 600;">Tốc độ</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Truy cập nhanh hơn (vì kích thước cố định).</td>
                  <td style="padding: 10px; border: 1px solid #ddd;">Thêm/Xóa nhanh hơn ở cuối, nhưng truy cập chậm hơn.</td>
              </tr>
          </tbody>
      </table>
  </div>

  <h3 style="color: #333; font-weight: 600; font-size: 1.5em; margin-top: 30px;">
      Trải nghiệm học của mình 🎓
  </h3>
  <div style="font-size: 1.25em; line-height: 1.8; margin-bottom: 30px;">
      <ul style="list-style-type: disc; padding-left: 20px;">
          <li>**Thực hành thêm xóa/sắp xếp:** Đây là cách duy nhất để hiểu được sự khác biệt về hiệu suất khi thao tác với Mảng và `ArrayList`.</li>
          <li>**Vẽ sơ đồ Feynman:** Sử dụng hình ảnh **Mảng = Ngăn hộp** (khóa chặt kích thước) và **ArrayList = Tủ đồ mở rộng** giúp mình dễ dàng hình dung khi nào nên sử dụng loại nào.</li>
      </ul>
  </div>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <h2 style="color: #e91e63; border-bottom: 3px solid #fce4ec; padding-bottom: 10px; margin-top: 40px; font-weight: 700; font-size: 2.0em;">
      4. Kết luận
  </h2>
  <p style="font-size: 1.3em; line-height: 1.8; margin-bottom: 30px; font-weight: 600;">
      Mảng & Collection là công cụ lưu trữ dữ liệu cơ bản và nâng cao, không thể thiếu trong bất kỳ chương trình Java nào. Hãy chọn đúng công cụ: dùng Mảng khi biết trước kích thước, dùng Collection khi cần sự linh hoạt.
  </p>

  <hr style="border: 0; height: 1px; background-color: #ddd; margin: 40px 0;">

  <div style="text-align:center; background:#f0f8ff; border-left:5px solid #007acc; border-radius:10px; padding:20px; font-size:1.2em; margin-bottom: 40px;">
      🎯 <strong>Chúc những ai đang đọc blog này luôn giữ được niềm đam mê học hỏi, kiên trì và sớm trở thành những lập trình viên Java vững vàng, tự tin bước vào thế giới công nghệ!</strong> 🚀  
      <p style="margin-top: 10px;"><em>— Đăng Nguyễn Hải</em></p>
  </div>
</div>