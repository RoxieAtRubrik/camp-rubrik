# VMDK Live Mount

To mount a virtual disk:

Using your assigned Windows 2016 Server \(`Win2016-vm1`\), select a snapshot by clicking on the blue dot on an available date. \(**Virtual Machines &gt; vSphere VMs**\)

Open the ellipsis \(`...`\) menu for the snapshot date chosen.

Choose **Mount Virtual Disks**.

Multiple disks should be listed. Select the checkbox in front of the 2GB drive.

![](https://lh6.googleusercontent.com/1lrPyfhjGcHZav11fgr1xHVSw9pspwlZR18VdAOfgVQVbwd8mkKZnkJNe1Onao0lfZU8lM27chKRFX_KSxFW4Zw7hFdSRd2CPXgGz3nRjn903PYfcG_p_E0lufweexmfrW-lvgId)

After clicking on **Next**, you have the option of selecting any of your VMs to mount the disk on. Select the radio button in front of the `Win10-vm1` virtual machine and click Finish.

![](https://lh4.googleusercontent.com/juTmqpZYSCVup_ZoyU5j49vOxWCR_NNAlXmkyEh9dJPS57LJzbvdEn4jJh546BKAAlSR-7NPiNAjp4S-0VJe6W6hpY-9vomqDi190b169v5kYQM5Ztw5nDWXM3aCD4hFixVuV3gi)

This will live mount the VMDK to the Windows 10 VM. You can check this by opening up the HTML5 vSphere client from the Chrome bookmark bar.

After logging into the vSphere client, click on `Win10-vm1` and look at the **Related Objects** to see the NFS datastore mounted from the Rubrik cluster.

![](https://lh5.googleusercontent.com/EQPviiepLnqxJf7LaAF8iBu20HV8RT-CU-8zAc1UjbpYTfnvtpB9k8CTSu_pTD9Pbz9fjLg5vOMwcbdfV5oCGkJ1ZRuO6QGrn65wsS56SeGDHoHjvfjImACs8n8kLOSlSfD5g_uc)

To see that the virtual disk is added to the VM, click on Launch Web Console. You may need to login using the following credentials:

* Username: `DemoRubrik`
* Password: `Welcome10!`

![](https://lh5.googleusercontent.com/uxXbz4r_yaDNoaq-STW5zJDFvq7Tjk1uO5brsbKzQddx0uQtHfcYzRjuA0mvoV_afQxzLO1NWvA7NusZpOCOkz5fIcgyb7uiuBs0ZQVd8y8js5n9jldBEf1IoB59wk1AEbqQ18Gh)

Right click on the Windows Start Menu and select **Computer Management**.

![](https://lh5.googleusercontent.com/nUCgpXrOuzyQfTRYQUf549qlYeOEAB2448SjrZatatmOpZgB8qRfpzQ84DBZg6-T0kka52w-aAUDvVyeHkxgTtPAbQkS7MuW9dqen9Ch33Ju9q47qpF4yVdCeJoYZXrDHcmLoD2l)

Select **Disk Management** under **Storage** to open up the Windows Disk Management screen.

![](https://lh5.googleusercontent.com/Wk9MTodJDGT2Yh6IzPbrp0Q9w1F-50iXbJeeLUTP4iiPyE-7oSDJJv6V2PAv3a4LNQU3caZ8FZSXThH1pZw8n97h2UMHkLEkL2FA0JabvDTfi-g3u5j1YoYgQBiGLBEYPio9Yriy)

If you don’t see a `vol2`, you may need to refresh the disks. If needed, select **Action** and then **Rescan Disks**.

![](https://lh4.googleusercontent.com/QF6adyR-lIcU-TO6tgwsrZSS_S_JXdR76DWABW_drUgJTaNakZ838sPXwxCjx5-LQls3kS0m0A_m_1xbzIbEt5zj5dAbfLLRi9U3jcnuilJiJW8uJ9iZtWasB48FTR-5xyGjucej)

This VMDK has been mounted as part of the recovery process.

Return to Windows Explorer and verify that the new `E:\` drive \(`vol2`\) has appeared.

Navigate to the `E:\logos` folder on the disk and verify the Rubrik logos exist.

Return to the Rubrik UI and navigate to **Live Mounts** &gt; **vSphere VMs**, select the ellipsis \(`...`\) menu choose **Unmount**. Confirm the unmount.

![](https://lh3.googleusercontent.com/zJCP7LU-ZvhXrH3XP7dMPxQjhNDQSm6t7CIiSExyquuY_3mCuvFh8v7szSOu7TvCs9nMMmq-5M15lO_4XEpRzub7r_r14jSq-r7h3YzmecX4EAxX6uTFgSm_jw_-RvSYHJIeo0BX)

You have now completed the Life-Saving badge!

