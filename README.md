## 总结一些自己完成的提高效率的工具

#### 1. yfci.sh
>  用于在linux系统上快速安装java和node环境的自动化脚本

* 源码地址: [https://github.com/yfsoftcom/mytools](https://github.com/yfsoftcom/mytools)
* 基于centos 6.x的系统环境
* 自动安装如下软件：git , lsof , node 4.5 , pm2 , cnpm , java1.8 , maven 3.2.x , tomcat 8.x
* 自动集成ci-web , 通过浏览器访问：http://[yourdomain]:3000 , 可执行系统shell命令，如：
```
$ free -m
```
```
$ yfci build
```
![执行 free -m 命令](http://upload-images.jianshu.io/upload_images/1449977-8a6e701bba8ec1da.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 2. task-trigger
> 可视化配置定时任务，在指定的时间执行任务请求，对已有系统无任何倾入，可快速集成使用。

* 源码地址: [https://github.com/yfsoftcom/task_trigger](https://github.com/yfsoftcom/task_trigger)
* 基于node环境，使用schedule模块
* 通过配置cron表达式和request执行web请求
* 需要配合 api-server 进行使用

![任务列表](http://upload-images.jianshu.io/upload_images/1449977-58809e5cf49946c9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 3. yf-fast-dbm
> 快速极简的orm框架

* 源码地址: [https://github.com/yfsoftcom/yf-fast-dbm](https://github.com/yfsoftcom/yf-fast-dbm)
* 目前支持mysql，使用 jugglingDB
* 通过delflag实现逻辑删除
* 默认带有四个字段：id,createAt,updateAt,delflag
* 支持批量插入
* TODO:事务，存储过程，mongodb语法

#### 4. yf-api-server
> api服务端集成框架，自动集成crud的数据操作，扩展自定义业务逻辑

* 源码地址: [https://github.com/yfsoftcom/yf-api-server](https://github.com/yfsoftcom/yf-api-server)
* 基于restify框架
* 支持key+secret双端验证
* 支持接口权限验证
* 支持hook钩子操作
* 支持接口多版本同时在线
