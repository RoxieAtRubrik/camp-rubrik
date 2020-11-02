# VM Live Mount

To Live Mount a VM:

Using your assigned Windows 2016 Server (`Win2016-vm1`), select a snapshot by clicking on the blue dot on an available date.

<p align="center">
<img src="../images/image29.png">
</p>

Open the ellipsis (`...`) menu for the snapshot and choose **Mount Virtual Machine**.

<p align="center">
<img src="../images/image30.png">
</p>

Choose an ESXi host for the virtual machine, expand **Advanced Settings**.

Select the checkbox next to **Remove virtual network devices**. This option should be enabled when networking configurations may result in an IP address conflict.

<p align="center">
<img src="../images/image31.png">
</p>

Click **Mount**.

The Rubrik cluster mounts the snapshot on the selected ESXi host using the original VM name appended by a date time stamp (e.g. `Win2016-vm1 03-05 23:18:0`). The virtual machine is then powered on. During the process, messages about the status appear in the Notifications page. The Rubrik cluster records the final result of the task in the Activity Log.

On the left-side menu, click **Live Mounts** &gt; **vSphere VMs**.

Locate your Windows virtual machine and wait for its **Status** to change to **Powered On**.

This may take about a minute to appear.

<p align="center">
<img src="../images/image32.png">
</p>

Open a new tab in the web browser and navigate to the vSphere HTML shortcut URL (bookmarked in the Chrome web browser) and authenticate using the following credentials:

* Username: `demo@rubrik.lab`
* Password: `Welcome10!`

Use the search function in the top center to locate `Win2016-vm1` (appended with the snapshot time/date stamp) in vCenter Server.

<p align="center">
<img src="../images/image33.png">
</p>

On the **Summary** tab of the VM, scroll down until the **Related Objects** pane is located. Notice the **Storage** on which the VM is running. It is recommended to Storage vMotion the VM files to primary storage if it is desired to keep the VM running long-term.

<p align="center">
<img src="../images/image34.png">
</p>

Switch back to the Rubrik UI tab and navigate to **Live Mounts** > **vSphere VMs**.

Locate your virtual machine and click the ellipses (`...`). Click **Unmount** and then **Unmount** again once the dialog appears.

(Optional) If you return to the vSphere Web Client, you will notice that the Live Mount VM has been removed from the vCenter Server inventory.

{% hint style="info" %}
**Trail Map:** 

The Rubrik cluster sets the protection state of the Live Mount recovered virtual machine to Do Not Protect. To protect the new virtual machine, add it to an SLA Domain, or remove the individual assignment of Do Not Protect to permit it to inherit protection.
{% endhint %}

Live Mount can be used to near-instantly instantiate identical environments in moments in isolated or test environments. You can also test an application upgrade, failure scenario, or other use cases using your backup storage. When you are done, you simply throw it away.