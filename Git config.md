# LOS COMANDOS MÁS USADOS EN GIT

## config inicial

1. Nombre del usuario: `git config --global user.name "Eduardo Herrera Forero"`
2. Correo Electrónico de Usuario: `git config --global user.email "ehfeduardo@gmail.com"`
3. Editor de texto usado: `git config --global core.editor "code --wait"`
4. Inhabilita la conversión los finales CRLF en LF: `git config --global core.autocrlf false`
5. No pagina los resultados de log o diff - por defecto usa less: `git config --global core.pager ''`

## CONFIGURACIÓN ALIASES COMO ATAJOS DE TECLADO

En el archivo se agrega al final => c:Program Files/Git/etc/gitconfig  
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

## LOS COMANDOS PARA EL MANEJO DE ARCHIVOS EN GIT

### Bajar el repo (clonar repo en local):

```ssh
`git clone dirección del Repo`
```

2. iniciar el repo local: `git init`
3. Adicionar archivos al índice: `git add **file**` 4. Sacar archivos del índice: `git restore --staged **file**` 5. Agregar archivos: `git commit -m "mensaje"` 6. Deja los archivos tal cual estaba en el último commit: `git checkout -- **file**` 7. Correción del mensaje del último commit: `git commit --amend` 8. listado de commits: `git log` 9. listado de commits en una línea: `git log --oneline` 10. ver un número limitado de commits (últimos tres): `git log -3` 11. Listado de commits con el nombre de archivos afectados: `git log --raw` 10. Listado de commits con cambios hechos en los archivos: `git log --patch`

4. git checkout -b miRama
5. git branch
6. git checkout master
7. git branch -d miRama
8. git push
9. git push --set-upstream origin miRama
10. git commit -am "msg"
11. git pull
