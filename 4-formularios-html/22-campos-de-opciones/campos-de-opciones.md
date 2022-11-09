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