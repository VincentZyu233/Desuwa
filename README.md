# ⌨️ Desuwa - ですわ

<div align="center">

![Desuwa Logo](Assets/DesuwaLogo.png)

**💬 全自动口癖添加工具 - 按下回车自动发送口癖**

[![.NET](https://img.shields.io/badge/.NET-8.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![Windows](https://img.shields.io/badge/Windows-x64-0078D4?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTAgMGgxMS4zNzd2MTEuMzcySDB6TTEyLjYyMyAwSDI0djExLjM3MkgxMi42MjN6TTAgMTIuNjIzaDExLjM3N1YyNEgweiBNMTIuNjIzIDEyLjYyM0gyNFYyNEgxMi42MjN6IiBmaWxsPSIjZmZmIi8+PC9zdmc+)](https://github.com/VincentZyu233/Desuwa/releases)

[![Checks](https://img.shields.io/github/checks-status/cneicy/Desuwa/main?style=for-the-badge&logo=github&logoColor=white)](https://github.com/VincentZyuApps/Desuwa/commits/main)
[![CI](https://img.shields.io/github/actions/workflow/status/cneicy/Desuwa/build.yml?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/VincentZyuApps/Desuwa/actions/workflows/build.yml)
[![Release](https://img.shields.io/github/v/release/cneicy/Desuwa?style=for-the-badge)](https://github.com/cneicy/Desuwa/releases)

</div>

## 🚀 简介

Desuwa 是一个轻量级的 Windows 系统托盘工具，可以在你按下回车键时自动在文本末尾添加自定义口癖（如"ですわ"、"喵"、"desu"等），让你的聊天更有个性！

### ✨ 主要特性

- 🎯 **全局键盘钩子** - 监听所有应用的回车键
- 🔄 **自动文本追加** - 智能在文本末尾添加口癖并发送
- 🧠 **双输入模式** - 支持"剪贴板粘贴"与"逐字模拟输入"两种方式
- ⌨️ **全局快捷键** - 默认 `Alt+F10` 启用/禁用，`Alt+F11` 切换输入方式
- 🎨 **自定义图标** - 启用/禁用状态使用不同的托盘图标
- ⚙️ **灵活配置** - 设置窗口可编辑口癖、输入方式和快捷键
- 💾 **配置持久化** - 配置保存到程序目录下的 `settings.json`
- 🪶 **轻量高效** - 单文件 exe，内存占用极低
- 🔇 **后台运行** - 单实例运行，最小化到系统托盘，不占用任务栏

## 📸 预览图片

#### 🐛 起因：B站评论区

![使用示例](images/bili.comment.png)

### 🖱️ 托盘菜单

![托盘菜单](images/preview.bottom-right.context-menu.png)

### 🎬 演示动画

![演示](images/preview.usage.gif)

## 📥 下载安装

### 📥 方式一：下载预编译版本（推荐）

前往 [Releases](https://github.com/VincentZyuApps/Desuwa/releases) 页面下载最新版本：

| 版本 | 下载 | 压缩 | PDB | 体积 | 场景 |
|------|:----:|:----:|:---:|:----:|------|
| **📦 Self-contained** | [![self-contained.exe](https://img.shields.io/badge/self--contained.exe-0078D4)](https://github.com/VincentZyuApps/Desuwa/releases) | ✅ gzip | ❌ stripped | ~60MB | 省C盘空间用户 |
| **🧩 Runtime-dependent** | [![runtime-dependent.zip](https://img.shields.io/badge/runtime--dependent.zip-67b7d1)](https://github.com/VincentZyuApps/Desuwa/releases) | ✅ zip | ❌ stripped | ~400KB | 已装 .NET 用户 |
| **🐛 Debug** | [![debug.zip](https://img.shields.io/badge/debug.zip-8E8E93)](https://github.com/VincentZyuApps/Desuwa/releases) | ❌ none | ✅ portable | ~140MB | 开发者调 crash |

> ✅ **Self-contained** — 单文件 exe，无需安装 .NET 运行时，双击即可运行。gzip 内压缩，剥离 PDB，体积约 60MB。
>
> ⚠️ **Runtime-dependent** — 需要预先安装 .NET 8.0 运行时。zip 格式压缩，剥离 PDB，体积仅约 400KB。
>
> 🐛 **Debug** — 未压缩，含 portable PDB 调试符号，适合开发者调试使用，体积约 140MB。

### 🔨 方式二：从源码构建

```bash
# 📦 克隆仓库
git clone https://github.com/cneicy/Desuwa.git
cd Desuwa

# 🏗️ 构建 Self-contained 版本
dotnet publish -c Release -r win-x64 --self-contained true

# 🧩 构建 Runtime-dependent 版本
dotnet publish -c Release -r win-x64 --self-contained false
```

## 🎮 使用方法

1. 🚀 **启动程序** - 双击 `Desuwa.exe`，程序会最小化到系统托盘
2. ⚙️ **打开设置** - 右键托盘图标 → 选择"设置..."
3. ✏️ **编辑配置** - 在设置窗口中修改口癖、输入方式和快捷键
4. 🔛 **启用/禁用** - 双击托盘图标、右键托盘菜单，或使用默认快捷键 `Alt+F10`
5. 🔄 **切换输入方式** - 在托盘菜单切换，或使用默认快捷键 `Alt+F11`
6. 🚪 **退出程序** - 右键托盘图标 → 选择"退出"

### ⚙️ 配置说明

- 📁 配置文件保存在程序目录下的 `settings.json`
- 📋 "剪贴板粘贴"模式更适合中文输入法场景
- ⌨️ "逐字模拟输入"模式不改剪贴板，但在中文输入法下兼容性较差

### ⚡ 工作原理

- 🎧 程序监听全局键盘事件
- 🔍 检测到回车键按下时，自动跳转到文本末尾
- ✏️ 根据当前输入方式，在末尾追加你设置的口癖文本
- 📤 然后发送回车键

## 🛠️ 技术栈

| 技术 | 版本 | 说明 |
|:---|:---|:---|
| [![.NET](https://img.shields.io/badge/.NET-8.0-512BD4?style=flat-square&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/) | 8.0 | 🎯 运行时框架 |
| [![C#](https://img.shields.io/badge/C%23-12.0-239120?style=flat-square&logo=cplusplus&logoColor=white)](https://docs.microsoft.com/en-us/dotnet/csharp/) | 12.0 | 💻 编程语言 |
| [![Windows Forms](https://img.shields.io/badge/Windows_Forms-net8.0--windows-0078D4?style=flat-square&logoColor=white&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTAgMGgxMS4zNzd2MTEuMzcySDB6TTEyLjYyMyAwSDI0djExLjM3MkgxMi42MjN6TTAgMTIuNjIzaDExLjM3N1YyNEgweiBNMTIuNjIzIDEyLjYyM0gyNFYyNEgxMi42MjN6IiBmaWxsPSIjZmZmIi8+PC9zdmc+)](https://docs.microsoft.com/en-us/dotnet/desktop/winforms/) | net8.0-windows | 🖼️ UI 框架 |
| [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions) | — | 🤖 CI/CD 自动化 |

### 🔬 核心技术

- 🎣 **全局键盘钩子** - 使用 Windows API `SetWindowsHookEx` 监听键盘事件
- 📟 **系统托盘集成** - 使用 `NotifyIcon` 实现托盘图标和菜单
- ⌨️ **全局快捷键** - 使用 `RegisterHotKey` 注册启用/切换快捷键
- 💉 **文本注入策略** - 使用剪贴板粘贴或 `SendKeys` 模拟输入
- 🎨 **自定义图标** - 嵌入资源加载 ICO 文件
- 💾 **本地配置持久化** - 使用 `settings.json` 保存用户设置

## 📦 项目结构

```
Desuwa/
├── Assets/                    # 🎨 资源文件
│   ├── DesuwaLogo.png        # 🖼️ 原始 logo
│   ├── app.ico               # 📱 应用程序图标
│   ├── enabled.ico           # ✅ 启用状态图标
│   └── disabled.ico          # ❌ 禁用状态图标
├── .github/workflows/        # 🤖 GitHub Actions CI/CD
│   ├── build.yml            # 📜 构建工作流
│   └── build.md             # 📖 构建文档
├── src/                     # 📄 应用源码
│   ├── Program.cs           # 🚀 程序入口
│   ├── TrayApplicationContext.cs # 🔄 托盘与状态协调
│   ├── KeyboardHookService.cs # 🎣 全局键盘钩子
│   ├── GlobalHotkeyService.cs # ⌨️ 全局快捷键
│   ├── SettingsForm.cs      # ⚙️ 设置窗口
│   ├── SettingsStore.cs     # 💾 配置读写
│   └── AppSettings.cs       # 📋 配置模型
├── Desuwa.csproj           # 📦 项目配置
└── README.md               # 📖 本文件
```

## 🔧 开发指南

### 📋 环境要求

- 🪟 Windows 10/11
- 🎯 .NET 8.0 SDK
- 💻 Visual Studio 2022 或 VS Code（可选）

### 💻 本地开发

```bash
# 📦 克隆仓库
git clone https://github.com/cneicy/Desuwa.git
cd Desuwa

# 📥 还原依赖
dotnet restore

# ▶️ 运行程序
dotnet run

# 🏗️ 构建 Release 版本
dotnet build -c Release
```

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📝 更新日志

查看 [Releases](https://github.com/VincentZyuApps/Desuwa/releases) 页面了解下游仓库版本的更新历史。

## 🙏 致谢

- 🎨 Logo 由 [Nano Banana](https://nanobana.ai/) 生成
- 🛠️ 开发辅助：[GitHub Copilot](https://github.com/features/copilot) & [opencode](https://opencode.ai) & [Claude Code](https://claude.ai/code)

---

<div align="center">

**[⬆ 回到顶部](#desuwa---ですわ)**

</div>
