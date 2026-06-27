# KazuistiCard

Denná klinická hra pre **Mladí Lekári** — prečítaj si kazuistiku, napíš diagnózu a po každom nesprávnom pokuse sa odhalí nová indícia. Wordle-style klinické uvažovanie v slovenčine.

## Hra

- **Jedna kazuistika denne** — 30 prípadov, každý so 6 postupne odhaľovanými indíciami (max. 6 pokusov).
- **Autocomplete diagnóz** — napíš a vyber zo zoznamu slovenských patológií (diakritika sa ignoruje).
- **Archív** — klikni na minulý deň a vyrieš jeho prípad. Odpoveď uvidíš až keď ho dohráš.
- **Zdieľanie** — vygeneruje obrázok s výsledkom a výzvou (pre Instagram / WhatsApp).
- Tmavý režim, séria posledných 7 dní, žiadne externé knižnice — celé v jednom súbore.

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
| `logo.png.png` | Logo Mladí Lekári |
| `high_yield_diagnoses.json` | Zdrojový zoznam diagnóz (MKCH-10) pre tvorbu prípadov |

## Pridanie prípadov

Edituj pole `PUZZLES` v `index.html` — každý prípad je `{ answer, clues:[6], explain }`. `answer` musí presne zodpovedať položke v poli `DIAGNOSES`, inak ju nebude možné vybrať v našepkávači.

Kalendár začína `EPOCH = 1. jún 2026`; prípady sa priraďujú dňom sekvenčne.

---

mladilekari.sk
