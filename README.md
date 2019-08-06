# Git操作介绍：
A simple introduction for git, maybe in VScode.

今天刚好给电脑重新配置git，所以上传上来记录一下，免得每次都得重新搞，给我这样的小白看的，嘻嘻嘻。

[whole.md](https://github.com/SadAngelF/git_Introduction_for_newer/blob/master/whole.md)是一份完整的git教程，是一个系统过程，此md只展示一些遇到的问题和代码。

# vscode配置git

1. 下载git，应该会默认配置到环境变量里，如果没有自己百度一下配置环境变量

2. 配置环境变量，最终的目录是：cmd\git.exe

3. 新建文件夹作为配置：

    git init

    git config --global user.name "用户名" 

    git config --global user.email "邮箱"

4. 提交第一个代码，并输入密码：

    执行git初始化仓库命令git init

    执行添加文件目录到git仓库命令 git add . （. 小数点是添加当前目录下的所有文件 也可以只添加制定文件或者文件夹）
    
    执行上传到git仓库命令git commit -m "可写注释内容"
    
    执行git仓库与github仓库的连接命令git remote add origin 仓库地址）
    
    执行推送到分支(master)的命令git push -u origin master（分支名字master为主分支）
    
5. 输入用户和密码之后保存：

    git config --global credential.helper store


# Git使用过程中的一些细节：

## 1. git提交时，出现本地与远程仓库不匹配，比如远程有readme.md，但是本地没有，所以无法提交时：问题如下图：

    ![错误图片](https://github.com/SadAngelF/git_Introduction_for_newer/blob/master/rejected.png)

    最简单的方法是：利用git pull将本地和远程先同步，再修改本地，再提交

    如果本地只是缺少readme：git pull --rebase origin master

    如果已经修改了文件：git pull origin master --allow-unrelated-histories //把远程仓库和本地同步，消除差异

## 2. 本地已有git仓库，只是修改文件之后（或者是git clone了一个仓库修改想提交）：

    git add 文件名
    
    git commit -m "文件注释"              //建议增加注释，说明本次push改变了什么，方便别人实时追踪代码

    git push -u origin master

## 3. 删除远程错误上传的文件：

    git rm -r -n --cached 文件/文件夹名称

    //加上 -n 这个参数，执行命令时，是不会删除任何文件，而是展示此命令要删除的文件列表预览。

    git rm -r --cached 文件/文件夹名称

    //真正地删除

    git commit -m "提交说明"
    
    git push -u origin master

    //完成

# 目前遇到的问题大概是这样，后续待更新！！！
