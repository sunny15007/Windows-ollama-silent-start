# Windows Ollama Silent Start

一键静默启动 Ollama Windows 桌面版，无弹窗、无干扰。

## 问题

新版 Ollama 桌面版 (`ollama app.exe`) 在启动时会弹出主窗口，影响使用体验。网上找不到相关解决方案。

## 解决方案

通过监测工具发现，`ollama app.exe` 支持两个隐藏的启动参数：

```bash
ollama app.exe --hide --fast-startup

参数说明
--hide : 启动时隐藏主窗口

--fast-startup : 跳过开屏动画，快速启动

使用方法
方法一：命令行
"%LOCALAPPDATA%\Programs\Ollama\ollama app.exe" --hide --fast-startup
方法二：创建快捷方式（推荐）
桌面右键 → "新建" → "快捷方式"

位置填入：
%LOCALAPPDATA%\Programs\Ollama\ollama app.exe --hide --fast-startup
命名为 Ollama，完成

以后双击这个快捷方式即可静默启动。

效果
✅ 完全静默，无任何弹窗

✅ 后台服务正常启动

✅ 右下角羊驼图标正常出现

✅ 右键菜单完整，可打开设置界面

✅ 退出干净利落

发现者
@sunny15007

声明
本仓库仅用于分享该启动参数的使用方法，不包含任何 Ollama 的源代码或二进制文件。

============================
Ollama app.exe --hide --fast-startup

Parameter Description
--hide : Hide the main window on startup
--fast-startup : Skip the splash screen animation for fast startup

Usage
Method 1: Command Line
"%LOCALAPPDATA%\Programs\Ollama\ollama app.exe" --hide --fast-startup

Method 2: Create a Shortcut (Recommended)
Right-click on the desktop → "New" → "Shortcut"

Enter the location:
%LOCALAPPDATA%\Programs\Ollama\ollama app.exe --hide --fast-startup

Name it "Ollama" and finish.

From then on, double-click this shortcut to start silently.

Effects
✅ Completely silent, no pop-up windows
✅ Background service starts normally
✅ The llama icon appears in the system tray (bottom-right)
✅ Full right-click menu available, can open settings interface
✅ Clean exit without leftovers

Discoverer
@sunny15007

Disclaimer
This repository is only for sharing the usage of these startup parameters and does not contain any source code or binary files of Ollama.
