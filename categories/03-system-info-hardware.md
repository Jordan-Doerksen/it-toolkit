# 03 — System Info & Hardware

What's inside the machine, how hot it's running, and whether the drive is about to die.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[HWiNFO](https://www.hwinfo.com/)** | The most thorough free hardware info + live sensors tool. Temps, voltages, fan speeds, every component. | Win | Free |
| **[CPU-Z](https://www.cpuid.com/softwares/cpu-z.html)** | Exact CPU, motherboard, RAM, and chipset details. The standard for "what CPU/RAM is this?" | Win | Free |
| **[GPU-Z](https://www.techpowerup.com/gpuz/)** | Same idea for graphics cards — model, clocks, temps, sensors. | Win | Free |
| **[CrystalDiskInfo](https://crystalmark.info/en/software/crystaldiskinfo/)** | Drive health via S.M.A.R.T. — tells you when a disk is failing before it does. Install-everywhere tool. | Win | **OSS** |
| **[CrystalDiskMark](https://crystalmark.info/en/software/crystaldiskmark/)** | Quick disk speed benchmark. "Is this drive actually slow?" | Win | **OSS** |
| **[HWMonitor](https://www.cpuid.com/softwares/hwmonitor.html)** | Simple temperature/voltage/fan monitor when you don't need HWiNFO's depth. | Win | Free |
| **[Speccy](https://www.ccleaner.com/speccy)** | Clean, friendly full-system spec summary. Nice for reports/handoffs. | Win | Free |
| **[Open Hardware Monitor](https://openhardwaremonitor.org/)** / **[LibreHardwareMonitor](https://github.com/LibreHardwareMonitor/LibreHardwareMonitor)** | Open-source temp/fan/voltage monitoring. LibreHardwareMonitor is the maintained fork. | Win | **OSS** |
| **[MemTest86](https://www.memtest86.com/)** | Bootable RAM tester. When a machine crashes randomly, prove or clear the memory. | Bootable USB | Free |
| **[BurnInTest / Furmark / Prime95](https://www.mersenne.org/download/)** | Stress-test CPU/GPU to reproduce heat or stability faults. ●● use with care (they run hardware hot). | Win | Free |

**Rule of thumb:** Full picture + sensors → HWiNFO. Is the drive dying? → CrystalDiskInfo. Random crashes? → MemTest86 (RAM) then temps in HWiNFO. Quick spec sheet for a client → Speccy.
