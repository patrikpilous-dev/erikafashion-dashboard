# Erika Fashion – Dashboard objednávek & počasí

Statický dashboard s analýzou objednávek e-shopu [erikafashion.cz](https://erikafashion.cz)
za klouzavý rok, vč. korelace s počasím (Open-Meteo, Praha).

**Live:** https://patrikpilous-dev.github.io/erikafashion-dashboard/

## Co dashboard obsahuje

- KPI souhrn (objednávky, obrat, košík, vrátky)
- Měsíční trend obratu + denní rolling 7d
- Den v týdnu × sezóna (heatmapa)
- Teplotní pásma (5 °C / 2 °C / 5denní predikce) s top5 produkty
- Heatmapy den v týdnu × teplota (objednávky / index / obrat)
- Státní svátky vs průměr daného dne v týdnu × sezóna
- B2B vs B2C přehled
- TOP 30 produktů, TOP 20 měst

## Anonymizace (GDPR)

Zdrojová data byla před analýzou anonymizována:
- Dropnuto: jméno, e-mail, telefon, ulice, číslo popisné, IP, IČO, DIČ, package number, remarks
- Ponecháno: město (jen pro top měst), prvních 3 znaky PSČ, B2B flag z přítomnosti firmy

## Zdroje dat

- **Objednávky:** Shoptet export (klouzavý rok, ~100 537 objednávek)
- **Počasí:** [Open-Meteo Archive API](https://open-meteo.com/) — Praha (50.0755, 14.4378)

## Lokální preview

```bash
python -m http.server 8765
# otevřít http://localhost:8765/
```
