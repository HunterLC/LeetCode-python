配置过程就不多说了


进入需要存放文件的位置，git bash

第一步：就是把**fork过来的代码**克隆到我们本地
```
git clone <url>.git //这里<url>换成fork过来的库的链接

```
第二步：让自己的库跟别人远端的保持一致
```
//这里<url>别人库的链接
git remote add upstream <url> 

//查看结果，不出意外最后多了两个upstream，当然这个名字随意，是可替换的
git remote -v 

//拉取远端分支
git fetch upstream

//把远端的main合并到当前分支
git merge upstream/main
```
第三步：创建新的分支，通常开发新功能就应该在新分支中进行
```
git checkout -b 名称
git add .
git commit -m ""
git push origin 名称
```

第四步：删除名称
git branch -a
git branch -d 本地分支名
git push origin --delete 远程分支名


git config --global http.sslVerify "false"