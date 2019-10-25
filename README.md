## ✌️📔 一个采用前后端分离开发模式实现的多用户博客管理平台
 
> 项目在线演示地址 : http://vblog.itboyhub.com/  🔐用户名 : sang，密码 : 123 ( 更多信息请参考数据库,密码都是123啦~ )


### 项目简介
✨*这或许是最简单的 springboot + vue 实现的前后端分离项目啦 ! 非常适合作为初次学习前后端开发模式的同学第一个入门项目哟~*


### 开发环境

| 工具    | 版本或描述                     |    
| ------- | ----------------------------- |    
| `OS`    | Windows 10                    | 
| `JDK`   | 1.8+                          |    
| `IDE`   | IntelliJ IDEA 2019.1          |    
| `Maven` | 3.6.0                         |    
| `MySQL` | 8.0.0+                        |



### 项目模块划分

| 模块          | 释义                             |    
| ------------- | ------------------------------- |    
| `blogserver`  | 后台管理模块                     |    
| `vueblog`     | 前台管理模块                     |
| `docs`        | 文档( 存储数据库文件及截图 )      |



### 数据库模型
![sql model](https://raw.githubusercontent.com/YUbuntu0109/VBlog/newfun-restore-article-del-m/docs/vblog-database-er.png)



### 图片预览  
*:camera_flash: 用户登录页*
![登录](https://raw.githubusercontent.com/lenve/VBlog/master/doc/login.png)  

*:camera_flash: 文章列表页*
![文章列表](https://raw.githubusercontent.com/lenve/VBlog/master/doc/article.png)  

*:camera_flash: 发表文章页*
![发表文章](https://raw.githubusercontent.com/lenve/VBlog/master/doc/post.png)  

*:camera_flash: 用户管理页*
![用户管理](https://raw.githubusercontent.com/lenve/VBlog/master/doc/usermana.png)  

*:camera_flash: 栏目管理页*
![栏目管理](https://raw.githubusercontent.com/lenve/VBlog/master/doc/category.png)  

*:camera_flash: 数据统计页*
![数据统计](https://raw.githubusercontent.com/lenve/VBlog/master/doc/datastatistics.png)  



### 项目技术栈

| 后端技术栈                  | 前端技术栈              |    
| -------------------------  | ---------------------- |    
| `SpringBoot`               | `Vue`                  | 
| `SpringSecurity`           | `axios`                |    
| `MyBatis`                  | `ElementUI`            |    
| `Druid`                    | `vue-echarts`          |    
| `MySQL`                    | `mavon-editor`         |
| 部分接口遵循`Restful`风格   | `vue-router`           |
 
> 其它一些琐碎的技术这里就不一一列举了咯~



### 使用说明  
1. *将本项目中的`blogserver`( 后端管理模块 )导入到`IDE`*
2. *导入数据库`docs/db/vueblog.sql`*
3. *修改`resources/application.properties`配置文件* 
4. *运行项目( 三种方式 )*
   1. 项目根目录下执行`mvn -X clean package -Dmaven.test.skip=true`编译打包，然后执行`java -jar blogserver/target/blogserver.jar`
   2. 项目根目录下执行`mvn springboot:run`
   3. 直接运行`BlogserverApplication.java`
5. *浏览器访问`http://localhost:8081/index.html`*

> 注意 : 如果要做二次开发,请继续看第五、六步哟 !

6. *进入`vueblog`( 前端管理模块 )目录中，在命令行依次执行如下命令 :*  
```
# 安装依赖
npm install

# 在 localhost:8080 启动项目
npm run dev
```  

> 由于我在`vueblog`( 前端管理模块 )项目中已经配置了端口转发，既将数据转发到`SpringBoot`上，因此项目启动之后，在浏览器中输入`http://localhost:8080`就可以访问我们的前端项目啦~ 所有的请求将通过端口转发将数据传输到`SpringBoot`中( 注意 : 这个过程要保持`SpringBoot`项目,既`blogserver`后台管理模块是处于运行状态的 ! )

7. *最后可以使用`WebStorm`等前端开发工具打开`vueblog`项目( 前端管理模块 )继续开发，待开发完成后，当项目要上线时，依然进入到`vueblog`目录，然后执行如下命令 :* 
```
npm run build
```

*该命令执行成功之后，`vueblog`目录下将生成一个名为`dist`的文件夹，然后将该文件夹中的`static`文件夹及`index.html`文件拷贝到`SpringBoot`项目中的`resources/static/`目录下，然后就可以像第 `4` 步那样通过启动后端管理模块来访问该项目咯~*

> 步骤 `6` 中需要大家对`NodeJS`、`NPM`等有一定的使用经验，不熟悉的小伙伴可以先自行学习下 : [Vue官方教程](https://cn.vuejs.org/v2/guide/)  



### 项目依赖
1. [`vue-echarts`](https://github.com/Justineo/vue-echarts)
2. [`mavonEditor`](https://github.com/hinesboy/mavonEditor)
