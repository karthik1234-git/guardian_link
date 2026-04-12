# GuardianLink — Real-Time Geofencing & GPS Tracker

> **IoT Mini Project** | Department of Computer Science & Engineering  
> Academic Year: 2024–25 | Submitted in partial fulfillment of the requirements for the degree of B.E. / B.Tech.

---

## 📌 Project Objective

GuardianLink is a real-time GPS tracking and geofencing system designed to enhance the safety of **dementia and Alzheimer's patients**. The system continuously monitors the patient's location using an IoT device and sends live coordinates to a web dashboard. If the patient moves outside a pre-defined safe zone (geofence), an automatic alert is triggered — notifying caregivers instantly.

---

## 🔧 Hardware Used

| Component | Description |
|-----------|-------------|
| **ESP32** | Main microcontroller with built-in Wi-Fi & Bluetooth |
| **GPS Neo-6M** | GPS module for real-time latitude/longitude data |
| **GSM SIM800L** (optional) | For SMS-based alerts when Wi-Fi is unavailable |
| **18650 Li-ion Battery** | Portable power supply for the wearable unit |
| **LED + Buzzer** | Local visual/audio alert on geofence breach |

---

## 💻 Software Stack

| Layer | Technology |
|-------|------------|
| **Firmware** | Arduino IDE (C/C++) for ESP32 |
| **Backend / Database** | Google Firebase Realtime Database |
| **Frontend** | HTML5, Tailwind CSS, JavaScript |
| **Maps** | Leaflet.js (OpenStreetMap tiles) |
| **Hosting** | GitHub Pages |

---

## 🗂️ Project Structure

```
guardian_link/
├── index.html        # Main dashboard (GitHub Pages entry point)
├── README.md         # Project documentation
├── LICENSE           # MIT License
└── .gitignore        # Git ignore rules
```

---

## 🚀 How to Run

### 1. Hardware Setup
1. Connect the GPS Neo-6M module to the ESP32 (TX → GPIO 16, RX → GPIO 17).
2. Upload the Arduino firmware to the ESP32 using Arduino IDE.
3. Configure your Firebase project credentials in the firmware (`firebaseConfig`).
4. Power the device using a USB cable or battery pack.

### 2. Web Dashboard
1. Clone this repository:
   ```bash
   git clone https://github.com/karthik1234-git/guardian_link.git
   ```
2. Open `index.html` in any modern web browser **or** visit the live GitHub Pages URL:  
   👉 [https://karthik1234-git.github.io/guardian_link/](https://karthik1234-git.github.io/guardian_link/)
3. The dashboard auto-connects to Firebase and displays the live device location on the map.

### 3. Firebase Configuration
- Create a Firebase project at [https://firebase.google.com](https://firebase.google.com).
- Enable **Realtime Database** and set read/write rules for testing.
- Replace the placeholder config in `index.html` with your own Firebase credentials.

---

## 📡 System Architecture

```
[ESP32 + GPS Neo-6M]
        |
        | (Wi-Fi / HTTPS)
        ▼
[Firebase Realtime Database]
        |
        | (JavaScript SDK)
        ▼
[Web Dashboard — index.html]
        |
        ▼
[Leaflet.js Map + Geofence Alert]
```

---

## ✅ Features

- 📍 **Real-Time Location Tracking** — Live GPS coordinates streamed via Firebase.
- 🔴 **Geofence Alerts** — Visual and audio alerts when the patient leaves the safe zone.
- 🗺️ **Interactive Map** — Leaflet.js powered map with custom patient/geofence markers.
- 📶 **Device Health Monitoring** — Battery level and connectivity status displayed on dashboard.
- 📱 **Responsive Design** — Works on desktop and mobile browsers (Tailwind CSS).
- ⚡ **Low Latency** — Firebase Realtime Database ensures sub-second location updates.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- [Leaflet.js](https://leafletjs.com/) — Open-source JavaScript maps library.
- [Firebase](https://firebase.google.com/) — Google's real-time backend platform.
- [Tailwind CSS](https://tailwindcss.com/) — Utility-first CSS framework.
- [OpenStreetMap](https://www.openstreetmap.org/) — Free map data providers.
