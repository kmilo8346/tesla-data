# Noruega (OFV) — notas

## Dos fuentes

| Fuente | Archivos | Meses | Qué trae |
|---|---|---|---|
| `ofv` (dashboard Power BI) | `top_20_registrations_by_brand.csv`, `top_20_registrations_by_model.csv` | 2023-01 a 2026-08 | Top 20 ordenado por **acumulado del año** (cifra del mes y share) |
| `ofv_api` (snapshots mensuales de ofv.no) | `top_30_registrations_by_brand.csv`, `top_30_registrations_by_model.csv` | desde 2026-07 | Top 30 ordenado por **ventas del mes** (cifra del mes y share con 2 decimales) |

- OFV dejó de actualizar el dashboard de Power BI en agosto 2026. El extractor `ofv` quedó deshabilitado.
- Los snapshots de `ofv_api` empiezan en julio 2026; no hay historia anterior.
- Julio y agosto 2026 están en las dos fuentes.

## Diferencias entre fuentes (jul y ago 2026)

Las cifras coinciden en todas las marcas y modelos comunes, salvo:

| Mes | Nombre | `ofv` | `ofv_api` |
|---|---|---|---|
| 2026-07 | Volvo | 726 | 727 |
| 2026-07 | Lexus | 73 | 72 |
| 2026-08 | Lexus | 77 | 78 |

(Lexus no entra al top 20 de `ofv`, solo aparece en el top 30 del dashboard.)

## Tesla puede faltar en `ofv_api`

`ofv_api` solo trae el top 30 del mes. En julio 2026 Tesla registró 24 autos y no aparece en `ofv_api` (ni la marca ni sus modelos). En `ofv` sí aparece porque el ranking es por acumulado del año.

## Revisiones posteriores en Power BI (no corregidas)

Al re-descargar meses antiguos (2024-06 a 2025-04) el 2026-11-20, Power BI muestra algunas cifras revisadas. Se mantienen las cifras guardadas originalmente:

| Mes | Modelo | CSV | Power BI hoy |
|---|---|---|---|
| 2024-12 | Hyundai IONIQ 5 | 155 | 159 |
| 2025-01 | Hyundai IONIQ 5 | 122 | 123 |

## Empates en el puesto 20

En 2026-01 el top 20 de modelos tiene 21 filas: Citroën E-C3 y Ford Explorer EV empatan en el puesto 20 (27 autos). Pasó también en 2023-01 con marcas.
