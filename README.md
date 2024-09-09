# 🌟 V2board Telegram 机器人 | Version 1.4

[![version](https://img.shields.io/badge/version-1.4-brightgreen)](https://github.com/Mini0001/-v2board-Telegram-) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

🚀 **V2board Telegram 机器人** 是一个基于 **Node.js** 开发的高效工具，旨在为用户提供流量管理、红包生成、签到功能及 USDT 在线充值等功能。它使用经过编译的安全文件，保证无后门或恶意行为。

## ✨ 主要功能

- **群组管理**：在群组中邀请机器人，可通过命令禁言用户。
- **流量查询**：用户可随时查询自己账户的流量使用情况。
- **兑换码生成**：管理员可生成套餐兑换码或流量兑换码。
- **兑换码删除**：一键快速删除不再需要的兑换码。
- **每日签到**：用户可每日签到领取随机流量，配置签到上限。
- **流量红包**：支持发送单人或多人随机抢流量红包。
- **USDT 在线充值**：支持用户通过 USDT 完成充值，汇率可配置，余额自动到账 V2board 后台。

## 📦 社区与支持

加入我们，提出问题或建议：[Telegram 交流群](https://t.me/+4IUsjeKgj04xNmRh)

## 🎨 界面预览

展示机器人功能的视觉效果：


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

机器人通过 `config.json` 文件进行配置，以下是关键字段：

- **hometext**: /start 命令后机器人的主页信息。
- **token**: 机器人密钥。
- **qd**: 最大签到流量，随机从 1 到最大值。
- **qdOpen**: 签到功能开关，`true` 表示开启。
- **qdtime**: 签到冷却时间，默认为 24 小时。
- **usdt**: USDT 支付汇率，7.2 表示 1 USDT = 7.2 余额。
- **adminuid**: 机器人管理员 UID 数组。
- **address**: 你的 TRC20 钱包地址，用户充值使用。
- **freetime**: 用户签到后获得的额外时间（如 10m 表示 10 分钟）。
- **web**: 你的官网地址，机器人会通过 "官网" 命令输出。


# 开打机器人内联模式

- **@BotFather 在官方机器人中设置**:
- **不开启内联模式无法分享流量红包**:
  
![image](https://github.com/user-attachments/assets/fb594680-b48c-4bcd-805f-6965e94c38d2)

![image](https://github.com/user-attachments/assets/e8b8e191-e4ec-43ea-8473-57474b4a5e1b)

![image](https://github.com/user-attachments/assets/99582514-5a18-4c3e-b8e2-ffb521c48497)

- **点击 Turn on 按钮为开启**:

# 克隆仓库
git clone https://github.com/Mini0001/-v2board-Telegram-
如克隆失败请手动下载文件可能因为文件太大导致

# v2_user 数据库中添加uid字段
![image](https://github.com/user-attachments/assets/594b251e-1b05-4365-9ee5-f0a6705dcf58)

# 安装 screen 以便在后台运行机器人
sudo npm install screen

# 给予文件 777 权限
chomd 777 app

# 启动机器人
screen -S Robot ./app


### 机器人命令

```plaintext
/gift         生成兑换码 (管理员专用)
/delegift     删除兑换码 (管理员专用)
/dh [兑换码]  用户兑换命令

