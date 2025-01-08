# uniapp-bug

本项目用于演示个人发现到的uniapp相关的bug。

## 蓝牙模块相关bug

本BUG产生在APP的iOS端，具体表现为无法正确获取蓝牙授权状态和蓝牙开关状态。

## 项目安装

```bash
yarn install
```

## 复现步骤

1. 项目安装依赖后，在iOS端运行。
2. 点击`初始化蓝牙（openBluetoothAdapter）`按钮，触发蓝牙授权，单击允许。
3. 点击`获取设备设置（getSystemSetting）`按钮和`获取 APP 授权设置（getAppAuthorizeSetting）`按钮，观察相关结果，可以看出确实是已授权。蓝牙开关为开启状态。
4. 退出APP回到桌面，并清除APP的后台运行。
5. 不做任何其他操作，在此打开APP，直接点击`获取设备设置（getSystemSetting）`按钮和`获取 APP 授权设置（getAppAuthorizeSetting）`按钮，观察相关结果，发现蓝牙开关状态为`false`，且蓝牙授权状态为`not determined`。
