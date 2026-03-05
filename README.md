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

Se definieron dos señales discretas a partir de los dígitos del código estudiantil y el documento de identidad.

Para cada estudiante:

h[n] = dígitos del código - x[n] = dígitos de la cédula

Posteriormente se calculó la convolución discreta usando la definición matemática: y[n] = Σ x[k] h[n - k]

También se implementó el cálculo mediante Python para verificar los resultados obtenidos manualmente.

***- Estudiante 1***

Código: 5600905 - Cédula: 1014990049

h[n] = {5,6,0,0,9,0,5} - x[n] = {1,0,1,4,9,9,0,0,4,9}

*Resultado de la convolución:* y[n] = {5, 6, 5, 26, 78, 99, 68, 36, 106, 170, 99, 45, 36, 81, 20, 45}


<em>Imagen 1. Calculo manual convolución estudiante 1.</em>

***Estudiante 2***

Código: 5600948 - Cédula: 1011202182

h[n] = {5,6,0,0,9,4,8} - x[n] = {1,0,1,1,2,0,2,1,8,2}

*Resultado de la convolución:* y[n] = {5, 6, 5, 11, 25, 16, 27, 30, 76, 74, 46, 17, 92, 58, 72, 16}

<em>Imagen 2. Calculo manual convolución estudiante 2.</em>
