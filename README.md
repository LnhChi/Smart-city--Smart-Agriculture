<h2 align="center">
    <a href="https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin">
    🎓 Faculty of Information Technology (DaiNam University)
    </a>
</h2>
<h2 align="center">
    Hệ Thống Nhận Diện Cỏ Dại Thông Minh<br/>
    <small>Smart Weed Detection System</small>
</h2>
<div align="center">
    <p align="center">
        <img src="images/fitdnu_logo.png" alt="AIoTLab Logo" width="180"/>
        <img src="images/dnu_logo.png" alt="DaiNam University Logo" width="200"/>
    </p>

[![AIoTLab](https://img.shields.io/badge/AIoTLab-green?style=for-the-badge)](https://www.facebook.com/DNUAIoTLab)
[![Faculty of Information Technology](https://img.shields.io/badge/Faculty%20of%20Information%20Technology-blue?style=for-the-badge)](https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin)
[![DaiNam University](https://img.shields.io/badge/DaiNam%20University-orange?style=for-the-badge)](https://dainam.edu.vn)

</div>

## 📖 1. Giới thiệu
Hệ thống **Nhận diện Cỏ dại Thông minh (Smart Weed Detection)** là một giải pháp **AIoT** ứng dụng trong nông nghiệp, giúp tự động phát hiện cỏ dại trên đồng ruộng theo thời gian thực thông qua camera. Hệ thống được xây dựng theo mô hình phân tách rõ ràng giữa **module thị giác máy tính (Python)** và **backend xử lý nghiệp vụ (Node.js + Express)**, kết nối với **MongoDB**, **Blockchain** và **Telegram** để lưu trữ, bảo toàn và cảnh báo dữ liệu.

Các giá trị cốt lõi mà hệ thống mang lại:

- **Nhận diện thời gian thực**: Mô hình thị giác máy tính (run.py) phân tích khung hình từ camera/video, đếm số cây cỏ dại hiện tại, tổng tích lũy và độ tin cậy của mỗi lần phát hiện.
- **Lưu trữ tập trung**: Mỗi phiên giám sát được lưu vào MongoDB, chỉ ghi nhận khi tổng số cỏ dại tăng để tránh dư thừa dữ liệu.
- **Chống giả mạo dữ liệu (Blockchain)**: Tổng số cỏ dại được đồng bộ song song lên một blockchain gateway và liên tục đối soát với MongoDB để đảm bảo tính toàn vẹn.
- **Cảnh báo tức thời**: Khi phát hiện vượt ngưỡng, hệ thống gửi ảnh chụp kèm thông tin chi tiết qua bot Telegram (có cơ chế chống spam).
- **Giám sát trực quan**: Giao diện web hiển thị camera trực tiếp, các chỉ số real-time, biểu đồ và lịch sử phát hiện.

Thay vì kiểm tra cỏ dại thủ công, tốn công và thiếu dữ liệu lịch sử, giải pháp này cung cấp một nền tảng tự động hóa, minh bạch và dễ theo dõi cho công tác quản lý đồng ruộng.

## 🖼️ 2. Poster
<div align="center">

![Poster hệ thống](./images/poster.jpg)

<p>
<a href="./images/poster.pdf">Nhấn vô đây để xem chi tiết Poster (PDF)</a>
</p>

</div>
## 🔧 3. Các công nghệ được sử dụng
<div align="center">

### Nền Tảng Chính
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Express](https://img.shields.io/badge/Express%205-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)

### Cơ sở dữ liệu & Lưu trữ
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Mongoose](https://img.shields.io/badge/Mongoose-880000?style=for-the-badge&logo=mongoose&logoColor=white)](https://mongoosejs.com/)
[![Blockchain](https://img.shields.io/badge/Blockchain%20Gateway-121D33?style=for-the-badge&logo=hyperledger&logoColor=white)](#)

### Thị giác máy tính & Tích hợp
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Telegram](https://img.shields.io/badge/Telegram%20Bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://core.telegram.org/bots)

### Giao diện (Server-side Rendering)
[![Pug](https://img.shields.io/badge/Pug-A86454?style=for-the-badge&logo=pug&logoColor=white)](https://pugjs.org/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white)](https://www.chartjs.org/)

### Công cụ & Môi trường
[![ts-node](https://img.shields.io/badge/ts--node-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://typestrong.org/ts-node/)
[![Nodemon](https://img.shields.io/badge/Nodemon-76D04B?style=for-the-badge&logo=nodemon&logoColor=white)](https://nodemon.io/)
[![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com/)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
</div>

## 🏗️ 4. Kiến trúc & Luồng dữ liệu

Dự án được tổ chức theo mô hình phân lớp (layered) rõ ràng, dễ bảo trì và dễ kiểm thử:

```
Backend/
├── config/          # Cấu hình kết nối MongoDB (database.ts)
├── models/          # Schema Mongoose: weed.model.ts
├── validations/     # Kiểm tra & chuẩn hóa dữ liệu đầu vào (weed.validate.ts)
├── services/        # Logic nghiệp vụ chính: weed.service.ts
├── controllers/     # Xử lý request/response: weed.controller.ts
├── routes/          # Định nghĩa endpoint (home.routes.ts, index.routes.ts)
├── helpers/         # Tích hợp ngoài: blockchain.helper.ts, telegram.helper.ts
├── views/           # Template Pug (layouts + pages)
├── public/          # JS frontend, Chart.js, ảnh chụp cảnh báo
├── index.ts         # Điểm khởi động ứng dụng Express
└── script.ts        # Script tiện ích xóa toàn bộ dữ liệu collection weeds
```

**Luồng dữ liệu tổng quát:**

1. **Module Python (`run.py`)** nhận diện cỏ dại từ camera/video, sau đó gửi khung hình (ảnh base64) cùng các chỉ số (`currentWeeds`, `totalWeeds`, `confidence`) tới backend qua API stream.
2. **Backend (Express)** nhận và kiểm tra dữ liệu, lưu khung hình mới nhất trong RAM để hiển thị live, đồng thời đẩy vào lịch sử để vẽ biểu đồ.
3. Khi **tổng số cỏ dại tăng**, backend ghi bản ghi vào **MongoDB** và **đồng bộ song song** tổng số đó lên **Blockchain gateway** (đối soát Mongo ↔ Chain).
4. Nếu lần phát hiện được đánh dấu cảnh báo, backend gửi **ảnh + thông tin chi tiết qua Telegram** (có cooldown chống gửi liên tục).
5. **Giao diện web** liên tục polling để cập nhật camera trực tiếp, các chỉ số, biểu đồ và bảng lịch sử.

## 🚀 5. Các tính năng chính

### 📹 Giám sát & Điều khiển Camera
- ▶️ Khởi động camera ở hai chế độ: **demo** (chạy video mẫu) và **realtime** (luồng camera trực tiếp).
- ⏹️ Dừng tiến trình nhận diện an toàn (tự xử lý theo từng hệ điều hành).
- 🖼️ Hiển thị khung hình mới nhất theo cơ chế phiên bản (chỉ tải lại khi có frame mới — tiết kiệm băng thông).

### 🌿 Nhận diện & Ghi nhận Dữ liệu
- 🔢 Theo dõi số cỏ dại **hiện tại**, **tổng tích lũy** và **độ tin cậy** của từng lần phát hiện.
- 💾 Lưu trữ thông minh: chỉ ghi vào MongoDB khi tổng số cỏ dại tăng, tránh dư thừa.
- 📜 Lưu lịch sử trong bộ nhớ (RAM) để hiển thị biểu đồ ngay cả khi DB chưa có dữ liệu.

### 🔗 Đồng bộ & Bảo toàn Dữ liệu bằng Blockchain
- 🧩 Đồng bộ tổng số cỏ dại lên **World State** của blockchain qua gateway.
- ⚖️ Tự động **đối soát** dữ liệu giữa MongoDB và Blockchain, cảnh báo khi có sai lệch.
- 🆔 Ghi nhận mã giao dịch (txId) trả về từ blockchain để truy vết.

### 🔔 Cảnh báo qua Telegram
- 📩 Gửi **ảnh chụp hiện trường** kèm thời gian, số lượng, độ tin cậy và nguồn phát hiện.
- 🕒 Cơ chế **cooldown** (mặc định 20 giây) chống gửi cảnh báo liên tục gây spam.
- 🗄️ Lưu lại ảnh cảnh báo vào thư mục `public/screenshots`.

### 📊 Giao diện Web trực quan
- 📈 Biểu đồ cột + đường (Chart.js) thể hiện số cỏ dại hiện tại và tổng tích lũy.
- 🧾 Bảng lịch sử phát hiện gần đây với thời gian, số lượng, độ tin cậy, nguồn.
- ⚡ Cập nhật real-time qua polling khung hình và dữ liệu JSON.

## 🌐 6. Danh sách API

| Phương thức | Endpoint | Chức năng |
|-------------|----------|-----------|
| `GET` | `/` hoặc `/home` | Trang chủ hệ thống |
| `GET` | `/home/weed-detection` | Trang lịch sử (kèm `?limit=` để lấy dữ liệu biểu đồ dạng JSON) |
| `GET` | `/home/weed-detection/live` | Trang camera trực tiếp (`?frame=1` lấy ảnh JPEG, `?data=json` lấy trạng thái) |
| `POST` | `/home/api/weed-detection/stream` | Nhận dữ liệu nhận diện từ module Python |
| `POST` | `/home/api/camera/start` | Khởi động camera (`mode: "demo" \| "realtime"`) |
| `POST` | `/home/api/camera/stop` | Dừng camera |

## 🖼️ 7. Giao diện chính
<div align="center">

![Giao diện camera trực tiếp](./images/live_detection.png)

![Biểu đồ thống kê cỏ dại](./images/weed_chart.png)

![Cảnh báo Telegram](./images/telegram_alert.png)

</div>

## ⚙️ 8. Cài đặt và Chạy Hệ Thống

> **Yêu cầu môi trường:** Node.js >= 18, MongoDB (cục bộ hoặc MongoDB Atlas). Module nhận diện chạy bằng Python (tùy chọn, cần nếu muốn camera hoạt động thật).

**Bước 1**: Clone project
```bash
git clone <ĐƯỜNG_DẪN_REPO_CỦA_BẠN>
cd Backend
```

**Bước 2**: Cài đặt các dependency
```bash
npm install
```
> Script `postinstall` sẽ tự động sao chép thư viện Chart.js vào `public/vendor`.

**Bước 3**: Tạo file cấu hình môi trường `.env`
```bash
# === Server ===
PORT=3000
CORS_ORIGIN=http://localhost:3000

# === MongoDB ===
MONGOOSE_URL=mongodb://localhost:27017/weed_detection

# === Blockchain Gateway (để "0" hoặc "false" nếu chưa dùng) ===
BLOCKCHAIN_GATEWAY_URL=http://localhost:8080/api/weed-detection
WEED_WORLD_STATE_KEY=weed-total

# === Telegram (để trống nếu chưa dùng) ===
TELEGRAM_TOKEN=your_bot_token
CHAT_ID=your_chat_id
ALERT_COOLDOWN=20

# === Stream URL cho module Python ===
API_STREAM_URL=http://localhost:3000/home/api/weed-detection/stream
```

**Bước 4**: Chạy ở chế độ phát triển (tự reload khi sửa code)
```bash
npm run dev
```
Hoặc chạy bình thường:
```bash
npm start
```

**Bước 5**: Truy cập hệ thống
- Mở trình duyệt: `http://localhost:3000`

**Bước 6 (tùy chọn)**: Cấu hình module nhận diện Python
> Trong `services/weed.service.ts`, các đường dẫn tới Python và script `run.py` đang được đặt cố định cho máy phát triển (ví dụ `C:\Users\admin\...`).
> Khi triển khai trên máy khác, cần chỉnh lại các đường dẫn `visionRoot`, `pythonExe`, `scriptPath` cho phù hợp (hoặc tốt hơn là chuyển chúng ra biến môi trường).

**Tiện ích**: Xóa toàn bộ dữ liệu trong collection `weeds`
```bash
npx ts-node script.ts
```

## 📞 9. Support & Liên Hệ

- 📧 Email: [your_email@example.com]
- 🌐 Website: [https://dainam.edu.vn]

<div align="center">

Made with 💚 by Nguyễn Thị Linh Chi

</div>
