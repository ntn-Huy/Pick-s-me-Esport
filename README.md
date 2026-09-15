# ⚡ Nexus Pick'Em Esport Arena — Multi-Title Prediction Platform

> Nền tảng dự đoán kết quả thi đấu (Pick'em), phân nhánh giải đấu, tính điểm thông minh và bảng xếp hạng thể thao điện tử (Esport) xây dựng theo kiến trúc Single-file Web App độc lập (`index.html`), sẵn sàng triển khai trên GitHub Pages mà không cần cấu hình build phức tạp.

![Pick'Em Arena Banner](https://images.unsplash.com/photo-1542751371-adc38448a05e?w=1200&h=420&fit=crop&q=80)

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-00f2fe?style=for-the-badge&logo=github)](https://pages.github.com/)
[![Esport Titles](https://img.shields.io/badge/Esports-Liên%20Quân%20Mobile%20%7C%20Multi--Title%20Ready-8b5cf6?style=for-the-badge)](https://lienquan.garena.vn/)
[![Architecture](https://img.shields.io/badge/Architecture-Single--File%20All--In--One-f59e0b?style=for-the-badge)](index.html)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

---

## 🎮 TỔNG QUAN HỆ THỐNG (SYSTEM OVERVIEW)

**Nexus Pick'Em Esport** là hệ thống dự đoán kết quả thi đấu trực quan dành cho cộng đồng Esport. Nền tảng được tối ưu hóa giao diện và dữ liệu theo chuẩn mùa giải **Đấu Trường Danh Vọng (AOG Mùa Đông 2026 - ERA OF GLORY)** của bộ môn **Liên Quân Mobile**, đồng thời sở hữu thiết kế module linh hoạt để mở rộng sang các tựa game Esport khác như Valorant, League of Legends, PUBG,...

### Lộ Trình Hỗ Trợ Bộ Môn (Title Roadmap)
- [x] **Liên Quân Mobile (Arena of Valor):** Chuẩn thể thức AOG (Vòng bảng BO5, Play-off Double Elimination BO7, Bounty Hunter, Swiss Stage AIC/APL).
- [ ] **Valorant / CS2:** Thể thức Nhánh Thắng/Thua Map Veto BO3/BO5 *(Đang phát triển)*.
- [ ] **Liên Minh Huyền Thoại (LoL - LCK/VCS):** Bảng xếp hạng điểm tích lũy & Play-off 6 đội *(Dự kiến)*.

---

## 🌟 TÍNH NĂNG NỔI BẬT (CORE CAPABILITIES)

### 1. ⚔️ Dự Đoán Lịch Trình & Tỉ Số 1-Chạm (Match Pick'Em)
- **Thẻ trận Mecha Strip:** Cắt góc đa giác đặc trưng của thể thao điện tử, hiển thị màu sắc và logo nhận diện của từng tổ chức.
- **Bộ tùy biến tỉ số trực tiếp:** Tùy biến tỉ số nhanh qua nút `+ / -` cho các thể thức BO3, BO5, BO7; tự động xác định đội chiến thắng khi chạm điểm trần và cộng điểm Pick'em tức thì.

### 2. 📊 Bảng Điểm On-Air & Tự Động Tính Thưởng "Bounty Hunter"
- Mô phỏng chính xác giao diện truyền hình giải đấu (Broadcast On-Air).
- **Chỉnh sửa trực tiếp (In-line Edit):** Tự do thay đổi số trận đã đấu, số trận thắng/thua, hiệu số game.
- **Thuật toán tự động:** Tự động tính điểm tổng và tiền thưởng tích lũy **Bounty Hunter (VNĐ)** theo từng trận thắng; phân định rực rỡ vị trí Top 1 Hoàng kim, Top 2-4 Playoff và nhóm nguy hiểm rớt hạng.

### 3. 🔱 Sơ Đồ Nhánh Thắng / Nhánh Thua (Double Elimination Playoff)
- **Đường rẽ nhánh Vector SVG (`cyber-line`):** Hiệu ứng laser phát sáng neon kết nối trực tiếp các cặp đấu từ Bán kết nhánh thắng, Bán kết nhánh thua, Chung kết nhánh tới Chung kết tổng.
- Tích hợp ô nhập tỉ số BO7 độc lập cho từng cặp đấu; tự động luân chuyển đội thắng/thua lên nhánh trên hoặc xuống nhánh dưới.

### 4. 🌐 Mô Phỏng Thể Thức Thụy Sĩ (Swiss Stage System)
- Chuẩn thi đấu quốc tế (AIC/APL/CKTG): Tự động phân loại các đội tuyển theo kết quả: **Đủ điều kiện vào Tứ Kết (3 Thắng)**, **Khu vực cạnh tranh (1-2, 2-1)** và **Chính thức dừng cuộc chơi (3 Thua)**.

### 5. 🛠️ Trung Tâm Quản Trị Giải Đấu Toàn Diện (Master Admin Control)
- Dễ dàng tạo thêm tuần đấu mới, thêm/sửa lịch thi đấu, đổi ngày giờ, thể thức (BO3/BO5/BO7).
- **Kho đội tuyển & Nén ảnh Canvas:** Bộ nén ảnh tự động HTML5 Canvas đưa logo đội tuyển tải lên về kích thước tối ưu `< 10KB` (JPEG 65%), bảo đảm không làm tràn dung lượng ô lưu trữ.

---

## ⚙️ BỘ KHUNG KỸ THUẬT NEXUS ARCHITECT

1. **All-in-One Single File:** HTML5, Tailwind CSS, Font chữ gaming (`Orbitron`, `Teko`, `Rajdhani`, `Plus Jakarta Sans`), FontAwesome 6, hiệu ứng âm thanh **Web Audio API** (không phụ thuộc file ngoài) và pháo hoa `canvas-confetti` tích hợp trong **duy nhất 1 file `index.html`**.
2. **Chống đơ & Treo giao diện (Anti-Freeze Modals):** Quản lý trạng thái mở/đóng modal bằng CSS thuần `.system-modal` độc lập, triệt tiêu hoàn toàn lỗi đè lớp phủ tàng hình.
3. **Lưu trữ Offline & Đồng bộ Cloud không máy chủ:**
   - Hoạt động mượt mà ở chế độ ngoại tuyến qua `localStorage` đi kèm bộ lọc dữ liệu an toàn `sanitizeAppState`.
   - Cơ chế **Debounce Sync 1.5s** tự động đẩy dữ liệu dự đoán về Google Sheets thông qua Google Apps Script Web App.

---

## 🚀 HƯỚNG DẪN TRIỂN KHAI NHANH

### Cách 1: Xuất Bản Lên GitHub Pages (Chỉ mất 1 phút)
1. Tạo một repository mới trên GitHub (Ví dụ: `nexus-pickem-esport` hoặc `aog-w26-pickem-arena`).
2. Tải trực tiếp tệp `index.html` lên thư mục gốc (`root`) của repo.
3. Vào **Settings** > **Pages** > Tại mục **Build and deployment**, chọn Branch là `main` (hoặc `master`) / thư mục `/root` rồi nhấn **Save**.
4. Trang web của bạn sẽ hoạt động trực tuyến ngay lập tức với đầy đủ tính năng.

### Cách 2: Kết Nối Google Sheets Làm Cơ Sở Dữ Liệu (Tùy chọn)
Để tự động thu thập kết quả dự đoán của người xem về Google Sheets:
1. Mở một trang tính mới tại [Google Sheets](https://sheets.google.com).
2. Vào **Tiện ích mở rộng (Extensions)** > **Apps Script**, xóa nội dung mặc định và dán đoạn mã sau:
   ```javascript
   function doPost(e) {
     try {
       var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
       var data = JSON.parse(e.postData.contents);
       sheet.appendRow([
         data.timestamp,
         data.tournament,
         data.state.points,
         data.state.playoffs.champion || "Chưa chọn",
         JSON.stringify(data.state.matches),
         JSON.stringify(data.state.standings)
       ]);
       return ContentService.createTextOutput("SUCCESS").setMimeType(ContentService.MimeType.TEXT);
     } catch (err) {
       return ContentService.createTextOutput("ERROR: " + err.message).setMimeType(ContentService.MimeType.TEXT);
     }
   }
