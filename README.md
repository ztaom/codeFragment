# 拿来即用的代码片段

## 一、JavaScript

### 1、获取链接category后的值
```
var getCategory = function(){
    var url = location.href;
    var url_param = {};
    if (url.indexOf("?") != -1) {
        var str = url.substr(url.indexOf("?") + 1);
        var strs = str.split("&");
        for (var i = 0; i < strs.length; i++) {
            url_param[strs[i].split("=")[0]] = decodeURI(strs[i].split("=")[1]);
        }
    }
    
    return url_param["category"];
};
var category = getCategory();
```  
#### 2、动态计算屏幕分辨率
```
(function (doc, win) {
  var docEl = doc.documentElement,
    resizeEvt = 'orientationchange' in window ? 'orientationchange' : 'resize',
    recalc = function () {
      var clientWidth = docEl.clientWidth;
      if (!clientWidth) return;
      docEl.style.fontSize = 20 * (clientWidth / 320) + 'px';
    };
  if (!doc.addEventListener) return;
  win.addEventListener(resizeEvt, recalc, false);
  doc.addEventListener('DOMContentLoaded', recalc, false);
})(document, window);
```  


## 二、CSS
## 三、新技术
## 四、移动端问题
## 五、移动端优化
![alt](https://raw.githubusercontent.com/ztaom/codeFragment/master/source/youhua.png)