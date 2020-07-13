# Dashboard Walkthrough

Rubrik’s simple user interface is built on a API-driven framework with a HTML5 web user interface. To see it for yourself:

1. Once you have accessed the Camp Rubrik lab environment, select the **Jump1** Host and authenticate using the following OS credentials:

    * Username: `demo@rubrik.lab`
    * Password: `Welcome10!`

2. Open up the web browser (Chrome) and select the shortcut for the Rubrik UI. Login using the following credentials:

    * Username: `admin`
    * Password: `Welcome10!Rubrik`

![alt_text](images/image2.png "image_tooltip")

3. Once authenticated, the Rubrik UI will default to the **Dashboard** page.

![alt_text](images/image3.png "image_tooltip")

4. Let’s explore the various Dashboard panes.

   The **vSphere VMs** pane provides a high-level overview of how many vSphere objects are protected by an SLA Domain.

   Click on **vSphere VMs** to display the dropdown box that allows you to view a protection overview by workload type.

![alt_text](images/image4.png "image_tooltip")

5. **SLA Domains** provides an overview of each SLA Domain and how many objects are being protected.

![alt_text](images/image5.png "image_tooltip")

6. ** Activity** pane lists all currently and recently completed tasks.

![alt_text](images/image6.png "image_tooltip")

7. Towards the middle of the Dashboard screen, you can see the number of active **Live Mounts** as well as the number of **Incoming Snapshots**.

![alt_text](images/image7.png "image_tooltip")

   At the bottom, you are able to get a quick peek at the number of snapshots residing on this Rubrik cluster, percent data reduction using deduplication and compression, and amount of data archived.

![alt_text](images/image8.png "image_tooltip")

8. Looking at the bottom left of the Dashboard, select **See More** in the **System** pane. This section details the specs of the Rubrik cluster as well as some performance details.

![alt_text](images/image9.png "image_tooltip")