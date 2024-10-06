# Mantener el sistema limpio
#comandos 

---
## Limpiar el caché de dnf (gestor de paquetes)

Este comando elimina los archivos temporales descargados por **dnf** durante las actualizaciones e instalaciones de paquetes.
```bash
sudo dnf clean all
```
## Eliminar paquetes huérfanos

Estos son paquetes instalados como dependencias de otros programas que ya no se utilizan.
```bash
sudo dnf autoremove
```
## Limpiar el caché de los usuarios

Elimina archivos temporales del sistema y del usuario.
```bash
sudo rm -rf /var/tmp/* && rm -rf ~/.cache/*
```
## Limpiar registros del sistema

Los registros pueden ocupar espacio con el tiempo. Puedes limpiarlos con:
```bash
sudo journalctl --vacuum-time=2weeks
```
## Limpiar las miniaturas

Las miniaturas generadas por el sistema también pueden ocupar bastante espacio:
```bash
rm -rf ~/.cache/thumbnails/*
```