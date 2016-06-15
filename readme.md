- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

> git reset --hard HEAD~1 (con el comando --hard hacemos que se descarten los cambios de los archivos en el working copy)

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? 

> git reflog (para buscar el commit id donde se formateó el archivo)

> git checkout master

> git branch -f styled 1cf601a (para mover la rama styled al commit id donde se formateó el archivo)

> git checkout styled

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No, ya que era un fast forward. Es decir que no existen dos versión del mismo archivo que hayan tenido modificaciones en líneas coincidentes en cada una de las ramas, por lo que git simplemente mueve el puntero. Aquí, la rama que se quiere fusionar (master) es un ancestro directo de la que se fusiona (styled)

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
 
Si, un conflicto en todas las líneas del archivo. En este caso, a partir del archivo original creamos dos ramas (la htmlify y la styled). Al hacer el merge, git detecta que ha habido modificaciones del archivo original en las mismas líneas de las dos ramas. 

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 

No, porque es un fast forward.

- ¿Qué comando o comandos utilizaste en el paso 25? 

He usado 'git graph' que es un alias global que había creado anteriormente con:

>git config --global alias.graph 'log --graph --decorate --pretty=oneline'

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si, porque master es el antecesor directo de title.

- ¿Qué comando o comandos utilizaste en el paso 27?

>git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?

>git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?

>git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?

> git reflog

> git checkout ce6ac76

> git branch -D master

> git branch master

> git checkout master

- ¿Qué comando o comandos usaste en el paso 32?

> git reflog

> git checkout baca3d2

- ¿Qué comando o comandos usaste en el punto 33?

> git checkout master