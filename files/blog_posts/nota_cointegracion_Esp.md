# Cointegración como estructura de rango reducido: una reflexión para el análisis macroeconómico

La cointegración suele explicarse como una herramienta para estudiar relaciones estables entre variables no estacionarias. Esa descripción es es básicamente correcta, pero no es suficiente para presentar una intuición más profunda de lo que significa analizar dinámicas macroeconómicas de largo plazo. Cuando se analizan series que evolucionan con tendencias y muestran episodios de quiebres estructurales, observar combinaciones lineales que permanecen relativamente estables nos presenta la pregunta de fondo:  ¿qué estructura genera ese comportamiento?

Este post propone una lectura que combina intuiciones conocidas con algunos avances que han ido consolidándose en la literatura: el carácter limitado de los métodos basados en regresiones en niveles, la propuesta de Johansen de interpretar la cointegración como una restricción de rango sobre un VAR, y la utilidad de enmarcar todo esto dentro del enfoque de autoregresiones de rango reducido.

La tesis general es sencilla: más que una técnica puntual, la cointegración invita a pensar el largo plazo como un objeto multidimensional que surge de la interacción entre tendencias comunes y fuerzas de corrección. En este sentido, el estudio de series de tiempo usando métodos de co-integración son fundamentales para los interesados en estudiar procesos de larga duración conjuntamente a episodios historicos coyunturales 

El método de Engle y Granger ha sido uno de una de las puertas de entrada canonicas para el estudio del concepto de co-integración. Usando una regresión en niveles entre variables integradas de orden uno, seguida de un test de raíz unitaria sobre los residuos. El método destaca por ser simple, intuitivo, y fácil de aplicar.

Sin embargo, cuando el análisis exige recuperar más de una relación de largo plazo, o cuando interesa modelar simultáneamente la dinámica de ajuste, este enfoque muestra límites claros. La elección de la variable dependiente introduce asimetrías difíciles de justificar, y la inferencia del residuo tiende a ser frágil en muestras pequeñas. Por lo mismo, muchos trabajos lo utilizan hoy como una etapa previa de pre-testeo, más que como un modelo definitivo.

El enfoque de Johansen parte de un VAR en niveles y lo reescribe como un modelo de corrección del errores. En ese formato, la cointegración está contenida en la matriz de largo plazo \(\Pi\). Su rango determina cuántas relaciones de largo plazo existen, y su descomposición \(\Pi = \alpha \beta'\) separa el (o los) vector de co-integración de largo plazo, del coeficiente de ajuste en el corto plazo. 

Esta forma de proceder tiene dos ventajas. Primero, permite identificar múltiples relaciones de largo plazo. Segundo, integra la dinámica de corto plazo en el mismo sistema, de modo que las fuerzas de ajuste del sistema se estiman simultaneamente como parte estructural del modelo, no por etapas. 

Los tests de traza y de máximo valor propio, habituales en esta literatura, derivan directamente del problema de valores propios asociado al VECM. Aunque puedan parecer instrumentos técnicos, en realidad reflejan una idea más simple: determinar cuántas combinaciones lineales se mantienen estacionarias mientras el resto del sistema tiene una tendencia implicita. 

Una forma útil de interpretar estos resultados es ver la cointegración como un caso particular de las autoregresiones de rango reducido. En ese marco, un VAR sin restricciones tiene coeficientes de rango completo; imponer cointegración equivale a acotar el rango de la matriz de largo plazo. La dimensión reducida define el espacio en el que se estabilizan ciertas combinaciones, mientras que su complemento contiene las tendencias comunes.

Esta lectura pone el acento en *la geometría del sistema* en vez de en la interpretación neo-clásica bajo la noción de un “equilibrio” único . De est modo, el largo plazo no aparece como un punto al que todo converge, sino como un subespacio en el que operan las fuerzas de ajuste del sistema, en contraste con otras direcciones en las que la dinámica es más persistente.

Pensar la cointegración desde esta óptica tiene implicancias prácticas para quienes trabajan con series macroeconómicas históricas o comparativas:

- Invita a considerar que pueden existir varias relaciones de largo plazo simultáneas, cada una con distinta relevancia económica.
- Refuerza la conveniencia de emplear métodos de sistema cuando se analizan variables estrechamente vinculadas en teoría, como producto, capital, salarios o tasas de ganancia.
- Ayuda a interpretar el largo plazo no como un equilibrio estático, sino como una estructura compuesta de tendencias y restricciones.
- Sugiere cautela con muestras pequeñas, donde las pruebas estándar pueden sobredetectar relaciones estables, haciendo útil complementar el análisis con métodos basados en replicaciones para la inferencia causal como bootstrap.

La cointegración no es únicamente un mecanismo econométrico para “controlar tendencias”. Es una forma de representar cómo ciertas combinaciones económicas se estabilizan mientras otras se desplazan en el tiempo. El enfoque de Johansen con foco en el rango reducido permiten captar esa estructura de modo más completo, integrando el corto y el largo plazo en un mismo sistema.

Para quienes investigan procesos económicos de larga duración, esta perspectiva puede resultar especialmente útil para articular hipótesis sobre acumulación, distribución o productividad sin depender de supuestos fuertes sobre convergencia. En ese sentido, más que ofrecer respuestas cerradas, abre un espacio de análisis donde la teoría, la historia, y la econometría pueden dialogar en tierra fertil. 
