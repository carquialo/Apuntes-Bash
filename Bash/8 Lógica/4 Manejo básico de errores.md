### Códigos de salida

  

* `0` → Éxito

* `!=0` → Error

  

```

#!/bin/bash

cp file.txt ../Course

if [ $? -ne 0 ]; then

    echo "Error al copiar el archivo"

fi

```

  

* `cp file.txt ../Course` → intenta realizar la copia.

* `$? -ne 0` → accede al código de salida y comprueba si es distinto de cero (error).

  

### Atajos

  

* `|| command` → ejecuta el comando si hay un error.

* `$$ command` → ejecuta el comando si no hay un error.

  

```

cp file.txt ../Course || echo "Otra vez se ha producido el error"

cp script.sh ../Course && echo "No se ha producido un error"

```

  

* `||` → se ejecuta el *echo* si se produce un error en el *cp*.

* `&&` → se ejecuta el *echo* si *cp* se realiza con éxito.