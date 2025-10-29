---
title: "✨ ECMAScript 6 (ES6) – Kỷ nguyên mới của JavaScript"
date: 2025-10-27T11:10:00+07:00
draft: false
author: "Vũ Thị Thu Thủy"
cover:
  image: "images/javascript-es6.png"
  alt: "Hình ảnh minh họa ECMAScript 6"
  caption: "Nguồn: Vũ Thị Thu Thủy Blog"
  relative: true
  hidden: false
---
<h1 align="center" style="color:#2980b9; font-size:2.4rem; font-weight:800; text-shadow:1px 1px 4px rgba(0,0,0,0.1);"> ✨ ECMAScript 6 (ES6) – Kỷ nguyên mới của JavaScript </h1>
🌍 Giới thiệu
ECMAScript 6 (ES6) – hay còn gọi là ECMAScript 2015 – là bản nâng cấp lớn nhất trong lịch sử JavaScript.
Phiên bản này mang lại cú pháp hiện đại, tối ưu hiệu năng, và dễ bảo trì hơn, giúp JavaScript trở thành một ngôn ngữ mạnh mẽ thực thụ.

🎥 Video minh họa tổng quan về ES6
<div style="background: linear-gradient(135deg, #e3f2fd, #bbdefb); padding: 16px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); text-align:center; margin: 30px 0;"> <h2 style="color:#1565c0; font-weight:800; font-size:1.8rem; margin-bottom:12px;"> 🎬 Video giới thiệu ECMAScript 6 (ES6) </h2> <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 10px;"> <iframe src="https://www.youtube.com/embed/MFDXxCNqjKQ" title="Tổng quan về ECMAScript 6 (ES6)" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen> </iframe> </div> </div>
⚙️ 1. Khai báo biến với let và const
Trước ES6, chỉ có var, dễ gây lỗi vì phạm vi biến toàn cục.
Giờ đây, let và const ra đời, giúp code an toàn hơn và dễ kiểm soát phạm vi.

🔹 let – biến có phạm vi khối (block scope)
javascript
Sao chép mã
function exampleLet() {
  let x = 10;
  if (true) {
    let x = 20; // Biến mới trong khối if
    console.log("Trong khối if:", x); // 20
  }
  console.log("Ngoài khối if:", x); // 10
}
🔹 const – biến hằng (constant)
javascript
Sao chép mã
const PI = 3.14;
const user = { name: "Thủy" };
user.name = "Vũ Thủy"; // Được phép (chỉ ngăn gán lại object)
⚡ 2. Arrow Function (Hàm mũi tên)
Cú pháp ngắn gọn, dễ đọc và không có this riêng — cực kỳ hữu ích trong callback.

javascript
Sao chép mã
// Hàm truyền thống
const addTraditional = function(a, b) {
  return a + b;
};

// Arrow Function
const addArrow = (a, b) => a + b;
console.log(addArrow(5, 3)); // 8
👉 Ưu điểm: Không cần function, không cần return (nếu chỉ 1 dòng),
và this sẽ lấy theo phạm vi cha (lexical scope).

💬 3. Template Literals (Chuỗi mẫu)
Dễ dàng nối chuỗi và chèn biến bằng cú pháp ${variable}.

javascript
Sao chép mã
const item = "Laptop";
const price = 15000000;

const info = `Sản phẩm: ${item}
Giá: ${price.toLocaleString()} VNĐ`;

console.log(info);
✅ Có thể xuống dòng trực tiếp và đọc dễ hơn nhiều so với chuỗi truyền thống.

🧩 4. Destructuring (Phá vỡ cấu trúc)
Giúp trích xuất dữ liệu nhanh chóng từ Object hoặc Array.

javascript
Sao chép mã
// Object
const student = { name: "Vũ Thủy", age: 21, major: "CNTT" };
const { name, major } = student;

// Array
const colors = ["Đỏ", "Xanh", "Vàng"];
const [first, second] = colors;

console.log(name);   // Vũ Thủy
console.log(second); // Xanh
📦 5. Modules (import / export)
Giúp chia nhỏ chương trình thành các file độc lập – dễ quản lý, dễ tái sử dụng.

📁 math.js

javascript
Sao chép mã
export const PI = 3.14;
export function multiply(a, b) {
  return a * b;
}
📁 app.js

javascript
Sao chép mã
import { PI, multiply } from './math.js';
console.log("Kết quả:", multiply(3, 4)); // 12
🚀 6. Các tính năng hữu ích khác
Default Parameters – giá trị mặc định cho hàm

Spread / Rest Operator (...) – mở rộng hoặc gom nhóm dữ liệu

Promises / Async Await – xử lý bất đồng bộ gọn gàng hơn

Class syntax – cú pháp OOP rõ ràng, hiện đại

🎯 Tổng kết
ES6 là bước ngoặt quan trọng đưa JavaScript lên tầm ngôn ngữ lập trình hiện đại.
Nếu bạn nắm vững ES6, bạn sẽ dễ dàng tiếp cận các framework như React, Vue, hay Node.js.

💡 Hãy luyện tập bằng cách viết lại những đoạn code cũ theo cú pháp ES6 –
bạn sẽ cảm nhận ngay sự đơn giản, sạch sẽ và mạnh mẽ của ngôn ngữ này!