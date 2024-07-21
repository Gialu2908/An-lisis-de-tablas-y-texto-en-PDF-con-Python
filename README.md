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
def extract_from_astore_shop(path):
    """ Extracts information from pdf"""
    pdf = pdfp.open(path)
    first_page = pdf.pages[0]
    first_page_text = first_page.extract_text().split('\n')
    data = []
    dates = []
```
- Descripcion linea por linea del anterior Script
- Esta línea define la función principal. Toma un parámetro , que es la ruta al archivo PDF que se va a procesar.path
```Función principal
extract_from_astore_shop(path)
```

Esta es una docstring, que proporciona una breve descripción de lo que hace la función. En este caso, indica que la función extrae información de un PDF.
```Esta es una docstring
""" Extracts information from pdf"""
```

- Aquí, se utiliza la biblioteca (importada como ) para abrir el archivo PDF especificado por .pdfplumberpdfppath
- El objeto PDF resultante se almacena en la variable .pdf
``` pdf = pdfp.open(path)
pdf = pdfp.open(path)
```

- Esta línea accede a la primera página del PDF.
- pdf.pages es una lista de todas las páginas del PDF, y selecciona la primera página.[0]
```first_page = pdf.pages[0]
first_page = pdf.pages[0]
```

- first_page.extract_text() extrae todo el texto de la primera página como una sola cadena.
- .split('\n') divide esta cadena en una lista de strings, separando por saltos de línea.
- El resultado es una lista donde cada elemento es una línea de texto de la primera página.
```first_page_text = first_page.extract_text().split('\n')
first_page_text = first_page.extract_text().split('\n')
```

- Inicializa una lista vacía llamada .data
- Esta lista se utilizará más adelante para almacenar la información extraída de los productos o ítems del pedido.
```data = []
data = []
```

- Inicializa otra lista vacía llamada .dates
- Esta lista se usará para almacenar las fechas encontradas en el documento.
```data = []
data = []
```

Estas líneas de código constituyen la fase de inicialización y preparación del proceso de extracción. Están diseñadas para:

- 1. Abrir y acceder al contenido del PDF.
- 2. Extraer y preparar el texto de la primera página para su procesamiento.
- 3. Preparar estructuras de datos (listas) para almacenar la información que se extraerá posteriormente.
