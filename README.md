# Gimme

Moderná webová aplikácia na generovanie platobných QR kódov (PayBySquare), vytváranie platobných odkazov a odosielanie žiadostí o platbu.

![PWA Ready](https://img.shields.io/badge/PWA-pripravené-green)
![Vue.js](https://img.shields.io/badge/Vue.js-3-4FC08D?logo=vue.js)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-06B6D4?logo=tailwindcss)

---

## ✨ Funkcie

### 💳 Generovanie platobných QR kódov
- QR kód obsahuje **Payme odkaz** – po naskenovaní sa otvorí Banková applikácia
- Funguje s akýmkoľvek QR skenerom alebo fotoaparátom
- Skenovateľné QR kódy priamo z obrazovky telefónu alebo počítača
- Automatické rozpoznávanie banky podľa IBAN (Tatra banka, Slovenská sporiteľňa, VÚB, ČSOB, mBank, atď.)

### 📱 Viacero bankových účtov
- Pridajte a spravujte viacero bankových účtov/profilov
- Jednoduché prepínanie medzi účtami potiahnutím (swipe carousel)
- Označte účty vlastnými farbami a ikonami pre ľahšiu identifikáciu
- Nastavte predvolený účet (hviezdička)
- Kategórie účtov: Osobný, Firemný, Úspory, Projekt, Rodina, Dar

### 🤖 AI skenovanie účteniek
- Odfotografujte faktúru alebo účtenku
- AI automaticky extrahuje platobné údaje (suma, variabilný symbol, IBAN, správa)
- Poháňané **Google Gemini AI**
- Vyžaduje bezplatný Gemini API kľúč (dostupný na [Google AI Studio](https://aistudio.google.com/app/apikey))

### 📋 Platobné šablóny
- Uložte si často používané platby ako šablóny
- Rýchly prístup k opakujúcim sa platbám (nájom, predplatné, atď.)
- Vyhľadávanie a filtrovanie šablón
- Úprava a mazanie existujúcich šablón

### 📊 História platieb s analytikou
- Sledujte všetky vygenerované žiadosti o platbu
- **Analytika**: celkový počet platieb, celková suma, priemerná suma
- Rozdelenie podľa kategórií s vizuálnym grafom
- Filtrovanie podľa obdobia (dnes, týždeň, mesiac, rok alebo vlastné)
- Označenie platby ako zaplatenej / čakajúcej
- Duplikovanie predchádzajúcich platieb jedným kliknutím

### 🔐 Nostr integrácia
- Odosielanie žiadostí o platbu priamo cez protokol Nostr
- Správa vašej Nostr identity (NPUB/NSEC kľúče)
- **Zdieľanie Nostr ID** – vygeneruje odkaz s vaším NPUB, ktorý môžete poslať ostatným (napr. `?nostr_id=npub1...`)
- **Adresár kontaktov** – uloženie a správa Nostr kontaktov
- **Rozdelenie účtu** – odoslanie žiadosti viacerým kontaktom naraz (split bill)
- Prijímanie žiadostí o platbu od iných používateľov
- Keď niekto otvorí váš zdieľaný odkaz, automaticky sa mu ponúkne pridať vás do adresára

### 🧮 Vstavaná kalkulačka
- Vypočítajte sumy priamo v aplikácii
- Integrovaná do poľa pre sumu
- Podpora základných operácií (+, -, ×, ÷)
- Nie je potrebné prepínať medzi aplikáciami

### 🎨 Prispôsobenie
- Podpora svetlej a tmavej témy
- **6 farebných schém**: Indigo, Rose, Emerald, Amber, Sky, Violet
- Automatická detekcia systémovej témy
- Responzívny dizajn optimalizovaný pre mobily

### 📖 Interaktívny tutoriál
- Krok za krokom sprievodca aplikáciou
- Možnosť spustiť kedykoľvek z nastavení

---

## 🚀 Ako používať

### Prvé kroky
1. **Pridajte svoj bankový účet** – Kliknite na tlačidlo "+" a zadajte IBAN a údaje účtu
2. Vyberte kategóriu a farbu karty
3. Aplikácia automaticky rozpozná vašu banku

### Vytvorenie žiadosti o platbu
1. **Vyberte si účet** potiahnutím doľava/doprava na kartách účtov
2. **Zadajte sumu**, ktorú chcete vyžiadať (môžete použiť kalkulačku)
3. **Pridajte voliteľné údaje:**
   - Variabilný symbol (VS) – na identifikáciu platby
   - Dátum splatnosti – kedy má byť platba vykonaná
   - Správa – poznámka pre platiteľa
4. **Kliknite na "Vyžiadať platbu"**
5. **Zdieľajte QR kód** – ukážte ho na obrazovke, skopírujte platobný odkaz alebo odošlite cez Nostr

### Používanie AI skenovania účteniek
1. Kliknite na **ikonu fotoaparátu** 📷 vedľa hlavného tlačidla
2. **Vyberte fotografiu** faktúry alebo účtenky
3. AI automaticky vyplní platobné údaje
4. Skontrolujte a vygenerujte QR kód

> **Poznámka:** Najprv je potrebné pridať Gemini API kľúč v Nastaveniach. Získajte ho zadarmo na [Google AI Studio](https://aistudio.google.com/app/apikey).

### Ukladanie šablón
1. Po vyplnení platobných údajov prejdite do **Šablón** (📋 ikona)
2. Kliknite na **"Pridať"** pre uloženie aktuálnej platby ako šablóny
3. Pomenujte ju a uložte
4. Používajte šablóny pre opakujúce sa platby

### Odosielanie cez Nostr
1. Vygenerujte žiadosť o platbu
2. Kliknite na tlačidlo **"Vyžiadať"** v zobrazení QR kódu
3. Vyberte kontakt(y) z adresára alebo vyhľadajte podľa mena
4. Pre rozdelenie účtu vyberte viacero kontaktov
5. Kliknite na **"Odoslať"** (alebo "Odoslať všetkým")

---

## ⚙️ Nastavenia

Prístup k nastaveniam cez **ikonu ozubeného kolieska** (⚙️) v ľavom hornom rohu:

| Nastavenie | Popis |
|------------|-------|
| **Téma** | Svetlá, Tmavá alebo Automatická (podľa systému) |
| **Farba zvýraznenia** | Vyberte si preferovanú farebnú schému (6 možností) |
| **Nostr identita** | Zobrazenie/správa NPUB kľúča, import NSEC |
| **Adresár** | Správa Nostr kontaktov |
| **Gemini API kľúč** | Pridanie API kľúča pre AI funkcie |
| **Tutoriál** | Spustenie sprievodcu znova |

---

## 🛠️ Technológie

Táto aplikácia je postavená ako **single-file aplikácia** (všetko v jednom HTML súbore) a používa:

| Technológia | Účel |
|-------------|------|
| **Vue.js 3** | Reaktívny UI framework (Composition API) |
| **Tailwind CSS** | Utility-first CSS framework |
| **QRCode.js** | Generovanie QR kódov |
| **Nostr Tools** | Decentralizovaný protokol na zasielanie správ |
| **Google Gemini AI** | OCR a extrakcia údajov z účteniek/faktúr |
| **IndexedDB** | Lokálne uloženie dát v prehliadači |

### Externé závislosti (CDN)
- `https://cdn.tailwindcss.com` – Tailwind CSS
- `https://unpkg.com/vue@3` – Vue.js 3
- `https://cdnjs.cloudflare.com/ajax/libs/qrcodejs` – QRCode.js
- `https://esm.sh/nostr-tools@1.17.0` – Nostr Tools

---

## 🔒 Súkromie a bezpečnosť

- ✅ **Všetky dáta sú uložené lokálne** na vašom zariadení pomocou IndexedDB
- ✅ Údaje o vašom bankovom účte **nikdy neopustia váš prehliadač**
- ✅ Nostr kľúče sú bezpečne uložené vo vašom prehliadači
- ⚠️ Pri použití AI skenovania sa obrázok odošle do Google Gemini API

---

## 📞 Čo je Nostr?

**Nostr** (Notes and Other Stuff Transmitted by Relays) je otvorený, decentralizovaný protokol na komunikáciu.

### Ako Nostr funguje

- **Decentralizácia** – Správy sa prenášajú cez sieť nezávislých serverov nazývaných "relays"
- **Kryptografická identita** – Každý používateľ má unikátny pár kľúčov:
  - **NPUB** (verejný kľúč) – Vaša verejná adresa, ktorú môžete zdieľať s ostatnými
  - **NSEC** (súkromný kľúč) – Váš tajný kľúč na podpisovanie správ. **Nikdy ho nezdieľajte!**

### Prečo Nostr v tejto aplikácii?

Nostr umožňuje **odosielať žiadosti o platbu priamo** príjemcovi bez potreby e-mailu, SMS alebo iných centralizovaných služieb:

| Výhoda | Popis |
|--------|-------|
| **Súkromie** | Komunikácia prebieha priamo, bez prostredníkov |
| **Spoľahlivosť** | Správy sa ukladajú na viacerých relays |
| **Jednoduchosť** | Stačí poznať NPUB príjemcu (kontakt) |
| **Bez registrácie** | Nepotrebujete vytvárať účty na žiadnych službách |

---
