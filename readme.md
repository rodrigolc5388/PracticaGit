#Práctica del curso de git, gitHub y Sourcetree#

- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**  
Utilicé el comando: git rese --hard HEAD~1.  
Este comando mueve los punteros HEAD y de rama un commit atrás (o los que indiquemos después de la virgulilla), y deshace los cambios en el working copy.

- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**  
Volví a modificar el archivo, utilicé "git add git-nuestro.md" para pasar el archivo modificado al staging area y luego ejecuté "git commit -m .....". Acabo en el mismo punto.  
También podría haber hecho un "git reflog", encontrar el identificador del commit deshecho, volver a la rama y hacer un "git merge identificadorCommit", con lo que habría vuelto exactamente al mismo punto.

- **El merge del paso 13, ¿causó algún conflicto? ¿Por qué?**  
El merge fue fast-forward y no causó conflicto porque, en ese momento, la rama styled estaba más avanzada que la rama master; si el merge hubiese sido en el sentido inverso, master abosrbe a styled, sí habría habido conflicto, ya que la rama master no contiene los cambios de la rama styled.

- **El merge del paso 19, ¿causó algún conflicto? ¿Por qué?**  
Sí, hubo un conflicto al hacer el merge porque, cada uno de los archivos git-nuestro que se encuentran en ambas ramas, tienen modificaciones distintas en las mismas líneas.

- **El merge del paso 21, ¿causó algún conflicto? ¿Por qué?**  
El merge no causó conflicto porque, a pesar de que el archivo git-nuestro de la rama master se encontraba más atrás que el de la rama styled, las modificaciones que se iban a añadir, aunque estaban en las mismas líneas, no eliminaban contenido del archivo de la rama master, solo lo aumentaban.

- **¿Qué comando o comandos utilizaste en el paso 25?**  
Usé toda la colección de comandos aprendidos el fin de semana:  
"git log --graph/--decorate/--pretty=oneline", y el todo-en-uno "git log --graph --decorate --pretty=oneline". Pero prefiero usar solo "git log --graph"; me parece más limpio, sencillo y entendible.

- **El merge del paso 26, ¿podría ser fast-forward? ¿Por qué?**  
Sí, por lo visto podría haber sido fast-forward, porque al hacerlo no surgió ningún conflicto.  
Aunque la verdad es que en primera instancia pensé que sí habría conflicto ya que el archivo git-nuestro tenía modificaciones distintas en cada rama; en cada rama el archivo tenía un título distinto.

- **¿Qué comando o comandos utilizaste en el paso 27?**  
Usé el comando "git reset HEAD~1"; este comando me devuelve al commit anterior al del merge, pero sin perder los cambios que tengo en el working copy.

- **¿Qué comando o comandos utilizaste en el paso 28?**  
Uso el comando "git reset --hard HEAD~1"; es el mismo comando que en el paso anterior, pero, al usar "--hard" descarta los cambios en el working copy.


- **¿Qué comando o comandos utilizaste en el paso 29?**  
El comando que utilicé fue "git branch -d title", pero git me advierte de que esa rama no está "fully merge" y que si estoy seguro de querer eliminarla, utilice "git branch -D title". Cambio la d minúscula por una mayúscula.

- **¿Qué comando o comandos utilizaste en el paso 30?**  
Primero hice un "git reflog" para encontrar el identificador del commit resultante de mergear title en master; copio el identificador, "git checkout master" y una vez en master, ejecuto "git merge identificadorCommit" y vuelvo al mismo estado en el que estaba antes de deshacer el merge en el paso 27.


- **¿Qué comando o comandos utilizaste en el paso 32?**  
Ejecuto "git reflog" para encontrar el identificador del commit que necesito; una vez encontrado, hago un "git reset identificadorCommit": este comando mueve los punteros HEAD y de rama al commit que le estoy indicando, manteniendo los cambios en el staging area.


- **¿Qué comando o comandos utilizaste en el paso 33?**  
Exactamente los mismos comandos que en el paso anterior.
