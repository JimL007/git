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

## 5. 工作去和暂存区
啊哈哈哈!!!自行百度去吧!不做解释,本文档仅用于万一你忘了某天命令!

## 6. 删除文件和恢复文件
`git rm readme.md` //删除readme.md文件  
`git checkout -- readme.md` //让readme.md文件回到最近一次 `git add`或`git commit`的状态    

***
# 生成SSH key及访问Github

1. `ls -al ~/.ssh` 检查SSH key 是否存在
	*  存在:
		* `pbcopy < ~/.ssh/id_rsa.pub` 复制id_rsa.pub里的内容
		* 然后打开github将id_rsa.pub里的内容放入Key
	* 不存在:
		* `ssh-keygen -t rsa -C "your_email@example.com"` //生成新的SSH key
		* 都是开源的文件,一路回车即可.
2. `ssh git@github.com` //检测SSH key是否可以访问Github   

# 添加远程仓库
1. `git remote add origin https://github.com/JimL007(你的账户名)/learngit(仓库名).git 
`  将当前仓库与git仓库链接(在你的本地仓库下执行)
2. `git remote rm origin` 移出链接
3. `git push -u origin master`第一次推动master分支要使用该命令
4. `git push origin master` 将本地master分支推送到github

# 从远程仓库克隆
1. `git clone https://github.com/JimL007/gitskills.git` 克隆你的仓库



