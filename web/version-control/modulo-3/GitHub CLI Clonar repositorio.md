# GitHub CLI: Clonar repositorio

Creado: 28 de septiembre de 2024 8:59

---

Para clonar un repositorio usando el cliente de GitHub CLI (`gh`), puedes seguir estos pasos:

1. Asegúrate de haber iniciado sesión usando `gh auth login` (como ya te mencioné antes).
2. Ejecuta el siguiente comando para clonar un repositorio:

```bash
gh repo clone <nombre_del_usuario>/<nombre_del_repositorio>
```

Por ejemplo, si quieres clonar el repositorio de un usuario llamado "octocat" y el repositorio se llama "Spoon-Knife", usarías:

```bash
gh repo clone octocat/Spoon-Knife
```

Esto descargará una copia completa del repositorio a tu máquina local.

### Notas:

- Si el repositorio es privado, debes tener acceso a él.
- El repositorio se clonará en la carpeta en la que estés ubicado dentro de la terminal.