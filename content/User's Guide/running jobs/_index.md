---
title: "Running Jobs"
weight: 30
---

To run a job on the HPC cluster, you will need to set up a **Portable Batch System (PBS) file**.

This PBS file defines the commands and cluster resources used for the job. 

A PBS file is a simple text file that can be easily edited with a UNIX editor, such as vi, pico, or emacs.

{{% notice warning %}}
Any high-cpu process in foreground/background will be killed. The user will be deleted after warned twice.
{{% /notice %}}