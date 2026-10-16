# 实验二 网络访问与HTTP对比实验

**姓名：** 鲁哲恺
**学号：** 202530224024

## 一、实验目标
1. 学习在 Android 中配置网络权限。
2. 学习使用 network_security_config.xml 控制明文流量。
3. 对比测试 HTTP 明文请求与 HTTPS 加密请求的区别。

## 二、运行方式
使用 Android Studio 

## 三、接口地址
本项目使用的测试接口为：`http://httpbin.org/get?room=A203`

## 四、实验内容说明
- 点击“HTTPS 请求”按钮：请求成功，返回 HTTP 200 及 `room: A203` 响应。
- 点击“HTTP 请求”按钮（拦截状态下）：请求失败，提示 CLEARTEXT 明文被禁止。
- 修改配置允许明文后重新运行：点击“HTTP 请求”按钮，返回 HTTP 200。

## 五、声明
HTTP 仅用于教学对比，实际服务优先 HTTPS。