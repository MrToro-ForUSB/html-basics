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

