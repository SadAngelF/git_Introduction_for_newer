# A-new-learning-process-for-Git
Chicken log!! This repository will be updated in a long time. Welcome to connect with me!!

MD 写得不好，勿喷，正在学，之后再更新！！！

## The base use for Git:
一、将本地项目上传到github

1、创建本地仓库（文件夹）

mkdir study//创建文件夹study
cd study //进入study文件夹

2、通过命令git init把这个文件夹变成Git可管理的仓库

git init //把这个文件夹变成Git可以管理的仓库

这时可以发现study里面多了个.git文件夹，它是Git用来跟踪和管理版本库的。如果你看不到，是因为它默认是隐藏文件，那你就需要设置一下让隐藏文件可见。

3、把项目粘贴到这个本地Git仓库里面（粘贴后你可以通过git status来查看你当前的状态），然后通过

git add . //把项目添加到仓库（或git add .把该目录下的所有文件添加到仓库，注意点是用空格隔开的）。在这个过程中你其实可以一直使用git status来查看你当前的状态。

git commit -m "注释"// 把项目提交到仓库。

4、在github上创建study文件夹后

git remote add origin https://github.com/husterlihuijuan/study.git   //与github（远程仓库）建立联系

git push -u origin master  //把本地库study的所有内容推送到远程仓库（也就是Github）上，此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

 至此就完成了将本地项目上传到Github的整个过程。

5、创建分支

git branch note //创建note分支

git checkout note //切换到note分支

6、把分支添加到github上

git push --set-upstream origin note //note分支已经上传到了 github

二、删除github上某个分支的文件夹

在github上只能删除仓库,却无法删除文件夹, 所以只能通过命令来解决，如下：删除master分支下的doc文件夹

git pull origin master //将远程仓库里面master分支的项目拉下来

dir  //查看master分支有哪些文件夹

git rm -r --cached doc  //删除master分支下的doc文件夹

git commit -m '删除了doc'  //提交,添加操作说明

git push origin master// 将本次更改更新到github项目上去

（每次增加文件、删除文件或修改文件，都要add、commit 然后直接 git push origin master，就可以同步到github上了）

三、从github上clone项目到本地

git clone https://github.com/SadAngelF/A-new-learning-process-for-Git.git

此时 在所选的盘里会自动有一个reacter文件夹，说明已经克隆到本地，但此时该目录 并不是git可以管理的仓库

进入该目录，在项目目录下

D:\reacter>git init //让该reacter目录变成git可以管理的仓库，且此时已经和远程仓库自动建立好了联系

但此时 只有一个master分支，若你需要另外一个分支，在另外一个分支上工作，把另外一个分支也克隆下来,如，你需要 greeting分支

D:\reacter>git checkout -b greeting origin/greeting //此时你就把greeting分支克隆到本地了，通过 git branch 可以查看

接下来就可以在本地进行工作了
