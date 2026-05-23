# Capcut With AI (v0.9.1)

**Capcut With AI** là một ứng dụng máy tính (Desktop App) chuyên dụng với giao diện đồ họa GUI hiện đại trên hệ điều hành **Windows**, hỗ trợ biên tập và cắt ghép video thông minh (Talking Head, Vlog, Podcast) cho phần mềm **CapCut Desktop**.

Bằng cách phân tích trực tiếp dữ liệu phụ đề tự động (Auto Captions) từ file nháp của dự án CapCut, **Capcut With AI** tự động phát hiện, cắt bỏ các đoạn nói vấp/lặp (Duplicate Takes) và tăng tốc các phân đoạn im lặng (Gaps) trực tiếp trên dòng thời gian (Timeline) mà không cần render trung gian hay qua ứng dụng bên thứ ba.

---

## 📝 Thông tin Bản quyền & Phát triển

* **Tên Chính thức:** `Capcut With AI`
* **Phiên bản Hiện tại:** `0.9.1`
* **Tác giả phát triển:** **VEGA**
* **Dựa trên dự án 'capcut-ai-editor' của tác giả** **mrbuslov**


---

## ⚡ Các Tính năng Nổi bật (Offline 100% - Windows Only)

### 1. Giao diện Đồ họa (GUI) Hiện đại & Cao cấp

### 2. Quản lý Dự án CapCut Thông minh & Tiện lợi
* **Tự động Tìm kiếm nháp:** Tự động dò tìm thư mục lưu trữ dự án nháp mặc định của CapCut Desktop ngay trong lần chạy đầu tiên.
* **Tốc độ Tải danh sách Siêu tốc:** Khởi động và tải danh sách dự án tức thì (< 0.5 giây cho hơn 600 dự án) nhờ cơ chế quét thông minh chỉ đọc tệp thông tin cấu hình thu gọn `draft_meta_info.json`.
* **Sắp xếp theo Thời gian:** Danh sách dự án tự động được sắp xếp theo thứ tự ngày chỉnh sửa gần nhất (`modified_time` mới nhất lên đầu).
* **Tìm kiếm Thời gian thực:** Bộ lọc tìm kiếm cực nhạy, phản hồi ngay lập tức khi gõ tên dự án.
* **Phân trang Linh hoạt:** Hỗ trợ phân trang mượt mà nếu danh sách dự án quá nhiều (người dùng tự chọn hiển thị 10, 20 hoặc 50 dự án trên một trang).

### 3. Cấu hình Cắt ghép Thông minh (SmartCut)
* **Tự động Kiểm tra Phụ đề:** Tự động đọc và kiểm tra trạng thái phụ đề của dự án:
  * **Đã có phụ đề:** Hiện tích xanh kèm tổng số câu phụ đề, mở khóa tính năng SmartCut.
  * **Chưa có phụ đề:** Hiện bảng cảnh báo màu đỏ chi tiết, tạm khóa nút SmartCut để tránh lỗi timeline, nhắc nhở người dùng tạo Auto Captions trên CapCut hoặc dùng chức năng **Subtitle with AI**.
* **Tùy chỉnh Tốc độ (Speed Sliders):** Hỗ trợ 3 thanh trượt điều chỉnh tốc độ vô cùng trực quan:
  * **Tốc độ tối đa đoạn có phụ đề:** Tăng tốc nhẹ nhàng cho các đoạn nói có phụ đề (Mặc định **1.5x**, cho phép chỉnh từ `1.0x` đến `5.0x`).
  * **Tốc độ tối đa tua nhanh âm thanh:** Giới hạn tốc độ của âm thanh khi tăng tốc tua nhanh để tránh bị méo tiếng/giọng chói (Mặc định **1.3x**, cho phép chỉnh từ `1.0x` đến `3.0x`).
  * **Tốc độ đoạn không có phụ đề (Gaps):** Tăng tốc tua nhanh các khoảng im lặng/gần trống để tạo hiệu ứng Vlog timelapse hiện đại (Mặc định **2.0x**, cho phép chỉnh từ `1.0x` đến `10.0x`).
* **Bảo toàn thành phần timeline tuyệt đối (Mới trong v0.9.1) 🛡️**: Đảm bảo khi chạy SmartCut, hoàn toàn **không có bất kỳ phân đoạn video, âm thanh gốc, phụ đề hay sticker nào** bị xóa đi. Các khoảng lặng và phân đoạn thoại chỉ được thực hiện tua nhanh (timelapse) hoặc đồng bộ tốc độ theo cấu hình thanh trượt tối đa của bạn, bảo toàn nguyên vẹn tài nguyên dự án.

