---
Fecha: 2024-12-18
Notas relacionadas:
  - "[[742 Importar archivos en Python]]"
  - "[[743 Trabajar con archivos en Python]]"
tags:
  - ciberseguridad
  - curso-7
  - modulo-4
---
## Introducción

En esta actividad, practicará el uso de funciones y otra sintaxis para importar y analizar archivos de texto en Python. Preparará un archivo de registro de seguridad para su análisis y creará un archivo de texto con las direcciones IP que tienen permiso para acceder a información restringida.

## Lo que hará

Usted tiene múltiples tareas en este laboratorio:

- Importar y almacenar un archivo de texto como una cadena

- Convertir el archivo de texto en una lista utilizando el método de cadena .split()

- Añadir información al archivo de texto

- Crear otro archivo de texto

```python
import_file = "login.txt"

with open(import_file, "r") as file:
	text = file.read()
print(text)

# Convertir el texto en una lista
text_to_list = text.split()
print(text_to_list)

# Agregar entrada faltante
missing_entry = "jrafael,192.168.243.140,4:56:27,2022-05-09"

with open(import_file, "a") as file:
	file.write(missing_entry)

with open(import_file, "r") as file:
	text = file.read()

print("Registro de la nueva entrada \n" + text)
```