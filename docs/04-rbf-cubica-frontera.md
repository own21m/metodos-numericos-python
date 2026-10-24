# Colocación con RBF cúbica para y''=0 y condiciones de Dirichlet

Original: `Untitled8.ipynb`. Archivo conservado: [04-rbf-cubica-frontera.ipynb](../notebooks/04-rbf-cubica-frontera.ipynb).

## Contenido

- 0: usa 30 nodos en [-3,1], kernel |x-x_j|^3, primera y segunda derivadas; impone y(-3)=1, y(1)=3 y y''=0 dentro; resuelve coeficientes, compara con recta exacta y grafica.
- 1: reformula el mismo problema con nombres F, F_ddx, alphas, constants, numeric_sol y exact_sol; contiene una descripción que lo llama elementos finitos y vuelve a graficar con nombres de la celda anterior.

## Evidencias en el source

- Funciones fbr/dfbr/d2fbr y f/df/d2f; las filas interiores contienen la segunda derivada del kernel y las filas extremas el kernel.
- La solución exacta definida es la recta que interpola las dos condiciones de Dirichlet.

## Variantes y duplicados

Dos implementaciones del mismo ejercicio, con nombres y estructura cambiados; no son celdas o funciones AST exactamente iguales. Conviene tratarlas como variantes, no como proyectos separados.

## Limitaciones históricas

- En c0 ErrorRMS se calcula antes de llenar vsolexac, por lo que compara contra un vector de ceros, no contra la solución exacta.
- En c1 se calculan numeric_sol y exact_sol, pero las gráficas usan x, vsolnum y vsolexac de c0. En una sesión limpia esos nombres no existen; después de c0 muestran datos anteriores.
- La descripción de c1 dice elementos finitos, pero el código implementa colocación global por RBF, sin ensamblaje de elementos finitos.
- esppun se define usando L/(numpun-1), aunque el intervalo tiene longitud L-xa; esa variable no se usa después.

## Procedencia

El usuario confirmó que estos cuadernos corresponden a trabajos académicos suyos. Se preserva el original, incluidas sus variantes, sin atribuir novedad a los métodos clásicos o a las bibliotecas utilizadas. Los índices de celda parten de cero.

La revisión leyó íntegramente código, comentarios y Markdown sin ejecutar las celdas. Los resultados guardados son históricos.
