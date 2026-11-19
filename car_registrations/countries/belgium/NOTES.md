# Bélgica (FEBIAC) — notas

## Revisiones posteriores de FEBIAC (pendiente de decidir si corregir)

`registrations_by_brand.csv` guarda las cifras **tal como FEBIAC las publicó** en el PDF de cada mes (`_/febiac/YYYY_M.pdf`).

FEBIAC a veces corrige sus cifras después de publicarlas, pero **no actualiza los PDFs antiguos**: al re-descargar dic-2023 a oct-2025 (validado el 2026-11-19), todos los PDFs eran idénticos byte a byte a los guardados. La cifra corregida solo aparece en la columna del año anterior del PDF del mismo mes del año siguiente (por ejemplo, el PDF de abril 2026 trae abril 2025 revisado).

Por ahora se decidió **mantener las cifras publicadas originalmente**. Si algún día se quiere corregir, la fuente es esa columna del año anterior.

Diferencias encontradas (columna del año anterior del PDF del año siguiente vs CSV):

| Mes | Marca | CSV (publicado) | Revisado | Tipo |
|---|---|---|---|---|
| 2023-05 | AUDI | 2634 | 2635 | ajuste |
| 2023-09, 2023-10, 2023-11 | CHERY → OMODA | 1, 3, 1 | 1, 3, 1 | renombre |
| 2024-01 | CHEVROLET | 1 | — | eliminado |
| 2024-01, 2024-03, 2024-06, 2024-08 | CHERY → OMODA | 1 | 1 | renombre |
| 2024-02 | DREAMER | 1 | — | eliminado |
| 2024-03 | KG_MOBILITY | 15 | 20 | ajuste |
| 2024-03 | SSANGYONG | 103 | 98 | ajuste (probable traspaso a KG_MOBILITY) |
| 2024-11 | DONGFENG | — | 1 | agregado |
| 2024-12 | CUPRA | 137 | 136 | ajuste |
| 2024-12 | SEAT | 146 | 147 | ajuste |
| 2025-01 | DONG_FENG → DONGFENG | 10 | 10 | renombre |
| 2025-04 | UNKNOWN | 22 | — | eliminado |
| 2025-04 | BMW | 3779 | 3801 | ajuste (+22, probable reasignación de UNKNOWN) |
| 2025-07 | DR | 5 | 4 | ajuste |
| 2025-07 | EVO | — | 1 | agregado |
| 2025-10 | VOLKSWAGEN | 2874 | 2873 | ajuste |

- TESLA no tuvo ninguna revisión en los meses comparados (2023-01 a 2025-10).
- Meses desde 2025-11 en adelante aún no se pueden comparar (falta el PDF del año siguiente).
- No se pueden re-descargar del sitio: 2023-01 a 2023-10, 2023-11, 2024-01 y 2024-03; solo existen en este repo.
