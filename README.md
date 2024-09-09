# 🌟 V2board Telegram机器人 Version 1.4

[![version](https://img.shields.io/badge/version-1.4-brightgreen)](https://github.com/Mini0001/-v2board-Telegram-) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

🚀 ** V2board Telegram机器人** 是一个基于 Nodejs 编写的机器人，它的文件那么大是因为是使用编译后的文件，文件安全没有任何的后门等恶意行为

## ✨ 主要特性

- **群管功能**：把机器人邀请加入你的群组中可使用禁言命令禁言用户，使用方法: 需引用到用户发送的信息下方
- **极简设计**：用户可以通过机器人完成查询流量等操作
- **生成礼品兑换码**：管理员可使用命令生成兑换码，可生成兑换你套餐和兑换流量的礼品码
- **快速删除兑换码**：管理员可使用命令快捷删除兑换码
- **用户签到**：可在配置文件 "config.json" 文件中 qd字段设置最大可签到的流量 1 - 最大可签到的流量随机领取流量
- **流量红包**：用户可在机器人内发送流量红包可选单人红包(单人领取) 和 随机红包(多人抢红包)
- **在线USDT充值**：用户可在机器人内使用USDT充值可在"config.json" 文件中设置汇率usdt字段7.2表示1USDT = 7.2余额，用户充值成功后余额将自动充值在用户网页V2board面板余额中, 可在 config.json文件address字段设置为你自己的TRC20地址，二维码图片为目录中的2.jpg可替换为你的二维码

## 📦 交流群

- **Bug 问题，建议都可以提出**：https://t.me/+4IUsjeKgj04xNmRh

## 🎨 界面预览
![image](https://github.com/user-attachments/assets/6e0eae20-c07b-4201-bdf4-2e8631953b2e)
![image](https://github.com/user-attachments/assets/dd29f430-c524-42ba-87d2-fa8a897b8479)
![image](https://github.com/user-attachments/assets/513ad55b-6e3b-45b8-bdb1-26827ac512f8)
![image](https://github.com/user-attachments/assets/be037d01-2000-4bb9-a605-e5893a31d15f)
![image](https://github.com/user-attachments/assets/f7bd9a48-b8d9-4133-b68d-15bc371f8ebe)
![image](https://github.com/user-attachments/assets/aabb43b1-4a0d-4585-afd5-d7c85fb0da35)
![image](https://github.com/user-attachments/assets/a95175d9-1ab3-4374-9cd1-1130faba30de)
![image](https://github.com/user-attachments/assets/bab295d5-6e44-499c-8c1d-4055c643030a)
![image](https://github.com/user-attachments/assets/753c2f83-78fd-4334-84d6-0fdb53a31d96)
![image](https://github.com/user-attachments/assets/3945f26e-88fb-493d-8309-0fb4dd3bd519)


## 🛠️ 安装与使用

```bash
# 配置文件介绍
config.json文件为配置文件
hometext 字段为机器人 发送/start命令后输出的主页内容
token 字段为 机器人的 token 信息
qd 字段为 签到最大可获得的流量
qdOpen字段为签到功能是否开启 true:开 false:关
qdtime字段为用户需要多久才能继续签到 24为 24小时也就是用户一天只能签到一次
usdt字段为用户在机器人内使用usdt支付的汇率7.2表示1USDT = 7.2余额
adminuid字段是一个数组表示机器人管理员的UID如多个管理员 "adminuid": ["6659040184","6659040184","6659040184"],
count字段为用户发随机多人抢红包最大限制红包个数5代表用户最大可设置5个人抢红包
address字段为你的trc20钱包地址用户提供给用户充值使用的
freetime字段为用户签到后赠送的时间10m代表用户签到后获得了流量并且还获得了10分钟的时长 (s:秒, m:分钟, h:小时, d:天)
web字段请填写你官网的地址，用户可对机器人发送 官网 机器人会输出你的官网地址

# 机器人命令
/gift 生成兑换码 (仅管理员UID使用)
/delegift 删除兑换码 (仅管理员UID使用)
/dh [兑换码] (用户兑换命令)

# v2_user 数据库中添加uid字段
![image](https://github.com/user-attachments/assets/594b251e-1b05-4365-9ee5-f0a6705dcf58)

# 克隆仓库
因为文件太大需要手动下载文件

# 安装 screen
sudo npm install screen

# 启动机器人
screen -S Robot ./app
