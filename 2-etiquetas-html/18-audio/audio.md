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


