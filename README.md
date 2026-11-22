# Phần mềm phòng chống lừa đảo

Website giáo dục an toàn số dạng tĩnh, có thể chạy trực tiếp trên trình duyệt hoặc xuất bản bằng GitHub Pages.

## Xuất bản bằng GitHub Pages

1. Tạo một repository công khai tên `phong-chong-lua-dao`.
2. Đưa `index.html` lên thư mục gốc của repository.
3. Vào **Settings → Pages**, chọn nhánh `main` và thư mục `/ (root)`, rồi lưu.
4. Sau khi GitHub Pages hoàn tất triển khai, mở URL được hiển thị trong trang Pages.

## Tính năng trong bản demo

- Kiểm tra văn bản/đường link bằng bộ quy tắc chạy ngay trong trình duyệt.
- Cảnh báo thủ đoạn, hướng dẫn an toàn và ví dụ minh họa.
- Đọc kết quả theo hàng đợi. Trang ưu tiên MP3 trong thư mục `audio/`, rồi dùng Web Speech API nếu thiếu file hoặc phát lỗi.
- Chỉ phát khi người dùng bấm; có tạm dừng, dừng và chọn tốc độ.
- Bộ MP3 thu sẵn sử dụng giọng nữ HN - Ngọc Huyền từ Vbee; các đoạn chính cho kết quả và dấu hiệu đã được đặt tên theo mã trong `AUDIO_CONTENT`.
- Biểu mẫu báo cáo chỉ mô phỏng giao diện; không gửi báo cáo đi.

## Giới hạn

Đây là bản demo tĩnh. Kết quả chấm điểm chỉ là đánh giá tham khảo, không đảm bảo phát hiện mọi hình thức lừa đảo. Website không dùng máy chủ hoặc API và không lưu nội dung người dùng nhập.
Web Speech API dùng giọng tiếng Việt đầu tiên trình duyệt cung cấp, như bản cũ. MP3 thu sẵn sẽ dùng chất giọng trong file.

## Thay file MP3

Đặt file ghi âm trong thư mục `audio/` với đúng tên `file` trong mảng `AUDIO_CONTENT` ở đầu phần JavaScript. Ví dụ: `audio/ket-qua-cao.mp3` và `audio/dau-hieu-otp.mp3`. Thay bản ghi bằng cách giữ nguyên tên file; nếu đổi tên, cập nhật thuộc tính `file`. Giữ `text` đồng nhất với nội dung MP3 để dự phòng khi file không phát được. Nếu trình duyệt không tải hoặc phát được MP3, trang sẽ chuyển sang giọng tiếng Việt có sẵn trên thiết bị.
