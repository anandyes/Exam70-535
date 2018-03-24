### Azure Backup[^](https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup)

Key features:
* Automatic Storage Management (Pay-as-you-use)
* Unlimited Scaling
* Multiple storage options (LRS and GRS)
* Unlimited data transfer (no limit and charge for inbound and outbound data transfers)
* Data encryption
* Application-consistent backup
* Long-term retention

### Azure Backup Components[^](https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use)


||||||
|:--|:--|:--|:--|:--|
|**Component**|**Benefits**|**Limits**|**What is protected?**|**Where are backups stored?**|
|Azure Backup Agent (MARS)|<ul><li>Backup files and folders on Physical or virtual windows OS</li> <li> No backup server required </li> </ul>|<ul><li> Backup 3x per day</li><li>Not application aware; file, folder, and volume-level restore only</li> <li>**No support for Linux**</li> </ul>| <ul> <li>Files</li> <li> Folders </li> <li> System State</li></ul>| Recovery Services vault |
|System Center DPM|<ul><li>Application-aware snapshots (VSS)</li> <li>Linux support on Hyper-V and VMware VMs</li></ul>|<ul><li>Cannot back up Oracle workload</li></ul>|<ul><li>Files</li><li> Folders</li><li>Volumes</li><li>VMs</li><li>Applications</li><li>Workloads</li><li>System State</li></ul>| <ul><li> Recovery Services vault</li> <li>Locally attached disk</li><li>Tapes (on-prem)</li></ul>|
|Azure Backup Server | <ul> <li>Does not require System Center license</li></ul>|<ul><li>Cannot back up Oracle workload</li><li>Always requires live Azure subscription</li><li>No support for tape backup</li> </ul>|<ul><li>Files</li><li>Folders</li><li>Volumes</li><li>VMs</li><li>Applications</li><li>Workloads</li><li>System State</li></ul>| <ul><li> Recovery Services vault</li> <li>Locally attached disk</li></ul>|
|Azure IaaS VM Backup|<ul><li>Native backups for Windows/Linux</li><li>No specific agent installation required</li><li>Fabric-level backup with no backup infrastructure needed</li></ul>|<ul><li>Back up VMs once-a-day</li><li>Restore VMs only at disk level</li><li> **Cannot back up on-premises**</li></ul>|<ul><li>VMs</li><li>All disks (using PowerShell)</li></ul>|Recovery Services vault|
||||||