### 4. Đa luồng Bảo vệ Toàn diện (Background Threading)
* Toàn bộ tác vụ quét ổ đĩa, tải thông tin chi tiết dự án, lọc tìm kiếm, thực hiện SmartCut và tạo phụ đề AI đều được xử lý bất đồng bộ dưới nền bằng các luồng độc lập (`QThread`).
* Giao diện chính luôn phản hồi tức thì, không bao giờ xảy ra hiện tượng đơ/đóng băng hoặc crash ứng dụng khi xử lý danh sách dự án lớn.

### 5. Tạo & Dịch phụ đề tự động bằng AI (Subtitle with AI)
* **Tích hợp Whisper API của Groq:** Sử dụng mô hình nhận diện giọng nói tiên tiến `whisper-large-v3` thông qua API Groq siêu tốc, giúp tạo phụ đề tiếng Việt chính xác cao và khớp khớp mốc thời gian.
* **Tùy chọn Dịch Phụ đề A.I:** Tích hợp dịch thuật thông minh với **Gemini API** (hỗ trợ nhiều model: `gemini-2.5-flash`, `gemini-2.5-flash-lite`, v.v... cấu hình linh hoạt trong cài đặt).
* **Đa Ngôn ngữ Hỗ trợ:** Hỗ trợ dịch phụ đề dịch thuật ra nhiều ngôn ngữ phổ biến: Tiếng Việt, Tiếng Anh, Trung Quốc, Nhật Bản, Hàn Quốc, Pháp, Đức.
* **Phân tách Dòng Phụ đề Độc lập:** Cả phụ đề gốc (tạo từ Whisper) và phụ đề dịch (từ Gemini) khi chèn vào dự án CapCut được phân thành **2 luồng song song độc lập**. Mỗi loại sử dụng UUID nhóm (`group_id` & `recognize_task_id`) riêng biệt. Nhờ đó, các câu cùng loại được liên kết đồng bộ với nhau, nhưng việc thay đổi định dạng/kiểu chữ/vị trí của phụ đề gốc sẽ **hoàn toàn không ảnh hưởng** tới phụ đề dịch và ngược lại.
* **Tích hợp FFMPEG cục bộ:** Tự động trích xuất luồng âm thanh và nén sang định dạng siêu nhẹ (Mono, 16kHz, 64kbps MP3) trước khi gửi đi. Ưu tiên sử dụng file `bin/ffmpeg.exe` lưu trực tiếp trong thư mục dự án để chạy độc lập không phụ thuộc cài đặt hệ thống.
* **Dọn dẹp tự động:** Sử dụng thư mục tạm `temp` ngầm và tự động dọn dẹp sạch sẽ sau khi hoàn thành công việc.
* *Lưu ý:* Tính năng này được thiết kế và tối ưu dành riêng cho các dự án có **đúng 1 video gốc**.

### 6. Tự động ReScript & Cắt ghép video bằng AI (ReScript with AI) 📝
Chỉ khả dụng khi sử dụng mô hình **'gemini-3.1-pro-preview'**
* **Rescript Shorts siêu tốc bằng Gemini**: Tự động tải video thô lên Gemini để phân tích nội dung, viết lại kịch bản ngắn gọn và lựa chọn những mốc thời gian (start/end) đắt giá nhất để cắt ghép thành một video Short dạng đứng (50-60 giây) tối ưu cho TikTok/Shorts/Reels.
* **Khớp Khẩu hình & Lời thoại**: Yêu cầu AI điều khiển kịch bản/subtitles khớp tuyệt đối với chuyển động khẩu hình miệng (lip-sync) và đúng nhân vật trong các phân đoạn được chọn, tránh hiện tượng khớp thoại sai nhân vật hoặc nói một đằng hình một nẻo.
* **Tối ưu Hook & Tránh kết thúc đột ngột**:
  * Tự động đặt một đoạn **Hook ấn tượng** dài 3-5 giây ở giây đầu tiên của video (được chọn lọc thông minh từ các khoảnh khắc cao trào sau đó) để giữ chân người xem lập tức.
  * Đảm bảo video chuyển tiếp mượt mà và **không bao giờ bị kết thúc đột ngột** (out-speech) giữa chừng hoặc mất chữ ở câu cuối cùng.
