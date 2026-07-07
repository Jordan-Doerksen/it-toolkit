# 13 — Virtualization & Labs

Spin up test machines, build a home/work lab, run legacy OSes safely.

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[VirtualBox](https://www.virtualbox.org/)** | The free desktop hypervisor. Run Windows/Linux VMs on your machine for testing. The default for a first lab. | Win / macOS / Linux | **OSS** |
| **[VMware Workstation Player / Pro](https://www.vmware.com/products/desktop-hypervisor.html)** | Now **free for personal use** (and Pro free for personal too). Snappier than VirtualBox for some workloads. | Win / Linux | Free (personal) |
| **[Proxmox VE](https://www.proxmox.com/en/proxmox-virtual-environment/overview)** | Free, open-source **server** virtualization (KVM VMs + LXC containers) with a web UI. The homelab/small-business favorite for a dedicated host. ●● medium. | Self-host / Linux | **OSS** |
| **[Hyper-V](https://learn.microsoft.com/virtualization/hyper-v-on-windows/)** | Built into Windows Pro/Enterprise — enable a feature, no download. Solid if you're all-Windows. | Win | Free (built-in) |
| **[Windows Sandbox](https://learn.microsoft.com/windows/security/application-security/application-isolation/windows-sandbox/)** | Throwaway clean Windows desktop in seconds to test a sketchy installer — wipes itself on close. Win Pro/Enterprise. | Win | Free (built-in) |
| **[QEMU](https://www.qemu.org/)** | The open-source engine behind a lot of this. Powerful, scriptable, emulates other CPU architectures too. ●● medium (CLI). | Win / macOS / Linux | **OSS** |
| **[Vagrant](https://www.vagrantup.com/)** | Define a VM in a text file and `vagrant up` — reproducible dev/test boxes on top of VirtualBox/others. ●● medium. | Win / macOS / Linux | Free/OSS core |
| **[Docker Desktop](https://www.docker.com/products/docker-desktop/)** / **[Podman](https://podman.io/)** | Containers, not full VMs — the fastest way to run one of the self-hosted tools on this list. Podman is fully open and daemonless. ●● medium. | Win / macOS / Linux | Free / OSS |

**Rule of thumb:** Quick test VM on your laptop → VirtualBox (or Hyper-V if you're on Win Pro). Test a risky installer → Windows Sandbox. Dedicated always-on lab host → Proxmox. Running the self-hosted tools from this repo → Docker/Podman.
