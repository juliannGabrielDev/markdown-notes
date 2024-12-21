# Configuración de un repositorio local sincronizado con uno remoto en GitHub

Creado: 28 de septiembre de 2024 3:25

---

En este flujo de trabajo de Git, estás configurando un nuevo repositorio local y tratando de sincronizarlo con un repositorio remoto en GitHub. A continuación te explico paso a paso lo que está sucediendo:

### 1. **Creación de un nuevo repositorio local**:

```bash
mkdir My-second-repo
cd My-second-repo
git init
```

- **`mkdir My-second-repo`**: Creas un nuevo directorio llamado `My-second-repo`.
- **`cd My-second-repo`**: Entras en este directorio.
- **`git init`**: Inicializas un repositorio Git vacío en tu máquina local. Git te informa que la rama predeterminada es `master`, pero que esto puede cambiar y ofrece sugerencias para cambiarla a `main`, `trunk`, etc.

### 2. **Verificación del remoto del repositorio anterior**:

```bash
cd ../My-first-repo
git remote -v
```

- **`cd ../My-first-repo`**: Cambias al directorio de un repositorio anterior (`My-first-repo`).
- **`git remote -v`**: Verificas qué repositorios remotos están configurados. Aquí, el repositorio remoto está configurado como `origin` apuntando a `https://github.com/juliannGabrielDev/My-first-repo.git`.

### 3. **`git pull` y advertencia sobre la rama rastreada**:

```bash
git pull
```

- Al ejecutar **`git pull`**, Git intenta traer los cambios del repositorio remoto. Ingresa tu usuario y token de GitHub.
- Git descarga las ramas del repositorio remoto (`feature/lesson` y `main`).
- Git muestra un mensaje que indica que no hay información de rastreo para la rama actual. Esto significa que no has configurado qué rama local debe sincronizarse (rastrear) con una rama remota.

### 4. **Cambio a la rama `main` y sincronización**:

```bash
git checkout main
```

- Cambias a la rama `main`, que ahora rastrea la rama remota `origin/main`.
- Después de cambiar de rama, haces un **`ls`** y puedes ver los archivos descargados del repositorio remoto, como `README.md`, `test2.txt`, y `test.txt`.