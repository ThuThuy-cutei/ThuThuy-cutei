
<h1 align="center" style="color:#c2185b; font-size:2.4rem; font-weight:800; text-shadow:1px 1px 4px rgba(0,0,0,0.1);">
📝 Xử lý sự kiện (Event) trong JavaScript
</h1>

Sự kiện (Event) trong JavaScript giúp website phản hồi các hành động của người dùng như click chuột, nhập dữ liệu, cuộn trang, v.v. Nhờ event, bạn có thể biến trang web tĩnh thành một ứng dụng tương tác sinh động.

📺 Video Hướng Dẫn Chi Tiết

<!-- Nhúng video YouTube: https://www.youtube.com/watch?v=ax_tbXygZXQ -->

<div class="video-container" style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; background: #000; border-radius: 12px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
<iframe src="https://www.youtube.com/embed/ax_tbXygZXQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
</div>

1. Cơ chế Hoạt động của Event

Mỗi khi một hành động xảy ra trên trình duyệt (như tải trang, click chuột, nhấn phím), một "Event Object" sẽ được tạo ra. Event Listener (bộ lắng nghe sự kiện) được gán vào các phần tử DOM sẽ bắt sự kiện này và kích hoạt các hàm xử lý tương ứng.

1.1. Luồng sự kiện (Event Flow)

Sự kiện có ba giai đoạn:

Capturing Phase (Pha Chụp bắt): Sự kiện đi từ cửa sổ (window) xuống phần tử đích (target element).

Target Phase (Pha Đích): Sự kiện đến chính phần tử đã kích hoạt.

Bubbling Phase (Pha Nổi bọt): Sự kiện lan truyền ngược lại từ phần tử đích lên cửa sổ. (Đây là pha mặc định được sử dụng).

2. Các Cách Gán Event Listener

Có ba cách chính để gán một hàm xử lý cho sự kiện.

2.1. Gán qua thuộc tính HTML (Tuyệt đối KHÔNG nên dùng)

<button onclick="handleClick()">Click Me</button>


Phương pháp này làm lẫn lộn HTML và JavaScript, khó bảo trì.

2.2. Gán qua thuộc tính DOM Element

document.getElementById("btn").onclick = function() {
    console.log("Đây là cách gán cũ.");
    // Nhược điểm: Chỉ có thể gán MỘT hàm cho MỘT sự kiện (ví dụ: chỉ 1 hàm cho onclick).
};


2.3. Dùng addEventListener (Phương pháp chuẩn)

Đây là cách tốt nhất, cho phép gán nhiều hàm xử lý cho cùng một sự kiện trên cùng một phần tử.

// Ví dụ cơ bản
document.getElementById("btn").addEventListener("click", () => {
    // Sử dụng console.log() thay vì alert() để code chuyên nghiệp hơn
    console.log("1. Bạn vừa nhấn nút!");
});

// Bạn có thể gán thêm một hàm khác
document.getElementById("btn").addEventListener("click", () => {
    console.log("2. Hàm thứ hai được kích hoạt.");
});


3. Đối tượng Sự kiện (Event Object)

Khi một hàm xử lý sự kiện được kích hoạt, JavaScript tự động truyền vào một đối tượng gọi là Event Object. Đối tượng này chứa tất cả thông tin chi tiết về sự kiện vừa xảy ra.

document.addEventListener('mousemove', function(event) {
    // event là Event Object
    console.log("Tọa độ X:", event.clientX);
    console.log("Loại sự kiện:", event.type); // mousemove
});


3.1. Các Phương thức quan trọng

event.preventDefault(): Ngăn chặn hành động mặc định của trình duyệt (ví dụ: ngăn chặn việc gửi form khi nhấn nút submit).

event.stopPropagation(): Ngăn chặn sự kiện lan truyền (cả ở pha Capturing và Bubbling) đến các phần tử cha hoặc con.

Ví dụ về preventDefault()

const link = document.getElementById("myLink");

link.addEventListener('click', function(e) {
    // Ngăn chặn liên kết chuyển hướng đến URL
    e.preventDefault(); 
    console.log("Đã ngăn chặn hành vi mặc định của thẻ <a>.");
    // Thực hiện logic tùy chỉnh tại đây, ví dụ: mở modal
});
