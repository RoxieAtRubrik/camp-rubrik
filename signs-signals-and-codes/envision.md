# Envision

Rubrik Envision provides customizable data protection reports with valuable information from the Rubrik cluster. Envision gives insight into historical information based on Protection Tasks, SLA Compliance, and System Capacity.

You can explore Envision in two formats:



*   Reports Summary
*   Reports Gallery

In the **Reports Summary** you can view or create individual reports in the Daily Protection Tasks by Status, SLA Compliance, Local Snapshot Storage, System Capacity, or Weekly Protection Tasks by SLA Domain sections. Let’s explore that section:



1. In the Rubrik UI, in the left-hand pane, select **Reports** > **Summary**. 

The Protection Tasks Details page appears.



<p id="gdcalert87" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image87.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert88">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image87.png "image_tooltip")




2. Scroll down to **System Capacity** and you will notice: On Brik, Available Storage, Archived, Average Daily Growth, Across All Replicas, and Estimated Runway.

    One of the most critical details here is the **Estimated Runway** that reports the estimated number of days remaining before additional data storage space is required on the Rubrik cluster. This is a critical metric to have available on any system that leverages data reduction combining incremental forever, deduplication, and compression.




<p id="gdcalert88" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image88.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert89">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image88.png "image_tooltip")




3. Scroll back up to **Daily Protection Tasks by Status** and click **View Report**.



<p id="gdcalert89" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image89.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert90">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image89.png "image_tooltip")




4. The **Protection Tasks Details** page appears. Scroll down to where you can **Search by Object Name** and supply dynamic filters.
5. Type** <code>win</code></strong> to search for all objects that have been protected with the word <strong><code>win</code></strong> in it.



<p id="gdcalert90" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image90.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert91">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image90.png "image_tooltip")




6. Now select **Filter SLA Domain** and select the Gold SLA Domain to view.



<p id="gdcalert91" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image91.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert92">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image91.png "image_tooltip")




7. Now click **Gallery **on the left-side menu under Reports and the Reports Gallery appears.
8. Click the **Create Report** button in the right-side top corner. 



<p id="gdcalert92" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image92.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert93">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image92.png "image_tooltip")




9. The Create Report dialog appears where you can create your own Custom Report.

    Name the report **Example Report **and select **Protection Tasks Details** as the Report Template.




<p id="gdcalert93" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image93.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert94">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image93.png "image_tooltip")


	



10. There are several different combinations of reports that you can create to provide you with useful information such as:
*   Data Reduction Summary - Last 30 Days
*   Average Job Durations - Last 7 Days
*   System Capacity by Object Type - Last 30 Days
*   Daily Backup Administrator Report (You will create this one)
*   Daily DBA Report
11. Select the following items to create a Daily Backup Administrator Report. You will need to click Next to get to each new report.

<table>
  <tr>
   <td>
<strong>Report Type</strong>
   </td>
   <td><strong>Created from "Protection Tasks Details"</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Top Left Chart</strong>
   </td>
   <td><strong>Daily Protection Tasks by Status</strong>
   </td>
  </tr>
  <tr>
   <td>Attributes
   </td>
   <td>Task Type
   </td>
  </tr>
  <tr>
   <td>Measures
   </td>
   <td>Task Count by Status
   </td>
  </tr>
  <tr>
   <td>Chart Type
   </td>
   <td>Stacked Horizontal
   </td>
  </tr>
  <tr>
   <td><strong>Top Right Chart</strong>
   </td>
   <td><strong>Daily Failed Tasks by Object Name</strong>
   </td>
  </tr>
  <tr>
   <td>Attributes
   </td>
   <td>Object Name
   </td>
  </tr>
  <tr>
   <td>Measures
   </td>
   <td>Failed Tasks
   </td>
  </tr>
  <tr>
   <td>Chart Type
   </td>
   <td>Vertical
   </td>
  </tr>
  <tr>
   <td><strong>Table</strong>
   </td>
   <td><strong>Protection Tasks Details</strong>
   </td>
  </tr>
  <tr>
   <td>Search by Attribute
   </td>
   <td>SLA Domain, Task Status, Task Type, Location, Object Name, Object Type
   </td>
  </tr>
  <tr>
   <td>Search by Measure
   </td>
   <td>Start Time, End Time, Duration, Data Transferred, Data Stored, Dedup Ratio, Logical Dedup Ratio
   </td>
  </tr>
  <tr>
   <td><strong>Filter</strong>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Date
   </td>
   <td>Past 24 hours
   </td>
  </tr>
  <tr>
   <td>Task Status, Task Type, SLA Domain, Object Type, Object Name, Location, Cluster Location
   </td>
   <td>none
   </td>
  </tr>
</table>




12. Observe the report once it has been generated (note that it could take a few moments to generate).