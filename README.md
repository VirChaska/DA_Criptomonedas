# <h1 align=center> **Análisis de Datos del Mercado de Criptomonedas** </h1>

<p align='center'>
<img src = 'https://www.clarin.com/img/2023/06/14/WJlAYJhAg_360x240__1.jpg' height = 200>
<p>

## Descripción del Proyecto

En este proyecto, asumiré el rol de un Analista de Datos en una empresa de servicios financieros. Mi tarea consiste en realizar un análisis del mercado de criptomonedas utilizando datos obtenidos de la **API CoinGecko**. El objetivo es comprender mejor el comportamiento y la evolución de las criptomonedas y proporcionar hallazgos y recomendaciones.

## Recopilación de Datos

Utilizando la **API CoinGecko**, he obtenido datos actualizados de las 10 criptomonedas con mayor capitalización de mercado. Estos datos incluyen precios históricos, volúmenes de operaciones y capitalización del mercado.
También definí una función para obtener la *capitalización promedio* en el último año y efectivamente, las 10 criptomonedas con mayor capitalización del momento son las que se posicionaron entre los primeros puestos. <br>
**Ver mayor detalle en el archivo [Extracción_datos.ipynb](Extracción_datos.ipynb)**

**Criptomonedas con mayor capitalización promedio en el último año**

| Criptomonedas      | capitalización promedio (último año)  |
|--------------------|--------------------------|
| Bitcoin            | $453,558,268,323.96      |
| Ethereum           | $194,300,817,706.21      |
| Tether             | $73,857,212,643.01       |
| BNB                | $45,312,730,681.65       |
| USD Coin           | $38,673,175,065.93       |
| XRP                | $23,055,538,738.20       |
| Cardano            | $12,529,877,370.28       |
| Dogecoin           | $10,546,479,713.51       |
| Lido Staked Ether  | $9,293,168,051.20        |
| Solana             | $8,544,441,159.90        |

## Análisis Exploratorio de Datos

He realizado un análisis exploratorio de los datos para comprender mejor las tendencias generales del mercado. Esto incluye visualizaciones de precios a lo largo del tiempo, correlaciones, etc. <br>
No hay valores nulos, porque los datos extraídos son desde el 22 de diciembre del 2020, recién desde esa fecha, Staked Ether registra precios en la API. Si hubiese tomado la fecha de lanzamiento de **Bitcoin** (2009), hubiesen habido muchos valores nulos para las otras criptomonedas. Esta fue la razón por la que opté tomar los registros ya desde el 22 de diciembre del 2020. <br>
**Ver mayor detalle en el archivo [EDA.ipynb](EDA.ipynb)**

**Antes de profundizar en el análisis, es importante saber qué es una stablecoin**
### ¿Qué es una stablecoin?
Son activos digitales que son diseñados para mantener estable su valor en relación con algún activo externo, como una moneda fiduciaria como el dólar estadounidense por ejemplo. El objetivo principal de las stablecoins es mitigar la volatilidad inherente de muchas otras criptomonedas, como Bitcoin y Ethereum, y proporcionar a los usuarios una alternativa más predecible y confiable para almacenar valor y realizar transacciones.

### Tendencias de Precios

Tras analizar los datos, se observa que las criptomonedas seleccionadas han experimentado fluctuaciones significativas en sus precios en los últimos años. Algo que llama la atención es que durante el 2022, en promedio, las 10 criptomonedas tuvieron una tendencia bajista. En el 2023, están teniendo una tendencia alcista, pero muy poca en comparación con años anteriores.

![precios](/Imágenes/precio_2022.png)

Es interesante notar que dentro de las 10 criptomonedas, las dos stablecoins presentaron un comportamiento distinto (**Tether** y **USD Coin**). Estas stablecoins se mantuvieron relativamente constantes en su valor (1 USD) a lo largo del período estudiado. Esto se debe a su naturaleza como activos diseñados para mantener un valor estable, respaldado generalmente por monedas fiduciarias.

![precios](/Imágenes/precios.png)

**Finalmente elaboré un dashboard interactivo para tener un análisis aún más detallado de cada criptomoneda en el periodo de tiempo seleccionado y también elaboré 3 KPIs que están relacionados con la volatilidad, dominancia del mercado y la relación existente entre el volumen y la circulación, esto con el objetivo de recomendar la mejor oportunidad de inversión.**

## Tecnologías y Herramientas Utilizadas

- Python
- Jupyter Notebook
- Power BI
- API CoinGecko

