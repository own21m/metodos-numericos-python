# Tres ensayos de aproximación/interpolación RBF

Original: `Untitled7.ipynb`. Archivo conservado: [03-rbf-ensayos.ipynb](../notebooks/03-rbf-ensayos.ipynb).

## Contenido

- 0: arma una matriz de kernel gaussiano exp(-epsilon*r^2) para 20 puntos; el vector f_values es completamente cero; resuelve coeficientes y grafica la interpolación.
- 1: define f=sin(x), phi=(x^2+c)^n y solve; fija cinco coeficientes en uno sin ajustarlos; produce una aproximación escalar en x=1 y la compara con sin(1).
- 2: pasa a 1000 puntos y n=2, pero mantiene coeficientes unos y suma productos phi(x)*phi(x_i); compara esa curva con sin(x).

## Evidencias en el source

- Las funciones rbf_gaussian e interpolate_solution en c0, y phi/solve en c1-c2, identifican el tema.
- No se impone un operador diferencial ni condiciones de contorno explícitas en las ecuaciones de la primera celda.

## Variantes y duplicados

f y phi tienen AST idéntico en c1 y c2. Las tres celdas completas son diferentes. No hay duplicados exactos con Untitled8 ni EM/gravedad.

## Limitaciones históricas

- Con lado derecho cero, c0 busca una interpolación trivial; el título del gráfico menciona frontera, pero el código no impone el problema anunciado.
- En c1 y c2 los coeficientes se asignan a uno: no se resuelve un sistema para aproximar sin(x). La función f definida no se usa en el ajuste.
- La tercera celda usa productos de bases, no una suma de kernels centrados en x_i evaluados por distancia como la primera celda.

## Procedencia

El usuario confirmó que estos cuadernos corresponden a trabajos académicos suyos. Se preserva el original, incluidas sus variantes, sin atribuir novedad a los métodos clásicos o a las bibliotecas utilizadas. Los índices de celda parten de cero.

La revisión leyó íntegramente código, comentarios y Markdown sin ejecutar las celdas. Los resultados guardados son históricos.
