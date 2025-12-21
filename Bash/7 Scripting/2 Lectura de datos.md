## Lectura de datos

  

Permite solicitar datos interactivos durante la ejecución.

  

```

#!/bin/bash

echo "¿Cuál es tu nombre? "

read name

echo "Hola, $name"

read -p "¿Cuál es tu edad? " age

echo "Tu edad es $age"

read -s pass

echo "Tu contraseña es $pass"

```

  

* `read` → solicita datos y los almacena en la variable definida.

    * `read -p` → muestra el prompt en la misma línea.

    * `read -s` → entrada oculta para contraseñas.