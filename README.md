<div align="justify">


# Gestión básica de Git - Jonay Contreras

1. [Configuración](#tarea-configuración)

2. [Creación de un repositorio](#tarea-creación-de-un-repositorio)

3. [Comprobar el estado de un repositorio](#tarea-comprobar-el-estado-del-repositorio)

4. [Realizando Commit's](#tarea-realizando-commits)

5. [Modificación de ficheros](#tarea-modificación-de-ficheros)

6. [Historial](#tarea-historial)



## Tarea: Configuración

Configurar Git definiendo el nombre del usuario, el correo electrónico y activar el coloreado de la salida. Mostrar la configuración final.

```code
  git config --global user.name "Your-Full-Name"
  git config --global user.email "your-email-address"
  git config --global color.ui auto
  git config --list
```

- git config --globar color.ui auto
	- salida:

      ```code
      ```



- git config --list
	- salida:
      
      ```code
      user.email=jonaykb@gmail.com
      user.name=JonayKB
      color.ui=auto
      core.repositoryformatversion=0
      core.filemode=true
      core.bare=false
      core.logallrefupdates=true
      remote.origin.url=https://github.com/JonayKB/ETS
      remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
      branch.main.remote=origin
      branch.main.merge=refs/heads/main
      branch.feature_2.remote=origin
      branch.feature_2.merge=refs/heads/feature_2
      ```
    ---



## Tarea: Creación de un repositorio


```code
 mkdir dpl
 cd dpl
 git init
 ls -la
```



- git mkdir dpl
  - salida:

  ```code
  ```



- git cd dpl
  - salida:

  ```code
  ```



- git ls -la
  - salida:

  ```code
  total 24
  drwxrwxr-x 3 dam dam 4096 oct  3 15:22 .
  drwxrwxr-x 6 dam dam 4096 oct  3 14:56 ..
  drwxrwxr-x 8 dam dam 4096 oct  4 14:50 .git
  -rw-rw-r-- 1 dam dam 6663 oct  4 15:22 README.md
  ```




- git init
  - salida:

    ```code
    ayuda: Usando 'master' como el nombre de la rama inicial. Este nombre de rama predeterminado
    ayuda: está sujeto a cambios. Para configurar el nombre de la rama inicial para usar en todos
    ayuda: de sus nuevos repositorios, reprimiendo esta advertencia, llama a:
    ayuda: 
    ayuda: 	git config --global init.defaultBranch <nombre>
    ayuda: 
    ayuda: Los nombres comúnmente elegidos en lugar de 'master' son 'main', 'trunk' y
    ayuda: 'development'. Se puede cambiar el nombre de la rama recién creada mediante este comando:
    ayuda: 
    ayuda: 	git branch -m <nombre>
    Inicializado repositorio Git vacío en /home/dam/JonayKB/dpl/.git/
    ```


---



## Tarea: Comprobar el estado del repositorio


```code
 git status
 cat > indice.txt
 Capítulo 1: Instalación de Git por el alumno XXX
 Capítulo 2: Flujo de trabajo básico
 Ctrl+D
 git status
 git add indice.txt
 git status
```



- git status
  - salida:

    ```code
    En la rama master
    No hay commits todavía
    no hay nada para confirmar (crea/copia archivos y usa "git add" para hacerles seguimiento)
    ```



- git nano indice.txt
  - salida:

    ```code
    ```



- git status
  - salida:

    ```code
    En la rama master
    No hay commits todavía
    Archivos sin seguimiento:
    (usa "git add <archivo>..." para incluirlo a lo que se será confirmado)
    indice.txt
    no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)
    ```




- git add indice.txt
  - salida:

    ```code
    En la rama master
    No hay commits todavía
    Cambios a ser confirmados:
    (usa "git rm --cached <archivo>..." para sacar del área de stage)
    nuevos archivos: indice.txt
    ```



---



## Tarea: Realizando Commit's

```code
git commit -m "Añadido índice de la asignatura DPL."
git status
```



- git commit -m "Añadido índice de la asignatura DPL."
   - salida:

      ```code
      [master (commit-raíz) 77a6741] Añadido índice de la asignatura DPL.
      1 file changed, 2 insertions(+)
      create mode 100644 indice.txt
      ```



- git status
  - salida:

    ```code
    En la rama master
    nada para hacer commit, el árbol de trabajo está limpio
    ```


---




## Tarea: Modificación de ficheros

```code
cat > indice.txt
Capítulo 1: Instalación de Git por el alumno XXX _(donde XXX es el nombre del alumno)_
Capítulo 2: Flujo de trabajo básico
Capítulo 3: Gestión de ramas
Capítulo 4: Repositorios remotos
Ctrl+D
git diff
git add indice.txt
git commit -m "Añadido los capitulos 3"
```


- cat > indice.txt
  - salida:

    ```code
    ```



- git diff
  - salida:
      ```code
      -Capítulo 1: Instalación de Git por el alumno XXX
      -Capítulo 2: Flujo de trabajo básico
      +Capítulo 1: Instalación de Git por el alumno XXX _(donde XXX es el nombre del alumno)_
      +Capítulo 2: Flujo de trabajo básico
      +Capítulo 3: Gestión de ramas
      +Capítulo 4: Repositorios remoto
      ```


- git add indice.txt
  - salida:

    ```code
    ```



- git commit -m "Añadido los capitulos 3"
  - salida:

    ```code
    [master 5ac33b6] Añadido los capitulos 3
    1 file changed, 4 insertions(+), 2 deletions(-)
    ```



---



## Tarea: Historial 

```code
git show
git commit --amend -m "Añadido el capitulo sobre gestión de ramas al índice."
git show
```




- git show
  - salida:

    ```code
    commit 5ac33b687c044b7dc75cd289c19a7b0454e3ca44 (HEAD -> master)

    Author: JonayKB <JonayKB@gmail.com>
    Date:   Wed Oct 4 14:47:36 2023 +0100

    Añadido los capitulos 3
    diff --git a/indice.txt b/indice.txt
    index b29cf4c..f6b03eb 100644
    --- a/indice.txt
    +++ b/indice.txt
    @@ -1,2 +1,4 @@

    -Capítulo 1: Instalación de Git por el alumno XXX
    -Capítulo 2: Flujo de trabajo básico
    +Capítulo 1: Instalación de Git por el alumno XXX _(donde XXX es el nombre del alumno)_
    +Capítulo 2: Flujo de trabajo básico
    +Capítulo 3: Gestión de ramas
    +Capítulo 4: Repositorios remoto

    \ No newline at end of file
    ```


- git commit --ammend -m "Añadido el capitulo sobre gestión de ramas al índice."
  - salida:

    ```code
    [master c92f636] Añadido el capitulo sobre gestión de ramas al índice.

    Date: Wed Oct 4 14:47:36 2023 +0100

    1 file changed, 4 insertions(+), 2 deletions(-)
    ```



- git show
  - salida:

    ```code
    commit c92f636e05eafc9c400ed5b8b6a694c7b1979f62 (HEAD -> master)

    Author: JonayKB <JonayKB@gmail.com>
    Date:   Wed Oct 4 14:47:36 2023 +0100

    Añadido el capitulo sobre gestión de ramas al índice.
    diff --git a/indice.txt b/indice.txt
    index b29cf4c..f6b03eb 100644
    --- a/indice.txt
    +++ b/indice.txt
    @@ -1,2 +1,4 @@

    -Capítulo 1: Instalación de Git por el alumno XXX
    -Capítulo 2: Flujo de trabajo básico
    +Capítulo 1: Instalación de Git por el alumno XXX _(donde XXX es el nombre del alumno)_
    +Capítulo 2: Flujo de trabajo básico
    +Capítulo 3: Gestión de ramas
    +Capítulo 4: Repositorios remoto

    \ No newline at end of file
    ```


---



</div>