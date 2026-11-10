# KazuistiCard

Denná klinická hra od **Mladí lekári** — prečítaj si kazuistiku, napíš diagnózu a po každom nesprávnom pokuse sa odhalí nová indícia. Wordle-style klinické uvažovanie v slovenčine.

## Hra

- **Jedna kazuistika denne** — 31 prípadov, každý so 6 postupne odhaľovanými indíciami (max. 6 pokusov).
- **Autocomplete diagnóz** — napíš a vyber zo zoznamu slovenských patológií (diakritika sa ignoruje).
- **Archív** — klikni na minulý deň a vyrieš jeho prípad. Odpoveď uvidíš až keď ho dohráš.
- **Zdieľanie** — vygeneruje obrázok s výsledkom a výzvou (pre Instagram / WhatsApp).
- Séria posledných 7 dní, SK/EN, žiadne externé knižnice — celé v jednom súbore.

## Spustenie

Otvor `index.html` v prehliadači (dvojklik), alebo lokálny server:

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

> Pozn.: pri otvorení cez `file://` všetko funguje, lebo dáta sú inline.

## Štruktúra

| Súbor | Obsah |
|-------|-------|
| `index.html` | Celá hra (HTML + CSS + JS, `PUZZLES` a `DIAGNOSES` polia) |
| `logo2.png.png` | Logo Mladí lekári (horizontálne, RGB) |
| `logo.png.png` | Symbol loga — favicon |
| `amboss-wordmark.png` | Logo AMBOSS (partnerská karta, pätička) |
| `high_yield_diagnoses.json` | Zdrojový zoznam diagnóz (MKCH-10) pre tvorbu prípadov |

## Pridanie prípadov

Edituj pole `PUZZLES` v `index.html` — každý prípad je `{ answer, clues:[6], explain }`. `answer` musí presne zodpovedať položke v poli `DIAGNOSES`, inak ju nebude možné vybrať v našepkávači.

Kalendár začína `EPOCH = 1. júl 2026`; prípady sa priraďujú dňom sekvenčne.

## Dizajn

Vizuál sa drží brand manuálu Mladí lekári — tokeny sú v `:root` na začiatku `index.html`:

- **Farby** presne podľa manuálu, bez zmeny sýtosti či priehľadnosti: bordová `#C60253`, zelená `#5AE4A8`, ružová `#ff4d7f`, svetlozelená `#A1F4C8`, čierna `#1C1C1C`, biela.
- **Písmo** iba Lexend. **Logo** len oficiálne horizontálne, v pôvodných farbách na bielej.
- **Vlnky** vychádzajú z okraja v rohu; v hre sa zobrazia len na širokých obrazovkách, kde je pre ne miesto.
- **AMBOSS** je zámerne malý: partnerská karta pod výsledkom, riadok v pätičke a pásik na obrázku na zdieľanie. Tyrkysová AMBOSS sa inde nepoužíva.

---

mladilekari.sk
