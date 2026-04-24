Phần A
## Câu A1 – HTTP & Browser

### 1. Khi người dùng truy cập `https://shopee.vn` và nhấn Enter

Trình duyệt thực hiện các bước sau:

- Kiểm tra DNS cache để xem địa chỉ IP đã được lưu trước đó chưa.
- Nếu chưa có, trình duyệt gửi yêu cầu DNS để phân giải tên miền `shopee.vn` thành địa chỉ IP.
- Thiết lập kết nối TCP với máy chủ Shopee.
- Thực hiện bắt tay TLS để tạo kết nối HTTPS an toàn.
- Gửi HTTP Request đến máy chủ.
- Máy chủ xử lý và trả về HTTP Response chứa file HTML.
- Trình duyệt phân tích HTML, sau đó tiếp tục tải CSS, JavaScript, hình ảnh và các tài nguyên khác.
- Chrome xây dựng DOM, CSSOM, Render Tree và hiển thị trang web lên màn hình.

**Nguồn tham chiếu:** `01_introduction_html_universe.md` – phần *How the Web Works*.

---

### 2. Tab Network trong Chrome DevTools hiển thị

- Danh sách tất cả các request gửi tới máy chủ.
- HTTP Method (GET, POST, ...).
- Status Code của từng request.
- Loại tài nguyên (HTML, CSS, JavaScript, Image, ...).
- Kích thước dữ liệu tải xuống (Size).
- Thời gian tải của từng request (Time).
- Tổng thời gian tải trang (Finish).
- Waterfall timeline thể hiện thứ tự và thời gian thực hiện các request.

**Nguồn tham chiếu:** `01_introduction_html_universe.md` – phần *Chrome DevTools > Network  Tab*.

#A2.
    Trang web dưới đây bị Google đánh giá SEO thấp vì lạm dụng <div>.
    Lỗi 1: Không dùng <header> cho phần đầu trang mà dùng <div>: <div class="header">
    Lỗi 2: Không dùng <nav> cho menu mà dùng <div class="menu">
    Lỗi 3: Không dùng <main> cho nội dung chính mà dùng <div class="main">
    Lỗi 4: Không dùng <article> cho sản phẩm mà dùng  <div class="product">
    Dùng <p> để chứa 1 đoạn văn thay vì <div class="price">25.990.000đ</div>
    Nên dùng <footer> thay vì <div class="footer">© 2026 ShopTLU</div>
    Sửa lại:
    <header>
        <div class="logo">ShopTLU</div>
        <nav>
            <a href="/">Trang chủ</a>
            <a href="/products">Sản phẩm</a>
        </nav>
    </header>

    <main>
       <article class="product">
        <h1>iPhone 16 Pro</h1>
        <p class="price">25.990.000đ</p>
        <img src="iphone.jpg" alt= "iPhone 16 Pro">
       </article>
    </main>

    <footer>
        <p>© 2026 ShopTLU</p>
    </footer>

#A3.
    Do thẻ <div> là thẻ block, chiếm cả dòng nên khi đóng thẻ </div> thì sẽ phải xuống dòng mới để viết, còn các thẻ <span> và <strong> là các thẻ inline, chỉ chiếm phần nội dung nằm trong thẻ nên khí đóng 2 thẻ này vẫn có thể viết tiếp nội dung nằm cạnh nhau trên dòng đó hoặc xuống dòng mới để viết.
    Text art:
        Hộp 1
        Text A Text B
        Hộp 2
        Text C Text D
        Hộp 3

#A4.
    <thead>: Là phần đầu bảng, chứa tiêu đề cột
    <tbody>: Là phần nội dung chính của bảng, dùng để chứa dữ liệu chính của bảng
    <tfoot>: Là phần cuối bảng dùng để chứa các kết luận, thống kê, tổng kết của bảng
    KHÔNG NÊN dùng table để tạo layout trang web vì:
    - Table dùng để chứa dữ liệu bảng, không phải để chia layout web
    - Table phải load xong toàn bộ mới hiển thị đúng nên trang web sẽ bị tải chậm
    - 

# Bài B3 – Debug HTML

## Danh sách lỗi đã sửa

- Lỗi 1: Dòng 1 — Khai báo DOCTYPE thiếu `html` — Sửa thành `<!DOCTYPE html>`.
- Lỗi 2: Dòng 4 — Thẻ `<title>` chưa đóng — Thêm `</title>`.
- Lỗi 3: Dòng 5 — Giá trị charset sai chuẩn (`utf8`) — Sửa thành `UTF-8`.
- Lỗi 4: Dòng 9 — Thẻ `<h1>` đóng sai (`<h1>` thay vì `</h1>`) — Sửa lại đúng cú pháp.
- Lỗi 5: Dòng 13 — Thẻ `<a>` đầu tiên chưa đóng — Thêm `</a>`.
- Lỗi 6: Dòng 21 — Thuộc tính `src` của ảnh thiếu dấu ngoặc kép.
- Lỗi 7: Dòng 21 — Thẻ `<img>` thiếu thuộc tính `alt`.
- Lỗi 8: Dòng 23 — Thẻ `<b>` lồng sai vị trí với thẻ `<p>`.
- Lỗi 9: Dòng 39 — Tài liệu có hai thẻ `<main>`, vi phạm semantic HTML — Đổi thẻ thứ hai thành `<aside>`.
- Lỗi 10: Dòng 45 — Thẻ `<p>` trong footer chưa được đóng.
- Lỗi 11: Bảng sử dụng `<td>` cho hàng tiêu đề — Nên dùng `<th>` để đúng ngữ nghĩa HTML.