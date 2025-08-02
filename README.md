# 🔐 MT-RFID Toolkit


---

## 🇵🇱 MT-RFID Toolkit – przenośne narzędzie pentesterskie RFID (ESP32)

**MT-RFID Toolkit** to otwartoźródłowe, mobilne urządzenie pentesterskie oparte na **ESP32**, służące do testowania, emulacji i analizy tagów RFID (13.56 MHz), szczególnie systemów opartych na **MIFARE Classic**. Projekt jest w fazie aktywnego rozwoju.

---

### 🛠️ Status projektu

📅 **Etap:** Tworzenie PCB i podstawowego firmware  
🧪 **Status:** Wersja prototypowa, rozwijana na bieżąco  
📬 **Postępy:** Aktualizacje publikowane będą sukcesywnie

---

### 🔧 Założenia sprzętowe

| Komponent       | Opis                                              |
|----------------|---------------------------------------------------|
| ESP32-WROOM-32 | Mikrokontroler z WiFi + BLE                       |
| PN532          | Czytnik / zapis / emulacja tagów RFID 13.56 MHz   |
| OLED 128x64    | Wyświetlacz I2C (SSD1306)                         |
| 4 przyciski    | Sterowanie menu i funkcjami                       |
| USB-C + TP4056 | Zasilanie z USB lub LiPo (z ładowaniem)           |
| LED / Buzzer   | Sygnalizacja akcji (opcjonalnie)                  |
| I2C / UART     | Złącza dla rozszerzeń                             |

---

### 🧠 Planowane funkcje

- 📖 Odczyt UID i sektorów tagów RFID
- ✍️ Zapis danych do MIFARE (z autoryzacją Key A/B)
- 🎭 Emulacja tagów (np. MIFARE 1K)
- 🧬 Klonowanie i sniffing transmisji RFID
- 📋 Rejestrator obecności sygnałów (logger)
- 🌐 Zdalna kontrola przez WiFi lub BLE (aplikacja webowa PWA)

---

### ⚙️ Proponowany pinout (ESP32)

| Element     | GPIO ESP32 | Uwagi                  |
|-------------|------------|------------------------|
| OLED SDA    | GPIO21     | I2C                    |
| OLED SCL    | GPIO22     | I2C                    |
| PN532 TX    | GPIO17     | UART (lub SPI)         |
| PN532 RX    | GPIO16     | UART (lub SPI)         |
| Button K1   | GPIO32     | Nawigacja              |
| Button K2   | GPIO33     | Nawigacja              |
| Button K3   | GPIO25     | Akcja                  |
| Button K4   | GPIO26     | Akcja                  |
| LED/Buzzer  | GPIO27     | Sygnalizacja (opcjonalna) |

---

### 📎 Plan rozwoju

- [ ] Projekt PCB (KiCad)
- [ ] Firmware: menu + odczyt UID
- [ ] Emulacja i zapis do MIFARE
- [ ] Logger RFID
- [ ] Interfejs zdalny (BLE/WiFi)

---

## 🇬🇧 MT-RFID Toolkit – Portable RFID Pentest Tool (ESP32)

**MT-RFID Toolkit** is an open-source, portable pentesting device based on **ESP32**, designed for reading, emulating, and analyzing 13.56 MHz RFID tags – especially **MIFARE Classic** systems. The project is currently under active development.

---

### 🛠️ Project Status

📅 **Phase:** PCB + firmware prototyping  
🧪 **Status:** Experimental, evolving version  
📬 **Updates:** Work in progress, commits coming soon

---

### 🔧 Hardware Overview

| Component       | Description                                       |
|----------------|---------------------------------------------------|
| ESP32-WROOM-32 | Microcontroller with WiFi + BLE                   |
| PN532          | RFID Reader/Writer/Emulator (13.56 MHz)           |
| OLED 128x64    | Display via I2C (SSD1306)                         |
| 4 Buttons      | UI navigation and actions                         |
| USB-C + TP4056 | Power input and LiPo charging                    |
| LEDs/Buzzer    | Optional visual/audio feedback                    |
| I2C / UART     | External extension ports                          |

---

### 🧠 Planned Features

- 📖 Read tag UID and sector content
- ✍️ Write to MIFARE tags (with Key A/B auth)
- 🎭 Emulate RFID tags (e.g., MIFARE 1K)
- 🧬 Clone/sniff RFID communication
- 📋 Passive RFID signal logger
- 🌐 Remote control via BLE or WiFi (PWA interface)

---

### ⚙️ Suggested Pinout (ESP32)

| Element     | GPIO       | Description           |
|-------------|------------|------------------------|
| OLED SDA    | GPIO21     | I2C                   |
| OLED SCL    | GPIO22     | I2C                   |
| PN532 TX    | GPIO17     | UART (or SPI)         |
| PN532 RX    | GPIO16     | UART (or SPI)         |
| Button K1   | GPIO32     | UI navigation         |
| Button K2   | GPIO33     | UI navigation         |
| Button K3   | GPIO25     | Action button         |
| Button K4   | GPIO26     | Action button         |
| LED/Buzzer  | GPIO27     | Feedback (optional)   |

---

### 📎 Development Roadmap

- [ ] Design schematic and PCB (KiCad)
- [ ] Firmware: menu system + UID reading
- [ ] MIFARE write/emulate support
- [ ] RFID sniffing and logging
- [ ] Web UI for BLE/WiFi control (PWA)

---

## 💬 Contributions & License

This is a hobby project created for **educational and testing purposes**.  
All contributions and suggestions are welcome. Final license (MIT/GPL) will be confirmed upon first public release.

