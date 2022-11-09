# Campos de acción (botones)

Una vez que hemos insertado campos de texto en nuestro formulario es hora de insertar botones. Mediante los botones podremos realizar operaciones de envío del formulario, de manipulación de datos, borrado de datos, etc.

Existen dos formas de insertar botones dentro de un formulario: el elemento input y el elemento button. La primera es recurre nuevamente al elemento input que hemos visto anteriormente para los campos de texto.

La sintaxis para un botón mediante un elemento input será:

```html
<input type="button" value="TextoBotón"/>
```

Si bien, este botón no hace nada por sí solo y tendríamos que darle un comportamiento vía Javascript para que el botón tuviera funcionalidad.

Botones de envío
En el caso del elemento input podemos poner botones de otras dos formas y en estos casos ya con funcionalidad. Estos son los tipos “submit” y “reset”.

Para crear un botón que nos envíe los datos del formulario al servidor tenemos el tipo submit. Su sintaxis es la siguiente:

```html
<input type="submit" value="TextoBotón"/>
```

Una vez que pulsemos sobre el botón se enviarán los datos que el usuario haya insertado en el formulario.

Botones de borrado
El otro tipo de botón con funcionalidad es el que nos permite el borrado de los datos del formulario. Para ello tenemos el tipo “reset”. La sintaxis de este botón será:

```html
<input type="reset" value="TextoBotón"/>
```

Cuando el usuario pulse sobre el botón de borrado. Todos los valores que el usuario haya insertado en el formulario se eliminarán.

El elemento button
Como hemos visto hasta ahora los botones que hemos insertado han sido mediante el elemento `input`, si bien contamos con otro elemento para poner botones en el formulario que es el elemento `button`. Cuya funcionalidad es la misma que la del elemento `input`.

La sintaxis del elemento `button` es:

```html
<button name="nombre" type="TipoBoton" value="ValorBoton"></button>
```

Dependiendo del tipo que asignamos al atributo type obtendremos un comportamiento u otro:

- `submit`, crea un botón para el envío de formulario.
- `reset`, crea un botón para el borrado de datos del formulario.
- `button`, crea un botón normal.
