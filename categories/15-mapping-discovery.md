# 15 — Mapping & Discovery

You've walked into an unfamiliar environment and have to fix it. These tools answer the two questions
you always start with: **"what's on this network?"** and **"what *is* this machine and everything on it?"**
Every tool here was web-checked as free/OSS (or a genuine free tier) and current.

---

## A. Map the NETWORK — auto-discover & diagram

Point these at a subnet and they find the devices for you, and most will draw or inventory what they find.
Start at the top; they get heavier as you go down.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Spiceworks Inventory](https://www.spiceworks.com/free-pc-network-inventory-software/)** | Free, ad-supported cloud tool that agentlessly scans the LAN (WMI/SNMP) to auto-discover and inventory every IP device — PCs, servers, phones, IoT. Discovery/asset-tracking more than topology. | Web (cloud) | Free |
| **[Lansweeper](https://www.lansweeper.com/)** | Agentless scan that builds a live hardware + software asset inventory in one console. Free tier caps at 100 assets. ●● medium. | Win server / web | Free (tier) |
| **[PRTG Network Monitor](https://www.paessler.com/prtg)** | Sensor-based monitor that auto-discovers devices across an IP range and builds live status maps. Free tier = 100 sensors (~20 devices). ●● medium. | Win server / web / mobile | Free (tier) |
| **[Open-AudIT Community](https://open-audit.com/)** | Agentless scan (SNMP + credentialed WMI/SSH) that auto-builds a full hardware/software asset inventory and flags unknown devices. ●● medium. | Win / Linux (self-host) | **OSS** |
| **[Netdisco](https://netdisco.org/)** | Reads switch MAC/forwarding + router ARP tables over SNMP to tell you **exactly which switch port** any IP or MAC is plugged into. The "trace the cable" tool. ●● medium. | Linux / Docker (web UI) | **OSS** |
| **[NetXMS](https://netxms.com/)** | Auto-discovers and paints a live **L2/L3 connectivity map** from SNMP, LLDP/CDP, ARP caches and switch forwarding tables. ●● medium. | Win / Linux (+ web/desktop consoles) | **OSS** |
| **[Checkmk Raw](https://checkmk.com/)** | Point it at a host or SNMP device and it **auto-discovers the services** running, then monitors them without hand-writing a check per service. ●● medium. | Linux server / web | **OSS** |
| **[Observium Community](https://www.observium.org/)** | Auto-discovering SNMP platform that finds devices and maps their CDP/LLDP/FDP neighbors so you graph a whole network without adding each device by hand. ●● medium. | Linux (LAMP self-host) | **OSS** |
| **[OpenNMS Horizon](https://www.opennms.com/horizon/)** | Full open-source monitoring platform that auto-discovers the network and maps L2/L3 link topology (Enlinkd), with fault + performance monitoring. Heavier — for bigger networks. ●● medium. | Linux / Docker (Java) | **OSS** |

**See also (already elsewhere in this repo):**
[Advanced IP Scanner](02-networking-diagnostics.md) and [Nmap + Zenmap topology](02-networking-diagnostics.md) for a fast first sweep · [Zabbix](12-monitoring.md) and [LibreNMS](12-monitoring.md) both auto-discover **and** draw network/topology maps · [draw.io](11-documentation-ticketing.md) to hand-draw the map · [NetBox](11-documentation-ticketing.md) to record it as the source of truth.

**Rule of thumb:** Just need a device list fast → Advanced IP Scanner (LAN) or Spiceworks/Lansweeper (inventory). Which port is that device on? → Netdisco. A drawn topology map → NetXMS, Zabbix or LibreNMS. Small job, don't want a server → Advanced IP Scanner + draw.io.

---

## B. Map a single MACHINE — audit the box you're fixing

Everything about one computer: hardware, software, services, startup, what's locking a file, why it crashed.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Belarc Advisor](https://www.belarc.com/products/belarc-advisor)** | One-click local audit → a full HTML report of hardware, installed software, license keys, missing hotfixes and security status. Nothing leaves the machine. **The "what is this whole PC" snapshot.** | Win | Free (personal) |
| **[WinAudit](https://github.com/Dan-ATKA/Winaudit)** | Portable full inventory of one machine — hardware, software + licenses, services, drives, security config, network — into a searchable report (HTML/PDF/CSV). | Win | **OSS** |
| **[System Informer](https://systeminformer.io/)** | Task Manager on steroids (open-source successor to Process Hacker) — drill into processes, services, loaded modules, open handles, and live connections to find what's hogging or acting suspicious. | Win | **OSS** |
| **[ServiWin](https://www.nirsoft.net/utils/serviwin.html)** | Lists every Windows service and driver color-coded by state; start/stop/pause and change startup type, then export an HTML report. | Win | Free |
| **[WhatInStartup](https://www.nirsoft.net/utils/what_run_in_startup.html)** | Lists every program set to auto-run at startup (Run keys + Startup folder) with its command line, and lets you disable/delete to fix a slow boot. | Win | Free |
| **[Handle](https://learn.microsoft.com/sysinternals/downloads/handle)** | Command-line: finds which process has a file/folder open — the fast answer to "what's locking this file so I can't delete it" (and can force-close it). | Win | Free |
| **[Dependencies (lucasg)](https://github.com/lucasg/Dependencies)** | Modern open-source Dependency Walker replacement — point it at an .exe/.dll and it maps imported DLLs and flags missing ones. Diagnoses "X.dll was not found." | Win | **OSS** |
| **[FullEventLogView](https://www.nirsoft.net/utils/full_event_log_view.html)** | Flattens every Windows Event Log into one searchable, filterable table with full descriptions — local box, remote machine, or a saved .evtx. Export to CSV/HTML/JSON. | Win | Free |
| **[WhoCrashed](https://www.resplendence.com/whocrashed)** | Reads minidump/crash-dump files after a BSOD and names the likely culprit driver in plain English — no kernel-debugger skills needed. | Win | Free (personal) |
| **[Geek Uninstaller](https://geekuninstaller.com/)** | Portable single-exe: lists installed programs, force-removes stubborn apps with leftover cleanup, and exports the installed-software list to HTML. | Win | Free |

**See also (already elsewhere in this repo):**
[Speccy](03-system-info-hardware.md) / [HWiNFO](03-system-info-hardware.md) for the hardware side · [Autoruns](04-sysinternals.md) + [Process Explorer](04-sysinternals.md) (the Sysinternals pair that overlaps System Informer/Handle) · [CurrPorts](02-networking-diagnostics.md) for open-ports-to-process · [WizTree / WinDirStat](05-disk-imaging-backup.md) for disk usage.

**Rule of thumb:** "Give me a full report of this PC" → Belarc Advisor or WinAudit. What's using this port/process/handle? → System Informer (GUI) or Handle (CLI). It won't start / missing DLL → Dependencies. Why did it BSOD? → WhoCrashed, then dig deeper in FullEventLogView. Slow boot → WhatInStartup (or Autoruns).

> **A note on NirSoft & similar:** Several of these (ServiWin, WhatInStartup, FullEventLogView, CurrPorts) are NirSoft freeware — powerful and legit, but antivirus/SmartScreen often false-flags them as "hacktools." Download only from **nirsoft.net** and allowlist as needed. Same goes for System Informer (it loads a kernel driver).
