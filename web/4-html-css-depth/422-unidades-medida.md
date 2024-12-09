# Unidades de medida CSS
#front-end #curso-4 #modulo-2 

---
Una propiedad de una página web es su **tamaño**, que puede ser estático o dinámico. Cuando se haya encontrado con suficiente código CSS, observará una serie de formas diferentes en las que los valores de una misma propiedad pueden declararse utilizando distintas unidades de medida. La mayoría de estas unidades de medida se utilizan para tener en cuenta el dinamismo y la dimensionalidad de una página web.

Examinemos las unidades de medida más utilizadas. A grandes rasgos, pueden clasificarse en unidades **absolutas** y **relativas**.
## Unidades absolutas
Las unidades absolutas son constantes en diferentes dispositivos y tienen un **tamaño fijo**. ==No son tan adecuadas cuando se trata de la gran variedad de dispositivos que se utilizan hoy en día y que tienen diferentes tamaños de ventana gráfica==. Por ello, las unidades absolutas se utilizan cuando el tamaño de la página web es conocido y permanecerá constante.

| Unidad | Nombre              | Comparación              |
| ------ | ------------------- | ------------------------ |
| Q      | Cuarto de milímetro | Q = 1/40 de 1cm          |
| mm     | Milímetros          | mm = 1/10 de 1cm         |
| cm     | Centímetros         | 1cm = 37,8px = 25,2/64in |
| en     | Pulgadas            | 1in = 2,54cm = 96px      |
| pc     | Picas               | 1pc = 1/6 de 1in         |
| pt     | Puntos              | 1pt = 1/72 de 1 pulgada  |
| px     | Pixeles             | 1px = 1/96 de 1 pulgada  |
## Valores relativos
Cuando cree una página web, casi nunca tendrá un único elemento presente en su interior. Incluso en el caso de contenedores como flexboxes y rejillas, suele haber más de un elemento presente al que se aplican reglas. Los valores relativos se definen 'en relación' a los otros elementos presentes dentro del elemento padre. Además, ==se definen 'en relación' con la ventana gráfica o el tamaño de la página web visible==. Dada la naturaleza dinámica de las páginas web en la actualidad y el tamaño variable de los dispositivos en uso, ==las unidades relativas son la opción más adecuada en muchos casos==. A continuación encontrará una lista de algunas de las unidades relativas más importantes.

| Unidad | Descripción y relatividad                                                  |
| ------ | -------------------------------------------------------------------------- |
| `em`   | Tamaño de fuente del padre, cuando exista.                                 |
| `ex`   | Coordenada x o altura del elemento de fuente.                              |
| `ch`   | Anchura del carácter de fuente.                                            |
| `rem`  | Tamaño de fuente del elemento raíz.                                        |
| `lh`   | Valor calculado para la altura de línea del elemento padre.                |
| `rlh`  | Valor calculado para la altura de línea del elemento raíz que es `<html>`. |
| `vw`   | 1% de la anchura de la ventana gráfica.                                    |
| `vh`   | 1% de la altura de la ventana gráfica.                                     |
| `vmin` | 1% de la dimensión menor de la ventana gráfica.                            |
| `vmax` | 1% de la dimensión mayor de la ventana gráfica.                            |
| `%`    | Denota un valor porcentual en relación con su elemento padre.              |
Muchas de estas unidades se utilizan en función del tamaño relativo de las fuentes. Algunas unidades son más adecuadas en función del contexto relativo. Por ejemplo, cuando las dimensiones de la ventana gráfica son importantes, es más apropiado utilizar vw y vh. En un contexto más amplio, las unidades relativas que verá utilizar con más frecuencia son el porcentaje, `em`, `vh`, `vw` y `rem`.