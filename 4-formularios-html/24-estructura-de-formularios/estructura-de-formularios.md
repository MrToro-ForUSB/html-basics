# Estructura y Envío de Formularios HTML

Una de las cosas importantes que tenemos que saber de los formularios HTML es cómo funciona la Estructura y envío de formularios.

## Etiquetando el formulario
Hemos visto cómo insertar campos para que el usuario introduzca información en el formulario. En algunos casos hemos visto que aunque el campo tiene un dato de valor no lleva una etiqueta asociada. Es verdad que podemos poner texto al lado del elemento de entrada de datos. Por ejemplo en un checkbox:

```html
Equipo: <input type="checkbox" id="betis" name="equipo" value="Real Betis"/>Real Betis
```

¿Quién nos dice que el texto asociado al checkbox es “Equipo” o “Real Betis”? Para resolver esto el lenguaje HTML nos proporciona el elemento `label`.

La sintaxis del elemento `label` es la siguiente:

```html
<label for="identificador">Texto de la Etiqueta</label>
```

El atributo `for` llevará asociado un identificador que deberá de coincidir con el valor de algún atributo `id` de uno de los elementos del formulario. Y será sobre ese elemento sobre el que quede asociado.

De esta forma, en el caso que definimos anteriormente sobre el checkbox, la forma correcta de asociar una etiqueta al elemento será la siguiente:

```html
Equipo: <input type="checkbox" id="betis" name="equipo" value="Real Betis"/>
<label for="betis">Real Betis</label>
```

## Estructura del formulario
En HTML contamos con dos elementos para dar una estructura a los formularios. Estos elementos: `fieldset` y `legend` nos ayudan a agrupar los datos relacionados dentro del formulario.

Pero vayamos por parte. El primero es `fieldset`, este es un elemento que agrupa a diferentes elementos del formulario, elementos que están relacionados entre ellos.

La sintaxis de fieldset es la siguiente:

```html
<fieldset>...</fieldset>
```

Entre estos elementos aparecerán los campos del formulario. Por ejemplo si tenemos campos personales básicos podemos agruparlos de la siguiente forma:

```html
<fieldset>
 <label for="nombre">Nombre</label><input type="text" id="nombre"/>
 <label for="apellido">Apellido</label><input type="text" id="apellido"/>
</fieldset>
```

El elemento `legend` nos servirá para darle un significado a una agrupación

```html
<fieldset>
 <legend>Introduzca sus datos personales</legend>
 <label for="nombre">Nombre</label><input type="text" id="nombre"/>
 <label for="apellido">Apellido</label><input type="text" id="apellido"/>
</fieldset>
```

# Hacer foco en el formulario
Cuando construyamos un formulario deberemos de preocuparnos por cómo hacer foco en los elementos. Está claro que si utilizamos un navegador web el uso del ratón nos facilitará el ir rellenando cada uno de los campos del formulario.

Pero piensa en alguien que no tenga un ratón o bien que utilice un agente de usuario no visual adaptado para discapacitados. En este caso y para temas de accesibilidad tenemos dos formas de hacer foco en el formulario. Una será el uso de la tabulación, y el otro el uso de teclas de acceso.

## Tabulaciones por el formulario
Para las navegaciones por tabulación en el formulario existe el atributo `tabindex`. Este atributo que lo podemos encontrar en todos los elementos de un formulario nos sirve para establecer un orden mediante números ordinales de los campos del formulario. La estructura del atributo `tabindex` es:

```html
tabindex="numero"
```

De esta forma podríamos establecer el orden de un formulario de dos datos básicos y un botón mediante el siguiente código:

```html
<label for="nombre">Nombre</label><input tabindex="1" type="text" id="nombre"/>
<label for="apellido">Apellido</label><input tabindex="2" type="text" id="apellido"/>
<button id="envio" tabindex="3">Enviar Formulario</button>
```

## Teclas de acceso
Otra forma de poder acceder a un elemento del formulario es asignando al elemento una tecla de acceso. De esta manera cuando pulsamos esta tecla (en combinación con alguna definida en el sistema, como la tecla `ALT` para Windows) iremos directamente a dicho elemento.

El atributo que nos permite hacer esto es el atributo accesskey. La estructura del atributo accesskey es la siguiente:

```html
accesskey=tecla
```

Así podríamos definir un campo de un formulario al cual fuésemos al pulsar sobre la “tecla N”:

```html
<label for="nombre" accesskey="N">Nombre</label>
<input tabindex="1" type="text" id="nombre"/>
```

# Deshabilitar controles
A la hora de crear un formulario puede darse el caso que haya algunos campos que en determinados momentos nos aparezcan deshabilitados. Es decir, que el usuario no pueda modificar el valor de dichos campos.

Para poder deshabilitar los controles de un formulario contamos con el atributo disabled. La estructura del atributo disabled es directamente:

```html
disabled
```

De esta manera si queremos deshabilitar nuestro anterior campo de texto que nos permitía insertar un nombre escribimos lo siguiente:

```html
<label for="nombre" accesskey="N">Nombre</label>
<input disabled type="text" id="nombre"/>
```

No podremos hacer foco sobre los elementos de un formulario que estén deshabilitados. De igual manera al hacer tabulación tampoco se podrá tabular sobre ellos. Además no se enviarán como parte de la petición del formulario.

En el caso de que queramos buscar el mismo efecto de que el elemento esté deshabilitado, pero que se pueda tabular, hacer foco y enviar, tenemos el atributo de solo lectura o readonly.

La estructura del atributo readonly es básica:

```html
readonly
```

Si lo aplicamos nuevamente a nuestro campo de texto tendremos:

```html
<label for="nombre" accesskey="N">Nombre</label>
<input readonly type="text" id="nombre"/>
```

El atributo readonly solo se puede aplicar a elementos `input` y `textarea`.