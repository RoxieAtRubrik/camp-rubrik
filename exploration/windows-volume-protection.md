# Windows Volume Protection

A Rubrik cluster can protect a group of drives on a Windows server. Protecting Windows volumes uses the Rubrik Backup Service on a Windows host to create a Virtual Hard Drive \(VHD\) file.

To protect a Windows volume:

In the Rubrik UI, on the left-side menu, click **Servers & Apps** &gt; **Windows Hosts**. The Windows Hosts page appears.

Select the `sql-s1` workload, and then choose **Manage Protection**.

![](https://lh4.googleusercontent.com/HLjhF3QxzeAeu_1M6c72laBni59K26gCGQaBzW4GeBQoKshyGIzhSO0vaFxQ_QzrlTUlC_6tRk5FeHTxVT1XFeoIetCIsjbJklY7GPC1DzxAqluBp-i7mcMsZBfUDjXo5RU2RqpE)

Select **Volumes** as the Type and choose the `Z:\` drive. Press **Next**. 

![](https://lh3.googleusercontent.com/rV58kA_YN6ylEh2dqeesW1QZzlOQ2nv7DZ9oTlNeVEgFd3owl9RytfohvPNVYsMA1PvqGgdm716tgjeA69rAR4b3mth8Nxis62_ak-OECbMwN0GL2cde8Rn9PE4483K8hPCz3iUP)

Select the `Camp Rubrik` SLA Domain. Press **Next**.

![](https://lh5.googleusercontent.com/AvsptC9e4dW7h3wmjsnnX5PQXQVJtrPr0ABt2Mcmy9qgc53uw_RVkjQPRnBDU0Hfwnk728NoCuf2Mdo2CsBKSjbSy-21ED3PxcpHRlUuoY8nrfaurIQSCHZVaP2ajmnhB08Vvthx)

Review the changes and press **Finish**. 

Click on the `sql-s1` workload to navigate to the host page. Note the Volumes and Filesets pane. Press **On-Demand Snapshot** to take a backup. 

![](https://lh4.googleusercontent.com/huTpvKE_6HWo8S5KcLTGSkzRXUFNWPegAaGa-4FAraKS5_5yIUswW55-KijaWOT3Ff0aGQA0xoElQ_ePVHcvP2c7OfpRtMJXQrMMSXNCDYeu8oituww5T_Mijzgd_KD5ASWjCxnR)

The **On-Demand Snapshot** dialog appears, ensure the `Z:\`drive is selected and press **Next**.

![](https://lh3.googleusercontent.com/zvdPY6Dqk3K5dfLpDbfcsok1JVJ4eo5XRRxy6Db24fPs1JxG7e6CwALxX4JysAPgsBnkv66cePh_oSINX843GHnEdmyxNVuWDX5VF-F2NoajYO4yHIdF6yVfvI-BXmQP2Iwx7rgH)

Press **Next** and select the `Camp Rubrik` SLA Domain. Press **Finish**. Note that an on-demand snapshot can be managed by a separate policy to specify a different retention period. 

Click on the globe menu in the Activity Log. The **Activities** screen reports the latest status of the snapshot operation. Select the message under Activities to review the Activity Detail. 

![](https://lh3.googleusercontent.com/emv52F6wVhxo-1PRpPMT6TwsF8LU1qBdbpaUCSMxBivfZFqyaKdcnVBPdLpvt5VO5_W7yQUpFxF9UkY0_PxKR71HLWJ2UB_NE_izunvyN3lDo7JXK3ePrO7a6ErtXMUfGRmQkK4O)

A Live Mount of a volume group can provide direct access to the volumes in the group, allowing for quick recovery. To do so:

Locate the **Snapshots** calendar view screen and find a date indicated by a green dot.  Click on the green dot to see one or more available snapshots from that date.

Click on the ellipsis (**...**) menu and select **Mount**.  

![](https://lh6.googleusercontent.com/8tCo_YfVCL61mvpwlnAoXhRmexIOzE0AcvvMRKmhmmPtbWuqTpUHZRQFDvcOnmG5HtKX4CYczc9a4A0JMcvXZZW3KkeLmhqC-xScmih5wRYIBwW_JLUZFaE68p2zNihbtFlyDBwm)

In the **Mount Snapshot** screen, ensure the checkbox next to the `Z:\` is selected and click **Next** to continue.

![](https://lh4.googleusercontent.com/yNQWwtyWR-CX7RGR4zdNPKxvw_qYnvTcwELTPbxLogk0wSh4UP_eK_myNyfk1MuePgp2dzUVmp9yp0OlvdgHDQ1pjIpl_HhqIpInjrlX7zRAqqFxU3mXawe8x9YXbtKNPTLSBkc6)

Select the radio button next to **No Host**. This will expose the SMB path during the mount operation. Click **Next** to continue. 

![](https://lh5.googleusercontent.com/11moWwS3hRcP3nfXTsI4LhaIYWkF9s0wsRevoXGKdLLa_xm-m2wRfbt-Wz7Ug0Lb2goaUXSnnUt4_2Mrv6b-9nFiatYm73-gj4fbAdsAJeLlghf2uXynehPC1WyO_DBlH3IhBCMO)

Enter the following information on the **SMB Configuration** screen:

* Domain: `rubrik.lab`
* Usernames: `demo`
* Active Directory Groups: `rubrikgroup`
* Client IP: `10.0.2.100`

![](https://lh4.googleusercontent.com/CECpGcpoCjcriLk2DAkU_D5JpVaP-JaRLMY2R1OMzxhO8lX9HiVtNRm9NHWDtrOYu7ecuKw8eX4KiFaDZ7CLJ4iFWP4_E39Vm1VU2NARRhm7VD8AOXhSBzpV3D8FJVeLWA8uxFYe)

The process will take a few moments to complete to expose the SMB share. You can review progress in the **Activities** pane. 

![](https://lh5.googleusercontent.com/yEJhHIjpKbwpv-jN_aZVZ5h6Rzk2F5dBeJ8K2M83dvzfxp6-IzPICEsIcLNS4HmljzdurrJGuhy872YkqNKND1bYFI-1N1BG4fU7-P6DU4EKS-juCOdOdvxgOLnSh6yi33RcUFdM)

On the left-side menu, click **Live Mounts** > **Windows Volumes**. Hover over the `sql-s1.rubrik.lab` server name to view the SMB Path details. Click the SMB Path to copy the information into the Clipboard.

![](https://lh5.googleusercontent.com/yTYh4ce4B6ior5vgOxvm9Z-gi8QXtsJIOZRks-3E_fZPfSdOxsDslFsE2CsubV89tkTY62Hr3av0x5JCp_MO03HCmtFLz4Lv2jHOw5Xu7YA5dp2nm9YN4PNVkJcx7UE4wEpRb7LA)

Open the Windows File Explorer application on Jump1. Paste the contents of the Clipboard in the Navigation window of File Explorer and press **Enter**.

![](https://lh3.googleusercontent.com/ymNwyDQiCuagxDbjkdnHLhPq-hzlecB6SW3bpP6H48T-MOctkEPDoGXRN0r3ZjMLjCvY3ER5bDTADZNMoH_cH8Y62WdLbOjx507J9IKkstgbtBKNaszvkGJHi0EV4oWWibYz4biT)

In this case, notice the Live Mount has mounted the `E:\volume` as Data. There is a Files folder listed with seven files listed.

![](https://lh3.googleusercontent.com/d53gyU5HBc3wJnziEDMorW4_EfpITkao2Z_emI7QH4PWwYHzVAlKVtoX-k29bvJ7BDLi6EKCG3Clc7uLqiGv-3zoTXx1vGjO2fXB0C_wyjPFLvB6fxN16El0omaj4cHxQq5AcBEc)

