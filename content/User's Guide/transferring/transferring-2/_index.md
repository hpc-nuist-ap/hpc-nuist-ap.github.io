---
title: "CLI"
weight: 15
description: "Command line interface (Windows / Linux / OS X / Unix)"
---

The two most common tools you can use for data transfers over SSH:

- `scp`: for the full transfer of files and directories (only works fine for single files or directories of small/trivial size)

- `rsync`: a software application which synchronizes files and directories from one location to another while minimizing data transfer as only the outdated or inexistent elements are transferred (practically required for lengthy complex transfers, which are more likely to be interrupted in the middle).

Of both, normally the second approach should be preferred, as more generic; note that, both ensure a secure transfer of the data, within an encrypted tunnel.

{{% notice note %}}
Please check these two excellent tutorials: [scp_tutorial](https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/) and [rsync_tutorial](https://linuxize.com/post/how-to-use-rsync-for-local-and-remote-data-transfer-and-synchronization/).
{{% /notice %}}