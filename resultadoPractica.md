práctica Git


- ¿Qué comando utilizaste en el paso 11 (Deshacer el último commit (perdiendo los cambios realizados en el working copy)? ¿Por qué? 

	git reset --hard HEAD~1, porque era deshacer 1 y forzando con hard que el working copy también perdiera cambios

- ¿Qué comando o comandos utilizaste en el paso 12 (Rehacer el último commit (el que acabamos de deshacer))? ¿Por qué?

	git reflog (para ver al cual tengo que ir) git checkout 9741234 (el seleccionado en reflog)

- El merge del paso 13(Hacer un merge con ‘master’ (styled absorbe a master)), ¿Causó algún conflicto? ¿Por qué? 

	git branch para comprobar que estoy en styled, me muevo a styled con git checkout y hago git merge master, no causó conflicto.

- El merge del paso 19 (Hacer un merge de “htmlify” en “styled” (styled absorbe a htmlify)), ¿Causó algún conflicto? ¿Por qué?

	git checkout styled .. git merge htmlify, si causó conflicto, había archivos en común y con la misma línea modificada

- El merge del paso 21 (Desde “master”, hacer un merge con “styled”), ¿Causó algún conflicto? ¿Por qué? 

	(me requiere para cambiar de rama hacer un add del archivo), cambio de rama a master y hago desde master git merge styled. 

- ¿Qué comando o comandos utilizaste en el paso 25(Dibujar el diagrama)?
	git log --graph --oneline --all 

- El merge del paso 26 (Hacer un merge “no fast-forward” de “title” en “master” (master absorbe a title), ¿Podría ser fast forward? ¿Por qué? 
	(compruebo que estoy en master) git merge --no-ff title

- ¿Qué comando o comandos utilizaste en el paso 27(Deshacer el merge (sin perder los cambios del working copy)? 
	git reflog (para ver donde quiero volver) git reset 9740462

- ¿Qué comando o comandos utilizaste en el paso 28 (Descartar los cambios)? 
	git reflog (para ver donde quiero volver) … git reset --hard 9750322

- ¿Qué comando o comandos utilizaste en el paso 29 (Eliminar la rama “title”)? 
	git branch -D title
- ¿Qué comando o comandos utilizaste en el paso 30(Rehacer el merge que hemos deshecho)? 
 	git reflog (para ver donde quiero volver) … git checkout a donde quiero ir
- ¿Qué comando o comandos usaste en el paso 32 (Volver al commit inicial cuando se creó el poema)? 
	(Volver a la parte inicial del poema) git reflog .. git checkout commit primero (está en su estado inicial)
- ¿Qué comando o comandos usaste en el punto 33 ( Volver al estado final, cuando pusimos título al poema)?
	(Volver al estado final) git reflog .. git checkout commit de git-nuestro con titulo (lo abre y está escrito el título)

