# LOS COMANDOS MÁS USADOS EN GIT

## CONFIGURACIÓN INICIAL

- Nombre del usuario:

```ssh
   git config --global user.name "Eduardo Herrera Forero"
```

- Correo Electrónico de Usuario

```ssh
git config --global user.email "ehfeduardo@gmail.com"
```

- Editor de texto usado (Visual Studio Code):

```ssh
git config --global core.editor "code --wait"
```

- Inhabilita la conversión los finales CRLF en LF:

```ssh
git config --global core.autocrlf false
```

- No pagina los resultados de log o diff:

```ssh
git config --global core.pager ''
```

## CONFIGURACIÓN ALIAS CON ATAJOS DE TECLADO

En el archivo c:Program Files/Git/etc/gitconfig se le agrega al final:

```ssh
[alias]
    br = branch
    ci = commit
    co = checkout
    cob = checkout -b
    d = diff
    lo = log
    lg = log --pretty=format:'%h - %an, %ar : %s' --graph
    lgc = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)%Creset' --abbrev-commit --date=relative
    lgb = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)%Creset' --abbrev-commit --date=relative --branches
    hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
    st = status
    ri = rebase --interactive
    rc = rebase --continue
    mt = mergetool
    rf = reflog
    last = log -1 HEAD
    alias = config --get-regexp ^alias\\.
    lost = fsck --full
    broken = fsck --unreachable
    po = push origin HEAD:refs/for/master
    rs = rebase --skip
    type = cat-file -t
    dump = cat-file -p
```

## Los COMANDOS MÁS USADOS

```ssh
git clone <url del Repo> o git init

git add .
git commit -m "mensaje"
git push
git log
git status

git checkout -b Rama
git push --set-upstream origin Rama
git merge Rama -m "mensaje"
git branch -d Rama

git pull
```

## LOS COMANDOS PARA EL MANEJO DE ARCHIVOS EN GIT

### INICIAR REPOSITORIO

- Bajar el repo (clonar repo en local):

```ssh
git clone <url del Repo>
git clone <url del Repo> <carpeta local>
```

- iniciar el repo local:

```ssh
git init
```

### PREPARAR ARCHIVOS PARA EL COMMIT

- Preparar todos los archivos:

```ssh
git add .
```

- Preparar el archivo **file**:

```ssh
git add file
```

### DESHACER ARCHIVOS PREPARADOS

- Deshacer el archivo **file**, si es nuevo:

```ssh
git rm --cached file
```

- Deshacer el archivo **file**, si es modificado:

```ssh
git restore --staged file
```

### VOLVER AL ESTADO DEL ÚLTIMA CONFIRMACIÓN

- Dejar todos los archivos confirmados tal como estaban en el último commit

```ssh
git rm --cached .
```

### VER ESTADO DE LOS ARCHIVOS

- Muestra el estado de los archivos.

```ssh
git status
git st -s (versión abreviada)
git st --short (versión abreviada)
```

### CONFIRMAR LOS ARCHIVOS PREPARADOS

- Confirmar los archivos preparados con `git add`

```ssh
git commit -m "mensaje"
```

- Prepara y confirma los archivos a la vez:

```ssh
git commit -am "mensaje"
```

- Confirma los archivos que hicieron al último commit y/o cambio del mensaje, se edita la última confirmación:

```ssh
git commit --amend "mensaje"
```

### DESHACER LA CONFIRMACIÓN

- Se deshace la confirmación del archivo **file**:

```ssh
git rm --cached file
```

- Deshacer el comando anterior, vuelve a confirmar el archivo **file**:

```ssh
git restore --staged file
```

### HISTORIAL DE CONFIRMACIONES HECHAS

- Listado de Confirmaciones:

```ssh
git log
```

- Listado de Confirmaciones una línea por Confirmación:

```ssh
git log --oneline
```

- Número de Confirmaciones hechas hasta el momento:

```ssh
git log --oneline | wc -l
```

- Listado de las primeras **N** Confirmaciones:

```ssh
git log -N
```

- Listado de las Confirmaciones con el nombre de archivos afectados:

```ssh
git log --raw
```

- Listado de las Confirmaciones con cambios hechos en los archivos:

```ssh
git log --patch
```

- Listado de las Confirmaciones con los cambios hechos en cada Confirmación de las últimas **N**:

```ssh
git log -p -N
```

### RAMAS

- Muestra la rama actual:

```ssh
git branch
```

- Se crea una **Rama** y salta a ella:

```ssh
git branch Rama
git checkout Rama
```

```ssh
git checkout -b Rama
```

- Salta a la **Rama**:

```ssh
git checkout Rama
git checkout master

```

- Cambio de nombre de **Rama** a **Rama2**:

```ssh
git branch -m Rama2
```

- Fusión **Rama** con Master:

```ssh
git merge Rama -m "mensaje"
```

- Borrar la **Rama** (se debe estar en Master):

```ssh
git branch -d Rama
```

### ENVIAR A UN REPO EXTERNO

- Subir los archivos al repo remoto

```ssh
git push
```

- Subir los archivos de la **Rama**

```ssh
git push -u origin Rama
```

### BAJAR LOS CAMBIOS

- Bajar los cambios de los archivos del repo remoto (master)

```ssh
git pull
```

## FORMA DE SALIR DEL EDITOR VIM

Teclear <esc> wq!
