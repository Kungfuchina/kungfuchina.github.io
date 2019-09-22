---
layout: post
title: 用Python制作一个自动回复机器人
subtitle: 
date: 2019-09-22
author: Supertramp
header-img: img/post-bg-web-change.jpg
catalog: true
tags:
    - Python
    - 对话机器人
---

# 用Python制作一个自动回复机器人
## 本教程使用Python中pyautogui库的图片识别定位功能和模拟鼠标键盘操作功能来达到自动回复的目的，所以理论上支持所有聊天软件，这里使用Skype网页版

## 软件需要实现的功能
实时检测聊天窗口中的新消息和用户ID，将消息内容传递给第三方对话机器人，使用第三方机器人返回的对话内容回复消息

## 检测新消息
仔细观察Skype在线版消息框出现的位置会发现最后一个消息框与输入框的距离总是固定的
![image.png](https://i.loli.net/2019/09/22/OAjSfe2PkX4mhis.png)
截取一张包含消息框边缘和输入框的图片
使用pyautogui库中的locateCenterOnScreen来返回图片中心点所在位置
