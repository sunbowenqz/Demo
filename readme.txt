git is a distributed version control system
git is free software
linux command:
		pwd:查看当前所在位置
		ls:查看当前目录下的子文件；-a查看隐藏文件-F方便分辨子目录和文件
		cd 目录 :进入目录
		mkdir 目录名：创建新目录
		touch 文件名.后缀 ：创建文件
		mv oldName	newName:修改文件名
study git command :
			git init;	---初始化本地git仓库
			git add file;	---添加文件
			git commit -m "dec"		---提交文件到git仓库
			git diff	---查看提交project的不同之处
			git status	---查看git仓库状态
			git log 	--查看历史记录
			git log --pretty=oneline 	--只显示描述和版本号
			git reset -hard	版本号		--回退到某一个版本	注意：HERD^ 表示回退到上一个版本HEAD^^表示回退到上上一个版本……
			git reflog	--记录历史提交(即：commit和reset)
			理解GIT操作管理的是修改而不是文件。如：修改文件后，add到暂存区，然后再次修改，然后commit到版本库中，此次提交的是第一次修改的内容，第二次的需要从新add再commit。
			版本回退的三种撤销方式：
						1.仅仅修改了工作区的内容，未提交到暂存区和版本库中。
							git checkout -- 文件名
						2.工作区修改后提交到了暂存区未添加到版本库中。
							git reset HEAD 文件名
						3.修改提交到了版本库中。
							使用之前的版本回退功能	git reset -hard 版本号
			删除文件：
					rm 文件名		--删除本地工作区的文件（rm命令删除文件，删除文件夹需要带参数-r,rmdir命令仅仅删除空目录，详细查看Linux命令行手册）
					git rm 文件名	--删除版本库中的文件。注意：如果删除的文件没有被提交，则该命令会报错。
					
			