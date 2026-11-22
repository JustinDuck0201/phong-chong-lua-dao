# Thư mục file đọc thành tiếng

Các file MP3 hiện tại dùng giọng nữ HN - Ngọc Huyền từ Vbee. Tên file tương ứng với nội dung trong mảng `AUDIO_CONTENT` ở đầu phần JavaScript của `index.html`.

Khi thay bản ghi, giữ nguyên tên file. Nếu đổi tên, cập nhật thuộc tính `file` tương ứng trong mảng `AUDIO_CONTENT`. Giữ `text` đồng nhất với nội dung MP3 để làm phương án dự phòng.

Ví dụ: `ket-qua-thap.mp3`, `ket-qua-cao.mp3`, `dau-hieu-otp.mp3`.

Nếu MP3 thiếu hoặc không phát được, trang sẽ đọc phần `text` bằng giọng tiếng Việt đầu tiên mà trình duyệt cung cấp.
