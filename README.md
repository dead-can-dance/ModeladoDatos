# 📈 Modelado de Crecimiento Exponencial con EDOs: Caso Ethereum (ETH)

Este proyecto consiste en el análisis del comportamiento del precio de Ethereum (ETH) utilizando un modelo matemático basado en Ecuaciones Diferenciales Ordinarias (EDOs), específicamente para representar un crecimiento exponencial. Se modela el precio del activo como una función del tiempo y se ajusta a los datos históricos obtenidos mediante la API oficial de Binance.

## 📥 Obtención de datos

Los datos utilizados en este proyecto provienen de la API de Binance. Se recopila información diaria del par ETH/USDT en el rango comprendido entre el 1 de abril de 2021 y el 10 de mayo de 2021.

El archivo eth_plot_data.csv se genera automáticamente a partir de un script en Python que realiza la consulta y guarda los datos procesados

## 📐 Modelado con EDO
Se plantea una EDO del tipo:

dP/dt = kP

Donde:

P(t) es el precio de Ethereum en función del tiempo.

k es la tasa de crecimiento.

La solución general de esta EDO es:
P(t) = P₀ · e^(kt)

A partir de los datos extraídos, se linealiza el modelo aplicando logaritmo natural a los precios para obtener una relación lineal, de modo que se pueda estimar el parámetro k mediante regresión lineal simple.

## ⚙️ Proceso de ajuste
Se transforman los precios de cierre (Close) con logaritmo natural.

Se asocia cada precio con un valor de tiempo (t) a partir de la fecha.

Se aplica un modelo de regresión lineal para encontrar k y P₀.

Se utiliza la solución analítica de la EDO para generar la curva de predicción.

## 📊 Visualización de resultados
El gráfico resultante muestra:

Los precios reales de Ethereum en el rango de tiempo seleccionado.

La curva ajustada que representa el crecimiento exponencial estimado por el modelo.

Esto permite visualizar el grado de ajuste del modelo exponencial al comportamiento real del mercado en ese período específico.

### 📊 Dashboard en Google Sheets

Puedes ver el dashboard y cálculos del análisis con los datos del proyecto en el siguiente enlace:

👉 [Ver Dashboard en Google Sheets](https://docs.google.com/spreadsheets/d/1uqc-fxBi7dqWnMHfm4fMwAsJs82HoJJNM8NfZqDugfQ/edit?usp=sharing)


## 🧠 Conclusiones
Aunque el mercado de criptomonedas es inherentemente volátil y no sigue siempre una tendencia exponencial, este enfoque permite:

Explorar cómo ciertas tendencias a corto plazo pueden aproximarse con modelos matemáticos simples.

Tener una base conceptual para extender el análisis a modelos más complejos (por ejemplo, logísticos o basados en ecuaciones diferenciales no lineales).

Integrar técnicas matemáticas con programación y análisis de datos en un caso real del ámbito financiero.

