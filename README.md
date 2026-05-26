# Capcut With AI (v0.9.7)

**Capcut With AI** là một ứng dụng hỗ trợ biên tập và cắt ghép video thông minh (Talking Head, Vlog, Podcast) cho phần mềm **CapCut Desktop**.

Bằng cách can thiệp trực tiếp vào file nháp của CapCut, Capcut With AI mang đến bộ 3 công cụ tự động hóa mạnh mẽ: SmartCut (tự động cắt bỏ vấp/lặp và tua nhanh khoảng lặng), Subtitle with AI (nhận diện và dịch phụ đề đa ngôn ngữ siêu tốc bằng AI), và ReScript with AI (tự động phân tích, viết lại kịch bản và cắt ghép thành video Shorts viral). Tất cả được xử lý trực tiếp vào project Capcut

---

## ⚡ Các Tính năng Nổi bật

### 1. Quản lý Dự án CapCut Thông minh & Tiện lợi
* **Tự động Tìm kiếm nháp:** Tự động dò tìm thư mục lưu trữ dự án nháp mặc định của CapCut Desktop ngay trong lần chạy đầu tiên.
* **Tốc độ Tải danh sách Siêu tốc:** Khởi động và tải danh sách dự án tức thì (< 0.5 giây cho hơn 600 dự án).
* **Tìm kiếm Thời gian thực:** Bộ lọc tìm kiếm cực nhạy, phản hồi ngay lập tức khi gõ tên dự án.

### 2. Cấu hình Cắt ghép Thông minh (SmartCut)
* **Tự động Kiểm tra Phụ đề:** Tự động đọc và kiểm tra trạng thái phụ đề của dự án (mở khóa SmartCut nếu có phụ đề).
* **Tùy chỉnh Tốc độ (Speed Sliders):** Hỗ trợ 3 thanh trượt điều chỉnh tốc độ vô cùng trực quan (Tăng tốc đoạn có thoại, Tăng tốc âm thanh, Tăng tốc khoảng lặng).
* **Bảo toàn thành phần timeline tuyệt đối 🛡️**: Đảm bảo hoàn toàn **không có bất kỳ phân đoạn video, âm thanh gốc, phụ đề hay sticker nào** bị xóa đi. Các khoảng lặng và phân đoạn thoại chỉ được thực hiện tua nhanh (timelapse) hoặc đồng bộ tốc độ.

### 3. Tạo & Dịch phụ đề tự động bằng AI (Subtitle with AI)
* **Tích hợp Whisper API của Groq:** Tạo phụ đề tiếng Việt siêu chuẩn xác và cực nhanh.
* **Tùy chọn Dịch Phụ đề A.I:** Tích hợp dịch thuật thông minh với **Gemini API** (Hỗ trợ Tiếng Việt, Anh, Trung, Nhật, Hàn, Pháp, Đức).
* **Phân tách Dòng Phụ đề Độc lập:** Phụ đề gốc và phụ đề dịch được phân thành 2 luồng độc lập, bạn có thể đổi style cho từng loại mà không ảnh hưởng loại kia.

### 4. Tự động ReScript & Cắt ghép video bằng AI (ReScript with AI) 📝
Khả dụng với **tất cả các mô hình Gemini**.
* **Chế độ Marker an toàn & Cặp Marker Đầu/Cuối 📌**: Phần mềm chèn các cặp Marker chỉ dẫn rõ ràng (Bắt đầu = Xanh lá, Kết thúc = Đỏ) để bạn dễ dàng biên tập thủ công.

### 5. Tự động Cập nhật Phiên bản Mới 🚀
* Ứng dụng tích hợp luồng kiểm tra và tự động tải về cài đặt các phiên bản mới hoàn toàn tự động, giải nén và khởi động lại siêu mượt mà với giao diện Cyberpunk chuyên nghiệp.

### 6. Tự động Tạo bản sao Dự án - Safe Backup Mode 🛡️
* Nhấn tùy chọn nhân bản trước khi chạy SmartCut/ReScript, phần mềm sẽ sao lưu toàn bộ timeline của bạn chưa tới 0.5s, bảo vệ 100% thành quả gốc.

### 7. Xuất phụ đề chuẩn SRT 📤
* **Thao tác 1 chạm siêu nhanh:** Tự động làm sạch mọi thẻ tag định dạng của CapCut, trả về phụ đề chuẩn quốc tế `HH:MM:SS,mmm` (tương thích YouTube, VLC, Premiere...).

---

## 🚀 Hướng dẫn Sử dụng

### Yêu cầu Hệ thống:
* **Hệ điều hành:** Windows 10 / 11.
* **Ứng dụng:** Đã cài đặt phần mềm **CapCut Desktop**.

### Cách chạy phần mềm:
1. Giải nén toàn bộ thư mục từ tệp tin `ZIP` tải về.
2. Tìm và nhấp đúp chuột vào file **`CapCutWithAI.exe`** để khởi động giao diện.
3. Chờ phần mềm tự động quét danh sách dự án CapCut của bạn và bắt đầu sử dụng!

---

## 💡 Lưu ý An toàn Dữ liệu (Bảo vệ Dự án)

> [!WARNING]
> Quá trình **SmartCut** sẽ tác động và ghi đè trực tiếp lên dòng thời gian (Timeline) của file nháp gốc trong thư mục lưu trữ của CapCut Desktop. 
> 
> Luôn tích vào ô **Nhân bản dự án** hoặc tự tạo bản sao (Duplicate) trên CapCut trước khi thực hiện để đảm bảo an toàn tối đa cho dự án của bạn!
