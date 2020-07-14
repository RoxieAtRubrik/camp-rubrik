# VM Live Mount

To Live Mount a VM:

1. Using your assigned Windows 2016 Server \(`Win2016-vm1`\), select a snapshot by clicking on the blue dot on an available date.

![](https://lh4.googleusercontent.com/kApQvcNsksf2Tn-f12axVsiZ9Kfrqoz3avVgKyR2Nq-My8mkiBbdjw7bW4Kdl0oCFwYMXDt22MGCh-_8j9CyM5ek647gQC1_HbvAc8XA4vtj0vNh2OGysVxNunPmjFsMmV-ercU7)

1. Open the ellipsis \(`...`\) menu for the snapshot and choose **Mount Virtual Machine**.

![](https://lh5.googleusercontent.com/vttv_iKCYcov3QXvdirSy4W1AJtltyTGvZ8Lako8mYgjnKZX094drTCF7P4_CMw8KY2NapUfbybVqDg76nGRelFCnNn9jTTlVqxiTVLw-11Pbu0Eh2HkQEUgr245YA_pKcQsElUW)

1. Choose an ESXi host for the virtual machine, expand **Advanced Settings**.
2. Select the checkbox next to **Remove virtual network devices**. This option should be enabled when networking configurations may result in an IP address conflict.

![](https://lh5.googleusercontent.com/Zr6NFegMMGkEtDmNOuhwWilhW9421_MwGEgnTAYlBmydWqvEAQY73TUXfeyRLHHup8C5Kg6Qn--VwGnCK8aRi4HbwvZlQB5fxj__CW6aC38_HaenCqvsUy2-DVfNJLFxH_dSV0oy)

1. Click **Mount**.

   The Rubrik cluster mounts the snapshot on the selected ESXi host using the original VM name appended by a date time stamp \(e.g. `Win2016-vm1 03-05 23:18:0`\). The virtual machine is then powered on. During the process, messages about the status appear in the Notifications page. The Rubrik cluster records the final result of the task in the Activity Log.

2. On the left-side menu, click **Live Mounts** &gt; **vSphere VMs**.
3. Locate your Windows virtual machine and wait for its **Status** to change to **Powered On**.

This may take about a minute to appear.

![](https://lh3.googleusercontent.com/HTGKX8tK7k7BSDxZe58wRx2wRAS2mabiR1tLFpCo0ohIMp8sPZ3sseFDGNEJe8oIjXUZjzyRvDfzIQFFIJbpZRr1q2DRWFdtBYpEpLeTok93LsJbqG57veHMbUlJUe7svDCK2eZx)

1. Open a new tab in the web browser and navigate to the vSphere HTML shortcut URL \(bookmarked in the Chrome web browser\) and authenticate using the following credentials:

* Username: `demo@rubrik.lab`
* Password: `Welcome10!`

1. Use the search function in the top center to locate `Win2016-vm1` \(appended with the snapshot time/date stamp\) in vCenter Server.

![](https://lh3.googleusercontent.com/P53qPxKQvzJqNV_-unXB5W8ckPQoRidtJCQ6AsZbGUttNnTJRmWyJG8GrvaiFMKDUNga6BfWSa7ZC3eNfjXE38kxFOOpnqQO55itruSa8cDczaxT5sePmUpW767nzcTQnM1FrIqT)

1. On the **Summary** tab of the VM, scroll down until the **Related Objects** pane is located. Notice the **Storage** on which the VM is running. It is recommended to Storage vMotion the VM files to primary storage if it is desired to keep the VM running long-term.

![](https://lh6.googleusercontent.com/i42VK5eyCUbnUJXTpvx6bWz2jj1qlZpNK7324-9XGN2r7JzuKLJcIZPKxD1wDxCbWEfIz4JgpaT9bUfPj9LQrV2TtVK5iZOhb-76X64BqWdNKHqcBhnHOT88UljckZnzCsYq2VCM)

1. Switch back to the Rubrik UI tab and navigate to **Live Mounts** &gt; **vSphere VMs**.
2. Locate your virtual machine and click the ellipses \(`...`\). Click **Unmount** and then **Unmount** again once the dialog appears.
3. \(Optional\) If you return to the vSphere Web Client, you will notice that the Live Mount VM has been removed from the vCenter Server inventory.

{% hint style="info" %}
**Trail Map:** The Rubrik cluster sets the protection state of the Live Mount recovered virtual machine to Do Not Protect. To protect the new virtual machine, add it to an SLA Domain, or remove the individual assignment of Do Not Protect to permit it to inherit protection.
{% endhint %}

Live Mount can be used to near-instantly instantiate identical environments in moments in isolated or test environments. You can also test an application upgrade, failure scenario, or other use cases using your backup storage. When you are done, you simply throw it away.

