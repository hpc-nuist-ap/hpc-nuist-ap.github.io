---
title: "Account Resource Limits"
weight: 15
---

The following information outlines the usage limits for specific HPC account types.

### Compute Hour Limits

Time on the Linux computing resource is allocated in **core hours**.

{{% notice note %}}
core hours = nodes \* cores \* hours
{{% /notice %}}

For example, the use of 1 nodes with 24 CPU cores for three hours is counted as 72 core hours. Most of the HPC compute nodes have 24 CPU cores so if you are unsure of how many cores you are using per node, 24 is a good estimate.

### Concurrent Job Limits

In general, jobs will be scheduled and run on a first-come, first-served basis within a partition, provided that adequate resources are available. To maximize the use of computing resources, HPC management, in consultation with the HPC allocation committee, may restrict the number of jobs you can run concurrently from a given account.

### General Partition Rules

| Partition Name | Maximum Jobs Queued | Maximum Node Count | Maximum Wall Time | Maximum Jobs per User |
| :--------------: | :-----------------: | :----------------: | :---------------: | --------------------- |
| low            |                  |       |                  |                       |
| high |  |  |  | |
| Addnode |  |  |  | |
| zhao |  |  |  | |

### Disk Space

| Root of home directory | Quota |
| ---------------------- | ----- |
| `/pulic/home`          | 300 G |
| `/public1/home`        | 1.5 T |
| `/datadir1`            | 2.5 T |

{{% notice note %}}
Please check the home directory by `echo $HOME` and check used disk space by `du -sh $HOME`.
{{% /notice %}}

{{% notice warning %}}
 If used space is larger than quota, you couldn't store files anymore and need to delete some files.
{{% /notice %}}