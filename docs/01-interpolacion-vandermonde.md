# Interpolación polinómica mediante matriz de Vandermonde

Original: `Untitled6.ipynb`. Archivo conservado: [01-interpolacion-vandermonde.ipynb](../notebooks/01-interpolacion-vandermonde.ipynb).

## Contenido

- 0: solicita pares x,y mediante input hasta recibir una cadena vacía; construye potencias crecientes de cada x, resuelve con numpy.linalg.solve, evalúa polinomy en enteros de 1 a 7 y grafica.

## Evidencias en el source

- La matriz mx contiene [1,x,x^2,...] y el vector my contiene los valores y, lo que identifica una Vandermonde.
- La única función es polinomy; no hay celdas Markdown.

## Variantes y duplicados

Una única celda no vacía; sin coincidencia exacta de celda o función con los otros cuadernos comparados.

## Limitaciones históricas

- No valida puntos repetidos, entrada vacía inicial o un sistema singular.
- Se evalúa el polinomio en x=1,...,7, pero plt.plot(equis) dibuja contra índices 0,...,6; el eje horizontal no representa los x usados.
- La cuadrícula de visualización está fija y puede quedar fuera del intervalo de los datos introducidos.

## Procedencia

El usuario confirmó que estos cuadernos corresponden a trabajos académicos suyos. Se preserva el original, incluidas sus variantes, sin atribuir novedad a los métodos clásicos o a las bibliotecas utilizadas. Los índices de celda parten de cero.

La revisión leyó íntegramente código, comentarios y Markdown sin ejecutar las celdas. Los resultados guardados son históricos.
