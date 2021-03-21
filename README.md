### 轮播图插件
本项目基于原生JS手动封装了一个简单的轮播图插件

### 使用

1. 引入css，js文件
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="./banner.min.css">
</head>
<body>
    <script src="js/utils.js"></script>
    <script src="js/animate.js"></script>
    <script src="js/banner-plugin.js"></script>
</body>
</html>
``` 

2. 引入html结构
```html
    <section class="container" id="container2">
        <div class="wrapper">
        </div>
        <ul class="focus">
        </ul>
        <a href="javascript:;" class="arrow arrowLeft"></a>
        <a href="javascript:;" class="arrow arrowRight"></a>
    </section>
```
3. 此时你可以修改自己样式
```html
    <style>
        .container{
            width:300px;
            height:300px;
            //...
        }
    <style>
```
3. 创建banner实例
```
    <script>
        new Banner({
            ele: '#container',
            url: 'json/banner2.json',
            interval: 500,
            speed: 300,
            isFocus: false
        });
    </script>
```

### 配置项

```js
 new Banner({
     ele:'container',   //操作哪一个容器
     url:'',            //获取数据的API地址（插件内部帮我们获取数据）
     isArrow:true,      //是否支持左右切换
     isFoucs:true,      //是否支持焦点切换
     isAuto:true,       //是否支持自动切换
     defaultIndex:0,    //默认展示第几张图片
     interval:3000,     //多久切换一次
     speed:200,         //切换的速度
     moveEnd:()=>{}     //切换完成处理的事情
 });
```



