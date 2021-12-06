# .__Git__ 
*introduccion*
- fue creado por Linus Benedict Torvalds creador de linux
<a href="https://en.wikipedia.org/wiki/History_of_Linux">linux</a>
- Un repositorio es una carpeta oculta llamada .git(para ver los archivos ocultos usamos `ls -al`) que mantiene el historial de los cambios de un proyecto

*instalacion*
`git-scm.com/`-> Download
<a href="https://git-scm.com/">git</a>

*configuration*
- Para configurar el nombre de usuario y el email que se va a utilizar como autor de los cambios (por defecto)


```bash
       git config --list `nos muestra las configuraciones
       que tenemos asta el momento y lo que nos falta`
       git config --list --show-origin `nos muestra
       donde estan esas configuraciones`
     $ git config --global user.name "juancitoPerez" 
     `configura el nombre de usuario`
     $ git config --global user.email "juancita@alskd.com"
     `configura el email`
     
```
para almacenar en cache el registro dado en su computadora y recordar el token o contrasen:a
```bash
$ git config --global credential.helper cache
```
puedes eliminar el registro de cache de la siguiente manera
```bash
$ git config --global --unset credential.helper
$ git config --system --unset credential.helper
```
`check` con `git config -l`


 *𝐂𝐨𝐦𝐚𝐧𝐝𝐨𝐬 𝐝𝐞 𝐆𝐈𝐓 𝐛𝐚́𝐬𝐢𝐜𝐨𝐬*
```bash
git init ` Crea el repositorio .git es un carpeta oculta`
git add namearchivo `an:ade ese archivo a esa "base de
 datos"`
git add . `agrega todos los archivos que cambiaron`

git commit -m 'primer commit' `manda ese commit a la base
 de datos del control de versiones -m es para referle el mensaje`
git comit `Esc` `:wq`//? guarda los cambios

git push `envia a un repositorio remoto`

git log nombredelarchivo` permite ver el historial de commit de un
 repositorio `
git log -p//? te da mas datos del commit

git rm --cached nombredelarchivo `quita el add, remueve los
 cambios guardados --cached quiere decir que esta en
  memoria ram que no esta guardado en la base de datos `

git status `Nos da un panorama de el estado de el trabajo`
git show `se usa para mostrar información sobre cualquier
 objeto git. todos cambios historicos hechos las lineas
 de texto cuando se hicieron los cambios o quien los a hecho `
git checkout --nombreDelArchivo //? descarta los cambios 
git diff nombredelarchivo//? para veer las diferencias de los cambios que hemos hecho 
pwd //? para ver en que directorio estamos
cat archivoDeTexto.txt //? permite ver el contenido de un archivo de texto
```
# Ramas comandos mas usados
```http
git branch -r //? te muestra todas las ramas ramas remotas
git branch //? lista las ramas
git branch nombredelarama //? crea una rama
git checkout nombredelarama //? para moverse entre ramas
git pull origin nombreDeRamaEnLaQueEstamos //? traemos todos los cambios de la rama
git merge nombreDeLaRamaQueQueremosIgualar //? igualamos las ramas

