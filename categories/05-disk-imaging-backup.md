# 05 — Disk, Imaging & Backup

Bootable USBs, cloning drives, full-system images, and backups that actually restore.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Ventoy](https://www.ventoy.net/)** | Put many ISOs on one USB stick and pick at boot — no re-flashing. Once you use it you never go back. | Win / Linux | **OSS** |
| **[Rufus](https://rufus.ie/)** | Make a bootable USB from an ISO, fast. The single-ISO standard. | Win | **OSS** |
| **[balenaEtcher](https://etcher.balena.io/)** | Dead-simple cross-platform USB/SD flasher. | Win / macOS / Linux | **OSS** |
| **[Clonezilla](https://clonezilla.org/)** | Bootable disk/partition cloning and imaging. The free workhorse for mass or one-off imaging. ●● medium (text UI). | Bootable | **OSS** |
| **[Veeam Agent Free](https://www.veeam.com/windows-endpoint-server-backup-free.html)** | Free full-image backup + bare-metal restore for a single machine. Reliable, recovery-media included. | Win / Linux | Free |
| **[Macrium Reflect X (trial) / alternatives](https://www.macrium.com/reflectfree)** | Long the go-to free imager; free edition was retired, so for free imaging lean on **Veeam Agent Free** or **Clonezilla**. | Win | — |
| **[Duplicati](https://www.duplicati.com/)** | Encrypted, scheduled, incremental backups to cloud or network storage (S3, B2, Google Drive, etc.). | Win / macOS / Linux | **OSS** |
| **[WinDirStat](https://windirstat.net/)** / **[WizTree](https://diskanalyzer.com/)** | Visual "what's eating my disk space" map. WizTree is much faster (reads the MFT). | Win | OSS / Free |
| **[TreeSize Free](https://www.jam-software.com/treesize_free)** | Folder-size explorer for finding space hogs. | Win | Free |
| **[GParted](https://gparted.org/)** | Bootable partition editor — resize, move, create, fix partitions. | Bootable / Linux | **OSS** |

**Rule of thumb:** Boot media → Ventoy (many ISOs) or Rufus (one). Clone a drive → Clonezilla. Real backups → Veeam Agent Free (image) or Duplicati (files, offsite). "Where'd my space go?" → WizTree.
