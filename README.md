# Apuntes de lenguajes de marcas

**Índice**   
1. [GitHub](#id1)
2. [Markdown](#id2)
3. [HTML](#id3)
4. [CSS](#id4)
5. [Diseño Responsive](#id5)

## Github<a name="id1"></a>
Utilizado para el control de versiones, es decir para tener un manejo de registros con los cambios de los diferentes archivos. Por otra parte podemos tener colaboradores y ver tambien los cambios y actualizaciones.
### Creación de cuenta de GitHub

Comenzamos yendo a  esta URL:

![GitHub_web](fotos/github.PNG)

Luego de ello vamos a crearnos una cuenta para ello nos pedirá una verificación de correo electrónico.

### Crear repositorio 
Una vez hecho el paso iremos a crear un repositorio dandole aqui:

Le damos un nombre ,lo ponemos en público y le damos a crear:

![GitHub_repo](fotos/github1.PNG)

Copiamos el link del github creado:

![GitHub_linkrepo](fotos/github2.PNG)

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

![Texto alternativo](fotos/ia.webp)

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

 <img src =fotos/git>

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
### Form
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

### Tablas

Las tablas permiten organizar información en filas y columnas. Para páginas anteriormente pero ahora solo es para tabulaciones.
#### Etiquetas principales
- **`<table>`**: Inicia una tabla. Atributos comunes:
  - `border`: Define el grosor del borde.
  - `width`: Especifica el ancho.
  - Ejemplo: `<table border="1" width="100%">`

- **`<thead>`**: Agrupa el encabezado de la tabla, normalmente con etiquetas `<th>`.

- **`<tbody>`**: Agrupa el contenido principal de la tabla.

- **`<tfoot>`**: Agrupa el pie de la tabla, útil para resúmenes.

#### Otras etiquetas
- **`<tr>`**: Define una fila. Atributos:
  - `align`: Alinea el contenido (`left`, `right`, `center`).
  - `bgcolor`: Cambia el color de fondo.
  - Ejemplo: `<tr align="center" bgcolor="#f0f0f0">`

- **`<th>`**: Define una celda de encabezado. Atributos:
  - `colspan`: Combina varias columnas.
  - `rowspan`: Combina varias filas.
  - Ejemplo: `<th colspan="2">`

- **`<td>`**: Define una celda de datos. Atributos:
  - `align`: Alinea el contenido.
  - `colspan` y `rowspan`: Igual que en `<th>`.
  - Ejemplo: `<td align="right" colspan="3">`

#### Ejemplo básico
```html
<table border="1" width="100%">
  <thead>
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Dato 1</td>
      <td>Dato 2</td>
      <td>Dato 3</td>
    </tr>
    <tr>
      <td colspan="2">Dato combinado</td>
      <td>Dato 4</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="3">Pie de tabla</td>
    </tr>
  </tfoot>
</table>
``` 
## CSS<a name="id4"></a>
A medida que fue creciendo el Intenet tambien la información textual en las pagíans web debían ir cambiando para que se vea más atractivo.Por ello se idearon hojas de estilo o CSS para poder dar instrucciones a un navegador de como se debe ir viendo los elementos. Surgieron bastantes nombres como:  
- **CHSS** (Håkon Wium Lie, 1994)  
- **SSP** (Propuesta basada en flujo)  

**Cronología**:  
- **1996**: CSS Nivel 1  
- **1998**: CSS Nivel 2  
- **2008**: CSS2.1 Revisión  
- **Actualidad**: CSS3 modular (algunos módulos en desarrollo)

 **Ventajas**:  
- Código más limpio y mantenible  
- Más potente que las etiquetas de presentación de HTML  
- Lenguaje sencillo  
- Múltiples hojas de estilo para un documento
- Reutilizable en varios archivos HTML  

 **Desventajas**:  
- Inconsistencias entre navegadores (requieren soluciones como otras hojas de estilo)  
### Ubicación
 **Inline**
 -Propiedades  CSS directamente al elemento usando atributo style. 
```html
<p style="text-align:center; color:red">Texto rojo centrado</p>
```
**Interno**
 -Dentro del documento en parte head podemos poner el style. 
```html
<head>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
  </style>
</head>
```
**Externo**
 -Llamandolo con su direccion y que sea .css para los estilos
```html
<link rel="stylesheet" href="estilos.css">
```
### Prioridad
1. Estilos externos  
2. Estilos internos (en `<head>`)  
3. Estilos inline (en etiquetas)  
4. Reglas contradictorias: gana la última declarada  
Reglas:
 !important -> sobreescribe las reglas incluso si tiene menor especificidad.
Herencia:
 Propiedades como `color font-family` ,etc. Pueden heredarse, pero tiene menor prioridad que regla aplicadada directamente.
### Especificidad 
Sistema de puntuación:  

`Inline (1000) > ID (100) > Clase/Atributo (10) > Elemento (1)`
### Estructura
Conjunto de reglas que define estética final de documentos como HTML. Cada regla formada por selector y conjunto de declaraciones.
Declaracion-> Forma propiedad y valor asociado. ej. font-size: 10pt
Selector -> Nos sirve para definir a qué elemento o elementos aplicaremos declaraciones de regla ej. p (de parrafo)
```css 
 p {
  font-size: 10 pt;
  background-color: gray;
 }
```
### Comentarios en CSS
Los comentarios en CSS se escriben entre `/*` y `*/` y pueden ocupar varias líneas. El navegador ignora el contenido de los comentarios al renderizar.

**Ejemplo de comentario:**
```css
/* Esto es un comentario en CSS */
selector {
  propiedad1: valor;
  propiedad2: valor;
}
```
### Agrupar selectores en CSS
Para evitar repetición, se pueden agrupar selectores separados por comas. Las reglas dentro de las llaves se aplicarán a todos los selectores indicados.

**Ejemplo sin agrupar:**
```css
h1 {
  color: red;
}
p {
  color: red;
}
```

**Ejemplo agrupando selectores:**
```css
h1, p {
  color: red;
}
```
### Tipos de selectores en CSS

En CSS, los selectores permiten aplicar estilos a elementos específicos del documento HTML. Se dividen en:

#### Selectores básicos:
1. **Selector de elementos**: Aplica estilos a todas las etiquetas de un tipo específico.
2. **Selector de ID**: Aplica estilos a un elemento con un atributo `id` específico.
3. **Selector de clase**: Aplica estilos a todos los elementos con una clase específica.

#### Selectores avanzados:
1. **Selector universal (`*`)**: Aplica estilos a todos los elementos.
2. **Selectores de atributos**: Aplica estilos a elementos con atributos específicos.
3. **Selector de hijos (`>`):** Aplica estilos a hijos directos de un elemento.
4. **Selector de descendientes (espacio)**: Aplica estilos a todos los descendientes de un elemento.
5. **Selector de hermanos adyacentes (`+`)**: Aplica estilos al hermano inmediato de un elemento.
6. **Pseudoclases**: Estilos basados en el estado de un elemento (ej. `:hover`).
7. **Pseudoelementos**: Estilos para partes específicas de un elemento (ej. `::before`, `::after`).
#### Selector de elementos (selector de tipo)
Este selector aplica estilos a todos los elementos de un tipo específico en la página. Por ejemplo, el siguiente código afectará a **todos los elementos `<a>`** del documento HTML:

```css
/* Afecta a todos los elementos <a> del documento HTML */
a {
  color: red;
}
```
#### Selector de ID
El selector de ID aplica estilos a un elemento con un atributo `id` específico. Se define con el símbolo `#` seguido del valor del `id`.

**Ejemplo:**
```css
#example {
  property: value;
  property2: value2;
}
```

Este código afectará al siguiente elemento HTML:
```html
<p id="example">Texto de ejemplo</p>
#### Selector de clase
Aplica estilos a elementos con un atributo `class` específico. Se define con un punto (`.`) seguido del nombre de la clase.

**Ejemplo:**
```css
.example {
  property: value;
  property2: value2;
}
```
Afecta a elementos como:
```html
<p class="example">Texto de ejemplo</p>
<li class="example">Elemento de lista</li>
<div class="example">Div de ejemplo</div>
```

#### Selector universal
Selecciona todos los elementos de la página, representado por un asterisco (`*`).

**Ejemplo:**
```css
* {
  border: 1px solid #000000;
}
```
Aplica un borde negro sólido de 1px a todos los elementos del documento.

#### Selectores de atributos 
Aplica estilos a elementos con atributos específicos.  
   ```css
   img[alt] {
     border: 1px solid #000000;
   }
   ```
También se puede especificar el valor del atributo, como partes concretas como extensión de archivos:  
   ```css
   img[src="alert.gif"] {
     border: 1px solid #000000;
   }
   ```
#### Selectores de hijos
Permiten seleccionar elementos que son **hijos directos** de otros elementos. Por ejemplo, el siguiente código aplica estilos solo a los elementos `<strong>` que son hijos de `<h3>`:

```css
h3 > strong {
  color: blue;
}
```

También se puede aplicar estilos a un hijo específico utilizando la pseudoclase `:nth-child(n)`, donde `n` indica el número del hijo.

**Ejemplo:**
```css
.parent :nth-child(4) {
  color: red;
}
```

**HTML:**
```html
<div class="parent">
  <p>Primer hijo</p>
  <div>Segundo hijo</div>
  <span>Tercer hijo</span>
  <div>Cuarto hijo</div>
  <p>Quinto hijo</p>
</div>
```

En este caso, el estilo se aplicará al cuarto hijo directo del elemento con clase `parent`, sin importar su tipo.
#### Selectores descendientes
Seleccionan todos los elementos que están dentro de otro elemento, sin importar cuántos niveles de anidamiento existan.

**Sintaxis:**  
```css
ancestro descendiente {
  propiedad: valor;
}
```
#### Selector de Hermanos Adyacentes (`+`)

Selecciona **solo el primer elemento** que aparece **inmediatamente después** de otro elemento, **al mismo nivel** (hermanos).Ej

```css
elemento1 + elemento2 {
  propiedad: valor;
}
```
#### Pseudoelementos 
Estilizar solo la primera línea de un párrafo:
```css
p::first-line {
  font-weight: bold;
  color: #336699;
}
```
#### Flexbox: Diseño Flexible

Antes se usaban:  
- Posicionamiento (static, relative, absolute)  
- Elementos en línea/bloque  
- Propiedad float  

Estos métodos resultaban limitados para diseños modernos que deben adaptarse a:  
 - Diferentes dispositivos (móviles, escritorio)  
 - Múltiples resoluciones de pantalla  
 - Interfaces responsivas  

Flexbox, es un sistema donde:  
- Los elementos se vuelven **flexibles**  
- Se colocan **automáticamente**  
- Permite crear diseños **adaptables** con menos código  

## Diseño Responsive <a name="id5"></a>

Técnica que permite a los sitios web adaptarse automáticamente a diferentes dispositivos (PC, tabletas, móviles) y tamaños de pantalla.

**Características clave:**  
- **Adaptabilidad:** Elementos que se redimensionan (texto, imágenes, menús)  
- **Media Queries:** Reglas CSS condicionales según características del dispositivo  
- **Rejillas fluidas:** Uso de porcentajes en lugar de medidas fijas  
- **Elementos escalables:** Imágenes y tipografías que mantienen proporciones  

### Media query(CSS)
Reglas CSS que aplican estilos condicionales según características del dispositivo o ventana del navegador.Crea diseños responsive que se adapten a diferentes dispositivos y tamaños.

1. **Detectan características:**  
   - Ancho/alto de pantalla  
   - Orientación (horizontal/vertical)  
   - Resolución  
2. **Aplican estilos:**  
   Solo cuando se cumplen las condiciones especificadas  

**Uso típico:**  
Adaptar layouts, tipografías y elementos visuales para cada tamaño de pantalla.
```css
/* Ejemplo de media query */
body {
  background-color: lightblue;
}

/* Cambiar el fondo para pantallas menores a 600px */
@media (max-width: 600px) {
  body {
    background-color: lightgreen;
  }
}
/*Fondo de pantalla amarillo en 480*/
@media (max-width: 480px) {
  body {
    background-color: yellow;
  }
}
```
En este caso cuando sea menor a 600 px el fondo se hará de color verde y este cuando pase a ser menor a 480px será de color amarillo.

### Media queries posibilidades
Se pueden definir caracterísitcas para determinar resoluciones y anchos de pantalla, puede determinar orientación vertical u horizontal. Es posible poner condiciones AND NOT ONLY OR:

**Parámetros:**  
- **width:** anchura de ventana navegador (admite max i min ej. max-width)
- **height:** altura de ventana navegador
- **device-width:** anchura resolución de pantalla
- **device-heigth:** altura resolución de pantalla
- **orientation:** dispositivo horizontal o vertical
