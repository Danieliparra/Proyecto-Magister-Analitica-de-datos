# Proyecto Magister: Analítica de datos
by Daniel Parra, Mario Montorfano y Ronald Verdugo

## Objetivo
El objetivo principal de este proyecto es llevar a cabo un análisis exploratorio de datos y desarrollar un modelo de aprendizaje automático para predecir la readmisión hospitalaria.

## Descripción
Este proyecto se llevó a cabo como parte de la evaluación final de la asignatura de Análisis de Datos. Los estudiantes tenían la opción de elegir un proyecto de una lista de opciones proporcionadas. En este caso, decidimos abordar un problema relacionado con técnicas de clustering.

**Predicción de Readmisión Hospitalaria:** La readmisión hospitalaria ocurre cuando un paciente que había sido dado de alta de un hospital es admitido nuevamente dentro de un intervalo de tiempo especificado. Las tasas de readmisión se utilizan cada vez más como una medida de resultado en la investigación de servicios de salud y como referencia de calidad para los sistemas de salud. En este proyecto, se busca predecir si un paciente con diabetes será readmitido en un hospital en función de 127 atributos, que incluyen edad, sexo, tiempo en el hospital, medicamentos, entre otros.

## Conclusiones
- Se aplicaron diversas técnicas para abordar el desequilibrio en el conjunto de datos, y los resultados más prometedores se obtuvieron mediante el método de sobremuestreo (oversampling). Al aumentar la cantidad de muestras, creamos una población de datos más amplia y diversa, lo que permite que el modelo aprenda de una gama más amplia de relaciones entre los atributos.

- En relación con los resultados de los modelos para las tres etiquetas de readmisión, se observó que los algoritmos que seleccionan en función de la pureza de los conjuntos, como Random Forest o Decision Tree, presentan un mejor rendimiento en comparación con los algoritmos basados en medidas de distancia. Por otro lado, los algoritmos avanzados basados en boosting no obtuvieron un buen desempeño. Sin embargo, se planea explorar con más detalle sus parámetros en el futuro.

- Se destacó que el enfoque binario produjo resultados superiores al enfoque multiclase en los datos originales. En consecuencia, podemos concluir que existen dos categorías que son similares o difíciles de distinguir. Según los resultados, es posible diferenciar satisfactoriamente la categoría de "reingreso en <30 días" de las demás clases. Sin embargo, no se logró el mismo nivel de desempeño al intentar separar las categorías de "reingreso en >30 días" y "no reingreso".

![Matriz de confusión del mejor enfoque: binario y oversampling](https://i.ibb.co/X8N5B6M/Matriz-de-confusi-n.png)

## Implementación
Todo el código utilizado para generar los resultados y las figuras en el artículo se encuentra en el archivo "Diabetes hospital.ipynb". Los cálculos y la generación de las figuras se ejecutan dentro del cuaderno Jupyter. Los datos utilizados en este estudio se proporcionan en la carpeta "dataset_diabetes". Además, en la carpeta "Documentación" se encuentra información complementaria sobre el problema.

## Dependencias
Para ejecutar el código, necesitarás un entorno de Python funcional. Se recomienda configurar tu entorno utilizando la distribución de Python Anaconda, que incluye el gestor de paquetes conda. Anaconda se puede instalar en tu directorio de usuario sin interferir con la instalación de Python del sistema.

Las bibliotecas utilizadas en este proyecto son:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Licencia
Puedes utilizar y modificar libremente el código, siempre y cuando proporciones atribución a los autores.

¡Gracias por leer nuestro README! Si tienes alguna pregunta o comentario, no dudes en contactarnos.
