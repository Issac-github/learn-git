### git reset `<commit>`：

把 HEAD 指针往回移动到指定commit，后面的commit 会消失，本质是改写历史。

执行后，需要执行git push --force。

不适合已经 push 到共享远程的commit，否则会和其他人的本地历史冲突。

### git revert `<commit>`：

生成一条新的commit，这条新commit的内容正好是指定commit 的反向（undo），原来的commit依然保留在历史中，不会改写历史。

安全，适合在共享分支上回滚已发布的改动。

### git reset --hard ORIG_HEAD<commit></commit>：

| 部分                   | 含义                                                       |
| ---------------------- | ---------------------------------------------------------- |
| **ORIG_HEAD**    | 上一个大操作（如 merge、rebase）**之前** HEAD 的位置 |
| **reset --hard** | 强制重置当前分支到指定位置，**丢弃所有更改**         |

```shell
# 查看最近的操作历史
git reflog

# 查看当前 HEAD 和 ORIG_HEAD 的位置
git log -1 HEAD
git log -1 ORIG_HEAD

# 在当前位置创建备份分支
git branch backup-before-reset

# 然后执行重置
git reset --hard ORIG_HEAD

# 如果出问题，可以恢复
git reset --hard backup-before-reset
```

**合并失败后回滚**

```shell
git merge feature-branch
# 合并出现冲突，想放弃合并
git reset --hard ORIG_HEAD  # 回到 merge 前
```

**Rebase 失败后回滚**

```shell
git rebase main
# Rebase 出错，想放弃
git reset --hard ORIG_HEAD  # 回到 rebase 前
```

**Pull 失败后回滚**

```shell
git pull origin main
# Pull 出错
git reset --hard ORIG_HEAD  # 恢复到 pull 前状态
```

### 简单口诀：

reset是把时间倒回去，revert是走一步后退的步子。

共享分支永远优先用revert。
