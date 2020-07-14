# Create an SLA Domain

To create an SLA Domain:

1. On the left-hand navigation pane, select **SLA Domains &gt; Local Domains**.

{% hint style="info" %}
**Trail Map:** Local Domain - an SLA Domain that is created on the local Rubrik cluster. Remote Domain - an SLA Domain that was created on a Rubrik cluster other than the local Rubrik cluster. Remote SLA Domains appear on a local Rubrik cluster when the local Rubrik cluster is a replication target.
{% endhint %}

1. In the upper right-hand corner, click the blue **+** icon.

![](https://lh4.googleusercontent.com/3sUakfW2pyi4sbK7jPO6I5gx2FOVMMtNtVwntVkJWxYsxFMfgvPqy1ICKerrOi-Ejbbjut692cfmizq_zTsviRh8f2dJz0IgEMI7iJI_WXiGCBmW13ZjJxJWPc3Rgl2vN0Hmm4zH)

1. Create an SLA Policy using the same configuration values demonstrated in the following image:



![](https://lh3.googleusercontent.com/xe-wwKgu_0bZ_E6LWHaJujIzuKqY1oO1eXvPQZymusbKEM8GkbYJ2i73aLj01Fk65mxOlDPTqBAbboN-M6zIoqIaqxZ9-4tnix-aR6GIJQMxx9zbCMiX0Aio8K-zNTWjry-v5nbA)

{% hint style="info" %}
**Trail Map:** Continuous Data Protection enables you to protect your high value applications, running on vSphere, with near-zero RPOs. With CDP, you can recover from local or remote points in time with near zero RPOs for recovery from the latest point in time, or per-second granularity for recovery from historical points in time.
{% endhint %}

1. Select **Next** to configure replication and archive in the Remote Settings portion of the SLA Domain.

![](https://lh5.googleusercontent.com/udhjYv2gNfPjQR-9f-8Eq1FIt3DTFHyFmQCs6Nyqf822H68Pcvj0L92gdY9n-4QZthF7TkHHzD3aDryuELSZG3jBtkdGeTFK90rTsFPJshL9G7q8YUs_s0JyQ96J_xlULj8fK_fS)

1. Enable the **Archival** toggle and select `NFS:myarchive` from the dropdown box. Change **Retention On Brik** as 60 days. Note that the arrow keys can be used to fine-tune the amount of time specified. Press the **Next** button.

![](https://lh5.googleusercontent.com/m--dYrP3FukQSOFILFpMC3prYCgLzEA4R6aYCLyG5pLnaQPI6eosoQ8QKteiXLmsFSp0Lc9jCwKa_oA60PO5MWUg2djKgDZWZKtxEAdPkhr_Cq6QGciZyBBm21N5euN0l8b2gRk4)

1. Review and then click **Create** to finish.

