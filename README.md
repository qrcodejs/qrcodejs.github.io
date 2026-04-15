# ✨ QR Code Studio

A powerful, all-in-one QR code generator and scanner web application. Create beautiful, customizable QR codes with embedded images, emojis, gradient colors, and multiple dot styles. Scan QR codes from your camera or uploaded files with multi-engine detection.

![QR Code Studio](https://img.shields.io/badge/QR%20Code-Studio-6c5ce7?style=for-the-badge&logo=qrcode&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-00cec9?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML-Single%20File-fd79a8?style=for-the-badge&logo=html5&logoColor=white)

## 🚀 Live Demo

**[https://qrcodejs.github.io](https://qrcodejs.github.io)**

---

## 📸 Screenshots

### Generator Mode
<img width="1114" height="749" alt="image" src="https://github.com/user-attachments/assets/1acc86e8-1f3a-4545-8c76-fcc5a77f80be" />


### Scanner Mode
<img width="1114" height="774" alt="image" src="https://github.com/user-attachments/assets/7df00847-1b1d-4ad0-9e85-64fb54fe12cf" />


---

## ✨ Features

### 🎨 QR Code Generator

- **Rich Content Support** — URLs, plain text, and any UTF-8 encoded data
- **Gradient Colors** — Apply linear gradient foregrounds with custom start/end colors
- **Color Presets** — 8 curated gradient presets for quick styling
- **Custom Colors** — Full control over foreground and background colors
- **Dot Styles** — Square, rounded, and circular dot rendering
- **Container Shapes** — Square, rounded, or circular QR code containers
- **Emoji Embedding** — Embed any of 48 emojis directly into the QR code center
- **Image Embedding** — Upload custom logos/images with rounded corners and white background options
- **Error Correction Levels** — L (7%), M (15%), Q (25%), H (30%)
- **Adjustable Size** — 128px to 512px with real-time preview
- **Adjustable Margin** — 0 to 10 module margin control
- **Export Options** — Download as PNG, SVG, or copy to clipboard
- **Persistent State** — All settings saved to localStorage automatically

### 📷 QR Code Scanner

- **Camera Scanning** — Real-time QR code detection from device camera
- **File Scanning** — Upload QR code images for instant decoding
- **Drag & Drop** — Drop image files directly onto the scan area
- **Multi-Engine Detection** — Uses multiple scanning engines for maximum compatibility:
  - **QrScanner (ZXing-based)** — Superior detection for styled QR codes with dots, colors, gradients, and embedded logos
  - **jsQR** — Fast fallback engine with multi-scale scanning
- **Multi-Scale Processing** — Automatically tries multiple image scales and preprocessing techniques
- **Image Preprocessing** — Contrast enhancement, grayscale conversion, and binary thresholding for difficult QR codes
- **Smart Results** — Auto-detects URLs with clickable links and open-in-browser option
- **Use in Generator** — One-click transfer of scanned content to the generator
- **Scan History** — Keeps the last 10 scanned QR codes with timestamps
- **History Management** — Click to copy, delete individual entries, or clear all

### 🎯 General

- **Single HTML File** — No build tools, no dependencies to install, no server required
- **Fully Responsive** — Works on desktop, tablet, and mobile devices
- **Dark Theme** — Beautiful dark UI with animated gradient background
- **Offline Capable** — Works without internet after initial load (CDN libraries cached)
- **Zero Configuration** — Open the file and start using immediately

---

## 📦 Getting Started

### Option 1: Direct Use

1. Open **[https://qrcodejs.github.io](https://qrcodejs.github.io)** in your browser
2. Start generating or scanning QR codes

### Option 2: Local Use

```bash
git clone https://github.com/qrcodejs/qrcodejs.github.io.git
cd qrcodejs.github.io
```

Open `index.html` in your browser. That's it — no build step, no server needed.

### Option 3: Download

Download `index.html` directly and open it in any modern browser.

---

## 🏗️ Architecture

```
index.html (single file)
├── HTML Structure
│   ├── Generator Mode
│   │   ├── Settings Panel (content, colors, style, embed)
│   │   └── Preview Panel (canvas, download buttons)
│   └── Scanner Mode
│       ├── Scanner Panel (camera, file upload, results)
│       └── History Panel (last 10 scans)
├── CSS Styles
│   ├── Dark theme with CSS variables
│   ├── Animated gradient background
│   ├── Responsive grid layouts
│   └── Smooth transitions & animations
└── JavaScript
    ├── QR Generator (qrcode-generator library)
    ├── Multi-Engine Scanner
    │   ├── QrScanner (ZXing-based) — primary
    │   ├── jsQR — fallback
    │   └── Image preprocessing pipeline
    ├── State Management (localStorage)
    └── History Management (localStorage)
```

---

## 🔧 External Libraries

| Library | Purpose | CDN |
|---------|---------|-----|
| [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) | QR code generation | jsDelivr |
| [QrScanner](https://github.com/nimiq/qr-scanner) | ZXing-based QR scanning (styled QR support) | unpkg |
| [jsQR](https://github.com/cozmo/jsQR) | Fallback QR code scanning | jsDelivr |

All libraries are loaded from CDNs with graceful fallback — if one fails to load, the application continues working with available engines.

---

## 📖 Usage Guide

### Generating a QR Code

1. **Enter content** — Type or paste a URL, text, or any data
2. **Customize colors** — Pick a preset or set custom foreground/background colors
3. **Choose style** — Select dot style (square/rounded/dots) and container shape
4. **Embed content** *(optional)* — Add an emoji or upload a logo image
5. **Adjust settings** — Set size, margin, and error correction level
6. **Export** — Download as PNG/SVG or copy to clipboard

> 💡 **Tip:** Use **High (30%)** error correction when embedding logos or emojis to ensure the QR code remains scannable.

### Scanning a QR Code

1. **Switch to Scan mode** using the top toggle
2. **Camera scan** — Click "Start Camera" and point at a QR code
3. **File scan** — Click the upload area or drag & drop an image
4. **Use results** — Copy the content, open URLs, or send to the generator
5. **Browse history** — Click any history item to view and copy

> 💡 **Tip:** The scanner uses ZXing-based detection which handles styled QR codes (colored, dotted, with logos) much better than basic scanners.

---

## 🤝 Contributing

Contributions are welcome! Since this is a single-file application, contributing is straightforward:

1. Fork the repository
2. Edit `index.html`
3. Test in your browser
4. Submit a pull request

### Guidelines

- Maintain the single-file architecture
- Keep external dependencies minimal
- Test on both desktop and mobile
- Ensure dark theme consistency
- Preserve localStorage backward compatibility

---

## 📄 License

MIT
