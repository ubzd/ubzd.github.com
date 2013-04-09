---
layout: post
title:  ubuntu12.04开机亮度设置
category: ubuntu
tags: [ubuntu]
---
{% include JB/setup %}

1. 打开软件中心，安装laptop-mode；
2. `vim /etc/laptop-mode/laptop-mode.conf`
3. `ENABLE_LAPTOP_MODE_ON_BATTERY=1` `ENABLE_LAPTOP_MODE_ON_AC=1`
还要: `ENABLE_AUTO_MODULES=0`,  否则，摄像头的灯会一直亮着的
4. 打开`vim /etc/laptop-mode/conf.d/lcd-brightness.conf` 修改如下行：   
`CONTROL_BRIGHTNESS=1`   
`BATT_BRIGHTNESS_COMMAND="echo 3"`  
`LM_AC_BRIGHTNES_COMMAND="echo 3"`  
`NOLM_AC_BRIGHTNES_COMMAND="echo 3"`  
`BRIGHTNESS_OUTPUT="/sys/class/backlight/acpi_video0/brightness"`  
5. 执行`sudo update-grub`
