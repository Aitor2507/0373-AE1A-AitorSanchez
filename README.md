# Apuntes de lenguajes de marcas

**Índice**   
1. [GitHub](#id1)
2. [Markdown](#id2)
3. [HTML](#id3)

## Github<a name="id1"></a>
Utilizado para el control de versiones, es decir para tener un manejo de registros con los cambios de los diferentes archivos. Por otra parte podemos tener colaboradores y ver tambien los cambios y actualizaciones.
### Creación de cuenta de GitHub

Comenzamos yendo a  esta URL:

![GitHub_web](https://github.com/Aitor2507/0373-AE1A-AitorSanchez/blob/main/github.PNG "GitHub_web")

Luego de ello vamos a crearnos una cuenta para ello nos pedirá una verificación de correo electrónico.

### Crear repositorio 
Una vez hecho el paso iremos a crear un repositorio dandole aqui:

Le damos un nombre ,lo ponemos en público y le damos a crear:

![GitHub_repo](https://github.com/Aitor2507/0373-AE1A-AitorSanchez/blob/main/fotos/github1.PNG "GitHub_repo")

Copiamos el link del github creado:

![GitHub_linkrepo](https://github.com/Aitor2507/0373-AE1A-AitorSanchez/blob/main/fotos/github2.PNG "GitHub_linkrepo")

### Como enlazar un github a un git 

Primeramente hemos de instalarnos el git en su [página oficial](https://git-scm.com/) luego de hecho esto, abriremos el git e iniciaremos sesion en el local de esta manera y nos ubicaremos en la carpeta que queremos enlazar con la de github normalmente para que no haya problemas debemos tener el mismo nombre:

```
git config user.name "en este espacio tu nombre de github"
git config user.email "correo verificado"
git remote add origin " el link que queremos enlazar"

```

Luego cuando tenemos logeado nuestro git con el github  iniciaremos y haremos los diferentes cambios que queramos y al finalizar siempre hemos de hacer estos comandos para que se guarden tanto en el local como en el repositorio enlazado:

```
git init (para empezar)
git add . ( para solo un archivo ponemos en el punto "archivo.txt")
git commit -m "mensaje para explicar lo que se hizo aquí"
git push origin master
git pull origin master (para descargar cambios de repositorio a remoto)

```

Es importante que no se haga solo un commit entero sino que se tenga varios para tener una idea más clara de como se fue estructurando el trabajo.

## Markdown<a name="id2"></a>
Lenguaje marcado para editar documentos de texto como este para que tenga la mayor legibilidad y facilidad de publicación.

### Encabezados
En markdown para los diferentes tamaños de encabezados escribiremos una almohadilla delante del texto que queremos que se vea en un encabezado u otro:

```
# Primer nivel de encabezado
## Segundo nivel de encabezado
### Tercer nivel de encabezado
#### Cuarto nivel de encabezado
##### Quinto nivel de encabezado
###### Sexto nivel de encabezado
```

### Formato de letras
Para los diferentes formatos de letras tendremos ponerlos entre estos diferents símbolos:

```
*cursiva*
**negrita**
**_cursiva y negrita_**
```

### Lista y sublistas
En las listas lo ordenaremos por números como se escribe a mano pero aquí para que hayan sublistas se deben tabular de esta manera:

```
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
[nombre abreviado del enlace](hhttps://es.wired.com/articulos/la-onu-crea-consejo-consultivo-de-inteligencia-artificial-un-paso-hacia-su-gobernanza-global "Tit opcional")

![Texto alternativo](/fotos/ia.webp "Tit opcional")

Aqui podemos verlos en ejemplos:

### Tablas 
Para hacer tablas con titulo y diferente información hemo de ponerlos entre estos símbolos || que hacen como referencia a la tabla, aquí les tengo un ejemplo:

|Título 1|Título 2| Título 3|
|-----------|---------:|:------------:|    
|SMX2|Curso 2324|25|
|**ASIX1**|Curso 2425|33|
|DAW2|Curso 2425|32|

Tambien si queremos el titulo lo queremos de un lado u otro hemos de poner los dos puntos en la izquierda o centrado como en el titulo 2 y 3.

## HTML<a name="id3"></a>
Lenguaje marcado utilizado para la creación de páginas web.
###  


# Favicons


# A3
 