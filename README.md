# 关于Git的命令
***
## 1. 安装git
`git` //查看当前电脑是否安装了git  
`git config --global user.name "your name"` //设置你的git  
`git config --global user.email "email@example.com"` //设置你的邮箱地址  
## 2. 创建你的版本库
`mkdir learngit` //创建一个名为learngit的文件  
`cd learngit` //进入名为learngit的文件  
`pwd` //参看当前文件路径  
`git init` //将当前目录变为git可以管理的仓库  
`ls -ah` //显示隐藏的目录(如果没看到.git目录)  
`git add readme.md`// 将一个readme.md文件添加到当前仓库(文件还没有到达仓库)
`git commit -m"提交说明"` //将add里面的文件提交到仓库(文件到达仓库)

## 3. 查看仓库状态和文件
`git status` //查看仓库当前的状态   
`cat readme.md` //查看readme.md文件里的内容   
`git diff readme.md` // 查看仓库中的文件readme.md的具体修改内容  
`git checkout -- readme.md` //让文件回到最近一次 `git add`或`git commit`的状态    
`git diff HEAD -- readme.md` //查看工作区的readme.md文件和版本库里最新版的区别  

## 4. 仓库版本设置
`git log` // 查看当前仓库的提交历史记录(从最近到最远)
`git log --pretty=oneline`   
//查看当前仓库的提交历史记录(此时,`git commit -m"提交说明"`里面的提交说明就显的格外重要)  
`git reset --hard HEAD^` //将仓库退回上一个版本
`git reset --hard 版本号` //将仓库设置为版本号对应的版本
`git reset HEAD file`  //将暂存区的修改撤销掉,重新放回工作区(回退版本)
`git reflog` // 查找你曾输入的每一次命令(关于设置版本号的命令)

## 工作去和暂存区
啊哈哈哈!!!自行百度去吧!不做解释,本文档仅用于万一你忘了某天命令!



