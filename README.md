# .__Git__ 
*introduccion*
- fue creado por Linus Benedict Torvalds creador de linux
<a href="https://en.wikipedia.org/wiki/History_of_Linux">linux</a>
- Un repositorio es una carpeta oculta llamada .git(para ver los archivos
- ocultos usamos `ls -al`) que mantiene el historial de los cambios de un proyecto

*instalacion*
- `git-scm.com/`-> Download
<a href="https://git-scm.com/">git</a>


*configuration*
- Para configurar el nombre de usuario y el email que se va a utilizar como
 autor de los cambios (por defecto)
```bash
git config --list `nos muestra las configuraciones
que tenemos asta el momento y lo que nos falta`
git config --list --show-origin `nos muestra
donde estan esas configuraciones`
git config --global user.name "juancitoPerez" 
`configura el nombre de usuario`
git config --global user.email "juancita@alskd.com"
`configura el email`   
```

*code*
```bash
a
git add namearchivo `an:ade ese archivo a esa "base de
datos"`
git add . `agrega todos los archivos que cambiaron`

b
git branch -r ` te muestra todas las ramas ramas remotas`
git branch ` lista las ramas`
git branch nombredelarama ` crea una rama`
git branch -D namebranch ` borramos la rama`
git branch -m namebranch newnamebrach `cambiamos el nombre de la rama
si no funca probar con comillas`


c
git clone path `clonamos un repositorio path aqui debes poner la 
ubicacion del repositorio ya sea remoto o local`
git config --global credential.helper cache `recordar token o password`
git config --global --unset credential.helper `elimina el cache`

git commit -m 'primer commit' `manda ese commit a la base
de datos del control de versiones -m es para referle el mensaje`

git checkout numeroalfanumericodelcommit nameofarchivo.ejm`vuelve
al estado del commit de ese archivo`
git checkout master nameofarchivo.ejm `vuelve a los cambios de 
la master`
git checkout --nombreDelArchivo ` descarta los cambios `
git checkout nombredelarama ` para moverse entre ramas`
git checkout -b nombredelarama `crea una rama y se cambia a ella`

d
git diff numerodecommit numerodecommit `compara los commit:`
git diff `estando en un repo muesta las diferencias en mi directorio
actual y es staging `
git diff nombredelarchivo ` para veer las diferencias de los cambios 
que hemos hecho`

e
f
g
h
i
git init ` Crea el repositorio .git es un carpeta oculta`

j
k
l
git log nombredelarchivo` permite ver el historial de commit de un
repositorio `
git log -p`   te da mas datos del commit` 
git log --stat `permite ver los cambios especificos que se hicieron
en cuales archivos a partir de en cuales commit`

m
git merge nombreDeLaRamaQueQueremosIgualar ` igualamos las ramas`

n
o
p
git push `envia a un repositorio remoto`

git pull origin nombreDeRamaEnLaQueEstamos ` traemos todos los 
cambios de la rama`

q

r
git reset numeroalfanumericodelcommit --hard`nos permite volver a una
version anterior --hard es el mas peligroso y usado todo vuelve 
a su version anterior`
git reset numeroalfanumericocommit --soft `--soft volvemos a la
version anterior pero lo que tengamos en stageing sigue hay es 
decir si as hecho cambios y le has dado git add . eso sigue hay`

git rm --cached nombredelarchivo `quita el add, remueve los
cambios guardados --cached quiere decir que esta en
memoria ram que no esta guardado en la base de datos `

git remote `permite ver todos los repositorios remotos`

s
git status `Nos da un panorama de el estado de el trabajo`

git show `se usa para mostrar información sobre cualquier
objeto git. todos cambios historicos hechos las lineas
de texto cuando se hicieron los cambios o quien los a hecho `

git stash ` esto nos esconde los cambios en nuestro entorno de 
trabajo para que podamos hacer los push merge pull `

t
git tag 1.1.0 <instert-commitID-here> marca las versiones

u
v
w
x
y
z

```


   #fetch
   
          🔸git fetch le permite al usuario buscar todos los objetos de un repositorio remoto que actualmente no se encuentran en el directorio de trabajo                local.
          🔸git fetch origin
          🔸 git ls-tree te permite ver un objeto de árbol junto con el nombre y modo de cada ítem, y el valor blob de SHA-1. Si quieres ver el HEAD, usa:
          🔸git ls-tree HEAD
          🔸git cat-file se usa para ver la información de tipo y tamaño de un objeto del repositorio. Usa la opción -p junto con el valor SHA-1 del objeto               para ver la información de un objeto específico, por ejemplo:
          🔸git cat-file –p d670460b4b4aece5915caf5c68d12f560a9fe3e4
          🔸git grep le permite al usuario buscar frases y palabras específicas en los árboles de confirmación, el directorio de trabajo y en el área de                  preparación. Para buscar por www.hostinger.com en todos los archivos, usa:
          🔸git grep “www.hostinger.com”
          🔸gitk muestra la interfaz gráfica para un repositorio local. Simplemente ejecuta:
         🔸gitk
         
  #git instaweb
  
         🔸git instaweb te permite explorar tu repositorio local en la interfaz GitWeb. Por ejemplo:
         🔸git instaweb –http=webrick
         🔸git gc limpiará archivos innecesarios y optimizará el repositorio local.
         🔸git gc
         🔸git archive le permite al usuario crear archivos zip o tar que contengan los constituyentes de un solo árbol de repositorio. Por ejemplo:
         🔸git archive - -format=tar master
         🔸git prune elimina los objetos que no tengan ningún apuntador entrante.
         🔸git prune
         🔸git fsck realiza una comprobación de integridad del sistema de archivos git e identifica cualquier objeto corrupto
         🔸git fsck
         🔸git rebase se usa para aplicar ciertos cambios de una rama en otra. Por ejemplo:
         🔸git rebase master

    Conclusión
    Aprender los comandos básicos de GIT será de gran ayuda para los desarrolladores, ya que pueden controlar fácilmente el código fuente de los proyectos. Puede que te lleve algo de tiempo recordarlos todos, por esta hoja de trucos de GIT podría resultarte útil.

    ¡Practica estos comandos de GIT y aprovecha al máximo tus habilidades en desarrollo! ¡Buena suerte!
