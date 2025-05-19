# Clima y Agua Panama (IG: pty_agua_clima)

## Generales
Es una iniciativa destinada a difundir información climatológica e hidrlogica de Panamá con fines educativos y profesionales. La informacion presentada a traves de mapas brinda una perspectiva del comportamiento temporal y espacial de Panama a una escala mensual de variables como precipitacion y temperatura del aire (2 m). La informacion utilizada es administrada y generada por el Climate Hazards Center, Department of Geography, University of California Santa Barbara. Este proyecto es financiado en colaboracion por las agencias La Red de Sistemas de Alerta Temprana sobre Hambrunas (en ingles FEWS NET) de la Agencia de los Estados Unidos para el Desarrollo Internacional (USAID) y el Centro de Observación y Ciencia de los Recursos Terrestres del Servicio Geológico de los Estados Unidos (en ingles USGS EROS). A continuacion se detalla una descripcion de la informacion mensual presentada como guia para su interpretacion:

## Precipitacion 
La variable climatica precipitacion/lluvia (mm) es producto de la combinacion de informacion satelital (Observaciones infrarrojas de duración de nubes frías, en ingles CCD) y estaciones pluviometricas disponibles atraves del globo (60°N-60°S, 180°W-180°E) con una resolucion final de 0.05 grados, que abarca desde 1981 hasta la actualidad. La estimacion de precipitacion terrestres están disponibles en intervalos que van desde cada cinco días (pentadas). Cada mapa y grafico con sus respectivos valores y descripcion es presentado en un PDF ("Report_Mes_Año") para un uso mas accesible. Acontinuacion se detalla cada componente generado para la precipitacion:

- (a) Precipitation acumnulada mensual del mes de analisis ("Sum_Ppt_Mes_Año"): total de precipitation registrado en el mes de interes, 
- (b) Precipitation acumnulada mensual de la normal climatica (NC, "Normal_Ppt_Mes_Año"): total de precipitation registrado en el periodo 1990-2020 para el mes de interes.
- (c) Diferencia de precipitation mensual ("Diff_Ppt_Mes_Año"): diferencia entre el acumulado mensual y la normal climatica para el mes de interes.
- (d) Anomalia de precipitacion mensual ("Anomalia_Mes"): desviacion (positiva: por arriba-humedo de la NC y negativa: por debajo-seco de la NC) de la diferencia de precipitation en comparacion con la normal climatica (1991-2020).
- (e) Resumen mensual por provincia y pais ("Ppt_Summary_A_B@C_D"): A_B, precipitacion por pentadas (acumulados de5 dias) en el pais y C_D, total de precipitacion acumulada desde el primer mes del año (Enero) hasta el mes de analisis. Adicionalmente, se presenta         el total acumulado del año anterior y de la normal climatica (NC: 1991-2020) para el mismo periodo analisado.
- (f) Ranking de precipitacion, percentiles ("Ppt_Rank_Mes_Año"): comparacion de periodos humedos y secos con rescepto al periodo historico, en este caso 45 años (1981-2025), utilizando percetiles (metodo Weibull para clasificacion de rankings). Clasificacion o          pocisiones (rankings) de zonas/regiones basado en sus posicion por arriba (=>)/debajo (<=) del % definido: mas humedo del registro (=> del 99%), 10th mas humedo (=> del 90%), 20th mas humedo (=> del 80%); normal, 35th mas humedo (=> del 65%) y 35th mas seco        (<= del 65%); 20th mas seco (<= del 80%), 10th mas seco (<= del 90%), y mas seco del registro (<= del 99%).


## Referencia y Datos Utilizada para la Generacion de Mapas
- Funk, C., Peterson, P., Landsfeld, M. et al. The climate hazards infrared precipitation with stations—a new environmental record for monitoring extremes. Sci Data 2, 150066 (2015). https://doi.org/10.1038/sdata.2015.66
- Precipitacion (CHIRPS 3.0): https://data.chc.ucsb.edu/products/CHIRPS/v3.0/pentads/latam/tifs/
- Temperatura (CHIRTS-ERA5):
  - Tmax-https://data.chc.ucsb.edu/experimental/CHIRTS-ERA5/tmax/tifs/pentads/
  - Tmin-https://data.chc.ucsb.edu/experimental/CHIRTS-ERA5/tmin/tifs/pentads/
  



