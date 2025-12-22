### for

  

Recorre un listado de valores.

  

```

for i in 1 2 3 4 5

do

    echo "Número: $i"

done

  

for name in *.sh

do

    echo "Archivo: $name"

done

```

  

* `for i in 1 2 3 4 5` → recorre el listado de números definidos, almacenando el valor de cada iteración en la variable *i*.

* `for name in *.sh` → recorre el listado de archivos que cumplan el criterio de la extensión, almacenando el valor de cada iteración en la variable *name*.

  

### while

  

Se ejecuta mientras la condición sea verdadera.

  

```

count=1

while [ $count -le 5 ]

do

    echo "Contador: $count"

    ((count++))

done

```

  

* `while [ $count -le 5 ]` → se ejecuta el bucle mientras el valor de la variable *count* sea *menor o igual que 5*.

* `((count++))` → incrementa el valor de *count* en 1 tras cada ejecución del bucle.

  

### until

  

Se ejecuta hasta que la condición sea verdadera.

  

```

count=1

until [ $count -gt 10 ]

do

    echo "Contador: $count"

    ((count++))

done

```

  

* `until [ $count -gt 10 ]` → se ejecuta el bucle hasta el valor de la variable *count* sea *mayor que 10*.

* `((count++))` → incrementa el valor de *count* en 1 tras cada ejecución del bucle.

  

### Control de bucles

  

```

for i in 1 2 3 4 5

do

    if [ $i -eq 3 ]; then

        continue

    elif [ $i -eq 4 ]; then

        break

    fi

        echo "Número: $i"

done

```

  

* `continue` salta la iteración y pasa a la siguiente.

* `break` sale del bucle actual.