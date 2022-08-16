# PracticeProject_2022

使用三项技术完成的小项目（webworker / vdom 渲染/jsx编译）

项目功能：本项目为查询实时天气开发，使用和风天气的免费API进行天气查询。三项技术具体体现在：

WebWorker：将使用API来查询天气信息的任务交给WebWorker处理，子线程获取信息后向主线程发送，主线程接受数据后
           向子线程发送字符串‘RECEIVE’，子线程经过判断自行调用close()销毁。WebWorker的有关函数为index.js文件中的getWeather(id)函数中。
           
vdom 渲染和jsx编译：共同负责页面的渲染任务。
                  vdom主要运用diff算法，具体体现在vdom.js文件中
                  jsx的编译使用babel，具体体现在index.js文件中，其中包含简单的条件渲染和循环渲染
                  
 
项目结构：未列出文件无需关注

根目录
   |-----------------dist           jsx的编译结果存放处
        |------------vdom.js        和外层的vdom.js内容相同
        |------------index.js       jsx被编译
   |-----------------img            图片静态资源
   |-----------------node_modules   相关依赖
   |-----------------.babelrc.js    babel的配置
   |-----------------index.js       具体的Querier实例
   |-----------------vdom.js        vdom渲染算法的实现
   
