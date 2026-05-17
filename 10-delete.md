删除本地分支： 

git branch -d `<branch>`：安全删除，只有已经合并过的分支才允许删

git branch -D `<branch>`：强制删除（大写 D），未合并的也能删，要小心丢代码

删除远程分支： 

git push origin --delete `<branch>`（推荐写法）

等价写法 git push origin :`<branch>`（把"空"推上去，相当于删除）

清理已经在远程被删除但本地还缓存的跟踪分支： 

git fetch --prune 或 git remote prune origin
