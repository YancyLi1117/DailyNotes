# Git Tutorial

<img src="https://i.postimg.cc/RVrM69ts/Snipaste-2023-04-15-23-34-35.jpg" style="zoom:50%;" />

interactive tutorial: https://learngitbranching.js.org

about branch

```bash
#list all the remote and local branch
git branch -a
#new a branch xxx
git branch xxx
#switch to a branch
git checkout xxx
#new and switch to a branch
git checkout -b xxx
#switch branch b to branch a
git branch -f b a
```

merge and rebase

```bash
#保留完整记录
git merge xxx
#提交干净线性的记录
git rebase xxx
#更改提交记录顺序为c4 c3 c2
git cherry-pick c4 c3 c2
git rebase -i HEAD~4 #弹出交互面板进行调整
```

about HEAD

```bash
#isolate the HEAD 
git checkout xxx[the hash of the dot]
#HEAD的第n个父提交
HEAD^
#HEAD的第n个祖先提交
HEAD~
(<commit>|HEAD)~n = (<commit>|HEAD)^^^…(^的个数为n)
```

about remote

```bash
#从远程a分支拉取到本地b分支
git fetch origin a:b
#从远程a拉取合并到本地b分支，可以用rebase合并
git pull --rebase origin a:b 
#查看staging有无commit了没push上去的
git cherry
#修改commit的message
git commit --amend
#查看当前分支版本历史
git log
```

about modifying and repeal

```bash
#重置staging的指定文件，与上一次commit保持一致，但工作区不变
git reset [file]
# 重置当前分支的指针为指定commit，同时重置staging，但workplace不变
git reset [commit]
# 重置当前分支的HEAD为指定commit，同时重置staging和workplace，与指定commit一致
git reset --hard [commit]
# 暂时将未提交的变化移除，稍后再移入
git stash
git stash pop
```

