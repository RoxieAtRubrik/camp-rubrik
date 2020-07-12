# Adding a Cloud Archive Location

Using Amazon S3 as an example, let’s walk through adding an archive location:					 							



1. Click on the gear icon located on the top right bar of the web UI.

The Settings menu appears.



<p id="gdcalert75" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image75.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert76">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image75.png "image_tooltip")


	 							



2. From the **Settings** menu, select **Archival Locations**.					

The Archival Locations page appears.



3. Click the blue **+** icon.							

The Add Archival Location dialog box appears.



<p id="gdcalert76" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image76.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert77">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image76.png "image_tooltip")




4. In **Archival Type**, select **Amazon S3**.

	The Amazon S3 archival location fields appear.



<p id="gdcalert77" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image77.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert78">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image77.png "image_tooltip")



    Review the different inputs required for Amazon S3 as an archive. Feel free to browse other archive types to view required settings. 



5. Press **Cancel** when finished.

		 	 	 			



1. On the left pane of the web UI, select **SLA Domains** > **Local Domains**. The Local SLA Domains page appears.
2. Select the Camp Rubrik SLA Domain that you previously created. The SLA Domain page will load. 
3. Click the ellipses (**<code>...</code></strong>) at the top right corner of the SLA Domain page. Select <strong>Edit</strong>.				 							
4. Click <strong>Configure Remote Settings</strong> at the bottom of the dialog (depending on the resolution of your screen it may be necessary to scroll down).					 							
5. In Archival, click the toggle (if not already done). Notice the <strong>Enable Instant Archive</strong> option. Do not select it at this time although you can click the circled “<code>i</code>” to read what it does.



<p id="gdcalert78" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image78.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert79">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image78.png "image_tooltip")



    The Instant Archive feature can be enabled to instruct a Rubrik cluster to immediately queue a task to copy a new snapshot to a specified archival location. 



6. Press **Cancel**.