# 🌸 NIHONGO QUEST (日本語クエスト)

> **Interaktivní aplikace v cyberpunkovém stylu pro výuku japonštiny**  
> Procvičujte Hiraganu, Katakanu a Kanji pomocí kvízů, animací tahů znaků a nativní audio výslovnosti.

![Licence](https://img.shields.io/badge/licence-MIT-pink.svg)
![GitHub Pages](https://img.shields.io/badge/nasazení-GitHub%20Pages-cyan.svg)
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
  - Nastavený GitHub Actions workflow, který při každém pushi na větev `main` automaticky sestaví a nasadí nejnovější verzi na GitHub Pages.

---

## 🚀 Živá verze aplikace

Po aktivaci GitHub Pages bude aplikace dostupná na adrese:  
`https://Aircraft-A350.github.io/Nihongo-Quest/`

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
