# Datos crudos

Esta carpeta guarda los archivos oficiales **tal como se descargaron**. Nunca se modifican: toda transformación ocurre en los notebooks. Por su tamaño no se suben al repositorio (ver `.gitignore`).

| Carpeta | Archivo | Fuente y cómo descargarlo |
|---|---|---|
| `esi/` | `esi_2022.csv`, `esi_2023.csv`, `esi_2024.csv`, `esi_2025.csv` | INE → [Encuesta Suplementaria de Ingresos](https://www.ine.gob.cl/estadisticas-por-tema/mercado-laboral/encuesta-suplementaria-de-ingresos) → pestaña *Bases de datos* → CSV → base *Personas* de cada año |
| `ipc/` | `ipc_general_empalmado_2022_2025.xlsx` | [Banco Central, BDE](https://si3.bcentral.cl/siete) → Precios → IPC General → *Índice empalmado* · 2022–2025 · mensual · serie original · Excel vertical |
| `ipc/` | `ipc_divisiones_2023_2025.xlsx` | BDE → Precios → IPC - Aperturas → Índices 2023 → *Divisiones* · 2023–2025 · mensual · Excel vertical |
| `ipc/` | `ipc_ponderadores_divisiones_2023.xlsx` | BDE → Precios → IPC - Aperturas → Ponderadores 2023 → *Divisiones* · Excel vertical |
| `casen/` | `casen_2024spss.zip` | [BIDAT, CASEN 2024](https://bidat.gob.cl/directorio/Encuestas%20Observatorio%20Social/casen-2024) → base de datos en formato SPSS |

Los nombres deben quedar exactamente como en la tabla, porque el notebook los busca así.