* **Upload Resumable & Dọn dẹp Đám mây**: Truyền phát file video gốc qua giao thức Resumable API an toàn, không tốn tài nguyên phần cứng. Ngay sau khi hoàn thành (hoặc khi gặp sự cố thất bại), ứng dụng sẽ tự động gọi lệnh **xóa file khỏi máy chủ Google** để bảo mật thông tin và bảo vệ API limits của bạn.
* **Chế độ Marker an toàn & Cặp Marker Đầu/Cuối (Mới trong v0.9.1) 📌**: Khi kích hoạt, phần mềm sẽ không cắt trực tiếp timeline của bạn mà chèn các cặp Marker chỉ dẫn rõ ràng:
  * Marker **Bắt đầu** (`[AI ReScript #XX Bắt đầu]`) được cấu hình màu **Xanh lá** và Marker **Kết thúc** (`[AI ReScript #XX Kết thúc]`) màu **Đỏ**.
  * Nếu điểm kết thúc của đoạn trước trùng với điểm bắt đầu của đoạn sau, cả 2 marker vẫn được tạo đồng thời đầy đủ tại đúng mốc đó giúp biên tập thủ công cực kỳ rạch ròi.
* **Tự động Co giãn Thời gian - Timescale Auto-Scaling (Mới trong v0.9.1) ⏱️**: Khắc phục triệt để lỗi phụ đề bị văng ra ngoài timeline video do sự sai lệch tần số quét (Variable Frame Rate) của Gemini. Hệ thống tự động so khớp thời lượng và co giãn (scale) phụ đề cùng các marker khớp khít 100% với video thô.


---

## 🚀 Hướng dẫn Cài đặt & Khởi chạy nhanh

### Yêu cầu Hệ thống:
* **Hệ điều hành:** Windows 10 / 11.
* **Công cụ bổ trợ:** Python 3.10+ (Đã thêm vào biến môi trường PATH), ứng dụng CapCut Desktop trên Windows.

### Các bước chuẩn bị nhanh:
1. Tạo môi trường ảo Python `venv` trong thư mục dự án `capcut-with-ai`:
   ```powershell
   python -m venv venv
   ```
2. Kích hoạt môi trường ảo:
   ```powershell
   # Dành cho PowerShell
   .\venv\Scripts\Activate.ps1
   ```
3. Cài đặt các gói phụ thuộc cần thiết:
   ```powershell
   pip install -e .
   ```

### ⚡ Khởi chạy Ứng dụng:
* Bạn chỉ cần nhấp đúp chuột vào file **`Start.bat`** tại thư mục gốc của dự án. File script sẽ tự động nhận diện môi trường ảo và khởi chạy ứng dụng GUI **Capcut With AI** ngay lập tức mà không cần gõ lệnh!
* Hoặc chạy bằng dòng lệnh thủ công:
   ```powershell
   python capcut-gui.py
   ```

### 📦 Đóng gói Ứng dụng thành tệp thực thi (.EXE):
Bạn có thể dễ dàng biên dịch dự án thành ứng dụng chạy độc lập trên Windows bằng cách khởi chạy tập lệnh đóng gói **`build.bat`**. Ứng dụng hỗ trợ hai chế độ biên dịch nâng cao:
1. **Đóng gói dạng Thư mục (Khởi động Siêu tốc - Khuyên dùng) ⚡**:
   ```powershell
   .\build.bat --onedir
   ```
   * *Ưu điểm:* Giải nén sẵn toàn bộ DLLs và tài nguyên nền tảng. Khi chạy tệp **`dist/CapCutWithAI/CapCutWithAI.exe`**, cửa sổ ứng dụng sẽ **khởi động tức thì (dưới 1 giây)**!
2. **Đóng gói thành 1 Tệp duy nhất (Tiện chia sẻ) 📁**:
   ```powershell
   .\build.bat
   ```
   * *Đặc điểm:* Gom toàn bộ tài nguyên vào một file **`dist/CapCutWithAI.exe`** duy nhất. Khi khởi động sẽ mất khoảng 3-5 giây để Windows giải nén tạm thời ra bộ nhớ.

---

## 💡 Lưu ý An toàn Dữ liệu (Bảo vệ Dự án)

> [!WARNING]
> Quá trình **SmartCut** sẽ tác động và ghi đè trực tiếp lên dòng thời gian (Timeline) của file nháp gốc trong thư mục lưu trữ của CapCut Desktop. 
> 
> Trước khi nhấn nút **🚀 Thực Hiện SmartCut**, vui lòng mở ứng dụng **CapCut Desktop**, nhấp chuột phải vào dự án của bạn và chọn **Duplicate (Nhân bản)** để tạo một bản sao dự phòng an toàn.

---

  * `worker.py` - Trình quản lý chạy đa luồng `QThread`.
* `src/capcutwithai/tools/` - Lõi xử lý sửa đổi cấu trúc dữ liệu dự án nháp CapCut.
