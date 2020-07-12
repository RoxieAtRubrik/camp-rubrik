# VM Live Mount

To Live Mount a VM:

 	



1. Using your assigned Windows 2016 Server (`Win2016-vm1`), select a snapshot by clicking on the blue dot on an available date.



<p id="gdcalert28" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image28.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert29">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image28.png "image_tooltip")




2. Open the ellipsis (**<code>...</code></strong>) menu for the snapshot and choose <strong>Mount Virtual Machine</strong>.



<p id="gdcalert29" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image29.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert30">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image29.png "image_tooltip")




3. Choose an ESXi host for the virtual machine, expand **Advanced Settings**. 
4. Select the checkbox next to **Remove virtual network devices**. This option should be enabled when networking configurations may result in an IP address conflict.

    

<p id="gdcalert30" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image30.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert31">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image30.png "image_tooltip")


5.  Click **Mount**.

    				


    The Rubrik cluster mounts the snapshot on the selected ESXi host using the original VM name appended by a date time stamp (e.g.  `Win2016-vm1 03-05 23:18:0`). The virtual machine is then powered on. During the process, messages about the status appear in the Notifications page. The Rubrik cluster records the final result of the task in the Activity Log.


    		

6.  On the left-side menu, click **Live Mounts** > **vSphere VMs**. 
7. Locate your Windows virtual machine and wait for its **Status** to change to **Powered On**. 

This may take about a minute to appear. 


## 

<p id="gdcalert31" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image31.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert32">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image31.png "image_tooltip")




8. Open a new tab in the web browser and navigate to the vSphere HTML shortcut URL (bookmarked in the Chrome web browser) and authenticate using the following credentials:
*   Username: `demo@rubrik.lab`
*   Password: `Welcome10!`
9. Use the search function in the top center to locate `Win2016-vm1` (appended with the snapshot time/date stamp) in vCenter Server. 



<p id="gdcalert32" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image32.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert33">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image32.png "image_tooltip")




10. On the **Summary** tab of the VM, scroll down until the **Related Objects** pane is located. Notice the **Storage** on which the VM is running. It is recommended to Storage vMotion the VM files to primary storage if it is desired to keep the VM running long-term. 



<p id="gdcalert33" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image33.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert34">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image33.png "image_tooltip")




11. Switch back to the Rubrik UI tab and navigate to **Live Mounts** > **vSphere VMs**. 
12. Locate your virtual machine and click the ellipses (**<code>...</code></strong>). Click <strong>Unmount</strong> and then <strong>Unmount</strong> again once the dialog appears.
13. (Optional) If you return to the vSphere Web Client, you will notice that the Live Mount VM has been removed from the vCenter Server inventory.

    ```
Trail Map: 

The Rubrik cluster sets the protection state of the Live Mount recovered virtual machine to Do Not Protect. To protect the new virtual machine, add it to an SLA Domain, or remove the individual assignment of Do Not Protect to permit it to inherit protection.
```



Live Mount can be used to near-instantly instantiate identical environments in moments in isolated or test environments. You can also test an application upgrade, failure scenario, or other use cases using your backup storage. When you are done, you simply throw it away.