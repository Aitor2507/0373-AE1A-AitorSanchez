# Apuntes de lenguajes de marcas

**Índice**   
1. [GitHub](#id1)
2. [Markdown](#id2)
3. [HTML](#id3)

## Github<a name="id1"></a>
Utilizado para el control de versiones, es decir para tener un manejo de registros con los cambios de los diferentes archivos. Por otra parte podemos tener colaboradores y ver tambien los cambios y actualizaciones.
### Creación de cuenta de GitHub

Comenzamos yendo a  esta URL:

![GitHub_web](/fotos/github.PNG "GitHub_web")

Luego de ello vamos a crearnos una cuenta para ello nos pedirá una verificación de correo electrónico.

### Crear repositorio 
Una vez hecho el paso iremos a crear un repositorio dandole aqui:

Le damos un nombre ,lo ponemos en público y le damos a crear:

![GitHub_repo](fotos/github1.PNG "GitHub_repo")

Copiamos el link del github creado:

![GitHub_linkrepo](/fotos/github2.PNG "GitHub_linkrepo")

### Como enlazar un github a un git 

Primeramente hemos de instalarnos el git en su [página oficial](https://git-scm.com/) luego de hecho esto, abriremos el git e iniciaremos sesion en el local de esta manera y nos ubicaremos en la carpeta que queremos enlazar con la de github normalmente para que no haya problemas debemos tener el mismo nombre:

``` bash
git config user.name "en este espacio tu nombre de github"
git config user.email "correo verificado"
git remote add origin " el link que queremos enlazar"

```

Luego cuando tenemos logeado nuestro git con el github  iniciaremos y haremos los diferentes cambios que queramos y al finalizar siempre hemos de hacer estos comandos para que se guarden tanto en el local como en el repositorio enlazado:

``` bash
git init (para empezar)
git add . ( para solo un archivo ponemos en el punto "archivo.txt")
git commit -m "mensaje para explicar lo que se hizo aquí"
git push origin master
git pull origin master (para descargar cambios de repositorio a remoto)

```

Es importante que no se haga solo un commit entero sino que se tenga varios para tener una idea más clara de como se fue estructurando el trabajo.

### Clonar un github a local 
Para clonarlo hemos de situarnos en la carpeta que querramos guardarlo y por último abrimos cmd y escribimos:

```bash
git clone "url_del_github_que_se_quiere_clonar"
```

## Markdown<a name="id2"></a>
Lenguaje marcado para editar documentos de texto como este para que tenga la mayor legibilidad y facilidad de publicación.

### Encabezados
En markdown para los diferentes tamaños de encabezados escribiremos una almohadilla delante del texto que queremos que se vea en un encabezado u otro:

``` markdown
# Primer nivel de encabezado
## Segundo nivel de encabezado
### Tercer nivel de encabezado
#### Cuarto nivel de encabezado
##### Quinto nivel de encabezado
###### Sexto nivel de encabezado
```

### Formato de letras
Para los diferentes formatos de letras tendremos ponerlos entre estos diferents símbolos:

``` markdown
*cursiva*
**negrita**
**_cursiva y negrita_**
```

### Lista y sublistas
En las listas lo ordenaremos por números como se escribe a mano pero aquí para que hayan sublistas se deben tabular de esta manera:

``` markdown
1. Primer punto de la lista ordenado.
    1. Primer elemento de la sublista 1
    2. Segundo elemento de la sublista 1 
2. Segundo punto de la lista.
    2. Segundo elemento de la sublista 1 
3. Tercer punto de la lista.


* Primer punto de la lista desordenada.
- Segundo punto de la lista desordenada.
+ Tercer punto de la lista desordenada.

```

### Mostrar líneas de código en su formato

Para que se muestre de una manera más bonita un código importante pondremos todas las líneas así '''texto de código''', un ejemplo con HTML:

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

### Mostrar links e imágenes 
Para no estar copiando y pegando los enlaces o para que tenga un diseño más bonito los enlaces podemos ponerlo de esta siguiente manera`, por otra parte para mostrar las imágenes solo hemos de poner el mismo formato pero atras de este una exclamación, como:
```
[nombre abreviado del enlace](http://www.limni.net "Tit opcional")	
![Texto alternativo](/ruta/a/la/imagen.jpg "Tit opcional")
```
[nombre abreviado del enlace](https://es.wired.com/articulos/la-onu-crea-consejo-consultivo-de-inteligencia-artificial-un-paso-hacia-su-gobernanza-global "Tit opcional")

![Texto alternativo](/fotos/ia.webp "Tit opcional")

Aqui podemos verlos en ejemplos:

### Tablas 
Para hacer tablas con titulo y diferente información hemo de ponerlos entre estos símbolos || que hacen como referencia a la tabla, aquí les tengo un ejemplo:

|Título 1|Título 2| Título 3|
|-----------|---------:|:------------:|    
|SMX2|Curso 2324|25|
|**ASIX1**|Curso 2425|33|
|DAW2|Curso 2425|32|

Tambien si queremos el titulo lo queremos de un lado u otro hemos de poner otra tabla con guiones y los dos puntos en la izquierda o centrado como en el titulo 2 y 3.

## HTML<a name="id3"></a>
Lenguaje marcado utilizado para la creación de páginas web.Consiste en serie de elementos encerrado en una manera estructurada se comporta de una manera u otra. Ahora veremos los diferentes elementos y atributos en HTML:

###  Etiquetas 
HTML utiliza etiquetas para los diferentes elementos para su intepretación de estas por ello tenemos:
```Etiqueta de apertura -> Nombre de elemento ej. <p> (efecto del elemento párrafo)```

```Etiqueta de cierre -> Indica fin del elemento ej. </p> (fin del efecto del elemento párrafo)```

```Contenido -> Que contiene el elemento ej. texto```

```Elemento -> Lo que constituye etiquetas y contenido ej. <p>esto es un elemento completo</p>```
####  Etiquetas básicas de HTML
#### Etiquetas por diferentes rutas
Para enlazar a otros archivos ya sea un HTML, CSS e imágenes. Especificaremos la ubicación de estos por 2 tipos:
##### Ruta absoluta
Especifica la ubicación completa del archivo web desde el dominio. Útil para enlazar archivos en servidor diferente o ubicación específica de la web. Ej.
```<img src ="https://www.example.com/images/logo.png" alt ="Logo de Example">``` 
##### Ruta relativa
Especifica la ubicación del archivo en relación con la ubicación del documento actual. Útil para mantener estrucutura de enlaces clara dentro de un mismo sitio web. Ej.
```<img src ="images/logo.png" alt ="Logo del sitio">```

Indica que el archivo logo.png esta en el directorio images y este en el mismo directorio  que index.html donde ponemos este código anterior. 
#### Etiquetas para imágenes
Utilizado mucho para las páginas para que sea atractivo. Con la etiqueta '<img>' la cual va sin etiqueta de cierre, se utiliza el src para indicar la ruta de la imagen como anteriormente lo hicimos, alt para el texto alternativo en caso de que en navegador no muestre la imagen indicada.Ej.

```<img src ="media/logo.png" alt ="Logo de la web">```

#### Etiquetas para enlaces
La World Wide Web tiene la capacidad de saltar de una página web a otra por enlaces, llamada esta navegación como hipertexto y se usa con un <a> la cual si tiene la etiqueta de cierre. Por otro lado para indicar el destino del enlace utlizamos el atributo '<href>'
##### Enlaces a páginas externas
Para páginas externas como enlazar nuestra página web y que aparezca con un cierto nombre sería:
```html
<p><a href="https://m.joan23.fje.edu/" title="JonaXXIII">Jesuïtes Bellvitge - Joan XXIII</a></p>
```
##### Enlaces a páginas locales
Para un documento local usamos ruta relativa al archivo que se quiera enlazar el atributo href. Ej.
``` html
<div id="menu">
    <a href="index.html" title="Volver a la página de inicio">Inicio</a>
    <a href="secciones/presentaciones.html" title="Fotos de la web">Presentaciones</a>
<div>
```
#### Etiquetas anticuadas
Podemos encontrar etiquetas que se permite pero se recomienda no  utilizar, son para la presentación del documento y NO estructura. Ej. ``` <b>(negrita),<i>(cursiva), <u>subrayado, <font>(tipo de fuente), <center>(centrado texto)``` 
Y otras que pueden ser para reemplazar el uso de CSS como ```align, border... ```
#### Etiquetas para listas
##### Listas desordenadas
Orden de items no relevante como lista de compras encerradas con un elemento ``` <ul>``` y este se puede indicar el símbolo de tipografía.Ej. 
``` html
<ul type =DISC>
<ul type =SQUARE>
<ul type =CIRCLE>
```
##### Listas ordenadas
Orden de ítemos relevante como una receta con un elemento ``` <ol>``` y este se puede indicar el tipo de enumeración de lista, por defecto numérica.Ej.
``` html
<ol type =A>
<ol type =a>
<ol type =l>
<ol type=i start =10>
<ol type= 1>
```

- Añadiendo el  parámetro start=n fuerza la numeración de un cierto valor.
- Añadiendo el  parámetro value=n fuerza al elemento que tenga el número de orden que indiquemos.
- Cada elemento de la lista se coloca dentro de un elemento '<li>' (lis item).

###  Atributos
Información adicional del elemento, es abstracto cuando se muestra el contenido por lo que los atributos se colocan en la etiqueta de apertura y deben contener:

``` Espacio entre este y nombre del elemento ```

``` Nombre del atributo seguido por un igual ej. <p class = > ```

``` Comillas de apertura y cierre encerrando el valor del atributo ej. <p class ="editor-note" > ```

### Estructura básica de fichero HTML
HTML incluye una declaración DOCTYPE, html, dentro un head y un body. El head consta de metadatos, CSS, scripts y el body todo lo que se mostrara en la web. Para llamarlo sería con un HTML:5 :
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

### Elementos bloque y línea
Dentro del body incluimos todo el contenido web, es decir toda la información web que queramos que se vea para el usuario final. Y serán diferentes elementos con sus atributos para este objetivo.Clasificados en 2 tipos:
#### Elementos de bloque
Grandes estructuras que contiene otros elementos de bloque, elementos de línea o texto.Normalmente el navegador los pone como independientes y separa uno con otro con un salto de línea en blanco. Ej.
```<h1>-<h6> encabezado, <p> párrafo, <br> salto de línea, <hr> separador, <blockquote> (cita),<pre> texto preformateado, <div> división ```
#### Elementos de línea
Son pequeñas estructuras que representa pequeños trozos de texto o datos. Contiene solo texto u otro elementos de línea. Normalmente el navegador muestra los elementos de línea uno detrás de otro, en línea, dentro del elemento bloque que los contiene como hipervínculos, citas o imágenes.Ej.
```<em>(énfasis/cursiva), <strong>(fuerte énfasis/negrita),<q> (citas cortas), <span> (rango), <cite>, <abbr>, <code>```

### Resumen normas básicas de etiquetas HTML

- Normalmente en pares las etiquetas de apertura y cierre. Ej. ```<p></p>```
- Existen etiquetas vacías, sin cierre. Ej.  ```<img>,<br> y <input>```
- Anidación correctamente de las etiquetas HTML. Si una etiqueta ```<b>``` se abre dentro de una etiqueta ```<p>```, se debe cerrar antes de cerrar la etiqueta ```<p>```
- Atributos en etiquetas se especifica en las de apertura Ej. ```<img src="imagen.jpg"> ``` que src especifica la ruta de la imagen.
- Se recomienda escribir en minúsuculas aunque los atributos y elementos funcionen en mayúsuculas. 

### Legibilidad y organización del código
 Claridad con el que se codifica el código fuente, es decir que se entienda de manera fácil y rápida. Por lo que es importante que este código sea legible. Por otro lado, hemos de pensar que la mayoría de códigos serán hechos por dos o más personas.Tenemos varias técnicas para un código legible y organizado:
  - Comentarios
  - Indentación de código
  - Organización de archivos 

### Comentarios
Anotaciones no reflejadas en la web pero útil para el desarrollo web. Ej.
    ``` html
     <!--Esto  es un comentario-->
    ```
 - Utilizado para documentos largos.
 - Indicar secciones como cabecera, menú, columna izquierda, parte central con artículos, pie de página,etc.
### Identación de código
 Para leer de una manera cómoda lo que escribimos se agregar saltos de línea, tabulaciones,etc. Normalmente identaremos para todo código que tenga una etiqueta de inicio y su correspondiente etiqueta de cierre, se ha de realizar siempre excepto si es texto el contenido.Ej.

    ``` html
    <div>
      <p>Esto es el contenido de un párrafo, incluiremos un <a href="https://loquesea.com">enlace externo</a> y  seguimos escribiendo...</p>
    </div>
    ```

### Organización de archivos
 Para una aplicación web  tendremos varios archivos con extensiones incluso repetitivos por lo que es ideal tenerlo organizado por diferentes carpetas por multimedia,estilos. Para el incio de las aplicaciones siempre se pondrá el HTML como 'index.html' para accerder más rápido y sin necesidad de escribirlo.

### Elementos semánticos en HTML 5
Saber usar HTML como puede ser con ```<span>``` agrupa contenidos de línea y ```<div>``` contenido en bloque. Como valor semántico no aporta nada un div  que significa dividir y agrupar contenido en bloques pero "no da pistas" sobre que tipo de elemento estructural contiene pero se le encuentra uno.Ej.```<header>, <footer>, <article>, <section>, <nav> y <figure>```

 ![HTML_semantica](https://github.com/Aitor2507/0373-AE1A-AitorSanchez/blob/main/fotos/github_semantico.PNG "GitHub_semantica")

### Formularios
Interactua con el usuario para que pueda transmitir información, la cual es procesada de diferentes maneras según la web.Cada uno de estos contienen elementos como controles o campos que tienen el atributo name, que identifica que dato se quiere enviar.

### Etiquetas de formulario
#### Input
Utilizado para crear diversos campos interactivos en el formulario.
- type -> Define tipo de entrada que se debe mostrar
- id -> Identificador único para campo, se puede asociar  el ```<label>``` con campo de entrada
- name -> Nombre de campo de entrada
- value -> Valor predeterminado de campo de entrada o valor enviado al servidor si el campo no es interactivo
- placeholder -> Texto que aparece cuando el campo está vacío por lo que ofrece pista sobre el dato que se quiere ingresar
- required -> Indica campo que debe completarse antes de enviar formulario
- disabled -> Desactiva el campo, evitando interacción
- readonly -> Campo solo de lectura, evita modificarse su contenido

Ej. ```<input type="text" />```
#### Form
Utilizado para crear diversos formularios que permite al usuario enviar datos al servidor o realizar acción en la página web.

- action -> Define URL donde envía datos del formulario para su procesamiento, destino que apunta el formulario.
- method -> Método de envío de datos
- enctype -> Define como se codifica los datos antes de ser enviads al servidor comos subir archivos.
- target -> Indica dónde se debe mostrar la respuesta al enviar  el formulario. Pueden ser: _self (respuesta carga en la misma ventana), _blank (respuesta carga en otra ventana)
Ej.
``` html
<form action="process.php" method="POST"
enctype= "multipart/form-data">
    <label for="name">Nombre:</label>
    <input type="text" id="name" name="name">

    <label for="email">Correo electronico:</label>
    <input type="email" id="email" name="email">

    <label for="file">Subir archivo:</label>
    <input type="file" id="file" name="file">

    <button type="submit">Enviar</button>
</form>
```
#### Input type radio y checkbox
- Type radio : Permite selecciones múltiples Ej.
``` html
    <form action="recepcion.php" method="POST">
    <fieldset>
    <legend>Nacionalidad</legend>

        <input type="checkbox" name="nacionalidad" value="España" id="española">
        <label for="española">Española</label>

        <input type="checkbox" name="nacionalidad" value="España" id="francesa">
        <label for="francesa">Francesa</label>

        <input type="checkbox" name="nacionalidad" value="España" id="canadiense">
        <label for="canadiense">Canadiense</label>
    </fieldset>
    <button type="submit">Enviar datos</button>
```
- Type checkbox: Permite agrupar con otros de mismo nombre. Ej,
``` html
  <form action="recepcion.php" method="POST">
        <label for="nombre">Nombre: </label>  <!--Label para nombre-->
        <input type="text" id="nombre" name="nombre" placeholder="Introduce tu nombre"><br><br>

        <label for="password">Password: </label> 
        <input type="password" id="password" name="password" placeholder="Introduce tu contraseña"><br><br>

        <fieldset>
            <legend>Idioma</legend>
            <label for="castellano">Castellano: </label>  <!--Label para idiomas-->
            <input type="radio" name="idioma" value="castellano" id="castellano"> 
    
            <label for="catalan">Catalan: </label>
            <input type="radio" name="idioma" value="catalan" id="catalan"> 
    
            <label for="chino">Chino: </label>
            <input type="radio" name="idioma" value="chino" id="chino"> 
        </fieldset>
```
#### Textarea
Usado para crear área de texto en que usuarios puedan ingresar múltiples líneas de texto, para mensajes largos o descripciones detalladas.
- name -> Especifica nombre de control que se usará para el formulario. Usado como clave en par nombre-valor cuando se envíe datos del formulario del servidor.
- id -> Identificador único del elemento, puede usarse para asociar etiqueta ```<label>```  con área de texto.
- rows -> Define número de líneas visibles en una área de texto y especifica altura de caja.
- cols -> Define número de carácteres visibles en una línea y especifica ancho de caja.
- placeholder -> Texto que aparece cuando el campo está vacío por lo que ofrece pista sobre el dato que se quiere ingresar
- required -> Indica campo que debe completarse antes de enviar formulario
- disabled -> Desactiva el campo, evitando interacción
- readonly -> Campo solo de lectura, evita modificarse su contenido

#### Label
Proporciona una etiqueta o descripción para elemento de formulario, como campo de entrada o opción de menú desplegable.Útil para acceso y uso de formulario.
- for -> Especifica qué elemento de formulario esta asociado al ```<label>```, debe coincidir ```<id>```
- form -> Permite asociar etiqueta con formulario especifico si hay varios, el id debe pertenecer al formulario que pertenece
#### Select (o  option)
Crear menús desplegables en formularios.Permite al usuario seleccionar una opción de una listas de estas.
- name -> Especifica nombre de control que se usará para el formulario. Usado como clave en par nombre-valor cuando se envíe datos del formulario del servidor.
- id -> Identificador único del elemento, puede usarse para asociar etiqueta ```<label>```  con área de texto.
- size -> Define números de opciones visibles en la lista sin necesidad de desplazar.
- multiple -> Selección de varias opciones a la vez
- value -> Indica valor de la opción

#### Fieldset/legend
Utilizado para agrupar varios elementos de formulario en conjunto lógico, mejora estructura y legibilidad. Dentro de fieldset se utiliza un legend para proporcionar título o descripción  del grupo de elementos.
- name -> Especifica nombre de control que se usará para el formulario. Usado como clave en par nombre-valor cuando se envíe datos del formulario del servidor.
- disabled -> Desactiva el campo, evitando interacción como dentro del fieldset.
- form -> Permite asociar etiqueta con formulario especifico si hay varios, el id debe pertenecer al formulario que pertenece

#### Button
Utilizado para crear varios botones interactivos en un formulario o página web. A diferencia de ```<input type="submit">```, el contenido del botón ```<button>``` incluye texto,imagen o HTML adicional.
- type -> Define tipo de boton pueden ser:
  - submit -> Enviar formulario cuando se hace click en el botón.No se especifica valor
  - reset -> Restablecer campos de formulario. Utilizado con JavaScript y sin valor
  - name -> Define nombre de botón que será enviado con datos de formulario si el botón tiene atributo ```<type="submit">```
  - value -> Especifica valor que se enviar al servidor si es de tipo submit
  - disabled -> Desactivar botón impidiendo que se haga click en este