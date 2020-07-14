# Objective: Recover a VM

In this lab, you will perform the following tasks:

* Live Mount a VM
* Unmount a VM
* Mount a VMDK
* Unmount a VMDK

Rubrik radically simplifies the recovery process of virtual machines to deliver near-zero RTOs without additional storage provisioning. Quickly test upgrades or recover from ransomware without data loss.

## Getting Started

By serving as an online repository for VM data during the recovery process, Rubrik eliminates the requirement to transfer data before recovery can begin. Live Mount provides a near-zero Recovery Time Objective \(RTO\).

{% hint style="info" %}
**Trail Map:** 

_Recovery Time Objective_ - defines how long it takes to recover data, which can be a single file or a complete data center. This is sometimes referred to as "how long can you afford to have a system offline?" 

_Instant Recovery_ - replaces the source virtual machine with a fully functional point-in-time copy. The Rubrik cluster powers off and renames the source virtual machine and assigns the name of the source virtual machine to the recovered virtual machine. The recovered virtual machine is then powered on and the recovered virtual machine is connected to the source network. The Rubrik cluster is the datastore for the recovered virtual machine until it is Storage vMotioned to another datastore.

 _Live Mount_ - creates a new virtual machine from a point-in-time copy of the source virtual machine. The recovered virtual machine uses the Rubrik cluster as its datastore until it is Storage vMotioned to another datastore. The Rubrik cluster assigns a new name to the recovered virtual machine and powers it up. The source virtual machine runs in parallel. 

_Export_ - creates a new virtual machine from a point-in-time copy of the source virtual machine. The datastore of the selected Hyper-V host is the datastore for the recovered virtual machine. The Rubrik cluster assigns a new name to the recovered virtual machine and powers it up.
{% endhint %}

