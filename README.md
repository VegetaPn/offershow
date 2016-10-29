# 校招薪水 #

----------

###应用场景:一个offer数据爆料和展示的内部交流平台###
###想法初衷:就是简单提供一个校招签约之前可以匿名的offer数据交流以及分享平台，不在依赖于网上的比如看准网，知乎查找之类的，纯靠校友，页面简单粗暴，直接打分，按照可信度来对比区分各个待遇，以便签约时候的谈薪水了解等，至于侵权方面，平台仅供内部交流，希望大家理解###
###使用框架：前端jquery mobile+后端django###

----------

###技术速成方案：###
####jqm基础学习：半天时间，找个模板看看，简易的样式基本都比较好学，学习网址：[点此访问](http://www.runoob.com/jquerymobile/jquerymobile-tutorial.html "学习网址")
####django基础学习：这个看能力了，快的一两天，慢的一个星期左右，python的web框架，比较容易上手，我在这个项目中也就用了基础的东西，基本是下面这个教程的基础篇吧，学习网址：[点此访问](http://www.ziqiangxuetang.com/django/django-tutorial.html "学习网址")
####数据库基本学习：这里用了一下mysql，django默认是sqlite3，输入导入导出不方便，所以改成了mysql

######补充说明：整个项目只是实现了基本业务，前端不是很好看，并没有考虑太多反爬虫，高并发之类的问题，还希望感兴趣的朋友能够有兴趣交流一下，谢谢，有兴趣的朋友欢迎提供更新版本哈。

----------

###环境部署：###
#####前期准备:ubuntu服务器+mysql安装+apache服务器
#####步骤1：
    sudo easy-install pip
#####步骤2（初学者过滤掉这一步，以后也没体现）：
    sudo pip install virtualenv
    virtualenv website
    source website/bin/activate
#####步骤3：下载django版本，我这用的是1.7.3版本
    pip install Django==1.7.3
#####步骤4：下载了源码的可以略过这一步，创建django项目offershow以及创建工程salary
    django-admin.py startproject offershow
    cd offershow
    python manage.py startapp salary
#####步骤5：在源码的offershow路径下启动应用，我是在腾讯云上的，暂时没有部署apache或者ngnix，所以直接开启服务自己测试就好
    python manage.py makemigrations 
    python manage.py migrate
    python manage.py runserver 0.0.0.0:8000（这里是默认外网可以从8000端口访问）
#####步骤6：服务部署上线，赶得匆忙没有经过太多的复杂部署，直接采用了django框架自带的服务器，利用screen保持服务不断的手段（有点low），之后再去学习一下部署了，最近也忙着去找工作。这一步，建议大家自己测试的时候不用到这一步，不然还得去学习一下screen命令哈。
#####步骤7：使用自己服务器部署的时候，需要修改一下setting文件的数据库密码和名字，其中mysqldb安装会略麻烦，我晚会贴上解决方案。
#####备注：以上是一些初级的学习以及简单的部署，安全性和并发都依赖于框架，所以做的不是很好，大神请勿喷，也请不要乱去爬取数据，需要的话可以直接问我要，毕竟服务器和流量都是自费的，至于有什么别的问题或者比较厉害的大神愿意主动教我的，可以直接issue或者邮件反馈交流哈，abc_123@zju.edu.cn


----------

###最后，项目的初衷是为了交流互助，薪水可能大家都了解了，为了响应最近朋友们对于代码和数据的需求，这小项目的代码都开源了，数据大概一个月以后在公布给大家，相对来说技术犹如界面和使用一样简单粗糙，适合初学者，但是意义还是有的，也很开心能够帮助到一些朋友。

----------
###前端朋友的福利：###
#####restful api接口文档下载地址：[点我下载](http://pan.baidu.com/s/1o8Ep8wU "网盘下载地址") 提取密码（9uf4）
#####觉得页面丑陋，想自己写写练手的欢迎大家来参与，数据可以自行创建测试，如果可以的话，优秀的，我可以更新一下代码，展示你们的优秀版本，谢谢大家参与。







