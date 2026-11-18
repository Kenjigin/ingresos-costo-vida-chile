# Sueldos vs. Costo de Vida en Chile

Análisis de minería de datos sobre la relación entre los ingresos laborales y el costo de vida en Chile (2022–2025): diferencias territoriales, de género, educacionales y sectoriales, y sus posibles causas.

- **Metodología:** CRISP-DM
- **Modelo de datos:** dimensional de Kimball, esquema de constelación (cubo OLAP tabular)
- **Herramientas:** Python (Google Colab) · Power BI · SQL Server + SSAS (fase 2)
- **Gestión:** Jira (espacio ICH) · commits con la clave de la tarea (`ICH-xx`)

> 🚧 Proyecto en desarrollo.

## Preguntas de valor

1. ¿Creció más el sueldo o el costo de vida entre 2022 y 2025?
2. ¿En qué regiones rinde más el sueldo considerando el costo de la vivienda?
3. ¿Cuál es la brecha salarial de género y cómo varía por educación, edad y sector?
4. ¿Cuánto aumenta el ingreso con cada nivel educacional?
5. ¿Qué componentes del gasto explican el alza del costo de vida?
6. ¿Qué factores explican mejor las diferencias de ingreso?

## Estructura del repositorio

Basada en [Cookiecutter Data Science](https://cookiecutter-data-science.drivendata.org/), ordenada según el flujo de los datos.

```
├── 01_datos_crudos/            ← datos oficiales originales (NO se suben, ver instrucciones)
├── 02_documentacion_fuentes/   ← enlaces a libros de códigos y metodologías
├── 03_datos_procesados/        ← salidas del notebook (no se suben)
├── 04_notebooks/               ← análisis en Google Colab
├── 05_sql/                     ← scripts del data warehouse (fase 2)
├── 06_powerbi/                 ← dashboard
└── 07_informe/                 ← guías, informe, presentación y figuras
```

## Fuentes de datos

| Fuente | Organismo | Período | Uso |
|---|---|---|---|
| Encuesta Suplementaria de Ingresos (ESI), base personas | INE | 2022–2025 | Ingresos laborales |
| IPC general, serie empalmada (base 2023=100) | INE vía Banco Central | 2022–2025 mensual | Ingreso real |
| IPC por división y ponderadores (base 2023=100) | INE vía Banco Central | 2023–2025 mensual | Costo de vida por tipo de gasto |
| CASEN 2024 | Ministerio de Desarrollo Social y Familia | 2024 | Arriendo por región |

Los datos crudos no se incluyen por su tamaño (~400 MB). Ver [`01_datos_crudos/README.md`](01_datos_crudos/README.md) para descargarlos.

## Cómo reproducir

1. Descargar los datos según [`01_datos_crudos/README.md`](01_datos_crudos/README.md).
2. Copiar el proyecto a Google Drive en `MyDrive/Proyecto_Ingresos_Chile/`.
3. Abrir el notebook de `04_notebooks/` en Google Colab y ejecutarlo en orden.

## Validación

Las cifras se validan contra las publicadas por el INE (ocupados `ocup_ref = 1`, ponderado por `fact_cal_esi`):

| Año | Mediana calculada | Media calculada | INE |
|---|---|---|---|
| 2023 | $582.559 | $826.535 | Coincide |
| 2024 | $611.000 | $897.019 | Mediana oficial $611.162 |
| 2025 | $680.000 | $962.945 | Coincide |

## Limitaciones

- Chile no publica IPC regional: el costo de vida regional se aproxima con el arriendo mediano de la CASEN 2024.
- La ESI mide el ingreso personal líquido del trabajo; la CASEN, el arriendo pagado por el hogar.
- El IPC por división solo es comparable desde 2023 (cambio de canasta a base 2023=100).

## Autor

Claudio Galiano
