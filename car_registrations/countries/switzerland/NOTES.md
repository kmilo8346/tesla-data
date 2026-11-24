# Switzerland (auto-schweiz) – notes

## Source
`_/autoswiss/{year}_{month}.xlsx`: auto-schweiz yearly workbook `ModellePW{year}.xlsx`, one sheet per month (`Jan`, `Febr`, `Mrz`, …) with year-to-date registrations per model → `ytd_registrations_by_model.csv`.

The site only keeps the latest version of each yearly workbook, so files stored for older months are monthly snapshots and files stored after a year has closed are the final workbook. The month sheets do not change between versions.

## Corrections
- 2025-01: the stored file was the 2024 workbook (byte-identical to `2024_12.xlsx`), so the CSV had January 2024 data for January 2025 (e.g. Tesla Model Y 250 instead of 153). It was replaced by the 2025 workbook and the month regenerated. The extractor now only accepts the current-year workbook when its file name contains the requested year.

## Source quirks (kept as published)
- The last row of every sheet, `DIVERSE` (other models), is not stored.
- Some sheet titles have typos: `Januar - März` on the 2023-02 sheet and `Januar - Nobember` on the November sheets (2023, 2024, 2025). The data belongs to the sheet's month.
- In 12 cases (10 months) a model's year-to-date value is lower than in the previous month (up to 372 units), because auto-schweiz revises or reassigns models. No Tesla model is affected.
