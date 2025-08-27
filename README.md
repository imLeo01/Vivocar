# Vivocar
VimoCar là một ứng dụng web demo mô phỏng dịch vụ đặt xe công nghệ (xe ôm, taxi) chạy trực tiếp trên trình duyệt, không cần backend. Ứng dụng sử dụng bản đồ Leaflet + OpenStreetMap để hiển thị tuyến đường, kết hợp API Nominatim (geocoding) và OSRM (routing), xem giá cước ước tính bằng fuzzy logic pricing.
# VimoCar — Ride-Hailing Web Demo 🚖🏍️

**VimoCar** là một ứng dụng web demo đặt xe công nghệ, chạy trực tiếp trên trình duyệt (HTML/JS/CSS).  
Dự án này mô phỏng quy trình đặt xe tương tự Grab/Gojek/Be nhưng ở dạng demo học tập.

## 🚀 Tính năng

- 🌍 Hiển thị bản đồ với **Leaflet + OpenStreetMap**  
- 📍 Chọn điểm đón/điểm đến bằng click map hoặc nhập địa chỉ (tự động gợi ý từ **Nominatim API**)  
- 🚗 Chọn loại xe: **Xe máy, Xe hơi 4 chỗ, Xe 7 chỗ, Premium**  
- 💰 Tính giá ước tính bằng **fuzzy logic pricing** (dựa trên khoảng cách, thời gian, mức kẹt xe, loại xe, phí chờ, mã khuyến mãi)  
- 👨‍✈️ Mô phỏng tài xế (tên, xe, biển số) di chuyển đến điểm đón  
- 🛣️ Sau khi đón, mô phỏng lộ trình di chuyển đến điểm đến  
- ❌ Cho phép hủy chuyến với lý do hủy  
- ⭐ Đánh giá tài xế sau khi kết thúc chuyến  
- 📜 Lưu **lịch sử đặt xe** trong `localStorage`  

## 🖼️ Avatar Xe

- Nếu chọn **xe máy** → icon xe máy 🏍️  
- Nếu chọn **ô tô** → icon xe hơi 🚗  
- Avatar hiển thị trên bản đồ khi tài xế di chuyển.

## 🔧 Công nghệ

- [Leaflet](https://leafletjs.com/) — hiển thị bản đồ  
- [OpenStreetMap](https://www.openstreetmap.org/) — dữ liệu bản đồ  
- [Nominatim](https://nominatim.org/) — geocoding (chuyển địa chỉ ↔ tọa độ)  
- [OSRM](http://project-osrm.org/) — định tuyến đường đi  

## 📂 Cài đặt & Chạy

1. Clone repo về:
   ```bash
   git clone https://github.com/<your-username>/vivocar-demo.git
   cd vivocar-demo
   ```
2. Mở file vivocar.html trực tiếp trên trình duyệt (không cần server).
👉 Hoặc chạy với Python local server:
   ```bash
   python -m http.server 8000
   ```
## ⚠️ Lưu ý

Đây chỉ là demo client-side, dùng public API (không có backend).

Không dùng để triển khai thương mại.

Có thể bị giới hạn request từ Nominatim/OSRM nếu dùng nhiều.
