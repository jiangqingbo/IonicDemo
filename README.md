# IonicDemo
学习ionic for mobile app dev

### 学习步骤：

1、安装 [https://nodejs.org/en/]Node.js, 推荐安装稳定版本

2、安装之后运行cmd,执行node -v 和 npm -v命令， 出现版本号，说明安装成功

3、配置npm的全局模块global路径和存放模块cache路径，我在Node.js的安装路径下建两个文件夹node_global 和 node_cache

4、执行如下命令：

    > npm config set prefix "D:\Program Files\nodejs\node_global"  
    > npm config set cache "D:\Program Files\nodejs\node_cache"
    
    //执行之后，使用命令npm config get prefix，查看设置
    > npm config set prefix
    
5、安装模块bower, 执行命令

    // -g指安装到D:\Program Files\nodejs\node_global（global地址）
    > npm install bower -g
    
6、执行

    > bower -v
    //出现错误： 'bower' 不是内部或外部命令，也不是可运行的程序或批处理文件。
    
7、配置node_global 指令访问的环境变量

    在环境变量中新建 NODE_HOME = D:\Program Files\nodejs
    然后在path后面添加：%NODE_HOME%\node_global
    然后重新打开控制台cmd， 执行命令：
    
    > bower -v
    //出现版本好，说明global环境变量配置好了
    
8、安装ionic cordova

    > npm install -g cordova ionic
    
9、拉取demo项目, 进入D盘中ionicworkspace目录下

    > ionic start myApp tabs
    // 等待项目拉取完成
    > cd myApp
    //进入myApp项目，并启动服务
    > ionic serve
    //出现以下情况，服务已经启动好了，接着在手机或pc端访问地址即可看到效果
    dev server running: http://localhost:8100/
    
10、按 Ctrl + c 关闭服务
