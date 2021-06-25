#Práctica del curso de git, gitHug

###Luis Baeza
###baeza.luis@gmail.com


##Ejercicio 1

¿Qué comando utilizaste en el paso 11? ¿Por qué? 
Utilicé: git reset --hard HEAD~1
Porque: Retrocedo 1 commit (al anterior) y al aplicar "--hard", mi Working Copy quedará sin los cambios que se habian aplicado.



¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? 
Utilicé: git reflog
         git reset <Commit ID>
	 git status
	 git restore git-nuestro.md

Porque: Utilizó **git reflog** para mirar el último <Commit ID> que deshice, luego muevo mi Branch (styled) y Head 
con **git reset <Commit ID>**, despues ingreso **git status** para ver el archivo de texto modificado que
remplazará a la primera versión proveniente del Commit anterior y restauro el archivo modificado con 
**git restore git-nuestro.md**



El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 
No causó conflicto.
Porque:  Styled tiene el mismo texto de master + la  incorporación de caracteres marckdow. Y en resumen, no modifica las 
líneas sino que agrega caracteres. Por eso no hay conflicto, porque no cambia la base del commit master (padre).



El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 
Si, causó conflicto.
Porque: Al hacer un fast forward (merge por defecto), perdería el contenido del commit donde inicialmente estaba la rama styled.
Será necesario crear un commit hijo de las ramas styled y htmlify.



El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No causó conflicto.
Porque: El Commit styled proviene desde el Commit master, por lo que tenía acceso a sus Commit. Cuando la rama master absorbe 
a la rama styled, actualizá el contenido de su Commit.



¿Qué comando o comandos utilizaste en el paso 25?
Utilicé: git log --graph



El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 
Si, podría ser fast forward porque el Commit con la arama "title" proviene de "master", por lo que no generaría conflicto ya que
"title" tiene acceso a "master". 



¿Qué comando o comandos utilizaste en el paso 27? 
 1°: git reflog, para conocer Commit_Id de Master antes de que absorbiera a title
 2°: git reset <Commit_Id>, deshago el merge sin perder los cambios de working Copy



¿Qué comando o comandos utilizaste en el paso 28? 
 1°: git status
 2°: git restore git-nuestro.md



¿Qué comando o comandos utilizaste en el paso 29? 
 1°: git branch -D title



¿Qué comando o comandos utilizaste en el paso 30? 
 1°: git reflog , para conocer el Commit_Id resultante cuando Master absorbió a title
 2°: git checkout <Commit_Id>



¿Qué comando o comandos usaste en el paso 32? 
 1°: git reflog , para conocer el Commit_Id inicial cuando se ingresó el poema
 2°: git reset <Commit_Id> , vuelvo al commit inicial sin descartar cambios
 3°: git status , reviso el estado del archivo git-nuestro.md, y para descartar cambio ingreso el siguiente comando:
 4°: git restore git-nuestro.md



¿Qué comando o comandos usaste en el punto 33? 
 1°: git reflog , para conocer el Commit_Id final cuando se ingresó el titulo al poema
 2°: git reset --hard <Commit_Id> , vuelvo al commit inicial y descartar cambios









