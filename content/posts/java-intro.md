---
title: "Giới thiệu cơ bản về Java"
date: 2025-10-27T09:10:00+07:00
draft: false
author: "Vũ Thị Thu Thủy"
cover:
  image: "images/java-intro.png"
  alt: "images/java-intro.png"
  caption: "Nguồn: Vũ Thị Thu Thủy Blog"
  relative: true
  hidden: false
---
## ☕ Giới thiệu về **Java Cơ Bản**
---

---

Java là một ngôn ngữ lập trình hướng đối tượng mạnh mẽ, ổn định và phổ biến trên toàn thế giới.  
Nó được thiết kế với triết lý **“Write Once, Run Anywhere”** — viết một lần, chạy mọi nơi.  
Nhờ Java Virtual Machine (JVM), mã Java có thể chạy trên bất kỳ hệ điều hành nào mà không cần chỉnh sửa.

---

## 📹 Video giới thiệu Java cơ bản

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 12px; box-shadow: 0 0 10px rgba(0,0,0,0.15);">
  <iframe 
      src="https://www.youtube.com/embed/-vxX0KZaI9A"
      title="Video giới thiệu cơ bản về Java"
      style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen>
  </iframe>
</div>

---

Java cung cấp một hệ sinh thái phong phú gồm **thư viện chuẩn (Java Standard Library)** và hàng ngàn framework mạnh mẽ như **Spring**, **Hibernate**, **JavaFX**.  
Nó được ứng dụng trong các lĩnh vực:
- Phát triển ứng dụng web & server-side (Spring Boot)
- Ứng dụng di động (Android)
- Phần mềm doanh nghiệp
- Internet of Things (IoT)

### 💡 Mã ví dụ đơn giản
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Xin chào thế giới Java!");
    }
}
