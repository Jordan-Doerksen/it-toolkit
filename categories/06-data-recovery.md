# 06 — Data Recovery

Getting back files that were deleted, or pulling data off a drive that's on its way out.

> **First rule of recovery:** stop using the affected drive immediately, and recover **to a different drive**.
> Every write reduces your chances.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Recuva](https://www.ccleaner.com/recuva)** | Friendly undelete for accidentally-deleted files. First thing to try for "oops, emptied the recycle bin." | Win | Free |
| **[TestDisk](https://www.cgsecurity.org/wiki/TestDisk)** | Recover lost/deleted **partitions** and fix boot sectors. The tool when a drive suddenly shows as "unformatted." ●● medium (text UI). | Win / macOS / Linux | **OSS** |
| **[PhotoRec](https://www.cgsecurity.org/wiki/PhotoRec)** | Sister to TestDisk — carves files by signature even when the filesystem is trashed. Ignores partition damage entirely. | Win / macOS / Linux | **OSS** |
| **[ddrescue](https://www.gnu.org/software/ddrescue/)** | Image a failing drive intelligently (retries bad sectors, logs progress). Do this **first** on a dying disk, then recover from the image. ●● medium. | Linux / macOS | **OSS** |
| **[Disk Drill (Free)](https://www.cleverfiles.com/)** | Polished GUI recovery; free tier recovers up to a size cap. Good when you want something click-driven. | Win / macOS | Free (capped) |

**Rule of thumb:** Simple undelete → Recuva or Disk Drill. Missing/corrupt partition → TestDisk. Filesystem destroyed, just save the files → PhotoRec. **Drive physically failing/clicking → image it with ddrescue first**, then recover from the copy.
