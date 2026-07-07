# IT Toolkit — free & open-source tools that actually get used

A curated, no-nonsense list of the **free and open-source tools IT people reach for every day**, from
basic help-desk work up to solid mid-level admin tasks. Nothing exotic, nothing enterprise-only, nothing
that needs a sales call. If it's on this list, it's free (or has a genuinely useful free tier), it's
widely trusted, and a competent tech can be productive with it the same afternoon.

> **Scope:** basic → medium. Deep/advanced gear (full SIEMs, Kubernetes, pentest frameworks, etc.) is
> deliberately left out to keep this usable. Where a tool leans "medium," it's marked **●● medium**.

## How to use this

Every tool lives in a category file under [`categories/`](categories/). Open the one you need, or
`Ctrl+F` this page. Each entry tells you **what it does in one line, the platform, the license, and the link** —
so you can decide in five seconds whether to grab it.

| # | Category | What's in it |
|---|----------|--------------|
| 01 | [Remote Access & Support](categories/01-remote-access.md) | Get onto someone else's machine to fix it |
| 02 | [Networking & Diagnostics](categories/02-networking-diagnostics.md) | Scan, sniff, ping, trace, connect |
| 03 | [System Info & Hardware](categories/03-system-info-hardware.md) | What's inside the box, is it healthy |
| 04 | [Sysinternals (Windows)](categories/04-sysinternals.md) | Microsoft's own power-tools for Windows internals |
| 05 | [Disk, Imaging & Backup](categories/05-disk-imaging-backup.md) | Bootable USBs, clones, images, backups |
| 06 | [Data Recovery](categories/06-data-recovery.md) | Get deleted/lost files back |
| 07 | [Security & Malware Removal](categories/07-security-malware.md) | Find and remove nasties |
| 08 | [Passwords & Secrets](categories/08-passwords-secrets.md) | Store and share credentials safely |
| 09 | [File Transfer & Sync](categories/09-file-transfer-sync.md) | Move and mirror files reliably |
| 10 | [Everyday Utilities](categories/10-everyday-utilities.md) | The little tools you install on every machine |
| 11 | [Documentation & Ticketing](categories/11-documentation-ticketing.md) | Notes, diagrams, tickets, asset tracking |
| 12 | [Monitoring](categories/12-monitoring.md) | Know when something's down before they call |
| 13 | [Virtualization & Labs](categories/13-virtualization.md) | Spin up test machines |
| 14 | [Editors & Terminals](categories/14-editors-terminal.md) | Where you actually do the work |

## The "install these first" starter kit

If you set up a fresh tech workstation tomorrow, these earn their spot on almost any machine:

- **[7-Zip](categories/10-everyday-utilities.md)** — archives, everything
- **[Notepad++](categories/14-editors-terminal.md)** — fast text/code editor
- **[Everything](categories/10-everyday-utilities.md)** — instant file search
- **[PowerToys](categories/10-everyday-utilities.md)** — Windows power-user pack
- **[Sysinternals Suite](categories/04-sysinternals.md)** — Process Explorer, Autoruns, ProcMon
- **[Advanced IP Scanner](categories/02-networking-diagnostics.md)** — see what's on the LAN
- **[PuTTY](categories/02-networking-diagnostics.md)** + **[WinSCP](categories/09-file-transfer-sync.md)** — SSH + file transfer
- **[Rufus](categories/05-disk-imaging-backup.md)** / **[Ventoy](categories/05-disk-imaging-backup.md)** — bootable USBs
- **[KeePassXC](categories/08-passwords-secrets.md)** or **[Bitwarden](categories/08-passwords-secrets.md)** — passwords
- **[Malwarebytes](categories/07-security-malware.md)** — cleanup

## Legend

- **OSS** — open source. **Free** — free to use (may be closed-source or have a paid tier).
- **●● medium** — a bit more setup or know-how than the basics.
- Platforms: **Win**, **macOS**, **Linux**, **Web/self-host**.

## A note on trust & safety

- Always download from the **official site** linked here, not a random mirror or "download portal."
- Some free tools (AnyDesk, TeamViewer) are free **for personal use only** — check the license before using them commercially. Those are flagged.
- Portable/admin tools like PsExec and Nmap can trip antivirus. That's expected; know what you're running.

---

*Maintained as a living list. Missing a tool you swear by? Add it to the right category file.*
