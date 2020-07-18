# SLA Domains

The SLA Domain unifies data protection policies under a single policy engine. It provides a configurable set of policies that can be applied to all objects protected by Rubrik, whether groups of virtual machines, applications, or hosts to achieve specific data protection objectives.

Rubrik orchestrates end-to-end data lifecycle management. An SLA Domain can be automatically assigned to new workloads as each is provisioned. No manual intervention is required for data to be archived for long-term retention, replicated to your DR site, or expiry at the end of the lifecycle. Easily provision and sunset your workloads without worrying about data management.

SLA Domains represent an easy-to-configure container for data protection policies. The following table provides an overview of those policies.

| **Policy** | **Description** |
| :--- | :--- |
| Snapshot, backup frequency, and retention | Directs the Rubrik cluster when to create point-in-time snapshots, backups of data sources, and how long to keep the data. |
| Replication | Directs the Rubrik cluster to send replicas of source snapshots and backups to a target Rubrik cluster. Also defines the maximum time to keep the replica. |
| Archiving | Directs the Rubrik cluster to move snapshot and backup data to a separate data storage system for long-term retention. |

Rubrik provides Gold, Silver, and Bronze SLA Domains by default for your immediate use. Custom SLA Domains can be quickly and easily created to meet the data protection and retention requirements of different groups of virtual machines, applications, and file system hosts.