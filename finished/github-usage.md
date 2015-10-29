# GitHub的初步使用
本文系本人在使用git和github的实践中自行爬网总结 跪求大神勿喷
## 准备
- [创建账户](https://github.com/join)
- [下载Github客户端](https://desktop.github.com/)（有果子机和PC的版本，Linux用户请自行安装git这个包）

> 安装客户端时请保证有网络连接。

## 名词解释
- repository
repository叫做软件仓库，一般将一个完整的项目的源文件放到一个软件仓库中。

- branch
branch叫做分支。默认的分支叫做master（主分支）。创建分支时，会从一个已有的分支将全部文件拷到新的分支中，对分支的更改不影响其它分支，一般是开发新功能时使用。分支做完后，可以和其它分支合并（merge），这个过程一般是自动的。

## 提交文件的过程

** 文件在正式被提交之前会经过三个地方 **
** 本地仓库（你编辑文件的地方）→缓存区→HEAD（这是提交到github之前的最后一个本地位置） 这之后便提交到远端仓库 **

1. 在github网站登录并创建新的仓库（或使用客户端创建）。
2. 在本地创建文件夹，并将github上创建的库克隆到本地。按客户端提示操作。
3. 现在本地的库中除了gitignore（可能还有readme）之外应该什么都没有
4. 在本地库的目录创建并编辑文件，然后保存
5. 在github客户端中，右击你的库，点“在GitShell打开”（Open in Git Shell）。
6. 在弹出的命令行里输
>git add *
这会添加所有文件到缓存区，或者
git add ----all（两个短横线。吐血推荐此命令）
这个是添加所有文件，包括子目录（比如/sources/aaa.txt这样的）

7. 在本地提交改动。在命令行里输
>git commit [-m add your descriptions here]
>
>这将把改动提交到HEAD。

8. 将改动提交到github。在命令行输
> git push origin master
> 这将把改动提交到master分支。可以提交到其他分支。分支之间是隔离的

9. 合并分支。在github客户端中切到要合并到的分支（而不是被合并的分支），然后点“比较”（compare），在弹出的列表中选择要被合并的分支，点update from xxx，合并的信息将被写入HEAD。然后点最右边的sync，就可实际提交更改到github。或者直接在命令行输：
> git merge (branch-name)
> 
> 这将把分支（branch-name）合并到你的当前分支
>
> 要更改当前分支，执行：
>
> git checkout （branch-name）
>
> 这将切换到（branch-name）分支。10. 根据远端仓库更新本地仓库：
>
> git pull

11. 回滚更改
> git checkout --(filename)

## pull request的使用
1. 先fork一个仓库，这样你就有了一个和原仓库完全一样的仓库

2. 在你的repository中改动完毕之后，希望原仓库合并你的工作（原仓库不是你的），就去原仓库的页面提交你的pull request，选择分支，等待审核，通过之后即可被合并到原仓库中，这样你就为别人的开发做了贡献

## issues
issues是用来提交问题的。如果发现有什么问题 或者有什么建议 可以在issues提交。