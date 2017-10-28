#PEC1 - Minería de datos

##Pregunta 1:

*Haz un esquema y describe cómo se agrupan, en función del objetivo del proyecto, las diferentes técnicas de minería de datos.*

Existen varias agrupaciones de las técnicas de minería de datos. Atendiendo al tipo de información que se posea y, por tanto, el conocimiento que se quiera extraer una clasificación habitual es en modelos supervisados y no supervisados. 

Los modelos supervisados tienen como objetivo, dada una variable dependiente (*target*) conseguir una relación entre esta y un número P de variables dependientes (*factors*). Estas relaciones se componen mediante la estimación de reglas o parámetros minimizando alguna medida de error entre el valor que prediciría el modelo y el valor real de la variable dependiente. 

En función al tipo de relaciones podemos subdividir este grupo entre lineales o no lineales. Los modelos que componen estas relaciones pueden ser paramétricos, o no paramétricos en función de si el resultado del modelo es una serie de parámetros que componen una fórmula o si se trata de 'reglas' entre el *target* y los *factors* que permiten extraer el conocimiento o predicción. Dentro de este paragüas se encuentran modelos clásicos de minería de datos como el naive bayes, regresiones, árboles de decisión, etc.

Atendiendo al tipo de variable dependiente podemos clasificar las técnicas entre técnicas de clasificación (variable dependiente discreta y finita) y de regresión (variable dependiente contínua).

Los modelos no supervisados ante la ausencia de una variable dependiente u objetivo, pretenden extraer información sobre la estructura interna del problema. Estos modelos se entrenan, normalmente, minimizando alguna medida de 'distancia'.

En la literatura proporcionada se proporciona una agrupación más funcional atendiendo a la finalidad del proyecto. A continuación se muestra un esquema que pretende agrupar las técnicas en cada uno de los bloques proporcionados:

![alt text](./entregas/esquema_tipos_md.png)

Como se ve en la imagen tenemos cinco grupos de técnicas en función al objetivo: agrupar, clasificar, describir, explicar y predecir. 

La primera de ellas **agrupar** tiene como objetivo encontrar elementos similares dentro de un conjunto de datos. Dentro de esta técnica, encontramos el *clustering* que también podíamos encontrar en la clasificación de modelo no supervisado, por que, de nuevo, pretende encontrar una estructura dentro edl conjunto de datos. 

El *clustering*, junto con el análisis factorial y las redes bayesianas tienen la capacidad de realizar funciones de otro de los grupos propuestos: describir. Estas técnicas permiten encontrar asociaciones causales entre las variables. El clustering ofrece una primera aproximación mientras que las redes permiten encontrar esas relaciones subyacentes.

Otro gran bloque de técnicas la componen las técnicas de clasificación que pertenecían a los modelos supervisados, donde se pretende dado un conjunto de variables o atributos ser capaz de encontrar relaciones que permitan 'etiquetar' o clasificar un nuevo registro dentro de unos grupos existentes y definidos. 

La relación entre este bloque de técnicas y el bloque de 'predecir', es importante dentro de la minería de datos ya que la aplicabilidad de muchos de los modelos de clasificación es ser capaz de predecir a qué categoría pertenece un nuevo individuo o registro. Dentro de estos dos bloques caben destacar técnicas como las redes neuronales, los árboles de decisión o los algoritmos de gradient boosting. 

Dentro de este bloque de técnicas de predición hemos separado la capacidad del gradient bosting de predecir de la capacidad de los árboles. Esto se debe a que en la práctica se demuestran técnicas más precisas. Las redes neuronales, cuando se trabajan y se convinan con técnicas de convolución o recurrencia son capaces de tener una capacidad predictiva aún mayor, sobre todo, para el reconomiento de patrones o imágenes.

Un último bloque de técnicas que hemos situado en la intersección entre las agrupaciones de **clasificar**, **predecir** y **explicar** lo componen los modelos lineales y los árboles de decisión. Si bien estas técnicas poseen la capacidad de realizar predicciones buenas, una característica que los diferencia del resto es la capacidad de aportar respuestas a preguntas como '¿por qué esta política no ha funcionado en este conjunto?' o reformulando : '¿qué variable y en que medida ha propiciado el fallo de una acción sobre mi conjunto?'. Con modelos lineales nos referimos a técnicas como regresión logística que permite clasificar, regresiones lineales, modelos mixtos, etc.

## Pregunta 2:

*Propón un posible proyecto de Minería de Datos que se corresponda con tu área de actividad profesional o cualquier otra actividad que conozcas o te resulte interesante. A continuación: desarrolla un esquema del proyecto completo que indique cuáles y cómo serían las diferentes fases existentes en el ciclo de vida de este proyecto de minería de datos. ¿Cuál sería el producto de cada fase? Explica las relaciones que habría entre todas ellas y sus peculiaridades. No es necesario entrar en el detalle de las fases. Solamente el objetivo y el producto*

El proyecto propuesto sería dada la información histórica relativa al rendimiento de un programa de ayuda de carácter social, económico, psicológico y cultural a jóvenes entre 8-16 años, encontrar:

* variables significativas en el resultado del programa: **modelo descriptivo - explicativo**
* puntos de acción (variables accionables): **análisis causa raíz y explicatividad para variables accionables**
* grupos de acción (grupos sociales, grupos geográficos): **agrupación y cluster de participantes del programa, así como de los núcleos familiares a los que pertenecen**. **Análisis geo-espacial de los resultados del programa**
* evolución del rendimiento del programa: **análisis de series temporales**
* probabilidad de resultado del año siguiente con los nuevos candidatos al programa (algunos serían recurrentes): **modelos de previsión del rendimiento o de fuga del programa**.

El primer paso del proyecto, asumiento los objetivos arriba enunciados sería encontrar las fuentes de información. En este caso, los datos de rendimiento del programa, así como la ficha personal de cada candidato con la información socio-económica y de los centros donde se ha realizado el programa. El producto resultante sería un mapa de las fuentes.

El segundo sería la preparación de los *datasets* necesarios para la explotación de los resultados. El objetivo sería agrupar las fuentes para generar uno o varios tablones donde se contenga la información agregada o consolidada. 

La tercera fase sería realizar la limpieza de los datos. Al tratarse de datos manualmente recopilados, será necesario estandarizar la información, imputar o eliminar información faltante, etc. El resultado de esta fase serán los tablones de la fase dos, listos para ser explotados.

La cuarta fase la compondrá el proceso de creación de variables sintéticas o de conversión de variables. Al final de esta fase se tendrán los tablones que se emplearan en los modelos.

La quinta fase será la construcción de los distintos modelos. Tras varias iteracciones se generaran varios modelos entrenados para generar las salidas requeridas para cada objetivo.

La sexta fase tendrá como objetivo evaluar los modelos. El resultado serán un listado de informes con las salidas de los modelos validadas o el conocimiento generado listo para ser explotado.

En la séptima fase los resultados de los modelos servirán para la toma de decisiones de cara al programa del año próximo.

La última fase la compone la revisión de los resultados una vez concluya la campaña próxima para redefinir objetivos, recalibrar modelos y evaluar su impacto.


