# HTML Básico

> *Una guía para el curso de **Desarrollo Web Full Stack***

# ¿Qué es HTML?

HTML (*Lenguaje de Marcas de Hipertexto, del inglés HyperText Markup Language*) es el componente más básico de la Web. Define el significado y la estructura del contenido web. 

Además de HTML, generalmente se utilizan otras tecnologías para describir la apariencia/presentación de una página web (CSS) o la funcionalidad/comportamiento (JavaScript).

HTML utiliza "marcas" para etiquetar texto, imágenes y otro contenido para mostrarlo en un navegador Web. Las  marcas HTML incluyen "elementos" especiales como `<head>`, `<title>`, `<body>`, `<header>`, `<footer>`, `<article>`, `<section>`, `<p>`, `<div>`, `<span>`, `<img>`, `<aside>`, `<audio>`, `<canvas>`, `<datalist>`, `<details>`, `<embed>`, `<nav>`, `<output>`, `<progress>`, `<video>`, `<ul>`, `<ol>`, `<li>` y muchos otros.

> Cabe aclarar que **HTML no es un lenguaje de programación.** Es un lenguaje de marcado que le dice a los navegadores web cómo estructurar las páginas web que estás visitando.

## ¿Cómo uso HTML?

El HTML consiste en una serie de elementos, que puedes utilizar para encerrar, delimitar o marcar diferentes partes del contenido para hacer que aparezcan de una cierta manera, o actúen de determinada forma. Por ejemplo, dada la siguiente línea de contenido::

```
Mi gato es muy gruñón
```

Si queremos que la línea sea independiente de otras, podemos especificar que es un párrafo encerrándola con una etiqueta de elemento de párrafo (`<p>`):

```html
<p>Mi gato es muy gruñón</p>
```

# Anatomía de un documento HTML

