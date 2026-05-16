git commit --amend 用于修改最近一次的commit。

最常见的两种用法： 

只改提交信息：git commit --amend -m "新的提交信息"。

补提交漏掉的文件：先 git add `<file>`，再 git commit --amend --no-edit。

需要注意的是，amend 实际上是生成了一个新的 commit（hash 会变），替换掉原来的那个。

所以如果原 commit 已经 push 到远程并被别人拉过，不要 amend，否则会让别人的本地历史对不上。

对已推送的 commit 改完后必须 git push --force-with-lease（比 --force 更安全，因为它会检查远程有没有被别人推过新 commit）。
