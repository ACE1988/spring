## 原理图
 ![img](img/191439034705767.png)

## mvc 工作原理
 
 * 发起请求到前端控制器(DispatcherServlet);

 * 前端控制器请求HandlerMapping查找Handler，可以根据xml配置、注解进行查找；

 * 处理器映射器HandlerMapping向前端控制器返回Handler；

 * 前端控制器调用处理器适配器去执行Handler；

 * 处理器适配器去执行Handler；

*  Handler执行完成给适配器返回ModelAndView；

* 处理器适配器向前端控制器返回ModelAndView(是springmvc框架的一个底层对象，包括Model和View)；

* 前端控制器请求视图解析器去进行视图解析，根据逻辑视图名称解析真正的视图(jsp...)；

* 视图解析器向前端控制器返回View;

* 前端控制器进行视图渲染，视图渲染就是将模型数据(在ModelAndView对象中)填充到request域中。

* 前端控制器向用户响应结果。
