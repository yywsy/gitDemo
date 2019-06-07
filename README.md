# gitDemo


-  create a new repository on the command line

		echo "# gitDemo" >> README.md
		git init
		git add README.md
		git commit -m "first commit"
		git remote add origin https://github.com/yywsy/gitDemo.git
		git push -u origin master

-  push an existing repository from the command line

		git remote add origin https://github.com/yywsy/gitDemo.git
		git push -u origin master

-  import code from another repository

	You can initialize this repository with code from a Subversion, Mercurial, or TFS project.


由于Unix 和 Windows 下对换行符的解释不同，在win下用vim新建编辑的文件在提交到版本库是会出错，提示为

          fatal: LF would be replaced by CRLF in README.md
 

因为win下文件回车换行是以CRLF结尾，而用VIM编辑器新建的文件是以LF结尾，导致出现了此问题。

 

解决方法：找到win项目的.git目录,修改config文件，在[core]配置项添加下面一句话，就ok了。

		autocrlf = false  