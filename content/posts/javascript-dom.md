---
title: "🌐 Hiểu về DOM trong JavaScript"
date: 2025-10-27T10:10:00+07:00
draft: false
author: "Vũ Thị Thu Thủy"
cover:
  image: "images/javascript-dom.png"
  alt: "Hình ảnh minh họa về DOM trong JavaScript"
  caption: "Nguồn: Vũ Thị Thu Thủy Blog"
  relative: true
  hidden: false
---

<h1 align="center" style="color:#27ae60; font-size:2.3rem; font-weight:800; text-shadow:1px 1px 4px rgba(0,0,0,0.1);">
🌐 Hiểu về DOM trong JavaScript
</h1>

---

## 📘 Giới thiệu

**DOM (Document Object Model)** là **mô hình đối tượng tài liệu** – cách mà trình duyệt biểu diễn cấu trúc của trang web.  
Mỗi phần tử HTML (như `<p>`, `<div>`, `<img>`) đều là **một nút (node)** trong cây DOM.

Nhờ DOM, JavaScript có thể:
- Truy cập, thay đổi nội dung và thuộc tính của phần tử.
- Thêm hoặc xóa phần tử HTML.
- Xử lý các sự kiện người dùng như click, nhập liệu, cuộn trang...

> 💡 Nói cách khác: DOM là “cầu nối” giữa **HTML (giao diện)** và **JavaScript (hành vi)**.

---

## 🎬 Video minh họa DOM trong JavaScript

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 12px; box-shadow: 0 0 10px rgba(0,0,0,0.15); margin-bottom: 20px;">
  <iframe 
      src="https://www.youtube.com/embed/TsTr-tKCREc"
      title="Video hướng dẫn DOM trong JavaScript"
      style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen>
  </iframe>
</div>

---

## 🧩 1️⃣ Cấu trúc cây DOM

Ví dụ, HTML sau:

```html
<html>
  <body>
    <h1>Xin chào!</h1>
    <p>Đây là ví dụ về DOM.</p>
  </body>
</html>
