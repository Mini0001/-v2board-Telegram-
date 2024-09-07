# -v2board-Telegram BOT 机器人-
一款适用于v2board面板的Telegram机器人🔥

Version: 1.3

1 改进了一些显示个人信息的页面
![image](https://github.com/user-attachments/assets/fb32f1a1-fb15-4c49-8c02-e8b0f2fc4069)
![image](https://github.com/user-attachments/assets/f12f3979-3520-40c9-a04a-147ad702b58f)

2 另外配置文件中新增 freetime 字段表示用户签到后可获得流量和到期的时长 (s:秒, m:分钟, h:小时, d:天)，如用户套餐已到期也可以签到并且能获得免费的使用时长，如用户套餐未到期签到成功后会以用户原本的到期时间加上签到后赠送的时长
![image](https://github.com/user-attachments/assets/4551f89b-a2ca-4eab-950b-de89285f87e7)

-----------------------------------------------------------------------

* 启动命令
./app 即可，需要后台挂起任务可以使用 pm2 或 screen 等

⚠️ 此文件那么大是因为是编译后的文件，不存在任何的后门或恶意行为操作！

用户可使用机器人内的USDT支付，支付成功后会按照汇率计算将余额加入到充值成功的用户的v2board面板中，用户可直接在web面板使用余额订阅您的套餐

TG群组 https://t.me/+4IUsjeKgj04xNmRh 有问题可讨论

机器人在线支付内的二维码图片为目录中的 2.jpg 可替换为您的自定义图片 或者 您自己的收款码

* 更新 1.2
  可直接在群组中发送 me 查看个人流量使用情况，可在config.json文件中配置官网url，群组中发送官网后会得到提示，可在群组中引用到用户发送的消息下方发送命令"禁言10s" s(秒), m(分钟), h(小时), d(天)
![image](https://github.com/user-attachments/assets/c4fb5e7c-5ab1-4a7c-b42e-55e948b7a3e2)


![image](https://github.com/user-attachments/assets/18c6f3c3-a150-4ccb-a1ab-d2e513cf7512)
![image](https://github.com/user-attachments/assets/1459454b-6b71-4271-842c-b9ea7d08e277)
![image](https://github.com/user-attachments/assets/5f03c788-898f-4d61-b00c-8b7bfb8325c6)
![image](https://github.com/user-attachments/assets/0dec2336-2552-449d-8327-e994b442cb0a)
![image](https://github.com/user-attachments/assets/500a50b4-fbf5-4881-a126-ad96df6caaed)
![image](https://github.com/user-attachments/assets/8297eb59-1e48-4640-bd06-1a0231804ccd)
![image](https://github.com/user-attachments/assets/8c3b060a-0739-438e-a18d-e51108c88c7a)
![image](https://github.com/user-attachments/assets/34c5240d-6a66-4b27-90fa-c007da12e040)


* 部署教程

* 1. 如图在 v2_user 数据库中添加一个字段为 uid，类型 BIGINT 长度 28
![image](https://github.com/user-attachments/assets/a611c5fc-94c4-497e-9fa7-780cd9c3d1ed)

2 随后在TG官方机器人 @BotFather 中设置机器人
![image](https://github.com/user-attachments/assets/41e614d4-40d7-4eae-ae51-195db0b656c9)
![image](https://github.com/user-attachments/assets/f84294e8-2977-45d8-a9b7-ecf2e00c4139)

将内联模式打开 Turn on 为关闭如图，点击下此按钮后才为打开模式，可以翻译查看，打开此模式是为了用户可以分享红包，如果不打开此模式用户可以发送红包但是不能将红包分享出去
![image](https://github.com/user-attachments/assets/dde789cb-ec3e-4c90-906f-4a92c29fd70b)


* 配置文件
* 如图 config.json 文件中 hometext 字段为使用机器人的时候提示的欢迎语 token字段为机器人的token，qdOpen字段为签到功能true为开启 false 为关闭，qdtime字段为用户需要隔多久才能签到24为24小时这里单位为小时，usdt字段为用户支付usdt的汇率 7.2 表示 1U = 7.2人民币 (余额), adminuid 字段为机器人管理员用户的UID可写多个, count字段为用户发送随机红包个数最大限制，address字段为你钱包的地址仅限 TRC20 链
![image](https://github.com/user-attachments/assets/ebb2fcff-5de8-4cd1-ac7a-deccfd3da130)
