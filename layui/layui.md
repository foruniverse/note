## LAYUI

这是一个深度封装的前端框架,从目前的使用来看,基本即拿即用,只需在 后端封装好对应格式的数据,然后引用在layui内部深度封装好的模块,就可以快速的构建前端,仅以此文作为layui的日常使用记录,供WIKI查询



#### Layui中使用 jQuery

layui 是基于jQuery的框架,内部内置jQuery稳定版本,如果需要外部引用,必须在加载Layui的js文件前引用

同时,要想在内部使用jQuery,也必须 通过layui的接口使用

如下所示

~~~js
layui.use(['jQuery'],funciton(){
          var $ = layui.$;
          var layer = layui.layer;
          });
~~~

