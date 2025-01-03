---
title: "Rocky Linux 9.4VMware安装教程"
description: "仅限amdx86_64CPU架构"
pubDate: "Nov 3 2024"
image: "https://s1.imagehub.cc/images/2024/11/27/77cdf7b34f0ad71469ce6d87454af479.jpeg"
categories:
  - tech
tags:
  - VMware
  - Rocky Linux
---
# 1. 下载镜像
首先下载Rocky Linux 9.4的镜像，可以去[Rocky Linux官网](https://rockylinux.org/zh-CN)或者阿里、网易等镜像站下载
注意架构不要选择错了
![](https://s1.imagehub.cc/images/2024/11/03/31c21ae70f4b51629c2326f01a31ed15.png)
# 2. 创建新的虚拟机
打开VMware Workstation Pro 17，创建新的虚拟机。
类型选择`典型`
![](https://s1.imagehub.cc/images/2024/11/03/1e30ed84e83cffefea72cbb0ce1b795a.png)
选择`稍后安装操作系统`
![](https://s1.imagehub.cc/images/2024/11/03/1efc64baea0cfed74586ba8fee81f199.png)
客户机操作系统选择`Linux`，版本选择`其他 Linux 5.x 内核 64位`
![](https://s1.imagehub.cc/images/2024/11/03/e0d2145394fa858a99e9b28611d06403.png)
填写虚拟机名称及选择虚拟机安装位置
![](https://s1.imagehub.cc/images/2024/11/03/85eacea589f2d8ec46037a2e4f349893.png)
最大磁盘大小`50G+`
![](https://s1.imagehub.cc/images/2024/11/03/6ca2da271d26ac1fc0fc42439bde17c3.png)
点击`自定义硬件`
![](https://s1.imagehub.cc/images/2024/11/03/dee03260e54c14bb29d15cc774879d4f.png)
内存设置`4096MB`，根据你的实体机的硬件配置适量增减
![](https://s1.imagehub.cc/images/2024/11/03/b8bddfd6641d233173b5a2779dc4a467.png)
处理器数量设置`1`，每个处理器内核数量设置为`8`，适量减少也可以
如果有虚拟化需求就勾选`虚拟化引擎`
![](https://s1.imagehub.cc/images/2024/11/03/c38395f2f2d200624e9ac4ffe0d3a977.png)
CD/DVD 点击`浏览`选择到你的Rocky Linux9.4镜像
![](https://s1.imagehub.cc/images/2024/11/03/30bb80d183a1cfa6f531c4bc957ac7c0.png)
网络适配器模式按需选择，不了解的自行bing
全部设置完成后点击`关闭`，再点击`完成`即可
![](https://s1.imagehub.cc/images/2024/11/03/a01a3c983cae67e290f5ade38f9fe2f0.png)

# 3. 安装虚拟机
点击`开启此虚拟机`
![](https://s1.imagehub.cc/images/2024/11/03/6a20a914cd8ea76770a982a5e41842a6.png)
用上下方向键选择到`Install Rocky Linux 9.4`
![](https://s1.imagehub.cc/images/2024/11/03/7adaa375a6e9dcd9e30e9244c89cbe54.png)
稍加等待，然后选择系统语言，点击继续
![](https://s1.imagehub.cc/images/2024/11/03/c7541dcb57be97973335557211dd25be.png)
带有黄色感叹号的选项是必须进行配置的
![](https://s1.imagehub.cc/images/2024/11/03/238f6d7069a066b24e0c33718676fd24.png)
首先来配置安装位置，点击`SYSTEM`下方的`Installation Destination`
点击选择到这个80GiB的磁盘，然后点击`Done`
![](https://s1.imagehub.cc/images/2024/11/03/1f6b51f34a542c07810d3cf27cf0d5d3.png)
然后配置Root密码
![](https://s1.imagehub.cc/images/2024/11/03/a648a44fe9550311e059071a2ec68af2.png)
设置完密码后，勾选`Allow root SSH login with password`,允许root用户使用密码进行SSH登录
当你使用的密码是弱密码时，需要点击2次`Done`
![](https://s1.imagehub.cc/images/2024/11/03/b68d71b86124fa66d2abe7cdeec03d59.png)
同时也可以点击`User Creation`创建一个普通用户，键入你的用户名及密码
`Make this user administrator`：设置此用户为管理员
`Require a password to use this accout`：需要密码才能使用这个账户
点击`Done`保存配置
![](https://s1.imagehub.cc/images/2024/11/03/6653c450830e81e43c67485b0a6d9723.png)
然后点击`Software Selection`，选择软件版本
![](https://s1.imagehub.cc/images/2024/11/03/b65602c1df5a9611f68c847ce44eea90.png)
我选择的是`Minimal Install`最小安装，只有命令行界面
想要带有GUI界面的选择第1个`Server with GUI`,选择完成后点击`Done`
![](https://s1.imagehub.cc/images/2024/11/03/e02023bf89316d42023a025eb577e8ab.png)
然后就可以点击`Begin Installation`开始安装Rocky Linux 9.4了
耐心等待安装
![](https://s1.imagehub.cc/images/2024/11/03/de41c47666aebbd045ad42a75468da7b.png)
安装完成后点击`Reboot System`
![](https://s1.imagehub.cc/images/2024/11/03/df6efe6160f96cda0f1c856d7ef28f06.png)
然后就可以开始你的操作了
![](https://s1.imagehub.cc/images/2024/11/03/559f7af4612163eb6499e8e59d0de8f7.png)
