# Apuntes de lenguajes de marcas

**Índice**   
1. [GitHub](#id1)
2. [Markdown](#id2)
3. [HTML](#id3)

## Github<a name="id1"></a>
Utilizado para el control de versiones, es decir para tener un manejo de registros con los cambios de los diferentes archivos. Por otra parte podemos tener colaboradores y ver tambien los cambios y actualizaciones.
# Creación de cuenta de GitHub

Comenzamos yendo a  esta URL:

![GitHub_web](https://github.com/Aitor2507/0373-AE1A-AitorSanchez/blob/main/github.PNG "GitHub_web")

Luego de ello vamos a crearnos una cuenta para ello nos pedirá una verificación de correo electrónico.

# Crear repositorio 
Una vez hecho el paso iremos a crear un repositorio dandole aqui:

Le damos un nombre ,lo ponemos en público y le damos a crear:

![GitHub_repo](https://github.com/Aitor2507/0373-AE1A-AitorSanchez/blob/main/github1.PNG "GitHub_repo")

Copiamos el link del github creado:

![GitHub_linkrepo](https://github.com/Aitor2507/0373-AE1A-AitorSanchez/blob/main/github2.PNG "GitHub_linkrepo")

# Como enlazar un github a un git 

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
git branch origin master

```

Es importante que no se haga solo un commit entero sino que se tenga varios para tener una idea más clara de como se fue estructurando el trabajo.

## Markdown<a name="id2"></a>
Lenguaje marcado para editar documentos de texto como este para que tenga la mayor legibilidad y facilidad de publicación.

En markdown para los diferentes tamaños de encabezados escribiremos una almohadilla delante del texto que queremos que se vea en un encabezado u otro:
'''
# Primer nivel de encabezado
## Segundo nivel de encabezado
### Tercer nivel de encabezado
#### Cuarto nivel de encabezado
##### Quinto nivel de encabezado
###### Sexto nivel de encabezado
'''

## HTML<a name="id3"></a>


# Favicons

# A3
 