# ⚡ AOG W26: ERA OF GLORY — Nexus Esport Arena System

> Nền tảng dự đoán kết quả thi đấu (Pick'em), tính điểm thông minh và mô phỏng phân nhánh giải đấu Thể thao Điện tử (Đấu Trường Danh Vọng - Liên Quân Mobile) xây dựng theo kiến trúc Single-file Web App độc lập.

![AOG W26 Banner](https://images.unsplash.com/photo-1542751371-adc38448a05e?w=1200&h=400&fit=crop&q=80)

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-00f2fe?style=for-the-badge&logo=github)](https://pages.github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-8b5cf6?style=for-the-badge)](LICENSE)
[![Architecture: All--in--One](https://img.shields.io/badge/Architecture-Single--File%20index.html-f59e0b?style=for-the-badge)](index.html)

---

## 🌟 Điểm Nổi Bật & Tính Năng Đột Phá

Hệ thống được thiết kế dựa trên ngôn ngữ thị giác **Cyber Mecha Glass** của ấn phẩm chính thức **AOG Winter 2026 (W26) — ERA OF GLORY**:

### 1. 🎮 Dự Đoán Lịch Trình & Tỉ Số Chuẩn Esport
- **Dải thẻ trận đấu Mecha Strip:** Cắt góc đa giác (`clip-path`), hiển thị màu cờ nhận diện của từng đội tuyển.
- **Dự đoán 1-chạm & Tỉ số trực tiếp:** Hỗ trợ bộ đếm tỉ số chuyên nghiệp (BO3, BO5, BO7), tự động định đoạt đội thắng cuộc khi chạm trần ván đấu và tính điểm thưởng Pick'em tức thì.

### 2. 📊 Bảng Điểm On-Air & Tự Động Tính Thưởng "Bounty Hunter"
- Mô phỏng chính xác giao diện truyền hình giải đấu (Broadcast On-Air).
- **In-line Live Customization:** Cho phép chỉnh sửa trực tiếp số Trận, Thắng, Thua, Hiệu số game.
- **Thuật toán tự động:** Tính toán điểm số giải đấu và tiền thưởng tích lũy **Bounty Hunter (VNĐ)** theo từng trận thắng; hỗ trợ tự động xếp hạng Top 1 (Hoàng kim), Top 2-4 (Playoff) và Top nguy hiểm.

### 3. 🔱 Sơ Đồ Play-off Nhánh Thắng / Nhánh Thua (Double Elimination)
- **Đường rẽ nhánh Vector SVG (`cyber-line`):** Hiệu ứng đường truyền dữ liệu laser phát sáng nối trực tiếp các cặp đấu từ Bán kết nhánh thắng, Bán kết nhánh thua, Chung kết nhánh tới Chung kết tổng.
- Tích hợp ô nhập tỉ số BO7 độc lập cho từng cặp đấu; tự động luân chuyển đội thắng/thua lên nhánh trên hoặc xuống nhánh dưới.

### 4. 🌐 Mô Phỏng Thể Thức Thụy Sĩ (Swiss Stage System)
- Chuẩn quốc tế (AIC/APL): Phân loại tự động 3 nhóm: **Tiến vào Tứ Kết (3 Thắng)**, **Cạnh tranh vé vớt (1-2, 2-1)** và **Chính thức bị loại (3 Thua)**.

### 5. 🛠️ Trung Tâm Quản Trị Toàn Diện (Master Admin Control)
- Dễ dàng tạo thêm tuần đấu mới, thêm/sửa lịch thi đấu, đổi ngày giờ, thể thức.
- **Kho đội tuyển & Nén ảnh Canvas:** Tự động nén logo đội tuyển tải lên xuống `< 10KB` (JPEG 65%) qua Canvas HTML5, đảm bảo không bao giờ tràn bộ nhớ ô của bảng tính.

---

## 🏗️ Kiến Trúc Kỹ Thuật (Nexus Core Standards)

- **Single-file All-in-One:** Toàn bộ HTML5, Tailwind CSS CDN, Font chữ Google Fonts (`Orbitron`, `Teko`, `Rajdhani`, `Plus Jakarta Sans`), FontAwesome 6, hiệu ứng âm thanh **Web Audio API** (không cần file MP3 ngoài) và pháo hoa `canvas-confetti` tích hợp trong **duy nhất 1 tệp `index.html`**.
- **Chống Đơ / Treo Giao Diện (Anti-Freeze Modal):** Quản lý modal bằng lớp CSS thuần `.system-modal` độc lập, triệt tiêu hoàn toàn xung đột hiển thị lớp phủ đen.
- **Offline-First & Debounced Cloud Sync:** Lưu trữ an toàn tại trình duyệt qua `localStorage` với bộ lọc lỗi (`sanitizeData`), tự động đệm 1.5s gửi đồng bộ ngầm đến Google Apps Script / Google Sheets.

---

## 🚀 Hướng Dẫn Triển Khai

### 1. Đưa Lên GitHub Pages (Chỉ mất 1 phút)
1. Tạo một repository mới trên GitHub (ví dụ: `aog-w26-pickem-arena`).
2. Tải trực tiếp tệp `index.html` lên thư mục gốc (`root`) của repo.
3. Vào **Settings** > **Pages** > Tại mục **Build and deployment**, chọn Branch là `main` / `root` rồi nhấn **Save**.
4. Trang web của bạn sẽ được xuất bản trực tuyến ngay lập tức!

### 2. Kết Nối Google Sheets Làm Máy Chủ Lưu Trữ Dữ Liệu (Tùy chọn)
Nếu bạn muốn tự động lưu lại mọi dự đoán của khán giả về Google Sheets:
1. Mở một bảng tính mới tại [Google Sheets](https://sheets.google.com).
2. Vào menu **Tiện ích mở rộng (Extensions)** > **Apps Script**, dán đoạn mã sau:
   ```javascript
   function doPost(e) {
     try {
       var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
       var data = JSON.parse(e.postData.contents);
       sheet.appendRow([
         data.timestamp,
         data.tournament,
         data.state.points,
         data.state.playoffs.champion || "Chưa xác định",
         JSON.stringify(data.state.matches),
         JSON.stringify(data.state.standings)
       ]);
       return ContentService.createTextOutput("SUCCESS").setMimeType(ContentService.MimeType.TEXT);
     } catch (err) {
       return ContentService.createTextOutput("ERROR: " + err.message).setMimeType(ContentService.MimeType.TEXT);
     }
   }
