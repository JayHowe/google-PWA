## manifest.json 配置说明
pwa首先可以将web页面的入口添加至手机桌面成一个应用入口，而通过manifest文件的配置，我们可以设置应用的图标、应用入口路径、应用名称等。

1. 首先页面引入 **manifest.json** 文件：

2. 引入的方式：

```html
<link rel="manifest" href="manifest.json">
```

3. 通过这个文件配置，你可以设置：
  1. 应用启动的URL 
  ```json
  "start_url": "",
  ````

  2. 应用名称:
  ```json
     "name": "Fireworks!"
     "short_name": "Fireworks!"
  ```
 
  其中的`name`与`short_name`**最好是保持一致**，其中`name`就是桌面图片显示给用户看的名字，而`short_name`构件的目的是在桌面上没有足够的空间来显示全名的时候，则用`short_name`，如果两个同时存在chrome会默认使用`short_name`，其他浏览器可能有不同表现

  3. 应用的图标：
  ```json
  "icons": [
    {
     "src":"images/fireworks-icon192x192.png",
      "sizes": "192x192",
     "type": "image/png"
    }
  ]
  ````

  4. 颜色：
  ```
  "background_color": "#000"
  "theme_color": "#536878"
  ```
  这些值提供给浏览器的HTML和CSS文件被解析并呈现前，并不能取代html里面原有的样式

  5. 显示模式：
  ```
  "display": "standalone"
  ``` 
  设置chrome浏览器是否显示导航栏、菜单栏、选项卡等用户构件，对于要添加到手机桌面的web应用，最好就是设置为`standalone`或者`fullscreen`



参考地址:[https://codelabs.developers.google.com/codelabs/add-to-home-screen/#2](https://codelabs.developers.google.com/codelabs/add-to-home-screen/#2)
