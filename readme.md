#### 用于学习git开发流程的记录
=======================

* git教程
https://www.liaoxuefeng.com/wiki/896043488029600<br>
https://git-scm.com/book/zh/v2<br>
* readme教程https://blog.csdn.net/kaitiren/article/details/38513715<br>
* readme模版https://github.com/guodongxiaren/README/edit/master/README.md

#### README
===========================
* 该文件用来测试和展示书写README的各种markdown语法。GitHub的markdown语法在标准的markdown语法基础上做了扩充，称之为`GitHub Flavored Markdown`。简称`GFM`，GFM在GitHub上有广泛应用，除了README文件外，issues和wiki均支持markdown语法。

****
	
|Author|dengxit|
|---|---
|E-mail|dengxit@foxmail.com

    Hello,大家好，我是dengxit。
    
#### git流程简记
===========================
```
1.新建issue
2.根据issue号在本地基于master切issue-XXXX分支:git checkout -b issue-XXXX
3.开发&本地测试
4.git status
5.git add .
6.git commit -m "add: XXXXXXXX. close #XXXX"(add,fix,opt... #后的XXXX对应issue号)
7.git push origin issue-XXXX
8.提pr，跑ci，申请review，不通过接着改，循环3->7
9.通过，被merge，issue关闭；
10.出现bug，重开关闭的issue，基于master切bug分支:git checkout -b issue-XXXX-1(无bug则跳过10，11两步)
11.循环3-6，git push origin issue-XXXX-1
12.git checkout master
13.git pull
14.循环1-9开发新功能
```

#### github初始化设置
* 生成 ssh key 
ssh-keygen -t rsa -C "dengxit@gmail.com"
* 将sshkey添加到github设置中
* 测试连接
ssh -T git@github.com
ssh-add ~/.ssh/github_rsa （链接失败执行）
* github新建一个项目
* 本地新建一个项目
 git init
 git remote add github XXXXXXXX/XXX.git
 git add .
 git push origin master

#### cherry_pick
```
将某个分支上特定的更改拉到当前分支
```

#### 撤销 最后 一次错误的commit
* 例如：有多个个commit如下
```
commit4
commit3
commit2
commit1
```
* 如果commit4 已经提交 ，想要撤销，执行如下操作
```
git reset --hard HEAD~1
git push --force
```
* 这样commit4就被撤销了。不过如果commit4后有commit5提交，在强制推送后commit5也会消失



#### 链接
--------------------------------
[dengxit的网站](http://www.dengxitong.com "我的网站")
--------------------------------
