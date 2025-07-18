# AXAuthNode

AXAuthNode is a lightweight, extensible Python-based BBS-style node server for amateur packet radio over AX.25.  
It supports authenticated messaging, FX.25 framing, modular extensions, and live chess over RF.

## 📡 Features

- AX.25/FX.25 support via **Direwolf** (software TNC)
- Authenticated messaging using **Chattervox** as the backend
- Modular routing engine for:
  - `/chat` – IRC-style rooms
  - `/games` – for example turn-based boardgames with stateful games
- Works with radio-connected nodes via Digirig or similar USB interfaces
- Designed for Raspberry Pi + headless CLI setups

## 🧩 Architecture

AXAuthNode acts as a server wrapper and router for incoming AX.25 connections.


---

## 🔐 Auth System

The server leverages Chattervox for authenticated sessions, extending it with a custom module that verifies signed identities before allowing access to privileged services like game creation or message posting.

---

## 📦 Dependencies

- [Chattervox](https://github.com/danakj/chattervox) – Authenticated AX.25 messaging backend (MIT)
- [Direwolf](https://github.com/wb2osz/direwolf) – Software TNC & FX.25 framing
- Python 3.8+
- `ax25-tools` and `ax25-apps` (for kernel AX.25 interface)

---

## 🔧 Installation (WIP)

Coming soon. Setup scripts and configs will be provided to:

1. Configure Direwolf and AX.25
2. Launch AXAuthNode with service modules
3. Enable access via radio or SSH

---

## 📜 License

This project is licensed under the MIT License. See `LICENSE` for details.

Chattervox is © [@danakj](https://github.com/danakj) and used under the [MIT License](https://github.com/danakj/chattervox/blob/main/LICENSE).

---

## 📡 Connect

AXAuthNode is currently deployed on a Raspberry Pi node at **ZL2###-11**.  
Future deployments may support multiple RF regions and node linking.

---

## 🤝 Contributing

Pull requests are welcome! Please open an issue to discuss any large feature or protocol changes first.

---

## 💬 Future Modules

- `/mail` – Personal inbox + delivery over packet
- `/files` – Minimalist file transfer via AX.25
- `/weather` – APRS-style local weather integration

---

## 🛠 Maintainer

Developed by [ZL2DRS](https://github.com/MRPURPLENZ).  
Built for exploration, education, and extending the reach of ham radio.

