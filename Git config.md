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

## CONFIGURACIÓN ALIASES COMO ATAJOS DE TECLADO

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
git clone **url del Repo**
```

- iniciar el repo local:

```ssh
git init
```

## AÑADIR ARCHIVOS AL ÍNDICE

- Añadir **todos** archivos al índice:

```ssh
git add .
```

4. Sacar archivos del índice: `git restore --staged **file**` 5. Agregar archivos: `git commit -m "mensaje"` 6. Deja los archivos tal cual estaba en el último commit: `git checkout -- **file**` 7. Correción del mensaje del último commit: `git commit --amend` 8. listado de commits: `git log` 9. listado de commits en una línea: `git log --oneline` 10. ver un número limitado de commits (últimos tres): `git log -3` 11. Listado de commits con el nombre de archivos afectados: `git log --raw` 10. Listado de commits con cambios hechos en los archivos: `git log --patch`

5. git checkout -b miRama
6. git branch
7. git checkout master
8. git branch -d miRama
9. git push
10. git push --set-upstream origin miRama
11. git commit -am "msg"
12. git pull

```ssh

```
