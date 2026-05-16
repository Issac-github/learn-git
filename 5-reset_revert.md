### git reset `<commit>`：

把 HEAD 指针往回移动到指定commit，后面的commit 会消失，本质是改写历史。

执行后，需要执行git push --force。

不适合已经 push 到共享远程的commit，否则会和其他人的本地历史冲突。

### git revert `<commit>`：

生成一条新的commit，这条新commit的内容正好是指定commit 的反向（undo），原来的commit依然保留在历史中，不会改写历史。

安全，适合在共享分支上回滚已发布的改动。 

### 简单口诀：

reset是把时间倒回去，revert是走一步后退的步子。

共享分支永远优先用revert。
