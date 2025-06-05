# Online-Sktorrent-Stremio-addon

Tento doplnok pre [Stremio](https://www.stremio.com/) umožňuje vyhľadávanie a prehrávanie **priamych online streamov (.mp4)** z portálu [online.sktorrent.eu](https://online.sktorrent.eu), vrátane:

- 🎬 Filmov
- 📺 Seriálov (s podporou epizód a sezón)
- 📡 Streamov v kvalite **720p / 480p / 360p**
- 🇨🇿🇸🇰🇬🇧 Jazykové vlajky podľa názvu streamu

---

## ⚙️ Lokálna inštalácia a spustenie

### 1. Klonovanie repozitára
```bash
git clone https://github.com/tvoj-username/stremio-sktorrent-addon.git
cd stremio-sktorrent-addon

### 2. Inicializácia
npm init -y
npm install axios cheerio stremio-addon-sdk axios-cookiejar-support tough-cookie bncode entities

### 3. Spustenie skriptu/doplnku v príkazovom riadku (v príkazovom riadku sa potom budú zobrazujú debug výpisy práce doplnku) 
node sktorrent-addon.js

### 4. Overenie spustenia 
Zadaj v prehliadači: http://127.0.0.1:7000/manifest.json

### 5. V aplikácii Stremio klikni na doplnky a potom na tlačidlo "Add addon" alebo jednoducho zadaj nasledovný odkaz do vyhľadávacieh poľa a nainštaluj doplnok:
http://127.0.0.1:7000/manifest.json
