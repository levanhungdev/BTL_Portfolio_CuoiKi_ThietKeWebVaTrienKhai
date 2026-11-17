# Portfolio cá nhân

## Sản phẩm này là gì?
Website Portfolio cá nhân của Lê Văn Hùng (Sinh viên lớp 20-02 CNTT - Trường Đại học Đại Nam, đã hoàn thành chương trình Phát triển phần mềm tại FPT Aptech). Trang web tổng hợp thông tin cá nhân, mục tiêu nghề nghiệp, kỹ năng lập trình, kinh nghiệm thực tập thực tế tại VNATECH và danh sách các dự án phần mềm tiêu biểu. Sản phẩm được xây dựng bằng HTML5 và CSS3 thuần, phục vụ cho việc ứng tuyển vị trí Fresher Fullstack Developer và hoàn thành Bài tập lớn A3 học phần FIT4014.

## Demo
- URL website hoạt động (GitHub Pages): https://levanhungdev.github.io/BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai/
- Repository mã nguồn (GitHub): https://github.com/levanhungdev/BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai
- Phiên bản / Tag hiện tại: v1.0.0

## Tính năng
- Thanh điều hướng cố định (sticky header) hỗ trợ cuộn mượt tới 5 khu vực chính: Giới thiệu, Kỹ năng, Kinh nghiệm, Dự án và Liên hệ.
- Phần mở đầu (Hero) hiển thị thông tin định vị nghề nghiệp, các con số thống kê dự án và khung ảnh đại diện có cơ chế dự phòng chữ cái LH nếu ảnh gặp lỗi tải.
- Phân nhóm 4 mảng kỹ năng chuyên môn (Frontend, Backend, Database, Công cụ) và dòng thời gian (Timeline) quá trình học tập, thực tập.
- Danh sách dự án chia làm 3 nhóm (Dự án nổi bật, Dự án cá nhân, Dự án nhóm) kèm liên kết trực tiếp tới mã nguồn GitHub mở ở tab mới.
- Thiết kế đáp ứng (Responsive) tương thích tốt trên máy tính (1440px), máy tính bảng (768px) và điện thoại di động (375px).

## Cách mở
Cách 1: Mở trực tiếp trên trình duyệt qua đường dẫn GitHub Pages:
https://levanhungdev.github.io/BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai/

Cách 2: Chạy trên máy tính cá nhân:
1. Tải mã nguồn về máy bằng lệnh: git clone https://github.com/levanhungdev/BTL_Portfolio_CuoiKi_ThietKeWebVaTrienKhai.git
2. Mở thư mục dự án vừa tải về.
3. Nháy đúp vào tệp index.html để mở bằng trình duyệt web bất kỳ (Chrome, Edge, Firefox) hoặc mở qua tiện ích Live Server trong VS Code.

## Cấu trúc thư mục
BTL_CuoiKi/
- index.html: Tệp cấu trúc nội dung chính của website (HTML5 ngữ nghĩa)
- style.css: Tệp định dạng giao diện, màu sắc và bố cục Responsive (CSS3)
- assets/chandung.jpg: Ảnh đại diện cá nhân
- docs/: Thư mục chứa bản vẽ wireframe và ảnh chụp minh chứng kiểm thử
- README.md: Tài liệu giới thiệu và hướng dẫn mở website
- AI_LOG.md: Nhật ký khai báo quá trình hỏi và sử dụng công cụ AI
- CHANGELOG.md: Nhật ký ghi lại các lần cập nhật mã nguồn theo từng bản

## Đã kiểm tra
- Hiển thị giao diện và bố cục trên trình duyệt Chrome Desktop (kích thước 1440x900).
- Kiểm tra co giãn giao diện (Responsive) qua Chrome DevTools trên kích thước iPad (768px) và iPhone SE (375px), không bị tràn ngang.
- Kiểm tra thao tác bấm 5 liên kết trên thanh menu điều hướng, đảm bảo cuộn đúng vị trí và không bị thanh header che tiêu đề.
- Kiểm tra toàn bộ 7 liên kết GitHub ở phần Dự án và các nút Email, GitHub, Số điện thoại ở phần Liên hệ.
- Kiểm tra thực tế lỗi 404 ảnh đại diện trên GitHub Pages, sửa đường dẫn tương đối và kiểm tra lại ảnh hiển thị thành công.
- Đã thử trên iphone

## Hạn chế / Chưa kiểm tra
- Website tĩnh thuần túy nên chưa có chức năng gửi biểu mẫu liên hệ trực tiếp trên trang (hiện dùng giao thức mailto: để mở ứng dụng email mặc định).

## Khai báo AI
Xem chi tiết tại tệp AI_LOG.md