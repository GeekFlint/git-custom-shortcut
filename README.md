## 一、命令方式直接配置

```
git config --global alias.co  checkout
git config --global alias.cm  commit
git config --global alias.cam 'commit -a --amend'
git config --global alias.csm 'commit -s -m'
git config --global alias.br  branch
git config --global alias.fo  'fetch origin'
git config --global alias.st  status
git config --global alias.sh  stash
git config --global alias.sp  stash pop
git config --global alias.unstage 'reset HEAD --'
git config --global alias.u  push
git config --global alias.pr  pull -r
git config --global alias.rv  review
git config --global alias.rb  rebase
git config --global alias.last log -1 HEAD
git config --global alias.lg  'log --pretty=format:"%h - %Cgreen%an%Creset, %ar : %Cgreen%s%Creset" --graph'
git config --global alias.slg  'log --pretty=format:\"%h - %Cgreen%an%Creset, %ar : %Cgreen%s%Creset\" --graph --stat'
git config --global alias.df  difftool
git config --global alias.sdf  'difftool --stat'
git config --global alias.ft  fetch
```



## 二、配置文件 .gitconfig 的方式

编辑或新增 /home/.gitconfig 文件，增加如下内容：

```
[url "ssh://xxxx@gerrit.xxx.com.cn"]
    pushInsteadOf = ssh://xxx@gerritro.xx.com.cn
[alias]
    co = checkout
    cm = commit
    cam = commit -a --amend
    csm = commit -s -m
    br = branch
    fo = fetch origin
    st = status
    sh = stash
    sp = stash pop
    unstage = reset HEAD --
    pu = push
    pr = pull -r
    rv = review
    rb = rebase
    last = log -1 HEAD
    lg = log --pretty=format:\"%h - %Cgreen%an%Creset, %ar : %Cgreen%s%Creset\" --graph
    slg = log --pretty=format:\"%h - %Cgreen%an%Creset, %ar : %Cgreen%s%Creset\" --graph --stat
    df = difftool
    sdf = difftool --stat
    ft = fetch
[color]
    ui = true
[difftool]
    prompt = false
[diff]
    tool = vimdiff
[core]
    editor = vim
    quotepath = false
[merge]
    tool = vimdiff
[mergetool]
    prompt = false
[user]
    email = xxx
    name = xxx
```

————————————————
版权声明：本文为CSDN博主「Karson Tiger」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/qq_41739313/article/details/120820758