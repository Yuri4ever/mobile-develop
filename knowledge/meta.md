meta 标签
===
###1. viewport
```
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0,
user-scalable=no, target-densitydpi=medium-dpi" />
```

###2. format-detection
```
<meta name="format-detection" content="telephone=no" />
```
是否将数字转换为拨号链接

###3. apple-mobile-web-app-capable
```
<meta name="apple-mobile-web-app-capable" content="yes" />
```
用户将页面作为web application添加到桌面后的打开方式  
"yes"表示以全屏的方式打开，模拟原生App  
"no"表示用safari正常打开  
js中可以通过window.navigator.standalone查看

###4. apple-mobile-web-app-status-bar-style
```
<meta name="apple-mobile-web-app-status-bar-style" content="black" />
```
用户将页面作为web application添加到桌面后打开后status-bar的颜色  
默认为default(目测和设为black表现一样)  
还可以设置成black-translucent，黑色半透明

**如果先设置成default或black，后续再改成black-translucent不起作用，且status-bar会挡住页面的一部分**  
**如果先设置成black-translucent，后续可以修改成其他值，且status-bar不会挡住页面的一部分**

###5. X-UA-Compatible
```
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
```
指定用最高版本的IE来渲染，不加的话一些winphone的手机会用低版本的IE来渲染  

**此标签一定要放在css前面**
