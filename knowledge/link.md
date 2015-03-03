link 标签
===
###1. apple-touch-icon
```
<link rel="apple-touch-icon" href="touch-icon-iphone.png" />
<link rel="apple-touch-icon" sizes="72x72" href="touch-icon-ipad.png" />
<link rel="apple-touch-icon" sizes="114x114" href="touch-icon-iphone-retina.png" />
<link rel="apple-touch-icon" sizes="144x144" href="touch-icon-ipad-retina.png" />
```
**如果不想让IOS在icon上加上高亮半透的效果，就在apple-touch-icon后面加上-precomposed**  

默认sizes是"57x57"，IOS会优先去找size相近的，size相同的情况优先采用有-precomposed后缀的icon  
icon都没有的话IOS还会去网站的根目录下依次寻找  
apple-touch-icon-114x114-precomposed.png  
apple-touch-icon-114x114.png  
apple-touch-icon-precomposed.png  
apple-touch-icon.png  
（这里的尺寸是根据设备来的）

###2. apple-touch-startup-image
```
<link rel="apple-touch-startup-image" href="startup.png" />
```
设置用户将页面以app的形式添加到桌面后打开时的启动画面   

**iphone5以前包括ipod，图片尺寸必须是320x460，少了20应该是为最上面的status-bar留的，多一像素的话启动画面就没了...**    
**而且启动画面不会更新，除非用户删除然后重新添加网页到桌面**
