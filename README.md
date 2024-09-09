# 🌟 V2board Telegram 机器人 | Version 1.5

[![version](https://img.shields.io/badge/version-1.5-brightgreen)](https://github.com/Mini0001/-v2board-Telegram-) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

🚀 **V2board Telegram 机器人** 是一个基于 **Node.js** 开发的高效工具，专为流量管理、红包生成、每日签到以及 USDT 在线充值等功能打造。使用经过编译的安全文件，无任何后门或恶意行为，确保你的账户安全无忧。

## ✨ 主要功能

- **群组管理**：邀请机器人加入群组后，可使用禁言命令管理群组成员。
- **流量查询**：用户可随时查询自己账户的流量使用情况，操作简便。
- **兑换码管理**：支持管理员生成和删除套餐或流量兑换码。
- **每日签到**：用户每日签到可随机获得流量，签到冷却时间和流量上限可配置。
- **流量红包**：支持单人红包与多人随机红包，让用户享受抢流量的乐趣。
- **USDT 在线充值**：支持 TRC20 USDT 充值，自动为用户账户充值，汇率灵活配置。

## 🆕 更新日志

### Version 1.5 更新内容：

![image](https://github.com/user-attachments/assets/0eeb4604-7bea-4bb3-860f-defc44275413)

- **用户签到更新**：增加快捷签到命令，用户可以直接发送 `签到` 或点击按钮快速签到
- **新增命令 `/server`**：用户可使用此命令快速查看节点列表，方便快捷
- - **修复致命Bug**：如数据库连接错误问题，是因为打包后读取`sql.json`文件时出现的问题

## 📦 社区与支持

有任何疑问或建议，欢迎加入我们的 [Telegram 交流群](https://t.me/+4IUsjeKgj04xNmRh) 与我们交流。

## 🎨 界面预览

以下为机器人部分功能的截图展示：

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

### 配置文件介绍

机器人通过 `config.json` 文件进行配置，以下为关键字段说明：

- **hometext**: /start 命令后显示的主页内容。
- **token**: 机器人的 Telegram token。
- **qd**: 每日最大签到流量，用户随机领取 1 到最大值的流量。
- **qdOpen**: 控制签到功能的开启与关闭，`true` 表示开启。
- **qdtime**: 用户签到冷却时间，默认为 24 小时。
- **usdt**: USDT 汇率，7.2 表示 1 USDT = 7.2 元余额。
- **adminuid**: 管理员 UID 列表。
- **address**: 用户充值使用的 TRC20 钱包地址。
- **freetime**: 用户签到后获得的额外时长（如 10m 表示 10 分钟）。
- **web**: 机器人的官网地址，用户可通过输入 "官网" 命令查询。

### 开启机器人内联模式

在 @BotFather 官方机器人中设置 **内联模式** 以启用分享流量红包功能：

![image](https://github.com/user-attachments/assets/fb594680-b48c-4bcd-805f-6965e94c38d2)

![image](https://github.com/user-attachments/assets/e8b8e191-e4ec-43ea-8473-57474b4a5e1b)

![image](https://github.com/user-attachments/assets/99582514-5a18-4c3e-b8e2-ffb521c48497)

点击 **Turn on** 按钮即可开启内联模式。


# v2_user 数据库中添加uid字段
![image](https://github.com/user-attachments/assets/594b251e-1b05-4365-9ee5-f0a6705dcf58)

### 机器人命令

```plaintext
/gift         生成兑换码 (仅限管理员)
/delegift     删除兑换码 (仅限管理员)
/dh [兑换码]  用户兑换命令
/server       查看节点列表 (新增)

# 安装 screen 以便在后台运行机器人
sudo npm install screen

# 赋予 app 文件执行权限
chmod 777 app

# 启动机器人
screen -S Robot ./app
