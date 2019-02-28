# myDjangosite
学习通过Django建站

## 文件作用

- 最外层的 myDjangosite/ 根目录只是你项目的容器， Django 不关心它的名字，你可以将它重命名为任何你喜欢的名字。
- manage.py: 一个让你用各种方式管理 Django 项目的命令行工具。你可以阅读 django-admin and manage.py 获取所有 manage.py 的细节。
- 里面一层的 djangosite/ 目录包含你的项目，它是一个纯 Python 包。它的名字就是当你引用它内部任何东西时需要用到的 Python 包名。 (比如 djangosite.urls).
- djangosite/__init__.py：一个空文件，告诉 Python 这个目录应该被认为是一个 Python 包。如果你是 Python 初学者，阅读官方文档中的 更多关于包的知识。
- djangosite/settings.py：Django 项目的配置文件。如果你想知道这个文件是如何工作的，请查看 Django settings 了解细节。
- djangosite/urls.py：Django 项目的 URL 声明，就像你网站的“目录”。阅读 URL调度器 文档来获取更多关于 URL 的内容。
- djangosite/wsgi.py：作为你的项目的运行在 WSGI 兼容的Web服务器上的入口。阅读 如何使用 WSGI 进行部署 了解更多细节。

## 启动服务器

在根目录输入以下代码

$ python manage.py runserver 端口(默认8000)

## 创建应用

在与manage.py同级的目录下输入

$ python manage.py startapp 应用名

回创建如下文件目录

- 应用名
	- __init__.py
	- admin.py
	- apps.py
	- migrations/
		- __init__.py
	- models.py
	- tests.py
	- views.py


## 数据库配置

- 编辑 models.py 文件，改变模型。
- 运行 python manage.py makemigrations 为模型的改变生成迁移文件。
- 运行 python manage.py migrate 来应用数据库迁移。

