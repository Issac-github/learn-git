### 工作区 vs 暂存区

git diff

### 暂存区 vs HEAD

git diff --staged ( Equal to git diff --cached )

### 工作区(已被git跟踪，即被执行过add) + 暂存区 vs HEAD

git diff HEAD

### 分支 vs 分支

git diff branchA branchB

### commit vs commit

git diff commitA commitB

### 文件差异

git diff branchA branchB -- `<file>`

git diff commitA commitB -- `<file>`
