### Función simple

  

```

my_function() {

    echo "Hola desde la función"

}

my_function

```

  

* `my_function()` → definición

* `my_function` → invocación

  

### Función con parámetros

  

```

my_function_with_params() {

    echo "Hola $1"

}

my_function_with_params Carlos

  

```

  

* `$1` → accede al primer argumento posicional

* `my_function_with_params argumento` → invocación enviando el parámetro

  

### Función con retorno

  

```

my_function_with_return() {

    return 1

}

my_function_with_return

echo $?

```

  

* `return` → retorna un valor desde la función

* `$?` → accede al valor del retorno fuera de la función tras su invocación

  

> [!TIP]


> Retorna `0` como código de salida para indicar éxito en la ejecución y otro número para indicar un error.

  

## Variables globales y locales (ámbito)

  

* Variables **globales**: visibles en todo el script.

* Variables **locales**: visibles sólo dentro de la función (local).

  

```

name=Carlos # global

my_function_2() {

    local msj=", mundo" # local

    echo "Hola $msj $name"

}

echo "Hola desde fuera $msj"

my_function_2

```

  

* `local` → para definir variables locales.

* `echo "Hola $msj $name"` → puede acceder a las 2 variables desde su ámbito.

* `echo "Hola desde fuera $msj"` → no puede acceder a la variable local fuera del ámbito de la función.

  

> [!CAUTION]


> Utiliza `local` como buena práctica para definir variables locales.