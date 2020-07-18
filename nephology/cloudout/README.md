# CloudOut

CloudOut is Rubrik’s ability to cost effectively archive data to the cloud for long-term retention. An SLA Domain can include an archival policy that instructs Rubrik to copy protected data to an archival location. The archival policy specifies the archival location to use, how soon after a backup the data is copied, and how long the data is retained.

Rubrik supports a number archival location types, including:

* Amazon S3
* Amazon Glacier
* Google Cloud Platform 
* Azure
* Object Store
* NFS

A Rubrik cluster can have multiple archival locations and types. The archival policy of an SLA Domain can only specify one archival location but each SLA Domain can specify a different archival location.