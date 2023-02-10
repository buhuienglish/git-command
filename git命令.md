#### git命令



**分支查看**

```sh
git branch

git checkout 

git branch -a|grep +关键字
```



**复制分支**

①：git branch 分支名：新建本地分支

git merge --no-edit 另一个分支名：复制到另一个分支

②：git checkout -b tmp：在被复制分支执行，不得先创建tmp分支



**分支提交**

```sh
git push origin tmp:提交分支

git push origin --delete tmp：删除远程分支
```



**分支完整加载**

```sh
git submodule init

git submodule update
```



**分支缓存本地以及恢复**

```sh
git stash 

git stash list，查看本地当前的缓存列表。

git stash apply stash@{id}，恢复指定id的stash内容，同时不会删除恢复的缓存条目。

git stash pop，恢复最近的缓存到当前文件中，同时删除恢复的缓存条目。
```



**提交代码到远程库**：

```sh
git status             # 查看本地代码状态

git add .              # 添加修改代码到缓存

git commit -m "一些信息"  # 提交

git push 仓库地址        # push进去了

```



**删除本地分支tmp**

```sh
 git checkout dev 删除分支前先切换到其他分支

 git branch -D tmp
```



**复制本地已经改变的分支到另一个分支**

```sh
git status

git stash 

git checkout -b tmp：在被复制分支执行，不得先创建tmp分支

git stash list

git stash apply stash@{id}
```



git fetch :指令是强制下载远程仓库最新内容

```sh
git fetch --all  
git reset --hard origin/master 
git pull
```



```sh
#解决git add不显示中文的
git config --global core.quotepath false 

#美化显示git log
git log --oneline --graph --decorate --all


```
