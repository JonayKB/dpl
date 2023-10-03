<div align=justify>
# Gestión básica de Git

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


- git config --list
	- salida:
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
## Tarea: Creación de un repositirio
```code
 mkdir dpl
 cd dpl
 git init
 ls -la
```
- git init
  - salida:
  yuda: Usando 'master' como el nombre de la rama inicial. Este nombre de rama predeterminado
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
  En la rama master
  No hay commits todavía
  no hay nada para confirmar (crea/copia archivos y usa "git add" para hacerles seguimiento)


- git nano indice.txt
  - salida:


- git status
  - salida:
  En la rama master
  No hay commits todavía
  Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que se será confirmado)
	indice.txt
  no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)



- git add indice.txt
  - salida:
  En la rama master
  No hay commits todavía
  Cambios a ser confirmados:
  (usa "git rm --cached <archivo>..." para sacar del área de stage)
	nuevos archivos: indice.txt

## Tarea: Realizando Commit's
```code
git commit -m "Añadido índice de la asignatura DPL."
git status
```

- git commit -m "Añadido índice de la asignatura DPL."
   - salida:
   [master (commit-raíz) 77a6741] Añadido índice de la asignatura DPL.
   1 file changed, 2 insertions(+)
   create mode 100644 indice.txt
- git status
  - salida
  En la rama master
  nada para hacer commit, el árbol de trabajo está limpio


</div>