# Online-Sktorrent-Stremio-addon

Tento doplnok pre [Stremio](https://www.stremio.com/) umožňuje vyhľadávanie a prehrávanie **priamych online streamov (.mp4)** z portálu [online.sktorrent.eu](https://online.sktorrent.eu), vrátane:

- 🎬 Filmov
- 📺 Seriálov (s podporou epizód a sezón)
- 📡 Streamov v kvalite **🟦 HD (720p) / 🟨 SD (480p) /  🟥 LD (360p)**
- 🇨🇿 🇸🇰 🇬🇧 ... Jazykové vlajky podľa názvu streamu (Jazykové značky (vlajky) sú automaticky rozpoznávané z názvu streamu (napr. 🇨🇿, 🇸🇰, 🇬🇧, atď.))

  Note: Use [Node.js](https://nodejs.org/en/blog/release/v20.9.0) v 20.09 LTS for testing.
---

## 🧪 Lokálna inštalácia a spustenie

### 1. Klonovanie repozitára
```bash
git clone https://github.com/tvoj-username/stremio-sktorrent-addon.git
cd stremio-sktorrent-addon
```

### 2. Inicializácia
```bash
npm init -y
npm install axios cheerio stremio-addon-sdk axios-cookiejar-support tough-cookie bncode entities
```

### 3. Spustenie skriptu/doplnku v príkazovom riadku (v príkazovom riadku sa potom zobrazujú debug výpisy) 
```bash
node sktorrent-addon.js
```

### 4. Overenie spustenia 
Zadaj v prehliadači: http://127.0.0.1:7000/manifest.json

### 5. Inštalácia doplnku v aplikácii Stremio 
V aplikácii Stremio klikni na "Addons" a potom na tlačidlo "Add addon" alebo jednoducho zadaj nasledovný odkaz do vyhľadávacieh poľa a nainštaluj doplnok:
http://127.0.0.1:7000/manifest.json

## 🔍 Vlastnosti doplnku
- Vyhľadávanie na základe IMDb ID (podpora epizód ako tt1234567:1:2).
- Pokročilá fallback logika pri vyhľadávaní (skrátené názvy, rôzne formáty S01E01, 1x1).
- Automatická extrakcia jazykových vlajok zo streamu.
- Viacero pokusov pri vyhľadávaní na základe originálneho aj lokalizovaného názvu.
- Optimalizovaný výstup pre Stremio rozhranie (názov, jazyk, kvalita, zdroj).
- Podpora len priameho streamovania .mp4 z [online.sktorrent.eu](https://online.sktorrent.eu).

## 📜 Právne upozornenie
Tento addon je určený len na osobné experimentálne účely. Neobsahuje žiadny vlastný multimediálny obsah – slúži výhradne ako index pre verejne dostupné videá z domény [online.sktorrent.eu](https://online.sktorrent.eu).

Používateľ nesie plnú zodpovednosť za akékoľvek použitie. Vývojár nenesie žiadnu zodpovednosť za používanie doplnku, porušenie autorských práv alebo streamovanie chráneného obsahu. Streamovanie akéhokoľvek obsahu je na vlastné riziko.

Ak stránka zmení HTML štruktúru alebo obmedzí prístup, addon môže prestať fungovať.

## 🛠 Licencia

MIT License (voľné použitie, bez záruky)

## 👨‍💻 Autor

Tento addon bol vyvinutý ako komunitný projekt s cieľom poskytnúť streamingový rozšíriteľný doplnok pre platformu Stremio, využívajúci verejne dostupné odkazy z [online.sktorrent.eu](https://online.sktorrent.eu).

Tento doplnok je experimentálny projekt na osobné účely.

Ak máš návrhy na vylepšenie alebo chceš prispieť – neváhaj a pošli pull request.

Ukážka z lokálneho testovania doplnku:
<img title="Addon Usage Sample" alt="Example of Addon Usage" src="/sample.png">

🛠️ Krok za krokom: Deploy na Render (online testovanie)

    - Vytvor nový GitHub repozitár s týmito súbormi (alebo vytvor fork projektu na svojom GitHub učte)
    - Prejdi na: https://render.com/ a zaregistruj sa / prihlás.
    - Klikni na "New +" → "Web Service".
    - Vyber možnosť "Deploy from a Git repository" a prepoj svoj GitHub účet.
    - Vyber svoj repozitár (napr. Online-Sktorrent-Stremio-addon).
    - Vyplň nastavenia:
        Name: napr. Online-Sktorrent-Stremio-addon
        Environment: Node
        Build Command:	 npm install
        Start Command:   node Online-sktorrent-addon.js
        Region: podľa tvojho výberu
        Instance Type: Free (ak ti postačuje)
    - Klikni "Create Web Service".

🌐 Po deploy

Po deployi ti Render vygeneruje URL napr.:

https://sktorrent-addon.onrender.com/manifest.json

Túto adresu môžeš použiť v Stremio na inštaláciu doplnku a jeho testovanie.


