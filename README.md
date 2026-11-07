# 🎓 HSG English Master — Interactive Gifted Student Exam Platform

> **Ứng dụng luyện thi Học sinh Giỏi Tiếng Anh (Lớp 9 & THPT Chuyên)** dựa trên khoa học nhận thức và phương pháp sư phạm Socratic.  
> Được thiết kế & phát triển bởi **Thầy Mike Pham Bá Hong Son (Google for Education Innovator)**.

🌐 **Live GitHub Pages Web App:** [https://mikepham358.github.io/hsg-tieng-anh/](https://mikepham358.github.io/hsg-tieng-anh/)  
📦 **GitHub Repository:** [https://github.com/mikepham358/hsg-tieng-anh](https://github.com/mikepham358/hsg-tieng-anh)

---

## 🏛️ Đề Thi Đầu Tiên Được Tích Hợp
**Kỳ thi chọn Học sinh Giỏi Thành phố Hà Nội môn Tiếng Anh (Năm học 2023 - 2024)**:
- **Thời gian làm bài:** 150 phút
- **Thang điểm:** 20.0 (Chuẩn Sở GD&ĐT Hà Nội)
- **Tổng số câu:** 105 câu hỏi + 1 bài luận Task 3
- **Đề thi gốc:** Nhúng PDF viewer trực quan kèm Audio Listening chính thức (Part 1 & Part 2).

---

## ✨ Các Tính Năng Nổi Bật

### 1. Trình Duyệt Đề Thi Đa Năng (Split-Screen Viewer)
- **Màn hình chia đôi (Split-view):** Nửa bên trái nhúng file PDF đề thi gốc (`pdf/24-hanoi-de-thi.pdf`) tự động nhảy đến đúng trang của từng câu hỏi.
- **Trình phát Audio Listening tích hợp:** Tự động hiển thị và đồng bộ cho các câu hỏi Nghe (Part 1 & Part 2), hỗ trợ điều chỉnh tốc độ nghe (0.75x, 1.0x, 1.25x, 1.5x), thanh tua tiến trình và Pop-up Audioscript chính thức đối chiếu.

### 2. Phương Pháp Sư Phạm Socratic 4 Tầng Tư Duy
Mỗi câu hỏi đều được trang bị hệ thống gợi ý tiến trình nhận thức (Narciss / ANSAN levels):
- **Tầng 1 (Clue Identification):** Xác định từ khóa mấu chốt, manh mối ngữ pháp và thì của câu.
- **Tầng 2 (Context & Rule Analysis):** Phân tích ngữ cảnh, hiện tượng ngữ pháp, collocations hoặc từ loại cần điền.
- **Tầng 3 (Elimination & Trap Warning):** Nhận diện bẫy đề thi HSG (đảo ngữ, giả định, từ đồng nghĩa tinh tế, tiền tố phủ định).
- **Tầng 4 (Logical Reasoning & Full Key):** Lập luận giải pháp hoàn chỉnh và cung cấp đáp án chính xác.

### 3. Sơ Đồ Tư Duy Trực Quan (Mermaid Mindmap)
- Pop-up phân tích sơ đồ tư duy tương tác cho 100% các câu hỏi sau khi hoàn thành.
- Hỗ trợ phóng to, thu nhỏ và kéo rê sơ đồ tư duy logic bằng chuột hoặc cảm ứng tay.
- Bài luận Task 3 được trang bị sơ đồ lập luận phản biện hoàn chỉnh cùng bài mẫu Band 9 C2 Proficiency.

### 4. Đánh Giá Trả Lời Thông Minh (Smart Text Normalization)
- Hệ thống hỗ trợ đánh giá các câu hỏi tự luận (Điền từ, Word Form, Phrasal Verbs, Tri-gap, Viết lại câu).
- Tự động chuẩn hóa văn bản (loại bỏ dấu câu, chuyển chữ thường, khoảng trắng thừa) và chấp nhận danh sách đáp án tương đương (`acceptable_answers`).

### 5. Sổ Lỗi Thử Sai & Báo Cáo Kết Quả Tự Động
- **Sổ tay phản tư bắt buộc:** Khi học sinh thử sai ở lần đầu, hệ thống ghi nhận và hướng dẫn ghi chú bẫy đề thi trước khi mở khóa câu tiếp theo.
- **Nộp bài & Báo cáo qua Email:** Tự động xuất file Excel bài làm chi tiết và soạn email gửi về giáo viên và học sinh.
- **Lưu trữ độc lập 100% trên thiết bị cá nhân (LocalStorage Isolation):** Không cần đăng nhập máy chủ, bảo mật tuyệt đối dữ liệu học sinh.

### 6. Kho 1,000 Từ Vựng Học Thuật C1 - C2 Nâng Cao (AceSAT Vocab)
- Tích hợp 100 Word Lists với phát âm chuẩn bản xứ (Web Speech API).
- Thẻ lật 3D Flashcards tương tác và trắc nghiệm tạo bẫy thông minh.

---

## 📂 Cấu Trúc Dự Án

```
hsg-tieng-anh/
├── index.html                  # Giao diện chính Google Material Design 3 + Bluebook split-screen
├── styles.css                  # Toàn bộ mã định kiểu CSS, responsive, audio player & mindmap
├── app.js                      # Core logic điều khiển bài làm, chấm điểm, audio & LocalStorage
├── acesat-vocab.js             # Bộ điều khiển kho từ vựng 1,000 từ C1-C2
├── poster.png                  # Ảnh bìa giới thiệu ứng dụng
├── database.json               # Cơ sở dữ liệu đề thi fallback
├── audio/                      # Audio đề thi chính thức
│   ├── part1.mp3               # Audio Listening Part 1 (Questions 1 - 6)
│   └── part2.mp3               # Audio Listening Part 2 (Questions 7 - 15)
├── pdf/                        # File PDF đề thi gốc
│   └── 24-hanoi-de-thi.pdf     # Đề thi 9 trang chuẩn Sở GD&ĐT Hà Nội 2024
└── data/                       # Dữ liệu có cấu trúc JSON & JS
    ├── 24hanoi.json            # 105 câu hỏi có Socratic hints + Mermaid mindmaps + Essay
    ├── manifest.json           # Danh mục đề thi dạng JSON
    ├── tests.js                # Manifest nạp cho web app
    └── vocab.js                # Dữ liệu từ vựng 100 word lists
```

---

## 🚀 Hướng Dẫn Chạy Cục Bộ (Local Development)

```bash
# Clone repository
git clone https://github.com/mikepham358/hsg-tieng-anh.git
cd hsg-tieng-anh

# Khởi chạy máy chủ HTTP đơn giản bằng Python
python3 -m http.server 8000

# Mở trình duyệt tại địa chỉ:
# http://localhost:8000
```

---

## 👨‍🏫 Tác Giả & Bản Quyền
- **Tác giả:** Mike Pham Bá Hong Son
- **Danh hiệu:** Google for Education Innovator
- **Hồ sơ chính thức:** [Google Education Directory Profile](https://edudirectory.withgoogle.com/profiles/5087615831769088)
- **Liên hệ:** `mikepham358@gmail.com`
