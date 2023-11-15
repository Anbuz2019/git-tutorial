# GIT 初体验



## git diff 命令

**（工作树：即实际操作的目录，也就是工作区域）**

- `git diff` 		比较**暂存区**和工作区（工作树）的文件之间的差异
- `git diff HEAD`            比较**最新提交**和工作区（工作树）的文件之间的差异
- `git diff --cached`       比较**暂存区**和**最新提交**的文件之间的差异

<img src="res\git diff示意图.jpg" alt="image-20231115113156984" style="zoom: 40%;" />

## git checkout 命令

- `git checkout <branch name>`  切换到对应的分支中；
- `git checkout -b <branch name> `  创建新分支，并切换到对应的分支中；（相当于下面两句）
  - `git branch <branch name>`
  - `git checkout <branch name>`

- `git chaeckout -`  切换至上一个分支

- `git reflog`  查看当前仓库执行过的操作日志



## 特性分支

- **特性分支**：集中实现单一特性（主题）的分支，不进行任何额外的作业

- **稳定分支**：保留一个随时可发布的稳定版本，一般由 master 分支担当

- 基于特定主题的作业在特性分支中进行，主题完成后再与 master 分支合并
  - 主干分支：合并的最终点，没有开发到一半的代码，可随时供人查看
  - 即使在开发过程中发现了BUG，也需要再创建新的分支，在新分支中修正
  - 合并分支：`git merge --no-ff <branch name>`



## Log日志命令

- `git log`  打印日志
- `git log --pretty=short`  简略打印日志（只打印第一行）
- `git log -p`  详细打印文件的具体修改情况
- `git log --graph`   以图表形式查看分支日志 



## Rebase 压缩历史

- feature-C
