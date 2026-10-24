# Borradores de diferencias finitas para problemas de contorno unidimensionales

Original: `Untitled9.ipynb`. Archivo conservado: [05-diferencias-finitas-borradores.ipynb](../notebooks/05-diferencias-finitas-borradores.ipynb).

## Contenido

- 0: ensambla una matriz tridiagonal con D=1, U=k=0, N=10 y valores extremos 0 y 1; resuelve y muestra valores.
- 1: repite el esquema y añade referencia x^2, errores y dos gráficas.
- 2: repite casi íntegramente c1; las diferencias de espacios/saltos no cambian la idea.
- 3: celda vacía.
- 4: intenta un extremo de tipo derivada, añade un término D*Yb/h y compara con una recta de referencia; usa errors sin recalcularlo.
- 5: variante de c4 cuyo comentario del cálculo de errores cambia; el cálculo sigue desactivado.
- 6: celda vacía.
- 7: duplicado textual exacto de c4.
- 8: incorpora Uc=2, kc=0.5 y forzamiento sin(2x); modifica ab y añade una fórmula analítica sin dependencia de Uc.
- 9: regresa a coeficientes nulos de transporte/reacción y cambia escalado/signos de frontera; vuelve a usar x^2 como referencia y produce gráficas.

## Evidencias en el source

- Los coeficientes de la matriz corresponden al patrón D*y''+U*y'-k*y=f; se usa scipy.linalg.solve.
- c4/c5/c7 comentan y'(xb)=Yb, mientras las construcciones posteriores añaden Yb directamente como valor final de y.

## Variantes y duplicados

Duplicado exacto no vacío c4=c7. c1/c2 son casi duplicadas y c4/c5/c7 son variantes de la misma tentativa. analytical_solution(x)=x^2 tiene AST idéntico en c1,c2,c9. Celdas vacías c3,c6.

## Limitaciones históricas

- Con D=1, U=k=0 y extremos 0,1, la solución de y''=0 es lineal; x^2 no es una referencia válida para ese mismo problema.
- Los intentos de condición de derivada no modifican de forma coherente la fila final del sistema y mezclan derivada con valor de y en el extremo.
- En c4/c5/c7 la línea que recalcula errors está comentada, pero se grafica errors de una ejecución anterior o se produciría un nombre no definido en aislamiento.
- La referencia de c8 no incorpora Uc aunque el operador sí lo hace. No está justificada como solución del problema que se discretiza.
- c9 mezcla términos de frontera con /h y ensamblaje con /h^2; no documenta un problema matemático consistente que permita validar esa modificación.

## Procedencia

El usuario confirmó que estos cuadernos corresponden a trabajos académicos suyos. Se preserva el original, incluidas sus variantes, sin atribuir novedad a los métodos clásicos o a las bibliotecas utilizadas. Los índices de celda parten de cero.

La revisión leyó íntegramente código, comentarios y Markdown sin ejecutar las celdas. Los resultados guardados son históricos.
