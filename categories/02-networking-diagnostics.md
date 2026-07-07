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

## More diagnostics — DNS, capture, latency, ports, bandwidth

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[dig (BIND DNS tools)](https://www.isc.org/dns-tools/)** | Command-line DNS lookups — A/AAAA/MX/NS/TXT/SOA, trace delegation with `+trace`, and spot resolver-vs-authoritative mismatches. The DNS-troubleshooting standard. | Win / macOS / Linux | **OSS** |
| **[doggo](https://github.com/mr-karan/doggo)** | A friendlier modern `dig` — color/tabular or JSON output, DoH/DoT/DoQ support. Single binary. | Win / macOS / Linux | **OSS** |
| **[tcpdump](https://www.tcpdump.org/)** | Command-line packet capture with BPF filters — grab traffic to a `.pcap` on a headless box or over SSH, then open it in Wireshark. ●● medium. | Linux / macOS / BSD (Win via WinDump) | **OSS** |
| **[PingPlotter Free](https://www.pingplotter.com/products/free/)** | Visual traceroute that continuously graphs latency and packet loss **per hop** — pinpoint which hop is dropping or spiking. Free tier = one target. | Win / macOS / Linux | Free (tier) |
| **[PingInfoView](https://www.nirsoft.net/utils/multiple_ping_tool.html)** | Continuously pings a batch of hosts (ICMP or TCP) and tabulates response time, success/fail and loss in one window. Quick multi-host up/down. | Win | Free |
| **[SmokePing](https://oss.oetiker.ch/smokeping/)** | Self-hosted latency/loss grapher — pings targets on a schedule and renders the signature "smoke" graphs to spot jitter and flaky links over time. ●● medium. | Linux / Docker | **OSS** |
| **[CurrPorts](https://www.nirsoft.net/utils/cports.html)** | Lists every open TCP/UDP port mapped to its owning process; right-click to kill the process or close the connection. Flags unsigned listeners. | Win | Free |
| **[LibreSpeed](https://librespeed.org/)** | Free/OSS HTML5 speed test — run in-browser or self-host to measure down/up throughput, ping and jitter with no third-party telemetry. ●● medium (to self-host). | Web / self-host | **OSS** |
| **[arp-scan](https://github.com/royhills/arp-scan)** | Sweep the local subnet with ARP to find live hosts + their MAC/vendor — catches devices that block ping/ICMP. ●● medium. | Linux / macOS / BSD | **OSS** |
| **[bandwhich](https://github.com/imsnif/bandwhich)** | Terminal tool showing live bandwidth broken down by process, connection and remote host — spot what's saturating a link. ●● medium. | Win / macOS / Linux | **OSS** |
| **[NetSetMan](https://www.netsetman.com/en/freeware)** | One-click switch between saved network profiles (IP, subnet, gateway, DNS, PC name, printer) for techs hopping between sites. ⚠ free edition is **non-commercial only**. | Win | Free (personal) |

## Wi-Fi diagnostics — channels, signal, surveys

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[WifiInfoView](https://www.nirsoft.net/utils/wifi_information_view.html)** | Portable scanner that tables every nearby AP — SSID, BSSID, channel, RSSI, PHY type, max speed, vendor. Fast channel/signal triage, no install. | Win | Free |
| **[WiFi Analyzer](https://apps.microsoft.com/detail/9nblggh33n0n)** | Store app that plots nearby APs on live 2.4/5 GHz channel graphs with a signal meter — find the least-crowded channel and dial in router placement. | Win | Free (tier) |
| **[NetSpot](https://www.netspotapp.com/)** | WiFi analyzer + **site survey** — walk a floor plan to build a coverage heatmap that pinpoints dead zones. Free tier scans fully; heatmap survey is capped. ●● medium. | Win / macOS / Android / iOS | Free (tier) |
| **[Acrylic WiFi Home](https://www.acrylicwifi.com/en/wifi-analyzer/)** | Windows scanner listing SSIDs with RSSI, channels, band, encryption, vendor + signal/channel graphs to spot overlap. WiFi 7 / 6 GHz support. ⚠ personal use only. | Win | Free (personal) |
| **[WiFiman](https://wifiman.com/)** | Ubiquiti's free, ad-free phone analyzer — signal, throughput, latency, roaming, a speed test, subnet scan, and a coverage heatmap. Works with any WiFi. | iOS / Android / desktop | Free |
| **[WiFiAnalyzer (open-source)](https://github.com/VREMSoftwareDevelopment/WiFiAnalyzer)** | Free Android app graphing signal by channel across 2.4/5/6 GHz, rating channels and estimating AP distance. (Get it from Play/F-Droid, not a clone.) | Android | **OSS** |
| **[inSSIDer](https://www.oscium.com/inssider/)** | Lists nearby APs with channel, width, signal, WiFi generation, max rate and security to spot overlap and misconfigured APs. Needs a free account. | Win / macOS | Free (tier) |
| **[WirelessNetView](https://www.nirsoft.net/utils/wireless_network_view.html)** | Tiny background monitor logging nearby networks over time — signal (last/avg), channel, auth, MAC, and detection frequency. Good for spotting rogue APs. | Win | Free |
| **[Vistumbler](https://www.vistumbler.net/)** | Open-source scanner that logs APs via the Native WiFi API and, with a GPS receiver, maps signal coverage for export to Google Earth (KML/GPX). ●● medium. | Win | **OSS** |

**Wi-Fi rule of thumb:** Quick "what channel should I use" on a laptop → WifiInfoView or WiFi Analyzer. On a phone, walking the space → WiFiman. A real coverage heatmap/survey → NetSpot. Wardrive/GPS map → Vistumbler.

> **Heads-up on NirSoft tools** (WifiInfoView, WirelessNetView, PingInfoView, CurrPorts): powerful and legit, but antivirus/SmartScreen often false-flags them. Download only from **nirsoft.net**.
