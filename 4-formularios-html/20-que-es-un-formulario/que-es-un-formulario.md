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
