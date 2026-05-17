### switch：

git switch `<branch>` ：切换已有分支

git switch -c `<branch>` ：切换并创建分支

### restore：

git restore `<file>` ：撤销工作区修改

git restore --staged `<file>` ：将暂存区撤回工作区，等价于 git reset HEAD `<file>`

git restore --source `<branch>` `<file>` ：指定分支

git restore --source `<commit-hash>` `<file>` ：指定commit hash

### checkout：

git checkout `<branch>` ：切换已有分支

git checkout -b `<branch>` ：切换并创建分支

git checkout -- `<file>` ：撤销工作区修改

git checkout `<branch>` -- `<file>` ：指定分支

git checkout `<commit-hash>` -- `<file>` ：指定commit hash
