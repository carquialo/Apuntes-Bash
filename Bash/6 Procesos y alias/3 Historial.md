* `history` muestra el historial de comandos.

* `!!` repite el último comando.

* `!` expansión de comandos:

    * `!10` ejecuta el comando número *10*.

    * `!ls` ejecuta el último comando que empezó con `ls`.

  

> [!WARNING]


> Cuidado al escribir `!` en una cadena de texto, ya que puede intentar realizar un referencia al historial y producir un error. Para evitarlo, puedes escapar el signo utilizando la barra invertida `\` antes de `!`. También puedes usar comillas simples `'` en vez de dobles `"` para crear la cadena de texto.