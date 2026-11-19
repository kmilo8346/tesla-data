# Japón (JAIA) — notas

## Solo se guarda la columna "普通" (pendiente de decidir si corregir)

`registrations_by_brand.csv` toma de la hoja 3 (`生産拠点別`) del Excel de JAIA solo la columna **"普通"** (autos de tamaño normal), no la columna **"合計"** (total).

Japón clasifica los autos por tamaño:

- **普通**: más de 4,7 m de largo, más de 1,7 m de ancho o motor de más de 2.000 cc. Son casi todos los importados, incluidos los Tesla.
- **小型**: autos compactos (Fiat 500, ABARTH, algunos Renault, etc.).
- **合計** = 普通 + 小型.

Por eso, en las marcas de autos compactos el CSV queda muy por debajo del total real de la marca:

| Mes | Marca | CSV (普通) | 小型 | 合計 |
|---|---|---|---|---|
| 2023-01 | FIAT | 22 | 305 | 327 |
| 2023-01 | RENAULT | 454 | 154 | 608 |
| 2023-01 | ABARTH | 0 | 70 | 70 |
| 2023-01 | Subtotal (小計) | 14.927 | 549 | 15.476 |
| 2026-10 | Subtotal (小計) | 17.541 | 72 | 17.613 |

## Tesla

JAIA no publica Tesla como marca. El generador `tesla_monthly_registrations` usa la fila `OTHERS` como estimación de Tesla. En `OTHERS` la diferencia entre 普通 y 合計 es de 0 a 9 autos por mes (por ejemplo, 2026-10: 2.162 vs 2.163; 2026-06: 3.997 vs 4.003).

## Cómo corregir algún día

En `apps/extractor/src/extractors/car_registrations/japan/jaia/Extractor.ts`, leer la columna `D` (合計) en vez de `B` y correr `reindex()`. Todos los Excel fuente están en `_/jaia/`.
