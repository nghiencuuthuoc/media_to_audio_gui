# 🎵 PharmApp Media → Audio Converter  
### Công cụ chuyển đổi Video sang Audio chất lượng cao (MP3/M4A/OPUS/FLAC/WAV/OGG)

**PharmApp Media → Audio Converter** là ứng dụng giao diện Tkinter thân thiện, dùng để chuyển đổi **mọi định dạng video** sang **audio chất lượng cao**.  
Hỗ trợ đầy đủ tính năng: quét thư mục, xử lý hàng loạt, bỏ qua file đã xử lý, cắt thời gian, chuẩn hóa âm lượng, trim âm thừa, và xuất audio tối ưu.

Ứng dụng được đóng gói thành **một file .exe duy nhất cho Windows**, đồng thời hỗ trợ build `.app` cho macOS.

---

## ✅ **Tính năng chính**

### 🎧 Trích xuất & chuyển đổi audio
- Chuyển video/audio sang:
  - **MP3**, **M4A (AAC)**, **OPUS**, **FLAC**, **WAV**, **OGG**
- MP3 chất lượng cao:
  - **CBR** (ví dụ 320k)
  - **VBR** (q0–q9)
- Tùy chọn nâng cao:
  - **Trim silence** (cắt im lặng đầu/cuối)
  - **Chuẩn hóa loudness (EBU R128)**
  - Ép **mono** hoặc **stereo**
  - Đặt **Sample rate** thủ công
  - Cắt đoạn: **Start** / **End**

### 📁 Xử lý video hàng loạt
- Chọn **file** hoặc **folder**
- Hỗ trợ **quét subfolder (Recursive)**
- Hiển thị danh sách file trong **TreeView**
- Tự động **skip file đã xử lý** dựa trên MD5  
  (lưu vào `processed.json`)

### 🖥 Giao diện PharmApp
- Màu nền kem #fdf5e6
- Nút bấm thiết kế riêng
- TreeView tuỳ biến
- Footer gồm:
  - Link website
  - Zalo
  - Nút Donate PharmApp / NCT

### 🧩 Đa nền tảng
- Windows:
  - Có file portable `.exe`
  - Tích hợp `nct_logo.ico`
- macOS:
  - Build `.app` bằng PyInstaller
  - Dùng icon `nct_logo.icns`

---

## 📸 **Screenshot**

![Screenshot](./screenshot.2025-11-21%2020.10.13.png)

---

## 🔧 **Cài đặt & chạy (bản mã nguồn Python)**

### 1. Cài đặt thư viện
```bash
pip install -r requirements.txt
````

Yêu cầu bắt buộc:

* **ffmpeg** phải có trong PATH
  (Windows có thể dùng bản portable)

### 2. Chạy ứng dụng

```bash
python pharmapp_media_audio_gui.py
```

---

## 📦 **Build Windows (.exe 1 file)**

### Cài PyInstaller

```bash
pip install pyinstaller
```

### Đặt file icon trong thư mục dự án:

```
nct_logo.ico
nct_logo.png
```

### Lệnh build `.exe`:

```bash
pyinstaller ^
  --noconfirm ^
  --clean ^
  --onefile ^
  --windowed ^
  --icon nct_logo.ico ^
  --add-data "nct_logo.png;." ^
  pharmapp_media_audio_gui.py
```

Kết quả:

```
dist/media_to_audio_gui.exe
```

---

## 🍎 **Build macOS (.app)**

Chuyển PNG sang ICNS (nếu chưa có):

```bash
iconutil -c icns nct_logo.iconset
```

### Build:

```bash
pyinstaller \
  --noconfirm \
  --clean \
  --onefile \
  --windowed \
  --icon nct_logo.icns \
  --add-data "nct_logo.png:." \
  pharmapp_media_audio_gui.py
```

Kết quả:

* `dist/media_to_audio_gui`
* `dist/media_to_audio_gui.app`

---

## 📁 **Cấu trúc thư mục gợi ý**

```
/
├── pharmapp_media_audio_gui.py
├── nct_logo.ico
├── nct_logo.png
├── screenshot.2025-11-21 20.10.13.png
└── README.md
```

---

## ❤️ **Ủng hộ & kết nối**

* 🌐 Website: [https://www.nghiencuuthuoc.com](https://www.nghiencuuthuoc.com)
* 🌐 PharmApp: [https://www.pharmapp.vn](https://www.pharmapp.vn)
* 💙 Donate PharmApp: [https://www.pharmapp.vn/Donate](https://www.pharmapp.vn/Donate)
* 💝 Donate NCT: [https://www.nghiencuuthuoc.com/p/donate.html](https://www.nghiencuuthuoc.com/p/donate.html)
* 📞 Zalo: +84888999311

---

## 📜 **Giấy phép**

MIT License — được phép sử dụng thương mại và cá nhân.

---

## 🙌 **Tác giả**

**Nghiên Cứu Thuốc**
PharmApp • Discover • Design • Optimize • Create • Deliver
