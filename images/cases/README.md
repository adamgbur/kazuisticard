# Obrázky ku kazuistikám — návod

Táto zložka je určená pre obrázky (CT, RTG, USG, EKG, klinické foto...),
ktoré sa pripoja ako doplnková indícia ku konkrétnej kazuistike.

## Krok za krokom

1. **Nájdi obrázok** podľa tabuľky v `task-list.md` (presne, ktorý nález má obrázok ukazovať).
   Zdroje: Openi (openi.nlm.nih.gov), Wikimedia Commons (commons.wikimedia.org, kategória Medical),
   Radiopaedia.org (over si licenciu pri konkrétnom prípade), DermNet NZ (over aktuálnu licenciu).
2. **Stiahni obrázok** a ulož ho do tejto zložky (`images/cases/`) s presným názvom podľa vzoru nižšie.
3. **Vyplň jeden riadok** v `credits.csv` (otvor v Exceli / Numbers / Google Sheets) — meno súboru,
   popis, zdroj, autor, licencia. Bez tohto riadku obrázok nepôjde nasadiť (chýbala by licencia/zdroj).
4. Keď máš hotovo pár aj všetkých 30, pošli mi vedieť — nahrám všetko naraz do hry.

## Ako pomenovať súbor

```
{dvojčíslie prípadu}-{modalita}.{jpg|png}
```

Príklady: `01-ct.jpg`, `02-ekg.jpg`, `06-usg.jpg`, `28-foto.jpg`, `22-rtg.jpg`

Skratky modality, ktoré používame: `ct`, `mri`, `rtg`, `usg`, `angio`, `ekg`, `foto` (klinická fotografia),
`histo` (histopatológia/mikroskopia), `krv` (nátier/laboratórny obrázok).

Číslo prípadu (01–30) nájdeš v prvom stĺpci `task-list.md` a `credits.csv`.

## Čo napísať do credits.csv (stĺpce)

| stĺpec | čo tam patrí | príklad |
|---|---|---|
| `case_no` | číslo prípadu (01–30), už predvyplnené | `01` |
| `filename` | presný názov súboru, ktorý si sem uložil | `01-ct.jpg` |
| `caption_sk` | krátky slovenský popis toho, čo obrázok ukazuje (bude vidieť pod obrázkom v hre) | `CT mozgu: hyperdenzita v bazálnych cisternách` |
| `source_url` | odkaz na stránku, odkiaľ obrázok pochádza (nie priamo na súbor obrázka, ale na stránku prípadu/článku) | `https://commons.wikimedia.org/wiki/File:...` |
| `author` | meno autora / inštitúcie tak, ako je uvedené pri obrázku | `Case courtesy of Dr. X, Radiopaedia.org` |
| `license` | skratka licencie | `CC BY-SA 4.0` / `Public domain` / `CC0` |
| `license_url` | odkaz priamo na text licencie | `https://creativecommons.org/licenses/by-sa/4.0/` |

**Dôležité:** ak si pri obrázku nie si istý/á nálezom (napr. že CT naozaj ukazuje presne to, čo je
v indícii — napr. že ide o INFERIORNÝ, nie predný infarkt), radšej ho nepoužívaj alebo do `caption_sk`
napíš poznámku a označ to — pri diagnostických obrázkoch pre medikov/lekárov nesmie byť žiadna chyba.

## AMBOSS odkazy

Samostatný súbor `amboss-links.csv` v koreňovom priečinku repozitára. 12 z 30 riadkov je už
overených a vyplnených (stĺpec `overene` = `ano`). Pre zvyšné:

1. Prihlás sa do AMBOSS.
2. Do vyhľadávania hore zadaj anglický názov z stĺpca `hladaj_na_amboss_en` (AMBOSS Knowledge
   Library je anglická/nemecká, nie slovenská).
3. Otvor hlavný "Knowledge" článok k danej diagnóze (nie prípadovú štúdiu ani vedľajší článok).
4. Skopíruj presnú URL z adresového riadku prehliadača a vlož ju do stĺpca `amboss_url`.
5. Zmeň `overene` na `ano`.

Neodhaduj/nekonštruuj URL sám — rôzne diagnózy majú rôzne neobvyklé tvary adresy
(napr. nie vždy presný preklad názvu), over si to vždy priamym vyhľadaním a otvorením článku.
