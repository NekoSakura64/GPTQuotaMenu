# GPT 余量菜单栏

macOS 菜单栏小工具，显示当前 ChatGPT/Codex 的 **5 小时窗口剩余额度**；点开可查看每周额度和重置时间。它通过本机已登录的 Codex 读取数据，不需要 API Key，也不会保存账号密码。

## 安装

### 使用 DMG 安装包（推荐）

1. 在仓库页面下载 [`GPTQuotaMenu.dmg`](./GPTQuotaMenu.dmg)。
2. 双击打开 DMG，将 `GPTQuotaMenu.app` 拖入“应用程序”文件夹。
3. 从“应用程序”中打开 GPTQuotaMenu。若 macOS 提示无法验证开发者，请在“系统设置 → 隐私与安全性”中点击“仍要打开”。
4. 首次打开后，菜单栏右上角会出现 `GPTxx%`。

### 从源码运行

在此目录执行：

```bash
swift run
```

首次构建完成后，右上角会出现 `GPTxx%`。请先保持 ChatGPT Desktop 已登录。

## 使用

- 点击菜单栏中的 `GPTxx%` 查看 5 小时窗口和每周窗口的剩余额度。
- 选择“立即刷新”可手动更新；程序默认每分钟自动刷新。
- 选择“退出”可关闭工具。
- 如果希望开机自动运行：打开“系统设置 → 通用 → 登录项”，点击“+”，选择 `GPTQuotaMenu.app`。

工具只读取本机 ChatGPT Desktop/Codex 的登录状态，不需要 API Key，也不会保存账号密码。

## 制作成应用

可以在 Xcode 中打开 `Package.swift`，选择 Product → Archive 后导出为 `.app`；将它拖进“登录项”即可开机启动。

## 说明

此工具显示 Codex/Work 共享额度，而不是普通 Chat 对话次数。具体可用额度仍以 ChatGPT Desktop 的“设置 → Usage/用量”为准。
