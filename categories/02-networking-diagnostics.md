# 02 — Networking & Diagnostics

Scan the network, see what's talking, connect to devices, chase down "the internet is slow."

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Advanced IP Scanner](https://www.advanced-ip-scanner.com/)** | One-click LAN scan: IPs, hostnames, MACs, open shares. The fastest "what's on this network" tool. | Win | **Free** |
| **[Angry IP Scanner](https://angryip.org/)** | Cross-platform IP/port scanner. Lightweight, portable. | Win / macOS / Linux | **OSS** |
| **[Nmap](https://nmap.org/)** + **[Zenmap GUI](https://nmap.org/zenmap/)** | The network scanner. Host discovery, port scanning, service/OS detection. ●● medium — huge but you only need a few flags to start. | Win / macOS / Linux | **OSS** |
| **[Wireshark](https://www.wireshark.org/)** | Packet capture and analysis. When you truly need to see what's on the wire. ●● medium. | Win / macOS / Linux | **OSS** |
| **[PuTTY](https://www.putty.org/)** | The classic SSH / Telnet / serial client for Windows. Tiny, portable, essential. | Win | **OSS** |
| **[MobaXterm](https://mobaxterm.mobatek.net/)** | SSH client + tabbed terminal + X server + SFTP in one window. Free "Home Edition." | Win | Free |
| **[WinMTR](https://sourceforge.net/projects/winmtr/)** / **[mtr](https://github.com/traviscross/mtr)** | Combines ping + traceroute into a live table. Best tool for pinpointing where a route goes bad. | Win / Linux / macOS | **OSS** |
| **[iperf3](https://iperf.fr/)** | Measure real throughput between two machines. Settle "is it the network or the app" arguments. | Win / macOS / Linux | **OSS** |
| **[NetworkMiner](https://www.netresec.com/?page=NetworkMiner)** | Passive network forensics — pulls files, credentials, hosts from a capture. Free edition. ●● medium. | Win / Linux | Free |
| **[Fing](https://www.fing.com/)** | Phone-app network scanner. Handy for a quick device inventory from your pocket. | mobile | Free |
| **[TCPView](https://learn.microsoft.com/sysinternals/downloads/tcpview)** | Live list of every connection a Windows box has open, and which process owns it. (See also Sysinternals.) | Win | **Free** |

**Rule of thumb:** "What's on the LAN?" → Advanced IP Scanner. "Is this port open?" → Nmap. "Where's the slowdown?" → WinMTR. "What is this packet doing?" → Wireshark. SSH into gear → PuTTY / MobaXterm.
