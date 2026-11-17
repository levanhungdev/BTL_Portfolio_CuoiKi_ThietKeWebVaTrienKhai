## AI LOG – BÀI TẬP LỚN A3 (FIT4014)

# Thông tin sinh viên
-Họ và tên: Lê Văn Hùng
-Mã sinh viên – Lớp: 2071020088 - 20-02 CNTT
-Ngày thực hiện: 17/11/2026
-Link repository: https://github.com/levanhungdev/BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai
-URL website: https://levanhungdev.github.io/BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai/
-Tình huống: Website của tôi

# Tình huống 1: Tối ưu bố cục Responsive cho thanh menu và giao diện điện thoại

1. Nhận định của tôi trước khi hỏi AI

-Trang/thao tác gặp lỗi: Thanh điều hướng (header) và bố cục 2 cột phần Hero, About, Projects khi thu nhỏ màn hình xuống dưới 860px và 640px.

-Mong muốn và hiện tượng thực tế: Muốn trên máy tính các phần chia 2 cột rõ ràng, nhưng khi mở trên màn hình điện thoại (375px) thì thanh menu không bị tràn ngang, ảnh đại diện đưa lên trên phần chữ và các thẻ dự án xếp thành 1 cột dọc dễ đọc.

-Dữ kiện đã kiểm tra: Trong style.css, khối .hero__inner và .about đang dùng grid-template-columns 2 cột; .header__inner đặt height: 64px cố định nên khi thu hẹp dưới 640px các mục menu bị ép sát và tràn khung.

-Tôi nghi nguyên nhân là: Thiếu các quy tắc @media query cho các mốc màn hình trung bình (860px) và màn hình nhỏ (640px), đồng thời chiều cao header cố định 64px không đủ chỗ khi menu xuống dòng.

-Vì sao tôi nhận định như vậy: Kiểm tra trực tiếp bằng công cụ Responsive trong DevTools (F12) của trình duyệt Chrome ở kích thước 375x667.

2. Tôi hỏi AI và nhận được gợi ý

-Nguồn: Công cụ AI: Gemini

-Câu hỏi/prompt tôi đã gửi: Tôi đang viết trang Portfolio bằng HTML5 và CSS3 thuần. Làm sao để chia lưới các thẻ kỹ năng và dự án tự co giãn mà không cần Bootstrap, đồng thời trên màn hình điện thoại dưới 640px thanh header xếp dọc gọn gàng và tiêu đề mục không bị header che khuất khi bấm menu?

-Gợi ý chính của AI: Dùng CSS Grid với repeat(auto-fill, minmax(280px, 1fr)) cho danh sách thẻ; thêm @media (max-width: 860px) để chuyển layout sang 1 cột và dùng order: -1 đưa ảnh đại diện lên trên; thêm @media (max-width: 640px) đổi .header__inner sang flex-direction: column, height: auto và tăng scroll-padding-top lên 110px.

3. Quyết định của tôi

-Chỉnh sửa gợi ý rồi áp dụng

-Tôi quyết định làm gì: Áp dụng cấu trúc @media query ở 2 mốc 860px và 640px, nhưng tự điều chỉnh lại kích thước khung ảnh đại diện (width: 220px trên mobile) và khoảng cách padding của từng section cho cân đối với nội dung thực tế.

-Lý do, dựa trên dữ kiện nào: Giải quyết đúng hiện tượng tràn menu ở màn hình 375px và đảm bảo khi bấm liên kết #about, #projects thì tiêu đề không bị thanh sticky header che mất.

4. Thực hiện và kiểm chứng

-Tệp/vị trí đã sửa (không sửa thì ghi rõ): style.css: phần .skills, .grid và khối @media (max-width: 860px), @media (max-width: 640px).

-Nội dung thay đổi hoặc cách xử lý khác: Chuyển bố cục 2 cột thành 1 cột ở màn hình <= 860px; đưa ảnh đại diện lên đầu trang ở mobile; cho phép thanh menu tự xuống dòng gọn gàng ở màn hình <= 640px và cập nhật scroll-padding-top: 110px.

-Commit của bản sửa: 7b92a31

-Bản sửa đã deploy: Có

-Kiểm tra Request URL và Status của tài nguyên liên quan:

-Trước xử lý: style.css tải thành công (Status 200), nhưng bố cục vỡ trên khung nhìn 375px.

-Sau xử lý/thử lại: style.css tải thành công (Status 200), giao diện hiển thị đúng trên cả 1440px, 768px và 375px.

-Kiểm tra giao diện/chức năng trên URL website:

-Trước xử lý: Menu bị tràn ngang ở màn hình 375px, tiêu đề mục bị che một phần khi bấm menu.

-Sau xử lý/thử lại: Menu xếp 2 hàng cân đối, các thẻ dự án xếp 1 cột dọc, không có thanh cuộn ngang.

