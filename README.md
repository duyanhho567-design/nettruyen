# MangaVN - phiên bản có backend

## Chạy
1. Cài Node.js 18+.
2. Mở terminal tại thư mục này.
3. Chạy `npm install`.
4. Chạy `npm start`.
5. Mở http://localhost:3000

## Admin mặc định
- username: `admin`
- password: `admin123`
- Nên đặt biến môi trường `ADMIN_PASSWORD` trước lần chạy đầu tiên.

## Đã thay thế localStorage
- SQLite lưu users/comics/chapters/pages/comments/settings.
- Mật khẩu được hash bằng bcrypt.
- Session bằng cookie httpOnly.
- Ảnh lưu thành file trong `uploads/`, database chỉ lưu đường dẫn.
- Admin kiểm tra ở server, không tin quyền từ trình duyệt.
- Comment lưu trên server và dùng chung cho mọi người.
- Mỗi truyện có nhiều chương; mỗi chương có tối đa 100 ảnh trong một lần upload.
