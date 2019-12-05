# AdbGuide
Android调试桥
## wifi调试
- 启动adb `android_sdk/platform-tools/`，默认会启动adb服务器程序，端口号为5037。
- 打开命令行输入`adb tcpip 5555`（模拟器/手机的端口为奇数，作为后台程序，此命令会生成客户端程序，端口号为5554（偶数），以此类推）。
- 可以断开USB。
- 查找设备的IP地址，在关于手机那里可以查看。
- `adb connect 设备IP地址`
- `adb devices`列出所有连接设备
- `adb kill -server`
- `adb [-d|-e|-s serial_number] command`
  - `-d`将 adb 命令发送至唯一连接的 USB 设备
  - `-e`将 adb 命令发送至唯一运行的模拟器实例
  - `-s serial_number`将命令发送到指定的设备
- 将文件复制到设备/从设备复制文件
  - `adb pull remote local`
  - `adb push local remote`
- [详细请参考官方文档](https://developer.android.google.cn/studio/command-line/adb.html#copyfiles)
