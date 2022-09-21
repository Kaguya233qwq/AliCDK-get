# nonebot_plugin_alicdk_get

### ~~一款对阿里云盘说“**拿来吧你！**”的插件~~

![](.README_images/d1527335.png)

基于nonebot2与aligo的阿里云盘兑换码自动获取和兑换插件。通过使用定时任务每5秒向阿里盘盘酱的分享记录发送一个请求，如果检测到最新的记录含有兑换码，便会在五秒内执行自动兑换的逻辑，并通通过bot发送通知给用户。阿里盘盘酱每次分享的兑换码都是图片形式，故使用了在线图像识别接口来提取图片内容。（OCR接口失效本项目也会失效。需按时维护）

### **环境要求：**

aligo：[项目地址](https://github.com/foyoux/aligo)

apscheduler:[项目地址](https://github.com/nonebot/plugin-apscheduler)

### **开始使用**

1.安装本插件。

`pip install nonebot-plugin-alicdk-get`

2.第一次启动会弹出二维码，请使用阿里云盘app授权登录。

3.在`.env`文件中设置定时任务执行时间间隔，可根据自己的需求修改

(int)`SECONDS = 5`

4.修改接收bot消息的群号，兑换成功将会通知您

(str)`RECV_GROUP_ID = ""`

5.守株待兔。

### **使用命令**

您也可以不使用定时任务。当您发现有兑换码被发布时，可以直接在有bot的群内发送：`/福利码`来手动执行兑换。

### 注意👀️ ：当兑换成功时定时任务将会暂停。如需继续监控请重新启动
