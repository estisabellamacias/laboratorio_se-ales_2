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
<em>Grafica 8 . Grafica de cada señal y la correlación cruzada de ambas señales.</em>
</p>
<p align="center">
<img src="PARTE B/datos parte b.jpeg" width="600">
</p>
<p align="center">
<em>Tabla 3. Tabla con la secuencia resultante.</em>
</p>

#### ¿En qué situaciones resulta útil aplicar la correlación cruzada en el procesamiento digital de señales? 

La correlación cruzada es útil cuando se desea medir el grado de similitud entre dos señales o determinar el desfase temporal entre ellas. En procesamiento digital de señales se utiliza en aplicaciones como detección de patrones, sincronización de señales, localización de eventos en una señal y reconocimiento de señales en presencia de ruido, por ejemplo en el análisis de señales biomédicas como ECG o EEG.

### ***Parte C – Análisis de señal biológica***

Se generó una señal biológica utilizando un generador de señales y posteriormente se digitalizó.


#### Frecuencia de Nyquist para la señal generada:
La frecuencia de Nyquist es 200Hz 
#### Frecuencia de muestreo de 4 veces la frecuencia de Nyquist:
La frecuencia de muestreo seria 800Hz pero se utilizo 1000Hz para mejorar la imagen

<p align="center">
<img src="PARTE C/señal normalizada.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 9. Señal resultante.</em>
</p>

#### Caracterizar la señal obteniendo:

<p align="center">
<img src="PARTE C/punto 3.jpeg" width="600">
</p>
<p align="center">
<em>Imagen 5. Media, mediana, desviación estándar, máximo, mínimo.</em>
</p>

#### Clasificación de la señal según su tipo (determinística/aleatoria, periódica/aparádica, analógica/digital).

<p align="center">
<img src="PARTE C/cladificacion señal.jpeg" width="600">
</p>
<p align="center">
<em>Imagen 6. Clasificación de la señal.</em>
</p>

#### Transformada de Fourier a la señal y graficas:

***- Transformada de la señal y densidad espectral de potencia:***

<p align="center">
<img src="PARTE C/transformada y densidad.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 10.Transformada de la señal y desidad espectral de potencia.</em>
</p>

#### Análisis de los estadísticos en el dominio de la frecuencia:

<p align="center">
<img src="PARTE C/estadisticos dominio frecuencia.jpeg" width="600">
</p>
<p align="center">
<em>Imagen 7.Datos estadisticos en el dominio de la frecuencia.</em>
</p>

<p align="center">
<img src="PARTE C/histograma.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 11.Histograma.</em>
</p>

## Codigos utilizados 

### Codigo en C:

Este código implementa la captura de señales biomédicas utilizando un microcontrolador en este caso la STM32.

**Estructura de Datos**

Se definen variables globales para el manejo de la información capturada:

- `uint32_t datos`: Almacena la conversión actual del ADC asistida por DMA.
- `uint8_t datosenvio[50]`: Buffer de transmisión que acumula 25 muestras (cada una dividida en 2 bytes, sumando 50 bytes) antes de enviarlas por USB.
- `int contador`: Índice que rastrea el llenado del buffer para asegurar que siempre se envíen paquetes completos de 50 bytes.

**Configuración de Periféricos (HAL)**

En la función `main`, se inicializan los módulos críticos:

- `MX_ADC1_Init()`: Configura el ADC1 para trabajar con disparador externo del Timer 3 (`ADC_EXTERNALTRIGCONV_T3_TRGO`), permitiendo un muestreo preciso.
- `MX_TIM3_Init()`: Establece la frecuencia de muestreo. El Timer 3 actúa como el "reloj" que le indica al ADC cuándo tomar una muestra.
- `MX_USB_DEVICE_Init()`: Prepara la interfaz USB CDC (Puerto COM Virtual) para enviar los datos a la computadora.

**Lógica de Captura y Procesamiento**
(`HAL_ADC_ConvCpltCallback`)

Esta es la parte más importante del algoritmo, donde se gestiona la interrupción por conversión completa:

**• División de Bytes (Byte Splitting)**

Como el ADC entrega valores de 12 bits y el protocolo USB transmite datos en bytes (8 bits), cada muestra se divide en dos:

```c
datosenvio[contador++] = datos[0] & 0xFF;
datosenvio[contador++] = (datos[0] >> 8) & 0xFF;
```
- El primer byte guarda los 8 bits menos significativos.
- El segundo byte guarda los bits restantes desplazados.

**• Transmisión por USB:** Cuando el contador llega a 50 bytes (25 muestras), se dispara la función `CDC_Transmit_FS(datosenvio, 50)`; enviando el paquete a la computadora para su posterior análisis en Python. 

### Codigo en Python:

**Arquitectura y Librerías Utilizadas**

El código utiliza varias librerías especializadas de Python para realizar el procesamiento y análisis de las señales:

- `numpy`: Permite realizar operaciones matemáticas eficientes y manipular arreglos de datos numéricos.
- `matplotlib`: Se utiliza para generar las gráficas que permiten visualizar las señales y los resultados del análisis.
- `scipy.fft`: Implementa la Transformada Rápida de Fourier para analizar el contenido frecuencial de la señal.
- `scipy.signal`: Proporciona herramientas de análisis espectral como el método de Welch para calcular la densidad espectral de potencia.

