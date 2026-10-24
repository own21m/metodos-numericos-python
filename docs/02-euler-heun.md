# Comparación de Euler y Heun para una EDO escalar

Original: `eulerMN.ipynb`. Archivo conservado: [02-euler-heun.ipynb](../notebooks/02-euler-heun.ipynb).

## Contenido

- 0: define f(y,t)=y*sin(t)^3, Euler explícito, Heun y una referencia exponencial; usa y0=1, tf=20, h=0.1. Grafica e imprime los vectores.
- 1: repite los cuatro métodos/funciones, agrega import math y cambia y0 a 0.5; mantiene tf=20 y modifica estilos de gráfica.
- 2: repite las funciones de la celda 1, reduce tf a 5 y mantiene y0=0.5.

## Evidencias en el source

- Funciones euler, heun, fanalitic y f presentes en las tres celdas; NumPy y Matplotlib son las dependencias externas.
- No hay Markdown ni declaración de autor en el source.

## Variantes y duplicados

Las tres celdas no son exactamente iguales, pero f, euler, heun y fanalitic tienen AST idéntico en las tres. Son variantes del mismo ejercicio; no tres proyectos.

## Limitaciones históricas

- La referencia exp(-cos(t)+cos(t)^3/3) no incorpora la constante necesaria para satisfacer y(0)=1 o y(0)=0.5. La solución con condición y0 es y0*exp(-cos(t)+cos(t)^3/3+2/3).
- La primera celda usa math sin importarlo allí; depende de estado previo si se ejecuta en aislamiento.
- Euler/Heun devuelven el punto inicial más los pasos (201 o 51 muestras), mientras la referencia usa 200 o 50 muestras. Las gráficas usan índices implícitos en lugar del mismo vector temporal.

## Procedencia

El usuario confirmó que estos cuadernos corresponden a trabajos académicos suyos. Se preserva el original, incluidas sus variantes, sin atribuir novedad a los métodos clásicos o a las bibliotecas utilizadas. Los índices de celda parten de cero.

La revisión leyó íntegramente código, comentarios y Markdown sin ejecutar las celdas. Los resultados guardados son históricos.
