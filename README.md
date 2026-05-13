# 🧠 NEUROCHECK
### Early Neurological Symptoms Screening Tool

> A portable, embedded neurological screening device built on the **ESP32-S3-BOX-3**, designed to detect early warning signs of neurological conditions through guided motor, cognitive, and reflex assessments — right at the point of care.

---

## 📌 Overview

NEUROCHECK is a standalone embedded system that performs structured early-stage neurological screening without requiring hospital infrastructure. It presents interactive test modules via a touchscreen UI (powered by LVGL), collects user response data, and provides a preliminary risk assessment — making neurological screening accessible in rural clinics, schools, and homes.

This project was developed as part of an initiative to bridge the gap between clinical-grade screening tools and real-world accessibility.

---

## 🔧 Hardware

| Component | Details |
|---|---|
| Microcontroller | ESP32-S3-BOX-3 |
| Display | Built-in LCD with capacitive touch |
| Framework | ESP-IDF (v5.x) |
| UI Library | LVGL |
| Connectivity | Wi-Fi (ESP32-S3) |

**Board Support:**

| Board | Status |
|---|---|
| ESP32-S3-BOX-3 | ✅ Supported |
| ESP32-S3-BOX | ✅ Supported |
| ESP32-S3-BOX-Lite | ❌ Not Supported |

---

## 🚀 Features

- **Interactive Screening Modules** — Guided on-device tests for motor coordination, cognitive response, and reflex latency
- **Touch-based UI** — Clean, intuitive LVGL interface optimized for the ESP32-S3-BOX-3 display
- **Real-time Scoring** — Instant preliminary risk categorization based on response patterns
- **Standalone Operation** — No internet connection required for core screening
- **Wi-Fi Ready** — Architecture supports future cloud sync or remote monitoring

---

## 🛠️ Build & Flash

### Prerequisites

- [ESP-IDF v5.x](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s3/get-started/) installed and sourced
- ESP32-S3-BOX-3 connected via USB-C

### Steps

```bash
# Clone the repository
git clone https://github.com/thanuj012/NEUROCHECK.git
cd NEUROCHECK

# Set target
idf.py set-target esp32s3

# Build, flash, and monitor
idf.py flash monitor
```

> To speed up subsequent flashes (app only, skip bootloader):
> ```bash
> idf.py app-flash monitor
> ```

Press `Ctrl-]` to exit the serial monitor. Reset the board if the monitor doesn't exit cleanly.

---

## 📁 Project Structure

```
NEUROCHECK/
├── CMakeLists.txt          # Top-level CMake build config
├── sdkconfig               # ESP-IDF SDK configuration
├── sdkconfig.defaults      # Default SDK settings
├── sdkconfig.ci.box        # CI config for ESP32-S3-BOX
├── sdkconfig.ci.box-3      # CI config for ESP32-S3-BOX-3
├── sdkconfig.ci.box-lite   # CI config for BOX-Lite
├── dependencies.lock       # Component dependency lockfile
├── .clang-format           # Code style config
└── .clangd                 # Clangd LSP config
```

---

## 🧪 Screening Modules

> *(Expand as you add modules)*

- **Motor Coordination Test** — Timed touch target tracking
- **Cognitive Response Test** — Pattern recognition and recall prompts
- **Reflex Latency Test** — Visual stimulus → touch response timing

---

## 📊 Risk Assessment

After completing all modules, NEUROCHECK generates a preliminary score and categorizes the result as:

| Category | Description |
|---|---|
| 🟢 Low Risk | No significant indicators detected |
| 🟡 Moderate Risk | Some indicators present; follow-up recommended |
| 🔴 High Risk | Multiple indicators detected; clinical consultation advised |

> **Disclaimer:** NEUROCHECK is a screening aid only and does not replace professional medical diagnosis.

---


## 👤 Author

**Thanuj Srinivassalou**
B.E. Electrical & Electronics Engineering, SSN College of Engineering, Chennai
[GitHub](https://github.com/thanuj012)

---

## 📄 License

This project is open-source. Feel free to fork, build on, or contribute.

---

*Built with ESP-IDF · LVGL · ESP32-S3-BOX-3*
