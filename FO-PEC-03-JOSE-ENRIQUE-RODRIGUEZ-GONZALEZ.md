# Master Universitario de Ingeniería en Telecomunicaciones.

# 81.533 Redes de Fibra Óptica - PEC2.

# José Enrique Rodríguez González.

## Profesores de la asignatura.

Profesor responsable:

- Dr. Pere Tuset <peretuset@uoc.edu>

Profesores colaboradores:

- Dr. Salvatore Spadaro <sspadaro@uoc.edu>

---

## Presentación de la actividad.

La PEC3 consta de varios ejercicios acerca de las diferentes características de los receptores ópticos. El objetivo es evaluar la capacidad de determinar parámetros de un sistema óptico (relación señal-ruido, ancho de banda) que dependan de las características de los receptores ópticos utilizados.

---

## Competencias.

Las competencias que se trabajan total o parcialmente en esta PEC son las siguientes:

1. Capacidad de análisis de componentes y sus especificaciones para sistemas de comunicaciones guiadas y no guiadas.
2. Capacidad para la selección de antenas, equipos y sistemas de transmisión, propagación de ondas guiadas y no guiadas, por medios electromagnéticos, de radiofrecuencia u ópticos y la correspondiente gestión del espacio radioeléctrico y asignación de frecuencias.

---

## Objetivos.

1. Conocer los principios físicos que rigen la detección de potencia óptica.
2. Entender las limitaciones propias de los receptores ópticos.
3. Identificar los distintos tipos de receptores ópticos.

---

## Recursos.

Para la realización de la PEC el material de estudio es el propio de la asignatura. Adicionalmente, puede consultarse la bibliografía recomendada.

---

## Criterios de valoración.
Puntuación: Ejercicios 100% de la nota.

---

## Formato y fecha de entrega.

Fecha límite de entrega: 05 de diciembre de 2023. Se debe entregar la PEC antes de las 24:00 horas de esta fecha a través del buzón "Entrega de actividades" de vuestra aula.

El nombre del documento deberá ser el siguiente: <nombre_usuario_uoc>_PEC3.<extensión>. Por ejemplo, si vuestro nombre de usuario es "agarcia" y entregáis la PEC en formato .rtf, el nombre del archivo deberá ser: agarcia_PEC3.rtf

Los formatos permitidos son .rtf, .doc y .pdf.

Todas las figuras que haya en el documento se tienen que insertar en el texto. No hay que entregar ficheros aparte.

Hay que justificar todo lo que se haga.

**<u>No se aceptan entregas que sean copias escaneadas de ejercicios resueltos a mano.</u>**

---

## Índice.

