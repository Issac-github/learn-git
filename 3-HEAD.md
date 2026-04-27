### HEAD

正常情况下指向"当前分支的最新 commit"。

更准确地说，它通常指向一个分支引用（如 refs/heads/main），然后这个分支再指向具体的 commit。

### 游离+HEAD（detached+HEAD）

当执行 git checkout  `<commit-hash>` 或 git checkout `<tag>` 时，HEAD会直接指向一个 commit 而不是分支。

此时提交的 新commit 不属于任何分支，一旦 git switch，这些 commit 就可能被垃圾回收而丢失。

如果在 detached+HEAD 状态下做了重要修改，一定要 git switch -c new-branch 创建一个新分支把它们保存下来。
