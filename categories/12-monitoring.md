# 12 — Monitoring

Know a server or site is down before the phone rings. Ranges from "5-minute setup" to "medium."

| Tool | What it does | Platform | License |
|------|--------------|----------|---------|
| **[Uptime Kuma](https://github.com/louislam/uptime-kuma)** | The easy win. Self-hosted status/uptime monitor with a beautiful UI — HTTP, ping, port, cert-expiry checks + alerts to Discord/Slack/email/Telegram. Runs in one Docker container. Start here. | Self-host / web | **OSS** |
| **[Zabbix](https://www.zabbix.com/)** | Full-featured enterprise-grade monitoring for servers, network gear, and services — free and open source. ●● medium (real setup, but the standard). | Self-host / Linux | **OSS** |
| **[LibreNMS](https://www.librenms.org/)** | Auto-discovering network monitoring via SNMP — switches, routers, servers, with graphs and alerts. ●● medium. | Self-host / Linux | **OSS** |
| **[Prometheus](https://prometheus.io/)** + **[Grafana](https://grafana.com/oss/grafana/)** | The modern metrics stack: Prometheus scrapes metrics, Grafana draws the dashboards. Grafana is also the go-to for pretty dashboards on any data. ●● medium. | Self-host | **OSS** |
| **[Netdata](https://www.netdata.cloud/)** | Drop it on a box and instantly get thousands of real-time metrics with zero config. Fantastic for single-server deep-dives. | Win / Linux / macOS | **OSS** |
| **[Nagios Core](https://www.nagios.org/projects/nagios-core/)** | The old-guard monitoring engine. Still widely deployed; steeper to configure. ●● medium. | Self-host / Linux | **OSS** |
| **[Glances](https://nicolargo.github.io/glances/)** | A single-command, cross-platform "top on steroids" — quick live system overview in a terminal or browser. | Win / macOS / Linux | **OSS** |
| **[Healthchecks](https://healthchecks.io/)** | Dead-man's-switch monitoring for cron jobs and backups — pings you when a scheduled job *doesn't* run. Self-hostable. | Web / self-host | **OSS** |

**Rule of thumb:** Want "is it up?" alerts today → Uptime Kuma. One server's health right now → Netdata or Glances. Monitor a whole fleet/network properly → Zabbix (servers) or LibreNMS (network gear). Dashboards on anything → Grafana. Cron/backup didn't run → Healthchecks.
