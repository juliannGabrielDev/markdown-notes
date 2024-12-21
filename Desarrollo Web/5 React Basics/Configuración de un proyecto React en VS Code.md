---
Fecha: 2024-12-20
tags:
  - front-end
  - curso-5
---
## **1 Abrir el terminal incorporado de VS Code**
---
En VS Code, haga clic en _Ver_, _Terminal_ para abrir el terminal incorporado.

Ahora ejecute el comando para añadir una aplicación React completamente nueva a la máquina:

```shell
npm init react-app firstapp
```

Si sigue las sugerencias de la salida anterior, ejecutará: `cd firstapp`, y luego `npm start`.

Esto terminará con la siguiente salida en el terminal incorporado:

`¡Compilado con éxito!`


_Ahora puede ver firstapp en el navegador. 
Local:_ [_http://localhost:3000_](http://localhost:3000/) 
_en su red:_ [_http://192.168.1.167:3000_](http://192.168.1.167:3000/) 

_Tenga en cuenta que la compilación de desarrollo no está optimizada. Para crear una compilación de producción, utilice npm run build._

`webpack compilado con éxito`

Esto significa que ha compilado con éxito:

- Configurado su entorno de desarrollo local

- Ejecutado el paquete `npm create-react-app` (¡sin instalarlo!)

- Construido una starter React app en su máquina local

- Servido esa aplicación React de inicio en su navegador.