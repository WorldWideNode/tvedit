editor de campos en vista de tabla.

Hola en esta portunidad les quiero dejar para sus programas una aplicacion que les permitira, en las vista de tablas, poder editar rapidamente los campos.
Actulizando esta informaci�n via ajax.
Del lado del servidor cuenta con toda la seguridad que ofrece appgini con respecto al usuario, ejecutando los hooks de antes de actualizar y luego de actualizar, tambien registra la ctualizacion del usuario.

En primer lugar hay que registrar las librarias js para que estas se ejecuten.

Buscar y editar el archivo extras-header.php dentro de la carpeta hooks.
Agregar las siguientes dos lineas de comando:

<script src="<?php echo PREPEND_PATH; ?>LTE/plugins/jquery-jeditable/jquery.jeditable.js"></script>
<script src="<?php echo PREPEND_PATH; ?>LTE/tvedit/tv.edit.js"></script>

Para que se active dentro de la vista de tabla que necesites debes escribir dentro del archo tablename-tv.js (hay que crear uno nuevo si este no se encuentra) las siguientes lineas de comando:

$j(function(){
    tv_editlets(AppGini.currentTableName());
});

basta solo con comentar la linea anterio para que la aplicaci�n se desactive.

Pronto intentare hacerlo qeu funcione con un plugin, para evitar tener que escribir alg�n c�digo.

Esta aplicaci�n esta generada con c�digo propio de appgini y la librar�a jquery_jeditable
 que es de uso libre.
la misma la pueden econtrar ac�:
https://github.com/NicolasCARPi/jquery_jeditable/

la aplicaci�n se entrga as� como est�, hice las pruebas de rigor de funcionamiento, el uso y disitrbuc�n de todo el c�digo est� permitido ya que es un c�digo libre. De todas maneras no es reponsabilidad de este autor el mal uso o abuso del c�digo.

Por favor si consideran que hay alg�n error no dejen de comentar, como as� tambien si les ha gustado.

muchas gracias!

Espero lo disfruten