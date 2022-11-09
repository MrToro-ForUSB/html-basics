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
