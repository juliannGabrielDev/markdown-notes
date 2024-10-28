# Comandos fzf
#comandos 

---
## Visualizar archivos mediante `cat`
```bash
fzf --preview="cat {}"
```
## Visualizar archivos con resaltado de sintaxis
```bash
fzf --preview="bat --color=always {}"
```
## Abrir archivo en Visual Studio Code y Sublime Text
```shell
echo Visual Studio Code
code $(fzf --preview="bat --color=always {}")

echo Sublime Text
subl $(fzf --preview="bat --color=always {}")
```
