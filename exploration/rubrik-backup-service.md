# Rubrik Backup Service

The Rubrik Backup Service \(RBS\) provides the Rubrik cluster application-level visibility for SQL Server and Oracle databases, as well the ability to manage physical Windows, Linux, AIX, and Solaris workloads. Rubrik can backup Linux and Windows virtual machines at a more granular level than via a VM level backup.

The Rubrik Backup Service software can be downloaded directly from the Rubrik cluster, or the software can be downloaded once and copied to the appropriate server as needed.

{% hint style="info" %}
**Trail Map:**

The Rubrik Backup Service software can only be used with the Rubrik cluster from which the software is obtained. Each Rubrik cluster generates a copy of the Rubrik Backup Service software that includes authentication and encryption information specific to that Rubrik cluster. This method ensures that the Rubrik cluster and a hosted deployment of the Rubrik Backup Service can reliably authenticate each other and encrypt data-in-flight
{% endhint %}

After upgrading the Rubrik cluster software, the Rubrik cluster automatically upgrades the Rubrik Backup Service software on all protected server hosts. Upgrades do NOT require a reboot or a server restart.

The Rubrik Backup Service must run as an account that is a member of the Administrators group of the Windows Server host. On Linux or Unix machines you will need to install with root level access.

