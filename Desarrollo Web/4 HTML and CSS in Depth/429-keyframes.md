# Fotogramas clave CSS
#front-end #curso-4 #modulo-2 

---
Los fotogramas clave se definen como `@keyframes` en el código CSS. Los `@keyframes` forman parte de la secuencia de animación y ayudan a definir los pasos dentro de ella. Imagine un objeto en su página web moviéndose del punto A al punto B. Puede utilizar las propiedades de transición y transformación para hacerlo, pero las secuencias de animación se utilizan para lograr comportamientos más complejos de una forma más sencilla.

## Palabras clase `from` y `to` y uso de los porcentajes `%`
```css
@keyframes animation-name {
	from {
		property-a: value-a;
	}
	to {
		property-a: value-b;
	}
}
```
Las palabras clave `from` y `to` se utilizan dentro de la regla `@keyframes` para marcar la transición de una o varias propiedades y pueden verse como los puntos inicial y final de dicha transición. Para ampliar el uso de `from` y `to`, los `@keyframes` le permiten añadir más pasos a su animación mediante el uso de un porcentaje que representa la finalización de la animación.
```css
@keyframes identifier {
	0% {transform: rotate(100deg);}
	30% {opacity: 1;}
	50% {opacity: 0.50;}
	70% {opacity: 1;}
	100% {transform: rotate(50deg);
}
```
Los `@keyframes` van unidos al nombre de la animación a la que se van a aplicar. Para dar una visión general de la propiedad `animation`, ésta consta de otras subpropiedades. De ellas, `animation-name` y `animation-duration` deben definirse, mientras que pueden añadirse otras como `timing-function`, `delay`, `direction`, `fill-mode`, `iteration-count`, etc.

Abreviatura de la propiedad de animación:

La abreviatura de la propiedad de animación consiste en las siguientes propiedades con sus valores por defecto:
- animation-name: none 
- animation-duration: 0s 
- animation-timing-function: ease 
- animation-delay: 0s 
- animation-iteration-count: 1 
- animation-direction: normal 
- animation-fill-mode: none 
- animation-play-state: running 
- animation-timeline: auto