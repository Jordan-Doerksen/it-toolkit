# 14 — Editors & Terminals

Where you actually read logs, edit configs, and run commands.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Notepad++](https://notepad-plus-plus.org/)** | Fast, lightweight text/code editor with syntax highlighting, find-in-files, and column edit. First thing to open a config or log on Windows. | Win | **OSS** |
| **[Visual Studio Code](https://code.visualstudio.com/)** | The everything-editor: extensions for every language, built-in Git, integrated terminal, SSH remote editing. Free. | Win / macOS / Linux | **Free (OSS core: [VSCodium](https://vscodium.com/))** |
| **[Windows Terminal](https://learn.microsoft.com/windows/terminal/)** | Modern tabbed terminal for PowerShell, CMD, and WSL in one window. Ships with Windows 11. | Win | **OSS** |
| **[PowerShell 7](https://learn.microsoft.com/powershell/)** | Cross-platform, far more capable than the built-in Windows PowerShell 5.1. The scripting language for Windows admin. | Win / macOS / Linux | **OSS** |
| **[WSL](https://learn.microsoft.com/windows/wsl/)** | Run a real Linux environment inside Windows — `wsl --install` and you have Ubuntu with rsync, ssh, grep, and the rest. | Win | Free (built-in) |
| **[MobaXterm](02-networking-diagnostics.md)** | SSH client + terminal + SFTP + X server in one — see Networking. | Win | Free |
| **[Tabby](https://tabby.sh/)** / **[WezTerm](https://wezfurlong.org/wezterm/)** | Modern, cross-platform, highly configurable terminals if you want something beyond the defaults. | Win / macOS / Linux | **OSS** |
| **[VS Code Remote-SSH / Remote-WSL] extensions** | Edit files on a remote server or in WSL as if they were local. Turns VS Code into your everywhere-editor. | — | Free |
| **[jq](https://jqlang.github.io/jq/)** / **[yq](https://github.com/mikefarah/yq)** | Command-line JSON/YAML processors — slice API responses and config files without a script. ●● handy once you learn a couple filters. | Win / macOS / Linux | **OSS** |

**Rule of thumb:** Quick edit → Notepad++. Anything bigger, or editing on a server → VS Code (with Remote-SSH). Live on the command line → Windows Terminal + PowerShell 7, and `wsl --install` when you want real Linux tooling.
