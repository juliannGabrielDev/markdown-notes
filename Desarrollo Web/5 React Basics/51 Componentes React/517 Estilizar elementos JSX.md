---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
Habrá observado que JSX es increíblemente versátil y puede aceptar una combinación de JavaScript, HTML y CSS. En esta lectura, aprenderá algunos enfoques para estilizar elementos JSX y hacerlo de forma que se consiga un aspecto tanto funcional como visual dentro de una aplicación.

Existen varias formas de estilizar elementos JSX.

Probablemente la forma más sencilla de hacerlo es utilizando el elemento HTML link en la cabecera del archivo **index.html** en el que se montará su aplicación React.

El atributo `href` carga algunos estilos CSS, probablemente con algunas clases CSS, y luego, dentro de las declaraciones del componente de la función, puede acceder a esas clases CSS utilizando el atributo `className`.

```jsx
function Promo(props) {
    return (
        <div className="promo-section">
            <div>
                <h1>{props.heading}</h1>
            </div>
            <div>
                <h2>{props.promoSubHeading}</h2>
            </div>
        </div>
    );
}
```

En CSS:

```css
.promo-section {
    font-weight: bold;
    line-height: 20px;
}
```

Otra forma de añadir estilos CSS a los componentes es utilizando estilos en línea.

La sintaxis de los estilos en línea en JSX es un poco personalizada.

Considere un componente inicial `Promo` , que contiene el código que encontró anteriormente, ahora puede añadirle algunos estilos en línea:

```jsx
function Promo(props) {
    return (
        <div className="promo-section">
            <div>
                <h1 style={{color:"tomato", fontSize:"40px", fontWeight:"bold"}}>
                    {props.heading}
                </h1>
            </div>
            <div>
                <h2>{props.promoSubHeading}</h2>
            </div>
        </div>
    );
}

export default Promo;
```

Puede empezar a actualizar el componente `Promo` añadiendo la sintaxis de expresión JavaScript:

```jsx
<h1 style={}>
```

Como se explicó anteriormente, esto significa que cualquier código que añada dentro de estas llaves de apertura y cierre será analizado como JavaScript regular. Ahora vamos a añadir un **literal de objeto de estilo** dentro de estas llaves:

```jsx
<h1 style={{color:"tomato",fontSize:"40px"}}>
```

A continuación, puede reescribir este literal de objeto:

```jsx
{
    color: "tomato",
    fontSize: "40px"
}
```

Por lo tanto, no hay nada especial en este objeto, excepto el hecho de que lo ha alineado y colocado dentro de un par de llaves. Además, dado que se trata sólo de JavaScript, las propiedades CSS que en CSS plano estarían entrecomilladas, como, por ejemplo, `font-size:40px`, pasan a estar entrecomilladas, y el valor es una cadena, por lo que su aspecto es el siguiente: `fontSize:"40px"`.

Además de *inlining* un literal de objeto de _estilo_, también puede guardarlo en una variable, y luego utilizar esa variable en lugar de pasar un literal de objeto.

Así obtendrá un componente `Promo` actualizado, con el objeto de estilos guardado como una variable JavaScript:

```jsx
function Promo(props) {

const styles = {
    color: "tomato",
    fontSize: "40px"
}

return (
        <div className="promo-section">
            <div>
                <h1 style={styles}>
                    {props.heading}
                </h1>
            </div>
            <div>
                <h2>{props.promoSubHeading}</h2>
            </div>
        </div>
    );
}
```

Utilizar este enfoque hace que sus componentes sean más autónomos, porque vienen con sus propios estilos incorporados, pero también los hace un poco más difíciles de mantener.
