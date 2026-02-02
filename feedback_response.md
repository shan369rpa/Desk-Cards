# Phản hồi Feedback & Đề xuất Tiếp theo

**Người nhận:** Anh Pan (Product Owner)  
**Ngày:** 2026-02-02

---

## 📌 Ghi nhận Feedback từ Anh Pan

> _"Em nắm rất nhanh idea và triển khai khá sát, khoảng 70% so với ý tưởng ban đầu..."_

Cảm ơn anh đã feedback chi tiết! Em ghi nhận những điểm sau:

| Điểm đánh giá          | Chi tiết                                            |
| :--------------------- | :-------------------------------------------------- |
| ✅ Độ bám sát ý tưởng  | ~70% - Còn room để refine                           |
| ✅ UI Mockups          | Giúp hình dung sản phẩm thực tế                     |
| ✅ Format User Stories | "As a → I want to → So that → AC" được đánh giá cao |

---

## 🎯 Trả lời 3 câu hỏi của Anh Pan

### Câu 1: Tính năng nào nên BỎ hoặc HOÃN?

Dựa trên phân tích **độ phức tạp kỹ thuật** và **giá trị người dùng**, em đề xuất:

| Tính năng                           |     Đề xuất     | Lý do                                                                                                                                          |
| :---------------------------------- | :-------------: | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| **Video Recording (Final Station)** | 🟡 Đơn giản hoá | Chỉ ghi ÂM thay vì VIDEO. Lý do: Video tốn dung lượng, phức tạp encode, user cũng ngại quay mặt. Ghi âm đủ đáp ứng mục tiêu "lưu lại bài nói". |
| **US 4.8: Improv Challenge**        | 🔴 Hoãn Phase 2 | Bản chất chỉ là Timer + Random Topic. Không cần MVP, có thể thêm sau.                                                                          |
| **Virtual Partner (A/B Roleplay)**  | 🟡 Đơn giản hoá | Phase 1: App chỉ phát audio mẫu, user tự nói. Phase 2 mới làm interactive turn-taking.                                                         |
| **Growth Tree Animation**           | 🟡 Static trước | Phase 1: Hình ảnh cây tĩnh thay đổi theo level. Phase 2 mới làm animation.                                                                     |
| **Community Integration**           |     🔴 Hoãn     | Chỉ cần 1 link tới Zalo/Facebook Group. Không cần build in-app.                                                                                |

**Kết luận:** Cắt giảm này giúp **giảm ~30% effort** mà vẫn giữ được 90% trải nghiệm cốt lõi.

---

### Câu 2: 3 Module bắt đầu trước?

Em đề xuất thứ tự ưu tiên theo chiến lược **"Quick Win → Core Value → Delight"**:

|  Thứ tự  | Module                                        | Lý do ưu tiên                                                                                  |
| :------: | :-------------------------------------------- | :--------------------------------------------------------------------------------------------- |
| **🥇 1** | **Auth + Guest Mode + QR Scanner**            | Đây là "cửa vào" của app. User cần scan thẻ ngay được. Không có module này thì không có gì cả. |
| **🥈 2** | **Learning Core (Flashcard + Timer + Media)** | Đây là "trái tim" của sản phẩm. User quét thẻ xong phải thấy nội dung học ngay.                |
| **🥉 3** | **AI Speaking Feedback**                      | Đây là "điểm WOW" khác biệt với competitors. User nói vào → nhận kết quả → thấy ngay giá trị.  |

**Timeline gợi ý:**

```
Tuần 1-2: Module 1 + 2 → Demo được flow cơ bản
Tuần 3-4: Module 3 (AI) → Có điểm khác biệt
Tuần 5: Gamification (Postcard) + Polish
Tuần 6: Testing + Launch
```

---

### Câu 3: Em cần resource gì từ anh?

Để bắt đầu, em cần anh chuẩn bị các tài liệu/assets sau:

| STT | Resource cần                    | Mục đích                                                         |     Deadline      |
| :-: | :------------------------------ | :--------------------------------------------------------------- | :---------------: |
|  1  | **Bộ thẻ mẫu (10-20 thẻ)**      | Danh sách: ID, Loại (Vocab/Grammar/Listening), Nội dung, Link QR | Trước khi bắt đầu |
|  2  | **File Audio mẫu (5-10 files)** | Cho thẻ Listening và Virtual Partner                             |      Tuần 1       |
|  3  | **Logo + Brand Guidelines**     | Màu sắc chính xác, font chữ, icon set                            |      Tuần 1       |
|  4  | **Tài khoản cần thiết**         | GitHub (để share code), Supabase (anh tạo hay em tạo?)           |   Ngày bắt đầu    |

**Câu hỏi ngược lại cho anh:**

1. Anh muốn deploy lên domain nào? (ví dụ: `app.mate.vn` hay `mate-learning.vercel.app`?)
2. Authentication: Chỉ Email/SĐT hay cần thêm Google/Facebook login?
3. Ngôn ngữ app: Chỉ Tiếng Việt hay cần Bilingual (Việt + English)?

---

## 📊 Tóm tắt Action Items

| Người       | Action                                      |     Deadline      |
| :---------- | :------------------------------------------ | :---------------: |
| **Anh Pan** | Chuẩn bị Card Database (Excel/Google Sheet) |       ASAP        |
| **Anh Pan** | Gửi audio files mẫu                         |      Tuần 1       |
| **Anh Pan** | Xác nhận domain + login method              | Trước khi bắt đầu |
| **Sơn**     | Setup project, Auth, QR Scanner             |     Tuần 1-2      |
| **Sơn**     | Learning Core + AI Integration              |     Tuần 3-4      |

---

## ✅ Xác nhận bắt đầu

Nếu anh đồng ý với hướng đi trên, em sẽ:

1. Tạo repository chính thức
2. Setup Supabase database
3. Bắt đầu code Module 1 + 2

**Anh reply confirm để em khởi động nhé!** 🚀

---

_Document by: Sơn (Solution Architect + AI-Assisted Developer)_
