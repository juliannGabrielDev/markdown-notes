# zsh
#linux

---
## Instalación o configuración
### Instalar zsh y oh-my-zsh
```shell
sudo dnf install zsh
chsh -s $(which zsh)

sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### Descargar `powerlevel10k`
```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```
### Aplicar cambios
```shell
source ~/.zshrc
```
---
## Plugins
### Git
`plugins=(git)`

| alias | comando         |
| ----- | --------------- |
| `gst` | `git status`    |
| `gco` | `git checkout`  |
| `gl`  | `git log`       |
| `gcm` | `git commit -m` |
### zsh-autosuggestions
`plugins=(zsh-autosuggestions)`

```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
### zsh-syntax-highlighting
`plugins=(zsh-syntax-highlighting)`

```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
### history
`plugins=(history)`
### copypath
`plugins=(copypath)`