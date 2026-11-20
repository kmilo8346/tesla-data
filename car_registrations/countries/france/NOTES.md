# France (PFA) – notes

## Sources
- `_/pfa_brand/*.pdf`: "Flash Marché" PDF, brand table on page 2 → `registrations_by_brand.csv`.
- `_/pfa/*.pdf`: "Dossier de presse" PDF, "Top 100 VP France" (year to date) on page 18 → `top_100_ytd_registrations_by_model.csv`.

## Known issue: missing AUTRES row in 2024-07 to 2024-10
The brand extractor looks for a final row named `AUSTRES` (typo of `AUTRES`), never finds it, and
drops the last parsed row instead. Usually that row is a footer, so `AUTRES` (other brands) is kept.
In 2024-07, 2024-08, 2024-09 and 2024-10 there is no footer row, so `AUTRES` was dropped:

| Month | AUTRES in PDF |
|---|---|
| 2024-07 | 2 458 (1,95%) |
| 2024-08 | 1 772 (2,06%) |
| 2024-09 | 3 688 (2,65%) |
| 2024-10 | 3 455 (2,55%) |

Tesla and the other brands are not affected. Left as is for now.

## Market share values
`market_share` is stored as published by PFA. It can differ by up to ~0,03 points from
`registrations / TOTAL MARCHE`, because of PFA's own rounding.
