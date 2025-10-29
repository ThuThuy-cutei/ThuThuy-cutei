---
title: "Java Stream API – Xử lý dữ liệu hiện đại"
date: 2025-10-27T10:25:00+07:00
draft: false
author: "Vũ Thị Thu Thủy"
cover:
  image: "images/java-stream.png"
  alt: "Hình ảnh minh họa về Java Stream API"
  caption: "Nguồn: Vũ Thị Thu Thủy Blog"
  relative: true
  hidden: false
---

# ☕ Java Stream API – Xử lý dữ liệu hiện đại trong Java


## 📹 Video minh họa chi tiết

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 12px; box-shadow: 0 0 10px rgba(0,0,0,0.15);">
  <iframe 
      src="https://www.youtube.com/embed/2StXP1XaU04" 
      title="Video hướng dẫn Java Stream API"
      style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
      allowfullscreen>
  </iframe>
</div>

---

## 💡 Tổng quan về Stream API

**Stream API** được giới thiệu từ **Java 8**, giúp việc xử lý dữ liệu trở nên ngắn gọn, hiện đại và dễ đọc hơn.  
Thay vì dùng vòng lặp truyền thống, bạn có thể **“luồng hóa”** dữ liệu và áp dụng các thao tác như `filter()`, `map()`, `collect()` để xử lý.

Stream cho phép bạn thực hiện các thao tác chuỗi (chaining operations) trên các tập hợp dữ liệu như `List` hoặc `Array` một cách khai báo, giúp code dễ hiểu và dễ bảo trì hơn.

---

## 🧩 Ví dụ cơ bản: Lọc và Chuyển đổi

Ví dụ sau đây minh họa cách sử dụng Stream để **lọc những người dùng trên 18 tuổi** và **thu thập tên của họ** thành một danh sách mới:

```java
import java.util.List;
import java.util.stream.Collectors;

// Giả sử có class User
// List<User> users = ... 

List<String> names = users.stream()
  .filter(u -> u.getAge() > 18)  // Thao tác trung gian (Intermediate Operation)
  .map(User::getName)            // Thao tác trung gian
  .collect(Collectors.toList()); // Thao tác kết thúc (Terminal Operation)
