# cordova-yingyong
一.制作cordova项目
# 1.检查环境（确保开发环境）
## a. node.js
## b. git
## c. cordova 命令行（使用npm install -g cordova 安装）
# 2.创建新的cordova项目
## a.·cordova create· (文件夹名、项目命名空间、项目名)执行命令
#3.为cordova 项目加入目标平台加入平台前检查是否满足开发目标平台的基本需求
  如android需要android SDK  ios需要xCode；
  进入cordova项目的文件夹对应；
  执行·cordova platform add· （目标平台名称）；
# 4.将目标平台的项目导入开发工具如android导入eclipse ios xcode
# 5. 建立cordova插件的实现文件以android为例
## a.在导入的文件中新建一个java类
## b.让该类继承CordovaPlugin
## c，重写其中的execute的方法
## d. 调用execute的传入的回调方法保证将原生代码的处理结果返回浏览器
# 6.如何调用cordova 插件
   在调用cordova 插件之前请确认是在手机上执行的代码而不是在浏览器上执行的；
   在cordova环境中调用cordova.exec(调用成功之后的回调、调用失败后的回调、调用的插件名、调用的插件当中的方法名、数组（包含插件当中所传所有参数）)在调用成功之后的回调那结果。
# 7.将写好的cordova 插件实现注册到cordova项目当中
  修改 cordova config.xml文件加入 插件名称、插件的实现文件要写类的全名。


