# COMANDOS MÁS USADOS EM GIT
## config inicial
1. Nombre del usuario 
    `git config --global user.name "Eduardo Herrera Forero"}`
2. Correo Electrónico de Usuario  
    `git config --global user.email "ehfeduardo@gmail.com"`
3. Editor de texto usado 
    `git config --global core.editor "code --wait"`
4. Inhabilita la conversión los finales CRLF en LF
    `git config --global core.autocrlf false`
5. No pagina los resultados de log o diff - por defecto usa less  
    `git config --global core.pager ''`


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


