git reset --soft：同时保留工作区和暂存区

git reset --mixed：工作区和暂存区保留在工作区，等价于git reset

git reset --hard：工作区和暂存区都不保留

撤销commit，或者撤销push和commit，同时实现以上效果

git reset --soft HEAD^1：撤销最近一次的commit

git reset --mixed HEAD^1：撤销最近一次的commit

git reset --hard HEAD^1：撤销最近一次的commit
