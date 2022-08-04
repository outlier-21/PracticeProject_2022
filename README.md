# PracticeProject_2022
本次实习内容由两个项目来完成：

js的多线程通信（第一周）：天气百事通

开发环境为：微信开发者工具
具体思路为：通过和风天气提供的免费API，来实现具体某城市实时天气的查询。
                  然而使用和风天气的API之前，必须得到某个城市的LocationID，于是，可以利用WebWork，
                  创建副线程来获取LocationID，获取后，再发给主线程，主线程利用此ID进行天气的查询

注意事项：1、微信小程序只允许创建一个Web Worker
                2、微信小程序对Worker的路径有规定，
                     Worker的有效代码在路径‘/worker/request’文件夹下
                     主线程利用Worker的代码在‘/pages/index/index.js’文件中的getWeather函数中

vdom diff jsx编译（第二、三周）:备忘录

具体操作简单，在文件夹中点击index.html在浏览器中打开即可

进入网页之后 
在输入框中输入有效内容即可添加，点击每一条的项目之后即可删除

