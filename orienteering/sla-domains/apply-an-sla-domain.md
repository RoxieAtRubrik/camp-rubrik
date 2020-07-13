# Apply an SLA Domain

An SLA Domain may be applied at a broad level - such as the management server (e.g. vCenter Server), folder, host, cluster, or tag. This enables newly provisioned workloads to automatically inherit protection from a higher level resource. Alternatively, an SLA Domain may be granularly applied per object to achieve specific data protection objectives.

To do so:

1. In the web UI, on the left-side menu, click **Virtual Machines** > **vSphere VMs**. The vSphere VMs page appears, with the VMs tab selected.

2. Select **Clusters/Hosts**. The Clusters/Hosts tab appears.

<p id="gdcalert14" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image14.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert15">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

![alt_text](images/image14.png "image_tooltip")

3. Select the checkbox in front of the vCenter Server.

    Notice that the **Manage Protection** button in the upper right-hand corner illuminates and is now clickable. Do not assign an SLA Domain at this time.

<p id="gdcalert15" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image15.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert16">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image15.png "image_tooltip")

To place a granular policy on an individual object:

4. Select the **VMs** tab. The **VMs** page appears. Search for your Linux virtual machine running on vSphere.  Type in `ubuntu` in the **Search by Name** field to locate the assigned Linux VM (`ubuntu14-vm1`).

<p id="gdcalert16" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image16.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert17">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

![alt_text](images/image16.png "image_tooltip")

5. Select the Ubuntu virtual machine and click **Manage Protection**. 
6. Find and select the previously created `Camp Rubrik` SLA Domain and press **Next**.

<p id="gdcalert17" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image17.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert18">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

![alt_text](images/image17.png "image_tooltip")

7. Review the retention change caused by changing the SLA Domain.

<p id="gdcalert18" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image18.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert19">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

![alt_text](images/image18.png "image_tooltip")

8. Click **Submit**.

   The VM will soon update to reflect it is protected by the selected SLA Domain.

You have now completed the Orienteering badge!