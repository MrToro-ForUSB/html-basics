# Envío del formulario

Una vez que ya hemos construido nuestro formulario solo nos quedará una cosa, esta será enviar el formulario.

Para enviar el formulario deberemos de controlar dos cosas. Por un lado a dónde lo vamos a enviar, es decir, cual es la URL del programa destino (o página destino) que va a procesar los datos del formulario y que nos va a dar una respuesta. Por otro lado está el tipo de envío de los parámetros. En el caso del tipo de envío tenemos la posibilidad de hacerlo mediante un formato `GET` (con los datos visibles) o `POST` (con los datos no visibles).

Ambos elementos los configuraremos dentro del elemento `form`.

## Destino del formulario

Para establecer el destino del formulario tenemos el atributo action. El atributo action tiene la URL de destino del formulario. La estructura del atributo action es:

```html
<form action="url-destino"> … </form>
```

Las URL de destino suelen ser programas o código de servidor, ya sea Java, PHP, Node, ASP,… Los cuales recuperan la información del formulario, la manipulan y nos devuelven una nueva página HTML.

## Tipo de envío: `GET` y `POST`

Para establecer el tipo de envío del formulario tenemos el atributo method. El atributo method puede tener dos valores: `GET` y `POST`. El atributo method lo encontramos dentro del elemento `form`:

```html
<form method="GET|POST"> … </form>
```

A la hora de enviar los **formularios de forma GET** lo que vamos a conseguir es que a la URL destino del formulario se le añaden los parámetros con los datos del formulario en la estructura:

```html
action?nombre1=valor1&nombre2=valor2&...&nombreN=valorN
```

Si tenemos el siguiente formulario:

```html
<form action="envio.php" method="GET">
  <label for="nombre">Nombre</label>
  <input type="text" id="nombre" name="nombre"/>
  <label for="apellido">Apellido</label>
  <input type="text" id="apellido" name="apellido"/>
  <button id="envio">Enviar Formulario</button>
</form>
```

Lo que se enviará en la URL será algo parecido a:

```html
envio.php?name=Victor&apellido=Cuervo
```

Es importante que nos fijemos que utiliza el valor que hay dentro de los atributos name para realizar el envío. Si indicamos que el método de envío del formulario es `POST` lo que hará el navegador es enviar los datos junto al cuerpo del formulario y no se verán en la URL.

Así, en el siguiente formulario:

```html
<form action="envio.php" method="POST">
  <label for="nombre">Nombre</label>
  <input type="text" id="nombre" name="nombre"/>
  <label for="apellido">Apellido</label>
  <input type="text" id="apellido" name="apellido"/>
  <button id="envio">Enviar Formulario</button>
</form>
```

Solo veremos, al enviarlo:

```html
enviar.php
```

Formato del contenido del formulario
Cuando enviamos el formulario deberemos de saber qué sucede con el contenido. Es decir, si lo envía de alguna forma en especial o con algún tipo de tratamiento. Lo primero que tenemos que saber es que el campo que permite establecer el formato del contenido del formulario es enctype, que es un atributo del elemento form:

```html
<form enctype="formato-contenido">...</form>
```

Los formularios, por defecto, se envían mediante el formato `application/x-www-form-urlencoded`. Este formato lo que hace es sustituir los espacios por + y convierte los caracteres especiales en secuencias de escape. Por otro lado las combinaciones de nombre valor las separa por un `=` y las parejas con símbolos `&`. Como ya vimos en las peticiones del tipo `GET`.

```html
<form enctype="application/x-www-form-urlencoded">...</form>
```

Si bien, en el caso de que queramos enviar formularios con un gran volumen de información o con imágenes, deberemos de utilizar el tipo `multipart/form-data`.

```html
<form enctype="multipart/form-data">...</form>
```

Los formularios que utilizan el tipo `multipart/form-` contienen una serie de partes conocidas como `form-data` en las que va cada uno de los campos enviados en el formulario.

De esta forma si tenemos el siguiente formulario:

```html
<form enctype="multipart/form-data" action="envio.php" method="POST">
  <label for="nombre">Nombre</label>
  <input type="text" id="nombre" name="nombre"/>
  <label for="apellido">Apellido</label>
  <input type="text" id="apellido" name="apellido"/>
  <label for="fichero">Fichero</label>
  <input type="file" id=fichero" name="fichero"/>
  <button id="envio">Enviar Formulario</button>
</form>
```

La petición multipart podría ser de la siguiente forma:

```bash
-----------------------------931237358445456570660578548
Content-Disposition: form-data; name="nombre"

Victor
-----------------------------931237358445456570660578548
Content-Disposition: form-data; name="apellido"

Cuervo
-----------------------------931237358445456570660578548
Content-Disposition: form-data; name="fichero"; filename="fotografia.png"
Content-Type: image/png
```