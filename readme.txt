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
			git reflog	--记录历史命令