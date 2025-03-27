## 正文

### 01.简要介绍

#### 起源

- 采用python语言编写的开源web**框架**
- 重量级的python Web框架，配备了常用的大部分组件

#### 组件

- 基本配置文件/路由系统
- 模型层（M）/模板层（T）/视图层（V）
- Cookies 和 Session
- 分页以及发邮件
- Admin后台管理

#### 用途

- 网站/微信公众号/小程序后端开发（HTTP请求）
- 人工智能平台融合（转发请求至人工智能服务器）

### 02.第一节 请求和响应

当你初次创建你的Django项目后，系统会给你生成一下文件夹

```
项目名称/
    manage.py
    自定义名称/
    __init__.py
    settings.py
    urls.py
    asgi.py
    wsgi.py
```

- manage.py:一个让你用各种方式管理Django项目的命令行工具。
- 自定义名称/:一个目录，它是你实际上的python包，他的名称是你需要用来导入其中任何内容的python包名称。
- /__init__.py：一个空文件，告诉 Python 这个目录应该被认为是一个 Python 包。
- /settings.py：Django 项目的配置文件。
- /urls.py：Django 项目的 URL 声明，就像你网站的“目录”。
- /asgi.py：作为你的项目的运行在 ASGI 兼容的 Web 服务器上的入口。
- /wsgi.py：作为你的项目的运行在 WSGI 兼容的Web服务器上的入口。

#### 创建一个应用

Django中，实际干活的是各种应用。这些应用都是一个python包，遵循着相同的规定。

使用命令行

```shell
python manage.py startapp 应用名
```

来创建一个应用。

你会发现它有着和你的项目主包相同的结构。

为了启用这个应用，你需要做：

1. 在你的应用文件夹中新建`urls.py`文件，用来管理该包的链接。
2. 然后，进入`views.py`文件，用来管理网络视图。

*具体步骤可以参考<a src='https://docs.djangoproject.com/zh-hans/5.1/intro/tutorial01/'>Django官方文档</a>*

接下来我们开始使用数据库。

#### 数据库的使用

