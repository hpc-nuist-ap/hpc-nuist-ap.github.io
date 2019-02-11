---
title: "Persisting ENVs"
weight: 25
---

To persist ENVs, just put the commands in one of three [config files](https://hpc-nuist-ap.github.io/users-guide/environment-variables/config-files/) mentioned before, as these files will be executed when ever you access a shell.

Please check the [template](https://www.stefaanlippens.net/my_bashrc_aliases_profile_and_other_stuff/) written by Stefaan Lippens, especially the `.profile` part.

{{% notice note %}}

`$PATH` and `$LD_LIBRARY_PATH` are the most important for compiling models.<br>Please check these two tutorials in detail: [PATH_tutorial](https://www.tecmint.com/set-path-variable-linux-permanently/) and [LD_LIBRARY_PATH_tutorial](https://www.hpc.dtu.dk/?page_id=1180).

{{% /notice %}}