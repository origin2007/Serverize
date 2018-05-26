# Serverize

让程序像服务器程序那样运行。

## 功能说明

该程序包括一系列脚本，用于将普通程序转成服务程序，解决后台运行，运行时监控，日志占用空间清理等一系列现实的问题。该程序设计的初衷是为了解决Java写的服务器程序部署的问题，因为Java写后台程序比较困难，不使用框架或者JNI的话难度较大；另外很多时候Java服务器程序是运行在Linux系统上的，因此设计了该软件。

## 使用方法

serverize (app) \[params\]

将app放在后台运行，并将app的输出流定向到/tmp/app.log中。

deserverize (app) \[params\]

终止app的运行。注意：如果运行时有params，这里也要一模一样的params。

monitor (app) \[params\]

监控app的运行，发现app没有运行，则强行启动app。

clearlog (app) \[params\]

生成定期清理log的crontab。

monitorize (app) \[params\]

生成定期监控app运行的crontab。

## 开发阶段

初始阶段，没有经过详细的测试。

## 限制条件

目前需要将这些脚本程序拷贝到应用所在的目录，否则运行时可能会有问题。


