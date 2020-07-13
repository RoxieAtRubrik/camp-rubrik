# VMDK Live Mount

To mount a virtual disk:

1. Using your assigned Windows 2016 Server (`Win2016-vm1`), select a snapshot by clicking on the blue dot on an available date. (**Virtual Machines > vSphere VMs**)
2. Open the ellipsis (`...`) menu for the snapshot date chosen.
3. Choose **Mount Virtual Disks**.
4. Multiple disks should be listed. Select the checkbox in front of the 2GB drive.

![alt_text](images/image34.png "image_tooltip")

5. After clicking on **Next**, you have the option of selecting any of your VMs to mount the disk on. Select the radio button in front of the `Win10-vm1` virtual machine and click Finish.

![alt_text](images/image35.png "image_tooltip")

6. This will live mount the VMDK to the Windows 10 VM. You can check this by opening up the HTML5 vSphere client from the Chrome bookmark bar.
7. After logging into the vSphere client, click on `Win10-vm1` and look at the **Related Objects** to see the NFS datastore mounted from the Rubrik cluster.

![alt_text](images/image36.png "image_tooltip")

8. To see that the virtual disk is added to the VM, click on Launch Web Console. You may need to login using the following credentials:

    * Username: `DemoRubrik`
    * Password: `Welcome10!`

![alt_text](images/image37.png "image_tooltip")

9. Right click on the Windows Start Menu and select **Computer Management**.

![alt_text](images/image38.png "image_tooltip")

10. Select **Disk Management** under **Storage** to open up the Windows Disk Management screen.

![alt_text](images/image39.png "image_tooltip")

11. If you don’t see a `vol2`, you may need to refresh the disks. If needed, select **Action** and then **Rescan Disks**.

![alt_text](images/image40.png "image_tooltip")

   This VMDK has been mounted as part of the recovery process.

12. Return to Windows Explorer and verify that the new `E:\` drive (`vol2`) has appeared.
13. Navigate to the `E:\logos` folder on the disk and verify the Rubrik logos exist.
14. Return to the Rubrik UI and navigate to **Live Mounts **>** vSphere VMs**, select the ellipsis (`...`) menu choose **Unmount**. Confirm the unmount.

![alt_text](images/image41.png "image_tooltip")

You have now completed the Life-Saving badge!