-Cách thử lại và kết quả thực tế: Mở URL website bằng Chrome, bật DevTools chế độ thiết bị iPhone SE (375x667) và iPad (768x1024), bấm thử lần lượt 5 mục trên thanh điều hướng, đồng thời kiểm tra trực tiếp trên điện thoại iPhone. Kết quả cuộn mượt và hiển thị đầy đủ.

-Căn cứ để đối chiếu (URL tệp, commit, đường dẫn ảnh chụp hoặc dữ kiện quan sát): style.css, commit 7b92a31 và ảnh chụp docs/.

5. Kết luận

-Đã xử lý được

-Điều tôi rút ra hoặc việc cần làm tiếp: Khi làm sticky header thay đổi chiều cao trên mobile thì phải chỉnh lại scroll-padding-top tương ứng.

# Tình huống 2: Sửa lỗi không hiển thị ảnh đại diện (Status 404) khi triển khai lên GitHub Pages

1. Nhận định của tôi trước khi hỏi AI

-Trang/thao tác gặp lỗi: Khung ảnh đại diện ở phần Hero trên trang chủ sau khi đẩy lên GitHub Pages.

-Mong muốn và hiện tượng thực tế: Mong muốn hiển thị ảnh chân dung cá nhân (chandung.jpg), nhưng thực tế trên link GitHub Pages ảnh biến mất và chỉ hiện nền xanh cùng hai chữ cái viết tắt LH.

-Dữ kiện đã kiểm tra (cấu trúc tệp, Request URL, Status…): Mở DevTools (F12) tab Network thấy Request URL của ảnh là https://levanhungdev.github.io/assets/chandung.jpg với Status 404 (Not Found), trong khi tệp ảnh thực tế nằm trong thư mục của repository BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai.

-Tôi nghi nguyên nhân là: Do trong index.html đang viết đường dẫn bắt đầu bằng dấu gạch chéo /assets/chandung.jpg nên trình duyệt tìm từ thư mục gốc của tên miền thay vì thư mục con của dự án.

-Vì sao tôi nhận định như vậy: Khi mở file trực tiếp trên máy hoặc Live Server thì thư mục dự án là gốc nên ảnh hiện bình thường, nhưng lên GitHub Pages đường dẫn trang có thêm tên repository ở phía sau.

2. Tôi hỏi AI và nhận được gợi ý

-Nguồn: Công cụ AI: Gemini

-Câu hỏi/prompt tôi đã gửi: Trên máy cá nhân ảnh src="/assets/chandung.jpg" hiện bình thường nhưng khi deploy lên GitHub Pages lại báo lỗi 404 và nhảy về chữ LH. Cách sửa đường dẫn như thế nào cho đúng chuẩn?

-Gợi ý chính của AI:

-Xóa dấu gạch chéo / ở đầu đường dẫn để chuyển từ đường dẫn gốc sang đường dẫn tương đối: đổi src="/assets/chandung.jpg" thành src="assets/chandung.jpg".

3. Quyết định của tôi

-Chấp nhận gợi ý

-Tôi quyết định làm gì: Sửa thuộc tính src của thẻ img trong index.html từ "/assets/chandung.jpg" thành "assets/chandung.jpg".

-Lý do, dựa trên dữ kiện nào: Dữ kiện tab Network báo lỗi 404 do sai đường dẫn gốc trên môi trường subpath của GitHub Pages.

4. Thực hiện và kiểm chứng

-Tệp/vị trí đã sửa: index.html: dòng 60, thẻ img bên trong khối .avatar.

-Nội dung thay đổi hoặc cách xử lý khác: Đổi đường dẫn ảnh đại diện thành đường dẫn tương đối assets/chandung.jpg và đẩy commit lên nhánh main.

-Commit của bản sửa: faa3b8d

-Bản sửa đã deploy: Có

-Kiểm tra Request URL và Status của tài nguyên liên quan:

-Trước xử lý: Request URL: https://levanhungdev.github.io/assets/chandung.jpg

-Sau xử lý/thử lại: Request URL: https://levanhungdev.github.io/BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai/assets/chandung.jpg

-Kiểm tra giao diện/chức năng trên URL website:

-Trước xử lý: Chỉ hiển thị chữ LH, không có ảnh chân dung.

-Sau xử lý/thử lại: Hiển thị ảnh chân dung rõ nét trong khung tròn ở phần Hero.

-Cách thử lại và kết quả thực tế: Đợi GitHub Pages cập nhật xong bản deploy mới, mở trình duyệt ẩn danh truy cập lại URL website và bật tab Network kiểm tra. Ảnh tải thành công với mã 200.

-Căn cứ để đối chiếu (URL tệp, commit, đường dẫn ảnh chụp hoặc dữ kiện quan sát): index.html dòng 60, commit faa3b8d và ảnh chụp docs/.

5. Kết luận

-Đã xử lý được

-Điều tôi rút ra hoặc việc cần làm tiếp: Luôn sử dụng đường dẫn tương đối (không có dấu / ở đầu) cho tài nguyên tĩnh để trang web chạy đúng trên cả máy cục bộ lẫn GitHub Pages.