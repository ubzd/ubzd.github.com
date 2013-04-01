---
layout: post
title : ubuntu dock add icon
category: ubuntu
tags: [ubuntu]
---
{% include JB/setup %}

buntu 12.04 unity下eclipse图标不显示解决方法
 
在以前版本的ubuntu中，创建快捷方式是在/usr/share/applications
目录下创建*.desktop文件，在ubuntu12.04下，也同样可行
 
1、在/usr/share/applications目录下新建eclipse.desktop，内容如下
 
[java] 
[Desktop Entry]  
Type=Application  
Name=Eclipse    www.2cto.com  
Comment=Eclipse  
Icon=/home/lai/Software/eclipse/icon.xpm  
Exec=/home/lai/Software/eclipse/eclipse  
Terminal=false  
Categories=Development;IDE;Java;  