```



 
  # para hacer un push a un repo existente
  ```bash
     git remote add origin URL_del_repositorio
     gid add .
     git commit -m 'start'
     git push origin master
     
  ```
  # git new
 ```bash
     git config --global --list
 ```
  # add
  ```bash
  git add . //? agrega todas las carpetas
  git add nombredelarchivo //? agrega el archivo
  ```
  # stash
  ```bash
  git stash //? esto nos esconde los cambios en nuestro entorno de trabajo para que podamos hacer los push merge pull 
  ```
  
  
  
  𝐴𝑞𝑢𝑖́ 𝘩𝑎𝑦 𝑎𝑙𝑔𝑢𝑛𝑜𝑠 𝑐𝑜𝑚𝑎𝑛𝑑𝑜𝑠 𝑏𝑎́𝑠𝑖𝑐𝑜𝑠 𝑑𝑒 𝐺𝐼𝑇 𝑞𝑢𝑒 𝑑𝑒𝑏𝑒𝑠 𝑐𝑜𝑛𝑜𝑐𝑒𝑟:

          🔸𝐠𝐢𝐭 𝐢𝐧𝐢𝐭 | 𝑐𝑟𝑒𝑎𝑟𝑎́ 𝑢𝑛 𝑛𝑢𝑒𝑣𝑜 𝑟𝑒𝑝𝑜𝑠𝑖𝑡𝑜𝑟𝑖𝑜 𝑙𝑜𝑐𝑎𝑙 𝐺𝐼𝑇.
          𝐶𝑜𝑚𝑜 𝑎𝑙𝑡𝑒𝑟𝑛𝑎𝑡𝑖𝑣𝑎, 𝑝𝑢𝑒𝑑𝑒𝑠 𝑐𝑟𝑒𝑎𝑟 𝑢𝑛 𝑟𝑒𝑝𝑜𝑠𝑖𝑡𝑜𝑟𝑖𝑜 𝑑𝑒𝑛𝑡𝑟𝑜 𝑑𝑒 𝑢𝑛 𝑛𝑢𝑒𝑣𝑜 𝑑𝑖𝑟𝑒𝑐𝑡𝑜𝑟𝑖𝑜 𝑒𝑠𝑝𝑒𝑐𝑖𝑓𝑖𝑐𝑎𝑛𝑑𝑜 𝑒𝑙 𝑛𝑜𝑚𝑏𝑟𝑒 𝑑𝑒𝑙 𝑝𝑟𝑜𝑦𝑒𝑐𝑡𝑜:
          🔸𝐠𝐢𝐭 𝐢𝐧𝐢𝐭 [𝐧𝐨𝐦𝐛𝐫𝐞 𝐝𝐞𝐥 𝐩𝐫𝐨𝐲𝐞𝐜𝐭𝐨]
          🔸git clone se usa para copiar un repositorio. Si el repositorio está en un servidor remoto, usa:
          🔸git clone nombredeusuario@host:/path/to/repository
          A la inversa, ejecuta el siguiente comando básico para copiar un repositorio local:
          🔸git clone /path/to/repository
          🔸git add se usa para agregar archivos al área de preparación. Por ejemplo, el siguiente comando de Git básico indexará el archivo temp.txt:
          🔸 git add <temp.txt>
          🔸git commit creará una instantánea de los cambios y la guardará en el directorio git.
          🔸git commit –m “El mensaje que acompaña al commit va aquí”
          Ten en cuenta que los cambios confirmados no llegarán al repositorio remoto.
#config

          🔸git config puede ser usado para establecer una configuración específica de usuario, como el email, nombre de usuario y tipo de formato, etc. Por           ejemplo, el siguiente comando se usa para establecer un email:
          🔸git config --global user.email tuemail@ejemplo.com
          La opción -global le dice a GIT que vas a usar ese correo electrónico para todos los repositorios locales. Si quieres utilizar diferentes correos             electrónicos para diferentes repositorios, usa el siguiente comando:
          🔸git config --local user.email tuemail@ejemplo.com
          🔸git status muestra la lista de los archivos que se han cambiado junto con los archivos que están por ser preparados o confirmados.
          🔸git status
          🔸git push se usa para enviar confirmaciones locales a la rama maestra del repositorio remoto. Aquí está la estructura básica del código:
          🔸git push  origin <master>
          Reemplaza <master> con la rama en la que quieres enviar los cambios cuando no quieras enviarlos a la rama maestra.
#ramas

          🔸 git checkout crea ramas y te ayuda a navegar entre ellas. Por ejemplo, el siguiente comando crea una nueva y automáticamente se cambia a ella:
          command git checkout -b <branch-name>
          Para cambiar de una rama a otra, sólo usa:
          🔸git checkout <branch-name>
          🔸git remote te permite ver todos los repositorios remotos. El siguiente comando listará todas las conexiones junto con sus URLs:
          🔸git remote -v
          Para conectar el repositorio local a un servidor remoto, usa este comando:
          🔸git remote add origin <host-or-remoteURL>
          Por otro lado, el siguiente comando borrará una conexión a un repositorio remoto especificado:
          🔸git remote <nombre-del-repositorio>
          🔸git branch se usa para listar, crear o borrar ramas. Por ejemplo, si quieres listar todas las ramas presentes en el repositorio, el comando                   debería verse así:
          🔸 git branch
          
          Si quieres borrar una rama, usa:
          🔸git branch -D <branch-name>
          si queremos cambiarle de nombre
          git branch -m "nombredelaramavieja" "nombredelaramanew"
          
 #pull 
 
          🔸git pull fusiona todos los cambios que se han hecho en el repositorio local con el directorio de trabajo local.
          🔸git pull
          🔸git merge se usa para fusionar una rama con otra rama activa:
          🔸git merge <branch-name>
          🔸 git diff se usa para hacer una lista de conflictos. Para poder ver conflictos con respecto al archivo base, usa:
          🔸git diff --base <file-name>
          El siguiente comando se usa para ver los conflictos que hay entre ramas antes de fusionarlas:
          🔸git diff <source-branch> <target-branch>
          Para ver una lista de todos los conflictos presentes usa:
          🔸git diff
          🔸git tag marca commits específicos. Los desarrolladores lo usan para marcar puntos de lanzamiento como v1.0 y v2.0.
          🔸git tag 1.1.0 <instert-commitID-here>
          🔸git log se usa para ver el historial del repositorio listando ciertos detalles de la confirmación. Al ejecutar el comando se obtiene una salida               como ésta:
          commit 15f4b6c44b3c8344caasdac9e4be13246e21sadw
          Author: Alex Hunter <alexh@gmail.com>
          Date:   Mon Oct 1 12:56:29 2016 -0600
          
   #reset
   
          🔸git reset sirve para resetear el index y el directorio de trabajo al último estado de confirmación.
          🔸git reset --hard HEAD
          🔸git rm se puede usar para remover archivos del index y del directorio de trabajo.
          🔸git rm filename.txt
          🔸git stash guardará momentáneamente los cambios que no están listos para ser confirmados. De esta manera, pudes volver al proyecto más tarde.
          🔸git stash
          🔸 git show se usa para mostrar información sobre cualquier objeto git.
          🔸git show
          
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
