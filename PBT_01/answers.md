# Phần A: Đọc Hiểu

_Câu A1_

Khi gõ https://shopee.vn vào trình duyệt và nhấn Enter, thứ tự 5 bước xảy ra là:

1. Gửi Request: trình duyệt hỏi DNS Server "shopee.vn là IP nào?" và nhận về địa chỉ IP sau đó gửi yêu cầu đến Server thông qua mạng Internet
2. Server xử lý: "Trường muốn xem trang chủ shopee"
3. HTTP Response: Server sẽ gửi các file như html, css, js cho bên trình duyệt cũng thông qua mạng Internet
4. Parse html, css & execute js: Trình duyệt sẽ đọc các file html như bản kiến trúc, css như bản nội thất và xử lý js như lắp đặt hệ thống điện nước
5. Paint & render: Trình duyệt sẽ hoàn thiện và hiển thị giao diện lên trên màn hình cho Trường xem

Tab Network cho thấy toàn bộ các request mà trình duyệt gửi đi khi tải trang

![CauA1](./screenshots/cauA1.png)

_Câu A2_

Lỗi 1 — Dùng `<div>` thay vì thẻ semantic
Google không hiểu đâu là header, nav, main, footer. Với `<div class="header">` thì class "header" chỉ là tên cho con người đọc, máy không hiểu.

Lỗi 2 — Không có thẻ `<h1>` hay heading nào
Google dùng heading để hiểu nội dung chính của trang. Tên sản phẩm "iPhone 16 Pro" đang nằm trong `<div class="title">` — Google không biết đây là tiêu đề quan trọng.

Lỗi 3 — Thẻ `<img>` thiếu thuộc tính alt
Google đọc alt để hiểu ảnh nói về cái gì. Thiếu alt thì ảnh vô nghĩa với cả Google lẫn người dùng dùng screen reader.

Lỗi 4 — Menu điều hướng không dùng `<nav>`
Google ưu tiên `<nav>` để xác định cấu trúc điều hướng của trang. Dùng `<div class="menu">` thì Google không nhận ra đây là menu.
