## Diagrama de flujo del script

![Diagrama flujo](https://github.com/user-attachments/assets/55e7ead8-179c-4d5e-bf40-c7004d861e97)

Este script esta diseñado para extraer información de facturas u pedidos en formato PDF
### 1. Importaciones:

```
import re
import pdfplumber as pdfp
from rich import print
```

- re: Módulo para trabajar con expresiones regulares.
- pdfplumber: Biblioteca para extraer información de archivos PDF.
- rich: Biblioteca para mejorar la salida en la consola.


### 2. Función principal
```Función principal
extract_from_astore_shop(path)
```
- Esta línea define la función principal. Toma un parámetro , que es la ruta al archivo PDF que se va a procesar.path
