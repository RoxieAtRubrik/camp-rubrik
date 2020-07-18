# Filesets

A fileset defines a set of files and folders on a Linux host, a Windows host, or a NAS share. The Rubrik cluster interprets a fileset based on the values provided in the Include, Exclude, and Do Not Exclude fields. The Rubrik cluster applies a set of rules to the values provided in these fields and permits several types of values to be added to the fields. The Rubrik cluster uses the filesets that are assigned to a host or share to determine which data to manage and protect.

To create a fileset:

In the Rubrik UI, on the left-side menu, click **Servers & Apps** > **Windows Hosts**. The Windows Hosts page appears.

Select **Filesets** and then **Add Fileset**.

![](https://lh3.googleusercontent.com/y1Z9Nr0GFjEFZoVvc7WrgTCJk6zIeSp4_pbf8vWVp7o-Tl6qz52IqxF7AeJM-NEnS39TIbwVjsX0yVmTfGMW9_w14g1YAOhWl9tfpFFK_HTImmwkQ0nl7qqXg29cCxKzsAwIGtoM)

The Add Fileset dialog appears. Enter the following values:

* Fileset Name: `Camp Rubrik Fileset`
* Include: `C:\Users\**`
* Exclude: `C:\Users\AppData\**`

The fileset should resemble the following image.

![](https://lh6.googleusercontent.com/x2hWBEAek1xFqEctqZAAfyLp1UvudfE1sCabH_ebatW4X6EJCU3DV4GVTbKRulSUVq6R1-CwvOG2KI5fMwO63Nprtvt7BexIOx3ZMK6O0D6DWjfHxfGXyzVMdijEjBoN_sJc7yHZ)

Click **Add**.

Return to the **Windows Hosts** tab, select the `sql-s1` workload, and then choose **Manage Protection**.

![](https://lh4.googleusercontent.com/HLjhF3QxzeAeu_1M6c72laBni59K26gCGQaBzW4GeBQoKshyGIzhSO0vaFxQ_QzrlTUlC_6tRk5FeHTxVT1XFeoIetCIsjbJklY7GPC1DzxAqluBp-i7mcMsZBfUDjXo5RU2RqpE)

Select **Filesets** as the Type and choose the `Camp Rubrik Fileset` created in a previous step. 

![](https://lh6.googleusercontent.com/0D_Hf8H0-_jm8Rl5gpqJ8pt1cOwpw8_0rveQ-2vSvti_4NtVS_4Y3yN-5r-dkaerj8PbBDkprWe2apuMHx-VMXyuvizI_Pf2lArwlJic4ZLgq3BKdcr6r7wN83ZNjQURj5jeAfHT)

Press **Next** and select the `Camp Rubrik` SLA Domain. Press **Finish**. 

A host or share can be paired with several different filesets, with each host fileset or share fileset protecting a different set of data. Each of the host filesets or share filesets can be assigned to a different SLA Domain, permitting different levels of protection for each set of data.