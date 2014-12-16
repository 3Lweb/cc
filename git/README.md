# git备忘录

1. gitconfig文件： 命令简写
* 位置：/Users/username
* gitignore文件： 全局文件
* .git/config 文件可查看仓库位置信息
* 单独设置一个仓库的email:当前仓库内 git config user.email "ccking@foxmail.com"  
  或者在bash_profile文件中加入：  
  `alias github='git config user.email "ccking@foxmail.com"'`  
  最后编译bash文件  source .bash_profile
* cat .git/logs/HEAD  查看仓库的log信息
* git fetch 和 git pull   
  * 都是从远程分支获取最新的版本到本地
  * git fetch 不会自动 merge
  
  		git fetch origin master
  		git log -p master..origin/master
  		git merge origin/master
  	从远程origin的master分支下载最新版本到 origin/master 分支  
  	比较本地master分支和远程master分支的区别  
  	合并代码  
  	上述过程的描述:
  	
  		git fetch origin master:tmp
  		git diff tmp
  		git merge tmp
  * git pull 也是从远程master分支获取最新版本但是会自动merge
  * git fetch 相对安全点
  	
  