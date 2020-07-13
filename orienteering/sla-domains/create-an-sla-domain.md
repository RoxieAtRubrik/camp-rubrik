# Create an SLA Domain

To create an SLA Domain:

1. On the left-hand navigation pane, select **SLA Domains > Local Domains**.

```
Trail Map:

Local Domain - an SLA Domain that is created on the local Rubrik cluster.

Remote Domain - an SLA Domain that was created on a Rubrik cluster other than the local Rubrik cluster. Remote SLA Domains appear on a local Rubrik cluster when the local Rubrik cluster is a replication target.
```

2. In the upper right-hand corner, click the blue **+** icon.

![alt_text](images/image10.png "image_tooltip")

3. Create an SLA Policy using the same configuration values demonstrated in the following image:

![alt_text](images/image11.png "image_tooltip")

```
Trail Map:

Continuous Data Protection enables you to protect your high value applications, running on vSphere, with near-zero RPOs.

With CDP, you can recover from local or remote points in time with near zero RPOs for recovery from the latest point in time, or per-second granularity for recovery from historical points in time.
```

4. Select **Next** to configure replication and archive in the Remote Settings portion of the SLA Domain.

![alt_text](images/image12.png "image_tooltip")

5. Enable the **Archival** toggle and select `NFS:myarchive` from the dropdown box. Change **Retention On Brik** as 60 days. Note that the arrow keys can be used to fine-tune the amount of time specified. Press the **Next** button.

![alt_text](images/image13.png "image_tooltip")

6. Review and then click **Create** to finish.