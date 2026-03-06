# **Convolución, correlación y transformada de Fourier**

## *Contexto teorico* 
 La correlación y la convolución son operaciones básicas que realizamos para extraer información de señales o secuencias discretas e imágenes. Si bien estas operaciones son, en cierto sentido, unas de las más sencillas, son también extremadamente útiles. Además, al ser simples, se pueden analizar y comprender fácilmente, además de ser fáciles de implementar y calcular con gran eficiencia. La convolución se utiliza para filtrar linealmente una señal; por ejemplo, para suavizar un tren de picos y estimar la probabilidad de disparo. La correlación, por su parte, se utiliza para caracterizar las dependencias estadísticas entre dos señales. 

## *Objetivos* 
***Objetivo General:*** Reconocer la importancia de la aplicación de herramientasmatemáticas como la convolución y correlación en el área de procesamiento de señales. 

***Objetivos especificos:***
1. Comprender la convolución como una operación que permite obtener la respuesta de un sistema discreto ante una entrada determinada.
2. Analizar la correlación como medida de similitud entre dos señales.
3. Aplicar la Transformada de Fourier como herramienta de análisis en el
dominio de la frecuencia.

## *Desarrollo de la practica* 
El laboratorio se dividió en tres partes principales.

### ***Parte A – Convolución***

1. Se definieron dos señales discretas a partir de los dígitos del código estudiantil y el documento de identidad.

Para cada estudiante:  h[n] = dígitos del código - x[n] = dígitos de la cédula

2. Se calculó la convolución discreta usando la definición matemática: y[n] = Σ x[k] h[n - k]

3. Se implementó el cálculo mediante Python para verificar los resultados obtenidos manualmente.

#### ***- Estudiante 1***

Código: 5600905 - Cédula: 1014990049

h[n] = {5,6,0,0,9,0,5} - x[n] = {1,0,1,4,9,9,0,0,4,9}

*Resultado de la convolución:* y[n] = {5, 6, 5, 26, 78, 99, 68, 36, 106, 170, 99, 45, 36, 81, 20, 45}

#### Señal 𝑦[𝑛] resultante de la convolución usando sumatorias (a mano):

<p align="center">
<img src="PARTE A/Calculo manual est 1.jpg" width="600">
</p>
<p align="center">
<em>Imagen 1. Calculo manual convolución estudiante 1.</em>
</p>

#### Representación gráfica y secuencial (a mano):

<p align="center">
<img src="PARTE A/Grafica h(n) est 1.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 1. Representación grafica h(n) estudiante 1.</em>
</p>
<p align="center">
<img src="PARTE A/Grafica x(n) est 1.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 2. Representación grafica x(n) estudiante 1.</em>
</p>
<p align="center">
<img src="PARTE A/Grafica y(n) est 1.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 3. Representación grafica y(n) estudiante 1.</em>
</p>
<p align="center">
<img src="PARTE A/Representacion secuencia est 1.jpeg" width="600">
</p>
<p align="center">
<em>Tabla 1. Representación secuencial estudiante 1.</em>
</p>

#### Señal 𝑦[𝑛] resultante de la convolución usando Python. 

<p align="center">
<img src="PARTE A/y(n) con python est 1.jpeg" width="600">
</p>
<p align="center">
<em>Imagen 2. Calculo convolución con Python estudiante 1.</em>
</p>

#### Representación gráfica usando Python. 

<p align="center">
<img src="PARTE A/convolucion python est 1.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 4. Representación grafica usando Python estudiante 1.</em>
</p>


### ***Estudiante 2***

Código: 5600948 - Cédula: 1011202182

h[n] = {5,6,0,0,9,4,8} - x[n] = {1,0,1,1,2,0,2,1,8,2}

*Resultado de la convolución:* y[n] = {5, 6, 5, 11, 25, 16, 27, 30, 76, 74, 46, 17, 92, 58, 72, 16}

####  Señal 𝑦[𝑛] resultante de la convolución usando sumatorias (a mano):

<p align="center">
<img src="PARTE A/Calculo manual est 2.jpg" width="600">
</p>
<p align="center">
<em>Imagen 3. Calculo manual convolución estudiante 2.</em>
</p>

#### Representación gráfica y secuencial (a mano):

<p align="center">
<img src="PARTE A/Grafica h(n) est 2.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 5. Representación grafica h(n) estudiante 2.</em>
</p>
<p align="center">
<img src="PARTE A/Grafica x(n) est 2.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 6. Representación grafica x(n) estudiante 2.</em>
</p>
<p align="center">
<img src="PARTE A/Grafica y(n) est 2.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 7. Representación grafica y(n) estudiante 2.</em>
</p>
<p align="center">
<img src="PARTE A/Representacion secuencial est 2.jpeg" width="600">
</p>
<p align="center">
<em>Tabla 2. Representación secuencial estudiante 2.</em>
</p>


#### Señal 𝑦[𝑛] resultante de la convolución usando Python. 
<p align="center">
<img src="PARTE A/y(n) con Python est 2.jpeg" width="600">
</p>
<p align="center">
<em>Imagen 4. Calculo convolución con Python estudiante 2.</em>
</p>

