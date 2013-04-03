---
layout: post
title: U盘启动系统
category: other
tags: [U盘]
---
{% include JB/stup %}

1. 下载UltraISO
2. 加载ISO文件，启动->写入硬盘映像
3. 写入格式:USB-HDD+, 确定之后点击格式化，这一步会清空U盘数据
4. 开始写入
5. 在BIOS中，选择startup
6. 把在硬盘选项中把USB选到硬盘之前，再把BOOT顺序选到第一个，保存，重启。
