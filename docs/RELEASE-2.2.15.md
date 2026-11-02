## TeXEq 2.2.15 (KaTeX, macOS arm64) — 2026-11-02

### What's new / 本次更新

- **In-app feedback** — a new *Feedback & Suggestions* entry in the editor reports bugs, feature requests or other suggestions to the developer, with optional contact information and automatic version / system details.
  **App 内反馈** — 编辑器新增「反馈与建议…」，可提交问题、功能诉求或其他建议，自动附带版本与系统信息，可选填联系方式。
- Fixed: license, update and permission dialogs could open behind the editor window.
  修复：授权、更新与权限提示可能在编辑器窗口后方打开。
- Improved: keyboard focus and text input in dialogs.
  改进：弹窗中的键盘焦点与文字输入。
- Includes the 2.2.x fixes: Word insertion / double-click reliability, older license recognition, transparent background for colored equations, faster double-click response.
  包含 2.2.x 的修复：Word 插入与双击可靠性、旧授权识别、彩色公式透明背景、双击响应提速。

### Download / 下载

- `TeXEq-2.2.15-katex-arm64.pkg` (4,224,699 bytes, ≈ 4 MB)
- `TeXEq-2.2.15-katex-arm64.pkg.sha256`

SHA-256:

```
767ed863cad6600eabf399ab55259681e52c80f11a44f236f96d1a33beeb6923
```

Verify with / 校验：

```bash
shasum -a 256 TeXEq-2.2.15-katex-arm64.pkg
```

### Install / 安装

1. Double-click the `.pkg` and install (administrator password required).
   双击 `.pkg` 安装（需要管理员密码）。
2. The installer is not notarized: if macOS blocks it, right-click the `.pkg` → **Open**, or use **System Settings → Privacy & Security → Open Anyway**.
   安装包未公证：若被拦截，右键点击 `.pkg` → **打开**，或到「系统设置 → 隐私与安全性」点「仍要打开」。
3. On first launch, enable **TeXEq** in **System Settings → Privacy & Security → Accessibility**; otherwise double-click editing will not respond.
   首次运行请在「系统设置 → 隐私与安全性 → 辅助功能」中勾选 TeXEq，否则双击编辑不生效。

Full guide: [docs/INSTALL.md](https://github.com/Rancho-123/texeq/blob/main/docs/INSTALL.md)

### Requirements / 系统要求

- macOS 15 or later / macOS 15 及以上
- Apple silicon (arm64) — Intel Macs are not supported yet / Apple 芯片，暂不支持 Intel Mac
- Microsoft PowerPoint / Word 2019, 2021 or Microsoft 365 (desktop) / 桌面版 Office 2019 / 2021 / Microsoft 365

### Notes / 说明

- Free download with a 7-day full-feature trial; a license is required to keep editing after the trial. Existing equations remain viewable and printable.
  免费下载，7 天全功能试用；试用结束后需授权才能继续编辑，已有公式仍可查看与打印。
- License: 2 Macs per license, device transfer supported.
  授权默认绑定 2 台 Mac，支持换机。
- Changelog: [CHANGELOG.md](https://github.com/Rancho-123/texeq/blob/main/CHANGELOG.md)
- Website: <https://texeq.rancholab.cn> · Issues: <https://github.com/Rancho-123/texeq/issues>
