### 撤回 git commit

git commit -m 注释内容

git reset --soft HEAD^ (分别回退commit的内容和add的内容) (equal to git reset --soft HEAD^1)

git reset --mixed HEAD^ (回退commit的内容) (equal to git reset HEAD^)

`--mixed` 参数是 `git reset` 命令的默认选项

### 撤回 git push

git reset HEAD^

git push origin YOURBRANCH --force
