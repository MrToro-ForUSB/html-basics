# Anatomía de un documento HTML

Los elementos HTML no son muy útiles por sí mismos. Ahora veremos cómo combinar los elementos individuales para formar una página HTML completa:

```html	
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Mi página de prueba</title>
  </head>
  <body>
    <p>Esta es mi página</p>
  </body>
</html>
```	

Aquí tenemos:

- `<!DOCTYPE html>`: El elemento doctype. En sus inicios, cuando el HTML llevaba poco tiempo (alrededor de 1991-1992), los doctypes servían como enlaces al conjunto de reglas que la página HTML debía seguir para que fuera considerado buen HTML. Un elemento doctype de aquella época podía parecerse a esto:

  ```html	
  <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
  ```

  En la actualidad se ignora y se considera un legado histórico que hay que incluir para que todo funcione correctamente.
- `<html></html>`: El elemento `<html>`. Este elemento envuelve todo el contenido de la página. A veces se lo conoce como el elemento raíz.
`<head></head>`: El elemento `<head>` (cabecera). Este elemento actúa como contenedor para todos los parámetros que quieras incluir en el documento HTML que no serán visibles a los visitantes de la página. Incluye cosas como palabras clave y la descripción de la página que quieras mostrar en los resultados de búsqueda, así como la hoja de estilo para formatear nuestro contenido, declaraciones de codificación de caracteres y más.
- `<meta charset="utf-8">:` Este elemento establece que tu documento HTML usará la codificación UTF-8, que incluye la gran mayoría de caracteres de todos los idiomas humanos escritos. En resumen: puede gestionar cualquier contenido textual que pongas en tu documento. No hay razón para no configurar este valor y te puede ayudar a evitar problemas más adelante.
- `<title></title>`: El elemento `<title>`. Este establece el título de la página, que es el título que aparece en la pestaña del navegador en la que se carga la página. El título de la página también se utiliza para describir la página cuando se marca como favorita.
- `<body></body>`: El elemento `<body>`. Contiene todo el contenido que quieres mostrar a los usuarios cuando visitan tu página, ya sea texto, imágenes, vídeos, juegos, pistas de audio reproducibles o cualquier otra cosa.