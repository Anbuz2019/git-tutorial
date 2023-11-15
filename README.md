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
