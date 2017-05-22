# Base64.js
## 简介
虽然JavaScript中可以使用原生的btoa和atob函数进行Base64的编解码。但是不支持中文字符，并且不支持url-safe的Base64编解码。当编码后的结果要是通过get请求传输时（比如跨域提交时），结果中包含有'/'字符将导致出错。

本项目借鉴了loonhxl的 [jbase64](http://git.oschina.net/loonhxl/jbase64/tree/master) 项目，并做了一些修改。

- 支持一般Base64的编码和解码
- 支持符合RFC_4648标准中"URL and Filename Safe Alphabet"的URL安全Base64编解码
- 支持中文字符的编解码(Unicode编码)

## 使用
### 直接引入
```
<script type="text/javascript" src="base64.js"></script>
```
### 通过RequireJs
```
require(['base64'], function (BASE64) {
});
```
### 通过CommonJs
```
var BASE64 = require('base64');
```

## 示例
```
BASE64.encode(inputStr);//普通Base64编码
BASE64.decode(inputStr);//普通Base64解码
BASE64.urlsafe_encode(inputStr);//url-safe Base64编码
BASE64.urlsafe_decode(inputStr);//url-safe Base64解码
```
