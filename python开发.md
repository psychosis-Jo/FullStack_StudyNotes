# Python开发

## Django

### Python 的 Web 框架对比介绍

1. Django：
   - 特点：全功能、高度集成的框架，适用于构建复杂的 Web 应用程序。
   - 优点：自带ORM、表单处理、用户认证等功能模块，易于上手和学习，拥有强大的社区支持和文档资料。
   - 缺点：相对较重量级，对于简单的项目可能会显得过于复杂。
   - **全功能性**：Django是一个全功能的Web框架，提供了一整套工具和库来帮助开发者构建复杂的Web应用程序。它包含了ORM（对象关系映射器）、表单处理、认证系统、管理后台等多个组件，可用于快速搭建各种类型的应用。
   - **强大的ORM**：Django的ORM是它最著名的特点之一。它允许开发者使用Python代码来操作数据库，而无需直接编写SQL语句。ORM提供了高级的查询语法、模型关系定义和自动数据迁移等功能，极大地简化了与数据库的交互。
   - **admin站点**：Django内置了一个功能完备的管理后台（admin），可以轻松实现对数据模型的增删改查操作。通过简单的配置，开发者即可创建一个可定制的管理界面，方便非技术人员管理网站内容。
   - **路由和视图**：Django提供了强大而灵活的URL路由系统，通过简单的配置可以将URL映射到相应的视图函数或类。视图负责处理请求并返回响应，可以根据需要选择使用函数视图或基于类的视图。
   - 插件丰富：Django生态系统非常丰富，有许多第三方插件可用于扩展框架的功能。这些插件涵盖了各种需求，包括文件上传、缓存、认证、API开发等。
   - **MTV架构**：Django采用了MTV（Model-Template-View）的架构模式。Model负责处理数据相关的事务，Template用于呈现最终的HTML页面，而View则负责处理请求、调用适当的Model和Template，并生成响应。
2. Flask：
   - 特点：轻量级微框架，注重灵活性和可扩展性。
   - 优点：简洁明快，提供核心功能，可以根据需要选择插件和扩展。易于学习和使用，对定制化需求友好。
   - 缺点：功能相对简单，需要手动选择和集成其他库以完成一些高级功能。
3. Tornado：一个异步的、高性能的 Web 框架，适用于构建实时应用和高并发的 Web 服务。
   - **异步性能**：Tornado 是一个基于异步 I/O 的 Web 框架，它使用非阻塞的事件循环和协程机制来处理请求。这使得 Tornado 在高并发环境中表现出色，并具有出色的性能。
   - **高度可扩展**：Tornado 是为构建可伸缩的网络应用程序而设计的。它通过使用非阻塞 I/O 和单线程事件循环来实现高效的扩展，可以处理成千上万个并发连接。
   - **WebSocket 支持**：Tornado 是少数几个原生支持 WebSocket 的 Python 框架之一。它提供了内置的 WebSocket 功能，方便构建实时应用程序，如聊天应用、实时通知等。
   - **路由和中间件**：Tornado 提供了灵活的路由和中间件机制，可以帮助开发者轻松地定义 URL 路由规则并添加中间件来处理请求和响应。
   - **与Django 和 Flask 对比**：相较于 Django 和 Flask，Tornado 更注重异步处理和高性能。Django 是一个功能强大的全功能框架，适用于构建复杂的 Web 应用程序，而 Flask 更注重简洁性和灵活性。Tornado 则专注于高性能和可伸缩性，适用于需要处理大量并发请求和实时应用程序的场景。
4. FastAPI：一个现代化的框架，基于 Starlette，使用类型注解实现高性能的 API 构建，并支持自动生成交互式文档。
   - 高性能：FastAPI 基于异步编程模型，利用 Python 3.7+ 的新特性，实现了卓越的性能表现。
   - 快速开发：FastAPI 提供了自动的 API 文档生成、请求参数验证、异常处理等功能，可以大大加速 Web 应用程序的开发过程。
   - 类型注解：借助 Python 的类型注解功能，FastAPI 可以自动生成详细的 API 文档，并提供代码编辑器的自动补全和类型检查。
   - 标准兼容：FastAPI 遵循标准的 HTTP/JSON 规范，可以与现有的工具和库很好地集成，如 Pydantic、SQLAlchemy 等。
   - 异步支持：FastAPI 基于异步编程模型，可以轻松处理大量并发请求，提供出色的性能和可伸缩性。
5. Pyramid：
   - 特点：提供了灵活性和可扩展性，适用于中小型 Web 应用程序。
   - 优点：兼具了 Flask 和 Django 的优点，既可以用作简单的微框架，又能够构建复杂的应用程序。
   - 缺点：相对于 Django 来说，文档和教程资源相对较少。
6. Bottle：
   - 特点：极简的微框架，适用于小型项目和快速原型开发。
   - 优点：非常轻量级，代码量小，学习成本低。无需依赖其他库即可运行。
   - 缺点：功能相对简单，缺少一些重量级框架的高级功能。
7. CherryPy：一个简单而稳定的框架，提供了灵活的插件系统和强大的请求和响应处理能力。
8. web2py：一个全功能的框架，拥有自带的数据库抽象层、表单处理、安全性等功能模块。
9. Falcon：一个轻量级的框架，专注于构建快速的 RESTful API，具有出色的性能表现。
10. Sanic：一个异步 Web 框架，使用类似 Flask 的API，以及高性能和低延迟为目标。

### WSGI服务器

WSGI（Web Server Gateway Interface）服务器是一种用于运行 Python Web 应用程序的服务器。它遵循 WSGI 规范，使得不同的 Web 框架和服务器能够以一种统一的方式进行交互。
使用生产级的 WSGI 服务器可以提高您的应用程序的性能和可靠性，并支持更高的并发请求处理。下面是一些常用的生产级 WSGI 服务器：

1. **Gunicorn**：Gunicorn（Green Unicorn）是一个广受欢迎的基于 Python 的 UNIX HTTP 服务器。它兼容 WSGI 规范，易于配置和部署。
2. **uWSGI**：uWSGI 是另一个流行的基于 WSGI 的服务器，支持多种协议（HTTP、WebSocket 等）和多种部署模式（标准、快速CGI、WSGI、异步等）。
3. **mod_wsgi**：如果您使用 Apache Web 服务器，可以考虑使用 mod_wsgi 模块来托管 Python Web 应用程序。它将 Python 解释器嵌入到 Apache 进程中，以实现更高效的请求处理。
4. **Waitress**：Waitress 是一个纯 Python 实现的 WSGI 服务器，适用于小型应用程序或开发环境。
要使用这些生产级 WSGI 服务器，通常需要按照特定的安装和配置步骤进行设置。一般的步骤包括安装服务器软件、配置应用程序和启动服务器。具体的步骤可以在每个服务器的文档或官方网站上找到。
需要注意的是，生产环境中的部署通常比开发环境更复杂，涉及到安全性、性能优化、负载均衡等方面的考虑。建议在进行生产部署之前详细阅读相关服务器的文档，并遵循最佳实践。

### 使用

安装框架：`pip install django`
和express一样在安装框架的同时，会自动安装一个框架生成工具`django-admin.exe`，默认与`python.exe`同目录
安装完框架后，可以在项目目录下，执行命令`django-admin.exe startproject <项目名称>`
初始化后的目录结构

```powershell
├─.idea
│  │  .gitignore
│  │  07_django.iml
│  │  misc.xml
│  │  modules.xml
│  │  workspace.xml
│  │
│  └─inspectionProfiles
│          profiles_settings.xml
│          Project_Default.xml
│
└─first_ac
    │  manage.py  # 负责项目的管理，启动项目、创建app、数据管理等
    │
    └─first_ac
            asgi.py  # 接收异步网络请求
            wsgi.py  # 接收同步网络请求
            settings.py  # 项目的配置文件
            urls.py  # URL和函数的对应关系，路由
            __init__.py
```

### APP功能模块

- 层级关系：
  - 项目
    - app-用户管理（表结构、函数、HTML模板、CSS）
    - app-订单管理（表结构、函数、HTML模板、CSS）
    - app-后台管理（表结构、函数、HTML模板、CSS）
    - app-网站（表结构、函数、HTML模板、CSS）
    - app-API（表结构、函数、HTML模板、CSS）
    - ...
- 创建app，在项目目录下执行：`python manage.py startapp app01`
- app目录

   ```powershell
   ├─app01
   │  │  admin.py  # django默认提供的admin后台管理
   │  │  apps.py  # app启动类：配置
   │  │  models.py  # 操作数据库
   │  │  tests.py  # 单元测试
   │  │  views.py  # 函数定义文件，urls.py调用的函数来源
   │  │  __init__.py
   │  └─migrations
   │     __init__.py
   ```

- 注册app：
  - 在 `settings.py` 的 `INSTALLED_APPS` 中增加值，`'<app名>.apps.<AppConfig类名>'`，表示该应用程序的配置类位于`/app名/apps.py`里，类名为`AppConfig类名`。
  - 也可以直接使用`<app名>`进行注册，默认为`<app名>.apps.AppConfig`，若apps.py中的类名不为`AppConfig`则还需更改类名及对应的调用代码。

   ```python
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'app01.apps.App01Config',
      'usermanagement.apps.UsermanagementConfig',
   ]
   ```

- 编写URL和视图函数的对应关系 `urls.py`

   ```python
   from django.contrib import admin
   from django.urls import path
   from app01 import views

   urlpatterns = [
      # path('admin/', admin.site.urls),
      path('index/', views.index),
   ]
   ```

- 编写视图函数 `views.py`

   ```python
   from django.shortcuts import render, HttpResponse

   def index(request):
      return HttpResponse("欢迎使用")
   ```

- 启动
  - 命令行启动：`python manage.py runserver <port>`，如果不加端口号，默认监听8000端口
- 页面渲染
  - 在`views.py`中使用`return render(request, "user_list.html")`，渲染页面，默认到app的templates目录下检索文件。
  - 如果`settings.py`的`TEMPLATES`中有配置，如：`'DIRS': [os.path.join(BASE_DIR, 'templates'),],`，则到配置的路径下去检索该html文件；如果检索不到再按照app的注册顺序，逐个检索其下的templates目录。
- 静态文件加载
  - 路径配置(settings.py)

      ```python
      STATICFILES_DIRS = (
         os.path.join(BASE_DIR, 'static'),
      )
      ```

  - 查找时默认去已注册的每个app的static下去找，注册了多个app时，如果在先注册的static下找到了对应的静态资源，就不会再去其他app下查找了。
  - 支持使用django的模板语法，通过在`html`标签下`{% load static %}`来加载css、js、img等静态文件。
  - 加载时也要使用模板语法，在html页面头部增加 `{% load static %}`，引用静态文件时如 `<link rel="stylesheet" href="{% static 'plugins/bootstrap-5.3.0/css/bootstrap.css' %}">`
- 请求和响应(views.py)

   ```python
   def login(request):
      # 1. 获取请求方式 GET
      print(request.method)
      # 2. 获取URL中传递的参数 /login/?n1=123&n2=456&n3=789
      print(request.GET.get('n1'))
      print(request.GET)

      # 3. 数据放在请求体中传递过来
      print(request.POST)
      # 4. 返回文本字符串
      # return HttpResponse("Hello World")
      # 5. 返回重定向
      # return redirect("http://www.baidu.com")
      # 6. 返回HTML页面 +数据渲染
      return render(request, "login.html")
   ```

   ```python
   def login(req):
      # 浏览器上输入地址->跳转
      if req.method == "GET":
         return render(req, "login.html")
      # 否则就是POST方式提交
      user = req.POST.get("username")
      pwd = req.POST.get("password")
      if user == "root" and pwd = "123":
         # 登录成功，跳转到官网
         return redirect("https://www.baidu.com")
      else:
         # 登录失败，依旧显示登录页面
         return render(req, "login.html", {"error": "用户名或密码错误"})
   ```

   ```html
   <form action="/login/" method="post">
      {% csrf_token %}
      <input type="text" name="username" placeholder="用户名" />
      <input type="password" name="password" placeholder="密码" />
      <input type="submit" value="提交" />
      <span style="color: red">{{ error }}</span>
   </form>
   ```

### orm数据处理

#### 处理默认支持的嵌入式数据库SQLite数据

1. 在Django中，默认使用的是SQLite数据库。要查看数据库中的数据，可以按照以下步骤进行操作：
   1. **运行数据库迁移命令**：在项目的根目录下运行以下命令来进行数据库迁移：`python manage.py migrate`
   2. **启动Django开发服务器**：运行以下命令以启动Django开发服务器：`python manage.py runserver`
   3. **访问管理后台**：在浏览器中输入 `http://localhost:8000/admin/`，进入Django的管理后台界面。
   4. **创建超级用户**：如果还没有创建超级用户，在终端中运行以下命令来创建一个新的超级用户：`python manage.py createsuperuser`
   5. **登录管理后台**：使用在上一步中创建的超级用户凭据登录管理后台。
   6. **查看数据库内容**：在管理后台中，可以访问和管理数据库中的模型数据。通过浏览模型列表、编辑和添加模型对象等功能，可以查看和操作数据库中的数据。
2. 要打开和查看SQLite数据库文件中的表结构和数据，有多种工具可供选择，以下是其中一些常用的工具：
   1. **SQLite命令行工具**: 它是SQLite自带的官方命令行工具，可以直接在终端中运行SQLite命令来操作数据库文件。
   2. **DBeaver**: 这是一个跨平台的数据库管理工具，支持多种数据库包括SQLite。您可以使用DBeaver连接到SQLite数据库文件，并通过图形界面查看和管理表结构以及数据。
   3. **SQLiteStudio**: 这是一个专门针对SQLite数据库的开源图形化管理工具。它提供了一个直观的界面，可以轻松地查看和编辑表结构及数据。
3. Django项目目录下的db.sqlite3文件就是SQLite数据库文件。默认情况下，Django在项目根目录中创建名为db.sqlite3的SQLite数据库文件。可以使用SQLite的相关工具之一来打开和查看该文件中的表结构和数据。
4. 使用DBeaver打开SQLite数据库文件（例如Django项目中的db.sqlite3）：
   1. 下载和安装DBeaver：您可以从DBeaver的官方网站（`https://dbeaver.io/`）下载适用于您操作系统的安装程序，并按照提示进行安装。
   2. 启动DBeaver：安装完成后，启动DBeaver应用程序。
   3. 创建新连接：在DBeaver的主界面中，点击"创建新连接"或 "新建连接"按钮。这将打开连接配置向导。
   4. 选择数据库类型：在连接配置向导中，选择"SQLite"作为数据库类型，并点击"下一步"。
   5. 配置连接设置：在连接配置向导的下一个页面上，填写以下信息：
      - 主机: 填写SQLite数据库文件的完整路径。例如，如果数据库文件位于Django项目目录下的`db.sqlite3`，则填写类似于`/path/to/your/django/project/db.sqlite3`的路径。
      - 用户名和密码: 对于SQLite数据库，这些字段通常为空。
      - 其他可选设置: 您可以根据需要设置一些其他连接选项，如字符集、超时等。
      填写完毕后，点击"测试连接"按钮来验证连接是否成功，然后点击"完成"按钮。
   6. 查看数据库：在DBeaver的主界面中，您会看到刚刚创建的SQLite连接。展开该连接，您将看到数据库文件中的表结构。单击表名，即可查看该表中的数据。
5. 当使用Django的默认SQLite数据库创建超级用户时，该用户的信息将存储在SQLite数据库中的`auth_user`表中。
   Django通过内置的认证系统（`django.contrib.auth`）来管理用户身份验证和权限。`auth_user`表是该认证系统的一部分，用于存储用户信息，包括用户名、密码（经过哈希处理）、电子邮件等。
   当在Django项目中运行`createsuperuser`命令创建超级用户时，Django会提示输入用户名和密码。然后，它在`auth_user`表中创建一个对应的用户记录，其中包含了提供的用户名和密码的哈希值。该表还包含其他与用户相关的字段，例如电子邮件、姓名等。

### 编辑页面

- 点击编辑，跳转到编辑页面，并将编辑行的ID携带过去
- 编辑页面，默认数据应当根据ID获取并显示在该页面
- 提交：
  - 错误提示
  - 数据校验
  - 在数据库更新

#### 访问控制：cookie和session

当浏览器与服务器进行通信时，Cookie和Session是常用的机制来在客户端和服务器之间传递数据。

1. Cookie（HTTP Cookie）：
   - Cookie是服务器发送给浏览器并存储在客户端的小段数据。
   - 通过Cookie，服务器可以在后续请求中识别客户端，并提供个性化的功能。
   - 客户端的每个请求都会自动携带相关的Cookie，以便服务器使用。
   - Cookie可以包含各种信息，如用户身份、偏好设置等。
   - Cookie是存储在浏览器中的文本文件，可以通过JavaScript读取和修改。
2. Session（会话）：
   - Session是一种服务器端存储的数据结构，用于存储与特定用户相关的信息。
   - 每个会话都与唯一的会话ID相关联，这个ID通常存储在Cookie中。
   - 会话数据存储在服务器上，而不是在客户端。
   - 通过会话，服务器可以在多个请求之间保持状态，并跟踪用户的登录状态、购物车内容等。
   - 通常，会话数据保存在服务器的内存、数据库或缓存中。

Cookie和Session的关系：

- 当用户首次访问网站时，服务器会生成一个唯一的会话ID，并将其存储在Cookie中发送给浏览器。同时，在服务器端创建一个对应的会话，并将会话ID与会话数据关联起来存储在内存或数据库中。
- 浏览器在后续的请求中会自动携带Cookie，包括会话ID，服务器根据会话ID识别用户，并访问相应的会话数据。
- 通过Cookie中的会话ID，服务器能够获取与特定用户相关的数据，实现状态保持和个性化功能。

总结：
Cookie是存储在客户端的小段数据，用于识别用户和存储个人偏好等信息。而Session是存储在服务器端的会话数据，用于跟踪用户状态和保持数据的一致性。Cookie和Session通常配合使用，通过会话ID将服务器端的数据与客户端关联起来，提供更丰富的服务和用户体验。

```python
"""views.py"""
def login(req):
    if req.method == "GET":
        return render(req, "login.html")
    user = req.POST.get("username")
    pwd = req.POST.get("password")
    user_obj = models.UserInfo.objects.filter(name=user,password=pwd).first()
    if user_obj:
        print("当前登录用户：", user_obj.name)
        # 生成随机字符串返回用户浏览器，并将数据写入session
        req.session["user_info"] = {"id": user_obj.id, "user": user_obj.name}
        return redirect("/depart/list")
    else:
        return render(req, "login.html", {"error": "用户名或密码错误！"})

def depart_list(req):
    """部门列表"""
    # 未经登录不予访问，登录时设置的什么session，校验时就校验什么session
    user_info = req.session.get("user_info")
    if not user_info:
        return redirect('/login')
    # 去数据库中获取所有的部门数据
    queryset = models.Department.objects.all()
    return render(req, "depart_list.html", {'queryset':queryset})
```

通过在`login`中设置session，并在depart_list中校验session来实现没有登录就无法访问`/depart/list`的效果。

#### 访问控制：token

当谈到身份验证和访问控制时，Token是一种常用的机制。Token是一种代表用户身份、权限或访问凭证的字符串，它将用户的身份信息存储在客户端而不是服务器端。

1. Token的生成和使用：
   - 用户在进行身份验证后，服务器会生成一个Token，并将其返回给客户端。
   - 客户端在后续的请求中，将Token作为身份凭证携带到服务器。
   - 服务器通过验证Token的有效性来识别和认证用户，而不需要在服务器端存储会话数据。
   - Token通常是加密的，防止被篡改或伪造。
2. Token的特点：
   - 无状态：服务器不需要存储Token相关的会话数据，因为Token本身包含了所有必要的信息。
   - 可拓展性：Token可以存储更多的用户信息，如权限、角色等，从而实现更复杂的访问控制。
   - 跨平台：Token可以在不同的系统和应用之间使用，方便实现单点登录和集成外部服务。
   - 安全性：使用加密算法和签名机制，确保Token的安全性和真实性。
3. Token与Session的区别：
   - 存储位置：Token存储在客户端，而Session存储在服务器端。
   - 状态保持：Session需要在服务器端维护会话状态，而Token是无状态的，减轻了服务器的负担。
   - 扩展性：Token可以在不同系统之间共享，更适合跨平台和分布式环境。
   - 生命周期：Session通常具有较短的生命周期，而Token可以设置较长的有效期，并支持自动刷新。

总结：
Token是一种用于身份验证和访问控制的字符串，将用户的身份信息存储在客户端而不是服务器端。相比于传统的基于会话的认证机制，Token具有无状态、可拓展和跨平台等特点，使其在分布式系统和API认证中得到广泛应用。同时，Token的安全性也非常重要，可以使用加密算法和签名机制来保证Token的完整性和真实性。

#### 中间件

在Django框架中，中间件是一种用于在请求和响应处理过程中插入自定义逻辑的组件。注册一个中间件并将其添加到配置文件中后，它会在每个请求到达和响应离开视图之前被执行，即使没有在`views.py`中直接调用。Django的中间件是一个可插拔的组件，位于Django请求/响应处理过程的不同阶段，用于对请求和响应进行处理、修改或拦截。它们提供了一个灵活的机制，可以在处理请求之前或之后执行自定义的代码逻辑。
在Django的请求/响应处理过程中，每个中间件组件都有机会干预并对请求或响应进行修改。中间件的运行顺序由`settings.py`中`MIDDLEWARE`设置的顺序决定，每个中间件都可以选择中止请求处理或将控制权传递给下一个中间件。

中间件在请求处理过程中的三个主要阶段：

1. 请求处理前的中间件：
   - 在接收到请求后，在视图函数或Django内置视图之前运行。
     - 当一个请求到达时，Django会按照中间件的顺序依次执行中间件的 `process_request` 方法。
     - `process_request` 方法是中间件的一个可选方法，在请求进入视图之前被调用。
     - 如果请求涉及多个中间件，它们的 `process_request` 方法将按注册顺序被连续调用。
     - 当在 `process_request` 方法中无返回值或返回None时，代码会继续向下执行。
     - 当在 `process_request` 方法中有返回值(return)时，代码就直接带着返回值返回浏览器，而不会继续向下执行。
   - 可以对请求进行修改、验证或过滤，并根据需要进行重定向或返回响应。
   - 一些常见的用例包括身份验证、访问控制、跨域资源共享 (CORS) 等。
2. 视图函数（或Django内置视图）：
   - 请求通过所有的中间件后，Django将请求发送给与URL匹配的视图函数或类。
   - 在视图函数或类中执行具体的业务逻辑。
   - 中间件不会直接调用视图函数或类，而是在请求到达和离开视图之前执行自己的逻辑。
3. 响应处理后的中间件：
   - 在视图函数执行完毕并返回响应后运行。
     - 当视图函数或类返回一个响应后，Django会按照中间件的相反顺序依次执行中间件的 `process_response` 方法。
     - `process_response` 方法是中间件的可选方法，用于在响应返回给客户端之前对响应进行处理。
     - 同样，如果请求经过多个中间件，它们的 `process_response` 方法将按注册顺序被逆序调用。
   - 可以对响应进行修改或添加额外的信息，例如HTTP头部、Cookies等。
   - 一些常见的用例包括跨域资源共享 (CORS) 头部添加、缓存控制等。

中间件可以被应用于整个Django项目，也可以仅应用于特定的URL模式或视图函数。可以通过在Django项目的配置文件中的`MIDDLEWARE`设置中指定中间件的路径来启用和配置中间件。
注册进配置文件的中间件会在每个请求到达和响应离开视图之前自动执行。通过中间件机制，可以在请求和响应的不同阶段插入自定义逻辑来实现公共功能，如身份验证、会话管理、CSRF保护、请求拦截、日志记录、验证和响应处理等。即使在`views.py`中没有直接调用中间件，它仍然能够生效，因为Django框架在处理请求和响应的过程中会自动触发中间件的执行。

##### Django中间件的执行过程

Django 中间件是一种机制，用于在处理请求和响应的过程中插入自定义的处理逻辑。它可以对请求进行预处理、对响应进行后处理，并且可以在请求处理的不同阶段进行操作。下面是 Django 中间件的执行过程：

1. 请求到达服务器后，Django 根据 URL 匹配将其路由到相应的视图函数或类视图。
2. 在请求到达视图函数之前，中间件首先进行预处理操作。中间件按照定义的顺序依次执行，每个中间件都可以选择在请求到达视图函数之前或之后执行特定的操作。这些操作包括身份验证、请求日志记录、请求数据的处理等。如果任何一个中间件返回了响应，则请求将直接返回该响应，不再执行后续的中间件和视图函数。
3. 如果所有的中间件都执行完毕，请求将被传递给视图函数进行处理。视图函数根据业务逻辑进行处理，并生成响应。
4. 在视图函数处理完毕后，中间件开始进行后处理操作。中间件按照相反的顺序依次执行，每个中间件都可以选择在视图函数处理完毕之后进行特定的操作。这些操作包括响应日志记录、响应数据的加工处理等。同样，如果任何一个中间件返回了响应，则请求将直接返回该响应，不再执行后续的中间件的后处理操作。
5. 如果所有的中间件都执行完毕，响应将返回给客户端。

总结起来，Django 中间件的执行过程可以分为预处理阶段和后处理阶段。在预处理阶段，请求经过中间件的处理；在后处理阶段，响应经过中间件的处理。中间件可以自定义处理逻辑，对请求和响应进行干预、记录日志、修改数据等操作。

##### Django中间件各方法介绍

在 Django 中，中间件是一个 Python 类，可以定义以下常用的方法：

1. `__init__(self, get_response)`：初始化方法，接收一个参数 `get_response`，表示后续中间件或视图函数的调用链。在 Django 启动时实例化中间件类时，会调用该方法。
2. `process_request(self, request)`：预处理请求的方法。在请求到达视图函数之前执行，用于进行请求的预处理操作，例如身份验证、请求数据的处理等。可以选择在这里返回响应，以终止后续的请求处理过程。
3. `process_view(self, request, view_func, view_args, view_kwargs)`：在视图函数被调用前执行。用于对视图函数进行处理或进行一些附加操作。
4. `process_exception(self, request, exception)`：处理视图函数抛出异常的方法。当视图函数发生异常时，将调用该方法。可以在这里处理异常并返回响应，以替代原始异常信息的返回。
5. `process_template_response(self, request, response)`：在视图函数返回的响应经过模板渲染后执行。用于对渲染后的响应进行处理。
6. `process_response(self, request, response)`：在视图函数返回的响应发送给客户端前执行。用于对响应进行后处理操作，例如添加 HTTP 头部、修改响应内容等。
7. `__call__(self, request)`：调用中间件实例的方法。在中间件链中的每个中间件被调用时都会执行该方法。

这些方法各自起到不同的作用，可以在相应的环节对请求和响应进行处理、修改和拦截。中间件方法的执行顺序如下：

1. `process_request` 方法按照中间件定义的顺序依次执行，用于预处理请求。
2. 中间件链中符合 URL 匹配的视图函数被调用。
3. `process_view` 方法按照中间件定义的顺序依次执行，用于对视图函数进行处理。
4. 视图函数被调用，处理请求并生成响应。
5. `process_exception` 方法按照中间件定义的顺序逆序执行，处理视图函数抛出的异常。
6. `process_template_response` 方法按照中间件定义的顺序依次执行，对渲染后的响应进行处理。
7. `process_response` 方法按照中间件定义的顺序逆序执行，对响应进行后处理操作。
8. 响应返回给客户端。

这些方法共同构成了中间件的完整执行流程，通过这些方法可以灵活地对请求和响应进行处理和干预。

##### 应用场景

```python
# utils/md.py
from django.utils.deprecation import MiddlewareMixin
from django.shortcuts import HttpResponse

class DemoMiddleware(MiddlewareMixin):
    def process_request(self, request):
        print("来了")
        return HttpResponse("拦截了！")

    def process_response(self, request, response):
        print("走了")
        return response
```

```python
# settins.py
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
    # utils与app为同级目录
    "utils.md.DemoMiddleware",
]
```

1. 日志：获取用户访问的IP地址并记录到文件中。
2. 权限校验：有权限就返回None，无权限就返回`HttpResponse("无权访问")`。
3. 登录判断，判断用户的session中是否存储信息。

   ```python
   from django.utils.deprecation import MiddlewareMixin
   from django.shortcuts import redirect

   class DemoMiddleware(MiddlewareMixin):
      def process_request(self, req):
         # 0. 当请求路径为/login/时，进行放行
         if req.path_info == "/login/":
               # 返回None，继续执行视图中的代码
               return
         # 1. 获取用户session信息
         user_info = req.session.get("user_info")
         # 2. 有值，表示已登录，则继续
         if user_info:
               # 获取session信息，在views中可以通过req.user_info获取字典，req.userid获取用户id
               # 在html模板页面获取当前用户：{{ request.username }}
               req.user_info = user_info
               req.userid = user_info["id"]
               req.username = user_info["user"]
               return
         # 3. 没值，返回登录页面
         return redirect("/login/")

      def process_response(self, req, response):
         return response
   ```

##### 结合session和cookies机制来实现Django的会话控制功能

1. 配置设置：

   ```python
   # settings.py

   # 启用会话中间件
   MIDDLEWARE = [
      ...
      'django.contrib.sessions.middleware.SessionMiddleware',
      ...
   ]
   # 设置会话引擎
   SESSION_ENGINE = 'django.contrib.sessions.backends.db'
   # 设置会话存储方式为数据库
   SESSION_CACHE_ALIAS = 'default'
   ```

2. 使用会话：
   在视图函数或类视图中通过`request.session`访问会话对象，并使用它来读取和设置会话数据。

   ```python
   from django.http import HttpResponse

   def my_view(request):
      # 设置会话数据
      request.session['username'] = 'binjie09'
      # 获取会话数据
      username = request.session.get('username')
      return HttpResponse(f'Hello, {username}!')
   ```

3. 会话处理：
   Django会自动处理会话的创建、管理和销毁。在用户发送请求时，会自动生成一个唯一的会话ID，并将其存储在用户的浏览器中的cookie中。每次发送请求时，浏览器都会自动将会话ID作为cookie发送给服务器。
4. 配置cookie：
   默认情况下，Django会话使用名为`sessionid`的cookie来存储会话ID。如果需要自定义cookie的名称、过期时间或其他属性，可以通过在`settings.py`中进行配置来修改。

   ```python
   # settings.py

   # 设置会话cookie名称
   SESSION_COOKIE_NAME = 'myapp_session_id'
   # 设置会话cookie的过期时间（以秒为单位）
   SESSION_COOKIE_AGE = 3600
   # 设置会话cookie是否仅限于安全连接（HTTPS）
   SESSION_COOKIE_SECURE = True
   # 设置会话cookie是否仅限于同源策略
   SESSION_COOKIE_SAMESITE = 'Strict'
   ```

通过上述步骤，会话数据将在服务器端进行存储和管理，并通过cookie在客户端和服务器之间进行传递。可以根据需要设置、获取或删除会话数据，并根据会话的存在与否来进行相应的逻辑处理。

#### 处理MySQL数据

1. 安装：`pip install mysqlclient`
2. 创建数据库：`create database unicom;`
3. 数据库连接配置(settings.py)

   ```python
   DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'unicom',  # 数据库名称
        'USER': 'root',       # 数据库用户名
        'PASSWORD': 'Changping@13',   # 数据库密码
        'HOST': 'localhost',           # 数据库主机，默认为 localhost
        'PORT': '3306',                # 数据库端口，默认为 3306
        'OPTIONS': {
            'init_command': "SET sql_mode='STRICT_TRANS_TABLES'"  # 如果需要设置 SQL 模式，可以添加此配置项
         }
      }
   }
   ```

4. django操作表(app01/models.py)

   ```python
   from django.db import models
   # 当需要调整表结构时，只需要操作这个类即可
   class UserInfo(models.Model):
      name = models.CharField(max_length=32)
      password = models.CharField(max_length=64)
      age = models.IntegerField()
   """
   类名相当于表名，创建该类，相当于使用以下sql命令创建表
   create talbe app01_userinfo(
      id bigint auto_increment primary key,
      name varchar(32),
      password varchar(64),
      age int
   )
   """
   class UserList(models.Model):
      """员工表"""
      name = models.CharField(verbose_name="姓名", max_length=16)
      password = models.CharField(verbose_name="密码", max_length=64)
      age = models.IntegerField(verbose_name="年龄")
      account = models.DecimalField(verbose_name="工资", max_digits=10, decimal_places=2, default=0)
      create_time = models.DateTimeField(verbose_name="入职时间")
      # 1. 有外键约束
      #    - to，与哪张表关联
      #    - to_field，与表中的哪一列关联
      # 2. 当使用models.ForeignKey指令创建一个名为depart的外键字段时，django会自动生成一个depart_id的字段，即以下指令创建的字段名为department_id
      # 3. 部门表删除，对应的人员表的操作
      #    - 级联删除：`depart = models.ForeignKey(to="Department",to_field="id", on_delete=models.CASCADE)`
      #    - 外键置空：`depart = models.ForeignKey(to="Department",to_field="id", null=True, blank=True, on_delete=models.SET_NULL)`
      department = models.ForeignKey(to="Department",to_field="id", on_delete=models.CASCADE)
      # 在djangod中做的约束
      gender_choices = ((1,"男"),(2, "女"))
      gender = models.SmallIntegerField(verbose_name="性别", choices=gender_choices)
   ```

   ```shell
   # 每当涉及表结构的操作时都要执行这两条命令
   python manage.py makemigrations
   python manage.py migrate
   ```

5. orm操作数据

   ```python
   # insert into app01_dapartment(title) values("销售部");
   Department.objects.create(title="销售部")
   UserInfo.objects.create(name="张三", password="root134", age="18")

   # 删除
   Department.objects.filter(id=3).delete()

   # 查询
   data_list = UserInfo.objects.all()
   for obj in data_list:
      print(obj.id, obj.name, obj.password, obj.age)
   # 获取匹配到的数据
   data = UserInfo.objects.filter(id=1)
   print(data)
   # 获取匹配到的第一行数据
   row = UserInfo.objects.filter(id=1).first()
   print(row.id, row.name, row.password, row.age)

   # 修改
   # 把所有数据password重置为999
   UserInfo.objects.all().update(password=999)
   # 把匹配到的数据age重置为18
   UserInfo.objects.filter(id=2).update(age=18)
   ```

#### Django的pk属性

`pk` 是 Django 中常用的缩写，代表 "primary key"，即主键。在 Django 的模型中，每个对象都有一个主键字段，用于唯一标识该对象。
主键是一个自动生成的、唯一的整数字段，用于在数据库表中唯一标识每个记录。在 Django 中，默认情况下，每个模型都有一个名为 `id` 的自增主键字段。
可以用 `if self.instance.pk:` 来检查当前模型实例（对象）是否存在主键值。如果存在主键值，则说明当前操作为编辑（更新）对象的行为；如果不存在主键值，则说明当前操作为创建新对象的行为。
通过判断 `self.instance.pk` 是否为空，可以将代码分开处理编辑和创建两种不同的情况，以便执行相应的逻辑。

```python
# 自定义手机号格式校验
def clean_mobile(self):
   value = self.cleaned_data["mobile"]
   if self.instance.pk:
      # 编辑
      try:
            # 查询除了当前实例以外是否存在相同手机号的数据
            exists = models.UserInfo.objects.exclude(id=self.instance.pk).get(mobile=value)
      except models.UserInfo.DoesNotExist:
            return value
   else:
      # 新增数据
      try:
            # 查询是否存在相同手机号的数据
            exists = models.UserInfo.objects.get(mobile=value)
      except models.UserInfo.DoesNotExist:
            return value
   raise ValidationError("手机号已存在")
```

这段代码是一个自定义的表单字段校验方法，用于验证手机号字段的唯一性。

1. 首先，从表单数据中获取手机号 (`value = self.cleaned_data["mobile"]`)。
2. 然后，通过检查 `self.instance.pk` 是否存在来确定当前操作是新增数据还是编辑数据的行为。如果 `self.instance.pk` 存在，表示编辑操作；否则，表示新增操作。
3. 对于编辑操作：
   - 使用 `exclude` 方法查询除了当前实例以外是否存在具有相同手机号的数据。`self.instance.pk` 是当前正在编辑的实例的主键值。
   - 如果查询结果没有抛出 `models.UserInfo.DoesNotExist` 异常，则表示存在其他对象具有相同的手机号，说明该手机号已存在，应该抛出 `ValidationError` 异常，提示手机号已存在。
   - 如果查询结果抛出了 `models.UserInfo.DoesNotExist` 异常，则表示该手机号在其他对象中是唯一的，返回手机号值，校验通过。
4. 对于新增操作：
   - 使用 `get` 方法查询是否存在具有相同手机号的数据。
   - 如果查询结果没有抛出 `models.UserInfo.DoesNotExist` 异常，则表示存在其他对象具有相同的手机号，说明该手机号已存在，应该抛出 `ValidationError` 异常，提示手机号已存在。
   - 如果查询结果抛出了 `models.UserInfo.DoesNotExist` 异常，则表示该手机号是唯一的，返回手机号值，校验通过。
5. 如果在上述逻辑中未返回手机号值（即未发生异常），则会执行最后一行代码，抛出 `ValidationError` 异常，提示手机号已存在。

总之，这段代码的逻辑是根据当前操作是新增还是编辑，在数据库中查询是否存在相同手机号的数据。如果有相同的手机号存在，则抛出 `ValidationError` 异常；如果没有相同的手机号存在，则返回手机号值，表示校验通过。

### 模板继承

Django模板继承是一种方便的方式，可以在多个HTML页面中共享相同的结构和布局，并允许各个页面定义自己的内容。使用Django模板继承的步骤：

1. 创建基础模板（base template）：首先创建一个基础模板，作为其他页面模板的父模板。这个基础模板包含了所有页面都会共享的结构和布局，例如导航栏、页脚等。
2. 定义块（block）：在基础模板中，使用`block`标签定义可替换的内容区域。例如，你可以在基础模板中使用`{% block content %}{% endblock %}`来定义主要内容区域。
3. 创建子模板：在其他页面模板中，使用`extends`关键字指定要继承的基础模板。例如，`{% extends 'base.html' %}`。接着，在子模板中使用`{% block %}`标签填充基础模板中定义的块。例如，`{% block content %}`。

这样，在浏览器中渲染子模板时，基础模板和子模板会合并，生成最终的HTML页面。子模板中定义的块内容会替换掉基础模板中对应的块。
如果需要自定义多个不同的块，只需创建多个`{% block 自定义块名 %}`即可。如：不同页面的不同标题（title），可以在每个子模板中定义一个`{% block title %}`标签，并在具体页面中填充不同的标题内容。

```html
<!-- base.html -->
<!DOCTYPE html>
<html>
<head>
    <title>{% block title %}默认标题{% endblock %}</title>
</head>
<body>
    <!-- 导航栏等共通部分 -->
    <div class="content">
        {% block content %}
        {% endblock %}
    </div>
    <!-- 页脚等共通部分 -->
</body>
</html>
```

```html
<!-- home.html -->
{% extends 'base.html' %}

{% block title %}首页标题{% endblock %}

{% block content %}
    <h1>欢迎来到首页</h1>
    <!-- 具体页面内容 -->
{% endblock %}
```

```html
<!-- about.html -->
{% extends 'base.html' %}

{% block title %}关于我们标题{% endblock %}

{% block content %}
    <h1>关于我们</h1>
    <!-- 具体页面内容 -->
{% endblock %}
```

以上示例中，每个子模板都覆盖了基础模板中的`title`块，并填充了不同的标题内容。
通过合理使用模板继承和块，可以实现在不同页面中共享布局结构，并在每个页面中自定义特定内容的需求。

### 表单数据的处理

1. 用户提交的数据需要校验
2. 如果格式不匹配应当有错误提示
3. 应简化操作避免每个字段都要写一遍
4. 关联的数据，应当能自动获取并展示在页面
5. 可以通过Django来实现：Form/ModelForm

#### Form组件

在Django中，Form组件是用于处理表单数据的一个重要组件。它提供了一种方便的方式来创建HTML表单，并处理表单数据的验证、清理和保存。

使用Form组件可以实现的功能：

1. **表单字段定义**：通过定义Form类中的字段，可以指定表单需要包含的字段以及每个字段的类型、验证规则等。
2. **表单渲染**：Form组件可以将定义的字段转换为符合HTML标准的表单元素，并生成相应的HTML代码。
3. **数据验证和清理**：Form组件会自动验证用户提交的数据，并根据定义的字段验证规则进行验证。对于无效的数据，Form组件可以自动进行错误提示，并提供清理（cleaning）和转换（normalization）功能。
4. **表单数据处理**：一旦表单数据通过验证，Form组件可以将数据保存到数据库或执行其他必要的操作。

```python
"""views.py"""
from django import forms
def FormList(Form):
   # required=True 表示必填
    username = forms.CharField(required=True, widget=forms.Input)
    pwd = forms.CharField(required=True, widget=forms.Input)
    email = forms.CharField(required=True, widget=forms.Input)
    ctime = forms.CharField(widget=forms.Input)

def user_add(req):
    if req.method == "GET":
        form = FormList()
        return render(req, "user_add.html", {"form":form})
```

```html
<!-- user_add.html -->
<form method="post">
      {% for field in form %}
      {{ field }}
      {% endfor %}
      <!-- {{ form.ctime }} -->
      <!-- <input type="text" class="form-control" placeholder="创建时间" name="ctime"> -->
</form>
```

下面是使用Form组件的基本步骤：

1. 创建一个继承自`django.forms.Form`的Form类。
2. 在Form类中定义各个表单字段，如`CharField`、`IntegerField`等，以及其相应的验证规则。
3. 在视图函数或类中将表单实例化，并将请求数据传递给表单对象。
4. 调用表单对象的方法进行数据验证和清理。
5. 根据验证结果，处理有效的表单数据。

```python
from django import forms

class MyForm(forms.Form):
    name = forms.CharField(max_length=100, label='Name')
    age = forms.IntegerField(min_value=0, max_value=120, label='Age')

def my_view(request):
    if request.method == 'POST':
        form = MyForm(request.POST)
        if form.is_valid():
            # 处理有效的表单数据
            name = form.cleaned_data['name']
            age = form.cleaned_data['age']
            # 执行其他操作
    else:
        form = MyForm()
    
    return render(request, 'my_template.html', {'form': form})
```

上述示例创建了一个名为`MyForm`的Form类，定义了两个字段：`name`和`age`。`name`是一个字符字段，限制最大长度为100；`age`是一个整数字段，限制取值范围在0到120之间。当提交表单时，实例化`MyForm`，传递请求中的POST数据，并使用`is_valid()`方法进行验证。如果表单数据有效，可以通过`cleaned_data`属性来获取经过清理和转换的数据。

总结：
Django的Form组件提供了一种方便的方式来处理表单数据，包括定义表单字段、渲染HTML表单、数据验证和清理等功能。通过使用Form组件，可以简化表单处理的开发流程，提高代码的可读性和维护性。

#### ModelForm组件（主用）

在Django中，ModelForm组件是建立在Model模型基础上的表单组件，它简化了与数据库模型相关的表单处理。ModelForm可以根据指定的模型自动生成表单字段，并提供了对数据验证、保存等功能的支持。

使用ModelForm可以实现的功能：

1. **自动生成表单字段**：ModelForm会根据指定的模型自动生成表单字段，并根据字段类型和模型定义自动设置相应的验证规则。
2. **表单渲染**：ModelForm将自动生成的表单字段转换为HTML代码，并提供默认的表单样式。
3. **数据验证和清理**：ModelForm会根据模型字段的定义进行数据验证，并提供数据清理（cleaning）和转换（normalization）功能。
4. **实例化和保存**：ModelForm可以实例化为具体的表单对象，用于显示和处理用户提交的表单数据。**同时，它也提供了将表单数据保存到数据库的功能。**

```python
"""views.py"""
from django.forms import ModelForm

class UserModelForm(ModelForm):
    class Meta:
        model = models.UserInfo
        fields = ["name", "password", "age", "account", "gender","department","create_time"]

def user_add_modelform(req):
    """添加用户ModelForm版"""
    form = UserModelForm()
    return render(req, "user_add_modelform.html", {"form": form})
```

```html
<!-- user_add_modelform -->
<form action="" method="post">
   {% csrf_token %}
   <!-- {{form.name.label }}: {{ form.name }}
   {{form.password.label }}: {{ form.password }}
   {{form.age.label }}: {{ form.age }} -->
   {% for field in form %}
   {{ field.label }}: {{ field }}
   {% endfor %}
</form>
```

使用ModelForm的基本步骤：

1. 创建一个继承自`django.forms.ModelForm`的ModelForm类。
2. 在ModelForm类中指定关联的模型，并可以选择性地定义要包含的字段、排除的字段、额外的字段等。
3. 可选地自定义字段的验证规则、显示标签等。
4. 在视图函数或类中将ModelForm实例化，并将请求数据传递给表单对象。
5. 调用表单对象的方法进行数据验证和清理。
6. 根据验证结果，处理有效的表单数据，如保存到数据库。

```python
from django import forms
from .models import MyModel  # 导入相关的模型

class MyModelForm(forms.ModelForm):
    class Meta:
        model = MyModel
        fields = ['name', 'age']  # 指定包含的字段

def my_view(request):
    if request.method == 'POST':
        form = MyModelForm(request.POST)
        if form.is_valid():
            # 处理有效的表单数据
            instance = form.save()  # 将表单数据保存到数据库
            # 执行其他操作
    else:
        form = MyModelForm()
    
    return render(request, 'my_template.html', {'form': form})
```

在上述示例中，创建了一个名为`MyModelForm`的ModelForm类，关联了一个名为`MyModel`的模型，并指定了要包含的字段为`name`和`age`。当提交表单时，实例化`MyModelForm`，传递请求中的POST数据，并使用`is_valid()`方法进行验证。如果表单数据有效，可以通过调用`save()`方法将表单数据保存到数据库，并返回相关的模型实例。

总结：
Django的ModelForm组件简化了与数据库模型相关的表单处理，自动生成表单字段、支持数据验证和保存等功能。通过使用ModelForm，开发人员可以更方便地处理与模型相关的表单数据，并减少重复的代码编写。

#### 定制化对象输出内容

```python
class Foo(object):
   def __init__(self, name):
      self.name = name
   def __str__(self):
      return self.name

obj = Foo("IT部门")
print(obj)
```

```python
"""models.py"""
class Department(models.Model):
    """部门表"""
    title = models.CharField(verbose_name="标题", max_length=32)
    def __str__(self):
        return self.title
```

#### 数据校验

将编码语言改为中文，编辑`settings.py` 修改变量：`LANGUAGE_CODE = 'zh-hans'`

### 搜索

#### 模板语法

```python
models.UserInfo.objects.filter(id=9) # id=9
models.UserInfo.objects.filter(id=9, name="张三") # id=9 && name="张三"
models.UserInfo.objects.exclude(id=9) # id != 9

models.UserInfo.objects.filter(id__gt=9) # id>9
models.UserInfo.objects.filter(id__gte=9) # id>=9
models.UserInfo.objects.filter(id__lt=9) # id<9
models.UserInfo.objects.filter(id__lte=9) # id<=9

models.UserInfo.objects.filter(name__contains="张三") # name包含"张三"，相当于sql的 like "%张三%"

models.UserInfo.objects.filter(**{"id":9, "name":"张三"}) # 用字典的方式进行检索
models.UserInfo.objects.filter(**{"id__gte":9, "name__contains":"张三"}) # id>=9 && name包含"张三"
models.UserInfo.objects.filter(department__title="运营部") # 查找运营部的员工信息
```

#### Q查询

参考：`https://www.cnblogs.com/wupeiqi/articles/6216618.html`

导入模块：`from django.db.models import Q`

```python
models.UserInfo.objects.filter(Q(id=8)|Q(age=9)) # 支持或查询
models.UserInfo.objects.filter(Q(id=8)&Q(age=9)) # 支持且查询
models.UserInfo.objects.filter(Q(Q(id=8)&Q(age=9))&Q(name="张三")) # 同时使用或和且的条件查询

q1=Q() # 构造Q对象
q1.connector = "OR" # 或查询
q1.children.append(("id", 1))
q1.children.append(("name__contains", "张"))
q1.children.append(("department_title", "研发部"))
# id=1||name like '%张%'||department.title = "研发部"
models.UserInfo.objects.filter(q1) # 按照构建好的Q对象的规则进行查询
```

#### 页面展示

1. 将搜索框构建成form表单，以get方式提交数据
2. button的type为submit，用以提交数据
3. input标签添加name属性，以`url?属性=属性值`的方式提交请求

代码

1. 按条件搜索

   ```html
   <form class="d-flex me-3" role="search" method="get">
      <div class="input-group">
            <div class="col-auto">
               <!-- 保留左上和左下的圆角，去掉其他圆角 -->
               <select name="field" class="form-select" style="border-radius: 0.3rem 0 0 0.3rem;">
                  <option value="name__contains">姓名</option>
                  <option value="email__contains">邮箱</option>
                  <option value="mobile__contains">手机号</option>
               </select>
            </div>
            <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search"
               name="key">
            <button class="btn btn-outline-success" type="submit">Search</button>
      </div>
   </form>
   ```

2. 利用循环锁定选择的匹配条件

   ```html
   <form class="d-flex me-3" role="search" method="get">
      <div class="input-group">
            <div class="col-auto">
               <select name="field" class="form-select" style="border-radius: 0.3rem 0 0 0.3rem;">
                  <!-- 遍历 field_list 列表中的每个元素 -->
                  {% for group in field_list %}
                  <!-- 如果当前元素的第一个值等于变量 field 的值 -->
                  {% if group.0 == field %}
                  <!-- 创建一个选中的选项 -->
                  <option value="{{ group.0 }}" selected>{{ group.1 }}</option>
                  {% else %}
                  <!-- 创建一个未选中的选项 -->
                  <option value="{{ group.0 }}">{{ group.1 }}</option>
                  {% endif %}
                  {% endfor %}
               </select>
            </div>
            <!-- 创建一个输入框，value 属性设置为变量 key 的值 -->
            <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search"
               name="key" value="{{ key }}">
            <!-- 创建一个提交按钮 -->
            <button class="btn btn-outline-success" type="submit">Search</button>
      </div>
   </form>
   ```

#### 搜索功能

1. 提交数据
2. 接收数据
3. 结果筛选和展示
4. URL显示的信息太多需要用ajax来解决

#### 功能实现

1. 使用模糊匹配的方式实现

   ```python
   # views.py

   def user_list(req):
      key = req.GET.get("key")
      if key:
         # 如果key有值，即搜索框中有内容，则按照搜索内容模糊匹配姓名字段，倒序输出
         queryset = models.UserInfo.objects.filter(name__contains=key).order_by('-id')
      else:
         # 如果key没值，则把所有数据都倒序输出
         queryset = models.UserInfo.objects.all().order_by('-id')
      return render(req, "user_list.html", {'queryset':queryset})
   ```

2. 使用字典的方式实现

   ```python
   def user_list(req):
      # 设置过滤条件分类
      field_list = [("name__contains", "姓名"), ("email__contains", "邮箱"), ("mobile__contains", "手机号"), ("department__title__contains", "部门"),]
      # 创建一个空字典用于存储过滤条件
      condition = {}
      # 获取名为"key"的查询参数值，如果没有传值，值为空字符串，解决未传值时默认为None的问题
      key = req.GET.get("key", "")
      # 获取名为"field"的查询参数值
      field = req.GET.get("field")
      # 如果存在查询关键字，则将过滤条件设置为{字段名称: 查询关键字}
      if key:
         condition[field] = key.strip()
      # 根据过滤条件查询数据并按"id"字段降序排序
      queryset = models.UserInfo.objects.filter(**condition).order_by('-id')
      # return render(req, "user_list.html", {'queryset':queryset, 'key':key, 'field': field, 'field_list':field_list})
      # 返回渲染后的HTML页面，将查询结果传递给模板，locals()方法获取当前环境中所有局部变量（这个函数中定义的）
      return render(req, "user_list.html", locals())
   ```

   当 `key` 没有值时，也即为 `None` 或空字符串时，不执行 `if key` 下的代码块。因此，`condition` 字典保持为空字典，没有任何筛选条件。在 `filter(**condition)` 中，使用空字典作为参数传入查询函数，相当于没有设置任何过滤条件，所以会返回数据库中的所有数据。

#### 多个页面在非母版范围，需要相同html组件时，使用include功能

1. 将共用的功能组件写入单独的html页面，如搜索功能，文件名为 `search.html`

   ```html
   <form class="d-flex me-3" role="search" method="get">
      <div class="input-group">
         <div class="col-auto">
               <select name="field" class="form-select" style="border-radius: 0.3rem 0 0 0.3rem;">
                  <!-- <option value="name__contains">姓名</option>
                  <option value="email__contains">邮箱</option>
                  <option value="mobile__contains">手机号</option> -->
                  {% for group in field_list %}
                  {% if group.0 == field %}
                  <option value="{{ group.0 }}" selected>{{ group.1 }}</option>
                  {% else %}
                  <option value="{{ group.0 }}">{{ group.1 }}</option>
                  {% endif %}
                  {% endfor %}
               </select>
         </div>
         <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" name="key"
               value="{{ key }}">
         <button class="btn btn-outline-success" type="submit">Search</button>
      </div>
   </form>
   ```

2. 在需要这个功能的页面中使用 `{% include 'search.html' %}`

#### Q查询实现

```html
<!-- search2.html -->
<form class="d-flex me-3" role="search" method="get">
    <div class="input-group">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" name="key"
            value="{{ key }}">
        <button class="btn btn-outline-success" type="submit">Search</button>
    </div>
</form>
```

```python
from django.db.models import Q

def depart_list(req):
    """部门列表"""
    key = req.GET.get("key", "")
    q1 = Q()
    if key:
        q1.connector = "OR"
        q1.children.append(("departname__contains", key))
        q1.children.append(("depart_leader__contains", key))
        q1.children.append(("depart_phone__contains", key))
        q1.children.append(("superior_department__contains", key))
    queryset = models.Department.objects.filter(q1)
    return render(req, "depart_list.html", locals()).order_by("-id")
```

### 分页

1. 通过queryset支持的切片功能实现数据分页
2. 通过URL传递的参数来决定查看第几页数据（如`?page=2`）
3. 通过设置每页显示多少数据，来计算每页的起始索引和结束索引
4. 通过前端页面的调度来跳转到带有`page`参数的URL来实现功能
5. 通过`django.utils.safestring.mark_safe`生成页码标签
6. 处理极值情况：条件控制只显示有数据的页的页码

```python
def depart_list(req):
    """部门列表"""
    # 获取请求中的关键字参数
    key = req.GET.get("key", "")
    # 使用Q对象进行查询条件的构建
    q1 = Q()
    # 如果关键字参数存在，则将多个查询条件添加到Q对象中
    if key:
        # 使用"OR"逻辑连接符
        q1.connector = "OR"
        # 添加部门名称包含关键字的查询条件
        q1.children.append(("departname__contains", key))
        q1.children.append(("depart_leader__contains", key))
        q1.children.append(("depart_phone__contains", key))
        q1.children.append(("superior_department__contains", key))
    # 获取页码参数，默认为第一页
    page = int(req.GET.get("page", 1))
    # 如果页码小于1，则设置为1
    if page < 1:
        page = 1
    # 计算查询结果的起始索引和结束索引
    start = (page -1) * 20
    end = page * 20
    # 根据查询条件进行数据库查询并获取结果集
    queryset = models.Department.objects.filter(q1)[start:end]
    # 渲染模板并返回响应
    return render(req, "depart_list.html", locals())
```

### 封装组件

```python
"""
视图函数：
from utils.pagination import Pagination
def depart_list(req):
   # 定义参数
   perpage_datanum = 15
   page_num_count = 5
   # 实例化对象
   pager = Pagination(req, perpage_datanum, page_num_count)
   queryset = models.Department.objects.filter(q1)[pager.data_start:pager.data_end]
   # 返回结果
   return render(req, "depart_list.html", locals())

前端页面：
   {% for obj in queryset %}
   {% endfor %}
   {{ pager.html }}
"""

from usermanagement import models
from django.utils.safestring import mark_safe

class Pagination(object):
   def __init__(self, req, perpage_datanum, page_num_count):
      # 1. 获取访问的分页
      page = req.GET.get("page", "1")
      if not page.isdecimal():
         page = 1
      else:
         page = int(page)
         if page < 1:
               page = 1
      self.page = page
      # 2. 做数据分片
      self.data_start = (page -1) * perpage_datanum
      self.data_end = page * perpage_datanum
      # 3. 计算总共分几页
      # 计算有几条数据
      data_count = models.Department.objects.all().count()
      # 计算页数和剩余几条数据
      page_count, div = divmod(data_count, perpage_datanum)
      # 如果有剩余的数据，剩余的数据不为0条，则另开一页
      if div:
         page_count += 1
      # 4. 生成页码标签
      self.page_num_count = page_num_count
      half_page_num = divmod(self.page_num_count, 2)[0]
      # 极值处理，访问第1页时，只显示1-3的页码
      if page < page_num_count - half_page_num:
         self.page_previous = 1
         self.page_next = page_num_count
      elif page > page_count - half_page_num:
         # 两种算法
         self.page_previous = page_count - page_num_count + 1
         # page_previous = page - half_page_num - (half_page_num - (page_count - page))
         self.page_next = page_count
      else:
         # 限制显示页码个数：这里只显示上一页和下一页
         self.page_previous = page - half_page_num
         self.page_next = page + half_page_num
   def html(self):
      page_list = []
      for i in range(self.page_previous, self.page_next+1):
         if i == self.page:
               element = '<li class="page-item active"><a class="page-link" href="?page={0}">{0}</a></li>'.format(i)
         else:
               element = '<li class="page-item"><a class="page-link" href="?page={0}">{0}</a></li>'.format(i)
         page_list.append(element)
      page_string = mark_safe("".join(page_list))
      return page_string
```

### request.GET

1. request.GET获取URL中传递的所有参数

   ```python
   def depart_list(req):
      print(type(req.GET)) # <class 'django.http.request.QueryDict'>
   ```

2. QueryDict 默认无法被修改，`QueryDict._mutable = False`；当修改为 `QueryDict._mutable = True` 时，表示 QueryDict 可以被修改
3. 深拷贝（Deep Copy）是在计算机科学中用于复制对象的一种技术。它不仅会复制对象本身，还会递归地复制对象所引用的所有子对象，确保新创建的对象与原始对象完全独立，而不共享内存空间。在 Python 中，可以使用 `copy.deepcopy()` 函数实现深拷贝。这个函数接受一个对象作为参数，并返回该对象的一个深拷贝副本。深拷贝可以用于任何类型的对象，包括列表、字典、自定义类等。

   ```python
   import copy

   def depart_list(req):
      # 深拷贝 request.GET 对象，以便进行修改而不影响原始对象
      query_dict = copy.deepcopy(request.GET)
      # 设置查询字典为可修改的状态，以便设置参数值
      query_dict._mutable = True
      # 将名为 "page" 的参数的值设置为 [2]
      query_dict.setlist("page", [2])
      # 打印修改后的查询字典
      print(query_dict)  # <QueryDict: {'page': [2]}>
      # 使用 urlencode() 方法将查询字典转换为 URL 编码字符串
      print(query_dict.urlencode())  # page=2
   ```

   这段代码使用了 `copy.deepcopy()` 函数创建了 `request.GET` 的深拷贝副本，并将其赋值给 `query_dict`。
   然后，通过设置 `query_dict._mutable = True`，将查询字典对象设置为可修改的状态。这是因为在默认情况下，Django 的 HttpRequest 对象的 `GET` 和 `POST` 属性都是不可修改的 (`_mutable=False`)，需要将其设置为可修改才能进行参数的修改操作。
   接下来，使用 `query_dict.setlist("page", [2])` 将参数名为 "page" 的值设置为列表 `[2]`，即将原来的值进行替换。
   最后，通过打印 `query_dict` 可以看到修改后的查询字典对象，以及使用 `query_dict.urlencode()` 方法将查询字典转换为 URL 编码字符串，输出结果为 `page=2`。

4. 结合深拷贝和QueryDict的特性，可以将分页效果在基于获取到URL的参数的基础上实现。

   ```python
   from usermanagement import models # 导入模块
   from django.utils.safestring import mark_safe # 支持后端渲染html
   import copy # 拷贝
   from django.db.models import Q # Q查询

   """
   路径：utils/pagination.py，utils与app为同级目录

   视图函数：
   from utils.pagination import Pagination
   def depart_list(req):
      # 1. 定义参数
      # 每页显示的数据条数
      perpage_datanum = 15
      # 显示的页码数量
      page_num_count = 5
      # 获取搜索关键字
      key = req.GET.get("key", "")
      # 2. 实例化对象
      pager = Pagination(req, perpage_datanum, page_num_count,key)
      # 3. 根据搜索条件获取对应的部门数据
      queryset = models.Department.objects.filter(pager.get_search_condition(key))[pager.data_start:pager.data_end]
      # 4. 返回结果
      return render(req, "depart_list.html", locals())

   前端页面：
      {% for obj in queryset %}
         {% if pager.page > 1 %}
         {% else %}
         {% endif %}
      {% endfor %}
      {{ pager.html }}
   """

   class Pagination(object):
      def __init__(self, req, perpage_datanum, page_num_count, key):
         """
         初始化 Pagination 对象

         参数:
         - req: HttpRequest 对象，请求对象
         - perpage_datanum: int，每页显示的数据条数
         - page_num_count: int，显示的页码数量
         - key: str，搜索关键字
         """
         # 1. 获取访问的分页
         # 获取请求中的页码，默认为第一页
         page = req.GET.get("page", "1")
         # 如果页码不是数字，则设置为 1
         if not page.isdecimal():
               page = 1
         # 将页码转换为整数类型
         else:
               page = int(page)
               # 如果页码小于 1，则设置为 1
               if page < 1:
                  page = 1
         # 当前页码
         self.page = page

         # 2. 做数据分片
         # 计算起始数据索引
         self.data_start = (self.page - 1) * perpage_datanum
         # 计算结束数据索引
         self.data_end = self.page * perpage_datanum

         # 3. 计算总共分几页
         # 根据搜索条件获取数据的总数
         data_count = models.Department.objects.filter(self.get_search_condition(key)).count()
         # 计算总页数和剩余数据量
         self.page_count, div = divmod(data_count, perpage_datanum)
         # 如果有剩余的数据，剩余的数据不为0条，则另开一页
         if div:
               self.page_count += 1

         # 4. 生成页码标签
         # 显示的页码数量
         self.page_num_count = page_num_count
         # 页码数量的一半
         half_page_num = divmod(self.page_num_count, 2)[0]
         # 当数据量不足以填满设置的页码数时，只显示有数据的页码：起始页码设为 1，最后页码设为总页数
         if self.page_count < page_num_count:
               self.page_previous = 1
               self.page_next = self.page_count
         else:
               # 极值处理，访问的页码小于一半的页码数量时：起始页码设为 1，最后页码设为显示的页码数量
               if self.page < page_num_count - half_page_num:
                  self.page_previous = 1
                  self.page_next = page_num_count
               # 访问的页码离总页数小于一半的页码数量时：起始页码为(总页数-显示的页码数量+1)，最后页码为总页数
               elif self.page > self.page_count - half_page_num:
                  # 两种算法
                  self.page_previous = self.page_count - page_num_count + 1
                  # self.page_previous = self.page - half_page_num - (half_page_num - (self.page_count - self.page))
                  self.page_next = self.page_count
               # 处理访问中间页码的情况：起始页码为当前页码减去一半的页码数量，最后页码为当前页码加上一半的页码数量
               else:
                  # 限制显示页码个数：这里只显示上一页和下一页
                  self.page_previous = self.page - half_page_num
                  self.page_next = self.page + half_page_num
         # 搜索关键字
         self.key = key
         # 深拷贝请求参数
         self.query_dict = copy.deepcopy(req.GET)
         # 设置参数，使对象可以被修改
         self.query_dict._mutable = True                         

      def get_search_condition(self, key):
         """
         获取搜索条件

         参数:
         - key: str，搜索关键字

         返回:
         - q1: Q 对象，搜索条件
         """
         # 创建一个空的 Q 对象
         q1 = Q()
         if key:
               # 设置连接方式为 OR
               q1.connector = "OR"
               # 添加部门名称包含关键字的条件
               q1.children.append(("departname__contains", key))
               # 添加部门领导包含关键字的条件
               q1.children.append(("depart_leader__contains", key))
               # 添加部门电话包含关键字的条件
               q1.children.append(("depart_phone__contains", key))
               # 添加上级部门包含关键字的条件
               q1.children.append(("superior_department__contains", key))
         # 返回搜索条件
         return q1

      def html(self):
         """
         生成HTML标签字符串

         返回:
         - page_string: str，生成的HTML标签字符串
         """
         page_list = []
         for i in range(self.page_previous, self.page_next + 1):
               # 设置页码参数为当前页码
               self.query_dict.setlist("page", [i])
               # 将请求参数编码为URL查询字符串
               query = self.query_dict.urlencode()
               if i == self.page:
                  element = '<li class="page-item active"><a class="page-link" href="?{0}">{1}</a></li>'.format(query, i)
               else:
                  element = '<li class="page-item"><a class="page-link" href="?{0}">{1}</a></li>'.format(query, i)
               page_list.append(element)
         # 使用 mark_safe 函数将字符串标记为安全的 HTML 代码
         page_string = mark_safe("".join(page_list))
         # 返回生成的HTML标签字符串
         return page_string
   ```

   ```html
   {% load static %}
   <link rel="stylesheet" href="{% static 'plugins/bootstrap-5.3.0/css/bootstrap.min.css' %}">
   <nav aria-label="Pagination">
      <ul class="pagination justify-content-center">
         <!-- 如果当前页码大于1，则可用 Previous 按钮跳转到上一页-->
         {% if pager.page > 1 %}
         <li class="page-item">
               <a class="page-link" href="?page={{ page|add:'-1' }}">Previous</a>
         </li>
         <!-- 否则，禁用 Previous 按钮 -->
         {% else %}
         <li class="page-item disabled">
               <a class="page-link" href="?page={{ page|add:'-1' }}">Previous</a>
         </li>
         {% endif %}
         <!-- 输出 Pagination 中生成的 HTML 标签字符串，即页码标签 -->
         {{ pager.html }}
         <!-- 如果当前页码不是最后一页，则可用 Next 按钮跳转到下一页-->
         {% if pager.page < pager.page_count %} <li class="page-item">
               <a class="page-link" href="?page={{ page|add:'1' }}">Next</a>
               </li>
               {% else %}
               <!-- 否则，禁用 Next 按钮 -->
               <li class="page-item disabled">
                  <a class="page-link" href="?page={{ page|add:'1' }}">Next</a>
               </li>
               {% endif %}
      </ul>
   </nav>
   ```

## 项目：工单系统

### 项目初始化

1. 创建项目 + 创建虚拟环境
2. 下载django框架、MySQL连接组件 `pip install django pymysql`(pymysql或mysqlclient)
3. 创建django项目 `django-admin.exe startproject workflow`
4. 创建app `python .\workflow\manage.py startapp login`
5. 注册app(settings.py)

   ```python
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'login.apps.LoginConfig',
   ]
   ```

6. 如果连接数据库使用`pymysql`，配置 `workflow/__init__.py`

   ```python
   import pymysql

   pymysql.install_as_MySQLdb()
   ```

   `pymysql.install_as_MySQLdb()`将`pymysql`注册为Django的默认数据库引擎（Database Engine）——`MySQLdb`。在Django中将`pymysql`作为新的MySQL数据库驱动程序，并用于与MySQL数据库进行通信。
7. 配置settings.py连接MySQL

   ```python
   DATABASES = {
      'default': {
         'ENGINE': 'django.db.backends.mysql',
         'NAME': 'unicom',
         'USER': 'root',
         'PASSWORD': 'Changping@13',
         'HOST': '127.0.0.1',
         'POST': 3306
      }
   }
   ```

8. 创建数据库 `create database unicom DEFAULT CHARSET utf8 COLLATE utf8_general_ci;`

### 用户登录

不同用户权限不同，能看到的菜单不同

#### 基础框架部分

1. 创建表结构 `workflow/login/models.py`

   ```python
   from django.db import models


   class UserInfo(models.Model):
      role_choices = (('user', '员工'), ('leader', '领导'))
      role = models.CharField(verbose_name="角色", choices=role_choices, max_length=12)
      username = models.CharField(verbose_name="用户名", max_length=32)
      password = models.CharField(verbose_name="密码", max_length=64)
   ```

2. 将表结构同步到数据 `python manage.py makemigrations` `python manage.py migrate`
3. 创建视图函数
   1. 删除原app中的views.py，并创建views目录
   2. 在views目录中分别创建视图函数存放的文件
   3. 视图函数：

      ```python
      from django.shortcuts import render, redirect, HttpResponse
      from django import forms
      from login import models

      class LoginForm(forms.Form):
         username = forms.CharField(label="用户名", required=True)
         password = forms.CharField(label="密码", required=True, widget=forms.PasswordInput(render_value=True))

         def __init__(self, *args, **kwargs):
            super().__init__(*args, **kwargs)
            for name, field in self.fields.items():
                  # 为元素添加样式
                  field.widget.attrs["class"] = "form-control"
                  # 为元素添加placeholder
                  field.widget.attrs["placeholder"] = "请输入{}".format(field.label)


      def login(req):
         if req.method == "GET":
            form = LoginForm()
            return render(req, 'login.html', {"form": form})
         form = LoginForm(data=req.POST)
         # 1. 校验用户填写的数据是否合法
         if not form.is_valid():
            return render(req, "login.html", {"form": form})
         # 2. 获取数据库信息进行比对
         user_object = models.UserInfo.objects.filter(**form.cleaned_data).first()
         if not user_object:
            return render(req, "login.html", {"form": form, "error":"用户名或密码错误"})
         # 3. 登录成功，用户信息存储到session
         req.session["user_info"] = {"id":user_object.id, "username":user_object.username, "role":user_object.role}
         return redirect("/home/")

      def logout(req):
         req.session.clear()
         return redirect("/login/")

      def home(req):
         return render(req, 'home.html')
      ```

   4. 注册视图 `workflow/workflow/urls.py`

      ```python
      from login.views import account

      urlpatterns = [
         path('admin/', admin.site.urls),
         path('login/', account.login),
         path('logout/', account.logout),
         path('home/', account.home),
      ]
      ```

4. 中间件函数(utils/Auth.py)：

   ```python
   from django.utils.deprecation import MiddlewareMixin
   from django.shortcuts import redirect

   class AuthMiddleware(MiddlewareMixin):
      def process_request(self, req):
         # 0. 当请求路径为/login/时，进行放行
         if req.path_info == "/login/":
               # 返回None，继续执行视图中的代码
               return
         # 1. 获取用户session信息
         user_info = req.session.get("user_info")
         # 2. 有值，表示已登录，则继续
         if user_info:
               # 获取session信息
               req.user_info = user_info
               req.userid = user_info["id"]
               req.username = user_info["username"]
               req.role = user_info["role"]
               return
         # 3. 没值，返回登录页面
         return redirect("/login/")
   ```

5. 前端页面菜单权限控制部分：

   ```html
   <ul class="navbar-nav me-auto mb-2 mb-lg-0">
      {% if request.role == "leader" %}
      <li class="nav-item"><a class="nav-link" href="/depart/list">部门管理</a></li>
      <li class="nav-item"><a class="nav-link" href="/user/list">用户管理</a></li>
      {% else %}
      <li class="nav-item"><a class="nav-link" href="/user/list">资产管理</a></li>
      {% endif %}
   </ul>
   ```

6. 启动项目 `python manage.py runserver`

7. 导出依赖 `pip freeze > requirements.txt`

#### 自定义模板方法

Django 提供了自定义模板方法（Custom template tags）的功能，它允许在模板中定义自己的方法，以便在模板中执行特定的操作和逻辑。自定义模板方法可以方便地扩展模板引擎的功能，能够处理更复杂的逻辑。Django 自定义模板方法的使用步骤：

1. 创建一个`templatetags` 的 Python 模块来存放自定义模板方法。这个模块可以在 Django 项目中的任何位置，只需确保它可以被 Django 引用到即可。一般在已注册的app目录下。
2. 在该模块中，使用 `register.simple_tag` 装饰器来注册自定义模板方法。该装饰器接受一个可选的参数 `takes_context`，用于指示自定义方法是否需要访问模板上下文。
3. 在模板中加载自定义模板方法，并使用 `{% load %}` 标签将其导入到模板中。
4. 在模板中使用自定义模板方法，使用 `{% your_custom_tag %}` 这样的语法调用它。
5. 案例一

   ```python
   # myapp/templatetags/custom_tags.py

   from django import template

   register = template.Library()

   @register.simple_tag
   def multiply(value, arg):
      return value * arg
   ```

   ```html
   <!-- template.html -->

   {% load custom_tags %}

   <p>5 multiplied by 3 is {% multiply 5 3 %}.</p>
   ```

   以上代码创建了一个自定义模板方法 `multiply`，它接受两个参数并返回它们的乘积。然后，在模板中使用 `{% multiply 5 3 %}` 调用该方法，显示结果。
   除了 `register.simple_tag` 装饰器外，Django 还提供了其他几种装饰器来注册不同类型的自定义模板方法，如 `register.inclusion_tag` 用于渲染包含部分模板的片段，`register.assignment_tag` 用于将结果赋值给模板变量等等。可以根据需要选择合适的装饰器。
6. 案例二

   ```python
   # login/templatetags/memu.py
   from django.template import Library

   register = Library()


   @register.inclusion_tag('memu.html')
   def memu():
      """
      自定义模板方法：menu
      该方法用于生成菜单，并将菜单数据传递给指定的模板进行渲染。
      模板名称：'menu.html'
      """
      return {"title": "百工一道", "count": 90}
   ```

   ```html
   <!-- templates/memu.html -->
   <!-- 创建html模板 -->
   <div>
      本次参与学习的公司是 {{ title }}，参与的人数有{{ count }}
   </div>
   ```

   ```html
   <!-- templates/layout.html -->
   <!-- 加载html模板 -->
   {% load memu %}
   <body>
      <!-- 调用html模板 -->
      {% memu %}
   </body>
   ```

#### 菜单控制第二版

1. 配置 `settings.py`，在文件尾部追加：

   ```python
   # menu
   UNICOM_MENU = {
      "leader": [
         {"menu": "用户管理", "url": ""},
         {"menu": "订单管理", "url": ""},
         {"menu": "工单管理", "url": ""},
      ],
      "user": [
         {"menu": "用户管理", "url": ""},
         {"menu": "工单管理", "url": ""},
      ]
   }
   ```

2. 在 `login/templatetags` 文件夹中创建 `menu.py` 文件，编写自定义模板方法

   ```python
   from django.template import Library
   from django.conf import settings

   register = Library()


   @register.inclusion_tag('menu.html')
   def menu(req):
      # 0. 获取当前用户的角色信息，获取在中间件中定义的req.role
      role = req.role
      # 1. 去settings中获取所有菜单信息
      user_memu_list = settings.UNICOM_MENU[role]
      return {"menu_list": user_memu_list}
   ```

3. 编写自定义模板 `menu.html`

   ```html
   {% for item in menu_list %}
   <li class="nav-item"><a class="nav-link" href="{{ item.url }}">{{ item.menu }}</a></li>
   {% endfor %}
   ```

4. 在模板文件中加载使用自定义模板

   ```html
   <!-- 写在html文件头部 -->
   {% load menu %}

   <!-- 写在原导航栏的菜单部分 -->
   <ul class="navbar-nav me-auto mb-2 mb-lg-0">
      <!-- 这里的request是从自定义模板方法中传入的参数 -->
      {% menu request %}
   </ul>
   ```

#### 默认选中

在html中使用`<li class="active">`。
通过获取url与菜单中的url进行比较，使得访问到该菜单时，让它有默认选中的效果。

1. 在 `views` 目录下创建几个视图函数文件：`order.py` `user.py` `work.py`
2. 将其注册进 `urls.py`

   ```python
   from django.contrib import admin
   from django.urls import path
   from login.views import account
   from login.views import order
   from login.views import user
   from login.views import work

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('login/', account.login),
      path('logout/', account.logout),
      path('home/', account.home),
      path('order/', order.order),
      path('user/', user.user),
      path('work/', work.work),
   ]
   ```

3. 创建视图函数和对应的html模板

   ```python
   from django.shortcuts import render


   def order(req):
      return render(req, "order.html")
   ```

   ```html
   {% extends "layout.html" %}
   {% block title %}order{% endblock %}
   {% block content %}
   <h3>order</h3>

   {% endblock %}
   ```

   其他三个视图一样。

4. 修改settings中的url配置，修改后页面可以正常跳转

   ```python
   # menu
   UNICOM_MENU = {
      "leader": [
         {"menu": "用户管理", "url": "/user/"},
         {"menu": "订单管理", "url": "/order/"},
         {"menu": "工单管理", "url": "/work/"},
      ],
      "user": [
         {"menu": "工单管理", "url": "/work/"},
      ]
   }
   ```

5. 在 `menu.py` 中实现url比对逻辑

   ```python
   from django.template import Library
   from django.conf import settings
   import copy

   register = Library()


   @register.inclusion_tag('menu.html')
   def menu(req):
      # 0. 获取当前用户的角色信息
      # 获取在中间件中定义的req.role
      role = req.role
      # 1. 去settings中获取所有菜单信息
      # 使用深拷贝，避免加载的是内存中的url
      user_memu_list = copy.deepcopy(settings.UNICOM_MENU[role])
      # 2. 通过将 user_memu_list 原本的 {"menu": "用户管理", "url": "/user/"} 构造成 {"menu": "用户管理", "url": "/user/", "class": "active"} 来实现选中状态
      for row in user_memu_list:
         # 通过path_info来获取url后面的路径部分，如/work/
         # 3. 解决子菜单没有默认选中效果的问题，要确保每个子菜单的一级目录与父菜单一致
         if req.path_info.startswith(row["url"]):
               # 为 user_memu_list 中这个url的菜单添加样式
               row["class"] = "active"
         else:
               row["class"] = ""
      return {"menu_list": user_memu_list}
   ```

6. 在 `menu.html` 中应用样式

   ```html
   {% for item in menu_list %}
   <li class="nav-item"><a class="nav-link {{ item.class }}" href="{{ item.url }}">{{ item.menu }}</a></li>
   {% endfor %}
   ```

#### 权限控制

1. 在 `settings.py` 文件尾部添加权限配置

   ```python
   # 使用集合提升匹配速度
   UNICOM_PERMISSION = {
      "leader": {"home", "order", "user", "user_list", "work"},
      "user": {"home", "work"}
   }
   ```

2. 配置`urls.py` 中路由的name值，通过name值来指代类似 `user/<int:nid>/edit/` 这样动态的url

   ```python
   urlpatterns = [
      path('admin/', admin.site.urls),
      path('login/', account.login, name="login"),
      path('logout/', account.logout, name="logout"),
      path('home/', account.home, name="home"),
      path('user/', user.user, name="user"),
      path('user/list/', user.user_list, name="user_list"),

      path('order/', order.order, name="order"),
      path('work/', work.work, name="work"),
   ]
   ```

3. 编辑中间件的 `process_view()` 方法
   在 `process_request()` 中做用户是否登录的校验；在 `process_view()` 中做用户权限的校验。如果没有权限就不会执行对应的视图函数，直接走 `process_response()` 返回。

   ```python
   from django.utils.deprecation import MiddlewareMixin
   from django.shortcuts import redirect, HttpResponse
   from django.conf import settings

   class AuthMiddleware(MiddlewareMixin):
      def process_request(self, req):
         # 0. 当请求路径为/login/时，进行放行
         if req.path_info in ["/login/", "/logout/"]:
               # 返回None，继续执行视图中的代码
               return
         # 1. 获取用户session信息
         user_info = req.session.get("user_info")
         # 2. 有值，表示已登录，则继续
         if user_info:
               # 获取session信息
               req.user_info = user_info
               req.userid = user_info["id"]
               req.username = user_info["username"]
               req.role = user_info["role"]
               return
         # 3. 没值，返回登录页面
         return redirect("/login/")
      
      def process_view(self, req, view_func, *args, **kwargs):
         # 0. 当请求路径为/login/或/logout/时，进行放行
         if req.path_info in ["/login/", "/logout/"]:
               # 返回None，继续执行视图中的代码
               return
         # 获取匹配到的请求对象中的url_name，url_name就是urls中配置的name值
         # print(req.resolver_match.url_name)
         # 1. 获取当前用户角色
         role = req.role
         # 2. 获取自己具备的权限
         user_permission_set= settings.UNICOM_PERMISSION[role]
         # 3. 判断是否具有权限
         if req.resolver_match.url_name in user_permission_set:
               return
         # 无权限
         return HttpResponse("无权访问")
   ```

### 业务部分

发起工单申请、审批

#### 表结构设计

用户表：id、用户名、密码、角色
模板表：id、申请类型、审批者
工单表：id、用户id、模板id、审批者、状态、创建时间、审批时间

```python
from django.db import models


class UserInfo(models.Model):
    role_choices = (('user', '员工'), ('leader', '领导'))
    role = models.CharField(verbose_name="角色", choices=role_choices, max_length=12)
    username = models.CharField(verbose_name="用户名", max_length=32)
    password = models.CharField(verbose_name="密码", max_length=64)

class Template(models.Model):
    tpl_type = models.CharField(verbose_name="类型", max_length=32)
    approver = models.ForeignKey(verbose_name="审批者", to="UserInfo", on_delete=models.CASCADE)

class Order(models.Model):
    sponsor = models.ForeignKey(verbose_name="发起者", to="UserInfo", on_delete=models.CASCADE, related_name="sponsor")
    tpl_type = models.ForeignKey(verbose_name="申请模板", to="Template", on_delete=models.CASCADE)
    approver = models.ForeignKey(verbose_name="审批者", to="UserInfo", on_delete=models.CASCADE, related_name="approver")
    status = models.SmallIntegerField(verbose_name="审批状态", choices=((0, "待审批"),(1, "已通过"),(2, "未通过"),(3, "已撤销"),))
    apply_time = models.DateTimeField(verbose_name="申请时间")
    approval_time = models.DateTimeField(verbose_name="审批时间", null=True, blank=True)
```

执行生效：

```shell
python manage.py makemigrations
python manage.py migrate 
```

#### 确认删除对话框

##### AJAX

AJAX（Asynchronous JavaScript and XML）是一种用于创建快速动态网页的技术，它通过在后台与服务器异步地交换数据，可以使网页实现部分更新而无需刷新整个页面。它的核心就是利用 JavaScript 和 XML（或者 JSON 等）来实现异步通信。
使用 AJAX 可以实现以下几个优点：

1. 提高用户体验：通过不刷新整个页面，可以快速响应用户请求，提升用户交互体验。
2. 减少网络带宽：前后端只需要交换需要更新的数据，可以大量减少数据传输量。
3. 增加系统性能：由于只更新部分页面，可以减轻服务器端的压力和运算量，提高系统响应速度和性能。
4. 改善代码结构：将前端和后端逻辑分离，增强了代码的可维护性和可扩展性。

在 Web 开发中，常见的 AJAX 库包括 jQuery、Fetch、Axios 等。一般来说，AJAX 的工作流程如下：

1. 用户在前端页面上触发某个事件，例如点击按钮或滚动鼠标。
2. 前端 JavaScript 代码捕捉到该事件，并向服务器端发送一个异步请求，请求数据或执行某些操作。
3. 服务器处理该请求，将需要返回的数据封装成指定格式（如 XML 或 JSON）发回给前端。
4. 前端 JavaScript 代码接收到服务器端的返回数据，并根据需求更新页面上特定部分的内容。

通过 AJAX 技术，Web 应用程序可以实现更多交互性和动态性。但是在使用 AJAX 技术时需要注意一些问题，例如跨域问题、安全性问题等。

##### AJAX 工作流程演示

当使用 AJAX 进行异步通信时，以下是 AJAX 的典型工作流程：

1. 绑定事件：在页面中，我们绑定一个事件，例如点击按钮，触发需要发送 AJAX 请求的操作。

   ```html
   <button onclick="showDelete(1)">删除</button>
   ```

2. 发起 AJAX 请求：通过 JavaScript 代码，创建一个 AJAX 请求对象，然后使用该对象发送异步请求到服务器。

   ```javascript
   function showDelete(id) {
      // 创建 AJAX 请求对象
      var xhr = new XMLHttpRequest();
   
      // 设置请求参数（请求方法、URL）
      var url = "/template/" + id + "/del";
      xhr.open("GET", url, true);
   
      // 注册回调函数来处理服务器响应
      xhr.onreadystatechange = function() {
         if (xhr.readyState === XMLHttpRequest.DONE) {
               if (xhr.status === 200) {
                  // 处理响应数据
                  var response = xhr.responseText;
                  console.log(response);
               } else {
                  console.error("发生错误：" + xhr.status);
               }
         }
      };
   
      // 发送请求
      xhr.send();
   }
   ```

3. 服务器处理请求：服务器接收到请求后，根据请求的 URL 和参数进行相应处理，例如从数据库中删除对应的模板。

   ```python
   from flask import Flask, request

   app = Flask(__name__)

   @app.route("/template/<int:template_id>/del", methods=["GET"])
   def delete_template(template_id):
      # 在这里编写删除模板的逻辑
      return "模板已成功删除"

   if __name__ == "__main__":
      app.run()
   ```

4. 服务器响应请求：服务器处理完请求后，将响应数据返回给前端。
5. 前端处理响应：在 AJAX 的回调函数中，根据服务器返回的响应数据进行相应的处理。这可以包括更新页面内容、显示提示信息或执行其他操作。

以上是基本的 AJAX 工作流程。使用 AJAX 可以在不刷新整个页面的情况下，通过异步通信与服务器交换数据，从而实现动态更新页面的效果，提高用户体验和系统性能。

jQuery中封装了ajax，因此要使用ajax需要先导入jQuery。
发送请求

```javascript
$ajax({
   url:"/template/del/",
   type:"GET",
   data:{nid:123}
})
/template/del/?nid=123
```

##### 错误提示（AJAX请求）

1. 视图的返回值中要带错误信息

   ```python
   from django.http import JsonResponse
   from utils.bootstrapFormStyle import BootStrapModelForm
   from datetime import datetime


   class OrderModelForm(BootStrapModelForm):
      class Meta:
         model = models.Order
         fields = ['tpl_type']

   def order_add(req):
      form = OrderModelForm(data=req.POST)
      if not form.is_valid():
         return JsonResponse({"status": False, "error": form.errors})
      
      template_obj = form.cleaned_data["tpl_type"]
      form.instance.sponsor_id = req.userid
      form.instance.approver_id = template_obj.approvor_id
      form.instance.apply_time = datetime.now()
      form.save()
      return JsonResponse({"status": True})
   ```

2. 页面发起AJAX请求

   ```html
   <script>
      function showAddModal() {
         $("#AddModal").modal("show");
         $(".error-message").empty();
      }
      function confirmAdd() {
         //1. 获取数据
         var data = $("#myForm").serialize();
         //2. 发送请求
         //2.1 清楚错误信息
         $(".error-message").empty();
         //2.2 发送请求
         $.ajax({
               url: "/order/add",
               type: "POST",
               data: data,
               dataType: "JSON",
               success: function (res) {
                  if (res.status) {
                     //location.href = location.href;
                     location.reload();
                  } else {
                     $.each(res.error, function (key, valueList) {
                           $("#id_" + key).next().text(valueList[0]);
                     })
                  }
               }
         })
      }
   </script>
   ```

3. 标签和错误提示位置要放一块

   ```html
   <div class="col-sm-10" style="position: relative;">
      {{ field }}
      <span class="error-message" style="color:red;position: absolute;"></span>
   </div>
   ```

#### 工单审批

1. 只审批 `"审批者" == "当前登录用户"` 的；
2. 显示字段：发起者、申请模板、申请时间、审批状态
3. 操作：通过/不通过（最好有确认弹窗），通过修改（待审核的，审批者是自己的）审批单的status的值来实现
4. 在前端页面进行判断，只显示已审批的数据
5. 在`card-header`里，显示待审批的数据的条数；添加排序，将未审批的数据显示在上面（可以根据状态排序）

### 文件上传

#### 依靠django框架实现文件上传

```html
<form action="post" enctype="multipart/form-data">
    {% csrf_token %}
    <input type="file" name="fs">
    <input type="submit" value="提 交">
</form>
```

```python
from django.core.files.uploadedfile import InMemoryUploadedFile
    

def up(req):
   """上传文件的视图函数"""
    if req.method == "GET":
        return render(req, "up.html")
    
    file_obj = req.FILES.get("fs")
    print(file_obj.name) # 获取文件名
    print(file_obj.size) # 获取文件大小
    with open(file_obj.name, mode="wb") as f:
        for chunk in file_obj.chunks():
            f.write(chunk)

    return HttpResponse("上传成功！")
```

项目开发中的静态资源：

1. static：开发程序所需的自己的静态文件
2. media：用户上传的（需要加配置）
   - settings.py 追加配置

      ```python
      import os
      MEDIA_ROOT = os.path.join(BASE_DIR, "media")
      MEDIA_URL = "/media/"
      ```

   - urls.py 添加路由

      ```python
      from django.views.static import serve
      from django.urls import re_path
      from django.conf import settings

      urlpatterns = [
         path('admin/', admin.site.urls),
         re_path(r"^media/(?P<path>.*)$", serve, {"document_root":settings.MEDIA_ROOT}, name="media"),
      ]
      ```

#### 依靠ModelForm实现文件上传

1. models.py

   ```python
   class Info(models.Model):
      name = models.CharField(verbose_name="姓名", max_length=32)
      avatar = models.FileField(verbose_name="头像", upload_to="path/to/uploaddir/")
   ```

2. up.py

   ```python
   from django.db import models
   from django import forms


   class UpModelForm(forms.ModelForm):
      class Meta:
         model = models.Info
         fields = "__all__"


   def up_form(req):
      if req.method == "GET":
         form = UpModelForm()
         return render(req, "up.html", locals())
      
      form = UpModelForm(data=req.POST, files=req.FILES)
      if not form.is_valid():
         return render(req, "up.html", {"form": form})
      
      form.save()
      return HttpResponse("上传成功！")
   ```

3. up.html

   ```html
   <form action="post" enctype="multipart/form-data">
      {% csrf_token %}
      {% for i in form %}
         {{ i }}
      {% endfor %}
      <input type="submit" value="提 交">
   </form>
   ```

#### 上传Excel + 读取

```python
from openpyxl import load_workbook


def up_excel(req):
    if req.method == "GET":
        return render(req, "up_excel.html")
    file_obj = req.FILES.get("fs")
    wb = load_workbook(file_obj)
    sheet = wb.worksheets[0]
    for row in sheet.iter_rows():
        print(row[0].value, row[1].value)
        models.Info.objects.create(name=row[0].value, avatar=row[1].value)
    return HttpResponse("测试")
```

```html
<form action="post" enctype="multipart/form-data">
    {% csrf_token %}
    <input type="file" name="fs">
    <input type="submit" value="提 交">
</form>
```

## 爬虫开发

1. web爬虫，模拟浏览器发送请求获取数据
2. js逆向，网站内部集成算法，要去该网站找到算法位置，进行算法还原
3. app爬虫
4. app逆向

### web爬虫案例（一般在headers中添加"User-Agent"）

1. 发送请求获取网页解析HTML

   ```python
   import requests
   from bs4 import BeautifulSoup
   ```

2. 发送请求获取JSON数据

### JS逆向

1. URL
2. 方式：POST/GET...
3. 通过无痕获取请求体
4. 通过无痕获取cookie
5. 获取方式：1. 通过关键字搜素对应文件，一般是js文件，然后在文件中搜索关键字，寻找设置该值的代码

### app爬虫

1. 抓包工具（Charles）
2. 手机模拟器（mumu，安装对应app进行抓包）
3. 然后用代码去还原和模拟请求

### app逆向

1. 使用jadx工具对手机app的apk包进行反编译，得到源代码。
2. 如密码加密算法，从调用密码的部分一点点通过关键字找到密码是如何生成的。
3. 然后进行还原模拟请求。

## DRF框架

### 前后端分离

前后端分离（Frontend-Backend Separation）是一种软件架构模式，其中前端（即用户界面）和后端（即应用逻辑和数据处理）被分开开发和部署。在前后端分离的架构中，前端和后端是独立的系统，彼此通过API进行通信。
Django 框架的前后端分离：

1. 后端开发：
   - 使用 Django 框架开发后端应用，包括定义模型、视图、路由、表单等。
   - 在视图中，使用 Django 定义的方法处理请求和生成响应，可以将数据从数据库中检索出来，进行业务逻辑处理，并将结果返回给前端。
2. 前端开发：
   - 使用任何前端框架（如React、Vue.js、Angular等）或纯前端技术（如HTML、CSS、JavaScript）开发前端界面。
   - 前端通过API与后端通信，发送HTTP请求（通常是`AJAX`请求）获取数据或向后端发送数据。
   - 前端通过接收到的数据更新页面内容，交互等。
3. 如何实现前后端交互：
   - 后端：使用 Django 的 REST framework（如Django REST framework）构建基于RESTful原则的API，将数据以JSON格式返回给前端。
   - 前端：使用前端框架或者JavaScript库（如Axios、Fetch等）进行HTTP请求，获取后端API的数据，并将数据进行渲染和展示。
4. 优势：
   - 前后端分离允许前端和后端团队并行开发，提高开发效率。
   - 支持多平台，可以在不同的设备上使用相同的后端API提供服务。
   - 前后端松耦合，使得后端的变更不会直接影响前端代码。
需要注意的是，在前后端分离的架构中，前端和后端需要明确共同约定好API的数据格式，接口的调用方式等。
总结起来，前后端分离是通过将前端和后端分开开发，通过API进行通信的一种架构模式。这种模式带来了灵活性、可扩展性和团队协作的好处。在 Django 中，可以使用 Django REST framework 来构建强大的后端API，同时与任何前端技术栈进行交互。

### DRF 简介

DRF是Django REST framework的缩写，是一个基于Django框架的强大且灵活的工具包，用于构建Web API。它提供了许多开箱即用的功能和工具，帮助开发者更轻松地创建和管理RESTful API。

以下是DRF的一些主要特点和功能：

1. 序列化（Serialization）：DRF提供了序列化器（Serializer），可以将Django模型实例转换为JSON等格式，并且可以反序列化请求数据生成模型实例。
2. 视图（Views）：DRF提供了多种视图类，用于处理API请求和生成API响应。例如，使用基于类的视图（Class-based views）可以定义GET、POST、PUT、DELETE等HTTP请求方法的处理逻辑。
3. 路由（Routing）：DRF允许通过路由配置将URL映射到相应的视图。可以使用默认的路由类或自定义路由类来定义API的URL结构。
4. 认证和权限（Authentication & Permissions）：DRF提供了易于配置和使用的认证和权限类，用于保护API端点的安全性。可以选择各种认证方案（如Token认证、基于Session的认证、OAuth等）并设置相应的权限级别和访问控制。
5. 响应（Response）：DRF提供了统一的响应类，使得API的返回结果能够一致地包装为JSON数据，同时支持内容协商（Content Negotiation）来处理不同的请求格式，如JSON、XML等。
6. 分页（Pagination）：DRF可以处理大量数据的分页，并提供了各种内置分页器（Paginator），例如基于页数的分页和基于游标的分页。
7. 过滤（Filtering）和搜索（Searching）：DRF支持通过查询字符串进行过滤和搜索。可以轻松配置过滤器和搜索字段，以便在API中进行快速和灵活的数据筛选和搜索。
8. 规范化错误处理（Error Handling）：DRF提供了一致且可扩展的异常处理机制，可以捕获和处理请求过程中出现的各种错误，并以规范的方式返回给客户端。

DRF是一个功能强大而受欢迎的工具，可以帮助开发人员构建高效、安全和可扩展的RESTful API。它与Django紧密集成，提供了许多有用的功能，简化了API的构建和管理过程。无论是构建小型项目还是大型企业级应用，DRF都是一个不错的选择。

### DRF 使用

1. 创建项目目录
2. 创建虚拟环境 `python -m venv .venv`
3. 激活虚拟环境 `.\.venv\Scripts\activate`
4. 安装依赖包 `pip install django djangorestframework`
5. 创建新项目 `django-admin startproject drf_example`
6. 创建新应用 `cd .\drf_example\` `python .\manage.py startapp api`
7. `djangorestframework` 本质是一个app，因此如果需要使用，要把它注册进 `settings.py`

   ```python
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'rest_framework',
      'api.apps.ApiConfig',
   ]
   ```

8. 编辑视图函数

   ```python
   # urls.py
   from api import views

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('login/', views.login),
      path('info/', views.InfoView.as_view()),
      path('auth/', views.auth),  # FBV
      path('user/', views.UserView.as_view()),  # CBV
   ]
   ```

   ```python
   from django.http import JsonResponse
   from django.views import View   
   from rest_framework.response import Response
   from rest_framework.decorators import api_view
   from rest_framework.views import APIView


   # django的FBV（以函数的方式实现）
   def auth(request):
      return JsonResponse({'status': True, 'message': "auth"})


   # django的CBV（以类的方式实现（主要））
   class UserView(View):
      def get(self, req):
         return JsonResponse({'status': True, 'message': "get"})

      def post(self, req):
         return JsonResponse({'status': True, 'message': "post"})

      def put(self, req):
         return JsonResponse({'status': True, 'message': "put"})

      def delete(self, req):
         return JsonResponse({'status': True, 'message': "delete"})

   # DRF的FBV
   @api_view(["GET"])
   def login(req):
      return Response({'status': True, 'message': "login"})


   # DRF的CBV（主要）
   class InfoView(APIView):
      def get(self, req, version, pid):
         print(req.user)  # 当前登录的用户 -> 匿名用户
         print(req.auth)  # 用于验证身份信息
         print(version, pid)  # 返回参数
         print(self.kwargs)  # 返回字典
         print(self.args)  # 返回元组
         return Response({'status': True, 'message': "info"})
   ```

### FBV 和 CBV

在Django中，FBV（Function-Based Views）和CBV（Class-Based Views）是两种常见的视图开发方式。

1. FBV（Function-Based Views）：
   - FBV是一种基于函数的视图开发方式。每个视图都是一个独立的函数，接收请求对象作为参数，并返回响应对象。
   - 通过使用装饰器（如`@csrf_exempt`）可以为函数视图添加额外的功能，如跨站请求伪造（CSRF）保护的禁用。
   - 使用条件语句或多个URL模式可以实现视图处理不同类型的HTTP请求（如GET、POST、PUT等）。
   - 具有较低的学习曲线，适合简单的视图和快速原型开发。

   ```python
   from django.http import HttpResponse

   def hello(request):
      if request.method == 'GET':
         return HttpResponse("Hello, World!")

   def greet(request, name):
      if request.method == 'GET':
         return HttpResponse(f"Hello, {name}!")
   ```

2. CBV（Class-Based Views）：
   - CBV是一种基于类的视图开发方式。每个视图都是一个继承自Django提供的基础视图类的子类，通过重写类方法来定义视图的行为。
   - 提供了许多内置的类方法（如`get()`、`post()`、`put()`等）来处理不同类型的HTTP请求。
   - 通过继承和重写类方法，可以实现视图的复用和更好的组织代码结构。
   - 提供了许多内置的混合类（Mixin），可以在不同视图之间共享功能和行为。

   ```python
   from django.views import View
   from django.http import HttpResponse

   class HelloView(View):
      def get(self, request):
         return HttpResponse("Hello, World!")

   class GreetView(View):
      def get(self, request, name):
         return HttpResponse(f"Hello, {name}!")
   ```

3. 路由配置

   ```python
   from api import views

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('hello1/', views.hello),  # FBV
      path('greet1/', views.greet),
      path('hello2/', views.HelloView.as_view()),  # CBV
      path('greet2/', views.GreetView.as_view()),
   ]
   ```

CBV提供了更大的灵活性和可扩展性，适用于复杂的视图逻辑和需要共享功能的场景。它们可以通过继承和混合类的使用来减少代码重复，并且具有更好的可读性和结构性。

**注意**：测试接口时，url要以`/`结尾，并且要把django的csrf先关闭（注释掉），否则，POST、PUT、DELETE方法无法获取json数据。

CBV（Class-Based Views）是Django中一种基于类的视图开发方式。每个视图都是一个继承自Django提供的基础视图类的子类，通过重写类方法来定义视图的行为。

1. 类结构：
   - CBV中的视图类通常继承自Django提供的基础视图类，如`django.views.View`、`django.views.generic.base.TemplateView`等。
   - 这些基础视图类提供了一些默认的实现和常用的方法，可以被子类继承和重写。
2. 类方法：
   - CBV中的类方法对应于不同类型的HTTP请求，如`get()`、`post()`、`put()`等。
   - 可以通过重写这些方法来定义视图的处理逻辑。
   - 类方法接收两个参数：`self`表示当前视图实例，`request`表示当前的HTTP请求对象。
3. 视图类的处理逻辑：
   - CBV通过重写类方法来定义视图的处理逻辑。
   - 在类方法中可以执行与请求相关的操作，如访问数据库、执行业务逻辑等。
   - 最后，返回一个HttpResponse对象作为响应。
4. 内置的混合类（Mixin）：
   - 混合类是一种特殊的类，提供了一些可重用的功能和行为。
   - Django提供了许多内置的混合类，如`LoginRequiredMixin`、`PermissionRequiredMixin`等，用于在视图中添加身份验证、权限控制等功能。
   - 可以通过多继承来将混合类添加到视图类中，以实现特定功能的复用。

   ```python
   from django.views import View
   from django.http import HttpResponse
   from django.shortcuts import render

   class HomeView(View):
      def get(self, request):
         return HttpResponse("Welcome to the homepage!")

   class AboutView(View):
      def get(self, request):
         return render(request, 'about.html', {'message': 'This is the about page.'})

   class ContactView(View):
      def get(self, request):
         return render(request, 'contact.html')

      def post(self, request):
         name = request.POST.get('name')
         email = request.POST.get('email')
         # 处理表单数据并执行其他业务逻辑
         return HttpResponse("Thank you for contacting us!")
   ```

     - `HomeView`、`AboutView`和`ContactView`分别继承自`View`，并重写了`get()`或`post()`方法来定义处理逻辑。
     - `HomeView`的`get()`方法直接返回一个包含欢迎消息的HttpResponse对象。
     - `AboutView`的`get()`方法渲染了一个模板，并将上下文数据传递给模板。
     - `ContactView`的`get()`方法渲染了一个包含表单的模板，`post()`方法接收表单数据并做出相应处理。

CBV具有以下优点：

- 提供了更丰富的功能和灵活性，适用于复杂的视图逻辑和需要共享功能的场景。
- 通过继承和重写类方法，可以减少代码重复并实现更好的组织代码结构。
- 内置的混合类提供了可重用的功能，可以简化开发过程。

总体而言，CBV是Django中推荐使用的视图开发方式。然而，对于简单的视图和快速原型开发，FBV（Function-Based Views）也是一个不错的选择。根据项目的需求和复杂性，你可以选择适合的视图开发方式。

当使用CBV（Class-Based Views）时，Django的执行过程：

1. URL 匹配：
   - Django首先通过URL配置文件（urls.py）中的正则表达式来匹配用户请求的URL。
   - 当匹配到URL时，Django会将请求传递给对应的视图函数或视图类。
2. 视图类实例化：
   - 如果URL配置中指定了一个视图类作为处理请求的目标，Django首先会实例化这个视图类。
   - Django会调用视图类的构造函数，并传入与请求相关的参数，如request对象等。
3. 请求方法处理：
   - Django根据HTTP请求方法（GET、POST、PUT等）调用视图类中对应的方法（如get()、post()、put()）。
   - 如果视图类没有实现与请求方法对应的方法，Django会抛出一个适当的异常。
4. 中间件处理：
   - 在调用视图类方法之前和之后，Django会检查是否定义了中间件（Middleware）。
   - 中间件可以在请求处理的不同阶段进行预处理或后处理操作，例如身份验证、请求日志记录等。
   - Django按照中间件的顺序依次调用每个中间件的process_request()、process_view()、process_exception()和process_response()等方法。
5. CBV方法执行：
   - Django调用匹配到的视图类中对应的方法来处理请求。
   - 视图类方法接收两个参数：self（表示视图类实例本身）和request对象（表示当前的HTTP请求对象）。
   - 在方法中执行与请求相关的操作，例如访问数据库、执行业务逻辑等。
6. 返回响应：
   - 视图类方法处理完请求后，需要返回一个HttpResponse对象作为响应。
   - HttpResponse对象包含要在客户端显示的内容，如HTML模板渲染结果、JSON数据等。
   - Django会将HttpResponse对象发送回客户端，并根据需要进行进一步处理和渲染。

在实际开发中，还可能涉及更多细节，如模板渲染、URL反向解析等。通过使用CBV，可以更好地组织代码、提高代码复用性，并在开发过程中使用内置的混合类来简化开发任务。

视图函数加上装饰器 `@csrf_exempt` 可以免除`csrf`校验。

### django的CBV 和 DRF的CBV

1. 使用的模块不同
   - django的CBV `from django.views import View`，调用时要继承 `View` 类
   - DRF的CBV `from rest_framework.views import APIView` 调用时要继承 `APIView` 类
2. 本质上，`APIView` 又继承了 `View`，是对它功能的补充。且二者都定义了 `as_view()` 函数。`View` 源码：

   ```python
   class View:
      # 定义了一个http_method_names属性，包含了常见的HTTP请求方法（如GET、POST、PUT等）。
      http_method_names = [
         "get",
         "post",
         "put",
         "patch",
         "delete",
         "head",
         "options",
         "trace",
      ]

      # 定义了一个构造函数__init__()，用于初始化视图类实例。在构造函数中，通过遍历关键字参数（kwargs），将参数名和对应的值保存到视图类实例中。
      def __init__(self, **kwargs):
         for key, value in kwargs.items():
            setattr(self, key, value)

      # view_is_async是一个类属性（classproperty），用于判断视图类中的处理方法是否是异步的。它通过检查视图类中定义的各个HTTP处理方法，判断是否有异步处理的方法（coroutine function）。如果存在异步方法，则要求所有的处理方法要么都是同步的，要么都是异步的，否则会抛出异常。
      @classproperty
      def view_is_async(cls):
         handlers = [
            getattr(cls, method)
            for method in cls.http_method_names
            if (method != "options" and hasattr(cls, method))
         ]
         if not handlers:
            return False
         is_async = iscoroutinefunction(handlers[0])
         if not all(iscoroutinefunction(h) == is_async for h in handlers[1:]):
            raise ImproperlyConfigured(
                  f"{cls.__qualname__} HTTP handlers must either be all sync or all "
                  "async."
            )
         return is_async

      # as_view是一个类方法（classonlymethod），作为请求-响应处理的入口点。它接受一系列的初始化参数（initkwargs），并返回一个可调用对象（view函数）。
      @classonlymethod
      def as_view(cls, **initkwargs):
         # 对传入的初始化参数进行处理和校验。
         for key in initkwargs:
            if key in cls.http_method_names:
                  raise TypeError(
                     "The method name %s is not accepted as a keyword argument "
                     "to %s()." % (key, cls.__name__)
                  )
            if not hasattr(cls, key):
                  raise TypeError(
                     "%s() received an invalid keyword %r. as_view "
                     "only accepts arguments that are already "
                     "attributes of the class." % (cls.__name__, key)
                  )

         # 定义一个嵌套函数view，用于处理请求。
         # 在view函数中，首先创建了当前视图类的实例（self），并调用setup()方法对实例进行设置。如果实例没有request属性，会抛出异常。
         def view(request, *args, **kwargs):
            self = cls(**initkwargs)
            self.setup(request, *args, **kwargs)
            if not hasattr(self, "request"):
                  raise AttributeError(
                     "%s instance has no 'request' attribute. Did you override "
                     "setup() and forget to call super()?" % cls.__name__
                  )
            # 调用实例的dispatch()方法来处理请求，并将处理结果返回。
            return self.dispatch(request, *args, **kwargs)
         
         # view函数的一些元数据（如类名、文档字符串、模块名等）以及相关属性从视图类中继承和设置。
         view.view_class = cls
         view.view_initkwargs = initkwargs

         view.__doc__ = cls.__doc__
         view.__module__ = cls.__module__
         view.__annotations__ = cls.dispatch.__annotations__
         view.__dict__.update(cls.dispatch.__dict__)

         # 如果视图类是异步的，通过markcoroutinefunction标记view函数为异步函数。
         if cls.view_is_async:
            markcoroutinefunction(view)

         return view
   
         # 初始化视图方法共享的属性。
         def setup(self, request, *args, **kwargs):
            # 检查视图类中是否定义了get方法，并且没有定义head方法。如果满足这个条件，则将self.get方法赋值给self.head，以便在后续处理中使用。
            if hasattr(self, "get") and not hasattr(self, "head"):
                  self.head = self.get
            # 传入的请求(request)、位置参数(args)和关键字参数(kwargs)分别存储在self.request、self.args和self.kwargs属性中。
            self.request = request
            self.args = args
            self.kwargs = kwargs

         # 根据请求的方法分发到相应的处理方法进行处理。
         def dispatch(self, request, *args, **kwargs):
            # 检查请求方法(request.method)是否在允许的HTTP方法列表(http_method_names)中。
            # 如果是，则获取对应的处理方法(handler method)。通过getattr()函数，从当前视图对象中动态地获取对应的方法，并赋值给handler变量。
            if request.method.lower() in self.http_method_names:
                  handler = getattr(
                     self, request.method.lower(), self.http_method_not_allowed
                  )
            # 如果请求方法不存在于视图对象中，则获取self.http_method_not_allowed方法（错误处理方法）并赋值给handler变量。
            else:
                  handler = self.http_method_not_allowed
            # 调用获取到的处理方法handler(request, *args, **kwargs)来处理请求，并返回处理结果。
            return handler(request, *args, **kwargs)
   ```

### DRF 的 request

#### 类中的 `__getattr__()` 和 `__getattribute__()`

`__getattr__()`和`__getattribute__()`是Python中的特殊方法（也称为魔术方法），用于访问对象的属性。它们被用于不同的目的，并在类定义中具有不同的行为。

1. `__getattr__(self, name)`：
   - 当访问一个对象的属性时，如果找不到该属性，则会调用`__getattr__()`方法。
   - `__getattr__()`接受一个参数`name`，表示要访问的属性名称。
   - 可以在`__getattr__()`中实现自定义的处理逻辑，例如返回默认值、对不存在的属性进行惰性加载等。
   - 如果在`__getattr__()`中无法找到属性并且没有提供默认行为，则会抛出`AttributeError`异常。
2. `__getattribute__(self, name)`：
   - 当访问一个对象的属性时，不论该属性是否存在，都会调用`__getattribute__()`方法。
   - `__getattribute__()`接受两个参数：`self`表示实例本身，`name`表示要访问的属性名称。
   - 可以在`__getattribute__()`中实现自定义的处理逻辑，例如记录日志、检查权限、返回动态计算的属性值等。
   - 在`__getattribute__()`中如果要获取同一个属性的值，需要使用`super().__getattribute__(name)`以避免无限递归。
   - 如果在`__getattribute__()`中无法找到属性并且没有提供默认行为，则会抛出`AttributeError`异常。

注意：

- `__getattr__()`是在查找不到属性时才会被调用，而`__getattribute__()`是无条件地被调用。
- 当两个方法同时存在于同一个类中时，`__getattr__()`的优先级比`__getattribute__()`低。
- 如果要在`__getattribute__()`中访问同一个属性的值，应使用`super().__getattribute__(name)`以避免无限递归。

```python
class Example:
    def __init__(self):
        self.attribute = 42

    def __getattr__(self, name):
        if name == 'default_attribute':
            return 'default value'
        else:
            raise AttributeError(f'Attribute "{name}" not found')

    def __getattribute__(self, name):
        print(f'Accessing attribute: {name}')
        return super().__getattribute__(name)


obj = Example()
print(obj.unknown_attribute)  # 调用 __getattr__()，输出: default value
print(obj.attribute)  # 调用 __getattribute__()，输出: Accessing attribute: attribute; 42
```

当访问`obj.unknown_attribute`时，由于该属性不存在，会调用`__getattr__()`方法并返回默认值。而当访问`obj.attribute`时，会首先调用`__getattribute__()`方法，在打印日志后返回属性的实际值。

#### request.user

DRF对`request.user`进行了一些处理，以提供更加便捷的用户身份验证和授权功能。下面是一些DRF对`request.user`的处理：

1. **身份验证**：DRF提供了多种身份验证方式，例如Token认证、Session认证、OAuth2认证等。当请求到达时，DRF会根据配置的身份验证方式，自动对请求进行身份验证，并将验证后的用户对象存储在`request.user`属性中。
2. **权限控制**：DRF允许开发者在视图类或视图函数中定义权限，限制特定用户对API的访问。当用户尝试访问需要特定权限的API时，DRF会检查用户的权限并做出相应的响应。这些权限可以通过`request.user`来判断当前用户是否具有访问权限。
3. **扩展用户模型**：DRF允许开发者通过继承或扩展Django的用户模型（如`AbstractUser`）来定义自己的用户模型，并在`request.user`中使用该自定义用户模型。
4. **上下文处理器**：DRF允许开发者自定义上下文处理器，用于在请求过程中对`request.user`进行进一步处理。上下文处理器可以添加额外的信息到`request.user`中，使其更加丰富和有用。
5. **Serializer中的用户字段**：在Serializer中，可以使用`User`字段来表示当前请求的用户。`User`字段会自动将`request.user`中的用户对象序列化为适当的表示形式，并在反序列化时将用户表示转换为用户对象。
注意：DRF对`request.user`的处理是与Django框架密切相关的，因为DRF是建立在Django之上的。因此，一些有关身份验证和权限控制的默认行为是继承自Django的，而DRF则提供了更高级的抽象和扩展功能来满足Web API的需求。

追加配置 `settings.py`：

```python
REST_FRAMEWORK = {
    "UNAUTHENTICATED_USER": None
}
```

在DRF中，`UNAUTHENTICATED_USER`选项是用来指定未经身份验证的用户的占位符。当请求不包含有效的身份验证信息时，DRF会将`request.user`设置为该占位符。如果不进行配置，则默认情况下，DRF将使用`django.contrib.auth.models.AnonymousUser`作为占位符。
`django.contrib.auth.models.AnonymousUser`是Django自带的一个模型类，用于表示未经身份验证的用户。它拥有与普通用户相似的方法和属性，但它并没有在数据库中对应的记录，因此无法被认证和授权。
然而，在某些情况下，将`request.user`设置为`AnonymousUser`可能会导致意料之外的行为。例如，定义了一个验证请求是否包含特定头部信息的自定义身份验证器，希望在请求中缺少这些头部信息时，将`request.user`设置为`None`。如果设置为`AnonymousUser`，这可能会使身份验证逻辑混淆。
因此，在这种情况下，可以将`UNAUTHENTICATED_USER`选项设置为`None`，以便在没有有效身份验证信息时，将`request.user`设置为`None`。这样，就可以在视图中轻松地检查`request.user`是否为`None`，从而区分已验证和未验证的用户。

`req.auth` 和 `req.user` 在DRF中承担不同的角色：

1. `req.auth`：用于身份验证信息
   - `req.auth` 提供了有关请求是否经过身份验证以及身份验证方法的详细信息。
   - 它返回与请求相关联的身份验证实例，该实例包含有关身份验证的相关信息，如身份验证方法、认证用户等。
   - 如果请求未经过身份验证或身份验证失败，`req.auth` 将为 `None`。
2. `req.user`：当前登录的用户
   - `req.user` 是一个属性，表示当前登录的用户对象。
   - 当请求通过身份验证并成功验证身份时，`req.user` 将返回与身份验证相关联的用户对象。
   - 如果请求未经过身份验证或身份验证失败，`req.user` 将为匿名用户对象（`AnonymousUser`）。

总结：

- `req.auth` 提供有关请求的身份验证信息，例如身份验证方法。
- `req.user` 表示当前登录的用户对象。

#### request 对象

`DRF` 源码：

```python
class APIView(View):
   # 定义一些变量来存储默认的渲染器、解析器、身份验证类、限流类等设置。这些设置可以在全局范围或每个视图中进行设置。
   renderer_classes = api_settings.DEFAULT_RENDERER_CLASSES
   parser_classes = api_settings.DEFAULT_PARSER_CLASSES
   authentication_classes = api_settings.DEFAULT_AUTHENTICATION_CLASSES
   throttle_classes = api_settings.DEFAULT_THROTTLE_CLASSES
   permission_classes = api_settings.DEFAULT_PERMISSION_CLASSES
   content_negotiation_class = api_settings.DEFAULT_CONTENT_NEGOTIATION_CLASS
   metadata_class = api_settings.DEFAULT_METADATA_CLASS
   versioning_class = api_settings.DEFAULT_VERSIONING_CLASS

   # 定义一个类属性settings，用于存储API的设置。该属性引用了一个名为api_settings的变量，这个变量是开发者定义的API设置。
   settings = api_settings

   # 定义了一个类属性schema，用于存储API的模式（schema）。默认情况下，使用的是一个名为DefaultSchema的模式。
   schema = DefaultSchema()

   # 定义了一个类方法as_view()，用于将视图类转换为可调用对象（view函数）。
   @classmethod
   def as_view(cls, **initkwargs):
      # 首先检查视图类是否定义了queryset属性并且queryset是一个models.query.QuerySet类型的实例。
      # 如果是这样，那么定义了一个内部函数force_evaluation()，用于在直接访问.queryset属性时抛出异常。因为直接访问.queryset属性会导致查询结果被缓存和重用，而不是在每个请求中再次查询数据库。
      if isinstance(getattr(cls, 'queryset', None), models.query.QuerySet):
         def force_evaluation():
               raise RuntimeError(
                  'Do not evaluate the `.queryset` attribute directly, '
                  'as the result will be cached and reused between requests. '
                  'Use `.all()` or call `.get_queryset()` instead.'
               )
         cls.queryset._fetch_all = force_evaluation

      # 使用super().as_view(**initkwargs)调用父类的as_view()方法，将初始化参数传递给父类方法，并获取返回的视图函数（view）。
      view = super().as_view(**initkwargs)
      # 将视图类的引用存储在视图函数的cls属性中，并将初始化参数存储在initkwargs属性中。这样可以在URL反向解析时获取视图类的信息，用于生成面包屑导航等功能。
      view.cls = cls
      view.initkwargs = initkwargs

      # 使用csrf_exempt(view)装饰器将视图函数标记为免除CSRF验证。
      return csrf_exempt(view)
      # 注意，基于会话的身份验证（session based authentication）是需要进行CSRF验证的，其他身份验证方法则免除CSRF验证。

   # 用于处理请求的分发和异常处理。
   def dispatch(self, request, *args, **kwargs):
      # 将传入的请求(request)、位置参数(args)和关键字参数(kwargs)存储在self.args和self.kwargs属性中。
      self.args = args
      self.kwargs = kwargs
      # 调用self.initialize_request(request, *args, **kwargs)方法对请求进行初始化，并将返回的初始化后的请求对象重新赋值给request变量。
      request = self.initialize_request(request, *args, **kwargs)
      # 将request对象存储在self.request属性中，并将self.default_response_headers属性的值赋值给self.headers属性（此行代码可能已过时，可能不再使用）。
      self.request = request
      self.headers = self.default_response_headers  # deprecate?

      # 使用try-except语句块，捕获可能出现的异常。
      try:
         # 调用self.initial(request, *args, **kwargs)方法来进行请求的初始化工作。
         self.initial(request, *args, **kwargs)
         # 根据请求方法（request.method）获取相应的处理方法（handler method）。
         # 如果请求方法在允许的HTTP方法列表(http_method_names)中，则获取对应的方法，并赋值给handler变量；
         if request.method.lower() in self.http_method_names:
               handler = getattr(self, request.method.lower(), self.http_method_not_allowed)
         # 否则，使用self.http_method_not_allowed方法作为处理方法。
         else:
               handler = self.http_method_not_allowed

         # 调用处理方法handler(request, *args, **kwargs)来处理请求，并将返回的响应(response)赋值给response变量。
         response = handler(request, *args, **kwargs)

      # 捕获任何异常并将其赋值给exc变量。然后，调用self.handle_exception(exc)方法处理异常，并将返回的响应赋值给response变量。
      except Exception as exc:
         response = self.handle_exception(exc)

      # 调用self.finalize_response(request, response, *args, **kwargs)方法对响应进行最终处理，并将最终的响应赋值给self.response属性。
      self.response = self.finalize_response(request, response, *args, **kwargs)
      # 返回self.response作为视图函数的结果，完成请求的处理和响应的返回。
      return self.response

   def initialize_request(self, request, *args, **kwargs):
      # 该方法用于返回初始的请求对象。
      # 通过调用 self.get_parser_context(request) 获取解析器上下文。
      parser_context = self.get_parser_context(request)
      # 创建一个 Request 对象，并传入以下参数：
      return Request(
            # request：原始的 Django 请求对象。
            request,
            # parsers：通过调用 self.get_parsers() 获取的解析器列表。
            parsers=self.get_parsers(),
            # authenticators：通过调用 self.get_authenticators() 获取的身份验证器列表。
            authenticators=self.get_authenticators(),
            # negotiator：通过调用 self.get_content_negotiator() 获取的内容协商器。
            negotiator=self.get_content_negotiator(),
            # parser_context：通过前面获取的解析器上下文。
            parser_context=parser_context
      )

   def initial(self, request, *args, **kwargs):
      # 该方法在调用方法处理程序之前运行需要进行的任何操作。
      # 设置 self.format_kwarg 属性为通过调用 self.get_format_suffix(**kwargs) 获取的格式后缀。
      self.format_kwarg = self.get_format_suffix(**kwargs)

      # 调用 self.perform_content_negotiation(request) 执行内容协商，并将协商结果存储在请求对象中。协商结果包括了渲染器和媒体类型。
      neg = self.perform_content_negotiation(request)
      request.accepted_renderer, request.accepted_media_type = neg

      # 调用 self.determine_version(request, *args, **kwargs) 确定 API 版本，如果使用了版本控制。
      # determine_version 方法返回一个元组，包含版本号和版本控制方案。
      version, scheme = self.determine_version(request, *args, **kwargs)
      # 将版本号和版本控制方案存储在请求对象的 version 和 versioning_scheme 属性中。
      request.version, request.versioning_scheme = version, scheme

      # 调用 self.perform_authentication(request) 执行身份验证。
      self.perform_authentication(request)
      # 调用 self.check_permissions(request) 检查权限。
      self.check_permissions(request)
      # 调用 self.check_throttles(request) 检查流量控制。
      self.check_throttles(request)
```

```python
class Request:
   def __init__(self, request, parsers=None, authenticators=None,
               negotiator=None, parser_context=None):
      assert isinstance(request, HttpRequest), (
         'The `request` argument must be an instance of '
         '`django.http.HttpRequest`, not `{}.{}`.'
         .format(request.__class__.__module__, request.__class__.__name__)
      )

      self._request = request
      self.parsers = parsers or ()
      self.authenticators = authenticators or ()
      self.negotiator = negotiator or self._default_negotiator()
      self.parser_context = parser_context
      self._data = Empty
      self._files = Empty
      self._full_data = Empty
      self._content_type = Empty
      self._stream = Empty

      if self.parser_context is None:
         self.parser_context = {}
      self.parser_context['request'] = self
      self.parser_context['encoding'] = request.encoding or settings.DEFAULT_CHARSET

      force_user = getattr(request, '_force_auth_user', None)
      force_token = getattr(request, '_force_auth_token', None)
      if force_user is not None or force_token is not None:
         forced_auth = ForcedAuthentication(force_user, force_token)
         self.authenticators = (forced_auth,)


   def __getattr__(self, attr):
      try:
         return getattr(self._request, attr)
      except AttributeError:
         return self.__getattribute__(attr)
```

1. 说明：
   - 这段代码定义了一个名为 `Request` 的类，它是对 Django 中 `HttpRequest` 实例的增强包装器。
   - 在初始化方法 `__init__()` 中，接收以下参数：
     - `request`：原始的 `HttpRequest` 实例。
     - `parsers`：用于解析请求内容的解析器列表或元组。
     - `authenticators`：尝试对请求的用户进行身份验证的身份验证器列表或元组。
     - `negotiator`：协商器，用于内容协商。
     - `parser_context`：解析器上下文，用于配置解析器的行为。
   - 在初始化方法中，首先进行了参数验证，确保传入的 `request` 参数是有效的 `HttpRequest` 实例。
   - 然后，将传入的参数分别保存到类的实例变量中：
     - `self._request`：原始的 `HttpRequest` 实例。
     - `self.parsers`：用于解析请求内容的解析器列表，默认为空元组。
     - `self.authenticators`：用于尝试身份验证的身份验证器列表，默认为空元组。
     - `self.negotiator`：用于内容协商的协商器，默认为 `_default_negotiator()` 方法返回的默认协商器。
     - `self.parser_context`：解析器上下文，默认为空字典。如果未传递，则会创建一个空字典并将其保存在该变量中。同时，还将当前的请求对象和编码设置保存在该字典中。
   - 接下来，根据是否存在 `force_user` 或 `force_token` 属性，决定是否使用强制身份验证器。如果存在 `force_user` 或 `force_token` 属性，则创建一个 `ForcedAuthentication` 实例，并将其添加到 `self.authenticators` 中。
   - 最后，代码定义了 `__getattr__()` 方法，用于在当前实例没有指定属性时，尝试将该属性代理到底层的 `HttpRequest` 对象上。
   - 通过这个 `Request` 类的实例，可以对原始的 `HttpRequest` 进行额外的处理和功能扩展，例如自定义解析器、身份验证器等。
2. request封装
   - `View` 中直接使用 `request`
   - `APIView` 在 `dispatch` 函数中对 `request` 进行了封装 `request = self.initialize_request(request, *args, **kwargs)`
3. 参数传递
   - 在DRF中可以通过`self.args` 和 `self.kwargs` 来获取url参数
   - 原本的 `request.method` 由于在 `APIView`中又做了一层封装，因此要改为 `request._request.method`，但由于 `DRF` 在对 `Request` 的封装过程中使用了 `__getattr__()` 方法，因此在`DRF`中依旧可以使用 `request.method` 来获取访问方式。

#### request 对象的参数

在 Django REST Framework（DRF）中，URL参数可以通过 `request.query_params` 属性来获取。`request.query_params` 是一个字典，包含了请求 URL 中的查询参数。

DRF允许使用两种方式传递参数：查询字符串和路径参数。

1. 查询字符串参数：
   查询字符串参数是以键值对的形式出现在 URL 的问号之后，多个参数之间使用 `&` 符号分隔。例如，`http://example.com/api/users?name=john&age=25` 中的 `name` 和 `age` 就是查询字符串参数。
   在 DRF 中，查询字符串参数可以通过 `request.query_params` 字典来获取。例如，要获取上述 URL 中的 `name` 和 `age` 参数：

   ```python
   name = request.query_params.get('name')
   age = request.query_params.get('age')
   ```

   通过调用 `request.query_params.get()` 方法并传递键名，可以获取指定的查询字符串参数的值。
2. 路径参数：
   路径参数是在 URL 路径中的一部分，通常用于指定某个资源的唯一标识符或其他动态信息。例如，`http://example.com/api/users/42/` 中的 `42` 就是路径参数。
   在 DRF 中，路径参数可以通过 `request` 对象的 `kwargs` 属性来获取。`kwargs` 是一个字典，包含了视图函数或类中从 URL 捕获的参数。例如，如果有一个 URL 模式为 `path('users/<int:pk>/', views.user_detail)`，则在视图函数或类中可以这样获取路径参数：

   ```python
   def user_detail(request, pk):
       # 使用 pk 进行相关操作
   ```

   `pk` 参数对应于 URL 中的 `<int:pk>` 部分。

### API认证组件

Drf内置了四种API认证方式：

1. BasicAuthentication：每次提交请求的时候附加用户名和密码来进行认证
2. TokenAuthentication：每次提交请求的时候在HTTP headers里附加Token进行认证
3. SessionAuthentication：用户登录之后系统在cookies存入sessionid进行认证
4. RemoteUserAuthentication：通过web服务器认证(apache/nginx这些)

#### 认证组件介绍

在 Django REST Framework（DRF）中，认证（Authentication）组件用于验证请求的身份和权限。它提供了一种基于令牌、会话等方法的身份验证机制，以确保只有经过身份验证的用户可以访问受保护的资源。
常用的认证组件：

1. `SessionAuthentication`：基于Django的会话认证。
   - 使用基于Cookie的会话来管理用户认证状态。
   - 需要在Django项目中启用会话（session）支持。
2. `TokenAuthentication`：基于令牌的认证。
   - 使用预先分发给用户的令牌进行认证。
   - 客户端通常将令牌作为请求头或查询参数包含在每个请求中。
3. `BasicAuthentication`：基本认证。
   - 使用Base64编码的用户名和密码进行认证。
   - 安全性较低，通常用于测试和开发环境。
4. `JWTAuthentication`：JSON Web Token（JWT）认证。
   - 使用JWT进行身份验证和授权。
   - 令牌包含加密的信息，包括用户和其他相关数据。

使用认证组件时，可以在全局级别配置，也可以在视图级别进行配置。在DRF的视图类中，可以通过设置 `authentication_classes` 属性来指定要使用的认证组件。例如：

```python
from rest_framework.authentication import SessionAuthentication
from rest_framework.views import APIView

class MyView(APIView):
    authentication_classes = [SessionAuthentication]
```

此外，还可以将认证组件与权限（Permission）组件结合使用，以确保用户在访问受保护资源之前具有适当的权限。

#### DRF的认证过程

DRF的认证过程是在处理请求时进行的，它涉及以下步骤：

1. 在请求到达视图之前，DRF首先检查视图中是否定义了任何局部认证类（通过`authentication_classes`属性）。如果有，它会按照定义的顺序逐个尝试这些认证类。
2. 对于每个认证类，DRF会调用其`authenticate()`方法。该方法接收一个`request`对象，并返回一个元组`(user, authentication)`，其中`user`表示认证成功的用户对象（或`None`），`authentication`表示请求的认证信息。
3. 如果认证类成功验证了请求并返回了一个用户对象，则会继续处理请求，否则，DRF会将请求标记为未认证，并继续执行后续的认证类。
4. 如果所有的认证类都无法验证请求，DRF将抛出`AuthenticationFailed`异常，该异常表示认证失败。
5. 一旦成功通过认证，DRF会将`user`对象和`authentication`信息存储在请求的`request.user`和`request.auth`属性中，以供后续的视图和权限检查使用。

需要注意的是，对于全局应用的认证类（通过`DEFAULT_AUTHENTICATION_CLASSES`设置），它们将会被应用于项目中的所有视图，并且按照列表的顺序进行尝试验证。
总结起来，DRF的认证过程是在视图处理请求之前进行的，通过逐个尝试认证类来验证请求的身份并提取相关信息。这样可以确保请求合法性，并使得认证用户信息在视图中可用。

#### DRF认证类执行顺序

当一个认证类同时被局部应用和全局应用时，DRF会按照以下顺序执行认证过程：

1. 首先，DRF会执行全局应用的认证类。全局应用的认证类是通过`DEFAULT_AUTHENTICATION_CLASSES`设置的。它们逐个尝试验证请求，按照列表的顺序进行尝试。
2. 如果全局应用的认证类中的任何一个成功通过认证，并返回了一个用户对象，则认证过程终止，并将该用户对象存储在`request.user`属性中。这意味着局部应用的认证类不会再被执行。
3. 如果全局应用的认证类都无法验证请求，DRF会继续执行视图中定义的局部认证类。局部认证类是通过`authentication_classes`属性设置的。它们按照列表的顺序逐个尝试验证请求。
4. 如果局部应用的认证类中的任何一个成功通过认证，并返回了一个用户对象，则认证过程终止，并将该用户对象存储在`request.user`属性中。
5. 如果所有的认证类（包括全局应用和局部应用）都无法验证请求，DRF将抛出`AuthenticationFailed`异常，表示认证失败。

认证类的全局应用和局部应用的生效，使用了面向对象的继承特性。自定义的视图类，如果有自定义的`dispatch()`方法，就执行自己的`dispatch()`；如果没有，就执行父类`APIView`中的`dispatch()`方法。如果有应用自定义的 `authentication_classes` 属性，就使用自定义的属性（局部应用）；如果没有，就按照父类中定义的读取配置文件全局应用。

```python
class APIView(object):
   authentication_classes = api_settings.DEFAULT_AUTHENTICATION_CLASSES # 读取配置文件中的列表

   def dispatch(self):
      self.authentication_classes


class UserView(APIView):
   authentication_classes = [] # 自定义列表


obj = UserView()
obj.dispatch()
```

需要注意的是，全局应用的认证类将优先于局部应用的认证类进行验证。只有当全局应用的认证类无法验证请求时，才会执行局部应用的认证类。

#### 认证组件快速开始

定义三个视图，其中login无需认证就能访问，而user和auth需要经过认证才能访问。

1. 路由 `urls.py`

   ```python
   from api import views

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('login/', views.LoginView.as_view()),
      path('auth/', views.AuthView.as_view()),
      path('user/', views.UserView.as_view()),
   ]
   ```

2. 视图 `views.py`

   ```python
   from rest_framework.response import Response
   from rest_framework.views import APIView
   from rest_framework.authentication import BaseAuthentication
   from rest_framework.exceptions import AuthenticationFailed


   # 定义认证类
   class MyAuthentication(BaseAuthentication):
      def authenticate(self, request):
         # 做用户认证：1. 读取请求传递的token；2. 校验合法性
         # 返回值：
         # - 认证成功：返回元组 (request.user, request.auth)，一般user是用户信息，auth是token信息
         # - 认证失败：抛出异常，返回错误信息
         # - 返回None：多个认证类，依次执行，如果所有的认证类执行完毕，都返回None（既没有认证成功，也没有认证失败），即表示匿名用户。
         token = request.query_params.get("token")
         if token:
               return "Welcome!", token
         # raise AuthenticationFailed("认证失败")
         raise AuthenticationFailed({"code": 403, "detail": "认证失败"})


   class LoginView(APIView):
      # 局部应用认证类
      authentication_classes = []

      def get(self, req):
         print(req.user, req.auth)
         return Response("Login")


   class AuthView(APIView):
      # 局部应用认证类
      authentication_classes = [MyAuthentication,]

      def get(self, req):
         print(req.user, req.auth)
         return Response("Auth")


   class UserView(APIView):
      def get(self, req):
         print(req.user, req.auth)
         return Response("User")
   ```

3. 全局应用认证组件

   ```python
   REST_FRAMEWORK = {
      "UNAUTHENTICATED_USER": None,
      # 全局应用认证组件：与app同级的ext目录下，auth.py中的MyAuthentication类
      "DEFAULT_AUTHENTICATION_CLASSES": ["ext.auth.MyAuthentication", ],
   }
   ```

   **注意**：要全局应用的组件不能卸载`views.py`中，视图类要继承调用 `APIView`，`APIView` 调用了`settings.py`。如果全局认证类写在了 `views.py` 中会出现自己调用自己死循环的情况，会报错。

#### 认证组件的局部应用和全局应用

在Django REST Framework（DRF）中，认证组件可以以局部应用和全局应用两种方式来使用。

1. 局部应用（Per-view Authentication）：
   - 局部应用是指在视图级别对认证组件进行配置。可以在每个视图函数或类视图中独立地应用特定的认证组件。
   - 在视图函数或类视图中，可以通过`authentication_classes`属性来指定使用的认证类：

     ```python
     from rest_framework.authentication import TokenAuthentication
     
     @api_view(['GET'])
     @authentication_classes([TokenAuthentication])
     def my_view(request):
         # 视图函数的逻辑...
     ```

   - 通过在每个视图中设置适当的认证类，可以为不同的视图使用不同的认证方式或将其关闭。

2. 全局应用（Global Authentication）：
   - 全局应用是指在整个项目范围内对认证组件进行配置。可以在项目的设置文件（`settings.py`）中设置默认的全局认证类。
   - 在`settings.py`文件中，可以通过`DEFAULT_AUTHENTICATION_CLASSES`设置默认的全局认证类列表：

     ```python
     REST_FRAMEWORK = {
         'DEFAULT_AUTHENTICATION_CLASSES': [
             'rest_framework.authentication.TokenAuthentication',
             'rest_framework.authentication.SessionAuthentication',
         ],
         ...
     }
     ```

   - 全局应用会将指定的认证类应用于项目中的所有视图。所有未明确指定认证类的视图都会使用默认的全局认证类。

通过使用局部应用和全局应用，可以根据需求来选择在每个视图中设置特定的认证方式，或者在全局范围内统一配置默认的认证方式。这种灵活性使得DRF能够满足不同视图的不同认证需求。

在Django REST Framework（DRF）中，使用基于类的视图（Class-based views，CBV）时，可以通过覆盖视图类的属性来进行局部应用认证组件：

1. `authentication_classes`：该属性指定了在该视图中要使用的认证类列表。可以将其设置为一个包含认证类的列表。

   ```python
   from rest_framework.authentication import TokenAuthentication
   from rest_framework.views import APIView
   
   class MyView(APIView):
       authentication_classes = [TokenAuthentication]
       # 视图类的逻辑...
   ```

2. `permission_classes`：该属性指定了在该视图中要使用的权限类列表。权限类用于控制谁有权访问该视图。可以将其设置为一个包含权限类的列表。

   ```python
   from rest_framework.permissions import IsAuthenticated
   from rest_framework.views import APIView
   
   class MyView(APIView):
       permission_classes = [IsAuthenticated]
       # 视图类的逻辑...
   ```

注意：当CBV中同时存在`authentication_classes`和`permission_classes`属性时，DRF会先执行认证过程，然后再执行权限检查过程。

#### DRF 加载认证组件的过程

DRF加载认证组件，本质就是实例化每个认证类的对象，并将其封装到request对象中。

```python
class Request:
   def __init__(self, request, authenticators=None):
      self._request = request
      self.authenticators = authenticators or ()

   @property
   def user(self):
      if not hasattr(self, "_user"):
         with wrap_attributeerrors():
            self._authenticate()
      return self._user

   @user.setter
   def user(self, value):
      self._user = value
      self._request.user = value

   def _authenticate(self):
      # 读取每个认证组件的对象，执行 authenticate 方法， self=request对象
      for authenticator in self.authenticators:
         try:
            user_auth_tuple = authenticator.authenticate(self)
         except exceptions.APIException:
            self._not_authenticated()
            raise

         if user_auth_tuple is not None:
            self._authenticator = authenticator
            self.user, self.auth = user_auth_tuple
            return

      # 认证失败
      self._not_authenticated()

def _not_authenticated(self):
   self._authenticator = None

   if api_settings.UNAUTHENTICATED_USER:
      self.user = api_settings.UNAUTHENTICATED_USER()
   else:
      self.user = None

   if api_settings.UNAUTHENTICATED_TOKEN:
      self.auth = api_settings.UNAUTHENTICATED_TOKEN()
   else:
      self.auth = None

class APIView(View):
   authentication_classes = api_settings.DEFAULT_AUTHENTICATION_CLASSES

   def perform_authentication(self, request):
      request.user # 能这样调用，request.user要么是属性，要么是被@property装饰的方法

   def initial(self, request, *args, **kwargs):
      self.perform_authentication(request)
      self.check_permissions(request)
      self.check_throttles(request)

   def get authenticators(self):
      # 从认证类列表中调用类
      return [ auth() for auth in self.authentication_classes ]

   def initialze_request(self, request, *args, **kwargs):
      parser_context = self.get_parser_context(request)

      return Request(
         request,
         parsers = self.get_parsers(),
         authenticators = self.get_authenticators(),
         negotiator = self.get_content_negotiator(),
         parser_context = parser_context
      )
   
   def dispatch(self, request, *args, **kwargs):
      # 第一步：封装request（django的request对象 + authenticators认证组件）
      request = self.initialize_request(request, *args, **kwargs)
      self.request = request
      self.headers = self.default_response_headers
      # 第二步：
      self.initial(request, *args, **kwargs)
      handler = getattr(self, request.method, lower(), self.http_method_not_allowed)
      response = handler(request, *args, **kwargs)
      self.response = self.finalize_response(request, response, *args, **kwargs)
      return self.response

class UserView(APIView):
   authentication_classes = []
   def get(self, request):
      print(request.user, request.auth)
      return Response("UserView")
```

#### 多个认证类，满足不同的接口调用需求

`认证组件 = [认证类, 认证类, 认证类, ]`
执行每个认证类中的`authenticate()`方法，有返回值（不为None，表示认证成功或失败）就不会再执行后续的认证类；只有返回None的时候，才会执行后续的认证类。

```python
from rest_framework.authentication import BaseAuthentication
from rest_framework.exceptions import AuthenticationFailed


class ParamAuthentication(BaseAuthentication):
   def authenticate(self, request):
      token = request.query_params.get("token")
      if not token:
         return
      return "zhangsan", token

   # 在DRF的源码中定义了如果没有在authenticate_header中设返回值，则状态码为403
   def authenticate_header(self, request):
      return 'Token'

class HeaderAuthentication(BaseAuthentication):
   def authenticate(self, request):
      token = request.META.get("HTTP_AUTHORIZATION")
      if not token:
         return
      return "zhangsan", token

   def authenticate_header(self, request):
      return "Token"

class NoAuthentication(BaseAuthentication):
   def authenticate(self, request):
      raise AuthenticationFailed({"code": 400, "msg": "认证失败"})

   def authenticate_header(self, request):
      return "Token"
```

#### 面向对象：子类约束

在Python面向对象编程中，对子类的约束有以下几种常见方式：

1. 抽象基类（Abstract Base Class）约束：抽象基类是一种不能被实例化的基类，它定义了一组接口或方法，子类必须实现这些接口或方法。通过使用`abc`模块可以创建抽象基类，并通过`@abstractmethod`装饰器标记要求子类实现的抽象方法。

   ```python
   from abc import ABC, abstractmethod

   class Shape(ABC):
      @abstractmethod
      def area(self):
         pass

   class Circle(Shape):
      def __init__(self, radius):
         self.radius = radius
      
      def area(self):
         return 3.14 * self.radius ** 2
   ```

   `Shape`是一个抽象基类，它定义了一个抽象方法`area()`。子类`Circle`继承自`Shape`并实现了`area()`方法。通过使用`abstractmethod`装饰器将`area()`方法标记为抽象方法，告诉子类必须提供具体的实现。
2. 接口约束：尽管Python中没有内置的接口机制，但可以通过约定来定义接口。接口约束意味着子类必须按照接口约定提供相应的方法和属性。

   ```python
   class Logger:
      def log(self, message):
         raise NotImplementedError("Subclasses must implement log() method")

   class FileLogger(Logger):
      def log(self, message):
         with open('logfile.txt', 'a') as file:
               file.write(message + '\n')
   ```

   `Logger`是一个简单的接口，定义了一个`log()`方法。子类`FileLogger`继承自`Logger`并实现了`log()`方法，提供了将日志信息写入文件的功能。
3. 方法签名约束：父类定义的方法签名指定了参数数量和类型，子类必须保持相同的方法签名并实现该方法。如果子类违反了方法签名约束，可能会导致错误。

   ```python
   class Animal:
      def make_sound(self):
         raise NotImplementedError("Subclasses must implement make_sound() method")

   class Dog(Animal):
      def make_sound(self):
         print("Woof!")

   class Cat(Animal):
      def make_sound(self):
         print("Meow!")
   ```

   `Animal`是一个基类，定义了抽象方法`make_sound()`。子类`Dog`和`Cat`继承自`Animal`并分别实现了`make_sound()`方法，提供不同的动物叫声。
4. 属性约束：父类可以定义类属性或实例属性，并指定其访问权限。子类可以通过继承这些属性，并根据需要添加新的属性。但是，子类不能重写或删除父类的属性。

   ```python
   class Person:
      def __init__(self, name):
         self.name = name

      @property
      def name(self):
         return self._name

      @name.setter
      def name(self, value):
         if not isinstance(value, str):
               raise ValueError("Name must be a string")
         self._name = value
   ```

   `Person`类定义了一个实例属性`name`，并使用`@property`装饰器将其定义为只读属性。同时，定义了`name()`的setter方法，用于对属性进行验证。子类可以继承这个属性，并在需要的基础上进行定制化的操作。
5. 基本功能约束：某些情况下，父类定义了特定的行为或功能，子类必须遵循这些基本功能要求。例如，父类可能定义了一个核心算法，子类必须在此算法的基础上进行定制化实现。

   ```python
   class Shape:
      def calculate_area(self):
         raise NotImplementedError()

      def display(self):
         raise NotImplementedError()

   class Circle(Shape):
      def __init__(self, radius):
         self.radius = radius

      def calculate_area(self):
         return 3.14 * self.radius**2

      def display(self):
         print("This is a circle.")

   class Rectangle(Shape):
      def __init__(self, length, width):
         self.length = length
         self.width = width

      def calculate_area(self):
         return self.length * self.width

      def display(self):
         print("This is a rectangle.")

   circle = Circle(5)
   print(circle.calculate_area())  # 输出：78.5
   circle.display()                 # 输出：This is a circle.

   rectangle = Rectangle(4, 6)
   print(rectangle.calculate_area()) # 输出：24
   rectangle.display()                # 输出：This is a rectangle.
   ```

   父类`Shape`定义了两个基本功能方法：`calculate_area()`和`display()`，并且这两个方法都使用`raise NotImplementedError()`来引发未实现的错误。
   子类`Circle`和`Rectangle`继承了父类`Shape`，并且按照父类的基本功能约束，必须提供这两个方法的具体实现。
   在子类`Circle`中，`calculate_area()`方法根据圆的半径计算面积，并且`display()`方法打印出自己是一个圆。
   在子类`Rectangle`中，`calculate_area()`方法根据长和宽计算面积，并且`display()`方法打印出自己是一个矩形。
   通过这种方式，父类定义了基本功能要求，而子类必须按照这些要求进行定制化实现。这种基本功能约束可以确保父类和子类之间的一致性，同时允许子类根据自身的需要进行特定功能的扩展。

这些约束帮助确保子类在继承和扩展父类时遵循特定的规则和要求。它们有助于提高代码的可维护性、可扩展性和安全性，并确保类之间的一致性和一致的接口。

#### 方法签名约束 VS. 接口约束

1. **方法签名约束**主要用于强制子类实现与父类相同的方法签名。父类定义了一个方法，包括方法的名称、参数数量和参数类型。子类必须保持相同的方法签名并提供具体的实现。如果子类没有按照方法签名要求提供实现，则会引发`NotImplementedError`异常。例如，在方法签名约束的示例代码中，`Animal`类定义了`make_sound()`方法，在子类`Dog`和`Cat`中必须按照相同的方法签名实现该方法。
2. **接口约束**主要是通过约定来定义接口，并使得子类遵循该接口的约定。在Python中，没有内置的接口机制，因此接口约束主要是基于约定的。父类定义了一组接口或方法，并且子类必须按照这些接口约定提供相应的方法和属性。如果子类没有提供相应的方法或属性，则可能无法正确地实现父类的接口。例如，在接口约束的示例代码中，父类`Logger`定义了`log()`方法作为接口，子类`FileLogger`继承自`Logger`并实现了具体的日志写入功能。

总结起来，方法签名约束主要关注子类对方法签名的实现要求，而接口约束主要关注子类对一组接口或方法的完整实现。方法签名约束是一种形式上的约束，确保子类具有相同的方法签名。接口约束更加宽泛，需要子类提供完整的接口实现以满足父类的约定。

阅读代码时判断接口约束和方法签名约束：

1. 首先，查看父类声明的方法、属性等是否包含了`NotImplementedError`的语句。如果是，那么这个父类很有可能使用了方法签名约束或接口约束之一。
2. 进一步判断约束的类型：
   - 对于方法签名约束，可以查看父类方法的名称、参数数量和参数类型是否与子类完全相同，如果是，则该父类强制要求子类实现该方法。
   - 对于接口约束，可以查看父类定义的一组接口或方法，以及它们在子类中的完整实现情况。接口约束通常涉及一组相关的方法或属性，并且子类必须实现每个接口才能满足父类的接口约定。

在Python中，没有显式的接口类型声明和实现，因此更常见的是基于约定实现接口。如果看到一个类定义了一组相关的方法并使用它们作为接口，同时子类按照这些方法提供实现，则很可能是接口约束。

#### 认证组件应用案例

1. `settings.py`

   ```python
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'rest_framework', # 注册rest_framework
      'api.apps.ApiConfig', # 注册app
   ]
   # 设置中文编码，以支持中文字符在 Django 项目中的正常显示
   # 默认情况下 Django 的编码为 UTF-8，这里可以不做修改
   LANGUAGE_CODE = 'zh-hans'
   # 设置时区为上海时区
   TIME_ZONE = 'Asia/Shanghai'
   # 设置 Django 使用的日期格式：以 "%Y年%m月%d日" 的格式字符串表示方式
   DATETIME_FORMAT = "Y年m月d日"

   # drf 配置
   REST_FRAMEWORK = {
      "UNAUTHENTICATED_USER": None,
      # 全局应用认证组件，三个认证类
      "DEFAULT_AUTHENTICATION_CLASSES": [
         "ext.auth.QueryParamsAuthentication",
         "ext.auth.HeaderAuthentication",
         "ext.auth.NoAuthentication",
      ],
   }
   ```

2. `models.py`

   ```python
   from django.db import models


   class UserInfo(models.Model):
      username = models.CharField(verbose_name="用户名", max_length=32)
      password = models.CharField(verbose_name="密码", max_length=64)
      # 临时存储在数据库中，后续会存储到redis或jwt里
      token = models.CharField(verbose_name="TOKEN",
                              max_length=64, null=True, blank=True)
   ```

3. `/drf_example/ext/auth.py` 用户认证中间件

   ```python
   from rest_framework.authentication import BaseAuthentication
   from rest_framework.exceptions import AuthenticationFailed
   from api import models


   # 定义认证类
   class QueryParamsAuthentication(BaseAuthentication):
      def authenticate(self, request):
         # 做用户认证：1. 读取请求传递的token；2. 校验合法性
         # 返回值：
         # - 认证成功：返回元组 (request.user, request.auth)，一般user是用户信息，auth是token信息
         # - 认证失败：抛出异常，返回错误信息
         # - 返回None：多个认证类，依次执行，如果所有的认证类执行完毕，都返回None（既没有认证成功，也没有认证失败），即表示匿名用户。
         token = request.query_params.get("token")
         if not token:
               return
         user_object = models.UserInfo.objects.filter(token=token).first()
         if user_object:
               return user_object, token  # request.user = 用户对象，request.auth = token

      def authenticate_header(self, request):
         return 'API'


   class HeaderAuthentication(BaseAuthentication):
      def authenticate(self, request):
         token = request.META.get("HTTP_AUTHORIZATION")
         if not token:
               return
         user_object = models.UserInfo.objects.filter(token=token).first()
         if user_object:
               return user_object, token

      def authenticate_header(self, request):
         return 'API'


   class NoAuthentication(BaseAuthentication):
      def authenticate(self, request):
         raise AuthenticationFailed({"status": False, "msg": "认证失败"})

      def authenticate_header(self, request):
         return 'API'
   ```

4. `views.py`

   ```python
   from rest_framework.response import Response
   from rest_framework.views import APIView
   from api import models
   import uuid


   class LoginView(APIView):
      # 应用认证类
      authentication_classes = []

      def post(self, req):
         # 1. 接收用户提交的用户名和密码
         # print(req._request.body) # 输出：b'{\r\n    "username":"zhangsan",\r\n    "password":"123123"\r\n}'
         # 获取请求体中的参数
         print(req.data)  # 输出：{'username': 'zhangsan', 'password': '123123'}
         # 获取url中的参数
         print(req.query_params)  # 输出：<QueryDict: {'toekn': ['123']}>
         user = req.data.get("username")
         pwd = req.data.get("password")

         # 2. 数据库校验
         user_object = models.UserInfo.objects.filter(
               username=user, password=pwd).first()
         if not user_object:
               # from ext import code # 引入错误码配置文件
               # return Response({"code": code.ERROR_CODE, "msg": "用户名或密码错误"})
               return Response({"code": False, "msg": "用户名或密码错误"})
         # 3. 正确
         token = str(uuid.uuid4())
         user_object.token = token
         user_object.save()
         return Response({"code": True, "msg": token})


   class UserView(APIView):
      def get(self, req):
         print(req.user, req.auth)
         return Response("User")

      def post(self, req):
         print(req.user, req.auth)
         return Response("User")
   ```

5. `urls.py`

   ```python
   from api import views

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('login/', views.LoginView.as_view()),
      path('user/', views.UserView.as_view()),
   ]
   ```

6. Postman接口访问
   - POST `http://127.0.0.1:8000/login/`
     - Body-raw-JSON

         ```json
         {
            "username":"zhangsan",
            "password":"123123"
         }
         ```

   - GET `http://127.0.0.1:8000/user/?token=5c36d3fd-d0d7-43f1-9661-e1f3b90a5d9b`
   - POST `http://127.0.0.1:8000/user/?token=5c36d3fd-d0d7-43f1-9661-e1f3b90a5d9b`
   - POST `http://127.0.0.1:8000/user/`
     - Headers("Authorization": "5c36d3fd-d0d7-43f1-9661-e1f3b90a5d9b")
   - GET `http://127.0.0.1:8000/user/`
     - Headers("Authorization": "5c36d3fd-d0d7-43f1-9661-e1f3b90a5d9b")

### 权限组件

#### 权限组件介绍

Django REST framework（DRF）的权限组件是用于对 REST API 进行权限控制的一组工具。在 DRF 中，权限组件可以用来限制某些用户或用户组访问 API 的权限，以保证数据安全性。

DRF 常用的内置权限组件：

1. `AllowAny` 权限组件
   `AllowAny` 是 DRF 中内置的默认权限组件，它允许任何人都可以访问这个 API 视图。如果没有指定其它的权限组件，那么 Django REST framework 就会自动使用 `AllowAny` 权限组件。

   ```python
   from rest_framework.permissions import AllowAny
   from rest_framework.views import APIView

   class MyView(APIView):
       permission_classes = [AllowAny]
   ```

2. `IsAuthenticated` 权限组件
   `IsAuthenticated` 限制只有经过身份验证的用户才能访问这个 API 视图。如果用户尚未登录，系统会返回 401 错误。

   ```python
   from rest_framework.permissions import IsAuthenticated
   from rest_framework.views import APIView

   class MyView(APIView):
       permission_classes = [IsAuthenticated]
   ```

3. `IsAdminUser` 权限组件
   `IsAdminUser` 只允许站点管理员访问 API 视图。如果当前用户是普通用户，则无权访问。

   ```python
   from rest_framework.permissions import IsAdminUser
   from rest_framework.views import APIView

   class MyView(APIView):
       permission_classes = [IsAdminUser]
   ```

4. `IsAuthenticatedOrReadOnly` 权限组件
   `IsAuthenticatedOrReadOnly` 权限组件限制只有经过身份验证的用户才能创建、修改或删除数据，而未经身份验证的用户只能读取数据。

   ```python
   from rest_framework.permissions import IsAuthenticatedOrReadOnly
   from rest_framework.views import APIView

   class MyView(APIView):
       permission_classes = [IsAuthenticatedOrReadOnly]
   ```

上述四种常用的权限组件是 DRF 内置的，也可以自定义权限组件来实现更加灵活的权限控制。自定义权限组件需要实现 `BasePermission` 类，并重写 `has_permission` 和/或 `has_object_permission` 方法，以判断用户是否具有访问特定 API 视图的权限。

```python
from rest_framework.permissions import BasePermission

class CustomPermission(BasePermission):
    def has_permission(self, request, view):
        # 判断用户是否满足访问该视图的权限要求
        ...

    def has_object_permission(self, request, view, obj):
        # 判断用户是否满足访问该对象的权限要求
        ...
```

#### DRF的权限检查过程

DRF的权限检查过程是在认证成功后进行的，它涉及以下步骤：

1. 在通过认证后，DRF会检查视图中是否定义了任何局部权限类（通过`permission_classes`属性）。如果有，它会按照定义的顺序逐个尝试这些权限类。
2. 对于每个权限类，DRF会调用其`has_permission()`方法。该方法接收一个`request`对象和一个可选的`view`参数，并返回一个布尔值来指示用户是否具有访问权限。
3. 如果权限类返回`True`，表示用户具有访问权限，则请求将被继续处理；否则，DRF将抛出`PermissionDenied`异常，该异常表示权限拒绝。
4. 对于全局应用的权限类（通过`DEFAULT_PERMISSION_CLASSES`设置），它们将会被应用于项目中的所有视图，并且按照列表的顺序进行判断。

需要注意的是，在执行权限检查之前，必须先进行认证并获取用户对象。用户对象可以在`request.user`属性中找到。
DRF的权限检查过程是在认证成功后进行的，通过逐个尝试权限类来判断用户是否具有访问权限。这样可以确保只有被授权的用户可以访问相应的资源或执行相应的操作。
`权限组件 = [权限类, 权限类, 权限类, ]`
执行所有权限类中的`has_permission()`方法，返回`True`表示授权通过，返回`False`表示未通过。默认情况下，要所有权限类中的`has_permission()`方法都通过才表示权限的校验通过了；只要有一个`has_permission()`方法未通过，则权限的校验未通过。

#### 权限组件快速开始

1. 权限校验中间件 `/drf_example/ext/permitor.py`

   ```python
   from rest_framework.permissions import BasePermission
   import random


   class MyPermission(BasePermission):
      def has_permission(self, request, view):
         if random.randint(1, 3) == 2:
               return True
         return False
         """
         权限校验失败返回：
         {
               "detail": "您没有执行该操作的权限。"
         }
         """
   ```

2. 权限类局部应用 `views.py`

   ```python
   from ext.permitor import MyPermission
   class UserView(APIView):
      permission_classes = [MyPermission, ]

      def get(self, req):
         print(req.user, req.auth)
         return Response("User")

      def post(self, req):
         print(req.user, req.auth)
         return Response("User")
   ```

3. 权限类全局应用 `settings.py`

   ```python
   # drf 配置
   REST_FRAMEWORK = {
      "UNAUTHENTICATED_USER": None,
      # 全局应用认证组件
      "DEFAULT_AUTHENTICATION_CLASSES": [
         "ext.auth.QueryParamsAuthentication",
         "ext.auth.HeaderAuthentication",
         "ext.auth.NoAuthentication",
      ],
      "DEFAULT_PERMISSION_CLASSES": [
         "ext.permitor.MyPermission"
      ]
   }
   ```

#### 权限认证错误信息和多个认证类

1. 通过在权限类中定义`message`变量来定义权限认证未通过的错误信息

   ```python
   from rest_framework.permissions import BasePermission


   class MyPermission1(BasePermission):
      # 定义错误信息
      message = {"status": False, "msg": "无权访问"}

      def has_permission(self, request, view):
         print("MyPermission1")
         return False
         """
         权限校验失败返回：
         {
            "status": "False",
            "msg": "无权访问"
         }
         """
   ```

2. 多个权限类同时应用，只有当应用的权限类都返回`True`通过后，才授权成功，只要有一个返回`False`都是未授权。

   ```python
   # permitor.py
   from rest_framework.permissions import BasePermission


   class MyPermission1(BasePermission):
      # 定义错误信息
      message = {"status": False, "msg": "无权访问"}

      def has_permission(self, request, view):
         print("MyPermission1")
         return True


   class MyPermission2(BasePermission):
      # 定义错误信息
      message = {"status": False, "msg": "无权访问"}

      def has_permission(self, request, view):
         print("MyPermission2")
         return True


   class MyPermission3(BasePermission):
      # 定义错误信息
      message = {"status": False, "msg": "无权访问"}

      def has_permission(self, request, view):
         print("MyPermission3")
         return False
   ```

   ```python
   # views.py
   from ext.permitor import MyPermission1, MyPermission2, MyPermission3

   class AuthView(APIView):
      # 只有当permission_classes列表中的所有权限类都校验通过后，才能访问指定资源
      permission_classes = [MyPermission1, MyPermission3, MyPermission2, ]

      def get(self, req):
         print(req.user, req.auth)
         return Response({"status": True, "data": [11, 22, 33, 44]})
   ```

#### 权限认证的源码执行流程

```python
class APIView(View):
   def permission_denied(self, request, message=None, code=code):
      if request.authenticators and not request.successful_authenticators:
         raise exceptions.NoAuthenticated()
      raise exception.PermissionDenied(detail=message, code=code)

   def get_permissions(self):
      return [permission() for permission in self.permission_classes] # 读取全局配置或视图中定义的局部变量

   def check_permissions(self, request):
      for permission in self.get_permissions():
         if not permission.has_permission(request, self):
            self.permission_denied(
               request,
               message = getattr(permission, "message", None),
               code = getattr(permission, "code", None)
            )

   def initial(self, request, *args, **kwargs):
      self.perform_authentication(request) # 执行认证组件，认证失败抛出异常，后续代码不执行
      self.check_permissions(request) # 执行权限组件
      self.check_throttles(request)

   def dispatch(self, request, *args, **kwargs):
      request = self.initial_request(request, *args, **kwargs)
      self.request = request
      self.headers = self.default_response_headers
      try:
         self.initial(request, *args, **kwargs)
         handler = getattr(self, request.method.lower(), self.http_method_not_allowed)
         response = handler(request, *args, **kwargs)
      except Exception as exc:
         response = self.handle_exception(exc)
      self.response = self.finalize_response(request, response, *args, **kwargs)
      return self.response
```

#### 权限组件的扩展

重写`check_permissions()`

```python
# 自定义View，ext/myview.py
class OrAPIView(APIView):
   def check_permissions(self, request):
      # 权限检查
      # 保存未通过验证的权限对象
      no_permission_objects = []
      # 遍历所有哦权限类对象
      for permission in self.get_permissions():
         # 调用其has_permission方法，判断是否有访问该资源的权限
         if permission.has_permission(request, self):
               # 如果有权限则通过校验，直接返回
               return
         # 否则，把该权限对象添加到列表中
         else:
               no_permission_objects.append(permission)
      # 如果最终列表不为空，说明用户没有权限访问该资源，抛出异常并返回响应信息
      else:
         self.permission_denied(
               request,
               message=getattr(no_permission_objects[0], 'message', None),
               code=getattr(no_permission_objects[0], 'code', None)
         )
```

```python
# views.py
from ext.myview import OrAPIView

class AuthView(OrAPIView):
   pass
```

#### 权限组件应用案例

1. `ext/permitor.py` 编写权限类

   ```python
   from rest_framework.permissions import BasePermission


   class UserPermission(BasePermission):
      message = {"status": False, "msg": "无员工权限"}

      def has_permission(self, request, view):
         if request.user.role == 3:
               return True
         return False


   class ManagerPermission(BasePermission):
      message = {"status": False, "msg": "无管理权限"}

      def has_permission(self, request, view):
         if request.user.role == 2:
               return True
         return False


   class BossPermission(BasePermission):
      message = {"status": False, "msg": "无超管权限"}

      def has_permission(self, request, view):
         if request.user.role == 1:
               return True
         return False
   ```

2. `ext/permitView.py`: 编写权限校验规则，当满足其中一个权限校验类返回True，即通过校验

   ```python
   from rest_framework.views import APIView


   class PermitView(APIView):
      def check_permissions(self, request):
         # 保存未通过验证的权限对象
         no_permission_objects = []
         # 遍历所有权限类对象
         for permission in self.get_permissions():
               # 调用其has_permission方法，判断是否有访问该资源的权限
               if permission.has_permission(request, self):
                  # 如果有权限则通过校验，直接返回
                  return
               # 否则，把该权限对象添加到列表中
               else:
                  no_permission_objects.append(permission)
         # 如果最终列表不为空，说明用户没有权限访问该资源，抛出异常并返回响应信息
         else:
               self.permission_denied(
                  request,
                  message=getattr(no_permission_objects[0], 'message', None),
                  code=getattr(no_permission_objects[0], 'code', None)
               )
   ```

3. `views.py`

   ```python
   from ext.permitView import PermitView
   from ext.permitor import UserPermission, ManagerPermission, BossPermission


   class UserView(PermitView):
      # 三种角色任意一个都可以访问
      permission_classes = [UserPermission, ManagerPermission, BossPermission, ]

      def get(self, req):
         print(req.user, req.auth)
         return Response("User")

      def post(self, req):
         print(req.user, req.auth)
         return Response("User")


   class UserListView(PermitView):
      # Manager 或 Boss可以i访问
      permission_classes = [ManagerPermission, BossPermission, ]

      def get(self, req):
         print(req.user, req.auth)
         return Response({"status": True, "data": [11, 22, 33, 44]})
   ```

4. `urls.py`

   ```python
   from api import views

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('login/', views.LoginView.as_view()),
      path('user/', views.UserView.as_view()),
      path('user/list/', views.UserListView.as_view()),
   ]
   ```

#### 扩展

1. 如何在开发过程中想要重新封装request对象？
   - 定位源码：dispatch() -> initialize_request()方法， -> Request
   - 重新封装：在自己的View类中重写initialize_request()方法，对Request进行重新定义
2. drf的认证组件、权限组件和 django的中间件的关系：

   DRF 的认证和权限组件和 Django 的中间件都可以用来保护 API 路由或视图的安全性。但它们在实现上是有区别的。
   Django 中的中间件是一种类似于 "管道" 的机制，它可以在请求到达 view 前拦截请求，处理请求，再将请求传递下去。Django 中的中间件是基于 Django 框架的请求响应周期的，而且中间件是对 Django 的请求和响应对象进行操作的。
   DRF 的认证和权限组件则是针对 RESTful API 请求所提供的。它们主要是通过 `request` 对象上的属性和方法进行操作，例如 `request.user` 可以获取请求的用户信息。认证和权限组件都是作为 API View 的类属性来定义，并在 API View 中被使用。DRF 的认证和权限组件与 Django 中的中间件不同，它们旨在直接保护 API View，而非整个 Django Web 应用。
   当客户端发起请求时，Django 中间件的处理顺序是按照定义的顺序从上往下执行，直到最后一个中间件或者某个中间件返回了响应为止。而 DRF 的认证和权限组件则是在 API View 被访问时根据定义顺序依次执行。
   总的来说，Django 中的中间件和 DRF 的认证、权限组件都是通过对请求进行拦截、处理和验证，来保护 Web 应用或 API 的安全性。但它们的实现机制和使用方法都有所不同，需要根据具体情况选择合适的方式来实现安全控制。

### 限流组件

#### 限流组件介绍

DRF（Django REST framework）提供了一些内置的限流（Rate Limiting）组件，用于限制用户对 API 的访问频率，以防止滥用和确保系统的稳定性。

1. 限流概念：限流是指对用户或客户端在一定时间段内的请求进行限制，控制其访问频率。通过限制请求的速率，可以防止恶意用户或者过多的请求对系统造成过大负载。
2. DRF 限流组件：DRF 提供了几种内置的限流组件，包括：
   - `AnonRateThrottle`：匿名用户的限流组件，基于 IP 地址进行限流。
   - `UserRateThrottle`：认证用户的限流组件，基于用户身份进行限流。
   - `ScopedRateThrottle`：根据自定义的作用域对用户进行限流，可以根据不同的作用域配置不同的限流策略。
3. 配置限流组件：在 DRF 的 `settings.py` 中配置限流组件，可以通过 `DEFAULT_THROTTLE_CLASSES` 和 `DEFAULT_THROTTLE_RATES` 两个设置项来指定使用哪些限流组件以及每个组件的限流速率。
4. 限流速率设置：可以通过 `DEFAULT_THROTTLE_RATES` 设置项来指定每个限流组件的速率。速率可以是一个字符串，例如 `"1000/day"` 表示每天允许 1000 个请求；也可以是一个元组列表，例如 `[("user", "1000/day"), ("anon", "100/day")]` 表示对认证用户限流每天 1000 个请求，对匿名用户限流每天 100 个请求。
5. 应用到视图或整个项目：限流组件可以应用到特定的视图或整个项目中，具体取决于在哪里进行配置。在视图类中使用 `throttle_classes` 属性指定要应用的限流组件；如果要应用到整个项目，可以在 `settings.py` 中的 `DEFAULT_THROTTLE_CLASSES` 设置项中配置。

限制访问频率，最重要的是找到他的第一标识：

- **已登录用户**：需要在用户认证过程中获得用户的身份信息，并将身份信息与请求关联起来，例如使用会话或令牌。可以使用用户身份信息作为唯一标识符，并设置相应的访问频率限制。
- **匿名用户**：对于没有提供身份信息的请求，可以将其视为匿名用户。可以通过检测请求中的 IP 地址、用户代理、设备ID等信息来识别匿名用户。可以使用 IP 地址或设备标识等信息作为标识符，限制同一标识符的请求频率。

限流机制：短信发送平台限制1小时发10次、IP限制、验证码、防爬虫机制等。
代码层面的限流方法：

1. **计数器法**：使用计数器记录请求次数，当请求数达到设定的阈值时进行限流。可以通过内存、数据库或分布式缓存等方式存储计数器。
2. **令牌桶法**：使用令牌桶来控制访问频率。令牌桶中存放着一定数量的令牌，每个令牌代表一个请求的许可。当请求到达时，需要从令牌桶中获取一个令牌，如果令牌桶中没有足够的令牌，则进行限流。
3. **漏桶法**：漏桶模型假设系统以固定的速率来处理请求，而不管流量的突发情况。在漏桶中，请求被添加到桶中，然后以固定的速率处理请求。如果请求无法立即处理，则被丢弃或排队等待处理。这种方法可以平滑请求的处理速度。

#### 限流认证的源码执行流程

```python
class BaseThrottle:
   def allow_request(self, request, view):
      raise NotImplementedError('.allow_request() must be overridden')
   def get_ident(self, request):
      # 获取IP地址
      xff = request.META.get("HTTP_X_FORWARDED_FOR")
      remote_addr = request.META.get("REMOTE_ADDR")
      num_proxies = api_settings.NUM_PROXIES

      if num_proxies is not None:
         if num_proxies == 0 or xff is None:
            return remote_addr
         addrs = xff.split(",")
         client_addr = addrs[-min(num_proxies, len(addrs))]
         return client_addr.strip()

      return ''.join(xff.split()) if xff else remote_addr
         
   def wait(self):
      return None


class SimpleRateThrottle(BaseThrottle):
   cache = default_cache
   timer = time.time
   cache_format = "throttle_%(scope)s_%(ident)s"
   scope = None
   THROTTLE_RATES = api_settings.DEFAULT_THROTTLE_RATES

   def __init__(self):
      if not getattr(self, 'rate', None):
         self.rate = self.get_rate()
      self.num_requests, self.duration = self.parse_rate(self.rate)

   def get_cache_key(self, request, view):
      raise NotImplementedError(".get_cache_key() must be overridden")

   def get_rate(self):
      if not getattr(self, 'scope', None):
         msg = ("You must set either `.scope` or `.rate` for '%s' throttle") % self ImprperlyConfigured(msg)
         raise ImproperlyConfigured(msg)
      try:
         return self.THROTTLE_RATES[self.scope]
      except KeyError:
         msg = "No default throttle rate set for '%s' scope" % self.scope
         raise ImproperlyConfigured(msg)

   def parse_rate(self):
      # 处理 THROTTLE_RATES
      if rate is None:
         return (None, None)
      num, period = rate.split('/')
      num_requests = int(num)
      # [period[0]通过索引取hour、minutes、days的第一个字符，使支持写全
      duration = {'s': 1, 'm': 60, 'h': 3600, 'd': 86400}[period[0]]
      # THROTTLE_RATES = {"XX": "5/m"} 返回 (5, 60)
      return (num_requests, duration)

   def allow_request(self, request, view):
      # 如果没有配置rate就直接返回True，不作限流
      if self.rate is None:
         return True

      # 获取用户的唯一标识
      self.key = self.get_cache_key(request, view)
      if self.key is None:
         return True

      # 获取历史访问记录
      self.history = self.cache.get(self.key [])
      # 获取时间戳
      self.now = self.timer()

      # 从 self.history 列表的末尾开始遍历，如果最后一个元素小于等于当前时间减去持续时间的差值，则从列表中移除该元素。循环将一直执行，直到 self.history 列表为空或者最后一个元素不符合条件为止。
      while self.history and self.history[-1] <= self.now - self.duration:
         self.history.pop()
      
      # 如果 history的列表长度 >= 设置的访问次数，表示超过了限制，要进行限流
      if len(self.history) >= self.num_requests:
         return self.throttle_failure()
      # 否则，表示未超过限制，可以访问
      return self.throttle_success()

   def throttle_success(self):
      # 通过限流验证后，将当前访问的时间戳加入历史访问列表
      self.history.insert(0, self.now)
      # 并添加缓存
      self.cache.set(self.key, self.history, self.duration)
      return True

   def throttle_failure(self):
      return False

   def wait(self):
      if self.history:
         # 还需要等待多久
         remaining_duration = self.duration - (self.now - self.history[-1])
      else:
         remaining_duration = self.duration
      # 能访问几次
      availble_requests = self.num_requests - len(self.history) + 1
      if available_requests <= 0:
         return None
      
      return remaining_duration / float(available_requests)


class MyThrottle(SimpleRateThrottle):
   def get_cache_key(self, request, view):
      if request.user:
         ident = request.user.pk # 用户ID
      else:
         ident = self.get_ident(request) # 获取请求用户IP（在request的请求头中找）
      return self.cache_format % {"scope": self.scope, "ident": ident}
```

```python
# 可以通过重写截流类来定制错误信息
class Throttled(APIException):
   status_code = status.HTTP_429_T00_MANY_REQUESTS
   default_detail = _("Request was throttled")
   extra_detail_singular = _("Expected available in {wait} second.")
   extra_detail_plural = _("Expected availabel in {wait} seconds.")
   default_code = "throttled"

   def __init__(self, wait=None, detail=None, code=None):
      if detail is None:
         detail = force_str(self.default_detail)
      if wait is not None:
         wait = math.ceil(wait)
         detail = "".join((
            detail,
            force_str(ngettext(self.extra_detail_singular.format(wait=wait),
            self.extra_detail_plural.format(wait=wait),
            wait))
         ))
         self.wait = wait
         super().__init__(detail, code)


class APIView(View):
   permission_classes = 全局配置
   def get_throttles(self):
      return [throttle() for throttle in self.throttle_classes]

   def throttled(self, request, wait):
      raise exception.Throttled(wait)

   def check_throttles(self, request):
      throttle_durations = []
      for throttle in self.get_throttles():
         # 当 allow_request()返回false，则将它的等待时间加入列表，进行限流；返回true则直接返回视图
         if not throttle.allow_request(request, self):
            throttle_duration.append(throttle.wait())
         
      if throttle_durations:
         duration = [
            duration for duration in throttle_durations
            if duration is not None
         ]
         duration = max(duration, default=None)
         self.throttled(request, duration)

   def initial(self, request, *args, **kwargs):
      self.perform_authentication(request)
      self.check_permissions(request)
      self.check_throttles(request)
   
   def dispatch(self, request, *args, **kwargs):
      request = self.initialize_request(request, *args, **kwargs)
      self.request = request
      self.headers = self.default_response_headers
      try:
         self.initial(request, *args, **kwargs)
         handler = getattr(self, request.method.lower(), self.http_method_not_allowed)
         response = handler(request, *args, **kwargs)
      except Exception as exc:
         response = self.handle_exception(exc)
      self.response = self.finalize_response(request, response, *args, **kwargs)
      return self.response
```

源码解析：

1. 对象加载：获取每个限流类的对象，初始化（读取限流的配置，获取 限制的访问次数 num_requests + 时间间隔 duration）
2. allow_request 是否限流

#### 限流组件快速开始

1. 编写限流类 `/drf_example/ext/throttle.py`

   ```python
   from rest_framework.throttling import SimpleRateThrottle
   from django.core.cache import cache as default_cache


   class MyThrottle(SimpleRateThrottle):
      scope = "XX"
      THROTTLE_RATES = {"XX": "5/m"}
      cache = default_cache  # 连接settings.py中配置的CACHE（redis）

      def get_cache_key(self, request, view):
         if request.user:
               ident = request.user.pk  # 用户ID
         else:
               ident = self.get_ident(request)  # 获取请求用户IP（在request的请求头中找）
         return self.cache_format % {"scope": self.scope, "ident": ident}
   ```

2. 安装redis连接工具 `pip install django-redis`
3. 配置redis连接 `settings.py`

   ```python
   # redis缓存的配置
   CACHES = {
      "default": {
         "BACKEND": "django_redis.cache.RedisCache",
         "LOCATION": "redis://127.0.0.1:6379",
         "OPTIONS": {
               "CLIENT_CLASS": "django_redis.client.DefaultClient",
               "PASSWORD": "pass123",
         }
      }
   }
   ```

4. 启动redis服务 `redis-server.exe (G:\Redis-x64-5.0.14.1\redis.windows.conf)`
5. 应用限流类 `views.py`

   ```python
   class LoginView(APIView):
      authentication_classes = []
      throttle_classes = [MyThrottle, ]

      def post(self, req):
         pass
   ```

#### 连接redis

1. 安装 `pip install django_redis`
2. 在Django的设置文件（`settings.py`）中进行Redis配置，添加如下内容：

   ```python
   CACHES = {
      'default': {
         'BACKEND': 'django_redis.cache.RedisCache',
         'LOCATION': 'redis://127.0.0.1:6379/0',  # Redis的连接地址和数据库编号
         'OPTIONS': {
               'CLIENT_CLASS': 'django_redis.client.DefaultClient',
         }
      }
   }
   ```

   以上配置使用了`django_redis.cache.RedisCache`作为缓存的后端，并指定了Redis的连接地址和数据库编号。
3. 在代码中可以使用以下方式连接Redis并进行数据存储：

   ```python
   import redis

   # 连接到Redis
   redis_client = redis.Redis(host='localhost', port=6379, db=0)

   # 存储数据
   redis_client.set('key', 'value')
   ```

   这里使用`redis.Redis`类创建一个Redis客户端对象`redis_client`，需要传入Redis的主机地址、端口号和数据库编号等参数。然后，使用`set`方法将数据存储到Redis中，传入键名`key`和对应的值`value`。
4. redis 常用命令
   1. 启动服务：`redis-server.exe (G:\Redis-x64-5.0.14.1\redis.windows.conf)` 不加配置文件路径则以默认配置启动
   2. 打开redis客户端：`redis-cli.exe -h 127.0.0.1 -p 6379`
   3. 登录: `auth pass123`
   4. (连接后命令)连通性测试：`ping` 返回PONG说明连接正常
   5. (连接后命令)选择数据库：`select [key]` redis默认有16个数据库，初始默认使用0号库
   6. (连接后命令)`set` 设置键值，`get` 取出键值
   7. (连接后命令)关闭服务：`shutdown`

#### 限流组件应用案例

1. `settings.py`

   ```python
   # redis缓存的配置
   CACHES = {
      "default": {
         "BACKEND": "django_redis.cache.RedisCache",
         "LOCATION": "redis://127.0.0.1:6379/0",
         "OPTIONS": {
               "CLIENT_CLASS": "django_redis.client.DefaultClient",
               "PASSWORD": "pass123",
         }
      }
   }

   # drf 配置
   REST_FRAMEWORK = {
      "UNAUTHENTICATED_USER": None,
      # 全局应用认证组件
      "DEFAULT_AUTHENTICATION_CLASSES": [
         "ext.auth.QueryParamsAuthentication",
         "ext.auth.HeaderAuthentication",
         "ext.auth.NoAuthentication",
      ],
      "DEFAULT_THROTTLE_RATES": {
         "ip": "5/m",
         "user": "10/m"
      },
      # "DEFAULT_PERMISSION_CLASSES": [
      #     "ext.permitor.MyPermission"
      # ]
   }
   ```

2. `throttle.py` 限流类

   ```python
   from rest_framework.throttling import SimpleRateThrottle
   from django.core.cache import cache as default_cache


   class IpThrottle(SimpleRateThrottle):
      scope = "ip"
      cache = default_cache

      def get_cache_key(self, request, view):
         ident = self.get_ident(request)
         return self.cache_format % {"scope": self.scope, "ident": ident}


   class UserThrottle(SimpleRateThrottle):
      scope = "user"
      cache = default_cache

      def get_cache_key(self, request, view):
         ident = request.user.pk  # 用户ID
         return self.cache_format % {"scope": self.scope, "ident": ident}
   ```

3. `views.py`

   ```python
   from rest_framework.response import Response
   from rest_framework.views import APIView
   from api import models
   import uuid
   from ext.permitView import PermitView
   from ext.permitor import UserPermission, ManagerPermission, BossPermission
   from ext.throttle import IpThrottle, UserThrottle


   class LoginView(APIView):
      authentication_classes = []
      throttle_classes = [IpThrottle, ]

      def post(self, req):
         # 1. 接收用户提交的用户名和密码
         # 输出：b'{\r\n    "username":"zhangsan",\r\n    "password":"123123"\r\n}'
         # print(req._request.body)
         # 获取请求体中的参数
         print(req.data)  # 输出：{'username': 'zhangsan', 'password': '123123'}
         # 获取url中的参数
         print(req.query_params)  # 输出：<QueryDict: {'toekn': ['123']}>
         user = req.data.get("username")
         pwd = req.data.get("password")

         # 2. 数据库校验
         user_object = models.UserInfo.objects.filter(
               username=user, password=pwd).first()
         if not user_object:
               # return Response({"code": code.ERROR_CODE, "msg": "用户名或密码错误"})
               return Response({"code": False, "msg": "用户名或密码错误"})
         # 3. 正确
         token = str(uuid.uuid4())
         user_object.token = token
         user_object.save()
         return Response({"code": True, "msg": token})


   class UserView(PermitView):
      # 三种角色都可以访问
      permission_classes = [UserPermission, ManagerPermission, BossPermission, ]
      throttle_classes = [UserThrottle, ]

      def get(self, req):
         print(req.user, req.auth)
         return Response("User")
   ```

### 版本组件

在请求中携带版本号，便于后续API的更新迭代。
如：`http://www.test.com/api/v1/info`，`http://www.test.com/api/v2/info`

#### 版本类源码执行流程

```python
class BaseVersioning:
   default_version = api_settings.DEFAULT_VERSION
   allowed_version = api_settings.ALLOWED_VERSIONS
   version_param = api_settings.VERSION_PARAM

   def determine_version(self, request, *args, **kwargs):
      msg = "{cls}.determine_version() must be implemented."
      raise NotImplementedError(msg.format(
         cls=self.__class__.__name__
      ))

   def reverse(self, viewname, args=None, kwargs=None, request=None, format=None, **extra):
      return _reverse(viewname, args, kwargs, request, format, **extra)

   def is_allowed_version(self, version):
      if not self.allowed_versions:
         return True
      return ((version is not None and version == self.default_version) or (version in self.allowed_versions))

class QueryParameterVersioning(BaseVersioning):
   invalid_version_message = _("Invalid versoin in query parameter.")
   
   def determine_version(self, request, *args, **kwargs):
      version = request.query_params.get(self.version_param, self.default_version)
      if not self.is_allowed_version(version):
         raise exceptions.NotFound(self.invalid_version_message)
      return version

   def reverse(self, viewname, args=None, kwargs=None, request=None, format=None, **extra):
      url = super().reverse(
         viewname, args, kwargs, request, format, **extra
      )
      if request.version is not None:
         return replace_query_param(url, self.version_param, request.version)
      return url


class APIView(View):
   versioning_class = api_settings.DEFAULT_VERSIONING_CLASS

   def determine_version(self, request, *args, **kwargs):
      if self.versioning_class is None:
         return (None, None)
      scheme = self.versioning_class()
      # 返回一个元组 (版本,版本类的对象)
      return (scheme.determine_version(request, *args, **kwargs), scheme)

   def initial(self, request, *args, **kwargs):
      version, scheme = self.determine_version(request, *args, **kwargs)
      request.version, request.versioning_scheme = version, scheme
      self.perform_authentication(request)
      self.check_permission(request)
      self.check_throttles(request)


class HomeView(APIView):
   versioning_class = QueryParameterVersioning

   def get(self, request):
      print(request.version)
      return Response("Home")
```

#### 版本类应用案例

1. `settings.py`

   ```python
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'api.apps.ApiConfig',
      'rest_framework',
   ]
   REST_FRAMEWORK = {
      # 将默认的未认证用户身份由django.contrib.auth.models.AnonymousUser 设置为None
      "UNAUTHENTICATED_USER": None,
      # 设置版本参数名称为version
      "VERSION_PARAM": "version",
      # 设置默认版本
      "DEFAULT_VERSION": "v1",
      # 设置支持的版本，除此之外都会报错
      "ALLOWED_VERSIONS": ["v1", "v2"],
      # 设置默认使用URLPathVersioning进行版本管理
      "DEFAULT_VERSIONING_CLASS": "rest_framework.versioning.URLPathVersioning",
   }
   ```

2. `views.py`

   ```python
   from rest_framework.views import APIView
   from rest_framework.response import Response
   from rest_framework.versioning import QueryParameterVersioning, URLPathVersioning, AcceptHeaderVersioning


   class ParamView(APIView):
      # 优先读取配置文件的VERSION_PARAM
      versioning_class = QueryParameterVersioning

      def get(self, request):
         # 对于http://127.0.0.1:8000/param/?version=v1，request.version=v1
         print(request.version)
         print(request.versioning_scheme)
         url = request.versioning_scheme.reverse("param", request=request)
         # 反向生成URL： http://127.0.0.1:8000/param/?version=v1
         print("反向生成URL：", url)
         return Response("Param")


   class UrlPathView(APIView):
      versioning_class = URLPathVersioning

      def get(self, request, version):
         # print(request.version)
         # print(request.versioning_scheme)
         # url1 = request.versioning_scheme.reverse("urlpath", request=request)
         # # 反向生成URL： http://127.0.0.1:8000/api/v1/urlpath/
         # print("反向生成URL：", url1)
         return Response("UrlPath")


   class HeaderView(APIView):
      # 访问url：http://127.0.0.1:8000/api/header/；请求头增加：{version: v1}
      versioning_class = AcceptHeaderVersioning

      def get(self, request, *args, **kwargs):
         print(request.version)
         print(request.versioning_scheme)
         return Response("Header")


   class DefaultView(APIView):
      def get(self, request, *args, **kwargs):
         print(request.version)
         print(request.versioning_scheme)
         return Response("Default")
   ```

3. `urls.py`

   ```python
   from django.contrib import admin
   from django.urls import path, re_path
   from api import views

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('param/', views.ParamView.as_view(), name="param"),
      # http://127.0.0.1:8000/api/v1/urlpath/
      path('api/<str:version>/urlpath/',
            views.UrlPathView.as_view(), name="urlpath"),
      # http://127.0.0.1:8000/api/v1/reurlpath/
      re_path(r'^api/(?P<version>\w+)/reurlpath/$',
               views.UrlPathView.as_view(), name="reurlpath"),
      path('api/header/', views.HeaderView.as_view(), name="header"),
      path('api/<str:version>/default/',
            views.DefaultView.as_view(), name="default"),
   ]
   ```

### 解析器

读取不同格式数据进行解析然后赋值给`request.data`等对象。
如：`user=zhangsan&age=18` => `{"user": "zhangsan", "age": 18}`

#### 解析器介绍

解析器（Parser）是在Web框架中用于解析请求数据的组件。它的主要作用是将客户端发送的请求数据转换为可供后续处理的数据结构，并将其传递给视图函数或其他处理程序进行处理。
在Web开发中，常见的请求数据类型包括表单数据、JSON数据、文件上传等。不同的请求数据需要使用不同的解析器进行解析和处理。
**解析器的工作流程**：

1. 接收请求数据：解析器从HTTP请求中接收原始请求数据。
2. 数据解析：根据请求数据的类型，解析器将原始数据解析为对应的数据结构。比如，解析器可以将表单数据解析为字典、将JSON数据解析为Python数据类型等。
3. 数据验证：解析器可以对解析后的数据进行验证，例如检查数据字段是否符合规定的格式、是否缺少必需字段等。
4. 数据处理：解析器将解析和验证后的数据传递给视图函数或其他处理程序进行进一步的业务逻辑处理。
5. 返回响应：处理程序执行完业务逻辑后，生成响应数据并返回给客户端。

**常见的解析器**：

- 表单解析器（Form Parser）：用于解析URL编码的表单数据。
- 文件解析器（File Parser）：用于解析文件上传请求。
- JSON解析器（JSON Parser）：用于解析JSON格式的请求数据。
- 多部分解析器（MultiPart Parser）：用于解析多部分表单数据，包括文件上传和文本字段。

Web框架通常会提供默认的解析器，并允许开发人员根据需求选择或添加其他解析器。通过合理选择和配置解析器，可以确保服务器能够正确解析和处理各种类型的请求数据，并进行相应的业务逻辑处理。

#### DRF解析器

DRF框架中的解析器封装了常见的请求数据格式，通过将请求体数据解析成特定的数据结构来简化开发者的开发工作。以下是DRF框架中一些常用的解析器：

1. JSONParser：用于处理请求体中的 JSON 数据。

   ```python
   from rest_framework.parsers import JSONParser

   # 将请求体数据解析成JSON数据结构
   parser_classes = [JSONParser]

   class ExampleView(APIView):
      def post(self, request):
         # 对请求体数据进行JSON解析
         data = request.data
         # 使用JSON数据进行业务逻辑处理
         ...
   ```

2. FormParser：用于处理请求体中的表单数据。

   ```python
   from rest_framework.parsers import FormParser, MultiPartParser

   # 将表单数据解析成字典
   parser_classes = [FormParser, MultiPartParser]

   class ExampleView(APIView):
      def post(self, request):
         # 对请求体数据进行表单解析
         data = request.data
         # 使用表单数据进行业务逻辑处理
         ...
   ```

3. MultiPartParser：用于处理请求体中的多部分数据，包括文件上传和文本字段。

   ```python
   from rest_framework.parsers import MultiPartParser

   # 将多部分表单数据解析成字典
   parser_classes = [MultiPartParser]

   class ExampleView(APIView):
      def post(self, request):
         # 对请求体数据进行多部分解析
         data = request.data
         # 使用多部分数据进行业务逻辑处理
         ...
   ```

除此之外，还有其他一些解析器，比如 `XMLParser`、`YAMLParser` 等。

#### DRF解析器应用

```python
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework.parsers import JSONParser, FormParser
from rest_framework.negotiation import DefaultContentNegotiation


class DefaultView(APIView):
    # 获取所有的解析器
    parser_classes = [JSONParser, FormParser]
    # 根据请求，匹配解析器或渲染器
    content_negotiation_class = DefaultContentNegotiation

    def post(self, request, *args, **kwargs):
        print(request.data, type(request.data))
        return Response("POST")
```

1. 解析json格式数据
   - 访问URL：`http://127.0.0.1:8000/api/v1/default/`
   - 访问方式：`POST`
   - 设置路径：postman-Body-raw-JSON
   - 模拟数据：`{"name": "zhangsan", "age": 18}`
   - 输出：`{'name': 'zhangsan', 'age': 18} <class 'dict'>`
2. 解析表单数据
   - 访问URL：`http://127.0.0.1:8000/api/v1/default/`
   - 访问方式：`POST`
   - 设置路径：postman-Body-'x-www-form-urlencoded'
   - 模拟数据：`{"name": "zhangsan", "age": 19}`
   - 输出：`<QueryDict: {'name': ['zhangsan'], 'age': ['19']}> <class 'django.http.request.QueryDict'>`
3. 解析器全局配置 `settings.py`

```python
REST_FRAMEWORK = {
   "DEFAULT_PARSER_CLASSES": ["rest_framework.parsers.JSONParser", ]
}
```

#### DRF解析器源码执行流程

```python
class Request:
   def __init__(self, request, parsers=None, authenticatiors=None, negotiator=None, parser_context=None):
      self._request = request
      self.parsers = parsers or ()
      self.negotiator = negotiator or self._default_negotiator()
      self.parser_context = parser_context
      self.parser_context["request"] = self
      self.parser_context["encoding"] = request.encoding or settings.DEFAULT_CHARSET

   def _parse(self):
      # 读取请求者的Content-Type请求头
      media_type = self.content_type
      try:
         # 请求发来的原始数据
         stream = self.stream
      except RawPostDataException:
         if not hasattr(self._request, "_post"):
            raise
         if self._supports_form_parsing():
            return (self._request.POST, self._request.FILES)
         stream = None
      
      if stream is None or media_type is None:
         if media_type and is_form_media_type(media_type):
            empty_data = QueryDict("", encoding=self._request._encoding)
         else:
            empty_data = {}
         empty_files = MultiValueDict()
         return (empty_data, empty_files)
      # 获取解析器
      parser = self.negotiator.select_parser(self, self.parsers)

      if not parser:
         raise exceptions.UnsupportedMediaType(media_type)
      try:
         # 做解析
         # JSONParser -> json.load
         # FormParser -> 直接使用django中的QueryDict
         parsed = parser.parse(stream, media_type, self.parser_context)
      except Exception:
         self._data = QueryDict("", encoding=self._request._encoding)
         self._files = MultiValueDict()
         self._full_data = self._data
         raise
      try:
         return (parsed.data, parsed.files)
      except AttributeError:
         empty_files = MultiValueDict()
         return (parsed, empty_files)

   def _load_data_and_files(self):
      if not _hasattr(self, "_data"):
         self._data, self._files = self._parse()
         if self._files:
            self._full_data = self._data.copy()
            self._full_data.update(self._files)
         else:
            self._full_data = self._data
         if is_form_media_type(self.content_type):
            self._request._post = self.POST
            self._request._files = self.FILES 

   @property
   def data(self):
      if not _hasattr(self, "_full_data"):
         self._load_data_and_files()
      return self._full_data


class APIView(View):
   def initial(self, request, *args, **kwargs):
      self.format_kwarg = self.get_format_suffix(**kwargs)
      neg = self.perform_content_negotiation(request)
      request.accepted_renderer, request.accepted_media_type = neg
      version, scheme = self.determine_version(request, *args, **kwargs)
      request.version, request.versioning_scheme = version, scheme
      self.perform_authentication(request)
      self.check_permissions(request)
      self.check_throttles(request)


   def get_parser_context(self, http_request):
      return {
         "view": self,
         "args": getattr(self, "args", ()),
         "kwargs": getattr(self, "kwargs", {})
      }

   def initialize_request(self, request, *args, **kwargs):
      # {视图对象, URL路由参数}
      parser_context = self.get_parser_context(request)

      return Request(
         request, # Django的request
         parsers=self.get_parsers(), # 获取解析器列表 [JSONParser, FormParser]
         authenticators=self.get_authenticators(), # 获取认证组件列表
         negotiator=self.get_content_negotiator(), # DefaultContentNegotiation
         parser_context=parser_context # {视图对象, URL路由参数, drf的request对象, encoding}
      )

   def dispatch(self, request, *args, **kwargs):
      self.args = args
      self.kwargs = kwargs
      request = self.initialize_request(request, *args, **kwargs)
      self.request = request
      self.headers = self.default_response_headers
      try:
         self.initial(request, *args, **kwargs)
         response = handler(request, *args, **kwargs)
      except Exception as exc:
         response = self.handle_exception(exc)
      self.response = self.finalize_response(request, response, *args, **kwargs)
      return self.response
```

#### 文件解析器

1. `views.py`

   ```python
   from rest_framework.views import APIView
   from rest_framework.response import Response
   from rest_framework.parsers import FileUploadParser


   class FileView(APIView):
      parser_classes = [FileUploadParser,] 
      def post(self, request):
         print(request.content_type)
         print(request.data)
         
         file_obj = request.data.get("file")
         with open(file_obj.name, mode="wb") as target_file_obj:
               for chunk in file_obj:
                  target_file_obj.write(chunk)
               file_obj.close()
         return Response("file")
   ```

2. 访问
   - 访问方式：`POST`
   - 访问设置
     - 请求头：`{"Content-Disposition": "attachment;filename=upload.jpg", "Content-Type": "*/*"}`
     - 请求体：Body-binary-选择要上传的图片

#### 复合解析器

1. `views.py`

   ```python
   from rest_framework.views import APIView
   from rest_framework.response import Response
   from rest_framework.parsers import MultiPartParser

   class MultiView(APIView):
      parser_classes = [MultiPartParser, ]

      def post(self, request):
         print(request.content_type)
         print(request.data)
         file_obj = request.data.get("img")
         with open(file_obj.name, mode="wb") as target_file_obj:
               for chunk in file_obj:
                  target_file_obj.write(chunk)
               file_obj.close()
         return Response("Multi")
   ```

2. 访问
   - 访问方式：`POST`
   - 访问设置：Body-"form-data"
   - 参数设置：`{"img": "选择文件", "name": "zhangsan"}`

### 序列化器

将ORM获取的数据库QuerySet或数据对象序列化成JSON格式，并对请求数据进行格式校验。

#### 元类

**在Python中，元类（metaclass）是用来创建类的类。元类可以控制类的创建过程，并且可以自定义类的行为和特性。**
一般情况下，使用关键字`class`来定义一个类。这个类的类型是`type`，也就是说，**`type`是所有类的元类。**
元类可以通过继承`type`类或实现`type`类的子类来定义。当创建一个类时，解释器会检查该类是否指定了一个元类，如果没有指定，解释器会使用默认的元类`type`来创建类。
元类最常见的**使用场景**是在框架和库中对类的行为进行定制。

以下是元类的一些特点和用法：

1. **类型检查**：元类可以通过重写`__new__`或`__init__`方法，在类被创建时对类的定义进行自定义处理，例如检查类的属性和方法是否符合要求。
2. **动态修改类**：元类可以在类定义阶段动态地修改类的属性、方法或增加新的属性、方法。
3. **类注册**：元类可以用于实现类的注册机制，当定义一个类时，元类可以将该类注册到某个注册表中，以便后续的查找和调用。
4. **单例模式**：元类可以控制类的实例化过程，从而实现单例模式等特殊的对象创建方式。

```python
# 定义一个自定义元类 MyMeta
class MyMeta(type):
   def __new__(cls, name, bases, attrs):
      # 为所创建的类 MyClass 添加了一个属性 my_attribute
      attrs['my_attribute'] = 'Hello, world!'
      return super().__new__(cls, name, bases, attrs)

class MyClass(metaclass=MyMeta):
   pass

obj = MyClass()
# 当实例化`MyClass`之后，可以通过访问`my_attribute`属性来获取元类添加的属性值。
print(obj.my_attribute)  # 输出 'Hello, world!'
```

需要注意的是，元类是高级特性，在大部分情况下并不需要直接使用元类。大多数情况下，使用类装饰器、类继承或其他Python提供的特性即可满足需求。元类的使用需要谨慎，并且要理解其对类创建和行为的影响。

创建类的两种方式：

```python
class Foo1(object):
   v1 = 123

   def func(self):
      return 234

# type(类名, 父类, 成员)
Foo2 = type("Foo", (object, ), {"v1": 123, "func": lambda self: 234})

obj1 = Foo1()
obj2 = Foo2()
print(obj1.v1, obj2.v1) # 123 123
print(obj1.func(), obj2.func()) # 234 234
```

元类：

1. 基于类可以实例化对象。-> 类()
2. type也可以创建类（默认）。
   - 默认 type

      ```python
      class type(object):
         def __init__(self):
            # 在空值初始化数据
            pass

         def __new__(self):
            # 创建类
            pass
      ```

   - 自定义 继承type

      ```python
      class MyType(type):
         def __new__(self):
            super().__new__()
      ```

   - 自定义创建元类

      ```python
      class MyType(type):
         def __new__(cls, *args, **kwargs):
            xx = super().__new__(cls, *args, **kwargs)
            print("创建类", xx) # 创建类 <class "__main__.Foo">
            return xx


      Foo = MyType("Foo", (object, ), {"v1": 123, "func":lambda self: 456})
      print(Foo) # <class "__main__.Foo">
      ```

      ```python
      # 创建自己的type
      class MyType(type):
         def __init__(cls, *args, **kwargs):
            print(2) # 后执行__init__()
            super().__init__(cls)

         def __new__(cls, name, bases, attrs):
            print(1) # 先执行__new__()

            print(name) # Foo
            print(bases) # (<classes 'object'>, )
            print(attrs) # {'__module__': '__main__', '__qualname__': 'Foo', 'v1': 123, 'func': <function Foo.func at 0x7fc1700670d0>}
            # 在创建类之前可以对元类中的元素进行操作
            del attrs["v1"]
            attrs["index"] = "1"

            class_name = super().__new__(cls, name, bases, attrs)
            print("创建类：", class_name)
            return class_name


      # 基于自定义的MyType创建类
      class Foo(object, metaclass=MyType):
         v1 = 123

         def func(self):
            return 456

      # 实例化后可以根据修改后的进行访问
      print(Foo.func)
      print(Foo.index)
      ```

   - 一旦某个类中指定了`metaclass`，则其所有子类，都继承该特性，由`metaclass`指定的`type`创建。

      ```python
      class MyType(type):
         def __new__(cls, name, bases, attrs):
            print(name, bases, attrs)
            class_name = super().__new__(cls, name, bases, attrs)
            return class_name

      class Base(object, metaclass=MyType):
         # Base (<classes 'object'>, ) {'__module__': '__main__', '__qualname__': 'Base'}
         pass

      class Foo(Base):
         # Foo (<classes '__main__.Base'>, ) {'__module__': '__main__', '__qualname__': 'Foo'}
         pass
      ```

```python
class MyType(type):
   def __new__(cls, name, bases, attrs):
      print(name)
      return super().__new__(cls, name, bases, attrs)

   def __call__(cls, *args, **kwargs):
      print("执行type的call")
      obj = cls.__new__(cls, *args, **kwargs)
      print("---")
      cls.__init__(cls, *args, **kwargs)
      return obj

class Base(object, metaclass=MyType):
   def __init__(self):
      print("初始化")

   def __new__(cls, *args, **kwargs):
      print("实例化类的对象")
      return object.__new__(cls)

obj = Base()

"""输出：
Base
执行type的call
实例化类的对象
---
初始化
"""
```

1. `Base`类是由`MyType`创建出来的，其本质是`MyType`类的实例化对象
2. 当实例化一个类的对象时（在类名后加`()`执行），会调用类中的`__call__()` 方法。
3. 继承了哪个类，实例化对象时，就会执行那个类中的`__call__()` 方法。

#### 元类和基类

在Python中，元类（metaclass）和基类（base class）是两个不同的概念，它们分别用于控制类和实例的创建行为。

1. 元类（Metaclass）：
   - 元类是用来创建类的类。在Python中，可以通过定义元类来自定义类的创建过程、行为和属性。
   - 元类通过继承`type`类或实现`type`类的子类来定义。在类定义时，可以使用`metaclass`参数指定元类。
   - 元类的主要作用是控制类的创建过程，并可以在类被创建时对类的定义进行自定义处理，例如检查类的属性和方法是否符合要求，动态修改类的属性和方法，实现类的注册机制等。
   - 一般情况下，我们不需要直接使用元类，它是一个高级特性，只有在框架、库或需要对类的行为做特殊处理的场景下才会使用元类。

2. 基类（Base Class）：
   - 基类是类的父类，也称为超类。在Python中，所有的类都继承自一个基类，通常是`object`类。
   - 基类提供了一些基本的方法和属性，这些方法和属性是所有对象都具备的通用行为，例如`__str__()`、`__repr__()`、`__len__()`等。
   - 我们可以通过继承基类来获得这些通用行为，并且可以在子类中进行自定义实现，或者添加新的方法和属性。

区别：

- 元类是用于创建类的类，它控制类的创建过程，可以对类进行定制化处理，例如添加、修改或检查类的属性和方法。
- 基类是类的父类，它提供了一些基本的方法和属性，用于通用的对象行为。通过继承基类，子类可以获得这些通用行为。

总结：

- 元类用于控制类的创建过程，可以自定义类的行为和特性。
- 基类是类的父类，提供了通用的对象行为和属性。

在Python中，`type`是一个内置类，也是所有类的元类。它充当了创建类的工厂，可以用来动态创建类对象。

`type`类有两个主要的作用：作为类实例的类型检查器和作为类的构造函数。

1. 类型检查器：
   - 对于已经创建的对象，我们可以使用`type(obj)`来获取该对象的类型。
   - 例如，`type(5)`返回`<class 'int'>`，表示整数对象的类型是 `int`。

2. 类的构造函数：
   - 可以使用`type(name, bases, attrs)`的形式来动态地创建一个类，并指定类的名称、基类和属性。
   - 在传入参数`bases`时，可以指定类的继承关系，可以是一个类，也可以是一个包含多个类的元组。
   - 在传入参数`attrs`时，可以指定类的属性和方法，以字典的形式传入。
   - 例如，`MyClass = type('MyClass', (BaseClass,), {'attr': 123})`会创建一个名为`MyClass`的类，该类继承自`BaseClass`，并具有一个名为`attr`的属性。

`object`是所有类的基类，它是Python中所有类的超类，默认继承关系如下：

```shell
class object:
    ...
```

`object`类提供了一些基本的方法和属性，它们是所有对象都具备的通用行为。

一些常用的`object`类提供的方法和属性包括：

- `__str__()`：返回对象的字符串表示。可以通过重写该方法来自定义打印对象时的输出。
- `__repr__()`：返回对象的字符串表示，通常用于调试目的。可以通过重写该方法来自定义在交互式环境中显示对象的输出。
- `__len__()`：返回对象的长度。可以通过重写该方法让对象支持`len()`函数调用。
- `__getitem__(self, key)`和`__setitem__(self, key, value)`：用于获取和设置对象的索引值。可以通过重写这些方法来实现自定义的容器类型。
- `__call__(self, *args, **kwargs)`：使对象能够像函数一样被调用，可以通过重写该方法让对象具备函数的行为。

除了上述提到的功能，`object`类还提供了其他许多方法，比如`__eq__()`、`__hash__()`等，它们可以被子类继承或者重写，以实现对象的特定行为。

需要注意的是，在Python 3中，所有的类都默认继承自`object`类，因此当我们创建一个新类时，它已经隐式地继承了`object`类的方法和属性。

#### 序列化器的概念

序列化器是一种用于将复杂的数据结构，如对象或数据模型，转换成可传输或持久化存储的格式的工具。它将数据转换为可以在网络上进行传输、在文件中存储或在数据库中保存的格式。
序列化器的主要目标是将数据转换为一种通用、可被多种技术和平台支持的格式，例如JSON（JavaScript Object Notation）或XML（eXtensible Markup Language）。这样，无论使用什么编程语言、框架或平台，都可以轻松地对数据进行解析和处理。

通常，序列化器提供以下功能：

1. **将复杂数据结构转换为可传输格式**：通过序列化器，可以将对象、数据模型或其他数据结构转换为JSON、XML等格式，以便在网络上进行传输。
2. **反向操作（反序列化）**：序列化器还可以执行相反的操作，即将接收到的数据转换为原始的数据结构，以便进行处理或持久化存储。
3. **数据验证和转换**：序列化器经常提供数据验证和转换的功能。它可以定义字段的规则、类型、验证器等，以确保输入数据的有效性和一致性。
4. **处理关联关系和嵌套对象**：序列化器通常支持处理复杂的关联关系和嵌套对象。它可以将相关对象嵌套在一起，并递归地对它们进行序列化和反序列化。
5. **自定义字段表示**：序列化器允许自定义字段的表示方式。例如，可以指定某个字段在序列化为JSON时使用特定的名称、格式或转换函数。

通过使用序列化器，可以轻松地在不同的系统、平台和技术之间进行数据交换和共享，而不必担心复杂数据结构的处理和转换。常见的Python序列化器库包括`json`模块、`pickle`模块和第三方库如`PyYAML`、`Marshmallow`等。

#### 序列化器和解析器

序列化器和解析器是紧密相关的概念，它们通常一起使用。虽然两者有些相似之处，但它们在功能和用途上有所不同。
序列化器用于将数据转换为可传输或持久化存储的格式，例如将对象转换为JSON字符串。而解析器则用于将已经序列化的数据反向解析，将其转换回原始的数据结构。
简而言之，序列化器是将数据转换为特定格式的工具，而解析器是将格式化的数据解析回原始数据的工具。
在使用序列化器和解析器时，通常的流程是：先使用序列化器将数据转换为所需的格式，然后在需要时使用解析器将格式化的数据转换回原始数据结构。这种双向的转换过程可以使数据在不同系统、平台和技术之间进行交换和共享。
例如，在客户端-服务器应用程序中，客户端可以使用序列化器将用户输入的数据转换为JSON格式，然后通过网络发送给服务器。服务器接收到JSON数据后，可以使用解析器将其转换为原始的数据结构，以便进行后续处理或存储到数据库中。
常见的Python库，如`json`，提供了序列化器和解析器的功能，让开发者可以方便地进行数据的序列化和反序列化操作。

#### DRF中的序列化器

DRF中的序列化器是一个重要的组件，它主要用于处理HTTP请求和响应中的数据。 DRF的设计目标是提供一种简单、可扩展、灵活、高性能的方法来操作RESTful API，因此序列化器在DRF中占据着非常重要的地位。
序列化器为复杂的Python对象提供了一种通用的方式，以便将其序列化为JSON、XML等格式。它可以将整个对象或对象中指定的字段序列化为所需的输出格式，并提供相应的验证和数据转换功能。
DRF提供了两种类型的序列化器：

1. **基于类的序列化器（Class-based serializers）**：基于类的序列化器是最常用的类型。开发者可以定义一个类，并继承DRF提供的`Serializer`类或`ModelSerializer`类，然后通过定义类中的属性和方法来控制序列化器的行为。
2. **函数式序列化器（Function-based serializers）**：函数式序列化器是一种轻量级的序列化器类型。它由几个函数组成，这些函数接受原始数据并返回序列化后的数据。使用函数式序列化器时，开发者需要手动处理序列化和反序列化过程，并实现自定义验证和数据转换逻辑。
无论使用哪种类型的序列化器，在DRF中，序列化器都是非常强大和灵活的工具，可以满足各种不同场景下的数据处理需求。通过序列化器，我们可以轻松地将Python对象序列化为JSON格式，并根据需要自定义特定字段的输出格式、验证器以及其他相关功能。

#### 序列化器的使用

序列化：

- Serializer
- ModelSerializer
- source处理 choices、datetime、foreignkey等
- 自定义字段
- 嵌套类处理foreignkey、manytomany
- 继承：写一个继承自`serializers.ModelSerializer`的类，自定义字段，在视图函数中同时继承自定义类和`serializers.ModelSerializer`，则可以使用自定义类中定义的字段

1. `models.py`

   ```python
   from django.db import models


   class Department(models.Model):
      department_name = models.CharField(verbose_name="部门名称", max_length=32)
      employees_num = models.IntegerField(verbose_name="人数")


   class Tag(models.Model):
      caption = models.CharField(verbose_name="标签", max_length=32)


   class EmployeeInfo(models.Model):
      name = models.CharField(verbose_name="姓名", max_length=32)
      age = models.IntegerField(verbose_name="年龄")
      gender = models.SmallIntegerField(
         verbose_name="性别", choices=((1, "男"), (2, "女")))
      department = models.ForeignKey(
         verbose_name="所属部门", to="Department", on_delete=models.CASCADE)
      # ManyToManyField表示多对多关系，用于建立两个模型之间的多对多关联关系。这里表示：EmployeeInfo模型和Tag模型之间存在多对多关系，一个员工可以拥有多个标签，一个标签也可以被多个员工拥有。
      tags = models.ManyToManyField(verbose_name="标签", to="Tag")
      ctime = models.DateTimeField(verbose_name="创建时间", auto_now_add=True)
   ```

2. `views.py`

   ```python
   from rest_framework.views import APIView
   from rest_framework.response import Response
   from rest_framework import serializers
   from api import models

   # 基于serializers.Serializer的序列化器
   # class DepartSerializer(serializers.Serializer):
   #     department_name = serializers.CharField()
   #     employees_num = serializers.IntegerField()


   # 基于serializers.ModelSerializer序列化器
   class DepartSerializer(serializers.ModelSerializer):
      class Meta:
         model = models.Department
         fields = "__all__"


   class DepartView(APIView):
      def get(self, request, *args, **kwargs):
         # 1. 获取数据库中数据
         depart_obj = models.Department.objects.all().first()
         queryset = models.Department.objects.all()
         # 2. 使用序列化器将数据对象转换为JSON格式
         ser1 = DepartSerializer(instance=depart_obj)
         # 使用many=True参数，以支持序列化多个对象
         ser2 = DepartSerializer(instance=queryset, many=True)
         # print(ser.data) # 输出：{'department_name': '运维部', 'employees_num': 6}
         # 3. 返回给用户
         context = {"status": True, "data1": ser1.data, "data2": ser2.data}
         return Response(context)


   class TagSerializer(serializers.ModelSerializer):
      class Meta:
         model = models.Tag
         fields = "__all__"


   class EmployeeSerializer(serializers.ModelSerializer):
      # 字段的自定制
      # choices处理
      gender = serializers.CharField(source="get_gender_display")

      # 外键处理【方法1】
      # department = serializers.CharField(source="department.department_name")
      # 外键处理【方法2】
      department = DepartSerializer()

      # datetime处理
      ctime = serializers.DateTimeField(format="%Y-%m-%d")
      # 设置非数据库中包含的字段
      welcome = serializers.SerializerMethodField()
      # 处理ManyToMany数据类型【方法1】
      # tags = serializers.SerializerMethodField()
      # 处理ManyToMany数据类型【方法2】
      tags = TagSerializer(many=True)

      def get_welcome(self, obj):
         # get_字段名，返回什么，该字段的值就是什么
         return "欢迎：{}".format(obj.name)

      def get_tags(self, obj):
         queryset = obj.tags.all()
         result = [{"id": tag.id, "caption": tag.caption} for tag in queryset]
         return result

      class Meta:
         model = models.EmployeeInfo
         # 获取所有字段
         # fields = "__all__"
         # 获取指定字段
         fields = ["name", "age", "gender",
                     "department", "ctime", "welcome", "tags"]


   class EmployeeView(APIView):
      def get(self, request, *args, **kwargs):
         # models.EmployeeInfo.objects.all().update(ctime=datetime.now())
         queryset = models.EmployeeInfo.objects.all()
         ser = EmployeeSerializer(instance=queryset, many=True)
         context = {"status": True, "data": ser.data}
         return Response(context)
   ```

3. `urls.py`

   ```python
   from api import views

   urlpatterns = [
      # ...
      path("api/<str:version>/depart/", views.DepartView.as_view(), name="department"),
      path("api/<str:version>/employee/", views.EmployeeView.as_view(), name="employee"),
   ]
   ```

#### 补充：ManyToManyField 字段类型

`ManyToManyField`是Django框架中的一种字段类型，用于实现多对多关联关系。它适用于以下场景：

1. 多对多关系：当两个模型之间存在多对多的关联关系时，可以使用`ManyToManyField`来建立它们之间的连接。例如，在一个社交网络应用中，用户可以加入多个兴趣群组，而每个兴趣群组也可以有多个成员，这种多对多的关系可以通过`ManyToManyField`来表示和操作。
2. 中间表自动管理：使用`ManyToManyField`时，Django会自动创建一个中间表，用于跟踪和管理两个模型之间的多对多关系。该中间表记录了关联的外键信息，无需开发者手动创建和维护。这样，简化了开发者的工作，同时提供了灵活的数据查询和操作方式。
3. 多对多查询：使用`ManyToManyField`可以方便地进行多对多关联数据的查询。通过字段对象的属性，可以获取与当前对象相关联的另一个模型的对象集合。例如，可以轻松地获取某个对象所关联的所有对象或根据关联对象进行过滤查询。
4. 额外字段：`ManyToManyField`还可以包含额外的字段，用于存储关联关系的其他信息。这些额外字段可以通过设置`through`参数来添加到中间表中，并与多对多关联进行关联。这使得在关联关系中保存和查询额外的元数据变得非常方便。

需要注意的是，`ManyToManyField`并不适用于所有的多对多关系场景。如果多对多关系具有更复杂的结构或需要额外的逻辑处理，可能需要自行创建中间模型来代替`ManyToManyField`。但对于大多数简单的多对多关联关系，`ManyToManyField`提供了一种简洁而方便的方式来管理和操作数据。

#### DRF序列化器源码执行流程-概述

```python
class BaseSerializer(serializers.ModelSerializer):
   name = serializers.CharField(source="name")
   age = 12


class EmployeeSerializer(serializers.ModelSerializer, BaseSerializer):
   gender = serializers.CharField(source="get_gender_display")

   class Meta:
      model = models.EmployeeInfo
      fields = ["name", "age", "gender"]
```

1. 加载字段
   - 先将 `BaseSerializer` 所有的字段定义加载出来，汇总到 `BaseSerializer._declared_fields` 中，构造成一个字典：`BaseSerializer._declared_fields = {"name": 对象}`；
   - 然后将 `name` 这样的字段定义在类中删除；
   - 再加载 `EmployeeSerializer` 中的所有字段，与父类中的字段一起汇总到 `EmployeeSerializer._declared_fields` 中，构造成一个字典：`EmployeeSerializer._declared_fields = {"name": 对象, "gender": 对象}`
2. 序列化

   ```python
   queryset = models.UserInfo.objects.all()
   ser = UserSerializer(instance=queryset, many=True) # ListSerializer 对象（UserSerializer对象）
   db => queryset = [{"id":1, "name": "zhangsan", many=False}] # UserSerializer对象
   db => instance = {"id":1, "name": "zhangsan"} => UserSerializer
   ```

   `UserSerializer`是一个自定义的序列化器类，用于将模型类`models.UserInfo`对象序列化为JSON格式的数据，以便于前端展示和访问。
   首先，通过`models.UserInfo.objects.all()`获取了所有的用户数据，即一个QuerySet对象`queryset`。然后，通过`UserSerializer`类的构造函数将`queryset`作为参数传递给`instance`参数，并设置`many=True`表示序列化的是多个对象。
   接着，在将`queryset`序列化为JSON字符串时，Django Rest Framework会自动调用`UserSerializer`类的`to_representation`方法，该方法通过遍历每个对象，调用`UserSerializer`类的`to_representation`方法进行序列化，并返回一个包含所有对象序列化结果的List对象，也即`ListSerializer`对象。
   最后，`ListSerializer`对象再次通过调用`UserSerializer`类的`to_representation`方法，将每个对象序列化为JSON格式的数据，最终返回一个包含所有用户数据的JSON数组，如下：

   ```python
   [
      {"id":1, "name": "zhangsan"},
      {"id":2, "name": "lisi"},
      ...
   ]
   ```

序列化器的执行流程：

1. 首先，根据请求的方法和路由信息，Django Rest Framework中的视图函数（View）会从数据库中获取需要序列化的数据；
2. 然后，视图函数将这些数据交给序列化器进行处理。序列化器会根据定义的序列化规则，将模型类对象序列化为JSON或其他格式的数据；
3. 在执行序列化的过程中，序列化器会调用一系列的方法，对数据进行预处理、格式转换和类型转换等操作，并最终返回序列化后的结果；
4. 最后，视图函数将序列化后的数据返回给客户端，完成响应。

当序列化器对数据进行序列化时，涉及到的核心方法：

1. `to_representation()`：用于将模型对象序列化为特定格式的数据，如JSON、XML等。在执行序列化器时，Django Rest Framework会自动调用该方法，并且会遍历序列化器中定义的所有字段，对每个字段逐一执行该方法。该方法通常需要开发者根据具体的需求重写，例如可以进行数据转换、格式化等操作。
2. `to_internal_value()`：用于将请求提交的数据反序列化为模型对象。在处理POST/PUT等请求时，Django Rest Framework会在视图函数处理请求前，自动调用序列化器的`to_internal_value()`方法，将请求数据反序列化为模型对象，以便进行后续的验证、保存等操作。同时，该方法也可以进行格式验证、数据类型转换等操作，确保反序列化的结果符合要求。
3. `create()`和`update()`：用于在数据库中创建或更新模型对象。在视图函数处理POST/PUT等请求时，如果请求通过序列化器验证，那么视图函数可以直接调用序列化器的`save()`方法，将反序列化后的结果保存到数据库中。在执行`save()`方法时，序列化器会调用`create()`或`update()`方法，根据是否存在主键来判断是创建新对象还是更新已有对象。

#### DRF序列化器源码执行流程

1. 类中的对象实际要先于类创建，然后作为参数传递给类。当创建一个类时，实际上是执行了一个`Type`函数，`class1` 等效于 `class2`。

   ```python
   # class1
   class Foo(object, metaclass=MyType):
      v1 =123
      v2 =456


   # class2
   class MyType("Foo", (object, ), {"v1": 123, "v2":456})
   ```

步骤：

1. 运行Django项目，创建字段对象

   ```python
   class SerializerMethodField(Field):
      # 在使用时，需要定义一个名为 get_{field_name} 的方法，其中 {field_name} 是字段名，在这个方法中对需要返回的数据进行计算，并返回计算结果。
      def __init__(self, method_name=None, **kwargs):
         # __init__ 方法接受一个可选参数 method_name，用于指定调用的方法名，默认为 None。此外，还通过 kwargs 将 source='*' 和 read_only=True 添加到参数列表中，以设置源字段和只读属性。
         self.method_name = method_name
         kwargs['source'] = '*'
         kwargs['read_only'] = True
         super().__init__(**kwargs)

      def bind(self, field_name, parent):
         # bind 方法用于在字段绑定到父序列化器时进行操作。如果 method_name 为 None，则默认使用字段名生成方法名，即 method_name='get_{field_name}'。
         if self.method_name is None:
            self.method_name = 'get_{field_name}'.format(field_name=field_name)

         super().bind(field_name, parent)

      def to_representation(self, value):
         # to_representation 方法用于将字段的值转换为其表示形式。它使用 getattr 函数根据 method_name 获取父序列化器上的方法，并将字段的值作为参数传递给该方法，最后返回方法的执行结果作为字段的表示形式。
         method = getattr(self.parent, self.method_name)
         return method(value)


   class Field:
      _creation_counter = 0

      def __init__(self, *, read_only=False, write_only=False,
                  required=None, default=empty, initial=empty, source=None,
                  label=None, help_text=None, style=None,
                  error_messages=None, validators=None, allow_null=False):
         self._creation_counter = Field._creation_counter
         Field._creation_counter += 1

      def bind(self, field_name, parent):
         # 在字段实例添加到父类序列化器实例时，初始化字段名、父类以及一些相关属性，包括字段名与来源属性的关系、显示名称的设置以及来源属性的解析。并对冗余的 source 参数进行了检查。
         # 首先检查是否存在冗余的 source 参数。如果 self.source 和传入的 field_name 相同，即指定了冗余的来源属性，会抛出异常，提醒用户移除 source 关键字参数。
         assert self.source != field_name, (
            "It is redundant to specify `source='%s'` on field '%s' in "
            "serializer '%s', because it is the same as the field name. "
            "Remove the `source` keyword argument." %
            (field_name, self.__class__.__name__, parent.__class__.__name__)
         )

         # 设置字段实例的 field_name 属性为传入的 field_name ，将字段实例的 parent 属性设置为传入的 parent 。
         self.field_name = field_name
         self.parent = parent

         # 如果字段实例的 label 为 None ，则将其设置为根据字段名转换而来的名称（将下划线替换为空格，并将首字母大写）。
         if self.label is None:
            self.label = field_name.replace('_', ' ').capitalize()

         # 如果字段实例的 source 为 None ，则将其设置为传入的 field_name 。
         if self.source is None:
            self.source = field_name

         # ！根据 source 的值，将其拆分为 source_attrs 列表。如果 source 为 '*' ，则 source_attrs 为空列表，否则将 source 字符串按照点号进行切割。
         if self.source == '*':
            self.source_attrs = []
         else:
            self.source_attrs = self.source.split('.')

      def get_attribute(self, instance):
         # 从模型实例对象中获取字段的原始值。
         try:
            # ！首先尝试调用 get_attribute() 函数，将模型实例对象和字段的源属性传递给它，并返回结果。
            return get_attribute(instance, self.source_attrs)
         # 如果在调用过程中捕获到 BuiltinSignatureError 异常，说明字段的源属性映射到了内置函数类型并且是无效的。此时，会抛出异常并提供相应的错误信息。
         except BuiltinSignatureError as exc:
            msg = (
                  'Field source for `{serializer}.{field}` maps to a built-in '
                  'function type and is invalid. Define a property or method on '
                  'the `{instance}` instance that wraps the call to the built-in '
                  'function.'.format(
                     serializer=self.parent.__class__.__name__,
                     field=self.field_name,
                     instance=instance.__class__.__name__,
                  )
            )
            raise type(exc)(msg)
         # 如果在调用过程中捕获到 KeyError 或者 AttributeError 异常，说明未能找到相应的属性或键。这时会进行以下判断：
         except (KeyError, AttributeError) as exc:
            # 如果字段有默认值 (default is not empty)，则返回字段的默认值。
            if self.default is not empty:
                  return self.get_default()
            # 如果可以允许空值 (allow_null=True)，则返回 None。
            if self.allow_null:
                  return None
            # 如果字段没有指定 required=False，即必填项，则抛出 SkipField 异常。
            if not self.required:
                  raise SkipField()
            # 如果以上情况都不满足，会抛出异常，并提供相应的错误信息。
            msg = (
                  'Got {exc_type} when attempting to get a value for field '
                  '`{field}` on serializer `{serializer}`.\nThe serializer '
                  'field might be named incorrectly and not match '
                  'any attribute or key on the `{instance}` instance.\n'
                  'Original exception text was: {exc}.'.format(
                     exc_type=type(exc).__name__,
                     field=self.field_name,
                     serializer=self.parent.__class__.__name__,
                     instance=instance.__class__.__name__,
                     exc=exc
                  )
            )
            raise type(exc)(msg)

   class CharField(Field):
      def __init__(self, **kwargs):
         self.allow_blank = kwargs.pop('allow_blank', False)
         self.trim_whitespace = kwargs.pop('trim_whitespace', True)
         self.max_length = kwargs.pop('max_length', None)
         self.min_length = kwargs.pop('min_length', None)
         super().__init__(**kwargs)

      def to_representation(self, value):
         return str(value)


   class IntegerField(Field):
      def __init__(self, **kwargs):
         self.max_value = kwargs.pop('max_value', None)
         self.min_value = kwargs.pop('min_value', None)
         super().__init__(**kwargs)

      def to_representation(self, value):
         return int(value)

   # 自定义类
   class UserSerializer(serializers.ModelSerializer):
      name = serializers.CharField(source="name")
      age = serializers.IntegerField(source="age")
      gender = serializers.CharField(source="get_gender_display")
   ```

   由于 `CharField` 和 `IntegerField` 继承了同一个父类 `Field`，且三个在同一个类中定义的字段共用一个局部环境，所以它们使用同一个`_creation_counter` 变量。
   当执行了 `name`行时，`name` 被初始化为一个字典对象，其中继承了父类的 `_creation_counter`，其值为 `{..., "_creation_counter": 0}`。
   执行到 `age` 行时，`age`被初始化为一个字典对象，其中继承了父类的 `_creation_counter`，但由于父类中对其执行了自增1，则其值为 `{..., "_creation_counter": 1}`。
   到 `gender` 其值为 `{..., "_creation_counter": 2}`。
   在后续开发中，**可以按编写顺序来确定各个字段在源码中的处理顺序。**
   不同的`Field`方法，在类中定义了 `to_representation` 方法将数据处理成对应的数据类型，作为`value` 返回。
2. 创建类（利用metaclass）

   ```python
   class SerializerMetaclass(type):
      @classmethod
      def _get_declared_fields(cls, bases, attrs):
         # for field_name, obj in list(attrs.items()) 对类里所有成员循环， if isinstance(obj, Field) 并判断该成员对象是否由 Field 或 继承了 Field 的类创建，筛选出其中的字段， (field_name, attrs.pop(field_name)) 将该成员对象从attrs（类成员）中移除，并将字段名与该成员对象构造成一个元组，赋值给fields
         fields = [(field_name, attrs.pop(field_name)) for field_name, obj in list(attrs.items()) if isinstance(obj, Field)]
         # 对fields中的元组基于第一个元素的_creation_counter值进行排序
         fields.sort(key=lambda x: x[1]._creation_counter)

         # 解决字段定义重名的问题
         # class C(A, B), and A and B both define 'field', use 'field' from A.
         known = set(attrs)
         def visit(name):
            known.add(name)
            return name

         # 获取父类中的字段对象，并构造成元组
         base_fields = [
            (visit(name), f)
            # 相当于嵌套循环
            for base in bases if hasattr(base, '_declared_fields')
            for name, f in base._declared_fields.items() if name not in known
         ]

         # [父类字段元组, ] + [自定义Serializer类字段元组]，并转换为有序字典
         return OrderedDict(base_fields + fields)

      def __new__(cls, name, bases, attrs):
         attrs('_declared_fields') = cls._get_declared_fields(bases, attrs) # {自己的字段对象 + 父类的字段对象}
         return super().__new__(cls, name, bases, attrs)

   # 自定义元类
   class SerializerMetaclass(type):
      # 在定义 Serializer 子类时，自动将整数类型的属性从类属性字典中移除，并存储在 _declared_fields 类属性字典中。
      def __new__(cls, name, bases, attrs):
         data_dict = {}
         # 在循环遍历类属性字典时，判断每个属性值是否为整数类型。如果是，则将该属性从 attrs 字典中弹出并加入到 data_dict 字典中。
         for k, v in list(attrs.items()):
            if isinstance(v, int):
               data_dict[k] = attrs.pop(k)
         # 最后，将 data_dict 字典赋值给 _declared_fields 类属性，并通过调用 super() 方法创建并返回类对象。
         attrs['_declared_fields'] = data_dict
         return super().__new__(cls, name, bases, attrs)

   class BaseSerializer(object):
      pass

   class Serializer(BaseSerializer, metaclass=SerializerMetaclass):
      pass

   class ModelSerializer(Serializer):
      pass

   class UserSerializer(serializers.ModelSerializer):
      name = serializers.CharField(source="name")
      age = serializers.IntegerField(source="age")
      gender = serializers.CharField(source="get_gender_display")

      class Meta:
         model = models.employee
         fields = "__all__"
   ```

3. 用户请求到来，数据库获取数据 + 序列化类
   1. `many=False` 得到 `UserSerializer()`对象
   2. `many=True` 得到一个实例化的 `ListSerializer(obj = UserSerializer(),)`以便后续的循环
   3. 源码：

      ```python
      # 自定义类
      class SerializerMetaclass(type):
         pass

      class BaseSerializer(object):
         # 这里的__init__是初始化当前类的方法
         def __init__(self, instance=None, data=empty, **kwargs):
            self.instance = instance
            if data is not empty:
               self.initial_data = data
            self.partial = kwargs.pop('partial', False)
            self._context = kwargs.pop('context', {})
            kwargs.pop('many', None)
            super().__init__(**kwargs)

         # 这里的__new__是创建当前类的方法
         def __new__(cls, *args, **kwargs):
            if kwargs.pop('many', False):
               return cls.many_init(*args, **kwargs)
            return super().__new__(cls, *args, **kwargs)

         @classmethod
         def many_init(cls, *args, **kwargs):
            allow_empty = kwargs.pop('allow_empty', None)
            max_length = kwargs.pop('max_length', None)
            min_length = kwargs.pop('min_length', None)
            child_serializer = cls(*args, **kwargs)
            list_kwargs = {
               'child': child_serializer,
            }
            if allow_empty is not None:
               list_kwargs['allow_empty'] = allow_empty
            if max_length is not None:
               list_kwargs['max_length'] = max_length
            if min_length is not None:
               list_kwargs['min_length'] = min_length
            list_kwargs.update({
               key: value for key, value in kwargs.items()
               if key in LIST_SERIALIZER_KWARGS
            })
            meta = getattr(cls, 'Meta', None)
            list_serializer_class = getattr(meta, 'list_serializer_class', ListSerializer)
            return list_serializer_class(*args, **list_kwargs)

      @classmethod
         def many_init(cls, *args, **kwargs):
            child_serializer = cls(*args, **kwargs)
            meta = getattr(cls, 'Meta', None)
            list_serializer_class = getattr(meta, 'list_serializer_class', ListSerializer)
            return list_serializer_class(*args, **list_kwargs)

      class Serializer(BaseSerializer, metaclass=SerializerMetaclass):
         pass

      class ModelSerializer(Serializer):
         pass

      class UserSerializer(serializers.ModelSerializer):
         name = serializers.CharField(source="name")
         age = serializers.IntegerField(source="age")
         gender = serializers.CharField(source="get_gender_display")

         class Meta:
            model = models.employee
            fields = "__all__"
      ```

      `many_init()`：
      当 `Serializer` 对象被设置为 `many=True` 时，就会返回一个列表序列化器 `ListSerializer` 对象，该方法也用于生成该对象。
      1. 该方法接收变量 `cls`、`*args`、`**kwargs`，`cls` 表示当前的类对象，`*args` 和 `**kwargs` 分别表示位置参数和关键字参数。
      2. 该方法首先从关键字参数中弹出 `allow_empty`、`max_length` 和 `min_length`，然后创建一个子序列化器对象 `child_serializer`。
      3. 接着，将 `child_serializer` 对象作为一个参数传递给 `ListSerializer` 类构造函数，并将 `allow_empty`、`max_length`、`min_length` 等参数加入到 `list_kwargs` 字典中。
      4. 如果关键字参数中还有其他不属于列表序列化器 `ListSerializer` 的参数，则加入到 `list_kwargs` 字典中。
      5. 接着通过 `meta` 获取 `ListSerializer` 类中的类属性 `list_serializer_class` 或获取默认的 `ListSerializer` 类，最后以 `args` 和 `list_kwargs` 参数创建一个 `ListSerializer` 对象并返回。
      6. 补充：`list_kwargs.update({key: value for key, value in kwargs.items() if key in LIST_SERIALIZER_KWARGS})`：从字典 `kwargs` 中获取键为 `LIST_SERIALIZER_KWARGS` 中的键的值配置到 `list_kwargs` 字典中。
4. 通过 `ser.data` 触发序列化-当前类

   ```python
   class SerializerMetaclass(type):
      pass

   class BaseSerializer(object):
      @property # @property 装饰器将该方法转化为只读属性，即可以像访问类属性一样通过 serializer.data 的方式获取数据。
      def data(self):
         # 用于获取序列化后的数据。
         # 判断是否有传入 data 关键字参数并且还未进行过验证。如果有，则抛出异常提示用户必须先调用 .is_valid() 进行数据验证再访问 .data 属性。
         if hasattr(self, 'initial_data') and not hasattr(self, '_validated_data'):
            msg = (
               'When a serializer is passed a `data` keyword argument you '
               'must call `.is_valid()` before attempting to access the '
               'serialized `.data` representation.\n'
               'You should either call `.is_valid()` first, '
               'or access `.initial_data` instead.'
            )
            raise AssertionError(msg)
         # 如果当前序列化器实例已经缓存了 _data 属性，则直接返回 _data 属性。
         # 否则，根据当前序列化器实例对象的状态，获取相应的序列化数据
         if not hasattr(self, '_data'):
            # 如果实例已经有绑定的模型对象 instance 并且没有错误信息 _errors，则通过 to_representation() 方法将 instance 对象序列化成数据。
            if self.instance is not None and not getattr(self, '_errors', None):
               # to_representation 提供核心的序列化功能
               self._data = self.to_representation(self.instance)
            # 如果已经经过校验且没有错误信息 _errors，则通过 to_representation() 方法将已经验证的数据 validated_data 序列化成数据。
            elif hasattr(self, '_validated_data') and not getattr(self, '_errors', None):
               self._data = self.to_representation(self.validated_data)
            else:
               # 否则，通过 get_initial() 方法获取初始化数据并进行序列化。
               self._data = self.get_initial()
         # 最后将生成的 _data 缓存在实例的属性中，供下次访问使用，并返回 _data。
         return self._data

   class Serializer(BaseSerializer, metaclass=SerializerMetaclass):
      @property
      def data(self):
         ret = super().data # 调用父类的data
         return ReturnDict(ret, serializer=self)

      def get_fields(self):
         return copy.deepcopy(self._declared_fields)

      @cached_property
      def fields(self):
         fields = BindingDict(self)
         for key, value in self.get_fields().items():
            fields[key] = value
         return fields

      @property
      def _readable_fields(self):
         for field in self.fields.values():
            if not field.write_only:
               yield field

      def to_representation(self, instance):
         # 用于将模型实例对象转化为字典类型的基本数据类型。
         # 定义一个有序字典 ret，用于存储每个可读字段的值。
         ret = OrderedDict()

         # ！获取所有可读的字段：_declared_fields中的字段对象 + class Meta中的字段对象（包含给Meta字段创建对象的过程）
         # 可读的：没有 write_only参数的字段
         fields = self._readable_fields

         # _readable_fields 属性包含了所有可读取的字段，所以在循环遍历 _readable_fields 时，用 field 逐个获取可读字段。
         for field in fields:
            try:
               # 调用可读字段的 get_attribute() 方法获取当前模型实例对象的对应属性值，并将其赋值给变量 attribute。
               attribute = field.get_attribute(instance)
            # ！如果 get_attribute() 方法返回 SkipField 类型，则说明当前字段不能被序列化，直接进入下一次循环。
            except SkipField:
               continue

            # 如果 attribute 的值为 None，则直接将 None 赋给 ret 字典对应的键；
            check_for_none = attribute.pk if isinstance(attribute, PKOnlyObject) else attribute
            if check_for_none is None:
               ret[field.field_name] = None
            # ！否则，调用字段的 to_representation() 方法将 attribute 对象转化为字典类型的基本数据类型并存储到 ret 字典中。
            else:
               ret[field.field_name] = field.to_representation(attribute)
         # 循环结束后，将 ret 字典作为 to_representation() 方法的返回结果。
         return ret

   class ModelSerializer(Serializer):
      def get_fields(self):
         if self.url_field_name is None:
            self.url_field_name = api_settings.URL_FIELD_NAME

         assert hasattr(self, 'Meta'), (
            'Class {serializer_class} missing "Meta" attribute'.format(
                  serializer_class=self.__class__.__name__
            )
         )
         assert hasattr(self.Meta, 'model'), (
            'Class {serializer_class} missing "Meta.model" attribute'.format(
                  serializer_class=self.__class__.__name__
            )
         )
         if model_meta.is_abstract_model(self.Meta.model):
            raise ValueError(
                  'Cannot use ModelSerializer with Abstract Models.'
            )

         # 获取在类变量中定义的字段对象
         declared_fields = copy.deepcopy(self._declared_fields)
         model = getattr(self.Meta, 'model')
         depth = getattr(self.Meta, 'depth', 0)

         if depth is not None:
            assert depth >= 0, "'depth' may not be negative."
            assert depth <= 10, "'depth' may not be greater than 10."

         # 获取数据库中的所有字段
         info = model_meta.get_field_info(model)
         # 获取类变量中定义的字段名 + Meta类中定义的字段名
         field_names = self.get_field_names(declared_fields, info)

         # 确定应包含的任何额外字段参数和隐藏字段
         extra_kwargs = self.get_extra_kwargs()
         extra_kwargs, hidden_fields = self.get_uniqueness_extra_kwargs(
            field_names, declared_fields, extra_kwargs
         )

         # 确定序列化程序应包含的字段。
         fields = OrderedDict()

         for field_name in field_names:
            # 如果该字段是在类上显式声明的，则使用该字段。
            if field_name in declared_fields:
                  fields[field_name] = declared_fields[field_name]
                  continue

            extra_field_kwargs = extra_kwargs.get(field_name, {})
            source = extra_field_kwargs.get('source', '*')
            if source == '*':
                  source = field_name

            # 确定序列化程序字段类和关键字参数。
            field_class, field_kwargs = self.build_field(
                  source, info, model, depth
            )

            # 包括在 Meta.extra_kwargs 中定义的任何kwargs参数
            field_kwargs = self.include_extra_kwargs(
                  field_kwargs, extra_field_kwargs
            )

            # 创建序列化程序字段。
            fields[field_name] = field_class(**field_kwargs)

         # 添加任何隐藏字段。
         fields.update(hidden_fields)

         return fields

   class UserSerializer(serializers.ModelSerializer):
      name = serializers.CharField(source="name")
      age = serializers.IntegerField(source="age")
      gender = serializers.CharField(source="get_gender_display")

      class Meta:
         model = models.employee
         fields = "__all__"
   ```

5. 通过 `ser.data` 触发序列化-`ListSerializer`

   ```python
   class ListSerializer(BaseSerializer):
      # 在当前类的基础上多了一个循环
      def to_representation(self, data):
         iterable = data.all() if isinstance(data, models.Manager) else data
         return [
            self.child.to_representation(item) for item in iterable
         ]
   ```

#### 序列化器-数据校验

##### 序列化器之一些总结补充

序列化器：

1. 序列化
   - 序列化器的类
   - 路由 -> 视图 -> 去数据库获取对象或QuerySet -> 序列化器的类转换成列表、字典、有序字典 -> JSON处理 `ser = DepartSerializer(instance=request.data)` 这里是**对象**
2. 数据校验
   - 序列化器的类
   - 路由 -> 视图 -> request.data -> 校验（序列化器的类） -> 操作（db，序列化器的类） 这里是**数据**

   ```python
   # 基于Serializer
   ser = DepartSerializer(data=request.data)
   # 校验
   ser.validated_data
   # 保存
   models.Depart.objects.create(**ser.validated_data)

   # 基于ModelSerializer
   ser = DepartModelSerializer(data=request.data)
   ser.validated_data
   # 当DepartModelSerializer中定义的字段数 < models中要求的字段数时，可以通过ser.save(字段名=字段值)将该字段的值自动填充，可用于重复密码和用户id的携带
   ser.save()
   ```

3. 结合
   - 创建用户：`{"user":"zhangsan", "password": "pass123"}`
     - 校验（序列化器的类）
     - 数据库对象 = 连接数据保存
     - 再将新增的数据返回
       - 再次调用（序列化器的类），让它将新增的数据序列化：`{"user":"zhangsan", "password": "pass123"}` + 默认生成的数据

restful规范：

1. 获取数据：
   - `api/v1/user/` -> GET请求 -> 获取数据列表 `models.UserInfo.objects.all()`
   - `api/v1/user/2/` -> GET请求 -> 获取数据列表 `models.UserInfo.objects.filter(id=2).first()`
2. 新增数据：`api/v1/user/` -> POST请求
3. 更新数据：`api/v1/user/2/` -> PUT请求

数据校验实现：

1. 自定义 `Serializer` + 字段（内置 + 正则） + 字段钩子 + 全局钩子
2. 自定义 `ModelSerializer` + `extra_kwargs` + `save()`
   - 多了用`pop()`，少了`save()` 加参数
3. 自定义 `ModelSerializer` + FK -> 自动获取关联数据 `depart` -> `depart_id`
4. 自定义 `ModelSerializer` + M2M -> 自动获取关联数据 `ListField` 或 `DictField` + 钩子
5. `save()` 的返回值 `instance = ser.save()` 获取当前数据对象
6. 序列化返回：
   - 校验Serializer + 序列化Serializer

      ```python
      class UserView(APIView):
         def post(self, request, *args, **kwargs):
            ser = UserModelSerializer(data=request.data)
            if ser.is_valid():
               instance = ser.save()
               user_data = UserModelSerializer(instance=instance)
               return Response(user_data.data)
            else:
               return Response(ser.errors)
      ```

   - 校验和序列化用同一个Serializer：校验的字段与序列化的字段相同
   - 校验和序列化用同一个Serializer：校验的字段与序列化的字段不同
     - `read_only = True` 只在序列化时使用
     - `write_only = True` 只在校验时使用

```python
class DemoSerializer(serializers.ModelSerializer):
   # 获取gender元组中的内容，只用于展示
   gender_info = serializers.CharField(source="get_gender_display", read_only=True)
   gender_info1 = serializers.SerializerMethodField()
   # 获取foreign key字段内容，只用于展示
   depart_name = serializers.CharField(source="depart.depart_name", read_only=True)

   class Meta:
      model = models.Demo
      fields = ["id", "name", "age", "gender", "gender_info1", "gender_info"]
      extra_kwargs = {
         # 只在序列化时使用，不写入数据库，只展示
         "id": {"read_only": True},
         # 只在校验时使用，不展示，只写入数据库
         "gender": {"write_only": True},
      }

   
   def get_gender_info1(self, obj):
      return {"id": obj.gender, "text": obj.get_gender_display()}

class UserView(APIView):
   def post(self, request, *args, **kwargs):
      ser = UserModelSerializer(data=request.data)
      if ser.is_valid():
         ser.save()
         return Response(ser.data)
      else:
         return Response(ser.errors)
```

##### 内置校验

```python
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework import serializers


class DepartSerializer(serializers.Serializer):
    # required=True，该字段为必填字段
    username = serializers.CharField(required=True)
    password = serializers.CharField(required=True)


class DepartAddView(APIView):
    def post(self, request, *args, **kwargs):
        # 1. 获取原始数据
        # print(request.data)
        # 2. 校验-1
        # ser = DepartSerializer(data=request.data)
        # if ser.is_valid():
        #     print(ser.validated_data)
        # else:
        #     print(ser.errors)
        # return Response("DepartAdd")
        # 2. 校验-2
        ser = DepartSerializer(data=request.data)
        # 使用raise_exception=True，dispatch()中会捕获异常并进行处理
        ser.is_valid(raise_exception=True)
        print(ser.validated_data)
        return Response("DepartAdd")
```

##### 正则校验

```python
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework import serializers
from django.core.validators import RegexValidator, EmailValidator


class InfoSerializer(serializers.Serializer):
   title = serializers.CharField(required=True, max_length=20, min_length=6)
   order = serializers.IntegerField(
      required=False, max_value=100, min_value=10)
   level = serializers.ChoiceField(choices=[(1, "高级"), (2, "中级")])
   # email = serializers.EmailField()
   email = serializers.CharField(
      validators=[EmailValidator(message="邮箱格式错误")])
   more = serializers.CharField(
      validators=[RegexValidator(r"\d+", message="格式错误")])
   code = serializers.CharField()


class InfoView(APIView):
   def post(self, request):
      ser = InfoSerializer(data=request.data)
      if ser.is_valid():
         return Response(ser.validated_data)
      else:
         return Response(ser.errors)
```

##### 钩子校验

钩子校验（Hook Validation）是指在特定的时机对数据进行验证和处理的机制。在 Django REST framework（DRF）的序列化器中，钩子校验提供了一种灵活的方式来自定义字段级别或对象级别的验证逻辑。

DRF序列化器中的钩子校验主要通过下面两个方法来实现：

1. `validate_<field_name>()` 方法
   这个方法用于对特定字段进行验证。在对数据进行反序列化、验证和保存之前，会依次调用序列化器类中定义的 `validate_<field_name>()` 方法。可以在该方法中编写验证逻辑，并使用 `raise serializers.ValidationError()` 抛出异常来表示验证失败。

   ```python
   def validate_email(self, value):
       if 'example.com' not in value:
           raise serializers.ValidationError("Email domain must be example.com")
       return value
   ```

2. `validate()` 方法
   这个方法用于对整个对象进行验证。在对数据进行反序列化、验证和保存之前，会调用序列化器类中定义的 `validate()` 方法。可以在该方法中编写验证逻辑，并使用 `raise serializers.ValidationError()` 抛出异常来表示验证失败。

   ```python
   def validate(self, attrs):
       if attrs['start_date'] > attrs['end_date']:
           raise serializers.ValidationError("Start date must be before end date")
       return attrs
   ```

通过重写上述方法，可以在序列化器中增加自定义的验证逻辑。在校验发生错误时，可以使用 `serializers.ValidationError` 抛出异常，并在响应中返回相应的错误信息。钩子校验使得验证逻辑与序列化器解耦，提供了一种灵活的方式来实现数据校验和处理。

```python
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework import serializers
from rest_framework import exceptions


class InfoSerializer(serializers.Serializer):
   title = serializers.CharField(required=True, max_length=20, min_length=6)
   order = serializers.IntegerField(
      required=False, max_value=100, min_value=10)
   level = serializers.ChoiceField(choices=[(1, "高级"), (2, "中级")])

   # validate_字段名，对该字段进行钩子校验
   def validate_code(self, value):
      print(value)
      if len(value) > 6:
         raise exceptions.ValidationError("字段钩子校验失败")
      return value

   def validate(self, attrs):
      print("validate=", attrs)
      # api_settings.NON_FIELD_ERRORS_KEY
      # raise exceptions.ValidationError("全局钩子校验失败")
      return attrs


class InfoView(APIView):
   def post(self, request):
      ser = InfoSerializer(data=request.data)
      if ser.is_valid():
         return Response(ser.validated_data)
      else:
         return Response(ser.errors)
```

##### Model校验

```python
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework import serializers
from rest_framework import exceptions
from api import models
from django.core.validators import RegexValidator


class RoleSerializer(serializers.ModelSerializer):
   more = serializers.CharField(required=True)

   class Meta:
      model = models.Role
      fields = ["title", "order", "more"]
      extra_kwargs = {
         "title": {"validators": [RegexValidator(r"\d+", message="格式错误")]},
         "order": {"min_value": 5},
      }

   def validate_more(self, value):
      return value

   def validate(self, attrs):
      return attrs


class InfoView(APIView):
   def post(self, request):
      ser = RoleSerializer(data=request.data)
      if ser.is_valid():
         ser.validated_data.pop("more")
         instance = ser.save()
         print(instance)
         return Response(ser.validated_data)
      else:
         return Response(ser.errors)
```

##### 校验+保存+FK+M2M

```python
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework import serializers
from rest_framework import exceptions
from django.core.validators import RegexValidator
from datetime import datetime


class UserInfoSerializer(serializers.ModelSerializer):
   more = serializers.CharField(required=True)

   class Meta:
      model = models.UserInfo
      fields = ["name", "gender", "role", "tags", "more"]
      extra_kwargs = {
         "name": {"validators": [RegexValidator(r"n-\d+", message="格式错误")]},
      }
   
   # 要求在上述校验的基础上，部门只能选id >1的
   def validate_depart(self, value):
      if value.id > 1:
         return value
      raise exceptions.ValidationError("部门错误")

   # 对m2m数据进行二次处理
   def validate_tags(self, value):
      print(value, type(value)) # 这里的value是个列表
      return value

   def validate_more(self, value):
      return value

   def validate(self, attrs):
      return attrs


class InfoView(APIView):
   def post(self, request):
      ser = UserInfoSerializer(data=request.data)
      if ser.is_valid():
         ser.validated_data.pop("more")
         instance = ser.save(ctime=datetime.now())
         print(instance)
         return Response("Success")
      else:
         return Response(ser.errors)
```

由于 `ModelSerializer` 中的字段是根据 `models` 自动生成的，所以没有`foreign key` 的id字段，想用可以自行定义

```python
class UserInfoSerializer(serializers.ModelSerializer):
   depart_id = serializers.IntegerField()

   class Meta:
      model = models.UserInfo
      fields = ["name", "gender", "role", "depart_id", "tags", "more"]
```

##### 重自定义钩子-处理元组型数据

```python
class MyCharField(serializers.IntegerField):
   def __init__(self, method_name=None, **kwargs):
      self.method_name = method_name
      super().__init__(**kwargs)

   def bind(self, field_name, parent):
      if self.method_name is None:
         self.method_name = "xget_{field_name}".format(field_name=field_name)
      super().bind(field_name, parent)

   def get_attribute(self, instance):
      method = getattr(self.parent, self.method_name)
      return method(instance)

   def to_representation(self, value):
      return str(value)


class MyModelSerializer(serializers.ModelSerializer):
   gender = MyCharField()

   class Meta:
      model = models.UserInfo
      fields = ["id", "name", "age", "gender"]
      extra_kwargs = {
         "id": {"read_only": True}
      }

   def xget_gender(self, obj):
      return obj.get_gender_display()


class MyView(APIView):
   def post(self, request, *args, **kwargs):
      ser = MyModelSerializer(data=request.data)
      if ser.is_valid():
         ser.save()
         return Response(ser.data)
      else:
         return Response(ser.errors)
```

首先，定义了一个自定义字段类 `MyCharField`，它继承自 DRF 中的 `IntegerField` 类。该字段类具有以下功能：

1. `__init__` 方法接受一个可选参数 `method_name`，用于指定调用的方法名，默认为 `None`。然后调用父类的 `__init__` 方法初始化字段。
2. `bind` 方法在字段绑定到序列化器类时进行操作。如果 `method_name` 为 `None`，则默认使用字段名生成方法名，即 `method_name='xget_{field_name}'`。
3. `get_attribute` 方法用于获取字段的属性值，其中 `self.parent` 表示字段所属的序列化器对象，并通过 `getattr` 函数根据 `method_name` 获取父序列化器上的方法，并将该方法的执行结果作为字段的属性值返回。
4. `to_representation` 方法用于将字段的属性值转换为其表示形式，这里将其转换成字符串格式进行返回。
接下来，定义了一个自定义的模型序列化器 `MyModelSerializer`，它继承自 DRF 中的 `ModelSerializer` 类，并指定了相关的模型、字段和额外的选项。
在 `MyModelSerializer` 中，定义了一个名为 `xget_gender` 的方法，用于获取 `gender` 字段的显示值。
最后，定义了一个基于类的视图 `MyView`，其中的 `post` 方法用于处理请求。在该方法中，首先创建了 `MyModelSerializer` 的实例 `ser`，并将请求数据传递给它进行序列化。然后通过调用 `is_valid` 方法检查序列化的数据是否有效，如果有效则保存数据并返回序列化后的数据作为响应，否则返回序列化的错误信息作为响应。

访问：POST：`{"name": "zhangsan","age":11, "gender":1}`;
返回：`{"id":3, "name": "zhangsan","age":11, "gender":"男"}`

当通过 POST 请求提交 `{"name": "zhangsan","age":11, "gender":1}` 这样的数据时，视图 `MyView` 中的 `post` 方法会被触发。
在方法内部，首先创建了一个 `MyModelSerializer` 的实例 `ser`，并将请求的数据 `request.data` 传递给它进行序列化。
在序列化过程中，`MyModelSerializer` 使用 `MyCharField` 类来定义 `gender` 字段。根据定义的规则，该字段经过 `bind` 方法绑定到序列化器，并生成了一个名为 `xget_gender` 的方法。
接下来，`is_valid` 方法调用检查序列化的数据是否有效。在检查过程中，DRF 会根据字段定义验证输入数据的有效性，包括类型、长度、必填等规则。
`gender` 字段使用了自定义字段类 `MyCharField`，它重写了 `to_representation` 方法，将 `value` 转换为字符串形式。同时，`MyCharField` 还重写了 `get_attribute` 方法，在获取字段属性值时，通过 `getattr` 函数根据 `method_name` 获取到父序列化器上的 `xget_gender` 方法，并将该方法的执行结果作为 `gender` 字段的属性值。
因此，在序列化过程中，`MyModelSerializer` 会先调用 `xget_gender` 方法获取 `gender` 字段的显示值，即 "男"，然后将其与其他字段一起进行序列化。
如果序列化的数据有效，即通过了验证，`save` 方法会被调用来保存数据。在这里，没有看到具体的 `save` 方法实现，但通常它会使用序列化器中定义的模型类来创建或更新数据库中的记录，并返回一个包含保存后数据的实例。
最后，`ser.data` 将包含保存后的数据，根据模型序列化器的定义进行序列化，并作为响应返回。
因此，最终获得的响应是 `{"id":3, "name": "zhangsan","age":11, "gender":"男"}`，表示数据已成功保存，并包含了保存后的数据信息。

##### 自定义钩子2

1. `api/ext/hook.py`

   ```python
   from collections import OrderedDict
   from rest_framework.fields import SkipField
   from rest_framework.relations import PKOnlyObject


   class MyHookSerializer(object):
      def to_representation(self, instance):
         ret = OrderedDict()
         fields = self._readable_fields

         for field in fields:
            if hasattr(self, "my_%s" % field.field_name):
               value = getattr(self, "my_%s" % field.field_name)(instance)
               ret[field.field_name] = value
            else:
               try:
                  attribute = field.get_attribute(instance)
               except SkipField:
                  continue

               check_for_none = attribute.pk if isinstance(attribute, PKOnlyObject) else attribute
               if check_for_none is None:
                  ret[field.field_name] = None
               else:
                  ret[field.field_name] = field.to_representation(attribute)
         return ret
   ```

2. `views.py`

   ```python
   from api.ext.hook import MyHookSerializer


   class MyModelSerializer(MyHookSerializer, serializers.ModelSerializer):
      class Meta:
         model = models.User
         fields = ["id", "name", "age", "gender"]
         extra_kwargs = {
            "id": {"read_only": True}
         }

      def my_gender(self, obj):
         return obj.get_gender_display()


   class MyView(APIView):
      def post(self, request, *args, **kwargs):
         ser = MyModelSerializer(data=request.data)
         if ser.is_valid():
            ser.save()
            return Response(ser.data)
         else:
            return Response(ser.errors)
   ```

`api/ext/hook.py` 文件定义了一个名为 `MyHookSerializer` 的自定义序列化器。它继承自 DRF 提供的默认序列化器类，并重写了 `to_representation` 方法。在 `to_representation` 方法中，具体实现了对序列化数据的自定义处理逻辑。
`to_representation` 方法遍历序列化器的可读字段 `_readable_fields`，对于每个字段，首先判断序列化器是否定义了名为 `my_字段名` 的方法，如果定义了，则调用该方法获得该字段的值，并将其添加到返回结果 `ret` 中。
如果没有定义对应的方法，则通过调用字段的 `get_attribute` 方法获取字段在实例对象中的值，并根据字段的类型使用 `to_representation` 方法将其转换为表示形式，并添加到返回结果 `ret` 中。
最后，方法返回结果 `ret`，其中包含了根据自定义逻辑处理后的序列化数据。
`views.py` 文件中定义了一个名为 `MyModelSerializer` 的模型序列化器，它继承自上面提到的 `MyHookSerializer` 和 DRF 提供的 `ModelSerializer` 类。`MyModelSerializer` 指定了相关的模型类为 `User`，并定义了需要序列化的字段和额外的参数。
此外，`MyModelSerializer` 还定义了一个名为 `my_gender` 的方法，用于对 `gender` 字段进行自定义处理。在这个例子中，它通过调用模型对象的 `get_gender_display` 方法来获取 `gender` 字段的显示值。
`MyView` 是一个继承自 DRF 提供的 `APIView` 的视图类，定义了一个 `post` 方法用于处理 POST 请求。在方法内部，首先创建了 `MyModelSerializer` 的实例 `ser`，并将请求的数据传递给它进行序列化。
然后，通过调用序列化器的 `is_valid` 方法检查数据的有效性，如果数据验证通过，则调用序列化器的 `save` 方法保存数据，并返回保存后的数据作为响应；如果数据验证不通过，则返回错误信息作为响应。

提交的数据 `{"name": "zhangsan","age":11, "gender":1}` 经过视图类 `MyView` 的 `post` 方法处理，下面是具体步骤：

1. 创建 `MyModelSerializer` 实例 `ser`，并将请求的数据 `request.data` 传递给它进行序列化。
2. 序列化器首先验证数据的有效性，包括字段的数据类型、长度、是否满足模型的约束等。在这里，数据通过验证。
3. 序列化器调用 `save` 方法保存数据。这里，根据序列化器的 `Meta` 类中指定的 `model`，即 `models.User`，创建了一个新的 `User` 实例，并将提交的数据赋值给相应的字段。
4. 保存数据后，序列化器调用 `to_representation` 方法对保存后的数据进行序列化处理。
5. 在 `to_representation` 方法中，首先遍历序列化器的可读字段，这里有 `id`, `name`, `age`, `gender` 四个字段。
6. 对于 `id` 字段，由于在 `MyModelSerializer` 的 `Meta` 类中设置了 `read_only=True`，所以其值为默认的主键自增值，不需要进行自定义处理，直接添加到返回结果中。
7. 对于 `name` 和 `age` 字段，由于没有定义对应的 `my_字段名` 方法，序列化器会调用字段的 `to_representation` 方法将字段值转换为表示形式，并将其添加到返回结果中。
8. 对于 `gender` 字段，有定义了对应的 `my_gender` 方法，所以会调用该方法来获取字段的值，并将其添加到返回结果中。在这里，根据模型对象的 `get_gender_display` 方法，将数据库存储的 `1` 转换为显示值 `"男"`。
9. 最后，序列化器返回处理后的数据，即 `{"id":3, "name": "zhangsan","age":11, "gender":"男"}` 作为响应。
因此，视图处理过程经过了数据的验证、保存和序列化等步骤，并通过自定义的逻辑对数据进行了处理，最后返回了处理后的结果。

### DRF分页

对ORM中获取的数据进行分页处理，分批返回给用户。

#### PageNumberPagination

#### LimitOffsetPagination

### 视图类

DRF中提供了APIView等视图类可以继承使用。

#### APIView

APIView是DRF中最基本的视图类，它继承自Django的View类，并提供了更多用于处理API请求和响应的功能。APIView需要手动编写请求方法（如GET、POST等），并且需要手动处理请求参数和返回响应。

#### GenericAPIView（模型操作）

GenericAPIView是APIView的子类，它结合了通用模型视图的功能。它提供了与模型相关的操作，例如获取查询集、序列化数据、验证数据等。GenericAPIView需要与一个Mixin类组合使用，以实现不同的操作。

##### GenericAPIView特点

1. 通用模型操作
   GenericAPIView 可以通过继承 mixins 类实现常见的模型操作，例如获取查询集、序列化数据、验证数据等。这使得开发人员在编写 API 时能够更轻松地处理模型对象和序列化等方面的问题。
2. 简化请求方法的编写
   相比 APIView，GenericAPIView 提供了一些内置方法，如 get_object() 和 get_queryset()，用于快速处理 API 请求。这些方法可以帮助开发人员更快地编写请求方法，并提高代码复用性。
3. 支持多种请求方法
   GenericAPIView 支持多种请求方法，包括 GET、POST、PUT、PATCH 和 DELETE。这使得开发人员能够更轻松地实现常见的 CRUD 操作，从而提高开发效率。
4. 更好的代码复用性
   由于 GenericAPIView 可以实现通用的模型操作，因此可以在多个视图中重复使用，提高代码复用性。这意味着开发人员可以更快地编写更少的代码，并减少出错的可能性。
5. 简化序列化器的处理
   在通用模型视图中，GenericAPIView 还提供了默认的序列化器实例，可以自动根据视图中使用的模型对象生成。这Simple API for XML (SAX)使得开发人员能够更快地编写序列化器，并避免了一些常见的错误。

##### GenericAPIView 使用

1. 导入相关模块
   在使用 GenericAPIView 之前，需要导入相关模块。通常情况下，可以导入以下模块：

   ``` python
   from rest_framework import generics
   from rest_framework.response import Response
   from rest_framework import status
   ```

2. 继承 GenericAPIView 类
   使用 GenericAPIView 需要继承该类。在继承时，需要指定 serializer_class 和 queryset 属性，这些属性用于处理序列化和查询集。

   ``` python
   class BookListAPIView(generics.GenericAPIView):
      serializer_class = BookSerializer
      queryset = Book.objects.all()
   ```

3. 实现请求方法
   在 GenericAPIView 中，可以实现以下请求方法（根据需要实现即可）：

   - get: 处理 GET 请求，并返回查询结果。
   - post: 处理 POST 请求，并创建新的对象。
   - put: 处理 PUT 请求，并更新已有对象。
   - patch: 处理 PATCH 请求，并部分更新已有对象。
   - delete: 处理 DELETE 请求，并删除对象。

   ``` python
   class BookListAPIView(generics.GenericAPIView):
      serializer_class = BookSerializer
      queryset = Book.objects.all()

      def get(self, request, *args, **kwargs):
         queryset = self.get_queryset()
         serializer = self.get_serializer(queryset, many=True)
         return Response(serializer.data)

      def post(self, request, *args, **kwargs):
         serializer = self.get_serializer(data=request.data)
         serializer.is_valid(raise_exception=True)
         serializer.save()
         return Response(serializer.data, status=status.HTTP_201_CREATED)
   ```

4. 使用 mixins 类
   在 GenericAPIView 中，可以使用 mixins 类扩展其功能。例如，可以使用 ListModelMixin 来实现获取列表的功能，使用 CreateModelMixin 来实现创建新对象的功能。

   ``` python
   from rest_framework import mixins

   class BookListAPIView(generics.GenericAPIView, mixins.ListModelMixin, mixins.CreateModelMixin):
      serializer_class = BookSerializer
      queryset = Book.objects.all()

      def get(self, request, *args, **kwargs):
         return self.list(request, *args, **kwargs)

      def post(self, request, *args, **kwargs):
         return self.create(request, *args, **kwargs)
   ```

5. 结合视图集使用
   可以将 GenericAPIView 和视图集（ViewSet）结合起来使用，实现更高级和灵活的功能。例如，可以使用 GenericViewSet 实现自定义操作，并将其映射到 URL 路由中。

   ``` python
   from rest_framework import viewsets

   class BookViewSet(viewsets.GenericViewSet, mixins.ListModelMixin, mixins.CreateModelMixin):
      serializer_class = BookSerializer
      queryset = Book.objects.all()

      def get(self, request, *args, **kwargs):
         return self.list(request, *args, **kwargs)

      def post(self, request, *args, **kwargs):
         return self.create(request, *args, **kwargs)

      @action(detail=True, methods=['get'])
      def detail(self, request, pk=None):
         queryset = self.get_queryset()
         book = get_object_or_404(queryset, pk=pk)
         serializer = self.get_serializer(book)
         return Response(serializer.data)
   ```

总的来说，GenericAPIView 是一个非常强大和灵活的视图类，可以帮助开发人员更快地编写 RESTful API。使用 GenericAPIView 需要注意以下几点：

- 需要指定 serializer_class 和 queryset 属性。
- 需要实现请求方法，并处理相应的请求。
- 可以使用 mixins 类扩展其功能。
- 可以与视图集（ViewSet）结合使用，实现更高级和灵活的功能。

#### GenericViewSet（路由配置、处理序列化器）

GenericViewSet是一个特殊的视图类，它结合了GenericAPIView和ViewSetMixin。它提供了一组常用的操作方法，如列表、创建、检索、更新和删除，对应于HTTP方法GET、POST、GET、PUT/PATCH和DELETE。

##### GenericViewSet特点

1. 简化路由配置
   使用 GenericViewSet 可以更简化路由配置。相比于 APIView，GenericViewSet 可以自动为各种操作（例如获取列表、创建对象、更新对象等）生成默认的 URL 路由配置，无需手动编写每个操作的 URL 路由。
2. 内置 Action 方法
   GenericViewSet 提供了一些内置的 Action 方法，这些方法对应于常见的 RESTful 动作，如列表显示、创建、更新、删除等。通过重写这些方法，可以轻松实现自定义的行为，并将其映射到相应的 URL 路由。
3. 简化序列化器处理
   在 GenericViewSet 中，可以使用 serializer_class 属性指定默认的序列化器类。这使得开发人员无需在每个请求方法中手动编写序列化器的逻辑，而是直接使用默认的序列化器类，从而提高代码复用性和简化开发流程。
4. 简化查询集配置
   GenericViewSet 提供了 queryset 属性，用于指定默认的查询集。通过指定查询集，可以避免在每个请求方法中编写重复的查询逻辑，并且可以轻松地对查询集进行过滤、筛选等操作。
5. 支持多种请求方法
   与 APIView 类似，GenericViewSet 支持多种请求方法，包括 GET、POST、PUT、PATCH 和 DELETE。这意味着开发人员可以使用相同的视图类来处理不同类型的请求，并实现常见的 CRUD 操作。
6. 结合 ViewSetMixin 的灵活性
   GenericViewSet 通过结合 ViewSetMixin 类，提供了更高级和灵活的功能。ViewSetMixin 类为视图集提供了一些额外的方法和属性，用于处理分页、权限、过滤等常见的功能。

##### GenericViewSet使用

1. 导入相关模块
   在使用 GenericViewSet 之前，需要导入相关模块。通常情况下，可以导入以下模块：

   ```python
   from rest_framework import viewsets
   from rest_framework.response import Response
   from rest_framework import status
   ```

2. 继承 GenericViewSet 类
   使用 GenericViewSet 需要继承该类。在继承时，需要指定 serializer_class 和 queryset 属性，这些属性用于处理序列化和查询集。

   ```python
   class BookViewSet(viewsets.GenericViewSet):
      serializer_class = BookSerializer
      queryset = Book.objects.all()
   ```

3. 实现自定义操作
   在 GenericViewSet 中，可以实现自定义操作，并将其映射到 URL 路由中。可以使用装饰器 `@action` 来定义自定义操作。

   ```python
   from rest_framework.decorators import action

   class BookViewSet(viewsets.GenericViewSet):
      serializer_class = BookSerializer
      queryset = Book.objects.all()

      @action(detail=True, methods=['get'])
      def detail(self, request, pk=None):
         book = self.get_object()
         serializer = self.get_serializer(book)
         return Response(serializer.data)

      @action(detail=False, methods=['get'])
      def popular(self, request):
         queryset = self.filter_queryset(self.get_queryset().filter(popular=True))
         serializer = self.get_serializer(queryset, many=True)
         return Response(serializer.data)
   ```

   `@action` 装饰器用于定义两个自定义操作：`detail` 和 `popular`。`detail` 方法处理 `GET` 请求，并返回特定书籍的详细信息；`popular` 方法处理 `GET` 请求，并返回热门书籍列表。

4. 使用 mixins 类
   在 GenericViewSet 中，可以使用 mixins 类扩展其功能。例如，可以使用 ListModelMixin 来实现获取列表的功能，使用 CreateModelMixin 来实现创建新对象的功能。

   ```python
   from rest_framework import mixins

   class BookViewSet(viewsets.GenericViewSet, mixins.ListModelMixin, mixins.CreateModelMixin):
      serializer_class = BookSerializer
      queryset = Book.objects.all()
   ```

   使用 ListModelMixin 和 CreateModelMixin，这使得 BookViewSet 可以处理 `GET` 请求来获取书籍列表，以及 `POST` 请求来创建新的书籍。

总的来说，GenericViewSet 是一个非常强大和灵活的视图集类，可以帮助开发人员更快地编写 RESTful API。使用 GenericViewSet 需要注意以下几点：

- 需要指定 serializer_class 和 queryset 属性。
- 可以实现自定义操作，并使用 `@action` 装饰器将其映射到 URL 路由中。
- 可以使用 mixins 类扩展其功能，以便实现更多的通用操作。
- 可以与路由器（router）一起使用，将其注册到 URL 路由中。

### Mixin类

在 Django Rest Framework (DRF) 中，Mixin 类是一种被设计为与视图类组合使用的小型类。它们通常用于实现特定的行为或功能，可作为其他视图类的基础。

#### CreateModelMixin

CreateModelMixin是一个Mixin类，用于在GenericAPIView中实现创建操作。它提供了create方法，用于创建新的实例。

#### ListModelMixin

ListModelMixin是一个Mixin类，用于在GenericAPIView中实现列表操作。它提供了list方法，用于获取查询集并对其进行序列化。

#### RetrieveModelMixin

RetrieveModelMixin是一个Mixin类，用于在GenericAPIView中实现检索操作。它提供了retrieve方法，用于获取单个实例的详细信息。

#### UpdateModelMixin

UpdateModelMixin是一个Mixin类，用于在GenericAPIView中实现更新操作。它提供了update方法，用于更新现有的实例。

#### DestroyModelMixin

DestroyModelMixin是一个Mixin类，用于在GenericAPIView中实现删除操作。它提供了destroy方法，用于删除现有的实例。

#### RetrieveUpdateDestroyAPIView

此视图类结合了 RetrieveModelMixin、UpdateModelMixin 和 DestroyModelMixin，实现了 GET、PUT、PATCH 和 DELETE 请求的所有功能。

## 博客系统

### 博客系统规划

包含：注册、登录、博客列表、详细、评论、点赞、发布博客

- 注册：输入用户信息 + 重复密码进行注册
- 登录：登录成功，生成TOKEN+失效日期返回
- 博客列表：路由 + 视图（时间倒序排序） + 序列化
- 博客详情：路由（PK） + 新视图或原视图 + 序列化
- 评论列表：在URL上通过GET方式传入博客ID，根据博客ID获取相关评论（请求可以单独做也可以在博客详细的请求中返回）
- 新建博客（需登录）
- 创建评论（需登录）：在URL上通过GET方式传入博客ID + 请求体中评论信息 发送到后端API（1. 认证组件，request.user; 2. 构造参数保存）
  - 认证组件
  - 单独视图

      ```python
      class CreateComment(APIView):
         authentication_classes = []

         def post(self):
            pass
      ```

  - 评论列表 + 创建评论

      ```python
      class CommentView(APIView):
         # 登录成功，request.user有值；登录失败，request.user = None，为匿名用户
         authentication_classes = []

         def get(self, request, blog_id):
            """评论列表"""
            pass

         def post(self):
            """创建评论"""
            pass
      ```

- 点赞（需登录）：赞过不能再赞；结合事务实现添加赞 + 赞数量更新

### 博客系统实现

1. 创建blog项目，及api app。

2. `settings.py`

   ```py
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'rest_framework',
      'api.apps.ApiConfig',
   ]
   LANGUAGE_CODE = 'zh-hans'
   TIME_ZONE = 'Asia/Shanghai'
   DATETIME_FORMAT = "Y年m月d日"
   REST_FRAMEWORK = {
      "UNAUTHENTICATED_USER": None,
   }
   ```

3. `models.py`

   ```python
   from django.db import models


   class UserInfo(models.Model):
      username = models.CharField(verbose_name="用户名", max_length=32, db_index=True)
      password = models.CharField(verbose_name="密码", max_length=64)
      token = models.CharField(verbose_name="TOKEN", max_length=64, null=True, blank=True, db_index=True)


   class Blog(models.Model):
      category_choices = ((1, "云计算"), (2, "Python全栈"), (3, "Go开发"))
      category = models.IntegerField(verbose_name="分类", choices=category_choices)
      image = models.CharField(verbose_name="封面", max_length=255)
      title = models.CharField(verbose_name="标题", max_length=32)
      summary = models.CharField(verbose_name="简介", max_length=256)
      text = models.TextField(verbose_name="博文")
      ctime = models.DateTimeField(verbose_name="发布时间", auto_now_add=True)
      creator = models.ForeignKey(verbose_name="作者", to="UserInfo", on_delete=models.CASCADE)
      comment_count = models.PositiveIntegerField(verbose_name="评论数", default=0)
      favor_count = models.PositiveIntegerField(verbose_name="赞数", default=0)


   class Favor(models.Model):
      blog = models.ForeignKey(verbose_name="博客", to="Blog", on_delete=models.CASCADE)
      user = models.ForeignKey(verbose_name="用户", to="UserInfo", on_delete=models.CASCADE)
      create_datetime = models.DateTimeField(verbose_name="创建时间", auto_now_add=True)

      # 联合唯一索引，一个人不能对一篇博文点第二个赞
      class Meta:
         constraints = [
            models.UniqueConstraint(fields=["blog", "user"], name="uni_favor_blog_user")
         ]


   class Comment(models.Model):
      blog = models.ForeignKey(verbose_name="博客", to="Blog", on_delete=models.CASCADE)
      user = models.ForeignKey(verbose_name="用户", to="UserInfo", on_delete=models.CASCADE)
      content = models.CharField(verbose_name="内容", max_length=150)
      create_datetime = models.DateTimeField(verbose_name="创建时间", auto_now_add=True)
   ```

4. `urls.py`

   ```py
   from django.contrib import admin
   from django.urls import path
   from api import views

   urlpatterns = [
      path('admin/', admin.site.urls),
      path("api/blogs/", views.BlogsView.as_view()),
      path("api/blog/<int:pk>/", views.BlogDetailView.as_view()),
      path("api/comments/<int:blog_id>/", views.CommentsView.as_view()),
      path("api/register/", views.RegisterView.as_view()),
      path("api/login/", views.LoginView.as_view()),
      path("api/favor/", views.FavorView.as_view()),
   ]
   ```

5. `views.py`

   ```py
   from rest_framework.views import APIView
   from rest_framework import serializers
   from rest_framework.response import Response
   from rest_framework import exceptions
   from api import models
   from api.ext.hook import HookSerializer
   from api.ext.auth import BlogAuthentication, NoAuthentication
   import uuid


   class Creator(serializers.ModelSerializer):
      class Meta:
         model = models.UserInfo
         fields = ["id", "username"]


   class BlogsModelSerializer(HookSerializer, serializers.ModelSerializer):
      # category = serializers.CharField(source="get_category_display")
      ctime = serializers.DateTimeField(format="%Y-%m-%d", read_only=True)
      # creator_name = serializers.CharField(source="creator.username")
      # creator2 = serializers.SerializerMethodField()
      # 必须使用数据库同名字段
      creator = Creator(read_only=True)

      class Meta:
         model = models.Blog
         fields = ["id", "category", "image", "title", "text", "summary",
                  "ctime", "favor_count", "comment_count", "creator"]
         extra_kwargs = {
            "favor_count": {"read_only": True},
            "comment_count": {"read_only": True},
            "text": {"write_only": True},
         }

      def my_category(self, obj):
         return obj.get_category_display()

      # def get_creator2(self, obj):
      #     return {"id": obj.creator_id, "name": obj.creator.username}


   class BlogsView(APIView):
      authentication_classes = [BlogAuthentication, ]

      def get(self, request, *args, **kwargs):
         """获取博客列表"""
         # 1. 读取数据库中的博客信息
         queryset = models.Blog.objects.all().order_by("-id")
         # 2. 序列化
         ser = BlogsModelSerializer(instance=queryset, many=True)
         # 3. 返回
         context = {"code": 1000, "data": ser.data}
         return Response(context)

      def post(self, request, *args, **kwargs):
         """新建博客"""
         if not request.user:
            return Response({"code": 2001, "error": "认证失败"})
         ser = BlogsModelSerializer(data=request.data)
         if not ser.is_valid():
            return Response({"code": 1002, "error": "校验失败", "detail": ser.errors})
         ser.save(creator=request.user)
         return Response({"code": 1000, "data": ser.data})


   class BlogDetailModelSerializer(serializers.ModelSerializer):
      category = serializers.CharField(source="get_category_display")
      ctime = serializers.DateTimeField(format="%Y-%m-%d")
      creator = serializers.SerializerMethodField()
      comments = serializers.SerializerMethodField()

      class Meta:
         model = models.Blog
         fields = "__all__"

      def get_creator(self, obj):
         return {"id": obj.creator_id, "name": obj.creator.username}


   class BlogDetailView(APIView):
      def get(self, request, *args, **kwargs):
         """获取博客详情"""
         # 1. 获取文章ID
         pk = kwargs.get("pk")
         # 2. 根据ID获取文章对象
         instance = models.Blog.objects.filter(id=pk).first()
         if not instance:
            return Response({"code": 1001, "error": "文章不存在或已删除"})
         # 2. 序列化
         ser = BlogDetailModelSerializer(instance=instance, many=False)
         # 3. 返回
         context = {"code": 1000, "data": ser.data}
         return Response(context)


   class CommentsSerializer(HookSerializer, serializers.ModelSerializer):
      # user = serializers.CharField(source="user.username")
      # user = serializers.CharField(source="my_user")

      class Meta:
         model = models.Comment
         fields = ["id", "content", "user"]
         # fields = "__all__"
         extra_kwargs = {
            "id": {"read_only": True},
            "user": {"read_only": True}
         }

      # def my_user(self, obj):
      #     return obj.user.username


   class CommentsView(APIView):
      authentication_classes = [BlogAuthentication, ]

      def get(self, request, blog_id):
         """评论列表"""
         # 1. 根据ID获取评论
         queryset = models.Comment.objects.filter(blog_id=blog_id)
         # 2. 序列化
         ser = CommentsSerializer(instance=queryset, many=True)
         # 3. 返回
         context = {"code": 1000, "data": ser.data}
         return Response(context)

      def post(self, request, blog_id):
         """发布评论"""
         if not request.user:
            return Response({"code": 2000, "error": "未登录"})

         blog_obj = models.Blog.objects.filter(id=blog_id).first()
         if not blog_obj:
            return Response({"code": 2000, "error": "博客不存在"})
         print(request.data)
         ser = CommentsSerializer(data=request.data)
         if not ser.is_valid():
            return Response({"code": 1003, "error": "验证失败", "detail": ser.errors})

         ser.save(blog=blog_obj, user=request.user)
         return Response({"code": 1000, "data": ser.data})


   class RegisterModelSerializer(serializers.ModelSerializer):
      confirm_password = serializers.CharField(write_only=True)

      class Meta:
         model = models.UserInfo
         fields = ["username", "password", "confirm_password"]

      def validate_password(self, value):
         print("密码：", value)
         return value

      def validate_confirm_password(self, value):
         print("重复密码：", value)
         password = self.initial_data.get("password")
         if password != value:
            raise exceptions.ValidationError("密码不一致")
         return value


   class RegisterView(APIView):
      def post(self, request, *args, **kwargs):
         # 1. 提交数据 {"username": "", "password": "", "confirm_password": ""}

         # 2. 校验
         ser = RegisterModelSerializer(data=request.data)
         if ser.is_valid():
            ser.validated_data.pop("confirm_password")
            ser.save()
            return Response({"code": 1000, "data": ser.data})
         else:
            return Response({"code": 1001, "error": "注册失败", "detail": ser.errors})


   class LoginModelSerializer(serializers.ModelSerializer):
      class Meta:
         model = models.UserInfo
         fields = ["username", "password"]


   class LoginView(APIView):
      def post(self, request):
         ser = LoginModelSerializer(data=request.data)
         if not ser.is_valid():
            return Response({"code": 1002, "error": "校验失败", "detail": ser.errors})
         instance = models.UserInfo.objects.filter(**ser.validated_data).first()
         if not instance:
            return Response({"code": 1003, "error": "用户名或密码错误"})
         token = str(uuid.uuid4())
         instance.token = token
         instance.save()
         return Response({"code": 1000, "token": token})


   class FaverSerializer(serializers.ModelSerializer):
      class Meta:
         model = models.Favor
         fields = ["id", "blog"]


   class FavorView(APIView):
      authentication_classes = [BlogAuthentication, NoAuthentication, ]

      def post(self, request):
         # {"blog":1} + user: request.user
         ser = FaverSerializer(data=request.data)
         if not ser.is_valid():
            return Response({"code": 1002, "error": "校验失败", "detail": ser.errors})
         # 查询是否点过赞，不存在则添加，存在则删除
         exists = models.Favor.objects.filter(
            user=request.user, **ser.validated_data).exists()
         if exists:
            return Response({"code": 2001, "error": "已经点过赞了"})

         ser.save(user=request.user)
         return Response({"code": 1000, "data": ser.data})
   ```

6. `api/ext/auth.py`

   ```py
   from rest_framework.authentication import BaseAuthentication
   from rest_framework import exceptions
   from api import models


   class BlogAuthentication(BaseAuthentication):
      def authenticate(self, request):
         token = request.query_params.get("token")
         if not token:
            return
         user = models.UserInfo.objects.filter(token=token).first()
         if not user:
            return

         return user, token

      def authenticate_header(self, request):
         return "API"


   class NoAuthentication(BaseAuthentication):
      def authenticate(self, request):
         raise exceptions.AuthenticationFailed({"code": 2000, "errors": "认证失败"})

      def authenticate_header(self, request):
         return "API"
   ```

7. `api/ext/hook.py`

   ```py
   from collections import OrderedDict
   from rest_framework.fields import SkipField
   from rest_framework.relations import PKOnlyObject


   class HookSerializer(object):
      def to_representation(self, instance):
         ret = OrderedDict()
         fields = self._readable_fields

         for field in fields:
            if hasattr(self, "my_%s" % field.field_name):
               value = getattr(self, "my_%s" % field.field_name)(instance)
               ret[field.field_name] = value
            else:
               try:
                  attribute = field.get_attribute(instance)
               except SkipField:
                  continue

            check_for_none = attribute.pk if isinstance(
               attribute, PKOnlyObject) else attribute
            if check_for_none is None:
               ret[field.field_name] = None
            else:
               ret[field.field_name] = field.to_representation(attribute)
         return ret
   ```

## Vue.js

### 快速开始

基于vue.js框架来编写项目的步骤：

```html
<!DOCTYPE html>
<html lang="en">
   <head>
      <meta charset="UTF-8">
      <link rel="icon" href="/favicon.ico">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Vite App</title>
      <!-- 1. 引入vue.js文件 -->
      <script src="https://cdn.jsdelivr.net/npm/vue@w/dist/vue.js"></script>
   </head>
   <body>
      <!-- 2. 指定区域，该区域的内容希望由vue.js来接管 -->
      <div id="app">
      <h1>欢迎学习Vue.js</h1>
      <div>我叫 {{name}}, 年龄 {{age}}</div>
      <input type="button" value="点我" v-on:click="clickMe">
      </div>

      <!-- 3. 创建vue对象，并关联指定HTML区域 -->
      <!-- 其中 el, data, methods是固定的 -->
      <script>
      var app = new Vue({
         el: '#app',
         data: {
            name: "张三",
            age: 18
         },
         methods: {
            clickMe: function (){
            //获取值this.name
            //修改值this.name="xx"
            this.name = "lisi";
            this.age = "89";
            }
         }
      })
      </script>
   </body>
</html>
```

导入vue.js包（CDN）

```html
<!-- 开发环境版本，包含了有帮助的命令行警告 -->
<script src="https://cdn.jsdelivr.net/npm/vue@w/dist/vue.js"></script>
<!-- 生产环境版本，优化了尺寸和速度 -->
<script src="https://cdn.jsdeliver.net/npm/vue@2"></script>
<!-- 也可以将文件下载下来，再通过本地导入 -->
```

### 常见指令

#### 插值表达式

一般在显示文本内容的标签中使用。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>插值表达式</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
    <div id="app">
        <div>我叫{{name}}, 我喜欢{{hobby}}, 年龄{{age}}</div>
        <ul>
            <li>{{"张三"}}</li>
            <li>{{"张三"+"法外狂徒"}}</li>
            <li>{{base + 1 + 1}}</li>
            <!-- 三元表达式：如果1=1，张三；否则，李四 -->
            <li>{{1===1 ? "张三":"李四"}}</li>
        </ul>
        <ul><li>{{condition? "张三": "李四"}}</li></ul>
        <input type="button" value="点我" v-on:click="clickMe">
    </div>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                name: "王五",
                hobby: "围棋",
                dataInfo: {
                    id: 1,
                    email: "ss@xx.com"
                },
                condition: false,
                base: 1
            },
            methods: {
                clickMe: function(){
                    this.name = "王五";
                    this.condition = true;
                    this.dataInfo.email = "zhangsan@China.com";
                    this.base += 100;
                }
            }
        })
    </script>
</body>
</html>
```

#### v-bind指令(单向绑定)

一般用于对标签中的属性进行操作。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>v-bind</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
    <style>
        .ig {
            border: 2px solid red;
        }
        .info {
            color:green;
        }
        .danger{
            color:red;
        }
        .flag{
            color:yellow;
        }
    </style>
</head>
<body>
    <div id="app">
        <img v-bind:src="imgURL" v-bind:class="cls">
        <!-- 使用键值对，如果值为true该样式生效；false则不生效 -->
        <h1 v-bind:class="{info:info, danger:danger}">欢迎</h1>
        <!-- 使用按钮切换样式 -->
        <h1 v-bind:class="{flag:flag}">欢迎2</h1>
        <!-- 同时应用多个样式 -->
        <h2 v-bind:class="[a1, a2]">欢迎3</h2>
        <!-- 当count<=5时，应用info样式；count>5时，应用danger样式 -->
        <h2 v-bind:class="{'info': count <= 5, 'danger': count > 5}">16</h2>
        <!-- 动态绑定style属性 -->
        <h3 v-bind:style="{color: clr, fontSize:'19px'}">欢迎4</h3>
        <input type="button" value="点我" v-on:click="clickMe">
    </div>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                imgURL: "https://ts1.cn.mm.bing.net/th/id/R-C.b2deabf4f73362fdeded6ebb1759e6d5?rik=QTdjsA3RyD4v4g&riu=http%3a%2f%2fn.sinaimg.cn%2fsinacn20107%2f549%2fw600h749%2f20190427%2f07db-hvvuiyp2168388.jpg&ehk=ea6ytlOusTMhUxs4TgDNYQqymM8voeFn9db9ZiNcMOk%3d&risl=&pid=ImgRaw&r=0",
                cls: "ig",
                info: true,
                danger:false,
                flag:true,
                clr:"green",
                count:0
            },
            methods: {
               // 自定义函数，当发生点击时，flag的值会在true和false之间切换；count的值也会自增
                clickMe: function(){
                    if (this.flag){
                    this.flag = false;
                    } else {
                        this.flag = true;
                    }
                    this.count++;
                }
            }
        })
    </script>
</body>
</html>
```

- v-bind简写：`<h1 v-bind:class="v1">标题1</h1>` = `<h1 :class="v1">标题1</h1>`
- v-bind属于单向绑定（JS修改 -> HTML修改）
- v-model是双向绑定（JS修改 <-> HTML修改）

#### v-model指令(双向绑定)

一般用于在交互的表中使用，如：input、select、textarea等。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>v-model</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
   <div id="app">
      <div>
         用户名：<input type="text" v-model="info.user">
      </div>
      <div>
         密码：<input type="password" v-model="info.pwd">
      </div>
      <div>
         性别：
         <input type="raido" v-model="info.sex" value="1">男
         <input type="raido" v-model="info.sex" value="2">女
      </div>
      <div>
         爱好：
         <input type="checkbox" v-model="info.hobby" value="11">篮球
         <input type="checkbox" v-model="info.hobby" value="22">足球
         <input type="checkbox" v-model="info.hobby" value="33">乒乓球
      </div>
      <div>
         城市：
         <select v-model="info.city">
            <option value="sh">上海</option>
            <option value="bj">北京</option>
            <option value="sz">深圳</option>
            <option value="gz">广州</option>
         </select>
      </div>
      <div>
         技能：
         <select v-model="info.skill" multiple>
            <option value="system">System</option>
            <option value="python">Python</option>
            <option value="shell">Shell</option>
            <option value="docker">Docker</option>
         </select>
      </div>
      <div>
         其他：<textarea v-model="info.more"></textarea>
      </div>
      <input type="button" value="注册" v-on:click="register" />
      <input type="button" value="重置" v-on:click="resetForm" />
   </div>
   <script>
      var app = new Vue({
         el: '#app',
         data: {
            info:{
               user: "",
               pwd: "",
               sex: "2",
               hobby: ["22"],
               city: "sz",
               skill: ["system", "python"],
               more: "..."
            }
         },
         methods: {
            register: function(){
               console.log(this.info)
            },
            resetForm: function(){
               this.user = "";
               this.pwd = "";
            }
         }
      })
   </script>
</body>
</html>
```

#### v-for指令

用于循环数据并展示。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>v-for</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
    <div id="app">
        <ul><li v-for="item in dataList">{{item}}</li></ul>
        <ul><li v-for="(item,idx) in dataList">{{idx}} - {{item}}</li></ul>
        <ul><li v-for="(value,key) in dataDict">{{key}} - {{value}}</li></ul>
        <ul><li v-for="(item,idx) in cityList">{{item.id}} - {{item.city}}</li></ul>
        <ul><li v-for="(item,idx) in cityList">
            <span v-for="(v, k) in item">{{k}} - {{v}}  </span>
        </li></ul>
    </div>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                dataList: ["张三", "李四", "王五"],
                dataDict: {id:1, name: "张三", age: 18},
                cityList: [
                    {id:1, city: "上海"},
                    {id:2, city: "北京"},
                    {id:3, city: "广州"},
                    {id:4, city: "深圳"},
                ]
            }
        })
    </script>
</body>
</html>
```

#### v-on指令

事件相关指令。

```shell
v-on:click,
v-on:dblclick,
v-on:mouseover,
v-on:mouseout,
v-on:change,
v-on:focus,
...
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>v-on</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
    <div id="app">
        <ul>
            <li v-on:click="singleClick">单击</li>
            <!-- 简写 -->
            <li @click="singleClick">单击</li>
            <li v-on:dblclick="doSomething('双击')">双击</li>
            <li v-on:mouseover="doSomething('进入')" v-on:mouseout="doSomething('离开')">进入&离开</li>
        </ul>
    </div>
    <script>
        var app = new Vue({
            el: '#app',
            data: {},
            methods: {
                singleClick:function(){
                    alert("点击了")
                },
                doSomething:function(msg){
                    console.log(msg);
                }
            }
        })
    </script>
</body>
</html>
```

#### v-if指令

条件判断。
条件不满足，标签不渲染。

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>v-if</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
   <div id="app">
      <div>
         <a v-if="isLogin">{{user}}</a>
         <a v-else>登录</a>
      </div>
      <div>
         <!-- 单分支 -->
         <h1 v-if="v1">单独使用if</h1>
         <!-- 双分支 -->
         <h1 v-if="v2">去西藏</h1>
         <h1 v-else>去新疆</h1>
         <!-- 多分支 -->
         <div v-if="v3==='北京'">
               <h1>天安门</h1>
         </div>
         <div v-else-if="v3==='新疆'">
               <h1>乌鲁木齐</h1>
         </div>
         <div v-else-if="v3==='西藏'">
               <h1>拉萨</h1>
         </div>
         <div v-else>
               <h1>大理</h1>
         </div>
      </div>
   </div>
   <script>
      var app = new Vue({
         el: '#app',
         data: {
               isLogin:true,
               user: "张三",
               v1: true,
               v2: true,
               travelList: ['北京', '新疆', '西藏', '济南'],
         },
         computed: {
               v3: function() {
                  // 通过计算属性随机获取 travelList 中的值
                  var randomIndex = Math.floor(Math.random() * this.travelList.length);
                  return this.travelList[randomIndex];
               }
         }
      })
   </script>
</body>
</html>
```

#### v-show指令

根据条件显示或隐藏（`display=none`）。
标签都会渲染到页面。

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>v-show</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
   <div id="app">
      <input type="button" value="密码登录" @click="isSms=false" />
      <input type="button" value="短信登录" @click="isSms=true" />
      <div v-show="isSms">
         <p>
            <label>手机号</label>
            <input type="text" placeholder="手机号">
         </p>
         <p>
            <label>验证码</label>
            <input type="text" placeholder="验证码">
         </p>
      </div>
      <div v-show="!isSms">
         <p>
            <label>用户名</label>
            <input type="text" placeholder="用户名">
         </p>
         <p>
            <label>密码</label>
            <input type="password" placeholder="密码">
         </p>
      </div>
   </div>
   <script>
      var app = new Vue({
         el: '#app',
         data: {
            isSms: false,
         }
      })
   </script>
</body>
</html>
```

#### 编辑数据

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>数据管理</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
   <style>
      .penal {
         border: 1px solid #dddddd;
         margin: 20px 0 0 0;
         padding: 10px;
         border-bottom: 0;
         background-color: #d9d9d9;
         text-align: center;
      }
      .table {
         width: 100%;
         border-collapse: collapse;
         border-spacing: 0;
         table-layout: fixed;
      }
      .table th,
      .table td {
         padding: 8px;
         text-align: left;
         border: 1px solid #ddd;
         vertical-align: top;
      }
   </style>
</head>
<body>
   <div id="app">
      <div>
         <h3 class="penal">表单区域</h3>
         <div>
            <label for="">姓名</label>
            <input type="text" v-model="user">
         </div>
         <div>
            <label for="">年龄</label>
            <input type="text" v-model="age">
            <input type="button" :value="button" @click="addUser">
         </div>
      </div>
      <div>
         <h3 class="penal">数据列表</h3>
         <table class="table">
            <thead><tr><th>name</th><th>age</th><th>操作</th></tr></thead>
            <tbody>
               <tr v-for="(item, idx) in dataList">
                  <td>{{item.name}}</td>
                  <td>{{item.age}}</td>
                  <td>
                     <input type="button" value="删除1" @click="deleteRow1(idx)"/>
                     <input type="button" value="删除2" @click="deleteRow2" :data-idx="idx"/>
                     <input type="button" value="编辑" @click="editRow" :data-idx="idx"/>
                  </td>
               </tr>
            </tbody>
         </table>
      </div>
   </div>
   <script>
   // 创建一个 Vue 实例
   var app = new Vue({
      // 绑定到 HTML 中的元素 ID
      el: '#app',
      // 数据对象，包含了表单数据和数据列表
      data: {
         user: "",
         age: "",
         button: "新建",
         editIndex: undefined,
         dataList: [
            {name: "zhangsan", age: 19},
            {name: "lisi", age: 27},
         ]
      },
      // 方法对象，包含了表单提交、删除和编辑等操作
      methods: {
         addUser:function(){
            // 如果当前处于编辑状态，则更新对应行数据
            if (this.editIndex){
               // 修改
               this.dataList[this.editIndex].name = this.user;
               this.dataList[this.editIndex].age = this.age;
            } else {
               // 否则添加一行数据
               let row = {name: this.user, age:this.age};
               this.dataList.push(row);
            }
            // 清空表单数据
            this.user = "";
            this.age = "";
            // 恢复按钮文本为“新建”
            this.button = "新建";
            // 取消编辑状态
            this.editIndex = undefined;
         },
         deleteRow1:function(idx){
            // 根据索引删除dataList中的数据
            this.dataList.splice(idx, 1);
         },
         deleteRow2:function(event){
            // 根据索引删除dataList中的数据
            let idx = event.target.dataset.idx;
            this.dataList.splice(idx, 1);
         },
         editRow:function(event){
            // 解包
            let idx = event.target.dataset.idx;
            let {name, age} = this.dataList[idx]; 
            // 将对应行数据填充到表单中
            this.user = name;
            this.age = age;
            // 将按钮文本置为“修改”
            this.button = "修改";
            // 设置编辑状态
            this.editIndex = idx;
         }
      }
   })
   </script>
</body>
</html>
```

#### Axios库

Axios 是一个基于 Promise 的 HTTP 客户端库，用于浏览器和 Node.js。它可以在浏览器中发送 AJAX 请求，并且还提供了许多处理请求和响应的便捷功能。

Axios 的主要特点和用法：

1. 支持浏览器和 Node.js：Axios 可以在浏览器和 Node.js 环境中使用，这使得它成为一个通用的 HTTP 客户端库。
2. Promise API：Axios 使用 Promise API 处理异步请求和响应。这使得我们可以使用 `.then()` 和 `.catch()` 方法来处理请求的成功和失败。
3. 支持请求和响应拦截器：Axios 提供了请求和响应拦截器，可以在请求发送前和响应返回后对数据进行拦截、修改或处理。这对于添加全局的认证信息、错误处理等非常有用。
4. 自动转换数据：Axios 能够自动将请求和响应的数据转换为不同的格式，例如 JSON、XML、FormData 等。
5. 取消请求：Axios 允许我们取消正在进行的请求。这对于用户取消请求或避免重复请求非常有用。
6. 并发请求：Axios 允许我们同时发送多个并发请求，并且可以等待所有请求完成后再处理结果。
7. 提供了很多辅助方法：Axios 提供了许多辅助方法来简化我们的请求操作，例如设置请求头、超时设置、身份验证等。

使用 Axios 发送 GET 请求：

```javascript
// 引入 Axios
import axios from 'axios';

// 发送 GET 请求
axios.get('https://api.example.com/users')
  .then(response => {
    // 请求成功，处理响应数据
    console.log(response.data);
  })
  .catch(error => {
    // 请求失败，处理错误信息
    console.error(error);
  });
```

首先引入了 Axios 库。然后，使用 `axios.get()` 方法发送了一个 GET 请求到指定的 URL。通过 `.then()` 方法处理请求成功的响应，并通过 `.catch()` 方法处理请求失败的错误信息。
这只是 Axios 的基本用法，它还提供了许多其他功能和配置选项，如 POST 请求、设置请求头、请求超时、请求取消等。可以查阅 Axios 的官方文档以获得更详细的信息和用法示例：`https://axios-http.com/`

#### vue版用户登录

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>用户登录</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
   <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
</head>
<body>
   <div id="app">
      <input type="button" value="密码登录" @click="isSms=false" />
      <input type="button" value="短信登录" @click="isSms=true" />
      <div v-show="isSms">
         <p>
            <label>手机号</label>
            <input type="text" placeholder="手机号" v-model="sms.mobile">
         </p>
         <p>
            <label>验证码</label>
            <input type="text" placeholder="验证码" v-model="sms.code">
         </p>
      </div>
      <div v-show="!isSms">
         <p>
            <label>用户名</label>
            <input type="text" placeholder="用户名" v-model="info.username">
         </p>
         <p>
            <label>密码</label>
            <input type="password" placeholder="密码" v-model="info.password">
         </p>
      </div>
      <input type="button" value="登 录" @click="loginForm"/>
   </div>
   <script>
      var app = new Vue({
         el: '#app',
         data: {
            isSms: false,
            info: {
               username: "",
               password: ""
            },
            sms: {
               mobile: "",
               code: ""
            }
         },
         methods:{
            loginForm: function(){
               // 1. 获取用户输入的值
               let dataDict = this.isSms ? this.sms : this.info

               // 2. 向后端接口发送网络请求 axios
               let url;
               if (this.isSms){
                  // 接口不可用
                  url = "https://api.luffycity.com/api/v1/auth/mobile/login/?loginWay=mobile";
               } else {
                  url = "https://api.luffycity.com/api/v1/auth/password/login/?loginWay=password";
               }
               axios({
                  method: "post",
                  url: url,
                  data: dataDict,
                  headers: {
                     "Content-Type": "application/json"
                  }
               }).then(function(res){
                  if (res.data.code === -1){
                     alert(res.data.msg);
                     return;
                  }
                  // 登录成功后跳转
                  window.location.href = "https://www.luffycity.com"
               }).catch(function(error){
                  console.log(error);
                  alert("请求异常，请重新登录");
               })
            }
         }
      })
   </script>
</body>
</html>
```

### 组件化开发

#### 组件化开发介绍

Vue 的组件化开发是指将一个复杂的应用程序拆分成多个独立且可重用的组件，每个组件都有自己的功能和样式，并且可以通过组合这些组件来构建整个应用程序。组件化开发使得代码更易于维护、测试和复用，同时也提高了开发效率。

在 Vue 中，组件是由模板、脚本和样式组成的。

- **模板**定义了组件的结构和布局；
- **脚本**包含了组件的行为逻辑；
- **样式**则定义了组件的外观和样式。

Vue 组件示例：

```html
<template>
  <div>
    <h1>{{ title }}</h1>
    <p>{{ message }}</p>
    <button @click="increment">Click me</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello, Vue!',
      message: 'Welcome to component-based development',
      count: 0
    };
  },
  methods: {
    increment() {
      this.count++;
    }
  }
};
</script>

<style scoped>
h1 {
  color: blue;
}
button {
  background-color: green;
  color: white;
}
</style>
```

在一个名为 `MyComponent` 的组件中，包含了一个 `<h1>` 标题、一个 `<p>` 段落、一个按钮，以及一些与数据和方法相关的逻辑。
在模板中，使用了双花括号 `{{ }}` 来插入数据绑定，将组件的数据动态显示在页面上。还在按钮上绑定了一个点击事件，当按钮被点击时会调用 `increment` 方法。
在脚本部分，使用 `data` 方法返回组件的初始数据。还定义了一个 `increment` 方法，用于增加计数器的值。
在样式部分，使用 `scoped` 属性来限定样式仅应用于当前组件，以避免样式冲突。
要在应用程序中使用这个组件，只需在父组件的模板中添加 `<my-component></my-component>` 标签即可。
通过组件化开发，可以将应用程序拆分成多个独立的组件，每个组件负责特定的功能或视图。这样做可以提高代码的可读性和可维护性，并且可以方便地重用组件，减少重复编写代码的工作量。同时，组件之间可以通过 props 和 events 进行数据传递和通信，使得组件之间的关系更加清晰和灵活。
总结起来，Vue 的组件化开发是一种将应用程序拆分成多个独立、可重用的组件的开发方式，它使得代码更易于理解、维护和复用，提高了开发效率。

#### 局部组件

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>局部组件</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
   <div id="app">
      <h1>当前页面</h1>
      {{name}}
      <h1>在页面中引入组件</h1>
      <Demo1></Demo1>
      <D2></D2>
      <hr/>
   </div>
   <script>
      // 创建子组件
      const Demo1 = {
         data:function(){
            return {msg: '哈哈哈哈'}
         },
         template: `
         <div>
            <h1>{{msg}}</h1>
            <input type="text" v-model="msg" />
            <input type="button" @click="showMsg" value="展示">
         </div>
         `,
         methods: {
            showMsg:function(){
               alert(this.msg);
            }
         }
      }
      // 创建子组件
      const Demo2 = {
         // 组件中的data是一个方法，与返回值（与Vue的对象创建不同）
         data:function(){
            return {
               dataList:[
                  {"id": 1, "title": "111"},
                  {"id": 2, "title": "222"},
               ]
            }
         },
         template: `
         <div>
            <h1>数据列表</h1>
            <table border="1">
               <thead>
                  <tr><th>ID</th><th>标题</th></tr>
               </thead>
               <tbody><tr v-for="item in dataList">
                  <td>{{item.id}}</td><td>{{item.title}}</td>
               </tr></tbody>
            </table>
         </div>
      `
      }

      // 将组件挂载到当前页面
      var app = new Vue({
         el: '#app',
         data: {"name":"张三"},
         components: {
            Demo1, //直接放组件的名字
            D2: Demo2 //使用别名
         },
         methods: {}
      })
   </script>
</body>
</html>
```

#### 全局组件

相较于局部组件，无需挂载即可使用。

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>全局组件</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
</head>
<body>
   <div id="app">
      <h1>当前页面</h1>
      {{name}}
      <h1>在页面中引入组件</h1>
      <Demo1></Demo1>
      <Demo2></Demo2>
      <hr/>
   </div>
   <script>
      // 创建全局组件
      Vue.component('Demo1',{
         data:function(){
            return {msg: '哈哈哈哈'}
         },
         template: `
         <div>
            <h1>{{msg}}</h1>
            <input type="text" v-model="msg" />
            <input type="button" @click="showMsg" value="展示">
         </div>
         `,
         methods: {
            showMsg:function(){
               alert(this.msg);
            }
         }
      })
      // 创建全局组件
      Vue.component('Demo2',{
         // 组件中的data是一个方法，与返回值（与Vue的对象创建不同）
         data:function(){
            return {
               dataList:[
                  {"id": 1, "title": "111"},
                  {"id": 2, "title": "222"},
               ]
            }
         },
         template: `
         <div>
            <h1>数据列表</h1>
            <table border="1">
               <thead>
                  <tr><th>ID</th><th>标题</th></tr>
               </thead>
               <tbody><tr v-for="item in dataList">
                  <td>{{item.id}}</td><td>{{item.title}}</td>
               </tr></tbody>
            </table>
         </div>
      `
      })

      // 无需挂载
      var app = new Vue({
         el: '#app',
         data: {"name":"张三"},
         methods: {}
      })
   </script>
</body>
</html>
```

#### vue-router组件

##### vue-router简介

Vue Router 是 Vue.js 官方的路由管理器，它支持在 Vue 应用中实现单页应用（SPA）的路由功能。通过使用 Vue Router，可以将应用划分为多个页面（组件），并通过 URL 来导航和加载这些页面，实现前端路由的功能。
Vue Router 的核心概念包括路由器（Router）、路由（Route）和路由组件（Router Component）：

1. **路由器（Router）**：Vue Router 实例化的对象，负责管理整个应用的路由配置。它通过创建不同的路由规则和映射关系，来定义不同路径对应的组件渲染。
2. **路由（Route）**：路由是指 URL 和组件之间的映射关系。每个路由都有一个路径（path）和对应的组件（component）。当用户访问某个路径时，路由器会根据配置的路由规则找到匹配的组件，并将其渲染到指定的位置。
3. **路由组件（Router Component）**：路由组件是指根据不同的路径加载的组件。它们可以是 Vue 单文件组件或普通的组件。每个路由组件都可以包含自己的子路由和嵌套路由。

使用 Vue Router 的基本步骤如下：

1. 安装和引入：通过 npm 或 yarn 安装 Vue Router，并在项目中引入。
2. 创建路由实例：创建一个 Vue Router 实例，并配置路由规则。可以使用 `Vue.use(VueRouter)` 来注册路由器。
3. 定义路由组件：创建需要用到的路由组件，可以是单文件组件或普通组件。
4. 配置路由规则：在路由实例中配置路由规则，即定义路径和对应的组件。
5. 渲染路由组件：在 Vue 根实例中，通过 `<router-view>` 组件来渲染匹配到的路由组件。
6. 导航：使用 `<router-link>` 组件或编程式导航方式（如 `router.push()`）进行页面之间的跳转和导航。

通过 Vue Router，可以实现诸如动态路由、嵌套路由、路由传参、路由守卫等高级功能，以满足不同的业务需求。
需要注意的是，Vue Router 是针对 Vue.js 开发的，它与 Vue.js 深度集成，依赖于 Vue.js， 提供了一种方便的方式来管理前端路由。

官方地址：`https://router.vuejs.org/zh/`
下载地址：`https://unpkg.com/vue-router@4`

一个页面呈现多种界面的效果：
基于vue开发多个组件，例如：活动组件、课程组件、咨询组件
在页面上vue-router用来管理这些组件，用户点击某个按钮就显示特定的组件（数据基于Ajax获取）。

引用：

```html
<!-- vue-router.js依赖 vue.js -->
<script src="vue.js"></script>
<script src="vue-router.js"></script>
```

##### Vue Router 的使用

1. 需要安装和引入 Vue Router：`npm install vue-router --save`
2. 在项目中引入 Vue Router：

   ```javascript
   import Vue from 'vue'
   import VueRouter from 'vue-router'

   Vue.use(VueRouter)
   ```

3. 创建一个路由实例，并配置路由规则。

   ```javascript
   import Home from './views/Home.vue'
   import About from './views/About.vue'

   const router = new VueRouter({
   routes: [
      {
         path: '/',
         name: 'home',
         component: Home
      },
      {
         path: '/about',
         name: 'about',
         component: About
      }
   ]
   })
   ```

   这里定义了两个路由规则，分别对应路径 `/` 和 `/about`，并分别指定了对应的组件 `Home` 和 `About`。

4. 在 Vue 根实例中，通过 `<router-view>` 组件来渲染匹配到的路由组件：

   ```html
   <div id="app">
   <router-view></router-view>
   </div>
   ```

5. 使用 `<router-link>` 组件或编程式导航方式进行页面之间的跳转和导航：

   ```html
   <router-link to="/">Home</router-link>
   <router-link to="/about">About</router-link>

   <!-- 或者编程式导航 -->
   <button @click="$router.push('/')">Go Home</button>
   <button @click="$router.push('/about')">Go About</button>
   ```

完整的代码如下：

```javascript
import Vue from 'vue'
import VueRouter from 'vue-router'
import Home from './views/Home.vue'
import About from './views/About.vue'

Vue.use(VueRouter)

const router = new VueRouter({
  routes: [
    {
      path: '/',
      name: 'home',
      component: Home
    },
    {
      path: '/about',
      name: 'about',
      component: About
    }
  ]
})

new Vue({
  el: '#app',
  router,
  render: h => h(App)
})
```

当用户访问 `/` 路径时，会渲染 `Home` 组件；当用户访问 `/about` 路径时，会渲染 `About` 组件。同时，可以通过 `<router-link>` 组件或编程式导航方式进行页面之间的跳转和导航。

##### vue-router使用

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>vue-router</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
   <!-- 版本不兼容会报错：VueRouter is not a constructor -->
   <script src="vue-router@3.js"></script>

   <style>
      body {
         margin: 0;
      }
      .container {
         width: 980px;
         margin: 0 auto;
      }
      .menu {
         height: 48px;
         background-color: #399;
         line-height: 48px;
      }
      .menu a {
         color: white;
         text-decoration: none;
         padding: 0 10px;
      }
   </style>
</head>
<body>
   <div id="app">
      <div class="menu">
         <div class="container">
            <router-link to="/">Logo</router-link>
            <router-link to="/home">首页</router-link>
            <router-link to="/course">课程</router-link>
            <router-link to="/news">资讯</router-link>
         </div>
      </div>
      <div class="container">
         <router-view></router-view>
      </div>
   </div>
   <script>
      const Home = {template: '<div>首页内容</div>'};
      const Course = {template: '<div>课程内容</div>'};
      const News = {template: '<div>资讯内容</div>'};
      
      const router = new VueRouter({
         routes: [
            {path: "/", component: Home},
            {path: '/home', component: Home},
            {path: '/course', component: Course},
            {path: '/news', component: News},
         ],
      });

      var app = new Vue({
         el: '#app',
         data: {"name":"张三"},
         methods: {},
         router: router
      });
   </script>
</body>
</html>
```

##### vue-router案例

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>vue-router</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
   <!-- 版本不兼容会报错：VueRouter is not a constructor -->
   <script src="vue-router@3.js"></script>
   <script src="https://unpkg.com/axios/dist/axios.min.js"></script>

   <style>
      body {
         margin: 0;
      }
      .container {
         width: 980px;
         margin: 0 auto;
      }
      .menu {
         height: 48px;
         background-color: #399;
         line-height: 48px;
      }
      .menu a {
         color: white;
         text-decoration: none;
         padding: 0 10px;
      }
   </style>
</head>
<body>
   <div id="app">
      <div class="menu">
         <div class="container">
            <router-link to="/">Logo</router-link>
            <router-link to="/home">首页</router-link>
            <router-link to="/course">课程</router-link>
            <router-link to="/news">资讯</router-link>
         </div>
      </div>
      <div class="container">
         <router-view></router-view>
      </div>
   </div>
   <script>
      const Home = {
         data: function(){
            return {title: "欢迎"}
         },
         template: '<div>{{title}}</div>'
      };
      const Course = {
         data: function(){
            return {courseList: []}
         },
         created:function(){
            /* 组件创建完成之后自动触发（此时组件的对象已创建，但还未将页面相关的DOM创建并显示在页面上）
            - 可以操作组件对象，例如：this.courseList = [11,22,33]
            - 无法操作DOM，例如：document.getElementById，因为未创建 */
            axios({
               method:"get",
               url: 'https://api.luffycity.com/api/v1/course/actual/?limit=5&offset=0',
               headers: {"Content-Type": "application/json"}
            }).then((res) => {
               this.courseList = res.data.data.result;
            })
         },
         mounted:function(){
            // DOM对象已在页面上生成，此时可以操作DOM对象。
         },
         template: `
         <div class="course-list">
            <div class="item" v-for="item in courseList">
               <img :src="item.cover" alt="">
               <a>{{item.name}}</a>
            </div>
         </div>
         `
      };
      const News = {
         data: function(){return {dataList: []}},
         created: function(){
            // api网页访问没问题，但axios无法访问
            axios({
               method: "get",
               url: 'https://api.luffycity.com/api/v1/course/actual/?limit=5&offset=10',
               headers:{"Content-Type": "application/json"}
            }).then((res) => {
               console.log(res.data)
               this.dataList = res.data.result;
            })
         },
         template: `<ul><li v-for="item in dataList">{{item.name}}</li></ul>`
      };
      
      const router = new VueRouter({
         routes: [
            {path: "/", component: Home},
            {path: '/home', component: Home},
            {path: '/course', component: Course},
            {path: '/news', component: News},
         ],
      });

      var app = new Vue({
         el: '#app',
         data: {"name":"张三"},
         methods: {},
         router: router
      });
   </script>
</body>
</html>
```

##### 路由和传值

当某个组件可以根据某些参数值的不同，展示不同效果时，需要用到动态路由。
例如：访问网站看到课程列表，点击某个课程，就可以跳转到课程详细页面（根据课程ID不同展示不同数据）。

1. 定义路由

   ```javascript
   const router = new VueRouter({
      routes:[
         {path: '/', component: Home },
         {path: '/course', component: Course, name: "Course" },
         {path: '/detail/:id', component: Detail, name: "Detail" },
      ],
   })
   ```

2. HTML展示

   ```html
   <div id="app">
      <div class="menu">
         <div class="container">
            <router-link to="/">首页</router-link>
            <router-link to="/course">课程</router-link>
            <router-link :to="{path: '/course'}">课程</router-link>
            <router-link :to="{name: 'Course'}">课程</router-link>

            <router-link :to="{path: '/course?size=19&page=2'}">课程</router-link>
            <router-link :to="{name: 'Course', query:{size:19,page:2}}">课程</router-link>

            <router-link :to="{path: '/detail/2', query:{size:123}}">Linux</router-link>
            <router-link :to="{name: 'Detail', params:{id:3}, query:{size:29}}">网络安全</router-link>
         </div>
      </div>
      <div class="container">
         <h1>内容区域</h1>
         <router-view></router-view>
      </div>
   </div>
   ```

3. 组件获取URL传值和GET参数

   ```javascript
   const Detail = {
      data: function(){
         return {
            title: "详细页面",
            paramDict: null,
            queryDict: null,
         }
      },
      created: function(){
         this.paramDict = this.$route.params;
         this.queryDict = this.$route.query;
      },
      template: 
      `<div><h2>{{title}}</h2><div>当前请求的数据 {{paramDict}} {{queryDict}}</div></div>`
   }
   ```

##### watch属性

由于 `created`方法是在页面加载前触发的，同一个路由的跳转默认不会重新加载页面，因此无法获取数据，所以会出现无法刷新的情况，这时候就用到了watch属性。
例如：在详细页面再出现一个课程推荐，即：在课程详细，点击推荐的课程后跳转到课程详细页面（课程ID不同），此时课程的ID还是原来加载的ID，无法获取推荐课程的ID。
而watch属性会检测 $route值，一旦该值发生变化，就执行相应的函数。

```javascript
const Detail = {
   data: function(){
         return {
            title: "详细页面",
            courseId: null
         }
   },
   created: function(){
         this.courseId = this.$route.params.id;
         this.getCourseDetail();
   },
   watch: {
         $route:function(to, from){
            this.courseId = to.params.id;
            this.getCourseDetail();
         }
   },
   methods: {
         getCourseDetail: function(){
            // 根据this.courseId获取课程详细信息
         }
   },
   template: `
   <div>
         <h2>{{title}}</h2>
         <div>当前的课程ID为: {{courseId}}</div>
         <ul>
            <li v-for="item in hotCourseList">
               <router-link :to="{Detail}, params:{id:item.id}">{{item.title}}</router-link>
            </li>
         </ul>
   </div>
   `
```

##### 路由嵌套

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>vue-router</title>
   <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
   <!-- 版本不兼容会报错：VueRouter is not a constructor -->
   <script src="vue-router@3.js"></script>
   <script src="https://unpkg.com/axios/dist/axios.min.js"></script>

   <style>
      body {
         margin: 0;
      }
      .container {
         width: 980px;
         margin: 0 auto;
      }
      .menu {
         height: 48px;
         background-color: #399;
         line-height: 48px;
      }
      .menu a {
         color: white;
         text-decoration: none;
         padding: 0 10px;
      }
   </style>
</head>
<body>
   <div id="app">
      <div class="menu">
         <div class="container">
            <router-link to="/">Logo</router-link>
            <router-link to="/home">首页</router-link>
            <router-link to="/pins">沸点</router-link>
            <router-link to="/course">课程</router-link>
            <router-link to="/news">资讯</router-link>
         </div>
      </div>
      <div class="container">
         <router-view></router-view>
      </div>
   </div>
   <script>
      const Home = {
         data: function(){
            return {title: "欢迎"}
         },
         template: '<div>{{title}}</div>'
      };
      const Course = {
         data: function(){
            return {courseList: []}
         },
         created:function(){
            /* 组件创建完成之后自动触发（此时组件的对象已创建，但还未将页面相关的DOM创建并显示在页面上）
            - 可以操作组件对象，例如：this.courseList = [11,22,33]
            - 无法操作DOM，例如：document.getElementById，因为未创建 */
            axios({
               method:"get",
               url: 'https://api.luffycity.com/api/v1/course/actual/?limit=5&offset=0',
               headers: {"Content-Type": "application/json"}
            }).then((res) => {
               this.courseList = res.data.data.result;
            })
         },
         watch: {
            $route:function(to, from){
               this.courseId = to.params.id;
               this.getCourseDetail();
            }
         },
         methods: {
            getCourseDetail: function(){
               // 根据this.courseId获取课程详细信息
            }
         },
         mounted:function(){
            // DOM对象已在页面上生成，此时可以操作DOM对象。
         },
         template: `
         <div class="course-list">
            <div class="item" v-for="item in courseList">
               <img :src="item.cover" alt="">
               <a>{{item.name}}</a>
            </div>
         </div>
         `
      };
      const News = {
         data: function(){return {dataList: []}},
         created: function(){
            // api网页访问没问题，但axios无法访问
            axios({
               method: "get",
               url: 'https://api.luffycity.com/api/v1/course/actual/?limit=5&offset=10',
               headers:{"Content-Type": "application/json"}
            }).then((res) => {
               console.log(res.data)
               this.dataList = res.data.result;
            })
         },
         template: `<ul><li v-for="item in dataList">{{item.name}}</li></ul>`
      };
      const Detail = {
         data: function(){
            return {
               title: "详细页面",
               courseId: null,
               hotCourseList: []
            }
         },
         created: function(){
            this.courseId = this.$route.params.id;
            this.getCourseDetail();
         },
         watch: {
            $route:function(to, from){
               this.courseId = to.params.id;
               this.getCourseDetail();
            }
         },
         methods: {
            getCourseDetail: function(){
               // 根据this.courseId获取课程详细信息
            }
         },
         template: `
         <div>
            <h2>{{title}}</h2>
            <div>当前的课程ID为: {{courseId}}</div>
            <ul>
               <li v-for="item in hotCourseList">
               <router-link :to="{name: 'Detail'}, params:{id:item.id}">{{item.title}}</router-link>
               </li>
            </ul>
         </div>`
         };
      const Pins = {
         data: function(){
            return {}
         },
         template: `
            <div>
               <h2>沸点专区</h2>
               <router-link :to="{name: 'Hot'}">热点</router-link>
               <router-link :to="{name: 'Following'}">关注</router-link>
               <router-view></router-view>
            </div>`
      };
      const Hot = {template: '<span>热点</span>'};
      const Following = {template: '<span>关注</span>'};
      const router = new VueRouter({
         routes: [
            {path: "/", component: Home},
            {path: '/home', component: Home},
            {path: '/course', component: Course},
            {path: '/news', component: News},
            {path: '/detail/:id', component: Detail, name: 'Detail'},
            {
               path: '/pins',
               component: Pins,
               children: [
                  // 当 /pins/hot 匹配成功，Hot组件会被渲染在Pins的 <router-view>中
                  {path: 'hot', component: Hot, name: 'Hot'},
                  {path: 'following', component: Following, name: 'Following'}
               ]
            }
         ],
      });

      var app = new Vue({
         el: '#app',
         data: {"name":"张三"},
         methods: {},
         router: router
      });
   </script>
</body>
</html>
```

##### 编程式导航

除了使用 `<router-link>` 创建 a标签来定义导航链接，还可以借助router的实例方法，通过编写代码来实现。
想要导航到不同的URL，则使用`router.push`方法，它会向history栈添加一个新的记录，使用户点击浏览器后退按钮时，回到之前的URL。

1. `router.push`

   ```javascript
   // 字符串
   router.push('home')
   // 对象
   router.push({path: 'home'})
   // 命名的路由
   router.push({name: 'user', params: {userId: '123'}})
   // 带查询参数，/register?plan=private
   router.push({ path: 'register', query: {plan: 'private'}})
   ```

2. `router.replace`：跟 `router.push` 很像，但它不会向history添加新记录，而是跟它的方法名一样，替换掉当前的history记录。

   ```javascript
   // 字符串
   router.replace('home')
   // 对象
   router.replace({path, 'home'})
   // 命名的路由
   router.replace({name: 'user', params: {userId: '123'}})
   // 带查询参数
   router.replace({path: 'regisger', query: {plan: 'private'}})
   ```

3. `router.go`：参数是一个整数，意思是在history记录中前进几步。

   ```javascript
   // 在浏览器记录中前进一步，等同于history.forward()
   router.go(1)
   // 后退一步，等同于history.back()
   router.go(-1)
   // 前进三步
   router.go(3)
   ```

##### 导航守卫

基于vue-router实现访问跳转时，会执行一个钩子。

```javascript
const router = new VueRouter({});

router.beforeEach((to, from, next) => {
   // to: Route  即将要进入的目标，路由对象
   // from: Route  当前导航正要离开的路由
   // next()  继续向后执行
   // next(false) 中断导航，保持当前所在页面
   // next('/'), next({path: '/'}), next({name: 'Login'})  跳转到指定页面
})
```

#### vue案例

## rbac 权限系统

### 系统规划

v1，直接实现

1. 设计和实现
   1. 确定项目共有多少角色：管理员、财务、审核……
   2. 每个角色都具备的什么功能权限
2. 前端
   1. 登录：选择角色+登录， vuex => token、role
   2. 后台管理
      1. 动态菜单，每种角色加载自己的菜单
         1. vuex中保存当前用户角色role
         2. 定义路由

            ```javascript
            {
               path: 'menu',
               name: 'menu',
               component: () => import('@/views/admin/MenuView.vue'),
               meta:{is_menu:true, role:['admin', 'user']},
            }
            ```

         3. 打开页面，读取所有路由，筛选 `is_menu=true` && role合法的
      2. 是否有权限访问页面（路由）-基于路由的导航守卫实现
         1. 读取vuex中保存的当前用户角色 role
         2. 获取当前要访问的路由 to, 找到规定可以访问的roleList
         3. 判断是否有权限
      3. 页面的局部功能是否有权限：增删改查
         1. 展示：无权限不展示（vuex中保存当前用户角色role判断是否有此功能）
         `<el-button v-permission="['admin', 'manager']">新建</el-button> //自定义v-permission，是该角色才展示按钮`
         2. 功能：例如页面加载发送ajax请求

            ```javascript
            if (hasPermission)(["admin", "manager"]){
               ...
            }
            //自定义方法，符合该角色才执行该方法
            ```

3. 后端
   1. 用户登录成功，返回token凭证
   2. 登录后访问，通过认证组件保证凭证正确 + role
   3. 权限的校验
      1. 在每个视图中获取role，判断是否有权限访问

         ```python
         class UserView(APIView):
            def post(self, request):
               if request.user.role == 'admin':
                  pass
               else:
                  pass
         ```

      2. 基于drf的权限组件

         ```python
         class MyPermission():
            def has_permission():
               request.method
               if request.user.role == 'admin':
                  pass
               else:
                  pass


         class UserView(APIView):
            permission_classes = [MyPermission, ]
         ```

      3. 基于配置+权限组件
         1. 路由
            - `path('api/users/', UserView.as_view(), name="User"),`
            - `router = routers.SimpleRouter(); router.register(r'api/users/', views.UserView, basename='user')`
              - `user-list`: `GET api/users/`, `POST api/users/` ...
              - `user-detail`: `GET api/users/11`, `PUT api/users/11`, `DELETE api/users/11`...
         2. `settings.py`

            ```python
            PERMISSION = {
               'admin': {
                  'order': ["GET", "POST", "PUT"],
                  'user-list': ["GET", "POST", "PUT"],
               },
               'user': {},
               'manager': {},
            }
            ```

         3. 权限组件

            ```python
            class MyPermission(...):
               def has_permission(...):
                  # 1. 根据角色获取当前用户拥有的所有权限 request.user
                  # 2. 获取当前用户访问的路由信息 request.match_resolver.url_name
                  # 3. 判断当前访问路由是否在其权限之内 `if url_name in PERMISSION:`
                  # 4. 判断当前的访问方法是否被允许 request.method


            class UserView(APIView):
               permission_classes = [MyPermission, ]
            ```

### 功能实现-vue

1. 创建项目
   1. 安装Node.js：访问Node.js官方网站（`https://nodejs.org`）并下载适合操作系统的安装程序。按照安装向导进行安装。
   2. 验证Node.js和npm安装是否成功。 `node -v` 或 `npm -v`，如果能正确显示Node.js和npm的版本号，则表示安装成功。
   3. 安装Vue CLI：Vue CLI是用于快速创建Vue项目的命令行工具。在终端或命令行中运行以下命令来全局安装Vue CLI： `npm install -g @vue/cli`
   4. 创建Vue项目：在终端或命令行中进入想要创建项目的目录，并运行 `vue create 项目名` 命令来创建Vue项目。
   5. 定制化配置（可选）：Vue CLI会有一些预设模板供选择。可以选择默认的预设配置，也可以自定义配置。根据提示选择或输入对应的数字或内容。
      1. `vue add vuex`
      2. `vue add router`
   6. 安装项目依赖：创建项目后，进入项目目录，在终端或命令行中运行 `npm install` 命令，安装项目所需的依赖。
   7. 运行项目：安装完依赖后，运行 `npm run serve` 命令来启动Vue项目，运行成功后，会显示一个URL地址，将其复制到浏览器中打开，就可以看到创建的Vue项目了。
2. 创建基本路由：`src/router/index.js`

   ```js
   import { createRouter, createWebHistory } from 'vue-router';
   const routes = [
   {
      path: '/login',
      name: 'login',
      component: () => import('../views/LoginView.vue'),
   },
   {
      path: '/admin',
      name: 'admin',
      component: () => import('../views/AdminView.vue'),
      children: [
         {
         path: 'basic',
         name: 'basic',
         component: () => import('../views/admin/BasicView.vue'),
         meta: {role: ["admin", "manager", "user"], title: "基本配置", is_menu: true},
         },
         {
         path: 'user',
         name: 'user',
         component: () => import('../views/admin/UserView.vue'),
         meta: {role: ["admin", "manager"], title: "用户管理", is_menu: true},
         },
         {
         path: 'order',
         name: 'order',
         component: () => import('../views/admin/OrderView.vue'),
         meta: {role: ["admin"], title: "订单管理", is_menu: true},
         },
      ]
   },
   ]
   ```

3. 创建基本页面
   1. `src/App.vue`

      ```vue
      <template>
      <router-view/>
      </template>

      <style>
      body {
      margin: 0;
      }
      </style>
      ```

   2. `src/views/LoginView.vue`

      ```vue
      <template>
         <div class="box">
            <p>
                  <input type="text" placeholder="用户名" v-model="state.user">
            </p>
            <p>
                  <input type="password" placeholder="密码" v-model="state.pwd">
            </p>
            <p>
                  <select v-model="state.role">
                     <option :value="ele.value" v-for="ele in state.roleList" :key="ele.value">{{ ele.text }}</option>
                  </select>
            </p>
            <p>
                  <input type="button" value="登 录" @click="doLogin" />
            </p>
         </div>
      </template>

      <script setup>
      import { reactive } from "vue";
      import { useStore } from "vuex";
      import { useRouter } from "vue-router";

      const store = useStore();
      const router = useRouter();

      const state = reactive({
         user: "张三",
         pwd: "123123",
         role: "user",
         roleList: [
            { text: "管理员", value: "admin" },
            { text: "经理", value: "manager" },
            { text: "用户", value: "user" },
         ]
      });

      function doLogin() {
         // 1. 向后台发送请求并且登录成功
         // 2. 返回信息
         const context = {
            token: state.user + "123123",
            role: state.role,
         };
         // 3. 保存到vuex
         store.commit("login", context);
         // 4. 跳转后台
         router.replace({name:"basic"})
      }
      </script>

      <style scoped>
      .box {
         border: 1px solid #ddd;
         width: 300px;
         margin: 200px auto;
         padding: 30px;
      }
      </style>
      ```

   3. `src/views/AdminView.vue`

      ```vue
      <template>
         <div>
            <div class="pg-header"></div>
            <div class="pg-body">
                  <div class="left-menu">
                     <router-link v-for="item in routerList" :to="{name:item.name}" :key="item.name">{{ item.meta.title }}</router-link>
                  </div>
                  <div class="right-content" style="flex-grow: 1;">
                     <router-view></router-view>
                  </div>
            </div>
         </div>
      </template>

      <script setup>
      import { computed } from 'vue';
      import { useRouter } from 'vue-router';
      import { useStore } from 'vuex';

      const router = useRouter();
      const store = useStore();
      const routerList = computed(() => {
         // console.log(router.getRoutes());

         /*
         // 数组的 filter 方法会根据这个函数的返回值来决定是否保留元素，如果返回值为真，就将该元素保留在数组中；否则过滤掉该元素。
         let v1 = [11, 22, 33, 44];
         let v2 = v1.filter(item => {
            if (item > 22) {
                  return 999;
            }
         });
         console.log(v2);*/

         // 两种写法之一
         // let role = store.state.role;
         // let routerData = router.getRoutes().filter(item => {
         //     if (item.meta.title && item.meta.role.indexOf(role) !== -1) {
         //         return item;
         //     }
         // });
         // return routerData;

         // 两种写法之二
         let totalRouteList = router.getRoutes();
         return totalRouteList.filter(item => {
            if (item.meta.is_menu && item.meta.role.indexOf(store.state.role) !== -1){
                  return true;
            }
         })
      });

      </script>

      <style scoped>
      .pg-header {
         height: 48px;
         background-color: brown;
      }
      .pg-body {
         display: flex;
         flex-direction: row;
      }
      .pg-body .left-menu {
         width: 280px;
         background-color: aliceblue;
         height: calc(100vh - 48vh);
      }
      .pg-body .left-menu a {
         display: block;
         padding: 8px 10px;
         border-bottom: 1px solid #dddddd;
      }
      .pg-body .right-content {
         background-color: antiquewhite;
         height: calc(100vh - 48vh);
      }
      </style>
      ```

   4. `src/views/admin/BasicView.vue`

      ```vue
      <template>
         <h1>Basic</h1>
         <div v-if="permissionsGranted">
            <ul>
                  <li v-if="hasPermission(['admin', 'manager'])">增</li>
                  <li v-if="hasPermission(['admin'])">删</li>
                  <li v-if="hasPermission(['admin'])">改</li>
                  <li v-if="hasPermission(['admin', 'manager', 'user'])">查</li>
                  <li v-buttonpermission="['admin']">自定义指令</li>
            </ul>
         </div>
         <div v-else>
            <p>您没有访问该页面的权限。</p>
         </div>
      </template>

      <script setup>
      import { onMounted, ref } from 'vue';
      import { hasPermission } from '@/store/buttonpermission';

      const permissionsGranted = ref(false);

      onMounted(() => {
         initPage()
      });

      function initPage() {
      if (!hasPermission(['admin', 'manager'])) {
         permissionsGranted.value = false;
      } else {
         permissionsGranted.value = true;
      }
      }
      </script>

      <style scoped></style>
      ```

   5. `src/views/admin/OrderView.vue`

      ```vue
      <template>
         <h1>Order</h1>
      </template>

      <script>
         export default { name: 'OrderView' }
      </script>

      <style scoped></style>
      ```

   6. `src/views/admin/UserView.vue`

      ```vue
      <template>
         <h1>User</h1>
      </template>

      <script>
         export default { name: 'UserView' }
      </script>

      <style scoped></style>
      ```

4. 是否有权限访问路由-导航守卫：`src/router/index.js`

   ```js
   import { createRouter, createWebHistory } from 'vue-router';
   import store from '@/store';

   const routes = [
   {
      path: '/login',
      name: 'login',
      component: () => import('../views/LoginView.vue'),
   },
   {
      path: '/admin',
      name: 'admin',
      component: () => import('../views/AdminView.vue'),
      children: [
         {
         path: 'basic',
         name: 'basic',
         component: () => import('../views/admin/BasicView.vue'),
         meta: {role: ["admin", "manager", "user"], title: "基本配置", is_menu: true},
         },
         {
         path: 'user',
         name: 'user',
         component: () => import('../views/admin/UserView.vue'),
         meta: {role: ["admin", "manager"], title: "用户管理", is_menu: true},
         },
         {
         path: 'order',
         name: 'order',
         component: () => import('../views/admin/OrderView.vue'),
         meta: {role: ["admin"], title: "订单管理", is_menu: true},
         },
      ]
   },
   ]

   const router = createRouter({
   history: createWebHistory(process.env.BASE_URL),
   routes
   })

   // 导航守卫
   router.beforeEach((to, from, next) => {
   // 1. 当前访问的路由
   // console.log(to);
   // next();
   if (to.meta.role) {
      // 2. 获取当前vuex中自己的角色
      // 3. to.meta.role 就是允许的角色列表 ["admin"]
      let userRole = store.state.role;
      let allowRoleList = to.meta.role;

      if (allowRoleList.indexOf(userRole) === -1) {
         next({ name: "login" });
      } else {
         next();
      }
   } else {
      next();
   }
   })

   export default router
   ```

   `src/store/index.js`

   ```javascript
   import { createStore } from 'vuex'

   export default createStore({
   state: {
      // 初始状态，从本地存储中获取token，如果不存在则为空字符串
      token: localStorage.getItem("token") || "",
      // 同上，从本地存储中获取role，如果不存在则为空字符串
      role: localStorage.getItem("role") || "",
   },
   getters: {
      // 这里可以定义一些派生状态的方法
   },
   mutations: {
      // 定义修改state的方法，这里是登录操作
      login(state, { token, role }) {
         state.token = token;  // 设置state中的token为传入的token
         state.role = role;    // 设置state中的role为传入的role
         localStorage.setItem('token', token);  // 将token存储到本地存储中
         localStorage.setItem('role', role);    // 将role存储到本地存储中
      }
   },
   actions: {
      // 这里可以定义一些异步操作，如发送网络请求等
   },
   modules: {
      // 这里可以引入其他模块
   }
   })
   ```

5. 动态菜单（菜单本质是路由-meta参数）：读取所有路由并筛选出`is_menu:true`的，来拿到菜单列表`[{title: "", name: ""},{title: "", name: ""},]`
6. 按钮显示权限
7. 自定义指令

   `src/directives/buttonpermission.js`

   ```js
   import store from "@/store";

   export default {
      mounted(el, bindings) {
         let allowRoleList = bindings.value;
         let userRole = store.state.role;

         // 无权限则不加载
         if (allowRoleList.indexOf(userRole) === -1) {
               // 删除元素，不再加载
               el.parentNode && el.parentNode.removeChild(el);
         }
      }
   }
   ```

   `src/directives/index.js`

   ```js
   import buttonpermission from "./buttonpermission";

   // 批量注册指令（现在就一个buttonpermission）
   const directives = {
      buttonpermission
   }

   // 注册的一般写法，循环遍历derectives，通过vue.directive注册
   export default {
      install(Vue) {
         Object.keys(directives).forEach(key => {
               Vue.directive(key, directives[key])
         });
      }
   }
   ```

   `src/main.js`

   ```js
   import { createApp } from 'vue'
   import App from './App.vue'
   import store from './store'
   import router from './router'
   import directives from './directives'

   createApp(App).use(router).use(store).use(directives).mount('#app')
   ```

### 功能实现-DRF

#### 配置相关

1. 创建后端项目
2. 创建数据库并授权:

   ```sql
   -- 创建Wiki用户
   CREATE USER 'wiki'@'localhost' IDENTIFIED BY 'wikipass';

   -- 授予Wiki库权限
   GRANT ALL PRIVILEGES ON `wiki`.* TO 'wiki'@'localhost';
   ```

3. 创建名为api的app
4. 安装依赖包：`pip install django pymysql django-redis`
5. 配置 `rbac/__init__.py`

   ```python
   import pymysql

   pymysql.install_as_MySQLdb()
   ```

6. 配置权限 `settings.py`

   ```py
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'api.apps.ApiConfig',
      'rest_framework',
   ]

   DATABASES = {
      'default': {
         'ENGINE': 'django.db.backends.mysql',
         'NAME': 'wiki',
         'USER': 'wiki',
         'PASSWORD': 'wikipass',
         'HOST': '127.0.0.1',
         'POST': 3306
      }
   }

   LANGUAGE_CODE = 'zh-hans'

   TIME_ZONE = 'Asia/Shanghai'

   DATETIME_FORMAT = "Y年m月d日"

   # drf 配置
   REST_FRAMEWORK = {
      "UNAUTHENTICATED_USER": None,
   }

   # 权限配置
   PERMISSIONS = {
      "admin": {
         "depart-list": ["GET", "POST"],
         "depart-detail": ["GET", "POST", "PUT", "PATCH", "DELETE"],
      },
      "user": {
         "depart-list": ["GET"],
      },
      "manager": {
         "depart-list": ["GET", "POST"],
      },
   }
   ```

#### 框架构建

1. 创建用户表 `models.py`

   ```py
   from django.db import models


   class UserInfo(models.Model):
      """用户表"""
      user = models.CharField(verbose_name="用户名", max_length=32)
      pwd = models.CharField(verbose_name="密码", max_length=64)
      role_choices = (
         ("admin", "管理员"),
         ("user", "用户"),
         ("manager", "经理"),
      )
      role = models.CharField(verbose_name="角色", max_length=16, choices=role_choices, default="user")

   class Depart(models.Model):
      """部门表"""
      depart_name = models.CharField(verbose_name="部门名称", max_length=32)
      count = models.IntegerField(verbose_name="人数")
   ```

   `python manage.py makemigrations; python manage.py migrate`

2. `views.py`

   ```python
   from rest_framework.viewsets import ModelViewSet  # 导入ModelViewSet视图集
   from rest_framework import serializers  # 导入序列化模块
   from api import models  # 导入自定义的模型

   # 创建一个名为DepartSerializer的序列化器，继承自ModelSerializer
   class DepartSerializer(serializers.ModelSerializer):
      class Meta:
         model = models.Depart  # 指定要序列化的模型为models.Depart
         fields = "__all__"  # 序列化所有字段

   # 创建一个名为DepartView的视图集，继承自ModelViewSet
   class DepartView(ModelViewSet):
      queryset = models.Depart.objects.all()  # 指定查询集为models.Depart的所有对象
      serializer_class = DepartSerializer  # 指定使用DepartSerializer进行序列化
   ```

3. `urls.py`

   ```python
   from django.urls import path, include  # 导入path和include函数
   from rest_framework import routers  # 导入rest_framework中的路由器模块
   from api import views  # 从api模块导入views模块

   router = routers.SimpleRouter()  # 创建一个SimpleRouter实例

   # 使用router对象注册一个名为'depart'的路由，并将其关联到DepartView视图集，设置basename为'depart'
   router.register('depart', views.DepartView, basename='depart')

   urlpatterns = [
      path('api/', include(router.urls))  # 将router.urls包含在'/api/'路径下
   ]
   ```

4. 认证校验和权限校验 `views.py`

   ```python
   from rest_framework.viewsets import ModelViewSet
   from rest_framework import serializers
   from rest_framework.authentication import BaseAuthentication
   from rest_framework.permissions import BasePermission
   from rest_framework import exceptions
   from api import models
   from django.conf import settings


   class User(object):
      def __init__(self, name=None, role=None):
         self.name = name
         self.role = role


   class DepartSerializer(serializers.ModelSerializer):
      class Meta:
         model = models.Depart
         fields = "__all__"


   class DepartAuthentication(BaseAuthentication):
      def authenticate(self, request):
         # 读取用户请求token，校验是否合法
         token = request.query_params.get("token")
         role = request.query_params.get("role")
         if not token:
            raise exceptions.AuthenticationFailed("认证失败！")

         return (User("张三", role), None)

      def authenticate_header(self, request):
         return "API"


   class DepartPermission(BasePermission):
      def has_permission(self, request, view):
         # 1. 获取当前用户所有的权限
         permission_dict = settings.PERMISSIONS[request.user.role]
         # 2. 获取当前用户访问的URL和方式
         url_name = request.resolver_match.url_name
         # 3. 权限判断
         method_list = permission_dict.get(url_name)
         method = request.method
         if not method_list:
            return False
         if method not in method_list:
            return False
         return True

      def has_object_permission(self, request, view, obj):
         return True


   class DepartView(ModelViewSet):
      queryset = models.Depart.objects.all()
      serializer_class = DepartSerializer
      authentication_classes = [DepartAuthentication, ]
      permission_classes = [DepartPermission, ]
   ```

5. 返回值：用状态码 `Response({"code": 1000, "data": []}, status=?)`；不用状态码：把返回值中的status去掉。`{"code": "", "data": []}` 或 `{"code": "", "detail": []}`。
    - 正常：通过自定义继承自 `GenericViewSet` 类的 `ViewSet` 类中的`finalize_response`方法来实现。 `/rbac/utils/viewsets.py`

      ```python
      from rest_framework.viewsets import GenericViewSet as DrfGenericViewSet
      from rest_framework import mixins


      class GenericViewSet(DrfGenericViewSet):
         def finalize_response(self, request, response, *args, **kwargs):
            response = super().finalize_response(request, response, *args, **kwargs)
            if response.exception:
               return response
            response.data = {'code': 0, 'data': response.data}
            return response


      class ModelViewSet(mixins.CreateModelMixin, mixins.RetrieveModelMixin, mixins.UpdateModelMixin, mixins.DestroyModelMixin, mixins.ListModelMixin, GenericViewSet):
         pass
      ```

    - 异常：通过自定义`exception_handler`方法来实现。 `/rbac/utils/handlers.py`

      ```python
      from django.http import Http404
      from rest_framework import exceptions
      from rest_framework.response import Response
      from rest_framework.exceptions import ValidationError
      from rest_framework.exceptions import Throttled
      from rest_framework.exceptions import PermissionDenied
      from rest_framework.exceptions import NotAuthenticated
      from rest_framework.exceptions import AuthenticationFailed
      from rest_framework.views import set_rollback


      def exception_handler(exc, context):
         if isinstance(exc, Http404):
            exc = exceptions.NotFound()
            exc.ret_code = 1001
         elif isinstance(exc, PermissionDenied):
            exc = exceptions.PermissionDenied()
            exc.ret_code = 1002
         elif isinstance(exc, (AuthenticationFailed, NotAuthenticated)):
            exc.ret_code = 1003
         elif isinstance(exc, Throttled):
            exc.ret_code = 1004
         elif isinstance(exc, ValidationError):
            exc.ret_code = 1005

         # 只处理DRF相关异常
         if isinstance(exc, exceptions.APIException):
            headers = {}
            if getattr(exc, 'auth_header', None):
               headers['WWW-Authenticate'] = exc.auth_header
            if getattr(exc, 'wait', None):
               headers['Retry-After'] = '%d' % exc.wait

            if isinstance(exc.detail, (list, dict)) and "code" in exc.detail:
               data = exc.detail
            else:
               code = getattr(exc, 'ret_code', None) or -1
               data = {'code': code, 'detail': exc.detail}

            set_rollback()
            return Response(data, status=exc.status_code, headers=headers)
         return None
      ```

6. axios请求
    - 安装：`npm install axios`
    - 配置：`src/axios.js`

      ```js
      import axios from 'axios';

      const instance = axios.create({
      baseURL: 'http://127.0.0.1:8000',
      // 可以添加其他默认配置
      });

      export default instance;
      ```

    - 挂载：`src/main.js`

      ```js
      import { createApp } from 'vue';
      import App from './App.vue';
      import store from './store';
      import router from './router';
      import 'element-plus/dist/index.css';
      import ElementPlus from 'element-plus';
      import { zhCn } from 'element-plus/dist/locale/zh-cn.mjs';
      // 以组件的形式导入图标
      import * as components from "@element-plus/icons-vue";
      import instance from './axios';

      const app = createApp(App)

      // 全局挂载axios实例
      app.config.globalProperties.$axios = instance;

      for (const key in components) {
         const componentConfig = components[key];
         app.component(componentConfig.name, componentConfig);
      }

      app.use(router).use(store).use(ElementPlus, {locale: zhCn}).mount('#app')
      ```

    - 使用

      ```vue
      <template>
         <div class="box">
            <p>
               <input type="text" placeholder="用户名" v-model="state.user">
            </p>
            <p>
               <input type="password" placeholder="密码" v-model="state.pwd">
            </p>
            <p>
               <input type="button" value="登 录" @click="doLogin" />
            </p>
         </div>
      </template>

      <script setup>
      import { onMounted, reactive } from "vue";
      import { useStore } from "vuex";
      import { useRouter } from "vue-router";
      import instance from "../axios";

      const store = useStore();
      const router = useRouter();

      const state = reactive({
         backendData: null, //将需要从后台获取的数据初始化为null
      });

      onMounted(() => {
         // 页面加载完成时从后台获取数据
         fetchData();
      });

      function fetchData() {
         instance.get('http://127.0.0.1:8000') //替换为实际的后台数据接口
            .then(response => {
               state.backendData = response.data;
            }).catch(error => {
               console.error("获取数据失败", error);
            });
      }

      function doLogin() {
         // 1. 向后台发送请求并且登录成功
         instance.post('/login', {
            username: state.user,
            password: state.pwd
         }).then(response => {
            // 登录成功后返回后台数据
            const context = response.data;
            // 保存到vuex
            store.commit('login', context);
            // 跳转后台：跳转到当前用户具备权限的第一个路由
            router.replace({ name: context.routers[0] });
         }).catch(error => {
            console.error('登录失败', error);
         });
      }
      </script>

      <style scoped>
      .box {
         border: 1px solid #ddd;
         width: 300px;
         margin: 200px auto;
         padding: 30px;
      }
      </style>
      ```

7. jwt + 跨域

8. 业务开发

### v2 版本-根据权限来展示菜单和按钮

1. 登录

   ```vue
   <script setup>
   const context = {
      permission: {
         "depart-list": ["GET", "POST"],
         "depart-detail": ["GET", "POST", "PUT", "PATCH", "DELETE"],
      },
      token: "xxx",
      role: state.role
   };
   </script>
   ```

2. 动态菜单与v1版本一样
3. 动态按钮：获取当前用户的所有权限：`{'depart-list': 'GET', 'POST'}`，有权限就显示，没权限就不显示

   ```vue
   <li v-if="hasPermission({'depart-list': 'GET', 'POST'})">增</li>
   <li v-if="hasPermission({'depart-detail': 'GET', 'POST', 'PUT', 'PATCH', 'DELETE'})">删</li>
   ```

### v3 版本

设计思路：

1. 角色和权限是多对多的关系
2. 用户和角色是1对1的关系
3. 用户和权限是1对多的关系
4. 菜单，即路由（一般设计为二级菜单）
   1. 一级菜单，即目录，包含菜单名和图标
   2. 二级菜单，即路由，包含菜单名、父级目录、路由的name（与权限表关联）和是否为菜单
   3. 权限表，包含路由的name、方法、路由名称、路由ID（二级菜单的id）

功能：

0. 权限管理
   1. 权限&菜单等信息的录入
   2. 用户&角色&权限的分配
1. 登录
   1. 根据用户信息获取到此用户的所有权限 permission
   2. 获取用户具有权限的路由列表 router
   3. 获取用户有权限的菜单列表 menu
2. 动态菜单，基于menu来实现
3. 页面访问权限，基于router来实现
4. 动态按钮

`https://element-plus.org/zh-CN`

### AbstractUser 类

#### 基于 AbstractUser 创建用户模型

当你想要自定义继承了 `AbstractUser` 的模型时，你可以创建一个新的模型，并在其中重新定义你想要修改或剔除的字段。下面是一个示例：

```python
from django.contrib.auth.models import AbstractUser
from django.db import models

class CustomUser(AbstractUser):
    # 添加自定义字段
    nickname = models.CharField(max_length=100)
    gender = models.CharField(max_length=10)
    
    # 重新定义字段
    email = None
    
    # 移除字段
    first_name = None

    # 添加其他自定义方法和属性
    def get_full_name(self):
        full_name = "%s %s" % (self.last_name, self.first_name)
        return full_name.strip()
```

在这个示例中，我们创建了一个名为 `CustomUser` 的模型，它继承自 `AbstractUser`。我们添加了两个自定义字段 `nickname` 和 `gender`，并将 `email` 字段设为 `None`，从而剔除了原来继承的 `email` 字段。同时，我们也将 `first_name` 字段设为 `None`，以移除原来继承的 `first_name` 字段。

此外，我们还可以根据需要添加其他自定义的方法和属性。在这个示例中，我们重新定义了 `get_full_name()` 方法，以返回用户的姓和名的组合。

#### 基于 AbstractUser 创建用户模型的优势

如果你在 `models.py` 中自定义了一个与 `AbstractUser` 类的字段相同的模型，那么这两个模型之间主要的区别在于继承关系和功能的差异。

1. 继承关系：通过继承 `AbstractUser` 类创建的模型将直接继承 Django 框架提供的用户认证功能和权限管理功能。这意味着你可以使用 Django 提供的内置方法和属性来处理用户认证、权限控制和用户管理等操作。而自定义的模型则需要自己实现这些功能。
2. 功能差异：继承 `AbstractUser` 类的模型已经实现了一些通用的用户字段和方法，例如用户名、密码、电子邮件等字段，以及登录验证、密码重置等方法。此外，`AbstractUser` 还提供了一些与用户权限相关的方法和字段。通过继承 `AbstractUser` 类，你可以快速获得这些功能，并且可以根据需要进行自定义扩展。

继承 `AbstractUser` 来创建模型的优势包括：

1. 代码复用：通过继承 `AbstractUser`，你可以直接使用 Django 提供的用户认证和权限管理功能，无需从头实现这些功能，减少了代码的编写量。
2. 集成性：继承 `AbstractUser` 的模型可以无缝地与 Django 框架中的其他部分进行集成，例如认证、授权、用户管理等模块。这样可以简化开发流程，并提高代码的可维护性和扩展性。
3. 标准化：使用 `AbstractUser` 可以使你的模型与 Django 的标准用户模型保持一致，这有助于与其他 Django 应用程序和第三方库进行交互，避免出现数据模型不匹配的问题。

当然，如果你对用户模型的需求与 `AbstractUser` 提供的功能不完全符合，或者你需要添加额外的字段和方法，那么自定义模型可能更适合你的需求。
总之，继承 `AbstractUser` 来创建模型可以为你提供快速、方便和标准化的用户认证和权限管理功能，同时也可以根据需要进行自定义扩展。

#### 功能差异

当继承 `AbstractUser` 类来创建模型时，你会自动获得一些通用的用户字段和方法，以及与用户权限相关的功能。下面是一些常见的功能差异：

1. 用户字段：继承 `AbstractUser` 的模型会包含一些常见的用户字段，例如用户名、密码、电子邮件等。这些字段已经在 `AbstractUser` 中定义，并且与 Django 的其他模块（如认证、授权）无缝集成。
2. 认证方法：通过继承 `AbstractUser`，你可以使用内置的认证方法进行用户登录和验证。例如，你可以使用 `authenticate()` 方法验证用户的用户名和密码是否匹配。
3. 权限管理：`AbstractUser` 提供了一些与用户权限相关的方法和字段。例如，你可以使用 `is_superuser` 字段来判断用户是否是超级用户，使用 `is_staff` 字段来判断用户是否是员工。此外，还有一些方法可以用于检查用户的权限，例如 `has_perm()` 和 `has_perms()`。
4. 用户管理：继承 `AbstractUser` 的模型可以使用 Django 提供的内置用户管理功能。你可以使用 `create_user()` 方法来创建新用户，使用 `set_password()` 方法来设置用户密码，使用 `check_password()` 方法来验证用户密码，使用 `get_username()` 方法来获取用户的用户名等等。
5. 表单验证：继承 `AbstractUser` 的模型可以与 Django 的表单验证机制无缝集成。Django 提供了一些内置的表单和验证器，用于处理用户注册、登录、密码重置等场景。通过继承 `AbstractUser`，你可以直接使用这些功能，无需自己实现。

需要注意的是，如果你需要对用户模型进行更复杂的自定义，或者与其他模型之间建立关联，那么你可能需要进一步扩展和修改继承自 `AbstractUser` 的模型，以满足你的需求。
总结起来，继承 `AbstractUser` 来创建模型可以为你提供一些通用的用户字段和方法，以及与用户权限相关的功能。这些功能可以简化开发流程，并且与 Django 的其他模块集成良好，提高代码的可维护性和扩展性。

#### 与DRF结合使用的注意事项

在使用 Django REST framework (DRF) 创建后端接口时，继承 `AbstractUser` 类来创建模型不会直接导致冲突，但在结合使用时需要注意以下几个方面：

1. 序列化器（Serializer）：在使用 DRF 时，你需要创建序列化器来定义 API 接口的输入输出格式。当你使用继承 `AbstractUser` 的用户模型时，你需要创建一个定制的用户序列化器，以便控制返回给前端的用户信息的格式，并确保符合你的需求。
2. 定制用户模型：如果你需要对用户模型进行额外的扩展或定制，你可能需要创建定制的用户模型，并针对该模型创建相应的序列化器。这样可以确保 API 接口返回的数据结构与你的用户模型保持一致。
3. 权限控制：在使用 DRF 创建后端接口时，你需要考虑对 API 接口的权限控制。通过继承 `AbstractUser` 创建的用户模型已经集成了 Django 提供的权限管理功能，你可以利用这些功能来进行 API 接口的权限控制。
4. 视图和认证：使用 DRF 时，你需要编写视图类来处理 API 请求，并选择合适的认证方式来确保接口安全。结合使用 `AbstractUser` 类创建的模型时，你可以使用 DRF 提供的认证类和视图类来简化这些功能的实现。

总的来说，结合使用 DRF 和继承 `AbstractUser` 类创建模型并不会直接导致冲突，但你需要根据具体的业务需求来定制用户模型和序列化器，并合理控制权限和认证方式。此外，你还需要注意保持代码的清晰和可维护，以确保整个系统的稳定性和安全性。

#### AbstractUser 类的权限管理部分-PermissionsMixin

当你使用 `AbstractUser` 来创建模型时，它已经继承了 `PermissionsMixin`，这使得你可以方便地使用权限管理功能。`PermissionsMixin` 提供了一些字段和方法，可以用于定义和管理用户的权限。

下面是 `PermissionsMixin` 的一些常见用法：

1. `groups` 字段：`PermissionsMixin` 添加了一个名为 `groups` 的多对多字段，用于将用户分组。通过将用户分组，你可以方便地为整个组设置相同的权限，而不需要为每个用户单独设置权限。
2. `user_permissions` 字段：`PermissionsMixin` 添加了一个名为 `user_permissions` 的多对多字段，用于为用户设置特定的权限。通过为用户设置权限，你可以控制他们可以访问和执行哪些操作。
3. `has_perm()` 方法：`PermissionsMixin` 提供了一个 `has_perm()` 方法，用于检查用户是否具有特定的权限。你可以传递一个权限字符串给该方法，以检查用户是否拥有该权限。
4. `get_all_permissions()` 方法：`PermissionsMixin` 提供了一个 `get_all_permissions()` 方法，用于获取用户拥有的所有权限。该方法返回一个包含所有权限字符串的集合。

通过使用 `PermissionsMixin`，你可以在模型层级上定义用户的权限，并在视图中使用 `permission_classes` 属性进行权限验证。这两种方法之间的区别如下：

- 在模型层级上定义权限：使用 `PermissionsMixin` 可以为用户模型设置权限，例如为用户分组或设置特定权限。这些权限将与该用户的实例相关联，并可以在整个应用程序中使用。
- 在视图类中使用 `permission_classes`：在视图类中，你可以使用 `permission_classes` 属性来定义需要验证的权限类。这些权限类将根据请求的用户和当前操作进行权限验证。通过在视图类中使用 `permission_classes`，你可以细粒度地控制每个接口的访问权限。

综上所述，使用 `PermissionsMixin` 可以方便地管理用户的权限，包括在模型层级上定义权限和在视图类中使用 `permission_classes` 定义接口的访问权限。这两种方法都是有效的，具体取决于你的需求和设计。

#### 使用 PermissionsMixin来管理权限

当你有了一个基于 `AbstractUser` 创建的用户模型后，你可以使用 `PermissionsMixin` 来管理权限。下面是一个简单的示例，演示如何定义一个基于 `AbstractUser` 的用户模型，并使用 `PermissionsMixin` 来管理权限。

首先，假设你已经创建了一个用户模型 `CustomUser`，它继承自 `AbstractUser` 并且自动包含了 `PermissionsMixin` 的功能：

```python
from django.contrib.auth.models import AbstractUser, PermissionsMixin
from django.db import models

class CustomUser(AbstractUser, PermissionsMixin):
    # 添加任何其他自定义字段或方法
    pass
```

在这个示例中，`CustomUser` 继承自 `AbstractUser` 和 `PermissionsMixin`，这意味着它具有了权限管理的功能。接下来，你可以在视图中使用这个用户模型，并设置相应的权限。

假设你有一个基于 Django REST framework 的 API 视图，你可以使用 `permission_classes` 属性来控制接口的访问权限。下面是一个简单的视图示例，演示如何使用 `permission_classes` 属性进行权限管理：

```python
from rest_framework.views import APIView
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response

class MyAPIView(APIView):
    permission_classes = [IsAuthenticated]  # 只允许已认证的用户访问

    def get(self, request):
        # 在这里编写处理 GET 请求的代码
        return Response("GET 请求成功")

    def post(self, request):
        # 在这里编写处理 POST 请求的代码
        return Response("POST 请求成功")
```

在这个示例中，`MyAPIView` 是一个基于 DRF 的 API 视图类，它使用了 `IsAuthenticated` 权限类来限制只有已认证的用户可以访问该接口。通过将 `IsAuthenticated` 添加到 `permission_classes` 中，你可以确保只有登录用户才能访问该接口。
综上所述，通过继承 `AbstractUser` 和 `PermissionsMixin` 创建用户模型后，你可以在视图中使用 `permission_classes` 进行权限管理，以实现对接口的访问权限控制。

## 进度

8.1 - 9.9 django
9.10 - 9.25 整理笔记，尝试做项目但发现有问题，拼图不够完整
9.25 找到拼图 drf
9.26 - 10.17 drf
10.22 找到 drf+vue
10.24 找到 vue
10.24-31 vue
11.6-11.10 drf+vue

### 项目创建步骤

#### DRF项目

1. 创建项目文件夹
2. 进入该文件夹创建虚拟环境 `python -m venv .venv`
3. 激活虚拟环境 `.\.venv\Scripts\activate`
4. 安装依赖包 `pip install django djangorestframework`
5. 创建新项目 `django-admin startproject rbac`
6. 创建新应用 `cd .\rbac\` `python .\manage.py startapp api`
7. 注册app `settings.py` (如果忘记注册app，会报`Templatedoesnotexist`错误)

   ```python
   INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      'api.apps.ApiConfig',
      'rest_framework',
   ]

   LANGUAGE_CODE = 'zh-hans'
   TIME_ZONE = 'Asia/Shanghai'
   DATETIME_FORMAT = "Y年m月d日"

   # drf 配置
   REST_FRAMEWORK = {
      "UNAUTHENTICATED_USER": None,
      # 全局应用认证组件，三个认证类
      "DEFAULT_AUTHENTICATION_CLASSES": [
         "ext.auth.QueryParamsAuthentication",
         "ext.auth.HeaderAuthentication",
         "ext.auth.NoAuthentication",
      ],
   }
   ```

#### vue@3项目

1. `vue create 项目名` 创建项目，选版本3
2. `vue add vuex`，`vue add router` 添加插件
3. `npm install element-plus --save`

### OA表结构参考（申请模板可以参考钉钉的OA审批）

1. 用户表（User）：
   - 用户ID（ID）
   - 用户名（Username）
   - 密码（Password）
   - 姓名（Name）
   - 邮箱（Email）
   - 手机号（Phone）
2. 部门表（Department）：
   - 部门ID（ID）
   - 部门名称（Name）
   - 上级部门ID（ParentID）
3. 员工表（Employee）：
   - 员工ID（ID）
   - 员工姓名（Name）
   - 性别（Gender）
   - 出生日期（Birthdate）
   - 部门ID（DepartmentID）（外键关联至部门表）
4. 角色表（Role）：
   - 角色ID（ID）
   - 角色名称（Name）
5. 权限表（Permission）：
   - 权限ID（ID）
   - 权限名称（Name）
6. 员工角色关联表（EmployeeRole）：
   - 员工ID（EmployeeID）（外键关联至员工表）
   - 角色ID（RoleID）（外键关联至角色表）
7. 角色权限关联表（RolePermission）：
   - 角色ID（RoleID）（外键关联至角色表）
   - 权限ID（PermissionID）（外键关联至权限表）
8. 申请类型表（ApplicationType）：
   - 类型ID（ID）
   - 类型名称（Name）
9. 申请表（Application）：
   - 申请ID（ID）
   - 员工ID（EmployeeID）（外键关联至员工表）
   - 类型ID（ApplicationTypeID）（外键关联至申请类型表）
   - 开始日期（StartDate）
   - 结束日期（EndDate）
   - 申请事由（Reason）
   - 审批状态（Status）
10. 请假申请表（LeaveApplication）：
    - 申请ID（ID）
    - 员工ID（EmployeeID）（外键关联至员工表）
    - 开始日期（StartDate）
    - 结束日期（EndDate）
    - 请假类型（Type）
    - 请假事由（Reason）
    - 审批状态（Status）
11. 报销申请表（ExpenseApplication）：
    - 申请ID（ID）
    - 员工ID（EmployeeID）（外键关联至员工表）
    - 报销金额（Amount）
    - 报销事由（Reason）
    - 审批状态（Status）

### 待办

1. 整理
2. 研究一下 AWS的CodeWhisperer怎么用
3. 做个OA系统吧
4. 把红黑榜应用做个demo
5. 将drf中request对象的封装、用户认证、权限校验、限流组件、序列化器、序列化器-数据校验 进行源码解析+流程图，写博客
6. 案例：博客平台
   - 登录&注册 => 提交数据（数据校验）
   - 博客列表 => QuerySet => 序列化 => many=True
   - 博客详细 => ORM对象 => 序列化 => many=False
   - 新建博客
   - 认证 + 版本

```sql
insert into usermanagement_userinfo(name,password,age,account,create_time,gender,department_id) values("张三", "pass123",23,5000,CURRENT_TIMESTAMP(),1,5);
```

```sql
insert into login_userinfo(role,username,password) values("leader", "张三", "pass123");
insert into login_userinfo(role,username,password) values("user", "李四", "pass123");
 INSERT INTO login_order (sponsor_id, tpl_type_id, approver_id, status, apply_time) VALUES (2, 1, 1, 0, NOW());
```

《你的降落伞是什么颜色》
《副业的成长之道》
《职业生活的心理学》
