
`git tag` 用于给某个 commit 打一个固定的名字（通常是版本号，比如 `v1.0.0`），方便以后找到这个"关键节点"，比如发布版本、里程碑。

两种标签：

* **轻量标签（lightweight tag）** ：`git tag v1.0`，只是一个指向 commit 的指针，没有任何额外信息。
* **附注标签（annotated tag）** ：`git tag -a v1.0 -m "release 1.0"`，会作为**独立的对象**存储在 Git 里，包含打标签者、日期、说明、甚至 GPG 签名。

 **发布版本时应该用附注标签** ，因为它带有完整的元数据，可追溯性更好；轻量标签更像是一次性的临时书签。

推送标签到远程：

* `git push origin v1.0`：推送单个
* `git push origin --tags`：一次推送所有本地标签

删除标签：

* 本地：`git tag -d v1.0`
* 远程：`git push origin --delete v1.0`
