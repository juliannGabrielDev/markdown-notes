# Integración por sustitución trigonométrica
#Teoría #integrales

---
La **integración por sustitución trigonométrica** es una técnica útil cuando nos encontramos con integrales que involucran expresiones cuadráticas dentro de raíces o fracciones.

En estos casos, se utilizan las identidades trigonométricas para simplificar la integral. 

**Consideraciones:**
- **u** = función. Ejemplo u = x
- **a** = constante. Ejemplo a = 3
---
## Paso 1
Identificar a que caso pertenece nuestra integral:

| **Caso 1** | $\sqrt{a^2 - u^2}$ |
| ---------- | ------------------ |
| **Caso 2** | $\sqrt{a^2 + u^2}$ |
| **Caso 3** | $\sqrt{u^2 - a^2}$ |

---
## Paso 2
Encontrar los siguientes 3 elementos:
### El cambio:

|            | Valor de variable (x) | La derivada                                | Valor de la raíz                    |
| ---------- | --------------------- | ------------------------------------------ | ----------------------------------- |
| **Caso 1** | $u = a \sin(\theta)$  | $du = a \cos(\theta) d\theta$              | $\sqrt{a^2 - u^2} = a \cos(\theta)$ |
| **Caso 2** | $u = a \tan(\theta)$  | $du = a \sec^2(\theta) d\theta$            | $\sqrt{a^2 + u^2} = a \sec(\theta)$ |
| **Caso 3** | $u = a \sec(\theta)$  | $du = a \sec(\theta) \tan(\theta) d\theta$ | $\sqrt{u^2 - a^2} = a \tan(\theta)$ |

---
## Paso 3
Sustituir los valores en la integral y resolver la integral (Para esto probablemente debas hacer uso de las identidades trigonométricas antes de integrar).

---
## Paso 4
Convertir la expresión a términos de **X** usando el triángulo rectángulo. 
```
       |\
       | \
  c.o. |  \ h
       |   \
       |____\
         c.a.

```

**Caso 1**
Para este caso, tenemos la sustitución $u=a sin⁡(θ)$ que implica que:
- La **hipotenusa** es $a$.
- El **cateto opuesto** es $u$.
- El **cateto adyacente** es $\sqrt{a^2 - u^2}$.

**Caso 2**
En este caso, usamos la sustitución $u=a tan⁡(θ)$, lo que nos lleva a las siguientes relaciones en un triángulo rectángulo:
- La **hipotenusa** es $\sqrt{a^2 + u^2}$
- El **cateto opuesto** es $u$.
- El **cateto adyacente** es $a$.

**Caso 3**
Para esta forma, hacemos la sustitución $u=a sec⁡(θ)$, lo que genera las siguientes relaciones en un triángulo:
- La **hipotenusa** es $u$.
- El **cateto opuesto** es $\sqrt{u^2 - a^2}$
- El **cateto adyacente** es $a$.
---
## Paso 5
Ya que tenemos los datos de la **hipotenusa**, el **cateto opuesto** y el **cateto adyacente** usaremos las siguientes formulas dependiendo de la expresión trigonométrica que aparece en nuestro resultado de la integración (**Paso 3**).

| $$\sin(\theta) = \frac{\text{cateto opuesto}}{\text{hipotenusa}}$$ | $$\cos(\theta) = \frac{\text{cateto adyacente}}{\text{hipotenusa}}$$ | $$\tan(\theta) = \frac{\text{cateto opuesto}}{\text{cateto adyacente}}$$ |
| ------------------------------------------------------------------ | -------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| $$\csc(\theta) = \frac{\text{hipotenusa}}{\text{cateto opuesto}}$$ | $$\sec(\theta) = \frac{\text{hipotenusa}}{\text{cateto adyacente}}$$ | $$\cot(\theta) = \frac{\text{cateto adyacente}}{\text{cateto opuesto}}$$ |

---
## Paso 6
Sustituimos la **expresión trigonométrica** de nuestro resultado de la integración del paso 3 por **el resultado del paso 5**, de esta forma nuestro resultado ahora se encuentra en términos de **X**.

**LISTO HAS TERMINADO**