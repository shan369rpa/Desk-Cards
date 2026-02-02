# Resource & Cost Estimation: MATE Project

**Role:** Solution Architect  
**Date:** 2026-02-02  
**Input Documents:** `mate_user_stories.md`, `ui_concepts.md`

---

## 1. Kiến trúc Giải pháp (Solution Architecture)

Để tối ưu chi phí và hiệu năng cho mô hình PWA + Hybrid Learning, kiến trúc đề xuất như sau:

- **Frontend (PWA):** Next.js (React) - Tối ưu SEO, Performance và hỗ trợ Offline mode tốt.
- **Backend (BaaS):** Supabase (PostgreSQL) hoặc Firebase - Tiết kiệm thời gian dev backend, miễn phí giai đoạn đầu.
- **AI Engine:**
  - **STT (Speech-to-Text):** OpenAI Whisper API (Độ chính xác cao) hoặc Web Speech API (Miễn phí, độ chính xác khá).
  - **Evaluation:** OpenAI GPT-4o-mini (Rẻ, nhanh) để chấm điểm ngữ pháp/phát âm.
- **Media Storage:** Cloudinary hoặc Supabase Storage (Lưu ảnh/video).
- **Hosting:** Vercel (Frontend) + Supabase (Backend).

---

## 2. Ước lượng Thời gian & Công sức (Effort Estimation)

Đơn vị: **Man-Days (MD)** - Công làm việc của 1 kỹ sư trong 1 ngày (8h).

### Chi tiết theo Epic:

| Epic                          | Hạng mục (Features)                                                                                                                            | Độ phức tạp | Frontend (MD) | Backend/AI (MD) | Tổng (MD) |
| :---------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- | :---------: | :-----------: | :-------------: | :-------: |
| **1. Auth & Core Setup**      | Setup Next.js, PWA Config, Tailwind Design System. Đăng nhập (Email/SĐT/Social), Guest Mode logic.                                             |   Medium    |       4       |        2        |   **6**   |
| **2. Home Dashboard**         | Daily Quest UI, Growth Tree Logic (Gamification State), Navigation.                                                                            |   Medium    |       5       |        1        |   **6**   |
| **3. Learning Core**          | **QR Scanner** (Floating, optimize performance). <br> **Flashcard Logic** (Flow, Interaction, Animation). <br> **Media Player** (Audio/Video). |    High     |       8       |        1        |   **9**   |
| **4. AI Features**            | **AI Speaking Feedback:** Integrate Recorder -> API -> Show Result. <br> **Virtual Partner:** Interactive Audio Flow.                          |  Very High  |       6       |        6        |  **12**   |
| **5. Reports & Gamification** | **Postcard Gen:** Canvas rendering (xuất ảnh). <br> Logic "Tưới cây" tích lũy điểm.                                                            |   Medium    |       4       |        2        |   **6**   |
| **6. Testing & Polish**       | UI/UX Fine-tuning, PWA Offline Test, Bug fixing.                                                                                               |      -      |       5       |        -        |   **5**   |
| **Tổng cộng**                 |                                                                                                                                                |             |   **32 MD**   |    **12 MD**    | **44 MD** |

### Lịch trình dự kiến (Timeline):

- **Team:** 1 Frontend Lead (Full-time), 1 Backend/AI Engineer (Part-time/Support).
- **Tổng thời gian:** ~44 Man-Days.
- **Thực tế (bao gồm Buffer 20% + Review):** **6 - 8 Tuần (1.5 - 2 Tháng).**

---

## 3. Tài nguyên Hệ thống & Chi phí Hạ tầng (Infrastructure Costs)

Dự toán cho **1,000 Active Users/Tháng (MAU)**.

| Hạng mục                | Dịch vụ đề xuất        | Gói (Tier)      | Chi phí ước tính (Tháng) | Ghi chú                                                                                      |
| :---------------------- | :--------------------- | :-------------- | :----------------------- | :------------------------------------------------------------------------------------------- |
| **Hosting (FE)**        | Vercel                 | Pro (khi scale) | $20                      | Free cho Hobby project.                                                                      |
| **Database & Auth**     | Supabase               | Pro             | $25                      | Free tier chịu được ~500MB data.                                                             |
| **AI Speaking API**     | OpenAI (Whisper + GPT) | Pay-as-you-go   | ~$50 - $100              | Giả sử 1 user học 15p/ngày, dùng AI 5 lần. <br> _Có thể giảm về $0 nếu dùng Web Speech API._ |
| **Media Storage**       | Cloudinary/AWS S3      | Pay-as-you-go   | $10                      | Lưu video bài tập của user.                                                                  |
| **Domain**              | Namecheap/Porkbun      | Năm             | ~$1/tháng                | Chi phí mua tên miền .com/.vn                                                                |
| **Tổng chi phí System** |                        |                 | **~$106 - $156 / tháng** | ~2.5 - 4 triệu VNĐ/tháng vận hành.                                                           |

---

## 4. Chi phí Nhân sự (Development Cost)

_Lưu ý: Đây là mức giá tham khảo trung bình tại thị trường Việt Nam (Outsourcing)._

1.  **Frontend Developer (Senior):** 1.5 tháng x $2,500 = $3,750
2.  **Backend/AI Dev (Mid):** 0.5 tháng x $2,000 = $1,000
3.  **UI/UX Designer:** (Đã có concept, cần design chi tiết) ~ $1,000 (Project based)
4.  **Project Management & QA:** ~ $1,000

**=> Tổng chi phí phát triển (CAPEX): ~$6,750 - $8,000 (Khoảng 170 - 200 Triệu VNĐ).**

---

## 5. Kết luận & Khuyến nghị

1.  **Giai đoạn 1 (MVP):** Tập trung vào **PWA + Core Learning + Digital Cards**. Sử dụng các dịch vụ Free Tier của Vercel/Supabase.
2.  **Tối ưu AI:** Đối với tính năng Speaking, nên cân nhắc sử dụng **Web Speech API** (có sẵn trên trình duyệt Chrome/Safari) thay vì gọi API OpenAI cho mọi lượt nói để tiết kiệm $50-$100/tháng. Chỉ dùng OpenAI cho các bài kiểm tra cuối khoá (Final Test) cần độ chính xác cực cao.
3.  **Lưu trữ:** Video bài làm của học viên nên lưu cục bộ trên máy (Local Storage) hoặc chỉ lưu tạm thời, tránh chi phí Storage phình to không kiểm soát.

---

_File này được tạo tự động dựa trên yêu cầu của Solution Architect._
