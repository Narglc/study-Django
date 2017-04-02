# Django框架学习记录：

**2017-4-1**：

> * 教材：[自强学堂Django教程](http://www.ziqiangxuetang.com/django/django-tutorial.html "自强学堂_Django教程")
> * Python版本：2.7
> * Django版本：1.8.16

尝试着在VMware里的CentOS 7 中使用**virtualenv**、**virtualenvwrapper**搭建了Django的虚拟环境。   
安装**virtualenv**、**virtualenvwrapper**: 
`sudo pip install virtualenv virtualenvwrapper`
修改根目录下的**.zshrc**文件：
```shell
export WORKON_HOME=$HOME/.virtualenvs
export PROJECT_HOME=$HOME/workspace
source /usr/local/bin/virtualenvwrapper.sh   	#此处根据系统可能会有所不同，可使用**locate virtualenvwrapper.sh**查找相应文件的路径.
```
使之生效： 
`source ~/.zshrc`

与虚拟环境有关的几个重要Command： 
`mkvirtualenv nar_vir_space_name`  		创建某运行环境 	
`workon`								查看本机的所有运行环境 
`workon nar_vir_space_name`				进入某运行环境	
`deactivate`							离开该运行环境	

但无论如何在本机上都无法访问到虚拟中的搭建的网站。  
后来又尝试在阿里的ECS上搭建，开始也是访问不到。  
后来看到自强的相应文章评论中反应需要修改../settings.py中的ALLOWED_HOSTS字段为：  
        `ALLOWED_HOSTS = ['*']`  
晚上修改后使用手机访问正常嘞！！！(仿佛又打开一扇异世界的大门)  
