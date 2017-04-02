# 学习Django框架记录：

**2017-4-1**：

> * 教材：[自强学堂Django教程](http://www.ziqiangxuetang.com/django/django-tutorial.html "自强学堂_Django教程")
> * Python版本：2.7
> * Django版本：1.8.16

尝试着在VMware里的CentOS 7 中使用virtualenv、virtualenvwrapper搭建了Django的虚拟环境。   
但无论如何在本机上都无法访问到虚拟中的搭建的网站。  
后来又尝试在阿里的ECS上搭建，开始也是访问不到。  
后来看到自强的相应文章评论中反应需要修改../settings.py中的ALLOWED_HOSTS字段为：  
        `ALLOWED_HOSTS = ['*']`  
晚上使用修改后使用手机访问正常嘞！！！(仿佛又打开一扇异世界的大门)  




