
## Operadores

  

### Aritméticos

  

* `+` suma

* `-` resta

* `*` multiplicación

* `/` división entera

* `%` módulo

  

### Numéricos

  

* `-eq` igual

* `-ne` distinto

* `-gt` mayor

* `-lt` menor

* `-ge` mayor o igual

* `-le` menor o igual

  

### Cadenas

  

* `=` igual

* `!=` distinto

* `-z` cadena vacía

* `-n` cadena no vacía

* `>` mayor en orden alfabético (dentro de `[[ ]]`)

* `<` menor en orden alfabético (dentro de `[[ ]]`)

  

### Lógicos

  

* `&&` AND (Y)

* `||` OR (O)

* `!` NOT (NO)

  

### Archivos

  

* `-e` existe

* `-f` es un archivo regular (contiene datos legibles o binarios y no es un directorio)

* `-d` es un directorio

* `-r` tiene permisos de lectura

* `-w` tiene permisos de escritura

* `-x` es ejecutable

* `-s` existe y no está vacío

  

## Condicionales

  

Permiten ejecutar comandos sólo si se cumplen ciertas condiciones.

  

### if

  

```

if [ condición ]; then

    comando_si_verdadero

fi

```

  

### if con else

  

```

if [ condición ]; then

    comando_si_verdadero

else

    comando_por_defecto

fi

```

  

### if con elif

  

```

if [ condición ]; then

    comando_si_verdadero

elif [ condición ]; then

    comando_si_verdadero

fi

```

  

> [!WARNING]  


> Puedes crear tantos elif como quieras, pero, en el momento que se cumple la primera condición, se dejan de evaluar las restantes.

  

### if con elif y else

  

```

if [ condición ]; then

    comando_si_verdadero

elif [ condición ]; then

    comando_si_verdadero

elif [ condición ]; then

    comando_si_verdadero

else

    comando_por_defecto

fi

```

  

### case

  

Para múltiples condiciones que evalúan un mismo valor o menús.

  

```

case variable in

    valor_variable) comando_si_verdadero;;

    valor_variable) comando_si_verdadero;;

    valor_variable) comando_si_verdadero;;

    ...

    *) comando_por_defecto;;

esac

```

  

```

#!/bin/bash

read -p "Elige una opción (a/b/c): " option

case $option in

    a) echo "Elegiste A";;

    b) echo "Elegiste B";;

    c) echo "Elegiste C";;

    *) echo "Opción no válida";;

esac

```

  

### Ejemplo condicionales

  

```

#!/bin/bash

num=25

if [ $num -ge 10 ]; then

    echo "Número mayor o igual que 10"

elif [ $num -eq 0 ]; then

    echo "Número igual a 0"

else

    echo "Condición por defecto"

fi

read -p "Elige una opción (1/2/3): " option

case $option in

    1) echo "Elegiste 1";;

    2) echo "Elegiste 2";;

    3) echo "Elegiste 3";;

    *) echo "Opción no válida";;

esac

name=Carlos

if [ -n $name ]; then

    echo "El nombre existe"

fi

if [ $num -ge 18 ] && [ -n $name ]; then

    echo "Mayor de edad"

fi

if [ -e "./script.sh" ]; then

    echo "El archivo existe"

fi

```

  

* `$num -ge 10` → comprueba que la variable *num* sea *mayor o igual que 10*.

* `$num -eq 0` → comprueba que la variable *num* sea *igual a 10*.

* `case $option in` → inspecciona el valor de *option* para asignar el caso de ejecución correcto en base a su valor.

* `-n $name` → comprueba que la cadena asociada a *name* no esté *vacía*.

* `[ $num -ge 18 ] && [ -n $name ]` → comprueba que *num* sea *mayor o igual que 18* y que *name* no esté *vacío*.

* `-e "./script.sh"` → comprueba que el *script existe*.