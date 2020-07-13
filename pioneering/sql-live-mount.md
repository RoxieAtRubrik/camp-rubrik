# SQL Live Mount

SQL Live Mount creates a new database from a point-in-time copy of the source database. The Rubrik cluster presents an SMB share of the new database directly from the Rubrik cluster storage layer. Using Live Mount to access a copy of a database can significantly reduce the RTO for the database, especially for granular level recovery. 	

A Live Mount database can be attached to an SQL Server instance on any Windows Server host that is running the Rubrik Backup Service. Transmissions between the Rubrik cluster and the host of the Live Mount are secured by end-to-end encryption.	

Use Live Mount functionality to create a new database from a point-in-time copy of a source database:

1. On the left-side menu, click **Servers & Apps** > **SQL Server DBs**.  The Hosts/Instances window appears

![alt_text](images/image62.png "image_tooltip")

2. Click **All** **DBs**. The **All DBs** window appears.

![alt_text](images/image63.png "image_tooltip")

3. In the **Name** column, select the `AdventureWorks` database. Alternatively, enter `AdventureWorks` in the search field or use the filters at the top left of the list. 

![alt_text](images/image64.png "image_tooltip")

4.  The **Local** page for the database appears; on the right hand side, the **Recovery Points** pane displays the **Month** view.
5. On the **Recovery Points** pane, select a day that has a green dot. The green dot indicates that at least one successful snapshot was created on that day.

![alt_text](images/image65.png "image_tooltip")

<table>
  <tr>
   <td><strong>Trail Map:</strong>

While Rubrik always sends incremental backups of SQL Server databases, the green dot indicates the synthetically created Full to match the assigned policy. The points in time between fulls are offered for databases in Full Recovery mode using automatically rolling transaction logs. Restoring to a Full (blue dot) will be somewhat faster than choosing a point in time in between Fulls due to the time savings of not rolling transaction logs.
   </td>
  </tr>
</table>

6. The **Recovery Points** card displays the **Day** view for the selected calendar date. Move the Recovery point slider to select a recovery point.

![alt_text](images/image66.png "image_tooltip")

   To select a recovery point other than a snapshot time, move the slider to choose that time. The time appears in the time field and the selected time icon changes. Alternatively, type a specific time into the time field.

7. Open the ellipsis (`...`) menu and select **Mount**. 

The Mount Database dialog box appears.

8. In **Name**, select a Windows Server host, and click **Next**. You will automatically see all SQL Servers with the Rubrik connector installed. Alternatively, enter the name of a host in the search field.

![alt_text](images/image67.png "image_tooltip")

9. In **Name**, select a SQL Server instance. Alternatively, enter the name of an instance in the search field.
10. In **Live Mount Database Name**, type a unique name.

![alt_text](images/image68.png "image_tooltip")

11. Click **Mount**.						

   The Rubrik cluster shares the Live Mount over the SMB/CIFS protocol and automatically sets the protection state of the new database to **Do Not Protect**. This ensures the Rubrik cluster does not backup data stored on itself. The Rubrik cluster then mounts the share to the specified Windows Server host and attaches the Live Mount database to the specified SQL Server instance.

12.  On the left-side menu of the web UI, click **Live Mounts** > **SQL Server DBs**. The SQL Server DB Live Mounts page appears. Wait until the **Status** changes to **Available**. This may take approximately one minute. 

![alt_text](images/image69.png "image_tooltip")

13. On the desktop of Jump1, you will find a Remote Desktop icon labeled SQLServer. Double-click on the icon to open it. 

![alt_text](images/image70.png "image_tooltip")

14. Open Microsoft SQL Server Management Studio by clicking the icon on the bottom menu.

![alt_text](images/image71.png "image_tooltip")

15. Click **Connect **at the login prompt. 

![alt_text](images/image72.png "image_tooltip")

16. In the left-hand column, expand the **Instance name** > **Databases**. The Live Mounted Database should be listed.

![alt_text](images/image73.png "image_tooltip")

17. Minimize the SQL Server RDP window and return to the Rubrik UI tab. 
18. On the SQL Server DB Live Mounts page and open the ellipsis (**<code>...</code></strong>) menu next to the entry for your Live Mount database and select <strong>Unmount</strong>. A confirmation message appears.

![alt_text](images/image74.png "image_tooltip")

19. Click **Unmount **once more to confirm. The Rubrik cluster detaches the database from the SQL Server instance and unmounts the share from the Windows Server host.