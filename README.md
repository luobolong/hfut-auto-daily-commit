```
本项目遵从GPLv2协定，Copyright (C) 2021, Fw[a]rd

免责声明
根据GPL协定，我、本项目的作者，不会对您使用这个脚本带来的任何后果负责。
```

# 合肥工业大学自动健康打卡脚本

在此特别感谢[@HowardZorn](https://github.com/HowardZorn)大佬的工作！

[原项目地址](https://github.com/HowardZorn/hfut_auto_check-in)

我在原项目的基础上添加了QQ邮箱推送功能，为遵守GPLv2协议，现将我的修改内容开源。

你如果想使用其他邮箱，可以自行修改代码。

### 依赖安装

```
pip install -r requirements.txt
```

### 配置文件格式说明

打开config-example.ini配置文件，按照以下格式修改。

```
[info]
username=你的学号
password=你的密码
address=你当前的填报地址（定位信息）

[email]
enable=是否开启QQ邮箱推送功能：1 开启 / 0 关闭
sender_address=发送方地址（只能填一个）
receiver_address=接收方地址（可填多个，中间用逗号隔开，必须是QQ邮箱）
auth_code=授权码（需要开启SMTP服务）
```
### 如何打开QQ邮箱的SMTP服务功能

[如何打开POP3/SMTP/IMAP功能？](https://service.mail.qq.com/cgi-bin/help?subtype=1&&no=166&&id=28)

### 使用方法

```
python3 ./hfuter.py ./config-example.ini
```
可以在腾讯云函数或服务器上配合定时器使用此脚本。

### 声明

请务必谨慎、低调使用，学校可能会检查IP地址是否与填报地址一致，有一定的风险性，以此带来的后果与作者无关。
