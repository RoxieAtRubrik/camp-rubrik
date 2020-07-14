# SQL Live Mount

SQL Live Mount creates a new database from a point-in-time copy of the source database. The Rubrik cluster presents an SMB share of the new database directly from the Rubrik cluster storage layer. Using Live Mount to access a copy of a database can significantly reduce the RTO for the database, especially for granular level recovery.

A Live Mount database can be attached to an SQL Server instance on any Windows Server host that is running the Rubrik Backup Service. Transmissions between the Rubrik cluster and the host of the Live Mount are secured by end-to-end encryption.

Use Live Mount functionality to create a new database from a point-in-time copy of a source database:

1. On the left-side menu, click **Servers & Apps** &gt; **SQL Server DBs**.  The Hosts/Instances window appears

![](https://lh3.googleusercontent.com/ehYh_cB_8PyI7hh57CYnAGLqY3XD00-VhWox0kUpMd9hfnnMVaGFcBvqNN1FfM_KHiy4BAwj-mzMr6YcuIxHQJfBgnKhG8f6Rvq-5k40WXAl1SGYCQWm5oitnjT2ZC9YOI2YF9ST)

1. Click **All** **DBs**. The **All DBs** window appears.

![](https://lh3.googleusercontent.com/H6tfwUlyBpj5bi3DXXkIMwwdA1h5_vr2H5q3nTX0_a_9zzrqy0p2b8FAatebVLYO3P0cFffFbgJMbbyE_xNdKncZZtKzYDQ-JeVcgXOMgLyN9iSqOo8FEDJNPGt0bcIwj46sKk4H)

1. In the **Name** column, select the `AdventureWorks` database. Alternatively, enter `AdventureWorks` in the search field or use the filters at the top left of the list. 

![](https://lh5.googleusercontent.com/97I9oAVZrrey0JqXEgWKESuus5CnrgkBpMl_7CbVMu3jK9R1K0c2Md8HPAZXntrhNt0TBMJz9ASf_kY1WrSUoOmCnTuWvWsF_nTVV9RoGnVb-xPh3fqDWV3gbyzGb8L01ZiEb9EG)

1. The **Local** page for the database appears; on the right hand side, the **Recovery Points** pane displays the **Month** view.
2. On the **Recovery Points** pane, select a day that has a green dot. The green dot indicates that at least one successful snapshot was created on that day.

![](https://lh6.googleusercontent.com/gaETSqgNDFG5rr-Y1SNWWneewYL5TwR8GTQFQZ3o7Q8y8zKuF7PtnH8tbtsleKLNFhs3i6f6vuWc72FwJ_ylScJP1LsM4T9v4MXSKL4ojVL2A5bCr_haCD31u9vfSarM9fWQXH5Z)

{% hint style="info" %}
**Trail Map:** While Rubrik always sends incremental backups of SQL Server databases, the green dot indicates the synthetically created Full to match the assigned policy. The points in time between fulls are offered for databases in Full Recovery mode using automatically rolling transaction logs. Restoring to a Full \(blue dot\) will be somewhat faster than choosing a point in time in between Fulls due to the time savings of not rolling transaction logs.
{% endhint %}

1. The **Recovery Points** card displays the **Day** view for the selected calendar date. Move the Recovery point slider to select a recovery point.

![](https://lh5.googleusercontent.com/hlGLTBgOoeogNDB7LgNDqLHqP74ZR7m3t1iYLCeVDBhAk11Pa2rGu_qtfdfcyaCb0Ua5cw_VDU5o0oahjeggHb3BDoiqt35_CaKTAS17J3Etp0npKvzsNa73GFcpbW68fZPHLcys)

To select a recovery point other than a snapshot time, move the slider to choose that time. The time appears in the time field and the selected time icon changes. Alternatively, type a specific time into the time field.

1. Open the ellipsis \(`...`\) menu and select **Mount**. 

The Mount Database dialog box appears.

1. In **Name**, select a Windows Server host, and click **Next**. You will automatically see all SQL Servers with the Rubrik connector installed. Alternatively, enter the name of a host in the search field.

![](https://lh3.googleusercontent.com/DYtED478atDWCzyFjKfqHqQGTH8ftDP8Ri5NhuHsNHiuvdLVMEdSJNmIYlQbhj_HQsHkZh2hUbKc0j0AmHeQNK4vv9RlWAucg9bC0fX9FeluS7bCNhwQ8T6jKGH4Yin81ShSfEdy)

1. In **Name**, select a SQL Server instance. Alternatively, enter the name of an instance in the search field.
2. In **Live Mount Database Name**, type a unique name.

![](https://lh6.googleusercontent.com/y4ufJpgG3iS6L9_ItYyEBN5yUsp12sX_fs-5vVPC5eUYlCs464lDvYQr39lzbiM9xxPcGhiIJdqHAkK8riB2hgDdICXmjc6FOsLKJ4Pz7GC8sjdwh8O17T4hnoEUv9ozouZ0KXpz)

1. Click **Mount**.

   The Rubrik cluster shares the Live Mount over the SMB/CIFS protocol and automatically sets the protection state of the new database to **Do Not Protect**. This ensures the Rubrik cluster does not backup data stored on itself. The Rubrik cluster then mounts the share to the specified Windows Server host and attaches the Live Mount database to the specified SQL Server instance.

2. On the left-side menu of the web UI, click **Live Mounts** &gt; **SQL Server DBs**. The SQL Server DB Live Mounts page appears. Wait until the **Status** changes to **Available**. This may take approximately one minute.

![](https://lh6.googleusercontent.com/K_MSwq0KSQE72exCFNw49IYzTm1CUrzQsWBOi4YXK5Jd0lPP3M2xZtKqH5RnXxNxcccWsKOjrK-k-d5TMK2BIA2MAc-NUGuYl93HKvII5ZEj8EWfOBUTzTKeNLLnoCeZHpCSFFSb)

1. On the desktop of Jump1, you will find a Remote Desktop icon labeled **SQLServer**. Double-click on the icon to open it. 

![](https://lh5.googleusercontent.com/Cs5Y57bzujJJ90fUvPQpPD0jS_VV57iD8Zbj3psmpFZyW9gd1hCARa_dSTBWcRKHzInDRa6exp3UmGKIueONZKwfcylhaBz6DbbAJ_KTROfaEhkD1Mo1TxzDDE61kMnLiQwE7gxU)

1. Open Microsoft SQL Server Management Studio by clicking the icon on the bottom menu.

![](https://lh4.googleusercontent.com/ypO-DejBOBnAS062Ybo2D6-EM5haxttLnk5AJ7W9_j8EcR1BCS5anoF7EZQ-ngGps1GNTGlJMiP_s8J6ua_RS0_6fY5-ZDu_k1JQgrXJi6w1KQ1LG7gLxFD-FyimnZKWT4i5Cv8B)

1. Click **Connect** at the login prompt. 

![](https://lh6.googleusercontent.com/fUt1tDjCh1f7tZaBalKOABfz-9bgME5CVF0v3yc_tSIXVYi9W5XRM3-ry_RLMZdUUtXOw3b1XAn6-_yRmBO6um5YqCqxm9FHuLVEuJ1HS5fbArKr9xOVkePvpmVqDOlq0sy0hpOk)

1. In the left-hand column, expand the **Instance name** &gt; **Databases**. The Live Mounted Database should be listed.

![](https://lh4.googleusercontent.com/zrBKIBLoZFSrWImdcLwWvA-4yAJ4-rTWVj_RWRtuVkJDv8t7L6sAGlV2FqtQHWOyNarejidGcJs1zf2BhH_IrcGa4J_Ex9pw93i8rFkP8MWfl1uk8KuvyrBQUQ3wlJeDvSPTDQbA)

1. Minimize the SQL Server RDP window and return to the Rubrik UI tab. 
2. On the SQL Server DB Live Mounts page and open the ellipsis \(`...`\) menu next to the entry for your Live Mount database and select **Unmount**. A confirmation message appears.

![](https://lh4.googleusercontent.com/Hj4Pvqsz0TcZ1d0CAGdgzT0HATBawJRUeTsZTrPe3jTKzme-BxRQzkD2a4OYacS0CRUepWmxzFbn78_GuXjPLgQhWZauwKf6TtWXBD5LVoAWyYiOHLHbZ3YG0TisY99XMUZX2Rkn)

1. Click **Unmount** once more to confirm. The Rubrik cluster detaches the database from the SQL Server instance and unmounts the share from the Windows Server host.

