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