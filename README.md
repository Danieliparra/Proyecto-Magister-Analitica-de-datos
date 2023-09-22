# Proyecto Magister: Analítica de datos

### Objetivo
Realizar un análisis exploratorio de datos y crear un modelo de aprendizaje automático para la predicción de readmisión hospitalaria.


------------

### Descripción
Este proyecto se llevó a cabo como parte de la evaluación final de la asignatura de Análisis de Datos. En este curso, los estudiantes tenían la opción de seleccionar un proyecto de una lista de opciones proporcionadas. En nuestro caso, decidimos abordar un problema relacionado con técnicas de clustering

**Predicción de reingreso hospitalario:** Un reingreso hospitalario es un episodio cuando un paciente que había sido dado de alta de un hospital es admitido de nuevo dentro de un intervalo de tiempo especificado. Las tasas de readmisión se han utilizado cada vez más como medida de resultado en la investigación de servicios de salud y como referencia de calidad para los sistemas de salud. La idea de este proyecto es predecir si un paciente con diabetes va a ser readmitido a un hospital en función de 127 atributos (edad, sexo, tiempo en el hospital, medicamentos, etc.)

------------


### Conclusiones
- Se aplicaron diversas técnicas para mitigar el desequilibrio en nuestro conjunto de datos, y los resultados más prometedores se obtuvieron mediante el método de sobremuestreo (oversampling). Esto se debe a que al aumentar la cantidad de muestras, creamos una población de datos más amplia y diversa, lo que permite al modelo aprender de una gama más amplia de relaciones entre los atributos.

- En cuanto a los resultados de los modelos para las tres etiquetas de readmisión, se observó que los algoritmos que seleccionan en función de la pureza de los conjuntos, como Random Forest o Decision Tree, presentan un mejor rendimiento en comparación con los algoritmos basados en medidas de distancia. Por otro lado, los algoritmos avanzados basados en boosting no obtuvieron un buen desempeño. Sin embargo, al no contar con un conocimiento profundo de ellos, se evaluarán sus parámetros con mayor detalle en una futura ocasión

- Finalmente se destaca que el enfoque binario  arrojó resultados superiores al enfoque multiclase en los datos originales. En consecuencia, podemos concluir que existen dos categorías que son similares o difíciles de distinguir. Según los resultados obtenidos, es posible diferenciar satisfactoriamente la categoría de "reingreso <30 días" de las demás clases. Por otro lado, no logramos el mismo nivel de desempeño al intentar separar las categorías de "reingreso >30 días" y "no reingreso".

<p align="center">
**Matriz de confusión del mejor enfoque: binario y oversampling**
![Matriz de confusión del mejor enfoque: binario y oversampling](https://i.ibb.co/X8N5B6M/Matriz-de-confusi-n.png "Matriz de confusión del mejor enfoque: binario y oversampling")
</p>

------------


###Implementación
Todo el código utilizado para generar los resultados y las figuras en el artículo se encuentra en el archivo "Diabetes hospital.ipynb". Los cálculos y la generación de las figuras se ejecutan dentro del cuaderno Jupyter. Los datos utilizados en este estudio se proporcionan en la carpeta "dataset_diabetes". Además, en la carpeta "Documentación" se encuentra información complementacia al problema.

------------


###Dependencias
Necesitarás un entorno de Python funcional para ejecutar el código. La forma recomendada de configurar tu entorno es a través de la distribución de Python Anaconda, que proporciona el gestor de paquetes conda. Anaconda se puede instalar en tu directorio de usuario y no interfiere con la instalación de Python del sistema

Las librerias utilizadas son:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

-----------


###Licencias
Puedes utilizar y modificar libremente el código, siempre y cuando proporciones atribución a los autores
