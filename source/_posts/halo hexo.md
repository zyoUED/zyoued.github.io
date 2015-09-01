title: HEXO诞生记
---
1、首先你得有个github账号（例如cdll），然后创建一个repository，命名为‘<git_user_name>.github.io’（例如cdll.github.io），repo创建成功后，进入其设置页（setting），页面滚到下方会有一个github-page生成工具（generator），continue后会让你设置初始化内容，下一步选择主题，然后点击publish page就好了~

那么到了这一步，你就有了一个地址为 http://<git_user_name>.github.io 的博客页，是不是很赞~基于这个repo自己维护自己的gh-page博客也是可以的~

2、我们今天要说的是靠hexo来管理这个gh-page博客。hexo基于nodejs，关于nodejs的安装这里我们就不赘述了，请自行谷歌之~

3、安装好了nodejs之后，我们就可以安装hexo啦：

npm install -g hexo-cli（注意，是hexo-cli，官方文档写了啊）。

受到长城防火墙影响的用户可以使用淘宝镜像：

npm install -g hexo-cli --registry=https://registry.npm.taobao.org。

4、安装结束后通过直接执行hexo命令就可以检查我们的hexo是否安装完毕了。如有遇到hexo没反应的选手还请重试步骤3~

5、接下来使用mkdir <dir_name>命令在个人文件夹下创建一个目录，例如：

mkdir hexo。

6、cd进入新建的（hexo）目录，使用hexo init命令初始化我们的工作目录，这一步其实就是导入了hexo的npm依赖关系package.json~

7、通过init得到info通知后可以看到它提示我们‘执行npm install’命令来完成初始化工作，这里其实就是npm从导入的hexo依赖关系去自动安装好了依赖模块、生成了必要的目录结构~

8、静候片刻后我们就得到了必要的目录及模块，以及各种配置信息~

9、好了，到此为止我们就可以使用hexo new命令新建一个markdown文件开始写博文了，写完的博文可以通过hexo g命令转换成相应的html文件，自动扔到对应的分类子文件夹、自动套上了默认的（或是已经配置好的）主题样式~

PS：关于hexo new时遇到的错误，请首先查看本文第三部，如若还不行还请自行github之或sof之~

10、接下来就是在_config.yml配置文件中配置我们的repo地址进来了，这样可以方便我们在hexo d（deploy）时同步到github上~

well done，any question可以在下方留言给我~欢迎相互来群交流【WEB UX Club】。