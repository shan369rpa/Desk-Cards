# MVP Feature Matrix: MATE Project

**Mục đích:** Bảng tổng hợp tất cả tính năng, phân loại theo mức độ ưu tiên để Product Owner dễ quyết định scope MVP.

---

## Chú thích

| Ký hiệu | Ý nghĩa                                    |
| :-----: | :----------------------------------------- |
|   🟢    | **Must-Have** - Bắt buộc có trong MVP      |
|   🟡    | **Nice-to-Have** - Nên có nếu đủ thời gian |
|   🔴    | **Future** - Hoãn sang Phase 2             |
|   ✅    | Đã có mockup                               |
|   ⏱️    | Effort (Man-Days)                          |

---

## Feature Matrix

| Epic             | User Story                  | Priority | Mockup | Effort | Ghi chú                |
| :--------------- | :-------------------------- | :------: | :----: | :----: | :--------------------- |
| **Auth**         | US 1.1: Đăng nhập Email/SĐT |    🟢    |   ✅   |  ⏱️ 2  | Supabase Auth          |
| **Guest**        | US 2.1: Truy cập Trạm 0     |    🟢    |   ✅   |  ⏱️ 1  | Digital Cards only     |
| **Member**       | US 3.1: Daily Quest         |    🟢    |   ✅   |  ⏱️ 2  | Timeline UI            |
| **Learning**     | US 4.1: QR Scanner          |    🟢    |   ✅   |  ⏱️ 2  | + Manual fallback      |
| **Learning**     | US 4.2: Thẻ Listening       |    🟢    |   -    |  ⏱️ 1  | Audio/Video player     |
| **Learning**     | US 4.3: Thẻ Vocab/Concept   |    🟢    |   ✅   |  ⏱️ 2  | Swipe interaction      |
| **Learning**     | US 4.4: Virtual Partner     |    🟡    |   -    |  ⏱️ 3  | Phase 1: Audio only    |
| **Learning**     | US 4.5: AI Speaking         |    🟢    |   ✅   |  ⏱️ 4  | Traffic light feedback |
| **Learning**     | US 4.6: Final Station       |    🟡    |   -    |  ⏱️ 2  | Audio only (no video)  |
| **Learning**     | US 4.7: Timer & Progress    |    🟢    |   ✅   |  ⏱️ 1  | Countdown + controls   |
| **Learning**     | US 4.8: Improv Challenge    |    🔴    |   -    |  ⏱️ 1  | Phase 2                |
| **Gamification** | US 5.1: Growth Tree         |    🟡    |   ✅   |  ⏱️ 2  | Static image first     |
| **Gamification** | US 5.2: Postcard Report     |    🟡    |   ✅   |  ⏱️ 2  | Canvas export          |
| **Support**      | US 6.1: Community           |    🔴    |   -    | ⏱️ 0.5 | External link only     |
| **Support**      | US 6.2: Hướng dẫn           |    🟡    |   -    |  ⏱️ 1  | Static page/video      |
| **Support**      | US 6.3: Founder Corner      |    🔴    |   -    | ⏱️ 0.5 | Phase 2                |

---

## Tổng hợp theo Priority

| Priority        | Số features | Tổng Effort |
| :-------------- | :---------: | :---------: |
| 🟢 Must-Have    |     10      |  **17 MD**  |
| 🟡 Nice-to-Have |      5      |  **10 MD**  |
| 🔴 Future       |      3      |  **2 MD**   |

---

## Đề xuất MVP Scope

### ✅ MVP v1.0 (4-5 tuần)

Bao gồm tất cả **🟢 Must-Have** + một số **🟡 Nice-to-Have** chọn lọc:

- Auth + Guest Mode
- QR Scanner + Manual Input
- Learning Core (Flashcard, Timer, Media)
- AI Speaking Feedback
- Daily Quest Progress
- Postcard Report (đơn giản)

**Effort: ~20-22 Man-Days**

### 📦 Phase 2 (sau launch)

- Virtual Partner (Interactive)
- Improv Challenge
- Growth Tree Animation
- Community + Founder Corner
- Video Recording

---

_Matrix được tạo dựa trên `mate_user_stories.md` và `ui_concepts.md`_
