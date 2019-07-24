用于学习git开发流程的记录
=======================
1.git教程<br>
https://www.liaoxuefeng.com/wiki/896043488029600<br>
https://git-scm.com/book/zh/v2<br>
2.readme教程https://blog.csdn.net/kaitiren/article/details/38513715<br>
3.readme模版https://github.com/guodongxiaren/README/edit/master/README.md

README
===========================
该文件用来测试和展示书写README的各种markdown语法。GitHub的markdown语法在标准的markdown语法基础上做了扩充，称之为`GitHub Flavored Markdown`。简称`GFM`，GFM在GitHub上有广泛应用，除了README文件外，issues和wiki均支持markdown语法。

****
	
|Author|dengxit|
|---|---
|E-mail|dengxit@foxmail.com

    Hello,大家好，我是dengxit。
    
git流程简记
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





链接
--------------------------------
[dengxit的网站](http://www.dengxitong.com "我的网站")
--------------------------------
