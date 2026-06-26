<div align=center>

[![Downloads](https://img.shields.io/github/downloads/__REPO__/__VERSION__/total?style=for-the-badge&logo=github)](https://github.com/__REPO__/releases/tag/__VERSION__)

</div>

## 📦 Desuwa __VERSION__

### ⬇️ Download

| 版本 | 下载 | 压缩 | PDB | 体积 | 场景 |
|------|:----:|:----:|:---:|:----:|------|
| **Self-contained** | [![self-contained.exe](https://img.shields.io/badge/self--contained.exe-0078D4)](__BASE_URL__/Desuwa-windows-x64-self-contained-__VERSION__.exe) | ✅ gzip | ❌ stripped | ~60MB | 省C盘空间用户 |
| **Runtime-dependent** | [![runtime-dependent.zip](https://img.shields.io/badge/runtime--dependent.zip-67b7d1)](__BASE_URL__/Desuwa-windows-x64-runtime-dependent-__VERSION__.zip) | ✅ zip | ❌ stripped | ~400KB | 已装 .NET 用户 |
| **Debug** | [![debug.zip](https://img.shields.io/badge/debug.zip-8E8E93)](__BASE_URL__/Desuwa-windows-x64-debug-__VERSION__.zip) | ❌ none | ✅ portable | ~140MB | 开发者调 crash |

> ✅ **Self-contained** — 单文件 exe，无需安装 .NET 运行时，双击即可运行。gzip 内压缩，剥离 PDB，体积约 60MB。
>
> ⚠️ **Runtime-dependent** — 需要预先安装 .NET 8.0 运行时。zip 格式压缩，剥离 PDB，体积仅约 400KB。
>
> 🐛 **Debug** — 未压缩，含 portable PDB 调试符号，适合开发者调试使用，体积约 140MB。

---

### ✨ What's Changed

__CHANGE_LOG__

---

### 📊 Build Info

- **Build date**: __BUILD_DATE__
- **Commit**: [\`__COMMIT_SHA__\`](https://github.com/__REPO__/commit/__COMMIT_SHA__)

__FULL_CHANGELOG__
