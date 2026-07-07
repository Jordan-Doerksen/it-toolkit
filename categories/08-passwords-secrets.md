# 08 — Passwords & Secrets

Store client and admin credentials properly. Never in a spreadsheet, never in a sticky note.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Bitwarden](https://bitwarden.com/)** | The default recommendation. Cloud or self-hosted, free tier is genuinely generous, great apps + browser extensions. Team/org sharing on cheap paid tiers. | Win / macOS / Linux / mobile / web | **OSS** |
| **[KeePassXC](https://keepassxc.org/)** | Offline, local `.kdbx` vault — no cloud, no account, total control. The classic "the database is just a file I keep safe." | Win / macOS / Linux | **OSS** |
| **[Vaultwarden](https://github.com/dani-garcia/vaultwarden)** | Lightweight self-hosted server that's compatible with all the Bitwarden apps. Run your own password cloud on a tiny box. ●● medium. | Self-host | **OSS** |
| **[KeePass (classic)](https://keepass.info/)** | The original Windows KeePass. Huge plugin ecosystem; KeePassXC is the friendlier cross-platform cousin. | Win | **OSS** |
| **[Proton Pass](https://proton.me/pass)** | Free password manager with a clean UX and email aliases. Good consumer/handoff option. | Win / macOS / Linux / mobile / web | Free / OSS apps |

**For shared IT/admin credentials specifically:**

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Passbolt](https://www.passbolt.com/)** | Self-hosted team password manager built for exactly this — sharing infra/admin creds with a group, with permissions. ●● medium. | Self-host / web | **OSS** |
| **[Bitwarden Organizations](https://bitwarden.com/products/business/)** | Same Bitwarden you already use, with shared collections for a team. Easiest team path. | web | Free tier / paid |

**Rule of thumb:** One person or small shop → Bitwarden. No cloud, ever → KeePassXC. Own your own server → Vaultwarden or Passbolt. **Whatever you pick, turn on a strong master password + 2FA.**
