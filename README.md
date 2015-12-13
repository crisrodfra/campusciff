# EJECICIOS GIT

###2.1 REPOSITORIO CAMPUSCIFF (I)1. Crear un repositorio en vuestro GitHub llamado campusciff.

![MacDown logo](file:///Users/CristobalRodriguez/Desktop/resources/Crear%20Repositorio.tiff)

###2.2 REPOSITORIO CAMPUSCIFF (II)1. Clonar vuestro repositio en local.

```
MacBook-Pro-de-Cristobal:~ CristobalRodriguez$ git clone git@github.com:crisrodfra/campusciff.git
Cloning into 'campusciff'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Checking connectivity... done.
MacBook-Pro-de-Cristobal:~ CristobalRodriguez$ 
```
###2.3 README1. Crear (si no lo habéis creado ya) en vuestro repositorio local un documento README.md.

El fichero se había creado inicialmente al crear el repositorio.

###2.4 COMMIT INICIAL1. Añadir al README.md los comanddos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git add .
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git commit -m "Commit Inicial"
[master d4220f2] Commit Inicial
 1 file changed, 1 insertion(+)
```
###2.5 PUSH INICIAL1. Subir los cambios al repositorio remoto.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git push origin master
Counting objects: 3, done.
Writing objects: 100% (3/3), 309 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:crisrodfra/campusciff.git
   7721e11..d4220f2  master -> master
```
###2.6 IGNORAR ARCHIVOS (I)1. Crear en el repositorio local un fichero llamado privado.txt.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ touch privado.txt
```
2. Crear en el repositorio local una carpeta llamada privada.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ mkdir privada

```

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ ls
privada		privado.txt	readme.md

```
###2.7 IGNORAR ARCHIVOS (II)
1. Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.
 
Se ha editado el archivo **.gitignore** con el comando vim
Se han introducido dos líneas:

```
privado.txt  

privada/

```
Se ha grabado del fichero .gitignore con los cambios.

###2.8 AÑADIR FICHERO 1.TXT1. Añadir fichero 1.txt al repositorio local.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ touch fichero1.txt
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ ls
fichero1.txt	privada		privado.txt	readme.md

```
###2.9 CREAR EL TAG V0.11. Crear un tag v0.1.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git tag v0.1
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git tag
v0.1
```
###2.10 SUBIR EL TAG V0.11. Subir los cambios al repositorio remoto.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git add .
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git commit -m "Segundo commit"
[master 8809973] Segundo commit
 2 files changed, 2 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 fichero1.txt
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git push --tag origin master
Counting objects: 4, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 378 bytes | 0 bytes/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To git@github.com:crisrodfra/campusciff.git
   d4220f2..8809973  master -> master
 * [new tag]         v0.1 -> v0.1
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git list
* 8809973 (HEAD -> master, origin/master, origin/HEAD) Segundo commit
* d4220f2 (tag: v0.1) Commit Inicial
* 7721e11 Initial commit

```
###2.11 CREAR UNA RAMA V0.21. Crear una rama v0.2.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git branch v0.2
```2. Posiciona tu carpeta de trabajo en esta rama.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git checkout v0.2
Switched to branch 'v0.2'
```
###2.12 AÑADIR FICHERO 2.TXT1. Añadir un fichero 2.txt en la rama v0.2.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ touch fichero2.txt
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ ls
fichero1.txt	fichero2.txt	privada		privado.txt	readme.md
```
###2.13 CREAR RAMA REMOTA V0.21. Subir los cambios al repositorio remoto.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git add .
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git commit -m "Rama v0.2"
[v0.2 cb56fd0] Rama v0.2
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 fichero2.txt
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git push origin v0.2
Counting objects: 2, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 300 bytes | 0 bytes/s, done.
Total 2 (delta 1), reused 0 (delta 0)
To git@github.com:crisrodfra/campusciff.git
 * [new branch]      v0.2 -> v0.2
```
###2.14 MERGE DIRECTO1. Posicionarse en la rama master.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

```
2. Hacer un merge de la rama v0.2 en la rama master.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git merge v0.2
Updating 8809973..cb56fd0
Fast-forward
 fichero2.txt | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 fichero2.txt
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git list
* cb56fd0 (HEAD -> master, origin/v0.2, v0.2) Rama v0.2
* 8809973 (origin/master, origin/HEAD) Segundo commit
* d4220f2 (tag: v0.1) Commit Inicial
* 7721e11 Initial commit

```
###2.15 MERGE CON CONFLICTO (I)1. En la rama master poner Hola en el fichero 1.txt y hacer commit.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ vim fichero1.txt
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git add .
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git commit -m "Modificado fichero1 master Hola"
[master 7475c8c] Modificado fichero1 master Hola
 1 file changed, 1 insertion(+)
```
###2.16 MERGE CON CONFLICTO (II)1. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git checkout v0.2
Switched to branch 'v0.2'
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ vim fichero1.txt
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git add .
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git commit -m "Modificado fichero1 v0.2 Adiós"
[v0.2 704307c] Modificado fichero1 v0.2 Adiós
 1 file changed, 1 insertion(+)
```
###2.17 MERGE CON CONFLICTO (III)1. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git merge v0.2
Auto-merging fichero1.txt
CONFLICT (content): Merge conflict in fichero1.txt
Automatic merge failed; fix conflicts and then commit the result.
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git diff
diff --cc fichero1.txt
index a19abfe,e708525..0000000
--- a/fichero1.txt
+++ b/fichero1.txt
@@@ -1,1 -1,1 +1,5 @@@
++<<<<<<< HEAD
 +Hola
++=======
+ Adiós
++>>>>>>> v0.2
```
###2.18 LISTADO DE RAMAS1. Listar las ramas con merge y las ramas sin merge.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git branch --merged
* master
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git branch --no-merged
  v0.2 
```
###2.19 ARREGLAR CONFLICTO1. Arreglar el conflicto anterior y hacer un commit.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git list
*   2de7a76 (HEAD -> master) Merge branch 'v0.2'
|\  
| * 5f9ed6a (v0.2) Solucionar merge conflictivo
* |   ceb54b9 Solucionar merge conflictivo
|\ \  
| |/  
| * 704307c Modificado fichero1 v0.2 Adiós
* | 7475c8c Modificado fichero1 master Hola
|/  
* cb56fd0 (origin/v0.2) Rama v0.2
* 8809973 (origin/master, origin/HEAD) Segundo commit
* d4220f2 (tag: v0.1) Commit Inicial
* 7721e11 Initial commit
```
###2.20 BORRAR RAMA1. Crear un tag v0.2 

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git tag v0.2
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git tag
v0.1
v0.2
```
2. Borrar la rama v0.2

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git branch -d v0.2
Deleted branch v0.2 (was 5f9ed6a).
```
###2.21 LISTADO DE CAMBIOS1. Listar los distintos commits con sus ramas y sus tags.

```
MacBook-Pro-de-Cristobal:campusciff CristobalRodriguez$ git list
*   2de7a76 (HEAD -> master, tag: v0.2) Merge branch 'v0.2'
|\  
| * 5f9ed6a Solucionar merge conflictivo
* |   ceb54b9 Solucionar merge conflictivo
|\ \  
| |/  
| * 704307c Modificado fichero1 v0.2 Adiós
* | 7475c8c Modificado fichero1 master Hola
|/  
* cb56fd0 (origin/v0.2) Rama v0.2
* 8809973 (origin/master, origin/HEAD) Segundo commit
* d4220f2 (tag: v0.1) Commit Inicial
* 7721e11 Initial commit
```
2.22 CUENTA DE GITHUB1. Poner una foto en vuestro perfil de GitHub.
