[Github入门教程，适合新手学习（非常详细）_github教程-CSDN博客](https://blog.csdn.net/black_sneak/article/details/139600633)

[手把手教你用git上传项目到GitHub（图文并茂，这一篇就够了），相信你一定能成功！！ - 知乎](https://zhuanlan.zhihu.com/p/193140870)



上传本地文件到GitHub

```
git init //把这个目录变成Git可以管理的仓库
　　git add README.md //文件添加到仓库
　　git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了 
　　git commit -m "first commit" //把文件提交到仓库
　　git remote add origin git@github.com:wangjiax9/practice.git //关联远程仓库
　　git push -u origin master //把本地库的所有内容推送到远程库上
```



![img](https://i-blog.csdnimg.cn/blog_migrate/4f1cdb01c4d7eb6fd384fd84d3b232ea.png)