#### Representación gráfica usando Python. 

<p align="center">
<img src="PARTE A/convolucion python est 2.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 8. Representación grafica usando Python estudiante 2.</em>
</p>


### ***Parte B – Correlación***

Se definieron dos señales discretas: x1[nTs] = cos(2π100nTs) - x2[nTs] = sin(2π100nTs) con un periodo de muestreo: Ts = 1.25 ms, se encontró la correlación cruzada de ambas señales, la representación grafica y la secuencia resultante como se muestra a continuación.
<p align="center">
<img src="PARTE B/grafica y correlacion.jpeg" width="600">
</p>
<p align="center">
<em>Grafica . Grafica de cada señal y la correlación cruzada de ambas señales.</em>
</p>
<p align="center">
<img src="PARTE B/datos parte b.jpeg" width="600">
</p>
<p align="center">
<em>Tabla . Tabla con la secuencia resultante.</em>
</p>

#### ¿En qué situaciones resulta útil aplicar la correlación cruzada en el procesamiento digital de señales? 

La correlación cruzada es útil cuando se desea medir el grado de similitud entre dos señales o determinar el desfase temporal entre ellas. En procesamiento digital de señales se utiliza en aplicaciones como detección de patrones, sincronización de señales, localización de eventos en una señal y reconocimiento de señales en presencia de ruido, por ejemplo en el análisis de señales biomédicas como ECG o EEG.

### ***Parte C – Análisis de señal biológica***

Se generó una señal biológica utilizando un generador de señales y posteriormente se digitalizó.


#### Frecuencia de Nyquist para la señal generada.
#### Frecuencia de muestreo de 4 veces la frecuencia de Nyquist.
#### Caracterizar la señal obteniendo:

***- Media:***

***- Mediana:*** 

***- Desviación estándar:***

***- Máximo:*** 

***Mínimo:***
#### Clasificación de la señal según su tipo (determinística/aleatoria, periódica/aparádica, analógica/digital).

#### Transformada de Fourier a la señal y graficas:

***- Transformada de la señal:*** 

***-Densidad espectral de potencia:***

#### Análisis de los estadísticos en el dominio de la frecuencia:

***-Frecuencia media:***

***-Frecuencia mediana:***

***-Desviación estándar:***

***-Histograma de frecuencias:***

## Análisis de resultados 

*- Análisis 1: Determine el alcance y las posibles limitaciones de herramientas matemáticas como la convolución y la correlación en el análisis de señales biomédicas.*

Las herramientas matemáticas como la convolución y la correlación permiten analizar y procesar señales biomédicas, facilitando tareas como el filtrado de ruido, la detección de patrones y la comparación entre señales fisiológicas como ECG o EEG. Estas técnicas ayudan a entender cómo responde un sistema ante una señal o qué tan similares son dos señales.

Sin embargo, presentan limitaciones, ya que muchos modelos basados en convolución asumen sistemas lineales e invariantes en el tiempo, lo cual no siempre ocurre en sistemas biológicos reales. Además, la correlación puede verse afectada por ruido o artefactos, lo que puede dificultar la interpretación de los resultados.

*- Análisis 2: Determine el alcance y las posibles limitaciones de emplear la transformada de Fourier para aplicaciones en tiempo real.* 

La transformada de Fourier permite analizar señales en el dominio de la frecuencia e identificar las componentes espectrales presentes, lo cual es útil para estudiar señales biomédicas y detectar anomalías.

No obstante, su aplicación en tiempo real puede tener limitaciones debido al costo computacional del procesamiento continuo y porque la transformada de Fourier asume que la señal es estacionaria, lo cual no siempre se cumple en señales biomédicas que cambian con el tiempo.

## Preguntas para la discusión 

*- ¿Qué utilidad poseen herramientas como la convolución y la correlación en áreas como procesamiento de imágenes?*

En el procesamiento de imágenes, la convolución se utiliza para aplicar filtros que permiten mejorar la imagen, eliminar ruido o detectar bordes y contornos. Por su parte, la correlación se emplea para comparar patrones dentro de una imagen, lo que permite realizar tareas como reconocimiento de objetos o coincidencia de plantillas.
    
*- ¿En cuáles contextos de aplicación la transformada de Fourier ofrece un conjunto de características con mayor poder discriminativo que las que suelen considerarse desde el dominio temporal?* 

La transformada de Fourier es más útil cuando se necesita identificar las frecuencias presentes en una señal, como en el análisis de audio, vibraciones mecánicas o señales biomédicas como EEG o ECG. En estos casos, el dominio de la frecuencia permite detectar patrones o componentes periódicas que no son fáciles de observar en el dominio temporal.

*- ¿En qué se diferencia la correlación cruzada de la convolución?*

La principal diferencia es que en la convolución una de las señales se invierte en el tiempo antes de realizar la operación, mientras que en la correlación cruzada no se realiza esta inversión. La convolución se usa principalmente para analizar la respuesta de sistemas, mientras que la correlación se utiliza para medir la similitud entre dos señales.
