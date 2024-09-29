# Historial de fusiones(merge)

Creado: 28 de septiembre de 2024 9:18

---

El comando `git log --merge` se utiliza para mostrar el historial de commits relacionados con una operación de **fusión** (*merge*). Este comando es particularmente útil cuando te encuentras en medio de un conflicto de fusión, ya que muestra los commits involucrados en el proceso de la fusión actual.

### ¿Cuándo utilizar `git log --merge`?

- Cuando estás resolviendo un conflicto durante una fusión.
- Para ver los commits que están en conflicto.

### Funcionalidad:

- **`git log --merge`** te muestra solo los commits de las dos ramas que están en conflicto, lo cual ayuda a identificar qué cambios están causando el problema durante el merge.

Por ejemplo:

- Si has intentado hacer `git merge` entre dos ramas y te aparecen conflictos, usar este comando te dará una lista de los commits que podrían estar involucrados en esos conflictos.

### Ejemplo de uso:

Supongamos que intentas fusionar dos ramas con un comando como este:

```bash
git merge rama-secundaria
```

Si se generan conflictos, puedes ejecutar:

```bash
git log --merge
```

Esto te mostrará los commits relevantes de ambas ramas que podrían estar causando los conflictos.

Este comando es bastante útil para depurar conflictos en un merge y entender mejor qué cambios están en juego.