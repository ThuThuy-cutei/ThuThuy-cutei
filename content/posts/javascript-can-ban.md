---
title: "Kiến thức cơ bản về JavaScript"
date: 2025-10-27T10:30:00+07:00
draft: false
author: "Vũ Thị Thu Thủy"
cover:
  image: "images/javascript-can-ban.png"
  alt: "Hình ảnh minh họa về JavaScript cơ bản"
  caption: "Nguồn: Vũ Thị Thu Thủy Blog"
  relative: true
  hidden: false
---
<h1 align="center" style="color:#f57c00; font-size:2.4rem; font-weight:800; text-shadow:1px 1px 4px rgba(0,0,0,0.1);"> ✨ Kiến thức cơ bản về JavaScript </h1>
🧩 Giới thiệu
JavaScript (JS) là ngôn ngữ lập trình phổ biến nhất cho web hiện đại.
Nếu HTML giúp tạo cấu trúc và CSS giúp định dạng giao diện, thì JavaScript chính là ngôn ngữ mang lại tính năng động,tương tác cho trang web.

JavaScript có thể:

Thay đổi nội dung và kiểu dáng của HTML, CSS.

Phản hồi các hành động của người dùng (click, nhập liệu, cuộn trang, v.v.).

Tương tác với server thông qua API.

Xây dựng ứng dụng web, mobile, desktop (với Node.js, React, Electron...).

<div style="background: linear-gradient(135deg, #fff3e0, #ffe0b2); padding: 16px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); text-align:center; margin: 30px 0;">
  <h2 style="color:#e65100; font-weight:800; font-size:1.8rem; margin-bottom:12px;">
    🎥 Video minh họa học JavaScript cơ bản
  </h2>

  <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 10px;">
    <iframe 
        src="https://www.youtube.com/embed/0LX_B3-0XuU?list=PL33lvabfss1yGrOutFR03OZoqm91TSsvs"
        title="Video hướng dẫn JavaScript cơ bản"
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen>
    </iframe>
  </div>
</div>
🔹 Cấu trúc một chương trình JavaScript
Một chương trình JS thường được viết trong thẻ <script> hoặc trong file .js riêng.

Ví dụ:

html
Sao chép mã
<!DOCTYPE html>
<html>
<head>
  <title>Học JavaScript cơ bản</title>
</head>
<body>
  <h2 id="demo">Xin chào!</h2>

  <script>
    document.getElementById("demo").innerText = "Xin chào JavaScript!";
  </script>
</body>
</html>
🧠 Kết quả: khi chạy trang HTML trên, dòng chữ "Xin chào!" sẽ tự động đổi thành "Xin chào JavaScript!" nhờ đoạn mã JS.

⚙️ Biến và Kiểu dữ liệu
JavaScript có ba cách khai báo biến:

javascript
Sao chép mã
var x = 10;     // kiểu cũ, có phạm vi toàn hàm
let y = 20;     // kiểu hiện đại, có phạm vi khối
const PI = 3.14; // hằng số không thể thay đổi
Kiểu dữ liệu phổ biến:

String → chuỗi ký tự

Number → số

Boolean → đúng / sai

Array → mảng

Object → đối tượng

🧮 Toán tử và Biểu thức
javascript
Sao chép mã
let a = 5;
let b = 2;
console.log(a + b); // 7
console.log(a * b); // 10
Các nhóm toán tử:

Toán tử số học: +, -, *, /, %

So sánh: ==, ===, !=, >, <

Logic: &&, ||, !

🔁 Cấu trúc điều khiển
If...else:
javascript
Sao chép mã
let age = 18;
if (age >= 18) {
  console.log("Bạn đủ tuổi!");
} else {
  console.log("Chưa đủ tuổi!");
}
Vòng lặp for:
javascript
Sao chép mã
for (let i = 1; i <= 5; i++) {
  console.log("Lần thứ " + i);
}
🧱 Hàm (Function)
Hàm giúp tái sử dụng mã:

javascript
Sao chép mã
function sayHello(name) {
  return "Xin chào, " + name + "!";
}

console.log(sayHello("Thủy"));
Hoặc viết theo cú pháp ES6 hiện đại:

javascript
Sao chép mã
const sayHello = name => `Xin chào, ${name}!`;
🧠 Tổng kết
Khái niệm	Mô tả ngắn
HTML	Xây dựng cấu trúc trang
CSS	Trang trí, định dạng
JavaScript	Tạo tương tác, xử lý logic
DOM	Giao diện kết nối giữa JS và HTML

💬 Kết luận:
JavaScript là nền tảng quan trọng cho mọi lập trình viên web.
Nắm vững JS cơ bản sẽ giúp bạn dễ dàng học nâng cao hơn như ES6, DOM, Event, Async, API, và các framework hiện đại như React, Vue, Angular.