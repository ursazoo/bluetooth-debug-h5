# BLE LAB · 蓝牙调试台

无依赖的单文件 Web Bluetooth 调试页，用于 BLE GATT 设备。

## 使用

1. 在支持 Web Bluetooth 的浏览器中通过 HTTPS 打开页面，手机建议 Android Chrome。iPhone Safari 不支持此 API。
2. 开启系统蓝牙。调试自定义设备时，先填入厂商提供的 Service UUID（不是 Characteristic UUID）。
3. 点击“选择并连接设备”，在浏览器的设备选择窗口授权。
4. 选择服务与特征，按设备协议读取、写入或订阅通知。

不填 UUID 时默认申请电池、设备信息、心率三个标准服务。支持 HEX 和 UTF-8 写入、断连重连、JSON 日志导出。蓝牙通信及日志均在浏览器本地处理，不发送到服务器；导出日志可能包含设备标识及通信内容。

## 部署

GitHub Pages 从 `main` 分支根目录发布 `index.html`，无需构建步骤。

## 验证范围

已检查移动端布局，以及模拟 BLE 设备的连接、读写、通知、断连重连和输入校验。真实蓝牙兼容性需在目标手机和设备上验证。