![anatomía de una etiqueta HTML](https://i.postimg.cc/k4s9SqbT/Anatom-a-de-Etiqueta.png)

Las principales partes de nuestro elemento son:

- **La etiqueta de apertura:** consiste en el nombre del elemento (en este caso, p), encerrado entre paréntesis angulares de apertura y cierre. Esta etiqueta de apertura marca dónde comienza el elemento o comienza a tener efecto. En este ejemplo, precede al comienzo del texto del párrafo.
- **El contenido:** Este es el contenido del elemento. En este ejemplo, es el texto del párrafo.
- **La etiqueta de cierre:** Es lo mismo que la etiqueta de apertura, excepto que incluye una barra diagonal antes del nombre del elemento. Esto indica dónde termina el elemento; en este caso, dónde finaliza el párrafo.

# Elementos anidados

Se pueden poner elementos dentro de otros elementos. Esto se llama anidamiento. Si quisiéramos decir que nuestro gato es **muy gruñón**, podríamos encerrar la palabra muy en un elemento `<strong>` para que aparezca destacada.

```html
<p>Mi gato es <strong>muy</strong> gruñón.</p>
```
Los elementos tienen que abrirse y cerrarse correctamente para que estén claramente dentro o fuera el uno del otro. Con el tipo de superposición en el ejemplo anterior, el navegador tiene que adivinar tu intención. Este tipo de adivinanzas puede producir resultados inesperados.

# Elementos en línea y bloque

Hay dos categorías importantes de elementos en HTML — Estos son los elementos de bloque y los elementos en línea.

- Los elementos de bloque forman un bloque visible en la página. Aparecerán en una línea nueva después de cualquier contenido anterior. Cualquier contenido que vaya después también aparecerá en una línea nueva. Los elementos a nivel de bloque suelen ser elementos estructurales de la página. 
  
  Por ejemplo, un elemento a nivel de bloque puede representar encabezados, párrafos, listas, menús de navegación o pies de página. Un elemento a nivel de bloque no estaría anidado dentro de un elemento en línea, pero podría estar anidado dentro de otro elemento a nivel de bloque.

- Los elementos en línea están contenidos dentro de elementos de bloque y delimitan solo pequeñas partes del contenido del documento; (no párrafos enteros o agrupaciones de contenido) Un elemento en línea no hará que aparezca una nueva línea en el documento. 
  
  Suele utilizarse con texto. Por ejemplo es el caso de un elemento `<a>` (hipervínculo) o elementos de énfasis como `<em>` o `<strong>`.

# Elementos vacíos

No todos los elementos siguen el patrón de etiqueta de apertura, contenido y etiqueta de cierre. Algunos elementos consisten solo en una etiqueta única, que se utiliza generalmente para insertar/incrustar algo en el documento en el lugar donde se le quiere incluir. Por ejemplo, el elemento <img> inserta una imagen en la página:

```html	
<img src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png">
```	

![imagen de ejemplo](https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png)

# Atributos

Los elementos también pueden tener atributos. Los atributos tienen este aspecto:

![ilustración de atributo](https://mdn.mozillademos.org/files/11915/htmlatributos.png)

Los atributos contienen información extra sobre el elemento que no se mostrará en el contenido. En este caso, el atributo class asigna al elemento un identificador que se puede utilizar para dotarlo de información de estilo.

Un atributo debería tener:

- Un espacio entre este y el nombre del elemento. (Para un elemento con más de un atributo, los atributos también deben estar separados por espacios).
- El nombre del atributo, seguido por un signo igual.
- Un valor del atributo, rodeado de comillas de apertura y cierre.

# Anatomía de un documento HTML

Los elementos HTML no son muy útiles por sí mismos. Ahora veremos cómo combinar los elementos individuales para formar una página HTML completa:

```html	
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Mi página de prueba</title>
  </head>
  <body>
    <p>Esta es mi página</p>
  </body>
</html>
```	

Aquí tenemos:

- `<!DOCTYPE html>`: El elemento doctype. En sus inicios, cuando el HTML llevaba poco tiempo (alrededor de 1991-1992), los doctypes servían como enlaces al conjunto de reglas que la página HTML debía seguir para que fuera considerado buen HTML. Un elemento doctype de aquella época podía parecerse a esto:

  ```html	
  <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
  ```

  En la actualidad se ignora y se considera un legado histórico que hay que incluir para que todo funcione correctamente.
- `<html></html>`: El elemento `<html>`. Este elemento envuelve todo el contenido de la página. A veces se lo conoce como el elemento raíz.
`<head></head>`: El elemento `<head>` (cabecera). Este elemento actúa como contenedor para todos los parámetros que quieras incluir en el documento HTML que no serán visibles a los visitantes de la página. Incluye cosas como palabras clave y la descripción de la página que quieras mostrar en los resultados de búsqueda, así como la hoja de estilo para formatear nuestro contenido, declaraciones de codificación de caracteres y más.
- `<meta charset="utf-8">:` Este elemento establece que tu documento HTML usará la codificación UTF-8, que incluye la gran mayoría de caracteres de todos los idiomas humanos escritos. En resumen: puede gestionar cualquier contenido textual que pongas en tu documento. No hay razón para no configurar este valor y te puede ayudar a evitar problemas más adelante.
- `<title></title>`: El elemento `<title>`. Este establece el título de la página, que es el título que aparece en la pestaña del navegador en la que se carga la página. El título de la página también se utiliza para describir la página cuando se marca como favorita.
- `<body></body>`: El elemento `<body>`. Contiene todo el contenido que quieres mostrar a los usuarios cuando visitan tu página, ya sea texto, imágenes, vídeos, juegos, pistas de audio reproducibles o cualquier otra cosa.

# Referencias a entidades: Inclusión de caracteres especiales en HTML

En HTML, los caracteres `<`, `>`,`"`,`'` y & son caracteres especiales. Forman parte de la sintaxis HTML. Entonces, ¿cómo incluye uno de estos caracteres especiales en tu texto? Por ejemplo, si deseas utilizar un signo comercial o menor que, y no hacer que se interprete como código.

Haces esto con referencias de caracteres. Estos son códigos especiales que representan caracteres, para ser usados en estas circunstancias exactas. Cada referencia de caracter comienza con un signo de ampersand (&) y finaliza con un punto y coma (;).

# Comentarios

En HTML hay un mecanismo para escribir comentarios en el código. Los comentarios son ignorados por el navegador y, por tanto, son invisibles para el usuario. El propósito de los comentarios es permitirte incluir notas en el código para explicar tu lógica o codificación. Esto es muy útil si regresas a un código base después de estar ausente el tiempo suficiente como para no recordarlo por completo. Del mismo modo, los comentarios son invaluables ya que diferentes personas están realizando cambios y actualizaciones.

Para convertir en un comentario una sección de contenido de tu archivo HTML, debes delimitarlo con los marcadores especiales <!-- y -->. Por ejemplo:

```html
<p>No soy un comentario</p>

<!-- <p>¡Yo sí!</p> -->	
```

# Metadatos

El elemento `<head>` de un documento HTML es la parte que no se muestra en el navegador cuando se carga la página. Contiene información como el título de la página, enlaces al CSS, ersonalizar icono, y otros metadatos (datos sobre el HTML, como quién lo escribió y palabras claves importantes que describen el documento).

```html	
<head>
  <meta charset="utf-8">
  <title>Mi página de prueba</title>
</head> 
```

En páginas más grandes, sin embargo, la cabecera puede llegar a contener bastantes elementos. Prueba a ir a algunos de tus sitios web favoritos y comprueba el contenido de la cabecera usando las herramientas para el desarrollador.

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

# Encabezados y parrafos

La mayor parte del texto estructurado está compuesto por encabezados y párrafos, independientemente de si lees una historia, un periódico, un libro de texto, una revista, etc.

En HTML, cada párrafo tiene que estar delimitado por un elemento `<p>`, como en este ejemplo:

```html
<p>Soy un párrafo, ¡desde luego que lo soy!</p>
```

Cada sección tiene que estar delimitada por un elemento de encabezado:

```html
<h1>Yo soy el título de la historia</h1>
```

Hay seis elementos de encabezado: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` y `<h6>`. Cada elemento representa un nivel de contenido diferente en el documento; `<h1>` representa el título principal, `<h2>` representa el subtítulo, `<h3>` representa el subtítulo del subtítulo, y así sucesivamente.

## Estructura jerárquica

Por ejemplo, en esta historia, `<h1>` representa el título de la historia, `<h2>` representará el título de cada capítulo y `<h3>` las diferentes secciones del capítulo, y así sucesivamente.

```html	
<h1>El agujero aplastante</h1>

<p>Por Chris Mills</p>

<h2>Capítulo 1: La oscura noche</h2>

<p>Era una noche oscura. En algún lugar, un búho ululó. La lluvia azotó el ...</p>

<h2>Capítulo 2: El silencio eterno</h2>

<p>Nuestro protagonista ni susurrar pudo al ver esa sombría figura ...</p>

<h3>El espectro habla</h3>

<p>Habían pasado varias horas más, cuando de repente el espectro se incorporó y exclamó: "¡Por favor, ten piedad de mi alma!"</p>
```	

### Reglas a considerar

- Preferentemente debes usar solo un `<h1>` por página; este es el nivel de título superior, y todos los demás se sitúan por debajo de él en la jerarquía.

- Asegúrate de que usas los títulos en el orden correcto en la jerarquía. No uses los `<h3>` para representar subtítulos, seguidos de los `<h2>` para representar los subtítulos de los subtítulos; eso no tiene sentido y provocará resultados extraños.

- De los seis niveles de títulos disponibles, debes procurar no usar más de tres por página, a menos que creas que es realmente necesario. Los documentos con muchos niveles (es decir, una jerarquía de títulos muy profunda) son de difícil manejo y navegación. En esos casos se recomienda, si es posible, separar el contenido en varias páginas.

### ¿Porque necesitamos una jerarquía de títulos?

Esto se debe a que no hay elementos que den estructura al contenido, por lo que el navegador no sabe qué es un encabezado y qué es un párrafo. Además:

- Los usuarios que miran una página web tienden a escanearla rápidamente para encontrar el contenido relevante que hay en ella y a menudo empiezan por leer los encabezados para comenzar. (Solemos pasar muy poco tiempo en una página web). Si no pueden ver nada útil en unos segundos, es probable que se sientan frustrados y se vayan a otro sitio.

- Los motores de búsqueda que indizan tu página consideran el contenido de los títulos como palabras clave importantes e influyen en la puntuación de búsqueda de la página. Sin encabezados, tu página tendrá un rendimiento bajo en términos de optimización de motores de búsqueda SEO.

- Las personas con discapacidad visual severa no suelen leer páginas web: en lugar de ello, las escuchan. Lo hacen con un software llamado Lector de pantalla. Este software proporciona acceso rápido a un contenido textual dado. Entre las diversas técnicas que emplean, leen los encabezados para proporcionar un esquema del documento que permite a los usuarios encontrar rápidamente la información que quieren. Si no hay encabezados disponibles, se ven obligados a escuchar el documento entero.

- Para aplicar estilos al contenido con CSS, o para que haga cosas interesantes con JavaScript, necesitas tener elementos que delimiten el contenido relevante para que CSS/JavaScript se puedan focalizar en este efectivamente.

# Listas

Las listas están en todos lados en la web también y hay tres diferentes tipos de las que nos vamos a ocupar.

## Listas no ordenadas

Las listas no ordenadas se usan para marcar listas de artículos cuyo orden no es importante.

Vease una lista de compras:

```html
Leche
Huevos
Pan
Aceite
Sal
```
Cada lista desordenada comienza con un elemento `<ul>` («unordered list») que delimita todos los elementos de la lista:

```html	
<ul>
  Leche
  Huevos
  Pan
  Aceite
  Sal
</ul>
```

El siguiente paso es delimitar cada artículo de la lista con un elemento `<li>` («list item»).

```html
<ul>
  <li>Leche</li>
  <li>Huevos</li>
  <li>Pan</li>
  <li>Aceite</li>
  <li>Sal</li>
</ul>
```

Vamos a codepen y veamos cómo se ve la lista.

Las listas ordenadas son aquellas en las que el orden de los elementos sí importa. Tomemos como ejemplo una lista de instrucciones para seguir un itinerario:

```html
Conduce hasta el final de la calle
Gira a la derecha
Sigue derecho por las dos primeras glorietas
Gira a la izquierda en la tercer glorieta
El colegio está a la derecha, 300 metros más adelante
```

La estructura de marcado es la misma que para las listas no ordenadas, excepto que debes delimitar los elementos de la lista con una etiqueta `<ol>` («ordered list»), en lugar de `<ul>`:

```html
<ol>
  <li>Conduce hasta el final de la calle</li>
  <li>Gira a la derecha</li>
  <li>Sigue derecho por las dos primeras glorietas</li>
  <li>Gira a la izquierda en la tercer glorieta</li>
  <li>El colegio está a tu derecha, 300 metros más adelante</li>
</ol>
```
# Listas anidadas

Es perfectamente correcto anidar una lista dentro de otra. Posiblemente quieras tener subelementos bajo elementos de rango superior. Por ejemplo en el caso de una lista de una receta:

```html
<ol>
  <li>Pela el ajo y picarlo en trozos gruesos.</li>
  <li>Retira las semillas y el tallo del pimiento, y cortarlo en trozos gruesos.</li>
  <li>Mete todos los alimentos en un procesador de alimentos.</li>
  <li>Procesa todos los ingredientes hasta conseguir una pasta.
    <ul>
      <li>Si deseas un hummus "grueso", procésalo corto tiempo.</li>
      <li>Pica durante más tiempo si se desea obtener un hummus "suave".</li>
    </ul>
  </li>
</ol>

```

# Énfasis e importancia

HTML nos dota de diversos elementos semánticos que nos permiten destacar contenido textual con tales efectos, y en esta sección veremos los más comunes.

## Énfasis

Cuando queremos dar énfasis al lenguaje hablado, acentuamos ciertas palabras y así alteramos sutilmente el significado de lo que decimos.

Me alegro de que no llegues tarde.

Me *alegro* de que no llegues *tarde*.

En HTML usamos el elemento `<em>` («emphasis») para marcar estos casos. El documento logra entonces transmitir una lectura más interesante y además así lo reconocen los lectores de pantalla, que lo expresan con un diferente tono de voz.

```html
<p>Me <em>alegro</em> de que no llegues <em>tarde</em>.</p>
```

El navegador, de manera predeterminada, aplica el estilo de letra itálica, pero no debes utilizar esta etiqueta solamente para establecer el estilo de letra itálica. Para usar ese estilo, debes utilizar únicamente la etiqueta del elemento `<span>` y algo de CSS u otra etiqueta con el elemento `<i>` (ve abajo).

## Fuerte importancia

Para enfatizar palabras importantes al hablar solemos acentuarlas, y al escribir lo hacemos en estilo negrita. Por ejemplo:

Este líquido es **altamente tóxico**.

Cuento contigo. **¡No llegues tarde!**

En HTML usamos el elemento `<strong>` (importancia fuerte) para marcar tales expresiones. El documento resulta entonces más útil, y de nuevo los lectores de pantalla reconocen estos elementos y el tono de voz cambia a uno más fuerte. El estilo negrita es el que aplican los navegadores por omisión, pero no debes usar esta etiqueta solamente para aplicar este estilo. Para hacer eso usa el elemento `<span>` y CSS, o un elemento `<b>` (ve más abajo).

```html
<p>Este líquido es <strong>altamente tóxico</strong>.</p>

<p>Cuento contigo. <strong>¡No llegues tarde!</strong></p>
```

Puedes anidar elementos de énfasis dentro de elementos de importancia y viceversa si lo deseas:

```html
<p>Este líquido es <strong>altamente tóxico</strong> —
si lo bebes, <strong>podrías <em>morir</em></strong>.</p>
```
## Cursiva, negrita, subrayado...

Los elementos que hemos comentado hasta ahora tienen asociada una semántica clara. La situación con `<b>` (negrita o «bold»), `<i>` (cursiva o «italic») y `<u>` (subrayado o «underline») es algo más complicada. Surgieron para que las personas pudieran escribir textos en negrita, cursiva o subrayado en un tiempo en el que pocos navegadores o ninguno admitían el CSS. 

```html
<!-- nombres científicos -->
<p>
  El colibrí garganta de rubí (<i>Archilochus colubris</i>)
  es el colibrí más común en el este de América del Norte.
</p>

<!-- extranjerismos -->
<p>
  El menú era un mar de palabras exóticas como <i lang="uk-latn">vatrushka</i>,
  <i lang="id">nasi goreng</i> y <i lang="fr">soupe à l'oignon</i>.
</p>

<!-- un error ortográfico reconocido -->
<p>
  Algún día aprenderé a deletrear mejor.
</p>

<!-- Palabras clave destacadas en una serie de instrucciones -->
<ol>
  <li>
    <b>Corta</b> dos piezas de la hogaza de pan.
  </li>
  <li>
    <b>Inserta</b> una rodaja de tomate y una hoja de
    lechuga entre las rebanadas de pan.
  </li>
</ol>
```

También pueds ver: [Formateo de texto avanzado]([https://](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting))

# ¿Qué es un hipervínculo?

 Los hipervínculos nos permiten vincular documentos a otros documentos o recursos, vincular a partes específicas de documentos o hacer que las aplicaciones estén disponibles en una dirección web.

 El sitio web de la BBC, por ejemplo, contiene una gran cantidad de enlaces que apuntan a multitud de noticias en diferentes zonas de el sitio (funcionalidad de navegación), zonas de acceso/registro (herramientas de usuario) y otras.

 [ejemplo de enlaces de la BBC](https://mdn.mozillademos.org/files/12405/bbc-homepage.png)

 ## Anatomía de un enlace

 Un enlace básico se crea incluyendo el texto, que queramos convertir en un enlace usando un elemento ancla `<a>`, dándole un atributo `href` que contendrá la dirección web hacia dónde queremos que apunte el enlace.

```html
<p>Crea un enlace a <a href="https://www.mozilla.org/es-ES/">la página de inicio de Mozilla</a>.</p>
```

Crea un enlace a [la página de inicio de Mozilla]([https://](https://www.mozilla.org/es-ES/))

## Añadir información de asistencia con el atributo `title`

Otro atributo que posiblemente quieras agregar a tus enlaces es title. El título contiene información adicional sobre el enlace, como qué tipo de información contiene la página o cosas que debes tener en cuenta en el sitio web.

```html
<p>Crea un enlace a <a href="https://www.mozilla.org/es-ES/" title="El mejor lugar para encontrar más información acerca de la misión de Mozilla y cómo contribuir">la página de inicio de Mozilla</a>.</p>
```

Este código producirá el siguiente resultado (el título se mostrará al pasar el ratón sobre el texto del enlace):

Crea un enlace a [la pagina de inicio de Mozilla]([https://](https://www.mozilla.org/es-ES/)).

## Convertir bloques de contenido en enlaces

Como hemos mencionado anteriormente, puedes convertir cualquier contenido en un enlace, incluso Elementos de bloque y elementos en línea. Si quieres convertir una imagen en un enlace, simplemente usa el elemento `<a>` encerrando el elemento `<img>` entre `<a>` y `</a>`.

```html
<a href="https://www.mozilla.org/es-ES/">
  <img src="mozilla-image.png" alt="Logotipo de Mozilla que dirige a la página inicial de Mozilla">
</a>
```

## Fragmentos de documento

Es posible apuntar hacia una parte concreta de un documento HTML en vez de a todo un documento. Para ello hay que asignar previamente un atributo `id` al elemento hacia el que apuntamos. Esto se debe hacer en el encabezado y quedará así:

```html
<h2 id="Dirección_de_envío">Dirección de envío</h2>
```

Posteriormente para hacer referencia a este id concreto, lo añadiremos seguido de una almuadilla.

```html
<p>La <a href="#Dirección_de_envío">Dirección de envío de la empresa</a> se encuentra al final de esta página.</p>
```

# Imágenes

Para poner una imagen simple en una página web, utilizamos el elemento `<img>`. Se trata de un elemento vacío (lo que significa que no contiene texto o etiqueta de cierre) que requiere de por lo menos de un atributo para ser utilizado: `src`

El atributo `src` contiene una ruta que apunta a la imagen que quieres poner en la página, que puede ser una URL relativa o absoluta, de la misma forma que el elemento `<a>` contiene los valores del atributo `href`.

Por ejemplo, si tu imagen se llama `dinosaur.jpg`, y está en el mismo directorio que tu página HTML, deberás incrustar la imagen de la siguiente manera:

```html
<img src="dinosaur.jpg">
```

Si la imagen estaba en el subdirectorio images, que estaba en el mismo directorio que la página HTML (lo que Google recomienda con fines de indización y posicionamiento en buscadores SEO), entonces deberías incrustar la imagen así:

```html
<img src="images/dinosaur.jpg">
```

Puedes incrustar la imagen usando la URL absoluta, por ejemplo:


```html
<img src="https://www.example.com/images/dinosaur.jpg">
```

Pero esto no tiene sentido, solo hace que el navegador trabaje más buscando la dirección IP desde el servidor DNS cada vez, etc. Casi siempre mantendrás las imágenes para tu sitio web en el mismo servidor de tu HTML.

![Resultado gráfico del ejemplo](https://mdn.mozillademos.org/files/12700/basic-image.png)

## Texto alternativo

El próximo atributo que veremos es  alt. Su valor debe ser una descripción textual de la imagen para usarla en situaciones en que la imagen no puede ser vista/mostrada o tarde demasiado en mostrarse por una conexión lenta a internet. 

Por ejemplo, nuestro código anterior podría modificarse así:

```html
<img src="images/dinosaur.jpg" alt="La cabeza y el torso de un esqueleto de dinosaurio; tiene una cabeza grande con dientes largos y afilados">
```

La forma más fácil de probar el texto `alt` es escribir mal el nombre de archivo. Si, por ejemplo, escribimos el nombre archivo de nuestra imagen como `dinosooooor.jpg`, el navegador no podrá mostrar la imagen, en su lugar mostrará el texto alternativo:

¿Por qué vas a ver o necesitar el texto alternativo? Puede ser por varias razones:

- El usuario tiene alguna discapacidad visual y utiliza un lector de pantalla para leer el contenido de la web. De hecho, disponer de texto alternativo para describir las imágenes es útil para la mayoría de los usuarios.
- Como ya hemos dicho anteriormente, es posible que se haya escrito mal el nombre del archivo o su ruta.
- El navegador no admite el tipo de imagen. Algunas personas aún usan navegadores de solo texto, como Lynx, que muestran el texto del atributo alt.
- Quieres que los motores de búsqueda puedan utilizar este texto. Por ejemplo, los motores de búsqueda pueden hacer coincidir el texto alternativo con la consulta de búsqueda.
- Los usuarios han desactivado las imágenes para reducir el volumen de transferencia de datos y de distracciones. Esto sucede especialmente en teléfonos móviles y en países en que el ancho de banda es limitado y caro.

## Anchura y altura

Puedes usar los atributos  ancho (`width`) y alto (`height`) para especificar la anchura y altura de tu imagen. Puedes encontrar el ancho y el alto de tu imagen de diversas maneras.
```html
<img src="images/dinosaur.jpg"
     alt="La cabeza y el torso de un esqueleto de dinosaurio;
           tiene una cabeza grande con dientes largos y afilados"
     width="400"
     height="341">
```

Esto no proporciona una gran diferencia en la pantalla en circunstancias normales. Pero si la imagen no se muestra, por ejemplo, porque el usuario acaba de acceder a la página y esta aún no se ha cargado, observarás que el navegador reserva un espacio para la imagen:

![Ejemplo donde se visualiza una imagen que no fue cargada y un recuadro del tamaño en que fueron establecidas la imágen](https://mdn.mozillademos.org/files/12706/alt-text-with-width-height.png)

## Comentar imágenes con `figure` y `figcaption`

Hay varias formas en que puedes añadir un pie a tu imagen. Por ejemplo, nada te impediría hacer esto:

```html
<div class="figure">
  <img src="images/dinosaur.jpg"
       alt="La cabeza y el torso de un esqueleto de dinosaurio;
           tiene una cabeza grande con dientes largos y afilados"
       width="400"
       height="341">

  <p>Exposición de un T-Rex en el museo de la Universidad de Manchester.</p>
</div>
```

Una solución mejor es utilizar los elementos HTML5 `<figure>` y `<figcaption>`. Estos se crearon exactamente para este propósito: proporcionar un contenedor semántico para las figuras y vincular claramente la figura con el pie. Nuestro ejemplo anterior, podría reescribirse así:

```html
<figure>
  <img src="images/dinosaur.jpg"
       alt="La cabeza y el torso de un esqueleto de dinosaurio;
           tiene una cabeza grande con dientes largos y afilados" width="400"
       height="341">

  <figcaption>Exposición de un T-Rex en el museo de la Universidad de Manchester.</figcaption>
</figure>
```
El elemento `<figcaption>` dice al navegador, o a alguna tecnología de apoyo, que el texto que contiene describe la imagen que está contenida en el elemento `<figure>`.

# ¿Qué son las tablas en HTML?

Las tablas es el elemento del lenguaje HTML que utilizaremos para mostrar información de forma agrupada. Ya sea texto, imágenes, vídeos,…

El elemento table será el que nos ayudará para crear las tablas en HTML.

Un mal uso de las tablas en HTML es el motivo de maquetación, uso que se dió a las tablas en los principios del lenguaje HTML. Algo que hoy en día es una mala práctica. Cambiando por un modelo de maquetación apoyado en capas.

## Crear una tabla en HTML

Para crear una tabla vamos a necesitar conocer, al menos, tres elementos: `table`, `tr` y `td`. Si bien existen otros cuantos que nos permitirán ampliar la funcionalidad de las tablas.

El primer elemento es table. table es el elemento que representa las tablas y será el que agrupe al resto de elementos. Por lo tanto tiene sus etiquetas de inicio y cierre.

```html
<table> ... </table>
```

Siguiendo con la construcción de la tabla el siguiente elemento que necesitamos es `tr`. El elemento `tr` representa a una fila de la tabla. Por lo tanto tendremos tantos elementos `tr` como filas tenga la tabla.

Así, si queremos tener una tabla de tres filas tendremos un código como el que sigue:

```html
<table>
  <tr> ... </tr>
  <tr> ... </tr>
  <tr> ... </tr>
</table>
```

El último elemento que necesitamos conocer es `td`. El elemento `td` es el que representa de una forma unitaria a una celda. Por lo tanto los elementos `tr` tendrán tantos elementos `td` en su interior como celdas contenga la fila.

El contenido que haya entre los elementos `td` será el contenido de la celda.

Una tabla de tres filas por cuatro columnas quedaría de la siguiente forma:

```html
<table>
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
    <td>Fila 1 Columna 4</td>
  </tr>
  <tr>
    <td>Fila 2 Columna 1</td>
    <td>Fila 2 Columna 2</td>
    <td>Fila 2 Columna 3</td>
    <td>Fila 2 Columna 4</td>
  </tr>
  <tr>
    <td>Fila 3 Columna 1</td>
    <td>Fila 3 Columna 2</td>
    <td>Fila 3 Columna 3</td>
    <td>Fila 3 Columna 4</td>
  </tr>
</table>
```

Así con los tres elementos `table`, `tr` y `td` tenemos construida nuestra tabla.

# El elemento `<audio>`

El elemento  `<audio>` funciona exactamente de la misma forma que el elemento `<video>`, con algunas pequeñas diferencias como se describe a continuación. Un ejemplo típico podría ser así:

```html
<audio controls>
  <source src="viper.mp3" type="audio/mp3">
  <source src="viper.ogg" type="audio/ogg">
  <p>Your browser doesn't support HTML5 audio. Here is a <a href="viper.mp3">link to the audio</a> instead.</p>
</audio>
```

Esto ocupa menos espacio que un reproductor de video, ya que no hay un componente visual; solo necesita mostrar los controles para reproducir el audio. Otras diferencias con respecto al video HTML5 son las siguentes:

- El elemento `<audio>` no soporta los atributos  `width`/`height`  — de nuevo, no hay un componente visual, por no que no hay nada a lo que asignar un `width` o `height` (ancho o alto).
-Tampoco es compatible con el atributo  `poster`  — de nuevo, no hay componente visual.

# El elemento `<video>`

El elemento `<video>` nos permite incrustar video fácilmente. Un ejemplo muy simple luce como lo siguiente:


```html
<video src="rabbit320.webm" controls>
  <p>Tu navegador no soporta HTML5 video. Aquí está el <a href="rabbit320.webm">enlace del video</a>.</p>
</video>
```

Las características a notar son:

- `src`: De la misma manera que para el elemento `<img>`, el atributo src (source) contiene una ruta al video que deseas incrustar. Funciona de la misma manera.
- `controls` Los usuarios deben ser capaces de controlar la reproducción de video y audio (esto es especialmente crítico en personas que padecen  epilepsia). Se debe utilizar el atributo controls para incluir la interfaz de control del browser, o construir la nuestra utilizando la JavaScript API apropiada. Como mínimo la interfaz debe incluir una manera de empezar y terminar la reproducción, y ajustar el volumen.
- **El párrafo dentro de la etiqueta**  `<video>`: Se lo llama fallback content (contenido de reserva) — y será mostrado si el browser desde el que se está accediendo a la página no soporta el elemento `<video>`, permitiéndonos proveer un fallback para browsers más antiguos. Puede ser de la manera que se quiera; en este caso proporcionamos un link directo al archivo de video, por lo que el usuario puede al menos acceder de alguna manera, independientemente del browser que esté usando.

![Un reproductor de video simple que muestra un video de un pequeño conejo blanco](https://mdn.mozillademos.org/files/12794/simple-video.png)

## Uso de múltiples formatos para mejorar la compatibilidad

Tomamos el atributo src del tag `<video>` y en su lugar incluimos elementos separados `<source>` que apuntan a sus propias fuentes. En este caso el browser irá a los elementos `<source>` y reproducirá el primero de los elementos que el codec soporte. Incluir fuentes WebM y MP4 debería bastar para reproducir el video en la mayoría de los browsers en estos días.

```html
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Su navegador no soporta video HTML5. Aquí hay un <a href="rabbit320.mp4">enlace al video</a>.</p>
</video>
```

Cada elemento  `<source>`  tambien tiene un atributo `type`. Esto es opcional, pero se recomienda que se incluyan, ya que contienen `MIME types` de los archivos de vídeo y los navegadores pueden leerlos y omitir inmediatamente los vídeos que no tienen. Si no estan incluidos, los navegadores cargarán e intentarán reproducir cada archivo hasta que encuentren uno que funcione, lo que llevará aún más tiempo y recursos.

# Otras características de la etiqueta <video>

```html
<video controls width="400" height="400"
       autoplay loop muted
       poster="poster.png">
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```

`autoplay`: Hace que el audio o el vídeo empiece a reproducirse de inmediato, mientras se carga el resto de la página. Le aconsejamos que no utilice vídeo (o audio) de reproducción automática en sus sitios, ya que los usuarios pueden encontralo molesto.

`loop`: Hace que el vídeo (o audio) comience a reproducirse cada vez que finaliza.Esto puede en ocasiones resultar molesto, así que utilizalo solo si es realmente necesario.

`muted`: Hace que los medios se reproduzcan con el sonido apagado de forma predeterminada.

`poster` La URL de una imagen que se mostrará antes de reproducir el vídeo. Está destinado a ser utilizado para una pantalla de presentación o pantalla publicitaria (miniatura del vídeo).

`preload` Se utiliza para almacenar en búfer archivos grandes; Puede tomar uno de estos tres valores:

- `"none"` no almacena el archivo en el búfer
- `"auto"` almacena el archivo multimedia
- `"metadata"` almacena solo los metadatos del archivo

# HTML Semántico

## Partes básicas de un documento

Las páginas web pueden y se deben diferenciar las unas de las otras, pero todas tienden a contener elementos comunes parecidos. Estos elementos son:

- **Encabezado**: Normalmente formado por una gran franja que cruza la parte superior de la página con un gran título, un logotipo y quizás un lema. Esta parte suele permanecer invariable mientras navegas entre las páginas de un mismo sitio web.

- **Barra de navegación:** Son los enlaces a las secciones principales del sitio web. Normalmente está formada por un menú con botones, enlaces o pestañas. Al igual que el encabezado, este contenido suele permanecer invariable en las diferentes páginas del sitio.
  
  Tener un menú inconsistente en tu página web conducirá a los usuarios a la confusión y frustración. Muchos diseñadores web consideran que el menú de navegación forma parte del encabezado y que no posee un componente individual, aunque no es necesario que sea así; de hecho, algunos argumentan que tener ambos componentes por separado es mejor por motivos de accesibilidad porque los lectores de pantalla pueden leer mejor ambos elementos si están separados.
  
- **Contenido principal:** Es la gran parte central de la página y contiene la mayor parte del contenido particular de una página web concreta; por ejemplo, el video que quieres ver, la narración que quieres leer, el mapa que quieres consultar, los titulares de las noticias, etc.

- **Barra lateral:** Suele incluir algún tipo de información adicional, enlaces, citas, publicidad, etc. Normalmente está relacionada con el contenido principal de la página (por ejemplo, en una página de noticias, la barra lateral podría contener la biografía del autor o enlaces a artículos relacionados), pero en otras ocasiones encontraras elementos recurrentes como un menú de navegación secundario.
  
- **Pie de página:** Es la parte inferior de la página, que generalmente contiene la letra pequeña, el copyright o la información de contacto. Es el sitio donde se coloca la información común (al igual que en el encabezado), pero esta información no suele ser tan importante o es secundaria con respecto a la página en sí misma. El pie también se suele usar para propósitos SEO, e incluye enlaces de acceso rápido al contenido más popular.
  
Una página web semántica se podría parecer a esta:

![Un ejemplo de estructura de sitio web simple con un encabezado principal, menú de navegación, contenido principal, barra lateral y pie de página.](https://mdn.mozillademos.org/files/12417/sample-website.png)

## HTML para dar estructura al contenido

En tu código HTML puedes crear secciones de contenido basadas en su funcionalidad — puedes usar elementos que representen sin ambigüedad las diferentes secciones de contenido descritas, de forma que las tecnologías de accesibilidad y los lectores de pantalla puedan reconocer esos elementos y asistir en tareas como «encontrar el menú de navegación», o «encontrar el contenido principal». 

Hay una serie de consecuencias por no usar la estructura de elementos y semántica adecuada para hacer el trabajo correctamente. HTML dispone de etiquetas adecuadas que puedes usar para establecer estas secciones semánticas, por ejemplo:

- encabezado: `<header>`.
- menú de navegación :`<nav>`.
- contenido principal: `<main>`, con varias subsecciones (además de la barra lateral) representadas por los elementos `<article>`, `<section>`, y `<div>`.
- barra lateral: `<aside>`; a menudo colocada dentro de `<main>`.
- pie de página: `<footer>`.

## Elementos de diseño HTML en detalle

- `<main>` encierra el contenido particular a esta página. Utilizaremos `<main>` solamente una vez para cada página y lo situaremos directamente dentro del elemento `<body>`. Es mejor que no lo anidemos en otros elementos.
- `<article>` encuadra un bloque de contenido que tiene sentido por sí mismo aparte del resto de la página (por ejemplo una entrada en un blog).
- `<section>` es parecido al elemento `<article>`, pero se usa más para agrupar cada parte de la página que, por su funcionalidad, constituye una sección en sí misma (por ejemplo un minimapa o un conjunto de titulares y resúmenes). Se considera una buena práctica comenzar cada una de estas secciones con un título de encabezado (`heading`); observa que podemos subdividir artículos (`<article>`) en distintas secciones (`<section>`), o también secciones en distintos artículos, dependiendo del contexto.
- `<aside>` incluye contenido que no está directamente relacionado con el contenido principal, pero que puede aportar información adicional relacionada indirectamente con él (resúmenes, biografías del autor, enlaces relacionados, etc.).
- `<header>` representa un grupo de contenido introductorio. Si este es «hijo» de un elemento `<body>`, se convertirá en el encabezado principal del sitio web, pero si es hijo de un elemento `<article>` o un elemento `<section>`, entonces simplemente será el encabezado particular de cada sección (por favor, no lo confundas con títulos y encabezados).
- `<nav>` contiene la funcionalidad de navegación principal de la página. Los enlaces secundarios, etc., no entrarán en la navegación.
- `<footer>` representa un grupo de contenido al final de una página.

## Envolturas no semánticas

A veces hay situaciones en las que no encuentras un elemento semántico adecuado para agrupar ciertos elementos o englobar cierto contenido. Podrías querer agrupar ciertos elementos para referirte a ellos como una entidad que comparta cierto CSS o JavaScript. Para casos como esos, HTML dispone del elemento `<div>` y del elemento `<span>`. Preferentemente estos elementos se deberán utilizar con sus atributos (`class`), para conferirles algún tipo de etiquetado que permita determinarlos con facilidad.

`<span>` es un elemento no-semántico que se utiliza en el interior de una línea. Se utiliza cuando no se nos ocurre el uso de ningún otro elemento semántico de texto en el que incluir el contenido, o si no se desea añadir ningún significado específico. Por ejemplo:

```html
<p> El rey volvió ebrio a su habitación alrededor de la 01:00, y sin duda la cerveza no le ayudaba
cuando cruzó tambaleante la puerta <span class="editor-note">[nota del editor: en este instante de la
representación, deberían atenuarse las luces]</span>.</p>
```

En este caso, la nota del editor solo proporciona información extra para el director de la obra; se supone que estos elementos no incluyen contenido extra importante. Para los usuarios sin discapacidad visual, quizás debamos usar CSS para diferenciar sutilmente estas notas del texto principal.

`<div>` es un elemento de bloque no-semántico; lo utilizaras cuando no se te ocurra el uso de otro elemento semántico mejor, o si no deseas añadir ningún significado concreto. Por ejemplo, imagina un carrito de compras que puedes pulsar en cualquier momento durante tu estancia en una tienda virtual:

```html
<div class="shopping-cart">
  <h2>Carrito de compras</h2>
  <ul>
    <li>
      <p><a href=""><strong>Pendientes de plata</strong></a>: $99.95.</p>
      <img src="../products/3333-0985/" alt="Pendientes de plata">
    </li>
    <li>
      ...
    </li>
  </ul>
  <p>Importe total: $237.89</p>
</div>
```

Este no es un elemento lateral (`<aside>`) porque no necesariamente está relacionado con el contenido principal de la página (en realidad quieres que se pueda ver desde cualquier página). Ni siquiera se puede incluir en una sección (`<section>`) porque su contenido no forma parte del contenido principal de la página. Por lo tanto, un elemento `<div>` es el adecuado en este caso. Hemos incluido un encabezado para indicar a los lectores de pantalla donde van a encontrarlo.

# ¿Qué son los formularios web?

Los formularios web son uno de los principales puntos de interacción entre un usuario y un sitio web o aplicación. Los formularios permiten a los usuarios la introducción de datos, que generalmente se envían a un servidor web para su procesamiento y almacenamiento (consulta Enviar los datos de un formulario más adelante en el módulo), o se usan en el lado del cliente para provocar de alguna manera una actualización inmediata de la interfaz (por ejemplo, se añade otro elemento a una lista, o se muestra u oculta una función de interfaz de usuario).

El HTML de un formulario web está compuesto por uno o más controles de formulario (a veces llamados widgets), además de algunos elementos adicionales que ayudan a estructurar el formulario general; a menudo se los conoce como formularios HTML. Los controles pueden ser campos de texto de una o varias líneas, cajas desplegables, botones, casillas de verificación o botones de opción, y se crean principalmente con el elemento `<input>`, aunque hay algunos otros elementos que también hay que conocer.

Los controles de formulario también se pueden programar para forzar la introducción de formatos o valores específicos (validación de formulario), y se combinan con etiquetas de texto que describen su propósito para los usuarios con y sin discapacidad visual.

## Etiqueta `<form>`

Todos los formularios comienzan con un elemento `<form>`, como este:

```html
<form action="/my-handling-form-page" method="post"></form>
```

Este elemento define formalmente un formulario. Es un elemento contenedor, como un elemento <section> o `<footer>`, pero específico para contener formularios; también admite algunos atributos específicos para la configuración de la forma en que se comporta el formulario. Todos sus atributos son opcionales, pero es una práctica estándar establecer siempre al menos los atributos `action` y `method`:

- El atributo `action` define la ubicación (URL) donde se envían los datos que el formulario ha recopilado cuando se validan.
- El atributo `method` define con qué método HTTP se envían los datos (generalmente `get` o `post`)

# Campos de entrada

Son los elementos básicos de un formulario ya que son los que nos permiten recuperar información del usuario de diferentes formas.

El elemento que representa los campos de entrada de datos es input. La estructura básica de un campo de entrada es la siguiente:

```html
<input type="tipo" id="identificador" size="tamaño"
  name="nombre" value="texto por defecto"/>
```

Si vemos los atributos que tiene el elemento input nos encontramos los siguientes:

- `type`, indica el tipo de campo de entrada de datos que vamos a utilizar. Dependiendo del tipo que indiquemos obtendremos un resultado u otro. Los valores que puede tener el atributo type son: “`text`”, “`password`”, “`checkbox`”, “`radio`”, “`submit`”, “`reset`”, “`file`”, “`hidden`”, “`image`” y “`button`”.
- `id`, es el identificador del campo. Es importante ya que será el nombre por el cual podremos identificar, de forma unívoca, al campo.
- `size`, será el tamaño del campo. Es decir, el número de caracteres que podríamos insertar en el campo de texto.
- `name`, es el nombre del campo el cual se enviará desde el formulario al servidor.
- `value`, será el valor por defecto que tendrá el campo de texto y que le aparecerá al usuario al cargar el formulario.
Cuando enviemos el formulario al servidor, se coge el la combinación name=value para ser enviada.

## Campos de texto
El campo de texto, como bien indica su nombre, es el que nos permite insertar texto en un formulario. El usuario podrá insertar texto visible sobre el campo.

En este caso el tipo de elemento input que utilizaremos será “`text`”. Así, para definir un campo de texto lo haremos de la siguiente forma:

```html
<input type="text" id="identificador" size="tamaño"
  name="nombre" value="texto por defecto"/>

```
De esta forma si queremos crear un campo de texto para poder insertar 70 caracteres que contenga un email, lo definiremos de la siguiente forma:

```html
<input type="text" id="email" name="email"
  size="70" value="usuario@dominio.com"/>
```

## Contraseñas
Cuando un usuario inserte una contraseña dentro de un formulario necesitaremos, casi seguro, que el valor de la contraseña no aparezca y que por el contrario aparezcan caracteres como asteriscos.

Para insertar un campo que acepte contraseñas dentro de un formulario vamos a utilizar un tipo “`password`” dentro del elemento `input`.

```html
<input type="password" id="identificador" size="tamaño" name="nombre"/>
```

En este caso, aunque podemos poner un valor por defecto, si bien, no parece tener mucho sentido. Si queremos definir un campo que acepte contraseñas de 20 caracteres lo codificaremos de la siguiente forma:

```html
<input type="password" id="clave" name="clave" size="20"/>
```

## Checkbox
Un checkbox nos permite capturar un dato del usuario mediante un elemento de check. El check puede tener dos valores, seleccionado o no seleccionado. El tipo del elemento input que utilizaremos será “`checkbox`”. Así lo definiremos de la siguiente forma:

```html
<input type="checkbox" id="identificador" name="nombre"/>
```
En el caso del checkbox no tienen sentido el atributo tamaño ni el valor por defecto. Ya que, recordemos que solo podemos tener el check seleccionado o no. Pero lo que sí podemos hacer es generar un checkbox que esta preseleccionado. Para ello utilizamos el atributo checked.

```html
<input type="checkbox" id="identificador" name="nombre" checked="checked"/>
```

Pero ¿dónde está el texto que acompaña al checkbox? Realmente el checkbox no tiene definido que acompañe al checkbox. Si no que hay que añadir el texto directamente al lado del checkbox.

```html
<input type="checkbox" id="identificador" name="nombre" checked="checked"/>
```

## Texto del checkbox
Aunque más adelante vamos a ver una forma más correcta de asociar el texto al checkbox.

Así, si queremos crear un checkbox que nos pregunte si estamos de acuerdo con unas condiciones podríamos codificarlo de la siguiente forma:

```html
<input type="checkbox" id="condiciones" name="condiciones"/>Está de acuerdo con las condiciones explicadas más arriba.
```

Los checkbox suelen ir en grupos para seleccionar varias opciones. Por ejemplo podríamos tener el siguiente código con el que podamos seleccionar qué lenguaje de programación queremos aprender.

```html
<input type="checkbox" name="lenguaje" value="html">HTML
<input type="checkbox" name="lenguaje" value="javascript">Javascript
<input type="checkbox" name="lenguaje" value="css">CSS
<input type="checkbox" name="lenguaje" value="xml">XML
```

## Radios
Con los elementos de radio podemos ofrecer un conjunto de opciones al usuario de tal manera que solo pueda elegir una de ellas. El tipo de elemento input que utilizamos es “`radio`”.

La sintaxis que seguiremos en los elementos input de tipo radio será la siguiente:

```html
<input type="radio" id="identificador" value="valor" name="nombre"/>
```

En el caso de los elementos radio toma un papel principal el atributo name. Ya que para poder agrupar opciones deberemos de tener el mismo valor de atributo name.

Así, si queremos crear un grupo de radios para que nos elija una edad le podremos crear de la siguiente forma:

```html
<input type="radio" id="menos18" value="menos18" name="edad"/>Menos de 18
<input type="radio" id="18a30" value="18a30" name="edad"/>18 a 30
<input type="radio" id="31a50" value="31a50" name="edad"/>31 a 50
<input type="radio" id="mas50" value="mas50" name="edad"/>Más de 50
```

Al igual que sucedía con los campos de entrada de tipo check, podemos cargar campos de tipo radio en nuestro formulario con un elemento preseleccionado. Para ello volvemos a recurrir al atributo checked.

```html
<input type="radio" id="identificador" value="valor" name="nombre" checked="checked"/>
```

## Ficheros
Cuando diseñemos un formulario es posible que necesitemos enviar un fichero de datos al servidor. En este caso el campo de entrada de datos nos tiene que dar la posibilidad de acceder al sistema de fichero del dispositivo para poder seleccionar uno.

En este caso vamos a necesitar un campo de entrada de tipo “`file`”. La sintaxis de los campos de entrada para tipos file sería:

```html
<input type="file" id="identificador" value="valor" name="nombre"/>
```

## Campos Ocultos
Otra de las opciones que nos podemos encontrar dentro de los formularios es con la necesidad de enviar información oculta. Es decir, información que tiene que ir anexa al formulario pero que no necesita ser introducida por el usuario. Para ello tenemos la posibilidad de crear campos de datos ocultos.

La sintaxis para los campos de entrada ocultos es:

```html
<input type="hidden" id="identificador" value="valor" name="nombre"/>
```

En estos casos el campo valor siempre va relleno, ya que no hay otra forma de que el usuario le asigne un valor.

## Imágenes
Uno de los tipos de elementos input es el tipo “`image`”. Mediante el tipo “`image`” podemos crear un botón de envío que sea una imágen. La imagen se cargará mediante el atributo src. La estructura para elementos input de este tipo es:

```html
<input type="image" src="url-image" name="nombre" alt="texto-alternativo"/>
```

Como sucede cada vez que manipulamos imágenes hay que rellenar el atributo `alt` con un texto alternativo por motivos de accesibilidad.

## Áreas de texto
Un elemento algo más avanzado que el campo de entrada de datos es el área de texto. Mediante un área de texto tenemos la capacidad de que el usuario inserte una gran cantidad de datos y además que esos datos puedan estar en diferentes líneas.

Para poder insertar un área de texto en nuestro formulario utilizamos el elemento textarea. La sintaxis del elemento textarea será la siguiente:

```html
<textarea rows="numerofilas" cols="numerocolumnas" name="nombre"></textarea>
```

A diferencia del elemento input, el textarea tiene una etiqueta de inicio y una de fin.

Los atributos que nos encontramos en un textarea son:

- rows, indica el número de filas que tiene el área de texto.
- cols, indica el número de columnas que tiene el área de texto.
- name, al igual que sucede con otros elementos del formulario, name contiene el nombre del campo, el cual será enviado al servidor para ser procesado.
  
De esta forma, si queremos crear un área de texto de 20 filas por 100 columnas en el que un usuario pueda insertar un comentario tendríamos el siguiente código:

```html
<textarea rows="20" cols="100" name="comentario"></textarea>
```

Si queremos que el área de texto vaya con un valor por defecto, tendremos que añadir dicho contenido entre las etiquetas de textarea.

```html
<textarea rows="20" cols="100" name="comentario">Contenido de comentario...</textarea>
```

# Combos de opciones

Otro elemento que podemos insertar dentro de un formulario es un combo de opciones. Es decir, un elemento en el que el usuario pueda elegir un elemento o varios de una lista.

El elemento que nos permite insertar un combo de opciones es select. La sintaxis básica de un elemento `select` es:

```html
<select name="nombre" size="valoresvisibles" multiple="multiple">
</select>
```

De los valores que nos encontramos en el elemento select destacamos:

- `name`, que al igual que en anteriores casos sirve para dar un nombre al campo que se enviará al servidor.
- `size`, indica el número de opciones que aparecen visibles por defecto. En el caso de que haya más opciones que las elegidas por defecto lo que nos aparecerá será un scroll para poder localizar todas.
- `multiple`, este atributo nos servirá para poder elegir varias de las opciones. Es decir, para tener una elección múltiple.
  
Como hemos visto el elemento select sólo demarca el combo de las opciones. Para definir cada una de las opciones tenemos el elemento option.

La sintaxis básica del elemento option es la siguiente:

```html
<option label="etiqueta" value="valor"></option>
```

Dónde el atributo `label` indica el texto que aparecerá para poder ser seleccionado en el combo y value el valor realmente de ese item. En el caso de que no pongamos el atributo `label` o el atributo `value`, el valor que cogerán dichos atributos será el texto que encontremos entre los elementos de option.

Por lo tanto, si juntamos la sintaxis del elemento `select` y el elemento option tenemos la siguiente codificación:

```html
<select name="nombre" size="valoresvisibles" multiple="multiple">
  <option label="etiqueta" value="valor"></option>
</select>
```

Si queremos crear un combo de opciones donde podamos elegir un equipo de fútbol tendríamos el siguiente código:

```html
<select>
  <option>Atlético de Madrid</option>
  <option>Real Betis</option>
  <option>FC. Barcelona</option>
  <option>Real Madrid</option>
  <option>Zaragoza</option>
</select>
```

Si queremos que una de las opciones del combo vaya marcada recurriremos al atributo `selected`. Así, en nuestro ejemplo si marcamos como predefinido el equipo del Betis tendríamos el siguiente código:

```html
<select>
  <option>Atletico de Madrid</option>
  <option selected="selected">Betis</option>
  <option>FC. Barcelona</option>
  <option>Real Madrid</option>
  <option>Zaragoza</option>
</select>
```

Otra de las cosas que podemos realizar dentro de un combo es agrupar opciones. Si la lista de opciones es muy grande podemos utilizar el elemento optgroup.

La sintaxis del elemento optgroup es la siguiente:

```html
<optgroup label="etiqueta"></optgroup>
```

Dentro del elemento optgroup encontraremos todos los elementos option que queramos agrupar.

Si por ejemplo, queremos ofrecer un combo de ciudades y las queremos agrupar por continentes, tendríamos el siguiente código:

```html
<select name="ciudad">
  <optgroup label="Europa">
    <option>Madrid</option>
    <option>Londres</option>
    <option>Paris</option>
  </optgroup>
  <optgroup label="Suramerica">
    <option>Santiago</option>
    <option>Sao Paulo</option>
    <option>Lima</option>
    <option>Bogota</option>
  </optgroup>
    <optgroup label="Africa">
    <option>Casablanca</option>
    <option>Ciudad del Cabo</option>
  </optgroup>
</select>
```
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
