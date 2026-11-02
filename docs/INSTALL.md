# Installation guide

TeXEq runs as a native macOS app plus an Office add-in. The installer is a standard `.pkg`; no Homebrew, Python or TeX distribution is required.

## 1. Requirements

| Item | Requirement |
| --- | --- |
| Mac | Apple silicon (M1 / M2 / M3 / M4 or later) |
| macOS | 15 (Sequoia) or later |
| Office | Microsoft PowerPoint / Word 2019, 2021 or Microsoft 365 — **desktop** apps |
| Disk | About 20 MB after installation |
| Internet | Not required for editing and rendering; only for license activation and updates |

Not supported: Intel Macs, Windows, WPS Office, Office for the web, macOS 14 and earlier.

## 2. Download and verify

1. Download the latest `TeXEq-<version>-katex-arm64.pkg` from [Releases](https://github.com/Rancho-123/texeq/releases/latest) or the [official website](https://texeq.rancholab.cn/#download).
2. Each release page lists the SHA-256 checksum and ships a matching `.sha256` file. Verify with:

   ```bash
   shasum -a 256 ~/Downloads/TeXEq-2.2.15-katex-arm64.pkg
   ```

   The output must match the checksum in the release notes. If it does not, delete the file and download it again.

## 3. Install

1. Double-click the `.pkg` and follow the installer (administrator password required).
2. The package is **not notarized by Apple**. If macOS refuses to open it:
   - right-click the `.pkg` → **Open** → **Open**, or
   - open **System Settings → Privacy & Security**, scroll down and click **Open Anyway**.
3. When installation finishes, quit and reopen PowerPoint and Word so the ribbon is reloaded.

## 4. Grant Accessibility permission

TeXEq needs **Accessibility** permission to receive double-click events from Office and to write equations back.

1. Launch TeXEq once (from `/Applications/TeXEq.app` or from the Office ribbon).
2. Open **System Settings → Privacy & Security → Accessibility**.
3. Enable **TeXEq**. If it is not listed, click **+** and add `/Applications/TeXEq.app`.
4. Quit and reopen Office.

Without this permission, inserting equations may work but double-click editing will not respond.

## 5. First run

- Open PowerPoint or Word. A **TeXEq** tab appears in the ribbon.
  - PowerPoint: **Insert Equation**, **Inline Equation**.
  - Word: **Inline**, **Display**, **Numbered**.
- The first launch starts a **7-day full-feature trial** automatically. No registration or account is needed.
- After the trial, a license is required to insert or edit equations. Existing equations remain visible, printable and presentable.

## 6. Upgrading

- Quit PowerPoint, Word and TeXEq.
- Install the new `.pkg` over the old version. Settings, trial and license state are preserved.
- Re-check Accessibility permission after the upgrade if double-click editing stops working.

## 7. Troubleshooting

| Symptom | What to try |
| --- | --- |
| "Cannot be opened because the developer cannot be verified" | Right-click the `.pkg` → **Open**, or use **System Settings → Privacy & Security → Open Anyway**. |
| "TeXEq is damaged and can't be opened" | Check the SHA-256 first and re-download. If the checksum matches, remove the quarantine flag: `xattr -dr com.apple.quarantine /Applications/TeXEq.app`, then reopen. |
| No TeXEq tab in Office | Install using the desktop Office apps (not the Mac App Store web wrapper), quit all Office processes and reopen; check **Tools → Templates and Add-ins** / **Add-ins** in Word and PowerPoint. |
| Tab is visible but double-click does nothing | Check **System Settings → Privacy & Security → Accessibility**; TeXEq must be enabled. Reopen Office after changing it. |
| Insert works but the equation cannot be edited later | The equation was not created by TeXEq (for example, a screenshot or a third-party object). Only TeXEq equations and convertible legacy objects keep an editable source. |
| Trial expired | Existing equations still display and print; obtain a license to continue editing. |
| Intel Mac | Not supported. macOS 15 + Apple silicon is required. |

If the problem persists, open an [issue](https://github.com/Rancho-123/texeq/issues) with the TeXEq version, macOS version, Office version, steps to reproduce and a screenshot.

## 8. Uninstall

1. Quit PowerPoint, Word and TeXEq.
2. Move `/Applications/TeXEq.app` to the Trash.
3. Optional: remove the helper files the installer created:

   ```bash
   rm -f ~/Library/LaunchAgents/com.rancholab.eqvilo.watch.plist
   rm -f ~/Library/Application\ Scripts/com.microsoft.Powerpoint/FormulaPilot.scpt
   rm -f ~/Library/Application\ Scripts/com.microsoft.Word/MathNestWord.scpt
   rm -rf ~/Library/Application\ Support/FormulaPilot
   ```

   The Word global template is at
   `~/Library/Group Containers/UBF8T346G9.Office/User Content.localized/Startup.localized/Word/TeXEqWordGlobal.dotm`.

4. Restart Office. Documents already containing TeXEq equations keep displaying the equations; the LaTeX source stored in the shape remains readable by TeXEq if you reinstall.

## 9. For lab / classroom deployment

- The `.pkg` can be deployed with your usual macOS management tooling (for example `installer -pkg ... -target /`). It needs administrator rights.
- The installer writes per-user helper files on first install, using the currently logged-in user.
- No network access is required for editing; the license server is contacted only for activation, license checks and updates.
