# Métodos numéricos con Python

Colección de trabajos académicos de interpolación y solución aproximada de ecuaciones diferenciales. Reúne implementaciones con NumPy, SciPy y Matplotlib: interpolación polinómica por Vandermonde, integración con Euler y Heun, colocación con funciones de base radial y diferencias finitas para problemas de contorno.

Los cuadernos se conservan como archivo histórico de aprendizaje: contienen variantes de un mismo ejercicio, gráficos y salidas originales. El usuario confirmó su procedencia como trabajos académicos propios. La numeración organiza la lectura por tema y no establece una cronología de desarrollo.

## Cuadernos

| Archivo | Contenido | Nombre de origen |
| --- | --- | --- |
| [01-interpolacion-vandermonde.ipynb](notebooks/01-interpolacion-vandermonde.ipynb) | Interpolación polinómica mediante matriz de Vandermonde | `Untitled6.ipynb` |
| [02-euler-heun.ipynb](notebooks/02-euler-heun.ipynb) | Comparación de Euler y Heun para una EDO escalar | `eulerMN.ipynb` |
| [03-rbf-ensayos.ipynb](notebooks/03-rbf-ensayos.ipynb) | Tres ensayos de aproximación/interpolación RBF | `Untitled7.ipynb` |
| [04-rbf-cubica-frontera.ipynb](notebooks/04-rbf-cubica-frontera.ipynb) | Colocación con RBF cúbica para y''=0 y condiciones de Dirichlet | `Untitled8.ipynb` |
| [05-diferencias-finitas-borradores.ipynb](notebooks/05-diferencias-finitas-borradores.ipynb) | Borradores de diferencias finitas para problemas de contorno unidimensionales | `Untitled9.ipynb` |

## Tecnologías

- Python en cuadernos Jupyter/Google Colab.
- NumPy para matrices, vectores, kernels y solución de sistemas lineales.
- SciPy para la solución de sistemas en los experimentos de diferencias finitas.
- Matplotlib para comparar aproximaciones, referencias y errores.

[requirements.txt](requirements.txt) enumera las importaciones observadas. No fija versiones ni representa un entorno reproducido durante esta recuperación.

## Qué se estudia

La interpolación de Vandermonde obtiene los coeficientes de un polinomio a partir de puntos. Euler y Heun aproximan una EDO escalar mediante pasos temporales. Los experimentos RBF construyen aproximaciones con kernels gaussianos o cúbicos. Los borradores de diferencias finitas ensamblan operadores tridiagonales y exploran condiciones en los extremos de un intervalo.

Los métodos y las implementaciones se presentan con su alcance original. Las fichas de [docs/](docs/) explican las celdas, las variantes y los problemas observables en el código.

## Cómo retomarlos

Cada `.ipynb` se puede leer en GitHub o abrir en Jupyter/Google Colab. Para una nueva ejecución hacen falta las bibliotecas de `requirements.txt`. El ejemplo de interpolación pide puntos mediante `input`; los demás contienen parámetros definidos en sus celdas.

Conviene trabajar sobre copias y revisar las fichas antes de ejecutar. Algunos resultados dependen del orden de las celdas o de variables dejadas por intentos anteriores. No se ejecutó ningún cuaderno durante la recuperación.

## Estado de los ejercicios

- Euler/Heun: la referencia exponencial no incorpora la constante de la condición inicial usada. Las series comparadas tienen distinto número de muestras.
- Interpolación: no se validan puntos repetidos y la gráfica usa índices implícitos en lugar de los x evaluados.
- Ensayos RBF: hay coeficientes triviales o fijados a uno, sin resolver por completo el problema anunciado.
- RBF cúbica: una variante calcula RMS antes de rellenar la referencia y la reformulación grafica variables de la celda anterior.
- Diferencias finitas: hay referencias que no satisfacen la EDO de la variante y condiciones de frontera mezcladas. Una celda se repite exactamente.

Estas observaciones documentan el estado histórico; no se reemplazó el código por una versión corregida ni se anunciaron resultados nuevos como verificados.

## Conservación y procedencia

[docs/ORIGEN.md](docs/ORIGEN.md) identifica los originales, sus IDs y la confirmación del usuario. [origen/verificacion.json](origen/verificacion.json) registra tamaños, hashes, conteos de celdas/salidas y validación de sintaxis sin ejecutar código.

Los notebooks publicados conservan exactamente los bytes de sus archivos originales descargados. Se mantienen comentarios, variantes, metadatos y salidas; el código no se reescribió ni minificó. No se añade una licencia de redistribución que no figuraba en esos materiales.

La IA se utilizó como herramienta de aceleración de procesos para la organización y documentación del repositorio.