**Procesamiento de Convolución**

En la primera sección del código se implementa el cálculo de la convolución discreta entre dos secuencias. Esta operación permite determinar la salida de un sistema lineal e invariante en el tiempo cuando se conoce su respuesta al impulso.

Las señales utilizadas son:

- `x[n]`: señal de entrada asociada a los dígitos de la cédula.
- `h[n]`: respuesta del sistema asociada al código asignado.

El cálculo de la convolución se realiza mediante la función:

```python
y = np.convolve(x, h)
```

La secuencia resultante `y[n]` representa la salida del sistema al aplicar la señal de entrada.

Además del cálculo numérico, el código genera tres representaciones gráficas que permiten visualizar el proceso completo:

- La señal de entrada `x[n]`
- La respuesta del sistema `h[n]`
- La señal resultante `y[n] = x[n] * h[n]`

**Cálculo de Correlación Cruzada**

En la segunda sección del código se calcula la correlación cruzada entre dos señales periódicas para analizar su nivel de similitud.

Las señales utilizadas se definen de la siguiente forma:

```python
x1[nTs] = cos(2π100nTs)
x2[nTs] = sin(2π100nTs)
```

Estas señales tienen una frecuencia de 100 Hz y se generan a partir de un periodo de muestreo de 1.25 ms.

El cálculo de la correlación cruzada se realiza utilizando:

```python
r_x1x2 = np.correlate(x1, x2, mode='full')
```

La secuencia resultante muestra el grado de similitud entre ambas señales para diferentes desplazamientos temporales (`lags`).

En el análisis del resultado se observa que:

- La secuencia presenta un comportamiento antisimétrico.
- El valor en `lag = 0` es cercano a cero.

Esto ocurre porque las funciones seno y coseno son ortogonales, por lo que su correlación en fase es mínima.

El resultado también se representa gráficamente mediante un diagrama tipo *stem*, donde se observa la amplitud de la correlación para cada desplazamiento.

**Carga y Procesamiento de Señal Biológica**

La tercera sección del código realiza el análisis de una señal biológica de tipo Electrooculografía (EOG).

La señal se carga desde un archivo de texto mediante:

```python
raw_data = np.loadtxt(archivo)
```

La frecuencia de muestreo utilizada para esta señal es:

```
fs_eog = 1000 Hz
```

Esto significa que se registran 1000 muestras por segundo.

**Normalización de la Señal**

Para facilitar el análisis y comparación de los datos, la señal se normaliza al rango de amplitud [-1, 1] mV mediante una transformación lineal.

```python
eog_norm = 2*(raw_data - np.min(raw_data))/(np.max(raw_data)-np.min(raw_data)) - 1
```

Este proceso elimina diferencias de escala y permite analizar únicamente la forma de la señal.

**Caracterización Estadística de la Señal**

El código calcula varios parámetros estadísticos que permiten describir el comportamiento de la señal en el dominio del tiempo:

- `Media`: valor promedio de la señal.
- `Mediana`: valor central de la distribución.
- `Desviación estándar`: mide la dispersión de los datos.
- `Máximo`: mayor valor de amplitud registrado.
- `Mínimo`: menor valor de amplitud registrado.

**Análisis en el Dominio de la Frecuencia**

Para estudiar el contenido frecuencial de la señal se utiliza la Transformada Rápida de Fourier.

```python
yf = fft(eog_norm)
xf = fftfreq(N, 1/fs_eog)
```

La FFT permite transformar la señal desde el dominio del tiempo hacia el dominio de la frecuencia, mostrando qué componentes frecuenciales están presentes en la señal.

Adicionalmente se calcula la Densidad Espectral de Potencia utilizando el método de Welch:

```python
f_psd, psd = welch(eog_norm, fs_eog, nperseg=1024)
```

Este método permite estimar de manera más estable cómo se distribuye la energía de la señal en diferentes frecuencias.

**Estadísticos Espectrales**

A partir de la densidad espectral de potencia se calculan diferentes parámetros que describen el comportamiento espectral de la señal:

- `Frecuencia media`: frecuencia promedio ponderada por la potencia.
- `Frecuencia mediana`: frecuencia que divide el espectro en dos partes de igual energía.
- `Desviación estándar espectral`: indica la dispersión de la energía alrededor de la frecuencia media.

Estos valores permiten caracterizar el contenido frecuencial dominante de la señal.

**Visualización de Resultados**

El código genera varias gráficas para facilitar la interpretación del análisis realizado:

- Señal EOG en el dominio del tiempo.
- Magnitud de la Transformada de Fourier.
- Densidad Espectral de Potencia (PSD).
- Histograma de amplitudes de la señal.

## Diagramas de flujo

### Codigo en C

<p align="center">
<img src="DIAGRAMAS/Diagrama de flujo codigo c.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 12. Diagrama de flujo codigo en C.</em>
</p>

### Codigo en Python

<p align="center">
<img src="DIAGRAMAS/Diagra,a de flujo python.jpeg" width="600">
</p>
<p align="center">
<em>Grafica 13. Diagrama de flujo codigo en Python.</em>
</p>

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
