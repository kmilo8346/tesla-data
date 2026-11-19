# Turquía (ODMD/OSD) — notas

Fuente: página 21 del informe mensual de OSD, "İthal Otomobil Satışları" (venta de **autos importados**).

## Julio 2025: PDF re-guardado

- OSD publicó julio 2025 con otro nombre (`Aylık Rapor_07.pdf`), no con el patrón habitual `07-2025-OSD_Aylik_Degerlendirme_Raporu.pdf`. Por eso el extractor no lo encuentra.
- El PDF original (impreso desde Chrome, "Skia/PDF m138") da error en `pdf2json` ("Invalid XRef stream").
- `_/osd/2025_7.pdf` es ese mismo PDF re-guardado con `pdftocairo -pdf`. El texto de la portada y de la página 21 es idéntico al original: "TEMMUZ 2025", "RAPORU 7 / 2025".
- MD5 del original descargado: `6ac23d1efc522c46c2e61ea9bf5e6a56`.

## Aston Martin en 2023-08 a 2024-01 (corregido)

- En esos PDFs el nombre viene partido ("Aston Mart" + "n"), y antes el extractor descartaba la fila porque no tenía 15 celdas.
- Se corrigió en el extractor: une los pedazos del nombre de la marca y normaliza "Aston Mart n" a "Aston Martin". Con eso se recuperaron 6 filas (2023-08: 1, 2023-09: 2, 2023-10: 1, 2023-11: 1, 2023-12: 2, 2024-01: 2).

## KG MOBILITY aparece dos veces en algunos meses

- En algunos meses (por ejemplo 2024-08 y 2026-05 a 2026-08) el PDF trae dos filas "KG MOBILITY". El valor del mes está en una de las dos filas y la otra trae "-".
- Por eso el CSV tiene dos filas con la misma clave: una con valor y otra vacía. Es tal cual la fuente.
