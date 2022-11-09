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
