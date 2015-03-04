meta 标签
===
###1. viewport
```
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0,
user-scalable=no, target-densitydpi=medium-dpi" />
```
移动端浏览器在一个比屏幕更宽的虚拟"视窗"中渲染页面，从而无需将所有页面都压缩进小屏幕里（那样会把很多没有针对移动端优化的页面打乱），用户可以通过平移和缩放来浏览页面的不同区域。  

viewport允许开发者定义这个虚拟"视窗"的大小和缩放程度。
* width 单位是px；各个浏览器的默认值不同，Safari是980；区间是200~10000；device-width表示设备宽
* height 单位是px；默认会根据width和设备的宽高比来计算；区间是223~10000；device-height表示设备高
* initial-scale 默认设置成将页面缩小至可视"视窗"中
* minimum-scale 用户可以缩放的最小值；默认是0.25；区间是0~10.0
* maximum-scale 用户可以缩放的最大值；默认是5.0；区间是0~10.0
* user-scalable 默认是"yes"，设置成"no"可以阻止用户缩放，同时会阻止页面的滚动当用户在输入时
* target-densitydpi 指定屏幕密度，默认是medium-dpi,还有low-dpi和high-dpi；Safari不支持这个属性

**minimum-scale不指定的话可能会造成initial-scale不起作用**  
**如果页面是在一个小于屏幕宽度的容器中打开的，可以通过动态写viewport来达到自适应的效果**
```
function resetViewport(){
		document.getElementById("viewport").content = "width=" + window.innerWidth + ", 
initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no, target-densitydpi=medium-dpi";
}
```

###2. format-detection
```
<meta name="format-detection" content="telephone=no" />
```
是否将可能的数字串转换为拨号链接

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
