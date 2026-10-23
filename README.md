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

# 校园巡检（实验三）

## 运行方法
1. 用 Android Studio 打开工程，等待 Gradle Sync 完成。
2. 连接真机或启动模拟器。
3. 点击 Run，桌面应用名为“校园巡检”。

## 三个文件职责
- `MainActivity.kt`：系统入口，设置 Compose 内容，持有巡检状态，安排请求并更新结果。
- `InspectionScreen.kt`：显示巡检数据、两个请求按钮及结果文本，计算未检查数量。
- `InspectionNetwork.kt`：创建 OkHttpClient，以挂起函数方式执行 HTTPS 请求，处理响应和异常。

## 请求说明
本实验使用公共回显服务 `https://httpbin.org/get?room=...`，仅用于验证参数传递与网络接入，不保存巡检记录，也不是从真实服务器获取巡检任务。Room、DataStore、WorkManager 留待后续实验。