# User Stories: Dự án MATE - Hệ sinh thái hỗ trợ tự học tiếng Anh

**Slogan:** Dạy như thở, học như chơi  
**Mô hình:** Hybrid (Thẻ vật lý + WebApp PWA)  
**Phong cách:** Modern-Heritage

---

## 🏗 Epics (Chủ đề lớn)

1.  **Quản lý Tài khoản & Phân quyền (Auth & Access Control)**
2.  **Học thử (Guest/Trial Experience)**
3.  **Học chính thức (Member Experience)**
4.  **Công cụ Hỗ trợ Học tập (Learning Utilities)**
5.  **Gamification & Báo cáo (Engagement & Reporting)**
6.  **Hệ thống Hỗ trợ (Support System)**

---

## 📝 Chi tiết User Stories

### Epic 1: Quản lý Tài khoản & Phân quyền (Auth & Access Control)

**US 1.1: Đăng nhập thành viên**

- **As a** Học viên đã mua bộ thẻ (Member),
- **I want to** đăng nhập bằng Email hoặc Số điện thoại,
- **So that** tôi có thể truy cập vào lộ trình học đầy đủ và lưu lại tiến độ của mình.
- **Acceptance Criteria:**
  - Hệ thống xác thực đúng Email/SĐT có trong database.
  - Nếu chưa có tài khoản/chưa mua, hiển thị thông báo hướng dẫn liên hệ hoặc chuyển sang chế độ Guest.

### Epic 2: Học thử (Guest/Trial Experience)

**US 2.1: Truy cập chế độ khách**

- **As a** Người dùng chưa đăng ký (Guest),
- **I want to** truy cập ngay vào "Trạm 0" mà không cần đăng nhập,
- **So that** tôi có thể trải nghiệm cách học trước khi quyết định mua.
- **Acceptance Criteria:**
  - Mặc định vào mode Guest khi mở App lần đầu.
  - Chỉ hiển thị nội dung "Trạm 0".
  - Các tính năng AI Feedback và Lưu tiến trình bị khóa (bị làm mờ hoặc hiện khóa).
  - Sử dụng Thẻ ảo (Digital Cards) trên màn hình thay vì yêu cầu quét thẻ thật.

### Epic 3: Học chính thức (Member Experience)

**US 3.1: Lộ trình theo ngày (Daily Quest)**

- **As a** Member,
- **I want to** nhìn thấy lộ trình bài học theo từng ngày,
- **So that** tôi biết mình cần học gì hôm nay và duy trì thói quen.
- **Acceptance Criteria:**
  - Hiển thị danh sách ngày (Day 1, Day 2...).
  - Ngày chưa học bị khóa (Locked), chỉ mở khi hoàn thành ngày liền trước.
  - Trạng thái: Hoàn thành / Đang học / Chưa mở.

### Epic 4: Công cụ Hỗ trợ Học tập (Learning Utilities)

**US 4.1: Quét mã QR (Floating QR Scanner)**

- **As a** Người học,
- **I want to** có nút quét QR luôn hiển thị (Floating Button) trên màn hình,
- **So that** tôi có thể kích hoạt nội dung bài học từ thẻ vật lý bất cứ lúc nào mà không cần thoát ra menu chính.
- **Acceptance Criteria:**
  - Nút QR Floating nằm ở góc thuận tiện (ví dụ: góc dưới phải).
  - Tốc độ mở camera và nhận diện mã cực nhanh (Ưu tiên tối ưu tốc độ).

**US 4.2: Thẻ Listening**

- **As a** Người học,
- **I want to** quét thẻ Listening để nghe/xem nội dung tương ứng,
- **So that** tôi có thể luyện nghe thụ động hoặc chủ động.
- **Acceptance Criteria:**
  - Quét QR -> Tự động phát Audio hoặc Video player.
  - Có trình điều khiển cơ bản (Play/Pause, Seek).

**US 4.3: Thẻ Vocab & Concept Check**

- **As a** Người học,
- **I want to** xem từ vựng và tự kiểm tra trí nhớ,
- **So that** tôi có thể ghi nhớ từ mới hiệu quả.
- **Acceptance Criteria:**
  - Hiển thị mặt trước (Câu hỏi/Hình ảnh).
  - Có đồng hồ đếm ngược áp lực thời gian.
  - Nút "Show Answer" để lật mặt sau.
  - Tương tác vuốt hoặc chọn: Trái (Chưa thuộc) / Phải (Đã thuộc) để xác nhận trạng thái.

**US 4.4: Thẻ Ngữ pháp (Virtual Partner)**

- **As a** Người học 1 mình,
- **I want to** App đóng vai người bạn (Partner A) đọc mẫu câu hỏi,
- **So that** tôi có thể đóng vai B và phản xạ lại, tạo cảm giác hội thoại thực tế.
- **Acceptance Criteria:**
  - Chế độ Roleplay A/B.
  - App phát audio vai A, dừng lại chờ người dùng nói vai B.

