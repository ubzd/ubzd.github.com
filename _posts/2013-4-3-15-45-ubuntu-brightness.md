---
layout: post
title:  ubuntu12.04开机亮度设置
category: ubuntu
tags: [ubuntu]
---
{% include JB/setup %}

1. 打开软件中心，安装laptop-mode；
2. `vim /etc/laptop-mode/laptop-mode.conf`
3. 修改如下行：
`CONTROL_BRIGHTNESS=1`   
`BATT_BRIGHTNESS_COMMAND="echo 3"`
`LM_AC_BRIGHTNES_COMMAND="echo 3"`
`NOLM_AC_BRIGHTNES_COMMAND="echo 3"`
`BRIGHTNESS_OUTPUT="/sys/class/backlight/acpi_video0/brightness"`
4. 执行`sudo update-grub`
