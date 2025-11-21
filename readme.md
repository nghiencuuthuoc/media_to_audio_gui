# 🎵 PharmApp Media → Audio Converter  
### Convert Any Video to High-Quality Audio (MP3/M4A/OPUS/FLAC/WAV/OGG)

PharmApp Media → Audio Converter is a clean, modern Tkinter GUI tool for converting **any video or audio file** into high-quality audio formats.  
It supports **folder scanning**, **recursive processing**, **silence trimming**, **loudness normalization**, **time cutting**, and intelligent **skip-if-already-processed** using an MD5 `processed.json` state file.

The application is packaged as a **single portable executable (.exe)** for Windows, with cross-platform Python source code that also builds a macOS `.app`.

---

## ✅ **Features**

### 🎧 Audio Extraction & Conversion
- Convert video/audio into:
  - **MP3**, **M4A (AAC)**, **OPUS**, **FLAC**, **WAV**, **OGG**
- High-quality MP3:
  - **CBR** (e.g., 320k)
  - **VBR q0–q9**
- Optional enhancements:
  - **Trim silence** (head + tail)
  - **EBU R128 Loudness normalization**
  - **Mono / Stereo forcing**
  - **Custom sample rate**

### 📁 Input & Processing
- Drag-and-drop style browsing for:
  - Single file
  - Entire folder
- **Recursive** subfolder scanning
- Preview task list in TreeView
- Skip already converted files automatically using MD5 hash tracking
- Batch output folder auto-creation

### 🖥 GUI Features
- Fully themed **PharmApp UI**:
  - Warm cream background
  - Custom buttons
  - Styled TreeView
- Footer with:
  - **Clickable links**
  - **Donate buttons**
  - **Branding bar**

### 🧩 Executable & Cross-Platform
- Windows:
  - Single-file **`media_to_audio_gui.exe`**
  - Includes app icon (`nct_logo.ico`)  
- macOS:
  - Supported via PyInstaller to produce `.app`
  - Uses `nct_logo.icns` and `nct_logo.png`

---

## 📸 Screenshot

![Screenshot](./screenshot.2025-11-21%2020.10.13.png)

*(If the image fails to load, ensure the screenshot is named exactly as above and placed in the repository root.)*

---

## 🔧 Installation (From Source)

### **1. Install Dependencies**
```bash
pip install -r requirements.txt
````

Basic requirement:

* `ffmpeg` must be installed on your system and available in PATH.

### **2. Run the App**

```bash
python pharmapp_media_audio_gui.py
```

---

## 📦 Windows — Build Single-File EXE

### **Requirements**

```bash
pip install pyinstaller
```

### **Build Command**

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

After build:

* Output EXE is created in: `dist/media_to_audio_gui.exe`

---

## 🍎 macOS — Build .app Bundle

Convert PNG → ICNS (required for macOS icons):

```bash
iconutil -c icns nct_logo.iconset
```

### **Build Command**

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

Output:

* `dist/media_to_audio_gui`
* `dist/media_to_audio_gui.app`

---

## 📁 File Structure

```
/
├── pharmapp_media_audio_gui.py
├── nct_logo.ico          # Windows EXE icon
├── nct_logo.png          # Tkinter window icon
├── screenshot.2025-11-21 20.10.13.png
└── README.md
```

---

## ❤️ Donate & Support

* 🌐 Website: [https://www.nghiencuuthuoc.com](https://www.nghiencuuthuoc.com)
* 🌐 PharmApp: [https://www.pharmapp.vn](https://www.pharmapp.vn)
* 💙 Donate to PharmApp: [https://www.pharmapp.vn/Donate](https://www.pharmapp.vn/Donate)
* 💝 Donate NCT: [https://www.nghiencuuthuoc.com/p/donate.html](https://www.nghiencuuthuoc.com/p/donate.html)

---

## 📜 License

MIT License — Free to use in both personal and commercial projects.

---

## 🙌 Author

**Nghiên Cứu Thuốc**
PharmApp • Discover • Design • Optimize • Create • Deliver

