# 🚀 MATE Project Roadmap & Strategy

Dựa trên phân tích User Stories và mục tiêu "MVP (Minimum Viable Product) để test nhanh", đây là đề xuất chiến lược phát triển:

## 1. Phân tích Tính năng & Cắt giảm (Scope Optimization)

Để tối ưu nguồn lực và tập trung vào **Core Value (Giá trị cốt lõi)**, chúng ta nên tạm thời loại bỏ hoặc đơn giản hóa các tính năng sau trong giai đoạn 1:

| Tính năng                           | Đề xuất             | Lý do                                                                                                                                                 |
| :---------------------------------- | :------------------ | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Video Recording (Final Station)** | ❌ **Tạm hoãn**     | Lưu trữ Video tốn kém tài nguyên Server/Bandwidth. Xử lý Video trên PWA (Web) kém ổn định hơn Native App. **Thay thế:** Chỉ ghi âm (Audio Only).      |
| **Virtual Partner (Roleplay A/B)**  | ⚠️ **Đơn giản hóa** | Logic nhận diện giọng nói ngắt nghỉ tự động (VAD) khá phức tạp trên Web. **Thay thế:** Người dùng bấm nút thủ công để chuyển lượt nói.                |
| **Floating QR Scanner**             | ⚠️ **Cố định hóa**  | Nút trôi (Floating) dễ che nội dung. Trên iOS Safari, camera permission mỗi lần mở lại khá phiền. **Thay thế:** Nút Scan to ở Menu chính hoặc Header. |
| **Cộng đồng & Founder Corner**      | ❌ **Tạm hoãn**     | Chưa cần thiết phải build trong App. **Thay thế:** Dẫn link ra Group Facebook/Zalo.                                                                   |

---

## 2. Top 3 Modules Trọng tâm (MVP Selection)

Để sản phẩm chạy được và mang lại giá trị ngay lập tức, chúng ta tập trung vào 3 trụ cột này:

### 🥇 Module 1: The Learning Engine (Trình Phát Thẻ)

- **Là gì:** Giao diện hiển thị thẻ, mặt trước/sau, Audio player, Logic ghi nhớ (Đúng/Sai).
- **Tại sao:** Đây là trái tim của sản phẩm. Không có nó, WebApp vô dụng với người cầm thẻ.
- **Bao gồm:** Thẻ Vocab, Listening, AI Speaking (cơ bản).

### 🥈 Module 2: The Gateway (QR & Input Handler)

- **Là gì:** Tính năng quét mã QR hoặc nhập mã số thẻ (3 chữ số) để gọi Module 1.
- **Tại sao:** Cầu nối bắt buộc giữa Vật lý (Thẻ) và Kỹ thuật số (App). Cần làm thật mượt, nhanh.

### 🥉 Module 3: The Hook (Daily Quest + Growth Tree)

- **Là gì:** Màn hình chính hiển thị Lộ trình và Cây ngôn ngữ (Phiên bản đơn giản). Login/Guest Mode.
- **Tại sao:** Giữ chân người dùng. Nếu chỉ có module học, họ sẽ chán. Cần "Cây" để họ có lý do quay lại.

---

## 3. Lộ trình Triển khai (Phases)

### Phase 1: The Pilot (2-3 tuần)

- **Mục tiêu:** Chạy được luồng Guest Mode & 1 loại thẻ cơ bản (Vocab).
- **Output:** WebApp cho phép nhập mã thẻ -> Hiện nội dung -> Lật thẻ.

### Phase 2: The Core (3-4 tuần)

- **Mục tiêu:** Login Member & Daily Quests.
- **Output:** Hệ thống cây lớn lên, các loại thẻ Listening/Speaking cơ bản.

### Phase 3: The Polish (2 tuần)

- **Mục tiêu:** AI Feedback xịn & Báo cáo Postcard.
- **Output:** Hoàn thiện UI/UX, hiệu ứng mượt mà.

---

## 4. Yêu cầu Tài nguyên (Resources Needed)

Để bắt đầu Phase 1 ngay, em cần anh cung cấp:

1.  **Dữ liệu thô (Content Database):** File Excel/Google Sheet chứa danh sách khoảng 20-50 thẻ mẫu.
    - _Cột:_ ID Thẻ, Loại thẻ, Câu tiếng Anh, Nghĩa tiếng Việt, Link Audio/Video (nếu có).
2.  **Tài nguyên Brand (Brand Assets):**
    - Logo (File Vector/PNG tách nền).
    - Font chữ chủ đạo (Nếu có yêu cầu đặc biệt, chưa có thì em dùng Google Fonts: Libre Baskerville & Lato).
    - Hình ảnh Cây (Các trạng thái: Mầm, Cây con, Cây lớn) - Nếu chưa có Designer vẽ, em có thể dùng AI tạo tạm để demo.
