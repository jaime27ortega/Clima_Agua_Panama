# Clima y Agua Panama (IG: pty_agua_clima)

## Generales
Esta iniciativa tiene como objetivo difundir información climatológica e hidrológica de Panamá con fines educativos y profesionales. Los datos presentados mediante mapas ofrecen una perspectiva del comportamiento temporal y espacial del país, a escala mensual, de variables como precipitación, temperatura del aire a 2 metros de altura y otros. La información utilizada es generada y administrada por el Climate Hazards Center del Departamento de Geografía de la Universidad de California en Santa Barbara, US. Este proyecto es financiado en colaboración por FEWS NET (la Red de Sistemas de Alerta Temprana contra la Hambruna), una iniciativa de la Agencia de los Estados Unidos para el Desarrollo Internacional (en ingles USAID), y el Centro de Observación y Ciencia de los Recursos Terrestres del Servicio Geológico de los Estados Unidos (en ingles USGS EROS). A continuación, se presenta una descripción de la información mensual incluida, como guía para su correcta interpretación:

## Precipitacion
![Sum_Ppt_Apr_2025](https://github.com/user-attachments/assets/30989a4f-55a0-4441-9910-1f7f780ace8c)
La variable climática precipitación/lluvia (mm) es el resultado de la combinación de observaciones satelitales, específicamente imágenes infrarrojas de duración de nubes frías (Cold Cloud Duration, en ingles CCD)— con datos provenientes de estaciones pluviométricas disponibles a nivel global (entre 60°N–60°S y 180°W–180°E). Esta información se integra en una grilla con una resolución espacial de 0.05° (5.55 km), y está disponible desde 1981 hasta la actualidad. Las estimaciones de precipitación terrestre se presentan en intervalos temporales cada 5 dias (pentadas). Cada conjunto de datos se acompaña con mapas, gráficos y descripciones detalladas, organizados en un archivo PDF identificado como **"Report_Mes_Año"**, para facilitar su consulta y análisis. A continuación, se describen los componentes generados para la variable de precipitación (ver carpeta **Precipitation_2025**):

- (a) Precipitacion acumnulada mensual del mes de analisis ($Ppt_{Mes}$, **"Sum_Ppt_Mes_Año"**): total de precipitacion (mm) registrado en el mes de interes.
<p align="center">
$Ppt_{Mes} = \sum_{i=1}^{n} Ppt_{p_{i}}$
</p>

Donde: 

$Ppt_{p_{i}}$ es la precipitacion registrada en la pentada $i$ del mes de interes, mm.

$n$ es la número de pentadas completas (usualmente 6 por mes).

- (b) Precipitacion acumnulada mensual de la normal climatica ($Ppt_{NC (1991-2020)}$, **"Normal_Ppt_Mes_Año"**): total promedio de precipitacion (mm) registrado en el periodo 1991-2020 para el mes de interes.
<p align="center">
$Ppt_{NC (1991-2020)} = \sum_{i=1}^{n} Ppt_{p_{i}}$
</p>

Donde: 

$Ppt_{p_{i}}$ es la precipitacion promedio registrada en la pentada $i$ del mes de interes durante el periodo 1991-2020, mm.

$n$ es la número de pentadas completas (usualmente 6 por mes).

- (c) Diferencia de precipitacion mensual ($Ppt_{Diff}$, **"Diff_Ppt_Mes_Año"**): diferencia de precipitacion entre el acumulado mensual y la normal climatica para el mes de interes.
<p align="center">
$Ppt_{Diff} = Ppt_{Mes}-Ppt_{NC (1991-2020)}$
</p>

Donde:

$Ppt_{Mes}$ es el total de precipitacion (mm) registrado en el mes de interes, mm.

$Ppt_{NC (1991-2020)}$ es el total promedio de precipitacion registrado en el periodo 1991-2020 para el mes de interes, mm.

- (d) Anomalia de precipitacion mensual (Ppt_{Anom}, **"Anomalia_Mes"**): desviacion promedio (positiva: por arriba-humedo de la NC y negativa: por debajo-seco de la NC) de la diferencia de precipitacion $(Ppt_{Diff})$ en comparacion con la normal climatica (1991-2020).
<p align="center">
$Ppt_{Anom}$ = +/- $Ppt_{Diff_{Promedio}}$
</p>

Donde:

+/- $Ppt_{Diff_{Promedio}}$ es diferencia entre el acumulado mensual y la normal climatica para el mes de interes, mm.

- (e) Resumen mensual por provincia y pais (**"Ppt_Summary_A_B@C_D"**): A_B, precipitacion por pentadas (acumulado de 5 dias) en el pais y C_D, total de precipitacion acumulado desde el primer mes del año (Enero) hasta el mes de analisis. Adicionalmente, se presenta el total acumulado del año anterior y de la normal climatica (NC: 1991-2020) para el mismo periodo analizado.

- (f) Ranking de precipitacion, percentiles (**"Ppt_Rank_Mes_Año"**): comparacion de periodos humedos y secos con rescepto al periodo historico, en este caso 45 años (1981-2025), utilizando percetiles (metodo Weibull para clasificacion de rankings). Clasificacion o pocisiones (rankings) de zonas/regiones basado en sus posicion por arriba (=>) o por debajo (<=) del % definido: mas humedo del registro (=> del 99%), 10th mas humedo (=> del 90%), 20th mas humedo (=> del 80%); normal, 35th mas humedo (=> del 65%) y 35th mas seco (<= del 65%); 20th mas seco (<= del 80%), 10th mas seco (<= del 90%), y mas seco del registro (<= del 99%).

<p align="center">
$P_{i} = \frac{m}{n+1}$
</p>

Donde:

$P_{i}$ es el percentil correspondiente al valor de precipitación mensual ${i}$.

$m$ es la posición (ranking) del valor ${i}$ al ordenar de mayor a menor precipitación.

$n$ Número total de años del periodo histórico ($n$ = 45).

## Temperatura (Tmax y Tmin, 2m de altura)
![Ave_AirTemp_Tmean_Apr_2025](https://github.com/user-attachments/assets/25df4bc1-d1ef-49ec-9339-5f2b41b94888)
La variable climática temperatura (Tmax y Tmin, °C) es obtenida de la versión 5 (ERA5) del reanálisis atmosferico del Centro Europeo de Pronósticos Meteorológicos de Medio Plazo (ECMWF, por sus siglas en inglés), con una resolucion de orignal de 0.25° (27.8 km). Consequentemente, la informacion es procesada y reducida por el Climate Hazards Center a una resolucion de grilla de 0.05° (5.55 km). El area de cobertura de este producto oscilla entre 60°S–70°N y está disponible desde 1981 hasta la actualidad. Las estimaciones de temperatura se presentan en intervalos temporales cada 5 dias (pentadas). Cada conjunto de datos se acompaña con mapas, gráficos y descripciones detalladas, organizados en un archivo PDF identificado como **"Report_Mes_Año"**, para facilitar su consulta y análisis. A continuación, se describen los componentes generados para la variable de temperatura (ver carpeta **Temperatura_2025**):

- (a) Temperatura promedio mensual (Tprom, Tmax, y Tmin) del mes de analisis ($Temp_{Mes}_{Tprom, Tmax, y Tmin}$, **"Ave_AirTemp_Tmean/Tmax/Tmin_Mes_Año"**): promedio de temperartura (°C) registrado en el mes de interes. Tmax y Tmin: prommedio de maximas y minimas temperaturas en intervalos temporales cada 5 dias. Tprom: temperatura promedio obtenida del promedio de Tmax y Tmin (Tmean = Tmax+Tmin/2)
<p align="center">
$Ppt_{Mes} = \sum_{i=1}^{n} Ppt_{p_{i}}$
</p>

Donde: 

$Ppt_{p_{i}}$ es la precipitacion registrada en la pentada $i$ del mes de interes, mm.

$n$ es la número de pentadas completas (usualmente 6 por mes).

## Referencia y Datos Utilizada para la Generacion de Mapas
- Funk, C., Peterson, P., Landsfeld, M. et al. The climate hazards infrared precipitation with stations—a new environmental record for monitoring extremes. Sci Data 2, 150066 (2015). https://doi.org/10.1038/sdata.2015.66
- Precipitacion (CHIRPS 3.0): https://data.chc.ucsb.edu/products/CHIRPS/v3.0/pentads/latam/tifs/
- Temperatura (CHIRTS-ERA5):
  - Tmax-https: https://data.chc.ucsb.edu/experimental/CHIRTS-ERA5/tmax/tifs/pentads/
  - Tmin-https: https://data.chc.ucsb.edu/experimental/CHIRTS-ERA5/tmin/tifs/pentads/

 
