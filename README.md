# Clima y Agua Panama (IG: pty_agua_clima)

## Tabla de Contenidos
* [Generales](#Generales)
* [Precipitación](#Precipitación)
* [Temperatura (Tmax y Tmin, 2m de altura)](#Temperatura-Tmax-y-Tmin-2m-de-altura)
* [Referencia y Datos Utilizada para la Generacion de Mapas](#Referencia-y-Datos-Utilizada-para-la-Generacion-de-Mapas)
  
## Generales
Esta iniciativa tiene como objetivo difundir información climatológica e hidrológica de Panamá con fines educativos y profesionales. Los datos presentados mediante mapas ofrecen una perspectiva del comportamiento temporal y espacial del país, a escala mensual, de variables como precipitación, temperatura del aire a 2 metros de altura y otras. La información utilizada es generada y administrada por el Climate Hazards Center del Departamento de Geografía de la Universidad de California en Santa Bárbara, EE. UU. Este proyecto es financiado en colaboración por FEWS NET (Red de Sistemas de Alerta Temprana contra la Hambruna), una iniciativa de la Agencia de los Estados Unidos para el Desarrollo Internacional (en inglés, USAID), y el Centro de Observación y Ciencia de los Recursos Terrestres del Servicio Geológico de los Estados Unidos (en inglés, USGS EROS). A continuación, se presenta una descripción de la información mensual incluida, como guía para su correcta interpretación:

## Precipitación
![Sum_Ppt_May_2025](https://github.com/jaime27ortega/Clima_Agua_Panama/blob/main/Precipitacion/2025/05_May/Sum_Ppt_May_2025.jpeg?raw=true)

La variable climática precipitación/lluvia (mm) es el resultado de la combinación de observaciones satelitales —específicamente, imágenes infrarrojas de duración de nubes frías (Cold Cloud Duration, en inglés CCD)— con datos provenientes de estaciones pluviométricas disponibles a nivel global (entre 60° N–60° S y 180° O–180° E). Esta información se integra en una grilla con una resolución espacial de 0.05° (5.55 km), y está disponible desde 1981 hasta la actualidad. Las estimaciones de precipitación terrestre se presentan en intervalos temporales de cinco días (pentadas) a una resolusion reducida de 0.01° (1.11 km, metodo de interpolacion: bilinear). Cada conjunto de datos se acompaña de mapas, gráficos y descripciones detalladas, organizados en un archivo PDF identificado como **"Report_Mes_Año"**, para facilitar su consulta y análisis. A continuación, se describen los componentes generados para la variable de precipitación (ver carpeta **"Precipitación"**):

- (a) Precipitación acumulada mensual del mes de análisis ($Ppt_{Mes}$, **"Sum_Ppt_Mes_Año"**): total de precipitación (mm) registrado en el mes de interés.
<p align="center">
$Ppt_{Mes} = \sum_{i=1}^{n} Ppt_{p_{i}}$
</p>

Donde: 

$Ppt_{p_{i}}$ es la precipitación registrada en la pentada $i$ del mes de interés, mm.

$n$ es la número de pentadas completas (usualmente 6 por mes).

- (b) Precipitación acumulada mensual de la normal climática ($Ppt_{NC (1991-2020)}$, **"Normal_Ppt_Mes_Año"**): total promedio de precipitación (mm) registrado en el período 1991–2020 para el mes de interés.
<p align="center">
$Ppt_{NC (1991-2020)} = \sum_{i=1}^{n} Ppt_{p_{i}}$
</p>

Donde: 

$Ppt_{p_{i}}$ es la precipitación promedio registrada en la pentada $i$ del mes de interés durante el período 1991–2020, mm.

$n$ es la número de pentadas completas (usualmente 6 por mes).

- (c) Diferencia de precipitación mensual ($Ppt_{Diff}$, **"Diff_Ppt_Mes_Año"**): diferencia de precipitación entre el acumulado mensual y la normal climática para el mes de interés.
<p align="center">
$Ppt_{Diff} = Ppt_{Mes}-Ppt_{NC (1991-2020)}$
</p>

Donde:

$Ppt_{Mes}$ es el total de precipitación (mm) registrado en el mes de interes, mm.

$Ppt_{NC (1991-2020)}$ es el total promedio de precipitación registrado en el período 1991–2020 para el mes de interés, mm.

- (d) Anomalía de precipitación mensual ($Ppt_{Anom}$, **"Anomalia_Mes"**): desviación promedio (positiva: por arriba – húmedo – de la NC; y negativa: por debajo – seco – de la NC) de la diferencia de precipitación ($Ppt_{Diff}$) en comparación con la normal climática (1991–2020).
<p align="center">
$Ppt_{Anom}$ = +/- $Ppt_{Diff_{Promedio}}$
</p>

Donde:

+/- $Ppt_{Diff_{Promedio}}$ es diferencia entre el acumulado mensual y la normal climática para el mes de interés, mm.

- (e) Resumen mensual por provincia y país (**"Ppt_Summary_A_B@C_D"**): A_B, precipitación por pentadas (acumulado de 5 días) en el país; total de precipitación acumulada en el país desde el primer mes del año (enero) hasta el mes de análisis. Adicionalmente, se presenta el total acumulado del año anterior y de la normal climática (NC: 1991–2020) para el mismo período analizado. C_D, total acumulado de precipitación por provincia desde el primer mes del año (enero) hasta el mes de análisis, y comparación del total acumulado de precipitación por provincia (mes de interés) vs la NC.

- (f) Ranking de precipitación, percentiles (**"Ppt_Rank_Mes_Año"**): comparación de períodos húmedos y secos con respecto al período histórico, en este caso 45 años (1981–2025), utilizando percentiles (método Weibull para clasificación de rankings). Clasificación o posiciones (rankings) de zonas/regiones basada en su posición por arriba (≥) o por debajo (≤) del % definido: más húmedo del registro (≥ 99%), $10^{th}$ más húmedo (≥ 90%), $20^{th}$  más húmedo (≥ 80%); normal, $35^{th}$  más húmedo (≥ 65%) y $35^{th}$ más seco (≤ 65%); $20^{th}$  más seco (≤ 80%), $10^{th}$  más seco (≤ 90%) y más seco del registro (≤ 99%).
<p align="center">
$P_{i} = \frac{m}{n+1}$
</p>

Donde:

$P_{i}$ es el percentil correspondiente al valor de precipitación mensual ${i}$.

$m$ es la posición (ranking) del valor ${i}$ al ordenar de mayor a menor precipitación.

$n$ Número total de años del período histórico ($n$ = 45).

## Temperatura (Tmax y Tmin, 2m de altura)
![Ave_AirTemp_Tprom_May_2025](https://github.com/jaime27ortega/Clima_Agua_Panama/blob/main/Temperatura/2025/05_May/Ave_AirTemp_Tprom_May_2025.jpeg?raw=true)

La variable climática temperatura (Tmax y Tmin, °C) es obtenida de la versión 5 (ERA5) del reanálisis atmosférico del Centro Europeo de Pronósticos Meteorológicos de Medio Plazo (ECMWF, por sus siglas en inglés), con una resolución original de 0.25° (27.8 km). Consecuentemente, la información es procesada y reducida por el Climate Hazards Center a una resolución de grilla de 0.05° (5.55 km). El área de cobertura de este producto oscila entre 60°S–70°N y está disponible desde 1981 hasta la actualidad. Las estimaciones de temperatura se presentan en intervalos temporales de 5 días (pentadas) a una resolusion reducida de 0.01° (1.11 km, metodo de interpolacion: bilinear). Cada conjunto de datos se acompaña de mapas, gráficos y descripciones detalladas, organizados en un archivo PDF identificado como **"Report_Mes_Año"**, para facilitar su consulta y análisis. A continuación, se describen los componentes generados para la variable de temperatura (ver carpeta **Temperatura**):

- (a) Temperatura promedio mensual (Tprom, Tmáx y Tmín) del mes de análisis ($T_{Mes}$, **"Ave_AirTemp_Tprom/Tmax/Tmin_Mes_Año"**): promedio de temperatura (°C) registrado en el mes de interés. Tmax y Tmin: promedio de temperaturas máximas y mínimas en intervalos temporales de 5 días. Tprom: temperatura promedio obtenida del promedio de Tmáx y Tmín (Tprom= (Tmax + Tmin) / 2).
<p align="center">
$Temp_{Mes} = \frac{1}{n} \sum_{i=1} Temp_{p_{i}}$
</p>

Donde: 

$Temp_{p_{i}}$ es la temperatura (Tprom, Tmáx y Tmín) registrada en la pentada $i$ del mes de interés, °C.

$n$ es el número de pentadas completas (usualmente 6 por mes).

- (b) Anomalía de temperatura mensual ($Temp_{Anom}$, **"Anomalia_Tprom/Tmax/Tmin_Mes"**): desviación promedio (positiva: por arriba — frío respecto a la NC, y negativa: por debajo — cálido respecto a la NC) de la diferencia de temperatura ($Ppt_{Diff}$) en comparación con la normal climática (1991–2020).
<p align="center">
$Temp_{Anom}$ = +/- $Temp_{Diff_{Promedio}}$
</p>

Donde:

+/- $Temp_{Diff_{Promedio}}$ es diferencia entre la temperatura (Tprom, Tmax, y Tmin) mensual y la normal climática para el mes de interes, °C.

- (c) Resumen mensual por provincia y país (**"AirTemp_Summary_A_B@C_D_Mes_Año"**): A_B, temperatura promedio por pentadas en el país (Tprom, Tmax y Tmin), línea negra representa el promedio móvil (3 pentadas). C_D, temperatura (Tprom) promedio mensual por provincia y temperatura promedio mensual vs. NC (normal climática: 1991–2020) para el mes analizado.

- (d) Ranking de temperaturas, percentiles (**"AirTemp_Tprom_Rank_Mes_Año"**): comparación de períodos fríos y cálidos con respecto al período histórico, en este caso 45 años (1981–2025), utilizando percentiles (método Weibull para clasificación de rankings). Clasificación o posiciones (rankings) de zonas/regiones basado en su posición por arriba (=>) o por debajo (<=) del % definido: más frío del registro (=> del 99%), $10^{th}$ más frío (=> del 90%), $20^{th}$ más frío (=> del 80%); normal, $35^{th}$ más frío (=> del 65%) y $35^{th}$ más cálido (<= del 65%); $20^{th}$ más cálido (<= del 80%), $10^{th}$ más cálido (<= del 90%) y más cálido del registro (<= del 99%).
<p align="center">
$Temp_{i} = \frac{m}{n+1}$
</p>

Donde:

$Temp_{i}$ es el percentil correspondiente al valor de temperatura (Tprom) promedio mensual ${i}$.

$m$ es la posición (ranking) del valor ${i}$ al ordenar de mayor a menor temperatura.

$n$ Número total de años del  período histórico ($n$ = 45).

- (e) Temperaturas promedio, variación temporal (**"Temp_Prom_Mes__Año"**): media móvil (n= 3) de las temperaturas pentadales promedio (Tprom, n= 6 por mes) en el año de análisis desde el primer mes del año (enero) hasta el mes de análisis. Adicionalmente, se presentan los promedios de 1981–2010, 1991–2020, 2023 y 2024.

## Referencia y Datos Utilizada para la Generacion de Mapas
- Funk, C., Peterson, P., Landsfeld, M. et al. The climate hazards infrared precipitation with stations—a new environmental record for monitoring extremes. Sci Data 2, 150066 (2015). https://doi.org/10.1038/sdata.2015.66
- Verdin, A., Funk, C., Peterson, P. et al. Development and validation of the CHIRTS-daily quasi-global high-resolution daily temperature data set. Sci Data 7, 303 (2020). https://doi.org/10.1038/s41597-020-00643-7
- Precipitacion (CHIRPS 3.0): https://data.chc.ucsb.edu/products/CHIRPS/v3.0/pentads/latam/tifs/
- Temperatura (CHIRTS-ERA5):
  - Tmax-https: https://data.chc.ucsb.edu/experimental/CHIRTS-ERA5/tmax/tifs/pentads/
  - Tmin-https: https://data.chc.ucsb.edu/experimental/CHIRTS-ERA5/tmin/tifs/pentads/

 
