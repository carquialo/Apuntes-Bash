La búsqueda y el recuento son tareas comunes que permiten encontrar patrones de texto y contar sus ocurrencias en archivos o en la salida de otros comandos. 

`grep` (búsqueda):

El comando grep se utiliza para buscar líneas de texto que coincidan con un patrón específico. 

- grep "patrón" archivo: Busca el patrón en el archivo y muestra las líneas que lo contienen.
- grep -i "patrón" archivo: ignora mayúscula y minúsculas durante la búsqueda.
- grep -v "patrón" archivo: invierte la búsqueda, mostrando las líneas que no contienen el patrón.
- grep -r "patrón" directorio: Busca de forma recursiva en todos los archivos de un directorio y sus subdirectorios. 
- grep -n "patrón" archivos: muestra el número de línea junto con la línea encontrada. 

`wc` (Recuento):

El comando wc (word count) se utiliza para contar líneas, palabras y caracteres en un archivo.

- wc -l archivo: Cuenta solo el número de líneas.
- wc -w archivo: el número de palabras. 
- wc -c archivo : el número de caracteres (Bytes).