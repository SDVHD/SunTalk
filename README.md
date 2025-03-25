# [WIP] SunTalk - Dein modernes Intercom-System 🎙️☀️

SunTalk ist ein leistungsfähiges, UDP-basiertes Intercom-System, das eine schnelle und zuverlässige Kommunikation ermöglicht. Es nutzt **Opus** für hochwertige Audioübertragung und bietet eine moderne Web- und Electron-Oberfläche.

## 🚀 Features

- **Echtzeitkommunikation** über UDP
- **Opus Audio-Codec** für hohe Sprachqualität
- **Hybrid-Architektur**: Server-basiertes Routing & P2P
- **Datenbank:** MongoDB für Nutzer- und Channel-Management
- **Plattformübergreifend**: Webclient & Electron-App

## 📂 Projektstruktur

```
SunTalk/
├── backend/        # Node.js-Server (Express, UDP, WebSockets)
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   ├── config/
│   │   ├── utils/
│   │   ├── server.js
│   │   ├── udpServer.js
│   │   ├── wsServer.js
│   ├── .env
│   ├── package.json
│
├── frontend/       # Web- und Electron-Client
│   ├── src/
│   ├── electron/
│   ├── public/
│   ├── package.json
│
├── docs/           # Dokumentation
├── README.md       # Dieses Dokument
└── .gitignore
```

## 🔧 Installation & Setup

### Backend einrichten

```sh
cd backend
npm install
npm start
```

### Frontend starten

```sh
cd frontend
npm install
npm run dev
```

## 📡 Technologie-Stack

- **Backend**: Node.js, Express, UDP, WebSockets
- **Audio**: Opus (via @discordjs/opus oder opusscript)
- **Datenbank**: MongoDB
- **Frontend**: Vue.js, Electron, Tailwind CSS, DaisyUI, Lucide

## 🛠️ API-Endpunkte (WIP)

| Methode | Endpoint        | Beschreibung          |
| ------- | --------------- | --------------------- |
| `GET`   | `/api/channels` | Alle Kanäle abrufen   |
| `POST`  | `/api/channel`  | Neuen Kanal erstellen |
| `POST`  | `/api/talk`     | Sprachpaket senden    |

## 📜 Lizenz

Dieses Projekt steht unter der **MIT-Lizenz**.

---

🌞 **SunTalk – Weil Kommunikation strahlen sollte!**

