
<h1 align="center" style="color:#d32f2f; font-size:2.4rem; font-weight:800; text-shadow:1px 1px 4px rgba(0,0,0,0.1);">
⚡ Async/Await – Viết code bất đồng bộ như đồng bộ
</h1>

Lập trình bất đồng bộ (asynchronous) là khái niệm quan trọng trong JavaScript. Nó giúp code không bị "đơ" khi chờ các tác vụ tốn thời gian như tải dữ liệu, đọc file hay truy cập API.

Từ ES8, JS giới thiệu cú pháp async/await (được xây dựng trên Promises) giúp việc viết code bất đồng bộ trở nên dễ hiểu, sạch sẽ hơn và trông giống như code đồng bộ (synchronous) thông thường.

<h2 style="color:#ff6f00; font-size:1.8rem; font-weight:700; margin-top:30px; text-shadow:1px 1px 3px rgba(0,0,0,0.1);">
1️⃣ Promises – Nền tảng của Async/Await
</h2>

Trước khi có async/await, Promises là cách chuẩn để xử lý bất đồng bộ, giúp tránh tình trạng "Callback Hell".

Promise là một đối tượng đại diện cho việc hoàn thành (hoặc thất bại) của một thao tác bất đồng bộ.

Nó có ba trạng thái: pending (đang chờ), fulfilled (hoàn thành) và rejected (thất bại).

function delay(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}

delay(2000)
    .then(() => console.log("Đã đợi 2 giây!"))
    .catch(error => console.error("Có lỗi xảy ra:", error));

🎥 Video minh họa: Async/Await trong JavaScript </h2>

<div class="video-wrapper">
<h2 style="color:#d32f2f; text-align:center; font-size:1.5rem; margin-bottom:10px;"> 🎥 Async/Await chi tiết (nguồn: YouTube) </h2>
<div class="video-container" style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 12px;">
<!-- Đã sửa lỗi: URL nhúng trực tiếp -->
<iframe src="https://www.youtube.com/embed/670f71LTWpM" title="Async/Await trong JavaScript" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>
</div>


2️⃣ Cú pháp async và await </h2> <h3 style="color:#ff8f00; font-size:1.5rem; font-weight:600; margin-top:20px;">

2️.1. async Function </h2> <h3 style="color:#ff8f00; font-size:1.5rem; font-weight:600; margin-top:20px;">


Bạn phải đặt từ khóa async trước bất kỳ hàm nào muốn sử dụng await. Hàm async luôn trả về một Promise.

2.2. await Keyword

await chỉ có thể được sử dụng bên trong một hàm async.

Nó tạm dừng việc thực thi hàm async cho đến khi Promise ở phía trước nó được giải quyết (resolved) và trả về giá trị kết quả.

Ví dụ Thực tế (API Fetch)

// Hàm async luôn trả về Promise
async function loadData() {
    try {
        console.log("1. Bắt đầu gọi API...");
        

loadData();
// Lưu ý: Code sau khi gọi loadData() sẽ chạy ngay lập tức, 
// không bị blocking, vì loadData() là hàm bất đồng bộ.
console.log("5. Code tiếp theo chạy ngay lập tức.");


3. Xử lý Lỗi (Error Handling)

Khi sử dụng async/await, chúng ta sử dụng khối try...catch giống như xử lý code đồng bộ để bắt lỗi nếu Promise bị rejected. Điều này đơn giản và dễ quản lý hơn nhiều so với việc dùng .catch() liên tục.

Mọi lỗi bên trong hàm async (ví dụ: lỗi mạng, Promise bị reject) sẽ được bắt bởi khối catch.

async function safeLoadData(url) {
    try {
        const response = await fetch(url);
        

