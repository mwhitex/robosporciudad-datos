# Criminalidad por municipio en España (Balance de Criminalidad 2026T2 + Padrón INE 2025)

Tabla abierta con las infracciones penales conocidas en **431 municipios de más de 20.000 habitantes y 52 provincias** de España, con tasas por 1.000 habitantes, variación interanual y ventana de 12 meses (julio 2025 – junio 2026). Es el mismo fichero que alimenta **[robosporciudad.com](https://robosporciudad.com)**, donde cada municipio tiene su ficha con evolución desde 2016, rankings y metodología.

- Fichas por municipio: https://robosporciudad.com/robos (p. ej. [Madrid](https://robosporciudad.com/robos/madrid/madrid), [Barcelona](https://robosporciudad.com/robos/barcelona/barcelona), [Sevilla](https://robosporciudad.com/robos/sevilla/sevilla))
- Rankings: [robos en viviendas](https://robosporciudad.com/robos/ranking/robos-en-viviendas) · [ciudades más seguras](https://robosporciudad.com/robos/ranking/ciudades-mas-seguras)
- Metodología: https://robosporciudad.com/metodologia · Fuentes y licencias: https://robosporciudad.com/fuentes
- Fichero vivo (siempre la última versión): https://robosporciudad.com/datos/espana.csv

## Fichero

`data/criminalidad-municipios-espana-2026T2.csv` — UTF-8, separador coma, punto decimal, 483 filas (52 provincias + 431 municipios), 143 columnas. Es una copia del CSV publicado en robosporciudad.com/datos sin las líneas de comentario iniciales (están en `data/CABECERA-ORIGINAL.txt`) y con las URL en formato absoluto.

| Columna | Significado |
|---|---|
| `nivel` | `provincia` o `municipio` |
| `codigo_ine`, `codigo_provincia` | Código INE |
| `nombre`, `provincia` | Nombre oficial |
| `poblacion`, `poblacion_anio` | Padrón municipal del INE a 1-1-2025 |
| `periodo` | `2026T2` = enero-junio 2026 |
| `url_ficha`, `url_csv` | Ficha del municipio en robosporciudad.com y su CSV histórico |
| `{tipologia}_casos` | Casos enero-junio 2026 |
| `{tipologia}_casos_anterior` | Casos enero-junio 2025 |
| `{tipologia}_var_pct` | Variación % entre ambos semestres |
| `{tipologia}_u12m`, `{tipologia}_u12m_anterior` | Casos julio 2025-junio 2026 y los 12 meses previos |
| `{tipologia}_tasa_1000` | Casos u12m por 1.000 habitantes |
| `{tipologia}_var_pct_u12m` | Variación % de la ventana de 12 meses |

Tipologías: `total`, `criminalidad_convencional`, `cibercriminalidad`, `robos_domicilios`, `robos_fuerza_total`, `hurtos`, `robos_violencia`, `sustraccion_vehiculos`, `estafas_informaticas`, `otros_ciberdelitos`, `trafico_drogas`, `lesiones_rina`, `libertad_sexual`, `agresion_sexual_penetracion`, `resto_libertad_sexual`, `homicidios_consumados`, `homicidios_tentativa`, `secuestro`, `resto_convencional`.

## Cómo leerlo (importante)
- Son **infracciones penales conocidas** por las fuerzas de seguridad, no condenas.
- Los datos de 2026 son **provisionales**; el Ministerio del Interior puede revisarlos.
- La tasa usa la población **empadronada**. En municipios turísticos o con mucha población flotante, la tasa sobreestima el riesgo para quien vive allí.
- Con menos de 20 casos, las variaciones porcentuales son poco estables: mejor la cifra absoluta.

## Fuentes y licencia
- Origen de los datos: Portal Estadístico de Criminalidad (Ministerio del Interior), Balance de Criminalidad enero-junio 2026, actualizado el 17/09/2026.
- Elaboración propia con datos extraídos del sitio web del INE: www.ine.es (Padrón a 1-1-2025).
- Este fichero derivado (tasas, variaciones, selección de columnas) se publica bajo **CC BY 4.0**. Atribución: **«robosporciudad.com con datos del Ministerio del Interior»**, con enlace a https://robosporciudad.com. Los ficheros de origen del Ministerio del Interior y del INE conservan sus propias condiciones.
- Proyecto independiente, sin relación con el Ministerio del Interior ni con el INE.

## Cómo citar
Mancera Villa, J. (2026). *Criminalidad por municipio en España, 2026T2* [Conjunto de datos]. robosporciudad.com. https://robosporciudad.com/datos

## Actualización
Trimestral, cuando Interior publica un nuevo Balance (el siguiente, 3T 2026, hacia mediados de diciembre de 2026).

---

**English summary.** Open table of police-recorded crime for 431 Spanish municipalities (>20,000 inhabitants) and 52 provinces, January–June 2026 vs 2025, plus a 12-month window and rates per 1,000 residents (INE 2025 census). Source: Spanish Ministry of the Interior (Balance de Criminalidad) and INE. Derived data under CC BY 4.0 — attribution: "robosporciudad.com con datos del Ministerio del Interior". Municipality pages: https://robosporciudad.com
