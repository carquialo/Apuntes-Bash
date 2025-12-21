
## Argumentos y parámetros

  

Los scripts pueden recibir argumentos desde la línea de comandos.

  

```

#!/bin/bash

echo "El nombre del script es: $0"

echo "El primer parámetro es: $1"

echo "El segundo parámetro es: $2"

echo "Número de parámetros: $#"

echo "Todos los argumentos: $@"

```

  

Ejecución con argumentos: `./script.sh argumento1 argumento2`

  

* `$0` accede al nombre del script (*script.sh*).

* `$1` accede al argumento en la primera posición (*argumento1*).

* `$2` accede al argumento en la segunda posición (*argumento2*).

* `$#` accede al número total de parámetros (*2*).

* `$@` accede a todos los parámetros (*argumento1 argumento2*).