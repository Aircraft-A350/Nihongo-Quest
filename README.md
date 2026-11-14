# 🌸 NIHONGO QUEST (日本語クエスト)

> **Interaktivní aplikace v cyberpunkovém stylu pro výuku japonštiny**  
> Procvičujte Hiraganu, Katakanu a Kanji pomocí kvízů, animací tahů znaků a nativní audio výslovnosti.

![Licence](https://img.shields.io/badge/licence-MIT-pink.svg)
![Azure Storage](https://img.shields.io/badge/nasazení-Azure%20Storage-cyan.svg)
![Stav](https://img.shields.io/badge/stav-aktivní-brightgreen.svg)

---

## ⚡ Hlavní funkce

- **Databáze znaků (Database Mode)**:
  - Přehledná tabulka Gojūon pro Hiraganu i Katakanu s interaktivními detaily a animací tahů.
  - Kanji rozdělené do praktických tematických kategorií (Čísla, Čas a příroda, Lidé a tělo, Slovesa, Místa a věci).
- **Animace tahů a výslovnost (KanjiVG & TTS)**:
  - Vektorové vykreslování pořadí tahů znaků přímo z KanjiVG.
  - Hlasový syntetizér pro poslech správné japonské výslovnosti.
- **Tréninková aréna (Training Mode)**:
  - Rychlé procvičování čtení znaků v Romaji s okamžitou odezvou.
  - Combo multiplikátor bodů (1x, 2x, 5x XP bonus).
  - Denní Streak (počet dnů v řadě) a levelovací systém (od Novice po Master).
  - Cyberpunkové zvukové efekty syntetizované v reálném čase přes Tone.js.
  - Možnost filtrovat procvičované řady (A, K, S, T, N, H, M, Y, R, W, n).
- **Lokální i cloudové ukládání (Zero-friction)**:
  - Automatické ukládání postupu do paměti prohlížeče (LocalStorage).
  - Možnost exportu a importu kompletní zálohy postupu v JSON formátu bez nutnosti registrace.
  - Volitelná podpora Firebase Auth a synchronizace s Firestore.
- **Automatické nasazení (CI/CD)**:
  - GitHub Actions workflow nejprve ověří statické soubory a po úspěchu nahraje změny z větve `main` do Azure Storage Static Website.

---

## 🚀 Živá verze aplikace

Web běží na Azure Storage Static Website:

**https://nihongoquest1113220123.z1.web.core.windows.net/**

## ☁️ Nasazení na Azure

Aplikace je pouze statický HTML/JS web bez serveru nebo buildu. Azure Static Web Apps nebylo možné použít, protože podporované regiony služby nejsou dostupné v Azure for Students subscription; proto se používá Azure Storage Static Website jako nejjednodušší dostupná varianta. GitHub Actions zajišťuje nasazení bez ukládání tajných hodnot v repozitáři.

### Jednorázové nastavení v Azure

1. V Azure vytvořte **Storage account** typu `StorageV2`, SKU `Standard_LRS`, v regionu povoleném vaší subscription.
2. Zapněte **Static website**, nastavte `index.html` jako index document a `index.html` jako error document.
3. V **Access keys** zkopírujte jeden account key pouze do GitHubu a nikam jej necommitujte.
4. V GitHubu otevřete **Settings → Secrets and variables → Actions** a vytvořte secrets:
   - `AZURE_STORAGE_ACCOUNT_NAME` = název storage accountu.
   - `AZURE_STORAGE_ACCOUNT_KEY` = account key.
5. Po pushi do `main` workflow **CI/CD to Azure Storage Static Website** nejprve ověří soubory a následně nahraje web do `$web`. Pull requesty workflow nespouštějí deployment.

Veřejná adresa je v Azure u storage accountu v **Static website → Primary endpoint**. Tento hosting má náklady podle storage a operací; čerpá Azure for Students kredit.

---

## 🛠️ Spuštění na vlastním počítači

Stránka nevyžaduje žádné složité závislosti ani sestavování. Stačí otevřít soubor `index.html` v libovolném moderním webovém prohlížeči nebo spustit lokální HTTP server:

```bash
# Pomocí Python 3
python -m http.server 8000

# Nebo pomocí Node.js
npx serve .
```

A otevřít v prohlížeči adresu `http://localhost:8000`.

---

## 📜 Licence

MIT License. Volně k dispozici pro všechny studenty japonštiny.
