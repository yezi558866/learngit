# learngit<br />
主要介绍使用git的命令。<br />
<br />
<br />
## 创建版本库<br />
mkdir learngit &nbsp;--创建目录<br />
cd learngit &nbsp;--进入目录<br />
pwd &nbsp;--目录路径<br />
git init &nbsp;--初始化，多出一个.git目录<br />
<br />
<br />
## 时光穿梭机<br />
git status &nbsp;--查看工作区状态<br />
git diff &nbsp;--查看修改内容<br />
git add &nbsp;--提交修改<br />
git commit -m &quot;discription&quot; &nbsp;--合并更改<br />
<br />
<br />
## 版本回退<br />
git reset --hard commit_id &nbsp;--回到某个版本<br />
git reset --hard HEAD^ &nbsp;--回退到上一个版本<br />
git log &nbsp;--查看提交历史，确定回退到哪个版本<br />
git log --pretty=oneline &nbsp;--日志显示在一行<br />
git reflog &nbsp;--查看命令历史，确定回到未来哪个版本<br />
<br />
<br />
## 撤销修改<br />
git checkout -- &lt;file&gt; &nbsp;--丢弃工作区的改动<br />
git reset HEAD &lt;file&gt; &nbsp;--把暂存区的修改撤销掉，重新放回工作区<br />
<br />
<br />
## 删除文件<br />
git rm &lt;file&gt; &nbsp;--从版本库删除文件<br />
<br />
<br />
## 远程仓库<br />
ssh-keygen -t rsa -C &quot;youremail@example.com&quot; &nbsp;--创建ssh key<br />
将id_rsa.pub添加至github上。<br />
<br />
<br />
## 添加远程库<br />
git remote add origin git@github.com:username/learngit.git &nbsp;--关联一个远程库<br />
git push -u origin master &nbsp;--把本地库的所有内容推送到远程库，第一次加“-u”<br />
git push origin master &nbsp;--推送命令<br />
<br />
<br />
## 从远程克隆<br />
git clone git@github.com:username/learngit.git<br />
<br />
<br />
## 创建与合并分支<br />
git branch &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;--查看分支<br />
git branch &lt;name&gt; &nbsp; &nbsp;--创建分支<br />
git checkout &lt;name&gt; &nbsp;--切换分支<br />
git checkout -b &lt;name&gt; &nbsp;--创建+切换分支。-b:表示创建并切换。<br />
git merge &lt;name&gt; &nbsp; &nbsp; &nbsp;--合并某分支到当前分支<br />
git merge --no-ff -m &quot;discription&quot; &lt;name&gt; &nbsp;--推荐使用“禁用Fast forward”来合并分支<br />
git branch -d &lt;name&gt; &nbsp;--删除分支<br />
git branch -D &lt;name&gt; &nbsp;--强行删除一个未被合并过的分支<br />
<br />
<br />
## 解决冲突<br />
git log --graph --pretty=oneline --abbrev-commit --查看分支合并图<br />
<br />
<br />
## bug分支<br />
git stash &nbsp;--工作现场保存<br />
git stash pop &nbsp;--回到工作现场<br />
git stash list &nbsp;--查看stash内容<br />
<br />
<br />
## 多人协作<br />
git push origin &lt;branch-name&gt; &nbsp;--推送自己的修改<br />
git pull &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; --远程分支比本地新，则拉最新<br />
git branch --set-upstream &lt;branch-name&gt; origin/&lt;branch-name&gt; &nbsp;--创建本地分支和远程分支的链接关系<br />
git remote -v &nbsp;--查看远程库信息<br />
git checkout -b &lt;branch-name&gt; origin/&lt;branch-name&gt; &nbsp;--在本地创建和远程分支对应的分支<br />
<br />
<br />
## 创建标签<br />
git tag &lt;name&gt; &nbsp;--用于新建一个标签<br />
git tag &lt;name&gt; &lt;commit id&gt; &nbsp;--在指定的commit id上打标签<br />
git tag -a &lt;tagname&gt; -m &quot;blabla...&quot; &nbsp;--可以指定标签信息，“-a”指定标签名，“-m”指定说明文字<br />
git tag -s &lt;tagname&gt; -m &quot;blabla...&quot; &nbsp;--可以用PGP签名标签<br />
git tag &nbsp; &nbsp; &nbsp; &nbsp; --可以查看所有标签<br />
git show &lt;tagname&gt; &nbsp;--查看标签信息<br />
<br />
<br />
## 操作标签<br />
git push origin &lt;tagname&gt; &nbsp;--推送一个本地标签<br />
git push origin --tags &nbsp; &nbsp; --推送全部未推送过的本地标签<br />
git tag -d &lt;tagname&gt; &nbsp;--删除一个本地标签<br />
git push origin :refs/tags/&lt;tagname&gt; &nbsp;--删除一个远程标签
