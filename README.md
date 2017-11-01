# CMD命令总结
## 回显控制
- echo off #下一行开始关闭回显
- echo on #下一行开始打开回显
- @echo off #本行开始关闭回显
- echo #显示回显状态
- echo. #输出一个回换行符
- echo hello world #输出hello world
>**注意：默认回显是打开的**

## @命令
@命令：echo off相象，但它是加在其它命令行的最前面，表示运行时不显示命令行本身。
## PAUSE命令
pause命令用于暂停CMD命令提示符
## REM命令
注释效果
## CD命令
更改当前目录</br>
- cd mp3 #进入当前目录中的mp3 目录
- cd ..  #进入当前目录中的上级目录
- cd\    #进入根目录
- cd d:\mp3 #可以同时更改盘符和目录
一般地，进入某盘符文件夹，应如此操作
```
d:
cd \mongodb\bin
mongo
```
**特别注意：**经测试，以下操作无效，因为执行mongo操作时，未进入d:\mongodb\bin
```
cd d:\mongodb\bin
mongo
```
## Examples
>
```
@echo off
rem 进入D盘
D:
cd \mongodb\bin
echo on
mongo
pause
```
```
@rem 进入D盘
@D:
@cd \mongodb\bin
mongo
pause
```

以上两段效果相同，如下截图</br>
![](https://ip.freep.cn/593463/%E6%96%B0%E5%BB%BA%E6%96%87%E4%BB%B6%E5%A4%B9/%E7%A8%8B%E5%BA%8F%E5%9B%BE%E7%89%87/cmd1.PNG)
## CLS命令
清屏
## TITLE命令
- title 新标题 #可以看到cmd窗口的标题栏变了
## VER命令
显示系统版本
## DATE命令
- date #显示当前日期，并提示输入新日期，按"回车"略过输入
- date/t #只显示当前日期，不提示输入新日期
- time   #显示当前时间，并提示输入新时间，按"回车"略过输入
- time/t #只显示当前时间，不提示输入新时间
## 卷标命令
- vol #显示卷标
- label #显示卷标，同时提示输入新卷标
- label c:system #设置C盘的卷标为 system
## MD命令
- md abc #在当前目录里建立子目录 abc
- md d:\a\b\c #如果 d:\a 不存在，将会自动创建
## RD命令
- rd abc #删除当前目录里的 abc 子目录，要求为空目录
- rd /s/q d:\temp #删除 d:\temp 文件夹及其子文件夹和文件，不需要按 Y 确认
