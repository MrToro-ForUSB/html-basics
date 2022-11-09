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