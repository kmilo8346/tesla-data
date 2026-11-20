# Netherlands (BOVAG) – notes

## Source
`_/bovag/*.pdf`: RAI/BOVAG "Verkopen Personenauto's" PDF, rows per model followed by the brand total → `registrations_by_model.csv` (models and brand totals, as printed).

## Source quirks (kept as published)
- `OVERIGE MERKEN` is printed twice at the end of every PDF, so it appears twice per month in the CSV.
- Model names may use abbreviations for the brand: `VW …` under `VOLKSWAGEN`, `MB …` under `MERCEDES`, `SSANGYONG …` under `SSANGYONG/KGM`.
- In 15 older months (2023-01 → 2024-05) some brand totals printed in the PDF differ by 1–5 units from the sum of their models (e.g. TOYOTA 2023-11: 1 855 vs 1 851). From 2024-06 on, every brand total and the `TOTAAL Markt` match.
