# 01 — Remote Access & Support

Getting onto another machine to fix it, whether it's across the office or across the country.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[RustDesk](https://rustdesk.com/)** | Open-source TeamViewer alternative. Self-host your own relay server or use theirs. The go-to free remote-support tool right now. | Win / macOS / Linux / mobile | **OSS** |
| **[TightVNC](https://www.tightvnc.com/)** | Classic lightweight VNC for LAN remote control. Simple, no account. | Win / Linux | **OSS** |
| **[TigerVNC](https://tigervnc.org/)** | Faster, actively maintained VNC. Good cross-platform pick. | Win / macOS / Linux | **OSS** |
| **[Chrome Remote Desktop](https://remotedesktop.google.com/)** | Zero-config remote access through a Google account and browser. Dead simple for helping family/small clients. | Any (browser) | **Free** |
| **[AnyDesk](https://anydesk.com/)** | Fast, polished remote support. **Free for personal use only** — needs a paid license for business. | Win / macOS / Linux / mobile | Free (personal) |
| **[TeamViewer](https://www.teamviewer.com/)** | The old standard. **Free for personal use only**; commercial use gets flagged. | Win / macOS / Linux / mobile | Free (personal) |
| **[MeshCentral](https://meshcentral.com/)** | Self-hosted web-based remote management for a whole fleet of machines. ●● medium — you run the server. | Web / self-host | **OSS** |
| **[Tactical RMM](https://tacticalrmm.com/)** | Self-hosted remote monitoring & management (agent + web console). ●● medium — real RMM without the subscription. | Web / self-host | **OSS** |

**Rule of thumb:** LAN-only quick fix → TightVNC. Over the internet, no fuss → RustDesk or Chrome Remote Desktop. Managing many machines → MeshCentral / Tactical RMM. Watch the "personal use only" trap on AnyDesk/TeamViewer if it's for work.
