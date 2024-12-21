#front-end #curso-4 #modulo-2 

---
## Propiedad `transform`
### Ejemplo
```css
.sample-class {
	transform: rotate(60deg);
}
```
### Transformación múltiple sobre el mismo elemento
Se pueden aplicar transformaciones para rotate(), scale() y translate() que se pueden enumerar juntas. Cada una de estas propiedades puede tener sus propios valores y las acciones darán un efecto combinado.
```css
.sample-class {
	transform: rotate(45deg) scale(1.5) translate(45px);
}
```

---
## Propiedad `transition`
La abreviatura de `transition` tiene cuatro subpropiedades siguientes, cada una de las cuales puede definirse también individualmente.
- transition-property
- transition-duration
- transition-timing-function
- transition-delay
### Sintaxis
`transition: property duration timing-function delay;`
### Ejemplo 
`transition: margin-left2s ease-in-out 0.5s;`

---
## Animationes
### Sintaxis
`animation: _name duration timing-function delay iteration-count direction fill-mode play-state;`
### Ejemplo
```css
.sample-class {
	animation: none 2 ease 0.5 4 normal none running;
}
```
La propiedad animation es una abreviatura de las siguientes subpropiedades:
- `animation-name`
- `animation-duration`
- `animation-timing-function`
- `animation-delay`
- `animation-iteration-count`
- `animation-direction`
- `animation-fill-mode`
- `animation-play-state`

---
## `@keyframes`
### Sintaxis
```css
@keyframes mymove {
  from {property: value}
  to { property: value }
}
```
### Ejemplo
```css
@keyframes animation-name {
	from {bottom: 0px;}
	to {bottom: 100px;}
}
@keyframes animation-name {
	0%,100%{
		background-color: blue;
	}
	50% {
		background-color: green;
	}
}
```
## Animaciones múltiples
Funciona igual que la animación regular, se pueden establecer múltiples reglas.
```css
#some-class{
	animation: animation-a 2s linear infinite alternate, 
	animation-b 3s ease infinite alternate;
}
```
