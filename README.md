# react-native-webview
react-native-webview 基于 5.12.0 版本调整，在 `com.reactnativecommunity.webview.RNCWebViewManager.RNCWebView` 中添加了 `shouldInterceptRequest`，用于拦截 `http://android_image` ，支持 webview 加载服务端 html 中 &lt;img> 使用本地路径，目前支持 jpeg、jpg、png、svg、gif 扩展名的图片加载

使用方法，假定图片路径在设备上的绝对路径为  `/data/user/0/com.example.app/cache/test.jpg` , 在 html 代码中使用如下方式引用

```
<html>
<body>
  <img src="http://android_image/data/user/0/com.example.app/cache/test.jpg" />
</body>
</html>
```
使用 webview 加载该页面时便可以正常访问图片
