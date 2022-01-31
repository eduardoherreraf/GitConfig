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

### AÑADIR ARCHIVOS AL ÁREA DE PREPARACIÓN PARA EL COMMIT

- Añadir **todos** archivos:

```ssh
git add .
```

- Añadir el archivo **file**:

```ssh
git add file
```

### SACAR ARCHIVOS DEL ÁREA DE PREPARACIÓN

- Sacar el archivo **file**:

```ssh
git restore --staged file
```

### VOLVER AL ESTADO DEL ÚLTIMO COMMIT

- Dejar todos los archivos guardadados tal como estaban en el último commit

```ssh
git checkout -- .
```

### CONFIRMAR LOS ARCHIVOS GUARDADADOS

- Confirmar los archivos guardadados con `git add`

```ssh
git commit -m "mensaje"
```

- Comando que añade y confirma los archivos:

```ssh
git commit -am "mensaje"
```

- Corrige el mensaje del último commit:

```ssh
git commit --amend "mensaje"
```

### LISTADO DE COMMITS HECHOS

- Listado de Commits:

```ssh
git log
```

- Listado de Commits una línea por commit:

```ssh
git log --oneline
```

- Listado de los primeros **N** Commits:

```ssh
git log -N
```

- Listado de commits con el nombre de archivos afectados:

```ssh
git log --raw
```

- Listado de commits con cambios hechos en los archivos:

```ssh
git log --patch
```

### RAMAS

- Muestra la rama actual:

```ssh
git branch
```

- Se crea una **Rama** y salta a ella:

```ssh
git checkout -b Rama
```

- Salta a la rama Master:

```ssh
git checkout Master
```

- Fusión **Rama** con Master:

```ssh
git merge Rama
```

- Borrar la **Rama** con Master (se debe estar en Master):

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
git push --set-upstream origin Rama
```

### BAJAR LOS CAMBIOS

- Bajar los cambios de los archivos del repo remoto

```ssh
git pull
```

---

```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
