# Flujo de trabajo de Git

Creado: 27 de septiembre de 2024 21:17

---

El flujo de trabajo en Git generalmente sigue un ciclo que involucra los estados **modified**, **staged**, y **commit**. A continuación te explico cada uno de estos estados y cómo interactúan en el proceso:

### Flujo de trabajo básico en Git:

1. **Modified (Modificado)**:
    - Cuando editas un archivo en tu proyecto, este pasa al estado de **modificado**. En este estado, Git detecta que el archivo ha cambiado, pero aún no está preparado para ser enviado al repositorio.
    - El archivo sigue solo en tu área de trabajo local (working directory) y no se ha registrado en el historial de cambios de Git.
    - Comando relevante:
        - `git status`: para ver qué archivos han sido modificados.
2. **Staged (Preparado para commit)**:
    - Una vez que has modificado los archivos y decides que están listos para ser registrados en el repositorio, los pasas al área de **staging** (preparados para commit). En este estado, Git sabe que quieres incluir esos cambios en el próximo **commit**.
    - Esto te permite agrupar ciertos cambios y decidir cuáles de ellos quieres registrar.
    - Comando relevante:
        - `git add <archivo>`: para mover un archivo modificado al área de staging.
        - `git add .`: para añadir todos los archivos modificados al área de staging.
3. **Commit (Confirmado)**:
    - Después de haber añadido los archivos al área de staging, puedes hacer un **commit**. Un commit es una "fotografía" de tu proyecto en ese momento, guardando el estado exacto de los archivos.
    - Cada commit tiene un mensaje descriptivo que explica los cambios realizados. Estos commits se guardan en el historial de Git, lo que permite seguir el progreso y revertir cambios si es necesario.
    - Comando relevante:
        - `git commit -m "Mensaje del commit"`: para hacer un commit con un mensaje describiendo los cambios.