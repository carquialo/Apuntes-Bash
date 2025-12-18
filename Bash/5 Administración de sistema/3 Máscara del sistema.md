La máscara hace referencia a los permisos por defecto que se le otorgarán a nuevos directorios o archivos.

  

* `umask` muestra la máscara de permisos por defecto.

* `umask [permisos_octal]` establece los permisos por defecto.

    * Ejemplo: `umask 022`

  

> [!CAUTION]

>

> La modificación de la máscara es temporal, y sólo afecta a la sesión de la shell actual. Para hacerlo permanente, puedes agregarlo al script de configuración de Bash (como en el caso de variables globales explicado en una lección anterior).

  

### Cálculo de permisos con máscara

  

La máscara hace referencia a los valores que deben restarse a los permisos máximos razonables de un directorio o archivo.

  

* Permisos máximos razonables para un directorio: `777`

* Permisos máximos razonables para un archivo: `666` (Sin ejecución, ya que dar esos permisos por defecto a todos los archivos sería peligroso)

  

Si la máscara de permisos es `0022`, quiere decir lo siguiente:

  

* Si la máscara tiene 4 dígitos, el primer cero de la izquierda únicamente indica que la representación de los 3 siguientes está en sistema octal.

* 0 al usuario no le quito ningún permiso

* 2 a los grupos le quito el permiso de escritura (2)

* 2 a otros le quito el permiso de escritura (2)

  

Cálculo de permisos:

  

* Para directorios: `777` - `022` (bloque a bloque) = `755` [`rwxr-xr-x`]

* Para archivos: `666` - `022` (bloque a bloque) = `644` [`rw-r--r--`]

  

Esos son los permisos por defecto que se le otorgarían a nuevas carpetas y archivos.