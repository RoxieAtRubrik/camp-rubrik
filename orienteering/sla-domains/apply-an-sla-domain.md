# Apply an SLA Domain

An SLA Domain may be applied at a broad level - such as the management server \(e.g. vCenter Server\), folder, host, cluster, or tag. This enables newly provisioned workloads to automatically inherit protection from a higher level resource. Alternatively, an SLA Domain may be granularly applied per object to achieve specific data protection objectives.

To do so:

In the web UI, on the left-side menu, click **Virtual Machines** &gt; **vSphere VMs**. The vSphere VMs page appears, with the VMs tab selected.

Select **Clusters/Hosts**. The Clusters/Hosts tab appears.

![](https://lh4.googleusercontent.com/4Y9vKp6xfICeO8yEu9dyl15GAUqnDvXYbxEC5V8KMgTQy8pcMP_XrbwW-mAScUbc9jSA9ZQyG9d8WKxi2rtuMCgsHlyblpplxl-JWmOn2Zi3kL0Z_-RlJPSI1BCb_lJk6Qd2Y-jH)

Select the checkbox in front of the vCenter Server.

Notice that the **Manage Protection** button in the upper right-hand corner illuminates and is now clickable. Do not assign an SLA Domain at this time.

![](https://lh5.googleusercontent.com/1oIEr_S00EnfMThpnmkvJqXA9fsdbmL6w-oCb7lGlTOiL5vs3l6QxOpUg39V-wz8iPCvjbpFwKR0FgX9ZiLY3-XXW_qmqfMUyDuHb_nd2-ElMor86RLUHewwn8wb4vU87bzYkcwm)

To place a granular policy on an individual object:

Select the **VMs** tab. The **VMs** page appears. Search for your Linux virtual machine running on vSphere.  Type in `ubuntu` in the **Search by Name** field to locate the assigned Linux VM \(`ubuntu14-vm1`\).

![](https://lh6.googleusercontent.com/OVKmVWpu4nEBZEKrZIt7yMawI-gOnBUNYatIBXYYDFd1NAn-CsywDyPT1OXMq4XNfMAHLmadoCf21UtxgVnr0ZOm5R44JyLwTFh8IOXwcyIyXNQXpuBUP8mTNThmGsZ19djNX6ym)

Select the Ubuntu virtual machine and click **Manage Protection**. 

Find and select the previously created `Camp Rubrik` SLA Domain and press **Next**.

![](https://lh6.googleusercontent.com/wXuOvTXm18Y8gmVyHI3HywhE9rMmyNZ-Q1QKd4jQlJ-pd5SQNExBmKbyCkKTpm-DQwUyQx_69VMSkFG6quwoGuEtIxS6RJiZsNdyFOBap_sivC5aCNnZIs8DHLjD2GlvzwUSJiSp)

Review the retention change caused by changing the SLA Domain.

![](https://lh6.googleusercontent.com/4D5t8an4lX-8d0EgxIBU67LPROPQgvsZaFnPdi0VY8pXTJUWMx_mDxxDbGvcHiCVBEhgf6Y5PQPKyO6W5IqT4UDMVDdep3mlz96_-r_nkrnlfEZWconE5263_Iu_sSY3FT68EEV8)

Click **Submit**.

The VM will soon update to reflect it is protected by the selected SLA Domain.

You have now completed the Orienteering badge!

