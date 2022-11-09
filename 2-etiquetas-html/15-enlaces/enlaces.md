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

