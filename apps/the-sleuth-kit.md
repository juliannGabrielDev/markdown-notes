# The Sleuth Kit
#ciberseguridad #comandos 

---

| **Comando**                                                          | **Función**                       |
| -------------------------------------------------------------------- | --------------------------------- |
| `mmls -V`                                                            | Mostrar la versión                |
| `mmls {imagen}`                                                      | Muestra el diseño del disco       |
| `fls -r -o 2048 {imagen}`                                            | Muestra los archivos en la imagen |
| `tsk_recover -d imagen.dd dir_salida`                                | Recuperar archivos activos        |
| `tsk_recover -e imagen.dd directorio_salida`                         | Recuperar archivos eliminados     |
| `icat imagen.dd 128 > /ruta/al/directorio/archivo_eliminado.txt`<br> | Recuperar un archivo específico   |

**`configure.ac`** es un archivo utilizado por el sistema de construcción **Autotools**, específicamente por el programa **Autoconf**. Su función es definir cómo debe generarse el script de configuración `configure`, que es clave para preparar la compilación de un software en diferentes sistemas.