linux command:
		pwd:查看当前所在位置
		ls:查看当前目录下的子文件；-a查看隐藏文件-F方便分辨子目录和文件
		cd 目录 :进入目录
		mkdir 目录名：创建新目录
		touch 文件名.后缀 ：创建文件
		mv oldName	newName:修改文件名
		rm 删除文件。 rm -r 递归删除目录下的文件然后再删除自己
		rmdir删除目录(只能删除空目录)
		cat 文件名	--查看文件内容的	--一次性全部显示完
		more 文件名 --查看文件内容的(windows的git不支持该命令)	--一次只显示一个屏幕，需要用空格或者回车查看剩余内容
		less 文件名	--查看文件内容的	--一次只显示一个屏幕，需要用空格或者回车查看剩余内容
		tail -n 文件名	--只显示文件最后几行 -n 代表参数可以设置数值
			如： tail -n 10 readme.txt
				 tail -10 readme.txt			--两种输入皆可
		head -n 文件名	--只显示文件头部。用法同上。
		vim 文件名 --进入vim编译器，编辑文件：具体vim使用可以查看CSDN里的内容	http://blog.csdn.net/fungleo/article/details/53128157
		vim简单入门要熟悉vim请移步CSDN；
			输入 vim 文件名  后默认进入vim导航模式，导航模式下快捷键hjkl代表：左下上右;w --下一个单词,b	--前有一个单词,Ctrl+f	--下翻页
			Ctrl+b --上翻页；按a,i,o,进入编辑模式，推荐使用i；
			编辑完内容后按Esc键进入命令模式,命令模式下输入	:w --保存	:q	--退出  :q!	--不保存退出	常用	:wq --保存并退出
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
			配置远程仓库,看看用户主目录下(C:\Users\admin\.ssh)，有没有.ssh目录，有则跳过，无则创建SSH Key：
				ssh-keygen -t rsa -C "邮箱地址"
				配置完SSH Key后登陆GitHub把id_rsa.pub的文件内容复制到GitHub的‘Add SSH key ’中添加SSH
			添加远程仓库：
				GitHub上新建仓库；然后可以从新建的远程仓库克隆出一个新的，也可以把本地已经存在的本地仓库与之关联，然后把本地内容推送到GitHub上
				关联命令：	git remote add  远程仓库名(自起) git@github.com:sunbowenqz/dsfs.git
				第一次推送命令：	git push -u origin master		--origin是关联时任意起的远程仓库名字而已， master分支。
				在以上所有操作关联以及推送完成以后，我们的推送命令直接： git push 远程仓库名 master 即可。
			从远程仓库克隆项目：
				git clone https://github.com/sunbowenqz/Demo.git    	--git支持https,但通过ssh“支持的“的原生git协议速度最快
			
			
					
			
