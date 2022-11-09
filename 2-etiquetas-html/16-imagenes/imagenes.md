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
