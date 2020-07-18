# CloudOn

Cloud instantiation allows users to migrate existing on-premises workloads to the cloud for test/development or even disaster recovery purposes. This feature converts the workload data (VM image) sent to the cloud into a compute instance. Using Rubrik CloudOn, workloads can be migrated at a VM level from on-premises to AWS or Azure.

Rubrik offers three options that can be applied to on-premises workloads that customers choose to instantiate in AWS or Azure:

* **On-Demand** - The default configuration in which Amazon Machine Images (AMIs) or Azure Virtual Hard Drives (VHDs) are created only at the time of a “power on in the cloud” request.
* **Auto Convert Latest Snapshot - Keep One** - Rubrik will automatically construct an AMI or VHD reflecting the latest snapshot to be archived into S3 or Azure. When a new snapshot is sent to the archive, a new AMI or VHD is constructed with the new archive data. Once completed, the older AMI or VHD is removed.
* **Auto Convert Latest Snapshot -** **Keep All** - Rubrik will automatically construct an AMI or VHD reflecting the latest snapshot to be archived into S3 or Azure. When a new snapshot is sent to the archive, a new AMI or VHD is constructed with the new archive data. The older AMI or VHD is retained if desired (configurable via policy) creating a series of AMIs or VHDs representing each snapshot.