## Definición

  

Un script es un archivo de texto que contiene comandos que la shell ejecutará secuencialmente para permitir así automatizar tareas repetitivas.

  

## Convenciones en Bash

  

1. Extensión `.sh` (opcional, ya que Bash no la requiere).

2. Primera línea `#!/bin/bash` (shebang), para indicar con qué intérprete ejecutar el script.

3. Permisos de ejecución `chmod +x script.sh` (el archivo debe ser ejecutable para correr directamente).

  

## Ejemplo básico

  

```

#!/bin/bash

# Mi primer script

echo "Hola, este es mi primer script en Bash"

date

echo "Tu directorio actual es: $(pwd)"

```

  

* `#!/bin/bash` → shebang

* `# Mi primer script` → comentario (documenta, no se ejecuta)

* `echo, date` → comandos en Bash

* `"$(pwd)"` → interpolación de comandos

  

## Variables

  

```

name="Carlos"

echo "Hola $name"

```

  

* `name="Carlos"` → definición de la variable

* `"$name"` → interpolación de la variable

  

## Aritmética básica

  

Aunque Bash trata todo como texto, podemos realizar operaciones numéricas.

  

```

a=5

b=3

let sum=a+b

echo "La suma es $sum"

sum2=$((a+b))

echo "La suma2 es $sum2"

```

  

* `let` es el comando que se usa para realizar operaciones aritméticas directamente sobre variables.

* `$(( ))` es más habitual usar expansión aritmética en Bash moderno.

  