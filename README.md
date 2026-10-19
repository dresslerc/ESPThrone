# 🚽 ESPThrone

### Smart Toilet Control with ESPHome & Home Assistant

**ESPThrone** is an open-source ESPHome project that brings smart home integration to the **EPLO E18 Smart Toilet** using the **Seeed Studio XIAO Smart IR Mate**.

By capturing and reproducing the toilet's original infrared (IR) remote commands, ESPThrone allows you to control your toilet directly from **Home Assistant** — without modifying the toilet, installing custom wiring, or relying on cloud services.

From flushing and adjusting bidet settings to controlling seat temperature, lighting, and automatic functions, ESPThrone makes your smart toilet part of your smart home ecosystem.

## ✨ Features

ESPThrone exposes the following controls directly in Home Assistant:

| Category | Supported Functions |
|---|---|
| 🚽 Flushing | Full Flush, Half Flush, Automatic Flush Toggle |
| 💦 Bidet | Front Wash, Rear Wash, Stop |
| 🌡️ Water Temperature | Off, 86°F, 90°F, 93°F, 96°F, 99°F |
| ♨️ Seat Temperature | Off, 86°F, 90°F, 93°F, 96°F, 99°F |
| 💨 Dryer | Adjustable Levels 0–5 |
| 💧 Spray Settings | Spray Position (1–5), Spray Pressure (1–3) |
| 🛡️ Comfort Features | Foam Shield, Automatic Pre-Wetting |
| 💡 Lighting | Toilet Light, Automatic Night Light |
| 🔇 Other Controls | Silent Mode Toggle, Lid Toggle, Seat Toggle |
| 📡 Diagnostics | Wi-Fi Signal, Uptime, IP Address, Connection Status |

## 🛠️ Hardware

- **Seeed Studio XIAO Smart IR Mate** — Infrared transmitter and receiver hardware
- **XIAO ESP32C3** — ESP32-based microcontroller
- **EPLO E18 Smart Toilet** — Target device
- **Home Assistant** — Smart home platform
- **ESPHome** — Firmware and device integration

## ⚙️ How It Works

ESPThrone uses ESPHome's infrared transmitter functionality to reproduce commands from the EPLO E18's original remote control.

The project utilizes captured IR signals encoded in **Pronto format**, with dynamically generated command sequences for adjustable settings such as water temperature, seat temperature, dryer level, spray position, and spray pressure.

Commands are transmitted at approximately **38 kHz** and repeated three times to improve reception reliability.

Once connected to Home Assistant through ESPHome's native API, the controls become available as buttons and dropdown selections that can be added to dashboards, scripts, and automations.

### Key Benefits

- ✅ **Local Control** — No cloud service, manufacturer account, or internet connection required for normal operation
- ✅ **No Toilet Modifications** — Communicates using the existing infrared interface
- ✅ **Native Home Assistant Integration** — Controls appear as standard Home Assistant entities
- ✅ **Automation Ready** — Use controls in Home Assistant scripts, dashboards, and automations
- ✅ **Over-the-Air Updates** — Update firmware wirelessly through ESPHome
- ✅ **Open Source** — Customize or expand functionality to suit your needs

## 🏠 Home Assistant Integration

ESPThrone integrates directly with Home Assistant, allowing you to build a custom toilet control dashboard and incorporate functions into your existing smart home automations.

**Note:** ESPThrone uses one-way infrared commands. Most controls do not receive confirmation of the toilet's actual state. Dropdown selections use ESPHome's optimistic state handling, meaning Home Assistant displays the last selected value rather than a verified setting.

## 🚀 Project Goal

The goal of ESPThrone is simple: **make smart toilets truly smart by bringing their existing features into an open, locally controlled home automation ecosystem.**

No proprietary cloud integrations. No unnecessary complexity. Just ESPHome, infrared control, and Home Assistant.

---

*ESPThrone is an independent community project and is not affiliated with or endorsed by EPLO or Seeed Studio.*
