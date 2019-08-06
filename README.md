# Git操作介绍：
A simple introduction for git, maybe in VScode.

今天刚好给电脑重新配置git，所以上传上来记录一下，免得每次都得重新搞，给我这样的小白看的，嘻嘻嘻。


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
    
    执行git仓库与github仓库的连接命令git remote add origin https://github.com/你的github的用户名/test.git（这里是你创建的仓库名字加上 .git）
    
    执行推送到分支(master)的命令git push -u origin master（分支名字master为主分支）
    
5. 输入用户和密码之后保存：
    git config --global credential.helper store