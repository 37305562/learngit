来源于http://www.liaoxuefeng.com

- 1 创建版本库
	git init
	git add readme.txt
	git commit -m "wrote a readme file"
	git status
	git diff readme.txt 
	git log
	git reflog
版本回退
	git reset --hard HEAD^ 回退到上一个版本
	git reset --hard 3628164  版本号前几位
撤销修改
	git checkout -- readme.txt
删除文件
	git rm test.txt

添加远程库
	要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
	关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
	此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；
	
从远程库克隆
	git clone git@github.com:michaelliao/gitskills.git 