**US 4.5: Thẻ Phát âm (AI Speaking)**

- **As a** Người học,
- **I want to** được AI chấm điểm phát âm ngay lập tức,
- **So that** tôi biết mình đọc đúng hay sai để sửa.
- **Acceptance Criteria:**
  - Bước 1: Quét QR -> Video hướng dẫn khẩu hình ngắn.
  - Bước 2: Hold-to-record (Nhấn giữ Mic) để đọc.
  - Bước 3: AI trả về kết quả theo màu đèn giao thông:
    - 🟢 Xanh: Tốt.
    - 🟡 Vàng: Khá (Cần chỉnh sửa nhỏ).
    - 🔴 Đỏ: Thử lại (Sai nhiều).

**US 4.6: Thẻ Speaking (Final Station)**

- **As a** Người học,
- **I want to** quay video hoặc ghi âm bài nói cuối buổi,
- **So that** tôi có thể lưu lại thành quả và so sánh sự tiến bộ.
- **Acceptance Criteria:**
  - Tích hợp Camera/Recorder ngay trên trình duyệt (WebRTC).
  - Lưu file vào Local hoặc Cloud (tuỳ cấu hình Member).

**US 4.8: Thẻ Thử thách ngẫu hứng (Improv Challenge)**

- **As a** Người học,
- **I want to** nhận được một chủ đề ngẫu hứng kèm đồng hồ đếm ngược,
- **So that** tôi có thể luyện tập phản xạ nói mà không cần chuẩn bị trước (Free talk).
- **Acceptance Criteria:**
  - Hiển thị thông điệp/chủ đề khích lệ.
  - Chỉ có đồng hồ đếm ngược (Timer) chạy.
  - Không có đáp án mẫu, chỉ tập trung vào việc nói.

**US 4.7: Đồng hồ & Tiến độ (Timer & Progress)**

- **As a** Người học,
- **I want to** thấy thời gian đếm ngược cho mỗi thẻ,
- **So that** tôi duy trì được sự tập trung và nhịp độ (Pace).
- **Acceptance Criteria:**
  - Đồng hồ đếm lùi cho từng hoạt động.
  - Nút "Xong sớm" (Skip) và "Thêm thời gian (+30s)" nếu chưa làm xong.

### Epic 5: Gamification & Báo cáo (Engagement & Reporting)

**US 5.1: Cây Ngôn Ngữ (The Growth Tree)**

- **As a** Người học,
- **I want to** thấy cây ảo của mình lớn lên dựa trên thời gian học,
- **So that** tôi có động lực học đều đặn mỗi ngày (Nuôi cây).
- **Acceptance Criteria:**
  - Quy đổi: Ví dụ 10 phút học = 100ml nước.
  - User thực hiện hành động "Tưới cây" cuối buổi học.
  - Hình ảnh cây thay đổi trạng thái (Lớn lên, ra lá...) theo level.

**US 5.2: Báo cáo Postcard (Post-session)**

- **As a** Người học,
- **I want to** nhận được một tấm bưu thiếp tổng kết sau mỗi buổi học,
- **So that** tôi cảm thấy thoả mãn và có thể chia sẻ lên mạng xã hội.
- **Acceptance Criteria:**
  - Nội dung: Thời gian học (Food for thought / stats), Số từ vựng đã học.
  - AI Feedback ngắn gọn, động viên.
  - Thiết kế đẹp (Visual), cho phép tải về dưới dạng ảnh (JPG/PNG).

### Epic 6: Hệ thống Hỗ trợ (Support System)

**US 6.1: Menu Cộng đồng**

- **As a** User,
- **I want to** truy cập nhanh vào nhóm cộng đồng,
- **So that** tôi có thể giao lưu với những người học khác.

**US 6.2: Hướng dẫn sử dụng**

- **As a** User,
- **I want to** xem video/bài viết hướng dẫn cách dùng bộ thẻ,
- **So that** tôi không bị bỡ ngỡ khi mới bắt đầu.

**US 6.3: Góc Founder & Feedback**

- **As a** User,
- **I want to** xem video truyền cảm hứng hoặc gửi góp ý/donate,
- **So that** tôi cảm thấy kết nối với đội ngũ phát triển.

---

## 💡 Non-Functional Requirements (Yêu cầu phi chức năng)

1.  **Hiệu năng (Performance):**
    - Trình quét QR (QR Scanner) phải khởi động dưới 1 giây.
    - Tính năng ghi âm/quay video phải mượt mà, không giật lag trên các thiết bị di động phổ thông.
2.  **Giao diện (UI/UX):**
    - Minimalism (Tối giản), Modern-Heritage style.
    - Ít chữ (Text-light), tập trung vào icon và hình ảnh.
    - Tối ưu cho thao tác một tay (Mobile-first).
3.  **Hạ tầng:**
    - PWA (Progressive Web App): Có thể "Cài đặt" ra màn hình chính, hoạt động offline cơ bản (cache assets).
