# Como crear una imagen en formato .dd en #Linux

---
## 1. Identifica el dispositivo
```shell
lsblk
```
## 2. Crear la imagen .dd
```shell
sudo dd if=/dev/sdX of=/ruta/donde/guardar/imagen.dd bs=4M status=progress
```