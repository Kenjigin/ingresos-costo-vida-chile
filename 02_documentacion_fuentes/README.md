# Documentación de las fuentes

Libros de códigos y manuales oficiales usados para interpretar las variables. Se descargan junto con cada base de datos.

| Documento | Dónde obtenerlo |
|---|---|
| Manual y guía de variables, base personas ESI 2022, 2023 y 2024 | [INE, ESI](https://www.ine.gob.cl/estadisticas-por-tema/mercado-laboral/encuesta-suplementaria-de-ingresos) → *Bases de datos* / *Metadatos* |
| Manual de usuario de base de datos ESI 2025 | Ídem |
| Libro de códigos CASEN 2024 | [BIDAT, CASEN 2024](https://bidat.gob.cl/directorio/Encuestas%20Observatorio%20Social/casen-2024) |

## Variables clave

**ESI**

| Variable | Descripción |
|---|---|
| `ing_t_p` | Ingreso líquido de la ocupación principal |
| `fact_cal_esi` | Factor de expansión |
| `ocup_ref` | Ocupado con al menos 1 mes en el empleo (filtro oficial = 1) |
| `region` | Región (1–16) |
| `sexo` | 1 Hombre, 2 Mujer |
| `edad`, `tramo_edad` | Edad y tramo quinquenal |
| `cine11_1d` | Nivel educacional (CINE 2011 agregado) |
| `r_p_rev4cl_caenes` | Rama de actividad económica (21 ramas, 999 sin clasificación) |
| `categoria_ocupacion` | Categoría en la ocupación (CISE 93) |
| `ocup_form` | 1 Formal, 2 Informal |

**CASEN 2024**

| Variable | Descripción |
|---|---|
| `folio` | Identificador del hogar |
| `region` | Región (1–16) |
| `ten_viv` | Tenencia de la vivienda (2 = arrendada) |
| `v18` | Monto que paga el hogar de arriendo (`-88` = No sabe) |
| `v19` | Arriendo del sector para viviendas similares |
| `expr` | Factor de expansión regional |
