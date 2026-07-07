# 09 — File Transfer & Sync

Moving files to servers, mirroring folders, and keeping things in sync without babysitting.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[WinSCP](https://winscp.net/)** | SFTP / SCP / FTP client for Windows with a dual-pane Explorer feel. The default for "get files onto that Linux box." | Win | **OSS** |
| **[FileZilla](https://filezilla-project.org/)** | Cross-platform FTP / FTPS / SFTP client. (Grab from the official site; skip the bundled offers in the installer.) | Win / macOS / Linux | **OSS** |
| **[FreeFileSync](https://freefilesync.org/)** | Folder comparison + sync with real-time or scheduled jobs. Excellent for backups and mirroring. | Win / macOS / Linux | **OSS** |
| **[Syncthing](https://syncthing.net/)** | Continuous peer-to-peer folder sync between your own machines — no cloud, encrypted. Like self-hosted Dropbox. | Win / macOS / Linux | **OSS** |
| **[rclone](https://rclone.org/)** | "rsync for cloud storage" — sync/copy to 70+ backends (S3, B2, Drive, OneDrive…). Scriptable, rock-solid. ●● medium (CLI). | Win / macOS / Linux | **OSS** |
| **[rsync](https://rsync.samba.org/)** | The classic efficient file-sync/copy tool on Linux/macOS (and via WSL). Delta transfers, everywhere. | Linux / macOS / WSL | **OSS** |
| **[TeraCopy](https://www.codesector.com/teracopy)** | Faster, more reliable large file copies on Windows with verify + error handling. Free version covers most needs. | Win | Free |
| **[Snapdrop / PairDrop](https://pairdrop.net/)** | Browser-based "AirDrop for everything" — send files device-to-device over the LAN, no install. | Web | **OSS** |

**Rule of thumb:** Upload to a server → WinSCP. Mirror/backup folders on a schedule → FreeFileSync. Keep your own machines in sync → Syncthing. Cloud storage automation → rclone. Big local copy, want it verified → TeraCopy.