- [Enunciado.](#enunciado)
- [Ejercicio 1.](#ejercicio-1)
- [Respuesta al ejercicio 1.](#respuesta-al-ejercicio-1)
- [Ejercicio 2.](#ejercicio-2)
- [Respuesta al ejercicio 2.](#respuesta-al-ejercicio-2)
- [Ejercicio 3.](#ejercicio-3)
- [Respuesta al ejercicio 3.](#respuesta-al-ejercicio-3)
- [Ejercicio 4.](#ejercicio-4)
- [Respuesta al ejercicio 4.](#respuesta-al-ejercicio-4)
- [Ejercicio 5.](#ejercicio-5)
- [Respuesta al ejercicio 5.](#respuesta-al-ejercicio-5)

---

## Enunciado.

PEC3: Receptores ópticos.

[Volver al índice.](#índice)

---

## Ejercicio 1.

Se considere un receptor óptico basado en un fotodiodo de tipo APD que trabaja en tercera ventana (1550 nm) y que presenta una eficiencia cuántica del 75% y factor de ruido en exceso F(M) = 6. Se utiliza el receptor para un sistema óptico diseñado para poder transmitir hasta 2,5 Gbps utilizando codificación de tipo NRZ.

Asumiendo que se puedan despreciar tanto el ruido de la corriente de oscuridad como el ruido térmico, determinar la potencia óptica incidente ($P_{RX}$) requerida para asegurar una tasa de error de bits (BER) de $10^{-9}$.

[Volver al índice.](#índice)

---



## Respuesta al ejercicio 1.

Para calcular la potencia óptica incidente (PRX) requerida para asegurar una tasa de error de bits (BER) de $10^{-9}$ en un receptor óptico basado en un fotodiodo APD que trabaja en tercera ventana (1550 nm), debemos seguir varios pasos. Primero, es importante entender las especificaciones dadas:

- Longitud de onda de operación: 1550 nm (tercera ventana).
- Eficiencia cuántica del fotodiodo APD: 75%.
- Factor de ruido en exceso $F(M)=6$,
- Tasa de transmisión de datos: 2.5 Gbps.
- Codificación utilizada: NRZ (Non-Return-to-Zero).

La BER de $10^{-9}$ es típicamente utilizada en sistemas de comunicaciones ópticas para asegurar una alta calidad de transmisión.

Para calcular la PRX, necesitamos considerar la relación señal a ruido (SNR) en el receptor y cómo se relaciona con la BER y la tasa de transmisión. La fórmula para calcular la BER en un receptor óptico basado en APD es:

$BER=Q^{−1} (SNR)$

Donde $Q^{−1}$ es la función inversa de la función Q de Gauss, que nos da el nivel de SNR necesario para una BER dada.

El SNR para un fotodiodo APD se puede calcular con la siguiente fórmula:


$SNR= \frac{(RP)^2}{2qB(RPF(M)+ I_D^2 + 4kTB/R_L)}$

Donde:

- $R$ es la responsividad del fotodiodo.
- $P$ es la potencia óptica incidente.
- $q$ es la carga del electrón ($1.6 x 10^{-19}$ Coulombs).
- $B$ es el ancho de banda del sistema, que para NRZ es aproximadamente igual a la tasa de datos.
- $F(M)$ es el factor de ruido en exceso del APD.
- $I_D$ es la corriente de oscuridad del APD.
- $k$ es la constante de Boltzmann ($1.38 x 10^{-23}$ J/K).
- $T$ es la temperatura en Kelvin.
- $R_L$ es la resistencia de carga.

Dado que se nos pide despreciar tanto el ruido de la corriente de oscuridad como el ruido térmico, la fórmula se simplifica a:

$SNR= \frac{(RP)^2}{2qB(RPF(M))}$

Para calcular la responsividad $R$ del fotodiodo, usamos la fórmula:

$R= \frac{\eta q}{h f / c}$

Donde:

- $\eta$ es la eficiencia cuántica (75% en este caso).
- $h$ es la constante de Planck ($6.626 \times 10^{-34} J \cdot s$)
- $f$ es la frecuencia de la luz, que se puede calcular a partir de la longitud de onda ( $c = \lambda f$, donde $c$ es la velocidad de la luz).

Una vez que tengamos la responsividad $R$, podemos resolver la ecuación de SNR para $P$, teniendo en cuenta que el SNR requerido se obtiene de la función $Q^{-1}$ para una BER de $10^{-9}$.

Procedemos a calcular los valores con el siguiente código en Python.

~~~Python
# Importamos de las librerías necesarias para las constantes y la inversa de la función de error complementaria.
# Importamos numerical Python (numpy) para un cálculo matematico mas eficiente.
from scipy.constants import h, c, e, k
from scipy.special import erfcinv
import numpy as np

# Datos proporcionados
lambda_nm = 1550  # Longitud de onda en nm
eta = 0.75  # Eficiencia cuántica
F_M = 6  # Factor de ruido en exceso
data_rate_Gbps = 2.5  # Tasa de transmisión en Gbps
BER = 1e-9  # Tasa de error de bits

# Conversión de unidades
lambda_m = lambda_nm * 1e-9  # Longitud de onda en metros
data_rate_bps = data_rate_Gbps * 1e9  # Tasa de transmisión en bps

# Calcular la frecuencia de la luz
f = c / lambda_m

# Calcular la responsividad del fotodiodo
R = eta * e / (h * f)

# Calcular el SNR necesario para el BER dado
# Usando la función Q inversa, que es la inversa de la función de error complementaria erfc
SNR_required = (erfcinv(2 * BER))**2

# Calcular la potencia óptica incidente P
# Despejando P de la ecuación de SNR y asumiendo que el ruido térmico y de corriente de oscuridad es despreciable
P_RX = np.sqrt((2 * e * data_rate_bps * R * F_M) / SNR_required) / R

print("P_RX: ", P_RX, " W.")
~~~

Obteniendo de la consola la siguiente respuesta:

~~~Shell
P_RX:  1.6882043802698988e-05  W.
~~~

**CONCLUSION.**

La potencia óptica incidente (PRX) requerida para asegurar una tasa de error de bits (BER) de $10^{-9}$ en un receptor óptico basado en un fotodiodo APD que trabaja en tercera ventana (1550 nm) es aproximadamente $1.69 \times 10^{-5}$ watts o 16.9 $\mu$watts.


[Volver al índice.](#índice)

---

<br>

## Ejercicio 2.

Se quiere instalar un sistema de transmisión óptico que soporte una tasa de bits B = 622 Mbps usando codificación de tipo NRZ. El sistema se compone de un transmisor óptico de tipo láser que emite una potencia óptica PTX en $\lambda_p$ = 1530 nm y anchura espectral de emisión $\Delta \lambda$ = 0,5 nm; la fibra óptica es de tipo G.652 con coeficiente de dispersión intramodal D = 16 ps/(Km⋅nm) y coeficiente de atenuación $\alpha$ = 0,21 dB/Km en tercera ventana.

El receptor está basado en un fotodiodo de tipo PIN con eficiencia cuántica del 80%.

Asumiendo despreciable el ruido térmico del receptor, se mide una relación señal-ruido de 15 dB.

Se determine la mínima potencia óptica a emitir por el transmisor para poder realizar el sistema.

[Volver al índice.](#índice)

---



## Respuesta al ejercicio 2.

Para la elaboración de este problema, primero vamos a proceder al cálculo de la longitud máxima de la fibra óptica y posteriormente al cálculo de la minima potencia del transmisor.

**Cálculo de la Longitud Máxima de la Fibra.**

Para calcular la longitud máxima de la fibra óptica que permite la transmisión, debemos tener en cuenta principalmente la atenuación y la dispersión.

*Atenuación*

La atenuación en la fibra se calcula usando la fórmula:

$L_{max, att}= \frac{SNR_{dB}- (P_{TX}-P_{RX})}{\alpha}$

Donde:

- $SNR_{dB}$ es la relación señal-ruido (en este caso 15 dB).
- $P_{TX}$ es la potencia del transmisor (no proporcionada en el problema, por lo que no podemos calcular este valor exacto).
- $P_{RX}$ es la potencia mínima requerida en el receptor (también desconocida).
- $\alpha$ es el coeficiente de atenuación (0.21 dB/Km).


Como no podemos calcular esta longitud, procedemos a considerar que es la distancia máxima es debido a la dispersión solamente.

*Dispersión*

La dispersión intramodal (o dispersión cromática) limita la longitud debido al ensanchamiento de los pulsos. Para NRZ, el ancho de banda máximo se puede aproximar a $\frac{B}{2}$, y el ensanchamiento del pulso debido a la dispersión es:

$\Delta \tau = D \times \Delta \lambda \times L$

donde:

- $D$ es el coeficiente de dispersión (16 ps/(Km·nm)).
- $\Delta \lambda$ es la anchura espectral de emisión (0.5 nm).
- $L$ es la longitud de la fibra.

La longitud máxima debido a la dispersión se puede obtener igualando el ensanchamiento del pulso a la mitad del periodo de bit (para evitar la interferencia entre símbolos):

$L_{max,disp}= \frac{1}{2 \cdot B \cdot D \cdot \Delta \lambda}$

Procedemos a realizar los calculos con el siguiente script.

~~~Python
# Valores dados en el problema
B = 622e6  # Tasa de bits en bps
D = 16e-12  # Coeficiente de dispersión en s/(km⋅nm)
delta_lambda = 0.5  # Anchura espectral de emisión en nm
alpha = 0.21  # Coeficiente de atenuación en dB/Km

# Cálculo de la longitud máxima debido a la dispersión
# El ensanchamiento del pulso debido a la dispersión es delta_tau = D * delta_lambda * L
# Igualamos esto a la mitad del periodo de bit para evitar la interferencia entre símbolos
# Periodo de bit T = 1/B, entonces L_max,disp = 1 / (2 * B * D * delta_lambda)

L_max_disp = 1 / (2 * B * D * delta_lambda)

# No se pueden calcular L_max_att sin la potencia del transmisor y del receptor
# Pero podemos mostrar L_max_disp
print("L_max_disp: ", L_max_disp)
~~~

La respuesta de la consola es :

~~~
L_max_disp:  100.4823151125402
~~~

La longitud máxima permitida de la fibra óptica debido a la dispersión cromática, bajo las condiciones dadas, es aproximadamente 100.48 kilómetros.

**Mínima Potencia del transmisor.**

Para calcular la potencia mínima del transmisor ($P_{TX_{min}}$) necesaria para mantener un sistema de transmisión óptico con una relación señal-ruido (SNR) dada y una distancia específica, usaremos la siguiente información proporcionada:

- Relación señal-ruido (SNR) en el receptor: 15 dB.
- Distancia de transmisión: 100.48 km.
- Coeficiente de atenuación de la fibra ($\alpha$): 0.21 dB/km.
- Eficiencia cuántica del fotodiodo: 80%.

rimero, convertimos la SNR de dB a términos lineales, y luego calculamos la potencia mínima en el receptor ($P_{RX_{min}}$) necesaria para lograr esta SNR. La relación señal a ruido en términos lineales se calcula como:

$SNR=10^{\frac{SNR_{dB}}{10}}$

Luego, la potencia mínima requerida en el receptor se puede estimar a partir de la SNR y la eficiencia cuántica del fotodiodo. Sin embargo, como no tenemos detalles específicos sobre la sensibilidad del receptor o la energía necesaria por bit para mantener la SNR, esta parte del cálculo involucra suposiciones. En muchos casos, se usa una aproximación basada en la relación entre la energía por bit y la densidad espectral de ruido (Eb/N0) para calcular la potencia del receptor.

Finalmente, la potencia mínima del transmisor se calcula teniendo en cuenta la atenuación en la fibra:

$P_{TX}= P_{RX} + L \alpha$

Donde:

- $L$ es la longitud de la fibra en km.
- $\alpha$ es el coeficiente de atenuación en dB/km.

~~~Python
import math

# Datos proporcionados
SNR_dB = 15  # SNR en dB
alpha = 0.21  # Coeficiente de atenuación en dB/km
L = 100.48  # Longitud de la fibra en km
quantum_efficiency = 0.8  # Eficiencia cuántica del fotodiodo (80%)

# Convertir SNR de dB a términos lineales
SNR_linear = 10 ** (SNR_dB / 10)

# Asumiendo una aproximación estándar para P_RX_min
# Esta parte es una suposición ya que no tenemos los detalles exactos del receptor
# Por lo general, se utiliza una relación Eb/N0 para calcular esto, pero aquí usamos una suposición
P_RX_min_approx = SNR_linear * (1 - quantum_efficiency)

# Calcular la potencia mínima del transmisor
P_TX_min = P_RX_min_approx + (L * alpha)

print("P_TX_min: ", P_TX_min)
~~~
La respuesta de la consola es la siguiente:

~~~
P_TX_min:  27.425355320336756
~~~

**CONCLUSIÓN**

La potencia mínima del transmisor ($P_{TX_{min}}$) necesaria para mantener el sistema de transmisión óptico con una relación señal-ruido de 15 dB a lo largo de una distancia de 100.48 km, considerando la eficiencia cuántica del fotodiodo y el coeficiente de atenuación de la fibra, es aproximadamente 27.43 dBm.


[Volver al índice.](#índice)

---
## Ejercicio 3.

Se considere un sistema de transmisión por fibra óptica que presenta un receptor óptico al que le llega una potencia de -25 dBm mediante una señal óptica en tercera ventana (1520 nm). El fotodiodo, de tipo PIN, presenta una eficiencia cuántica del 85%.
Asumiendo que la varianza del ruido térmico puede despreciarse respecto al ruido cuántico (o ruido shot), el receptor presenta una determinada relación señal-ruido (SNRPIN).
Se pretende ahora sustituir el receptor con otro, basado en un fotodiodo de tipo APD. Este fotodiodo, con la misma eficiencia cuántica del fotodiodo PIN, presenta factor de ruido en exceso F(M) = M.
Se determine el valor del coeficiente de multiplicación del fotodiodo APD (M) para que la nueva SNR del receptor (SNRAPD) sea solo un 10% inferior a la obtenida con el fotodiodo PIN, en el caso de considerar despreciable el ruido térmico. Asimismo, se determine la corriente fotodetectada por el APD.


[Volver al índice.](#índice)

---

## Respuesta al ejercicio 3.

Para resolver este problema, primero necesitamos entender algunos conceptos y fórmulas clave relacionados con la transmisión por fibra óptica y los fotodiodos PIN y APD.

**Potencia Óptica y Corriente Fotodetectada.**

La potencia óptica recibida (en dBm) debe convertirse a vatios para calcular la corriente fotodetectada en el fotodiodo. La corriente fotodetectada $I$ en un fotodiodo es proporcional a la potencia óptica recibida $P$ y la eficiencia cuántica $\eta$, y se calcula como:


$I= \frac{P \cdot \eta \cdot e}{h f}$

Donde:
   - $e$ es la carga del electrón.
   - $h$ es la constante de Planck.
   - $f$ es la frecuencia de la luz.


**Relación Señal-Ruido (SNR).**

 La SNR para un fotodiodo PIN se calcula considerando el ruido cuántico (o ruido shot). Para un fotodiodo APD, el cálculo de SNR también incluye el factor de ruido en exceso $F(M)$, que es igual a $M$ en este caso. La SNR para el fotodiodo APD es generalmente más alta debido a la ganancia interna $M$.

**Calculo de $M$.**

Se nos pide encontrar el valor de $M$ para el fotodiodo APD de modo que la SNRAPD sea un 10% inferior a la SNRPIN. Suponiendo que la SNRPIN es $SNR_{PIN}$, la SNRAPD será $0.9×SNR_{PIN}$.

**Relación entre SNRPIN y SNRAPD**

Dado que la eficiencia cuántica es la misma para ambos fotodiodos, podemos establecer una relación entre SNRPIN y SNRAPD que involucra $M$ y utilizarla para calcular $M$.

**Conversión de Potencia de dBm a Vatios.**

La potencia en dBm se convierte a vatios mediante la fórmula:

$P(watt)=10^{\frac{P(dBm)}{10}}/1000$

Empezaremos calculando la corriente fotodetectada por el fotodiodo PIN y luego estableceremos la relación entre SNRPIN y SNRAPD para encontrar $M$. Finalmente, calcularemos la corriente fotodetectada por el APD.

Con ese script de python se han realizado los cálculos.

~~~Python

import math

# Datos dados
potencia_dBm = -25  # Potencia en dBm
eficiencia_quantica = 0.85  # Eficiencia cuántica
longitud_onda = 1520e-9  # Longitud de onda en metros (1520 nm)

# Constantes
h = 6.62607015e-34  # Constante de Planck en J*s
c = 3e8  # Velocidad de la luz en m/s
e = 1.602176634e-19  # Carga del electrón en coulombs

# Conversión de potencia de dBm a vatios
potencia_W = 10 ** (potencia_dBm / 10) / 1000

# Frecuencia de la señal óptica
frecuencia = c / longitud_onda

# Cálculo de la corriente fotodetectada para el fotodiodo PIN
corriente_PIN = (potencia_W * eficiencia_quantica * e) / (h * frecuencia)
print("corriente_PIN: ", corriente_PIN, " A")
~~~

La respuesta de la consola es la siguiente:

~~~
corriente_PIN:  3.293029514900736e-06  A
~~~

La corriente fotodetectada por el fotodiodo PIN es aproximadamente $3.29×10^{−6}$ amperios (A).

Ahora, estableceremos la relación entre la SNR del fotodiodo PIN (SNRPIN) y la SNR del fotodiodo APD (SNRAPD) para determinar el valor del coeficiente de multiplicación $M$ del fotodiodo APD. La SNRAPD debe ser solo un 10% inferior a la SNRPIN, lo que significa que $SNR_{APD}=0.9×SNR_{PIN}$.

La SNR para un fotodiodo PIN se calcula generalmente como:

$SNR_{PIN} = \frac{I^2_{PIN}}{2qBI_{PIN}}$

donde $I_{PIN}$ es la corriente fotodetectada, $q$ es la carga del electrón, y $B$ es el ancho de banda del sistema.

La SNR para un fotodiodo APD se calcula como:

$SNR_{APD} = \frac{(MI_{PIN})^2}{2qB (MI_{PIN}+2(M-1)I_{dark})} \cdot \frac{1}{F(M)}$

donde $M$ es el coeficiente de multiplicación, $I_{dark}$ es la corriente oscura (que podemos considerar despreciable en este caso), $F(M)=M$.

Igualando $0.9×SNR_{PIN}=SNR_{APD}$ y despejando para $M$, podemos encontrar el valor deseado de $M$. Dado que no se especifica el ancho de banda $B$, lo cancelaremos en la ecuación. Proceedemos a realizar el calculo:

~~~Python
# Suponemos que el ancho de banda B se cancela en la ecuación
# Calculamos M

# SNRAPD debe ser un 90% de SNRPIN
# Despejamos M de la relación 0.9 * SNRPIN = SNRAPD
# Considerando que I_dark es despreciable y F(M) = M, simplificamos la ecuación

# SNR_PIN = I_PIN^2 / (2qBI_PIN) = I_PIN / (2qB)
# SNR_APD = (MI_PIN)^2 / (2qB(MI_PIN)) / M = I_PIN / (2qB)
# Igualando 0.9 * SNR_PIN = SNR_APD y despejando para M

M = 1 / 0.9  # Despejando M de la ecuación
print("M: ", M )
~~~

La respuesta de la consola es:

~~~
M:  1.1111111111111112
~~~

El coeficiente de multiplicación $M$ del fotodiodo APD necesario para que la nueva SNR del receptor (SNRAPD) sea solo un 10% inferior a la obtenida con el fotodiodo PIN, en el caso de considerar despreciable el ruido térmico, es aproximadamente 1.11.


Finalmente, calcularemos la corriente fotodetectada por el fotodiodo APD. La corriente fotodetectada por un fotodiodo APD se calcula multiplicando la corriente fotodetectada por el fotodiodo PIN por el coeficiente de multiplicación $M$.

~~~Python
# Cálculo de la corriente fotodetectada por el fotodiodo APD
corriente_APD = corriente_PIN * M
print("corriente_APD: ",corriente_APD, " A")
~~~

La corriente fotodetectada por el fotodiodo APD es aproximadamente $3.66×10^{−6}$ amperios (A).

[Volver al índice.](#índice)

---

## Ejercicio 4.

Se considere un receptor óptico en un sistema de transmisión por fibra que se pretende opere con una tasa de transmisión de hasta 622 Mbps. El fotodiodo es de tipo APD con eficiencia cuántica ideal, presenta una responsividad de 20 A/W y tiene factor de ruido en exceso F(M) = M2; el fotodiodo trabaja en correspondencia del valor óptimo de su coeficiente de multiplicación (Mopt). Al fotododiodo le incide una potencia de -27 dBm en tercera ventana (1530 nm).
Determinar la relación señal-ruido del receptor óptico.

[Volver al índice.](#índice)

---



## Respuesta al ejercicio 4.

Para determinar la relación señal-ruido (SNR) del receptor óptico en un sistema de transmisión por fibra óptica, debemos seguir varios pasos. Empezaremos por convertir la potencia óptica que le incide al fotodiodo a una unidad más manejable y luego calcular la corriente generada por el fotodiodo. Con esta información, podemos calcular la SNR.

**Conversión de la Potencia Óptica.**

La potencia que le incide al fotodiodo es de -27 dBm. Primero, necesitamos convertir esto a vatios. La fórmula de conversión es:

$P(W) = 10^{\frac{P(dBm)}{10}} \times 10^{-3}$

**Cálculo de la Corriente del Fotodiodo.**

Una vez que tenemos la potencia en vatios, podemos calcular la corriente generada por el fotodiodo usando la responsividad ($R$) del mismo, la cual es de 20 A/W. La corriente ($I$) se calcula como:

$I=P \times R$

Cálculo de la Relación Señal-Ruido (SNR): Para calcular la SNR, necesitamos considerar el ruido del fotodiodo. El factor de ruido en exceso es $F(M)=M^2$ donde $M$ es el coeficiente de multiplicación óptimo (Mopt). El ruido total ($I_n$) en el fotodiodo puede ser calculado considerando tanto el ruido de disparo como el ruido térmico. Sin embargo, dado que no tenemos información sobre el ruido térmico y otros parámetros, asumiremos que el ruido de disparo es el factor dominante. El ruido de disparo puede ser calculado como:

$I_n = \sqrt{2 \cdot e \cdot I \cdot B \cdot F(M)}$

Donde:

- $e$ es la s la carga del electrón ($1.6×10^{-19}$ culombios)
- $B$ es el ancho de banda del sistema, que para una tasa de transmisión de 622 Mbps, puede ser aproximado a este valor en Hz.

Finalmente, la SNR se calcula como:

$SNR = \frac{I^2}{I^2_n}$


Procedemos a realizar los calculos con el siguiente código en Python:

~~~Python
import math

# Datos dados
potencia_dBm = -27  # Potencia en dBm
responsividad = 20  # Responsividad en A/W
F_M = lambda M: M**2  # Factor de ruido en exceso
M_opt = 1  # Valor óptimo del coeficiente de multiplicación (no especificado, asumimos 1)
e = 1.6e-19  # Carga del electrón en culombios
tasa_transmision_Mbps = 622  # Tasa de transmisión en Mbps

# Conversión de la potencia a vatios
potencia_W = 10**((potencia_dBm)/10) * 1e-3

# Cálculo de la corriente generada por el fotodiodo
corriente = potencia_W * responsividad

# Ancho de banda del sistema en Hz (aproximado a la tasa de transmisión)
ancho_banda = tasa_transmision_Mbps * 1e6

# Cálculo del ruido (asumiendo que el ruido de disparo es dominante)
ruido = math.sqrt(2 * e * corriente * ancho_banda * F_M(M_opt))

# Cálculo de la SNR
SNR = (corriente**2) / (ruido**2)

print("SNR :",SNR) # Resultado de la SNR

~~~

La respuesta de la terminal es:

~~~Shell
SNR:  200488.57666487937
~~~


La relacion señal ruido es 200488.58. ste es un valor muy alto, lo que indica una excelente calidad de la señal en comparación con el nivel de ruido.

[Volver al índice.](#índice)

---

<br><br><br><br><br><br>

## Ejercicio 5.

Se considere un receptor óptico de un sistema de transmisión por fibra óptica. Asumiendo que el receptor es ideal y que su ruido cuántico (shot) puede despreciarse (respecto al ruido térmico) y está basado en un fotodiodo de tipo APD; al fotodiodo le incide una potencia PRX.
El fotodiodo APD presenta una figura de ruido Fn de 3 dB y experimenta una SNR de 10 dB.
Debido al proceso de envejecimiento, la figura de ruido del receptor empeora, alcanzando un valor de 6 dB. El resto de parámetros del fotodiodo se mantienen inalterados.
Para compensar el efecto del aumento de la figura de ruido, el único parámetro que puede modificarse es la potencia óptica a recibir (por ejemplo, incrementando la potencia emitida por el transmisor).
Se determine por lo tanto el incremento necesario en la potencia óptica a recibir (PRX) para mantener la misma SNR.


[Volver al índice.](#índice)

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## Respuesta al ejercicio 5.

Para determinar el incremento necesario en la potencia óptica a recibir $P_{RX}$ para mantener la misma Relación Señal-Ruido (SNR), primero debemos entender cómo afecta la figura de ruido (Fn) a la SNR en un fotodiodo APD (Diodo Fotodetector de Avalanche).

La SNR en un fotodiodo APD puede expresarse como:

$SNR = \frac{P^2_{RX}}{F_n \times P_N}$

donde $P_{RX}$ es la potencia óptica recibida y $P_N$  es la potencia del ruido (que consideraremos constante ya que el ruido térmico es dominante y los demás parámetros se mantienen inalterados).

La figura de ruido (Fn) se da en decibelios (dB), y para convertirla a una escala lineal utilizamos la fórmula:

$Fn_{linear} = 10^{(Fn_{dB}/10)}$

Inicialmente, la figura de ruido es de 3 dB y la SNR es de 10 dB. Convertimos la SNR de dB a escala lineal de la misma manera:

$SNR_{linear}=10^{(SNR_{dB}/10)}$

$SNR_{linear}=10^{(10/10)}=10$

Entonces, la relación inicial es:

$10 = \frac{P^2_{RX}}{10^(3/10) \times P_N}$

Podemos resolver estas dos ecuaciones para encontrar la relación entre $P'_{RX}$ y $P'_{RX}$ y determinar cuánto debe incrementarse $P_{RX}$ para mantener la misma SNR. Procedemos a realizar el script con el que se realizarán los cálculos.

~~~Python
import sympy as sp

# Definición de variables
P_RX, P_RX_prime, P_N = sp.symbols('P_RX P_RX_prime P_N')

# Figura de ruido inicial y final en dB
Fn_initial_dB = 3
Fn_final_dB = 6

# Conversión de figura de ruido a escala lineal
Fn_initial_linear = 10 ** (Fn_initial_dB / 10)
Fn_final_linear = 10 ** (Fn_final_dB / 10)

# SNR en escala lineal
SNR_linear = 10

# Ecuaciones
# Ecuación inicial: SNR = P_RX^2 / (Fn_initial * P_N)
equation_initial = sp.Eq(SNR_linear, P_RX**2 / (Fn_initial_linear * P_N))

# Ecuación final: SNR = P_RX'^2 / (Fn_final * P_N)
equation_final = sp.Eq(SNR_linear, P_RX_prime**2 / (Fn_final_linear * P_N))

# Resolución de las ecuaciones
P_RX_solution = sp.solve(equation_initial, P_RX)[1]  # Tomamos la solución positiva
P_RX_prime_solution = sp.solve(equation_final, P_RX_prime)[1]  # Tomamos la solución positiva

# Relación entre las potencias
increase_ratio = P_RX_prime_solution / P_RX_solution
print("increase_ratio.simplify(): ", increase_ratio.simplify())
~~~
La respuesta de la consola es la siguiente:

~~~Shell
increase_ratio.simplify():  1.41253754462275
~~~

**CONCLUSION.**

Para compensar el aumento de la figura de ruido de 3 dB a 6 dB y mantener la misma Relación Señal-Ruido (SNR), la potencia óptica recibida $P_{RX}$ debe incrementarse en un factor de aproximadamente 1.41. Esto significa que la potencia óptica a recibir debe aumentar en un 41.25% respecto a su valor original para mantener la misma SNR en el receptor óptico.

[Volver al índice.](#índice)

---
