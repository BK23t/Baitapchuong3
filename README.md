LibraryMS v0.1 - Hệ Thống Quản Lý Thư ViệnDự án quản lý thư viện đơn giản được xây dựng bằng Python và Web Framework Flask.1. Cài đặt & Hướng dẫn khởi chạyYêu cầu tiên quyếtPython 3.xThư viện Flask (pip install flask)Lệnh khởi chạy ứng dụngMở Terminal tại thư mục dự án và chạy lệnh theo chuẩn yêu cầu:flask --app app run
Hoặc chạy trực tiếp bằng Python:python app.py
Sau khi khởi chạy, ứng dụng hoạt động tại địa chỉ: http://127.0.0.1:50002. Kiểm thử trên Trình duyệt (Browser URLs)Chức năngĐường dẫn (URL)Ghi chúTrang chủhttp://127.0.0.1:5000/Tổng số đầu sách và số sách sẵn sàng mượnDanh sách sáchhttp://127.0.0.1:5000/booksBảng danh sách sách kèm thanh liên kết lọc theo thể loạiLọc thể loạihttp://127.0.0.1:5000/books?category=Lập trìnhLọc danh sách sách thuộc thể loại "Lập trình"Chi tiết sáchhttp://127.0.0.1:5000/books/1Xem thông tin chi tiết sách có ID = 1Lỗi 404 HTMLhttp://127.0.0.1:5000/books/999Trang HTML thông báo lỗi 404 tùy biến kèm menu chung3. Lệnh curl Kiểm thử API JSONMở cửa sổ Terminal mới để thực thi các lệnh curl kiểm tra API:Lấy toàn bộ danh sách sách (API JSON):curl -X GET http://127.0.0.1:5000/api/books
Lấy thông tin sách theo ID hợp lệ (API JSON):curl -X GET http://127.0.0.1:5000/api/books/1
Lấy thông tin sách không tồn tại (Lỗi 404 JSON):curl -X GET http://127.0.0.1:5000/api/books/999
4. Hướng dẫn nộp bài Git & Tag v0.1Thực hiện các lệnh sau tại Terminal để commit và gắn tag đúng quy định:# Khởi tạo kho chứa
git init

# Thêm tất cả tập tin
git add .

# Tạo commit bài làm
git commit -m "Hoàn thành dự án LibraryMS v0.1"

# Gắn tag v0.1
git tag v0.1

# Đẩy mã nguồn và tag lên remote repository
git remote add origin https://github.com/<your-username>/libraryms.git
git push -u origin main
git push origin v0.1
