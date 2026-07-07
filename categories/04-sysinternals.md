# 04 — Sysinternals (Windows)

Microsoft's own free power-tools for looking inside Windows. Grab the **[whole suite](https://learn.microsoft.com/sysinternals/downloads/sysinternals-suite)**
once and keep it in your toolkit folder — or run any of them straight from **`\\live.sysinternals.com\tools\`**.

| Tool | What it does |
|------|--------------|
| **[Process Explorer](https://learn.microsoft.com/sysinternals/downloads/process-explorer)** | Task Manager on steroids — see the full process tree, which handle/DLL locks a file, verify signatures, check a process on VirusTotal. |
| **[Autoruns](https://learn.microsoft.com/sysinternals/downloads/autoruns)** | Every single thing that starts with Windows — startup, services, scheduled tasks, drivers. The #1 malware-hunting and slow-boot tool. |
| **[Process Monitor (ProcMon)](https://learn.microsoft.com/sysinternals/downloads/procmon)** | Live log of every file, registry, and process operation. "Why does this app fail?" → filter ProcMon. ●● medium. |
| **[TCPView](https://learn.microsoft.com/sysinternals/downloads/tcpview)** | Live view of all network connections and the process behind each. |
| **[PsExec](https://learn.microsoft.com/sysinternals/downloads/psexec)** | Run commands on a remote Windows machine from the command line. ●● medium (and AV loves to flag it — that's normal). |
| **[Autologon](https://learn.microsoft.com/sysinternals/downloads/autologon)** | Configure a machine to auto-login safely (encrypted password). Handy for kiosks/lab boxes. |
| **[BgInfo](https://learn.microsoft.com/sysinternals/downloads/bginfo)** | Paints machine name, IP, specs onto the desktop wallpaper. Great for labs and RDP jump boxes. |
| **[Disk2vhd](https://learn.microsoft.com/sysinternals/downloads/disk2vhd)** | Turn a live physical machine into a VHD you can boot in a VM. Quick P2V. |
| **[RAMMap](https://learn.microsoft.com/sysinternals/downloads/rammap)** / **[VMMap](https://learn.microsoft.com/sysinternals/downloads/vmmap)** | See exactly how memory is being used. For chasing leaks/pressure. |
| **[SDelete](https://learn.microsoft.com/sysinternals/downloads/sdelete)** | Securely wipe files/free space. |

**Rule of thumb:** Slow boot or suspected malware → Autoruns + Process Explorer. "What is this app doing / why does it break?" → ProcMon. Everything here is free, portable, and signed by Microsoft.
