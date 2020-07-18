# File Recovery

To recover a file:

Search for the `Win2016-vm1` virtual machine running on vSphere.

![](https://lh4.googleusercontent.com/kApQvcNsksf2Tn-f12axVsiZ9Kfrqoz3avVgKyR2Nq-My8mkiBbdjw7bW4Kdl0oCFwYMXDt22MGCh-_8j9CyM5ek647gQC1_HbvAc8XA4vtj0vNh2OGysVxNunPmjFsMmV-ercU7)

The **Overview** pane provides information regarding the object’s location, configuration for CloudOn (if configured), the SLA Domain applied, Oldest and Latest Snapshot, total snapshots, etc. This can vary depending on location and type of machine. On the right-hand side there is a **Snapshots** calendar view. The next few steps will guide you on your journey to explore this more.

![](https://lh6.googleusercontent.com/u6--xVhuel0uafxCweowWvhpx5mqkYCMF-c_LVpiHqhSs35Lh0VxI5Ruq5lb7gkrdUhuhJTqINBJwSfHqFvF-SCUIYXcr3coNK_sNTKVbUAi89e-i2pDi6whTCmPcXlilLzTMGCR)

Select a date that has a blue dot by hovering over and then clicking on the blue dot (indicating there are recovery points from this day). All available snapshots are listed. An example screenshot below demonstrates all of the snapshots available for the selected VM. Note that the date and number of snapshots may differ from the following image.

![](https://lh4.googleusercontent.com/O64fvXUjZi6IPeJQlWGXH1FUG73NiBHPWX6AmR2sevq4Jz2wz5aGgXjyhE0Tkaed7VC0Pcg0Cmg0UYfAavOIm8eUh3UwHYjONQ8Ijc2pNhJRcZRlLq50cZsjbruF2wX083mdZoY7)

Select the ellipses icon (`...`) next to one of the snapshots.

Click **Recover Files**. Next type in the search bar the word `hosts`. Two files are shown.

Click on the checkbox in front of the `C:\Windows\System32\drivers\etc\hosts` and then click **Next**.

![](https://lh3.googleusercontent.com/HMEJtVVl3S-9KuQIo4S46VYMEqlNX1y0Ga2nDeiaGG5yiIyWACXko4SeHVI39SJcIqz6zmdeeV43Hybn-o2Zp9UbqyfReI6YSq1SV6iJP_Mqy3HiPDSnNDvcouCjnGOdef9sMQbB)

There are four options shown: **Download**, **Overwrite original**, **Restore to separate folder**, and **Export**.

![](https://lh4.googleusercontent.com/CWG6dDr_2ItYFYtvy0Jxa3nJu9tv1gLAOxLg8MMFshRY9foy7RTG0uaHuCCcAOiynqNlPY_sCaXAGvoUsaZUCEcmLCYXcLsg4hItgbdLojXjtpAWKdGrYBo-9u-g8D2TZAVSO1HC)

Do not select any of the options at this time and click **Cancel** to exit the dialog.

{% hint style="info" %}
**Trail Map:** 

_Download_ - Rubrik cluster generates download links to use for file level restore (FLR) of files and folders, making it available to download locally to the user's device. 

_Overwrite original_ - files and folders restored directly to a guest file system of the protected workload whether a VM, physical server, or NAS share. This will overwrite the existing files on the machine. 

_Restore to separate folder_ - files and folders restored to a folder of your choosing.

_Export_ - allows you to restore files and folders to a different machine.
{% endhint %}

In the Rubrik UI, locate the **Search by File Name** in the **Snapshots** view and type in the word `hosts` to locate the file.

![](https://lh4.googleusercontent.com/7aiE7__Zy_WwV4jrmgWvsM86OXCwT1e2Aa3-IngXnhdQRNNKrk-PPh1bcJMDQOf8lT99UiFx5Mw2iR05IjNOC-ukDsPDH9E1kb1mZMYu8tZgPv4Ng0yMTbh1EK4J86U-wwoX-ir-)

Click on the `C:\Windows\System32\drivers\etc\hosts`. On the window that appears, choose a version of the file (screenshot below) and select the ellipses (`...`).

![](https://lh5.googleusercontent.com/VFl4Jg5y0xwCTACTtmc0gg9ap35lBlL4YnxonBOMMhYVw9YpL4SfdhuvDoYnZ-bNMVqC1jxTm6C_sIEDYDJ_YX2pzOvN_I4Hwpvgx75O2pgkfQeRiQrj_Zau8PAU83Smy-ZwUyM8)

Choose **Download**.

This may take a few moments. Click on the globe icon in the top right corner of the Rubrik UI to review the notification informing you that the file is ready to download. Click on the “Download link” message.

![](https://lh6.googleusercontent.com/ayiuwKnpAUJ07ier3xOBR4-DbDOElRnHgytichIabT8xT5qIuzMlGRWojcc1HBBamYb3UT_YmhD4WdfC41xiqf8urd6XJARbVzUw2OuPzAD2aQqgrPegSwPyXtZxVVbegibGAUTj)

On the window that opens, click on the download link.

![](https://lh5.googleusercontent.com/IE2PSQY-w4qBYV-MZDXAZ9uTg5IXPs2KBfV-1iufzUKm49GgUY8rD-zYRTMINui4yqMFsbUVBZexF4_-LXfwiCOV0di_gp9r3r_DnY9214C7X4cnnggKpEvjnz6hOc7nHapT1E_Y)

On your Jump1 host accessing the lab environment, browse to the **Downloads** folder to view hosts.

You have now completed the Search & Rescue badge!