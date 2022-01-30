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

## AÑADIR ARCHIVOS PARA EL COMMIT

- Añadir **todos** archivos:

```ssh
git add .
```

- Añadir el archivo **file**:

```ssh
git add file
```

## SACAR ARCHIVOS PARA EL COMMIT

- Sacar el archivo **file** del índice:

```ssh
git restore --staged file
```

- Dejar el archivo **file** como estaba en el último commit
  git checkout -- file

```ssh
git checkout -- file.ext
```

5. Agregar archivos: `git commit -m "mensaje"`
6. Deja los archivos tal cual estaba en el último commit: `git checkout -- **file**`
7. Correción del mensaje del último commit: `git commit --amend`
8. listado de commits: `git log`
9. listado de commits en una línea: `git log --oneline`
10. ver un número limitado de commits (últimos tres): `git log -3`
11. Listado de commits con el nombre de archivos afectados: `git log --raw`
12. Listado de commits con cambios hechos en los archivos: `git log --patch`

13. git checkout -b miRama
14. git branch
15. git checkout master
16. git branch -d miRama
17. git push
18. git push --set-upstream origin miRama
19. git commit -am "msg"
20. git pull

```ssh

```
