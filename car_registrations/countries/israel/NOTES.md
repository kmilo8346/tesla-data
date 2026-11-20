# Israel (car-importers.org.il) – notes

## Source
`_/car_importers_evs/*.pdf`: "Electrified Vehicles" PDF, registrations by brand **year to date** → `ytd_registrations_by_brand.csv`.

## Files not downloaded by the extractor
The page only lists the months of the current year. When the year changes, the previous year's months disappear and only an annual PDF remains on "previous years".
- `YYYY_12.pdf`: the extractor downloads the annual "Electrified Vehicles YYYY" PDF and checks it ends on 31/12/YYYY. It is the same file as December (2024: byte-identical to `2024_12.pdf`).
- `2025_4.pdf` to `2025_11.pdf` were downloaded manually: the links were taken from the archive.org copy of the page from 2025-12-06, and the files still exist on the official server. January to March 2025 downloaded this way are byte-identical to the stored files.

## Table format change in 2026
- Up to 2025: `Electric | Hybrid | Plug In | Diesel Plug In | Total`.
- From 2026: `Electric_2026 | Hybrid_2026 | Plug-In_2026 | Total_2026` plus the same columns for the previous year. `Diesel Plug In` no longer exists; those vehicles are now included in `Plug-In`.
- The CSV stores `ytd_diesel_plugin_registrations = 0` from 2026 on; `ytd_plugin_registrations` includes diesel plug-ins.
- Check: the previous-year columns of the 2026 PDFs match the 2025 monthly PDFs (2025 `Plug In + Diesel Plug In` = 2026 `Plug-In_2025`). Exceptions: OMODA and JAECOO are merged as `Omoda_Jaecoo`, and HYUNDAI hybrids for 2025-03 are 8 702 instead of 8 662 (later revision).
