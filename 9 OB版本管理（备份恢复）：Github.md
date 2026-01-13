
---
目录：[[【【【Obsidian总览】】】]]
上一页：
下一页：
关键词：
相关链接：[[8 ？？？OB同步]]

---
 
 > 注意：GitHub 不是**同步服务**！然而，它非常适合**异步协作**。


# 安装[GitHub Desktop](https://github.com/apps/desktop)


# 安装OB插件：Git
Git 的设计初衷并非用于将你的更改实时同步到云端或与他人共享。也就是说，它不适用于与他人实时协作。

https://publish.obsidian.md/git-doc/Installation

> 注意：仅仅安装[GitHub Desktop](https://github.com/apps/desktop)是**不够**的！你还需要安装常规的Git版本。

![image.png](https://repo.in4cell.com/2026/01/13_1768300927055.png)

# 安装Git

https://git-scm.com/install/windows

![image.png](https://repo.in4cell.com/2026/01/13_1768300954376.png)

![image.png](https://repo.in4cell.com/2026/01/13_1768300977660.png)


# OB仓库根目录创建文件：.gitignore

https://publish.obsidian.md/git-doc/Tips-and-Tricks#Gitignore

	# to exclude Obsidian's settings (including plugin and hotkey configurations)
	.obsidian/

	# to only exclude plugin configuration. Might be useful to prevent some plugin from exposing sensitive data
	.obsidian/plugins

	# OR only to exclude workspace cache
	.obsidian/workspace.json

	# to exclude workspace cache specific to mobile devices
.obsidian/workspace-mobile.json

	# Add below lines to exclude OS settings and caches
	.trash/
·.DS_Store

# 与 Obsidian Sync 配合使用时的注意事项

https://publish.obsidian.md/git-doc/Tips-and-Tricks#Usage+with+Obsidian+Sync

使用 Git 和 Obsidian Sync 的一个常见用例是使用 Obsidian Sync 在所有设备和 Git 之间进行同步，以此作为备份和版本历史记录的一种形式。

## 仅在一台设备上使用 Git 插件 ！

如果您正在同步已启用的插件及其设置，即使目录`.git`不存在或您不想在该设备上运行自动操作，Git 插件也会被启用并运行。要解决此问题，您可以在插件设置的“高级”选项下启用“在此设备上禁用”选项。此设置不会同步到其他设备。

## 使用 Git 插件，但不要用它来拉取文件！

另一种使用场景是，您可能不想在拉取操作时更新文件，因为 Obsidian Sync 已经更新了您的文件。您仍然可以进行提交/推送/提交并同步操作。要实现这一点，请在“拉取”操作下，将“合并策略”设置为“其他同步服务”。这样，在拉取操作时，只会将 HEAD 更新到最新的提交，而不会更改您的文件。
