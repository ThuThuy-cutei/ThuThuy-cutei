---
title: "💡 Lập trình Hướng Đối Tượng (OOP) trong Java"
date: 2025-10-27T10:10:00+07:00
draft: false
author: "Vũ Thị Thu Thủy"
cover:
  image: "images/java-oop.png"
  alt: "Minh họa OOP trong Java"
  caption: "Nguồn: Vũ Thị Thu Thủy Blog"
  relative: true
  hidden: false
---

<h1 align="center" style="color:#e67e22; font-size:2.4rem; font-weight:800; text-shadow:1px 1px 4px rgba(0,0,0,0.1);">
💡 Lập trình Hướng Đối Tượng (OOP) trong Java
</h1>

---

## 📘 Giới thiệu

**OOP (Object-Oriented Programming)** – *Lập trình Hướng Đối Tượng* là **nền tảng cốt lõi của Java**.  
Thay vì viết mã lệnh rời rạc, OOP cho phép bạn mô phỏng thế giới thực bằng **đối tượng (object)** – nơi **dữ liệu** và **hành vi** được gói gọn bên trong **lớp (class)**.

> 🎯 Mục tiêu của OOP là giúp code **dễ đọc**, **dễ bảo trì**, **tái sử dụng** và **mở rộng linh hoạt**.

---

## 🎥 Video minh họa: OOP trong Java

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 12px; box-shadow: 0 0 10px rgba(0,0,0,0.15); margin-bottom: 20px;">
  <iframe 
      src="https://www.youtube.com/embed/qwPvkhemvHA"
      title="Video hướng dẫn OOP trong Java"
      style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen>
  </iframe>
</div>

---

## 🧩 1️⃣ Khái niệm cơ bản trong OOP

| Thuật ngữ | Mô tả |
|------------|--------|
| **Class (Lớp)** | Khuôn mẫu để tạo ra các đối tượng. |
| **Object (Đối tượng)** | Thực thể cụ thể được tạo ra từ lớp. |
| **Attribute (Thuộc tính)** | Dữ liệu mô tả đối tượng. |
| **Method (Phương thức)** | Hành vi hoặc chức năng của đối tượng. |

📘 Ví dụ:

```java
class Student {
    // Thuộc tính (attributes)
    String name;
    int age;

    // Phương thức (methods)
    void study() {
        System.out.println(name + " đang học lập trình Java.");
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student(); // Tạo đối tượng
        s1.name = "Thủy";
        s1.age = 21;
        s1.study();
    }
}
Kết quả:

css
Sao chép mã
Thủy đang học lập trình Java.
🧱 2️⃣ Encapsulation (Đóng gói)
Đóng gói nghĩa là che giấu dữ liệu bên trong lớp và chỉ cho phép truy cập thông qua các getter/setter.

java
Sao chép mã
class Account {
    private double balance; // chỉ nội bộ lớp truy cập

    public void setBalance(double amount) {
        if (amount > 0) balance = amount;
    }

    public double getBalance() {
        return balance;
    }
}
✅ Lợi ích:

Bảo vệ dữ liệu khỏi truy cập sai.

Dễ kiểm soát và bảo trì.

🧬 3️⃣ Inheritance (Kế thừa)
Kế thừa cho phép lớp con tái sử dụng thuộc tính và phương thức của lớp cha.

java
Sao chép mã
class Animal {
    void eat() {
        System.out.println("Đang ăn...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Gâu gâu!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();  // từ lớp cha
        dog.bark(); // của lớp con
    }
}
🧠 Giúp tái sử dụng code và tạo cấu trúc phân cấp dễ mở rộng.

🎭 4️⃣ Polymorphism (Đa hình)
Đa hình cho phép cùng một phương thức có hành vi khác nhau tùy đối tượng cụ thể.

java
Sao chép mã
class Shape {
    void draw() {
        System.out.println("Vẽ hình...");
    }
}

class Circle extends Shape {
    void draw() {
        System.out.println("Vẽ hình tròn 🟢");
    }
}

class Square extends Shape {
    void draw() {
        System.out.println("Vẽ hình vuông 🟥");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape s1 = new Circle();
        Shape s2 = new Square();

        s1.draw();
        s2.draw();
    }
}
Kết quả:

bash
Sao chép mã
Vẽ hình tròn 🟢
Vẽ hình vuông 🟥
💡 Giúp code linh hoạt – có thể mở rộng hành vi mà không cần sửa mã gốc.

🧠 5️⃣ Abstraction (Trừu tượng)
Trừu tượng nghĩa là chỉ hiển thị “những gì cần thiết”, ẩn đi chi tiết bên trong.

java
Sao chép mã
abstract class Vehicle {
    abstract void start(); // phương thức trừu tượng
}

class Car extends Vehicle {
    void start() {
        System.out.println("Xe hơi khởi động bằng chìa khóa.");
    }
}

class Bike extends Vehicle {
    void start() {
        System.out.println("Xe máy khởi động bằng nút bấm.");
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle v = new Car();
        v.start();
    }
}
🧩 Trừu tượng giúp thiết kế chương trình rõ ràng và giảm sự phức tạp.

🚀 6️⃣ Tổng kết
Nguyên lý OOP	Ý nghĩa chính	Ví dụ
Encapsulation	Bảo vệ dữ liệu, chỉ cho phép truy cập qua phương thức.	private, get/set
Inheritance	Tái sử dụng code, tạo mối quan hệ cha – con.	extends
Polymorphism	Một hành vi – nhiều cách thực hiện khác nhau.	method overriding
Abstraction	Ẩn chi tiết, chỉ cung cấp giao diện chính.	abstract class, interface

💬 Kết luận
Lập trình hướng đối tượng là linh hồn của Java.
Nắm vững 4 nguyên lý OOP giúp bạn:

Thiết kế hệ thống logic, rõ ràng

Giảm lỗi khi mở rộng dự án

Là nền tảng để học Spring Boot, Hibernate, Android và nhiều framework khác.

✨ “Học OOP không chỉ là học cú pháp – mà là học cách tư duy như một nhà phát triển chuyên nghiệp.”
— Vũ Thị Thu Thủy