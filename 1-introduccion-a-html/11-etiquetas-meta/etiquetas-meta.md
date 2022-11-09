# Metadatos: etiqueta `<meta>`

Los metadatos son datos que describen datos, y HTML tiene una forma «oficial» de introducir metadatos en un documento — por medio de la etiqueta `<meta>`.

## La codificación de caracteres de tu documento

La línea `<meta charset="utf-8">` es una etiqueta que indica que el documento está codificado en UTF-8. Este elemento simplemente especifica el conjunto de caracteres que el documento puede usar. 

Recuerda que ahora ya podemos usar emojis en nuestro documento 😈. Esto es gracias al soporte de UTF-8 en el navegador. Así como emijis también se pueden usar en el texto con caracteres especiales, como lo son los acentos y los signos de puntuación.

## Añadir un autor y descripción

Muchos elementos `<meta>` incluyen atributos `name` y `content`:

```html	
<meta name="author" content="Juan">
<meta name="description" content="Este documento es una descripción">
```

Con description podemos indicar una descripción del documento. Resulta muy valioso en el posicionamiento de los motores de búsqueda como el de Google:

![imagen que ilustra ](https://mdn.mozillademos.org/files/16074/mdn-search-result.png)

## Otros tipos de metadatos

Al navegar por la web también puedes encontrar otros tipos de metadatos. 

Muchas de las funciones que verás en los sitios web son creaciones propietarias diseñadas para proporcionar a ciertos sitios (como los sitios de redes sociales) información específica que puedan usar.

```html	
<meta property="og:image" content="https://developer.mozilla.org/static/img/opengraph-logo.png">
<meta property="og:description" content="The Mozilla Developer Network (MDN) proporciona información
sobre tecnologías Open Web, incluidas HTML, CSS y APIs para ambos sitios web
y aplicaciones HTML5. También documenta productos Mozilla, como el sistema operativo Firefox.">
<meta property="og:title" content="Mozilla Developer Network">
```

Un efecto de esto es que cuando desde una red social enlazas a un Sitio con estos meta datos, el enlace aparece con una imagen y una descripción, lo que resulta en una experiencia más enriquecedora para los usuarios.

![Ilustración del resultado donde aparece una imagen, nombre y descripción del sitio web](https://mdn.mozillademos.org/files/12349/facebook-output.png)

## Agregar iconos personalizados a tu sitio

Para enriquecer un poco más el diseño de tu sitio puedes añadir en tus metadatos referencias a iconos personalizados, que se mostrarán en determinados contextos. 

El más común de ellos es el favicon (abreviatura de favorite icon —icono «favorito», referido al uso que se le da en las listas de «favoritos» o de marcadores («bookmarks»).

Para añadir un favicon a tu página:

1. Guárdalo en el mismo directorio que la página index de tu sitio, en formato `.ico` (la mayoría de los buscadores admiten favicon en los formatos más comunes como `.gif` o `.png`, pero usar el formato ICO garantiza que funcionará hasta en Internet Explorer 6.)
2. Añade la siguiente línea de referencia en el `<head>` de tu HTML:
   
  ```html
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
  ```

## Aplicar CSS y JavaScript a HTML

Prácticamente todos los sitios web usan CSS para darles un buen aspecto y JavaScript para añadir funcionalidades interactivas, como reproductores de vídeo, mapas, juegos y demás. La manera más habitual de añadir CSS y JavaScript a una página web es con los elementos `<link>` y el elemento `<script>`, respectivamente.

1. El elemento `<link>` siempre debe ir dentro del `<head>` de tu documento. Este toma dos atributos, rel="stylesheet", que indica que es la hoja de estilo del documento, y href, que contiene la ruta al archivo de la hoja de estilo:

  ```html
  <link rel="stylesheet" href="css/estilo.css">
  ```

2. El elemento `<script>` también debería ir en el head, y debería incluir un atributo src con la ruta al JavaScript que quieres cargar, y defer, que básicamente le dice al navegador que cargue el JavaScript al mismo tiempo que el HTML de la página.

```html
<script src="js/script.js" defer></script>
```

## Establecer el idioma principal del documento

Por último, merece la pena mencionar que puedes (y realmente deberías) especificar el idioma de tu página. Esto se puede hacer añadiendo el atributo lang a la etiqueta de apertura del HTML.

```html
<html lang="es">
```	

Esto resulta útil en muchos sentidos. Los motores de búsqueda indizarán tu documento HTML de modo más efectivo si estableces el idioma.

También resulta útil para que las personas con discapacidad visual que utilizan los lectores de pantalla (por ejemplo, la palabra «six» existe tanto en francés como en inglés, pero su pronunciación es diferente).

También puedes establecer que las subsecciones de tu documento se reconozcan en diferentes idiomas. Por ejemplo, podemos establecer que nuestra sección de japonés se reconozca como japonés, de la siguiente manera:

```html	
<p>
  Ejemplo Japonés: <span lang="ja">ご飯が熱い。</span>.
</p>
```