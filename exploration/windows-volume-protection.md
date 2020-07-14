# Windows Volume Protection

A Rubrik cluster can protect a group of drives on a Windows server. Protecting Windows volumes uses the Rubrik Backup Service on a Windows host to create a Virtual Hard Drive (VHD) file.

To protect a Windows volume:

1. In the Rubrik UI, on the left-side menu, click **Servers & Apps** > **Windows Hosts**. The Windows Hosts page appears.
2. Select the `sql-s1` workload, and then choose **Manage Protection**.

![alt_text](images/image46.png "image_tooltip")

3. Select **Volumes** as the Type and choose the `Z:\` drive. Press **Next**. 

![alt_text](images/image47.png "image_tooltip")

4. Select the `Camp Rubrik` SLA Domain. Press **Next**.

![alt_text](images/image48.png "image_tooltip")

5. Review the changes and press **Finish**. 
6. Click on the `sql-s1` workload to navigate to the host page. Note the Volumes and Filesets pane. Press **On-Demand Snapshot** to take a backup. 

![alt_text](images/image49.png "image_tooltip")

7. The **On-Demand Snapshot** dialog appears, ensure the `Z:\ `drive is selected and press **Next**.

![alt_text](images/image50.png "image_tooltip")

8. Press **Next** and select the `Camp Rubrik` SLA Domain. Press **Finish**. Note that an on-demand snapshot can be managed by a separate policy to specify a different retention period. 
9. Click on the globe menu in the Activity Log. The **Activities** screen reports the latest status of the snapshot operation. Select the message under Activities to review the Activity Detail. 

![alt_text](images/image51.png "image_tooltip")

A Live Mount of a volume group can provide direct access to the volumes in the group, allowing for quick recovery. To do so:

1. Locate the **Snapshots** calendar view screen and find a date indicated by a green dot.  Click on the green dot to see one or more available snapshots from that date.
2. Click on the ellipsis (**…**) menu and select **Mount**.  

![alt_text](images/image52.png "image_tooltip")

3. In the **Mount Snapshot** screen, ensure the checkbox next to the `Z:\` is selected and click **Next** to continue.

![alt_text](images/image53.png "image_tooltip")

4. Select the radio button next to **No Host**. This will expose the SMB path during the mount operation. Click **Next** to continue. 

![alt_text](images/image54.png "image_tooltip")

5. Enter the following information on the **SMB Configuration** screen:

    * Domain: `rubrik.lab`
    * Usernames: `demo`
    * Active Directory Groups: `rubrikgroup`
    * Client IP: `10.0.2.100`

![alt_text](images/image55.png "image_tooltip")

6. The process will take a few moments to complete to expose the SMB share. You can review progress in the **Activities** pane. 

![alt_text](images/image56.png "image_tooltip")

7. On the left-side menu, click **Live Mounts** > **Windows Volumes**. Hover over the `sql-s1.rubrik.lab` server name to view the SMB Path details. Click the SMB Path to copy the information into the Clipboard.

![alt_text](images/image57.png "image_tooltip")

8. Open the Windows File Explorer application on Jump1. Paste the contents of the Clipboard in the Navigation window of File Explorer and press **Enter**.

![alt_text](images/image58.png "image_tooltip")

9. In this case, notice the Live Mount has mounted the `E:\volume` as Data. There is a Files folder listed with seven files listed.

![alt_text](images/image59.png "image_tooltip")