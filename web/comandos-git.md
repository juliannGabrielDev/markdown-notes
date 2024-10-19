# Comandos Git
## git

| Nombre                   | Descripción                                            |
| ------------------------ | ------------------------------------------------------ |
| git branch               | Regresa todas las ramas disponibles en el repositorio. |
| git branch nombre-rama   | Crea una rama.                                         |
| git log --pretty=oneline | Muestra el historial de commits.                       |
| git checkout rama        | Cambiar a otra rama                                    |

## git diff

| Nombre                                                  | Descripción                                                                                                                                              |
| ------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| git diff                                                | git status le indica cuáles de sus archivos han sido modificados. El comando git diff va un poco más allá y le dice cuáles son exactamente esos cambios. |
| git diff 'codigo-commit-actual' 'codigo-commit-antiguo' | Comparar los cambios entre un commit y otro.                                                                                                             |
| git diff 'rama' 'rama'                                  | Comparar las diferencias entre una rama y otra.                                                                                                          |

## Instrucciones crear un  repositorio local y subirlo a uno remoto
```bash
git init

git add .

git commit -m "mensaje"

git remote add origin https://github.com/usuario/nombre-repositorio.git

git push origin master
```
---
## …or create a new repository on the command line
```bash
echo "# intel-backup" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/juliannGabrielDev/intel-backup.git
git push -u origin main
```
## …or push an existing repository from the command line
```bash
git remote add origin https://github.com/juliannGabrielDev/intel-backup.git
git branch -M main
git push -u origin main
```